---
title: DRM_OUTPUT_PROTECTION_EX estructura (Wmdrmsdk.h)
description: La estructura DRM \_ OUTPUT PROTECTION EX contiene información sobre una tecnología de protección de \_ \_ salida. Esta estructura amplía DRM \_ OUTPUT \_ PROTECTION agregando un número de versión.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- DRM_OUTPUT_PROTECTION_EX structure windows Media Format
- Estructura de windows Formato multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360950"
---
# <a name="drm_output_protection_ex-structure"></a>Estructura EX de DRM \_ OUTPUT \_ PROTECTION \_

La **estructura DRM OUTPUT PROTECTION \_ \_ \_ EX** contiene información sobre una tecnología de protección de salida. Esta estructura amplía DRM **\_ OUTPUT \_ PROTECTION** agregando un número de versión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Número de versión.

</dd> <dt>

**guidId**
</dt> <dd>

GUID que identifica la tecnología de protección de salida.

</dd> <dt>

**dwConfigData**
</dt> <dd>

Datos de configuración de la tecnología.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**DRM \_ PROTECCIÓN \_ DE SALIDA DE AUDIO \_ \_ EX** y **DRM VIDEO OUTPUT PROTECTION \_ \_ \_ \_ EX** se definen como **DRM OUTPUT PROTECTION \_ \_ en** **instrucciones typedef.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**PROTECCIÓN DE SALIDA DE DRM \_ \_**](drm-output-protection.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





