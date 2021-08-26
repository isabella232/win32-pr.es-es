---
description: Las funciones OpenEventLog, OpenBackupEventLog, RegisterEventSource, DeregisterEventSource y CloseEventLog abren y cierran identificadores de registro de eventos.
ms.assetid: e42a66c2-2f1e-46f8-99c7-4701075c8ec3
title: Operaciones de registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221218bdfa4fc5e4fc6a905353cde33357c4088119031062c074c75d4b8136dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901457"
---
# <a name="event-logging-operations"></a>Operaciones de registro de eventos

Las [**funciones OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga), [**OpenBackupEventLog,**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga) [**RegisterEventSource,**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)y [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog) abren y cierran identificadores de registro de eventos.

En la tabla siguiente se muestran las operaciones que se pueden realizar en un registro de eventos abierto y la función correspondiente para cada operación.



| Operación | Función                                                                                                                     |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| Copia de seguridad    | [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                                                                                     |
| Borrar     | [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                                                                                       |
| Supervisión   | [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)                                                                         |
| Consultar     | [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord), [ **GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) |
| Lectura      | [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                                                                                         |
| Escritura     | [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                                                                                           |



 

Las [**funciones OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) [**y ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) toman un nombre de servidor opcional como parámetro para que las operaciones se puedan realizar en el servidor remoto. Use [**OpenEventLog para**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) leer o realizar operaciones administrativas (copia de seguridad, borrar, supervisar y consultar) en el registro y usar [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) para escribir en el registro.

Cada llamada a una función de registro de eventos es una operación atómica. Cuando se lee desde el registro de eventos, solo se devuelven registros de eventos completos. Al escribir en el registro de eventos, se garantiza que cada registro de eventos se escribirá secuencialmente como un registro completo en el registro. En la lista siguiente se describe cómo el servicio de registro de eventos controla las condiciones especiales:

-   El servicio de registro de eventos recibe una operación de lectura y una operación de escritura al mismo tiempo: si la posición de lectura está al final del archivo, se produce un error en la operación de lectura con un estado de "fin de archivo" (si la operación de escritura no se ha completado) o devuelve el nuevo registro (si se ha completado la operación de escritura).
-   El servicio de registro de eventos completa una operación clara antes de recibir una operación de lectura: se produce un error en la operación de lectura con el estado de "fin de archivo".
-   El servicio de registro de eventos completa una operación de borrar antes de recibir una operación de escritura: la operación de borrar trunca el registro y, a continuación, la operación de escritura agrega el nuevo registro al principio del registro.

 

 



