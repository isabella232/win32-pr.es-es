---
description: Registra el proveedor e inicializa los conjuntos de contadores.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: Función de contrainicialización
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterInitialize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18996fc4349a120069a9b38293a11faf70632033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001983"
---
# <a name="counterinitialize-function"></a><span data-ttu-id="7fd7f-103">Función de contrainicialización</span><span class="sxs-lookup"><span data-stu-id="7fd7f-103">CounterInitialize function</span></span>

<span data-ttu-id="7fd7f-104">Registra el proveedor e inicializa los conjuntos de contadores.</span><span class="sxs-lookup"><span data-stu-id="7fd7f-104">Registers the provider and initializes the counter sets.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd7f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fd7f-105">Syntax</span></span>


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="7fd7f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fd7f-106">Parameters</span></span>

<span data-ttu-id="7fd7f-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7fd7f-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7fd7f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fd7f-108">Return value</span></span>

<span data-ttu-id="7fd7f-109">Devuelve un ERROR Si se realiza correctamente \_ ; en caso contrario, un código de error estándar de Win32.</span><span class="sxs-lookup"><span data-stu-id="7fd7f-109">Returns ERROR\_SUCCESS on success; otherwise, a standard Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fd7f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fd7f-110">Remarks</span></span>

<span data-ttu-id="7fd7f-111">El proveedor llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="7fd7f-111">Your provider calls this function.</span></span> <span data-ttu-id="7fd7f-112">La función incluye llamadas a la función [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) y a la función [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="7fd7f-112">The function includes calls to the [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) function and the [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) function.</span></span>

<span data-ttu-id="7fd7f-113">La herramienta [**CTRPP**](ctrpp.md) genera esta función insertada al especificar el argumento **-o** .</span><span class="sxs-lookup"><span data-stu-id="7fd7f-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="7fd7f-114">El nombre de la función incluye una cadena de *prefijo* si se especifica el argumento **-prefix** .</span><span class="sxs-lookup"><span data-stu-id="7fd7f-114">The function's name include a *prefix* string if you specify the **-prefix** argument.</span></span>

<span data-ttu-id="7fd7f-115">Si especifica los argumentos **-MemoryRoutines** o **-NotificationCallback** (o especifica el atributo de **devolución de llamada** para el elemento de [**proveedor**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) ), la signatura de **contrainicialización** cambia a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7fd7f-115">If you specify the **-MemoryRoutines** or **-NotificationCallback** arguments (or specify the **callback** attribute for the [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) element), the **CounterInitialize** signature changes to the following:</span></span>

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

<span data-ttu-id="7fd7f-116">donde,</span><span class="sxs-lookup"><span data-stu-id="7fd7f-116">where,</span></span>

<dl> <dt>

<span data-ttu-id="7fd7f-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback</span><span class="sxs-lookup"><span data-stu-id="7fd7f-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback</span></span>
</dt> <dd>

<span data-ttu-id="7fd7f-118">El nombre de la función de devolución de llamada [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) que se implementa para recibir notificaciones de las solicitudes de consumidor (por ejemplo, solicitudes para agregar o quitar contadores de la consulta).</span><span class="sxs-lookup"><span data-stu-id="7fd7f-118">The name of your [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) callback function that you implement to receive notification of consumer requests (for example, requests to add or remove counters from the query).</span></span> <span data-ttu-id="7fd7f-119">Establezca en **null** si no implementa la función de devolución de llamada *ControlCallback* .</span><span class="sxs-lookup"><span data-stu-id="7fd7f-119">Set to **NULL** if you do not implement the *ControlCallback* callback function.</span></span>

</dd> <dt>

<span data-ttu-id="7fd7f-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction</span><span class="sxs-lookup"><span data-stu-id="7fd7f-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction</span></span>
</dt> <dd>

<span data-ttu-id="7fd7f-121">El nombre de la función de devolución de llamada [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) que PERFLIB llama para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="7fd7f-121">The name of your [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) callback function that PERFLIB calls to allocate memory.</span></span> <span data-ttu-id="7fd7f-122">Se establece en **null** si no se especifica el argumento **-MemoryRoutines** .</span><span class="sxs-lookup"><span data-stu-id="7fd7f-122">Set to **NULL** if you did not specify the **-MemoryRoutines** argument.</span></span>

</dd> <dt>

<span data-ttu-id="7fd7f-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction</span><span class="sxs-lookup"><span data-stu-id="7fd7f-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction</span></span>
</dt> <dd>

<span data-ttu-id="7fd7f-124">El nombre de la función de devolución de llamada [*FreeMemory (*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) que PERFLIB llama para liberar la memoria asignada mediante la función [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) .</span><span class="sxs-lookup"><span data-stu-id="7fd7f-124">The name of your [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) callback function that PERFLIB calls to free the memory allocated using the [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) function.</span></span> <span data-ttu-id="7fd7f-125">Se establece en **null** si *MemoryAllocationFunction* es **null**.</span><span class="sxs-lookup"><span data-stu-id="7fd7f-125">Set to **NULL** if *MemoryAllocationFunction* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7fd7f-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext</span><span class="sxs-lookup"><span data-stu-id="7fd7f-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext</span></span>
</dt> <dd>

<span data-ttu-id="7fd7f-127">Información de contexto que se va a pasar a la asignación de memoria y a las rutinas gratuitas.</span><span class="sxs-lookup"><span data-stu-id="7fd7f-127">Context information to pass to your memory allocation and free routines.</span></span> <span data-ttu-id="7fd7f-128">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="7fd7f-128">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fd7f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fd7f-129">Requirements</span></span>



| <span data-ttu-id="7fd7f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fd7f-130">Requirement</span></span> | <span data-ttu-id="7fd7f-131">Value</span><span class="sxs-lookup"><span data-stu-id="7fd7f-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7fd7f-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fd7f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd7f-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7fd7f-133">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7fd7f-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fd7f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd7f-135">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7fd7f-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

