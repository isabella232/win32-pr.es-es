---
description: Especifica el nivel de protección para el contenido de vídeo.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1d1b76a6fea0dd6b966bd72001efb187a7a3a14e75b4d41d631e5a1ea163fe94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974714"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a>D3DAUTHENTICATEDCHANNEL PROTECTION FLAGS (ESTRUCTURA DE MARCAS DE PROTECCIÓN DE D3DAUTHENTICATEDCHANNEL) \_ \_

Especifica el nivel de protección para el contenido de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ProtectionEnabled**
</dt> <dd>

Si es 1, la protección de contenido de vídeo está habilitada.

</dd> <dt>

**OverlayOrFullscreenRequired**
</dt> <dd>

Si es 1, la aplicación requiere que el vídeo se muestre mediante una superposición de hardware o un modo exclusivo de pantalla completa.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado. Establezca todos los bits en cero.

</dd> <dt>

**Valor**
</dt> <dd>

Use este miembro para acceder a todos los bits de la unión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




