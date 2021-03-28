---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de la CPU.
ms.assetid: 5a24be04-9e5e-4ba9-baaf-b58b79ad947b
title: SystemConfig_CPU (clase)
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
ms.openlocfilehash: d08d0eeac9aa2287576bbb6dfe0e8ce41f116e8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985695"
---
# <a name="systemconfig_cpu-class"></a><span data-ttu-id="bd5cc-103">\_Clase de CPU SystemConfig</span><span class="sxs-lookup"><span data-stu-id="bd5cc-103">SystemConfig\_CPU class</span></span>

<span data-ttu-id="bd5cc-104">Esta clase es la clase de tipo de evento para los eventos de configuración de la CPU.</span><span class="sxs-lookup"><span data-stu-id="bd5cc-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="bd5cc-105">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="bd5cc-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd5cc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd5cc-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="bd5cc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bd5cc-107">Members</span></span>

<span data-ttu-id="bd5cc-108">La clase de **\_ CPU SystemConfig** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bd5cc-108">The **SystemConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="bd5cc-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bd5cc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd5cc-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bd5cc-110">Properties</span></span>

<span data-ttu-id="bd5cc-111">La clase de **\_ CPU SystemConfig** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bd5cc-111">The **SystemConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd5cc-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5cc-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd5cc-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-115">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="bd5cc-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="bd5cc-116">Granularidad con la que se asigna la memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="bd5cc-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="bd5cc-117">**nombreDeEquipo**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5cc-118">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd5cc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-120">Calificadores: **WmiDataId** (6), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-120">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="bd5cc-121">Nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="bd5cc-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="bd5cc-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5cc-123">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd5cc-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-125">Calificadores: **WmiDataId** (7), **Max** (132), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-125">Qualifiers: **WmiDataId** (7), **Max** (132), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="bd5cc-126">Nombre del dominio al que pertenece el equipo.</span><span class="sxs-lookup"><span data-stu-id="bd5cc-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="bd5cc-127">**HyperThreadingFlag**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-127">**HyperThreadingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5cc-128">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd5cc-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-130">Calificadores: **WmiDataId** (8), puntero</span><span class="sxs-lookup"><span data-stu-id="bd5cc-130">Qualifiers: **WmiDataId** (8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="bd5cc-131">Indica si la opción de Hyper-Threading está activada o desactivada para un procesador.</span><span class="sxs-lookup"><span data-stu-id="bd5cc-131">Indicates if the hyper-threading option is on or off for a processor.</span></span> <span data-ttu-id="bd5cc-132">Cada bit refleja el estado de Hyper-Threading de una CPU del equipo.</span><span class="sxs-lookup"><span data-stu-id="bd5cc-132">Each bit reflects the hyper-threading state of a CPU on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="bd5cc-133">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-133">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5cc-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd5cc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-136">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="bd5cc-136">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="bd5cc-137">Cantidad total de memoria física disponible para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bd5cc-137">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="bd5cc-138">**MHz**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-138">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5cc-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd5cc-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-141">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="bd5cc-141">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="bd5cc-142">Velocidad máxima del procesador, en megahercios.</span><span class="sxs-lookup"><span data-stu-id="bd5cc-142">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="bd5cc-143">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-143">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5cc-144">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd5cc-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-146">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="bd5cc-146">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="bd5cc-147">Número de procesadores del equipo.</span><span class="sxs-lookup"><span data-stu-id="bd5cc-147">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="bd5cc-148">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-148">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5cc-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd5cc-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5cc-151">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="bd5cc-151">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="bd5cc-152">Tamaño de una página de intercambio, en bytes.</span><span class="sxs-lookup"><span data-stu-id="bd5cc-152">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd5cc-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd5cc-153">Requirements</span></span>



| <span data-ttu-id="bd5cc-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd5cc-154">Requirement</span></span> | <span data-ttu-id="bd5cc-155">Value</span><span class="sxs-lookup"><span data-stu-id="bd5cc-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bd5cc-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd5cc-156">Minimum supported client</span></span><br/> | <span data-ttu-id="bd5cc-157">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bd5cc-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bd5cc-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd5cc-158">Minimum supported server</span></span><br/> | <span data-ttu-id="bd5cc-159">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd5cc-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd5cc-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd5cc-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5cc-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="bd5cc-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




