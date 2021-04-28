---
description: 'Thread_V2_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos de inicio y finalización de subprocesos. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Thread_V2_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 24ac4655fc374c40eb530828229a319f9ee1375e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105663"
---
# <a name="thread_v2_typegroup1-class"></a><span data-ttu-id="c967e-104">Clase \_ \_ TypeGroup1 de Thread V2</span><span class="sxs-lookup"><span data-stu-id="c967e-104">Thread\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="c967e-105">Esta clase es la clase de tipo de evento para los eventos de inicio y finalización de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c967e-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="c967e-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="c967e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c967e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c967e-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a><span data-ttu-id="c967e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c967e-108">Members</span></span>

<span data-ttu-id="c967e-109">La **clase \_ \_ TypeGroup1 de Thread V2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c967e-109">The **Thread\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="c967e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c967e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c967e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c967e-111">Properties</span></span>

<span data-ttu-id="c967e-112">La **clase \_ \_ TypeGroup1 de Thread V2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c967e-112">The **Thread\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c967e-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="c967e-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c967e-114">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c967e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c967e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c967e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c967e-116">Calificadores: WmiDataId(1), Format("x")</span><span class="sxs-lookup"><span data-stu-id="c967e-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="c967e-117">Identificador de proceso del subproceso implicado en el evento.</span><span class="sxs-lookup"><span data-stu-id="c967e-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="c967e-118">StackBase</span><span class="sxs-lookup"><span data-stu-id="c967e-118">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c967e-119">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c967e-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c967e-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c967e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c967e-121">Calificadores: WmiDataId(3), Pointer</span><span class="sxs-lookup"><span data-stu-id="c967e-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c967e-122">Dirección base de la pila del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c967e-122">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="c967e-123">StackLimit</span><span class="sxs-lookup"><span data-stu-id="c967e-123">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c967e-124">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c967e-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c967e-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c967e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c967e-126">Calificadores: WmiDataId(4), Pointer</span><span class="sxs-lookup"><span data-stu-id="c967e-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c967e-127">Límite de la pila del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c967e-127">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="c967e-128">Dirinicial</span><span class="sxs-lookup"><span data-stu-id="c967e-128">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c967e-129">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c967e-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c967e-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c967e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c967e-131">Calificadores: WmiDataId(7), Pointer</span><span class="sxs-lookup"><span data-stu-id="c967e-131">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c967e-132">Dirección de memoria en la que se inicia el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="c967e-132">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="c967e-133">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="c967e-133">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c967e-134">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c967e-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c967e-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c967e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c967e-136">Calificadores: WmiDataId(10), Format("x")</span><span class="sxs-lookup"><span data-stu-id="c967e-136">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="c967e-137">Identifica el servicio si el subproceso es propiedad de un servicio; de lo contrario, cero.</span><span class="sxs-lookup"><span data-stu-id="c967e-137">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="c967e-138">TebBase</span><span class="sxs-lookup"><span data-stu-id="c967e-138">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c967e-139">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c967e-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c967e-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c967e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c967e-141">Calificadores: WmiDataId(9), Pointer</span><span class="sxs-lookup"><span data-stu-id="c967e-141">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c967e-142">Dirección base del bloque de entorno de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c967e-142">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="c967e-143">TThreadId</span><span class="sxs-lookup"><span data-stu-id="c967e-143">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c967e-144">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c967e-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c967e-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c967e-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c967e-146">Calificadores: WmiDataId(2), Format("x")</span><span class="sxs-lookup"><span data-stu-id="c967e-146">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="c967e-147">Identificador de subproceso del subproceso implicado en el evento.</span><span class="sxs-lookup"><span data-stu-id="c967e-147">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="c967e-148">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="c967e-148">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c967e-149">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c967e-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c967e-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c967e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c967e-151">Calificadores: WmiDataId(5), Pointer</span><span class="sxs-lookup"><span data-stu-id="c967e-151">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c967e-152">Dirección base de la pila de modo de usuario del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c967e-152">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="c967e-153">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="c967e-153">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c967e-154">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c967e-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c967e-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c967e-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c967e-156">Calificadores: WmiDataId(6), Pointer</span><span class="sxs-lookup"><span data-stu-id="c967e-156">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c967e-157">Límite de la pila de modo de usuario del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c967e-157">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="c967e-158">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="c967e-158">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c967e-159">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c967e-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c967e-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c967e-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c967e-161">Calificadores: WmiDataId(8), Pointer</span><span class="sxs-lookup"><span data-stu-id="c967e-161">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c967e-162">Dirección inicial de la función que va a ejecutar este subproceso.</span><span class="sxs-lookup"><span data-stu-id="c967e-162">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c967e-163">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c967e-163">Remarks</span></span>

<span data-ttu-id="c967e-164">Los tipos de eventos DCStart y DCEnd enumeran los subprocesos que se están ejecutando actualmente en el momento en que se inicia y finaliza la sesión del kernel, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c967e-164">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="c967e-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c967e-165">Requirements</span></span>



| <span data-ttu-id="c967e-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="c967e-166">Requirement</span></span> | <span data-ttu-id="c967e-167">Valor</span><span class="sxs-lookup"><span data-stu-id="c967e-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c967e-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c967e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="c967e-169">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c967e-169">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c967e-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c967e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="c967e-171">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c967e-171">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c967e-172">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c967e-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c967e-173">**Hilo**</span><span class="sxs-lookup"><span data-stu-id="c967e-173">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="c967e-174">**Subproceso \_ V2**</span><span class="sxs-lookup"><span data-stu-id="c967e-174">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




