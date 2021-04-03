---
description: El espacio de la dirección virtual del sistema (VA) en los sistemas de 32 bits se puede agotar debido a la fragmentación. Se pueden utilizar varias claves del registro para configurar los límites de memoria en los sistemas de 32 bits que experimentan este problema.
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: Claves del registro de administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913682"
---
# <a name="memory-management-registry-keys"></a><span data-ttu-id="8a6c4-104">Claves del registro de administración de memoria</span><span class="sxs-lookup"><span data-stu-id="8a6c4-104">Memory Management Registry Keys</span></span>

<span data-ttu-id="8a6c4-105">El espacio de la dirección virtual del sistema (VA) en los sistemas de 32 bits se puede agotar debido a la fragmentación.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-105">System virtual address (VA) space on 32-bit systems can become exhausted due to fragmentation.</span></span> <span data-ttu-id="8a6c4-106">Se pueden utilizar varias claves del registro para configurar los límites de memoria en los sistemas de 32 bits que experimentan este problema.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-106">Several registry keys can be used to configure memory limits on 32-bit systems that experience this issue.</span></span> <span data-ttu-id="8a6c4-107">El espacio del sistema VA en los sistemas de 64 bits no está sujeto a agotamiento por fragmentación; por lo tanto, estas claves no tienen ningún efecto en los sistemas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-107">System VA space on 64-bit systems is not subject to exhaustion by fragmentation; therefore, these keys have no effect on 64-bit systems.</span></span>

<span data-ttu-id="8a6c4-108">En los sistemas de 32 bits, estas claves del registro de administración de memoria se deben crear explícitamente en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="8a6c4-108">For 32-bit systems, these memory management registry keys must be explicitly created under the following registry key:</span></span>

<span data-ttu-id="8a6c4-109">**HKEY \_ \_** \\ Control actual **del sistema** de equipo local \\ **configuración** de \\ **control** \\  \\ **Administración** de la memoria de administrador de sesión</span><span class="sxs-lookup"><span data-stu-id="8a6c4-109">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Control**\\**Session Manager**\\**Memory Management**</span></span>

<span data-ttu-id="8a6c4-110">**Windows Server 2008 y Windows Vista:** Estas claves del registro están disponibles en sistemas de 32 bits a partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="8a6c4-110">**Windows Server 2008 and Windows Vista:** These registry keys are available on 32-bit systems starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="8a6c4-111">Para conocer los límites de memoria y espacio de direcciones predeterminados en los sistemas de 32 y 64 bits, consulte [límites de memoria para las versiones de Windows](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="8a6c4-111">For default memory and address space limits on both 32-bit and 64-bit systems, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span>

<span data-ttu-id="8a6c4-112">En la tabla siguiente se describen las claves del registro de administración de memoria que se pueden usar para configurar los límites de memoria en los sistemas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-112">The following table describes the memory management registry keys that can be used to configure memory limits on 32-bit systems.</span></span> <span data-ttu-id="8a6c4-113">Todas estas claves tienen un tipo de registro \_ DWORD y valores posibles que van de 0 a 2.048 MB.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-113">All of these keys have a REG\_DWORD type and possible values that range from 0 through 2,048 MB.</span></span> <span data-ttu-id="8a6c4-114">El valor predeterminado es 0, lo que significa que no se aplica ningún límite.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-114">The default is 0, which means no limit is enforced.</span></span> <span data-ttu-id="8a6c4-115">Los valores se redondean al siguiente límite de asignación de redondeos del sistema, que es 2 MB en los sistemas de 32 bits con la [extensión de dirección física](physical-address-extension.md) (PAE) habilitada y 4 MB en sistemas de 32 bits que no tienen habilitado PAE.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-115">Values are automatically rounded up to the next system VA allocation boundary, which is 2 MB on 32-bit systems that have [Physical Address Extension](physical-address-extension.md) (PAE) enabled and 4 MB on 32-bit systems that do not have PAE enabled.</span></span>



| <span data-ttu-id="8a6c4-116">Clave</span><span class="sxs-lookup"><span data-stu-id="8a6c4-116">Key</span></span>                   | <span data-ttu-id="8a6c4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a6c4-117">Description</span></span>                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6c4-118">**NonPagedPoolLimit**</span><span class="sxs-lookup"><span data-stu-id="8a6c4-118">**NonPagedPoolLimit**</span></span> | <span data-ttu-id="8a6c4-119">Especifica la cantidad máxima de espacio de fin del sistema que puede usar el bloque no paginado.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-119">Specifies the maximum amount of system VA space that can be used by the nonpaged pool.</span></span> <span data-ttu-id="8a6c4-120">En determinadas condiciones, este límite se puede superar en una pequeña cantidad.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-120">Under certain conditions, this limit may be exceeded by a small amount.</span></span> |
| <span data-ttu-id="8a6c4-121">**PagedPoolLimit**</span><span class="sxs-lookup"><span data-stu-id="8a6c4-121">**PagedPoolLimit**</span></span>    | <span data-ttu-id="8a6c4-122">Especifica la cantidad máxima de espacio de fin del sistema que puede usar el grupo paginado.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-122">Specifies the maximum amount of system VA space that can be used by the paged pool.</span></span>                                                                            |
| <span data-ttu-id="8a6c4-123">**SessionSpaceLimit**</span><span class="sxs-lookup"><span data-stu-id="8a6c4-123">**SessionSpaceLimit**</span></span> | <span data-ttu-id="8a6c4-124">Especifica la cantidad máxima de espacio de fin del sistema que pueden usar las asignaciones de espacio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-124">Specifies the maximum amount of system VA space that can be used by session space allocations.</span></span>                                                                 |
| <span data-ttu-id="8a6c4-125">**SystemCacheLimit**</span><span class="sxs-lookup"><span data-stu-id="8a6c4-125">**SystemCacheLimit**</span></span>  | <span data-ttu-id="8a6c4-126">Especifica la cantidad máxima de espacio de fin del sistema que puede usar la memoria caché del sistema.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-126">Specifies the maximum amount of system VA space that can be used by the system cache.</span></span> <span data-ttu-id="8a6c4-127">En determinadas condiciones, este límite se puede superar en una pequeña cantidad.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-127">Under certain conditions, this limit may be exceeded by a small amount.</span></span>  |
| <span data-ttu-id="8a6c4-128">**SystemPtesLimit**</span><span class="sxs-lookup"><span data-stu-id="8a6c4-128">**SystemPtesLimit**</span></span>   | <span data-ttu-id="8a6c4-129">Especifica la cantidad máxima de espacio de fin del sistema que pueden usar las asignaciones de e/s y otros recursos que consumen las entradas de la tabla de páginas del sistema (PTE).</span><span class="sxs-lookup"><span data-stu-id="8a6c4-129">Specifies the maximum amount of system VA space that can be used by I/O mappings and other resources that consume system page table entries (PTEs).</span></span>            |



 

<span data-ttu-id="8a6c4-130">La determinación de si se está agotando el espacio del sistema VA requiere el uso de un depurador de kernel.</span><span class="sxs-lookup"><span data-stu-id="8a6c4-130">Determining whether system VA space is being exhausted requires the use of a kernel debugger.</span></span> <span data-ttu-id="8a6c4-131">Para obtener más información, vea [Herramientas de depuración de Windows](https://msdn.microsoft.com/library/cc267445.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a6c4-131">For more information, see [Debugging Tools for Windows](https://msdn.microsoft.com/library/cc267445.aspx).</span></span>

 

 



