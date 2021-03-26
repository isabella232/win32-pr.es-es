---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de la CPU.
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: SystemConfig_V0_CPU (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_CPU
- SystemConfig_V0_CPU.MHz
- SystemConfig_V0_CPU.NumberOfProcessors
- SystemConfig_V0_CPU.MemSize
- SystemConfig_V0_CPU.PageSize
- SystemConfig_V0_CPU.AllocationGranularity
- SystemConfig_V0_CPU.ComputerName
- SystemConfig_V0_CPU.DomainName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6963201f76afa40e9b1741dc2936fa2ab4433a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002790"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="35e70-103">\_Clase SystemConfig V0 \_ CPU</span><span class="sxs-lookup"><span data-stu-id="35e70-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="35e70-104">Esta clase es la clase de tipo de evento para los eventos de configuración de la CPU.</span><span class="sxs-lookup"><span data-stu-id="35e70-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="35e70-105">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="35e70-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e70-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35e70-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_V0_CPU : SystemConfig_V0
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
};
```

## <a name="members"></a><span data-ttu-id="35e70-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="35e70-107">Members</span></span>

<span data-ttu-id="35e70-108">La clase de **\_ \_ CPU SystemConfig V0** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="35e70-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="35e70-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35e70-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35e70-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35e70-110">Properties</span></span>

<span data-ttu-id="35e70-111">La clase de **\_ \_ CPU SystemConfig V0** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="35e70-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35e70-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="35e70-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e70-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35e70-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35e70-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35e70-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e70-115">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="35e70-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="35e70-116">Granularidad con la que se asigna la memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="35e70-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="35e70-117">**nombreDeEquipo**</span><span class="sxs-lookup"><span data-stu-id="35e70-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e70-118">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="35e70-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="35e70-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35e70-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e70-120">Calificadores: **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="35e70-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="35e70-121">Nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="35e70-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="35e70-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="35e70-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e70-123">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="35e70-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="35e70-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35e70-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e70-125">Calificadores: **WmiDataId** (7), **Max** (132)</span><span class="sxs-lookup"><span data-stu-id="35e70-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="35e70-126">Nombre del dominio al que pertenece el equipo.</span><span class="sxs-lookup"><span data-stu-id="35e70-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="35e70-127">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="35e70-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e70-128">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35e70-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35e70-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35e70-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e70-130">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="35e70-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="35e70-131">Cantidad total de memoria física disponible para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="35e70-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="35e70-132">**MHz**</span><span class="sxs-lookup"><span data-stu-id="35e70-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e70-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35e70-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35e70-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35e70-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e70-135">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="35e70-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="35e70-136">Velocidad máxima del procesador, en megahercios.</span><span class="sxs-lookup"><span data-stu-id="35e70-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="35e70-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="35e70-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e70-138">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35e70-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35e70-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35e70-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e70-140">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="35e70-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="35e70-141">Número de procesadores del equipo.</span><span class="sxs-lookup"><span data-stu-id="35e70-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="35e70-142">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="35e70-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e70-143">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35e70-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35e70-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35e70-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e70-145">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="35e70-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="35e70-146">Tamaño de una página de intercambio, en bytes.</span><span class="sxs-lookup"><span data-stu-id="35e70-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35e70-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35e70-147">Requirements</span></span>



| <span data-ttu-id="35e70-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="35e70-148">Requirement</span></span> | <span data-ttu-id="35e70-149">Value</span><span class="sxs-lookup"><span data-stu-id="35e70-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35e70-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35e70-150">Minimum supported client</span></span><br/> | <span data-ttu-id="35e70-151">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="35e70-151">None supported</span></span><br/>                            |
| <span data-ttu-id="35e70-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35e70-152">Minimum supported server</span></span><br/> | <span data-ttu-id="35e70-153">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="35e70-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35e70-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="35e70-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e70-155">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="35e70-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




