---
description: La estructura KEYSVC \_ UNICODE STRING define una cadena Unicode y una longitud máxima para la \_ cadena. La función RKeyPFXInstall usa esta estructura.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: KEYSVC_UNICODE_STRING estructura (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ac1e82ab481b9844e8a21940112c6014a19f111cab53db2974c488dff0982027
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622335"
---
# <a name="keysvc_unicode_string-structure"></a>Estructura DE CADENA \_ UNICODE KEYSVC \_

La **estructura KEYSVC \_ UNICODE \_ STRING** define una [*cadena Unicode*](../secgloss/u-gly.md) y una longitud máxima para la cadena. La función [**RKeyPFXInstall**](rkeypfxinstall.md) usa esta estructura.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Duración**
</dt> <dd>

Valor **USHORT que** especifica la longitud, en bytes, usada para **buffer**.

</dd> <dt>

**MaximumLength**
</dt> <dd>

Valor **USHORT que** especifica la longitud máxima, en bytes, permitida para **buffer**.

</dd> <dt>

**Buffer**
</dt> <dd>

Puntero a un **USHORT que** representa la cadena Unicode.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**KEYSVC \_ BLOB**](keysvc-blob.md)
</dt> </dl>

 

 
