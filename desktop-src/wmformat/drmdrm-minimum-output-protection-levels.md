---
title: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS estructura (wmdrmsdk. h)
description: La \_ estructura de \_ niveles de \_ protección de salida mínima de DRM \_ contiene los niveles mínimos de protección de salida (OPLs) para la reproducción de varios tipos de contenido. Un dispositivo debe admitir el valor de OPL mínimo para un tipo de datos para recibir ese tipo de datos del lector.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS estructura de Windows Media Format
- Formato de Windows Media de estructura
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708206"
---
# <a name="drm_minimum_output_protection_levels-structure"></a>\_Estructura de \_ \_ niveles de protección de salida mínima de DRM \_

La estructura de **\_ niveles de \_ \_ protección \_ de salida mínima de DRM** contiene los niveles mínimos de protección de salida (OPLs) para la reproducción de varios tipos de contenido. Un dispositivo debe admitir el valor de OPL mínimo para un tipo de datos para recibir ese tipo de datos del lector.

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



## <a name="members"></a>Miembros

<dl> <dt>

**wCompressedDigitalVideo**
</dt> <dd>

Mínimo de OPL necesario para recibir vídeo digital comprimido.

</dd> <dt>

**wUncompressedDigitalVideo**
</dt> <dd>

Mínimo de OPL necesario para recibir vídeo digital no comprimido.

</dd> <dt>

**wAnalogVideo**
</dt> <dd>

Mínimo de OPL necesario para recibir vídeo analógico.

</dd> <dt>

**wCompressedDigitalAudio**
</dt> <dd>

Mínimo de OPL necesario para recibir audio digital comprimido.

</dd> <dt>

**wUncompressedDigitalAudio**
</dt> <dd>

Mínimo de OPL necesario para recibir audio digital no comprimido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa como miembro de la estructura [**del \_ \_ OPL de reproducción de DRM**](drmdrm-play-opl.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





