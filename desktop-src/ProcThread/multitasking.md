---
description: Un sistema operativo multitarea divide el tiempo de procesador disponible entre los procesos o subprocesos que lo necesitan.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitarea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360692"
---
# <a name="multitasking"></a><span data-ttu-id="1fce9-103">Multitarea</span><span class="sxs-lookup"><span data-stu-id="1fce9-103">Multitasking</span></span>

<span data-ttu-id="1fce9-104">Un sistema operativo multitarea divide el tiempo de procesador disponible entre los procesos o subprocesos que lo necesitan.</span><span class="sxs-lookup"><span data-stu-id="1fce9-104">A multitasking operating system divides the available processor time among the processes or threads that need it.</span></span> <span data-ttu-id="1fce9-105">El sistema está diseñado para la multitarea preferente; asigna un *intervalo de tiempo* de procesador a cada subproceso que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="1fce9-105">The system is designed for preemptive multitasking; it allocates a processor *time slice* to each thread it executes.</span></span> <span data-ttu-id="1fce9-106">El subproceso que se está ejecutando actualmente se suspende cuando transcurre el intervalo de tiempo, lo que permite la ejecución de otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="1fce9-106">The currently executing thread is suspended when its time slice elapses, allowing another thread to run.</span></span> <span data-ttu-id="1fce9-107">Cuando el sistema cambia de un subproceso a otro, guarda el contexto del subproceso que se ha cambiado y restaura el contexto guardado del subproceso siguiente en la cola.</span><span class="sxs-lookup"><span data-stu-id="1fce9-107">When the system switches from one thread to another, it saves the context of the preempted thread and restores the saved context of the next thread in the queue.</span></span>

<span data-ttu-id="1fce9-108">La duración del período de tiempo depende del sistema operativo y del procesador.</span><span class="sxs-lookup"><span data-stu-id="1fce9-108">The length of the time slice depends on the operating system and the processor.</span></span> <span data-ttu-id="1fce9-109">Dado que cada intervalo de tiempo es pequeño (aproximadamente 20 milisegundos), parece que varios subprocesos se ejecutan al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="1fce9-109">Because each time slice is small (approximately 20 milliseconds), multiple threads appear to be executing at the same time.</span></span> <span data-ttu-id="1fce9-110">Este es realmente el caso en sistemas multiprocesador, donde los subprocesos ejecutables se distribuyen entre los procesadores disponibles.</span><span class="sxs-lookup"><span data-stu-id="1fce9-110">This is actually the case on multiprocessor systems, where the executable threads are distributed among the available processors.</span></span> <span data-ttu-id="1fce9-111">Sin embargo, debe tener cuidado al usar varios subprocesos en una aplicación, ya que el rendimiento del sistema puede disminuir si hay demasiados subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1fce9-111">However, you must use caution when using multiple threads in an application, because system performance can decrease if there are too many threads.</span></span>

<span data-ttu-id="1fce9-112">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="1fce9-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="1fce9-113">Ventajas de la multitarea</span><span class="sxs-lookup"><span data-stu-id="1fce9-113">Advantages of Multitasking</span></span>](advantages-of-multitasking.md)
-   [<span data-ttu-id="1fce9-114">Cuándo usar la multitarea</span><span class="sxs-lookup"><span data-stu-id="1fce9-114">When to Use Multitasking</span></span>](when-to-use-multitasking.md)
-   [<span data-ttu-id="1fce9-115">Consideraciones sobre la multitarea</span><span class="sxs-lookup"><span data-stu-id="1fce9-115">Multitasking Considerations</span></span>](multitasking-considerations.md)

 

 



