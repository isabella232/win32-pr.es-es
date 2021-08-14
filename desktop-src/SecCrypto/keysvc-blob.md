---
description: La estructura KEYSVC \_ BLOB define un BLOB de servicio de claves. La función RKeyPFXInstall usa esta estructura.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: KEYSVC_BLOB estructura (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 7e71a090558b31444c550146a2cb99f062080db9b80e7d69561ff891b93262b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992975"
---
# <a name="keysvc_blob-structure"></a>ESTRUCTURA DE BLOBS KEYSVC \_

La **estructura KEYSVC \_ BLOB** define un BLOB de servicio de claves. La función [**RKeyPFXInstall**](rkeypfxinstall.md) usa esta estructura.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Cb**
</dt> <dd>

Valor **ULONG** que especifica el tamaño, en bytes, de **pb**.

</dd> <dt>

**pb**
</dt> <dd>

Puntero a un **BYTE que** contiene el BLOB, en [*formato PKCS \# 12.*](../secgloss/p-gly.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**CADENA UNICODE KEYSVC \_ \_**](keysvc-unicode-string.md)
</dt> </dl>

 

 
