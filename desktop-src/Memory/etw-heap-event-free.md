---
description: Evento de seguimiento de administración de memoria para una operación sin montón.
ms.assetid: 0CCC59F1-AB96-4B7A-9A86-19CA4FBA4A8A
title: ETW_HEAP_EVENT_FREE evento (Ntwmi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_FREE
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: fd30eccb5848917d752441df79881078dc14d36e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159871"
---
# <a name="etw_heap_event_free-event"></a>Evento ETW \_ HEAP \_ EVENT \_ FREE

El **evento ETW \_ HEAP EVENT FREE \_ \_ es** un evento de seguimiento de administración de memoria para una operación libre del montón.


```C++
typedef struct ETW_HEAP_EVENT_FREE
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Identificador del montón donde se asignó la memoria. Este es el identificador del montón que una aplicación pasó a la [**función AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) cuando se asignó la memoria.

</dd> <dt>

*Dirección* 
</dt> <dd>

Dirección de la memoria que se ha liberado.

</dd> <dt>

*Origen* 
</dt> <dd>

Origen de la memoria que el asignador usó para la asignación del montón.

En la tabla siguiente se enumeran los valores posibles para *el parámetro Source* tal como se define en el archivo de encabezado *ntetw.h:*



| Value                                                                                                                                                                                                                                                                               | Significado                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <dt>**MEMORY \_ DE \_ LOOKASIDE**</dt> <dt>1</dt> </dl>                                       | Memoria de la lista de aspecto.<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <dt>**MEMORY \_ DESDE \_ LOWFRAG**</dt> <dt>2</dt> </dl>                                             | Memoria del montón de fragmentación baja.<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <dt>**MEMORY \_ DESDE \_ MAINPATH**</dt> <dt>3</dt> </dl>                                          | Memoria de la ruta de acceso del código principal.<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **MEMORIA \_ DE \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Memoria de c lenta.<br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**MEMORY \_ FROM \_ INVALID**</dt> <dt>5</dt> </dl>                                             | Memoria que no era válida.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**MEMORY \_ FROM \_ SEGMENT \_ HEAP**</dt> <dt>6</dt> </dl>                             | Este valor está reservado para uso futuro y nunca se devolverá.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **evento ETW \_ HEAP EVENT \_ \_ FREE** se registra en todas las operaciones gratuitas del montón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Ntwmi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Eventos de seguimiento de administración de memoria](memory-management-tracing-events.md)
</dt> </dl>

 

 
