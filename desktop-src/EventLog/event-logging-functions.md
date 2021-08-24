---
description: Las siguientes funciones se usan con el registro de eventos.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Funciones de registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6ba5e43286a65b9d3456edc9cd80e8812bd9a32975ec63158c0717b41c6894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069595"
---
# <a name="event-logging-functions"></a>Funciones de registro de eventos

Las siguientes funciones se usan con el registro de eventos.



| Función                                                         | Descripción                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | Guarda el registro de eventos especificado en un archivo de copia de seguridad.                                                     |
| [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | Borra el registro de eventos especificado y, opcionalmente, guarda la copia actual del registro en un archivo de copia de seguridad.  |
| [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | Cierra un identificador de lectura al registro de eventos especificado.                                                    |
| [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | Cierra un identificador de escritura al registro de eventos especificado.                                                   |
| [**GetEventLogInformation**](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | Recupera información sobre el registro de eventos especificado.                                                |
| [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | Recupera el número de registros del registro de eventos especificado.                                         |
| [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | Recupera el número de registro absoluto del registro más antiguo del registro de eventos especificado.               |
| [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | Permite que una aplicación reciba una notificación cuando se escribe un evento en el registro de eventos especificado. |
| [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | Abre un identificador en un registro de eventos de copia de seguridad.                                                               |
| [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | Abre un identificador para el registro de eventos especificado.                                                          |
| [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | Lee un número entero de entradas del registro de eventos especificado.                                       |
| [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | Recupera un identificador registrado en el registro de eventos especificado.                                           |
| [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | Escribe una entrada al final del registro de eventos especificado.                                              |



 

 

 



