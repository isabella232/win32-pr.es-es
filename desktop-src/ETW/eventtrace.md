---
description: Clase abstracta de la que se derivan todas las clases de seguimiento de eventos.
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: Clase Eventtracer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: f04399942b39a2da5b746933884a436a65bb370c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810454"
---
# <a name="eventtrace-class"></a><span data-ttu-id="bbc78-103">Clase Eventtracer</span><span class="sxs-lookup"><span data-stu-id="bbc78-103">EventTrace class</span></span>

<span data-ttu-id="bbc78-104">Clase abstracta de la que se derivan todas las clases de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="bbc78-104">An abstract class from which all event trace classes are derived.</span></span>

<span data-ttu-id="bbc78-105">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="bbc78-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc78-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bbc78-106">Syntax</span></span>

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a><span data-ttu-id="bbc78-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bbc78-107">Members</span></span>

<span data-ttu-id="bbc78-108">La clase **eventtracer** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bbc78-108">The **EventTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="bbc78-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bbc78-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bbc78-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bbc78-110">Properties</span></span>

<span data-ttu-id="bbc78-111">La clase **eventtracer** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bbc78-111">The **EventTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bbc78-112">**EventGuid**</span><span class="sxs-lookup"><span data-stu-id="bbc78-112">**EventGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-113">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="bbc78-113">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-115">Calificadores: **WmiDataId** (8), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="bbc78-115">Qualifiers: **WmiDataId** (8), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-116">GUID de la clase de seguimiento de eventos de este evento.</span><span class="sxs-lookup"><span data-stu-id="bbc78-116">Event trace class GUID of this event.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-117">**Eventos**</span><span class="sxs-lookup"><span data-stu-id="bbc78-117">**EventSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-118">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbc78-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-120">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="bbc78-120">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-121">Número total de bytes del evento.</span><span class="sxs-lookup"><span data-stu-id="bbc78-121">Total number of bytes of the event.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-122">**EventType**</span><span class="sxs-lookup"><span data-stu-id="bbc78-122">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-123">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bbc78-123">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-125">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="bbc78-125">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-126">Tipo de evento definido por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="bbc78-126">Provider-defined event type.</span></span> <span data-ttu-id="bbc78-127">Indica la clase de tipo de evento que se va a utilizar para descifrar los datos de eventos definidos por el proveedor (los datos a los que apunta **MofData**.</span><span class="sxs-lookup"><span data-stu-id="bbc78-127">Tells you which event type class to use to decipher the provider-defined event data (the data pointed to by **MofData**.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-128">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="bbc78-128">**InstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbc78-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-131">Calificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="bbc78-131">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-132">Identificador de esta instancia de evento.</span><span class="sxs-lookup"><span data-stu-id="bbc78-132">Identifier of this event instance.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-133">**KernelTime**</span><span class="sxs-lookup"><span data-stu-id="bbc78-133">**KernelTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbc78-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-136">Calificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="bbc78-136">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-137">Tiempo de ejecución transcurrido para instrucciones en modo kernel, en TICs de CPU.</span><span class="sxs-lookup"><span data-stu-id="bbc78-137">Elapsed execution time for kernel-mode instructions, in CPU ticks.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-138">**MofData**</span><span class="sxs-lookup"><span data-stu-id="bbc78-138">**MofData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbc78-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-141">Calificadores: **WmiDataId** (14), **puntero**</span><span class="sxs-lookup"><span data-stu-id="bbc78-141">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-142">Puntero a los datos de evento específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="bbc78-142">Pointer to the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-143">**MofLength**</span><span class="sxs-lookup"><span data-stu-id="bbc78-143">**MofLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-144">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbc78-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-146">Calificadores: **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="bbc78-146">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-147">Longitud de los datos de eventos específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="bbc78-147">Length of the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-148">**ParentGuid**</span><span class="sxs-lookup"><span data-stu-id="bbc78-148">**ParentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-149">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="bbc78-149">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-151">Calificadores: **WmiDataId** (12), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="bbc78-151">Qualifiers: **WmiDataId** (12), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-152">GUID de la clase de seguimiento de eventos de la instancia primaria.</span><span class="sxs-lookup"><span data-stu-id="bbc78-152">Event trace class GUID of the parent instance.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-153">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="bbc78-153">**ParentInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-154">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbc78-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-156">Calificadores: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="bbc78-156">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-157">Identificador de los datos de la instancia primaria.</span><span class="sxs-lookup"><span data-stu-id="bbc78-157">Identifier of the parent instance data.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-158">**ReservedHeaderField**</span><span class="sxs-lookup"><span data-stu-id="bbc78-158">**ReservedHeaderField**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-159">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbc78-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-161">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="bbc78-161">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-162">Reservado.</span><span class="sxs-lookup"><span data-stu-id="bbc78-162">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-163">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="bbc78-163">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-164">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bbc78-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-166">Calificadores: **WmiDataId** (6), **puntero**</span><span class="sxs-lookup"><span data-stu-id="bbc78-166">Qualifiers: **WmiDataId** (6), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-167">Identifica el subproceso que ha generado el evento.</span><span class="sxs-lookup"><span data-stu-id="bbc78-167">Identifies the thread that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-168">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="bbc78-168">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-169">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bbc78-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-171">Calificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="bbc78-171">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-172">Contiene la fecha y hora en que se produjo el evento.</span><span class="sxs-lookup"><span data-stu-id="bbc78-172">Contains the date and time when the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-173">**TraceLevel**</span><span class="sxs-lookup"><span data-stu-id="bbc78-173">**TraceLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-174">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bbc78-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-176">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="bbc78-176">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-177">Valor definido por el proveedor que define el nivel de gravedad usado para generar el evento.</span><span class="sxs-lookup"><span data-stu-id="bbc78-177">Provider-defined value that defines the severity level used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-178">**TraceVersion**</span><span class="sxs-lookup"><span data-stu-id="bbc78-178">**TraceVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-179">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbc78-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-181">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="bbc78-181">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-182">Número de versión definido por el proveedor de la clase de seguimiento de eventos utilizada para generar el evento.</span><span class="sxs-lookup"><span data-stu-id="bbc78-182">Provider-defined version number of the event trace class used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="bbc78-183">**UserTime**</span><span class="sxs-lookup"><span data-stu-id="bbc78-183">**UserTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbc78-184">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbc78-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbc78-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbc78-186">Calificadores: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="bbc78-186">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="bbc78-187">Tiempo de ejecución transcurrido para instrucciones en modo de usuario, en TICs de CPU.</span><span class="sxs-lookup"><span data-stu-id="bbc78-187">Elapsed execution time for user-mode instructions, in CPU ticks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bbc78-188">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bbc78-188">Remarks</span></span>

<span data-ttu-id="bbc78-189">No utilice estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bbc78-189">Do not use these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc78-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbc78-190">Requirements</span></span>



| <span data-ttu-id="bbc78-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbc78-191">Requirement</span></span> | <span data-ttu-id="bbc78-192">Value</span><span class="sxs-lookup"><span data-stu-id="bbc78-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc78-193">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbc78-193">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc78-194">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bbc78-194">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bbc78-195">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbc78-195">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc78-196">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bbc78-196">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bbc78-197">MOF</span><span class="sxs-lookup"><span data-stu-id="bbc78-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbc78-198"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbc78-198"><dt>Wmi.mof</dt></span></span> </dl> |



 

 




