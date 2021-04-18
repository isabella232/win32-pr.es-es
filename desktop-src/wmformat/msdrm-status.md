---
title: Enumeración MSDRM_STATUS (wmdrmsdk. h)
description: El \_ tipo de enumeración de estado MSDRM define las condiciones de estado para el subsistema DRM.
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- MSDRM_STATUS enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- MSDRM_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2a73de9e33216e22a01966be8f2ed6a3185fdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721589"
---
# <a name="msdrm_status-enumeration"></a><span data-ttu-id="12386-105">\_Enumeración de estado de MSDRM</span><span class="sxs-lookup"><span data-stu-id="12386-105">MSDRM\_STATUS enumeration</span></span>

<span data-ttu-id="12386-106">El tipo de enumeración de **\_ Estado MSDRM** define las condiciones de estado para el subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="12386-106">The **MSDRM\_STATUS** enumeration type defines status conditions for the DRM subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="12386-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12386-107">Syntax</span></span>


```C++
typedef enum MSDRM_STATUS { 
  DRM_ERROR                        = 0,
  DRM_INFORMATION                  = 1,
  DRM_BACKUPRESTORE_BEGIN          = 2,
  DRM_BACKUPRESTORE_END            = 3,
  DRM_BACKUPRESTORE_CONNECTING     = 4,
  DRM_BACKUPRESTORE_DISCONNECTING  = 5,
  DRM_ERROR_WITHURL                = 6,
  DRM_RESTRICTED_LICENSE           = 7,
  DRM_NEEDS_INDIVIDUALIZATION      = 8,
  DRM_PLAY_OPL_NOTIFICATION        = 9,
  DRM_COPY_OPL_NOTIFICATION        = 10,
  DRM_REFRESHCRL_COMPLETE          = 11
} ;
```



## <a name="constants"></a><span data-ttu-id="12386-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="12386-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="12386-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**ERROR de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="12386-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**DRM\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="12386-110">Especifica que se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="12386-110">Specifies that an error has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="12386-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**información de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="12386-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**DRM\_INFORMATION**</span></span>
</dt> <dd>

<span data-ttu-id="12386-112">Especifica que hay información de estado adicional.</span><span class="sxs-lookup"><span data-stu-id="12386-112">Specifies that there is additional status information.</span></span>

</dd> <dt>

<span data-ttu-id="12386-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**\_Inicio de BACKUPRESTORE de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="12386-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM\_BACKUPRESTORE\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="12386-114">Especifica que se ha iniciado una operación de restauración o copia de seguridad de licencias.</span><span class="sxs-lookup"><span data-stu-id="12386-114">Specifies that a license backup or restore operation has begun.</span></span>

</dd> <dt>

<span data-ttu-id="12386-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**\_final de BACKUPRESTORE DRM \_**</span><span class="sxs-lookup"><span data-stu-id="12386-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM\_BACKUPRESTORE\_END**</span></span>
</dt> <dd>

<span data-ttu-id="12386-116">Especifica que ha finalizado una operación de copia de seguridad o restauración de una licencia.</span><span class="sxs-lookup"><span data-stu-id="12386-116">Specifies that a license backup or restore operation has ended.</span></span>

</dd> <dt>

<span data-ttu-id="12386-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**\_conexión de BACKUPRESTORE DRM \_**</span><span class="sxs-lookup"><span data-stu-id="12386-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM\_BACKUPRESTORE\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="12386-118">Especifica que una operación de copia de seguridad o restauración de licencias está en curso y que el equipo cliente se está conectando con el servidor de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="12386-118">Specifies that a license backup or restore operation is in progress and that the client computer is connecting with the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="12386-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**desconexión de BACKUPRESTORE de DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12386-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM\_BACKUPRESTORE\_DISCONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="12386-120">Especifica que una operación de copia de seguridad o restauración de licencias está en curso y que el equipo cliente se está desconectando del servidor de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="12386-120">Specifies that a license backup or restore operation is in progress and that the client computer is disconnecting from the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="12386-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**\_error \_ WITHURL de DRM**</span><span class="sxs-lookup"><span data-stu-id="12386-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**DRM\_ERROR\_WITHURL**</span></span>
</dt> <dd>

<span data-ttu-id="12386-122">Especifica que la operación DRM ha encontrado una dirección URL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="12386-122">Specifies that the DRM operation has encountered a bad URL.</span></span>

</dd> <dt>

<span data-ttu-id="12386-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**licencia de DRM \_ restringida \_**</span><span class="sxs-lookup"><span data-stu-id="12386-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**DRM\_RESTRICTED\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="12386-124">Especifica que la operación DRM no puede continuar porque no existe ninguna licencia que conceda el derecho necesario en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="12386-124">Specifies that the DRM operation cannot continue because no license granting the required right exists on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="12386-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ necesita la \_ individualización**</span><span class="sxs-lookup"><span data-stu-id="12386-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM\_NEEDS\_INDIVIDUALIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="12386-126">Especifica que la operación DRM no puede continuar porque el subsistema DRM debe ser individualizado.</span><span class="sxs-lookup"><span data-stu-id="12386-126">Specifies that the DRM operation cannot continue because the DRM subsystem needs to be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="12386-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**\_notificación del \_ OPL de reproducción de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="12386-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**DRM\_PLAY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="12386-128">Especifica que no se puede completar una operación de reproducción porque no se ha cumplido un requisito de nivel de protección de salida.</span><span class="sxs-lookup"><span data-stu-id="12386-128">Specifies that a playback operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="12386-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**\_notificación del \_ OPL de copia de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="12386-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**DRM\_COPY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="12386-130">Especifica que no se puede completar una operación de copia porque no se ha cumplido un requisito de nivel de protección de salida.</span><span class="sxs-lookup"><span data-stu-id="12386-130">Specifies that a copy operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="12386-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**REFRESHCRL de DRM \_ \_ completado**</span><span class="sxs-lookup"><span data-stu-id="12386-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**DRM\_REFRESHCRL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="12386-132">Especifica que una llamada a [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) ha completado la actualización de una lista de revocación.</span><span class="sxs-lookup"><span data-stu-id="12386-132">Specifies that a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) has completed refreshing a revocation list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12386-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12386-133">Remarks</span></span>

<span data-ttu-id="12386-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="12386-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="12386-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12386-135">Requirements</span></span>



| <span data-ttu-id="12386-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="12386-136">Requirement</span></span> | <span data-ttu-id="12386-137">Value</span><span class="sxs-lookup"><span data-stu-id="12386-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12386-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12386-138">Header</span></span><br/> | <dl> <span data-ttu-id="12386-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="12386-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12386-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="12386-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12386-141">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="12386-141">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





