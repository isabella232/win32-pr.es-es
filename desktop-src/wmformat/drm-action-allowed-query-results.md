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
# <a name="drm_action_allowed_query_results-enumeration"></a><span data-ttu-id="0e79e-105">\_Acción DRM \_ permitida \_ \_ enumeración de resultados de consulta</span><span class="sxs-lookup"><span data-stu-id="0e79e-105">DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS enumeration</span></span>

<span data-ttu-id="0e79e-106">La interfaz [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) usa el tipo de enumeración de **\_ \_ \_ \_ resultados de consulta permitidos de la acción DRM** para especificar la razón por la que no se permite una acción.</span><span class="sxs-lookup"><span data-stu-id="0e79e-106">The **DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS** enumeration type is used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e79e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e79e-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="0e79e-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="0e79e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0e79e-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**no se habilitó la \_ consulta de acción DRM \_ permitida \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0e79e-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-110">Especifica que no se permite la acción de consultas.</span><span class="sxs-lookup"><span data-stu-id="0e79e-110">Specifies that the queries action is not allowed.</span></span> <span data-ttu-id="0e79e-111">En el caso de las acciones no permitidas, el valor devuelto es este valor combinado mediante una operación OR bit a bit con uno o varios de los valores de esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="0e79e-111">For actions that are not allowed, the returned value is this value combined by using a bitwise OR with one or more of the other values in this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="0e79e-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**la \_ consulta de acción DRM \_ \_ \_ no \_ está habilitada \_ sin \_ licencia**</span><span class="sxs-lookup"><span data-stu-id="0e79e-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-113">Especifica que no existe una licencia para el contenido solicitado.</span><span class="sxs-lookup"><span data-stu-id="0e79e-113">Specifies that a license does not exist for the requested content.</span></span>

</dd> <dt>

<span data-ttu-id="0e79e-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**no \_ se \_ \_ \_ ha \_ habilitado la \_ consulta de acción DRM \_**</span><span class="sxs-lookup"><span data-stu-id="0e79e-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-115">Especifica que existe una licencia para el contenido, pero que no se permite el derecho consultado.</span><span class="sxs-lookup"><span data-stu-id="0e79e-115">Specifies that a license exists for the content, but that the queried right is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="0e79e-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_no se \_ \_ \_ ha \_ habilitado la \_ consulta de acción DRM permitida**</span><span class="sxs-lookup"><span data-stu-id="0e79e-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXHAUSTED**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-117">Especifica que el derecho consultado está restringido por un recuento y que no quedan más usos.</span><span class="sxs-lookup"><span data-stu-id="0e79e-117">Specifies that the queried right is restricted by a count, and that no more uses remain.</span></span>

</dd> <dt>

<span data-ttu-id="0e79e-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**la \_ consulta de la acción DRM \_ permitida \_ \_ no \_ está habilitada \_**</span><span class="sxs-lookup"><span data-stu-id="0e79e-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-119">Especifica que el derecho consultado está restringido con una fecha de expiración anterior a la fecha actual.</span><span class="sxs-lookup"><span data-stu-id="0e79e-119">Specifies that the queried right is restricted with an expiration date that is earlier than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="0e79e-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**\_no se \_ \_ \_ \_ \_ \_ ha iniciado la consulta de acción DRM habilitada**</span><span class="sxs-lookup"><span data-stu-id="0e79e-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NOT\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-121">Especifica que el derecho consultado está restringido con una fecha de inicio posterior a la fecha actual.</span><span class="sxs-lookup"><span data-stu-id="0e79e-121">Specifies that the queried right is restricted with a start date that is later than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="0e79e-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**la \_ consulta de DRM \_ permitida \_ \_ no \_ está habilitada \_ APPSEC \_ demasiado \_ baja**</span><span class="sxs-lookup"><span data-stu-id="0e79e-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_APPSEC\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-123">Especifica que existe una licencia para el contenido y que la licencia permite el derecho consultado, pero que el nivel de seguridad de la aplicación que realiza la llamada no es suficientemente alto.</span><span class="sxs-lookup"><span data-stu-id="0e79e-123">Specifies that a license exists for the content and that the license allows the queried right, but that the security level of the calling application is not high enough.</span></span>

</dd> <dt>

<span data-ttu-id="0e79e-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**acción de DRM \_ \_ permitida de \_ solicitud \_ no \_ habilitada \_ \_ indiv**</span><span class="sxs-lookup"><span data-stu-id="0e79e-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_REQ\_INDIV**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-125">Especifica que existe una licencia para el contenido y que la licencia permite el derecho consultado, pero que se debe individualizar el subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="0e79e-125">Specifies that a license exists for the content and that the license allows the queried right, but that the DRM subsystem must be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="0e79e-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**la \_ acción de DRM \_ permitió \_ consulta \_ no \_ habilitada de \_ copia de \_ OPL \_ demasiado \_ baja**</span><span class="sxs-lookup"><span data-stu-id="0e79e-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-127">Especifica que el nivel de protección de salida del cliente es demasiado bajo.</span><span class="sxs-lookup"><span data-stu-id="0e79e-127">Specifies that the output protection level of the client is too low.</span></span>

</dd> <dt>

<span data-ttu-id="0e79e-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**la \_ acción DRM \_ permitió la \_ consulta \_ no \_ habilitada de copia de \_ \_ OPL \_ excluida**</span><span class="sxs-lookup"><span data-stu-id="0e79e-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_EXCLUDED**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-129">Especifica que el nivel de protección de salida del cliente se encuentra en la lista de exclusión.</span><span class="sxs-lookup"><span data-stu-id="0e79e-129">Specifies that the output protection level of the client is on the exclusion list.</span></span>

</dd> <dt>

<span data-ttu-id="0e79e-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**la \_ consulta de acción DRM \_ permitía \_ \_ no \_ habilitada, \_ \_ no se admite el reloj \_**</span><span class="sxs-lookup"><span data-stu-id="0e79e-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_CLOCK\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-131">Especifica que la licencia requiere compatibilidad con el reloj seguro y que el cliente no la proporciona.</span><span class="sxs-lookup"><span data-stu-id="0e79e-131">Specifies that the license requires secure clock support and that the client does not provide it.</span></span>

</dd> <dt>

<span data-ttu-id="0e79e-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**no \_ se \_ \_ \_ ha \_ habilitado la \_ \_ consulta de acción \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="0e79e-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_METERING\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-133">Especifica que la acción consultada está permitida por una licencia, pero que es necesaria y que el cliente no admite la medición.</span><span class="sxs-lookup"><span data-stu-id="0e79e-133">Specifies that the queried action is allowed by a license, but that metering is required and the client does not support metering.</span></span>

</dd> <dt>

<span data-ttu-id="0e79e-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**la \_ acción de DRM \_ permitió \_ consulta \_ no \_ habilitada \_ profundidad de cadena \_ \_ demasiado \_ alta**</span><span class="sxs-lookup"><span data-stu-id="0e79e-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_CHAIN\_DEPTH\_TOO\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="0e79e-135">Especifica que no se pueden determinar los derechos para la acción consultada porque el contenido está incluido en una licencia encadenada y falta la licencia de hoja.</span><span class="sxs-lookup"><span data-stu-id="0e79e-135">Specifies that the rights for the queried action cannot be determined because the content is covered by a chained license and the leaf license is missing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e79e-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e79e-136">Remarks</span></span>

<span data-ttu-id="0e79e-137">Los valores de este tipo de enumeración indican que no se permite una acción.</span><span class="sxs-lookup"><span data-stu-id="0e79e-137">The values of this enumeration type indicate that an action is not allowed.</span></span> <span data-ttu-id="0e79e-138">Un valor de cero indica que se permite la acción.</span><span class="sxs-lookup"><span data-stu-id="0e79e-138">A value of zero indicates that the action is allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e79e-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e79e-139">Requirements</span></span>



| <span data-ttu-id="0e79e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e79e-140">Requirement</span></span> | <span data-ttu-id="0e79e-141">Value</span><span class="sxs-lookup"><span data-stu-id="0e79e-141">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e79e-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e79e-142">Header</span></span><br/> | <dl> <span data-ttu-id="0e79e-143"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e79e-143"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e79e-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e79e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e79e-145">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="0e79e-145">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





