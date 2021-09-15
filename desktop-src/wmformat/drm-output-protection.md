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
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359927"
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



## <a name="members"></a>Members

<dl> <dt>

**guidId**
</dt> <dd>

GUID que identifica la tecnología de protección de salida.

</dd> <dt>

**bConfigData**
</dt> <dd>

Datos de configuración de la tecnología.

</dd> </dl>

## <a name="remarks"></a>Observaciones

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

 

 





