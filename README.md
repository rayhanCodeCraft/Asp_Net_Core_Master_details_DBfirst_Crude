# ASP.NET Core Master-Details Database First CRUD Application

![Project Screenshot 1](https://github.com/rayhanCodeCraft/Asp_Net_Core_Master_details_DBfirst_Crude/blob/main/Screenshot%202024-10-06%20231510.png)
![Project Screenshot 2](https://github.com/rayhanCodeCraft/Asp_Net_Core_Master_details_DBfirst_Crude/blob/main/Screenshot%202024-10-06%20231543.png)

## Overview

This project is a Database-First CRUD (Create, Read, Update, Delete) application with Master-Details functionality developed using ASP.NET Core. The project includes a step-by-step process for setting up the database and configuring the project to run in your local environment.

## Table of Contents

- [Overview](#overview)
- [Technologies Used](#technologies-used)
- [Features](#features)
- [UNZIP File Run Process](#unzip-file-run-process)
- [New Project Setup Process](#new-project-setup-process)
- [Contributing](#contributing)
- [License](#license)

## Technologies Used

- **ASP.NET Core** for backend development
- **Entity Framework Core** for database-first approach
- **Bootstrap** for responsive design
- **Razor View Engine** for dynamic page rendering
- **SQL Server** for database management

## Features

- Master-detail relationship between Students and Modules.
- Full CRUD functionality:
  - Add, edit, view, and delete students.
  - Add, edit, view, and delete modules for each student.
- Razor Pages for clean UI separation.
- Form validation and error handling.
- Integrated SQL Server database using Entity Framework Core.

## UNZIP File Run Process

Follow these steps to run the project from the ZIP file:

1. **Delete All Classes:**
   - Go to the project folder and delete all classes from the `Models` folder.

2. **Comment Controllers, ViewModels, and Views:**
   - Temporarily comment out the controller, view model code, and all views to prevent errors during the initial setup.

3. **Update SQL Connection & Database Name:**
   - In the `Program.cs` file, update the SQL connection string and the database name accordingly.

4. **Create Database in Visual Studio or SQL Server:**
   - Use Visual Studio's SQL or SQL Server to create a new database.

5. **Scaffold Database Context:**
   - Open the Package Manager Console and run the following command to scaffold the database context:
     ```bash
     Scaffold-DbContext "Server=(localdb)\MSSQLLocalDB;database=DemoDB25;Trusted_Connection=true;TrustServerCertificate=true;Integrated Security=true" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models
     ```

6. **Update `appsettings.json`:**
   - In the `appsettings.json` file, add or update the connection string as follows:
     ```json
     "ConnectionStrings": {
       "StudentCon": "Server=(localdb)\\MSSQLLocalDB;database=DemoDB25;Trusted_Connection=true;TrustServerCertificate=true;MultipleActiveResultSets=true;"
     }
     ```

7. **Wait for Build:**
   - Build the project and wait for the process to complete.

8. **Uncomment Code:**
   - After the build, uncomment all the previously commented code (controllers, view models, and views).

9. **Run the Project:**
   - Now you can run the project successfully.

## New Project Setup Process

1. **Create New ASP.NET Core Empty Project:**
   - Start a new project using the ASP.NET Core Empty template.

2. **Install and Update Required Packages:**
   - Open the NuGet Package Manager and install the following packages:
     - `Microsoft.EntityFrameworkCore`
     - `Microsoft.EntityFrameworkCore.SqlServer`
     - `Microsoft.EntityFrameworkCore.Tools`
     - `Microsoft.AspNetCore.Mvc.Razor.RuntimeCompilation`

   - Then, go to the `Program.cs` file and add the following line to enable Razor runtime compilation:
     ```csharp
     builder.Services.AddControllersWithViews().AddRazorRuntimeCompilation();
     ```

3. **Create `wwwroot` Folder and Add Client-Side Libraries:**
   - Add the `wwwroot` folder to your project and include any client-side libraries (Bootstrap, jQuery, etc.) required for the UI.

4. **Create Database in Visual Studio or SQL Server:**
   - Set up your SQL Server and create the required database.

5. **Scaffold Database Context:**
   - Open the Package Manager Console and run the following command to scaffold the database context:
     ```bash
     Scaffold-DbContext "Server=(localdb)\MSSQLLocalDB;database=DemoDB25;Trusted_Connection=true;TrustServerCertificate=true;Integrated Security=true" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models

     ```

6. **Update `appsettings.json`:**
   - In the `appsettings.json` file, add or update the connection string as follows:
     ```json
     "ConnectionStrings": {
       "StudentCon": "Server=(localdb)\\MSSQLLocalDB;database=DemoDB25;Trusted_Connection=true;TrustServerCertificate=true;MultipleActiveResultSets=true;"
     }
     ```

7. **Wait for Build:**
   - Wait for the project to build.

8. **Create Controllers and Folders:**
   - Create the necessary controllers, models (ViewModel folder), and views (View/Shared folder).
   - Generate the required views (Razor View Empty), layout (Razor Layout), and other partial views (such as ModulesTable and IndexModulesTable).

9. **Run the Project:**
   - After everything is set up, you can now run the project successfully.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to improve this project.

## License

This project is licensed under the MIT License.
