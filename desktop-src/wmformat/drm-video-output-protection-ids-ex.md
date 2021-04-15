---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX estructura (wmdrmsdk. h)
description: La \_ \_ \_ \_ estructura de ID. de protección de salida de vídeo DRM \_ contiene una matriz de \_ estructuras de protección de salida de vídeo DRM \_ \_ .
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708142"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a>\_Estructura de \_ los \_ \_ identificadores \_ de salida de vídeo DRM

La estructura de ID. de **\_ protección de salida de vídeo \_ \_ \_ \_ DRM** contiene una matriz de estructuras de **protección de \_ \_ salida \_ de vídeo DRM** .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
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

Número de elementos de la matriz a los que hace referencia **rgVop**.

</dd> <dt>

**rgVop**
</dt> <dd>

Dirección de una matriz de estructuras de **\_ protección de salida de vídeo \_ \_ \_ DRM** . **DRM \_ Protección de salida de vídeo: por \_ \_ \_ ejemplo** , un tipo definido como [**protección de \_ salida DRM \_ \_ ex**](drm-output-protection-ex.md).

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

 

 





