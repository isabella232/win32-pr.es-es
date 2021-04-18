---
title: DRM_OUTPUT_PROTECTION estructura (wmdrmsdk. h)
description: La estructura de protección de salida de DRM \_ \_ contiene información sobre una tecnología de protección de la salida.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- DRM_OUTPUT_PROTECTION estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708947"
---
# <a name="drm_output_protection-structure"></a>Estructura de protección de \_ salida de DRM \_

La estructura de **\_ \_ protección de salida de DRM** contiene información sobre una tecnología de protección de la salida.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**guidId**
</dt> <dd>

GUID que identifica la tecnología de protección de la salida.

</dd> <dt>

**bConfigData**
</dt> <dd>

Datos de configuración de la tecnología.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**DRM \_ La \_ \_** protección de salida de audio y la **protección de \_ \_ salida \_ de vídeo DRM** se definen como **\_ \_ protección de salida DRM** en instrucciones **typedef** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_protección de salida DRM \_ \_ ex**](drm-output-protection-ex.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





