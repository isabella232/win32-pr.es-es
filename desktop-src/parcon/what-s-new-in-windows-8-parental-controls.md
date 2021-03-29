---
description: Proporciona información general sobre los cambios en los controles parentales de Windows introducidos en Windows 8.
ms.assetid: 7EB33215-8F8B-4EA4-87E6-A98F0D014548
title: Novedades en la seguridad de la familia de Windows 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2123ec7f0d9c3af66528c6c203a3e8ea64bd0384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909390"
---
# <a name="whats-new-in-windows-8-family-safety"></a>Novedades en la seguridad de la familia de Windows 8

## <a name="overview-of-parental-controls-changes-for-windows-8"></a>Información general de los cambios de controles parentales para Windows 8

El propósito de este documento es proporcionar una visión general de los cambios en el control parental de Windows en Windows 8 y permitir a los proveedores de soluciones de control parental de terceros aprovechar estos cambios. En este documento se da por supuesto que los lectores están familiarizados con los controles parentales para Windows 7 y Windows Vista, y solo reflejarán los cambios realizados en esta funcionalidad en Windows 8 que sean relevantes para el desarrollo de soluciones de control parental de terceros.

## <a name="key-design-decisions-for-windows-8-parental-controlfamily-safety-changes"></a>Decisiones de diseño clave para los cambios en el control parental y la seguridad de la familia de Windows 8

Los cambios en los controles parentales introducidos en Windows 8 continúan el objetivo de introducir mejoras en las características y, al mismo tiempo, promover la coexistencia de soluciones de control parental de terceros con la funcionalidad integrada. Los cambios son:

-   Uso de la seguridad de la familia de Microsoft para proporcionar administración remota y supervisión de actividades remotas.
-   Integración del filtrado web como parte de las restricciones de Microsoft y la capacidad de ver informes de actividad en un equipo con Windows 8.
-   Se ha cambiado el nombre de la característica de controles parentales del panel de control a seguridad de la familia y se hará referencia a ella como tal en este documento.
-   Las restricciones de tiempo integradas se han mejorado proporcionando la capacidad de controlar la cantidad total de tiempo por día que se puede usar (asignación de tiempo), además de la capacidad de controlar los tiempos en que se puede usar el equipo (Curfew). Curfew estaba disponible en versiones anteriores de Windows.
-   La funcionalidad de seguridad de la familia de Windows 8 se puede activar durante el flujo de creación de cuentas estándar.
-   Las características de extensibilidad de los controles parentales de Windows Vista y Windows 7 continúan siendo compatibles con la protección de la familia de Windows 8, incluida la capacidad de soluciones de terceros para reemplazar el filtro de contenido web o para reemplazar la interfaz de usuario de configuración integrada mientras sigue confiando en la implementación integrada de tiempo, aplicación, restricciones de juegos y filtro de contenido Web.
-   La activación de proveedores de terceros desactiva la administración remota y los informes de controles de seguridad de la familia de Windows 8 a través del sitio web de seguridad de la familia.
-   La extensibilidad de terceros para la protección infantil solo es compatible con las aplicaciones de escritorio de Windows 8.

## <a name="family-safety-and-standard-account-creation-in-windows-8"></a>Seguridad de la familia y creación de cuentas estándar en Windows 8

Como parte de la creación de cuentas estándar en Windows 8, un administrador tiene la capacidad de activar la supervisión de la cuenta por seguridad de la familia. A continuación se muestra una lista de la funcionalidad y la capacidad del proveedor de terceros para controlarla:

-   En la última pantalla del flujo de creación de cuentas estándar de Windows 8, se muestra un administrador con una casilla para activar la protección infantil de la cuenta recién creada.
-   Si esta casilla está activada, la protección de la familia está activada para la cuenta con la siguiente configuración:
    -   Informes de actividades en
    -   Todas las restricciones están desactivadas
-   Si el administrador usó un cuenta Microsoft para iniciar sesión en Windows, el equipo con Windows 8 se configurará para la administración remota de la configuración de seguridad de la familia y los informes de actividad de correo electrónico. El sitio web de seguridad de la familia se puede usar para administrar este tipo de equipo de forma remota.
-   Si el proveedor de terceros desea que la casilla esté presente en un flujo de creación de cuenta estándar, el siguiente valor debe estar presente entre los valores de registro del proveedor. Para obtener más información sobre los detalles de registro del proveedor, consulte la sección [registro del proveedor](what-s-new-in-windows-7-parental-controls.md) en el tema Novedades de los controles parentales de Windows 7.

    

    | Término                                                                                                                         | Descripción                                                                                                                                                                                                                                                                                  |
    |------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span id="AddUserVisible"></span><span id="adduservisible"></span><span id="ADDUSERVISIBLE"></span>AddUserVisible<br/> | Un valor **DWORD** distinto de cero opcional que especifica que la opción de casilla para activar la supervisión de la protección de la familia para una cuenta recién creada debe ser visible durante la creación de la cuenta estándar en Windows 8 después de que se seleccione el proveedor como proveedor de seguridad de la familia actual.<br/> |

    

     

-   Dado que los proveedores de terceros están diseñados para reemplazar la interfaz de usuario de configuración integrada para los controles de seguridad de la familia, de forma predeterminada, la instalación y la activación de un proveedor de terceros dará lugar a la opción casilla para activar la seguridad de la familia durante la creación de cuentas estándar que no se mostrará.

## <a name="family-safety-top-level-user-interface-changes-in-windows-8"></a>Cambios en la interfaz de usuario de nivel superior de protección infantil en Windows 8

Windows 8 lleva a cabo los siguientes cambios en la interfaz de usuario de nivel superior del panel de control de controles parentales:

-   Cuando los controles de seguridad de la familia integrados están activados para al menos una cuenta estándar en un equipo con Windows 8, se muestra el vínculo administrar la configuración del sitio web de seguridad familiar que permite a un administrador establecer la administración remota de la configuración de seguridad de la familia de equipos Windows 8 a través del sitio web de seguridad de la familia.
-   Cuando un equipo con Windows 8 está configurado para la administración remota a través del sitio web de seguridad de la familia, el control más información permite a un administrador deshabilitar la administración remota de un equipo con Windows 8 a través del sitio web de seguridad de la familia.
-   La sección de controles solo es visible cuando se registra al menos un proveedor de terceros con seguridad de familia. La interfaz de usuario y la funcionalidad de esta sección es idéntica a la sección controles adicionales en el control parental de Windows 7. Para obtener más información, consulte la sección controles parentales de la interfaz de usuario de nivel superior del tema [controles parentales de Windows 7](what-s-new-in-windows-7-parental-controls.md) .
-   Cuando se instala y selecciona un proveedor de terceros como el proveedor actual, se deshabilita la administración remota de la configuración de seguridad de la familia de equipos con Windows 8 a través del sitio web de seguridad de la familia.

## <a name="family-safety-in-box-restrictions-changes-in-windows-8"></a>Cambios en las restricciones de In-Box de seguridad de la familia en Windows 8

Windows 8 lleva a cabo los siguientes cambios en las restricciones de seguridad de la familia:

Restricciones Web

-   La implementación ha cambiado de un filtro de proveedor de servicios por capas (LSP) a un controlador de plataforma de filtrado de Windows (WFP) que se comunica con el proceso de supervisión de seguridad de la familia que se ejecuta en las sesiones de los usuarios.

Límites de tiempo

-   Las restricciones de tiempo integradas se han mejorado ofreciendo la posibilidad de controlar la cantidad total de tiempo por día que se puede usar (asignación de tiempo), además de la capacidad de controlar los tiempos en que se puede usar el equipo (Curfew), que estaba disponible en versiones anteriores de Windows.
-   La interfaz de usuario de Curfew permite un control independiente para cada día de la semana con granularidad de media hora.
-   La interfaz de usuario para la asignación de tiempo permite controles para los días laborables y fines de semana, o control independiente para cada día de la semana con una granularidad de 15 minutos.
-   El mecanismo de cambio rápido de usuario (FUS) ya no se usa para bloquear o bloquear el inicio de sesión del usuario controlado en un período de tiempo bloqueado. Para estos propósitos, se usa un conmutador a un escritorio independiente.
-   Los eventos de advertencia de desconexión ya no están disponibles para que las aplicaciones se suscriban a.

## <a name="family-safety-api-changes-in-windows-8"></a>Cambios de la API de seguridad de la familia en Windows 8

Las API que se usan para la protección de la familia exponen la Directiva y las restricciones en el cuadro y la funcionalidad de registro.

Registro

-   Los eventos personalizados ya no se admiten en el visor de informes de actividad de protección de la familia.

Escritura/lectura de la configuración de la API de WMI

-   WpcUserSettings: anteriormente, las restricciones de temporizador admitían una granularidad de 1 hora. En Windows 8, la propiedad existente representa la primera media hora de cada hora. Se ha agregado una nueva propiedad de media hour para representar la segunda mitad de cada hora. Se presentó una nueva propiedad adicional para representar la asignación de tiempo diaria.

Filtro de contenido web permitir/bloquear lista exportar/importar un formato

-   Filtro de contenido web: la funcionalidad de exportación de la lista de bloqueo ya no se admite.

Esquema de proveedor WMI de configuración de familia

-   Las siguientes adiciones se realizaron en la clase WpcUserSettings para reflejar las mejoras en las restricciones de tiempo:
    -   `[write: ToInstance ToSubClass, Description("Logon Half-Hours (30 minute offset) mask for this user"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 LogonHalfHours[7];`
    -   `[write: ToInstance ToSubClass, Description("Daily minute allowance"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 AllowanceMinutes[7];`

> [!Note]  
> Windows 8 usa una nueva clave del registro para indicar que la API de protección de la familia está habilitada para un usuario determinado.
>
> **HKLM** \\ **Microsoft** \\ **Software** \\ de **Windows** \\ **CurrentVersion** \\ Controles parentales  \\ **Usuarios** \\ de **{UserSid}** \\ **Web** \\ de **Filtrar por**

 

La siguiente clave del registro solo es compatible con Windows 7.

**HKLM** \\ **Microsoft** \\ **Software** \\ de **Windows** \\ **CurrentVersion** \\ Controles parentales  \\ **Usuarios** \\ de **{UserSid}** \\ **Controles parentales en**

Para ambas claves, un valor de "0x00" (**DWORD**) indica que la característica está deshabilitada para el usuario actual y un valor de "0x01" (**DWORD**) indica que la característica está habilitada para el usuario actual. Al intentar leer los valores de estas claves, reemplace el token "{UserSid}" por el identificador del sistema del usuario.

 

 




