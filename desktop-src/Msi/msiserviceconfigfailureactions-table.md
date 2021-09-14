---
description: En la tabla MsiServiceConfigFailureActions se enumeran las operaciones que se ejecutarán después de que se produce un error en un servicio. Las operaciones especificadas en esta tabla se ejecutan la próxima vez que se inicia el sistema.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Tabla MsiServiceConfigFailureActions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae55d095e227611271de35d673289fc9eb5b174e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161492"
---
# <a name="msiserviceconfigfailureactions-table"></a>Tabla MsiServiceConfigFailureActions

En la tabla MsiServiceConfigFailureActions se enumeran las operaciones que se ejecutarán después de que se produce un error en un servicio. Las operaciones especificadas en esta tabla se ejecutan la próxima vez que se inicia el sistema.

**[Windows instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Esta tabla está disponible a partir de Windows Installer 5.0.

La tabla MsiServiceConfigFailureActions tiene las columnas siguientes.



| Columna                         | Tipo                         | Clave | Nullable |
|--------------------------------|------------------------------|-----|----------|
| MsiServiceConfigFailureActions | [Identificador](identifier.md) | Y   | No        |
| Nombre                           | [Formato](formatted.md)   | No   | No        |
| Evento                          | [Entero](integer.md)       | No   | No        |
| ResetPeriod                    | [Entero](integer.md)       | No   | Y        |
| RebootMessage                  | [Formato](formatted.md)   | No   | Y        |
| Get-Help                        | [Formato](formatted.md)   | No   | Y        |
| Acciones                        | [Texto](text.md)             | No   | Y        |
| DelayActions                   | [Texto](text.md)             | No   | Y        |
| Componente\_                    | [Identificador](identifier.md) | No   | No        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions
</dt> <dd>

Esta es la clave principal de esta tabla que identifica una acción de error.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Esta columna contiene el nombre de un servicio que forma parte de este paquete o que ya está instalado.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Esta columna especifica cuándo se debe cambiar la configuración del servicio. Los siguientes valores son campos de bits que se pueden combinar para representar varias operaciones. Se omiten los demás valores de campo de bits.



| Constante                                         | Descripción                                     |
|--------------------------------------------------|-------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Cambie durante la instalación del componente.    |
| **msidbServiceConfigEventUninstall** 2<br/> | Cambie durante la desinstalación del componente.  |
| **msidbServiceConfigEventReinstall** 4<br/> | Cambie durante la re-instalación del componente. |



 

</dd> <dt>

<span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod
</dt> <dd>

Período de restablecimiento en segundos del recuento de errores del servicio. El [Administrador de control de](../services/service-control-manager.md) servicios (SCM) cuenta el número de veces que cada servicio ha dado error desde que se reinició por última vez el sistema. El recuento se restablece a cero si el servicio no da error durante el período de restablecimiento. Cuando se produce un error en el servicio por enésima vez, el sistema realiza la acción especificada en el elemento N-1 de la matriz especificada en el \[ \] campo Acciones.

Deje el campo ResetPeriod vacío para indicar que nunca se debe restablecer el recuento de errores.

</dd> <dt>

<span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage
</dt> <dd>

Mensaje enviado a los usuarios antes de reiniciar el equipo en respuesta a una acción **DE SC \_ ACTION \_ REBOOT** especificada en la columna Acciones. Puede usar una cadena vacía, "", para enviar el mensaje actual sin cambios. Puede usar la \[ ~ \] sintaxis del tipo de datos [Formatted](formatted.md) para eliminar el mensaje actual y no enviar ningún mensaje.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Comando
</dt> <dd>

Línea de comandos ejecutada por el proceso creado por la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) en respuesta a una acción **RUN \_ \_ \_ COMMAND** de SC ACTION especificada en la columna Acciones. El nuevo proceso se ejecuta en la misma cuenta que el servicio y solo si el campo Acción es **SC \_ ACTION RUN \_ \_ COMMAND**. Puede usar una cadena vacía, "", para usar la línea de comandos actual sin cambios. Puede usar la sintaxis del tipo de datos Formatted para eliminar la línea de comandos actual y no ejecutar ninguna operación cuando se produce un error \[ ~ \] en el servicio. [](formatted.md)

</dd> <dt>

<span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Acciones
</dt> <dd>

Este campo contiene una matriz de valores enteros que especifican las acciones realizadas por el SCM si se produce un error en el servicio. Separe los valores de la matriz por \[ ~ \] . El valor entero del enésimo elemento de la matriz especifica la acción realizada cuando se produce un error en el servicio por enésima vez. Cada miembro de la matriz es uno de los siguientes valores enteros.



| Constante                                 | Descripción           |
|------------------------------------------|-----------------------|
| **SC \_ ACCIÓN \_ NONE** 0<br/>         | No se requiere ninguna acción.            |
| **SC \_ ACTION \_ REBOOT** 2<br/>       | Reinicie el equipo. |
| **SC \_ ACTION \_ RESTART** 1<br/>      | Reinicie el servicio.  |
| **SC \_ COMANDO \_ ACTION RUN \_** 3<br/> | Ejecute un comando.        |



 

</dd> <dt>

<span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions
</dt> <dd>

Este campo contiene una matriz de valores enteros que especifican el tiempo en milisegundos que se debe esperar antes de realizar la acción especificada en la columna Acción. Separe los valores de la matriz por \[ ~ \] . El número de elementos de la matriz DelayActions debe ser igual al número de elementos de la matriz Actions. El enésimo elemento de la matriz DelayActions especifica el retraso de tiempo para el enésimo elemento de la matriz Actions.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
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

 

 
