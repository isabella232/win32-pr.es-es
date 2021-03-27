---
description: Esta clase es la clase de tipo de evento para procesar eventos de contador. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Process_V2_TypeGroup2 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup2
- Process_V2_TypeGroup2.ProcessId
- Process_V2_TypeGroup2.PageFaultCount
- Process_V2_TypeGroup2.HandleCount
- Process_V2_TypeGroup2.Reserved
- Process_V2_TypeGroup2.PeakVirtualSize
- Process_V2_TypeGroup2.PeakWorkingSetSize
- Process_V2_TypeGroup2.PeakPagefileUsage
- Process_V2_TypeGroup2.QuotaPeakPagedPoolUsage
- Process_V2_TypeGroup2.QuotaPeakNonPagedPoolUsage
- Process_V2_TypeGroup2.VirtualSize
- Process_V2_TypeGroup2.WorkingSetSize
- Process_V2_TypeGroup2.PagefileUsage
- Process_V2_TypeGroup2.QuotaPagedPoolUsage
- Process_V2_TypeGroup2.QuotaNonPagedPoolUsage
- Process_V2_TypeGroup2.PrivatePageCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 284b77da03b53f9c2662c8729a7bf6606c45630a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912325"
---
# <a name="process_v2_typegroup2-class"></a><span data-ttu-id="9a759-104">\_ \_ Clase TypeGroup2 de proceso V2</span><span class="sxs-lookup"><span data-stu-id="9a759-104">Process\_V2\_TypeGroup2 class</span></span>

<span data-ttu-id="9a759-105">Esta clase es la clase de tipo de evento para procesar eventos de contador.</span><span class="sxs-lookup"><span data-stu-id="9a759-105">This class is the event type class for process counter events.</span></span>

<span data-ttu-id="9a759-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="9a759-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a759-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a759-107">Syntax</span></span>

``` syntax
[EventType{32, 33}, EventTypeName{"PerfCtr", PerfCtrRundown"}]
class Process_V2_TypeGroup2 : Process_V2
{
  uint32 ProcessId;
  uint32 PageFaultCount;
  uint32 HandleCount;
  uint32 Reserved;
  object PeakVirtualSize;
  object PeakWorkingSetSize;
  object PeakPagefileUsage;
  object QuotaPeakPagedPoolUsage;
  object QuotaPeakNonPagedPoolUsage;
  object VirtualSize;
  object WorkingSetSize;
  object PagefileUsage;
  object QuotaPagedPoolUsage;
  object QuotaNonPagedPoolUsage;
  object PrivatePageCount;
};
```

## <a name="members"></a><span data-ttu-id="9a759-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9a759-108">Members</span></span>

<span data-ttu-id="9a759-109">La **clase \_ \_ TypeGroup2 de Process V2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9a759-109">The **Process\_V2\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="9a759-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a759-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a759-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a759-111">Properties</span></span>

<span data-ttu-id="9a759-112">La **clase \_ \_ TypeGroup2 de proceso V2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9a759-112">The **Process\_V2\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a759-113">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="9a759-113">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a759-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-116">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="9a759-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="9a759-117">Recuento de identificadores usados.</span><span class="sxs-lookup"><span data-stu-id="9a759-117">Count of used handles.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-118">**PageFaultCount**</span><span class="sxs-lookup"><span data-stu-id="9a759-118">**PageFaultCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a759-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-121">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="9a759-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="9a759-122">Recuento de errores de página.</span><span class="sxs-lookup"><span data-stu-id="9a759-122">Count of page faults.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-123">**PagefileUsage**</span><span class="sxs-lookup"><span data-stu-id="9a759-123">**PagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-124">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="9a759-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-126">Calificadores: WmiDataId (12), extensión ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="9a759-126">Qualifiers: WmiDataId(12), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="9a759-127">Uso del archivo de paginación actual.</span><span class="sxs-lookup"><span data-stu-id="9a759-127">Current page file usage.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-128">**PeakPagefileUsage**</span><span class="sxs-lookup"><span data-stu-id="9a759-128">**PeakPagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-129">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="9a759-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-131">Calificadores: WmiDataId (7), extensión ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="9a759-131">Qualifiers: WmiDataId(7), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="9a759-132">Tamaño de archivo de página más grande usado.</span><span class="sxs-lookup"><span data-stu-id="9a759-132">Largest page file size used.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-133">**PeakVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="9a759-133">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-134">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="9a759-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-136">Calificadores: WmiDataId (5), extensión ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="9a759-136">Qualifiers: WmiDataId(5), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="9a759-137">Tamaño de página virtual más grande usado.</span><span class="sxs-lookup"><span data-stu-id="9a759-137">Largest virtual page size used.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-138">**PeakWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="9a759-138">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-139">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="9a759-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-141">Calificadores: WmiDataId (6), extensión ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="9a759-141">Qualifiers: WmiDataId(6), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="9a759-142">Mayor tamaño del espacio de trabajo usado.</span><span class="sxs-lookup"><span data-stu-id="9a759-142">Largest working set size used.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-143">**PrivatePageCount**</span><span class="sxs-lookup"><span data-stu-id="9a759-143">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-144">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="9a759-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-146">Calificadores: WmiDataId (15), extensión ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="9a759-146">Qualifiers: WmiDataId(15), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="9a759-147">Recuento de páginas físicas privadas actuales.</span><span class="sxs-lookup"><span data-stu-id="9a759-147">Current private physical page count.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-148">ProcessId</span><span class="sxs-lookup"><span data-stu-id="9a759-148">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a759-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-151">Calificadores: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="9a759-151">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="9a759-152">Identificador de proceso global que puede usar para identificar un proceso.</span><span class="sxs-lookup"><span data-stu-id="9a759-152">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="9a759-153">El valor es válido desde el momento en que se crea un proceso hasta que se termina.</span><span class="sxs-lookup"><span data-stu-id="9a759-153">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-154">**QuotaNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="9a759-154">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-155">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="9a759-155">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-157">Calificadores: WmiDataId (14), extensión ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="9a759-157">Qualifiers: WmiDataId(14), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="9a759-158">Uso de memoria no paginada actual.</span><span class="sxs-lookup"><span data-stu-id="9a759-158">Current committed non-paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-159">**QuotaPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="9a759-159">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-160">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="9a759-160">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-162">Calificadores: WmiDataId (13), extensión ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="9a759-162">Qualifiers: WmiDataId(13), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="9a759-163">Uso de memoria paginada actual.</span><span class="sxs-lookup"><span data-stu-id="9a759-163">Current committed paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-164">**QuotaPeakNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="9a759-164">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-165">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="9a759-165">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-167">Calificadores: WmiDataId (9), extensión ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="9a759-167">Qualifiers: WmiDataId(9), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="9a759-168">Mayor memoria no paginada confirmada utilizada.</span><span class="sxs-lookup"><span data-stu-id="9a759-168">Largest committed non-paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-169">**QuotaPeakPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="9a759-169">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-170">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="9a759-170">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-172">Calificadores: WmiDataId (8), extensión ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="9a759-172">Qualifiers: WmiDataId(8), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="9a759-173">Mayor memoria paginada confirmada utilizada.</span><span class="sxs-lookup"><span data-stu-id="9a759-173">Largest committed paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-174">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="9a759-174">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-175">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a759-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-177">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="9a759-177">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="9a759-178">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9a759-178">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-179">**VirtualSize**</span><span class="sxs-lookup"><span data-stu-id="9a759-179">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-180">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="9a759-180">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-182">Calificadores: WmiDataId (10), extensión ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="9a759-182">Qualifiers: WmiDataId(10), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="9a759-183">Tamaño actual de la página virtual.</span><span class="sxs-lookup"><span data-stu-id="9a759-183">Current virtual page size.</span></span>

</dd> <dt>

<span data-ttu-id="9a759-184">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="9a759-184">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a759-185">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="9a759-185">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9a759-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a759-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a759-187">Calificadores: WmiDataId (11), extensión ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="9a759-187">Qualifiers: WmiDataId(11), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="9a759-188">Tamaño del espacio de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="9a759-188">Current working set size.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a759-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a759-189">Remarks</span></span>

<span data-ttu-id="9a759-190">Estos eventos se registran cuando finaliza el proceso.</span><span class="sxs-lookup"><span data-stu-id="9a759-190">These events are logged when the process ends.</span></span> <span data-ttu-id="9a759-191">El evento indica el modo en que un proceso controla el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="9a759-191">The event indicates how a process handled memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a759-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a759-192">Requirements</span></span>



| <span data-ttu-id="9a759-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a759-193">Requirement</span></span> | <span data-ttu-id="9a759-194">Value</span><span class="sxs-lookup"><span data-stu-id="9a759-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9a759-195">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a759-195">Minimum supported client</span></span><br/> | <span data-ttu-id="9a759-196">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9a759-196">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9a759-197">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a759-197">Minimum supported server</span></span><br/> | <span data-ttu-id="9a759-198">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a759-198">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a759-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a759-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a759-200">**Proceso \_ V2**</span><span class="sxs-lookup"><span data-stu-id="9a759-200">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




