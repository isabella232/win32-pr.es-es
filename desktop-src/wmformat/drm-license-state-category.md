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
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a><span data-ttu-id="4ff59-105">Enumeración DRM_LICENSE_STATE_CATEGORY (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="4ff59-105">DRM_LICENSE_STATE_CATEGORY enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="4ff59-106">El tipo de enumeración **\_ \_ \_ categoría de estado de licencia DRM** define las categorías de las cadenas de [*licencia*](wmformat-glossary.md) DRM que se muestran al usuario.</span><span class="sxs-lookup"><span data-stu-id="4ff59-106">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type defines the categories for DRM [*license*](wmformat-glossary.md) strings that are displayed to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ff59-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ff59-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="4ff59-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="4ff59-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4ff59-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**Estado de la licencia de DRM de WM \_ \_ \_ \_ noright**</span><span class="sxs-lookup"><span data-stu-id="4ff59-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="4ff59-110">Indica que la cadena tendrá el formato "reproducción no permitida".</span><span class="sxs-lookup"><span data-stu-id="4ff59-110">Indicates the string will take the form "Playback not permitted."</span></span>

</dd> <dt>

<span data-ttu-id="4ff59-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**Estado de licencia de DRM de WM \_ \_ \_ \_ UNLIM**</span><span class="sxs-lookup"><span data-stu-id="4ff59-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="4ff59-112">Indica que la cadena tendrá el formato "reproducción ilimitada".</span><span class="sxs-lookup"><span data-stu-id="4ff59-112">Indicates the string will take the form "Playback unlimited."</span></span>

</dd> <dt>

<span data-ttu-id="4ff59-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**recuento de Estados de licencias de \_ DRM de WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4ff59-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="4ff59-114">Indica que la cadena tendrá el formato "reproducción válida 5 veces".</span><span class="sxs-lookup"><span data-stu-id="4ff59-114">Indicates the string will take the form "Playback valid 5 times."</span></span>

</dd> <dt>

<span data-ttu-id="4ff59-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ \_ estado \_ de licencia de DRM de WM desde**</span><span class="sxs-lookup"><span data-stu-id="4ff59-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="4ff59-116">Indica que la cadena tendrá el formato "reproducción válida desde 7/12/00".</span><span class="sxs-lookup"><span data-stu-id="4ff59-116">Indicates the string will take the form "Playback valid from 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="4ff59-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**Estado de la licencia de DRM de WM \_ \_ \_ \_ hasta**</span><span class="sxs-lookup"><span data-stu-id="4ff59-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="4ff59-118">Indica que la cadena tendrá el formato "reproducción válida hasta 7/12/00".</span><span class="sxs-lookup"><span data-stu-id="4ff59-118">Indicates the string will take the form "Playback valid until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="4ff59-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ \_ Estado de la licencia \_ de DRM de WM desde \_ hasta**</span><span class="sxs-lookup"><span data-stu-id="4ff59-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="4ff59-120">Indica que la cadena tendrá el formato "reproducción válida de 5/12 a 9/12".</span><span class="sxs-lookup"><span data-stu-id="4ff59-120">Indicates the string will take the form "Playback valid from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="4ff59-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_recuento \_ \_ de Estados \_ de licencias de DRM de WM \_ desde**</span><span class="sxs-lookup"><span data-stu-id="4ff59-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="4ff59-122">Indica que la cadena tendrá el formato "reproducción válida 5 veces de 5/12 a 9/12".</span><span class="sxs-lookup"><span data-stu-id="4ff59-122">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="4ff59-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**recuento de Estados de licencias de DRM de WM \_ \_ \_ \_ \_ hasta**</span><span class="sxs-lookup"><span data-stu-id="4ff59-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="4ff59-124">Indica que la cadena tendrá el formato "reproducción válida 5 veces hasta 7/12/00".</span><span class="sxs-lookup"><span data-stu-id="4ff59-124">Indicates the string will take the form "Playback valid 5 times until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="4ff59-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_recuento \_ \_ de Estados \_ de licencias de DRM de WM \_ desde \_ hasta**</span><span class="sxs-lookup"><span data-stu-id="4ff59-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="4ff59-126">Indica que la cadena tendrá el formato "reproducción válida 5 veces de 5/12 a 9/12".</span><span class="sxs-lookup"><span data-stu-id="4ff59-126">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="4ff59-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_expiración del estado de licencia de DRM de WM \_ \_ después de \_ \_ \_ FIRSTUSE**</span><span class="sxs-lookup"><span data-stu-id="4ff59-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="4ff59-128">Indica que la cadena tendrá el formato "reproducción válida durante 24 horas del primer uso".</span><span class="sxs-lookup"><span data-stu-id="4ff59-128">Indicates the string will take the form "Playback valid for 24 hours from first use."</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ff59-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ff59-129">Remarks</span></span>

<span data-ttu-id="4ff59-130">Esta enumeración indica la categoría de cada cadena de salida posible que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="4ff59-130">This enumeration indicates the category for each possible output string to be displayed.</span></span> <span data-ttu-id="4ff59-131">Es miembro de la estructura de [**\_ datos de \_ estado \_**](drm-license-state-data.md) de la licencia de DRM.</span><span class="sxs-lookup"><span data-stu-id="4ff59-131">It is a member of the [**DRM\_LICENSE\_STATE\_DATA**](drm-license-state-data.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ff59-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ff59-132">Requirements</span></span>



| <span data-ttu-id="4ff59-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ff59-133">Requirement</span></span> | <span data-ttu-id="4ff59-134">Value</span><span class="sxs-lookup"><span data-stu-id="4ff59-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ff59-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ff59-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4ff59-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4ff59-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4ff59-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ff59-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4ff59-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4ff59-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4ff59-139">Versión</span><span class="sxs-lookup"><span data-stu-id="4ff59-139">Version</span></span><br/>                  | <span data-ttu-id="4ff59-140">SDK de Windows Media Format 7 o versiones posteriores del SDK</span><span class="sxs-lookup"><span data-stu-id="4ff59-140">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="4ff59-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ff59-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ff59-142"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ff59-142"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ff59-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ff59-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ff59-144">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="4ff59-144">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





