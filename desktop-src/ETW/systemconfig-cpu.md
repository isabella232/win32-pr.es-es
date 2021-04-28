---
description: 'SystemConfig_CPU clase : esta clase es la clase de tipo de evento para los eventos de configuración de CPU.'
ms.assetid: 5a24be04-9e5e-4ba9-baaf-b58b79ad947b
title: SystemConfig_CPU clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_CPU
- SystemConfig_CPU.MHz
- SystemConfig_CPU.NumberOfProcessors
- SystemConfig_CPU.MemSize
- SystemConfig_CPU.PageSize
- SystemConfig_CPU.AllocationGranularity
- SystemConfig_CPU.ComputerName
- SystemConfig_CPU.DomainName
- SystemConfig_CPU.HyperThreadingFlag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 07efa01bf58aeadfdfe12cd5db4d010a7f6dbca0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106123"
---
# <a name="systemconfig_cpu-class"></a><span data-ttu-id="33ed5-103">Clase de CPU SystemConfig \_</span><span class="sxs-lookup"><span data-stu-id="33ed5-103">SystemConfig\_CPU class</span></span>

<span data-ttu-id="33ed5-104">Esta clase es la clase de tipo de evento para los eventos de configuración de CPU.</span><span class="sxs-lookup"><span data-stu-id="33ed5-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="33ed5-105">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="33ed5-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ed5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33ed5-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_CPU : SystemConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
  uint32 HyperThreadingFlag;
};
```

## <a name="members"></a><span data-ttu-id="33ed5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="33ed5-107">Members</span></span>

<span data-ttu-id="33ed5-108">La **clase de \_ CPU SystemConfig** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="33ed5-108">The **SystemConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="33ed5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33ed5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33ed5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33ed5-110">Properties</span></span>

<span data-ttu-id="33ed5-111">La **clase de \_ CPU SystemConfig** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="33ed5-111">The **SystemConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33ed5-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="33ed5-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ed5-113">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="33ed5-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33ed5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-115">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="33ed5-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="33ed5-116">Granularidad con la que se asigna la memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="33ed5-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="33ed5-117">**nombreDeEquipo**</span><span class="sxs-lookup"><span data-stu-id="33ed5-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ed5-118">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="33ed5-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33ed5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-120">Calificadores: **WmiDataId** (6), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="33ed5-120">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="33ed5-121">Nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="33ed5-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="33ed5-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="33ed5-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ed5-123">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="33ed5-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33ed5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-125">Calificadores: **WmiDataId** (7), **Max** (132), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="33ed5-125">Qualifiers: **WmiDataId** (7), **Max** (132), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="33ed5-126">Nombre del dominio en el que el equipo es miembro.</span><span class="sxs-lookup"><span data-stu-id="33ed5-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="33ed5-127">**HyperThreadingFlag**</span><span class="sxs-lookup"><span data-stu-id="33ed5-127">**HyperThreadingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ed5-128">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="33ed5-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33ed5-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-130">Calificadores: **WmiDataId** (8), Pointer</span><span class="sxs-lookup"><span data-stu-id="33ed5-130">Qualifiers: **WmiDataId** (8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="33ed5-131">Indica si la opción hyper-threading está activa o desactivada para un procesador.</span><span class="sxs-lookup"><span data-stu-id="33ed5-131">Indicates if the hyper-threading option is on or off for a processor.</span></span> <span data-ttu-id="33ed5-132">Cada bit refleja el estado de hyper-threading de una CPU en el equipo.</span><span class="sxs-lookup"><span data-stu-id="33ed5-132">Each bit reflects the hyper-threading state of a CPU on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="33ed5-133">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="33ed5-133">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ed5-134">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="33ed5-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33ed5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-136">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="33ed5-136">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="33ed5-137">Cantidad total de memoria física disponible para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="33ed5-137">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="33ed5-138">**MHz**</span><span class="sxs-lookup"><span data-stu-id="33ed5-138">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ed5-139">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="33ed5-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33ed5-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-141">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="33ed5-141">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="33ed5-142">Velocidad máxima del procesador, en megahercios.</span><span class="sxs-lookup"><span data-stu-id="33ed5-142">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="33ed5-143">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="33ed5-143">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ed5-144">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="33ed5-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33ed5-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-146">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="33ed5-146">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="33ed5-147">Número de procesadores del equipo.</span><span class="sxs-lookup"><span data-stu-id="33ed5-147">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="33ed5-148">**Pagesize**</span><span class="sxs-lookup"><span data-stu-id="33ed5-148">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ed5-149">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="33ed5-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33ed5-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33ed5-151">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="33ed5-151">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="33ed5-152">Tamaño de una página de intercambio, en bytes.</span><span class="sxs-lookup"><span data-stu-id="33ed5-152">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33ed5-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33ed5-153">Requirements</span></span>



| <span data-ttu-id="33ed5-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="33ed5-154">Requirement</span></span> | <span data-ttu-id="33ed5-155">Valor</span><span class="sxs-lookup"><span data-stu-id="33ed5-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="33ed5-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33ed5-156">Minimum supported client</span></span><br/> | <span data-ttu-id="33ed5-157">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="33ed5-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="33ed5-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33ed5-158">Minimum supported server</span></span><br/> | <span data-ttu-id="33ed5-159">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="33ed5-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="33ed5-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="33ed5-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ed5-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="33ed5-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




