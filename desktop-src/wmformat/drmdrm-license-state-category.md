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
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a><span data-ttu-id="1fcfc-104">Enumeración DRM_LICENSE_STATE_CATEGORY (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="1fcfc-104">DRM_LICENSE_STATE_CATEGORY enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="1fcfc-105">El tipo de enumeración **\_ categoría de \_ estado \_ de licencia DRM** especifica el tipo de restricción de licencia que se describe mediante una estructura de [**datos de \_ Estado de licencia \_ \_ DRM**](drmdrm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcfc-105">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fcfc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fcfc-106">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="1fcfc-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="1fcfc-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1fcfc-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**Estado de la licencia de DRM de WM \_ \_ \_ \_ noright**</span><span class="sxs-lookup"><span data-stu-id="1fcfc-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="1fcfc-109">Especifica que no se permite la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-109">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="1fcfc-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**Estado de licencia de DRM de WM \_ \_ \_ \_ UNLIM**</span><span class="sxs-lookup"><span data-stu-id="1fcfc-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="1fcfc-111">Especifica que la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM se permite sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-111">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="1fcfc-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**recuento de Estados de licencias de \_ DRM de WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1fcfc-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="1fcfc-113">Especifica que se permite la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM, pero solo un número de veces establecido.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-113">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times.</span></span>

</dd> <dt>

<span data-ttu-id="1fcfc-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ \_ estado \_ de licencia de DRM de WM desde**</span><span class="sxs-lookup"><span data-stu-id="1fcfc-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="1fcfc-115">Especifica que la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM se permite después de una fecha establecida.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-115">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="1fcfc-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**Estado de la licencia de DRM de WM \_ \_ \_ \_ hasta**</span><span class="sxs-lookup"><span data-stu-id="1fcfc-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="1fcfc-117">Especifica que la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM se permite hasta una fecha establecida.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-117">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="1fcfc-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ \_ Estado de la licencia \_ de DRM de WM desde \_ hasta**</span><span class="sxs-lookup"><span data-stu-id="1fcfc-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="1fcfc-119">Especifica que la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM se permite entre dos fechas establecidas.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-119">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="1fcfc-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_recuento \_ \_ de Estados \_ de licencias de DRM de WM \_ desde**</span><span class="sxs-lookup"><span data-stu-id="1fcfc-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="1fcfc-121">Especifica que se permite la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM, pero solo un número establecido de veces después de una fecha establecida.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-121">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="1fcfc-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**recuento de Estados de licencias de DRM de WM \_ \_ \_ \_ \_ hasta**</span><span class="sxs-lookup"><span data-stu-id="1fcfc-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="1fcfc-123">Especifica que se permite la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM, pero solo un número de veces establecido hasta una fecha establecida.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-123">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="1fcfc-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_recuento \_ \_ de Estados \_ de licencias de DRM de WM \_ desde \_ hasta**</span><span class="sxs-lookup"><span data-stu-id="1fcfc-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="1fcfc-125">Especifica que se permite la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM, pero solo un número establecido de veces entre dos fechas establecidas.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-125">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="1fcfc-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_expiración del estado de licencia de DRM de WM \_ \_ después de \_ \_ \_ FIRSTUSE**</span><span class="sxs-lookup"><span data-stu-id="1fcfc-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="1fcfc-127">Especifica que la acción para la que se recibieron los **\_ datos de \_ estado \_** de la licencia de DRM se permite durante un período de tiempo determinado, empezando por el primer uso de la acción.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-127">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed for a set amount of time beginning with the first use of the action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fcfc-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fcfc-128">Remarks</span></span>

<span data-ttu-id="1fcfc-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-129">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fcfc-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fcfc-130">Requirements</span></span>



| <span data-ttu-id="1fcfc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fcfc-131">Requirement</span></span> | <span data-ttu-id="1fcfc-132">Value</span><span class="sxs-lookup"><span data-stu-id="1fcfc-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcfc-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fcfc-133">Header</span></span><br/> | <dl> <span data-ttu-id="1fcfc-134"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fcfc-134"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fcfc-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fcfc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fcfc-136">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="1fcfc-136">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





