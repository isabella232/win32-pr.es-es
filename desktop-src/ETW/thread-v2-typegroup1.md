---
description: Esta clase es la clase de tipo de evento para los eventos de inicio y fin de subproceso. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Thread_V2_TypeGroup1 (clase)
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
ms.openlocfilehash: c89d573f4eda2580002bedfd0ad17eb9b50c1575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277388"
---
# <a name="thread_v2_typegroup1-class"></a><span data-ttu-id="96d9c-104">\_ \_ Clase TypeGroup1 de Thread V2</span><span class="sxs-lookup"><span data-stu-id="96d9c-104">Thread\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="96d9c-105">Esta clase es la clase de tipo de evento para los eventos de inicio y fin de subproceso.</span><span class="sxs-lookup"><span data-stu-id="96d9c-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="96d9c-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="96d9c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="96d9c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96d9c-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="96d9c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="96d9c-108">Members</span></span>

<span data-ttu-id="96d9c-109">La **clase \_ \_ TypeGroup1 del subproceso V2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="96d9c-109">The **Thread\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="96d9c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96d9c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96d9c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96d9c-111">Properties</span></span>

<span data-ttu-id="96d9c-112">La **clase \_ \_ TypeGroup1 del subproceso V2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="96d9c-112">The **Thread\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96d9c-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="96d9c-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d9c-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96d9c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96d9c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-116">Calificadores: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="96d9c-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="96d9c-117">Identificador de proceso del subproceso implicado en el evento.</span><span class="sxs-lookup"><span data-stu-id="96d9c-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="96d9c-118">StackBase</span><span class="sxs-lookup"><span data-stu-id="96d9c-118">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d9c-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96d9c-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96d9c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-121">Calificadores: WmiDataId (3), puntero</span><span class="sxs-lookup"><span data-stu-id="96d9c-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="96d9c-122">Dirección base de la pila del subproceso.</span><span class="sxs-lookup"><span data-stu-id="96d9c-122">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="96d9c-123">StackLimit</span><span class="sxs-lookup"><span data-stu-id="96d9c-123">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d9c-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96d9c-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96d9c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-126">Calificadores: WmiDataId (4), puntero</span><span class="sxs-lookup"><span data-stu-id="96d9c-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="96d9c-127">Límite de la pila del subproceso.</span><span class="sxs-lookup"><span data-stu-id="96d9c-127">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="96d9c-128">StartAddr</span><span class="sxs-lookup"><span data-stu-id="96d9c-128">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d9c-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96d9c-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96d9c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-131">Calificadores: WmiDataId (7), puntero</span><span class="sxs-lookup"><span data-stu-id="96d9c-131">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="96d9c-132">Dirección de memoria en la que se inicia el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="96d9c-132">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="96d9c-133">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="96d9c-133">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d9c-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96d9c-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96d9c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-136">Calificadores: WmiDataId (10), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="96d9c-136">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="96d9c-137">Identifica el servicio si el subproceso es propiedad de un servicio; de lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="96d9c-137">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="96d9c-138">TebBase</span><span class="sxs-lookup"><span data-stu-id="96d9c-138">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d9c-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96d9c-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96d9c-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-141">Calificadores: WmiDataId (9), puntero</span><span class="sxs-lookup"><span data-stu-id="96d9c-141">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="96d9c-142">Dirección base del bloque del entorno del subproceso.</span><span class="sxs-lookup"><span data-stu-id="96d9c-142">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="96d9c-143">TThreadId</span><span class="sxs-lookup"><span data-stu-id="96d9c-143">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d9c-144">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96d9c-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96d9c-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-146">Calificadores: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="96d9c-146">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="96d9c-147">Identificador de subproceso del subproceso implicado en el evento.</span><span class="sxs-lookup"><span data-stu-id="96d9c-147">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="96d9c-148">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="96d9c-148">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d9c-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96d9c-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96d9c-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-151">Calificadores: WmiDataId (5), puntero</span><span class="sxs-lookup"><span data-stu-id="96d9c-151">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="96d9c-152">Dirección base de la pila de modo de usuario del subproceso.</span><span class="sxs-lookup"><span data-stu-id="96d9c-152">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="96d9c-153">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="96d9c-153">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d9c-154">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96d9c-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96d9c-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-156">Calificadores: WmiDataId (6), puntero</span><span class="sxs-lookup"><span data-stu-id="96d9c-156">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="96d9c-157">Límite de la pila de modo de usuario del subproceso.</span><span class="sxs-lookup"><span data-stu-id="96d9c-157">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="96d9c-158">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="96d9c-158">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d9c-159">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96d9c-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96d9c-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96d9c-161">Calificadores: WmiDataId (8), puntero</span><span class="sxs-lookup"><span data-stu-id="96d9c-161">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="96d9c-162">Dirección de inicio de la función que va a ejecutar este subproceso.</span><span class="sxs-lookup"><span data-stu-id="96d9c-162">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96d9c-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96d9c-163">Remarks</span></span>

<span data-ttu-id="96d9c-164">Los tipos de eventos DCStart y DCEnd enumeran los subprocesos que se están ejecutando actualmente en el momento en que se inicia y finaliza la sesión del kernel, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="96d9c-164">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="96d9c-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96d9c-165">Requirements</span></span>



| <span data-ttu-id="96d9c-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="96d9c-166">Requirement</span></span> | <span data-ttu-id="96d9c-167">Value</span><span class="sxs-lookup"><span data-stu-id="96d9c-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="96d9c-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96d9c-168">Minimum supported client</span></span><br/> | <span data-ttu-id="96d9c-169">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="96d9c-169">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="96d9c-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96d9c-170">Minimum supported server</span></span><br/> | <span data-ttu-id="96d9c-171">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="96d9c-171">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96d9c-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="96d9c-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d9c-173">**Conversaciones**</span><span class="sxs-lookup"><span data-stu-id="96d9c-173">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="96d9c-174">**Subproceso \_ V2**</span><span class="sxs-lookup"><span data-stu-id="96d9c-174">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




