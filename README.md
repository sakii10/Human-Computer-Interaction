# HCI Project 02 — Travel Agent for Serbia

<img width="23" height="33" alt="Screenshot 2026-09-24 002428" src="https://github.com/user-attachments/assets/5da27413-6a4f-476c-acb9-56642a0ee56f" />

A desktop application developed for the **Human-Computer Interaction** course at the Faculty of Technical Sciences, University of Novi Sad.

The application represents a **travel agency system for organizing and managing trips around Serbia**, with a focus on usability, direct manipulation, efficient interaction, and adapting the interface to a specific user profile and usage scenario.

## Screenshots

### Login

<img width="590" height="331" alt="Screenshot 2026-09-24 003635" src="https://github.com/user-attachments/assets/e9b9044b-3d85-483f-9c61-73d29a5e3218" />

### Attractions

<img width="587" height="329" alt="Screenshot 2026-09-24 003350" src="https://github.com/user-attachments/assets/1acff07f-725d-497c-a61a-f0d58bd8a8a0" />

### Agent — Attraction Management

<img width="588" height="331" alt="Screenshot 2026-09-24 003756" src="https://github.com/user-attachments/assets/06c2710e-f9cb-43eb-92dc-b59e62d36761" />

## Project Context

The project was created as part of the **Human-Computer Interaction** course, where the goal was not only to implement application functionality, but also to design the interaction according to a defined user profile and usage scenario.

The application was developed around the concept of a **travel agent for Serbia** who manages travel arrangements and the associated destinations, attractions, accommodation and restaurants.

The main goal was to create an interface that allows an agent to perform everyday management tasks efficiently while following HCI principles such as:

* direct manipulation
* drag & drop interaction
* clear and consistent dialogs
* efficient navigation
* user-oriented documentation and help
* adaptation to the user's experience level
* adaptation to the physical usage environment
* consistency and visibility of system state

## User Profile and Use Case

The application was designed for the assigned user profile **Đorđe**:

* **Age:** 33
* **Domain knowledge:** None
* **Computer/programming experience:** Very high
* **User needs:** Well-explained functionality through integrated documentation and a high level of automation

Because Đorđe has strong computer skills but no specific knowledge of the travel-agency domain, the interface was designed to make the available functionality clear without requiring prior knowledge of the application.

The project was also adapted to **Scenario U**, in which the application is used on a relatively small display of approximately **750 × 430 pixels at 96 DPI**. This required attention to the available screen space, compact layouts and efficient interaction.

## Main Functionality

The application provides functionality for a travel agent to manage and work with travel-agency data, including:

* user authentication
* management of travel arrangements
* viewing available trips
* management of attractions
* adding new attractions
* editing existing attractions
* deleting attractions
* management of accommodation and restaurants
* viewing trips and associated information
* booking and purchasing arrangements
* viewing purchased and reserved trips
* viewing all available trips
* monthly sales overview
* overview of sold arrangements for a selected trip
* interactive manipulation of application elements
* persistent storage of application data

CRUD operations are implemented through dedicated dialogs, allowing the agent to create, view, update and delete relevant entities.

## HCI Focus

A major part of the project was applying Human-Computer Interaction principles rather than focusing only on the underlying functionality.

The application was designed around:

* **Direct manipulation** — users interact directly with visible application elements.
* **Drag & drop** — used as part of the interaction model required by the assignment.
* **Feedback and visibility** — actions and changes should be clear to the user.
* **Consistency** — similar operations follow consistent interaction patterns.
* **Error prevention** — dialogs and interaction flows are designed to reduce accidental actions.
* **User adaptation** — the interface and documentation take the assigned user's experience and needs into account.
* **Scenario adaptation** — the layout is designed with the small-screen usage scenario in mind.
* **Help and documentation** — functionality is accompanied by explanations intended for users without prior domain knowledge.

The project therefore combines a functional travel-agency application with an HCI-oriented interface design.

## Technologies

The application was developed as a **C# WPF desktop application** using:

* **C#**
* **.NET 6**
* **WPF**
* **Entity Framework Core**
* **SQLite**
* **Material Design**
* **LiveCharts**
* **Newtonsoft.Json**
* **Ninject**
* **Serilog**

Entity Framework Core is used for database access and persistence, with SQLite as the local database.

## Project Structure

The solution is organized into separate parts for application views, models, persistence and supporting functionality.

The main project contains:

* WPF views and user interface components
* application models
* database context and persistence
* database migrations
* seed data
* services and supporting logic
* application resources and images

## Database Setup

The project uses Entity Framework Core migrations to create the local SQLite database.

### 1. Open the project

Open the solution in **Visual Studio**.

### 2. Recreate the database

If the repository does not contain an existing database, remove the existing files from the `Migrations` directory except `.gitkeep`, and remove existing `.db` files from:

```text
HCIProject02/Core/Persistence
```

### 3. Create the migration

Open:

**Tools → NuGet Package Manager → Package Manager Console**

Run:

```powershell
Add-Migration InitialCreate
```

Then:

```powershell
Update-Database
```

### 4. Seed the database

Open:

```text
HCIProject02/App.xaml.cs
```

Temporarily enable:

```csharp
DatabaseContextSeed.Seed(db);
```

Run the application once so that the database is populated with the initial data.

After the initial run, disable the seed call again to prevent the seed data from being inserted every time the application starts.

The database persists between application launches.

## Running the Application

1. Open the solution in Visual Studio.
2. Restore the NuGet packages if necessary.
3. Make sure the SQLite database has been created using the migration steps above.
4. Build the solution.
5. Run the application.

The application starts with the login screen and provides access to the travel-agent functionality after authentication.

## Original Project

The original project can be found here:

[HCIProject02 — Original Repository](https://github.com/vdevic01/HCIProject02?utm_source=chatgpt.com)

The original repository also contains the initial project setup and course-specific instructions.


