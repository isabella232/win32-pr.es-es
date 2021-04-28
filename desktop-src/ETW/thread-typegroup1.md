---
description: 'Thread_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos de inicio y finalización de subprocesos. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: d9e3e33a-0e59-4753-a8d8-5320cbae9d95
title: Thread_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_TypeGroup1
- Thread_TypeGroup1.ProcessId
- Thread_TypeGroup1.TThreadId
- Thread_TypeGroup1.StackBase
- Thread_TypeGroup1.StackLimit
- Thread_TypeGroup1.UserStackBase
- Thread_TypeGroup1.UserStackLimit
- Thread_TypeGroup1.Affinity
- Thread_TypeGroup1.Win32StartAddr
- Thread_TypeGroup1.TebBase
- Thread_TypeGroup1.SubProcessTag
- Thread_TypeGroup1.BasePriority
- Thread_TypeGroup1.PagePriority
- Thread_TypeGroup1.IoPriority
- Thread_TypeGroup1.ThreadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9693bef4449cc076710a74dd9cef88ae608754b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105713"
---
# <a name="thread_typegroup1-class"></a>Clase \_ TypeGroup1 de subproceso

Esta clase es la clase de tipo de evento para los eventos de inicio y finalización de subprocesos.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_TypeGroup1 : Thread
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 Affinity;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
  uint8  BasePriority;
  uint8  PagePriority;
  uint8  IoPriority;
  uint8  ThreadFlags;
};
```

## <a name="members"></a>Miembros

La **clase \_ Thread TypeGroup1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Thread TypeGroup1** tiene estas propiedades.

<dl> <dt>

Afinidad
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(7), Pointer
</dt> </dl>

Conjunto de procesadores en los que se puede ejecutar el subproceso.

</dd> <dt>

BasePriority
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(11)
</dt> </dl>

Prioridad del programador del subproceso (vea la [**función SetThreadPriority).**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)

</dd> <dt>

IoPriority
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(13)
</dt> </dl>

Sugerencia de prioridad de E/S para programar las E/S generadas por el subproceso.

</dd> <dt>

PagePriority
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(12)
</dt> </dl>

Sugerencia de prioridad de página de memoria para las páginas de memoria a las que tiene acceso el subproceso.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Format("x")
</dt> </dl>

Identificador de proceso del subproceso implicado en el evento.

</dd> <dt>

StackBase
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3), Pointer
</dt> </dl>

Dirección base de la pila del subproceso.

</dd> <dt>

StackLimit
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4), Pointer
</dt> </dl>

Límite de la pila del subproceso.

</dd> <dt>

SubProcessTag
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(10), Format("x")
</dt> </dl>

Identifica el servicio si el subproceso es propiedad de un servicio; de lo contrario, cero.

</dd> <dt>

TebBase
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(9), Pointer
</dt> </dl>

Dirección base del bloque de entorno de subproceso.

</dd> <dt>

ThreadFlags
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(14)
</dt> </dl>

No se utiliza.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Format("x")
</dt> </dl>

Identificador de subproceso del subproceso implicado en el evento.

</dd> <dt>

UserStackBase
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(5), Pointer
</dt> </dl>

Dirección base de la pila de modo de usuario del subproceso.

</dd> <dt>

UserStackLimit
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(6), Pointer
</dt> </dl>

Límite de la pila de modo de usuario del subproceso.

</dd> <dt>

Win32StartAddr
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(8), Pointer
</dt> </dl>

Dirección inicial de la función que va a ejecutar este subproceso.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los tipos de eventos DCStart y DCEnd enumeran los subprocesos que se ejecutan actualmente en el momento en que se inicia y finaliza la sesión del kernel, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Hilo**](thread.md)
</dt> </dl>

 

 
