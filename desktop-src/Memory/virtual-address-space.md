---
description: El espacio de direcciones virtuales para un proceso es el conjunto de direcciones de memoria virtual que puede usar. El espacio de direcciones de cada proceso es privado y no es accesible para otros procesos a menos que sea compartido.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Espacio de direcciones virtuales (administración de memoria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001297"
---
# <a name="virtual-address-space-memory-management"></a><span data-ttu-id="4819f-104">Espacio de direcciones virtuales (administración de memoria)</span><span class="sxs-lookup"><span data-stu-id="4819f-104">Virtual Address Space (Memory Management)</span></span>

<span data-ttu-id="4819f-105">El espacio de direcciones virtuales para un proceso es el conjunto de direcciones de memoria virtual que puede usar.</span><span class="sxs-lookup"><span data-stu-id="4819f-105">The virtual address space for a process is the set of virtual memory addresses that it can use.</span></span> <span data-ttu-id="4819f-106">El espacio de direcciones de cada proceso es privado y no es accesible para otros procesos a menos que sea compartido.</span><span class="sxs-lookup"><span data-stu-id="4819f-106">The address space for each process is private and cannot be accessed by other processes unless it is shared.</span></span>

<span data-ttu-id="4819f-107">Una dirección virtual no representa la ubicación física real de un objeto en la memoria; en su lugar, el sistema mantiene una *tabla de páginas* para cada proceso, que es una estructura de datos interna que se usa para traducir direcciones virtuales en sus direcciones físicas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="4819f-107">A virtual address does not represent the actual physical location of an object in memory; instead, the system maintains a *page table* for each process, which is an internal data structure used to translate virtual addresses into their corresponding physical addresses.</span></span> <span data-ttu-id="4819f-108">Cada vez que un subproceso hace referencia a una dirección, el sistema traduce la dirección virtual a una dirección física.</span><span class="sxs-lookup"><span data-stu-id="4819f-108">Each time a thread references an address, the system translates the virtual address to a physical address.</span></span>

<span data-ttu-id="4819f-109">El espacio de direcciones virtuales para Windows de 32 bits tiene un tamaño de 4 gigabytes (GB) y se divide en dos particiones: una para su uso por parte del proceso y la otra reservada para su uso por parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="4819f-109">The virtual address space for 32-bit Windows is 4 gigabytes (GB) in size and divided into two partitions: one for use by the process and the other reserved for use by the system.</span></span> <span data-ttu-id="4819f-110">Para obtener más información sobre el espacio de direcciones virtuales en Windows de 64 bits, consulte [espacio de direcciones virtuales en Windows de 64 bits](../winprog64/virtual-address-space.md).</span><span class="sxs-lookup"><span data-stu-id="4819f-110">For more information about the virtual address space in 64-bit Windows, see [Virtual Address Space in 64-bit Windows](../winprog64/virtual-address-space.md).</span></span>

<span data-ttu-id="4819f-111">Para obtener más información acerca de la memoria virtual, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="4819f-111">For more information about virtual memory, see the following topics:</span></span>

-   [<span data-ttu-id="4819f-112">Espacio de direcciones virtuales y almacenamiento físico</span><span class="sxs-lookup"><span data-stu-id="4819f-112">Virtual Address Space and Physical Storage</span></span>](virtual-address-space-and-physical-storage.md)
-   [<span data-ttu-id="4819f-113">Espacio de trabajo</span><span class="sxs-lookup"><span data-stu-id="4819f-113">Working Set</span></span>](working-set.md)
-   [<span data-ttu-id="4819f-114">Estado de la página</span><span class="sxs-lookup"><span data-stu-id="4819f-114">Page State</span></span>](page-state.md)
-   [<span data-ttu-id="4819f-115">Ámbito de la memoria asignada</span><span class="sxs-lookup"><span data-stu-id="4819f-115">Scope of Allocated Memory</span></span>](scope-of-allocated-memory.md)
-   [<span data-ttu-id="4819f-116">Prevención de ejecución de datos</span><span class="sxs-lookup"><span data-stu-id="4819f-116">Data Execution Prevention</span></span>](data-execution-prevention.md)
-   [<span data-ttu-id="4819f-117">Protección de la memoria</span><span class="sxs-lookup"><span data-stu-id="4819f-117">Memory Protection</span></span>](memory-protection.md)
-   [<span data-ttu-id="4819f-118">Límites de memoria para las versiones de Windows</span><span class="sxs-lookup"><span data-stu-id="4819f-118">Memory Limits for Windows Releases</span></span>](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="4819f-119">Espacio de direcciones virtual predeterminado para Windows de 32 bits</span><span class="sxs-lookup"><span data-stu-id="4819f-119">Default Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="4819f-120">En la tabla siguiente se muestra el intervalo de memoria predeterminado para cada partición.</span><span class="sxs-lookup"><span data-stu-id="4819f-120">The following table shows the default memory range for each partition.</span></span>



| <span data-ttu-id="4819f-121">Intervalo de memoria</span><span class="sxs-lookup"><span data-stu-id="4819f-121">Memory range</span></span>                             | <span data-ttu-id="4819f-122">Uso</span><span class="sxs-lookup"><span data-stu-id="4819f-122">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="4819f-123">2 GB inferiores (de 0x00000000 a 0x7FFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="4819f-123">Low 2GB (0x00000000 through 0x7FFFFFFF)</span></span>  | <span data-ttu-id="4819f-124">Utilizado por el proceso.</span><span class="sxs-lookup"><span data-stu-id="4819f-124">Used by the process.</span></span> |
| <span data-ttu-id="4819f-125">2 GB superiores (0x80000000 a 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="4819f-125">High 2GB (0x80000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="4819f-126">Utilizado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="4819f-126">Used by the system.</span></span>  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a><span data-ttu-id="4819f-127">Espacio de direcciones virtuales para Windows de 32 bits con 4GT</span><span class="sxs-lookup"><span data-stu-id="4819f-127">Virtual Address Space for 32-bit Windows with 4GT</span></span>

<span data-ttu-id="4819f-128">Si está habilitada la [optimización de 4 gigabytes](4-gigabyte-tuning.md) (4GT), el intervalo de memoria para cada partición es el siguiente.</span><span class="sxs-lookup"><span data-stu-id="4819f-128">If [4-gigabyte tuning](4-gigabyte-tuning.md) (4GT) is enabled, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="4819f-129">Intervalo de memoria</span><span class="sxs-lookup"><span data-stu-id="4819f-129">Memory range</span></span>                             | <span data-ttu-id="4819f-130">Uso</span><span class="sxs-lookup"><span data-stu-id="4819f-130">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="4819f-131">3 GB bajos (0x00000000 a 0xBFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="4819f-131">Low 3GB (0x00000000 through 0xBFFFFFFF)</span></span>  | <span data-ttu-id="4819f-132">Utilizado por el proceso.</span><span class="sxs-lookup"><span data-stu-id="4819f-132">Used by the process.</span></span> |
| <span data-ttu-id="4819f-133">1 GB alto (de 0xC0000000 a 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="4819f-133">High 1GB (0xC0000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="4819f-134">Utilizado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="4819f-134">Used by the system.</span></span>  |



 

<span data-ttu-id="4819f-135">Una vez habilitada la opción 4GT, un proceso que tiene la marca [**\_ \_ \_ \_ reconocimiento de direcciones grandes del archivo de imagen**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) establecida en su encabezado de imagen tendrá acceso a los 1 GB de memoria adicionales por encima de 2 GB de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="4819f-135">After 4GT is enabled, a process that has the [**IMAGE\_FILE\_LARGE\_ADDRESS\_AWARE**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) flag set in its image header will have access to the additional 1 GB of memory above the low 2 GB.</span></span>

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="4819f-136">Ajuste del espacio de direcciones virtuales para Windows de 32 bits</span><span class="sxs-lookup"><span data-stu-id="4819f-136">Adjusting the Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="4819f-137">Puede usar el siguiente comando para establecer una opción de entrada de arranque que configure el tamaño de la partición que está disponible para que la use el proceso en un valor entre 2048 (2 GB) y 3072 (3 GB):</span><span class="sxs-lookup"><span data-stu-id="4819f-137">You can use the following command to set a boot entry option that configures the size of the partition that is available for use by the process to a value between 2048 (2 GB) and 3072 (3 GB):</span></span>

<span data-ttu-id="4819f-138">[Bcdedit/Set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *megabytes*</span><span class="sxs-lookup"><span data-stu-id="4819f-138">[BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *Megabytes*</span></span>

<span data-ttu-id="4819f-139">Después de establecer la opción de entrada de arranque, el intervalo de memoria para cada partición es el siguiente.</span><span class="sxs-lookup"><span data-stu-id="4819f-139">After the boot entry option is set, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="4819f-140">Intervalo de memoria</span><span class="sxs-lookup"><span data-stu-id="4819f-140">Memory range</span></span>                            | <span data-ttu-id="4819f-141">Uso</span><span class="sxs-lookup"><span data-stu-id="4819f-141">Usage</span></span>                |
|-----------------------------------------|----------------------|
| <span data-ttu-id="4819f-142">Bajo (de 0x00000000 a *megabytes*)</span><span class="sxs-lookup"><span data-stu-id="4819f-142">Low (0x00000000 through *Megabytes*)</span></span>    | <span data-ttu-id="4819f-143">Utilizado por el proceso.</span><span class="sxs-lookup"><span data-stu-id="4819f-143">Used by the process.</span></span> |
| <span data-ttu-id="4819f-144">Alto (*megabytes*+ 1 hasta 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="4819f-144">High (*Megabytes*+1 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="4819f-145">Utilizado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="4819f-145">Used by the system.</span></span>  |



 

<span data-ttu-id="4819f-146">**Windows Server 2003:** Establezca el modificador **/USERVA** en boot.ini en un valor entre 2048 y 3072.</span><span class="sxs-lookup"><span data-stu-id="4819f-146">**Windows Server 2003:** Set the **/USERVA** switch in boot.ini to a value between 2048 and 3072.</span></span>

 

 
