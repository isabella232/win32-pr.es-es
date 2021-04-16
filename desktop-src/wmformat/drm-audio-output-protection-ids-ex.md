---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX estructura (wmdrmsdk. h)
description: La \_ \_ estructura de los ID. de protección de la salida de audio DRM \_ \_ \_ contiene una lista de identificadores de protección de salida de audio. Esta estructura extiende los \_ \_ \_ identificadores de protección de salida de audio DRM \_ agregando un número de versión.
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX estructura de Windows Media Format
- Formato de Windows Media de estructura
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
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718964"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a>\_Estructura de \_ los \_ \_ identificadores \_ de salida de audio DRM

La estructura de los ID. de protección de la **\_ salida de audio \_ \_ \_ \_ DRM** contiene una lista de identificadores de protección de salida de audio. Esta estructura extiende **los \_ \_ \_ \_ identificadores de protección de salida de audio DRM** agregando un número de versión.

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

Número de entradas de la matriz **rgAop** .

</dd> <dt>

**rgAop**
</dt> <dd>

Matriz de **estructuras \_ \_ ex de \_ protección \_ de salida de audio DRM** . **DRM \_ La \_ protección de salida de audio \_ \_ ex** es un tipo definido como [**protección de \_ salida DRM \_ \_ ex**](drm-output-protection-ex.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_ \_ \_ identificadores de protección de salida de audio DRM \_**](drm-audio-output-protection-ids.md)
</dt> <dt>

[**\_ \_ \_ identificadores de protección de salida de \_ vídeo DRM \_**](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





