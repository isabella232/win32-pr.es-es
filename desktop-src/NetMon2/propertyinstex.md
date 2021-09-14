---
description: La estructura PROPERTYINSTEX define una instancia de propiedad extendida de forma libre.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: Estructura PROPERTYINSTEX (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362132"
---
# <a name="propertyinstex-structure"></a>PROPERTYINSTEX (estructura)

La **estructura PROPERTYINSTEX** define una instancia de propiedad extendida de forma libre.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a>Members

<dl> <dt>

**Duración**
</dt> <dd>

Longitud de los datos en bytes.

</dd> <dt>

**LengthEx**
</dt> <dd>

Longitud de los datos extendidos.

</dd> <dt>

**lpData**
</dt> <dd>

Puntero a los datos extendidos.

</dd> <dt>

**Byte**
</dt> <dd>

Puntero a los **datos BYTE.**

</dd> <dt>

**Word**
</dt> <dd>

Puntero a los **datos de WORD.**

</dd> <dt>

**Dword**
</dt> <dd>

Puntero a los **datos DWORD.**

</dd> <dt>

**LargeInt**
</dt> <dd>

Puntero a los **datos LARGEINT.**

</dd> <dt>

**SysTime**
</dt> <dd>

Puntero a los **datos SYSTEMTIME.**

</dd> <dt>

**TypedString**
</dt> <dd>

Cadena con tipo que puede tener datos extendidos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




