---
title: DRM_OUTPUT_PROTECTION_EX estructura (wmdrmsdk. h)
description: La estructura de protección de salida de DRM \_ \_ \_ contiene información sobre una tecnología de protección de la salida. Esta estructura extiende la \_ \_ protección de salida de DRM agregando un número de versión.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- DRM_OUTPUT_PROTECTION_EX estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709221"
---
# <a name="drm_output_protection_ex-structure"></a>\_Estructura de \_ protección de salida de DRM \_

La estructura de protección de salida de DRM contiene información sobre una tecnología de protección de la salida. **\_ \_ \_** Esta estructura extiende **la \_ \_ protección de salida de DRM** agregando un número de versión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwVersion**
</dt> <dd>

Número de versión.

</dd> <dt>

**guidId**
</dt> <dd>

GUID que identifica la tecnología de protección de la salida.

</dd> <dt>

**dwConfigData**
</dt> <dd>

Datos de configuración de la tecnología.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**DRM \_ La protección de salida de AUDIO \_ \_ \_ ex** y la **protección de salida de \_ vídeo DRM \_ \_ \_ ex** se definen como **\_ \_ protección de salida DRM** en instrucciones **typedef** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_protección de salida de DRM \_**](drm-output-protection.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





