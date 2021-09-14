---
title: DRM_ACTION_ALLOWED_QUERY_RESULTS enumeración (Wmdrmsdk.h)
description: La interfaz \_ \_ \_ \_ IWMDRMLicenseQuery QueryActionAllowed usa el tipo de enumeración DRM ACTION ALLOWED QUERY RESULTS para especificar el motivo por el que no se permite una acción.
ms.assetid: dc784cdf-6efe-415b-ba72-eb8fc50bef10
keywords:
- DRM_ACTION_ALLOWED_QUERY_RESULTS de enumeración windows Media Format
- enumeración windows Media Format
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267164"
---
# <a name="drm_action_allowed_query_results-enumeration"></a>ENUMERACIÓN DE \_ \_ RESULTADOS \_ DE CONSULTA PERMITIDOS \_ DE ACCIÓN DRM

La interfaz [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) usa el tipo de enumeración **DRM ACTION ALLOWED QUERY \_ \_ \_ \_ RESULTS** para especificar el motivo por el que no se permite una acción.

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

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**CONSULTA \_ PERMITIDA DE ACCIÓN DRM NO \_ \_ \_ \_ HABILITADA**
</dt> <dd>

Especifica que no se permite la acción de consultas. Para las acciones que no se permiten, el valor devuelto es este valor combinado mediante un OR bit a bit con uno o varios de los otros valores de esta enumeración.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**CONSULTA \_ PERMITIDA DE ACCIÓN DRM NO HABILITADA SIN \_ \_ \_ \_ \_ \_ LICENCIA**
</dt> <dd>

Especifica que no existe una licencia para el contenido solicitado.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**CONSULTA \_ PERMITIDA DE ACCIÓN DRM NO HABILITADA SIN \_ \_ \_ \_ \_ \_ DERECHO**
</dt> <dd>

Especifica que existe una licencia para el contenido, pero que no se permite el derecho de consulta.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**CONSULTA \_ PERMITIDA DE ACCIÓN DRM NO HABILITADA \_ \_ \_ \_ \_ AGOTADA**
</dt> <dd>

Especifica que el derecho de consulta está restringido por un recuento y que no quedan más usos.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**LA CONSULTA \_ PERMITIDA DE ACCIÓN DRM NO HABILITADA \_ \_ \_ \_ \_ EXPIRÓ**
</dt> <dd>

Especifica que el derecho de consulta está restringido con una fecha de expiración anterior a la fecha actual.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**CONSULTA \_ PERMITIDA DE ACCIÓN DRM NO HABILITADA NO \_ \_ \_ \_ \_ \_ INICIADA**
</dt> <dd>

Especifica que la derecha consultada está restringida con una fecha de inicio posterior a la fecha actual.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**CONSULTA \_ PERMITIDA DE LA ACCIÓN DRM \_ \_ \_ \_ APPSEC NO HABILITADA \_ DEMASIADO \_ \_ BAJA**
</dt> <dd>

Especifica que existe una licencia para el contenido y que la licencia permite el derecho de consulta, pero que el nivel de seguridad de la aplicación que realiza la llamada no es lo suficientemente alto.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**CONSULTA \_ PERMITIDA DE LA ACCIÓN DRM NO HABILITADA PARA LA CONSULTA \_ \_ \_ \_ \_ \_ REQ INDIV**
</dt> <dd>

Especifica que existe una licencia para el contenido y que la licencia permite el derecho de consulta, pero que el subsistema DRM debe ser individualizado.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**CONSULTA \_ PERMITIDA DE ACCIÓN DRM NO HABILITADA PARA COPIAR \_ \_ \_ \_ \_ \_ OPL DEMASIADO \_ \_ BAJA**
</dt> <dd>

Especifica que el nivel de protección de salida del cliente es demasiado bajo.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**CONSULTA \_ PERMITIDA DE ACCIÓN DRM NO HABILITADA PARA COPIAR \_ \_ \_ \_ \_ \_ OPL \_ EXCLUIDA**
</dt> <dd>

Especifica que el nivel de protección de salida del cliente está en la lista de exclusión.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**CONSULTA \_ PERMITIDA DE ACCIÓN DRM NO HABILITADA SIN COMPATIBILIDAD CON \_ \_ \_ \_ \_ \_ \_ RELOJ**
</dt> <dd>

Especifica que la licencia requiere compatibilidad con el reloj seguro y que el cliente no la proporciona.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**CONSULTA \_ PERMITIDA DE ACCIÓN DRM NO HABILITADA SIN COMPATIBILIDAD CON LA \_ \_ \_ \_ \_ \_ \_ MEDICIÓN**
</dt> <dd>

Especifica que una licencia permite la acción consultada, pero esa medición es necesaria y el cliente no admite la medición.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**CONSULTA PERMITIDA \_ DE LA ACCIÓN DRM NO HABILITADA PROFUNDIDAD DE CADENA \_ DEMASIADO \_ \_ \_ \_ \_ \_ \_ ALTA**
</dt> <dd>

Especifica que no se pueden determinar los derechos de la acción consultada porque el contenido está cubierto por una licencia encadenada y falta la licencia hoja.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores de este tipo de enumeración indican que no se permite una acción. Un valor de cero indica que se permite la acción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





