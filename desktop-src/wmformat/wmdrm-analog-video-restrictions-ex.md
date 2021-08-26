---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX estructura (Wmdrmsdk.h)
description: La estructura WMDRM ANALOG VIDEO RESTRICTIONS EX contiene información extendida sobre una restricción para reproducir \_ \_ contenido como vídeo \_ \_ análogo.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX estructura windows Formato multimedia
- estructura windows Formato multimedia
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9cbacff2d330c869c35eb7a3d1ca46ae6c80a030495ffec42eabc3726436c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006545"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a>Estructura EX \_ DE \_ \_ RESTRICCIONES DE VÍDEO ANÁLOGO DE WMDRM \_

La **estructura WMDRM \_ ANALOG VIDEO \_ \_ RESTRICTIONS \_ EX** contiene información extendida sobre una restricción para reproducir contenido como vídeo análogo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwVersion**
</dt> <dd>

Número de versión.

</dd> <dt>

**guidRestrictionID**
</dt> <dd>

Id. de restricción.

</dd> <dt>

**cbRestrictionData**
</dt> <dd>

Tamaño de los datos de restricción en bytes.

</dd> <dt>

**pbRestrictionData**
</dt> <dd>

Datos de restricción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> <dt>

[**RESTRICCIONES DE \_ VÍDEO ANÁLOGO \_ DE WMDRM \_**](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





