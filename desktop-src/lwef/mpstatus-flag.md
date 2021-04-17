---
title: Enumeración MPSTATUS_FLAG (MpClient. h)
description: Posibles marcas de bits de estado de producto generales.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- MPSTATUS_FLAG enumeración características de entorno heredado de Windows
- PMPSTATUS_FLAG el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSTATUS_FLAG
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c7175980c09c63938be04626091c31b53335756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665979"
---
# <a name="mpstatus_flag-enumeration"></a><span data-ttu-id="46f72-105">\_Enumeración de marcas MPSTATUS</span><span class="sxs-lookup"><span data-stu-id="46f72-105">MPSTATUS\_FLAG enumeration</span></span>

<span data-ttu-id="46f72-106">Posibles marcas de bits de estado de producto generales.</span><span class="sxs-lookup"><span data-stu-id="46f72-106">Possible overall product status bit flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f72-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46f72-107">Syntax</span></span>


```C++
typedef enum tagMPSTATUS_FLAG { 
  MP_STATUS_FLAG_NONE                           = 0,
  MP_STATUS_FLAG_SERVICE_UNAVAILABLE            = 1 << 0,
  MP_STATUS_FLAG_MPENGINE_UNAVAILABLE           = 1 << 1,
  MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED       = 1 << 2,
  MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED         = 1 << 3,
  MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED   = 1 << 4,
  MP_STATUS_FLAG_DUE_AV_SIGNATURE               = 1 << 5,
  MP_STATUS_FLAG_DUE_AS_SIGNATURE               = 1 << 6,
  MP_STATUS_FLAG_DUE_QUICK_SCAN                 = 1 << 7,
  MP_STATUS_FLAG_DUE_FULL_SCAN                  = 1 << 8,
  MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN         = 1 << 9,
  MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING    = 1 << 10,
  MP_STATUS_FLAG_DUE_SAMPLES                    = 1 << 11,
  MP_STATUS_FLAG_EVALUATION_MODE                = 1 << 12,
  MP_STATUS_FLAG_NONGENUINE                     = 1 << 13,
  MP_STATUS_FLAG_PRODUCT_EXPIRED                = 1 << 14,
  MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED       = 1 << 15,
  MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN     = 1 << 16,
  MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE       = 1 << 17,
  MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE   = 1 << 18,
  MP_STATUS_FLAG_HEALTH_INITIALIZED             = 1 << 19,
  MP_STATUS_FLAG_DUE_PLATFORM_UPDATE            = 1 << 20,
  MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE     = 1 << 21,
  MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED  = 1 << 22,
  MP_STATUS_FLAG_END_OF_LIFE                    = 1 << 23,
  MP_STATUS_FLAG_MAX                            = 1 << 23,
  MP_STATUS_FLAG_ALL                            = (1 << 24)-1
} MPSTATUS_FLAG, *PMPSTATUS_FLAG;
```



## <a name="constants"></a><span data-ttu-id="46f72-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="46f72-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="46f72-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**marca de estado de MP \_ \_ \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="46f72-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MP\_STATUS\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-110">No se ha establecido ninguna marca de estado (estado no inicializado).</span><span class="sxs-lookup"><span data-stu-id="46f72-110">No status flags set (non-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="46f72-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**marca de estado de MP \_ \_ \_ servicio \_ no disponible**</span><span class="sxs-lookup"><span data-stu-id="46f72-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**MP\_STATUS\_FLAG\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-112">El servicio no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="46f72-112">Service not running.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**marca de estado de MP \_ \_ \_ MPENGINE \_ no disponible**</span><span class="sxs-lookup"><span data-stu-id="46f72-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP\_STATUS\_FLAG\_MPENGINE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-114">El servicio se inició sin ningún motor de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="46f72-114">Service started without any malware protection engine.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**marca de estado de MP \_ \_ \_ amenaza \_ \_ requerida**</span><span class="sxs-lookup"><span data-stu-id="46f72-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**MP\_STATUS\_FLAG\_THREAT\_FULLSCAN\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-116">Examen completo pendiente debido a una acción de amenaza.</span><span class="sxs-lookup"><span data-stu-id="46f72-116">Pending full scan due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**marca de estado de MP se \_ \_ \_ \_ requiere reinicio de amenazas \_**</span><span class="sxs-lookup"><span data-stu-id="46f72-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**MP\_STATUS\_FLAG\_THREAT\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-118">Reinicio pendiente debido a una acción de amenaza.</span><span class="sxs-lookup"><span data-stu-id="46f72-118">Pending reboot due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**marca de estado de MP \_ \_ \_ \_ pasos manuales de amenazas \_ \_ necesarios**</span><span class="sxs-lookup"><span data-stu-id="46f72-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**MP\_STATUS\_FLAG\_THREAT\_MANUAL\_STEPS\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-120">Pasos manuales pendientes debidos a una acción de amenaza.</span><span class="sxs-lookup"><span data-stu-id="46f72-120">Pending manual steps due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**marca de estado de MP \_ \_ \_ por \_ firma de AV \_**</span><span class="sxs-lookup"><span data-stu-id="46f72-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AV\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-122">Firmas de antivirus no actualizadas.</span><span class="sxs-lookup"><span data-stu-id="46f72-122">Antivirus signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**\_ \_ marca de estado \_ de MP debida \_ como \_ firma**</span><span class="sxs-lookup"><span data-stu-id="46f72-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AS\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-124">Firmas de AntiSpyware no actualizadas.</span><span class="sxs-lookup"><span data-stu-id="46f72-124">Antispyware signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**detección de estado de MP \_ \_ debido a \_ \_ \_ examen rápido**</span><span class="sxs-lookup"><span data-stu-id="46f72-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**MP\_STATUS\_FLAG\_DUE\_QUICK\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-126">No se ha producido ningún examen rápido durante un período especificado.</span><span class="sxs-lookup"><span data-stu-id="46f72-126">No quick scan has happened for a specified period.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**marca de estado del módulo de administración \_ \_ debido a \_ \_ \_ examen completo**</span><span class="sxs-lookup"><span data-stu-id="46f72-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MP\_STATUS\_FLAG\_DUE\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-128">no se ha producido ningún examen completo durante un período especificado</span><span class="sxs-lookup"><span data-stu-id="46f72-128">no full scan has happened for a specified period</span></span>

</dd> <dt>

<span data-ttu-id="46f72-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**marca de estado del módulo de administración \_ \_ \_ \_ examen del sistema en curso \_**</span><span class="sxs-lookup"><span data-stu-id="46f72-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_SYSTEM\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-130">Examen iniciado por el sistema en curso.</span><span class="sxs-lookup"><span data-stu-id="46f72-130">System-initiated scan in progress.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**marca de estado de MP \_ \_ limpieza de \_ rutina en curso \_ \_**</span><span class="sxs-lookup"><span data-stu-id="46f72-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_ROUTINE\_CLEANING**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-132">Limpieza iniciada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="46f72-132">System-initiated clean in progress.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**marca de estado de MP \_ \_ \_ por \_ ejemplos**</span><span class="sxs-lookup"><span data-stu-id="46f72-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**MP\_STATUS\_FLAG\_DUE\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-134">Hay ejemplos de envío pendientes.</span><span class="sxs-lookup"><span data-stu-id="46f72-134">There are samples pending submission.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**\_modo de \_ evaluación de marca de estado de MP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="46f72-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MP\_STATUS\_FLAG\_EVALUATION\_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-136">El producto se está ejecutando en modo de evaluación.</span><span class="sxs-lookup"><span data-stu-id="46f72-136">Product is running in evaluation mode.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**marca de estado de MP no \_ \_ \_ original**</span><span class="sxs-lookup"><span data-stu-id="46f72-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MP\_STATUS\_FLAG\_NONGENUINE**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-138">El producto se está ejecutando en modo Windows no original.</span><span class="sxs-lookup"><span data-stu-id="46f72-138">Product is running in non-genuine Windows mode.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**marca de estado de MP \_ \_ \_ \_ expirada del producto**</span><span class="sxs-lookup"><span data-stu-id="46f72-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**MP\_STATUS\_FLAG\_PRODUCT\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-140">Producto expirado.</span><span class="sxs-lookup"><span data-stu-id="46f72-140">Product expired.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**marca de estado de MP \_ \_ \_ amenaza \_ Callisto \_ requerida**</span><span class="sxs-lookup"><span data-stu-id="46f72-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**MP\_STATUS\_FLAG\_THREAT\_CALLISTO\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-142">Se requiere un análisis sin conexión de Callisto.</span><span class="sxs-lookup"><span data-stu-id="46f72-142">Callisto off-line scan required.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ \_ servicio \_ de marca de estado de MP al \_ apagar el sistema \_**</span><span class="sxs-lookup"><span data-stu-id="46f72-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**MP\_STATUS\_FLAG\_SERVICE\_ON\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-144">El servicio se está cerrando como parte del cierre del sistema.</span><span class="sxs-lookup"><span data-stu-id="46f72-144">Service is shutting down as part of system shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**\_ \_ \_ error crítico de servicio de indicador \_ de estado de MP \_**</span><span class="sxs-lookup"><span data-stu-id="46f72-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-146">Error en la corrección de amenazas de forma crítica.</span><span class="sxs-lookup"><span data-stu-id="46f72-146">Threat remediation failed critically.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**error de servicio de indicador de estado de MP \_ \_ \_ \_ no \_ crítico \_**</span><span class="sxs-lookup"><span data-stu-id="46f72-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_NON\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-148">Error de corrección de amenazas no crítico.</span><span class="sxs-lookup"><span data-stu-id="46f72-148">Threat remediation failed non-critically.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**Estado de indicador de estado de MP \_ \_ \_ \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="46f72-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**MP\_STATUS\_FLAG\_HEALTH\_INITIALIZED**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-150">No se ha establecido ninguna marca de estado (estado bien inicializado).</span><span class="sxs-lookup"><span data-stu-id="46f72-150">No status flags set (well-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="46f72-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**marca de estado de MP \_ \_ \_ debida \_ actualización de plataforma \_**</span><span class="sxs-lookup"><span data-stu-id="46f72-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP\_STATUS\_FLAG\_DUE\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-152">La plataforma no está actualizada.</span><span class="sxs-lookup"><span data-stu-id="46f72-152">The platform is out of date.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**marca de estado de MP \_ \_ actualización de \_ plataforma en curso \_ \_**</span><span class="sxs-lookup"><span data-stu-id="46f72-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-154">La actualización de la plataforma está en curso.</span><span class="sxs-lookup"><span data-stu-id="46f72-154">Platform update is in progress.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**\_plataforma de marca de estado de MP \_ \_ \_ \_ a punto de \_ ser \_ obsoleto**</span><span class="sxs-lookup"><span data-stu-id="46f72-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**MP\_STATUS\_FLAG\_PLATFORM\_ABOUT\_TO\_BE\_OUTDATED**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-156">La plataforma está a punto de estar obsoleta</span><span class="sxs-lookup"><span data-stu-id="46f72-156">The platform is about to be outdated</span></span>

</dd> <dt>

<span data-ttu-id="46f72-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**\_ \_ marca de estado \_ de MP final \_ de \_ ciclo de vida**</span><span class="sxs-lookup"><span data-stu-id="46f72-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**MP\_STATUS\_FLAG\_END\_OF\_LIFE**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-158">La firma o el final de la plataforma de la vida es posterior o está pendiente.</span><span class="sxs-lookup"><span data-stu-id="46f72-158">The signature or platform end of life is past or is pending.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**marca de estado de MP \_ \_ \_ máx.**</span><span class="sxs-lookup"><span data-stu-id="46f72-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP\_STATUS\_FLAG\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-160">Marca válida máxima.</span><span class="sxs-lookup"><span data-stu-id="46f72-160">Maximum valid flag.</span></span>

</dd> <dt>

<span data-ttu-id="46f72-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**marca de estado de MP \_ \_ \_ todos**</span><span class="sxs-lookup"><span data-stu-id="46f72-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MP\_STATUS\_FLAG\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="46f72-162">Valor máximo posible.</span><span class="sxs-lookup"><span data-stu-id="46f72-162">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46f72-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46f72-163">Requirements</span></span>



| <span data-ttu-id="46f72-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="46f72-164">Requirement</span></span> | <span data-ttu-id="46f72-165">Value</span><span class="sxs-lookup"><span data-stu-id="46f72-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46f72-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46f72-166">Minimum supported client</span></span><br/> | <span data-ttu-id="46f72-167">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="46f72-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="46f72-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46f72-168">Minimum supported server</span></span><br/> | <span data-ttu-id="46f72-169">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="46f72-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46f72-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46f72-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="46f72-171"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="46f72-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





