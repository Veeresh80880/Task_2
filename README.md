# Employee Time Tracker

A comprehensive C# solution for visualizing employee time data through interactive HTML tables and professional pie charts.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Program A: HTML Table Generator](#program-a-html-table-generator)
- [Program B: PIE Chart Generator](#program-b-pie-chart-generator)
- [API Reference](#api-reference)
- [Output Examples](#output-examples)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This project consists of two C# console applications that fetch employee time data from a REST API and generate professional visualizations:

1. *HTML Table Generator* - Creates an interactive HTML table showing employee work hours
2. *PIE Chart Generator* - Produces a high-quality PNG pie chart displaying time distribution

## ✨ Features

### Common Features
- 🌐 Fetches real-time data from REST API
- 🔍 Filters out deleted entries and invalid data
- 📊 Calculates total hours worked per employee
- 🎨 Professional styling and design
- ⚡ Fast processing and error handling
- 📱 Responsive design (HTML table)

### HTML Table Features
- 📋 Interactive table with hover effects
- 🔴 *Red highlighting* for employees under 100 hours
- 📈 Summary statistics dashboard
- 🎯 Ordered by total time worked (descending)
- 📱 Mobile-responsive design
- 🎨 Gradient backgrounds and modern styling

### PIE Chart Features
- 🥧 High-quality PNG pie chart generation
- 🌈 Distinct colors for each employee
- 📊 Percentage labels on chart slices
- 📋 Detailed legend with rankings
- 📈 Summary statistics panel
- 🎭 3D effects with shadows and gradients

## 🛠 Requirements

### System Requirements
- .NET 6.0 or later
- Windows, macOS, or Linux
- Internet connection (for API access)

### Dependencies

#### Program A (HTML Table)
- No external dependencies (uses built-in System.Text.Json)

#### Program B (PIE Chart)
- System.Drawing.Common NuGet package

## 📦 Installation

### Option 1: Using .NET CLI (Recommended)

#### For HTML Table Generator:
bash
# Create new console project
dotnet new console -n HTMLTableGenerator
cd HTMLTableGenerator

# Replace Program.cs with Program A code
# No additional packages needed

# Run the application
dotnet run


#### For PIE Chart Generator:
bash
# Create new console project
dotnet new console -n PieChartGenerator
cd PieChartGenerator

# Add required package
dotnet add package System.Drawing.Common

# Replace Program.cs with Program B code

# Run the application
dotnet run


### Option 2: Using Visual Studio

1. Create a new Console Application project
2. Install System.Drawing.Common package (for PIE chart only):
   - Right-click project → Manage NuGet Packages
   - Search for "System.Drawing.Common"
   - Install the package
3. Replace Program.cs with the appropriate code
4. Build and run

### Option 3: Direct Compilation

bash
# For HTML Table (no dependencies)
csc HTMLTableGenerator.cs
HTMLTableGenerator.exe

# For PIE Chart (requires System.Drawing reference)
csc /reference:System.Drawing.dll PieChartGenerator.cs
PieChartGenerator.exe


## 🚀 Usage

### Running Program A (HTML Table)
bash
cd HTMLTableGenerator
dotnet run


*Expected Output:*

HTML Table Generator for Employee Time Data
==========================================
Fetching data from API...
✓ Data received: 156789 characters
Parsing JSON data...
✓ Parsed 1247 time entries
✓ Valid entries: 1089
Calculating total hours per employee...
✓ Processed 12 employees
Generating HTML table...
✓ HTML file created: employee_time_table.html

📊 SUMMARY:
Total employees: 12
Total hours tracked: 1127.83
Average hours per employee: 93.99
Employees under 100 hours: 5

🏆 TOP 5 EMPLOYEES:
1. 🟢 Abhay Singh: 158.75 hours
2. 🟢 Patrick Huthinson: 142.33 hours
3. 🟢 Stewart Malachi: 135.17 hours
4. 🟢 John Black: 126.92 hours
5. 🟢 Tim Perkinson: 118.58 hours

⚠️  EMPLOYEES UNDER 100 HOURS (5):
   🔴 Raju Sunuwar: 87.42 hours
   🔴 Rita Alley: 76.17 hours
   🔴 Tamoy Smith: 68.33 hours
   🔴 Kavvay Verma: 45.25 hours
   🔴 Mary Poppins: 32.15 hours

🎉 Success! Open 'employee_time_table.html' in your browser to view the table.


### Running Program B (PIE Chart)
bash
cd PieChartGenerator
dotnet run


*Expected Output:*

PIE Chart PNG Generator for Employee Time Data
==============================================
Fetching data from API...
✓ Data received: 156789 characters
Parsing JSON data...
✓ Parsed 1247 time entries
✓ Valid entries: 1089
Calculating total hours per employee...
✓ Processed 12 employees
✓ Total hours tracked: 1127.83
Assigning colors...
Generating PIE chart PNG...
✓ PNG file created: employee_pie_chart.png

📊 PIE CHART SUMMARY:
Total employees: 12
Total hours tracked: 1127.83
Average hours per employee: 93.99

🏆 TOP 10 EMPLOYEES (by percentage):
 1. Abhay Singh          158.8h (14.1%) ███████
 2. Patrick Huthinson    142.3h (12.6%) ██████
 3. Stewart Malachi      135.2h (12.0%) ██████
 4. John Black           126.9h (11.3%) █████
 5. Tim Perkinson        118.6h (10.5%) █████
 6. Mary Poppins         112.8h (10.0%) █████
 7. Kavvay Verma         108.3h ( 9.6%) ████
 8. Raju Sunuwar          87.4h ( 7.8%) ███
 9. Rita Alley            76.2h ( 6.8%) ███
10. Tamoy Smith           68.3h ( 6.1%) ███

🎉 Success! PIE chart saved as 'employee_pie_chart.png'


## 📊 Program A: HTML Table Generator

### Purpose
Creates a professional HTML table displaying employee time data with responsive design and visual highlighting.

### Key Features
- *Red Row Highlighting*: Employees with less than 100 hours are highlighted in red
- *Responsive Design*: Works on desktop, tablet, and mobile devices
- *Interactive Elements*: Hover effects and smooth transitions
- *Summary Dashboard*: Statistics overview with key metrics
- *Professional Styling*: Modern CSS with gradients and shadows

### Output File
- employee_time_table.html - Complete HTML page with embedded CSS

### Technical Implementation
- Uses System.Text.Json for JSON parsing
- HttpClient for API requests
- Custom HTML generation with embedded CSS
- Data validation and error handling

## 🥧 Program B: PIE Chart Generator

### Purpose
Generates a high-quality PNG pie chart showing the percentage distribution of total time worked by each employee.

### Key Features
- *High-Quality Graphics*: Anti-aliased rendering with smooth edges
- *Color Coding*: Distinct colors for each employee segment
- *Percentage Labels*: Clear labeling on chart slices (for segments ≥5%)
- *Comprehensive Legend*: Employee rankings with hours and percentages
- *Visual Effects*: 3D shadows, gradients, and professional styling
- *Statistics Panel*: Summary information at the bottom

### Output File
- employee_pie_chart.png - High-resolution PNG image (1000x700 pixels)

### Technical Implementation
- Uses System.Drawing.Common for graphics generation
- Custom color generation using HSV color space
- Advanced graphics rendering with anti-aliasing
- Mathematical calculations for pie slice positioning

## 🔗 API Reference

### Endpoint

GET https://rc-vault-fap-live-1.azurewebsites.net/api/gettimeentries?code=vO17RnE8vuzXzPJo5eaLLjXjmRW07law99QTD90zat9FfOQJKKUcgQ==


### Response Format
json
[
  {
    "Id": "string",
    "EmployeeName": "string",
    "StarTimeUtc": "2022-02-22T14:15:00",
    "EndTimeUtc": "2022-02-22T16:01:00",
    "EntryNotes": "string",
    "DeletedOn": null
  }
]


### Data Processing
- Filters out entries where DeletedOn is not null
- Excludes entries with empty or null EmployeeName
- Handles time calculation edge cases (end time before start time)
- Groups entries by employee name
- Calculates total hours worked per employee

## 📸 Output Examples

### HTML Table Output
- *Professional table* with green header
- *Red highlighting* for employees under 100 hours
- *Summary statistics* dashboard
- *Hover effects* and responsive design
- *Modern styling* with gradients and shadows

### PIE Chart Output
- *1000x700 pixel PNG* image
- *Colorful pie slices* with distinct colors
- *Percentage labels* on larger slices
- *Detailed legend* with employee rankings
- *Summary statistics* panel
- *Professional layout* with title and metadata
