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

## 🛠️ Tools & Technologies Used
* **Power BI Desktop & Service:** Data visualization, RLS implementation, and dashboard publishing.
* **Power Query Editor:** Data cleaning, transformation, and conditional logic.
* **AI Insights:** Text Analytics for sentiment scoring.

## 📊 Dashboard Previews

*Note: The images below demonstrate the dashboard's filtering capabilities and Row-Level Security in action.*

**1. Overall Dashboard View**
![Overall Dashboard View](path/to/image(9).png)

**2. Demographic Filtering Applied (Female)**
![Female Filter Applied](path/to/image(10).png)

**3. Single Policy Record Filtered**
![Specific Policy Filtered](path/to/image(8).png)

**4. Row-Level Security: Travel Role View**
![Travel Role View](path/to/image(6).png)

**5. Row-Level Security: Health Role View**
![Health Role View](path/to/image(7).png)
