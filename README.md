## LIBRARY APP

## Descripción

Library App es una aplicación de consola diseñada para gestionar una biblioteca. Permite a los usuarios buscar y gestionar información sobre los usuarios de la biblioteca (patrons) y sus préstamos de libros (loans). La aplicación está estructurada en varias capas para mantener una separación clara de responsabilidades y mejorar la mantenibilidad y testabilidad del código.

## Estructura del Proyecto

```
AccelerateDevGitHubCopilot.sln
README.md
src/
    Library.ApplicationCore/
        Entities/
        Enums/
        Interfaces/
        Library.ApplicationCore.csproj
        Services/
    Library.Console/
        appSettings.json
        CommonActions.cs
        ConsoleApp.cs
        ConsoleState.cs
        Json/
        Library.Console.csproj
        Program.cs
    Library.Infrastructure/
        Data/
        Library.Infrastructure.csproj
tests/
    UnitTests/
        ApplicationCore/
        LoanFactory.cs
        PatronFactory.cs
```

## Clases Principales e Interfaces

### Library.ApplicationCore

- **Entities**: Contiene las clases de entidades principales como `Loan`, `Patron`, `Book`, `Author`, etc.
- **Enums**: Contiene enumeraciones utilizadas en la aplicación.
- **Interfaces**: Define contratos para los servicios y repositorios.
- **Services**: Contiene la implementación de los servicios de la aplicación.

### Library.Console

- **appSettings.json**: Archivo de configuración de la aplicación.
- **CommonActions.cs**: Define acciones comunes que pueden realizarse en la consola.
- **ConsoleApp.cs**: Clase principal que maneja la lógica de la interfaz de usuario de la aplicación de consola.
- **ConsoleState.cs**: Define los diferentes estados de la aplicación de consola.
- **Program.cs**: Punto de entrada de la aplicación de consola.

### Library.Infrastructure

- **Data**: Contiene la implementación de los repositorios que interactúan con los archivos JSON para almacenar y recuperar datos.

### UnitTests

- **LoanFactory.cs**: Clase de fábrica para crear instancias de `Loan` para pruebas.
- **PatronFactory.cs**: Clase de fábrica para crear instancias de `Patron` para pruebas.

## Cómo Usarlas

### ConsoleApp

La clase `ConsoleApp` es la clase principal que maneja la lógica de la interfaz de usuario de la aplicación de consola. Permite a los usuarios buscar y gestionar información sobre los usuarios de la biblioteca y sus préstamos.

```csharp
public class ConsoleApp
{
    public async Task Run()
    {
        // Lógica principal de la aplicación de consola
    }
}
```

### JsonPatronRepository

La clase `JsonPatronRepository` implementa la interfaz `IPatronRepository` y proporciona métodos para buscar, obtener y actualizar usuarios (patrons).

```csharp
public class JsonPatronRepository : IPatronRepository
{
    public async Task<List<Patron>> SearchPatrons(string searchInput)
    {
        // Lógica para buscar usuarios
    }

    public async Task<Patron?> GetPatron(int id)
    {
        // Lógica para obtener un usuario por su ID
    }

    public async Task UpdatePatron(Patron patron)
    {
        // Lógica para actualizar un usuario
    }
}
```

### JsonLoanRepository

La clase `JsonLoanRepository` implementa la interfaz `ILoanRepository` y proporciona métodos para obtener y actualizar préstamos (loans).

```csharp
public class JsonLoanRepository : ILoanRepository
{
    public async Task<Loan?> GetLoan(int id)
    {
        // Lógica para obtener un préstamo por su ID
    }

    public async Task UpdateLoan(Loan loan)
    {
        // Lógica para actualizar un préstamo
    }
}
```

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Para más detalles, consulte el archivo LICENSE en el repositorio.

Apolo11x: @workspace Generar contenido para el archivo readme.md de todo el repositorio de codigo actual. haga uso de  "Library App" como titulo de proyecto. el archivo readme debe contener informacion del proyecto en general como: Descripcion,  eStructuradel proyecto, Clases Principales e interfaces, como usarlas, la licencia de uso. formatee todas las secciones como un documento tipo markdown . Use etiquetas para las listas identando la estructura del proyecto. no incluya las carpetas ".gitignore" or the ".github", "bin", and "obj".

