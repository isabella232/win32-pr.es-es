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
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569453"
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



## <a name="members"></a>Members

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>D3d9types.h (incluir D3d9.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




