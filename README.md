# Add a MultiSelect Dropdown to a Blazor WebAssembly App

## Overview

This sample demonstrates how to integrate the Syncfusion [Blazor MultiSelect Dropdown](https://www.syncfusion.com/blazor-components/blazor-multiselect-dropdown) into a hosted Blazor WebAssembly application. The application shows how to present selectable data using a multi-selection interface and illustrates working with both local and remote data sources.

The sample is intended as a starting point for developers who want to implement multi-value selection scenarios in Blazor applications while customizing the appearance and behavior of the dropdown popup.

## Key Features

- Configures `TValue="string[]"` to support multiple selected values.
- Uses a strongly typed data source through the `GamesDataModel` class.
- Binds local collection data using the `DataSource="@GamesData"` property.
- Maps display and value fields through `MultiSelectFieldSettings` with:
  - `Text="Name"`
  - `Value="ID"`
- Displays a placeholder using `Placeholder="Select a game"`.
- Customizes the dropdown popup dimensions with:
  - `PopupHeight="450px"`
  - `PopupWidth="250px"`
- Demonstrates multi-selection of sports items such as Badminton, Basketball, Cricket, Football, Golf, Hockey, and Tennis.
- Includes a responsive container (`control_wrapper`) to position and size the MultiSelect component within the page layout.
- Contains a hosted ASP.NET Core Web API endpoint (`WeatherForecastController`) that returns sample weather forecast data.
- Demonstrates server-to-client data retrieval using `HttpClient.GetFromJsonAsync<WeatherForecast[]>()` in the `FetchData` page.
- Displays weather forecast data in a tabular format after fetching it from the server API.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download this repository.
2. Open the solution file:

   `MultiSelectDropDownSample.sln`

3. Restore NuGet packages.
4. Build the solution.
5. If required, set the hosted server project as the startup project.
6. Run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Open the repository folder in Visual Studio Code.
2. Navigate to the project directory.

```bash
dotnet restore
dotnet run
```

3. Open the URL displayed in the console after the application starts.

## Project Structure

- `MultiSelectDropDownSample.sln` - Solution file containing the hosted Blazor WebAssembly sample.
- `Client/Pages/Index.razor` - Main sample page that renders the Syncfusion MultiSelect Dropdown, defines the `GamesDataModel` data model, provides the local sports data source, and configures popup dimensions.
- `Client/Pages/FetchData.razor` - Demonstrates consuming the server API using `HttpClient` and displays weather forecast data in a table.
- `Server/Controllers/WeatherForecastController.cs` - ASP.NET Core Web API controller that generates and returns sample weather forecast records used by the FetchData page.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Official documentation: https://blazor.syncfusion.com/documentation/multiselect-dropdown/getting-started

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.