---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS estructura (wmdrmsdk. h)
description: La \_ \_ \_ estructura de IDS de protección de vídeo de DRM \_ contiene una matriz de \_ estructuras de protección de salida de vídeo DRM \_ \_ .
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51af3ccebec52ab6f6863aeb376ed27f8c8e2467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708205"
---
# <a name="drm_video_output_protection_ids-structure"></a>\_Estructura de \_ IDS de protección de salida de vídeo DRM \_ \_

La estructura de **\_ \_ \_ \_ IDS de protección de vídeo de DRM** contiene una matriz de estructuras de **\_ \_ \_ protección de salida de vídeo DRM** .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cEntries**
</dt> <dd>

Número de elementos de la matriz a los que hace referencia **rgVop**.

</dd> <dt>

**rgVop**
</dt> <dd>

Dirección de una matriz de estructuras de **\_ protección de \_ salida \_ de vídeo DRM** . **DRM \_ La \_ \_ protección de salida de vídeo** es un tipo definido como [**\_ \_ protección de salida de DRM**](drm-output-protection.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa como miembro de la estructura [**del \_ \_ OPL de reproducción de DRM**](drmdrm-play-opl.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_ \_ \_ identificadores de protección de salida de audio DRM \_**](drm-audio-output-protection-ids.md)
</dt> <dt>

[**\_ \_ \_ identificadores de protección de salida de \_ vídeo DRM \_**](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





