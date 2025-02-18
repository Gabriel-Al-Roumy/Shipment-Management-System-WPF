# Shipment Management System (WPF + EF Core)

A **WPF-based desktop application** with **Entity Framework Core** and **MS SQL Server**, designed to streamline shipment management.  
The system provides an intuitive interface to manage shipments, including **CRUD operations** and filtering options.

---

## 📌 **Overview**
The Shipment Management System is a **Windows desktop application** built with **WPF and EF Core**, offering an efficient way to manage shipments and their details.  
It enables users to **add, update, delete, and filter shipments** using a **database-backed system (MS SQL Server)**.

---

## 🚀 **Features**
### **Shipment Management**
- Add, edit, delete, and view shipments.
- Search and filter shipments based on **sender, recipient, destination, dates, status**.

### **Address Management**
- Manage shipment destinations with **city, street, and zip code**.
- Address validation ensures proper data consistency.

### **Dashboard (Upcoming Feature)**
- Table displaying all shipment information

### **Reports (Planned)**
- **Cost Analysis Report**: Breakdown of shipment costs over time.
- **Courier Performance Report**: Delivery times and success rates by courier.
- **Status Report**: Overview of shipped, in-transit, and delivered packages.

---

## 🛠 **Technologies Used**
- **C# (.NET 8+)**: Main programming language.
- **WPF (Windows Presentation Foundation)**: For the user interface.
- **Entity Framework Core**: For database access.
- **MS SQL Server (via EF Core Code-First)**: To store shipment records.
- **XAML**: To design WPF UI components.

---

## 📦 **Database Setup**
### **1️⃣ Install SQL Server & SSMS**
Make sure you have **MS SQL Server** and **SQL Server Management Studio (SSMS)** installed.

### **2️⃣ Modify Database Connection in `AppDbContext.cs`**
Update the connection string inside `OnConfiguring`:
```csharp
protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
{
    optionsBuilder.UseSqlServer("Server=(localdb)\\ProjectModels;Database=ShipmentDB;Trusted_Connection=True;");
}
