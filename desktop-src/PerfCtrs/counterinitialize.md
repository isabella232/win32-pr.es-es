---
description: Registra el proveedor e inicializa los conjuntos de contadores.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: CounterInitialize ( Función)
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
ms.openlocfilehash: e7c2fb61b53ca1847eefcc453a91f69b3c0602e06277b4858b8f0b733be7f71b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517685"
---
# <a name="counterinitialize-function"></a>CounterInitialize ( Función)

Registra el proveedor e inicializa los conjuntos de contadores.

## <a name="syntax"></a>Sintaxis


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve ERROR \_ SUCCESS si se ejecuta correctamente; de lo contrario, un código de error estándar de Win32.

## <a name="remarks"></a>Comentarios

El proveedor llama a esta función. La función incluye llamadas a la [**función PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) y a [**la función PerfSetCounterSetInfo.**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)

La [**herramienta CTRPP**](ctrpp.md) genera esta función insertda cuando se especifica el **argumento -o.** El nombre de la función incluye una *cadena de* prefijo si especifica el **argumento -prefix.**

Si especifica los **argumentos -MemoryRoutines** o **-NotificationCallback** (o especifica el atributo **de** devolución de llamada para el elemento [**provider),**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) la firma **CounterInitialize** cambia a lo siguiente:

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

Nombre de la función de devolución de llamada [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) que implementa para recibir notificaciones de solicitudes de consumidor (por ejemplo, solicitudes para agregar o quitar contadores de la consulta). Establezca en **NULL** si no implementa la función de devolución de llamada *ControlCallback.*

</dd> <dt>

<span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction
</dt> <dd>

Nombre de la función de [*devolución de llamada AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) a la que LLAMA PERFLIB para asignar memoria. Establezca en **NULL** si no especificó el **argumento -MemoryRoutines.**

</dd> <dt>

<span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction
</dt> <dd>

Nombre de la función de devolución de [*llamada FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) a la que LLAMA PERFLIB para liberar la memoria asignada mediante la [*función AllocateMemory.*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) Se establece **en NULL** *si MemoryAllocationFunction* es **NULL.**

</dd> <dt>

<span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext
</dt> <dd>

Información de contexto que se pasa a la asignación de memoria y a las rutinas libres. Puede ser **NULL.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

