---
description: Esta clase es la clase de tipo de evento para los eventos de inicio del subproceso. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 412de56f-4f54-46e8-ab60-d47371247e79
title: Thread_V1_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup1
- Thread_V1_TypeGroup1.ProcessId
- Thread_V1_TypeGroup1.TThreadId
- Thread_V1_TypeGroup1.StackBase
- Thread_V1_TypeGroup1.StackLimit
- Thread_V1_TypeGroup1.UserStackBase
- Thread_V1_TypeGroup1.UserStackLimit
- Thread_V1_TypeGroup1.StartAddr
- Thread_V1_TypeGroup1.Win32StartAddr
- Thread_V1_TypeGroup1.WaitMode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 13c419b417b614eb9022d1cb7c09a84ca705b3dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002203"
---
# <a name="thread_v1_typegroup1-class"></a><span data-ttu-id="c3a73-104">\_ \_ Clase TypeGroup1 de Thread v1</span><span class="sxs-lookup"><span data-stu-id="c3a73-104">Thread\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="c3a73-105">Esta clase es la clase de tipo de evento para los eventos de inicio del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c3a73-105">This class is the event type class for thread start events.</span></span>

<span data-ttu-id="c3a73-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="c3a73-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a73-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3a73-107">Syntax</span></span>

``` syntax
[EventType{1, 3}, EventTypeName{"Start", "DCStart"}]
class Thread_V1_TypeGroup1 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  sint8  WaitMode;
};
```

## <a name="members"></a><span data-ttu-id="c3a73-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c3a73-108">Members</span></span>

<span data-ttu-id="c3a73-109">La **clase \_ \_ TypeGroup1 del subproceso v1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c3a73-109">The **Thread\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="c3a73-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c3a73-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3a73-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c3a73-111">Properties</span></span>

<span data-ttu-id="c3a73-112">La **clase \_ \_ TypeGroup1 del subproceso v1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c3a73-112">The **Thread\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3a73-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="c3a73-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a73-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a73-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c3a73-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-116">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="c3a73-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="c3a73-117">Identificador de proceso del subproceso implicado en el evento.</span><span class="sxs-lookup"><span data-stu-id="c3a73-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="c3a73-118">**Windows Server 2003:** Contiene el calificador de formato ("x").</span><span class="sxs-lookup"><span data-stu-id="c3a73-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="c3a73-119">StackBase</span><span class="sxs-lookup"><span data-stu-id="c3a73-119">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a73-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a73-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c3a73-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-122">Calificadores: WmiDataId (3), puntero</span><span class="sxs-lookup"><span data-stu-id="c3a73-122">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c3a73-123">Dirección base de la pila del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c3a73-123">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="c3a73-124">StackLimit</span><span class="sxs-lookup"><span data-stu-id="c3a73-124">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a73-125">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a73-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c3a73-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-127">Calificadores: WmiDataId (4), puntero</span><span class="sxs-lookup"><span data-stu-id="c3a73-127">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c3a73-128">Límite de la pila del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c3a73-128">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="c3a73-129">StartAddr</span><span class="sxs-lookup"><span data-stu-id="c3a73-129">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a73-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a73-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c3a73-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-132">Calificadores: WmiDataId (7), puntero</span><span class="sxs-lookup"><span data-stu-id="c3a73-132">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c3a73-133">Dirección de memoria en la que se inicia el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="c3a73-133">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="c3a73-134">TThreadId</span><span class="sxs-lookup"><span data-stu-id="c3a73-134">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a73-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a73-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c3a73-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-137">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="c3a73-137">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="c3a73-138">Identificador de subproceso del subproceso implicado en el evento.</span><span class="sxs-lookup"><span data-stu-id="c3a73-138">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="c3a73-139">**Windows Server 2003:** Contiene el calificador de formato ("x").</span><span class="sxs-lookup"><span data-stu-id="c3a73-139">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="c3a73-140">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="c3a73-140">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a73-141">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a73-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c3a73-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-143">Calificadores: WmiDataId (5), puntero</span><span class="sxs-lookup"><span data-stu-id="c3a73-143">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c3a73-144">Dirección base de la pila de modo de usuario del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c3a73-144">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="c3a73-145">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="c3a73-145">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a73-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a73-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c3a73-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-148">Calificadores: WmiDataId (6), puntero</span><span class="sxs-lookup"><span data-stu-id="c3a73-148">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c3a73-149">Límite de la pila de modo de usuario del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c3a73-149">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="c3a73-150">WaitMode</span><span class="sxs-lookup"><span data-stu-id="c3a73-150">WaitMode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a73-151">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="c3a73-151">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c3a73-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-153">Calificadores: WmiDataId (9), formato ("c")</span><span class="sxs-lookup"><span data-stu-id="c3a73-153">Qualifiers: WmiDataId(9), Format("c")</span></span>
</dt> </dl>

<span data-ttu-id="c3a73-154">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c3a73-154">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3a73-155">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="c3a73-155">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a73-156">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a73-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c3a73-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a73-158">Calificadores: WmiDataId (8), puntero</span><span class="sxs-lookup"><span data-stu-id="c3a73-158">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c3a73-159">Dirección de inicio de la función que va a ejecutar este subproceso.</span><span class="sxs-lookup"><span data-stu-id="c3a73-159">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3a73-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3a73-160">Requirements</span></span>



| <span data-ttu-id="c3a73-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3a73-161">Requirement</span></span> | <span data-ttu-id="c3a73-162">Value</span><span class="sxs-lookup"><span data-stu-id="c3a73-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c3a73-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3a73-163">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a73-164">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c3a73-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c3a73-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3a73-165">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a73-166">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c3a73-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c3a73-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3a73-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a73-168">**Subproceso \_ v1**</span><span class="sxs-lookup"><span data-stu-id="c3a73-168">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




