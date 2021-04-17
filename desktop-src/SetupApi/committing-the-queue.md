---
description: Si se va a llamar a la función de devolución de llamada predeterminada durante el compromiso de la cola, el contexto para ella se debe inicializar mediante las funciones SetupInitDefaultQueueCallback o SetupInitDefaultQueueCallbackEx.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Confirmar la cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ed721c60457a77a168218aa0294bf448889129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667611"
---
# <a name="committing-the-queue"></a><span data-ttu-id="7ce28-103">Confirmar la cola</span><span class="sxs-lookup"><span data-stu-id="7ce28-103">Committing the Queue</span></span>

<span data-ttu-id="7ce28-104">Si se va a llamar a la función de devolución de llamada predeterminada durante el compromiso de la cola, el contexto para ella se debe inicializar mediante las funciones [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) .</span><span class="sxs-lookup"><span data-stu-id="7ce28-104">If the default callback function is going to be called during the queue commitment, the context for it must be initialized using the [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) functions.</span></span> <span data-ttu-id="7ce28-105">Si usa una función de devolución de llamada personalizada que nunca llama a la función de devolución de llamada predeterminada, este paso no es necesario.</span><span class="sxs-lookup"><span data-stu-id="7ce28-105">If you are using a custom callback function that never calls the default callback function, this step is not necessary.</span></span>

<span data-ttu-id="7ce28-106">Una vez que se ha generado la cola y se ha inicializado la función de devolución de llamada que procesará las notificaciones de cola, puede llamar a [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para confirmar las operaciones que se han puesto en cola.</span><span class="sxs-lookup"><span data-stu-id="7ce28-106">After the queue is built and the callback function that will process queue notifications has been initialized, you can call [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to commit the operations that have been enqueued.</span></span>

<span data-ttu-id="7ce28-107">En el ejemplo siguiente se usa [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para confirmar la cola mediante la rutina de devolución de llamada predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7ce28-107">The following example uses [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to commit the queue using the default callback routine.</span></span>

``` syntax
test = SetupCommitFileQueue (
     OwnerWindow,          //window that will own dialog boxes
                           //created by the callback routine
     MyQueue,              //the queue to commit
  
                           //use the default callback routine
     SetupDefaultQueueCallback,  
  
     Context               //context information that will be 
                           //  used by the callback routine
);
```

<span data-ttu-id="7ce28-108">En el ejemplo anterior, alqueue es la cola que se va a confirmar, OwnerWindow es la ventana que será propietaria de los cuadros de diálogo creados por la rutina de devolución de llamada predeterminada, SetupDefaultQueueCallback especifica que se utilizará la función de devolución de llamada predeterminada y *Context* es un puntero a la estructura devuelta por la llamada anterior a [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).</span><span class="sxs-lookup"><span data-stu-id="7ce28-108">In the preceding example, MyQueue is the queue to commit, OwnerWindow is the window that will own any dialog boxes created by the default callback routine, SetupDefaultQueueCallback specifies that the default callback function will be used, and *Context* is a pointer to the structure returned by the previous call to [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).</span></span>

 

 



