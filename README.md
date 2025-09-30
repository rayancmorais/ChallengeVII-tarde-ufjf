# 💰 Challenge VII: Codi Cash Financial Management System (UFJF)

This repository holds the solution for **Challenge VII: Codi Cash**, a front-end development project aimed at creating a complete, functional, and responsive interface for a financial management software. This challenge was undertaken by the "**Tarde**" (Afternoon) team as part of a competitive or academic setting at the **Universidade Federal de Juiz de Fora (UFJF)**, in partnership with **Codi Academy**.

The primary goal is to deliver a modern web interface ready for future integration with APIs, focusing heavily on **usability and responsive design**.

---

## 🎯 Project Goal: Codi Cash System

The **Codi Cash** system is a financial management software designed to centralize and simplify the financial control (sales, expenses, and KPIs) for different units of the Codi Academy.

---

## 🚀 Technical Stack

Based on the file structure (`vite.config.ts`, `tsconfig.json`, `index.html`), this project uses a modern web development setup:

* **Front-end**: React.js (or similar library)
* **Language**: TypeScript
* **Build Tool**: Vite
* **Styling**: HTML5, CSS3, and a **Utility-First CSS Framework** (e.g., TailwindCSS or Bootstrap, as per challenge requirements)

---

## ✨ Frontend Functionalities

The challenge required the development of a clean, responsive front-end interface, covering the following key modules:

### 1. Dashboard Principal

* Display monthly summaries of **revenue, expenses, and current balance**.
* Integrate data visualization (**bar/line charts**) to show financial flow over periods (week, month, year).
* **Key Performance Indicator (KPI) cards**: Total Sales, Total Expenses, and Net Balance.

### 2. Sales Module

* **Registration Form**: Comprehensive form for new sales, including:
    * Course Type (Online or In-person)
    * Client Details (Name, Email, Phone)
    * Gross Value, Discounts Applied
    * Taxes, Commissions, and Card Fees
    * Calculation of the Final Sale Value.
* **Sales List**: Display a list of registered sales with filters for period and course type.

### 3. Expenses Module

* **Registration**: Ability to register both **Fixed Expenses** (rent, payroll, utilities) and **Variable Expenses** (maintenance, supplies).
* **Management**: Functionality for editing and deleting expense entries.
* **History**: Visualization of the complete expense history.

### 4. Visualization and Graphs

* Comparative chart of **Revenue vs. Expenses**.
* **Pie chart** showing the distribution of expenses by category.
* Time and category filters for all visualizations.

### 5. User Experience (UX)

* Clean, **responsive**, and intuitive layout (**Mobile First** design is mandatory).
* Clear visual feedback for user actions (e.g., successful registration, form errors).
* Use of **Modals** for confirmations and form submission.

---

## ⚙️ Setup and Installation

### Prerequisites

You must have **Node.js** and **npm** (or `yarn`/`pnpm`) installed.

### Steps

1.  **Clone the repository:**

    ```bash
    git clone [https://github.com/rayancmorais/ChallengeVII-tarde-ufjf.git](https://github.com/rayancmorais/ChallengeVII-tarde-ufjf.git)
    cd ChallengeVII-tarde-ufjf
    ```

2.  **Install dependencies:**

    ```bash
    npm install
    # or
    # yarn install
    ```

3.  **Run the application (Development Mode):**
    Since this project uses Vite, use the standard command to launch the development server:

    ```bash
    npm run dev
    # or
    # yarn dev
    ```

    The application will typically be accessible at `http://localhost:5173`.

---

## 📋 Evaluation Criteria

This project was developed based on the following evaluation criteria:

* Interface is fully **responsive and functional**.
* Codebase exhibits excellent **organization and structure**.
* Effective **reuse and componentization** of UI elements.
* Alignment with the specified challenge requirements.
* Quality of the final project presentation.
