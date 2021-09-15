---
title: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS estructura (Wmdrmsdk.h)
description: La estructura DRM MINIMUM OUTPUT PROTECTION LEVELS contiene los niveles mínimos de protección de salida \_ \_ \_ (OPL) para la reproducción \_ de varios tipos de contenido. Un dispositivo debe admitir el OPL mínimo para que un tipo de datos reciba ese tipo de datos del lector.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS windows Media Format de estructura
- estructura windows Formato multimedia
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060fdda4cd1c3cc665e396a72d46ac05e721abe4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360597"
---
# <a name="drm_minimum_output_protection_levels-structure"></a>ESTRUCTURA DE \_ NIVELES \_ MÍNIMOS DE \_ PROTECCIÓN DE \_ SALIDA DE DRM

La **estructura DRM MINIMUM OUTPUT PROTECTION \_ \_ \_ \_ LEVELS** contiene los niveles mínimos de protección de salida (OPL) para la reproducción de varios tipos de contenido. Un dispositivo debe admitir el OPL mínimo para que un tipo de datos reciba ese tipo de datos del lector.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**wCompressedDigitalVideo**
</dt> <dd>

OPL mínimo necesario para recibir vídeo digital comprimido.

</dd> <dt>

**wUncompressedDigitalVideo**
</dt> <dd>

OPL mínimo necesario para recibir vídeo digital sin comprimir.

</dd> <dt>

**wAnalogVideo**
</dt> <dd>

OPL mínimo necesario para recibir vídeo análogo.

</dd> <dt>

**wCompressedDigitalAudio**
</dt> <dd>

OPL mínimo necesario para recibir audio digital comprimido.

</dd> <dt>

**wUncompressedDigitalAudio**
</dt> <dd>

OPL mínimo necesario para recibir audio digital sin comprimir.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa como miembro de la estructura [**\_ \_ OPL de DRM PLAY.**](drmdrm-play-opl.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





