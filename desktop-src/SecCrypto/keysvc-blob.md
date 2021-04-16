---
description: La \_ estructura de blobs KEYSVC define un BLOB de servicio de claves. La función RKeyPFXInstall usa esta estructura.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: KEYSVC_BLOB estructura (Rkeysvcc. h)
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
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669887"
---
# <a name="keysvc_blob-structure"></a>KEYSVC \_ estructura de BLOB

La estructura de **\_ blobs KEYSVC** define un BLOB de servicio de claves. La función [**RKeyPFXInstall**](rkeypfxinstall.md) usa esta estructura.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a>Miembros

<dl> <dt>

**CB**
</dt> <dd>

Valor **ULong** que especifica el tamaño, en bytes, de **PB**.

</dd> <dt>

**PB**
</dt> <dd>

Un puntero a un **byte** que contiene el BLOB, en formato [*PKCS \# 12*](../secgloss/p-gly.md) .

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

[**KEYSVC \_ cadena UNIcode \_**](keysvc-unicode-string.md)
</dt> </dl>

 

 
