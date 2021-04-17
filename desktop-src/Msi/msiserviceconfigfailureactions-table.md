---
description: En la tabla MsiServiceConfigFailureActions se enumeran las operaciones que se ejecutarán después de que se produzca un error en un servicio. Las operaciones especificadas en esta tabla se ejecutan la próxima vez que se inicia el sistema.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Tabla MsiServiceConfigFailureActions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae55d095e227611271de35d673289fc9eb5b174e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668269"
---
# <a name="msiserviceconfigfailureactions-table"></a>Tabla MsiServiceConfigFailureActions

En la tabla MsiServiceConfigFailureActions se enumeran las operaciones que se ejecutarán después de que se produzca un error en un servicio. Las operaciones especificadas en esta tabla se ejecutan la próxima vez que se inicia el sistema.

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Esta tabla está disponible a partir de Windows Installer 5,0.

La tabla MsiServiceConfigFailureActions tiene las columnas siguientes.



| Columna                         | Tipo                         | Clave | Nullable |
|--------------------------------|------------------------------|-----|----------|
| MsiServiceConfigFailureActions | [Identificador](identifier.md) | Y   | N        |
| Nombre                           | [Formatea](formatted.md)   | N   | N        |
| Evento                          | [Entero](integer.md)       | N   | N        |
| ResetPeriod                    | [Entero](integer.md)       | N   | Y        |
| RebootMessage                  | [Formatea](formatted.md)   | N   | Y        |
| Get-Help                        | [Formatea](formatted.md)   | N   | Y        |
| Acciones                        | [Texto](text.md)             | N   | Y        |
| DelayActions                   | [Texto](text.md)             | N   | Y        |
| Componente\_                    | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions
</dt> <dd>

Esta es la clave principal de esta tabla que identifica una acción de error.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Esta columna contiene el nombre de un servicio que forma parte de este paquete o que ya está instalado.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ceso
</dt> <dd>

Esta columna especifica cuándo se debe cambiar la configuración del servicio. Los valores siguientes son campos de bits que se pueden combinar para representar varias operaciones. Se omiten los demás valores de campo de bits.



| Constante                                         | Descripción                                     |
|--------------------------------------------------|-------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Cambiar durante la instalación del componente.    |
| **msidbServiceConfigEventUninstall** 2<br/> | Cambiar durante la desinstalación del componente.  |
| **msidbServiceConfigEventReinstall** 4<br/> | Cambiar durante la reinstalación del componente. |



 

</dd> <dt>

<span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod
</dt> <dd>

El período de restablecimiento en segundos del número de errores del servicio. El [Administrador de control de servicios](../services/service-control-manager.md) (SCM) cuenta el número de veces que se ha producido un error en cada servicio desde que el sistema se reinició por última vez. El recuento se restablece en cero si no se produce un error en el servicio durante el período de restablecimiento. Cuando se produce un error en el servicio durante el enésima tiempo, el sistema realiza la acción especificada en el elemento \[ N-1 \] de la matriz especificada en el campo acciones.

Deje vacío el campo ResetPeriod para indicar que el recuento de errores nunca debe restablecerse.

</dd> <dt>

<span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage
</dt> <dd>

Mensaje que se envía a los usuarios antes de reiniciar el equipo en respuesta a una acción de **\_ \_ reinicio de acción de SC** especificada en la columna actions. Puede usar una cadena vacía, "", para enviar el mensaje actual sin cambios. Puede utilizar \[ ~ \] la sintaxis del tipo de datos [con formato](formatted.md) para eliminar el mensaje actual y no enviar ningún mensaje.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command
</dt> <dd>

La línea de comandos ejecutada por el proceso creado por la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) en respuesta a una acción de comando de ejecución de la **\_ acción \_ \_ SC** especificada en la columna actions. El nuevo proceso se ejecuta en la misma cuenta que el servicio y solo si el campo acción **es \_ \_ \_ comando SC Action Run**. Puede usar una cadena vacía, "", para usar la línea de comandos actual sin modificar. Puede utilizar \[ ~ \] la sintaxis del tipo de datos [con formato](formatted.md) para eliminar la línea de comandos actual y no ejecutar ninguna operación cuando se produce un error en el servicio.

</dd> <dt>

<span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Operaciones
</dt> <dd>

Este campo contiene una matriz de valores enteros que especifican las acciones realizadas por el SCM si se produce un error en el servicio. Separe los valores de la matriz por \[ ~ \] . El valor entero del elemento n de la matriz especifica la acción que se realiza cuando se produce un error en el servicio durante el número de horas. Cada miembro de la matriz es uno de los siguientes valores enteros.



| Constante                                 | Descripción           |
|------------------------------------------|-----------------------|
| **SC \_ ACCIÓN \_ ninguno** 0<br/>         | No se requiere ninguna acción.            |
| **SC \_ ACCIÓN de \_ reinicio** 2<br/>       | Reinicie el equipo. |
| **SC \_ ACCIÓN de \_ reinicio** 1<br/>      | Reinicie el servicio.  |
| **SC \_ \_ \_ Comando de ejecución de acción** 3<br/> | Ejecutar un comando.        |



 

</dd> <dt>

<span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions
</dt> <dd>

Este campo contiene una matriz de valores enteros que especifican el tiempo en milisegundos que se debe esperar antes de realizar la acción especificada en la columna de acción. Separe los valores de la matriz por \[ ~ \] . El número de elementos de la matriz DelayActions debe ser igual al número de elementos de la matriz actions. El elemento n de la matriz DelayActions especifica el retardo de tiempo para el elemento n de la matriz actions.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa para la columna uno de la [tabla de componentes](component-table.md).

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

 

 
