---
description: Proporciona información general sobre los cambios en los controles parentales de Windows introducidos en Windows 7.
ms.assetid: 5723fddd-52e2-46a1-a48f-647d479b21d9
title: Novedades de controles parentales de Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8282021c81ee8611fb7206d75f7e6aab48ebf2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720606"
---
# <a name="whats-new-in-windows-7-parental-controls"></a>Novedades de los controles parentales de Windows 7

## <a name="overview-of-parental-controls-changes-for-windows-7"></a>Información general de los cambios de controles parentales para Windows 7

El propósito de este documento es proporcionar una visión general de los cambios en los controles parentales de Windows introducidos en Windows 7 y permitir a los proveedores de soluciones de control parental de terceros aprovechar estos cambios. En este documento se da por supuesto que los lectores están familiarizados con los controles parentales para Windows Vista y solo reflejarán los cambios realizados en esta funcionalidad en Windows 7, que son relevantes para el desarrollo de soluciones de control parental de terceros. En una fecha posterior, se mostrará una actualización completa de la documentación de control parental de Windows de MSDN.

## <a name="key-design-decisions-for-windows-7-parental-control-changes"></a>Decisiones de diseño clave para los cambios en el control parental de Windows 7

Los cambios en los controles parentales introducidos en Windows 7 continúan el objetivo de promover la coexistencia de soluciones de control parental de terceros con la funcionalidad integrada. Los cambios son:

-   Eliminación de los informes de actividad y filtrado web de la funcionalidad de controles parentales en la caja. Los controles parentales integrados proporcionan restricciones básicas implementadas por Microsoft, como los límites de tiempo, las restricciones de aplicaciones y las restricciones de juego. El filtrado web, la generación de informes de actividades y otras funciones las puede proporcionar Microsoft o soluciones de control parental de terceros. Por ejemplo, la solución de protección de la familia Windows Live proporciona filtrado web, administración remota y supervisión de actividades, así como la administración de contactos para todas las aplicaciones de Windows Live.
-   Habilitación de soluciones de terceros para reemplazar la interfaz de usuario de configuración del proveedor integrado mientras sigue confiando en la implementación integrada de tiempo, aplicación y restricciones de juegos.
-   Habilitación de soluciones de terceros para que las detecte un padre o tutor (cuenta de administrador).

## <a name="parental-controls-top-level-user-interface-changes-in-windows-7"></a>Cambios en la interfaz de usuario de nivel superior de los controles parentales en Windows 7

Windows 7 lleva a cabo los siguientes cambios en la interfaz de usuario de nivel superior del panel de control de controles parentales:

-   Se presenta la sección controles adicionales, donde los controles que proporcionan funcionalidad adicional, como el filtrado web, los informes de actividad, etc., se pueden seleccionar en un cuadro de lista desplegable. Los proveedores de Microsoft o de terceros deben registrar sus soluciones con controles parentales de Windows 7 para que se puedan seleccionar en el cuadro de lista desplegable controles adicionales. Para obtener información sobre cómo registrar una solución, vea registro del proveedor, más adelante en este tema.
-   La imagen del logotipo del proveedor seleccionado actualmente se muestra en la esquina superior derecha de la página.
-   Los iconos de usuario administrado pueden mostrar un resumen de la configuración parental proporcionada por el proveedor seleccionado actualmente.

El proveedor seleccionado actualmente puede optar por usar su propia interfaz de usuario para las pantallas de control de usuario para los usuarios administrados, o bien puede seleccionar confiar en la implementación de WPC en el cuadro de esta pantalla. La implementación integrada tiene los siguientes cambios realizados en sus elementos:

-   Se quita la sección informes de actividades.
-   Se quita el vínculo para ver los informes de actividad.

## <a name="parental-controls-api-overview-windows-7-changes"></a>Información general sobre la API de controles parentales: cambios de Windows 7

El mecanismo de integración de proveedores de soluciones de terceros se amplió para permitir:

-   Registro del proveedor. Tras el registro, un proveedor se vuelve seleccionable en el cuadro de lista desplegable controles adicionales en la pantalla del panel de control de controles parentales.
-   Consulta para el proveedor seleccionado actualmente. Se expone una interfaz COM pública para habilitar esta funcionalidad.
-   También es nuevo el conjunto de interfaces COM que implementarán los proveedores para permitir:
    -   Habilitación o deshabilitación del proveedor WPC al seleccionar el usuario de controles adicionales.
    -   WPC para pasar el control al proveedor con el fin de configurar los valores del control parental del usuario administrado.
    -   WPC para consultar al proveedor el Resumen de la configuración del control parental del usuario administrado.

## <a name="third-party-provider-integration"></a>Integración de proveedores de terceros

### <a name="provider-registration"></a>Registro del proveedor

Para registrar un nuevo proveedor con controles parentales, se debe escribir un valor del registro en la clave de proveedores de controles parentales de Windows. El nombre del valor es un GUID único que se utiliza para identificar el proveedor. Los datos del valor serán una ruta de acceso a una clave del registro en el **\_ \_ equipo local HKEY** que contiene información del proveedor.

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

En la ubicación de la clave del registro especificada, se esperan los siguientes valores.



| Término                                                                                                                 | Descripción                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LogoImage"></span><span id="logoimage"></span><span id="LOGOIMAGE"></span>**LogoImage**<br/>         | Ruta de acceso completa a un archivo binario de recursos con un identificador de recurso negativo para la imagen del logotipo del proveedor (almacenado como un **\_ mapa de bits de imagen**).<br/>                                                        |
| <span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Mostrar**<br/> | Ruta de acceso completa a un archivo binario de recursos con un identificador de recurso negativo para el nombre del proveedor. La longitud de **displayName** no debe superar los 50 caracteres.<br/>                                       |
| <span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**<br/> | Ruta de acceso completa a un archivo binario de recursos con un identificador de recurso negativo para la descripción del proveedor. La longitud de la descripción no debe superar los 200 caracteres.<br/>                               |
| <span id="StateCLSID"></span><span id="stateclsid"></span><span id="STATECLSID"></span>**StateCLSID**<br/>     | IDENTIFICADOR de clase de la clase del proveedor que implementa IWPCProviderState.<br/>                                                                                                                     |
| <span id="ConfigCLSID"></span><span id="configclsid"></span><span id="CONFIGCLSID"></span>**ConfigCLSID**<br/> | IDENTIFICADOR de clase de la clase del proveedor, que implementa IWPCProviderConfig. **StateCLSID** y **ConfigCLSID** pueden ser iguales.<br/>                                                               |
| <span id="GRSVisible"></span><span id="grsvisible"></span><span id="GRSVISIBLE"></span>**GRSVisible**<br/>     | Valor **DWORD** opcional distinto de cero que especifica que el control parental de Windows muestra un vínculo a la pantalla del sistema de clasificación de juego después de seleccionar un proveedor como el nuevo proveedor actual.<br/> |



 

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

El panel de control de controles parentales usa **LogoImage**, **displayName** y **Description** para cambiar la Página principal del panel de control de controles parentales cuando se selecciona ese proveedor. El valor **StateCLSID** se usa cuando el proveedor está habilitado o deshabilitado. El valor **ConfigCLSID** se usa cuando la interfaz de usuario obtiene información dinámica sobre cada usuario (es solo el caso si el proveedor está seleccionado actualmente).

 

 




