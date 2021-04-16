---
title: Enumeración DRM_ACTION_ALLOWED_QUERY_RESULTS (wmdrmsdk. h)
description: La \_ \_ interfaz IWMDRMLicenseQuery QueryActionAllowed usa el tipo de enumeración de resultados de consulta permitidos de la acción DRM \_ \_ para especificar la razón por la que no se permite una acción.
ms.assetid: dc784cdf-6efe-415b-ba72-eb8fc50bef10
keywords:
- DRM_ACTION_ALLOWED_QUERY_RESULTS enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- DRM_ACTION_ALLOWED_QUERY_RESULTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e328acb915bd32547f3455e8556e4caba2360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671549"
---
# <a name="drm_action_allowed_query_results-enumeration"></a>\_Acción DRM \_ permitida \_ \_ enumeración de resultados de consulta

La interfaz [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) usa el tipo de enumeración de **\_ \_ \_ \_ resultados de consulta permitidos de la acción DRM** para especificar la razón por la que no se permite una acción.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum DRM_ACTION_ALLOWED_QUERY_RESULTS { 
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED                       = 0x00000001,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE            = 0x00000002,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT              = 0x00000004,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED             = 0x00000008,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED               = 0x00000010,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED           = 0x00000020,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW        = 0x00000040,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV             = 0x00000080,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW      = 0x00000100,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED     = 0x00000200,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT      = 0x00000400,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT   = 0x00000800,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH  = 0x00001000
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**no se habilitó la \_ consulta de acción DRM \_ permitida \_ \_ \_**
</dt> <dd>

Especifica que no se permite la acción de consultas. En el caso de las acciones no permitidas, el valor devuelto es este valor combinado mediante una operación OR bit a bit con uno o varios de los valores de esta enumeración.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**la \_ consulta de acción DRM \_ \_ \_ no \_ está habilitada \_ sin \_ licencia**
</dt> <dd>

Especifica que no existe una licencia para el contenido solicitado.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**no \_ se \_ \_ \_ ha \_ habilitado la \_ consulta de acción DRM \_**
</dt> <dd>

Especifica que existe una licencia para el contenido, pero que no se permite el derecho consultado.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_no se \_ \_ \_ ha \_ habilitado la \_ consulta de acción DRM permitida**
</dt> <dd>

Especifica que el derecho consultado está restringido por un recuento y que no quedan más usos.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**la \_ consulta de la acción DRM \_ permitida \_ \_ no \_ está habilitada \_**
</dt> <dd>

Especifica que el derecho consultado está restringido con una fecha de expiración anterior a la fecha actual.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**\_no se \_ \_ \_ \_ \_ \_ ha iniciado la consulta de acción DRM habilitada**
</dt> <dd>

Especifica que el derecho consultado está restringido con una fecha de inicio posterior a la fecha actual.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**la \_ consulta de DRM \_ permitida \_ \_ no \_ está habilitada \_ APPSEC \_ demasiado \_ baja**
</dt> <dd>

Especifica que existe una licencia para el contenido y que la licencia permite el derecho consultado, pero que el nivel de seguridad de la aplicación que realiza la llamada no es suficientemente alto.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**acción de DRM \_ \_ permitida de \_ solicitud \_ no \_ habilitada \_ \_ indiv**
</dt> <dd>

Especifica que existe una licencia para el contenido y que la licencia permite el derecho consultado, pero que se debe individualizar el subsistema DRM.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**la \_ acción de DRM \_ permitió \_ consulta \_ no \_ habilitada de \_ copia de \_ OPL \_ demasiado \_ baja**
</dt> <dd>

Especifica que el nivel de protección de salida del cliente es demasiado bajo.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**la \_ acción DRM \_ permitió la \_ consulta \_ no \_ habilitada de copia de \_ \_ OPL \_ excluida**
</dt> <dd>

Especifica que el nivel de protección de salida del cliente se encuentra en la lista de exclusión.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**la \_ consulta de acción DRM \_ permitía \_ \_ no \_ habilitada, \_ \_ no se admite el reloj \_**
</dt> <dd>

Especifica que la licencia requiere compatibilidad con el reloj seguro y que el cliente no la proporciona.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**no \_ se \_ \_ \_ ha \_ habilitado la \_ \_ consulta de acción \_ DRM**
</dt> <dd>

Especifica que la acción consultada está permitida por una licencia, pero que es necesaria y que el cliente no admite la medición.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**la \_ acción de DRM \_ permitió \_ consulta \_ no \_ habilitada \_ profundidad de cadena \_ \_ demasiado \_ alta**
</dt> <dd>

Especifica que no se pueden determinar los derechos para la acción consultada porque el contenido está incluido en una licencia encadenada y falta la licencia de hoja.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores de este tipo de enumeración indican que no se permite una acción. Un valor de cero indica que se permite la acción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





