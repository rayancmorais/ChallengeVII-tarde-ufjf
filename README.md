# 💰 Codi Cash - Financial Management System

## 🎯 Project Objective

**Codi Cash** is a financial management software developed to facilitate the control of finances for each unit of the **Codi Academy**. This system allows for the registration, viewing, and management of **sales, expenses, and key financial indicators (KPIs)** through a modern, responsive, and intuitive web interface.

This project was developed as part of a **Challenge**, with an exclusive focus on the **frontend** development of the application, ensuring an optimized user experience and a clean, modular code architecture.

---

## 🚀 Challenge Scope (Frontend)

The challenge consisted of developing the complete and functional interface of the system, using modern technologies and ensuring:

* Responsive interfaces for various devices (**mobile first** approach).
* High usability and intuitive navigation.
* Componentization and code reuse for scalability and maintenance.
* Clean and organized project structure.

---

## ✨ Required Functionality

### 1. Main Dashboard

* **Monthly Summaries**: Clear display of revenue, expenses, and balance for the period.
* **Interactive Charts**: Bar/line charts to visualize financial data across different periods (week, month, year).
* **KPI Cards**: Visual cards with key performance indicators like Total Sales, Total Expenses, and Net Balance.

### 2. Sales Module

* **Registration Form**:
    * Course type (online or in-person).
    * Customer data (name, email, phone).
    * Gross sales value.
    * Applied discounts.
    * Taxes, commissions, and card fees.
    * **Automatic calculation** of the Final Sales Value.
* **Sales List**: Visualization of all registered sales, with filters by period and course type.

### 3. Expenses Module (Gastos)

* **Expense Registration**:
    * **Fixed**: Electricity, water, rent, internet, payroll, transportation vouchers, payroll tax.
    * **Variable**: Maintenance, supplies, etc.
* **Entry Management**: Editing and deletion of expenses.
* **Expense History**: Detailed visualization of all registered expenses.

### 4. Advanced Visualizations and Charts

* **Comparative Chart**: Revenue vs. Expenses over time.
* **Pie Chart**: Distribution of expenses by category.
* **Dynamic Filters**: By time range and category.

### 5. User Experience (UX)

* Responsive layout (desktop, tablet, mobile).
* Clear and easy navigation.
* Visual feedback (success and error messages).
* Modals for confirmations and forms.

---

## 🛠️ Technical Requirements

* **HTML5, CSS3, and JavaScript**.
* **TailwindCSS**.
* **ReactJS** with a **mobile first** approach.
* Modular structure with reusable components.

---

## ✅ Evaluation Criteria

* Responsive and functional interface.
* Good code organization.
* Component reuse.
* Alignment with requirements.
* Final presentation.

---

## 📦 Deliverables

* GitHub Repository.
* Deployment link (Vercel, Netlify, etc).
* Documentation for local setup.
* Frontend documentation.
* Project presentation.

### CHALLENGEVII-TARDE-UFJF

---

## 1. 🎨 Figma Prototypes

The project's visual design was initially structured in Figma by the group, serving as the basis for developing the system's interface.

* 🔗 [View Mobile Prototype](https://www.figma.com/proto/GqZUatYhyc7vB4leHz24uO/CodiAcademy--Copy-?page-id=2612%3A9344&node-id=2612-9353&p=f&viewport=115%2C266%2C0.16&t=Dd2gEp0czH9oICpj-1&scaling=scale-down&content-scaling=fixed&starting-point-node-id=2612%3A9353&show-proto-sidebar=1)
* 🔗 [View Desktop Prototype](https://www.figma.com/proto/GqZUatYhyc7vB4leHz24uO/CodiAcademy--Copy-?page-id=618%3A11050&node-id=654-29657&p=f&viewport=309%2C338%2C0.05&t=U968KR5HwadZvLsa-1&scaling=scale-down&content-scaling=fixed&starting-point-node-id=654%3A29584&show-proto-sidebar=1)

---

## 2. 🗂️ Project Structure and Organization

Below is an overview of the project's main folders, their responsibilities, and examples of their contents:

| Folder | Description | Examples/Main Content |
| :--- | :--- | :--- |
| `assets/` | Static images, logos, and icons used in the interface. | Codi Academy Logo |
| `components/` | Reusable React components used throughout the application. | Header, Modal, Sidebar |
| `contexts/` | React Contexts for global state management and shared logic. | HeaderContext for header title and actions |
| `features/` | Page-specific components, isolated to prevent impact on the rest of the system. | Unique components for specific functionalities |
| `hooks/` | Custom hooks for reusable logic, such as detection of device and data manipulation. | `useFinancialMetrics`, `useIsMobile`, `useLocalStorageData` |
| `layouts/` | Main layouts that structure the navigation and visual arrangement of the pages. | `MainLayout` with responsive sidebar |
| `libs/` | Utility functions used globally for common operations and helpers. | `cn` function for CSS class manipulation with Tailwind |
| `pages/` | Application pages that correspond to routes. | Dashboard, Sales, Expenses |
| `services/` | Modules for data manipulation logic and integration with external APIs. | Data aggregation for charts |
| `types/` | TypeScript definitions and interfaces to ensure consistent and safe typing. | `Sale`, `Expense` Interfaces |
| `utils/` | Utility functions for formatting, financial calculations, and data manipulation. | Calculation of IRR, Payback, date and currency formatting |

### Modular Organization and Benefits

This modular structure allows for:

* Reuse and isolation of components to facilitate maintenance.
* Clear separation between logic, visual presentation, and data.
* Project scalability, with easy addition of new functionalities.
* More readable and organized code, benefiting collaborative work.

---

## 🚀 Quick Guide: Adding Test Data

This step is for quickly inserting simulated data into the system, allowing you to test and visualize the charts and tables with real information in a practical way, without the need to enter everything manually.

### 3. Add Simulated Sales

```javascript
const nomes = ["João Silva", "Maria Oliveira", "Carlos Santos", "Ana Souza", "Pedro Lima", "Juliana Costa", "Lucas Rocha", "Fernanda Alves", "Rafael Martins", "Camila Ribeiro"];
const cursos = ["online", "presencial"];
const vendasSimuladas = [];

for (let i = 0; i < 50; i++) {
    const ano = 2023 + Math.floor(Math.random() * 3); // 2023, 2024, 2025
    const mes = String(1 + Math.floor(Math.random() * 12)).padStart(2, "0");
    const dia = String(1 + Math.floor(Math.random() * 28)).padStart(2, "0");

    const data = `${ano}-${mes}-${dia}`;
    const tipoCurso = cursos[Math.floor(Math.random() * cursos.length)];
    const nomeCliente = nomes[Math.floor(Math.random() * nomes.length)];
    const email = nomeCliente.toLowerCase().replace(" ", ".") + "@example.com";
    const telefone = `(11) 9${Math.floor(1000 + Math.random() * 9000)}-${Math.floor(1000 + Math.random() * 9000)}`;

    const valorBruto = Math.floor(800 + Math.random() * 2200); // between R$800 and R$3000
    const desconto = Math.floor(Math.random() * 200);
    const imposto = Math.floor(valorBruto * 0.1); // 10%
    const comissao = Math.floor(valorBruto * 0.05); // 5%
    const valorFinal = valorBruto - desconto - imposto - comissao;

    vendasSimuladas.push({
        id: Date.now() + i,
        data,
        tipoCurso,
        nomeCliente,
        email,
        telefone,
        valorBruto,
        desconto,
        imposto,
        comissao,
        valorFinal,
    });
}
localStorage.setItem("vendas", JSON.stringify(vendasSimuladas));
console.log("✅ 50 simulated sales added to localStorage!");
### 4. Adicionar Vendas Simuladas
```javascript
const categorias = [
    "moradia",
    "contas_casa",
    "internet_telefone",
    "impostos_taxas",
    "dividas_emprestimos",
    "folha_pagamento",
    "vale_transporte",
    "imposto_sobre_folha",
    "outros"
];

const tipos = [
    "fixo_essencial",
    "fixo_nao_essencial",
    "variavel_essencial",
    "variavel_nao_essencial",
    "extraordinario",
    "recorrente",
    "unico",
    "outro_tipo"
];

const nomesGasto = [
    "Aluguel",
    "Conta de Luz",
    "Água",
    "Internet",
    "Telefone",
    "IPTU",
    "Empréstimo",
    "Folha de Pagamento",
    "Transporte Funcionários",
    "INSS Patronal",
    "Netflix",
    "Spotify",
    "Compra de Material",
    "Assinatura de Software",
    "Deslocamento",
    "Hospedagem de Site",
    "Compra Equipamento",
    "Reparo de Máquina",
    "Pagamento Freelancer",
    "Outros"
];

const gastosSimulados = [];

// Adiciona investimento inicial
gastosSimulados.push({
    id: 1,
    data: "2023-01-01",
    nome: "Investimento Inicial",
    preco: -10000, // Ajustado para ser negativo, representando uma saída de caixa
    categoria: "investimentos_poupanca",
    tipoDespesa: "investimento"
});

// Adiciona os outros 49 gastos
for (let i = 2; i <= 50; i++) {
    const nome = nomesGasto[Math.floor(Math.random() * nomesGasto.length)];
    const categoria = categorias[Math.floor(Math.random() * categorias.length)];
    const tipoDespesa = tipos[Math.floor(Math.random() * tipos.length)];

    const ano = 2023 + Math.floor(Math.random() * 3);
    const mes = String(Math.floor(Math.random() * 12) + 1).padStart(2, "0");
    const dia = String(Math.floor(Math.random() * 28) + 1).padStart(2, "0");
    const data = `${ano}-${mes}-${dia}`;

    const preco = parseFloat((Math.random() * 1000 + 50).toFixed(2)); // Valor positivo
    const precoComSinal = -preco; // Transformando em negativo para representar despesa

    gastosSimulados.push({
        id: i,
        data,
        nome,
        preco: precoComSinal, // Salva o preço como negativo
        categoria,
        tipoDespesa
    });
}

localStorage.setItem("gastos", JSON.stringify(gastosSimulados));

console.log("✅ Dados de gastos salvos no localStorage, incluindo o investimento inicial.");
```

---

### 4. Add Simulated Expenses

```javascript
const categorias = [
    "moradia",
    "contas_casa",
    "internet_telefone",
    "impostos_taxas",
    "dividas_emprestimos",
    "folha_pagamento",
    "vale_transporte",
    "imposto_sobre_folha",
    "outros"
];
const tipos = [
    "fixo_essencial",
    "fixo_nao_essencial",
    "variavel_essencial",
    "variavel_nao_essencial",
    "extraordinario",
    "recorrente",
    "unico",
    "outro_tipo"
];
const nomesGasto = [
    "Aluguel",
    "Conta de Luz",
    "Água",
    "Internet",
    "Telefone",
    "IPTU",
    "Empréstimo",
    "Folha de Pagamento",
    "Transporte Funcionários",
    "INSS Patronal",
    "Netflix",
    "Spotify",
    "Compra de Material",
    "Assinatura de Software",
    "Deslocamento",
    "Hospedagem de Site",
    "Compra Equipamento",
    "Reparo de Máquina",
    "Pagamento Freelancer",
    "Outros"
];
const gastosSimulados = [];

// Adds initial investment
gastosSimulados.push({
    id: 1,
    data: "2023-01-01",
    nome: "Investimento Inicial",
    preco: -10000, // Adjusted to be negative, representing a cash outflow
    categoria: "investimentos_poupanca",
    tipoDespesa: "investimento"
});

// Adds the other 49 expenses
for (let i = 2; i <= 50; i++) {
    const nome = nomesGasto[Math.floor(Math.random() * nomesGasto.length)];
    const categoria = categorias[Math.floor(Math.random() * categorias.length)];
    const tipoDespesa = tipos[Math.floor(Math.random() * tipos.length)];

    const ano = 2023 + Math.floor(Math.random() * 3);
    const mes = String(Math.floor(Math.random() * 12) + 1).padStart(2, "0");
    const dia = String(Math.floor(Math.random() * 28) + 1).padStart(2, "0");
    const data = `${ano}-${mes}-${dia}`;

    const preco = parseFloat((Math.random() * 1000 + 50).toFixed(2)); // Positive value
    const precoComSinal = -preco; // Transforming to negative to represent an expense

    gastosSimulados.push({
        id: i,
        data,
        nome,
        preco: precoComSinal, // Saves price as negative
        categoria,
        tipoDespesa
    });
}
localStorage.setItem("gastos", JSON.stringify(gastosSimulados));
console.log("✅ Expense data saved to localStorage, including the initial investment.");
```

---

## 5. 🌐 Project Hosting

The project is available online at:

🔗 **https://codi-vercel3-0.vercel.app/**

---

## 6. Understanding the Initial Investment in Expenses

The **“Initial Investment”** item is essential for the **IRR**, **Payback**, and **NPV** metrics to function correctly.

* **IRR** and **Payback** are calculated **per year**; they do not accumulate across multiple years.
* Therefore, to analyze these indicators annually, an **Initial Investment** must be manually added at the start of each year (ideally based on the costs from the previous year).

---

## 7. 📊 Understanding the Financial Metrics

### 7.1 🔢 NPV (Net Present Value)

* Calculates the present value of future cash flows discounted by a rate.
* Used to assess project viability:
    * **NPV > 0**: Project is viable.
    * **NPV < 0**: Project is not viable.
    * **NPV = 0**: Project merely covers costs.
* In Codi Cash, the **Accumulated Net Balance** in the chart visually represents the NPV.

### 7.2 📈 TIR (Internal Rate of Return)

* The discount rate at which the NPV of a project equals zero.
* Represents the project's **profitability** (or rate of return).
* The higher the IRR, the better the investment.

### 7.3 ⏳ Payback

* The time required to **recover the initial investment** from accumulated profits.
* A liquidity indicator: the shorter the time, the quicker the return.
* In the system, it is displayed **in months**.

---

## 8. 💻 How the Project Was Implemented

### 8.1 🧰 Core Technologies

* **React**: UI declarative and efficient.
* **TypeScript**: Static typing for greater robustness.
* **Tailwind CSS**: Fast styling with utility classes.

---

## 9. 📦 Libraries and Tools

### 9.1 🛠️ Production

| Library/Tool | Description |
| :--- | :--- |
| `@heroicons/react`, `lucide-react` | SVG Icons. |
| `@radix-ui/react-*` | Accessible components (modals, tooltips, etc.). |
| `chart.js`, `react-chartjs-2`, `recharts` | Interactive charts. |
| `clsx`, `class-variance-authority`, `tailwind-merge` | Intelligent CSS class management. |
| `financejs` | NPV, IRR, Payback calculations. |
| `moment` | Date manipulation and formatting. |
| `react-router-dom` | SPA routing. |
| `react-datepicker`, `react-icons` | UI utilities. |

### 9.2 ⚙️ Development

| Library/Tool | Description |
| :--- | :--- |
| `eslint`, `prettier` | Linting and formatting. |
| `vite`, `@vitejs/plugin-react` | Modern and fast build tool. |
| `@types/*`, `typescript` | Typings and compilation. |
| `tailwindcss`, `postcss`, `autoprefixer` | CSS styling pipeline. |

---

## 10. ⚠️ Important Note

> 🔍 **Detail about automatic expense data**
> The code automatically inserts an **"Initial Investment"** at the start of the year. This is **fundamental** for calculating **IRR** and **Payback**, as these metrics depend on an **initial negative cash flow**.
>
> ❗ **Current Limitation:**
> The **IRR** and **Payback** metrics currently function only **per year**, and **do not** consider multiple years cumulatively.
>
> ✅ **Recommendation:**
> If you wish to track these indicators annually, **always add** an expense called `Investimento Inicial` at the beginning of each year, based on the costs from the end of the previous year (e.g., December).
>
> 💡 **Future Improvement:**
> The logic can be expanded to support **multi-year projections** and assist with **long-term strategic planning**.

---

## 11. 📝 License

This project was developed for learning purposes as part of the [Codi Academy](https://codiacademy.com.br/) course.

---

## 12. 👨‍💻 Authorship

Developed by:

* [Gabriel Teperino](https://github.com/zSevens7)
* [Vitor Reis](https://github.com/vitorszreis)
* [Rayan Morais](https://github.com/rayancmorais)

---

## 13. 🙏 **Acknowledgements**

Thank you for taking the time to read and test this project! Your interest and feedback are very important to us. Feel free to open issues, suggestions, or collaborate!
