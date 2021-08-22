---
description: Evento de seguimiento de administración de memoria para una operación de reasignación del montón.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: ETW_HEAP_EVENT_REALLOC evento (Ntwmi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_REALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 705f31eaf403c4edd608c0b3347713e43ec3c81746b5efde90e14b7213425963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067875"
---
# <a name="etw_heap_event_realloc-event"></a>Evento ETW \_ HEAP \_ EVENT \_ REALLOC

El **evento ETW \_ HEAP EVENT \_ \_ REALLOC** es un evento de seguimiento de administración de memoria para una operación de reasignación del montón.


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Identificador del montón donde se asignó la memoria. Este es el identificador del montón que una aplicación pasó a la [**función AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) cuando se asignó la memoria.

</dd> <dt>

*NewAddress* 
</dt> <dd>

Nueva dirección de la memoria que se asignó.

</dd> <dt>

*OldAddress* 
</dt> <dd>

Dirección antigua de la memoria que se asignó anteriormente.

</dd> <dt>

*NewSize* 
</dt> <dd>

Nuevo tamaño en bytes asignados desde el montón.

</dd> <dt>

*OldSize* 
</dt> <dd>

Tamaño anterior en bytes asignados previamente desde el montón.

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
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **MEMORIA \_ DE \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Memoria de c lenta.<br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**MEMORY \_ FROM \_ INVALID**</dt> <dt>5</dt> </dl>                                             | Memoria que no era válida.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**MEMORY \_ FROM \_ SEGMENT \_ HEAP**</dt> <dt>6</dt> </dl>                             | Este valor está reservado para uso futuro y nunca se devolverá.<br/> |



 

</dd> </dl>

Este evento no tiene parámetros.

## <a name="remarks"></a>Comentarios

El **evento ETW \_ HEAP EVENT \_ \_ REALLOC** se registra en todas las reasignaciones de montón.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Ntwmi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de seguimiento de administración de memoria](memory-management-tracing-events.md)
</dt> </dl>

 

 
