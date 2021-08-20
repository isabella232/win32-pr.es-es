---
title: WMDRM_OUTPUT_PROTECTION_LEVELS estructura (Wmdrmsdk.h)
description: La estructura WMDRM OUTPUT PROTECTION LEVELS contiene los niveles de protección de salida \_ (OPL) que requiere una \_ licencia para realizar varias \_ acciones.
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- WMDRM_OUTPUT_PROTECTION_LEVELS windows Media Format de estructura
- estructura windows Formato multimedia
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
ms.openlocfilehash: 4a19d7098266857f8a17e395ad749b216e45ce101278812f67c032943933955a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843968"
---
# <a name="wmdrm_output_protection_levels-structure"></a>Estructura DE NIVELES DE \_ PROTECCIÓN DE SALIDA DE WMDRM \_ \_

La **estructura WMDRM \_ OUTPUT PROTECTION \_ \_ LEVELS** contiene los niveles de protección de salida (OPL) que requiere una licencia para realizar varias acciones.

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

</dd> <dt>

**wMinimumCopyProtectionLevel**
</dt> <dd>

OPL mínimo necesario para copiar el contenido.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El método [**IWMDRMLicense::GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) usa esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





