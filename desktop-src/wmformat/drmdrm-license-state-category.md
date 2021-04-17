---
title: Enumeración DRM_LICENSE_STATE_CATEGORY (wmdrmsdk. h)
description: El \_ \_ \_ tipo de enumeración categoría de estado de licencia DRM especifica el tipo de restricción de licencia que se describe mediante una \_ estructura de datos de estado de licencia DRM \_ \_ .
ms.assetid: 51258be9-2f4d-4f25-97f7-2cac6c155ade
keywords:
- DRM_LICENSE_STATE_CATEGORY enumeración formato de Windows Media
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
ms.openlocfilehash: e928a95a71d9636f88bc3c79ac36168072527040
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690734"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a>Enumeración DRM_LICENSE_STATE_CATEGORY (wmdrmsdk. h)

El tipo de enumeración **\_ categoría de \_ estado \_ de licencia DRM** especifica el tipo de restricción de licencia que se describe mediante una estructura de [**datos de \_ Estado de licencia \_ \_ DRM**](drmdrm-license-state-data.md) .

## <a name="syntax"></a>Sintaxis


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

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**Estado de la licencia de DRM de WM \_ \_ \_ \_ noright**
</dt> <dd>

Especifica que no se permite la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**Estado de licencia de DRM de WM \_ \_ \_ \_ UNLIM**
</dt> <dd>

Especifica que la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM se permite sin restricciones.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**recuento de Estados de licencias de \_ DRM de WM \_ \_ \_**
</dt> <dd>

Especifica que se permite la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM, pero solo un número de veces establecido.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ \_ estado \_ de licencia de DRM de WM desde**
</dt> <dd>

Especifica que la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM se permite después de una fecha establecida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**Estado de la licencia de DRM de WM \_ \_ \_ \_ hasta**
</dt> <dd>

Especifica que la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM se permite hasta una fecha establecida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ \_ Estado de la licencia \_ de DRM de WM desde \_ hasta**
</dt> <dd>

Especifica que la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM se permite entre dos fechas establecidas.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_recuento \_ \_ de Estados \_ de licencias de DRM de WM \_ desde**
</dt> <dd>

Especifica que se permite la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM, pero solo un número establecido de veces después de una fecha establecida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**recuento de Estados de licencias de DRM de WM \_ \_ \_ \_ \_ hasta**
</dt> <dd>

Especifica que se permite la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM, pero solo un número de veces establecido hasta una fecha establecida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_recuento \_ \_ de Estados \_ de licencias de DRM de WM \_ desde \_ hasta**
</dt> <dd>

Especifica que se permite la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM, pero solo un número establecido de veces entre dos fechas establecidas.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_expiración del estado de licencia de DRM de WM \_ \_ después de \_ \_ \_ FIRSTUSE**
</dt> <dd>

Especifica que la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM se permite durante un período de tiempo determinado, empezando por el primer uso de la acción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





