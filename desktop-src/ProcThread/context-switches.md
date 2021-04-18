---
description: Scheduler mantiene una cola de subprocesos ejecutables para cada nivel de prioridad.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Cambios de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276825"
---
# <a name="context-switches"></a><span data-ttu-id="b66bc-103">Cambios de contexto</span><span class="sxs-lookup"><span data-stu-id="b66bc-103">Context Switches</span></span>

<span data-ttu-id="b66bc-104">Scheduler mantiene una cola de subprocesos ejecutables para cada nivel de prioridad.</span><span class="sxs-lookup"><span data-stu-id="b66bc-104">The scheduler maintains a queue of executable threads for each priority level.</span></span> <span data-ttu-id="b66bc-105">Estos se conocen como *subprocesos listos*.</span><span class="sxs-lookup"><span data-stu-id="b66bc-105">These are known as *ready threads*.</span></span> <span data-ttu-id="b66bc-106">Cuando un procesador está disponible, el sistema realiza un *cambio de contexto*.</span><span class="sxs-lookup"><span data-stu-id="b66bc-106">When a processor becomes available, the system performs a *context switch*.</span></span> <span data-ttu-id="b66bc-107">Los pasos de un cambio de contexto son:</span><span class="sxs-lookup"><span data-stu-id="b66bc-107">The steps in a context switch are:</span></span>

1.  <span data-ttu-id="b66bc-108">Guarde el contexto del subproceso que acaba de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="b66bc-108">Save the context of the thread that just finished executing.</span></span>
2.  <span data-ttu-id="b66bc-109">Coloque el subproceso que acaba de ejecutarse al final de la cola para su prioridad.</span><span class="sxs-lookup"><span data-stu-id="b66bc-109">Place the thread that just finished executing at the end of the queue for its priority.</span></span>
3.  <span data-ttu-id="b66bc-110">Busque la cola de prioridad más alta que contiene los subprocesos listos.</span><span class="sxs-lookup"><span data-stu-id="b66bc-110">Find the highest priority queue that contains ready threads.</span></span>
4.  <span data-ttu-id="b66bc-111">Quite el subproceso en el encabezado de la cola, cargue su contexto y ejecútelo.</span><span class="sxs-lookup"><span data-stu-id="b66bc-111">Remove the thread at the head of the queue, load its context, and execute it.</span></span>

<span data-ttu-id="b66bc-112">Las siguientes clases de subprocesos no son subprocesos listos.</span><span class="sxs-lookup"><span data-stu-id="b66bc-112">The following classes of threads are not ready threads.</span></span>

-   <span data-ttu-id="b66bc-113">Subprocesos creados con la marca de creación \_ suspendida</span><span class="sxs-lookup"><span data-stu-id="b66bc-113">Threads created with the CREATE\_SUSPENDED flag</span></span>
-   <span data-ttu-id="b66bc-114">Subprocesos detenidos durante la ejecución con la función [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) o [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)</span><span class="sxs-lookup"><span data-stu-id="b66bc-114">Threads halted during execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function</span></span>
-   <span data-ttu-id="b66bc-115">Subprocesos que esperan un objeto de sincronización o una entrada.</span><span class="sxs-lookup"><span data-stu-id="b66bc-115">Threads waiting for a synchronization object or input.</span></span>

<span data-ttu-id="b66bc-116">Hasta que los subprocesos suspendidos o bloqueados estén listos para ejecutarse, el programador no asigna ningún tiempo de procesador a ellos, independientemente de su prioridad.</span><span class="sxs-lookup"><span data-stu-id="b66bc-116">Until threads that are suspended or blocked become ready to run, the scheduler does not allocate any processor time to them, regardless of their priority.</span></span>

<span data-ttu-id="b66bc-117">Los motivos más comunes para un cambio de contexto son:</span><span class="sxs-lookup"><span data-stu-id="b66bc-117">The most common reasons for a context switch are:</span></span>

-   <span data-ttu-id="b66bc-118">El intervalo de tiempo ha transcurrido.</span><span class="sxs-lookup"><span data-stu-id="b66bc-118">The time slice has elapsed.</span></span>
-   <span data-ttu-id="b66bc-119">Un subproceso con una prioridad más alta está listo para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="b66bc-119">A thread with a higher priority has become ready to run.</span></span>
-   <span data-ttu-id="b66bc-120">Un subproceso en ejecución debe esperar.</span><span class="sxs-lookup"><span data-stu-id="b66bc-120">A running thread needs to wait.</span></span>

<span data-ttu-id="b66bc-121">Cuando un subproceso en ejecución debe esperar, abandona el resto de su intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b66bc-121">When a running thread needs to wait, it relinquishes the remainder of its time slice.</span></span>

 

 
