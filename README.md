desktop application · .net framework 4.7.2
ServiceMarketplace
A full-featured desktop solution managing the end-to-end lifecycle of a service-based business — from authentication and service discovery to real-time communication and secure transaction processing.

.NET 4.7.2
C# · Windows Forms
Build: Passing
SQL Server
Visual Studio 2017+
License: MIT
01 —
Overview
ServiceMarketplace ships two purpose-built dashboards (client and seller), a built-in real-time chat system, a booking and payment pipeline, and a business analytics module — all backed by a SQL Server database. Every screen in the application is driven by a clean separation of UI logic, domain models, and data access.

02 —
Key Features
⊞
Dual Dashboard Architecture
Separate, purpose-built interfaces for client and seller workflows — no shared clutter.
◈
Service Management
Sellers can create, edit, and track detailed service listings from their dashboard.
✓
Booking System
Streamlined booking forms with real-time status updates for both parties.
◎
Communication Hub
Built-in direct messaging between buyers and sellers, no external tools needed.
$
Financial Tracking
Integrated payment forms and full transaction history with exportable reports.
↗
Business Intelligence
Analytics module for tracking performance metrics and marketplace trends.
◉
User Profiles
Self-service profile updates and a rating system to maintain marketplace trust.
03 —
Tech Stack
C#
.NET Framework 4.7.2
Windows Forms
SQL Server
System.Data.SqlClient
DEPS —
NuGet Dependencies
Package	Purpose in this project
Newtonsoft.Json	Serializing service listings, user payloads, and API data interchange
BouncyCastle.Cryptography	Secure password hashing and cryptographic credential storage
Google.Protobuf	High-performance structured data serialization for internal messaging
ZstdSharp / LZ4	High-speed compression of transaction records and analytics datasets
04 —
Project Structure
ServiceMarketplace/
Program.cs
Entry point — initializes and launches LoginForm
/Forms
All UI logic — dashboards, payments, chat, bookings, analytics
/Models
Core domain objects: Users.cs, Service.cs, Booking.cs
/Database
SQL connection management via DatabaseHelper.cs
App.config
Connection strings and assembly binding redirects
ServiceMarketplace.csproj
Build settings, target framework, and file references
05 —
Getting Started
Windows OS
Visual Studio 2017+
.NET Framework 4.7.2 SDK
SQL Server (local or remote)
01
Clone the repository
git clone https://github.com/yourusername/ServiceMarketplace.git
02
Set up the database
Run the SQL scripts in /Database/schema.sql against your SQL Server instance. Then update the connection string in App.config to point to your server and database.

03
Restore NuGet packages
Open ServiceMarketplace.sln in Visual Studio. NuGet will automatically restore all dependencies defined in packages.config on first build.

04
Build and run
Set the configuration to Debug or Release, build the solution, and launch. The application starts at LoginForm.cs.

⚠
Ensure your SQL Server instance is running and App.config contains the correct connection string before launching the application.
06 —
Configuration Files
ServiceMarketplace.csproj
Defines project build settings, target framework (.NET 4.7.2), and all file references. Open this in Visual Studio to manage the solution.
App.config
Manages environment-specific settings including the database connection string and runtime assembly binding redirects for libraries like System.Memory.
ℹ
Both files must be present in the project root. The App.config is environment-specific — do not commit production credentials to source control.
SERVICEMARKETPLACE · .NET 4.7.2 · MIT LICENSE
GitHub
Issues
Contributing
