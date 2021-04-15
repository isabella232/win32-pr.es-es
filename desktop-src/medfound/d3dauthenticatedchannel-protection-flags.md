---
description: Especifica el nivel de protección del contenido de vídeo.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS estructura (D3d9types. h)
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
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696156"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a>Estructura de marcas de \_ protección de D3DAUTHENTICATEDCHANNEL \_

Especifica el nivel de protección del contenido de vídeo.

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

Si es 1, se habilita la protección de contenido de vídeo.

</dd> <dt>

**OverlayOrFullscreenRequired**
</dt> <dd>

Si es 1, la aplicación requiere que el vídeo se muestre mediante una superposición de hardware o el modo exclusivo de pantalla completa.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado. Establezca todos los bits en cero.

</dd> <dt>

**Valor**
</dt> <dd>

Utilice este miembro para tener acceso a todos los bits de la Unión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




