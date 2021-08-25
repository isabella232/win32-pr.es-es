---
title: DRM_OUTPUT_PROTECTION estructura (Wmdrmsdk.h)
description: La estructura DRM \_ OUTPUT PROTECTION contiene información sobre una tecnología de protección de \_ salida.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- DRM_OUTPUT_PROTECTION windows Media Format de estructura
- estructura windows Formato multimedia
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
ms.openlocfilehash: 82454d8b4982e6546b003ae3977c7a98869d46ba393ea49f0b97773f95572777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881135"
---
# <a name="drm_output_protection-structure"></a>Estructura DE \_ PROTECCIÓN DE SALIDA DE \_ DRM

La **estructura DRM OUTPUT \_ \_ PROTECTION** contiene información sobre una tecnología de protección de salida.

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

GUID que identifica la tecnología de protección de salida.

</dd> <dt>

**bConfigData**
</dt> <dd>

Datos de configuración de la tecnología.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**DRM \_ PROTECCIÓN \_ DE SALIDA \_ DE AUDIO** y DRM VIDEO OUTPUT **\_ \_ \_ PROTECTION** se definen como **DRM OUTPUT PROTECTION \_ \_ en** **instrucciones typedef.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PROTECCIÓN DE \_ SALIDA \_ DE \_ DRM, por ejemplo,**](drm-output-protection-ex.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





