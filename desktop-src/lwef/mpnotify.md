---
title: Enumeración MPNOTIFY (MpClient. h)
description: Posibles notificaciones de devolución de llamada.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- Enumeración MPNOTIFY características de entorno heredado de Windows
- Puntero de enumeración PMPNOTIFY características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPNOTIFY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afa0eeb6cb1d610f28cc82f578617f7bd71cf886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705153"
---
# <a name="mpnotify-enumeration"></a><span data-ttu-id="e3744-105">Enumeración MPNOTIFY</span><span class="sxs-lookup"><span data-stu-id="e3744-105">MPNOTIFY enumeration</span></span>

<span data-ttu-id="e3744-106">Posibles notificaciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e3744-106">Possible callback notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3744-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3744-107">Syntax</span></span>


```C++
typedef enum tagMPNOTIFY { 
  MPNOTIFY_NONE,
  MPNOTIFY_CALL_START,
  MPNOTIFY_CALL_COMPLETE,
  MPNOTIFY_INTERNAL_FAILURE,
  MPNOTIFY_STATUS_SERVICE_START,
  MPNOTIFY_STATUS_SERVICE_RUNNING,
  MPNOTIFY_STATUS_SERVICE_STOP,
  MPNOTIFY_STATUS_COMPONENT,
  MPNOTIFY_STATUS_CHANGE,
  MPNOTIFY_STATUS_COMPONENT_CONFIGURATION,
  MPNOTIFY_STATUS_EXPIRATION_CHANGE,
  MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE,
  MPNOTIFY_SCAN_START,
  MPNOTIFY_SCAN_PAUSED,
  MPNOTIFY_SCAN_RESUMED,
  MPNOTIFY_SCAN_CANCEL,
  MPNOTIFY_SCAN_COMPLETE,
  MPNOTIFY_SCAN_PROGRESS,
  MPNOTIFY_SCAN_ERROR,
  MPNOTIFY_SCAN_INFECTED,
  MPNOTIFY_SCAN_MEMORYSTART,
  MPNOTIFY_SCAN_MEMORYCOMPLETE,
  MPNOTIFY_SCAN_SFC_BUILD_START,
  MPNOTIFY_SCAN_SFC_BUILD_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_START,
  MPNOTIFY_SCAN_FASTPATH_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_PROGRESS,
  MPNOTIFY_CLEAN_START,
  MPNOTIFY_CLEAN_COMPLETE,
  MPNOTIFY_CLEAN_RESTOREPOINT_START,
  MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED,
  MPNOTIFY_CLEAN_RESTOREPOINT_FAILED,
  MPNOTIFY_CLEAN_THREAT_START,
  MPNOTIFY_CLEAN_THREAT_SUCCEEDED,
  MPNOTIFY_CLEAN_THREAT_FAILED,
  MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED,
  MPNOTIFY_CLEAN_RESOURCE_FAILED,
  MPNOTIFY_CLEAN_THREAT_COMPLETE,
  MPNOTIFY_PRECHECK_START,
  MPNOTIFY_PRECHECK_COMPLETE,
  MPNOTIFY_PRECHECK_RESOURCE_BLOCKED,
  MPNOTIFY_THREAT_DETECTED,
  MPNOTIFY_THREAT_MODIFIED,
  MPNOTIFY_THREAT_CLEAN_SUCCEEDED,
  MPNOTIFY_THREAT_CLEAN_FAILED,
  MPNOTIFY_THREAT_ABANDONED,
  MPNOTIFY_THREAT_CLEAN_EVENT_START,
  MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE,
  MPNOTIFY_SIGUPDATE_START,
  MPNOTIFY_SIGUPDATE_SEARCH_START,
  MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE,
  MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_START,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE,
  MPNOTIFY_SIGUPDATE_INSTALL_START,
  MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS,
  MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE,
  MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED,
  MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED,
  MPNOTIFY_SIGUPDATE_COMPLETE,
  MPNOTIFY_SAMPLE_START,
  MPNOTIFY_SAMPLE_COMPLETE,
  MPNOTIFY_SAMPLE_ITEM_START,
  MPNOTIFY_SAMPLE_ITEM_SUCCEEDED,
  MPNOTIFY_SAMPLE_ITEM_FAILED,
  MPNOTIFY_RESERVED_DATA,
  MPNOTIFY_FASTPATH_SIG_ADDED,
  MPNOTIFY_FASTPATH_SIG_REMOVED,
  MPNOTIFY_NIS_PRIVATE,
  MPNOTIFY_HEALTH_CHANGE,
  MPNOTIFY_HEALTH_RECOVERY,
  MPNOTIFY_HEALTH_START,
  MPNOTIFY_ENDOFLIFE_CHANGE,
  MPNOTIFY_MALWARETOAST_DATA
} MPNOTIFY, *PMPNOTIFY;
```



## <a name="constants"></a><span data-ttu-id="e3744-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="e3744-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e3744-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="e3744-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY\_NONE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e3744-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**\_Inicio de llamada de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**MPNOTIFY\_CALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-111">Inicio de la llamada de notificación.</span><span class="sxs-lookup"><span data-stu-id="e3744-111">Notification call start.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**llamada de MPNOTIFY \_ \_ completada**</span><span class="sxs-lookup"><span data-stu-id="e3744-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**MPNOTIFY\_CALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-113">Llamada de notificación completada.</span><span class="sxs-lookup"><span data-stu-id="e3744-113">Notification call completed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**\_error interno de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**MPNOTIFY\_INTERNAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-115">Error interno genérico.</span><span class="sxs-lookup"><span data-stu-id="e3744-115">Generic internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**\_Inicio del \_ servicio de estado de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**MPNOTIFY\_STATUS\_SERVICE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-117">El servicio de protección contra malware se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="e3744-117">Malware protection service has started.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**servicio de estado de MPNOTIFY en \_ \_ \_ ejecución**</span><span class="sxs-lookup"><span data-stu-id="e3744-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**MPNOTIFY\_STATUS\_SERVICE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-119">El servicio de protección contra malware se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="e3744-119">Malware protection service is running.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**\_detención del \_ servicio de estado de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**MPNOTIFY\_STATUS\_SERVICE\_STOP**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-121">El servicio de protección contra malware se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="e3744-121">Malware protection service has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**\_componente de estado MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**MPNOTIFY\_STATUS\_COMPONENT**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-123">Componente determinado habilitar o deshabilitar el estado.</span><span class="sxs-lookup"><span data-stu-id="e3744-123">Particular component enable/disable status.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**\_cambio de estado de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**MPNOTIFY\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-125">El estado general del producto ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e3744-125">Overall product status has changed.</span></span> <span data-ttu-id="e3744-126">Llame a [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) para obtener el estado actual.</span><span class="sxs-lookup"><span data-stu-id="e3744-126">Call [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) to obtain the current status.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**\_configuración del \_ componente de estado MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**MPNOTIFY\_STATUS\_COMPONENT\_CONFIGURATION**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-128">Un componente determinado ha cambiado la configuración.</span><span class="sxs-lookup"><span data-stu-id="e3744-128">A particular component has changed configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**\_cambio de \_ expiración de estado de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**MPNOTIFY\_STATUS\_EXPIRATION\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-130">El estado de expiración del producto ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e3744-130">Product expiration status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**Estado de MPNOTIFY \_ \_ cambio de examen sin conexión \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**MPNOTIFY\_STATUS\_OFFLINE\_SCAN\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-132">Cambio de Estado requerido del examen sin conexión.</span><span class="sxs-lookup"><span data-stu-id="e3744-132">Offline scan required state changed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**\_Inicio de examen de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**MPNOTIFY\_SCAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-134">Examen iniciado.</span><span class="sxs-lookup"><span data-stu-id="e3744-134">Scan started.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**examen de MPNOTIFY en \_ \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="e3744-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**MPNOTIFY\_SCAN\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-136">Examen en pausa.</span><span class="sxs-lookup"><span data-stu-id="e3744-136">Scan paused.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**examen de MPNOTIFY \_ \_ reanudado**</span><span class="sxs-lookup"><span data-stu-id="e3744-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**MPNOTIFY\_SCAN\_RESUMED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-138">examen reanudado.</span><span class="sxs-lookup"><span data-stu-id="e3744-138">scan resumed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**\_Cancelar examen de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY\_SCAN\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-140">Examen cancelado.</span><span class="sxs-lookup"><span data-stu-id="e3744-140">Scan cancelled.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**examen de MPNOTIFY \_ \_ completado**</span><span class="sxs-lookup"><span data-stu-id="e3744-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**MPNOTIFY\_SCAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-142">Examen completado.</span><span class="sxs-lookup"><span data-stu-id="e3744-142">Scan completed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**\_progreso del examen de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**MPNOTIFY\_SCAN\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-144">Notificación de progreso del recurso específico que se está examinando.</span><span class="sxs-lookup"><span data-stu-id="e3744-144">Progress notification for the specific resource being scanned.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**\_error de examen de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**MPNOTIFY\_SCAN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-146">Error al examinar un recurso determinado.</span><span class="sxs-lookup"><span data-stu-id="e3744-146">Failure to scan a particular resource.</span></span> <span data-ttu-id="e3744-147">El examen continuará.</span><span class="sxs-lookup"><span data-stu-id="e3744-147">Scan will still continue.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**examen de MPNOTIFY \_ \_ infectado**</span><span class="sxs-lookup"><span data-stu-id="e3744-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**MPNOTIFY\_SCAN\_INFECTED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-149">El examen encontró un recurso infectado.</span><span class="sxs-lookup"><span data-stu-id="e3744-149">Scan found an infected resource.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ scan \_ MEMORYSTART**</span><span class="sxs-lookup"><span data-stu-id="e3744-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY\_SCAN\_MEMORYSTART**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-151">Se inició el progreso de la notificación en la parte de análisis de la memoria del examen del sistema.</span><span class="sxs-lookup"><span data-stu-id="e3744-151">Scan progress to notify memory scan portion of the system scan has started.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ scan \_ MEMORYCOMPLETE**</span><span class="sxs-lookup"><span data-stu-id="e3744-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-153">Examinar el progreso para notificar a la parte de análisis de memoria del análisis del sistema se ha completado.</span><span class="sxs-lookup"><span data-stu-id="e3744-153">Scan progress to notify memory scan portion of the system scan has completed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY \_ examinar el inicio de la \_ compilación de SFC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-155">Progreso del examen para notificar que la parte de la compilación de SFC se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="e3744-155">Scan progress to notify sfc build portion has started.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY \_ examinar la \_ compilación de SFC \_ \_ completada**</span><span class="sxs-lookup"><span data-stu-id="e3744-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-157">Progreso del examen para notificar que la parte de la compilación de SFC ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="e3744-157">Scan progress to notify sfc build portion has completed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY \_ scan \_ FASTPATH \_ Start**</span><span class="sxs-lookup"><span data-stu-id="e3744-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY\_SCAN\_FASTPATH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-159">Se ha iniciado la exploración de FastPATH SpyNet.</span><span class="sxs-lookup"><span data-stu-id="e3744-159">Scan fastpath spynet has begun.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY \_ examen de \_ FASTPATH \_ completado**</span><span class="sxs-lookup"><span data-stu-id="e3744-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY\_SCAN\_FASTPATH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-161">La exploración de FastPATH SpyNet ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="e3744-161">Scan fastpath spynet has ended.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**\_progreso de \_ FASTPATH de examen de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY\_SCAN\_FASTPATH\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-163">Notificación de progreso para los nuevos análisis de FastPATH, que se usan internamente y se convierten en el **\_ \_ progreso de examen de MPNOTIFY** para los externos.</span><span class="sxs-lookup"><span data-stu-id="e3744-163">Progress notification for fastpath rescans, used internally and converted to **MPNOTIFY\_SCAN\_PROGRESS** for external.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**\_Inicio limpio de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**MPNOTIFY\_CLEAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-165">Limpieza iniciada.</span><span class="sxs-lookup"><span data-stu-id="e3744-165">Cleaning started.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**limpieza de MPNOTIFY \_ \_ completada**</span><span class="sxs-lookup"><span data-stu-id="e3744-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY\_CLEAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-167">Limpieza completada.</span><span class="sxs-lookup"><span data-stu-id="e3744-167">Cleaning completed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ Start**</span><span class="sxs-lookup"><span data-stu-id="e3744-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-169">Se inició para crear un punto de restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="e3744-169">Started to create a system restore point.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ Succeeded**</span><span class="sxs-lookup"><span data-stu-id="e3744-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-171">Punto de restauración del sistema creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e3744-171">System restore point successfully created.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ failed**</span><span class="sxs-lookup"><span data-stu-id="e3744-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-173">No se pudo crear el punto de restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="e3744-173">System restore point creation failed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**Inicio de la amenaza de limpieza de MPNOTIFY \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**MPNOTIFY\_CLEAN\_THREAT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-175">La limpieza se inicia para una amenaza determinada.</span><span class="sxs-lookup"><span data-stu-id="e3744-175">Cleaning is started for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**la amenaza de limpieza de MPNOTIFY se \_ \_ \_ realizó correctamente**</span><span class="sxs-lookup"><span data-stu-id="e3744-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-177">La limpieza se realiza correctamente para una amenaza determinada.</span><span class="sxs-lookup"><span data-stu-id="e3744-177">Cleaning is succeeded for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**error de la amenaza de limpieza de MPNOTIFY \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**MPNOTIFY\_CLEAN\_THREAT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-179">Error en la limpieza de una amenaza determinada.</span><span class="sxs-lookup"><span data-stu-id="e3744-179">Cleaning has failed for a particular threat.</span></span> <span data-ttu-id="e3744-180">**Error \_ de El código de error de la amenaza de MP \_ \_ no \_ encontrada** indica que no se encontró la amenaza (y no se pudo limpiar).</span><span class="sxs-lookup"><span data-stu-id="e3744-180">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="e3744-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**el recurso de limpieza de MPNOTIFY se \_ \_ \_ realizó correctamente**</span><span class="sxs-lookup"><span data-stu-id="e3744-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-182">La limpieza se realiza correctamente para un recurso determinado.</span><span class="sxs-lookup"><span data-stu-id="e3744-182">Cleaning is succeeded for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**\_ \_ \_ no se pudo limpiar el recurso MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="e3744-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-184">Error en la limpieza de un recurso determinado.</span><span class="sxs-lookup"><span data-stu-id="e3744-184">Cleaning has failed for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**amenaza de limpieza de MPNOTIFY \_ \_ \_ completada**</span><span class="sxs-lookup"><span data-stu-id="e3744-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY\_CLEAN\_THREAT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-186">La limpieza se ha completado para una amenaza determinada.</span><span class="sxs-lookup"><span data-stu-id="e3744-186">Cleaning has completed for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**Inicio de la comprobación de MPNOTIFY \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**MPNOTIFY\_PRECHECK\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-188">Se inició la comprobación previamente limpia.</span><span class="sxs-lookup"><span data-stu-id="e3744-188">Clean precheck started.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**\_comprobación de MPNOTIFY \_ completada**</span><span class="sxs-lookup"><span data-stu-id="e3744-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**MPNOTIFY\_PRECHECK\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-190">Comprobación de limpieza completada.</span><span class="sxs-lookup"><span data-stu-id="e3744-190">Clean precheck completed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY \_ precomprobar \_ recurso \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="e3744-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-192">La precomprobación limpia detectó un recurso bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e3744-192">Clean precheck detected blocked resource.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**\_amenaza MPNOTIFY \_ detectada**</span><span class="sxs-lookup"><span data-stu-id="e3744-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**MPNOTIFY\_THREAT\_DETECTED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-194">Se ha detectado una nueva amenaza en el sistema.</span><span class="sxs-lookup"><span data-stu-id="e3744-194">New threat detected in system.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**MPNOTIFY \_ amenaza \_ modificada**</span><span class="sxs-lookup"><span data-stu-id="e3744-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**MPNOTIFY\_THREAT\_MODIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-196">Información de amenazas modificada.</span><span class="sxs-lookup"><span data-stu-id="e3744-196">Threat information modified.</span></span> <span data-ttu-id="e3744-197">Por ejemplo, se ha agregado un nuevo recurso.</span><span class="sxs-lookup"><span data-stu-id="e3744-197">For example, a new resource was added.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**limpieza de la amenaza de MPNOTIFY \_ \_ \_ correcta**</span><span class="sxs-lookup"><span data-stu-id="e3744-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-199">Acción de limpieza correcta para una amenaza.</span><span class="sxs-lookup"><span data-stu-id="e3744-199">Cleaning action succeeded for a threat.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**\_ \_ error al limpiar la amenaza de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**MPNOTIFY\_THREAT\_CLEAN\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-201">No se pudo limpiar la acción de una amenaza.</span><span class="sxs-lookup"><span data-stu-id="e3744-201">Cleaning action failed for a threat.</span></span> <span data-ttu-id="e3744-202">**Error \_ de El código de error de la amenaza de MP \_ \_ no \_ encontrada** indica que no se encontró la amenaza (y no se pudo limpiar).</span><span class="sxs-lookup"><span data-stu-id="e3744-202">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="e3744-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MPNOTIFY \_ amenaza \_ abandonada**</span><span class="sxs-lookup"><span data-stu-id="e3744-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MPNOTIFY\_THREAT\_ABANDONED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-204">No se ha producido ninguna corrección antes de que se detuviera el servicio.</span><span class="sxs-lookup"><span data-stu-id="e3744-204">No remediation occurred before the service was stopped.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**\_Inicio de \_ evento de limpieza de amenazas MPNOTIFY \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-206">Se ha iniciado una acción de limpieza.</span><span class="sxs-lookup"><span data-stu-id="e3744-206">A cleaning action has been started.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**evento de limpieza de la amenaza de MPNOTIFY \_ \_ \_ \_ completado**</span><span class="sxs-lookup"><span data-stu-id="e3744-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-208">Ha finalizado una acción de limpieza.</span><span class="sxs-lookup"><span data-stu-id="e3744-208">A cleaning action has ended.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**Inicio de MPNOTIFY \_ SIGUPDATE \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY\_SIGUPDATE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-210">Actualización de firma iniciada.</span><span class="sxs-lookup"><span data-stu-id="e3744-210">Signature update started.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**Inicio de la búsqueda de MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-212">Buscar actualizaciones iniciadas.</span><span class="sxs-lookup"><span data-stu-id="e3744-212">Search for updates started.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ Search \_ completado**</span><span class="sxs-lookup"><span data-stu-id="e3744-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-214">Buscar actualizaciones completadas.</span><span class="sxs-lookup"><span data-stu-id="e3744-214">Search for updates completed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**actualización de software de MPNOTIFY \_ SIGUPDATE \_ \_ \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="e3744-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**MPNOTIFY\_SIGUPDATE\_SOFTWARE\_UPDATE\_AVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-216">Actualización de software disponible.</span><span class="sxs-lookup"><span data-stu-id="e3744-216">Software update available.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**Inicio de la descarga de MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-218">Descarga iniciada.</span><span class="sxs-lookup"><span data-stu-id="e3744-218">Download started.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**progreso de descarga de MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-220">Descarga en curso.</span><span class="sxs-lookup"><span data-stu-id="e3744-220">Download in progress.</span></span> <span data-ttu-id="e3744-221">Los datos de devolución de llamada contienen progreso.</span><span class="sxs-lookup"><span data-stu-id="e3744-221">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**descarga de MPNOTIFY \_ SIGUPDATE \_ \_ completado**</span><span class="sxs-lookup"><span data-stu-id="e3744-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-223">Descarga completada.</span><span class="sxs-lookup"><span data-stu-id="e3744-223">Download completed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**Inicio de la instalación de MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-225">Instalación iniciada.</span><span class="sxs-lookup"><span data-stu-id="e3744-225">Installation started.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**progreso de la instalación de MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-227">Instalación en curso.</span><span class="sxs-lookup"><span data-stu-id="e3744-227">Installation in progress.</span></span> <span data-ttu-id="e3744-228">Los datos de devolución de llamada contienen progreso.</span><span class="sxs-lookup"><span data-stu-id="e3744-228">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**instalación de MPNOTIFY \_ SIGUPDATE \_ \_ completado**</span><span class="sxs-lookup"><span data-stu-id="e3744-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-230">Instalación completada.</span><span class="sxs-lookup"><span data-stu-id="e3744-230">Installation complete.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**se \_ \_ requiere un reinicio de MPNOTIFY SIGUPDATE \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-232">La actualización requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="e3744-232">Update requires reboot.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**solicitud de MPNOTIFY \_ SIGUPDATE \_ \_ procesada**</span><span class="sxs-lookup"><span data-stu-id="e3744-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-234">El servicio procesó una solicitud de actualización de firma.</span><span class="sxs-lookup"><span data-stu-id="e3744-234">Service processed a signature update request.</span></span> <span data-ttu-id="e3744-235">El error o el éxito se indica mediante **hResult** en los datos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e3744-235">Failure or success is indicated by **hResult** in the callback data.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ completado**</span><span class="sxs-lookup"><span data-stu-id="e3744-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-237">Actualización completada.</span><span class="sxs-lookup"><span data-stu-id="e3744-237">Update complete.</span></span> <span data-ttu-id="e3744-238">**S \_** El estado False indica que no se necesita ninguna actualización.</span><span class="sxs-lookup"><span data-stu-id="e3744-238">**S\_FALSE** status indicates that no updates were needed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**\_Inicio del ejemplo MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**MPNOTIFY\_SAMPLE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-240">Se inició el envío de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e3744-240">Sample submission started.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**ejemplo de MPNOTIFY \_ \_ completado**</span><span class="sxs-lookup"><span data-stu-id="e3744-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**MPNOTIFY\_SAMPLE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-242">Envío de ejemplo completado.</span><span class="sxs-lookup"><span data-stu-id="e3744-242">Sample submission completed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**\_Inicio del \_ elemento de ejemplo MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**MPNOTIFY\_SAMPLE\_ITEM\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-244">Se inició el envío del elemento de ejemplo específico.</span><span class="sxs-lookup"><span data-stu-id="e3744-244">Specific sample item submission started.</span></span> <span data-ttu-id="e3744-245">El índice de elemento de ejemplo está disponible en los [**\_ datos de MPSAMPLE**](mpsample-data.md).</span><span class="sxs-lookup"><span data-stu-id="e3744-245">Sample item index is available in [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3744-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**el \_ elemento de ejemplo MPNOTIFY se \_ \_ realizó correctamente**</span><span class="sxs-lookup"><span data-stu-id="e3744-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**MPNOTIFY\_SAMPLE\_ITEM\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-247">El envío del elemento de ejemplo específico se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e3744-247">Specific sample item submission succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**error en el \_ elemento de ejemplo MPNOTIFY \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**MPNOTIFY\_SAMPLE\_ITEM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-249">Error en el envío del elemento de ejemplo específico.</span><span class="sxs-lookup"><span data-stu-id="e3744-249">Specific sample item submission failed.</span></span> <span data-ttu-id="e3744-250">El código de error está disponible en los [**\_ datos de MPCALLBACK**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="e3744-250">Error code is available in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3744-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY \_ \_ datos reservados**</span><span class="sxs-lookup"><span data-stu-id="e3744-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY\_RESERVED\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-252">Datos reservados internos.</span><span class="sxs-lookup"><span data-stu-id="e3744-252">Internal reserved data.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ Added**</span><span class="sxs-lookup"><span data-stu-id="e3744-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY\_FASTPATH\_SIG\_ADDED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-254">Una firma FastPath ha agregado o deshabilitado una firma.</span><span class="sxs-lookup"><span data-stu-id="e3744-254">A Fastpath signature has either added or disabled a signature.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ quitado**</span><span class="sxs-lookup"><span data-stu-id="e3744-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY\_FASTPATH\_SIG\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-256">Se ha quitado una firma de FastPath.</span><span class="sxs-lookup"><span data-stu-id="e3744-256">A FastPath signature has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ privado**</span><span class="sxs-lookup"><span data-stu-id="e3744-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY\_NIS\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-258">Notificaciones privado NIS.</span><span class="sxs-lookup"><span data-stu-id="e3744-258">NIS private notifcations.</span></span> <span data-ttu-id="e3744-259">No se debe registrar ningún socio para esto.</span><span class="sxs-lookup"><span data-stu-id="e3744-259">No partners should register for this.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**\_cambio de estado de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY\_HEALTH\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-261">El servicio AM entró en un estado nuevo.</span><span class="sxs-lookup"><span data-stu-id="e3744-261">The AM service has entered a new state.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**\_recuperación de mantenimiento de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**MPNOTIFY\_HEALTH\_RECOVERY**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-263">El servicio AM se ha recuperado de un estado.</span><span class="sxs-lookup"><span data-stu-id="e3744-263">The AM service has recovered from a state.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**\_Inicio de estado de MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**MPNOTIFY\_HEALTH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-265">El servicio AM ha inicializado el estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="e3744-265">The AM service has initialized the health of the system.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**cambio de MPNOTIFY \_ ENDOFLIFE \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MPNOTIFY\_ENDOFLIFE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-267">Las fechas de expiración del "final del ciclo de vida" del servicio AM han cambiado.</span><span class="sxs-lookup"><span data-stu-id="e3744-267">The "End Of Life" expiry dates for the AM service have changed.</span></span>

</dd> <dt>

<span data-ttu-id="e3744-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**datos de MPNOTIFY \_ MALWARETOAST \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY\_MALWARETOAST\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="e3744-269">El servicio AM ha detectado malware que podría haber provocado un cambio de configuración crítico en el equipo.</span><span class="sxs-lookup"><span data-stu-id="e3744-269">The AM service has encountered malware that might have caused critical settings change in the machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3744-270">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3744-270">Requirements</span></span>



| <span data-ttu-id="e3744-271">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3744-271">Requirement</span></span> | <span data-ttu-id="e3744-272">Value</span><span class="sxs-lookup"><span data-stu-id="e3744-272">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3744-273">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3744-273">Minimum supported client</span></span><br/> | <span data-ttu-id="e3744-274">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3744-274">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e3744-275">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3744-275">Minimum supported server</span></span><br/> | <span data-ttu-id="e3744-276">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3744-276">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3744-277">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3744-277">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3744-278"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3744-278"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3744-279">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3744-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3744-280">**MpManagerStatusQueryEx**</span><span class="sxs-lookup"><span data-stu-id="e3744-280">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="e3744-281">**datos de MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-281">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="e3744-282">**datos de MPSAMPLE \_**</span><span class="sxs-lookup"><span data-stu-id="e3744-282">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> </dl>

 

 





