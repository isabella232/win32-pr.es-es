---
title: Constantes de error de NAP (WinError. h)
description: Las siguientes constantes de error de NAP se definen en WinError. h.
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b871d6f00174f05ab580aad54395851fa70af877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996888"
---
# <a name="nap-error-constants"></a><span data-ttu-id="9fda7-103">Constantes de error de NAP</span><span class="sxs-lookup"><span data-stu-id="9fda7-103">NAP Error Constants</span></span>

> [!Note]  
> <span data-ttu-id="9fda7-104">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="9fda7-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9fda7-105">Las siguientes constantes de error de NAP se definen en WinError. h.</span><span class="sxs-lookup"><span data-stu-id="9fda7-105">The following NAP error constants are defined in WinError.h.</span></span>

<dl> <dt>

<span data-ttu-id="9fda7-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**\_paquete NAP E \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="9fda7-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP\_E\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-107">\_HRESULT \_ \_ (TYPEDEF) (0x80270001L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-107">\_HRESULT\_TYPEDEF\_(0x80270001L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-108">El paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) de NAP no es válido.</span><span class="sxs-lookup"><span data-stu-id="9fda7-108">The NAP [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**falta el SOH de NAP \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9fda7-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP\_E\_MISSING\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-110">\_HRESULT \_ \_ (TYPEDEF) (0x80270002L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-110">\_HRESULT\_TYPEDEF\_(0x80270002L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-111">Falta un [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) en el paquete NAP.</span><span class="sxs-lookup"><span data-stu-id="9fda7-111">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) was missing from the NAP packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**\_ \_ identificador conflictivo de NAP \_ E**</span><span class="sxs-lookup"><span data-stu-id="9fda7-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**NAP\_E\_CONFLICTING\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-113">\_HRESULT \_ \_ (TYPEDEF) (0x80270003L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-113">\_HRESULT\_TYPEDEF\_(0x80270003L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-114">El identificador de entidad entra en conflicto con un identificador de entidad ya registrado.</span><span class="sxs-lookup"><span data-stu-id="9fda7-114">The entity ID conflicts with an already-registered entity ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**\_no se \_ ha \_ almacenado en caché el \_ SOH de NAP E**</span><span class="sxs-lookup"><span data-stu-id="9fda7-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP\_E\_NO\_CACHED\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-116">\_HRESULT \_ \_ (TYPEDEF) (0x80270004L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-116">\_HRESULT\_TYPEDEF\_(0x80270004L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-117">No hay ningún [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) en caché presente.</span><span class="sxs-lookup"><span data-stu-id="9fda7-117">No cached [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP \_ E \_ todavía \_ enlazado**</span><span class="sxs-lookup"><span data-stu-id="9fda7-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP\_E\_STILL\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-119">\_HRESULT \_ \_ (TYPEDEF) (0x80270005L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-119">\_HRESULT\_TYPEDEF\_(0x80270005L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-120">La entidad sigue estando enlazada al sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="9fda7-120">The entity is still bound to the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP \_ E \_ no \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="9fda7-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP\_E\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-122">\_HRESULT \_ \_ (TYPEDEF) (0x80270006L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-122">\_HRESULT\_TYPEDEF\_(0x80270006L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-123">La entidad no está registrada con el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="9fda7-123">The entity is not registered with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ no \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="9fda7-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP\_E\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-125">\_HRESULT \_ \_ (TYPEDEF) (0x80270007L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-125">\_HRESULT\_TYPEDEF\_(0x80270007L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-126">La entidad no se ha inicializado con el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="9fda7-126">The entity is not initialized with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**identificador de NAP \_ E no \_ coincidente \_**</span><span class="sxs-lookup"><span data-stu-id="9fda7-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**NAP\_E\_MISMATCHED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-128">\_HRESULT \_ \_ (TYPEDEF) (0x80270008L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-128">\_HRESULT\_TYPEDEF\_(0x80270008L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-129">Los identificadores de correlación de la solicitud de [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) y la respuesta de **SOH** no coinciden.</span><span class="sxs-lookup"><span data-stu-id="9fda7-129">The correlation IDs in the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) request and **SoH** response do not match up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ no \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="9fda7-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP\_E\_NOT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-131">\_HRESULT \_ \_ (TYPEDEF) (0x80270009L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-131">\_HRESULT\_TYPEDEF\_(0x80270009L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-132">La finalización se indicó en una solicitud que no está pendiente actualmente.</span><span class="sxs-lookup"><span data-stu-id="9fda7-132">Completion was indicated on a request that is not currently pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**\_ \_ \_ no \_ se encontró el identificador de NAP E**</span><span class="sxs-lookup"><span data-stu-id="9fda7-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**NAP\_E\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-134">\_HRESULT \_ \_ (TYPEDEF) (0x8027000AL)</span><span class="sxs-lookup"><span data-stu-id="9fda7-134">\_HRESULT\_TYPEDEF\_(0x8027000AL)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-135">No se encontró el identificador del componente NAP.</span><span class="sxs-lookup"><span data-stu-id="9fda7-135">The NAP component's ID was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**tamaño de NAP \_ E \_ MaxSize \_ demasiado \_ pequeño**</span><span class="sxs-lookup"><span data-stu-id="9fda7-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP\_E\_MAXSIZE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-137">\_HRESULT \_ \_ (TYPEDEF) (0x8027000BL)</span><span class="sxs-lookup"><span data-stu-id="9fda7-137">\_HRESULT\_TYPEDEF\_(0x8027000BL)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-138">El tamaño máximo de la conexión es demasiado pequeño para un paquete SoH.</span><span class="sxs-lookup"><span data-stu-id="9fda7-138">The maximum size of the connection is too small for an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**el \_ servicio NAP E \_ \_ no se \_ está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="9fda7-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**NAP\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-140">\_HRESULT \_ \_ (TYPEDEF) (0x8027000CL)</span><span class="sxs-lookup"><span data-stu-id="9fda7-140">\_HRESULT\_TYPEDEF\_(0x8027000CL)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-141">El servicio NapAgent no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="9fda7-141">The NapAgent service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**\_certificado NAP \_ S \_ ya \_ presente**</span><span class="sxs-lookup"><span data-stu-id="9fda7-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**NAP\_S\_CERT\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-143">\_HRESULT \_ \_ (TYPEDEF) (0x0027000DL)</span><span class="sxs-lookup"><span data-stu-id="9fda7-143">\_HRESULT\_TYPEDEF\_(0x0027000DL)</span></span> 
</dt> <dt>



<span data-ttu-id="9fda7-144">Ya existe un certificado en el almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="9fda7-144">A certificate is already present in the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**\_entidad E de NAP \_ \_ deshabilitada**</span><span class="sxs-lookup"><span data-stu-id="9fda7-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**NAP\_E\_ENTITY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-146">\_HRESULT \_ \_ (TYPEDEF) (0x8027000EL)</span><span class="sxs-lookup"><span data-stu-id="9fda7-146">\_HRESULT\_TYPEDEF\_(0x8027000EL)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-147">La entidad se deshabilita con el servicio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="9fda7-147">The entity is disabled with the NapAgent service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**ERROR de NAP \_ E \_ netsh \_ GROUPPOLICY \_**</span><span class="sxs-lookup"><span data-stu-id="9fda7-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**NAP\_E\_NETSH\_GROUPPOLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-149">\_HRESULT \_ \_ (TYPEDEF) (0x8027000FL)</span><span class="sxs-lookup"><span data-stu-id="9fda7-149">\_HRESULT\_TYPEDEF\_(0x8027000FL)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-150">Directiva de grupo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="9fda7-150">Group Policy is not configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP \_ E \_ demasiadas \_ \_ llamadas**</span><span class="sxs-lookup"><span data-stu-id="9fda7-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP\_E\_TOO\_MANY\_CALLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-152">\_HRESULT \_ \_ (TYPEDEF) (0x80270010L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-152">\_HRESULT\_TYPEDEF\_(0x80270010L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-153">Demasiadas llamadas simultáneas.</span><span class="sxs-lookup"><span data-stu-id="9fda7-153">Too many simultaneous calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**\_existe la \_ configuración de SHV E \_ NAP \_**</span><span class="sxs-lookup"><span data-stu-id="9fda7-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**NAP\_E\_SHV\_CONFIG\_EXISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-155">\_HRESULT \_ \_ (TYPEDEF) (0x80270011L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-155">\_HRESULT\_TYPEDEF\_(0x80270011L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-156">La configuración de SHV ya existe.</span><span class="sxs-lookup"><span data-stu-id="9fda7-156">SHV configuration already exists.</span></span>

> [!Note]  
> <span data-ttu-id="9fda7-157">Compatible con Windows 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9fda7-157">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**\_ \_ \_ \_ no se encontró la configuración \_ de SHV de NAP**</span><span class="sxs-lookup"><span data-stu-id="9fda7-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-159">\_HRESULT \_ \_ (TYPEDEF) (0x80270012L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-159">\_HRESULT\_TYPEDEF\_(0x80270012L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-160">No se encuentra la configuración de SHV.</span><span class="sxs-lookup"><span data-stu-id="9fda7-160">SHV configuration is not found.</span></span>

> [!Note]  
> <span data-ttu-id="9fda7-161">Compatible con Windows 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9fda7-161">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fda7-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**tiempo de espera de NAP \_ E \_ SHV \_**</span><span class="sxs-lookup"><span data-stu-id="9fda7-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**NAP\_E\_SHV\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fda7-163">\_HRESULT \_ \_ (TYPEDEF) (0x80270013L)</span><span class="sxs-lookup"><span data-stu-id="9fda7-163">\_HRESULT\_TYPEDEF\_(0x80270013L)</span></span>
</dt> <dt>



<span data-ttu-id="9fda7-164">SHV agotó el tiempo de espera en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9fda7-164">SHV timed out on the request.</span></span>

> [!Note]  
> <span data-ttu-id="9fda7-165">Compatible con Windows 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9fda7-165">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9fda7-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fda7-166">Requirements</span></span>



| <span data-ttu-id="9fda7-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fda7-167">Requirement</span></span> | <span data-ttu-id="9fda7-168">Value</span><span class="sxs-lookup"><span data-stu-id="9fda7-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fda7-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fda7-169">Minimum supported client</span></span><br/> | <span data-ttu-id="9fda7-170">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9fda7-170">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9fda7-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fda7-171">Minimum supported server</span></span><br/> | <span data-ttu-id="9fda7-172">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9fda7-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9fda7-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fda7-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fda7-174"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fda7-174"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fda7-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fda7-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fda7-176">**Constantes de NAP**</span><span class="sxs-lookup"><span data-stu-id="9fda7-176">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 





