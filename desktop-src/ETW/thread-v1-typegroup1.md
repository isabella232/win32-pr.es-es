---
description: Esta clase es la clase de tipo de evento para los eventos de inicio de subprocesos. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 412de56f-4f54-46e8-ab60-d47371247e79
title: Thread_V1_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup1
- Thread_V1_TypeGroup1.ProcessId
- Thread_V1_TypeGroup1.TThreadId
- Thread_V1_TypeGroup1.StackBase
- Thread_V1_TypeGroup1.StackLimit
- Thread_V1_TypeGroup1.UserStackBase
- Thread_V1_TypeGroup1.UserStackLimit
- Thread_V1_TypeGroup1.StartAddr
- Thread_V1_TypeGroup1.Win32StartAddr
- Thread_V1_TypeGroup1.WaitMode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 90d8f4afe9d78cc774dea3159a728ccc6d4db52314e692594d026f7e4fe2161c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069445"
---
# <a name="thread_v1_typegroup1-class"></a>Clase \_ \_ TypeGroup1 del subproceso V1

Esta clase es la clase de tipo de evento para los eventos de inicio de subprocesos.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{1, 3}, EventTypeName{"Start", "DCStart"}]
class Thread_V1_TypeGroup1 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  sint8  WaitMode;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ TypeGroup1 de Thread V1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Thread \_ V1 \_ TypeGroup1** tiene estas propiedades.

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1)
</dt> </dl>

Identificador de proceso del subproceso implicado en el evento.

**Windows Server 2003:** Contiene el calificador Format("x").

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

TThreadId
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2)
</dt> </dl>

Identificador de subproceso del subproceso implicado en el evento.

**Windows Server 2003:** Contiene el calificador Format("x").

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

WaitMode
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(9), Format("c")
</dt> </dl>

No se usa.

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

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Subproceso \_ V1**](thread-v1.md)
</dt> </dl>

 

 




