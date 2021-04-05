---
description: La información sobre cada evento se almacena en el registro de eventos en una entrada del registro de eventos. La entrada del registro de eventos incluye información sobre la hora, el tipo y la categoría. Para obtener más información, vea la estructura EVENTLOGRECORD.
ms.assetid: 73731505-97f5-4985-8d00-c6ce8604902d
title: Entradas del registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cc6caf1011c06eda0dca240bb7a3478c549827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908866"
---
# <a name="event-log-records"></a>Entradas del registro de eventos

La información sobre cada evento se almacena en el registro de eventos en una *entrada del registro de eventos*. La entrada del registro de eventos incluye información sobre la hora, el tipo y la categoría. Para obtener más información, vea la estructura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .

El miembro **recordNumber** de [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contiene el número de registro de la entrada del registro de eventos. El primer registro que se escribe en un registro de eventos es el número de registro 1 y otros registros se numeran secuencialmente. Si el número de registro alcanza el valor de ULONG \_ Max, el siguiente número de registro será 0, no 1; sin embargo, se usa cero para buscar el registro.

Si el valor del registro de [retención](eventlog-key.md) se establece en cero, los registros de eventos se sobrescriben cuando se alcanza el tamaño máximo del registro. Por lo tanto, el registro más antiguo de un registro de eventos no puede ser el número de registro 1. Para identificar el registro más antiguo en el registro, llame a la función [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) . Después, puede llamar a la función [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) y agregar el valor devuelto al número de registro más antiguo para determinar el registro más reciente.

Puede leer registros individuales del registro de eventos mediante la función [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) . Para obtener más información, vea [consultar información de eventos](querying-for-event-source-messages.md).

 

 



