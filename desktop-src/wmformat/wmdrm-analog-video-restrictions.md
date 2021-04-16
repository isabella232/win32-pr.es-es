---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS estructura (wmdrmsdk. h)
description: La \_ \_ \_ estructura de restricciones de vídeo analógico de WMDRM contiene información sobre una restricción para reproducir el contenido como vídeo analógico.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS estructura de Windows Media Format
- Formato de Windows Media de estructura
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
ms.openlocfilehash: e3d6b8fe957468baebb6da06f45ba7b37756413c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699528"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a>\_Estructura de \_ restricciones de vídeo analógico de WMDRM \_

La estructura de **\_ \_ \_ restricciones de vídeo analógico de WMDRM** contiene información sobre una restricción para reproducir el contenido como vídeo analógico.

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

## <a name="remarks"></a>Observaciones

Esta estructura se recibe cuando se llama a [**IWMDRMLicense:: GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> <dt>

[**\_restricciones de vídeo analógico de WMDRM \_ \_ \_ ex**](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





