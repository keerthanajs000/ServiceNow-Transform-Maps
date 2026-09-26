# Import Data using Transform Maps (Spreadsheet)

## Skill Wallet / Project

This repository/documentation package contains the project **Import Data using Transform Maps (Spreadsheet)** implemented on the **ServiceNow** platform.

### Project purpose

The project demonstrates importing structured employee data from a spreadsheet into ServiceNow using:

- Import Sets
- Transform Maps
- Field Mapping
- Coalesce
- Transform History validation
- Reports
- Dashboard

### Project configuration

| Item | Value |
|---|---|
| Platform | ServiceNow |
| Target table | Employee Test (`u_employee_test`) |
| Import Set table | Employee Import (`u_employee_import`) |
| Transform Map | Sample Spreadsheet Import |
| Target fields | Employee ID, Employee Name, Email, Department, Location |
| Dashboard | Employee Analytics Dashboards |

### Workflow

```text
Spreadsheet
    ↓
Import Set Table
    ↓
Transform Map
    ↓
Field Mapping
    ↓
Transform
    ↓
Employee Test Table
    ↓
Validation / Transform History
    ↓
Reports
    ↓
Employee Analytics Dashboards
```

### Main implementation phases

1. Prepare the spreadsheet.
2. Create the Employee Test custom table.
3. Create the Employee Import table.
4. Create the Sample Spreadsheet Import Transform Map.
5. Transform and validate the data.
6. Enable Coalesce to avoid duplicate records.
7. Insert new/modified spreadsheet data and review Transform History.
8. Create Employees by Department, Employees by Location, and Employee List reports.
9. Add the reports to Employee Analytics Dashboards.

### Coalesce test documented in the project

The supplied project document records that, after Coalesce was configured:

- 4 rows were uploaded.
- 2 new employee IDs were inserted.
- 2 existing employee records were updated.
- Re-uploading the same sheet resulted in 4 ignored rows, with 0 inserts and 0 updates.

### Reports

- **Employees by Department** — Pie Chart, grouped by Department, Count aggregation.
- **Employees by Location** — Bar Chart, grouped by Location, Count aggregation.
- **Employee List Report** — List containing Employee ID, Employee Name, Email, Department, and Location.

### Dashboard

The three reports are added to:

**Employee Analytics Dashboards**

### Documentation

`Import_Data_using_Transform_Maps_Skill_Wallet_Report.pdf` contains the polished project report and evidence screenshots extracted from the supplied project document.

### Evidence

The `evidence/` folder contains selected screenshots extracted from the original supplied project PDF.

### Important note

This README and report are based only on the supplied project document. No unrelated project topic, additional implementation, script, integration, or unsupported technical claim has been added.
