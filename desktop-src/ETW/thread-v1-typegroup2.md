---
description: Esta clase es la clase de tipo de evento para los eventos de finalización de subprocesos. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Thread_V1_TypeGroup2 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: d00e2d535cdc0fe14d2ae0f48fb7809f627b24fe19cdaff5d63750ee9b5f2c42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814242"
---
# <a name="thread_v1_typegroup2-class"></a>Clase \_ \_ TypeGroup2 de Thread V1

Esta clase es la clase de tipo de evento para los eventos de finalización de subprocesos.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ TypeGroup2 de Thread V1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Thread \_ V1 \_ TypeGroup2** tiene estas propiedades.

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

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Subproceso \_ V1**](thread-v1.md)
</dt> </dl>

 

 




