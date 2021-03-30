---
title: Valores devueltos de BITS
description: El archivo Bitsmsg. h contiene las siguientes constantes de valor devuelto.
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- BITS de errores
- BITS de errores, códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9086de1d55bbdc9695876bd06368ab28dbbb161
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995501"
---
# <a name="bits-return-values"></a><span data-ttu-id="d0802-105">Valores devueltos de BITS</span><span class="sxs-lookup"><span data-stu-id="d0802-105">BITS Return Values</span></span>

<span data-ttu-id="d0802-106">El archivo Bitsmsg. h contiene las siguientes constantes de valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="d0802-106">The Bitsmsg.h file contains the following return value constants.</span></span> <span data-ttu-id="d0802-107">Las constantes representan los valores devueltos que genera BITS y los valores devueltos de HTTP que BITS captura.</span><span class="sxs-lookup"><span data-stu-id="d0802-107">The constants represent return values that BITS generates and HTTP return values that BITS captures.</span></span> <span data-ttu-id="d0802-108">Todos los demás valores devueltos que puede recibir son COM, RPC o valores devueltos de Windows convertidos (BITS usa el [valor HRESULT de la macro \_ \_ Win32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) para convertir los valores devueltos de Windows en valores HRESULT).</span><span class="sxs-lookup"><span data-stu-id="d0802-108">All other return values that you can receive are COM, RPC, or converted Windows return values (BITS uses the [HRESULT\_FROM\_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) macro to convert the Windows return values to HRESULT values).</span></span>

<span data-ttu-id="d0802-109">Tenga en cuenta que el archivo Bitsmsg. h contiene valores devueltos adicionales que no se enumeran a continuación.</span><span class="sxs-lookup"><span data-stu-id="d0802-109">Note that the Bitsmsg.h file contains additional return values not listed below.</span></span>

<dl> <dt>

<span data-ttu-id="d0802-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>Total de BG \_ S \_ parcial \_ (0x00200017)</span><span class="sxs-lookup"><span data-stu-id="d0802-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG\_S\_PARTIAL\_COMPLETE (0x00200017)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-111">Un subconjunto de los archivos del trabajo transferidos correctamente antes de que se llamara al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="d0802-111">A subset of the job's files transferred successfully before the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method was called.</span></span> <span data-ttu-id="d0802-112">Se eliminaron los que no se completaron.</span><span class="sxs-lookup"><span data-stu-id="d0802-112">Those that were not complete were deleted.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ S \_ no \_ puede \_ eliminar \_ archivos (0x0020001A)</span><span class="sxs-lookup"><span data-stu-id="d0802-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG\_S\_UNABLE\_TO\_DELETE\_FILES (0x0020001A)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-114">No se pueden eliminar todos los archivos temporales asociados al trabajo.</span><span class="sxs-lookup"><span data-stu-id="d0802-114">Unable to delete all temporary files associated with the job.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG \_ S \_ invalidada \_ por la \_ Directiva (0x00200055)</span><span class="sxs-lookup"><span data-stu-id="d0802-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG\_S\_OVERRIDDEN\_BY\_POLICY (0x00200055)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-116">La preferencia de configuración se ha guardado correctamente, pero no se usará la preferencia porque un valor de directiva de grupo configurado invalida la preferencia.</span><span class="sxs-lookup"><span data-stu-id="d0802-116">The configuration preference has been saved successfully, but the preference will not be used because a configured Group Policy setting overrides the preference.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E \_ no \_ encontrado (0x80200001)</span><span class="sxs-lookup"><span data-stu-id="d0802-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG\_E\_NOT\_FOUND (0x80200001)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-118">No se encontró el trabajo solicitado.</span><span class="sxs-lookup"><span data-stu-id="d0802-118">The requested job was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>\_ \_ Estado no válido de BG E \_ (0x80200002)</span><span class="sxs-lookup"><span data-stu-id="d0802-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG\_E\_INVALID\_STATE (0x80200002)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-120">La acción solicitada no se permite en el estado de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="d0802-120">The requested action is not allowed in the current job state.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ Empty (0x80200003)</span><span class="sxs-lookup"><span data-stu-id="d0802-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG\_E\_EMPTY (0x80200003)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-122">El trabajo debe contener uno o más archivos para poder reanudar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="d0802-122">The job must contain one or more files before you can resume the job.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>Archivo de BG \_ E \_ \_ no \_ disponible (0x80200004)</span><span class="sxs-lookup"><span data-stu-id="d0802-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>BG\_E\_FILE\_NOT\_AVAILABLE (0x80200004)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-124">La información del archivo no está disponible porque el error no está asociado a un archivo local o remoto.</span><span class="sxs-lookup"><span data-stu-id="d0802-124">File information is not available because the error is not associated with a local or remote file.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>\_Protocolo BG \_ E \_ no \_ disponible (0x80200005)</span><span class="sxs-lookup"><span data-stu-id="d0802-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>BG\_E\_PROTOCOL\_NOT\_AVAILABLE (0x80200005)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-126">La información del Protocolo no está disponible porque el error no está asociado con el protocolo de transferencia especificado.</span><span class="sxs-lookup"><span data-stu-id="d0802-126">Protocol information is not available because the error is not associated with the specified transfer protocol.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>Destino de BG \_ E \_ \_ bloqueado (0x8020000D)</span><span class="sxs-lookup"><span data-stu-id="d0802-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG\_E\_DESTINATION\_LOCKED (0x8020000D)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-128">El volumen del sistema de archivos de destino, especificado en el nombre de archivo local, está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="d0802-128">The destination file system volume, specified in the local file name, is locked.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>Volumen de BG \_ E \_ \_ cambiado (0x8020000E)</span><span class="sxs-lookup"><span data-stu-id="d0802-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG\_E\_VOLUME\_CHANGED (0x8020000E)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-130">Ha cambiado el volumen de destino especificado en el nombre de archivo local.</span><span class="sxs-lookup"><span data-stu-id="d0802-130">The destination volume, specified in the local file name, has changed.</span></span> <span data-ttu-id="d0802-131">Por ejemplo, el disquete original se ha reemplazado por un disquete diferente.</span><span class="sxs-lookup"><span data-stu-id="d0802-131">For example, the original floppy disk has been replaced with a different floppy disk.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>Información de error de BG \_ E \_ \_ \_ no disponible (0x8020000F)</span><span class="sxs-lookup"><span data-stu-id="d0802-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>BG\_E\_ERROR\_INFORMATION\_UNAVAILABLE (0x8020000F)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-133">La información del error solo está disponible cuando el estado del trabajo es \_ error de estado del trabajo de BG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d0802-133">Error information is only available when the state of the job is BG\_JOB\_STATE\_ERROR.</span></span> <span data-ttu-id="d0802-134">La información del error no está disponible después de que BITS empiece a transferir los datos del trabajo o se cierre el cliente.</span><span class="sxs-lookup"><span data-stu-id="d0802-134">The error information is not available after BITS begins transferring the job's data or the client exits.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>\_Red BG \_ E \_ desconectada (0x80200010)</span><span class="sxs-lookup"><span data-stu-id="d0802-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG\_E\_NETWORK\_DISCONNECTED (0x80200010)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-136">El adaptador de red está inactivo o está desconectado.</span><span class="sxs-lookup"><span data-stu-id="d0802-136">The network adapter is inactive or disconnected.</span></span> <span data-ttu-id="d0802-137">Todos los trabajos se colocan en el \_ \_ Estado de error transitorio de estado de trabajo de BG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d0802-137">All jobs are placed in the BG\_JOB\_STATE\_TRANSIENT\_ERROR state.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>\_ \_ Falta el tamaño de archivo de BG E \_ \_ (0x80200011)</span><span class="sxs-lookup"><span data-stu-id="d0802-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG\_E\_MISSING\_FILE\_SIZE (0x80200011)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-139">El servidor no devolvió el tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="d0802-139">The server did not return the file size.</span></span> <span data-ttu-id="d0802-140">BITS solo transfiere contenido estático y requiere que el servidor HTTP devuelva el encabezado Content-Length.</span><span class="sxs-lookup"><span data-stu-id="d0802-140">BITS only transfers static content and requires the HTTP server to return the Content-Length header.</span></span> <span data-ttu-id="d0802-141">Se produce un error en la solicitud de transferencia si la dirección URL señala a contenido dinámico.</span><span class="sxs-lookup"><span data-stu-id="d0802-141">The transfer request fails if the URL points to dynamic content.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>\_ \_ Compatibilidad con http insuficiente en BG E \_ \_ (0x80200012)</span><span class="sxs-lookup"><span data-stu-id="d0802-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG\_E\_INSUFFICIENT\_HTTP\_SUPPORT (0x80200012)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-143">El servidor no admite el protocolo HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="d0802-143">The server does not support the HTTP/1.1 protocol.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>\_ \_ Compatibilidad con el intervalo insuficiente de BG E \_ \_ (0x80200013)</span><span class="sxs-lookup"><span data-stu-id="d0802-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG\_E\_INSUFFICIENT\_RANGE\_SUPPORT (0x80200013)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-145">El servidor no admite el encabezado Content-Range.</span><span class="sxs-lookup"><span data-stu-id="d0802-145">The server does not support the Content-Range header.</span></span> <span data-ttu-id="d0802-146">Normalmente, recibirá este error al intentar descargar contenido dinámico.</span><span class="sxs-lookup"><span data-stu-id="d0802-146">Typically, you receive this error when you try to download dynamic content.</span></span> <span data-ttu-id="d0802-147">También puede recibir este error si un proxy intermedio está quitando el encabezado Content-Range o Content-Length.</span><span class="sxs-lookup"><span data-stu-id="d0802-147">You can also receive this error if an intermediate proxy is removing the Content-Range or Content-Length header.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG \_ E \_ Remote \_ no \_ compatible (0x80200014)</span><span class="sxs-lookup"><span data-stu-id="d0802-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG\_E\_REMOTE\_NOT\_SUPPORTED (0x80200014)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-149">No se admite el uso remoto de BITS.</span><span class="sxs-lookup"><span data-stu-id="d0802-149">Remote use of BITS is not supported.</span></span> <span data-ttu-id="d0802-150">Para obtener más información, consulte [usuarios y conexiones de red](users-and-network-connections.md).</span><span class="sxs-lookup"><span data-stu-id="d0802-150">For more information, see [Users and Network Connections](users-and-network-connections.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0802-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>\_Asignación de diferencias de nuevo propietario de BG E \_ \_ \_ \_ (0x80200015)</span><span class="sxs-lookup"><span data-stu-id="d0802-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG\_E\_NEW\_OWNER\_DIFF\_MAPPING (0x80200015)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-152">La asignación de unidad de red para el archivo local es diferente para el propietario actual que para el propietario anterior.</span><span class="sxs-lookup"><span data-stu-id="d0802-152">The network drive mapping for the local file is different for the current owner than for the previous owner.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ New \_ Owner \_ no \_ file \_ Access (0x80200016)</span><span class="sxs-lookup"><span data-stu-id="d0802-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG\_E\_NEW\_OWNER\_NO\_FILE\_ACCESS (0x80200016)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-154">El nuevo propietario no tiene permisos suficientes para los archivos de trabajo temporales.</span><span class="sxs-lookup"><span data-stu-id="d0802-154">The new owner has insufficient permissions to the temporary job files.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>Lista de proxy de BG \_ E \_ \_ \_ demasiado \_ grande (0x80200018)</span><span class="sxs-lookup"><span data-stu-id="d0802-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>BG\_E\_PROXY\_LIST\_TOO\_LARGE (0x80200018)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-156">La lista de proxy HTTP es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="d0802-156">The HTTP proxy list is too long.</span></span> <span data-ttu-id="d0802-157">La lista no debe superar los 32 KB.</span><span class="sxs-lookup"><span data-stu-id="d0802-157">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>Lista de omisión de proxy de BG \_ E \_ \_ \_ \_ demasiado \_ grande (0x80200019)</span><span class="sxs-lookup"><span data-stu-id="d0802-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG\_E\_PROXY\_BYPASS\_LIST\_TOO\_LARGE (0x80200019)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-159">La lista de omisión de proxy HTTP es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="d0802-159">The HTTP proxy bypass list is too long.</span></span> <span data-ttu-id="d0802-160">La lista no debe superar los 32 KB.</span><span class="sxs-lookup"><span data-stu-id="d0802-160">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>Rebg \_ E \_ demasiados \_ \_ archivos (0x8020001C)</span><span class="sxs-lookup"><span data-stu-id="d0802-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG\_E\_TOO\_MANY\_FILES (0x8020001C)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-162">No se puede agregar más de un archivo a un trabajo de carga.</span><span class="sxs-lookup"><span data-stu-id="d0802-162">You cannot add more than one file to an upload job.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>\_Cambio de archivo local de BG E \_ \_ \_ (0x8020001D)</span><span class="sxs-lookup"><span data-stu-id="d0802-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>BG\_E\_LOCAL\_FILE\_CHANGED (0x8020001D)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-164">El contenido del archivo local cambió después del inicio del proceso de transferencia.</span><span class="sxs-lookup"><span data-stu-id="d0802-164">The contents of the local file changed after the transfer process began.</span></span> <span data-ttu-id="d0802-165">El contenido del archivo local no puede cambiar después de que se inicie el proceso de transferencia en un trabajo de carga o de carga-respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0802-165">The contents of the local file cannot change after the transfer process begins on an upload or upload-reply job.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E \_ demasiado \_ grande (0x80200020)</span><span class="sxs-lookup"><span data-stu-id="d0802-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG\_E\_TOO\_LARGE (0x80200020)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-167">El tamaño del archivo de carga supera el tamaño de carga máximo permitido especificado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d0802-167">The size of the upload file exceeds the maximum allowed upload size specified on the server.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>Cadena de BG \_ E \_ \_ demasiado \_ larga (0x80200021)</span><span class="sxs-lookup"><span data-stu-id="d0802-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG\_E\_STRING\_TOO\_LONG (0x80200021)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-169">La cadena especificada es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="d0802-169">The specified string is too long.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>Error \_ de \_ \_ coincidencia del protocolo del servidor cliente de BG E \_ \_ (0x80200022)</span><span class="sxs-lookup"><span data-stu-id="d0802-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>BG\_E\_CLIENT\_SERVER\_PROTOCOL\_MISMATCH (0x80200022)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-171">El cliente y el servidor no pudieron negociar un protocolo para usarlo en el trabajo de carga.</span><span class="sxs-lookup"><span data-stu-id="d0802-171">The client and server were unable to negotiate a protocol to use for the upload job.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>Ejecución de BG \_ E \_ Server \_ Execute \_ Enabled (0x80200023)</span><span class="sxs-lookup"><span data-stu-id="d0802-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG\_E\_SERVER\_EXECUTE\_ENABLED (0x80200023)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-173">Los permisos de ejecución o scripting están habilitados en el directorio virtual de IIS asociado al trabajo.</span><span class="sxs-lookup"><span data-stu-id="d0802-173">Scripting or execute permissions are enabled on the IIS virtual directory associated with the job.</span></span> <span data-ttu-id="d0802-174">Para cargar archivos en el directorio virtual, deshabilite los permisos de ejecución y scripting en el directorio virtual.</span><span class="sxs-lookup"><span data-stu-id="d0802-174">To upload files to the virtual directory, disable the scripting and execute permissions on the virtual directory.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG \_ E \_ nombreDeUsuario \_ demasiado \_ grande (0x80200025)</span><span class="sxs-lookup"><span data-stu-id="d0802-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG\_E\_USERNAME\_TOO\_LARGE (0x80200025)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-176">El nombre de usuario no puede superar los 300 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d0802-176">The user name cannot exceed 300 characters.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>La \_ contraseña de BG E \_ \_ es demasiado \_ grande (0x80200026)</span><span class="sxs-lookup"><span data-stu-id="d0802-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG\_E\_PASSWORD\_TOO\_LARGE (0x80200026)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-178">La contraseña no puede superar los 65535 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d0802-178">The password cannot exceed 65535 characters.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>Destino de autenticación de BG \_ E \_ no válido \_ \_ (0x80200027)</span><span class="sxs-lookup"><span data-stu-id="d0802-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG\_E\_INVALID\_AUTH\_TARGET (0x80200027)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-180">El destino de autenticación especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="d0802-180">The specified authentication target is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>\_Esquema de \_ autenticación no válido de BG E \_ \_ (0x80200028)</span><span class="sxs-lookup"><span data-stu-id="d0802-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG\_E\_INVALID\_AUTH\_SCHEME (0x80200028)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-182">El esquema de autenticación especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="d0802-182">The specified authentication scheme is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>\_ \_ Intervalo no válido de BG E \_ (0x8020002B)</span><span class="sxs-lookup"><span data-stu-id="d0802-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG\_E\_INVALID\_RANGE (0x8020002B)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-184">El intervalo de bytes especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="d0802-184">The specified byte range is invalid.</span></span> <span data-ttu-id="d0802-185">El intervalo de bytes debe existir en el archivo remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="d0802-185">The byte range must exist within the specified remote file.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>\_ \_ Intervalos superpuestos de BG E \_ (0x8020002C)</span><span class="sxs-lookup"><span data-stu-id="d0802-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>BG\_E\_OVERLAPPING\_RANGES (0x8020002C)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-187">La lista de intervalos de bytes contiene intervalos superpuestos o duplicados, que no se admiten.</span><span class="sxs-lookup"><span data-stu-id="d0802-187">The list of byte ranges contains overlapping or duplicate ranges, which are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ bloqueada \_ por la \_ Directiva (0x8020003E)</span><span class="sxs-lookup"><span data-stu-id="d0802-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG\_E\_BLOCKED\_BY\_POLICY (0x8020003E)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-189">Directiva de grupo configuración evita que los trabajos en segundo plano se ejecuten en este momento.</span><span class="sxs-lookup"><span data-stu-id="d0802-189">Group Policy settings prevent background jobs from running at this time.</span></span> <span data-ttu-id="d0802-190">Para obtener más información, consulte la directiva [MaxInternetBandwidth](group-policies.md) .</span><span class="sxs-lookup"><span data-stu-id="d0802-190">For details, see the [MaxInternetBandwidth](group-policies.md) policy.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>\_Información de \_ proxy no válida de BG E \_ \_ (0x8020003F)</span><span class="sxs-lookup"><span data-stu-id="d0802-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG\_E\_INVALID\_PROXY\_INFO (0x8020003F)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-192">Error en tiempo de ejecución que indica la lista de proxy o la lista de omisión de proxy que especificó mediante el método [**IBackgroundCopyJob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) no es válido.</span><span class="sxs-lookup"><span data-stu-id="d0802-192">Run-time error that indicates the proxy list or proxy bypass list that you specified using the [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) method is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>\_ \_ Credenciales no válidas de BG E \_ (0x80200040)</span><span class="sxs-lookup"><span data-stu-id="d0802-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG\_E\_INVALID\_CREDENTIALS (0x80200040)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-194">El formato de las credenciales de seguridad proporcionadas no es válido.</span><span class="sxs-lookup"><span data-stu-id="d0802-194">The format of the supplied security credentials is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>Se \_ eliminó el registro de BG E \_ \_ (0x80200042)</span><span class="sxs-lookup"><span data-stu-id="d0802-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG\_E\_RECORD\_DELETED (0x80200042)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-196">Se ha eliminado el registro de caché.</span><span class="sxs-lookup"><span data-stu-id="d0802-196">The cache record has been deleted.</span></span> <span data-ttu-id="d0802-197">Se ha abandonado el intento de actualización.</span><span class="sxs-lookup"><span data-stu-id="d0802-197">The attempt to update it has been abandoned.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>ERROR de desbg \_ E \_ UPnP \_ (0x80200045)</span><span class="sxs-lookup"><span data-stu-id="d0802-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>BG\_E\_UPNP\_ERROR (0x80200045)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-199">Se ha producido un error de Plug and Play universal (UPnP).</span><span class="sxs-lookup"><span data-stu-id="d0802-199">A Universal Plug and Play (UPnP) error has occurred.</span></span> <span data-ttu-id="d0802-200">Compruebe el dispositivo de puerta de enlace a Internet.</span><span class="sxs-lookup"><span data-stu-id="d0802-200">Please check your Internet Gateway Device.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>Deshabilitación de la caché de BG \_ E \_ \_ (0x80200047)</span><span class="sxs-lookup"><span data-stu-id="d0802-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG\_E\_PEERCACHING\_DISABLED (0x80200047)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-202">El almacenamiento en caché del mismo nivel está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d0802-202">Peer-caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ BUSYCACHERECORD (0x80200048)</span><span class="sxs-lookup"><span data-stu-id="d0802-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG\_E\_BUSYCACHERECORD (0x80200048)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-204">El registro de caché está en uso y no se puede cambiar ni eliminar.</span><span class="sxs-lookup"><span data-stu-id="d0802-204">The cache record is in use and cannot be changed or deleted.</span></span> <span data-ttu-id="d0802-205">Vuelva a intentarlo después de unos segundos.</span><span class="sxs-lookup"><span data-stu-id="d0802-205">Try again after a few seconds.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ E \_ demasiados \_ \_ trabajos \_ por \_ usuario (0x80200049)</span><span class="sxs-lookup"><span data-stu-id="d0802-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_USER (0x80200049)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-207">El número de trabajos para el usuario ha superado el límite de trabajos por usuario establecido por el valor de MaxJobsPerUser directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d0802-207">The job count for the user has exceeded the per user job limit set by the MaxJobsPerUser Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ E \_ demasiados \_ \_ trabajos \_ por \_ equipo (0x80200050)</span><span class="sxs-lookup"><span data-stu-id="d0802-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_MACHINE (0x80200050)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-209">El recuento de trabajos del equipo ha superado el límite de trabajos por equipo establecido por el valor de MaxJobsPerMachine directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d0802-209">The job count for the computer has exceeded the per computer job limit set by the MaxJobsPerMachine Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ E \_ demasiados \_ \_ archivos \_ en el \_ trabajo (0x80200051)</span><span class="sxs-lookup"><span data-stu-id="d0802-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG\_E\_TOO\_MANY\_FILES\_IN\_JOB (0x80200051)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-211">El número de archivos del trabajo ha superado el límite de archivos por trabajo establecido por el valor de MaxFilesPerJob directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d0802-211">The file count for the job has exceeded the per job file limit set by the MaxFilesPerJob Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG \_ E \_ demasiados \_ \_ intervalos \_ en el \_ archivo (0x80200052)</span><span class="sxs-lookup"><span data-stu-id="d0802-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG\_E\_TOO\_MANY\_RANGES\_IN\_FILE (0x80200052)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-213">El recuento de intervalos del archivo ha superado el límite por intervalo de archivos establecido por el valor de MaxRangesPerFile directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d0802-213">The range count for the file has exceeded the per file range limit set by the MaxRangesPerFile Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>Error de validación de BG \_ E \_ \_ (0x80200053)</span><span class="sxs-lookup"><span data-stu-id="d0802-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>BG\_E\_VALIDATION\_FAILED (0x80200053)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-215">La aplicación solicitó datos de un sitio web, pero la respuesta no era válida.</span><span class="sxs-lookup"><span data-stu-id="d0802-215">The application requested data from a website, but the response was not valid.</span></span> <span data-ttu-id="d0802-216">Para obtener más información, use Visor de eventos para ver los registros de aplicación \\ Microsoft \\ Windows \\ bits- \\ registro operativo del cliente.</span><span class="sxs-lookup"><span data-stu-id="d0802-216">For details, use Event Viewer to view the Application Logs\\Microsoft\\Windows\\Bits-client\\Operational log.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>Tiempo de espera de BG \_ E \_ MAXDOWNLOAD \_ (0x80200054)</span><span class="sxs-lookup"><span data-stu-id="d0802-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG\_E\_MAXDOWNLOAD\_TIMEOUT (0x80200054)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-218">BITS agotó el tiempo de espera de descarga del trabajo.</span><span class="sxs-lookup"><span data-stu-id="d0802-218">BITS timed out downloading the job.</span></span> <span data-ttu-id="d0802-219">La descarga no se completó en el tiempo de descarga máximo establecido en el trabajo o en la configuración del directiva de grupo de MaxDownloadTime.</span><span class="sxs-lookup"><span data-stu-id="d0802-219">The download did not complete within the maximum download time set on the job or the MaxDownloadTime Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>\_Error http de BG E \_ \_ \_ 400 (0x80190190)</span><span class="sxs-lookup"><span data-stu-id="d0802-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG\_E\_HTTP\_ERROR\_400 (0x80190190)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-221">El servidor no pudo procesar la solicitud de transferencia porque la sintaxis del nombre de archivo remoto no es válida.</span><span class="sxs-lookup"><span data-stu-id="d0802-221">The server could not process the transfer request because the syntax of the remote file name is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>\_Error http de BG E \_ \_ \_ 401 (0x80190191)</span><span class="sxs-lookup"><span data-stu-id="d0802-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG\_E\_HTTP\_ERROR\_401 (0x80190191)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-223">El usuario no tiene permiso para obtener acceso al archivo remoto.</span><span class="sxs-lookup"><span data-stu-id="d0802-223">The user does not have permission to access the remote file.</span></span> <span data-ttu-id="d0802-224">El recurso solicitado requiere autenticación de usuarios.</span><span class="sxs-lookup"><span data-stu-id="d0802-224">The requested resource requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>\_Error http de BG E \_ \_ \_ 404 (0x80190194)</span><span class="sxs-lookup"><span data-stu-id="d0802-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG\_E\_HTTP\_ERROR\_404 (0x80190194)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-226">La dirección URL solicitada no existe en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d0802-226">The requested URL does not exist on the server.</span></span>

<span data-ttu-id="d0802-227">En IIS 7, este error puede indicar</span><span class="sxs-lookup"><span data-stu-id="d0802-227">In IIS 7, this error can indicate</span></span>

-   <span data-ttu-id="d0802-228">Las cargas de BITS no están habilitadas en el directorio virtual (vdir) del servidor.</span><span class="sxs-lookup"><span data-stu-id="d0802-228">That BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>
-   <span data-ttu-id="d0802-229">Que el tamaño de carga supere el límite máximo de carga (para obtener más información, consulte la propiedad extensión IIS de [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) ).</span><span class="sxs-lookup"><span data-stu-id="d0802-229">That the upload size exceeds the maximum upload limit (for details, see the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property).</span></span>

</dd> <dt>

<span data-ttu-id="d0802-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>\_Error http de BG E \_ \_ \_ 407 (0x80190197)</span><span class="sxs-lookup"><span data-stu-id="d0802-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG\_E\_HTTP\_ERROR\_407 (0x80190197)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-231">El usuario no tiene permiso para obtener acceso al proxy.</span><span class="sxs-lookup"><span data-stu-id="d0802-231">The user does not have permission to access the proxy.</span></span> <span data-ttu-id="d0802-232">El proxy requiere autenticación de usuario.</span><span class="sxs-lookup"><span data-stu-id="d0802-232">The proxy requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>\_Error http de BG E \_ \_ \_ 414 (0x8019019E)</span><span class="sxs-lookup"><span data-stu-id="d0802-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG\_E\_HTTP\_ERROR\_414 (0x8019019E)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-234">El servidor no puede procesar la solicitud de transferencia.</span><span class="sxs-lookup"><span data-stu-id="d0802-234">The server cannot process the transfer request.</span></span> <span data-ttu-id="d0802-235">El identificador uniforme de recursos (URI) en el nombre de archivo remoto es más largo que el que el servidor puede interpretar.</span><span class="sxs-lookup"><span data-stu-id="d0802-235">The Uniform Resource Identifier (URI) in the remote file name is longer than the server can interpret.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>\_Error http de BG E \_ \_ \_ 501 (0x801901F5)</span><span class="sxs-lookup"><span data-stu-id="d0802-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG\_E\_HTTP\_ERROR\_501 (0x801901F5)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-237">El servidor no admite la funcionalidad necesaria para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0802-237">The server does not support the functionality required to fulfill the request.</span></span> <span data-ttu-id="d0802-238">En IIS 6, este error indica que las cargas de BITS no están habilitadas en el directorio virtual (vdir) del servidor.</span><span class="sxs-lookup"><span data-stu-id="d0802-238">In IIS 6, this error indicates that BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>\_Error http de BG E \_ \_ \_ 503 (0x801901F7)</span><span class="sxs-lookup"><span data-stu-id="d0802-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG\_E\_HTTP\_ERROR\_503 (0x801901F7)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-240">El servicio está sobrecargado temporalmente y no puede procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0802-240">The service is temporarily overloaded and cannot process the request.</span></span> <span data-ttu-id="d0802-241">Reanude el trabajo más tarde.</span><span class="sxs-lookup"><span data-stu-id="d0802-241">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>\_Error http de BG E \_ \_ \_ 504 (0x801901F8)</span><span class="sxs-lookup"><span data-stu-id="d0802-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG\_E\_HTTP\_ERROR\_504 (0x801901F8)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-243">Se agotó el tiempo de espera de la solicitud de transferencia mientras se esperaba una puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="d0802-243">The transfer request timed out while waiting for a gateway.</span></span> <span data-ttu-id="d0802-244">Reanude el trabajo más tarde.</span><span class="sxs-lookup"><span data-stu-id="d0802-244">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="d0802-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>\_Error http de BG E \_ \_ \_ 505 (0x801901F9)</span><span class="sxs-lookup"><span data-stu-id="d0802-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG\_E\_HTTP\_ERROR\_505 (0x801901F9)</span></span>
</dt> <dd>

<span data-ttu-id="d0802-246">El servidor no admite la versión del protocolo HTTP especificada en el nombre de archivo remoto.</span><span class="sxs-lookup"><span data-stu-id="d0802-246">The server does not support the HTTP protocol version specified in the remote file name.</span></span>

</dd> </dl>

<span data-ttu-id="d0802-247">El archivo de encabezado Bitsmsg. h contiene valores devueltos HTTP adicionales que no se enumeran antes que BITS usa internamente.</span><span class="sxs-lookup"><span data-stu-id="d0802-247">The Bitsmsg.h header file contains additional HTTP return values not listed above that BITS uses internally.</span></span> <span data-ttu-id="d0802-248">Para obtener información sobre estos y otros valores devueltos de HTTP que puede recibir, consulte la especificación RFC 2616 de Internet Engineering Task Force en [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .</span><span class="sxs-lookup"><span data-stu-id="d0802-248">For information on these and other HTTP return values you can receive, see the RFC 2616 specification from the Internet Engineering Task Force at [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10).</span></span>

 

 