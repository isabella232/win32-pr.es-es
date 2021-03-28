---
description: Esta clase es la clase de tipo de evento para los eventos de asignación virtual. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: PageFault_VirtualAlloc (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_VirtualAlloc
- PageFault_VirtualAlloc.BaseAddress
- PageFault_VirtualAlloc.RegionSize
- PageFault_VirtualAlloc.ProcessId
- PageFault_VirtualAlloc.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: f9e754bc3dc09f492682d5a522a6489cfde27ceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360399"
---
# <a name="pagefault_virtualalloc-class"></a><span data-ttu-id="7b34c-104">Errores \_ VirtualAlloc (clase)</span><span class="sxs-lookup"><span data-stu-id="7b34c-104">PageFault\_VirtualAlloc class</span></span>

<span data-ttu-id="7b34c-105">Esta clase es la clase de tipo de evento para los eventos de asignación virtual.</span><span class="sxs-lookup"><span data-stu-id="7b34c-105">This class is the event type class for virtual allocation events.</span></span>

<span data-ttu-id="7b34c-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="7b34c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b34c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b34c-107">Syntax</span></span>

``` syntax
[EventType{98, 99}, EventTypeName{"VirtualAlloc", "VirtualFree"}]
class PageFault_VirtualAlloc : PageFault_V2
{
  uint32 BaseAddress;
  object RegionSize;
  uint32 ProcessId;
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="7b34c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7b34c-108">Members</span></span>

<span data-ttu-id="7b34c-109">La clase **errores \_ VirtualAlloc** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7b34c-109">The **PageFault\_VirtualAlloc** class has these types of members:</span></span>

-   [<span data-ttu-id="7b34c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b34c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b34c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b34c-111">Properties</span></span>

<span data-ttu-id="7b34c-112">La clase **errores \_ VirtualAlloc** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7b34c-112">The **PageFault\_VirtualAlloc** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b34c-113">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="7b34c-113">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b34c-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b34c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b34c-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b34c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b34c-116">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="7b34c-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7b34c-117">Dirección inicial en la que se ha asignado o liberado la memoria.</span><span class="sxs-lookup"><span data-stu-id="7b34c-117">The starting address at which memory was allocated or freed.</span></span>

</dd> <dt>

<span data-ttu-id="7b34c-118">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="7b34c-118">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b34c-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b34c-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b34c-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b34c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b34c-121">Calificadores: WmiDataId (4), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="7b34c-121">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="7b34c-122">El tipo de asignación de memoria que se ha realizado.</span><span class="sxs-lookup"><span data-stu-id="7b34c-122">The type of memory allocation that was performed.</span></span> <span data-ttu-id="7b34c-123">Para ver los valores posibles, vea el parámetro *flAllocationType* de la función [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) .</span><span class="sxs-lookup"><span data-stu-id="7b34c-123">For possible values, see the *flAllocationType* parameter of the [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) function.</span></span>

</dd> <dt>

<span data-ttu-id="7b34c-124">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="7b34c-124">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b34c-125">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b34c-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b34c-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b34c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b34c-127">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="7b34c-127">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="7b34c-128">Proceso que poseía la memoria (puede ser diferente del subproceso que realizó la asignación).</span><span class="sxs-lookup"><span data-stu-id="7b34c-128">The process that owned the memory (can be different from the thread that performed the allocation).</span></span>

</dd> <dt>

<span data-ttu-id="7b34c-129">**Regiones**</span><span class="sxs-lookup"><span data-stu-id="7b34c-129">**RegionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b34c-130">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="7b34c-130">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7b34c-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b34c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b34c-132">Calificadores: WmiDataId (2), extensión ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="7b34c-132">Qualifiers: WmiDataId(2), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="7b34c-133">Tamaño, en bytes, de la memoria asignada o liberada.</span><span class="sxs-lookup"><span data-stu-id="7b34c-133">The size, in bytes, of the memory that was allocated or freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b34c-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b34c-134">Requirements</span></span>



| <span data-ttu-id="7b34c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b34c-135">Requirement</span></span> | <span data-ttu-id="7b34c-136">Value</span><span class="sxs-lookup"><span data-stu-id="7b34c-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7b34c-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b34c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7b34c-138">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b34c-138">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7b34c-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b34c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7b34c-140">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b34c-140">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b34c-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b34c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b34c-142">**Errores \_ V2**</span><span class="sxs-lookup"><span data-stu-id="7b34c-142">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 
