---
title: DRM_LICENSE_STATE_CATEGORY enumeración (Drmexternals.h)
description: El tipo de enumeración DRM LICENSE STATE CATEGORY define las categorías de las cadenas de licencia drm que \_ \_ se muestran al \_ usuario.
ms.assetid: f5c5aa78-84f9-4ee4-b551-05bf864243ab
keywords:
- DRM_LICENSE_STATE_CATEGORY enumeración windows Media Format
- enumeración windows Media Format
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
ms.openlocfilehash: 2bbfd6c566d6c58314416c787110ea77da25416ed73d80ec87fd2d66602d820b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931005"
---
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a>DRM_LICENSE_STATE_CATEGORY enumeración (Drmexternals.h)

El **tipo \_ de enumeración DRM LICENSE STATE \_ \_ CATEGORY** define las categorías de las cadenas de licencia [*drm*](wmformat-glossary.md) que se muestran al usuario.

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
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ NORIGHT**
</dt> <dd>

Indica que la cadena tendrá el formato "No se permite la reproducción".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**ESTADO DE LICENCIA DRM DE WM \_ \_ \_ \_ UNLIM**
</dt> <dd>

Indica que la cadena tendrá el formato "Reproducción ilimitada".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**RECUENTO DE \_ ESTADO DE LICENCIA DE DRM \_ \_ \_ DE WM**
</dt> <dd>

Indica que la cadena tendrá el formato "Reproducción válida 5 veces".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**ESTADO DE LICENCIA DRM DE WM \_ \_ \_ \_ DESDE**
</dt> <dd>

Indica que la cadena tendrá el formato "Playback valid from 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**ESTADO DE \_ LICENCIA DRM DE WM \_ \_ \_ HASTA**
</dt> <dd>

Indica que la cadena tendrá el formato "Playback valid until 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**ESTADO DE LICENCIA DRM DE WM \_ \_ DESDE \_ \_ \_ HASTA**
</dt> <dd>

Indica que la cadena tendrá el formato "Playback valid from 5/12 to 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**RECUENTO DE ESTADO DE LICENCIA DRM DE WM \_ \_ \_ \_ \_ DESDE**
</dt> <dd>

Indica que la cadena tendrá el formato "Playback valid 5 times from 5/12 to 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**RECUENTO DE ESTADO DE LICENCIA DE DRM DE WM \_ \_ \_ \_ \_ HASTA**
</dt> <dd>

Indica que la cadena tendrá el formato "Playback valid 5 times until 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**NÚMERO DE ESTADOS DE LICENCIA DE DRM DE WM \_ \_ DESDE \_ \_ \_ \_ HASTA**
</dt> <dd>

Indica que la cadena tendrá el formato "Playback valid 5 times from 5/12 to 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**EXPIRACIÓN DEL ESTADO DE LA LICENCIA DRM DE WM \_ DESPUÉS DE LA PRIMERA \_ \_ \_ \_ \_ USO**
</dt> <dd>

Indica que la cadena tendrá el formato "Reproducción válida durante 24 horas desde el primer uso".

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta enumeración indica la categoría de cada cadena de salida posible que se va a mostrar. Es miembro de la estructura [**\_ DRM LICENSE STATE \_ \_ DATA.**](drm-license-state-data.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Versión<br/>                  | Windows SDK de formato multimedia 7 o versiones posteriores del SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





