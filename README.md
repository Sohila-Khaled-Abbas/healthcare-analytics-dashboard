# Healthcare Analytics Dashboard 🏥

## Overview

The **Healthcare Analytics Dashboard** is an interactive Power BI project designed to provide actionable insights into hospital operations, including **patient waitlists**, **patient demographics**, and **service utilization trends**. This dashboard helps stakeholders improve decision-making and optimize hospital efficiency.

---

## Dashboard Features

- **Waitlist Analysis**:
  - Identify trends in patient wait times.
  - Highlight bottlenecks and resource allocation needs.

- **Patient Demographics**:
  - Analyze patient distribution by age, gender, and region.
  - Uncover patterns in patient profiles.

- **Service Utilization**:
  - Track which services are in highest demand.
  - Compare trends across time periods and demographics.

---

## Repository Contents

| File/Folder Name            | Description                                                                 |
|-----------------------------|-----------------------------------------------------------------------------|
| `code/`                     | Contains DAX formulas and data preprocessing steps used for the dashboard. |
| `data/`                     | Includes raw and cleaned datasets.                                         |
| `visualizations/`           | Dashboard screenshots and key visualization images.                        |
| `pbix/`                     | Power BI file for the Healthcare Analytics Dashboard.                      |
| `README.md`                 | Project overview and instructions.                                         |
| `LICENSE`                   | License for the project.                                                   |

---

## How to Use This Repository

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Sohila-Khaled-Abbas/healthcare-analytics-dashboard.git
   ```

2. **Open the Power BI Dashboard**:
   - Download the `Healthcare_Analytics_Dashboard.pbix` file from the `pbix/` folder.
   - Open it using Power BI Desktop to explore or modify the dashboard.

3. **Explore Visualizations**:
   - Screenshots of the dashboard are available in the `visualizations/` folder. These include:
     - `dashboard-overview.png`: Overview of the main dashboard page.
     - `waitlist-trends.png`: Insights into patient waitlists and trends.

4. **Recreate the Dashboard**:
   - Use the data in the `data/` folder (both raw and cleaned) to rebuild the dashboard.
   - Refer to the `code/` folder for DAX formulas and data preprocessing instructions.

---

## Key Metrics and DAX Formulas

### 1. Average Wait Time
```dax
Avg Wait Time = AVERAGE(Waitlist[Wait Time (Days)])
```

### 2. Patient Distribution by Age Group
```dax
Age Group = 
SWITCH(
    TRUE(),
    Patients[Age] < 18, "Child",
    Patients[Age] >= 18 && Patients[Age] < 65, "Adult",
    "Senior"
)
```

### 3. Top Utilized Services
```dax
Top Services = 
CALCULATE(
    COUNT(Appointments[Service Type]),
    FILTER(Appointments, Appointments[Completed] = TRUE)
)
```

---

## Screenshots

### **1. Dashboard Overview**
![Dashboard Overview](visualizations/dashboard-overview.png)

### **2. Waitlist Trends**
![Waitlist Trends](visualizations/waitlist-trends.png)

---

## Future Improvements

- **Real-Time Data Integration**:
  - Connect the dashboard to a live database for real-time insights.

- **Predictive Modeling**:
  - Incorporate predictive analytics to forecast patient demand.

- **Enhanced Visualizations**:
  - Add more drill-through pages for deeper data exploration.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## About Me

👋 I’m **Sohila Khaled Galal Abbas**, a passionate data analyst specializing in **Power BI** and **SQL**.  
Let’s connect:  
- **LinkedIn**: [linkedin.com/in/sohilakhaledabbas](https://www.linkedin.com/in/sohilakhaledabbas)  
- **GitHub**: [github.com/Sohila-Khaled-Abbas](https://github.com/Sohila-Khaled-Abbas)

.
