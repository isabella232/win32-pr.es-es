---
title: Flujo de trabajo del adaptador
description: En esta sección se describe el flujo de trabajo de inscripción desde la perspectiva de los complementos de adaptador.
ms.assetid: 0392124A-78CF-49E3-A52A-1E2E3A100E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68f93146e1d6cedd42094876547bfe0c945d6a7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665717"
---
# <a name="adapter-workflow"></a><span data-ttu-id="18799-103">Flujo de trabajo del adaptador</span><span class="sxs-lookup"><span data-stu-id="18799-103">Adapter Workflow</span></span>

<span data-ttu-id="18799-104">En esta sección se describe el flujo de trabajo de inscripción desde la perspectiva de los complementos de adaptador.</span><span class="sxs-lookup"><span data-stu-id="18799-104">This section describes the enrollment workflow from the perspective of the adapter plugins.</span></span>

<span data-ttu-id="18799-105">En Windows 10, hemos implementado una interfaz de motor V4 que proporciona dos nuevas funciones de adaptador de motor, [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) y [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn).</span><span class="sxs-lookup"><span data-stu-id="18799-105">In Windows 10, we ve implemented a V4 engine interface that provides 2 new engine adapter functions, [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) and [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn).</span></span> <span data-ttu-id="18799-106">Estas nuevas funciones permiten la compatibilidad con la biometría segura mediante el TPM 2,0.</span><span class="sxs-lookup"><span data-stu-id="18799-106">These new functions allow support for secure biometrics using TPM 2.0.</span></span> <span data-ttu-id="18799-107">En la tabla siguiente se muestra el flujo de trabajo de inscripción del adaptador.</span><span class="sxs-lookup"><span data-stu-id="18799-107">The following table shows the adapter-side enrollment workflow.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18799-108">API de cliente</span><span class="sxs-lookup"><span data-stu-id="18799-108">Client API</span></span></td>
<td><span data-ttu-id="18799-109">Métodos de adaptador</span><span class="sxs-lookup"><span data-stu-id="18799-109">Adapter Methods</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18799-110"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENGINE_INFO)</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-110"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty(EXTENDED_ENGINE_INFO)</strong></a></span></span></td>
<td><span data-ttu-id="18799-111"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>EngineAdapterQueryExtendedInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-111"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>EngineAdapterQueryExtendedInfo</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18799-112"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>WinBioEnrollBegin</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-112"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>WinBioEnrollBegin</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="18799-113"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>StorageAdapterQueryBySubject</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-113"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>StorageAdapterQueryBySubject</strong></a></span></span></li>
<li><span data-ttu-id="18799-114"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>SensorAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-114"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>SensorAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="18799-115"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-115"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="18799-116"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-116"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="18799-117"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>EngineAdapterCreateEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-117"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>EngineAdapterCreateEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="18799-118"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>EngineAdapterSetEnrollmentParameters</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-118"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>EngineAdapterSetEnrollmentParameters</strong></a></span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18799-119"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"><strong>WinBioEnrollCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-119"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"><strong>WinBioEnrollCapture</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="18799-120"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>SensorAdapterStartCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-120"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>SensorAdapterStartCapture</strong></a></span></span></li>
<li><span data-ttu-id="18799-121"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>SensorAdapterFinishCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-121"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>SensorAdapterFinishCapture</strong></a></span></span></li>
<li><span data-ttu-id="18799-122"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>SensorAdapterPushDataToEngine</strong></a><strong>[-></strong> <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>EngineAdapterAcceptSampleData</strong></a>]</span><span class="sxs-lookup"><span data-stu-id="18799-122"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>SensorAdapterPushDataToEngine</strong></a><strong>[-></strong><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>EngineAdapterAcceptSampleData</strong></a>]</span></span></li>
<li><span data-ttu-id="18799-123">Si S_OK o WINBIO_I_MORE_DATA</span><span class="sxs-lookup"><span data-stu-id="18799-123">If S_OK or WINBIO_I_MORE_DATA</span></span>
<ol>
<li><span data-ttu-id="18799-124"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>EngineAdapterUpdateEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-124"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>EngineAdapterUpdateEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="18799-125">[El autor de la llamada continúa la inscripción]</span><span class="sxs-lookup"><span data-stu-id="18799-125">[Caller continues enrollment]</span></span></li>
</ol></li>
<li><span data-ttu-id="18799-126">De lo contrario, si WINBIO_E_BAD_CAPTURE [el autor de la llamada muestra los comentarios de rechazo, continúa la inscripción]</span><span class="sxs-lookup"><span data-stu-id="18799-126">Else if WINBIO_E_BAD_CAPTURE [Caller displays reject feedback, continues enrollment]</span></span> <br/></li>
<li><span data-ttu-id="18799-127">En caso contrario, si hay otro ERROR</span><span class="sxs-lookup"><span data-stu-id="18799-127">Else if other ERROR</span></span>
<ol>
<li><span data-ttu-id="18799-128"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-128"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="18799-129"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-129"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="18799-130">[Anulación de la inscripción del servicio bio]</span><span class="sxs-lookup"><span data-stu-id="18799-130">[Bio service aborts enrollment]</span></span></li>
</ol></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18799-131"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENROLLMENT_STATUS)</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-131"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENROLLMENT_STATUS)</strong></a></span></span></td>
<td><span data-ttu-id="18799-132"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>EngineAdapterQueryExtendedEnrollmentStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-132"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>EngineAdapterQueryExtendedEnrollmentStatus</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18799-133"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>WinBioEnrollCommit</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-133"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>WinBioEnrollCommit</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="18799-134"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>EngineAdapterCheckForDuplicate</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-134"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>EngineAdapterCheckForDuplicate</strong></a></span></span></li>
<li><span data-ttu-id="18799-135">Si la base de datos extraíble</span><span class="sxs-lookup"><span data-stu-id="18799-135">If REMOVABLE DATABASE</span></span>
<ol>
<li><span data-ttu-id="18799-136"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>EngineAdapterGetEnrollmentHash</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-136"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>EngineAdapterGetEnrollmentHash</strong></a></span></span></li>
<li><span data-ttu-id="18799-137"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-137"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span></span></li>
</ol></li>
<li><span data-ttu-id="18799-138">Else<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-138">Else<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18799-139"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"><strong>WinBioEnrollDiscard</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-139"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"><strong>WinBioEnrollDiscard</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="18799-140"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>EngineAdapterDiscardEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-140"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>EngineAdapterDiscardEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="18799-141"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-141"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="18799-142"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="18799-142"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 





