---
title: DRM_PLAY_OPL estructura (wmdrmsdk. h)
description: La estructura del OPL de reproducción de DRM \_ \_ contiene información sobre los niveles de protección de salida (OPLs) especificados en una licencia para las acciones de reproducción.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- DRM_PLAY_OPL estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700370"
---
# <a name="drm_play_opl-structure"></a>Estructura del OPL de \_ reproducción de DRM \_

La estructura del **\_ \_ OPL de reproducción de DRM** contiene información sobre los niveles de protección de salida (OPLs) especificados en una licencia para las acciones de reproducción.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**minOPL**
</dt> <dd>

[**DRM \_ Estructura \_ de \_ \_ niveles de protección de salida mínima**](drmdrm-minimum-output-protection-levels.md) que contiene el OPL mínimo necesario para reproducir contenido en distintos formatos.

</dd> <dt>

**oplIdReserved**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**vopi**
</dt> <dd>

[**DRM \_ La estructura de \_ \_ \_ IDS de protección de salida de vídeo**](drmdrm-video-output-protection-ids.md) contiene los identificadores de protección de salida de vídeo que se aplican a la reproducción del contenido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**el \_ OPL de copia de DRM \_**](drmdrm-copy-opl.md)
</dt> <dt>

[**el \_ OPL de reproducción de DRM \_ \_ ex**](drm-play-opl-ex.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





