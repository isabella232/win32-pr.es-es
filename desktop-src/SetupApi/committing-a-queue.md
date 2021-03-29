---
description: Una vez que se han puesto en cola todas las operaciones de archivo deseadas, la cola debe estar confirmada. Esto hace que se procesen las operaciones de archivo en cola.
ms.assetid: 536f47f5-785e-4a83-a500-c769442e3e68
title: Confirmar una cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d995f6811dbd19bba9e13f29bc119cdf2f471f74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818078"
---
# <a name="committing-a-queue"></a><span data-ttu-id="f307a-104">Confirmar una cola</span><span class="sxs-lookup"><span data-stu-id="f307a-104">Committing a Queue</span></span>

<span data-ttu-id="f307a-105">Una vez que se han puesto en cola todas las operaciones de archivo deseadas, la cola debe estar confirmada.</span><span class="sxs-lookup"><span data-stu-id="f307a-105">After all the desired file operations have been queued, the queue must be committed.</span></span> <span data-ttu-id="f307a-106">Esto hace que se procesen las operaciones de archivo en cola.</span><span class="sxs-lookup"><span data-stu-id="f307a-106">This causes the enqueued file operations to be processed.</span></span>

<span data-ttu-id="f307a-107">Una cola de archivos no se puede reutilizar una vez confirmada.</span><span class="sxs-lookup"><span data-stu-id="f307a-107">A file queue cannot be reused after it has been committed.</span></span> <span data-ttu-id="f307a-108">El procedimiento recomendado es recopilar todas las operaciones de archivo necesarias para la cola de archivos y confirmar la cola una sola vez.</span><span class="sxs-lookup"><span data-stu-id="f307a-108">The best practice is to collect all the required file operations for the file queue and commit the queue only once.</span></span> <span data-ttu-id="f307a-109">Si se requiere un procesamiento adicional de la cola una vez confirmado, se debe cerrar el identificador de la cola y crear una nueva cola de archivos.</span><span class="sxs-lookup"><span data-stu-id="f307a-109">If additional processing of the queue is required after it has been committed, the handle to the queue should be closed and a new file queue created.</span></span> <span data-ttu-id="f307a-110">Para confirmar la cola de archivos, llame a la función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , especificando una rutina de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f307a-110">To commit the file queue, call the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function, specifying a callback routine.</span></span> <span data-ttu-id="f307a-111">La rutina de devolución de llamada recibirá notificaciones de **SetupCommitFileQueue** a medida que se procesen las operaciones de archivo.</span><span class="sxs-lookup"><span data-stu-id="f307a-111">The callback routine will receive notifications from **SetupCommitFileQueue** as the file operations are processed.</span></span> <span data-ttu-id="f307a-112">Si desea utilizar la rutina de devolución de llamada de cola predeterminada, primero debe inicializar el contexto necesario llamando a [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="f307a-112">If you want to use the default queue callback routine, you must first initialize the necessary context by calling either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span> <span data-ttu-id="f307a-113">Para obtener más información sobre la rutina de devolución de llamada de cola predeterminada, vea [rutina de devolución de llamada de cola predeterminada](default-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="f307a-113">For more information about the default queue callback routine, see [Default Queue Callback Routine](default-queue-callback-routine.md).</span></span>

> [!Note]  
> <span data-ttu-id="f307a-114">Se debe llamar a [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) antes de que se cierre la cola.</span><span class="sxs-lookup"><span data-stu-id="f307a-114">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) should be called before the queue is closed.</span></span> <span data-ttu-id="f307a-115">Las operaciones que no se confirman cuando se llama a [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) no se realizarán.</span><span class="sxs-lookup"><span data-stu-id="f307a-115">Any operations that are uncommitted when [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) is called will not be performed.</span></span>

 

 

 



