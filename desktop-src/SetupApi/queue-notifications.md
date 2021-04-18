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
# <a name="queue-notifications"></a>Notificaciones de cola

Una vez confirmada una cola mediante una llamada a [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), comenzará a procesar las operaciones en cola. En cada paso, la cola envía una notificación a la rutina de devolución de llamada especificada en la llamada a **SetupCommitFileQueue**.

A continuación se encuentra la sintaxis que usa [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para enviar una notificación a la rutina de devolución de llamada.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

Los valores de *parám1* y *Param2* contienen información adicional relevante para la notificación que se envía a la rutina de devolución de llamada. Cada notificación, sus valores *parám1* y *Param2* , y cómo la rutina de devolución de llamada de cola predeterminada controla esa notificación, se describe en detalle en las [notificaciones de cola de archivos](file-queue-notifications.md).

 

 



