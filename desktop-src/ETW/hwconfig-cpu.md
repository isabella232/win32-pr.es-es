---
description: La \_ clase de CPU HWConfig es la clase de tipo de evento para los eventos de configuración de la CPU. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: a94714c6-009c-4300-a0a0-b7b3ce94f91e
title: HWConfig_CPU (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_CPU
- HWConfig_CPU.MHz
- HWConfig_CPU.NumberOfProcessors
- HWConfig_CPU.MemSize
- HWConfig_CPU.PageSize
- HWConfig_CPU.AllocationGranularity
- HWConfig_CPU.ComputerName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 493952e25080d4a64e018477ca1b45033c8747af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984798"
---
# <a name="hwconfig_cpu-class"></a><span data-ttu-id="dc1c5-104">\_Clase de CPU HWConfig</span><span class="sxs-lookup"><span data-stu-id="dc1c5-104">HWConfig\_CPU class</span></span>

<span data-ttu-id="dc1c5-105">La clase de **\_ CPU HWConfig** es la clase de tipo de evento para los eventos de configuración de la CPU.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-105">The **HWConfig\_CPU** class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="dc1c5-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc1c5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc1c5-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class HWConfig_CPU : HWConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  string ComputerName;
};
```

## <a name="members"></a><span data-ttu-id="dc1c5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc1c5-108">Members</span></span>

<span data-ttu-id="dc1c5-109">La clase de **\_ CPU HWConfig** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dc1c5-109">The **HWConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="dc1c5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc1c5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc1c5-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc1c5-111">Properties</span></span>

<span data-ttu-id="dc1c5-112">La clase de **\_ CPU HWConfig** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-112">The **HWConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc1c5-113">AllocationGranularity</span><span class="sxs-lookup"><span data-stu-id="dc1c5-113">AllocationGranularity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc1c5-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc1c5-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc1c5-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc1c5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc1c5-116">Calificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="dc1c5-117">Granularidad con la que se asigna la memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-117">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="dc1c5-118">ComputerName</span><span class="sxs-lookup"><span data-stu-id="dc1c5-118">ComputerName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc1c5-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc1c5-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc1c5-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc1c5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc1c5-121">Calificadores: WmiDataId (6), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="dc1c5-121">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="dc1c5-122">Nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-122">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="dc1c5-123">MemSize</span><span class="sxs-lookup"><span data-stu-id="dc1c5-123">MemSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc1c5-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc1c5-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc1c5-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc1c5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc1c5-126">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="dc1c5-127">Cantidad total de memoria física disponible para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-127">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="dc1c5-128">MHz</span><span class="sxs-lookup"><span data-stu-id="dc1c5-128">MHz</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc1c5-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc1c5-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc1c5-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc1c5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc1c5-131">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="dc1c5-132">Velocidad máxima del procesador, en megahercios.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-132">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="dc1c5-133">NumberOfProcessors</span><span class="sxs-lookup"><span data-stu-id="dc1c5-133">NumberOfProcessors</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc1c5-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc1c5-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc1c5-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc1c5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc1c5-136">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="dc1c5-137">Número de procesadores del equipo.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-137">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="dc1c5-138">PageSize</span><span class="sxs-lookup"><span data-stu-id="dc1c5-138">PageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc1c5-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc1c5-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc1c5-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc1c5-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc1c5-141">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="dc1c5-142">Tamaño de una página de intercambio, en bytes.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-142">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc1c5-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc1c5-143">Requirements</span></span>



| <span data-ttu-id="dc1c5-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc1c5-144">Requirement</span></span> | <span data-ttu-id="dc1c5-145">Value</span><span class="sxs-lookup"><span data-stu-id="dc1c5-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="dc1c5-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc1c5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="dc1c5-147">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="dc1c5-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dc1c5-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc1c5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="dc1c5-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dc1c5-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="dc1c5-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc1c5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc1c5-151">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="dc1c5-151">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




