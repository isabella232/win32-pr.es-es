---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS estructura (Wmdrmsdk.h)
description: La estructura WMDRM ANALOG VIDEO RESTRICTIONS contiene información sobre una restricción para reproducir \_ \_ contenido como vídeo \_ análogo.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS structure windows Media Format
- Estructura de windows Formato multimedia
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8221fe325983387107f4e0c03f5672a6762502d8865e1d5895a9e48e96b99d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928815"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a>Estructura DE \_ RESTRICCIONES DE VÍDEO ANÁLOGO \_ DE WMDRM \_

La **estructura WMDRM \_ ANALOG VIDEO \_ \_ RESTRICTIONS** contiene información sobre una restricción para reproducir contenido como vídeo análogo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**guidRestrictionID**
</dt> <dd>

Identificador de restricción.

</dd> <dt>

**dwRestrictionData**
</dt> <dd>

Datos de restricción.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se recibe cuando se llama [**a IWMDRMLicense::GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> <dt>

[**RESTRICCIONES DE VÍDEO ANÁLOGO DE WMDRM, \_ \_ POR \_ \_ EJEMPLO,**](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





