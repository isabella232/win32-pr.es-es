---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX estructura (wmdrmsdk. h)
description: La \_ \_ \_ \_ estructura de restricciones de vídeo analógico de WMDRM contiene información amplia sobre una restricción para reproducir el contenido como vídeo analógico.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59c9ca5f58cf2adadeb5a6a0618457472cde976c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699529"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a>\_Restricciones de vídeo analógico de WMDRM ( \_ \_ \_ estructura)

La estructura de **\_ \_ \_ restricciones de \_ vídeo analógico de WMDRM** contiene información amplia sobre una restricción para reproducir el contenido como vídeo analógico.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwVersion**
</dt> <dd>

Número de versión.

</dd> <dt>

**guidRestrictionID**
</dt> <dd>

IDENTIFICADOR de restricción.

</dd> <dt>

**cbRestrictionData**
</dt> <dd>

Tamaño de los datos de restricción en bytes.

</dd> <dt>

**pbRestrictionData**
</dt> <dd>

Datos de restricción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> <dt>

[**\_restricciones de \_ vídeo \_ analógico de WMDRM**](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





