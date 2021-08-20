---
description: Especifica qué bytes se cifran en una superficie de vídeo protegida.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: D3DENCRYPTED_BLOCK_INFO estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 94027dac3956376e32ad10cf7c1b600d9c65f3918e2781ab9da96d4d3891f43b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879738"
---
# <a name="d3dencrypted_block_info-structure"></a>Estructura D3DENCRYPTED \_ BLOCK \_ INFO

Especifica qué bytes se cifran en una superficie de vídeo protegida.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**NumEncryptedBytesAtBeginning**
</dt> <dd>

Número de bytes que se cifran al principio del búfer.

</dd> <dt>

**NumBytesInSkipPattern**
</dt> <dd>

Número de bytes que se omiten después del primer bytes **NumEncryptedBytesAtBeginning** y, a continuación, después de cada bloque de bytes **NumBytesInEncryptPattern.** Los bytes omitido no se cifran.

</dd> <dt>

**NumBytesInEncryptPattern**
</dt> <dd>

Número de bytes que se cifran después de cada bloque de bytes omitido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types.h (incluir D3d9.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




