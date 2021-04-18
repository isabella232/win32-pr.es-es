---
title: WMDRM_OUTPUT_PROTECTION_LEVELS estructura (wmdrmsdk. h)
description: La estructura de niveles de protección de salida de WMDRM \_ \_ \_ contiene los niveles de protección de salida (OPLs) requeridos por una licencia para realizar varias acciones.
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- WMDRM_OUTPUT_PROTECTION_LEVELS estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d720a8aef42178da188b71a1635d97031b138397
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718714"
---
# <a name="wmdrm_output_protection_levels-structure"></a>\_Estructura de \_ niveles de protección de salida WMDRM \_

La estructura de niveles de protección de salida de WMDRM contiene los niveles de protección de salida (OPLs) requeridos por una licencia para realizar varias acciones. **\_ \_ \_**

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
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

</dd> <dt>

**wMinimumCopyProtectionLevel**
</dt> <dd>

Mínimo de OPL necesario para copiar el contenido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método [**IWMDRMLicense:: GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) usa esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





