---
description: La tabla MsiServiceConfig configura un servicio que está instalado o instalado por el paquete actual.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Tabla MsiServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668270"
---
# <a name="msiserviceconfig-table"></a>Tabla MsiServiceConfig

La tabla MsiServiceConfig configura un servicio que está instalado o instalado por el paquete actual.

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Esta tabla está disponible a partir de Windows Installer 5,0.

La tabla MsiServiceConfig tiene las columnas siguientes.



| Columna           | Tipo                         | Clave | Nullable |
|------------------|------------------------------|-----|----------|
| MsiServiceConfig | [Identificador](identifier.md) | Y   | N        |
| Nombre             | [Formatea](formatted.md)   | N   | N        |
| Evento            | [Entero](integer.md)       | N   | N        |
| ConfigType       | [Entero](integer.md)       | N   | N        |
| Argumento         | [Formatea](formatted.md)   | N   | Y        |
| Componente\_      | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig
</dt> <dd>

Esta es la clave principal de esta tabla.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Esta columna contiene el nombre de un servicio que forma parte de este paquete o que ya está instalado.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ceso
</dt> <dd>

Esta columna especifica cuándo se debe cambiar la configuración del servicio. Se pueden combinar los valores siguientes para representar varias operaciones. Se omiten los valores que no se incluyan.



| Constante                                         | Descripción                                              |
|--------------------------------------------------|----------------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Realiza la acción durante la instalación del componente.   |
| **msidbServiceConfigEventUninstall** 2<br/> | Realiza la acción durante la desinstalación del componente. |
| **msidbServiceConfigEventReinstall** 4<br/> | Realiza la acción durante la reinstalación del componente. |



 

</dd> <dt>

<span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType
</dt> <dd>

El valor de este campo, combinado con el valor del campo arguments, especifica qué cambio se debe hacer en la configuración del servicio. El cambio especificado tendrá efecto la próxima vez que se inicie el sistema.



| Config                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Servicio \_ de \_ \_ \_ Inicio automático retrasado de configuración** 3<br/>       | Configure el tiempo de espera de un [servicio de inicio automático](../services/automatically-starting-services.md). <br/> Escriba 1 en el campo argumento para iniciar el servicio después de otros servicios de inicio automático más un tiempo de retardo. <br/> Escriba 0 en el campo argumento para desactivar el retraso del servicio de inicio automático.<br/> Solo se aplica a los servicios de inicio automático instalados o a los servicios instalados por este paquete con **\_ \_ Inicio automático de servicio** en el campo StartType de la [tabla ServiceInstall](serviceinstall-table.md).<br/>                                                                         |
| **Servicio \_ de CONFIGURACIÓN \_ de \_ privilegios necesarios \_ información** 6<br/> | Cambiar la lista de privilegios necesarios para el servicio.<br/> Escriba una lista de privilegios solicitados en el campo argumento. El valor de cadena [con formato](formatted.md) en el campo argumento muestra las [**constantes de privilegio**](../secauthz/privilege-constants.md) para los privilegios solicitados. Puede usar la \[ ~ \] Sintaxis de la cadena [con formato](formatted.md) para insertar un carácter nulo. Separe las constantes de privilegio en la lista mediante \[ ~ \] .<br/>                                                                                                                              |
| **Servicio \_ de \_Información del \_ SID \_ del servicio de configuración** 5<br/>         | Agregue un tipo de SID de servicio al token de proceso que contiene este servicio.<br/> Escriba en el campo de argumento un tipo de SID de servicio válido para la estructura de [**\_ \_ información de SID de servicio**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) : tipo de SID de **servicio \_ \_ \_ ninguno** (0x00), **tipo de SID de servicio \_ \_ \_ restringido** (0x03) o **tipo de SID de servicio no \_ \_ \_ restringido** (0x01). <br/>                                                                                                                                                                                                                                              |
| **Servicio \_ de \_ \_ Información de preapagado de configuración** 7<br/>          | Configure la duración del tiempo que el [Administrador de control de servicios](../services/service-control-manager.md) (SCM) espera antes de continuar con otras operaciones de apagado. El SCM espera este período de tiempo después de enviar la notificación **de \_ \_ cierre del servicio** al servicio. <br/> Escriba la longitud del retraso de tiempo, en milisegundos, en el campo argumento. Deje el campo de argumento vacío para restablecer el tiempo de retardo en el valor predeterminado de 3 minutos. <br/>                                                                                                                               |
| **Servicio \_ de \_Marca de \_ acciones \_ de error de configuración** 4<br/>     | Configure Cuándo se deben ejecutar las acciones de error para este servicio. Este valor se omite si el servicio no tiene ninguna acción de error configurada.<br/> Escriba 0 para ejecutar las acciones solo si el servicio termina sin que se **\_ detenga el servicio** de informes.<br/> Escriba 1 para ejecutar las acciones si el servicio finaliza el servicio de informes **\_ detenido** y el miembro **dwWin32ExitCode** de la estructura de [**\_ Estado de servicio**](/windows/win32/api/winsvc/ns-winsvc-service_status) no es **\_ correcto**. También se ejecutan acciones de error configuradas si el servicio termina sin que se **\_ detenga el servicio** de informes.<br/> |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument
</dt> <dd>

El valor de este campo, combinado con el valor del campo ConfigType, especifica qué cambio se debe hacer en la configuración del servicio. El cambio especificado tendrá efecto la próxima vez que se inicie el sistema.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa para la columna componente de la [tabla componente](component-table.md).

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

 

 
