---
description: Una vez que la cola ha terminado de confirmar sus operaciones, debe cerrarse con la función SetupCloseFileQueue con el identificador creado por SetupOpenFileQueue.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Cerrar la cola de archivos y el archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b4005e3ce9d084d759612d70cd9fd256fe9ba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669880"
---
# <a name="closing-the-file-queue-and-inf-file"></a><span data-ttu-id="399ea-103">Cerrar la cola de archivos y el archivo INF</span><span class="sxs-lookup"><span data-stu-id="399ea-103">Closing the File Queue and INF File</span></span>

<span data-ttu-id="399ea-104">Una vez que la cola ha terminado de confirmar sus operaciones, debe cerrarse con la función [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) con el identificador creado por [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span><span class="sxs-lookup"><span data-stu-id="399ea-104">After the queue has finished committing its operations, it should be closed using the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function with the handle that was created by [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span> <span data-ttu-id="399ea-105">La devolución de llamada de cola predeterminada se debe destruir y volver a crear antes de que se pueda confirmar otra cola.</span><span class="sxs-lookup"><span data-stu-id="399ea-105">The default queue callback must be destroyed and recreated before another queue can be committed.</span></span>

<span data-ttu-id="399ea-106">Si se inició un contexto predeterminado para que lo use la rutina de devolución de llamada predeterminada, también debe terminar llamando a la función [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) .</span><span class="sxs-lookup"><span data-stu-id="399ea-106">If a default context was initiated for use by the default callback routine, it should also be terminated by calling the [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) function.</span></span> <span data-ttu-id="399ea-107">El *contexto* es un puntero a la estructura devuelta por la función [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) .</span><span class="sxs-lookup"><span data-stu-id="399ea-107">The *Context* is a pointer to the structure returned by the [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) function.</span></span>

<span data-ttu-id="399ea-108">Cuando ya no se necesite el acceso a la información del archivo INF, llame a la función [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) con el identificador creado por [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) para liberar recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="399ea-108">When access to the INF information is no longer needed, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function with the handle that was created by [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) to free system resources.</span></span>

 

 



