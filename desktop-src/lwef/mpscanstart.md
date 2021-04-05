---
title: Función MpScanStart (MpClient. h)
description: Inicia una operación de digitalización.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- Función MpScanStart características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d343787edc85a18dc7471d19165999a7252d18a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996659"
---
# <a name="mpscanstart-function"></a><span data-ttu-id="b129d-104">MpScanStart función)</span><span class="sxs-lookup"><span data-stu-id="b129d-104">MpScanStart function</span></span>

<span data-ttu-id="b129d-105">Inicia una operación de digitalización.</span><span class="sxs-lookup"><span data-stu-id="b129d-105">Starts a scanning operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b129d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b129d-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a><span data-ttu-id="b129d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b129d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b129d-108">*hMpHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b129d-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b129d-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="b129d-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="b129d-110">Identificador de la interfaz del administrador de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="b129d-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="b129d-111">La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="b129d-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b129d-112">*ScanType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b129d-112">*ScanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b129d-113">Tipo: **[ **MPSCAN \_ Type**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="b129d-113">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

<span data-ttu-id="b129d-114">Especifica el tipo de examen.</span><span class="sxs-lookup"><span data-stu-id="b129d-114">Specifies the type of scan.</span></span> <span data-ttu-id="b129d-115">Este parámetro debe ser uno de los miembros del [**\_ tipo MPSCAN**](mpscan-type.md) enueration.</span><span class="sxs-lookup"><span data-stu-id="b129d-115">This parameter must be one of the members of the [**MPSCAN\_TYPE**](mpscan-type.md) enueration.</span></span>

</dd> <dt>

<span data-ttu-id="b129d-116">*dwScanOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b129d-116">*dwScanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b129d-117">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b129d-117">Type: **DWORD**</span></span>

<span data-ttu-id="b129d-118">Especifica varias opciones para la operación de examen.</span><span class="sxs-lookup"><span data-stu-id="b129d-118">Specifies various options for scanning operation.</span></span>



| <span data-ttu-id="b129d-119">Value</span><span class="sxs-lookup"><span data-stu-id="b129d-119">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="b129d-120">Significado</span><span class="sxs-lookup"><span data-stu-id="b129d-120">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <span data-ttu-id="b129d-121"><dt>**opción de MPSCAN \_ \_ ninguna**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-121"><dt>**MPSCAN\_OPTION\_NONE**</dt></span></span> </dl>                               | <span data-ttu-id="b129d-122">No se solicita ninguna opción específica.</span><span class="sxs-lookup"><span data-stu-id="b129d-122">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <span data-ttu-id="b129d-123"><dt>**\_opción MPSCAN \_ Async**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-123"><dt>**MPSCAN\_OPTION\_ASYNC**</dt></span></span> </dl>                            | <span data-ttu-id="b129d-124">La operación de examen es asincrónica, donde **MpScanStart** vuelve inmediatamente después del inicio correcto del examen.</span><span class="sxs-lookup"><span data-stu-id="b129d-124">The scan operation is to be asynchronous, where **MpScanStart** returns immediately after the successful initiation of scanning.</span></span> <span data-ttu-id="b129d-125">(De forma predeterminada, la operación de examen es sincrónica, lo que significa que **MpScanStart** solo devolverá una vez finalizada la exploración).</span><span class="sxs-lookup"><span data-stu-id="b129d-125">(By default the scan operation is synchronous, meaning **MpScanStart** will return only after the scan is finished.)</span></span><br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <span data-ttu-id="b129d-126"><dt>**progreso de la \_ opción MPSCAN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-126"><dt>**MPSCAN\_OPTION\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="b129d-127">El autor de la llamada está interesado en recibir información de progreso del examen a través de una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b129d-127">The caller is interested in receiving scan progress information via a callback.</span></span><br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <span data-ttu-id="b129d-128"><dt>**MPSCAN \_ opción \_ LOWPRIORITY**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-128"><dt>**MPSCAN\_OPTION\_LOWPRIORITY**</dt></span></span> </dl>          | <span data-ttu-id="b129d-129">Realice el examen con prioridad baja.</span><span class="sxs-lookup"><span data-stu-id="b129d-129">Perform the scan with low priority.</span></span> <span data-ttu-id="b129d-130">(De forma predeterminada, la operación de examen se realiza con prioridad normal).</span><span class="sxs-lookup"><span data-stu-id="b129d-130">(By default the scan operation is performed with normal priority.)</span></span><br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <span data-ttu-id="b129d-131"><dt>**MPSCAN \_ opción \_ PACKEDEXES**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-131"><dt>**MPSCAN\_OPTION\_PACKEDEXES**</dt></span></span> </dl>             | <span data-ttu-id="b129d-132">Examinar los ejecutables empaquetados en busca de posibles amenazas.</span><span class="sxs-lookup"><span data-stu-id="b129d-132">Scan packed executables for possible threats.</span></span><br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <span data-ttu-id="b129d-133"><dt>**\_archivos de opciones de MPSCAN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-133"><dt>**MPSCAN\_OPTION\_ARCHIVES**</dt></span></span> </dl>                   | <span data-ttu-id="b129d-134">Examinar el contenido del archivo en busca de posibles amenazas.</span><span class="sxs-lookup"><span data-stu-id="b129d-134">Scan archive contents for possible threats.</span></span> <span data-ttu-id="b129d-135">Los archivos son archivos con extensiones como. zip,. cab o. tar.</span><span class="sxs-lookup"><span data-stu-id="b129d-135">Archives are files with extensions such as .zip, .cab, or .tar.</span></span><br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <span data-ttu-id="b129d-136"><dt>**heurística de la \_ opción MPSCAN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-136"><dt>**MPSCAN\_OPTION\_HEURISTICS**</dt></span></span> </dl>             | <span data-ttu-id="b129d-137">Habilitar el examen basado en la heurística.</span><span class="sxs-lookup"><span data-stu-id="b129d-137">Enable heuristics-based scanning.</span></span> <span data-ttu-id="b129d-138">Se buscarán amenazas con el tipo de detección establecido en heurística.</span><span class="sxs-lookup"><span data-stu-id="b129d-138">This will scan for threats with detection type set to heuristics.</span></span><br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <span data-ttu-id="b129d-139"><dt>**MPSCAN \_ opción \_ REPORTFRIENDLY**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-139"><dt>**MPSCAN\_OPTION\_REPORTFRIENDLY**</dt></span></span> </dl> | <span data-ttu-id="b129d-140">Notificar elementos descriptivos en un examen de recursos.</span><span class="sxs-lookup"><span data-stu-id="b129d-140">Report friendly items in a resource scan.</span></span> <span data-ttu-id="b129d-141">Solo está pensado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="b129d-141">This is intended for internal use only.</span></span><br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <span data-ttu-id="b129d-142"><dt>**MPSCAN \_ opción \_ REPORTUNKNOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-142"><dt>**MPSCAN\_OPTION\_REPORTUNKNOWN**</dt></span></span> </dl>    | <span data-ttu-id="b129d-143">Notificar elementos desconocidos en un examen de recursos.</span><span class="sxs-lookup"><span data-stu-id="b129d-143">Report unknown items in a resource scan.</span></span> <span data-ttu-id="b129d-144">Solo está pensado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="b129d-144">This is intended for internal use only.</span></span><br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <span data-ttu-id="b129d-145"><dt>**\_opción MPSCAN \_ noconsolidate**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-145"><dt>**MPSCAN\_OPTION\_NOCONSOLIDATE**</dt></span></span> </dl>    | <span data-ttu-id="b129d-146">No consolide los resultados de los exámenes con la vista de amenazas global.</span><span class="sxs-lookup"><span data-stu-id="b129d-146">Do not consolidate scan results with global threat view.</span></span> <span data-ttu-id="b129d-147">Esto resulta útil para un cliente (por ejemplo, un cliente de correo electrónico) que desee controlar la experiencia de usuario de limpieza por sí misma en lugar de permitir la limpieza antimalware predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b129d-147">This is useful for a client (such as an email client) which wants to control cleaning UX by itself rather than allowing default anti-malware cleaning UX.</span></span> <span data-ttu-id="b129d-148">Solo está pensado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="b129d-148">This is intended for internal use only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b129d-149">*pScanResources* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b129d-149">*pScanResources* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b129d-150">Tipo: **\_ recursos PMPSCAN**</span><span class="sxs-lookup"><span data-stu-id="b129d-150">Type: **PMPSCAN\_RESOURCES**</span></span>

<span data-ttu-id="b129d-151">Puntero a la información de recurso de examen.</span><span class="sxs-lookup"><span data-stu-id="b129d-151">A pointer to the scan resource information.</span></span> <span data-ttu-id="b129d-152">Este parámetro debe ser **null** para un examen rápido.</span><span class="sxs-lookup"><span data-stu-id="b129d-152">This parameter must be **NULL** for a quick scan.</span></span> <span data-ttu-id="b129d-153">Se trata de un parámetro opcional para un examen completo.</span><span class="sxs-lookup"><span data-stu-id="b129d-153">This is an optional parameter for a full scan.</span></span> <span data-ttu-id="b129d-154">Para un examen de recursos, este parámetro debe especificarse con al menos una estructura de información de recursos.</span><span class="sxs-lookup"><span data-stu-id="b129d-154">For a resource scan this parameter must be specified with at least one resource information structure.</span></span> <span data-ttu-id="b129d-155">Para examinar recursos específicos, el llamador debe tener permiso de **\_ lectura genérico** para el recurso.</span><span class="sxs-lookup"><span data-stu-id="b129d-155">To scan specific resources the caller must have **GENERIC\_READ** permission for the resource.</span></span> <span data-ttu-id="b129d-156">Vea [**\_ recursos de MPSCAN**](mpscan-resources.md).</span><span class="sxs-lookup"><span data-stu-id="b129d-156">See [**MPSCAN\_RESOURCES**](mpscan-resources.md).</span></span>

</dd> <dt>

<span data-ttu-id="b129d-157">*pCallbackInfo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b129d-157">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b129d-158">Tipo: **PMPCALLBACK \_ info**</span><span class="sxs-lookup"><span data-stu-id="b129d-158">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="b129d-159">Un puntero a la información de devolución de llamada que se usa para alimentar al cliente con los cambios de estado de exploración (como inicio y finalización) y la información de progreso.</span><span class="sxs-lookup"><span data-stu-id="b129d-159">A pointer to the callback information used to feed the client with scan state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="b129d-160">Los [**\_ datos de MPCALLBACK**](mpcallback-data.md) que se devuelven en la función de devolución de llamada notifican el estado de examen real y la información relacionada con el progreso.</span><span class="sxs-lookup"><span data-stu-id="b129d-160">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual scan state and progress-related information.</span></span> <span data-ttu-id="b129d-161">A continuación se muestra una lista de posibles devoluciones de llamada:</span><span class="sxs-lookup"><span data-stu-id="b129d-161">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="b129d-162">Value</span><span class="sxs-lookup"><span data-stu-id="b129d-162">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="b129d-163">Significado</span><span class="sxs-lookup"><span data-stu-id="b129d-163">Meaning</span></span>                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <span data-ttu-id="b129d-164"><dt>**\_Inicio de examen de MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-164"><dt>**MPNOTIFY\_SCAN\_START**</dt></span></span> </dl>                            | <span data-ttu-id="b129d-165">Operación de examen iniciada.</span><span class="sxs-lookup"><span data-stu-id="b129d-165">Scan operation started.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <span data-ttu-id="b129d-166"><dt>**examen de MPNOTIFY \_ \_ completado**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-166"><dt>**MPNOTIFY\_SCAN\_COMPLETE**</dt></span></span> </dl>                   | <span data-ttu-id="b129d-167">Operación de examen completada.</span><span class="sxs-lookup"><span data-stu-id="b129d-167">Scan operation completed.</span></span> <span data-ttu-id="b129d-168">Hay información adicional disponible a través de la estructura de [**\_ datos MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="b129d-168">Additional information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <span data-ttu-id="b129d-169"><dt>**examen de MPNOTIFY en \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-169"><dt>**MPNOTIFY\_SCAN\_PAUSED**</dt></span></span> </dl>                         | <span data-ttu-id="b129d-170">La operación de examen está en pausa.</span><span class="sxs-lookup"><span data-stu-id="b129d-170">Scan operation is paused.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <span data-ttu-id="b129d-171"><dt>**examen de MPNOTIFY \_ \_ reanudado**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-171"><dt>**MPNOTIFY\_SCAN\_RESUMED**</dt></span></span> </dl>                      | <span data-ttu-id="b129d-172">La operación de examen se reanudó de la pausa.</span><span class="sxs-lookup"><span data-stu-id="b129d-172">Scan operation resumed from pause.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <span data-ttu-id="b129d-173"><dt>**\_Cancelar examen de MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-173"><dt>**MPNOTIFY\_SCAN\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="b129d-174">Se canceló la operación de examen.</span><span class="sxs-lookup"><span data-stu-id="b129d-174">Scan operation was cancelled.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <span data-ttu-id="b129d-175"><dt>**\_progreso del examen de MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-175"><dt>**MPNOTIFY\_SCAN\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="b129d-176">Información de progreso de la exploración.</span><span class="sxs-lookup"><span data-stu-id="b129d-176">Scan progress information.</span></span> <span data-ttu-id="b129d-177">La información adicional (como las estadísticas de recursos) está disponible a través de la estructura de [**\_ datos MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="b129d-177">Additional information (such as resource statistics) is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <span data-ttu-id="b129d-178"><dt>**\_error de examen de MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-178"><dt>**MPNOTIFY\_SCAN\_ERROR**</dt></span></span> </dl>                            | <span data-ttu-id="b129d-179">Examinar la información de error de un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="b129d-179">Scan error information for a specific resource.</span></span> <span data-ttu-id="b129d-180">La información de recursos específica está disponible a través de la estructura de [**\_ datos MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="b129d-180">The specific resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <span data-ttu-id="b129d-181"><dt>**examen de MPNOTIFY \_ \_ infectado**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-181"><dt>**MPNOTIFY\_SCAN\_INFECTED**</dt></span></span> </dl>                   | <span data-ttu-id="b129d-182">El examen encontró un recurso infectado.</span><span class="sxs-lookup"><span data-stu-id="b129d-182">Scan found an infected resource.</span></span> <span data-ttu-id="b129d-183">Tenga en cuenta que, en la mayoría de los casos, esto dará lugar a la notificación de alguna amenaza al final del examen.</span><span class="sxs-lookup"><span data-stu-id="b129d-183">Note that in most of the cases this will result in some threat reported at the end of the scan.</span></span> <span data-ttu-id="b129d-184">En ocasiones, es posible que no se materializa como amenaza debido a las exclusiones.</span><span class="sxs-lookup"><span data-stu-id="b129d-184">Sometimes it may not materialize as a threat because of exclusions.</span></span> <span data-ttu-id="b129d-185">La información adicional sobre los recursos infectados está disponible a través de la estructura de [**\_ datos MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="b129d-185">Additional infected resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <span data-ttu-id="b129d-186"><dt>**MPNOTIFY \_ scan \_ MEMORYSTART**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-186"><dt>**MPNOTIFY\_SCAN\_MEMORYSTART**</dt></span></span> </dl>          | <span data-ttu-id="b129d-187">Se ha iniciado la parte de examen rápido del examen completo.</span><span class="sxs-lookup"><span data-stu-id="b129d-187">Quick scan portion of the full scan has started.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <span data-ttu-id="b129d-188"><dt>**MPNOTIFY \_ scan \_ MEMORYCOMPLETE**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-188"><dt>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="b129d-189">Se ha completado la parte de examen rápido del examen completo.</span><span class="sxs-lookup"><span data-stu-id="b129d-189">Quick scan portion of the full scan has completed.</span></span><br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="b129d-190"><dt>**\_error interno de MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-190"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>          | <span data-ttu-id="b129d-191">La operación de examen ha encontrado un error genérico.</span><span class="sxs-lookup"><span data-stu-id="b129d-191">Scan operation has encountered a generic failure.</span></span> <span data-ttu-id="b129d-192">El *hResult* en [**los \_ datos de MPCALLBACK**](mpcallback-data.md) tiene el código de error específico.</span><span class="sxs-lookup"><span data-stu-id="b129d-192">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="b129d-193">*phScanHandle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b129d-193">*phScanHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b129d-194">Tipo: **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="b129d-194">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="b129d-195">Identificador de examen devuelto que identifica el examen iniciado actualmente.</span><span class="sxs-lookup"><span data-stu-id="b129d-195">Returned scan handle which identifies the currently initiated scan.</span></span> <span data-ttu-id="b129d-196">Este identificador se puede usar en las llamadas de función subsiguientes, como para recuperar el resultado de un examen.</span><span class="sxs-lookup"><span data-stu-id="b129d-196">This handle can be used in subsequent function calls, such as to retrieve a scan result.</span></span> <span data-ttu-id="b129d-197">El identificador debe cerrarse con la función [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="b129d-197">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b129d-198">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b129d-198">Return value</span></span>

<span data-ttu-id="b129d-199">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b129d-199">Type: **HRESULT**</span></span>

<span data-ttu-id="b129d-200">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b129d-200">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="b129d-201">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="b129d-201">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="b129d-202">El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="b129d-202">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b129d-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b129d-203">Requirements</span></span>



| <span data-ttu-id="b129d-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="b129d-204">Requirement</span></span> | <span data-ttu-id="b129d-205">Value</span><span class="sxs-lookup"><span data-stu-id="b129d-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b129d-206">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b129d-206">Minimum supported client</span></span><br/> | <span data-ttu-id="b129d-207">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b129d-207">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b129d-208">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b129d-208">Minimum supported server</span></span><br/> | <span data-ttu-id="b129d-209">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b129d-209">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b129d-210">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b129d-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="b129d-211"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-211"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b129d-212">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b129d-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b129d-213"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b129d-213"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b129d-214">Vea también</span><span class="sxs-lookup"><span data-stu-id="b129d-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b129d-215">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="b129d-215">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="b129d-216">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="b129d-216">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="b129d-217">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="b129d-217">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="b129d-218">**datos de MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="b129d-218">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="b129d-219">**datos de MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="b129d-219">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="b129d-220">**recursos de MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="b129d-220">**MPSCAN\_RESOURCES**</span></span>](mpscan-resources.md)
</dt> <dt>

[<span data-ttu-id="b129d-221">**\_tipo MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="b129d-221">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> </dl>

 

 





