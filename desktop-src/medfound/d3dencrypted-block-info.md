---
description: Especifica qué bytes se cifran en una superficie de vídeo protegida.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: D3DENCRYPTED_BLOCK_INFO estructura (D3d9types. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153646"
---
# <a name="d3dencrypted_block_info-structure"></a>D3DENCRYPTED \_ estructura de información de bloque \_

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

Número de bytes que se omiten después de los primeros **NumEncryptedBytesAtBeginning** bytes y después de cada bloque de **NumBytesInEncryptPattern** bytes. Los bytes omitidos no se cifran.

</dd> <dt>

**NumBytesInEncryptPattern**
</dt> <dd>

Número de bytes que se cifran después de cada bloque de bytes omitidos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>D3d9types. h (incluye d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




