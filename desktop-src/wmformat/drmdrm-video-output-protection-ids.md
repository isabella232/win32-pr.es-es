---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS estructura (Wmdrmsdk.h)
description: La estructura DRM \_ VIDEO \_ OUTPUT PROTECTION \_ \_ IDS contiene una matriz de estructuras DRM \_ VIDEO OUTPUT \_ \_ PROTECTION.
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS structure windows Media Format
- Estructura de windows Formato multimedia
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
ms.openlocfilehash: 9439328ed817da40630c3a600cf7e6db553738a12799babbe9e71c48f28923b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119085877"
---
# <a name="drm_video_output_protection_ids-structure"></a>Estructura DE \_ IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE VÍDEO \_ \_ DRM

La **estructura DRM VIDEO OUTPUT PROTECTION \_ \_ \_ \_ IDS** contiene una matriz de estructuras **DRM VIDEO OUTPUT \_ \_ \_ PROTECTION.**

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

Número de elementos de la matriz a la que hace referencia **rgVop.**

</dd> <dt>

**rgVop**
</dt> <dd>

Dirección de una matriz de estructuras **\_ DRM VIDEO OUTPUT \_ \_ PROTECTION.** **DRM \_ VIDEO \_ OUTPUT \_ PROTECTION es** un tipo definido como DRM OUTPUT [**\_ \_ PROTECTION**](drm-output-protection.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se usa como miembro de la estructura [**\_ \_ OPL de DRM PLAY.**](drmdrm-play-opl.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE AUDIO \_ \_ \_ DRM**](drm-audio-output-protection-ids.md)
</dt> <dt>

[**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE VÍDEO \_ \_ \_ \_ DRM, POR EJEMPLO,**](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





