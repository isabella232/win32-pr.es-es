---
title: DRM_LICENSE_STATE_CATEGORY enumeración (Wmdrmsdk.h)
description: El tipo de enumeración DRM LICENSE STATE CATEGORY especifica el tipo de restricción de licencia descrito \_ por una estructura DRM LICENSE STATE \_ \_ \_ \_ \_ DATA.
ms.assetid: 51258be9-2f4d-4f25-97f7-2cac6c155ade
keywords:
- DRM_LICENSE_STATE_CATEGORY enumeración windows Media Format
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b8724526142236b70faade68bf7d3ca358eb3f3810cae73f58adde17f25a0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591575"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a>DRM_LICENSE_STATE_CATEGORY enumeración (Wmdrmsdk.h)

El **tipo \_ de enumeración DRM LICENSE STATE \_ \_ CATEGORY** especifica el tipo de restricción de licencia descrito por una [**estructura DRM LICENSE STATE \_ \_ \_ DATA.**](drmdrm-license-state-data.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum DRM_LICENSE_STATE_CATEGORY { 
  WM_DRM_LICENSE_STATE_NORIGHT                    = 0,
  WM_DRM_LICENSE_STATE_UNLIM,
  WM_DRM_LICENSE_STATE_COUNT,
  WM_DRM_LICENSE_STATE_FROM,
  WM_DRM_LICENSE_STATE_UNTIL,
  WM_DRM_LICENSE_STATE_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM,
  WM_DRM_LICENSE_STATE_COUNT_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE
} DRM_LICENSE_STATE_CATEGORY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ NORIGHT**
</dt> <dd>

Especifica que no se permite la acción para la que se **recibió DRM LICENSE STATE \_ \_ \_ DATA.**

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**ESTADO DE LICENCIA DRM DE WM \_ \_ \_ \_ UNLIM**
</dt> <dd>

Especifica que la acción para la que se recibió **\_ DRM LICENSE STATE \_ \_ DATA** se permite sin restricciones.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**RECUENTO DE \_ ESTADO DE LICENCIA DE DRM \_ \_ \_ DE WM**
</dt> <dd>

Especifica que se permite la acción para la que se recibieron los DATOS DE ESTADO DE LICENCIA DE DRM, pero solo un número establecido de veces. **\_ \_ \_**

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**ESTADO DE LICENCIA DRM DE WM \_ \_ \_ \_ DESDE**
</dt> <dd>

Especifica que la acción para la que se recibió **\_ DRM LICENSE STATE \_ \_ DATA** se permite después de una fecha establecida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**ESTADO DE \_ LICENCIA DRM DE WM \_ \_ \_ HASTA**
</dt> <dd>

Especifica que la acción para la que se recibió **\_ DRM LICENSE STATE \_ \_ DATA** se permite hasta una fecha establecida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**ESTADO DE LICENCIA DRM DE WM \_ \_ DESDE \_ \_ \_ HASTA**
</dt> <dd>

Especifica que la acción para la que se recibió **\_ DRM LICENSE STATE \_ \_ DATA** se permite entre dos fechas establecidas.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**RECUENTO DE ESTADO DE LICENCIA DRM DE WM \_ \_ \_ \_ \_ DESDE**
</dt> <dd>

Especifica que se permite la acción para la que se recibió **DRM \_ LICENSE STATE \_ \_ DATA,** pero solo un número establecido de veces después de una fecha establecida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**RECUENTO DE ESTADO DE LICENCIA DE DRM DE WM \_ \_ \_ \_ \_ HASTA**
</dt> <dd>

Especifica que se permite la acción para la que se recibió **DRM \_ LICENSE STATE \_ \_ DATA,** pero solo un número establecido de veces hasta una fecha establecida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**NÚMERO DE ESTADOS DE LICENCIA DE DRM DE WM \_ \_ DESDE \_ \_ \_ \_ HASTA**
</dt> <dd>

Especifica que se permite la acción para la que se recibió **DRM \_ LICENSE STATE \_ \_ DATA,** pero solo un número establecido de veces entre dos fechas establecidas.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**EXPIRACIÓN DEL ESTADO DE LA LICENCIA DRM DE WM \_ DESPUÉS DE LA PRIMERA \_ \_ \_ \_ \_ USO**
</dt> <dd>

Especifica que la acción para la que se recibió **DRM \_ LICENSE STATE \_ \_ DATA** se permite durante un período de tiempo establecido a partir del primer uso de la acción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





