# Online Grocery Shop (ASP.NET Web Forms)

## Project Overview

This is an ASP.NET Web Forms website built with .NET Framework 4.5. It includes customer pages, admin pages, shopping cart, orders, product listings, search, and a local SQL Server database under `App_Data`.

## Requirements

- Visual Studio (2013, 2015, 2017, 2019, 2022 or later) with ASP.NET and web development workloads installed
- .NET Framework 4.5 or higher
- SQL Server Express / LocalDB installed

## How to Run Locally

1. Open Visual Studio.
2. Choose `File > Open > Web Site...`.
3. Browse to the folder:
   `c:\Users\HP\Downloads\Grocery Shop\Grocery Shop\Online Grocery Shop`
4. Open the website.
5. In Solution Explorer, check `Web.config` and confirm the connection string is correct for your SQL Server instance.

### Database Setup

The project expects a local SQL Server database named `GROCERYDB`.

1. Install SQL Server Express or LocalDB if not already installed.
2. Open SQL Server Management Studio or use Visual Studio Server Explorer.
3. Attach the database file located at `Online Grocery Shop\App_Data\GroceryDB.mdf`.
4. Update the connection string in `Web.config` if needed.

Example connection strings:

- For SQL Server Express:
  ```xml
  <add name="GroceryDB" connectionString="Data Source=.\SQLEXPRESS;AttachDbFilename=|DataDirectory|\\GroceryDB.mdf;Integrated Security=True;Connect Timeout=30" />
  ```
- For LocalDB:
  ```xml
  <add name="GroceryDB" connectionString="Data Source=(LocalDB)\\MSSQLLocalDB;AttachDbFilename=|DataDirectory|\\GroceryDB.mdf;Integrated Security=True;Connect Timeout=30" />
  ```

> Note: The current connection string in `Web.config` uses a machine-specific SQL Server instance: `LAPTOP-83GOR2JH\SQLEXPRESS`. Change this value to match your local machine.

## Run the Website

1. Press `F5` or click `Start Debugging` in Visual Studio.
2. The website should launch in your browser using IIS Express.
3. If you only want to run without debugging, press `Ctrl+F5`.

## Common Pages

- `Home.aspx` — home page
- `Products.aspx` — product listing
- `Search.aspx` — product search
- `Cart.aspx` — shopping cart
- `Order.aspx`, `OrderDetails.aspx`, `OrderHistory.aspx`
- `Registration.aspx` — customer registration

## Admin Section

The admin pages are under the `Admin` folder.

- `Admin/Login.aspx`
- `Admin/ManageProducts.aspx`
- `Admin/ManageOrders.aspx`
- `Admin/ManageCustomers.aspx`

## Troubleshooting

- If the website fails to connect to the database, update the `GroceryDB` connection string in `Web.config`.
- If Visual Studio cannot open the site, install the ASP.NET workload for Visual Studio.
- If the database file is locked, close all open instances of SQL Server and Visual Studio, then try again.

## Notes

This project is a classic ASP.NET Web Forms site, so it must run in Visual Studio or IIS Express. It is not a modern ASP.NET Core app.
