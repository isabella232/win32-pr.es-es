---
title: Enumeración DRM_LICENSE_STATE_CATEGORY (Drmexternals. h)
description: El \_ tipo de \_ \_ enumeración categoría de estado de licencia DRM define las categorías de las cadenas de licencia DRM que se muestran al usuario.
ms.assetid: f5c5aa78-84f9-4ee4-b551-05bf864243ab
keywords:
- DRM_LICENSE_STATE_CATEGORY enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40763ec7f610073784e3bd1516d4c955abcd65b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491836"
---
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a>Enumeración DRM_LICENSE_STATE_CATEGORY (Drmexternals. h)

El tipo de enumeración **\_ \_ \_ categoría de estado de licencia DRM** define las categorías de las cadenas de [*licencia*](wmformat-glossary.md) DRM que se muestran al usuario.

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
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**Estado de la licencia de DRM de WM \_ \_ \_ \_ noright**
</dt> <dd>

Indica que la cadena tendrá el formato "reproducción no permitida".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**Estado de licencia de DRM de WM \_ \_ \_ \_ UNLIM**
</dt> <dd>

Indica que la cadena tendrá el formato "reproducción ilimitada".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**recuento de Estados de licencias de \_ DRM de WM \_ \_ \_**
</dt> <dd>

Indica que la cadena tendrá el formato "reproducción válida 5 veces".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ \_ estado \_ de licencia de DRM de WM desde**
</dt> <dd>

Indica que la cadena tendrá el formato "reproducción válida desde 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**Estado de la licencia de DRM de WM \_ \_ \_ \_ hasta**
</dt> <dd>

Indica que la cadena tendrá el formato "reproducción válida hasta 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ \_ Estado de la licencia \_ de DRM de WM desde \_ hasta**
</dt> <dd>

Indica que la cadena tendrá el formato "reproducción válida de 5/12 a 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_recuento \_ \_ de Estados \_ de licencias de DRM de WM \_ desde**
</dt> <dd>

Indica que la cadena tendrá el formato "reproducción válida 5 veces de 5/12 a 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**recuento de Estados de licencias de DRM de WM \_ \_ \_ \_ \_ hasta**
</dt> <dd>

Indica que la cadena tendrá el formato "reproducción válida 5 veces hasta 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_recuento \_ \_ de Estados \_ de licencias de DRM de WM \_ desde \_ hasta**
</dt> <dd>

Indica que la cadena tendrá el formato "reproducción válida 5 veces de 5/12 a 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_expiración del estado de licencia de DRM de WM \_ \_ después de \_ \_ \_ FIRSTUSE**
</dt> <dd>

Indica que la cadena tendrá el formato "reproducción válida durante 24 horas del primer uso".

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración indica la categoría de cada cadena de salida posible que se va a mostrar. Es miembro de la estructura de [**\_ datos de \_ estado \_**](drm-license-state-data.md) de la licencia de DRM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Versión<br/>                  | SDK de Windows Media Format 7 o versiones posteriores del SDK<br/>                       |
| Encabezado<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





