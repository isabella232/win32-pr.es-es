---
description: La \_ estructura de cadena Unicode KEYSVC \_ define una cadena Unicode y una longitud máxima para la cadena. La función RKeyPFXInstall usa esta estructura.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: KEYSVC_UNICODE_STRING estructura (Rkeysvcc. h)
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
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688672"
---
# <a name="keysvc_unicode_string-structure"></a>KEYSVC \_ estructura de \_ cadena Unicode

La estructura de **\_ \_ cadena Unicode KEYSVC** define una cadena [*Unicode*](../secgloss/u-gly.md) y una longitud máxima para la cadena. La función [**RKeyPFXInstall**](rkeypfxinstall.md) usa esta estructura.

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

Valor **USHORT** que especifica la longitud, en bytes, que se usa para el **búfer**.

</dd> <dt>

**MaximumLength**
</dt> <dd>

Valor **USHORT** que especifica la longitud máxima, en bytes, permitida para el **búfer**.

</dd> <dt>

**Buffer**
</dt> <dd>

Un puntero a un valor **USHORT** que representa la cadena Unicode.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**\_BLOB KEYSVC**](keysvc-blob.md)
</dt> </dl>

 

 
