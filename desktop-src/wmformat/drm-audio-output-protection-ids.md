---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS estructura (Wmdrmsdk.h)
description: La estructura DRM \_ AUDIO \_ OUTPUT PROTECTION \_ \_ IDS contiene una lista de identificadores de protección de salida de audio.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS windows Media Format de estructura
- estructura windows Formato multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574332"
---
# <a name="drm_audio_output_protection_ids-structure"></a>Estructura DE \_ \_ IDENTIFICADORES DE PROTECCIÓN DE SALIDA DE AUDIO \_ \_ DRM

La **estructura DRM AUDIO OUTPUT PROTECTION \_ \_ \_ \_ IDS** contiene una lista de identificadores de protección de salida de audio.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**cEntries**
</dt> <dd>

Número de entradas de la **matriz rgAop.**

</dd> <dt>

**rgAop**
</dt> <dd>

Matriz de **estructuras DRM AUDIO OUTPUT \_ \_ \_ PROTECTION.** **DRM \_ AUDIO \_ OUTPUT \_ PROTECTION es** un tipo definido como DRM OUTPUT [**\_ \_ PROTECTION**](drm-output-protection.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE AUDIO \_ \_ \_ \_ DRM, POR EJEMPLO,**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE VÍDEO \_ \_ \_ DRM**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





