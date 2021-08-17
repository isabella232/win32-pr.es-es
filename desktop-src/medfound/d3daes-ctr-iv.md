---
description: Contiene un vector de inicialización (IV) para el cifrado de bloques de Estándar de cifrado avanzado de 128 bits en modo CTR (AES-CTR).
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: D3DAES_CTR_IV estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 09535b432ff1af60ad33b622810d0d8a4d190cb81650214aa71b445ba3c22f4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974794"
---
# <a name="d3daes_ctr_iv-structure"></a>Estructura D3DAES \_ CTR \_ IV

Contiene un vector de inicialización (IV) para el cifrado de bloques de Estándar de cifrado avanzado de 128 bits en modo CTR (AES-CTR).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a>Miembros

<dl> <dt>

**IV**
</dt> <dd>

Iv, en formato big-endian.

</dd> <dt>

**Recuento**
</dt> <dd>

Recuento de bloques, en formato big-endian.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura D3DAES \_ CTR \_ IV** y la [**estructura DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) son equivalentes.

Para obtener más información, [**vea DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types.h (incluir D3d9.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




