

# **Expense Report App**

## Overview

The **Expense Report App** is a comprehensive Power Platform application that integrates **Power Apps**, **Power Automate**, **Power BI** and **Dataverse** to streamline **expense management** and reporting. This app provides an easy-to-use interface for users to submit, track, and approve expenses, while also providing insightful data visualizations.

## Features

### **Power Apps**

#### **Screen 1: View Expenses**
- **View Expenses**: Easily navigate and view a list of all submitted expenses.
- **Filter & Search Expenses**: Quickly find specific expenses by applying custom filters and search criteria.
- **Email Notifications**: Directly mail the approver when the status of an expense is either **"Submitted"** or **"Declined"**.
- **Reset Filters**: Reset all filtering fields with a single click for quick access to full records.

![Image Alt Text](images/image(1).png)
![Image Alt Text](images/image(3).png)

#### **Screen 2: Add Expenses**
- **Create New Expenses**: Submit new expense entries with ease.
- **Auto Date Assignment**: The app automatically fills in the expense date with the current date.
- **Auto Approver Assignment**: Automatically assigns an approver based on the user's manager status in Office 365.
- **Submit to Dataverse**: Expense data is submitted to a **Dataverse table** via the Patch function. Users are notified of successful submissions or when required fields are missing.
- **Reset Fields**: Clear all input fields with a single button click.

![Image Alt Text](images/image(4).png)

#### **Screen 3: Expense Analysis**
- **Power BI Integration**: View an embedded Power BI report for comprehensive data visualization and insights. It allows users to filter data and analyze expenses.
- **Multiple Selections**: Users can filter data by date, submitter, category, and status.

![Image Alt Text](images/image(5).png)

#### **Screen 4: Created By**
- **Contact Information**: Displays contact information about the app’s creator for support or inquiries.

![Image Alt Text](images/image(6).png)

### **Design & Customization**
- The app uses global variables for colors, allowing you to easily update the app’s theme.
- Two reusable components enable quick customization of the app's header and left column, which serves as the navigation panel.

---

### **Power Automate**

#### **Expense Approval Workflow**
- **Approval Email Notifications**: When a new expense is created in Dataverse, an email is sent to the assigned approver with the details of the expense, and they can approve or reject it directly.
- **Status Update**: The expense's status in Dataverse is updated based on the approver's decision.

#### **Refresh Power BI Dataset Workflow**
- **Data Synchronization**: Whenever a new expense item is added or modified, Power Automate triggers a refresh of the related Power BI dataset, ensuring that the data in Power Apps and Power BI is always up to date.

---

### **Power BI Service**

- **Expense Analysis Report**: A Power BI report is linked to the Dataverse table, providing a detailed analysis of expense data.
- **Data Visualization**: The report offers various visualizations and filtering options, including filters for date, submitter, status, and category.

---

## Installation Instructions

### 1. **Prepare Dataverse Environment**
   - Ensure access to **Power Platform** and permissions to create and manage **Power Apps**.
   - Create a Dataverse table (e.g., `dbExpenses`) to store the expense records.

### 2. **Download the App Files**
   - Download the [**ExpenseReportApp** solution zip](ExpenseAnalysis_1_0_0_1.zip) and extract it.

### 3. **Import Components**
   - Import the `dbExpenses.xlsx` file into your **Dataverse** environment.
   - Import the `Expense_Analysis.pbix` file into **Power BI**.

### 4. **Link Power Automate Flows**
   - Set up **Power Automate** for **Expense Approval** and **Power BI Dataset Refresh**.
   - Link these flows with the Dataverse tables and Power BI datasets.

---

### 5. **Getting Started**  
   - Ensure you have the necessary permissions for the app and services.
   - Run the Power BI report and ensure data synchronization between Power Apps, Power Automate, and Power BI.


### **Contributors**

This app was created by **Sharoon Gafoor**. For questions or support, please reach out to **sharoongafoor@gmail.com**.

---

### Conclusion

This **Expense Report App** is designed to simplify and automate the process of expense management, approval, and analysis. By combining **Power Apps**, **Power Automate**, and **Power BI**, it provides a comprehensive solution that improves efficiency and data accuracy across organizations.

Let me know if you need further assistance or improvements!
