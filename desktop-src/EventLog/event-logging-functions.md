---
description: Las siguientes funciones se usan con el registro de eventos.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Funciones de registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437899684861c5fc7ddbfe98c2499dc07bd9da8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687380"
---
# <a name="event-logging-functions"></a>Funciones de registro de eventos

Las siguientes funciones se usan con el registro de eventos.



| Función                                                         | Descripción                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | Guarda el registro de eventos especificado en un archivo de copia de seguridad.                                                     |
| [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | Borra el registro de eventos especificado y, opcionalmente, guarda la copia actual del registro en un archivo de copia de seguridad.  |
| [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | Cierra un identificador de lectura para el registro de eventos especificado.                                                    |
| [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | Cierra un identificador de escritura en el registro de eventos especificado.                                                   |
| [**GetEventLogInformation**](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | Recupera información sobre el registro de eventos especificado.                                                |
| [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | Recupera el número de registros del registro de eventos especificado.                                         |
| [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | Recupera el número de registro absoluto del registro más antiguo en el registro de eventos especificado.               |
| [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | Permite a una aplicación recibir una notificación cuando se escribe un evento en el registro de eventos especificado. |
| [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | Abre un identificador de un registro de eventos de copia de seguridad.                                                               |
| [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | Abre un identificador del registro de eventos especificado.                                                          |
| [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | Lee un número entero de entradas del registro de eventos especificado.                                       |
| [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | Recupera un identificador registrado en el registro de eventos especificado.                                           |
| [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | Escribe una entrada al final del registro de eventos especificado.                                              |



 

 

 



