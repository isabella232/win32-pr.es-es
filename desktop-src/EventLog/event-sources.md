---
description: Cada registro de la clave EventLog contiene subclaves denominadas orígenes de eventos. El origen del evento es el nombre del software que registra el evento.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Orígenes de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b408b76cdbc6e93e44099fea2842f9655a963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666971"
---
# <a name="event-sources"></a>Orígenes de eventos

Cada registro de la [clave EventLog](eventlog-key.md) contiene subclaves denominadas *orígenes de eventos*. El origen del evento es el nombre del software que registra el evento. Suele ser el nombre de la aplicación o el nombre de un subcomponente de la aplicación si la aplicación es grande. Puede Agregar un máximo de 16.384 orígenes de eventos al registro. El registro de **seguridad** es solo para uso del sistema. Los controladores de dispositivo deben agregar sus nombres al registro **del sistema** . Las aplicaciones y los servicios deben agregar sus nombres al registro de la **aplicación** o crear un registro personalizado.

La estructura de los orígenes de eventos es la siguiente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            EventLog
               Application
                  AppName
               Security
               System
                  DriverName
               CustomLog
                  AppName
```

No se puede usar un nombre de origen que ya se haya usado como nombre de registro. Además, los nombres de origen no pueden ser jerárquicos; es decir, no pueden contener el carácter de barra diagonal inversa (" \\ ").

Cada origen de eventos contiene información (por ejemplo, un [archivo de mensajes](message-files.md)) específica del software que registrará los eventos, tal como se muestra en la tabla siguiente.



<table>
<thead>
<tr class="header">
<th>Valor del registro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CategoryCount</strong></td>
<td>Número de categorías de eventos admitidas. Este valor es de tipo <strong>REG_DWORD</strong>.</td>
</tr>
<tr class="even">
<td><strong>CategoryMessageFile</strong></td>
<td>Ruta de acceso al archivo de mensajes de categoría. Un archivo de mensaje de categoría contiene cadenas dependientes del idioma que describen las categorías. Este valor puede ser de tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="odd">
<td><strong>EventMessageFile</strong></td>
<td>Ruta de acceso a uno o más archivos de mensajes de eventos; Use un punto y coma para delimitar varios archivos. Un archivo de mensajes de evento contiene cadenas dependientes del lenguaje que describen los eventos. Este valor puede ser de tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="even">
<td><strong>ParameterMessageFile</strong></td>
<td>Ruta de acceso al archivo de mensajes de parámetros. Un archivo de mensajes de parámetros contiene cadenas independientes del lenguaje que se van a insertar en las cadenas de Descripción del evento. Este valor puede ser de tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="odd">
<td><strong>TypesSupported</strong></td>
<td>Máscara de máscara de los tipos admitidos. Este valor es de tipo <strong>REG_DWORD</strong>. Puede ser uno o varios de los siguientes valores: <dl> <strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)<br />
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)<br />
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)<br />
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)<br />
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)<br />
</dl></td>
</tr>
</tbody>
</table>



 

Cuando una aplicación utiliza la función [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) o [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) para obtener un identificador de un registro de eventos, el servicio de registro de eventos busca el origen de eventos especificado en el registro. Por ejemplo, el registro de **aplicación** puede contener orígenes de eventos para Microsoft SQL Server y Microsoft Excel. Si una aplicación utiliza [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) o **OpenEventLog** con un nombre de origen de aplicación, SQL o Excel, el servicio de registro de eventos devuelve un identificador al registro de la **aplicación** .

Una aplicación puede utilizar el registro de **aplicaciones** sin agregar un nuevo origen de eventos al registro. Si la aplicación llama a [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) y pasa un nombre de origen que no se encuentra en el registro, el servicio de registro de eventos utiliza el registro de la **aplicación** de forma predeterminada. Sin embargo, dado que no hay archivos de mensajes, el Visor de eventos no puede asignar ningún identificador de evento o categoría de eventos a una cadena de descripción, y mostrará un error. Por esta razón, debe agregar un origen de eventos único al registro de la aplicación y especificar un archivo de mensaje.

 

 



