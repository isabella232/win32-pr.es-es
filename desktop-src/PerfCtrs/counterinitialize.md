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
# <a name="counterinitialize-function"></a>Función de contrainicialización

Registra el proveedor e inicializa los conjuntos de contadores.

## <a name="syntax"></a>Sintaxis


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un ERROR Si se realiza correctamente \_ ; en caso contrario, un código de error estándar de Win32.

## <a name="remarks"></a>Observaciones

El proveedor llama a esta función. La función incluye llamadas a la función [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) y a la función [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) .

La herramienta [**CTRPP**](ctrpp.md) genera esta función insertada al especificar el argumento **-o** . El nombre de la función incluye una cadena de *prefijo* si se especifica el argumento **-prefix** .

Si especifica los argumentos **-MemoryRoutines** o **-NotificationCallback** (o especifica el atributo de **devolución de llamada** para el elemento de [**proveedor**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) ), la signatura de **contrainicialización** cambia a lo siguiente:

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

donde,

<dl> <dt>

<span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback
</dt> <dd>

El nombre de la función de devolución de llamada [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) que se implementa para recibir notificaciones de las solicitudes de consumidor (por ejemplo, solicitudes para agregar o quitar contadores de la consulta). Establezca en **null** si no implementa la función de devolución de llamada *ControlCallback* .

</dd> <dt>

<span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction
</dt> <dd>

El nombre de la función de devolución de llamada [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) que PERFLIB llama para asignar memoria. Se establece en **null** si no se especifica el argumento **-MemoryRoutines** .

</dd> <dt>

<span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction
</dt> <dd>

El nombre de la función de devolución de llamada [*FreeMemory (*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) que PERFLIB llama para liberar la memoria asignada mediante la función [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) . Se establece en **null** si *MemoryAllocationFunction* es **null**.

</dd> <dt>

<span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext
</dt> <dd>

Información de contexto que se va a pasar a la asignación de memoria y a las rutinas gratuitas. Puede ser **null**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

