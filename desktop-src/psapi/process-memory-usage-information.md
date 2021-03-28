---
title: Información de uso de memoria de proceso
description: La función GetProcessMemoryInfo toma un identificador de proceso como entrada y rellena una \_ estructura de contadores de memoria de proceso \_ con información sobre las estadísticas de memoria para el proceso.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133032b8cfb8a9af4ccea5661c9e0e0181ab4d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903705"
---
# <a name="process-memory-usage-information"></a><span data-ttu-id="5786a-103">Información de uso de memoria de proceso</span><span class="sxs-lookup"><span data-stu-id="5786a-103">Process Memory Usage Information</span></span>

<span data-ttu-id="5786a-104">La función [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) toma un identificador de proceso como entrada y rellena una estructura de [**\_ \_ contadores de memoria de proceso**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) con información sobre las estadísticas de memoria para el proceso.</span><span class="sxs-lookup"><span data-stu-id="5786a-104">The [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) function takes a process handle as input and fills a [**PROCESS\_MEMORY\_COUNTERS**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) structure with information about the memory statistics for the process.</span></span> <span data-ttu-id="5786a-105">El miembro **CB** recibe el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="5786a-105">The **cb** member receives the size of the structure.</span></span> <span data-ttu-id="5786a-106">El miembro **PageFaultCount** recibe el número de errores de página.</span><span class="sxs-lookup"><span data-stu-id="5786a-106">The **PageFaultCount** member receives the number of page faults.</span></span> <span data-ttu-id="5786a-107">Los miembros restantes reciben el uso actual y máximo de memoria en las siguientes categorías:</span><span class="sxs-lookup"><span data-stu-id="5786a-107">The remaining members receive the current and peak memory usage in the following categories:</span></span>

-   <span data-ttu-id="5786a-108">Espacio de trabajo</span><span class="sxs-lookup"><span data-stu-id="5786a-108">working set</span></span>
-   <span data-ttu-id="5786a-109">Grupo paginado</span><span class="sxs-lookup"><span data-stu-id="5786a-109">paged pool</span></span>
-   <span data-ttu-id="5786a-110">bloque no paginado</span><span class="sxs-lookup"><span data-stu-id="5786a-110">nonpaged pool</span></span>
-   <span data-ttu-id="5786a-111">paginación</span><span class="sxs-lookup"><span data-stu-id="5786a-111">pagefile</span></span>

<span data-ttu-id="5786a-112">El espacio de *trabajo* es la cantidad de memoria asignada físicamente al contexto del proceso en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="5786a-112">The *working set* is the amount of memory physically mapped to the process context at a given time.</span></span> <span data-ttu-id="5786a-113">La memoria del *Grupo paginado* es la memoria del sistema que puede transferirse al archivo de paginación en el disco (paginado) cuando no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5786a-113">Memory in the *paged pool* is system memory that can be transferred to the paging file on disk (paged) when it is not being used.</span></span> <span data-ttu-id="5786a-114">La memoria del *bloque no paginado* es la memoria del sistema que no se puede paginar en el disco, siempre y cuando se asignen los objetos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="5786a-114">Memory in the *nonpaged pool* is system memory that cannot be paged to disk as long as the corresponding objects are allocated.</span></span> <span data-ttu-id="5786a-115">El uso del archivo de *paginación* representa la cantidad de memoria que se reserva para el proceso en el archivo de paginación del sistema.</span><span class="sxs-lookup"><span data-stu-id="5786a-115">The *pagefile* usage represents how much memory is set aside for the process in the system paging file.</span></span> <span data-ttu-id="5786a-116">Cuando el uso de memoria es demasiado alto, el administrador de memoria virtual pagina la memoria en el disco.</span><span class="sxs-lookup"><span data-stu-id="5786a-116">When memory usage is too high, the virtual memory manager pages selected memory to disk.</span></span> <span data-ttu-id="5786a-117">Cuando un subproceso necesita una página que no está en la memoria, el administrador de memoria la vuelve a cargar desde el archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="5786a-117">When a thread needs a page that is not in memory, the memory manager reloads it from the paging file.</span></span>

 

 




