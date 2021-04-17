---
description: Evento de traza de administración de memoria para una operación de reasignación de montón.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: Evento ETW_HEAP_EVENT_REALLOC (Ntwmi. h)
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
ms.openlocfilehash: 7aec225793967c38b97fecae88d28141e48a3cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687448"
---
# <a name="etw_heap_event_realloc-event"></a>Evento \_ de \_ evento REALLOC del montón ETW \_

El evento de **\_ \_ evento \_ REALLOC del montón ETW** es un evento de seguimiento de administración de memoria para una operación de reasignación del montón.


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Identificador del montón en el que se asignó la memoria. Este es el montón que controla una aplicación pasada a la función [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) cuando se asignó la memoria.

</dd> <dt>

*La* 
</dt> <dd>

La nueva dirección de la memoria que se asignó.

</dd> <dt>

*OldAddress* 
</dt> <dd>

Dirección antigua de la memoria que se asignó previamente.

</dd> <dt>

*NewSize* 
</dt> <dd>

Nuevo tamaño en bytes asignado desde el montón.

</dd> <dt>

*OldSize* 
</dt> <dd>

Tamaño anterior en bytes previamente asignado desde el montón.

</dd> <dt>

*Origen* 
</dt> <dd>

El origen de la memoria que el asignador utilizó para la asignación del montón.

En la tabla siguiente se enumeran los posibles valores para el parámetro *source* tal y como se define en el archivo de encabezado *ntetw. h* :



| Value                                                                                                                                                                                                                                                                               | Significado                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <dt>**Memoria \_ de DESDE \_**</dt> la <dt>primera</dt> de la </dl>                                       | Memoria de la lista de direcciones.<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <dt>**Memoria \_ de DESDE \_ LOWFRAG**</dt> <dt>2</dt> </dl>                                             | Memoria del montón de fragmentación baja.<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <dt>**Memoria \_ de DESDE \_ MAINPATH**</dt> <dt>3</dt> </dl>                                          | Memoria de la ruta de acceso del código principal.<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **Memoria \_ de \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Memoria de c lentamente.<br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**Memoria \_ de DESDE \_ 5 no válidos**</dt> <dt></dt> </dl>                                             | Memoria no válida.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**Memoria \_ de DEL \_ \_ montón de segmentos**</dt> <dt>6</dt> </dl>                             | Este valor se reserva para uso futuro y nunca se devolverá.<br/> |



 

</dd> </dl>

Este evento no tiene parámetros.

## <a name="remarks"></a>Observaciones

El evento de **\_ \_ evento \_ REALLOC del montón ETW** se registra en todas las reasignaciones del montón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Ntwmi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de seguimiento de administración de memoria](memory-management-tracing-events.md)
</dt> </dl>

 

 
