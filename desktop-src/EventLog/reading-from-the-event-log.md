---
description: Una aplicación del visor de eventos utiliza la función OpenEventLog para abrir el registro de eventos de un origen de eventos.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Leer del registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4642c003d31c986be55a819b513f1c28c784af2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082488"
---
# <a name="reading-from-the-event-log"></a><span data-ttu-id="b55d0-103">Leer del registro de eventos</span><span class="sxs-lookup"><span data-stu-id="b55d0-103">Reading from the Event Log</span></span>

<span data-ttu-id="b55d0-104">Una aplicación del visor de eventos utiliza la función [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) para abrir el registro de eventos de un origen de eventos.</span><span class="sxs-lookup"><span data-stu-id="b55d0-104">An event viewer application uses the [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to open the event log for an event source.</span></span> <span data-ttu-id="b55d0-105">Después, el visor de eventos puede usar la función [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) para leer los registros de eventos del registro.</span><span class="sxs-lookup"><span data-stu-id="b55d0-105">The event viewer can then use the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to read event records from the log.</span></span> <span data-ttu-id="b55d0-106">**ReadEventLog** devuelve un búfer que contiene una estructura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) e información adicional que describe un evento registrado.</span><span class="sxs-lookup"><span data-stu-id="b55d0-106">**ReadEventLog** returns a buffer containing an [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure and additional information that describes a logged event.</span></span> <span data-ttu-id="b55d0-107">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="b55d0-107">The following diagram illustrates this process.</span></span>

![leer del registro de eventos](images/readlog.png)

<span data-ttu-id="b55d0-109">Para obtener código de ejemplo, consulte [consultar información de eventos](querying-for-event-source-messages.md).</span><span class="sxs-lookup"><span data-stu-id="b55d0-109">For example code, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



