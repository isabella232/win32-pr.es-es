---
description: 'Thread_V2_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos de inicio y finalización de subprocesos. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Thread_V2_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 24ac4655fc374c40eb530828229a319f9ee1375e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105663"
---
# <a name="thread_v2_typegroup1-class"></a>Clase \_ \_ TypeGroup1 de Thread V2

Esta clase es la clase de tipo de evento para los eventos de inicio y finalización de subprocesos.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ TypeGroup1 de Thread V2** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ TypeGroup1 de Thread V2** tiene estas propiedades.

<dl> <dt>

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

Dirinicial
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(7), Pointer
</dt> </dl>

Dirección de memoria en la que se inicia el seguimiento.

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

Dirección base del bloque de entorno de subprocesos.

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

Los tipos de eventos DCStart y DCEnd enumeran los subprocesos que se están ejecutando actualmente en el momento en que se inicia y finaliza la sesión del kernel, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Hilo**](thread.md)
</dt> <dt>

[**Subproceso \_ V2**](thread-v2.md)
</dt> </dl>

 

 




