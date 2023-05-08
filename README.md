# KYH-BLAZOR

Demo projekt för att visa en del av vad man kan utveckla med blazor utan att använda javascript

## Teknik

Detta projekt använder följande tekniker

- Entity Framework with MS SQLSERVER
- .net7
- Signal R
- Webassembly

## Krav för att köra projektet

- SQL Server
- .net 7 runtime
- Visual Studio 2022

## Struktur

En Solution som innehåller 4 projekt enligt följande.

### BlazorDemo.Backend

En class bibliotek projekt som sköter backend delen som databas anslutningen och services som ansvarar för att prata med databasen åt klienten.

Detta innehåller även några DTO modeller och en AutoMapper config.

### BlazorDemo.Server (Går att starta)

Detta är en blazor server projekt som har en referens till BlazorDemo.Backend projektet.
Projektet har en appsetting.json fil som innehåller ConnectionString för databasen, detta behöver ni anpassa för att kunna köra detta projekt.

### BlazorDemo.WebAssembly.Client

Detta är en blazor WebAssembly projekt som körs i klienten.

### BlazorDemo.WebAssembly.Server (Går att starta)

Detta är i praktiken en WebAPI projekt som också serverar våra WebAssembly Projektet till klienten.
För att starta WebAssembly Projekten behöver man starta detta projekt bara så körs även "BlazorDemo.WebAssembly.Client" också.
Man behöver anpassa ConnectionString i appsettings.json för att få detta att fungera ordentligt.
