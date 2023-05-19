## Using T4 to generate enums from database lookup tables

  
# Using T4 to generate enums from database lookup tables
 
Database lookup tables are often used to store predefined values that can be referenced by other tables. For example, a table called `Country` might store the names and codes of all the countries in the world, and a table called `Customer` might have a column called `CountryId` that references the `Country` table.
 
## Using T4 to generate enums from database lookup tables


[**Download File**](https://www.google.com/url?q=https%3A%2F%2Furlca.com%2F2tLrld&sa=D&sntz=1&usg=AOvVaw3wYeQg9M3gJ2v0j133MZTu)

 
In some cases, it might be useful to have an enum type in C# that corresponds to the values in a lookup table. This can make the code more readable and type-safe, as well as enable features like switch statements and intellisense. However, manually creating and maintaining such enums can be tedious and error-prone, especially if the lookup table changes frequently.
 
A better solution is to use T4 templates to automatically generate enums from database lookup tables. T4 (Text Template Transformation Toolkit) is a powerful tool that allows you to write code that generates code. You can use T4 to access the database schema and generate enums based on the values in the lookup tables.
 
In this article, we will show you how to use T4 to generate enums from database lookup tables in a few simple steps.
 
## Step 1: Create a T4 template file
 
The first step is to create a T4 template file in your project. A T4 template file has the extension `.tt` and consists of two parts: a directive section and a template section. The directive section contains instructions for the T4 engine, such as the output file name and the references to other assemblies. The template section contains the code that generates the output file.
 
To create a T4 template file, right-click on your project in Visual Studio and select Add > New Item. Choose Text Template from the list of items and name it `Enums.tt`.
 
The default content of the template file should look something like this:

    <#@ template debug="false" hostspecific="false" language="C#" #>
    <#@ assembly name="System.Core" #>
    <#@ import namespace="System.Linq" #>
    <#@ import namespace="System.Text" #>
    <#@ import namespace="System.Collections.Generic" #>
    <#@ output extension=".cs" #>
    
    // This is the output file content

## Step 2: Add a connection string to the database
 
The next step is to add a connection string to the database that contains the lookup tables. You can use any database provider that supports Entity Framework, such as SQL Server, MySQL, SQLite, etc. For this example, we will use SQL Server Express LocalDB.
 
To add a connection string to the database, open the `app.config` or `web.config` file in your project and add a `<connectionStrings>` section with a name and a connection string. For example:

    <connectionStrings>
      <add name="LookupDb" connectionString="Data Source=(LocalDB)\MSSQLLocalDB;AttachDbFilename=|DataDirectory|\LookupDb.mdf;Integrated Security=True;" providerName="System.Data.SqlClient" />
    </connectionStrings>

Note that you need to replace the `|DataDirectory|` placeholder with the actual path to your database file.
 
To access the connection string from the T4 template file, you need to add a reference to the `System.Configuration` assembly and import the `System.Configuration` namespace. You also need to set the `hostspecific` attribute of the template directive to `true`, which allows you to access host-specific information such as project settings. For example:

    <#@ template debug="false" hostspecific="true" language="C#" #>
    <#@ assembly name="System.Core" #>
    <#@ assembly name="System.Configuration" #>
    <#@ import namespace="System.Linq" #>
    <#@ import namespace="System.Text" #>
    <#@ import namespace="System 0f148eb4a0
