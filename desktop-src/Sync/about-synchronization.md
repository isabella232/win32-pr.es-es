---
description: Para sincronizar el acceso a un recurso, use uno de los objetos de sincronización en una de las funciones de espera.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Acerca de la sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ad53dc8c309d8ec55f37cef5f78839348071477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667988"
---
# <a name="about-synchronization"></a><span data-ttu-id="f8378-103">Acerca de la sincronización</span><span class="sxs-lookup"><span data-stu-id="f8378-103">About Synchronization</span></span>

<span data-ttu-id="f8378-104">Para sincronizar el acceso a un recurso, use uno de los [objetos de sincronización](synchronization-objects.md) en una de las [funciones de espera](wait-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f8378-104">To synchronize access to a resource, use one of the [synchronization objects](synchronization-objects.md) in one of the [wait functions](wait-functions.md).</span></span> <span data-ttu-id="f8378-105">El estado de un objeto de sincronización es *señalado* o no *señalado*.</span><span class="sxs-lookup"><span data-stu-id="f8378-105">The state of a synchronization object is either *signaled* or *nonsignaled*.</span></span> <span data-ttu-id="f8378-106">Las funciones de espera permiten que un subproceso bloquee su propia ejecución hasta que un objeto no señalado especificado se establezca en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="f8378-106">The wait functions allow a thread to block its own execution until a specified nonsignaled object is set to the signaled state.</span></span> <span data-ttu-id="f8378-107">Para obtener más información, consulte [sincronización entre procesos](interprocess-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="f8378-107">For more information, see [Interprocess Synchronization](interprocess-synchronization.md).</span></span>

<span data-ttu-id="f8378-108">A continuación se muestran otros mecanismos de sincronización:</span><span class="sxs-lookup"><span data-stu-id="f8378-108">The following are other synchronization mechanisms:</span></span>

-   [<span data-ttu-id="f8378-109">entrada y salida superpuestas</span><span class="sxs-lookup"><span data-stu-id="f8378-109">overlapped input and output</span></span>](synchronization-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="f8378-110">llamadas a procedimientos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="f8378-110">asynchronous procedure calls</span></span>](asynchronous-procedure-calls.md)
-   [<span data-ttu-id="f8378-111">objetos de sección crítica</span><span class="sxs-lookup"><span data-stu-id="f8378-111">critical section objects</span></span>](critical-section-objects.md)
-   [<span data-ttu-id="f8378-112">variables de condición</span><span class="sxs-lookup"><span data-stu-id="f8378-112">condition variables</span></span>](condition-variables.md)
-   [<span data-ttu-id="f8378-113">bloqueos finos de lector/escritor</span><span class="sxs-lookup"><span data-stu-id="f8378-113">slim reader/writer locks</span></span>](slim-reader-writer--srw--locks.md)
-   [<span data-ttu-id="f8378-114">inicialización única</span><span class="sxs-lookup"><span data-stu-id="f8378-114">one-time initialization</span></span>](one-time-initialization.md)
-   [<span data-ttu-id="f8378-115">acceso a variables entrelazadas</span><span class="sxs-lookup"><span data-stu-id="f8378-115">interlocked variable access</span></span>](interlocked-variable-access.md)
-   [<span data-ttu-id="f8378-116">listas vinculadas de un solo vínculo</span><span class="sxs-lookup"><span data-stu-id="f8378-116">interlocked singly linked lists</span></span>](interlocked-singly-linked-lists.md)
-   [<span data-ttu-id="f8378-117">colas de temporizador</span><span class="sxs-lookup"><span data-stu-id="f8378-117">timer queues</span></span>](timer-queues.md)
-   <span data-ttu-id="f8378-118">la macro [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)</span><span class="sxs-lookup"><span data-stu-id="f8378-118">the [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) macro</span></span>

<span data-ttu-id="f8378-119">Para obtener información adicional sobre la sincronización, vea [problemas de sincronización y multiprocesador](synchronization-and-multiprocessor-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f8378-119">For additional information on synchronization, see [Synchronization and Multiprocessor Issues](synchronization-and-multiprocessor-issues.md).</span></span>

 

 
