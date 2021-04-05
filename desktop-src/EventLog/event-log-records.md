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
# <a name="event-log-records"></a><span data-ttu-id="00396-105">Entradas del registro de eventos</span><span class="sxs-lookup"><span data-stu-id="00396-105">Event Log Records</span></span>

<span data-ttu-id="00396-106">La información sobre cada evento se almacena en el registro de eventos en una *entrada del registro de eventos*.</span><span class="sxs-lookup"><span data-stu-id="00396-106">Information about each event is stored in the event log in an *event log record*.</span></span> <span data-ttu-id="00396-107">La entrada del registro de eventos incluye información sobre la hora, el tipo y la categoría.</span><span class="sxs-lookup"><span data-stu-id="00396-107">The event log record includes time, type, and category information.</span></span> <span data-ttu-id="00396-108">Para obtener más información, vea la estructura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="00396-108">For more information, see the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure.</span></span>

<span data-ttu-id="00396-109">El miembro **recordNumber** de [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contiene el número de registro de la entrada del registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="00396-109">The **RecordNumber** member of [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contains the record number for the event log record.</span></span> <span data-ttu-id="00396-110">El primer registro que se escribe en un registro de eventos es el número de registro 1 y otros registros se numeran secuencialmente.</span><span class="sxs-lookup"><span data-stu-id="00396-110">The very first record written to an event log is record number 1, and other records are numbered sequentially.</span></span> <span data-ttu-id="00396-111">Si el número de registro alcanza el valor de ULONG \_ Max, el siguiente número de registro será 0, no 1; sin embargo, se usa cero para buscar el registro.</span><span class="sxs-lookup"><span data-stu-id="00396-111">If the record number reaches ULONG\_MAX, the next record number will be 0, not 1; however, you use zero to seek to the record.</span></span>

<span data-ttu-id="00396-112">Si el valor del registro de [retención](eventlog-key.md) se establece en cero, los registros de eventos se sobrescriben cuando se alcanza el tamaño máximo del registro.</span><span class="sxs-lookup"><span data-stu-id="00396-112">If the [Retention](eventlog-key.md) registry value is set to zero, the event records are overwritten when the maximum log size is reached.</span></span> <span data-ttu-id="00396-113">Por lo tanto, el registro más antiguo de un registro de eventos no puede ser el número de registro 1.</span><span class="sxs-lookup"><span data-stu-id="00396-113">Therefore, the oldest record in an event log may not be record number 1.</span></span> <span data-ttu-id="00396-114">Para identificar el registro más antiguo en el registro, llame a la función [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="00396-114">To identify the oldest record in the log, call the [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) function.</span></span> <span data-ttu-id="00396-115">Después, puede llamar a la función [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) y agregar el valor devuelto al número de registro más antiguo para determinar el registro más reciente.</span><span class="sxs-lookup"><span data-stu-id="00396-115">You can then call the [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) function and add the returned value to the oldest record number to determine the newest record.</span></span>

<span data-ttu-id="00396-116">Puede leer registros individuales del registro de eventos mediante la función [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) .</span><span class="sxs-lookup"><span data-stu-id="00396-116">You can read individual records from the event log using the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function.</span></span> <span data-ttu-id="00396-117">Para obtener más información, vea [consultar información de eventos](querying-for-event-source-messages.md).</span><span class="sxs-lookup"><span data-stu-id="00396-117">For more information, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



