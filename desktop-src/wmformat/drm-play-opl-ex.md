---
title: DRM_PLAY_OPL_EX estructura (wmdrmsdk. h)
description: La estructura de la \_ reproducción \_ de OPL de DRM \_ incluye información sobre los niveles de protección de salida (OPLs) especificados en una licencia para las acciones de reproducción.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- DRM_PLAY_OPL_EX estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edf85ee664b33df9c63c390a870401b100327f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708946"
---
# <a name="drm_play_opl_ex-structure"></a>\_Estructura del \_ OPL de reproducción de DRM \_

La estructura de la **\_ reproducción de \_ OPL \_ de DRM** incluye información sobre los niveles de protección de salida (OPLs) especificados en una licencia para las acciones de reproducción.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwVersion**
</dt> <dd>

Número de versión.

</dd> <dt>

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

## <a name="remarks"></a>Observaciones

Esta estructura es idéntica a la estructura del **\_ \_ OPL de reproducción de DRM** , salvo que incluye un número de versión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**el \_ OPL de reproducción de DRM \_**](drmdrm-play-opl.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





