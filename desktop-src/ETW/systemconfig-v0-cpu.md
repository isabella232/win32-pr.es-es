---
description: 'SystemConfig_V0_CPU clase : esta clase es la clase de tipo de evento para los eventos de configuración de CPU.'
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: SystemConfig_V0_CPU clase
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
ms.openlocfilehash: de3b63def40cb6ead40f6f4c95625603cfc581ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105993"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="42e68-103">Clase de CPU SystemConfig \_ V0 \_</span><span class="sxs-lookup"><span data-stu-id="42e68-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="42e68-104">Esta clase es la clase de tipo de evento para los eventos de configuración de CPU.</span><span class="sxs-lookup"><span data-stu-id="42e68-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="42e68-105">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="42e68-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="42e68-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42e68-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="42e68-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="42e68-107">Members</span></span>

<span data-ttu-id="42e68-108">La **clase de CPU SystemConfig \_ V0 \_** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="42e68-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="42e68-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42e68-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42e68-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42e68-110">Properties</span></span>

<span data-ttu-id="42e68-111">La **clase de CPU SystemConfig \_ V0 \_** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="42e68-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42e68-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="42e68-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42e68-113">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="42e68-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42e68-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42e68-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42e68-115">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="42e68-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="42e68-116">Granularidad con la que se asigna la memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="42e68-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="42e68-117">**nombreDeEquipo**</span><span class="sxs-lookup"><span data-stu-id="42e68-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42e68-118">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="42e68-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="42e68-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42e68-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42e68-120">Calificadores: **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="42e68-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="42e68-121">Nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="42e68-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="42e68-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="42e68-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42e68-123">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="42e68-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="42e68-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42e68-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42e68-125">Calificadores: **WmiDataId** (7), **Max** (132)</span><span class="sxs-lookup"><span data-stu-id="42e68-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="42e68-126">Nombre del dominio en el que el equipo es miembro.</span><span class="sxs-lookup"><span data-stu-id="42e68-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="42e68-127">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="42e68-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42e68-128">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="42e68-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42e68-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42e68-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42e68-130">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="42e68-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="42e68-131">Cantidad total de memoria física disponible para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="42e68-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="42e68-132">**MHz**</span><span class="sxs-lookup"><span data-stu-id="42e68-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42e68-133">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="42e68-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42e68-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42e68-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42e68-135">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="42e68-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="42e68-136">Velocidad máxima del procesador, en megahercios.</span><span class="sxs-lookup"><span data-stu-id="42e68-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="42e68-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="42e68-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42e68-138">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="42e68-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42e68-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42e68-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42e68-140">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="42e68-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="42e68-141">Número de procesadores del equipo.</span><span class="sxs-lookup"><span data-stu-id="42e68-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="42e68-142">**Pagesize**</span><span class="sxs-lookup"><span data-stu-id="42e68-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42e68-143">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="42e68-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42e68-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42e68-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42e68-145">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="42e68-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="42e68-146">Tamaño de una página de intercambio, en bytes.</span><span class="sxs-lookup"><span data-stu-id="42e68-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42e68-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42e68-147">Requirements</span></span>



| <span data-ttu-id="42e68-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="42e68-148">Requirement</span></span> | <span data-ttu-id="42e68-149">Valor</span><span class="sxs-lookup"><span data-stu-id="42e68-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42e68-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42e68-150">Minimum supported client</span></span><br/> | <span data-ttu-id="42e68-151">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="42e68-151">None supported</span></span><br/>                            |
| <span data-ttu-id="42e68-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42e68-152">Minimum supported server</span></span><br/> | <span data-ttu-id="42e68-153">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="42e68-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42e68-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="42e68-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e68-155">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="42e68-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




