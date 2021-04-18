---
description: La e/s de alertas es el método por el que los subprocesos de la aplicación procesan las solicitudes de e/s asincrónicas solo cuando se encuentran en un estado de alerta.
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: E/s de alertas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb830dfadb97051c47b2472eb3e7a3c2d6a0bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687141"
---
# <a name="alertable-io"></a><span data-ttu-id="ce527-103">E/s de alertas</span><span class="sxs-lookup"><span data-stu-id="ce527-103">Alertable I/O</span></span>

<span data-ttu-id="ce527-104">La e/s de alertas es el método por el que los subprocesos de la aplicación procesan las solicitudes de e/s asincrónicas solo cuando se encuentran en un estado de alerta.</span><span class="sxs-lookup"><span data-stu-id="ce527-104">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span>

<span data-ttu-id="ce527-105">Para saber si un subproceso está en un estado de alerta, considere el siguiente escenario:</span><span class="sxs-lookup"><span data-stu-id="ce527-105">To understand when a thread is in an alertable state, consider the following scenario:</span></span>

1.  <span data-ttu-id="ce527-106">Un subproceso inicia una solicitud de lectura asincrónica mediante una llamada a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) con un puntero a una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="ce527-106">A thread initiates an asynchronous read request by calling [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) with a pointer to a callback function.</span></span>
2.  <span data-ttu-id="ce527-107">El subproceso inicia una solicitud de escritura asincrónica mediante una llamada a [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) con un puntero a una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="ce527-107">The thread initiates an asynchronous write request by calling [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) with a pointer to a callback function.</span></span>
3.  <span data-ttu-id="ce527-108">El subproceso llama a una función que captura una fila de datos de un servidor de base de datos remoto.</span><span class="sxs-lookup"><span data-stu-id="ce527-108">The thread calls a function that fetches a row of data from a remote database server.</span></span>

<span data-ttu-id="ce527-109">En este escenario, lo más probable es que las llamadas a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) devuelvan antes de la llamada de función en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="ce527-109">In this scenario, the calls to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) will most likely return before the function call in step 3.</span></span> <span data-ttu-id="ce527-110">Cuando lo hacen, el kernel coloca los punteros a las funciones de devolución de llamada en la cola de llamadas a procedimiento asincrónico (APC) del subproceso.</span><span class="sxs-lookup"><span data-stu-id="ce527-110">When they do, the kernel places the pointers to the callback functions on the thread's Asynchronous Procedure Call (APC) queue.</span></span> <span data-ttu-id="ce527-111">El kernel mantiene esta cola específicamente para almacenar los datos de solicitud de e/s devueltos hasta que el subproceso correspondiente pueda procesarlas.</span><span class="sxs-lookup"><span data-stu-id="ce527-111">The kernel maintains this queue specifically to hold returned I/O request data until it can be processed by the corresponding thread.</span></span>

<span data-ttu-id="ce527-112">Cuando se completa la recopilación de filas y el subproceso vuelve de la función, su prioridad más alta es procesar las solicitudes de e/s devueltas en la cola llamando a las funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="ce527-112">When the row fetch is complete and the thread returns from the function, its highest priority is to process the returned I/O requests on the queue by calling the callback functions.</span></span> <span data-ttu-id="ce527-113">Para ello, debe especificar un estado de alerta.</span><span class="sxs-lookup"><span data-stu-id="ce527-113">To do this, it must enter an alertable state.</span></span> <span data-ttu-id="ce527-114">Un subproceso solo puede hacerlo mediante una llamada a una de las siguientes funciones con las marcas apropiadas:</span><span class="sxs-lookup"><span data-stu-id="ce527-114">A thread can only do this by calling one of the following functions with the appropriate flags:</span></span>

-   [<span data-ttu-id="ce527-115">**SleepEx**</span><span class="sxs-lookup"><span data-stu-id="ce527-115">**SleepEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [<span data-ttu-id="ce527-116">**WaitForSingleObjectEx**</span><span class="sxs-lookup"><span data-stu-id="ce527-116">**WaitForSingleObjectEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [<span data-ttu-id="ce527-117">**WaitForMultipleObjectsEx**</span><span class="sxs-lookup"><span data-stu-id="ce527-117">**WaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [<span data-ttu-id="ce527-118">**SignalObjectAndWait**</span><span class="sxs-lookup"><span data-stu-id="ce527-118">**SignalObjectAndWait**</span></span>](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [<span data-ttu-id="ce527-119">**MsgWaitForMultipleObjectsEx**</span><span class="sxs-lookup"><span data-stu-id="ce527-119">**MsgWaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

<span data-ttu-id="ce527-120">Cuando el subproceso entra en un estado de alerta, se producen los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="ce527-120">When the thread enters an alertable state, the following events occur:</span></span>

1.  <span data-ttu-id="ce527-121">El kernel comprueba la cola APC del subproceso.</span><span class="sxs-lookup"><span data-stu-id="ce527-121">The kernel checks the thread's APC queue.</span></span> <span data-ttu-id="ce527-122">Si la cola contiene punteros de función de devolución de llamada, el kernel quita el puntero de la cola y lo envía al subproceso.</span><span class="sxs-lookup"><span data-stu-id="ce527-122">If the queue contains callback function pointers, the kernel removes the pointer from the queue and sends it to the thread.</span></span>
2.  <span data-ttu-id="ce527-123">El subproceso ejecuta la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="ce527-123">The thread executes the callback function.</span></span>
3.  <span data-ttu-id="ce527-124">Los pasos 1 y 2 se repiten para cada puntero que quede en la cola.</span><span class="sxs-lookup"><span data-stu-id="ce527-124">Steps 1 and 2 are repeated for each pointer remaining in the queue.</span></span>
4.  <span data-ttu-id="ce527-125">Cuando la cola está vacía, el subproceso vuelve de la función que la colocó en un estado de alerta.</span><span class="sxs-lookup"><span data-stu-id="ce527-125">When the queue is empty, the thread returns from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="ce527-126">En este escenario, una vez que el subproceso entra en un estado de alerta, llamará a las funciones de devolución de llamada enviadas a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)y, a continuación, devolverá desde la función que la colocó en un estado de alerta.</span><span class="sxs-lookup"><span data-stu-id="ce527-126">In this scenario, once the thread enters an alertable state it will call the callback functions sent to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), then return from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="ce527-127">Si un subproceso entra en un estado de alerta mientras su cola APC está vacía, el kernel suspenderá la ejecución del subproceso hasta que se produzca uno de los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="ce527-127">If a thread enters an alertable state while its APC queue is empty, the thread's execution will be suspended by the kernel until one of the following occurs:</span></span>

-   <span data-ttu-id="ce527-128">El objeto de kernel en el que se espera se señala.</span><span class="sxs-lookup"><span data-stu-id="ce527-128">The kernel object that is being waited on becomes signaled.</span></span>
-   <span data-ttu-id="ce527-129">Se coloca un puntero de función de devolución de llamada en la cola APC.</span><span class="sxs-lookup"><span data-stu-id="ce527-129">A callback function pointer is placed in the APC queue.</span></span>

<span data-ttu-id="ce527-130">Un subproceso que usa e/s de alerta procesa las solicitudes de e/s asincrónicas de forma más eficaz que cuando simplemente esperan la marca de evento en la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) que se va a establecer, y el mecanismo de e/s de alertas es menos complicado que los [puertos de finalización de e/s](i-o-completion-ports.md) que se van a usar.</span><span class="sxs-lookup"><span data-stu-id="ce527-130">A thread that uses alertable I/O processes asynchronous I/O requests more efficiently than when they simply wait on the event flag in the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure to be set, and the alertable I/O mechanism is less complicated than [I/O completion ports](i-o-completion-ports.md) to use.</span></span> <span data-ttu-id="ce527-131">Sin embargo, la e/s de alertas devuelve el resultado de la solicitud de e/s solo al subproceso que la inició.</span><span class="sxs-lookup"><span data-stu-id="ce527-131">However, alertable I/O returns the result of the I/O request only to the thread that initiated it.</span></span> <span data-ttu-id="ce527-132">Los puertos de finalización de e/s no tienen esta limitación.</span><span class="sxs-lookup"><span data-stu-id="ce527-132">I/O completion ports do not have this limitation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce527-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce527-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce527-134">Llamadas a procedimientos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="ce527-134">Asynchronous Procedure Calls</span></span>](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
