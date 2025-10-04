# EmployeeManagementSystem

# Steps to Create Employee Management System Project

    -- Create ASP.NET Core Web App (Model-View-Controller) project 
    
    -- Define the 3 model class 
            DepartmentMaster.cs
            DesignationMaster.cs
            EmployeeMaster.cs
            Add the properties in each model class with Data Annotation validations 
            
    -- install the EntityFramework packages through NuGet package manager
            Microsoft.EntityFrameworkCore
            Microsoft.EntityFrameworkCore.SqlServer
            Microsoft.EntityFrameworkCore.Tools
            Microsoft.VisualStudio.Web.CodeGeneration.Design
            
    -- Create the folder for DatabaseContext that contain the database with its table
    
    -- add the connection string in appSetting.json
            "ConnectionStrings": {
                      "ProjectConnectionString": "Server=LAPTOP-FQQBVLIE;Database=EmployeeMgmtSystem;Trusted_Connection=True;TrustServerCertificate=True;"
            },
    -- add the services in Program.cs file for Database connection 
            builder.Services.AddDbContext<DatabaseContext>(options => 
                    options.UseSqlServer(builder.Configuration.GetConnectionString("DefaultConnection")));

    -- perform the migration 
            Add-Migration "InitialCreate"
            Update-Database
            
    -- Create the Controller for each model class 
            It is mendetory to add prefix of each controller as a Controller.cs 
            add the code in each controller for action method (Index, Create, Edit, Delete)

    -- Create the folder for each model class in View Folder 
            add view as a controller view 
            
