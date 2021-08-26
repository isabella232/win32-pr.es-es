---
description: Evento de seguimiento de administración de memoria para una operación de asignación de montón.
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: ETW_HEAP_EVENT_ALLOC evento (Ntwmi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 111c9268cb6ad174dc79323a9b867923e6264428f939caeae7089685e62f4318
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963205"
---
# <a name="etw_heap_event_alloc-event"></a>Evento ETW \_ HEAP \_ EVENT \_ ALLOC

El **evento ETW \_ HEAP EVENT \_ \_ ALLOC** es un evento de seguimiento de administración de memoria para una operación de asignación de montón.


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Identificador del montón donde se asignó la memoria. Este es el identificador del montón que una aplicación pasó a la [**función AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) cuando se asignó la memoria.

</dd> <dt>

*Tamaño* 
</dt> <dd>

Tamaño en bytes asignados desde el montón.

</dd> <dt>

*Dirección* 
</dt> <dd>

Dirección de la memoria que se asignó.

</dd> <dt>

*Origen* 
</dt> <dd>

Origen de la memoria que el asignador usó para la asignación del montón.

En la tabla siguiente se enumeran los valores posibles para *el parámetro Source* tal como se define en el archivo de encabezado *ntetw.h:*



| Value                                                                                                                                                                                                                                                                               | Significado                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <dt>**MEMORY \_ DE \_ LOOKASIDE**</dt> <dt>1</dt> </dl>                                       | Memoria de la lista de aspecto.<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <dt>**MEMORY \_ DESDE \_ LOWFRAG**</dt> <dt>2</dt> </dl>                                             | Memoria del montón de baja fragmentación.<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <dt>**MEMORY \_ FROM \_ MAINPATH**</dt> <dt>3</dt> </dl>                                          | Memoria de la ruta de acceso del código principal.<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **MEMORIA \_ DE \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Memoria de la ruta de acceso lenta.<br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**MEMORY \_ FROM \_ INVALID**</dt> <dt>5</dt> </dl>                                             | Memoria que no era válida.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**MEMORY \_ FROM \_ SEGMENT \_ HEAP**</dt> <dt>6</dt> </dl>                             | Este valor está reservado para uso futuro y nunca se devolverá.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **evento ETW \_ HEAP EVENT \_ \_ ALLOC** se registra en todas las asignaciones de montón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Ntwmi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de seguimiento de administración de memoria](memory-management-tracing-events.md)
</dt> </dl>

 

 
