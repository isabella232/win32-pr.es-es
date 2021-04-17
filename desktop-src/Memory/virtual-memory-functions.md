---
description: Las funciones de memoria virtual permiten a un proceso manipular o determinar el estado de las páginas en su espacio de direcciones virtuales.
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: Funciones de memoria virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76866fd10dac01315622e8a4faef7bea436a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677471"
---
# <a name="virtual-memory-functions"></a><span data-ttu-id="c720d-103">Funciones de memoria virtual</span><span class="sxs-lookup"><span data-stu-id="c720d-103">Virtual Memory Functions</span></span>

<span data-ttu-id="c720d-104">Las funciones de memoria virtual permiten a un proceso manipular o determinar el estado de las páginas en su espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="c720d-104">The virtual memory functions enable a process to manipulate or determine the status of pages in its virtual address space.</span></span> <span data-ttu-id="c720d-105">Pueden realizar las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="c720d-105">They can perform the following operations:</span></span>

-   <span data-ttu-id="c720d-106">Reserve un intervalo de espacio de direcciones virtuales de un proceso.</span><span class="sxs-lookup"><span data-stu-id="c720d-106">Reserve a range of a process's virtual address space.</span></span> <span data-ttu-id="c720d-107">La reserva de espacio de direcciones no asigna ningún almacenamiento físico, pero impide que otras operaciones de asignación usen el intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="c720d-107">Reserving address space does not allocate any physical storage, but it prevents other allocation operations from using the specified range.</span></span> <span data-ttu-id="c720d-108">No afecta a los espacios de direcciones virtuales de otros procesos.</span><span class="sxs-lookup"><span data-stu-id="c720d-108">It does not affect the virtual address spaces of other processes.</span></span> <span data-ttu-id="c720d-109">La reserva de páginas evita el consumo innecesario de almacenamiento físico, a la vez que permite que un proceso Reserve un intervalo de su espacio de direcciones en el que puede aumentar la estructura de datos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="c720d-109">Reserving pages prevents needless consumption of physical storage, while enabling a process to reserve a range of its address space into which a dynamic data structure can grow.</span></span> <span data-ttu-id="c720d-110">El proceso puede asignar almacenamiento físico para este espacio, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c720d-110">The process can allocate physical storage for this space, as needed.</span></span>
-   <span data-ttu-id="c720d-111">Confirme un intervalo de páginas reservadas en el espacio de direcciones virtuales de un proceso para que el almacenamiento físico (ya sea en RAM o en disco) sea accesible únicamente para el proceso de asignación.</span><span class="sxs-lookup"><span data-stu-id="c720d-111">Commit a range of reserved pages in a process's virtual address space so that physical storage (either in RAM or on disk) is accessible only to the allocating process.</span></span>
-   <span data-ttu-id="c720d-112">Especifique lectura/escritura, de solo lectura o sin acceso para un intervalo de páginas confirmadas.</span><span class="sxs-lookup"><span data-stu-id="c720d-112">Specify read/write, read-only, or no access for a range of committed pages.</span></span> <span data-ttu-id="c720d-113">Esto difiere de las funciones de asignación estándar que siempre asignan páginas con acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c720d-113">This differs from the standard allocation functions that always allocate pages with read/write access.</span></span>
-   <span data-ttu-id="c720d-114">Libere un intervalo de páginas reservadas, haciendo que el intervalo de direcciones virtuales esté disponible para las operaciones de asignación posteriores por parte del proceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="c720d-114">Free a range of reserved pages, making the range of virtual addresses available for subsequent allocation operations by the calling process.</span></span>
-   <span data-ttu-id="c720d-115">Desconfirma un intervalo de páginas confirmadas, liberando su almacenamiento físico y haciéndolo disponible para su posterior asignación por cualquier proceso.</span><span class="sxs-lookup"><span data-stu-id="c720d-115">Decommit a range of committed pages, releasing their physical storage and making it available for subsequent allocation by any process.</span></span>
-   <span data-ttu-id="c720d-116">Bloquee una o más páginas de la memoria asignada en la memoria física (RAM) para que el sistema no pueda intercambiar las páginas al archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="c720d-116">Lock one or more pages of committed memory into physical memory (RAM) so that the system cannot swap the pages out to the paging file.</span></span>
-   <span data-ttu-id="c720d-117">Obtener información sobre un intervalo de páginas en el espacio de direcciones virtuales del proceso de llamada o un proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="c720d-117">Obtain information about a range of pages in the virtual address space of the calling process or a specified process.</span></span>
-   <span data-ttu-id="c720d-118">Cambiar la protección de acceso para un intervalo especificado de páginas confirmadas en el espacio de direcciones virtuales del proceso de llamada o un proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="c720d-118">Change the access protection for a specified range of committed pages in the virtual address space of the calling process or a specified process.</span></span>

<span data-ttu-id="c720d-119">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="c720d-119">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="c720d-120">Asignación de memoria virtual</span><span class="sxs-lookup"><span data-stu-id="c720d-120">Allocating Virtual Memory</span></span>](allocating-virtual-memory.md)
-   [<span data-ttu-id="c720d-121">Comparar métodos de asignación de memoria</span><span class="sxs-lookup"><span data-stu-id="c720d-121">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)
-   [<span data-ttu-id="c720d-122">Liberar memoria virtual</span><span class="sxs-lookup"><span data-stu-id="c720d-122">Freeing Virtual Memory</span></span>](freeing-virtual-memory.md)
-   [<span data-ttu-id="c720d-123">Trabajar con páginas</span><span class="sxs-lookup"><span data-stu-id="c720d-123">Working With Pages</span></span>](working-with-pages.md)
-   [<span data-ttu-id="c720d-124">Funciones de administración de memoria</span><span class="sxs-lookup"><span data-stu-id="c720d-124">Memory Management Functions</span></span>](memory-management-functions.md)

 

 



