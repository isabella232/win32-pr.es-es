---
title: DRM_PLAY_OPL_EX estructura (Wmdrmsdk.h)
description: La estructura OPL EX de DRM PLAY contiene información sobre los niveles de protección \_ \_ de salida (OL) especificados en una licencia para \_ las acciones de reproducción.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- DRM_PLAY_OPL_EX structure windows Media Format
- Estructura de windows Formato multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360222"
---
# <a name="drm_play_opl_ex-structure"></a>Estructura \_ \_ OPL EX de DRM PLAY \_

La **estructura \_ \_ OPL \_ EX** de DRM PLAY contiene información sobre los niveles de protección de salida (OL) especificados en una licencia para las acciones de reproducción.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Número de versión.

</dd> <dt>

**minOPL**
</dt> <dd>

[**DRM \_ ESTRUCTURA \_ MINIMUM OUTPUT PROTECTION LEVELS \_ \_ que**](drmdrm-minimum-output-protection-levels.md) contiene el OPL mínimo necesario para reproducir contenido en formatos diferentes.

</dd> <dt>

**oplIdReserved**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**vopi**
</dt> <dd>

[**DRM \_ VIDEO \_ OUTPUT PROTECTION Estructura \_ \_ IDS**](drmdrm-video-output-protection-ids.md) que contiene los identificadores de protección de salida de vídeo que se aplican a la reproducción del contenido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura es idéntica a la estructura **\_ \_ OPL de DRM PLAY,** salvo que incluye un número de versión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





