# MyMvcApp-Contact-Database-Application

## Descripción

MyMvcApp-Contact-Database-Application es una aplicación ASP.NET Core MVC diseñada para gestionar una base de datos de contactos. Esta aplicación incluye funcionalidades para crear, leer, actualizar y eliminar contactos.

## Estructura del Proyecto

El proyecto está organizado de la siguiente manera:

```
MyMvcApp-Contact-Database-Application/
    appsettings.Development.json
    appsettings.json
    deploy.json
    deploy.parameters.json
    MyMvcApp.csproj
    MyMvcApp.sln
    Program.cs
    README.md
    .github/
        workflows/
    .vscode/
        launch.json
        tasks.json
    bin/
        Debug/
    Controllers/
        UserController.cs
    Models/
        ErrorViewModel.cs
        User.cs
    obj/
        MyMvcApp.csproj.nuget.dgspec.json
    Properties/
    Views/
    wwwroot/
MyMvcApp.Tests/
    MyMvcApp.Tests.csproj
    UserControllerTests.cs
    bin/
    obj/
```

## Requisitos

- .NET 8.0 SDK
- Visual Studio Code o Visual Studio 2022
- Una cuenta de Azure para el despliegue

## Configuración

1. Clona el repositorio:
    ```sh
    git clone https://github.com/tu-usuario/MyMvcApp-Contact-Database-Application.git
    cd MyMvcApp-Contact-Database-Application
    ```

2. Restaura los paquetes NuGet:
    ```sh
    dotnet restore
    ```

3. Configura las variables de entorno en `appsettings.json` y `appsettings.Development.json` según tus necesidades.

## Construcción y Ejecución

Para construir y ejecutar la aplicación localmente:

1. Construye la aplicación:
    ```sh
    dotnet build --configuration Release
    ```

2. Publica la aplicación:
    ```sh
    dotnet publish -c Release -o "bin/Release/net8.0/MyMvcApp"
    ```

3. Ejecuta la aplicación:
    ```sh
    dotnet run
    ```

## Pruebas

Para ejecutar las pruebas unitarias:

1. Navega al directorio de pruebas:
    ```sh
    cd MyMvcApp.Tests
    ```

2. Ejecuta las pruebas:
    ```sh
    dotnet test
    ```

## Despliegue en Azure

El proyecto incluye un flujo de trabajo de GitHub Actions para desplegar la aplicación en Azure Web App.

1. Configura los secretos de GitHub con tus credenciales de Azure:
    - `AZUREAPPSERVICE_CLIENTID`
    - `AZUREAPPSERVICE_TENANTID`
    - `AZUREAPPSERVICE_SUBSCRIPTIONID`

2. El flujo de trabajo de GitHub Actions se encuentra en `.github/workflows/master_mymvcapplj.yml`. Este flujo de trabajo se ejecuta en cada push a la rama `master` y despliega la aplicación en Azure.

## Contribución

1. Haz un fork del repositorio.
2. Crea una nueva rama (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza tus cambios y haz commit (`git commit -am 'Añadir nueva funcionalidad'`).
4. Haz push a la rama (`git push origin feature/nueva-funcionalidad`).
5. Abre un Pull Request.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.
