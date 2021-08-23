---
title: DRM_PLAY_OPL estructura (Wmdrmsdk.h)
description: La estructura OPL de DRM PLAY contiene información sobre los niveles de protección \_ de salida (OPL) especificados en una licencia \_ para las acciones de reproducción.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- DRM_PLAY_OPL estructura windows Formato multimedia
- estructura windows Formato multimedia
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
ms.openlocfilehash: 3f649263db5435310d076386c49b2e77960552646e7ea2325190c3f0b94f27bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708315"
---
# <a name="drm_play_opl-structure"></a>Estructura \_ OPL de DRM PLAY \_

La **estructura \_ \_ OPL de DRM PLAY** contiene información sobre los niveles de protección de salida (OPL) especificados en una licencia para las acciones de reproducción.

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

[**DRM \_ ESTRUCTURA \_ DE NIVELES DE PROTECCIÓN DE \_ \_ SALIDA**](drmdrm-minimum-output-protection-levels.md) MÍNIMA que contiene la OPL mínima necesaria para reproducir contenido en distintos formatos.

</dd> <dt>

**oplIdReserved**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**vopi**
</dt> <dd>

[**DRM \_ VIDEO \_ OUTPUT PROTECTION Estructura \_ \_ IDS**](drmdrm-video-output-protection-ids.md) que contiene los identificadores de protección de salida de vídeo que se aplican a la reproducción del contenido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**OPL \_ DE COPIA DE DRM \_**](drmdrm-copy-opl.md)
</dt> <dt>

[**DRM \_ PLAY \_ OPL \_ EX**](drm-play-opl-ex.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





