# Insurance Data Analysis & Sentiment Dashboard

## 📌 Project Overview
This project is an interactive Power BI dashboard designed to analyze insurance data, track key performance indicators (KPIs), and process customer feedback. It features advanced data modeling, row-level security for role-based access, and AI-driven text analytics to gauge customer sentiment.

## Key Features

### 1. Interactive Filtering & Slicers
* **Dynamic KPIs:** Cards displaying Premium Amount, Coverage Amount, and Claim Amount automatically update based on user selections.
* **Granular Slicers:** Users can filter the entire dashboard by specific `Policy Number`, `Claim Number`, or `Customer ID` using dropdown menus.
* **Demographic Filtering:** A dedicated Gender slicer allows for quick comparisons between male and female customer metrics.

### 2. Drill-Through Navigation
* **Deep Dive Analysis:** Implemented drill-through functionality connecting a high-level overview to detailed records. Clicking on a specific policy category in the *Premium Amount by Policy Type* visual on Page 1 seamlessly navigates to Page 2, filtering the detailed table view to show only the records relevant to the selected policy.

### 3. Row-Level Security (RLS) - Role Management
Configured dynamic Row-Level Security (RLS) to ensure data privacy and relevant viewing for different department managers. 
* **Custom Roles:** Created specific roles including `Travel`, `Health`, `Auto`, `Life`, and `Home`.
* **Filtered Access:** When a manager logs in (e.g., the Travel Manager viewing under the "Travel Role"), the dashboard restricts the dataset to only display insights, policies, and claims associated with their specific department.

### 4. AI-Driven Sentiment Analysis (Power Query)
Integrated Power BI's AI Text Analytics within Power Query Editor to process customer feedback imported from an Excel workbook.
* **Sentiment Scoring:** Automatically generated a sentiment score between 0.0 and 1.0 for each piece of customer feedback.
* **Conditional Categorization:** Created a custom column to group scores into actionable insights:
  * **Excellent:** Score >= 0.8
  * **Good:** Score >= 0.6
  * **Needs Improvement:** Score < 0.6

### 5. Multi-Source Data Integration & Modeling
* **Hybrid Data Architecture:** Built a unified relational data model by connecting Power BI directly to **Microsoft SQL Server** for large-scale policy and claims data, while seamlessly integrating external customer feedback data from an **Excel workbook**.

## 🛠️ Tools & Technologies Used
* **Microsoft SQL Server:** Primary relational database used to query and import the core insurance policy, customer, and claims datasets.
* **Power BI Desktop & Service:** Data visualization, data modeling across multiple sources, RLS implementation, and report publishing.
* **Power Query Editor:** Data cleaning, transformation, conditional logic, and integrating SQL database tables with external Excel sheets.
* **Microsoft Excel:** Secondary data source utilized for importing customer feedback records.
* **AI Insights:** Text Analytics integrated within Power Query for automated sentiment scoring.

## 📊 Dashboard Previews

*Note: The images below demonstrate the dashboard's filtering capabilities and Row-Level Security in action.*

**1. Overall Dashboard View**
<img width="1482" height="1001" alt="image (9)" src="https://github.com/user-attachments/assets/ef9ecc2d-6a89-45c0-aa36-fb797324e97a" />

**2. Demographic Filtering Applied (Female)**
<img width="1477" height="990" alt="image (10)" src="https://github.com/user-attachments/assets/67e95b69-35a6-4ab5-a7da-c24932ae48b2" />

**3. Single Policy Record Filtered**
<img width="1485" height="996" alt="image (8)" src="https://github.com/user-attachments/assets/54019cb1-aa81-4494-9219-a19c3e15c636" />

**4. Row-Level Security: Travel Role View**
<img width="1467" height="993" alt="image (6)" src="https://github.com/user-attachments/assets/6e06cca6-aef3-440e-88ac-43fa80de9c65" />

**5. Row-Level Security: Health Role View**
<img width="1476" height="992" alt="image (7)" src="https://github.com/user-attachments/assets/59893f96-21f4-429c-b9af-2a58036b63e7" />

