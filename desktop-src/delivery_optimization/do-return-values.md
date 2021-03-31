---
title: Devolver valores
description: Las constantes siguientes representan valores devueltos que la optimización de entrega (DO) genera y valores devueltos de HTTP que realizan capturas.
ms.assetid: 68AC4581-C748-49AB-A588-15816E534756
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e58d66587061cc44fc441249407b73653153322
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078111"
---
# <a name="do-return-values"></a><span data-ttu-id="02ac4-103">Devolver valores</span><span class="sxs-lookup"><span data-stu-id="02ac4-103">DO Return Values</span></span>

<span data-ttu-id="02ac4-104">Las constantes siguientes representan valores devueltos que la optimización de entrega (DO) genera y valores devueltos de HTTP que realizan capturas.</span><span class="sxs-lookup"><span data-stu-id="02ac4-104">The below constants represent return values that Delivery Optimization (DO) generates and HTTP return values that DO captures.</span></span> <span data-ttu-id="02ac4-105">Todos los demás valores devueltos que se pueden recibir son COM, RPC o valores devueltos de Windows convertidos (use la macro [HRESULT_FROM_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) para convertir los valores devueltos de Windows en valores HRESULT).</span><span class="sxs-lookup"><span data-stu-id="02ac4-105">All other return values that you can receive are COM, RPC, or converted Windows return values (DO uses the [HRESULT_FROM_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) macro to convert the Windows return values to HRESULT values).</span></span>

<dl> <dt>

<span data-ttu-id="02ac4-106"><span id="DO_E_NO_SERVICE__0x80d01001_"></span><span id="do_e_no_service__0x80d01001_"></span><span id="DO_E_NO_SERVICE__0X80D01001_"></span>DO_E_NO_SERVICE (0x80d01001)</span><span class="sxs-lookup"><span data-stu-id="02ac4-106"><span id="DO_E_NO_SERVICE__0x80d01001_"></span><span id="do_e_no_service__0x80d01001_"></span><span id="DO_E_NO_SERVICE__0X80D01001_"></span>DO_E_NO_SERVICE (0x80d01001)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-107">La optimización de entrega no pudo proporcionar el servicio.</span><span class="sxs-lookup"><span data-stu-id="02ac4-107">Delivery Optimization was unable to provide the service.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-108"><span id="DO_E_DOWNLOAD_NO_PROGRESS__0x80d02002_"></span><span id="do_e_download_no_progress__0x80d02002_"></span><span id="DO_E_DOWNLOAD_NO_PROGRESS__0X80D02002_"></span>DO_E_DOWNLOAD_NO_PROGRESS (0x80d02002)</span><span class="sxs-lookup"><span data-stu-id="02ac4-108"><span id="DO_E_DOWNLOAD_NO_PROGRESS__0x80d02002_"></span><span id="do_e_download_no_progress__0x80d02002_"></span><span id="DO_E_DOWNLOAD_NO_PROGRESS__0X80D02002_"></span>DO_E_DOWNLOAD_NO_PROGRESS (0x80d02002)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-109">La descarga de un archivo no ha observado ningún progreso dentro del período definido.</span><span class="sxs-lookup"><span data-stu-id="02ac4-109">Download of a file saw no progress within the defined period.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-110"><span id="DO_E_JOB_NOT_FOUND__0x80d02003_"></span><span id="do_e_job_not_found__0x80d02003_"></span><span id="DO_E_JOB_NOT_FOUND__0X80D02003_"></span>DO_E_JOB_NOT_FOUND (0x80d02003)</span><span class="sxs-lookup"><span data-stu-id="02ac4-110"><span id="DO_E_JOB_NOT_FOUND__0x80d02003_"></span><span id="do_e_job_not_found__0x80d02003_"></span><span id="DO_E_JOB_NOT_FOUND__0X80D02003_"></span>DO_E_JOB_NOT_FOUND (0x80d02003)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-111">No se encontró el trabajo, se esperaba que el trabajo estuviera presente.</span><span class="sxs-lookup"><span data-stu-id="02ac4-111">Job was not found, expecting a job to be present.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-112"><span id="DO_E_JOB_EMPTY__0x80d02004_"></span><span id="do_e_job_empty__0x80d02004_"></span><span id="DO_E_JOB_EMPTY__0X80D02004_"></span>DO_E_JOB_EMPTY (0x80d02004)</span><span class="sxs-lookup"><span data-stu-id="02ac4-112"><span id="DO_E_JOB_EMPTY__0x80d02004_"></span><span id="do_e_job_empty__0x80d02004_"></span><span id="DO_E_JOB_EMPTY__0X80D02004_"></span>DO_E_JOB_EMPTY (0x80d02004)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-113">No había ningún archivo en el trabajo, se esperaba al menos un archivo.</span><span class="sxs-lookup"><span data-stu-id="02ac4-113">There was no file in the job, expecting at least one file.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-114"><span id="DO_E_LOCALPATH_NOT_SET__0x80d0200d_"></span><span id="do_e_localpath_not_set__0x80d0200d_"></span><span id="DO_E_LOCALPATH_NOT_SET__0X80D0200D_"></span>DO_E_LOCALPATH_NOT_SET (0x80d0200d)</span><span class="sxs-lookup"><span data-stu-id="02ac4-114"><span id="DO_E_LOCALPATH_NOT_SET__0x80d0200d_"></span><span id="do_e_localpath_not_set__0x80d0200d_"></span><span id="DO_E_LOCALPATH_NOT_SET__0X80D0200D_"></span>DO_E_LOCALPATH_NOT_SET (0x80d0200d)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-115">No se especificó ninguna ruta de acceso de archivo local para esta descarga.</span><span class="sxs-lookup"><span data-stu-id="02ac4-115">There is no local file path specified for this download.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-116"><span id="DO_E_FILE_NOT_AVAILABLE__0x80d02010_"></span><span id="do_e_file_not_available__0x80d02010_"></span><span id="DO_E_FILE_NOT_AVAILABLE__0X80D02010_"></span>DO_E_FILE_NOT_AVAILABLE (0x80d02010)</span><span class="sxs-lookup"><span data-stu-id="02ac4-116"><span id="DO_E_FILE_NOT_AVAILABLE__0x80d02010_"></span><span id="do_e_file_not_available__0x80d02010_"></span><span id="DO_E_FILE_NOT_AVAILABLE__0X80D02010_"></span>DO_E_FILE_NOT_AVAILABLE (0x80d02010)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-117">No hay ningún archivo disponible porque ninguna dirección URL ha generado un error.</span><span class="sxs-lookup"><span data-stu-id="02ac4-117">No file is available because no URL generated an error.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-118"><span id="DO_E_UNKNOWN_PROPERTY_ID__0x80d02011_"></span><span id="do_e_unknown_property_id__0x80d02011_"></span><span id="DO_E_UNKNOWN_PROPERTY_ID__0X80D02011_"></span>DO_E_UNKNOWN_PROPERTY_ID (0x80d02011)</span><span class="sxs-lookup"><span data-stu-id="02ac4-118"><span id="DO_E_UNKNOWN_PROPERTY_ID__0x80d02011_"></span><span id="do_e_unknown_property_id__0x80d02011_"></span><span id="DO_E_UNKNOWN_PROPERTY_ID__0X80D02011_"></span>DO_E_UNKNOWN_PROPERTY_ID (0x80d02011)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-119">Se llama a SetProperty () o GetProperty () con un identificador de propiedad desconocido.</span><span class="sxs-lookup"><span data-stu-id="02ac4-119">SetProperty() or GetProperty() called with an unknown property ID.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-120"><span id="DO_E_READ_ONLY_PROPERTY__0x80d02012_"></span><span id="do_e_read_only_property__0x80d02012_"></span><span id="DO_E_READ_ONLY_PROPERTY__0X80D02012_"></span>DO_E_READ_ONLY_PROPERTY (0x80d02012)</span><span class="sxs-lookup"><span data-stu-id="02ac4-120"><span id="DO_E_READ_ONLY_PROPERTY__0x80d02012_"></span><span id="do_e_read_only_property__0x80d02012_"></span><span id="DO_E_READ_ONLY_PROPERTY__0X80D02012_"></span>DO_E_READ_ONLY_PROPERTY (0x80d02012)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-121">No se puede llamar a SetProperty () en una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="02ac4-121">Unable to call SetProperty() on a read-only property.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-122"><span id="DO_E_INVALID_STATE__0x80d02013_"></span><span id="do_e_invalid_state__0x80d02013_"></span><span id="DO_E_INVALID_STATE__0X80D02013_"></span>DO_E_INVALID_STATE (0x80d02013)</span><span class="sxs-lookup"><span data-stu-id="02ac4-122"><span id="DO_E_INVALID_STATE__0x80d02013_"></span><span id="do_e_invalid_state__0x80d02013_"></span><span id="DO_E_INVALID_STATE__0X80D02013_"></span>DO_E_INVALID_STATE (0x80d02013)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-123">La acción solicitada no se permite en el estado de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="02ac4-123">The requested action is not allowed in the current job state.</span></span> <span data-ttu-id="02ac4-124">Es posible que el trabajo se haya cancelado o se haya completado la transferencia.</span><span class="sxs-lookup"><span data-stu-id="02ac4-124">The job might have been canceled or completed transferring.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-125"><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0x80d02014_"></span><span id="do_e_error_information_unavailable__0x80d02014_"></span><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0X80D02014_"></span>DO_E_ERROR_INFORMATION_UNAVAILABLE (0x80d02014)</span><span class="sxs-lookup"><span data-stu-id="02ac4-125"><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0x80d02014_"></span><span id="do_e_error_information_unavailable__0x80d02014_"></span><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0X80D02014_"></span>DO_E_ERROR_INFORMATION_UNAVAILABLE (0x80d02014)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-126">No se ha producido ningún error.</span><span class="sxs-lookup"><span data-stu-id="02ac4-126">No errors have occurred.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-127"><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0x80d03002_"></span><span id="do_e_no_download_extsettings__0x80d03002_"></span><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0X80D03002_"></span>DO_E_NO_DOWNLOAD_EXTSETTINGS (0x80d03002)</span><span class="sxs-lookup"><span data-stu-id="02ac4-127"><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0x80d03002_"></span><span id="do_e_no_download_extsettings__0x80d03002_"></span><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0X80D03002_"></span>DO_E_NO_DOWNLOAD_EXTSETTINGS (0x80d03002)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-128">No se permite el trabajo de descarga debido a la configuración de usuario/administración.</span><span class="sxs-lookup"><span data-stu-id="02ac4-128">Download job not allowed due to user/admin settings.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-129"><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0x80d03801_"></span><span id="do_e_blocked_by_cost_transfer_policy__0x80d03801_"></span><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0X80D03801_"></span>DO_E_BLOCKED_BY_COST_TRANSFER_POLICY (0x80d03801)</span><span class="sxs-lookup"><span data-stu-id="02ac4-129"><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0x80d03801_"></span><span id="do_e_blocked_by_cost_transfer_policy__0x80d03801_"></span><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0X80D03801_"></span>DO_E_BLOCKED_BY_COST_TRANSFER_POLICY (0x80d03801)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-130">Haga una pausa en el trabajo debido a las restricciones de la Directiva de costos.</span><span class="sxs-lookup"><span data-stu-id="02ac4-130">DO paused the job due to cost policy restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-131"><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0x80d03803_"></span><span id="do_e_blocked_by_cellular_policy__0x80d03803_"></span><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0X80D03803_"></span>DO_E_BLOCKED_BY_CELLULAR_POLICY (0x80d03803)</span><span class="sxs-lookup"><span data-stu-id="02ac4-131"><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0x80d03803_"></span><span id="do_e_blocked_by_cellular_policy__0x80d03803_"></span><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0X80D03803_"></span>DO_E_BLOCKED_BY_CELLULAR_POLICY (0x80d03803)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-132">Haga una pausa en el trabajo debido a la detección de restricciones de directivas y redes móviles.</span><span class="sxs-lookup"><span data-stu-id="02ac4-132">DO paused the job due to detection of cellular network and policy restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-133"><span id="DO_E_BLOCKED_BY_POWER_STATE__0x80d03804_"></span><span id="do_e_blocked_by_power_state__0x80d03804_"></span><span id="DO_E_BLOCKED_BY_POWER_STATE__0X80D03804_"></span>DO_E_BLOCKED_BY_POWER_STATE (0x80d03804)</span><span class="sxs-lookup"><span data-stu-id="02ac4-133"><span id="DO_E_BLOCKED_BY_POWER_STATE__0x80d03804_"></span><span id="do_e_blocked_by_power_state__0x80d03804_"></span><span id="DO_E_BLOCKED_BY_POWER_STATE__0X80D03804_"></span>DO_E_BLOCKED_BY_POWER_STATE (0x80d03804)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-134">Haga una pausa en el trabajo debido a la detección de cambios de estado de energía en modo no AC.</span><span class="sxs-lookup"><span data-stu-id="02ac4-134">DO paused the job due to detection of power state change into non-AC mode.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-135"><span id="DO_E_BLOCKED_BY_NO_NETWORK__0x80d03805_"></span><span id="do_e_blocked_by_no_network__0x80d03805_"></span><span id="DO_E_BLOCKED_BY_NO_NETWORK__0X80D03805_"></span>DO_E_BLOCKED_BY_NO_NETWORK (0x80d03805)</span><span class="sxs-lookup"><span data-stu-id="02ac4-135"><span id="DO_E_BLOCKED_BY_NO_NETWORK__0x80d03805_"></span><span id="do_e_blocked_by_no_network__0x80d03805_"></span><span id="DO_E_BLOCKED_BY_NO_NETWORK__0X80D03805_"></span>DO_E_BLOCKED_BY_NO_NETWORK (0x80d03805)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-136">Haga una pausa en el trabajo debido a la pérdida de conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="02ac4-136">DO paused the job due to loss of network connectivity.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-137"><span id="DO_E_BLOCKED_BY_VPN_POLICY__0x80d03807_"></span><span id="do_e_blocked_by_vpn_policy__0x80d03807_"></span><span id="DO_E_BLOCKED_BY_VPN_POLICY__0X80D03807_"></span>DO_E_BLOCKED_BY_VPN_POLICY (0x80d03807)</span><span class="sxs-lookup"><span data-stu-id="02ac4-137"><span id="DO_E_BLOCKED_BY_VPN_POLICY__0x80d03807_"></span><span id="do_e_blocked_by_vpn_policy__0x80d03807_"></span><span id="DO_E_BLOCKED_BY_VPN_POLICY__0X80D03807_"></span>DO_E_BLOCKED_BY_VPN_POLICY (0x80d03807)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-138">Pausa el trabajo completado debido a la detección de la red VPN.</span><span class="sxs-lookup"><span data-stu-id="02ac4-138">DO paused the completed job due to detection of VPN network.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-139"><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0x80d03808_"></span><span id="do_e_blocked_by_critical_memory_usage__0x80d03808_"></span><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0X80D03808_"></span>DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE (0x80d03808)</span><span class="sxs-lookup"><span data-stu-id="02ac4-139"><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0x80d03808_"></span><span id="do_e_blocked_by_critical_memory_usage__0x80d03808_"></span><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0X80D03808_"></span>DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE (0x80d03808)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-140">Pausa el trabajo completado debido a la detección del uso de memoria crítico en el sistema.</span><span class="sxs-lookup"><span data-stu-id="02ac4-140">DO paused the completed job due to detection of critical memory usage on the system.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-141"><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0x80d05001_"></span><span id="do_e_http_blocksize_mismatch__0x80d05001_"></span><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0X80D05001_"></span>DO_E_HTTP_BLOCKSIZE_MISMATCH (0x80d05001)</span><span class="sxs-lookup"><span data-stu-id="02ac4-141"><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0x80d05001_"></span><span id="do_e_http_blocksize_mismatch__0x80d05001_"></span><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0X80D05001_"></span>DO_E_HTTP_BLOCKSIZE_MISMATCH (0x80d05001)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-142">El servidor HTTP devolvió una respuesta con un tamaño de datos no igual a lo que se solicitó.</span><span class="sxs-lookup"><span data-stu-id="02ac4-142">HTTP server returned a response with data size not equal to what was requested.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-143"><span id="DO_E_INVALID_RANGE__0x80d05010_"></span><span id="do_e_invalid_range__0x80d05010_"></span><span id="DO_E_INVALID_RANGE__0X80D05010_"></span>DO_E_INVALID_RANGE (0x80d05010)</span><span class="sxs-lookup"><span data-stu-id="02ac4-143"><span id="DO_E_INVALID_RANGE__0x80d05010_"></span><span id="do_e_invalid_range__0x80d05010_"></span><span id="DO_E_INVALID_RANGE__0X80D05010_"></span>DO_E_INVALID_RANGE (0x80d05010)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-144">El intervalo de bytes especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="02ac4-144">The specified byte range is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-145"><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0x80d05011_"></span><span id="do_e_insufficient_range_support__0x80d05011_"></span><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0X80D05011_"></span>DO_E_INSUFFICIENT_RANGE_SUPPORT (0x80d05011)</span><span class="sxs-lookup"><span data-stu-id="02ac4-145"><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0x80d05011_"></span><span id="do_e_insufficient_range_support__0x80d05011_"></span><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0X80D05011_"></span>DO_E_INSUFFICIENT_RANGE_SUPPORT (0x80d05011)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-146">El servidor no es compatible con el protocolo HTTP necesario.</span><span class="sxs-lookup"><span data-stu-id="02ac4-146">The server does not support the necessary HTTP protocol.</span></span> <span data-ttu-id="02ac4-147">La optimización de entrega (DO) requiere que el servidor admita el encabezado del Protocolo de intervalo.</span><span class="sxs-lookup"><span data-stu-id="02ac4-147">Delivery Optimization (DO) requires that the server support the Range protocol header.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-148"><span id="DO_E_OVERLAPPING_RANGES__0x80d05012_"></span><span id="do_e_overlapping_ranges__0x80d05012_"></span><span id="DO_E_OVERLAPPING_RANGES__0X80D05012_"></span>DO_E_OVERLAPPING_RANGES (0x80d05012)</span><span class="sxs-lookup"><span data-stu-id="02ac4-148"><span id="DO_E_OVERLAPPING_RANGES__0x80d05012_"></span><span id="do_e_overlapping_ranges__0x80d05012_"></span><span id="DO_E_OVERLAPPING_RANGES__0X80D05012_"></span>DO_E_OVERLAPPING_RANGES (0x80d05012)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-149">La lista de intervalos de bytes contiene algunos intervalos superpuestos, que no se admiten.</span><span class="sxs-lookup"><span data-stu-id="02ac4-149">The list of byte ranges contains some overlapping ranges, which are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="02ac4-150"><span id="DO_E_FATAL_CORE_ERROR__0x80d06802_"></span><span id="do_e_fatal_core_error__0x80d06802_"></span><span id="DO_E_FATAL_CORE_ERROR__0X80D06802_"></span>DO_E_FATAL_CORE_ERROR (0x80d06802)</span><span class="sxs-lookup"><span data-stu-id="02ac4-150"><span id="DO_E_FATAL_CORE_ERROR__0x80d06802_"></span><span id="do_e_fatal_core_error__0x80d06802_"></span><span id="DO_E_FATAL_CORE_ERROR__0X80D06802_"></span>DO_E_FATAL_CORE_ERROR (0x80d06802)</span></span>
</dt> <dd>

<span data-ttu-id="02ac4-151">Error irrecuperable en Core.</span><span class="sxs-lookup"><span data-stu-id="02ac4-151">Fatal error encountered in core.</span></span>

</dd> </dl>

 

 