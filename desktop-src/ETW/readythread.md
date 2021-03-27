---
description: Esta clase es la clase de tipo de evento para eventos de subprocesos listos. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: Clase ReadyThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: e10029c0397c16a5a5eb30be6e3db64c0baec596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908104"
---
# <a name="readythread-class"></a><span data-ttu-id="a48f7-104">Clase ReadyThread</span><span class="sxs-lookup"><span data-stu-id="a48f7-104">ReadyThread class</span></span>

<span data-ttu-id="a48f7-105">Esta clase es la clase de tipo de evento para eventos de subprocesos listos.</span><span class="sxs-lookup"><span data-stu-id="a48f7-105">This class is the event type class for ready thread events.</span></span>

<span data-ttu-id="a48f7-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="a48f7-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a48f7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a48f7-107">Syntax</span></span>

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a><span data-ttu-id="a48f7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a48f7-108">Members</span></span>

<span data-ttu-id="a48f7-109">La clase **ReadyThread** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a48f7-109">The **ReadyThread** class has these types of members:</span></span>

-   [<span data-ttu-id="a48f7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a48f7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a48f7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a48f7-111">Properties</span></span>

<span data-ttu-id="a48f7-112">La clase **ReadyThread** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a48f7-112">The **ReadyThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a48f7-113">AdjustIncrement</span><span class="sxs-lookup"><span data-stu-id="a48f7-113">AdjustIncrement</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a48f7-114">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="a48f7-114">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="a48f7-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a48f7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a48f7-116">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="a48f7-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="a48f7-117">Valor por el que se va a ajustar la prioridad.</span><span class="sxs-lookup"><span data-stu-id="a48f7-117">The value by which the priority is being adjusted.</span></span>

</dd> <dt>

<span data-ttu-id="a48f7-118">AdjustReason</span><span class="sxs-lookup"><span data-stu-id="a48f7-118">AdjustReason</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a48f7-119">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="a48f7-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="a48f7-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a48f7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a48f7-121">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="a48f7-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="a48f7-122">Motivo del aumento de prioridad.</span><span class="sxs-lookup"><span data-stu-id="a48f7-122">The reason for the priority boost.</span></span>



| <span data-ttu-id="a48f7-123">Value</span><span class="sxs-lookup"><span data-stu-id="a48f7-123">Value</span></span>                                                                        | <span data-ttu-id="a48f7-124">Significado</span><span class="sxs-lookup"><span data-stu-id="a48f7-124">Meaning</span></span>                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a48f7-125"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a48f7-125"><dt>0</dt></span></span> </dl> | <span data-ttu-id="a48f7-126">Omitir el incremento.</span><span class="sxs-lookup"><span data-stu-id="a48f7-126">Ignore the increment.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="a48f7-127"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a48f7-127"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a48f7-128">Aplique el incremento, que se detendrá de forma incremental al final de cada Quantum.</span><span class="sxs-lookup"><span data-stu-id="a48f7-128">Apply the increment, which will decay incrementally at the end of each quantum.</span></span><br/>                              |
| <dl> <span data-ttu-id="a48f7-129"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a48f7-129"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a48f7-130">Aplique el incremento como aumento que determinará en su totalidad en cuanto a Quantum (normalmente para donaciones prioritarias).</span><span class="sxs-lookup"><span data-stu-id="a48f7-130">Apply the increment as a boost that will decay in its entirety at quantum (typically for priority donation).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a48f7-131">Marca</span><span class="sxs-lookup"><span data-stu-id="a48f7-131">Flag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a48f7-132">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="a48f7-132">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="a48f7-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a48f7-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a48f7-134">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="a48f7-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="a48f7-135">A continuación se indican las posibles marcas de estado:</span><span class="sxs-lookup"><span data-stu-id="a48f7-135">The following are the possible state flags:</span></span>



| <span data-ttu-id="a48f7-136">Value</span><span class="sxs-lookup"><span data-stu-id="a48f7-136">Value</span></span>                                                                          | <span data-ttu-id="a48f7-137">Significado</span><span class="sxs-lookup"><span data-stu-id="a48f7-137">Meaning</span></span>                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a48f7-138"><dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="a48f7-138"><dt>0x1</dt></span></span> </dl> | <span data-ttu-id="a48f7-139">El subproceso se ha prepararon de DPC (llamada a procedimiento diferida).</span><span class="sxs-lookup"><span data-stu-id="a48f7-139">The thread has been readied from DPC (deferred procedure call).</span></span><br/> |
| <dl> <span data-ttu-id="a48f7-140"><dt>0X2</dt></span><span class="sxs-lookup"><span data-stu-id="a48f7-140"><dt>0x2</dt></span></span> </dl> | <span data-ttu-id="a48f7-141">La pila de kernel está intercambiada actualmente.</span><span class="sxs-lookup"><span data-stu-id="a48f7-141">The kernel stack is currently swapped out.</span></span><br/>                      |
| <dl> <span data-ttu-id="a48f7-142"><dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="a48f7-142"><dt>0x4</dt></span></span> </dl> | <span data-ttu-id="a48f7-143">El espacio de direcciones de proceso se intercambia.</span><span class="sxs-lookup"><span data-stu-id="a48f7-143">The process address space is swapped out.</span></span><br/>                       |



 

<span data-ttu-id="a48f7-144">Tenga en cuenta que cuando se intercambia la pila de kernel o el espacio de direcciones de proceso, habrá un evento ReadyThread adicional después de que la pila de kernel o el espacio de direcciones de proceso se haya cambiado de nuevo en y el subproceso esté listo para enviarse.</span><span class="sxs-lookup"><span data-stu-id="a48f7-144">Note that when the kernel stack or the process address space is swapped out, there will be an additional ReadyThread event after the kernel stack or the process address space has been swapped back in and the thread is made ready to be dispatched.</span></span>

</dd> <dt>

<span data-ttu-id="a48f7-145">Reservado</span><span class="sxs-lookup"><span data-stu-id="a48f7-145">Reserved</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a48f7-146">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="a48f7-146">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="a48f7-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a48f7-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a48f7-148">Calificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="a48f7-148">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="a48f7-149">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a48f7-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a48f7-150">TThreadId</span><span class="sxs-lookup"><span data-stu-id="a48f7-150">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a48f7-151">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a48f7-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a48f7-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a48f7-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a48f7-153">Calificadores: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="a48f7-153">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="a48f7-154">Identificador del subproceso del subproceso que se va prepararon para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="a48f7-154">The thread identifier of the thread being readied for execution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a48f7-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a48f7-155">Requirements</span></span>



| <span data-ttu-id="a48f7-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="a48f7-156">Requirement</span></span> | <span data-ttu-id="a48f7-157">Value</span><span class="sxs-lookup"><span data-stu-id="a48f7-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a48f7-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a48f7-158">Minimum supported client</span></span><br/> | <span data-ttu-id="a48f7-159">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a48f7-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a48f7-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a48f7-160">Minimum supported server</span></span><br/> | <span data-ttu-id="a48f7-161">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a48f7-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a48f7-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="a48f7-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a48f7-163">**Subproceso \_ V2**</span><span class="sxs-lookup"><span data-stu-id="a48f7-163">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




