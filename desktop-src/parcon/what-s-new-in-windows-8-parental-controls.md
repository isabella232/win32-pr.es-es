---
description: Proporciona información general sobre los cambios en el Windows parentales introducidos en Windows 8.
ms.assetid: 7EB33215-8F8B-4EA4-87E6-A98F0D014548
title: Novedades de la seguridad Windows 8 familia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2123ec7f0d9c3af66528c6c203a3e8ea64bd0384
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268444"
---
# <a name="whats-new-in-windows-8-family-safety"></a>Novedades de la seguridad Windows 8 familia

## <a name="overview-of-parental-controls-changes-for-windows-8"></a>Introducción a los cambios en los controles parentales Windows 8

El propósito de este documento es proporcionar información general sobre los cambios en los controles parentales de Windows en Windows 8 y permitir que los proveedores de soluciones de control parental de terceros aprovechen estos cambios. En este documento se da por supuesto que los lectores están familiarizados con los controles parentales para Windows 7 y Windows Vista y solo reflejarán los cambios realizados en esta funcionalidad en Windows 8 que son pertinentes para el desarrollo de soluciones de control parental de terceros.

## <a name="key-design-decisions-for-windows-8-parental-controlfamily-safety-changes"></a>Decisiones clave de diseño para Windows 8 control parental o cambios de seguridad familiar

Los cambios en los controles parentales introducidos en Windows 8 continúan el objetivo general de introducir mejoras de características y, al mismo tiempo, promover la coexistencia de soluciones de control parental de terceros con la funcionalidad integrada. Los cambios son:

-   Uso de Microsoft Family Safety para proporcionar administración remota y supervisión remota de la actividad.
-   Integración del filtrado web como parte de las restricciones de Microsoft y la capacidad de ver informes de actividad en Windows 8 equipo.
-   La característica Controles parentales de la Panel de control se ha cambiado a Seguridad familiar y se hará referencia como tal a lo largo de este documento.
-   Las restricciones de tiempo incluidas se mejoraron al proporcionar la capacidad de controlar la cantidad total de tiempo al día que se puede usar el equipo (asignación de tiempo), además de la capacidad de controlar las horas en las que se puede usar el equipo (toque de queda). El toque de queda estaba disponible en versiones anteriores de Windows.
-   Windows 8 La funcionalidad de seguridad de familia se puede desactivar durante el flujo de creación de cuentas estándar.
-   Windows Las características de extensibilidad de los controles parentales de Vista y Windows 7 siguen siendo compatibles con la seguridad de la familia de Windows 8, incluida la capacidad de las soluciones de terceros para reemplazar el filtro de contenido web o reemplazar la interfaz de usuario de configuración integrada mientras se sigue basando en la implementación integrada de Tiempo, Aplicación, Restricciones de juegos y Filtro de contenido web.
-   La activación de proveedores de terceros desactiva la administración remota y la generación de informes de Windows 8 seguridad familiar a través del sitio web de seguridad familiar.
-   La extensibilidad de terceros para la seguridad de familia solo se admite Windows 8 aplicaciones de escritorio.

## <a name="family-safety-and-standard-account-creation-in-windows-8"></a>Seguridad para la familia y creación de cuentas estándar en Windows 8

Como parte de la creación de cuentas estándar en Windows 8, un administrador tiene la capacidad de activar la supervisión de la cuenta por seguridad familiar. A continuación se muestra una lista de la funcionalidad y la capacidad del proveedor de terceros para controlarla:

-   En la última pantalla de Windows 8 flujo de creación de cuentas estándar, se muestra a un administrador una casilla para activar La seguridad de familia para la cuenta recién creada.
-   Si esta casilla está activada, La seguridad de la familia está activada para la cuenta con la siguiente configuración:
    -   Informe de actividades en
    -   Todas las restricciones están desactivadas
-   Si el administrador usó una cuenta Microsoft para iniciar sesión en Windows, el equipo Windows 8 se configurará para la administración remota de la configuración de seguridad familiar y los informes de actividad de correo electrónico. A continuación, se puede usar el sitio web de seguridad para familias para administrar este tipo de equipo de forma remota.
-   Si el proveedor de terceros desea que la casilla esté presente en un flujo de creación de cuentas estándar, el siguiente valor debe estar presente entre los valores de registro del proveedor. Para obtener más información sobre [](what-s-new-in-windows-7-parental-controls.md) los detalles de registro del proveedor, vea la sección Registro del proveedor en el tema Novedades de Windows 7 Parental Controls .

    

    | Término                                                                                                                         | Descripción                                                                                                                                                                                                                                                                                  |
    |------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span id="AddUserVisible"></span><span id="adduservisible"></span><span id="ADDUSERVISIBLE"></span>AddUserVisible<br/> | Un valor **DWORD** distinto de cero opcional que especifica que la opción de casilla para activar la supervisión de seguridad familiar para una cuenta recién creada debe estar visible durante la creación de la cuenta estándar en Windows 8 después de seleccionar el proveedor como proveedor de seguridad de familia actual.<br/> |

    

     

-   Dado que los proveedores de terceros están diseñados para reemplazar la interfaz de usuario de configuración en cuadro para los controles de seguridad familiar, de forma predeterminada, la instalación y activación de un proveedor de terceros dará lugar a la opción de casilla para activar la seguridad de familia durante la creación de cuentas estándar que no se mostrará.

## <a name="family-safety-top-level-user-interface-changes-in-windows-8"></a>Cambios de nivel superior de seguridad Interfaz de usuario familia en Windows 8

Windows 8 incluye los siguientes cambios en la interfaz de usuario de Panel de control parental:

-   Cuando se activen los controles de seguridad de familia en el cuadro para al menos una cuenta estándar en un equipo de Windows 8, se muestra el vínculo de comando Administrar la configuración en el sitio web de seguridad familiar que permite Windows 8 a un administrador establecer la administración remota de la configuración de seguridad de la familia de un equipo a través del sitio web de seguridad familiar.
-   Cuando un equipo Windows 8 está configurado para la administración remota a través del sitio web de seguridad familiar, el control Más información permite a un administrador deshabilitar la administración remota de un equipo Windows 8 a través del sitio web de seguridad familiar.
-   La sección Controles solo es visible cuando al menos un proveedor de terceros está registrado con seguridad de familia. La interfaz de usuario y la funcionalidad de esta sección son idénticas a la sección Controles adicionales Windows 7 Controles parentales. Para obtener más información, vea la sección Cambios en la interfaz de usuario de nivel superior de Los controles parentales [del tema Windows 7 Parental Controls](what-s-new-in-windows-7-parental-controls.md) .
-   Cuando se instala y selecciona un proveedor de terceros como proveedor actual, se deshabilita la administración remota de la configuración de seguridad familiar de Windows 8 equipo a través del sitio web de seguridad familiar.

## <a name="family-safety-in-box-restrictions-changes-in-windows-8"></a>Cambios en las restricciones de seguridad In-Box familia en Windows 8

Windows 8 incluye los siguientes cambios en las restricciones de seguridad en familia:

Restricciones web

-   La implementación ha cambiado de un filtro de proveedor de servicios por capas (LSP) a un controlador de Windows Filtering Platform (WFP) que se comunica con el proceso de supervisión de seguridad familiar que se ejecuta en las sesiones de los usuarios.

Límites de tiempo

-   Las restricciones de tiempo incluidas se mejoraron al proporcionar la capacidad de controlar la cantidad total de tiempo al día que se puede usar el equipo (asignación de tiempo), además de la capacidad de controlar las horas en las que se puede usar el equipo (toque de queda), que estaba disponible en versiones anteriores de Windows.
-   La interfaz de usuario para el toque de queda permite un control independiente para cada día de la semana con granularidad de media hora.
-   La interfaz de usuario para la asignación de tiempo permite controles para días laborables o fines de semana o control independiente para cada día de la semana con granularidad de 15 minutos.
-   El mecanismo de cambio rápido de usuario (FUS) ya no se usa para bloquear o bloquear el inicio de sesión del usuario controlado cuando se encuentra bloqueado. Para estos fines se usa un conmutador a un escritorio independiente.
-   Los eventos de advertencia de desconexión ya no están disponibles para que las aplicaciones se suscriban.

## <a name="family-safety-api-changes-in-windows-8"></a>Cambios en la API de seguridad de familia en Windows 8

Las API que se usan para la seguridad de familia exponen la configuración de restricciones integradas y la directiva, así como la funcionalidad de registro.

Registro

-   Los eventos personalizados ya no se admiten en el visor de informes de actividad de seguridad familiar.

Lectura y escritura Configuración API WMI

-   WpcUserSettings: anteriormente, las restricciones de temporizador admiten una granularidad de 1 hora. En Windows 8 la propiedad existente representa la primera media hora para cada hora. Se ha agregado una nueva propiedad de media hora para representar la segunda mitad de cada hora. Se introdujo una nueva propiedad adicional para representar la asignación de tiempo diaria.

Filtro de contenido web Allow/Block List Export/Import A Format

-   Ya no se admite la funcionalidad allow/block list export del filtro de contenido web.

Esquema de proveedor WMI Configuración familia

-   Se realizaron las siguientes adiciones a la clase WpcUserSettings para reflejar las mejoras de restricciones de tiempo:
    -   `[write: ToInstance ToSubClass, Description("Logon Half-Hours (30 minute offset) mask for this user"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 LogonHalfHours[7];`
    -   `[write: ToInstance ToSubClass, Description("Daily minute allowance"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 AllowanceMinutes[7];`

> [!Note]  
> Windows 8 usa una nueva clave del Registro para indicar que Family Safety API está habilitada para un usuario determinado.
>
> **HKLM** \\ **Microsoft** \\ **Software** \\ **Windows** \\ **CurrentVersion** \\ **Controles parentales** \\ **Usuarios** \\ **{UserSid}** \\ **Web** \\ **Filtrar por**

 

La siguiente clave del Registro solo se admite Windows 7.

**HKLM** \\ **Microsoft** \\ **Software** \\ **Windows** \\ **CurrentVersion** \\ **Controles parentales** \\ **Usuarios** \\ **{UserSid}** \\ **Controles parentales en**

Para ambas claves, un valor de "0x00"**(DWORD**) indica que la característica está deshabilitada para el usuario actual y un valor de "0x01"**(DWORD)** indica que la característica está habilitada para el usuario actual. Al intentar leer los valores de estas claves, reemplace el token "{UserSid}" por el identificador del sistema del usuario.

 

 




