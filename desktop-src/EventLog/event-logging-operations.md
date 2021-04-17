---
description: Las funciones OpenEventLog, OpenBackupEventLog, RegisterEventSource, DeregisterEventSource y CloseEventLog abren y cierran los identificadores de registro de eventos.
ms.assetid: e42a66c2-2f1e-46f8-99c7-4701075c8ec3
title: Operaciones de registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065acd268788de8c9674baa1fe47a3b89a719d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687379"
---
# <a name="event-logging-operations"></a>Operaciones de registro de eventos

Las funciones [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga), [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga), [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea), [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)y [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog) abren y cierran los identificadores de registro de eventos.

En la tabla siguiente se muestran las operaciones que se pueden realizar en un registro de eventos abierto y la función correspondiente para cada operación.



| Operación | Función                                                                                                                     |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| Copia de seguridad    | [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                                                                                     |
| Borrar     | [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                                                                                       |
| Supervisión   | [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)                                                                         |
| Consultar     | [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord), [ **GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) |
| Lectura      | [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                                                                                         |
| Escritura     | [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                                                                                           |



 

Las funciones [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) y [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) toman un nombre de servidor opcional como parámetro, por lo que las operaciones se pueden realizar en el servidor remoto. Use [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) para leer o realizar operaciones administrativas (copia de seguridad, borrar, supervisar y consultar) en el registro y use [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) para escribir en el registro.

Cada llamada a una función de registro de eventos es una operación atómica. Cuando se lee desde el registro de eventos, solo se devuelven los registros de eventos completos. Cuando se escribe en el registro de eventos, se garantiza que cada registro de eventos se escribe secuencialmente como un registro completo en el registro. En la lista siguiente se describe cómo el servicio de registro de eventos administra condiciones especiales:

-   El servicio de registro de eventos recibe una operación de lectura y una operación de escritura al mismo tiempo: Si la posición de lectura está al final del archivo, se produce un error en la operación de lectura con un estado de "fin de archivo" (si la operación de escritura no se ha completado) o devuelve el nuevo registro (si se ha completado la operación de escritura).
-   El servicio de registro de eventos completa una operación de borrado antes de recibir una operación de lectura: se produce un error en la operación de lectura con el estado "fin de archivo".
-   El servicio de registro de eventos completa una operación de borrado antes de recibir una operación de escritura: la operación de borrado trunca el registro y, a continuación, la operación de escritura agrega el nuevo registro al principio del registro.

 

 



