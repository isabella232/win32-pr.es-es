---
description: Una vez confirmada una cola mediante una llamada a SetupCommitFileQueue, comenzará a procesar las operaciones en cola. En cada paso, la cola envía una notificación a la rutina de devolución de llamada especificada en la llamada a SetupCommitFileQueue.
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: Notificaciones de cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842a3ebc82640789fdb6e730e881d6790a0d642b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668180"
---
# <a name="queue-notifications"></a><span data-ttu-id="1f25f-104">Notificaciones de cola</span><span class="sxs-lookup"><span data-stu-id="1f25f-104">Queue Notifications</span></span>

<span data-ttu-id="1f25f-105">Una vez confirmada una cola mediante una llamada a [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), comenzará a procesar las operaciones en cola.</span><span class="sxs-lookup"><span data-stu-id="1f25f-105">After a queue is committed by calling [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), it will begin to process the queued operations.</span></span> <span data-ttu-id="1f25f-106">En cada paso, la cola envía una notificación a la rutina de devolución de llamada especificada en la llamada a **SetupCommitFileQueue**.</span><span class="sxs-lookup"><span data-stu-id="1f25f-106">At each step, the queue sends a notification to the callback routine specified in the call to **SetupCommitFileQueue**.</span></span>

<span data-ttu-id="1f25f-107">A continuación se encuentra la sintaxis que usa [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para enviar una notificación a la rutina de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1f25f-107">Following is the syntax that [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

<span data-ttu-id="1f25f-108">Los valores de *parám1* y *Param2* contienen información adicional relevante para la notificación que se envía a la rutina de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1f25f-108">The values of *Param1* and *Param2* contain additional information relevant to the notification being sent to the callback routine.</span></span> <span data-ttu-id="1f25f-109">Cada notificación, sus valores *parám1* y *Param2* , y cómo la rutina de devolución de llamada de cola predeterminada controla esa notificación, se describe en detalle en las [notificaciones de cola de archivos](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="1f25f-109">Each notification, its *Param1* and *Param2* values, and how the default queue callback routine handles that notification, is described in detail in [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 



