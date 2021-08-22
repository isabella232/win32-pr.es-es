---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX estructura (Wmdrmsdk.h)
description: La estructura DRM \_ VIDEO \_ OUTPUT PROTECTION \_ \_ IDS EX contiene una matriz de estructuras DRM VIDEO OUTPUT \_ \_ \_ \_ PROTECTION.
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX structure windows Media Format
- Estructura de windows Formato multimedia
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
ms.openlocfilehash: f5482734c2ded470b4e3dc885e32505c556b3106a12518969622f8007cf6e4f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704092"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a>Estructura EX de LA PROTECCIÓN DE SALIDA DE VÍDEO \_ \_ \_ \_ \_ DRM

La **estructura DRM VIDEO OUTPUT PROTECTION \_ \_ \_ \_ IDS \_ EX** contiene una matriz de estructuras **DRM VIDEO OUTPUT \_ \_ \_ PROTECTION.**

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

Número de elementos de la matriz a la que hace referencia **rgVop.**

</dd> <dt>

**rgVop**
</dt> <dd>

Dirección de una matriz de estructuras **DRM VIDEO OUTPUT PROTECTION \_ \_ \_ \_ EX.** **DRM \_ VIDEO \_ OUTPUT \_ PROTECTION \_ EX** es un tipo definido como [**DRM OUTPUT PROTECTION \_ \_ \_ EX**](drm-output-protection-ex.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE AUDIO \_ \_ \_ \_ DRM, POR EJEMPLO,**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE VÍDEO \_ \_ \_ DRM**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





