# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Blazor Server application built with .NET 9.0 for learning Blazor concepts, particularly data binding and component interactions. The project demonstrates various Blazor features including two-way data binding, event handling, and dynamic UI updates.

## Architecture

- **Framework**: ASP.NET Core Blazor Server (.NET 9.0)
- **Rendering Mode**: Interactive Server Components
- **Structure**: Standard Blazor project layout with Components, Models, and wwwroot folders
- **Key Features**: 
  - Real-time UI updates with server-side rendering
  - Two-way data binding examples
  - Product management demonstrations

## Key Components Structure

- `Components/Pages/LearnBlazor/`: Contains learning examples and demos
  - `BindProp.razor`: Demonstrates property binding, form controls, and dynamic lists
  - `DemoProduct.razor`: Product demonstration component
- `Models/`: Contains data models
  - `Product.cs`: Main product entity with properties
  - `Product_Prop.cs`: Product properties/attributes model
- `Components/Layout/`: Layout components including navigation

## Development Commands

### Build and Run
```bash
dotnet build              # Build the solution
dotnet run               # Run the application (from LearnBlazor folder)
dotnet watch run         # Run with hot reload for development
```

### Development URLs
- HTTP: http://localhost:5157
- HTTPS: https://localhost:7188

### Project Structure Commands
```bash
dotnet sln add [project]  # Add projects to solution
dotnet restore           # Restore NuGet packages
```

## Development Notes

- Uses `ImplicitUsings` and `Nullable` enabled in project configuration
- Global using statements are configured for common namespaces
- Bootstrap CSS framework is included for styling
- Interactive server components are enabled for real-time updates
- The application uses Antiforgery protection and HTTPS redirection
- Static assets are mapped for CSS, JS, and image files

## Component Patterns

The project follows standard Blazor patterns:
- `@page` directives for routing
- `@code` blocks for component logic
- Two-way binding with `@bind` and `@bind-value`
- Event handling with `@bind:event` 
- Conditional rendering with `@if` statements
- List rendering with `@foreach` loops

## Models and Data

The Product model demonstrates:
- Basic properties (Id, Name, Price, IsActive)
- Complex properties (ProductProperties collection)
- Data binding in forms and tables
- Dynamic property selection and display