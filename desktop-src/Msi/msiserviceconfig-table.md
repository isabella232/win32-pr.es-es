---
description: La tabla MsiServiceConfig configura un servicio instalado o instalado por el paquete actual.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Tabla MsiServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169733"
---
# <a name="msiserviceconfig-table"></a>Tabla MsiServiceConfig

La tabla MsiServiceConfig configura un servicio instalado o instalado por el paquete actual.

**[Windows Installer 4.5 o versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite. Esta tabla está disponible a partir de Windows Installer 5.0.

La tabla MsiServiceConfig tiene las columnas siguientes.



| Columna           | Tipo                         | Clave | Nullable |
|------------------|------------------------------|-----|----------|
| MsiServiceConfig | [Identificador](identifier.md) | Y   | No        |
| Nombre             | [Formato](formatted.md)   | No   | No        |
| Evento            | [Entero](integer.md)       | No   | No        |
| ConfigType       | [Entero](integer.md)       | No   | No        |
| Argumento         | [Formato](formatted.md)   | No   | Y        |
| Componente\_      | [Identificador](identifier.md) | No   | No        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig
</dt> <dd>

Esta es la clave principal de esta tabla.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Esta columna contiene el nombre de un servicio que forma parte de este paquete o que ya está instalado.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Esta columna especifica cuándo se debe cambiar la configuración del servicio. Los valores siguientes se pueden combinar para representar varias operaciones. Se omiten todos los valores incluidos que no sean estos.



| Constante                                         | Descripción                                              |
|--------------------------------------------------|----------------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Realiza la acción durante la instalación del componente.   |
| **msidbServiceConfigEventUninstall** 2<br/> | Realiza la acción durante la desinstalación del componente. |
| **msidbServiceConfigEventReinstall** 4<br/> | Realiza la acción durante la reinstalación del componente. |



 

</dd> <dt>

<span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType
</dt> <dd>

El valor de este campo, combinado con el valor del campo Argumentos, especifica el cambio que se debe realizar en la configuración del servicio. El cambio especificado entra en vigor la próxima vez que se inicia el sistema.



| Config                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SERVICE \_ CONFIG \_ DELAYED \_ AUTO \_ START** 3<br/>       | Configure el retraso de tiempo de un [servicio de inicio automático.](../services/automatically-starting-services.md) <br/> Escriba 1 en el campo Argumento para iniciar el servicio después de otros servicios de inicio automático más un retraso de tiempo. <br/> Escriba 0 en el campo Argumento para desactivar el retraso del servicio de inicio automático.<br/> Solo se aplica a los servicios de inicio automático instalados por este paquete con **SERVICE \_ AUTO \_ START** en el campo StartType de la [tabla ServiceInstall](serviceinstall-table.md).<br/>                                                                         |
| **SERVICE \_ CONFIGURACIÓN DE \_ \_ PRIVILEGIOS NECESARIOS \_ INFO** 6<br/> | Cambie la lista de privilegios requeridos por el servicio.<br/> Escriba una lista de privilegios solicitados en el campo Argumento. El [valor Cadena con](formatted.md) formato del campo Argumento enumera las constantes de [**privilegios**](../secauthz/privilege-constants.md) para los privilegios solicitados. Puede usar la \[ ~ \] sintaxis de la cadena [con formato](formatted.md) para insertar un carácter nulo. Separe las constantes de privilegios de la lista por \[ ~ \] .<br/>                                                                                                                              |
| **SERVICE \_ CONFIG \_ SERVICE \_ SID \_ INFO** 5<br/>         | Agregue un tipo de SID de servicio al token de proceso que contiene este servicio.<br/> Escriba en el campo Argumento un tipo de SID de servicio válido para la estructura DE INFORMACIÓN DE SID DE SERVICIO: SERVICE [**\_ \_ SID**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) **TYPE \_ \_ \_ NONE** (0x00), **SERVICE \_ SID TYPE \_ \_ RESTRICTED** (0x03) o **SERVICE \_ SID TYPE \_ \_ UNRESTRICTED** (0x01). <br/>                                                                                                                                                                                                                                              |
| **SERVICE \_ CONFIG \_ PRESHUTDOWN \_ INFO** 7<br/>          | Configure el tiempo que el Administrador de [control](../services/service-control-manager.md) de servicios (SCM) espera antes de continuar con otras operaciones de apagado. El SCM espera durante este período de tiempo después de enviar la notificación **\_ DE \_ PRESHUTDOWN DE SERVICE CONTROL** al servicio. <br/> Escriba la longitud del retraso de tiempo, en milisegundos, en el campo Argumento. Deje vacío el campo Argumento para restablecer el retraso de tiempo al valor predeterminado de 3 minutos. <br/>                                                                                                                               |
| **SERVICE \_ MARCA 4 \_ DE ACCIONES DE ERROR \_ \_ DE** CONFIGURACIÓN<br/>     | Configure cuándo ejecutar las acciones de error para este servicio. Esta configuración se omite si el servicio no tiene ninguna acción de error configurada.<br/> Escriba 0 para ejecutar las acciones solo si el servicio finaliza sin notificar **SERVICE \_ STOPPED**.<br/> Escriba 1 para ejecutar las acciones si el servicio finaliza el informe **SERVICE \_ STOPPED** y el **miembro dwWin32ExitCode** de la estructura [**SERVICE \_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) no es **ERROR \_ SUCCESS**. Las acciones de error configuradas también se ejecutan si el servicio finaliza sin notificar **SERVICE \_ STOPPED**.<br/> |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento
</dt> <dd>

El valor de este campo, combinado con el valor del campo ConfigType, especifica qué cambio se debe realizar en la configuración del servicio. El cambio especificado entra en vigor la próxima vez que se inicia el sistema.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa a la columna Componente de la [tabla de componentes](component-table.md).

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE102](ice-102.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 
