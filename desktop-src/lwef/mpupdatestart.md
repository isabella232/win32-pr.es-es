---
title: Función MpUpdateStart (MpClient. h)
description: Inicia una operación de actualización de firma.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- Función MpUpdateStart características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39867525529339c6b354ae771b070589ca52acfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492628"
---
# <a name="mpupdatestart-function"></a><span data-ttu-id="67f0d-104">MpUpdateStart función)</span><span class="sxs-lookup"><span data-stu-id="67f0d-104">MpUpdateStart function</span></span>

<span data-ttu-id="67f0d-105">Inicia una operación de actualización de firma.</span><span class="sxs-lookup"><span data-stu-id="67f0d-105">Starts a signature update operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="67f0d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67f0d-106">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a><span data-ttu-id="67f0d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67f0d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67f0d-108">*hMpHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="67f0d-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67f0d-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="67f0d-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="67f0d-110">Identificador de la interfaz del administrador de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="67f0d-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="67f0d-111">La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="67f0d-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="67f0d-112">*dwUpdateOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="67f0d-112">*dwUpdateOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67f0d-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="67f0d-113">Type: **DWORD**</span></span>

<span data-ttu-id="67f0d-114">Especifica la opción para la operación de actualización de la firma.</span><span class="sxs-lookup"><span data-stu-id="67f0d-114">Specifies the option for the signature update operation.</span></span> <span data-ttu-id="67f0d-115">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="67f0d-115">It can be one of the following values:</span></span>



| <span data-ttu-id="67f0d-116">Value</span><span class="sxs-lookup"><span data-stu-id="67f0d-116">Value</span></span>                                                                                                                                                                                              | <span data-ttu-id="67f0d-117">Significado</span><span class="sxs-lookup"><span data-stu-id="67f0d-117">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <span data-ttu-id="67f0d-118"><dt>**opción de MPUPDATE \_ \_ ninguna**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-118"><dt>**MPUPDATE\_OPTION\_NONE**</dt></span></span> </dl>                | <span data-ttu-id="67f0d-119">No se solicita ninguna opción específica.</span><span class="sxs-lookup"><span data-stu-id="67f0d-119">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <span data-ttu-id="67f0d-120"><dt>**\_opción MPUPDATE \_ Async**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-120"><dt>**MPUPDATE\_OPTION\_ASYNC**</dt></span></span> </dl>             | <span data-ttu-id="67f0d-121">La operación de actualización es asincrónica, donde **MpUpdateStart** vuelve inmediatamente después de que se iniciase correctamente la actualización de la firma.</span><span class="sxs-lookup"><span data-stu-id="67f0d-121">The update operation is to be asynchronous, where **MpUpdateStart** returns immediately after the successful initiation of the signature update.</span></span> <span data-ttu-id="67f0d-122">(De forma predeterminada, la operación de actualización es sincrónica, lo que significa que **MpUpdateStart** solo devolverá una vez finalizada la actualización de la firma).</span><span class="sxs-lookup"><span data-stu-id="67f0d-122">(By default the update operation is synchronous, meaning **MpUpdateStart** will return only after the signature update is finished.)</span></span><br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <span data-ttu-id="67f0d-123"><dt>**progreso de la \_ opción MPUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-123"><dt>**MPUPDATE\_OPTION\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="67f0d-124">El autor de la llamada está interesado en recibir información de progreso de actualización de firmas a través de una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="67f0d-124">The caller is interested in receiving signature update progress information via a callback.</span></span><br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <span data-ttu-id="67f0d-125"><dt>**\_opción MPUPDATE \_ http**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-125"><dt>**MPUPDATE\_OPTION\_HTTP**</dt></span></span> </dl>                | <span data-ttu-id="67f0d-126">La actualización de la firma se realiza mediante la descarga del paquete de firmas completo desde el sitio del portal de seguridad de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="67f0d-126">The signature update is performed by downloading the full signature package from the Microsoft security portal site.</span></span> <span data-ttu-id="67f0d-127">Se puede usar como opción de reserva si el cliente tiene un problema de descarga de la firma a través de Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="67f0d-127">This can be used as a fallback option if the client is experiencing a signature download problem via Microsoft Update.</span></span><br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <span data-ttu-id="67f0d-128"><dt>**MPUPDATE \_ , opción \_ UNC**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-128"><dt>**MPUPDATE\_OPTION\_UNC**</dt></span></span> </dl>                   | <span data-ttu-id="67f0d-129">Realiza una actualización de firmas mediante la descarga directa desde recursos compartidos UNC.</span><span class="sxs-lookup"><span data-stu-id="67f0d-129">Performs signature update using direct download from UNC shares.</span></span><br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <span data-ttu-id="67f0d-130"><dt>**\_opción MPUPDATE \_ administrada**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-130"><dt>**MPUPDATE\_OPTION\_MANAGED**</dt></span></span> </dl>       | <span data-ttu-id="67f0d-131">Realiza una actualización de firmas mediante el servicio administrado WSUS.</span><span class="sxs-lookup"><span data-stu-id="67f0d-131">Performs signature update using the Managed Service WSUS.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <span data-ttu-id="67f0d-132"><dt>**\_opción MPUPDATE \_ no administrada**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-132"><dt>**MPUPDATE\_OPTION\_UNMANAGED**</dt></span></span> </dl> | <span data-ttu-id="67f0d-133">Realiza una actualización de firmas mediante el servicio no administrado MU/WU.</span><span class="sxs-lookup"><span data-stu-id="67f0d-133">Performs signature update using the Unmanaged Service MU/WU.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="67f0d-134">*pCallbackInfo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="67f0d-134">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="67f0d-135">Tipo: **PMPCALLBACK \_ info**</span><span class="sxs-lookup"><span data-stu-id="67f0d-135">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="67f0d-136">Un puntero a la información de devolución de llamada que se usa para suministrar al cliente los cambios de estado de actualización de firma (como inicio y finalización) y la información de progreso.</span><span class="sxs-lookup"><span data-stu-id="67f0d-136">A pointer to the callback information used to feed the client with signature update state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="67f0d-137">Los [**\_ datos de MPCALLBACK**](mpcallback-data.md) que se devuelven en la función de devolución de llamada notifican el estado de actualización real y la información relacionada con el progreso.</span><span class="sxs-lookup"><span data-stu-id="67f0d-137">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual update state and progress-related information.</span></span> <span data-ttu-id="67f0d-138">A continuación se muestra una lista de posibles devoluciones de llamada:</span><span class="sxs-lookup"><span data-stu-id="67f0d-138">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="67f0d-139">Value</span><span class="sxs-lookup"><span data-stu-id="67f0d-139">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="67f0d-140">Significado</span><span class="sxs-lookup"><span data-stu-id="67f0d-140">Meaning</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <span data-ttu-id="67f0d-141"><dt>**Inicio de MPNOTIFY \_ SIGUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-141"><dt>**MPNOTIFY\_SIGUPDATE\_START**</dt></span></span> </dl>                                      | <span data-ttu-id="67f0d-142">Operación de actualización iniciada.</span><span class="sxs-lookup"><span data-stu-id="67f0d-142">Update operation started.</span></span><br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <span data-ttu-id="67f0d-143"><dt>**MPNOTIFY \_ SIGUPDATE \_ completado**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-143"><dt>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</dt></span></span> </dl>                             | <span data-ttu-id="67f0d-144">Operación de actualización completada.</span><span class="sxs-lookup"><span data-stu-id="67f0d-144">Update operation completed.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <span data-ttu-id="67f0d-145"><dt>**Inicio de la búsqueda de MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-145"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</dt></span></span> </dl>                | <span data-ttu-id="67f0d-146">Buscar actualizaciones iniciadas.</span><span class="sxs-lookup"><span data-stu-id="67f0d-146">Search for updates started.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <span data-ttu-id="67f0d-147"><dt>**MPNOTIFY \_ SIGUPDATE \_ Search \_ completado**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-147"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</dt></span></span> </dl>       | <span data-ttu-id="67f0d-148">Buscar actualizaciones completadas.</span><span class="sxs-lookup"><span data-stu-id="67f0d-148">Search for updates completed.</span></span> <span data-ttu-id="67f0d-149">Hay información adicional disponible a través de la estructura de [**\_ datos MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="67f0d-149">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <span data-ttu-id="67f0d-150"><dt>**Inicio de la descarga de MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-150"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</dt></span></span> </dl>          | <span data-ttu-id="67f0d-151">Descarga de la actualización iniciada.</span><span class="sxs-lookup"><span data-stu-id="67f0d-151">Download for update started.</span></span><br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <span data-ttu-id="67f0d-152"><dt>**progreso de descarga de MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-152"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</dt></span></span> </dl> | <span data-ttu-id="67f0d-153">Descargar información de progreso.</span><span class="sxs-lookup"><span data-stu-id="67f0d-153">Download progress information.</span></span> <span data-ttu-id="67f0d-154">Hay información adicional disponible a través de la estructura de [**\_ datos MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="67f0d-154">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <span data-ttu-id="67f0d-155"><dt>**descarga de MPNOTIFY \_ SIGUPDATE \_ \_ completado**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-155"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</dt></span></span> </dl> | <span data-ttu-id="67f0d-156">Descarga para completar la actualización.</span><span class="sxs-lookup"><span data-stu-id="67f0d-156">Download for update complete.</span></span> <span data-ttu-id="67f0d-157">Hay información adicional disponible a través de la estructura de [**\_ datos MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="67f0d-157">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <span data-ttu-id="67f0d-158"><dt>**Inicio de la instalación de MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-158"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</dt></span></span> </dl>             | <span data-ttu-id="67f0d-159">Se inició la instalación de la actualización.</span><span class="sxs-lookup"><span data-stu-id="67f0d-159">Installation of update started.</span></span><br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <span data-ttu-id="67f0d-160"><dt>**progreso de la instalación de MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-160"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="67f0d-161">Información sobre el progreso de la instalación.</span><span class="sxs-lookup"><span data-stu-id="67f0d-161">Installation progress information.</span></span> <span data-ttu-id="67f0d-162">Hay información adicional disponible a través de la estructura de [**\_ datos MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="67f0d-162">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <span data-ttu-id="67f0d-163"><dt>**instalación de MPNOTIFY \_ SIGUPDATE \_ \_ completado**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-163"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</dt></span></span> </dl>    | <span data-ttu-id="67f0d-164">Se completó la instalación de la actualización.</span><span class="sxs-lookup"><span data-stu-id="67f0d-164">Installation of update completed.</span></span> <span data-ttu-id="67f0d-165">Hay información adicional disponible a través de la estructura de [**\_ datos MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="67f0d-165">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <span data-ttu-id="67f0d-166"><dt>**solicitud de MPNOTIFY \_ SIGUPDATE \_ \_ procesada**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-166"><dt>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</dt></span></span> </dl> | <span data-ttu-id="67f0d-167">El servicio antimalware procesó una solicitud de actualización de firma.</span><span class="sxs-lookup"><span data-stu-id="67f0d-167">The antimalware service processed a signature update request.</span></span> <span data-ttu-id="67f0d-168">El error o el éxito se indica mediante *hResult* en los [**\_ datos de MPCALLBACK**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="67f0d-168">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <span data-ttu-id="67f0d-169"><dt>**se \_ \_ requiere un reinicio de MPNOTIFY SIGUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-169"><dt>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</dt></span></span> </dl>       | <span data-ttu-id="67f0d-170">Requiere un reinicio para completar la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="67f0d-170">Requires reboot to complete the update operation.</span></span> <span data-ttu-id="67f0d-171">El error o el éxito se indica mediante *hResult* en los [**\_ datos de MPCALLBACK**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="67f0d-171">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="67f0d-172"><dt>**\_error interno de MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-172"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>                                   | <span data-ttu-id="67f0d-173">La operación de actualización de firma ha encontrado un error genérico.</span><span class="sxs-lookup"><span data-stu-id="67f0d-173">Signature update operation has encountered a generic failure.</span></span> <span data-ttu-id="67f0d-174">El *hResult* en [**los \_ datos de MPCALLBACK**](mpcallback-data.md) tiene el código de error específico.</span><span class="sxs-lookup"><span data-stu-id="67f0d-174">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="67f0d-175">*phUpdateHandle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="67f0d-175">*phUpdateHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67f0d-176">Tipo: **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="67f0d-176">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="67f0d-177">Identificador de actualización devuelto que identifica la operación de actualización de firmas iniciada actualmente.</span><span class="sxs-lookup"><span data-stu-id="67f0d-177">Returned update handle which identifies the currently initiated signature update operation.</span></span> <span data-ttu-id="67f0d-178">Este identificador se puede usar en las llamadas de función subsiguientes, como para controlar la operación de actualización de la firma.</span><span class="sxs-lookup"><span data-stu-id="67f0d-178">This handle can be used in subsequent function calls, such as to control the signature update operation.</span></span> <span data-ttu-id="67f0d-179">El identificador debe cerrarse con la función [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="67f0d-179">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67f0d-180">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67f0d-180">Return value</span></span>

<span data-ttu-id="67f0d-181">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="67f0d-181">Type: **HRESULT**</span></span>

<span data-ttu-id="67f0d-182">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="67f0d-182">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="67f0d-183">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="67f0d-183">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="67f0d-184">El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="67f0d-184">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="67f0d-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67f0d-185">Requirements</span></span>



| <span data-ttu-id="67f0d-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="67f0d-186">Requirement</span></span> | <span data-ttu-id="67f0d-187">Value</span><span class="sxs-lookup"><span data-stu-id="67f0d-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67f0d-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67f0d-188">Minimum supported client</span></span><br/> | <span data-ttu-id="67f0d-189">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="67f0d-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="67f0d-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67f0d-190">Minimum supported server</span></span><br/> | <span data-ttu-id="67f0d-191">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="67f0d-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67f0d-192">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67f0d-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="67f0d-193"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-193"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="67f0d-194">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67f0d-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67f0d-195"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67f0d-195"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67f0d-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="67f0d-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67f0d-197">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="67f0d-197">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="67f0d-198">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="67f0d-198">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="67f0d-199">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="67f0d-199">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="67f0d-200">**datos de MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="67f0d-200">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="67f0d-201">**datos de MPSIGUPDATE \_**</span><span class="sxs-lookup"><span data-stu-id="67f0d-201">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> </dl>

 

 





