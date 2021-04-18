---
description: La cantidad máxima de memoria física admitida por Microsoft Windows oscila entre 2 GB y 2 TB, en función de la versión de Windows.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: Espacio de direcciones virtuales y almacenamiento físico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d36445eb2639cbfc4db2a6e4abaf28b9af87cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545211"
---
# <a name="virtual-address-space-and-physical-storage"></a><span data-ttu-id="0935b-103">Espacio de direcciones virtuales y almacenamiento físico</span><span class="sxs-lookup"><span data-stu-id="0935b-103">Virtual Address Space and Physical Storage</span></span>

<span data-ttu-id="0935b-104">La cantidad máxima de memoria física admitida por Microsoft Windows oscila entre 2 GB y 24 TB, dependiendo de la versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="0935b-104">The maximum amount of physical memory supported by Microsoft Windows ranges from 2 GB to 24 TB, depending on the version of Windows.</span></span> <span data-ttu-id="0935b-105">Para obtener más información, consulte [límites de memoria para las versiones de Windows](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="0935b-105">For more information, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span> <span data-ttu-id="0935b-106">El espacio de direcciones virtuales de cada proceso puede ser menor o mayor que la memoria física total disponible en el equipo.</span><span class="sxs-lookup"><span data-stu-id="0935b-106">The virtual address space of each process can be smaller or larger than the total physical memory available on the computer.</span></span> <span data-ttu-id="0935b-107">El subconjunto del espacio de direcciones virtuales de un proceso que reside en la memoria física se conoce como espacio de *trabajo*.</span><span class="sxs-lookup"><span data-stu-id="0935b-107">The subset of the virtual address space of a process that resides in physical memory is known as the *working set*.</span></span> <span data-ttu-id="0935b-108">Si los subprocesos de un proceso intentan usar más memoria física de la que está disponible actualmente, el sistema pagina parte del contenido de la memoria en el disco.</span><span class="sxs-lookup"><span data-stu-id="0935b-108">If the threads of a process attempt to use more physical memory than is currently available, the system pages some of the memory contents to disk.</span></span> <span data-ttu-id="0935b-109">La cantidad total de espacio de direcciones virtuales disponible para un proceso está limitada por la memoria física y el espacio libre en disco disponible para el archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="0935b-109">The total amount of virtual address space available to a process is limited by physical memory and the free space on disk available for the paging file.</span></span>

<span data-ttu-id="0935b-110">El almacenamiento físico y el espacio de direcciones virtuales de cada proceso se organizan en *páginas*, unidades de memoria, cuyo tamaño depende del equipo host.</span><span class="sxs-lookup"><span data-stu-id="0935b-110">Physical storage and the virtual address space of each process are organized into *pages*, units of memory, whose size depends on the host computer.</span></span> <span data-ttu-id="0935b-111">Por ejemplo, en equipos x86, el tamaño de página del host es de 4 kilobytes.</span><span class="sxs-lookup"><span data-stu-id="0935b-111">For example, on x86 computers the host page size is 4 kilobytes.</span></span>

<span data-ttu-id="0935b-112">Para maximizar la flexibilidad en la administración de la memoria, el sistema puede trasladar páginas de la memoria física hacia y desde un archivo de paginación en el disco.</span><span class="sxs-lookup"><span data-stu-id="0935b-112">To maximize its flexibility in managing memory, the system can move pages of physical memory to and from a paging file on disk.</span></span> <span data-ttu-id="0935b-113">Cuando una página se mueve en la memoria física, el sistema actualiza los mapas de páginas de los procesos afectados.</span><span class="sxs-lookup"><span data-stu-id="0935b-113">When a page is moved in physical memory, the system updates the page maps of the affected processes.</span></span> <span data-ttu-id="0935b-114">Cuando el sistema necesita espacio en la memoria física, mueve las páginas usadas menos recientemente de la memoria física al archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="0935b-114">When the system needs space in physical memory, it moves the least recently used pages of physical memory to the paging file.</span></span> <span data-ttu-id="0935b-115">La manipulación de la memoria física por parte del sistema es completamente transparente para las aplicaciones, que solo funcionan en sus espacios de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="0935b-115">Manipulation of physical memory by the system is completely transparent to applications, which operate only in their virtual address spaces.</span></span>

 

 



