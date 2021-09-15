---
description: Proporciona información general sobre los cambios en los controles Windows parentales introducidos en Windows 7.
ms.assetid: 5723fddd-52e2-46a1-a48f-647d479b21d9
title: Novedades de Windows 7 controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8282021c81ee8611fb7206d75f7e6aab48ebf2e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574685"
---
# <a name="whats-new-in-windows-7-parental-controls"></a>Novedades de los controles parentales Windows 7

## <a name="overview-of-parental-controls-changes-for-windows-7"></a>Introducción a los cambios en los controles parentales Windows 7

El propósito de este documento es proporcionar información general sobre los cambios en los controles parentales de Windows introducidos en Windows 7 y permitir que los proveedores de soluciones de control parental de terceros aprovechen estos cambios. En este documento se da por supuesto que los lectores están familiarizados con los controles parentales de Windows Vista y que solo reflejarán los cambios realizados en esta funcionalidad en Windows 7 que son pertinentes para el desarrollo de soluciones de control parental de terceros. Más adelante se realizará una actualización completa de la documentación Windows control parental de MSDN.

## <a name="key-design-decisions-for-windows-7-parental-control-changes"></a>Decisiones clave de diseño para Windows 7 cambios de control parental

Los cambios en los controles parentales introducidos en Windows 7 continúan el objetivo general de promover la coexistencia de soluciones de control parental de terceros con la funcionalidad integrada. Los cambios son:

-   Eliminación del filtrado web y los informes de actividad de la funcionalidad de controles parentales en cuadro. Los controles parentales de entrada proporcionan restricciones básicas implementadas por Microsoft sin conexión, como límites de tiempo, restricciones de aplicación y restricciones de juegos. Microsoft o soluciones de control parental de terceros pueden proporcionar el filtrado web, los informes de actividad y otras funcionalidades. Por ejemplo, Windows Live Protección infantil solución proporciona filtrado web, administración remota y supervisión de actividad, así como administración de contactos para todas las Windows Live.
-   Permitir que las soluciones de terceros reemplacen la interfaz de usuario de configuración del proveedor en el cuadro mientras se sigue basando en la implementación integrada de las restricciones de tiempo, aplicación y juego.
-   Permitir que un elemento primario o guardián (cuenta de administrador) pueda detectar y habilitar soluciones de terceros en el equipo.

## <a name="parental-controls-top-level-user-interface-changes-in-windows-7"></a>Controles parentales De nivel superior Interfaz de usuario cambios en Windows 7

Windows 7 incluye los siguientes cambios en la interfaz de usuario de Panel de control parental:

-   Se ha introducido la sección Controles adicionales, donde los controles que proporcionan funcionalidad adicional, como el filtrado web, los informes de actividad, entre otros, se pueden seleccionar en un cuadro de lista desplegable. Microsoft o proveedores de terceros deben registrar sus soluciones con Windows 7 Controles parentales para que se puedan seleccionar en el cuadro de lista desplegable Controles adicionales. Para obtener información sobre cómo registrar una solución, vea Registro del proveedor, más adelante en este tema).
-   La imagen de logotipo del proveedor seleccionado actualmente se muestra en la esquina superior derecha de la página.
-   Los iconos de usuario administrado pueden mostrar un resumen de la configuración parental proporcionada por el proveedor seleccionado actualmente.

El proveedor seleccionado actualmente podría optar por usar su propia interfaz de usuario para las pantallas de Control de usuarios para los usuarios administrados, o bien puede optar por confiar en la implementación de WPC integrada de esta pantalla. La implementación en cuadro tiene los siguientes cambios realizados en sus elementos:

-   Se quita la sección de informes de actividad.
-   Se quita el vínculo para ver los informes de actividad.

## <a name="parental-controls-api-overview-windows-7-changes"></a>Información general sobre la API de controles parentales: Windows 7 cambios

El mecanismo de integración para proveedores de soluciones de terceros se expandió para permitir lo siguiente:

-   Registro del proveedor. Tras el registro, un proveedor se puede seleccionar en el cuadro de lista desplegable Controles adicionales de la pantalla Controles parentales Panel de control pantalla.
-   Consulta del proveedor seleccionado actualmente. Se expone una interfaz COM pública para habilitar esta funcionalidad.
-   También es nuevo el conjunto de interfaces COM que los proveedores implementarán para permitir lo siguiente:
    -   Habilitar o deshabilitar el proveedor mediante WPC tras la selección por parte del usuario de controles adicionales.
    -   WPC para pasar el control al proveedor para configurar las opciones de control parental del usuario administrado.
    -   WPC para consultar al proveedor el resumen de la configuración de control parental del usuario administrado.

## <a name="third-party-provider-integration"></a>Integración de proveedores de terceros

### <a name="provider-registration"></a>Registro del proveedor

Para registrar un nuevo proveedor con controles parentales, se debe escribir un valor del Registro en la clave Proveedores Windows parentales. El nombre del valor es un GUID único que se usa para identificar el proveedor. Los datos de valor serán una ruta de acceso a una clave del Registro en **HKEY \_ LOCAL \_ MACHINE** que contiene información del proveedor.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Parental Controls
                  Providers
                     {45D63315-0824-4df4-B8A4-EF137D8810D1} = SOFTWARE\Microsoft\Family Safety\WPC\
```

En la ubicación de clave del Registro especificada, se esperan los valores siguientes.



| Término                                                                                                                 | Descripción                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LogoImage"></span><span id="logoimage"></span><span id="LOGOIMAGE"></span>**LogoImage**<br/>         | Ruta de acceso completa a un archivo binario de recursos con un identificador de recurso negativo para la imagen del logotipo del proveedor (almacenada como **image \_ bitmap).**<br/>                                                        |
| <span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**<br/> | Ruta de acceso completa a un archivo binario de recursos con un identificador de recurso negativo para el nombre del proveedor. **La longitud de DisplayName** no debe superar los 50 caracteres.<br/>                                       |
| <span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**<br/> | Ruta de acceso completa a un archivo binario de recursos con un identificador de recurso negativo para la descripción del proveedor. La longitud de la descripción no debe superar los 200 caracteres.<br/>                               |
| <span id="StateCLSID"></span><span id="stateclsid"></span><span id="STATECLSID"></span>**StateCLSID**<br/>     | Identificador de clase de la clase del proveedor que implementa IWPCProviderState.<br/>                                                                                                                     |
| <span id="ConfigCLSID"></span><span id="configclsid"></span><span id="CONFIGCLSID"></span>**ConfigCLSID**<br/> | Identificador de clase de la clase del proveedor, que implementa IWPCProviderConfig. **StateCLSID** y **ConfigCLSID** pueden ser iguales.<br/>                                                               |
| <span id="GRSVisible"></span><span id="grsvisible"></span><span id="GRSVISIBLE"></span>**GRSVisible**<br/>     | Valor **DWORD** distinto de cero opcional que especifica que Windows Parental Controls muestra un vínculo a la pantalla Game Rating System (Sistema de clasificación de juegos) después de seleccionar un proveedor como nuevo proveedor actual.<br/> |



 

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Family Safety
            WPC
               LogoImage = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40001
               DisplayName = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40002
               Description = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40003
               StateCLSID = {B4BAAE4D-3D86-4fa9-86F0-CF82C94D8A6A}
               ConfigCLSID = {B4BAAE4D-3D86-4fa9-86F0-CF82C94D8A6A}
               GRSVisible = 0x00000001 (1)
```

El control Controles parentales Panel de control los controles **LogoImage,** **DisplayName** y **Description** para cambiar la página principal de la ventana Controles parentales Panel de control cuando se selecciona ese proveedor. El **valor StateCLSID** se usa cuando el proveedor está habilitado o deshabilitado. El **valor ConfigCLSID** se usa cuando la interfaz de usuario obtiene información dinámica sobre cada usuario (este es solo el caso si el proveedor está seleccionado actualmente).

 

 




