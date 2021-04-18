---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS estructura (wmdrmsdk. h)
description: La \_ \_ \_ \_ estructura de ID. de protección de salida de audio DRM contiene una lista de identificadores de protección de salida de audio.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718963"
---
# <a name="drm_audio_output_protection_ids-structure"></a>\_Estructura de \_ IDS de protección de salida de audio DRM \_ \_

La estructura de ID. de **\_ protección de salida de audio \_ \_ \_ DRM** contiene una lista de identificadores de protección de salida de audio.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cEntries**
</dt> <dd>

Número de entradas de la matriz **rgAop** .

</dd> <dt>

**rgAop**
</dt> <dd>

Matriz de estructuras de **\_ protección de \_ salida \_ de audio DRM** . **DRM \_ La \_ \_ protección de salida de audio** es un tipo definido como [**\_ \_ protección de salida de DRM**](drm-output-protection.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_ \_ \_ identificadores de protección de salida de \_ audio DRM \_**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**\_ \_ \_ identificadores de protección de salida de vídeo DRM \_**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





