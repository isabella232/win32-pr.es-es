---
description: 'Thread_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos de inicio y finalización de subprocesos. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: d9e3e33a-0e59-4753-a8d8-5320cbae9d95
title: Thread_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_TypeGroup1
- Thread_TypeGroup1.ProcessId
- Thread_TypeGroup1.TThreadId
- Thread_TypeGroup1.StackBase
- Thread_TypeGroup1.StackLimit
- Thread_TypeGroup1.UserStackBase
- Thread_TypeGroup1.UserStackLimit
- Thread_TypeGroup1.Affinity
- Thread_TypeGroup1.Win32StartAddr
- Thread_TypeGroup1.TebBase
- Thread_TypeGroup1.SubProcessTag
- Thread_TypeGroup1.BasePriority
- Thread_TypeGroup1.PagePriority
- Thread_TypeGroup1.IoPriority
- Thread_TypeGroup1.ThreadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9693bef4449cc076710a74dd9cef88ae608754b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105713"
---
# <a name="thread_typegroup1-class"></a><span data-ttu-id="df9fc-104">Clase \_ TypeGroup1 de subproceso</span><span class="sxs-lookup"><span data-stu-id="df9fc-104">Thread\_TypeGroup1 class</span></span>

<span data-ttu-id="df9fc-105">Esta clase es la clase de tipo de evento para los eventos de inicio y finalización de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="df9fc-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="df9fc-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="df9fc-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="df9fc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df9fc-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_TypeGroup1 : Thread
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 Affinity;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
  uint8  BasePriority;
  uint8  PagePriority;
  uint8  IoPriority;
  uint8  ThreadFlags;
};
```

## <a name="members"></a><span data-ttu-id="df9fc-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="df9fc-108">Members</span></span>

<span data-ttu-id="df9fc-109">La **clase \_ Thread TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="df9fc-109">The **Thread\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="df9fc-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="df9fc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df9fc-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="df9fc-111">Properties</span></span>

<span data-ttu-id="df9fc-112">La **clase \_ Thread TypeGroup1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="df9fc-112">The **Thread\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df9fc-113">Afinidad</span><span class="sxs-lookup"><span data-stu-id="df9fc-113">Affinity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-114">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="df9fc-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-116">Calificadores: WmiDataId(7), Pointer</span><span class="sxs-lookup"><span data-stu-id="df9fc-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-117">Conjunto de procesadores en los que se puede ejecutar el subproceso.</span><span class="sxs-lookup"><span data-stu-id="df9fc-117">The set of processors on which the thread is allowed to run.</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-118">BasePriority</span><span class="sxs-lookup"><span data-stu-id="df9fc-118">BasePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-119">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="df9fc-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-121">Calificadores: WmiDataId(11)</span><span class="sxs-lookup"><span data-stu-id="df9fc-121">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-122">Prioridad del programador del subproceso (vea la [**función SetThreadPriority).**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)</span><span class="sxs-lookup"><span data-stu-id="df9fc-122">The scheduler priority of the thread (see the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function).</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-123">IoPriority</span><span class="sxs-lookup"><span data-stu-id="df9fc-123">IoPriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-124">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="df9fc-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-126">Calificadores: WmiDataId(13)</span><span class="sxs-lookup"><span data-stu-id="df9fc-126">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-127">Sugerencia de prioridad de E/S para programar las E/S generadas por el subproceso.</span><span class="sxs-lookup"><span data-stu-id="df9fc-127">An IO priority hint for scheduling IOs generated by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-128">PagePriority</span><span class="sxs-lookup"><span data-stu-id="df9fc-128">PagePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-129">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="df9fc-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-131">Calificadores: WmiDataId(12)</span><span class="sxs-lookup"><span data-stu-id="df9fc-131">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-132">Sugerencia de prioridad de página de memoria para las páginas de memoria a las que tiene acceso el subproceso.</span><span class="sxs-lookup"><span data-stu-id="df9fc-132">A memory page priority hint for memory pages accessed by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-133">ProcessId</span><span class="sxs-lookup"><span data-stu-id="df9fc-133">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-134">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="df9fc-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-136">Calificadores: WmiDataId(1), Format("x")</span><span class="sxs-lookup"><span data-stu-id="df9fc-136">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-137">Identificador de proceso del subproceso implicado en el evento.</span><span class="sxs-lookup"><span data-stu-id="df9fc-137">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-138">StackBase</span><span class="sxs-lookup"><span data-stu-id="df9fc-138">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-139">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="df9fc-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-141">Calificadores: WmiDataId(3), Pointer</span><span class="sxs-lookup"><span data-stu-id="df9fc-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-142">Dirección base de la pila del subproceso.</span><span class="sxs-lookup"><span data-stu-id="df9fc-142">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-143">StackLimit</span><span class="sxs-lookup"><span data-stu-id="df9fc-143">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-144">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="df9fc-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-146">Calificadores: WmiDataId(4), Pointer</span><span class="sxs-lookup"><span data-stu-id="df9fc-146">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-147">Límite de la pila del subproceso.</span><span class="sxs-lookup"><span data-stu-id="df9fc-147">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-148">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="df9fc-148">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-149">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="df9fc-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-151">Calificadores: WmiDataId(10), Format("x")</span><span class="sxs-lookup"><span data-stu-id="df9fc-151">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-152">Identifica el servicio si el subproceso es propiedad de un servicio; de lo contrario, cero.</span><span class="sxs-lookup"><span data-stu-id="df9fc-152">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-153">TebBase</span><span class="sxs-lookup"><span data-stu-id="df9fc-153">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-154">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="df9fc-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-156">Calificadores: WmiDataId(9), Pointer</span><span class="sxs-lookup"><span data-stu-id="df9fc-156">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-157">Dirección base del bloque de entorno de subproceso.</span><span class="sxs-lookup"><span data-stu-id="df9fc-157">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-158">ThreadFlags</span><span class="sxs-lookup"><span data-stu-id="df9fc-158">ThreadFlags</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-159">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="df9fc-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-161">Calificadores: WmiDataId(14)</span><span class="sxs-lookup"><span data-stu-id="df9fc-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-162">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="df9fc-162">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-163">TThreadId</span><span class="sxs-lookup"><span data-stu-id="df9fc-163">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-164">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="df9fc-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-166">Calificadores: WmiDataId(2), Format("x")</span><span class="sxs-lookup"><span data-stu-id="df9fc-166">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-167">Identificador de subproceso del subproceso implicado en el evento.</span><span class="sxs-lookup"><span data-stu-id="df9fc-167">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-168">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="df9fc-168">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-169">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="df9fc-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-171">Calificadores: WmiDataId(5), Pointer</span><span class="sxs-lookup"><span data-stu-id="df9fc-171">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-172">Dirección base de la pila de modo de usuario del subproceso.</span><span class="sxs-lookup"><span data-stu-id="df9fc-172">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-173">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="df9fc-173">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-174">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="df9fc-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-176">Calificadores: WmiDataId(6), Pointer</span><span class="sxs-lookup"><span data-stu-id="df9fc-176">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-177">Límite de la pila de modo de usuario del subproceso.</span><span class="sxs-lookup"><span data-stu-id="df9fc-177">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="df9fc-178">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="df9fc-178">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9fc-179">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="df9fc-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df9fc-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9fc-181">Calificadores: WmiDataId(8), Pointer</span><span class="sxs-lookup"><span data-stu-id="df9fc-181">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="df9fc-182">Dirección inicial de la función que va a ejecutar este subproceso.</span><span class="sxs-lookup"><span data-stu-id="df9fc-182">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df9fc-183">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df9fc-183">Remarks</span></span>

<span data-ttu-id="df9fc-184">Los tipos de eventos DCStart y DCEnd enumeran los subprocesos que se ejecutan actualmente en el momento en que se inicia y finaliza la sesión del kernel, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="df9fc-184">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="df9fc-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df9fc-185">Requirements</span></span>



| <span data-ttu-id="df9fc-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="df9fc-186">Requirement</span></span> | <span data-ttu-id="df9fc-187">Valor</span><span class="sxs-lookup"><span data-stu-id="df9fc-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="df9fc-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df9fc-188">Minimum supported client</span></span><br/> | <span data-ttu-id="df9fc-189">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="df9fc-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="df9fc-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df9fc-190">Minimum supported server</span></span><br/> | <span data-ttu-id="df9fc-191">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="df9fc-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df9fc-192">Consulte también</span><span class="sxs-lookup"><span data-stu-id="df9fc-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df9fc-193">**Hilo**</span><span class="sxs-lookup"><span data-stu-id="df9fc-193">**Thread**</span></span>](thread.md)
</dt> </dl>

 

 
