# **SQL Server Database CI/CD Project**  

## **Overview**  
This project demonstrates how to implement **Continuous Integration (CI) and Continuous Deployment (CD)** for a **SQL Server database** using **Azure DevOps**. It automates database schema changes, version control, and deployment processes, ensuring efficient database management with minimal manual intervention.

## **Features**  
- **Automated Database Deployment**: Uses Azure DevOps pipelines to deploy SQL Server schema changes.  
- **Version Control**: Tracks all database modifications using Git.  
- **CI/CD Workflow**: Automates build, validation, and deployment processes.  
- **Error Handling & Rollback**: Ensures safe deployment with rollback mechanisms.  
- **Scalability**: Can be extended for multiple environments (development, staging, production).  

## **Technology Stack**  
- **SQL Server** – Database engine  
- **Azure DevOps** – CI/CD pipeline management  
- **Git** – Version control  
- **PowerShell & YAML** – Automation scripts for deployment  

## **Project Structure**  
```
├── .gitattributes           # Defines repository behavior
├── .gitignore               # Excludes unnecessary files
├── README.md                # Project documentation
├── SqlServerDatabase.sln    # SQL Server project solution file
├── DatabaseScripts/         # SQL scripts for schema and stored procedures
│   ├── Tables/              # SQL scripts for table creation/modification
│   ├── StoredProcedures/    # SQL scripts for stored procedures
│   ├── Views/               # SQL scripts for database views
│   ├── Triggers/            # SQL scripts for triggers
│   ├── SeedData/            # SQL scripts for initial data population
├── Pipelines/               # CI/CD pipeline configurations
│   ├── azure-pipelines.yml  # Azure DevOps pipeline definition
│   ├── deploy-sql.ps1       # PowerShell script for deployment
```

## **Setup Instructions**  
### **Prerequisites**  
1. Install **SQL Server Management Studio (SSMS)** or **Azure Data Studio**.  
2. Configure an **Azure DevOps** organization and repository.  
3. Install **Azure CLI** for command-line automation (optional).  

### **Steps to Set Up CI/CD in Azure DevOps**  
1. **Clone the Repository:**  
   ```sh
   git clone https://github.com/your-username/sqlserver-database-cicd.git
   cd sqlserver-database-cicd
   ```

2. **Configure Azure DevOps Pipeline:**  
   - Navigate to **Azure DevOps → Pipelines → New Pipeline**  
   - Select **GitHub Repository** or **Azure Repos Git**  
   - Choose **Starter Pipeline** and replace contents with `azure-pipelines.yml`  
   - Save and run the pipeline  

3. **Deploy Database Changes:**  
   - Update SQL scripts in `DatabaseScripts/`  
   - Commit and push changes to the repository  
   - The pipeline will automatically deploy the changes to SQL Server  

## **Contributing**  
1. Fork the repository  
2. Create a new branch  
3. Make your changes and submit a pull request  

## **License**  
This project is open-source and available under the **MIT License**. 🚀
