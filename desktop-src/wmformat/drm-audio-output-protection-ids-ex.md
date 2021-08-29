---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX estructura (Wmdrmsdk.h)
description: La estructura DRM \_ AUDIO \_ OUTPUT PROTECTION \_ \_ IDS EX contiene una lista de \_ identificadores de protección de salida de audio. Esta estructura amplía los identificadores de PROTECCIÓN DE SALIDA DE AUDIO DE DRM \_ \_ \_ \_ agregando un número de versión.
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX structure windows Media Format
- Estructura de windows Formato multimedia
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f08489b15efbfae594138185202db0b5b8472570c8e67a6aa71904236c9b6ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705665"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a>Estructura EX \_ de LA PROTECCIÓN DE SALIDA DE AUDIO \_ \_ \_ \_ DRM

La **estructura DRM AUDIO OUTPUT PROTECTION \_ \_ \_ \_ IDS \_ EX** contiene una lista de identificadores de protección de salida de audio. Esta estructura amplía los identificadores **de PROTECCIÓN DE SALIDA DE AUDIO \_ \_ \_ \_ DE DRM** agregando un número de versión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwVersion**
</dt> <dd>

Número de versión.

</dd> <dt>

**cEntries**
</dt> <dd>

Número de entradas de la **matriz rgAop.**

</dd> <dt>

**rgAop**
</dt> <dd>

Matriz de **estructuras DRM AUDIO OUTPUT PROTECTION \_ \_ \_ \_ EX.** **DRM \_ AUDIO \_ OUTPUT \_ PROTECTION \_ EX** es un tipo definido como [**DRM OUTPUT PROTECTION \_ \_ \_ EX**](drm-output-protection-ex.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE AUDIO \_ \_ \_ DRM**](drm-audio-output-protection-ids.md)
</dt> <dt>

[**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE VÍDEO \_ \_ \_ \_ DRM, POR EJEMPLO,**](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





