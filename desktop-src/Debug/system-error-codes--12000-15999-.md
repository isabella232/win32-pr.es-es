---
description: Describe los códigos de error 12000-1599 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Códigos de error del sistema (12000-15999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496246"
---
# <a name="system-error-codes-12000-15999"></a><span data-ttu-id="1b6f6-103">Códigos de error del sistema (12000-15999)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-103">System Error Codes (12000-15999)</span></span>

> [!NOTE]
> <span data-ttu-id="1b6f6-104">Esta información está destinada a los desarrolladores que depuran errores del sistema.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="1b6f6-105">En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1b6f6-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="1b6f6-106">En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) (errores 12000 a 15999).</span><span class="sxs-lookup"><span data-stu-id="1b6f6-106">The following list describes [system error codes](system-error-codes.md) (errors 12000 to 15999).</span></span> <span data-ttu-id="1b6f6-107">La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="1b6f6-108">Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="1b6f6-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**Error \_ de \_Internet \** _</span><span class="sxs-lookup"><span data-stu-id="1b6f6-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**ERROR\_INTERNET\_\** _</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-110">12000-12175 (0x2EE0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-110">12000 - 12175 (0x2EE0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-111">Consulte [códigos de error de Internet](../wininet/wininet-errors.md) y Wininet. h.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-111">See [Internet Error Codes](../wininet/wininet-errors.md) and WinInet.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *error en la \_ \_ \_ directiva \_ IPSec QM*\*</span><span class="sxs-lookup"><span data-stu-id="1b6f6-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *ERROR\_IPSEC\_QM\_POLICY\_EXISTS*\*</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-113">13000 (0x32C8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-113">13000 (0x32C8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-114">La Directiva de modo rápido especificada ya existe.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-114">The specified quick mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró la directiva IPSec del QM**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERROR\_IPSEC\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-116">13001 (0x32C9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-116">13001 (0x32C9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-117">No se encontró la Directiva de modo rápido especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-117">The specified quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERROR \_ \_ \_ \_ en uso de la directiva IPSec QM \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERROR\_IPSEC\_QM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-119">13002 (0x32CA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-119">13002 (0x32CA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-120">Se está utilizando la Directiva de modo rápido especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-120">The specified quick mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERROR: la \_ Directiva de IPSec \_ mm \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERROR\_IPSEC\_MM\_POLICY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-122">13003 (0x32CB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-122">13003 (0x32CB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-123">La Directiva de modo principal especificada ya existe.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-123">The specified main mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró la Directiva de IPSec mm**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERROR\_IPSEC\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-125">13004 (0x32CC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-125">13004 (0x32CC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-126">No se encontró la Directiva de modo principal especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-126">The specified main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERROR \_ \_ en el \_ \_ uso de la Directiva de IPSec mm \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERROR\_IPSEC\_MM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-128">13005 (0x32CD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-128">13005 (0x32CD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-129">Se está utilizando la Directiva de modo principal especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-129">The specified main mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERROR \_ el \_ filtro de mm de IPSec \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERROR\_IPSEC\_MM\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-131">13006 (0x32CE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-131">13006 (0x32CE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-132">El filtro de modo principal especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-132">The specified main mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró el filtro IPSec mm**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERROR\_IPSEC\_MM\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-134">13007 (0x32CF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-134">13007 (0x32CF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-135">No se encontró el filtro de modo principal especificado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-135">The specified main mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERROR \_ de \_ filtro de transporte IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-137">13008 (0x32D0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-137">13008 (0x32D0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-138">El filtro de modo de transporte especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-138">The specified transport mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró el filtro de transporte IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-140">13009 (0x32D1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-140">13009 (0x32D1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-141">El filtro de modo de transporte especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-141">The specified transport mode filter does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERROR: \_ IPSec \_ mm \_ auth \_ existe**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERROR\_IPSEC\_MM\_AUTH\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-143">13010 (0x32D2)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-143">13010 (0x32D2)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-144">Existe la lista de autenticación de modo principal especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-144">The specified main mode authentication list exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró la autenticación de IPSec mm**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERROR\_IPSEC\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-146">13011 (0x32D3)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-146">13011 (0x32D3)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-147">No se encontró la lista de autenticación de modo principal especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-147">The specified main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERROR \_ \_ \_ de autenticación de IPSec mm \_ en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERROR\_IPSEC\_MM\_AUTH\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-149">13012 (0x32D4)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-149">13012 (0x32D4)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-150">Se está utilizando la lista de autenticación de modo principal especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-150">The specified main mode authentication list is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERROR \_ \_ \_ \_ \_ no se encontró la directiva \_ mm predeterminada de IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-152">13013 (0x32D5)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-152">13013 (0x32D5)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-153">No se encontró la Directiva de modo principal predeterminada especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-153">The specified default main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERROR \_ IPSec \_ predeterminado \_ \_ \_ no \_ se encontró la autenticación mm**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-155">13014 (0x32D6)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-155">13014 (0x32D6)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-156">No se encontró la lista de autenticación de modo principal predeterminada especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-156">The specified default main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERROR \_ : \_ \_ \_ \_ no \_ se encontró la Directiva de QM predeterminada de IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-158">13015 (0x32D7)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-158">13015 (0x32D7)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-159">No se encontró la directiva predeterminada de modo rápido especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-159">The specified default quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERROR: el \_ \_ filtro de túnel IPSec \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-161">13016 (0x32D8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-161">13016 (0x32D8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-162">El filtro de modo de túnel especificado existe.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-162">The specified tunnel mode filter exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró el filtro de túnel IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-164">13017 (0x32D9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-164">13017 (0x32D9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-165">No se encontró el filtro de modo de túnel especificado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-165">The specified tunnel mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERROR de \_ filtro de mm de IPsec con \_ \_ \_ \_ eliminación pendiente**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERROR\_IPSEC\_MM\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-167">13018 (0x32DA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-167">13018 (0x32DA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-168">El filtro de modo principal está pendiente de eliminación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-168">The Main Mode filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERROR \_ de \_ filtro de transporte IPSec \_ pendiente de \_ \_ eliminación**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-170">13019 (0x32DB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-170">13019 (0x32DB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-171">El filtro de transporte está pendiente de eliminación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-171">The transport filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERROR \_ de \_ filtro de túnel IPSec \_ pendiente de \_ \_ eliminación**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-173">13020 (0x32DC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-173">13020 (0x32DC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-174">El filtro de túnel está pendiente de eliminación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-174">The tunnel filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERROR \_ de \_ directiva IPSec mm de \_ \_ \_ eliminación pendiente**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERROR\_IPSEC\_MM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-176">13021 (0x32DD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-176">13021 (0x32DD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-177">La Directiva de modo principal está pendiente de eliminación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-177">The Main Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERROR \_ de \_ autenticación de IPSec mm de \_ autorización pendiente de \_ \_ eliminación**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERROR\_IPSEC\_MM\_AUTH\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-179">13022 (0x32DE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-179">13022 (0x32DE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-180">El paquete de autenticación de modo principal está pendiente de eliminación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-180">The Main Mode authentication bundle is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERROR \_ de \_ \_ \_ eliminación pendiente de directiva IPSec QM \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERROR\_IPSEC\_QM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-182">13023 (0x32DF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-182">13023 (0x32DF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-183">La Directiva de modo rápido está pendiente de eliminación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-183">The Quick Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**ADVERTENCIA \_ de \_ Directiva de IPSec mm \_ \_ eliminada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**WARNING\_IPSEC\_MM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-185">13024 (0x32E0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-185">13024 (0x32E0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-186">La Directiva de modo principal se agregó correctamente, pero no se admiten algunas de las ofertas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-186">The Main Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**ADVERTENCIA \_ de \_ directiva IPSec QM \_ \_ eliminada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**WARNING\_IPSEC\_QM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-188">13025 (0x32E1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-188">13025 (0x32E1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-189">La Directiva de modo rápido se agregó correctamente, pero no se admiten algunas de las ofertas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-189">The Quick Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERROR de \_ Inicio de estado de IPSec de \_ IKE \_ NEG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-191">13800 (0x35E8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-191">13800 (0x35E8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-192">ERROR de \_ Inicio de estado de IPSec de \_ IKE \_ NEG \_ \_</span><span class="sxs-lookup"><span data-stu-id="1b6f6-192">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERROR \_ de \_ autenticación IKE de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERROR\_IPSEC\_IKE\_AUTH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-194">13801 (0x35E9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-194">13801 (0x35E9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-195">Las credenciales de autenticación IKE no son aceptables.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-195">IKE authentication credentials are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERROR de protocolo \_ \_ IKE IPSec \_ \_ erróneo**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERROR\_IPSEC\_IKE\_ATTRIB\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-197">13802 (0x35EA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-197">13802 (0x35EA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-198">Los atributos de seguridad de IKE son inaceptables.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-198">IKE security attributes are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERROR \_ de \_ negociación IKE de IPSec \_ \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-200">13803 (0x35EB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-200">13803 (0x35EB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-201">Negociación IKE en curso.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-201">IKE Negotiation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**error \_ de \_ \_ procesamiento general de IKE de \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**ERROR\_IPSEC\_IKE\_GENERAL\_PROCESSING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-203">13804 (0x35EC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-203">13804 (0x35EC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-204">Error de procesamiento general.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-204">General processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERROR \_ de \_ IKE de IPSec \_ agotó el tiempo de \_ espera**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERROR\_IPSEC\_IKE\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-206">13805 (0x35ED)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-206">13805 (0x35ED)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-207">Se agotó el tiempo de espera de la negociación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-207">Negotiation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERROR \_ IPSec \_ IKE \_ no \_ CERT**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-209">13806 (0x35EE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-209">13806 (0x35EE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-210">IKE no encontró el certificado de equipo válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-210">IKE failed to find valid machine certificate.</span></span> <span data-ttu-id="1b6f6-211">Póngase en contacto con el administrador de seguridad de red sobre la instalación de un certificado válido en el almacén de certificados adecuado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-211">Contact your Network Security Administrator about installing a valid certificate in the appropriate Certificate Store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERROR \_ IPSec \_ IKE \_ SA \_ eliminado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERROR\_IPSEC\_IKE\_SA\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-213">13807 (0x35EF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-213">13807 (0x35EF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-214">SA IKE eliminada por el par antes del establecimiento completado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-214">IKE SA deleted by peer before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERROR de \_ IPSec \_ IKE \_ SA \_ cosechado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERROR\_IPSEC\_IKE\_SA\_REAPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-216">13808 (0x35F0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-216">13808 (0x35F0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-217">SA de IKE eliminada antes de que se completara el establecimiento.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-217">IKE SA deleted before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERROR de \_ adquisición de adquisición de IPSec \_ IKE \_ mm \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-219">13809 (0x35F1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-219">13809 (0x35F1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-220">La solicitud de negociación SAT en la cola es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-220">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERROR de \_ IPSec \_ IKE de \_ \_ adquisición \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-222">13810 (0x35F2)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-222">13810 (0x35F2)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-223">La solicitud de negociación SAT en la cola es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-223">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERROR \_ de \_ \_ eliminación de cola IKE \_ de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-225">13811 (0x35F3)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-225">13811 (0x35F3)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-226">La solicitud de negociación SAT en la cola es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-226">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERROR \_ de \_ cola IKE de IPSec \_ \_ \_ no entrega no \_ mm**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_NO\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-228">13812 (0x35F4)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-228">13812 (0x35F4)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-229">La solicitud de negociación SAT en la cola es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-229">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERROR \_ no se pudo \_ quitar la \_ \_ \_ respuesta IKE de IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERROR\_IPSEC\_IKE\_DROP\_NO\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-231">13813 (0x35F5)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-231">13813 (0x35F5)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-232">No hay respuesta del elemento del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-232">No response from peer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERROR \_ de \_ eliminación de retraso IPSec de IKE \_ mm \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-234">13814 (0x35F6)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-234">13814 (0x35F6)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-235">La negociación tardó demasiado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-235">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERROR \_ de \_ retraso de IPSec IKE de \_ QM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-237">13815 (0x35F7)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-237">13815 (0x35F7)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-238">La negociación tardó demasiado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-238">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**error \_ IKE de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**ERROR\_IPSEC\_IKE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-240">13816 (0x35F8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-240">13816 (0x35F8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-241">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-241">Unknown error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERROR \_ de \_ CRL IKE de IPSec \_ \_ errónea**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERROR\_IPSEC\_IKE\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-243">13817 (0x35F9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-243">13817 (0x35F9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-244">Error en la comprobación de revocación de certificados.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-244">Certificate Revocation Check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERROR \_ de \_ \_ uso de \_ clave no válida IKE de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERROR\_IPSEC\_IKE\_INVALID\_KEY\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-246">13818 (0x35FA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-246">13818 (0x35FA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-247">Uso de clave de certificado no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-247">Invalid certificate key usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERROR \_ de \_ IPSec \_ IKE \_ tipo de certificado no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-249">13819 (0x35FB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-249">13819 (0x35FB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-250">Tipo de certificado no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-250">Invalid certificate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERROR \_ IPSec \_ IKE \_ sin \_ \_ clave privada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-252">13820 (0x35FC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-252">13820 (0x35FC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-253">Error de negociación IKE porque el certificado de equipo utilizado no tiene una clave privada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-253">IKE negotiation failed because the machine certificate used does not have a private key.</span></span> <span data-ttu-id="1b6f6-254">Los certificados IPsec requieren una clave privada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-254">IPsec certificates require a private key.</span></span> <span data-ttu-id="1b6f6-255">Póngase en contacto con el administrador de seguridad de red para reemplazar por un certificado que tenga una clave privada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-255">Contact your Network Security administrator about replacing with a certificate that has a private key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERROR \_ de \_ \_ regeneración de \_ claves simultánea de IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERROR\_IPSEC\_IKE\_SIMULTANEOUS\_REKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-257">13821 (0x35FD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-257">13821 (0x35FD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-258">Se detectaron claves simultáneas.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-258">Simultaneous rekeys were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERROR de \_ IPSec \_ DH de IKE \_ \_ erróneo**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERROR\_IPSEC\_IKE\_DH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-260">13822 (0x35FE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-260">13822 (0x35FE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-261">Error en el cálculo de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-261">Failure in Diffie-Hellman computation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERROR \_ : \_ \_ no se \_ reconoce la carga crítica de \_ IKE de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERROR\_IPSEC\_IKE\_CRITICAL\_PAYLOAD\_NOT\_RECOGNIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-263">13823 (0x35FF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-263">13823 (0x35FF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-264">No sepa cómo procesar la carga crítica.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-264">Don't know how to process critical payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERROR \_ de \_ encabezado IPSec IKE \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-266">13824 (0x3600)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-266">13824 (0x3600)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-267">Encabezado no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-267">Invalid header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERROR \_ IPSec \_ IKE \_ sin \_ Directiva**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-269">13825 (0x3601)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-269">13825 (0x3601)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-270">No hay ninguna directiva configurada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-270">No policy configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERROR \_ de \_ \_ firma IKE no válida de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-272">13826 (0x3602)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-272">13826 (0x3602)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-273">No se pudo comprobar la firma.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-273">Failed to verify signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**error \_ de \_ Kerberos IKE de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**ERROR\_IPSEC\_IKE\_KERBEROS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-275">13827 (0x3603)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-275">13827 (0x3603)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-276">No se pudo autenticar con Kerberos.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-276">Failed to authenticate using Kerberos.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERROR \_ IPSec \_ IKE \_ sin \_ \_ clave pública**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PUBLIC\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-278">13828 (0x3604)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-278">13828 (0x3604)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-279">El certificado del mismo nivel no tenía una clave pública.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-279">Peer's certificate did not have a public key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERROR \_ de \_ proceso IKE de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-281">13829 (0x3605)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-281">13829 (0x3605)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-282">Error al procesar la carga de error.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-282">Error processing error payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERROR \_ IPSec \_ IKE de \_ proceso IKE \_ \_ SA**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-284">13830 (0x3606)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-284">13830 (0x3606)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-285">Error al procesar la carga de SA.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-285">Error processing SA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERROR \_ IPSec \_ IKE de proceso de IKE \_ \_ \_ prop**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_PROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-287">13831 (0x3607)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-287">13831 (0x3607)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-288">Error al procesar la carga de propuesta.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-288">Error processing Proposal payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERROR \_ IPSec \_ IKE de proceso de IKE \_ \_ \_ Trans**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_TRANS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-290">13832 (0x3608)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-290">13832 (0x3608)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-291">Error al procesar la carga de transformación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-291">Error processing Transform payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERROR en el \_ \_ proceso IKE de IPSec \_ \_ Err \_ ke**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_KE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-293">13833 (0x3609)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-293">13833 (0x3609)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-294">Error al procesar la carga de la KE.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-294">Error processing KE payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERROR \_ de \_ IKE de \_ proceso IKE \_ \_ de IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-296">13834 (0x360A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-296">13834 (0x360A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-297">Error al procesar la carga de identificador.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-297">Error processing ID payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERROR \_ de \_ IKE de \_ proceso IKE \_ \_ de IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-299">13835 (0x360B)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-299">13835 (0x360B)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-300">Error al procesar la carga de certificado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-300">Error processing Cert payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERROR en el \_ proceso IKE de IPSec de \_ \_ \_ Err \_ \_ req**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-302">13836 (0x360C)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-302">13836 (0x360C)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-303">Error al procesar la carga de la solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-303">Error processing Certificate Request payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERROR en el \_ hash de Err del \_ proceso IKE de IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-305">13837 (0x360D)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-305">13837 (0x360D)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-306">Error al procesar la carga hash.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-306">Error processing Hash payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERROR \_ IPSec \_ IKE de proceso de IKE \_ \_ \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-308">13838 (0x360E)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-308">13838 (0x360E)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-309">Error al procesar la carga de la firma.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-309">Error processing Signature payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERROR \_ de \_ IKE de \_ proceso IKE \_ \_ de IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NONCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-311">13839 (0x360F)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-311">13839 (0x360F)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-312">Error al procesar la carga de nonce.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-312">Error processing Nonce payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERROR en la notificación de ERROR del \_ \_ proceso IKE de IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-314">13840 (0x3610)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-314">13840 (0x3610)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-315">Error al procesar la carga de notificación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-315">Error processing Notify payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERROR de \_ IPSec \_ IKE de proceso de IKE \_ \_ \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-317">13841 (0x3611)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-317">13841 (0x3611)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-318">Error al procesar la carga de eliminación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-318">Error processing Delete Payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERROR en el proveedor de errores de \_ \_ proceso IKE de IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_VENDOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-320">13842 (0x3612)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-320">13842 (0x3612)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-321">Error al procesar la carga VendorId.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-321">Error processing VendorId payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERROR de \_ IPSec: \_ \_ carga no válida IKE \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-323">13843 (0x3613)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-323">13843 (0x3613)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-324">Carga no válida recibida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-324">Invalid payload received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERROR de \_ IPSec \_ IKE \_ carga \_ software \_ SA**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERROR\_IPSEC\_IKE\_LOAD\_SOFT\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-326">13844 (0x3614)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-326">13844 (0x3614)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-327">SA flexible cargada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-327">Soft SA loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERROR de \_ IPSec \_ IKE temporal de IKE \_ \_ \_ \_ desactivada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERROR\_IPSEC\_IKE\_SOFT\_SA\_TORN\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-329">13845 (0x3615)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-329">13845 (0x3615)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-330">SA flexible desactivada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-330">Soft SA torn down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERROR de \_ IPSec \_ IKE \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERROR\_IPSEC\_IKE\_INVALID\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-332">13846 (0x3616)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-332">13846 (0x3616)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-333">Cookie no válida recibida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-333">Invalid cookie received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERROR \_ IPSec \_ IKE \_ no \_ peer \_ CERT**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_PEER\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-335">13847 (0x3617)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-335">13847 (0x3617)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-336">El par no pudo enviar un certificado de equipo válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-336">Peer failed to send valid machine certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERROR \_ de \_ \_ CRL IPSec del mismo nivel \_ \_ no superada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERROR\_IPSEC\_IKE\_PEER\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-338">13848 (0x3618)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-338">13848 (0x3618)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-339">Error en la comprobación de revocación de certificación del certificado del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-339">Certification Revocation check of peer's certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERROR \_ de \_ \_ cambio de directiva IKE de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERROR\_IPSEC\_IKE\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-341">13849 (0x3619)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-341">13849 (0x3619)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-342">Nueva SAs invalidada de la Directiva con la Directiva antigua.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-342">New policy invalidated SAs formed with old policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERROR \_ de \_ IPSec \_ IKE \_ no \_ Directiva de mm**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_MM\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-344">13850 (0x361A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-344">13850 (0x361A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-345">No hay ninguna directiva IKE de modo principal disponible.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-345">There is no available Main Mode IKE policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERROR \_ IPSec \_ IKE \_ NOTCBPRIV**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERROR\_IPSEC\_IKE\_NOTCBPRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-347">13851 (0x361B)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-347">13851 (0x361B)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-348">No se pudo habilitar el privilegio TCB.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-348">Failed to enabled TCB privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERROR \_ IPSec \_ IKE \_ SECLOADFAIL**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERROR\_IPSEC\_IKE\_SECLOADFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-350">13852 (0x361C)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-350">13852 (0x361C)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-351">No se pudo cargar SECURITY.DLL.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-351">Failed to load SECURITY.DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERROR \_ IPSec \_ IKE \_ FAILSSPINIT**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERROR\_IPSEC\_IKE\_FAILSSPINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-353">13853 (0x361D)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-353">13853 (0x361D)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-354">No se pudo obtener la dirección de envío de la tabla de funciones de seguridad de SSPI.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-354">Failed to obtain security function table dispatch address from SSPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERROR \_ IPSec \_ IKE \_ FAILQUERYSSP**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERROR\_IPSEC\_IKE\_FAILQUERYSSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-356">13854 (0x361E)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-356">13854 (0x361E)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-357">No se pudo consultar el paquete Kerberos para obtener el tamaño máximo del token.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-357">Failed to query Kerberos package to obtain max token size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERROR \_ IPSec \_ IKE \_ SRVACQFAIL**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERROR\_IPSEC\_IKE\_SRVACQFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-359">13855 (0x361F)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-359">13855 (0x361F)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-360">No se pudieron obtener las credenciales del servidor Kerberos para el \_ servicio IKE/error IPSec \_ IKE.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-360">Failed to obtain Kerberos server credentials for ISAKMP/ERROR\_IPSEC\_IKE service.</span></span> <span data-ttu-id="1b6f6-361">La autenticación Kerberos no funcionará.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-361">Kerberos authentication will not function.</span></span> <span data-ttu-id="1b6f6-362">La razón más probable de esto es la falta de pertenencia a un dominio.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-362">The most likely reason for this is lack of domain membership.</span></span> <span data-ttu-id="1b6f6-363">Esto es normal si el equipo es miembro de un grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-363">This is normal if your computer is a member of a workgroup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERROR \_ IPSec \_ IKE \_ SRVQUERYCRED**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERROR\_IPSEC\_IKE\_SRVQUERYCRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-365">13856 (0x3620)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-365">13856 (0x3620)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-366">No se pudo determinar el nombre de entidad de seguridad de SSPI para el \_ \_ servicio IKE IKE/error IPSec ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).</span><span class="sxs-lookup"><span data-stu-id="1b6f6-366">Failed to determine SSPI principal name for ISAKMP/ERROR\_IPSEC\_IKE service ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERROR \_ IPSec \_ IKE \_ GETSPIFAIL**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERROR\_IPSEC\_IKE\_GETSPIFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-368">13857 (0x3621)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-368">13857 (0x3621)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-369">No se pudo obtener el SPI nuevo para la SA de entrada del controlador IPsec.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-369">Failed to obtain new SPI for the inbound SA from IPsec driver.</span></span> <span data-ttu-id="1b6f6-370">La causa más común es que el controlador no tenga el filtro correcto.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-370">The most common cause for this is that the driver does not have the correct filter.</span></span> <span data-ttu-id="1b6f6-371">Compruebe la Directiva para comprobar los filtros.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-371">Check your policy to verify the filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERROR \_ de \_ \_ filtro IKE no válido de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERROR\_IPSEC\_IKE\_INVALID\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-373">13858 (0x3622)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-373">13858 (0x3622)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-374">El filtro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-374">Given filter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERROR \_ \_ \_ \_ de memoria insuficiente de IKE de \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERROR\_IPSEC\_IKE\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-376">13859 (0x3623)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-376">13859 (0x3623)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-377">Se produjo un error de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-377">Memory allocation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERROR de \_ IPSec: \_ \_ \_ \_ \_ no se pudo agregar la clave de actualización IKE**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERROR\_IPSEC\_IKE\_ADD\_UPDATE\_KEY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-379">13860 (0x3624)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-379">13860 (0x3624)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-380">No se pudo agregar la Asociación de seguridad al controlador IPsec.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-380">Failed to add Security Association to IPsec Driver.</span></span> <span data-ttu-id="1b6f6-381">La causa más común es que la negociación IKE tardó demasiado tiempo en completarse.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-381">The most common cause for this is if the IKE negotiation took too long to complete.</span></span> <span data-ttu-id="1b6f6-382">Si el problema persiste, reduzca la carga en el equipo con errores.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-382">If the problem persists, reduce the load on the faulting machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERROR \_ de \_ directiva IPSec IKE \_ no válida \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERROR\_IPSEC\_IKE\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-384">13861 (0x3625)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-384">13861 (0x3625)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-385">Directiva no válida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-385">Invalid policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERROR \_ de \_ \_ Doi desconocido de IKE de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERROR\_IPSEC\_IKE\_UNKNOWN\_DOI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-387">13862 (0x3626)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-387">13862 (0x3626)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-388">DOI no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-388">Invalid DOI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERROR en la \_ \_ situación IPSec IKE \_ no válida \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SITUATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-390">13863 (0x3627)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-390">13863 (0x3627)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-391">Situación no válida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-391">Invalid situation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERROR de IPSec: error \_ \_ DH de IKE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERROR\_IPSEC\_IKE\_DH\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-393">13864 (0x3628)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-393">13864 (0x3628)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-394">Error de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-394">Diffie-Hellman failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERROR \_ de \_ Grupo IPSec IKE \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERROR\_IPSEC\_IKE\_INVALID\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-396">13865 (0x3629)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-396">13865 (0x3629)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-397">Grupo de Diffie-Hellman no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-397">Invalid Diffie-Hellman group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERROR \_ IPSec \_ \_ cifrado de IKE**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERROR\_IPSEC\_IKE\_ENCRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-399">13866 (0x362A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-399">13866 (0x362A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-400">Error al cifrar la carga.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-400">Error encrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERROR \_ de \_ \_ descifrado IKE de IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERROR\_IPSEC\_IKE\_DECRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-402">13867 (0x362B)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-402">13867 (0x362B)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-403">Error al descifrar la carga.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-403">Error decrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERROR \_ de \_ \_ coincidencia de directiva IKE de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERROR\_IPSEC\_IKE\_POLICY\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-405">13868 (0x362C)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-405">13868 (0x362C)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-406">Error de coincidencia de directiva.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-406">Policy match error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERROR de \_ IPSec \_ IKE \_ no compatible \_ ID**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERROR\_IPSEC\_IKE\_UNSUPPORTED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-408">13869 (0x362D)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-408">13869 (0x362D)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-409">IDENTIFICADOR no compatible.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-409">Unsupported ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERROR de \_ IPSec \_ IKE \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-411">13870 (0x362E)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-411">13870 (0x362E)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-412">Error de comprobación de hash.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-412">Hash verification failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERROR \_ de \_ hash IPSec de IKE \_ no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-414">13871 (0x362F)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-414">13871 (0x362F)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-415">Algoritmo hash no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-415">Invalid hash algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERROR de \_ IPSec \_ IKE \_ no válido tamaño de \_ hash \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-417">13872 (0x3630)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-417">13872 (0x3630)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-418">Tamaño de hash no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-418">Invalid hash size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERROR \_ IPSec \_ IKE \_ no válido \_ cifrado \_ alg**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_ENCRYPT\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-420">13873 (0x3631)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-420">13873 (0x3631)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-421">Algoritmo de cifrado no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-421">Invalid encryption algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERROR \_ IPSec \_ IKE \_ de \_ autenticación no válida \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-423">13874 (0x3632)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-423">13874 (0x3632)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-424">Algoritmo de autenticación no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-424">Invalid authentication algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERROR en el \_ \_ SIG IPSec IKE \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-426">13875 (0x3633)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-426">13875 (0x3633)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-427">Firma de certificado no válida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-427">Invalid certificate signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERROR \_ de \_ carga IKE de IPSec \_ \_ errónea**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERROR\_IPSEC\_IKE\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-429">13876 (0x3634)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-429">13876 (0x3634)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-430">Error de carga.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-430">Load failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERROR \_ de \_ \_ RPC IKE \_ Delete de IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERROR\_IPSEC\_IKE\_RPC\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-432">13877 (0x3635)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-432">13877 (0x3635)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-433">Eliminado a través de una llamada RPC.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-433">Deleted via RPC call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERROR \_ de \_ \_ reinicialización benigna de IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERROR\_IPSEC\_IKE\_BENIGN\_REINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-435">13878 (0x3636)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-435">13878 (0x3636)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-436">Estado temporal creado para realizar la reinicialización.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-436">Temporary state created to perform reinitialization.</span></span> <span data-ttu-id="1b6f6-437">No se trata de un error real.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-437">This is not a real failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERROR \_ de \_ \_ notificación de \_ duración del respondedor no válido IKE \_ de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERROR\_IPSEC\_IKE\_INVALID\_RESPONDER\_LIFETIME\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-439">13879 (0x3637)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-439">13879 (0x3637)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-440">El valor de duración recibido en la notificación de duración del respondedor está por debajo del valor mínimo configurado en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-440">The lifetime value received in the Responder Lifetime Notify is below the Windows 2000 configured minimum value.</span></span> <span data-ttu-id="1b6f6-441">Corrija la Directiva en el equipo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-441">Please fix the policy on the peer machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERROR \_ de \_ IPSec \_ IKE \_ versión principal no válida \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MAJOR\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-443">13880 (0x3638)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-443">13880 (0x3638)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-444">El destinatario no puede controlar la versión de IKE especificada en el encabezado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-444">The recipient cannot handle version of IKE specified in the header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERROR \_ IPSec \_ IKE \_ \_ KEYLEN de certificado no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_KEYLEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-446">13881 (0x3639)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-446">13881 (0x3639)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-447">La longitud de clave del certificado es demasiado pequeña para los requisitos de seguridad configurados.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-447">Key length in certificate is too small for configured security requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERROR en el \_ límite de IPSec \_ IKE \_ mm \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERROR\_IPSEC\_IKE\_MM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-449">13882 (0x363A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-449">13882 (0x363A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-450">Número máximo de SA de MM establecidas en el mismo nivel superado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-450">Max number of established MM SAs to peer exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERROR \_ de \_ negociación IKE IPSec \_ \_ deshabilitada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-452">13883 (0x363B)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-452">13883 (0x363B)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-453">IKE recibió una directiva que deshabilita la negociación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-453">IKE received a policy that disables negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERROR de \_ IPSec \_ IKE de \_ QM \_ Limit**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERROR\_IPSEC\_IKE\_QM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-455">13884 (0x363C)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-455">13884 (0x363C)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-456">Se alcanzó el límite de modo rápido máximo para el modo principal.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-456">Reached maximum quick mode limit for the main mode.</span></span> <span data-ttu-id="1b6f6-457">Se iniciará el nuevo modo principal.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-457">New main mode will be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERROR de \_ IPSec \_ IKE \_ mm \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERROR\_IPSEC\_IKE\_MM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-459">13885 (0x363D)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-459">13885 (0x363D)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-460">La vigencia de SA de modo principal expiró o el interlocutor envió una eliminación de modo principal.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-460">Main mode SA lifetime expired or peer sent a main mode delete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERROR \_ IPSec \_ IKE \_ del mismo nivel \_ \_ asumido \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERROR\_IPSEC\_IKE\_PEER\_MM\_ASSUMED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-462">13886 (0x363E)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-462">13886 (0x363E)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-463">Se supone que la SA de modo principal no es válida porque el elemento del mismo nivel dejó de responder.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-463">Main mode SA assumed to be invalid because peer stopped responding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de \_ Directiva de cadena de certificado \_ IKE \_ de IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERROR\_IPSEC\_IKE\_CERT\_CHAIN\_POLICY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-465">13887 (0x363F)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-465">13887 (0x363F)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-466">El certificado no está encadenado a una raíz de confianza en la directiva IPsec.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-466">Certificate doesn't chain to a trusted root in IPsec policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERROR de \_ IPSec \_ IKE \_ inesperado \_ \_ ID. de mensaje**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERROR\_IPSEC\_IKE\_UNEXPECTED\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-468">13888 (0x3640)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-468">13888 (0x3640)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-469">Se recibió un ID. de mensaje inesperado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-469">Received unexpected message ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERROR en \_ IPSec: carga de \_ \_ autenticación no válida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-471">13889 (0x3641)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-471">13889 (0x3641)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-472">Ofertas de autenticación no válidas recibidas.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-472">Received invalid authentication offers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERROR \_ de \_ cookie de dos de IKE de IPSec \_ \_ \_ enviada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERROR\_IPSEC\_IKE\_DOS\_COOKIE\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-474">13890 (0x3642)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-474">13890 (0x3642)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-475">La cookie DoS enviadas notifica al iniciador.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-475">Sent DoS cookie notify to initiator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERROR \_ de \_ cierre de IKE de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERROR\_IPSEC\_IKE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-477">13891 (0x3643)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-477">13891 (0x3643)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-478">El servicio IKE se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-478">IKE service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERROR \_ IPSec \_ IKE \_ CGA \_ auth \_ no se pudo ejecutar**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERROR\_IPSEC\_IKE\_CGA\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-480">13892 (0x3644)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-480">13892 (0x3644)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-481">No se pudo comprobar el enlace entre la dirección CGA y el certificado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-481">Could not verify binding between CGA address and certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERROR \_ de \_ proceso IKE de IPSec \_ \_ \_ NATOA**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NATOA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-483">13893 (0x3645)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-483">13893 (0x3645)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-484">Error al procesar la carga de NatOA.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-484">Error processing NatOA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERROR \_ IPSec \_ IKE \_ no \_ válido \_ para el \_ QM**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MM\_FOR\_QM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-486">13894 (0x3646)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-486">13894 (0x3646)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-487">Los parámetros del modo principal no son válidos para este modo rápido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-487">Parameters of the main mode are invalid for this quick mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERROR \_ IPSec \_ IKE \_ QM \_ caducado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERROR\_IPSEC\_IKE\_QM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-489">13895 (0x3647)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-489">13895 (0x3647)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-490">El controlador IPsec expiró la SA de modo rápido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-490">Quick mode SA was expired by IPsec driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERROR \_ IPSec \_ IKE \_ demasiados \_ \_ filtros**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERROR\_IPSEC\_IKE\_TOO\_MANY\_FILTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-492">13896 (0x3648)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-492">13896 (0x3648)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-493">Se detectaron demasiados filtros de IKEEXT agregados dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-493">Too many dynamically added IKEEXT filters were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERROR de \_ fin de estado de IPSec de \_ IKE \_ NEG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-495">13897 (0x3649)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-495">13897 (0x3649)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-496">ERROR de \_ fin de estado de IPSec de \_ IKE \_ NEG \_ \_</span><span class="sxs-lookup"><span data-stu-id="1b6f6-496">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERROR \_ del \_ \_ túnel de \_ \_ NAP ficticio \_ de IKE de IPSec Kill**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERROR\_IPSEC\_IKE\_KILL\_DUMMY\_NAP\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-498">13898 (0x364A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-498">13898 (0x364A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-499">La reautenticación NAP se realizó correctamente y debe eliminar el túnel IKEv2 NAP ficticio.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-499">NAP reauth succeeded and must delete the dummy NAP IKEv2 tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERROR \_ de \_ \_ asignación de \_ dirección IP interna IKE \_ de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERROR\_IPSEC\_IKE\_INNER\_IP\_ASSIGNMENT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-501">13899 (0x364B)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-501">13899 (0x364B)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-502">Error al asignar la dirección IP interna al iniciador en modo de túnel.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-502">Error in assigning inner IP address to initiator in tunnel mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERROR \_ IPSec \_ IKE \_ requiere \_ \_ falta de carga de CP \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERROR\_IPSEC\_IKE\_REQUIRE\_CP\_PAYLOAD\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-504">13900 (0x364C)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-504">13900 (0x364C)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-505">Falta la carga de configuración necesaria.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-505">Require configuration payload missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERROR \_ de \_ \_ negociación de \_ suplantación de módulo de clave IPSec \_ \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERROR\_IPSEC\_KEY\_MODULE\_IMPERSONATION\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-507">13901 (0x364D)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-507">13901 (0x364D)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-508">Una negociación que se ejecuta como el principio de seguridad que emitió la conexión está en curso.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-508">A negotiation running as the security principle who issued the connection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERROR en la \_ \_ \_ coexistencia IKE de IPSec \_ suprimir**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERROR\_IPSEC\_IKE\_COEXISTENCE\_SUPPRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-510">13902 (0x364E)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-510">13902 (0x364E)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-511">SA eliminado debido a que la coexistencia de IKEv1/AuthIP suprime la comprobación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-511">SA was deleted due to IKEv1/AuthIP co-existence suppress check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERROR \_ IPSec \_ IKE \_ RATELIMIT \_ Drop**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERROR\_IPSEC\_IKE\_RATELIMIT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-513">13903 (0x364F)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-513">13903 (0x364F)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-514">Se quitó la solicitud SA entrante debido a la limitación de velocidad de direcciones IP del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-514">Incoming SA request was dropped due to peer IP address rate limiting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERROR \_ IPSec \_ IKE \_ del mismo nivel \_ \_ no admite \_ Mobike**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERROR\_IPSEC\_IKE\_PEER\_DOESNT\_SUPPORT\_MOBIKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-516">13904 (0x3650)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-516">13904 (0x3650)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-517">El elemento del mismo nivel no es compatible con MOBIKE.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-517">Peer does not support MOBIKE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERROR \_ de \_ autorización IKE de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-519">13905 (0x3651)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-519">13905 (0x3651)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-520">El establecimiento de la asociación de seguridad no está autorizado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-520">SA establishment is not authorized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERROR \_ de \_ \_ autorización de \_ credenciales seguras \_ IKE IKE \_ de IPSec**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-522">13906 (0x3652)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-522">13906 (0x3652)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-523">El establecimiento de SA no está autorizado porque no hay una credencial basada en PKINIT suficientemente segura.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-523">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERROR \_ \_ \_ de autorización IKE \_ \_ de IPSec \_ con \_ reintento opcional**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE\_WITH\_OPTIONAL\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-525">13907 (0x3653)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-525">13907 (0x3653)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-526">El establecimiento de la asociación de seguridad no está autorizado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-526">SA establishment is not authorized.</span></span> <span data-ttu-id="1b6f6-527">Es posible que tenga que especificar credenciales actualizadas o diferentes, como una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-527">You may need to enter updated or different credentials such as a smartcard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERROR \_ \_ \_ \_ de autorización de credenciales sólidas IKE \_ \_ de IPSec y \_ \_ error CERTMAP**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_AND\_CERTMAP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-529">13908 (0x3654)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-529">13908 (0x3654)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-530">El establecimiento de SA no está autorizado porque no hay una credencial basada en PKINIT suficientemente segura.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-530">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span> <span data-ttu-id="1b6f6-531">Esto puede estar relacionado con un error de asignación de certificado a cuenta para la SA.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-531">This might be related to certificate-to-account mapping failure for the SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERROR \_ de \_ \_ servidor de \_ estado \_ extendido \_ de IPSec IKE NEG**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-533">13909 (0x3655)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-533">13909 (0x3655)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-534">ERROR \_ de \_ \_ servidor de \_ estado \_ extendido \_ de IPSec IKE NEG</span><span class="sxs-lookup"><span data-stu-id="1b6f6-534">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERROR \_ de \_ SPI incorrecto de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERROR\_IPSEC\_BAD\_SPI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-536">13910 (0x3656)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-536">13910 (0x3656)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-537">El SPI en el paquete no coincide con una SA de IPsec válida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-537">The SPI in the packet does not match a valid IPsec SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERROR: \_ vigencia de SA de IPSec \_ \_ \_ expirada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERROR\_IPSEC\_SA\_LIFETIME\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-539">13911 (0x3657)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-539">13911 (0x3657)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-540">El paquete se recibió en una SA de IPsec cuya duración ha expirado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-540">Packet was received on an IPsec SA whose lifetime has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERROR \_ SA de IPSec \_ incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERROR\_IPSEC\_WRONG\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-542">13912 (0x3658)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-542">13912 (0x3658)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-543">El paquete se recibió en una SA de IPsec que no coincide con las características del paquete.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-543">Packet was received on an IPsec SA that does not match the packet characteristics.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERROR \_ \_ al comprobar la reproducción de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERROR\_IPSEC\_REPLAY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-545">13913 (0x3659)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-545">13913 (0x3659)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-546">Error al comprobar el número de secuencia de paquete.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-546">Packet sequence number replay check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERROR \_ de \_ paquete IPSec no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERROR\_IPSEC\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-548">13914 (0x365A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-548">13914 (0x365A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-549">El encabezado o el finalizador IPsec del paquete no es válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-549">IPsec header and/or trailer in the packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERROR \_ de \_ comprobación de integridad de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERROR\_IPSEC\_INTEGRITY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-551">13915 (0x365B)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-551">13915 (0x365B)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-552">Error de comprobación de integridad de IPsec.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-552">IPsec integrity check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERROR \_ de \_ \_ eliminación de texto no cifrado de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERROR\_IPSEC\_CLEAR\_TEXT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-554">13916 (0x365C)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-554">13916 (0x365C)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-555">IPsec quitó un paquete de texto no cifrado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-555">IPsec dropped a clear text packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERROR \_ de \_ \_ eliminación de Firewall de autenticación IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERROR\_IPSEC\_AUTH\_FIREWALL\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-557">13917 (0x365D)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-557">13917 (0x365D)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-558">IPsec quitó un paquete ESP entrante en modo de Firewall autenticado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-558">IPsec dropped an incoming ESP packet in authenticated firewall mode.</span></span> <span data-ttu-id="1b6f6-559">Esta caída es benigna.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-559">This drop is benign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERROR en el \_ límite de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERROR\_IPSEC\_THROTTLE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-561">13918 (0x365E)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-561">13918 (0x365E)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-562">IPsec quitó un paquete debido a la limitación de DoS.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-562">IPsec dropped a packet due to DoS throttling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERROR en el \_ \_ bloque DOSP de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERROR\_IPSEC\_DOSP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-564">13925 (0x3665)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-564">13925 (0x3665)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-565">La protección de DoS de IPsec coincidía con una regla de bloqueo explícita.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-565">IPsec DoS Protection matched an explicit block rule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERROR \_ IPSec \_ DOSP \_ de \_ multidifusión recibido**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERROR\_IPSEC\_DOSP\_RECEIVED\_MULTICAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-567">13926 (0x3666)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-567">13926 (0x3666)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-568">La protección de DoS de IPsec recibió un paquete de multidifusión específico de IPsec que no está permitido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-568">IPsec DoS Protection received an IPsec specific multicast packet which is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERROR \_ IPSec \_ DOSP \_ paquete no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERROR\_IPSEC\_DOSP\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-570">13927 (0x3667)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-570">13927 (0x3667)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-571">La protección DoS de IPsec recibió un paquete con un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-571">IPsec DoS Protection received an incorrectly formatted packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERROR en la \_ \_ \_ búsqueda de estado DOSP \_ de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERROR\_IPSEC\_DOSP\_STATE\_LOOKUP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-573">13928 (0x3668)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-573">13928 (0x3668)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-574">La protección de DoS de IPsec no pudo buscar el estado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-574">IPsec DoS Protection failed to look up state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**DOSP de ERROR de \_ \_ \_ entradas Max de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERROR\_IPSEC\_DOSP\_MAX\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-576">13929 (0x3669)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-576">13929 (0x3669)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-577">La protección de DoS de IPsec no pudo crear el estado porque se ha alcanzado el número máximo de entradas permitidas por la Directiva.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-577">IPsec DoS Protection failed to create state because the maximum number of entries allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERROR \_ IPSec \_ DOSP \_ KEYMOD \_ \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERROR\_IPSEC\_DOSP\_KEYMOD\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-579">13930 (0x366A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-579">13930 (0x366A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-580">La protección DoS de IPsec recibió un paquete de negociación IPsec para un módulo de creación de claves que no está permitido por la Directiva.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-580">IPsec DoS Protection received an IPsec negotiation packet for a keying module which is not allowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERROR \_ IPSec \_ DOSP \_ no \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERROR\_IPSEC\_DOSP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-582">13931 (0x366B)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-582">13931 (0x366B)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-583">No se ha habilitado la protección de DoS de IPsec.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-583">IPsec DoS Protection has not been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERROR de \_ IPSec \_ DOSP \_ Max \_ por \_ \_ \_ cola de RATELIMIT IP**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERROR\_IPSEC\_DOSP\_MAX\_PER\_IP\_RATELIMIT\_QUEUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-585">13932 (0x366C)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-585">13932 (0x366C)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-586">La protección de DoS de IPsec no pudo crear una cola de límite de tasa de IP por interno porque se ha alcanzado el número máximo de colas permitido por la Directiva.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-586">IPsec DoS Protection failed to create a per internal IP rate limit queue because the maximum number of queues allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**\_ \_ \_ no \_ se encontró la sección de error SxS**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**ERROR\_SXS\_SECTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-588">14000 (0x36B0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-588">14000 (0x36B0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-589">La sección solicitada no estaba presente en el contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-589">The requested section was not present in the activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERROR SxS no se pudo \_ \_ \_ gen \_ ACTCTX**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERROR\_SXS\_CANT\_GEN\_ACTCTX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-591">14001 (0x36B1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-591">14001 (0x36B1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-592">No se pudo iniciar la aplicación porque la configuración en paralelo es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-592">The application has failed to start because its side-by-side configuration is incorrect.</span></span> <span data-ttu-id="1b6f6-593">Vea el registro de eventos de la aplicación o use la herramienta de sxstrace.exe de línea de comandos para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-593">Please see the application event log or use the command-line sxstrace.exe tool for more detail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERROR \_ SxS \_ \_ ACTCTXDATA \_ formato no válido**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERROR\_SXS\_INVALID\_ACTCTXDATA\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-595">14002 (0x36B2)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-595">14002 (0x36B2)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-596">El formato de datos de enlace de la aplicación no es válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-596">The application binding data format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERROR \_ \_ \_ no \_ se encontró el ensamblado SxS**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-598">14003 (0x36B3)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-598">14003 (0x36B3)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-599">El ensamblado al que se hace referencia no está instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-599">The referenced assembly is not installed on your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**error \_ de \_ formato de manifiesto SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**ERROR\_SXS\_MANIFEST\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-601">14004 (0x36B4)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-601">14004 (0x36B4)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-602">El archivo de manifiesto no comienza con la información de formato y etiqueta necesaria.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-602">The manifest file does not begin with the required tag and format information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**error \_ de \_ análisis de manifiestos SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**ERROR\_SXS\_MANIFEST\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-604">14005 (0x36B5)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-604">14005 (0x36B5)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-605">El archivo de manifiesto contiene uno o varios errores de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-605">The manifest file contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERROR en el \_ \_ contexto de activación SxS \_ \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERROR\_SXS\_ACTIVATION\_CONTEXT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-607">14006 (0x36B6)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-607">14006 (0x36B6)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-608">La aplicación intentó activar un contexto de activación deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-608">The application attempted to activate a disabled activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**\_ \_ \_ no \_ se encontró la clave SxS**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERROR\_SXS\_KEY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-610">14007 (0x36B7)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-610">14007 (0x36B7)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-611">No se encontró la clave de búsqueda solicitada en ningún contexto de activación activo.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-611">The requested lookup key was not found in any active activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERROR \_ de \_ conflicto de versión de SxS \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERROR\_SXS\_VERSION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-613">14008 (0x36B8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-613">14008 (0x36B8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-614">Una versión de componente requerida por la aplicación entra en conflicto con otra versión de componente que ya está activa.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-614">A component version required by the application conflicts with another component version already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERROR \_ SxS \_ \_ tipo de sección incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERROR\_SXS\_WRONG\_SECTION\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-616">14009 (0x36B9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-616">14009 (0x36B9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-617">La sección de contexto de activación solicitado de tipo no coincide con la API de consulta utilizada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-617">The type requested activation context section does not match the query API used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERROR \_ SxS \_ consultas de subproceso \_ \_ deshabilitadas**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERROR\_SXS\_THREAD\_QUERIES\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-619">14010 (0x36BA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-619">14010 (0x36BA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-620">La falta de recursos del sistema requiere una activación aislada para deshabilitarse en el subproceso de ejecución actual.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-620">Lack of system resources has required isolated activation to be disabled for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERROR \_ el \_ valor predeterminado del proceso SxS \_ \_ ya está \_ establecido**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERROR\_SXS\_PROCESS\_DEFAULT\_ALREADY\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-622">14011 (0x36BB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-622">14011 (0x36BB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-623">Error al tratar de establecer el contexto de activación predeterminado del proceso porque el contexto de activación de proceso predeterminado ya estaba establecido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-623">An attempt to set the process default activation context failed because the process default activation context was already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERROR \_ SxS \_ \_ grupo de codificación desconocido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-625">14012 (0x36BC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-625">14012 (0x36BC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-626">No se reconoce el identificador de grupo de codificación especificado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-626">The encoding group identifier specified is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERROR \_ de \_ codificación SxS desconocida \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-628">14013 (0x36BD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-628">14013 (0x36BD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-629">No se reconoce la codificación solicitada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-629">The encoding requested is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERROR \_ SxS \_ \_ URI de \_ espacio de nombres XML no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERROR\_SXS\_INVALID\_XML\_NAMESPACE\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-631">14014 (0x36BE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-631">14014 (0x36BE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-632">El manifiesto contiene una referencia a un URI no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-632">The manifest contains a reference to an invalid URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERROR \_ de \_ dependencia del manifiesto raíz SxS \_ \_ \_ no \_ instalada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERROR\_SXS\_ROOT\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-634">14015 (0x36BF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-634">14015 (0x36BF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-635">El manifiesto de aplicación contiene una referencia a un ensamblado dependiente que no está instalado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-635">The application manifest contains a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERROR \_ de \_ dependencia de manifiesto de hoja \_ \_ \_ no \_ instalada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERROR\_SXS\_LEAF\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-637">14016 (0x36C0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-637">14016 (0x36C0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-638">El manifiesto de un ensamblado utilizado por la aplicación tiene una referencia a un ensamblado dependiente que no está instalado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-638">The manifest for an assembly used by the application has a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERROR \_ SxS \_ \_ atributo de identidad de ensamblado no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-640">14017 (0x36C1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-640">14017 (0x36C1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-641">El manifiesto contiene un atributo para la identidad del ensamblado que no es válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-641">The manifest contains an attribute for the assembly identity which is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**el \_ manifiesto de error SxS \_ falta el espacio de \_ \_ \_ nombres predeterminado necesario \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_MISSING\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-643">14018 (0x36C2)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-643">14018 (0x36C2)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-644">En el manifiesto falta la especificación de espacio de nombres predeterminada necesaria en el elemento de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-644">The manifest is missing the required default namespace specification on the assembly element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERROR \_ SxS \_ \_ no válido \_ requerido \_ \_ espacio de nombres predeterminado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_INVALID\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-646">14019 (0x36C3)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-646">14019 (0x36C3)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-647">El manifiesto tiene un espacio de nombres predeterminado especificado en el elemento de ensamblado, pero su valor no es "urn: schemas-microsoft-com: ASM. v1".</span><span class="sxs-lookup"><span data-stu-id="1b6f6-647">The manifest has a default namespace specified on the assembly element but its value is not "urn:schemas-microsoft-com:asm.v1".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERROR \_ \_ \_ \_ de ruta de acceso cruzada del manifiesto privado SxS \_ \_ con \_ punto de reanálisis \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERROR\_SXS\_PRIVATE\_MANIFEST\_CROSS\_PATH\_WITH\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-649">14020 (0x36C4)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-649">14020 (0x36C4)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-650">El manifiesto privado sondeado ha cruzado una ruta de acceso con un punto de reanálisis no admitido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-650">The private manifest probed has crossed a path with an unsupported reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERROR \_ SxS \_ Duplicate \_ dll \_ Name**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERROR\_SXS\_DUPLICATE\_DLL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-652">14021 (0x36C5)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-652">14021 (0x36C5)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-653">Dos o más componentes a los que hace referencia directa o indirectamente el manifiesto de aplicación tienen archivos con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-653">Two or more components referenced directly or indirectly by the application manifest have files by the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERROR \_ SxS \_ WINDOWCLASS duplicado \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERROR\_SXS\_DUPLICATE\_WINDOWCLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-655">14022 (0x36C6)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-655">14022 (0x36C6)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-656">Dos o más componentes a los que se hace referencia directa o indirectamente mediante el manifiesto de aplicación tienen clases de ventana con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-656">Two or more components referenced directly or indirectly by the application manifest have window classes with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERROR \_ SxS \_ duplicado de \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERROR\_SXS\_DUPLICATE\_CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-658">14023 (0x36C7)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-658">14023 (0x36C7)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-659">Dos o más componentes a los que se hace referencia directa o indirectamente mediante el manifiesto de aplicación tienen los mismos CLSID de servidor COM.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-659">Two or more components referenced directly or indirectly by the application manifest have the same COM server CLSIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERROR \_ SxS \_ duplicado de \_ IID**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERROR\_SXS\_DUPLICATE\_IID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-661">14024 (0x36C8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-661">14024 (0x36C8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-662">Dos o más componentes a los que se hace referencia directa o indirectamente mediante el manifiesto de aplicación tienen proxies para la misma interfaz COM IID.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-662">Two or more components referenced directly or indirectly by the application manifest have proxies for the same COM interface IIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERROR \_ SxS \_ duplicado \_ TLBID**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERROR\_SXS\_DUPLICATE\_TLBID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-664">14025 (0x36C9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-664">14025 (0x36C9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-665">Dos o más componentes a los que hace referencia directa o indirectamente el manifiesto de aplicación tienen la misma biblioteca de tipos COM TLBIDs.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-665">Two or more components referenced directly or indirectly by the application manifest have the same COM type library TLBIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERROR \_ SxS \_ Duplicate \_ ProgID**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERROR\_SXS\_DUPLICATE\_PROGID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-667">14026 (0x36CA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-667">14026 (0x36CA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-668">Dos o más componentes a los que se hace referencia directa o indirectamente mediante el manifiesto de aplicación tienen los mismos ProgID de COM.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-668">Two or more components referenced directly or indirectly by the application manifest have the same COM ProgIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERROR \_ SxS \_ \_ nombre de ensamblado duplicado \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERROR\_SXS\_DUPLICATE\_ASSEMBLY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-670">14027 (0x36CB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-670">14027 (0x36CB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-671">Dos o más componentes a los que se hace referencia directa o indirectamente mediante el manifiesto de aplicación son versiones diferentes del mismo componente, lo cual no está permitido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-671">Two or more components referenced directly or indirectly by the application manifest are different versions of the same component which is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERROR \_ de \_ hash de archivo SxS \_ \_ no coincidente**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERROR\_SXS\_FILE\_HASH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-673">14028 (0x36CC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-673">14028 (0x36CC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-674">El archivo de un componente no coincide con la información de comprobación presente en el manifiesto del componente.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-674">A component's file does not match the verification information present in the component manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**error \_ de \_ análisis de directiva SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**ERROR\_SXS\_POLICY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-676">14029 (0x36CD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-676">14029 (0x36CD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-677">El manifiesto de Directiva contiene uno o varios errores de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-677">The policy manifest contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERROR \_ SxS \_ XML \_ E \_ MISSINGQUOTE**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERROR\_SXS\_XML\_E\_MISSINGQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-679">14030 (0x36CE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-679">14030 (0x36CE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-680">Error de análisis de manifiesto: se esperaba un literal de cadena, pero no se encontró ningún carácter de comilla de apertura.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-680">Manifest Parse Error : A string literal was expected, but no opening quote character was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERROR \_ SxS \_ XML \_ E \_ COMMENTSYNTAX**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERROR\_SXS\_XML\_E\_COMMENTSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-682">14031 (0x36CF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-682">14031 (0x36CF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-683">Error de análisis de manifiesto: se usó una sintaxis incorrecta en un comentario.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-683">Manifest Parse Error : Incorrect syntax was used in a comment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERROR \_ SxS \_ XML \_ E \_ BADSTARTNAMECHAR**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERROR\_SXS\_XML\_E\_BADSTARTNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-685">14032 (0x36D0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-685">14032 (0x36D0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-686">Error de análisis de manifiesto: se ha iniciado un nombre con un carácter no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-686">Manifest Parse Error : A name was started with an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERROR \_ SxS \_ XML \_ E \_ BADNAMECHAR**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERROR\_SXS\_XML\_E\_BADNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-688">14033 (0x36D1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-688">14033 (0x36D1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-689">Error de análisis de manifiesto: un nombre contenía un carácter no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-689">Manifest Parse Error : A name contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERROR \_ SxS \_ XML \_ E \_ BADCHARINSTRING**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERROR\_SXS\_XML\_E\_BADCHARINSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-691">14034 (0x36D2)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-691">14034 (0x36D2)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-692">Error de análisis de manifiesto: un literal de cadena contenía un carácter no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-692">Manifest Parse Error : A string literal contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERROR \_ SxS \_ XML \_ E \_ XMLDECLSYNTAX**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERROR\_SXS\_XML\_E\_XMLDECLSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-694">14035 (0x36D3)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-694">14035 (0x36D3)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-695">Error de análisis de manifiesto: sintaxis no válida para una declaración XML.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-695">Manifest Parse Error : Invalid syntax for an xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERROR \_ SxS \_ XML \_ E \_ BADCHARDATA**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERROR\_SXS\_XML\_E\_BADCHARDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-697">14036 (0x36D4)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-697">14036 (0x36D4)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-698">Error de análisis de manifiesto: se encontró un carácter no válido en el contenido de texto.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-698">Manifest Parse Error : An Invalid character was found in text content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERROR \_ SxS \_ XML \_ E \_ MISSINGWHITESPACE**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERROR\_SXS\_XML\_E\_MISSINGWHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-700">14037 (0x36D5)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-700">14037 (0x36D5)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-701">Error de análisis de manifiesto: falta el espacio en blanco necesario.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-701">Manifest Parse Error : Required white space was missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERROR \_ SxS \_ XML \_ E \_ EXPECTINGTAGEND**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGTAGEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-703">14038 (0x36D6)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-703">14038 (0x36D6)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-704">Error de análisis de manifiesto: se esperaba el carácter ' > '.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-704">Manifest Parse Error : The character '>' was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERROR \_ SxS \_ XML \_ E \_ MISSINGSEMICOLON**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERROR\_SXS\_XML\_E\_MISSINGSEMICOLON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-706">14039 (0x36D7)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-706">14039 (0x36D7)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-707">Error de análisis de manifiesto: se esperaba un carácter de punto y coma.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-707">Manifest Parse Error : A semi colon character was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERROR \_ SxS \_ XML \_ E \_ UNBALANCEDPAREN**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERROR\_SXS\_XML\_E\_UNBALANCEDPAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-709">14040 (0x36D8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-709">14040 (0x36D8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-710">Error de análisis de manifiesto: paréntesis desequilibrados.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-710">Manifest Parse Error : Unbalanced parentheses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERROR \_ SxS \_ XML \_ E \_ INTERNALERROR**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERROR\_SXS\_XML\_E\_INTERNALERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-712">14041 (0x36D9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-712">14041 (0x36D9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-713">Error de análisis de manifiesto: error interno.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-713">Manifest Parse Error : Internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERROR \_ SxS \_ XML \_ E \_ espacio en blanco inesperado \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_WHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-715">14042 (0x36DA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-715">14042 (0x36DA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-716">Error de análisis de manifiesto: no se permite un espacio en blanco en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-716">Manifest Parse Error : Whitespace is not allowed at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERROR \_ de \_ codificación SxS XML \_ E \_ incompleta \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERROR\_SXS\_XML\_E\_INCOMPLETE\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-718">14043 (0x36DB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-718">14043 (0x36DB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-719">Error de análisis de manifiesto: se alcanzó el final del archivo en un estado no válido para la codificación actual.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-719">Manifest Parse Error : End of file reached in invalid state for current encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERROR \_ SxS \_ XML \_ E \_ falta el \_ paréntesis**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERROR\_SXS\_XML\_E\_MISSING\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-721">14044 (0x36DC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-721">14044 (0x36DC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-722">Error de análisis de manifiesto: faltan paréntesis.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-722">Manifest Parse Error : Missing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERROR \_ SxS \_ XML \_ E \_ EXPECTINGCLOSEQUOTE**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGCLOSEQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-724">14045 (0x36DD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-724">14045 (0x36DD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-725">Error de análisis de manifiesto: falta un carácter de comilla simple o doble ( \\ ' o ' \\ ).</span><span class="sxs-lookup"><span data-stu-id="1b6f6-725">Manifest Parse Error : A single or double closing quote character (\\' or \\") is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERROR \_ SxS \_ XML \_ E \_ varios \_ signos de dos puntos**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERROR\_SXS\_XML\_E\_MULTIPLE\_COLONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-727">14046 (0x36DE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-727">14046 (0x36DE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-728">Error de análisis de manifiesto: no se permiten varios signos de dos puntos en un nombre.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-728">Manifest Parse Error : Multiple colons are not allowed in a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERROR \_ SxS \_ XML \_ E \_ decimal no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_DECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-730">14047 (0x36DF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-730">14047 (0x36DF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-731">Error de análisis de manifiesto: carácter no válido para el dígito decimal.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-731">Manifest Parse Error : Invalid character for decimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERROR \_ SxS \_ XML \_ E \_ hexadecimal no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_HEXIDECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-733">14048 (0x36E0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-733">14048 (0x36E0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-734">Error de análisis de manifiesto: carácter no válido para el dígito hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-734">Manifest Parse Error : Invalid character for hexadecimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERROR \_ SxS \_ XML \_ E \_ \_ Unicode no válido**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERROR\_SXS\_XML\_E\_INVALID\_UNICODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-736">14049 (0x36E1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-736">14049 (0x36E1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-737">Error de análisis de manifiesto: valor de carácter Unicode no válido para esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-737">Manifest Parse Error : Invalid unicode character value for this platform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERROR \_ SxS \_ XML \_ E \_ WHITESPACEORQUESTIONMARK**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERROR\_SXS\_XML\_E\_WHITESPACEORQUESTIONMARK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-739">14050 (0x36E2)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-739">14050 (0x36E2)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-740">Error de análisis de manifiesto: se esperaba un espacio en blanco o '? '.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-740">Manifest Parse Error : Expecting whitespace or '?'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERROR \_ SxS \_ XML \_ E \_ UNEXPECTEDENDTAG**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-742">14051 (0x36E3)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-742">14051 (0x36E3)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-743">Error de análisis de manifiesto: no se esperaba una etiqueta de cierre en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-743">Manifest Parse Error : End tag was not expected at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDTAG**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-745">14052 (0x36E4)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-745">14052 (0x36E4)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-746">Error de análisis de manifiesto: no se cerraron las siguientes etiquetas: %1.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-746">Manifest Parse Error : The following tags were not closed: %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERROR \_ SxS \_ XML \_ E \_ DUPLICATEATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERROR\_SXS\_XML\_E\_DUPLICATEATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-748">14053 (0x36E5)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-748">14053 (0x36E5)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-749">Error de análisis de manifiesto: atributo duplicado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-749">Manifest Parse Error : Duplicate attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERROR \_ SxS \_ XML \_ E \_ MULTIPLEROOTS**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERROR\_SXS\_XML\_E\_MULTIPLEROOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-751">14054 (0x36E6)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-751">14054 (0x36E6)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-752">Error de análisis de manifiesto: solo se permite un elemento de nivel superior en un documento XML.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-752">Manifest Parse Error : Only one top level element is allowed in an XML document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERROR \_ SxS \_ XML \_ E \_ INVALIDATROOTLEVEL**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERROR\_SXS\_XML\_E\_INVALIDATROOTLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-754">14055 (0x36E7)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-754">14055 (0x36E7)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-755">Error de análisis de manifiesto: no válido en el nivel superior del documento.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-755">Manifest Parse Error : Invalid at the top level of the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERROR \_ SxS \_ XML \_ E \_ BADXMLDECL**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERROR\_SXS\_XML\_E\_BADXMLDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-757">14056 (0x36E8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-757">14056 (0x36E8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-758">Error de análisis de manifiesto: declaración XML no válida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-758">Manifest Parse Error : Invalid xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERROR \_ SxS \_ XML \_ E \_ MISSINGROOT**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERROR\_SXS\_XML\_E\_MISSINGROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-760">14057 (0x36E9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-760">14057 (0x36E9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-761">Error de análisis de manifiesto: el documento XML debe tener un elemento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-761">Manifest Parse Error : XML document must have a top level element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERROR \_ SxS \_ XML \_ E \_ UNEXPECTEDEOF**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDEOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-763">14058 (0x36EA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-763">14058 (0x36EA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-764">Error de análisis de manifiesto: final de archivo inesperado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-764">Manifest Parse Error : Unexpected end of file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERROR \_ SxS \_ XML \_ E \_ BADPEREFINSUBSET**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERROR\_SXS\_XML\_E\_BADPEREFINSUBSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-766">14059 (0x36EB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-766">14059 (0x36EB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-767">Error de análisis de manifiesto: no se pueden usar entidades de parámetro dentro de las declaraciones de marcado de un subconjunto interno.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-767">Manifest Parse Error : Parameter entities cannot be used inside markup declarations in an internal subset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDSTARTTAG**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTARTTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-769">14060 (0x36EC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-769">14060 (0x36EC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-770">Error de análisis de manifiesto: el elemento no se cerró.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-770">Manifest Parse Error : Element was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDENDTAG**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-772">14061 (0x36ED)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-772">14061 (0x36ED)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-773">Error en el análisis del manifiesto: falta el carácter ' > ' en el elemento final.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-773">Manifest Parse Error : End element was missing the character '>'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDSTRING**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-775">14062 (0x36EE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-775">14062 (0x36EE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-776">Error de análisis de manifiesto: no se cerró un literal de cadena.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-776">Manifest Parse Error : A string literal was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDCOMMENT**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCOMMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-778">14063 (0x36EF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-778">14063 (0x36EF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-779">Error de análisis de manifiesto: no se cerró un comentario.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-779">Manifest Parse Error : A comment was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDDECL**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-781">14064 (0x36F0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-781">14064 (0x36F0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-782">Error de análisis de manifiesto: no se cerró una declaración.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-782">Manifest Parse Error : A declaration was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDCDATA**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-784">14065 (0x36F1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-784">14065 (0x36F1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-785">Error de análisis de manifiesto: no se cerró una sección CDATA.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-785">Manifest Parse Error : A CDATA section was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERROR \_ SxS \_ XML \_ E \_ RESERVEDNAMESPACE**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERROR\_SXS\_XML\_E\_RESERVEDNAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-787">14066 (0x36F2)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-787">14066 (0x36F2)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-788">Error de análisis de manifiesto: el prefijo de espacio de nombres no puede comenzar con la cadena reservada "XML".</span><span class="sxs-lookup"><span data-stu-id="1b6f6-788">Manifest Parse Error : The namespace prefix is not allowed to start with the reserved string "xml".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERROR \_ SxS \_ XML \_ E \_ INVALIDENCODING**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERROR\_SXS\_XML\_E\_INVALIDENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-790">14067 (0x36F3)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-790">14067 (0x36F3)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-791">Error de análisis de manifiesto: el sistema no admite la codificación especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-791">Manifest Parse Error : System does not support the specified encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERROR \_ SxS \_ XML \_ E \_ INVALIDSWITCH**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERROR\_SXS\_XML\_E\_INVALIDSWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-793">14068 (0x36F4)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-793">14068 (0x36F4)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-794">Error de análisis de manifiesto: no se admite el cambio de la codificación actual a la codificación especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-794">Manifest Parse Error : Switch from current encoding to specified encoding not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERROR \_ SxS \_ XML \_ E \_ BADXMLCASE**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERROR\_SXS\_XML\_E\_BADXMLCASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-796">14069 (0x36F5)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-796">14069 (0x36F5)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-797">Error de análisis de manifiesto: el nombre ' XML ' está reservado y debe estar en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-797">Manifest Parse Error : The name 'xml' is reserved and must be lower case.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERROR \_ SxS \_ XML \_ E \_ independiente no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERROR\_SXS\_XML\_E\_INVALID\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-799">14070 (0x36F6)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-799">14070 (0x36F6)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-800">Error de análisis de manifiesto: el atributo Standalone debe tener el valor ' Yes ' o ' no '.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-800">Manifest Parse Error : The standalone attribute must have the value 'yes' or 'no'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERROR \_ SxS \_ XML \_ E \_ inesperado \_ independiente**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-802">14071 (0x36F7)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-802">14071 (0x36F7)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-803">Error de análisis de manifiesto: no se puede usar el atributo independiente en entidades externas.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-803">Manifest Parse Error : The standalone attribute cannot be used in external entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERROR \_ de \_ versión de XML SxS \_ E \_ no válida \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERROR\_SXS\_XML\_E\_INVALID\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-805">14072 (0x36F8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-805">14072 (0x36F8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-806">Error de análisis de manifiesto: número de versión no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-806">Manifest Parse Error : Invalid version number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERROR \_ SxS \_ XML \_ E \_ MISSINGEQUALS**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERROR\_SXS\_XML\_E\_MISSINGEQUALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-808">14073 (0x36F9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-808">14073 (0x36F9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-809">Error de análisis de manifiesto: falta el signo igual entre el atributo y el valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-809">Manifest Parse Error : Missing equals sign between attribute and attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERROR \_ de \_ recuperación de protección SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERROR\_SXS\_PROTECTION\_RECOVERY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-811">14074 (0x36FA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-811">14074 (0x36FA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-812">Error de protección del ensamblado: no se puede recuperar el ensamblado especificado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-812">Assembly Protection Error : Unable to recover the specified assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERROR \_ SxS: la \_ \_ \_ clave pública \_ es demasiado \_ corta**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERROR\_SXS\_PROTECTION\_PUBLIC\_KEY\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-814">14075 (0x36FB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-814">14075 (0x36FB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-815">Error de protección del ensamblado: la clave pública para un ensamblado era demasiado corta para permitirse.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-815">Assembly Protection Error : The public key for an assembly was too short to be allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERROR \_ de \_ Catálogo de protección SxS \_ \_ no \_ válido**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-817">14076 (0x36FC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-817">14076 (0x36FC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-818">Error de protección del ensamblado: el catálogo de un ensamblado no es válido o no coincide con el manifiesto del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-818">Assembly Protection Error : The catalog for an assembly is not valid, or does not match the assembly's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERROR SxS no traducible que se va a \_ \_ traducir \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERROR\_SXS\_UNTRANSLATABLE\_HRESULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-820">14077 (0x36FD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-820">14077 (0x36FD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-821">No se pudo traducir un valor HRESULT a un código de error de Win32 correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-821">An HRESULT could not be translated to a corresponding Win32 error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERROR \_ SxS \_ \_ falta el archivo de catálogo de protección \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_FILE\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-823">14078 (0x36FE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-823">14078 (0x36FE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-824">Error de protección del ensamblado: falta el catálogo de un ensamblado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-824">Assembly Protection Error : The catalog for an assembly is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERROR \_ SxS \_ falta \_ el \_ atributo de identidad de ensamblado \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERROR\_SXS\_MISSING\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-826">14079 (0x36FF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-826">14079 (0x36FF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-827">En la identidad del ensamblado proporcionado faltan uno o varios atributos que deben estar presentes en este contexto.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-827">The supplied assembly identity is missing one or more attributes which must be present in this context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERROR \_ SxS \_ \_ nombre de \_ atributo de identidad de ensamblado no \_ válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-829">14080 (0x3700)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-829">14080 (0x3700)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-830">La identidad del ensamblado proporcionada tiene uno o más nombres de atributo que contienen caracteres no permitidos en los nombres XML.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-830">The supplied assembly identity has one or more attribute names that contain characters not permitted in XML names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERROR \_ \_ no se encuentra el ensamblado SxS \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERROR\_SXS\_ASSEMBLY\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-832">14081 (0x3701)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-832">14081 (0x3701)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-833">No se pudo encontrar el ensamblado al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-833">The referenced assembly could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERROR \_ de \_ \_ pila de activación dañada SxS \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERROR\_SXS\_CORRUPT\_ACTIVATION\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-835">14082 (0x3702)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-835">14082 (0x3702)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-836">La pila de activación del contexto de activación para el subproceso de ejecución en ejecución está dañada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-836">The activation context activation stack for the running thread of execution is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERROR \_ de \_ daños en SxS**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERROR\_SXS\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-838">14083 (0x3703)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-838">14083 (0x3703)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-839">Los metadatos de aislamiento de la aplicación para este proceso o subproceso se han dañado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-839">The application isolation metadata for this process or thread has become corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERROR \_ de \_ \_ desactivación temprana de SxS**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERROR\_SXS\_EARLY\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-841">14084 (0x3704)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-841">14084 (0x3704)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-842">El contexto de activación que se está desactivando no es el que se activó más recientemente.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-842">The activation context being deactivated is not the most recently activated one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERROR \_ SxS \_ \_ desactivación no válida**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERROR\_SXS\_INVALID\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-844">14085 (0x3705)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-844">14085 (0x3705)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-845">El contexto de activación que se está desactivando no está activo para el subproceso de ejecución actual.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-845">The activation context being deactivated is not active for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERROR \_ de \_ \_ desactivación múltiple SxS**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERROR\_SXS\_MULTIPLE\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-847">14086 (0x3706)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-847">14086 (0x3706)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-848">El contexto de activación que se está desactivando ya se ha desactivado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-848">The activation context being deactivated has already been deactivated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERROR \_ de \_ terminación de proceso SxS \_ \_ solicitada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERROR\_SXS\_PROCESS\_TERMINATION\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-850">14087 (0x3707)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-850">14087 (0x3707)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-851">Un componente usado por la utilidad de aislamiento ha solicitado terminar el proceso.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-851">A component used by the isolation facility has requested to terminate the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERROR \_ SxS \_ : \_ contexto de activación de versión \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERROR\_SXS\_RELEASE\_ACTIVATION\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-853">14088 (0x3708)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-853">14088 (0x3708)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-854">Un componente de modo kernel está liberando una referencia en un contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-854">A kernel mode component is releasing a reference on an activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERROR \_ de \_ \_ contexto de activación predeterminado del sistema SxS \_ \_ \_ vacío**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERROR\_SXS\_SYSTEM\_DEFAULT\_ACTIVATION\_CONTEXT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-856">14089 (0x3709)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-856">14089 (0x3709)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-857">No se pudo generar el contexto de activación del ensamblado predeterminado del sistema.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-857">The activation context of system default assembly could not be generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERROR \_ SxS \_ \_ valor de \_ atributo de identidad no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-859">14090 (0x370A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-859">14090 (0x370A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-860">El valor de un atributo de una identidad no está dentro del intervalo legal.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-860">The value of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERROR \_ SxS \_ \_ nombre de \_ atributo de identidad no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-862">14091 (0x370B)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-862">14091 (0x370B)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-863">El nombre de un atributo de una identidad no está dentro del intervalo legal.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-863">The name of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERROR \_ de \_ \_ atributo duplicado de identidad SxS \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERROR\_SXS\_IDENTITY\_DUPLICATE\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-865">14092 (0x370C)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-865">14092 (0x370C)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-866">Una identidad contiene dos definiciones para el mismo atributo.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-866">An identity contains two definitions for the same attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**error \_ de \_ análisis de identidad SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERROR\_SXS\_IDENTITY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-868">14093 (0x370D)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-868">14093 (0x370D)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-869">La cadena de identidad tiene un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-869">The identity string is malformed.</span></span> <span data-ttu-id="1b6f6-870">Esto puede deberse a una coma final, a más de dos atributos sin nombre, que falta el nombre del atributo o que falta un valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-870">This may be due to a trailing comma, more than two unnamed attributes, missing attribute name or missing attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERROR de \_ cadena de sustitución con formato incorrecto \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERROR\_MALFORMED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-872">14094 (0x370E)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-872">14094 (0x370E)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-873">Una cadena que contiene contenido sustituible localizado tenía un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-873">A string containing localized substitutable content was malformed.</span></span> <span data-ttu-id="1b6f6-874">No se encontró un signo de dólar ($) seguido de un paréntesis de apertura o de otro signo de dólar o de un paréntesis derecho de sustitución.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-874">Either a dollar sign ($) was followed by something other than a left parenthesis or another dollar sign or an substitution's right parenthesis was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERROR \_ de \_ \_ token de \_ clave \_ pública incorrecto SxS**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERROR\_SXS\_INCORRECT\_PUBLIC\_KEY\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-876">14095 (0x370F)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-876">14095 (0x370F)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-877">El token de clave pública no se corresponde con la clave pública especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-877">The public key token does not correspond to the public key specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERROR de \_ cadena de sustitución no asignada \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERROR\_UNMAPPED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-879">14096 (0x3710)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-879">14096 (0x3710)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-880">Una cadena de sustitución no tiene ninguna asignación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-880">A substitution string had no mapping.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERROR \_ de \_ ensamblado SxS \_ no \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-882">14097 (0x3711)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-882">14097 (0x3711)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-883">El componente debe estar bloqueado antes de realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-883">The component must be locked before making the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERROR \_ SxS \_ almacén de componentes \_ \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERROR\_SXS\_COMPONENT\_STORE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-885">14098 (0x3712)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-885">14098 (0x3712)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-886">El almacén de componentes está dañado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-886">The component store has been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERROR \_ de \_ instalador \_ avanzado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERROR\_ADVANCED\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-888">14099 (0x3713)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-888">14099 (0x3713)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-889">Error de un instalador avanzado durante la instalación o el servicio.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-889">An advanced installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERROR \_ de \_ coincidencia de codificación XML \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERROR\_XML\_ENCODING\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-891">14100 (0x3714)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-891">14100 (0x3714)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-892">La codificación de caracteres en la declaración XML no coincidía con la codificación utilizada en el documento.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-892">The character encoding in the XML declaration did not match the encoding used in the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERROR en la \_ identidad del manifiesto SxS, \_ pero el contenido es \_ \_ \_ \_ \_ diferente**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERROR\_SXS\_MANIFEST\_IDENTITY\_SAME\_BUT\_CONTENTS\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-894">14101 (0x3715)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-894">14101 (0x3715)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-895">Las identidades de los manifiestos son idénticas, pero su contenido es diferente.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-895">The identities of the manifests are identical but their contents are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERROR \_ de \_ identidades SxS \_ diferentes**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERROR\_SXS\_IDENTITIES\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-897">14102 (0x3716)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-897">14102 (0x3716)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-898">Las identidades de los componentes son diferentes.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-898">The component identities are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**\_el error SxS \_ Assembly \_ no es \_ \_ una \_ implementación**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**ERROR\_SXS\_ASSEMBLY\_IS\_NOT\_A\_DEPLOYMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-900">14103 (0x3717)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-900">14103 (0x3717)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-901">El ensamblado no es una implementación de.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-901">The assembly is not a deployment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERROR \_ \_ de archivo SxS que \_ no \_ forma parte \_ del \_ ensamblado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERROR\_SXS\_FILE\_NOT\_PART\_OF\_ASSEMBLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-903">14104 (0x3718)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-903">14104 (0x3718)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-904">El archivo no forma parte del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-904">The file is not a part of the assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**el \_ manifiesto de error SxS \_ \_ es demasiado \_ grande**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**ERROR\_SXS\_MANIFEST\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-906">14105 (0x3719)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-906">14105 (0x3719)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-907">El tamaño del manifiesto supera el máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-907">The size of the manifest exceeds the maximum allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERROR \_ de \_ configuración de SxS \_ no \_ registrada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERROR\_SXS\_SETTING\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-909">14106 (0x371A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-909">14106 (0x371A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-910">La configuración no está registrada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-910">The setting is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERROR \_ de \_ cierre de transacción SxS \_ \_ incompleto**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERROR\_SXS\_TRANSACTION\_CLOSURE\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-912">14107 (0x371B)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-912">14107 (0x371B)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-913">Uno o varios miembros necesarios de la transacción no están presentes.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-913">One or more required members of the transaction are not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERROR en el \_ \_ \_ instalador \_ primitivo de SMI**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERROR\_SMI\_PRIMITIVE\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-915">14108 (0x371C)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-915">14108 (0x371C)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-916">Error del instalador primitivo de SMI durante la instalación o el servicio.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-916">The SMI primitive installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERROR \_ de \_ comando genérico \_ erróneo**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERROR\_GENERIC\_COMMAND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-918">14109 (0x371D)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-918">14109 (0x371D)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-919">Un ejecutable de comando genérico devolvió un resultado que indica un error.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-919">A generic command executable returned a result that indicates failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERROR \_ de \_ hash de archivo SxS \_ \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERROR\_SXS\_FILE\_HASH\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-921">14110 (0x371E)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-921">14110 (0x371E)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-922">Falta la información de comprobación de archivos en un componente en su manifiesto.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-922">A component is missing file verification information in its manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR \_ evt \_ \_ ruta de acceso de canal no válida \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-924">15000 (0x3A98)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-924">15000 (0x3A98)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-925">La ruta de acceso del canal especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-925">The specified channel path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR \_ evt \_ consulta no válida \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR\_EVT\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-927">15001 (0x3A99)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-927">15001 (0x3A99)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-928">La consulta especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-928">The specified query is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR \_ evt \_ metadatos del publicador \_ \_ no \_ encontrados**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR\_EVT\_PUBLISHER\_METADATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-930">15002 (0x3A9A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-930">15002 (0x3A9A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-931">No se encuentran los metadatos del publicador en el recurso.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-931">The publisher metadata cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR \_ : \_ \_ \_ no \_ se encontró la plantilla de evento evt**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR\_EVT\_EVENT\_TEMPLATE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-933">15003 (0x3A9B)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-933">15003 (0x3A9B)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-934">No se encuentra la plantilla para una definición de evento en el recurso (error = %1).</span><span class="sxs-lookup"><span data-stu-id="1b6f6-934">The template for an event definition cannot be found in the resource (error = %1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR \_ evt \_ \_ nombre de publicador no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-936">15004 (0x3A9C)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-936">15004 (0x3A9C)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-937">El nombre del publicador especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-937">The specified publisher name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR \_ evt \_ \_ datos de evento no válidos \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR\_EVT\_INVALID\_EVENT\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-939">15005 (0x3A9D)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-939">15005 (0x3A9D)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-940">Los datos de evento generados por el publicador no son compatibles con la definición de la plantilla de evento en el manifiesto del publicador.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-940">The event data raised by the publisher is not compatible with the event template definition in the publisher's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR \_ : \_ \_ no \_ se encontró el canal evt**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR\_EVT\_CHANNEL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-942">15007 (0x3A9F)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-942">15007 (0x3A9F)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-943">No se pudo encontrar el canal especificado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-943">The specified channel could not be found.</span></span> <span data-ttu-id="1b6f6-944">Compruebe la configuración del canal.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-944">Check channel configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR \_ evt de \_ \_ texto XML con formato incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR\_EVT\_MALFORMED\_XML\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-946">15008 (0x3AA0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-946">15008 (0x3AA0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-947">El texto XML especificado no tiene el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-947">The specified xml text was not well-formed.</span></span> <span data-ttu-id="1b6f6-948">Vea error extendido para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-948">See Extended Error for more details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR \_ \_ de suscripción \_ de EVT a \_ \_ canal directo**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR\_EVT\_SUBSCRIPTION\_TO\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-950">15009 (0x3AA1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-950">15009 (0x3AA1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-951">El autor de la llamada está intentando suscribirse a un canal directo que no está permitido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-951">The caller is trying to subscribe to a direct channel which is not allowed.</span></span> <span data-ttu-id="1b6f6-952">Los eventos de un canal directo van directamente a un archivo de registro y no se pueden suscribir.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-952">The events for a direct channel go directly to a logfile and cannot be subscribed to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**error \_ : \_ error de configuración de EVT \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERROR\_EVT\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-954">15010 (0x3AA2)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-954">15010 (0x3AA2)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-955">Error de configuración.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-955">Configuration error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR \_ de \_ consulta evt \_ resultado \_ obsoleto**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR\_EVT\_QUERY\_RESULT\_STALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-957">15011 (0x3AA3)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-957">15011 (0x3AA3)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-958">El resultado de la consulta es obsoleto o no es válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-958">The query result is stale / invalid.</span></span> <span data-ttu-id="1b6f6-959">Esto puede deberse a que el registro se borra o se revierte una vez creado el resultado de la consulta.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-959">This may be due to the log being cleared or rolling over after the query result was created.</span></span> <span data-ttu-id="1b6f6-960">Los usuarios deben controlar este código liberando el objeto de resultado de la consulta y reemitiendo la consulta.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-960">Users should handle this code by releasing the query result object and reissuing the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR \_ : \_ \_ \_ posición no válida del resultado de la consulta evt \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR\_EVT\_QUERY\_RESULT\_INVALID\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-962">15012 (0x3AA4)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-962">15012 (0x3AA4)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-963">El resultado de la consulta se encuentra actualmente en una posición no válida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-963">Query result is currently at an invalid position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR \_ evt \_ no \_ validando \_ MSXML**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR\_EVT\_NON\_VALIDATING\_MSXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-965">15013 (0x3AA5)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-965">15013 (0x3AA5)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-966">El MSXML registrado no admite la validación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-966">Registered MSXML doesn't support validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR \_ evt \_ filtro \_ ALREADYSCOPED**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR\_EVT\_FILTER\_ALREADYSCOPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-968">15014 (0x3AA6)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-968">15014 (0x3AA6)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-969">Una expresión solo puede ir seguida de un cambio de operación de ámbito si se evalúa en sí misma como un conjunto de nodos y aún no forma parte de otro cambio de operación de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-969">An expression can only be followed by a change of scope operation if it itself evaluates to a node set and is not already part of some other change of scope operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR \_ evt \_ filtro \_ NOTELTSET**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR\_EVT\_FILTER\_NOTELTSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-971">15015 (0x3AA7)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-971">15015 (0x3AA7)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-972">No se puede realizar una operación Step desde un término que no representa un conjunto de elementos.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-972">Can't perform a step operation from a term that does not represent an element set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR \_ evt \_ filtro \_ INVARG**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR\_EVT\_FILTER\_INVARG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-974">15016 (0x3AA8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-974">15016 (0x3AA8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-975">Los argumentos del lado izquierdo de los operadores binarios deben ser atributos, nodos o variables y los argumentos del lado derecho deben ser constantes.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-975">Left hand side arguments to binary operators must be either attributes, nodes or variables and right hand side arguments must be constants.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR \_ evt \_ filtro \_ INVTEST**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR\_EVT\_FILTER\_INVTEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-977">15017 (0x3AA9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-977">15017 (0x3AA9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-978">Una operación Step debe implicar una prueba de nodo o, en el caso de un predicado, una expresión algebraica en la que probar cada nodo en el conjunto de nodos identificado por el conjunto de nodos anterior se puede evaluar.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-978">A step operation must involve either a node test or, in the case of a predicate, an algebraic expression against which to test each node in the node set identified by the preceeding node set can be evaluated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR \_ evt \_ filtro \_ INVTYPE**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR\_EVT\_FILTER\_INVTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-980">15018 (0x3AAA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-980">15018 (0x3AAA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-981">Este tipo de datos no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-981">This data type is currently unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR \_ evt \_ filtro \_ PARSEERR**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR\_EVT\_FILTER\_PARSEERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-983">15019 (0x3AAB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-983">15019 (0x3AAB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-984">Error de sintaxis en la posición %1! d!.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-984">A syntax error occurred at position %1!d!.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR \_ evt \_ filtro \_ UNSUPPORTEDOP**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR\_EVT\_FILTER\_UNSUPPORTEDOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-986">15020 (0x3AAC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-986">15020 (0x3AAC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-987">Este operador no es compatible con esta implementación del filtro.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-987">This operator is unsupported by this implementation of the filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR \_ evt \_ filtro \_ UNEXPECTEDTOKEN**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR\_EVT\_FILTER\_UNEXPECTEDTOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-989">15021 (0x3AAD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-989">15021 (0x3AAD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-990">El token encontrado era inesperado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-990">The token encountered was unexpected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR \_ evt \_ operación no válida \_ \_ en el \_ \_ canal directo habilitado \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR\_EVT\_INVALID\_OPERATION\_OVER\_ENABLED\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-992">15022 (0x3AAE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-992">15022 (0x3AAE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-993">La operación solicitada no se puede realizar a través de un canal directo habilitado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-993">The requested operation cannot be performed over an enabled direct channel.</span></span> <span data-ttu-id="1b6f6-994">Primero debe deshabilitarse el canal antes de realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-994">The channel must first be disabled before performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR \_ evt \_ \_ valor de \_ propiedad de canal no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-996">15023 (0x3AAF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-996">15023 (0x3AAF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-997">Propiedad de canal %1! s!</span><span class="sxs-lookup"><span data-stu-id="1b6f6-997">Channel property %1!s!</span></span> <span data-ttu-id="1b6f6-998">contiene un valor no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-998">contains invalid value.</span></span> <span data-ttu-id="1b6f6-999">El valor tiene un tipo no válido, está fuera del intervalo válido, no se puede actualizar o no es compatible con este tipo de canal.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-999">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR \_ evt \_ \_ valor de propiedad de publicador no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1001">15024 (0x3AB0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1001">15024 (0x3AB0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1002">Propiedad del publicador %1! s!</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1002">Publisher property %1!s!</span></span> <span data-ttu-id="1b6f6-1003">contiene un valor no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1003">contains invalid value.</span></span> <span data-ttu-id="1b6f6-1004">El valor tiene un tipo no válido, está fuera del intervalo válido, no se puede actualizar o no es compatible con este tipo de publicador.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1004">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR: el \_ \_ canal evt \_ no se puede \_ activar**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR\_EVT\_CHANNEL\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1006">15025 (0x3AB1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1006">15025 (0x3AB1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1007">No se puede activar el canal.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1007">The channel fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR \_ : \_ filtro evt \_ demasiado \_ complejo**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR\_EVT\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1009">15026 (0x3AB2)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1009">15026 (0x3AB2)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1010">La expresión XPath superó la complejidad admitida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1010">The xpath expression exceeded supported complexity.</span></span> <span data-ttu-id="1b6f6-1011">Symplify o divídalo en dos o más expresiones simples.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1011">Please symplify it or split it into two or more simple expressions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR \_ : \_ mensaje evt \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR\_EVT\_MESSAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1013">15027 (0x3AB3)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1013">15027 (0x3AB3)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1014">el recurso de mensaje está presente pero el mensaje no se encuentra en la tabla de cadena/mensaje.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1014">the message resource is present but the message is not found in the string/message table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR \_ : \_ \_ \_ no \_ se encontró el identificador de mensaje evt**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR\_EVT\_MESSAGE\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1016">15028 (0x3AB4)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1016">15028 (0x3AB4)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1017">No se pudo encontrar el ID. de mensaje para el mensaje deseado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1017">The message id for the desired message could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR \_ evt: \_ inserción de \_ valor sin resolver \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR\_EVT\_UNRESOLVED\_VALUE\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1019">15029 (0x3AB5)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1019">15029 (0x3AB5)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1020">No se encontró la cadena de sustitución para insertar índice (%1).</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1020">The substitution string for insert index (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR \_ evt: \_ inserción de \_ parámetro sin resolver \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR\_EVT\_UNRESOLVED\_PARAMETER\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1022">15030 (0x3AB6)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1022">15030 (0x3AB6)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1023">No se pudo encontrar la cadena de descripción para la referencia de parámetro (%1).</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1023">The description string for parameter reference (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR \_ evt se \_ alcanzó el número máximo de \_ inserciones \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR\_EVT\_MAX\_INSERTS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1025">15031 (0x3AB7)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1025">15031 (0x3AB7)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1026">Se ha alcanzado el número máximo de reemplazos.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1026">The maximum number of replacements has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR \_ : \_ \_ \_ no \_ se encontró la definición del evento evt**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR\_EVT\_EVENT\_DEFINITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1028">15032 (0x3AB8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1028">15032 (0x3AB8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1029">No se encontró la definición de evento para el ID. de evento (%1).</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1029">The event definition could not be found for event id (%1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR \_ : \_ \_ \_ no \_ se encontró la configuración regional del mensaje evt**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR\_EVT\_MESSAGE\_LOCALE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1031">15033 (0x3AB9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1031">15033 (0x3AB9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1032">El recurso específico de configuración regional para el mensaje deseado no está presente.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1032">The locale specific resource for the desired message is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR \_ evt \_ versión \_ demasiado \_ antigua**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR\_EVT\_VERSION\_TOO\_OLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1034">15034 (0x3ABA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1034">15034 (0x3ABA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1035">El recurso es demasiado antiguo para ser compatible.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1035">The resource is too old to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR \_ evt \_ versión \_ demasiado \_ nueva**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR\_EVT\_VERSION\_TOO\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1037">15035 (0x3ABB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1037">15035 (0x3ABB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1038">El recurso es demasiado nuevo para ser compatible.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1038">The resource is too new to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR \_ evt \_ no se puede \_ abrir el \_ canal \_ de la \_ consulta**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR\_EVT\_CANNOT\_OPEN\_CHANNEL\_OF\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1040">15036 (0x3ABC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1040">15036 (0x3ABC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1041">El canal en el índice %1! d!</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1041">The channel at index %1!d!</span></span> <span data-ttu-id="1b6f6-1042">no se puede abrir la consulta.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1042">of the query can't be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR \_ evt \_ publicador \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR\_EVT\_PUBLISHER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1044">15037 (0x3ABD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1044">15037 (0x3ABD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1045">El publicador se ha deshabilitado y su recurso no está disponible.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1045">The publisher has been disabled and its resource is not available.</span></span> <span data-ttu-id="1b6f6-1046">Esto suele ocurrir cuando el publicador se está desinstalando o actualizando.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1046">This usually occurs when the publisher is in the process of being uninstalled or upgraded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR \_ \_ de filtro evt \_ fuera \_ del \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR\_EVT\_FILTER\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1048">15038 (0x3ABE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1048">15038 (0x3ABE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1049">Se intentó crear un tipo numérico que está fuera de su intervalo válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1049">Attempted to create a numeric type that is outside of its valid range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERROR \_ la \_ suscripción de EC \_ no se puede \_ activar**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERROR\_EC\_SUBSCRIPTION\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1051">15080 (0x3AE8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1051">15080 (0x3AE8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1052">La suscripción no se puede activar.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1052">The subscription fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERROR \_ de \_ registro EC \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERROR\_EC\_LOG\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1054">15081 (0x3AE9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1054">15081 (0x3AE9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1055">El registro de la suscripción está en estado deshabilitado y no se puede usar para reenviar eventos a.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1055">The log of the subscription is in disabled state, and can not be used to forward events to.</span></span> <span data-ttu-id="1b6f6-1056">Primero se debe habilitar el registro antes de que se pueda activar la suscripción.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1056">The log must first be enabled before the subscription can be activated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERROR \_ de \_ reenvío circular de EC \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERROR\_EC\_CIRCULAR\_FORWARDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1058">15082 (0x3AEA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1058">15082 (0x3AEA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1059">Al reenviar eventos del equipo local a sí mismo, la consulta de la suscripción no puede contener el registro de destino de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1059">When forwarding events from local machine to itself, the query of the subscription can't contain target log of the subscription.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERROR \_ EC \_ CREDSTORE \_ completo**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERROR\_EC\_CREDSTORE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1061">15083 (0x3AEB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1061">15083 (0x3AEB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1062">El almacén de credenciales que se usa para guardar las credenciales está lleno.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1062">The credential store that is used to save credentials is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERROR \_ EC \_ CRED \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERROR\_EC\_CRED\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1064">15084 (0x3AEC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1064">15084 (0x3AEC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1065">No se encuentra la credencial usada por esta suscripción en el almacén de credenciales.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1065">The credential used by this subscription can't be found in credential store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERROR \_ EC \_ no hay ningún \_ \_ canal activo**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERROR\_EC\_NO\_ACTIVE\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1067">15085 (0x3AED)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1067">15085 (0x3AED)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1068">No se encuentra ningún canal activo para la consulta.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1068">No active channel is found for the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**\_ \_ \_ no \_ se encontró el archivo mui de error**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**ERROR\_MUI\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1070">15100 (0x3AFC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1070">15100 (0x3AFC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1071">El cargador de recursos no encontró el archivo MUI.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1071">The resource loader failed to find MUI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERROR \_ de \_ archivo no válido de MUI \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERROR\_MUI\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1073">15101 (0x3AFD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1073">15101 (0x3AFD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1074">El cargador de recursos no pudo cargar el archivo MUI porque el archivo no supera la validación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1074">The resource loader failed to load MUI file because the file fail to pass validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERROR \_ de \_ \_ configuración de RC no válida de MUI \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERROR\_MUI\_INVALID\_RC\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1076">15102 (0x3AFE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1076">15102 (0x3AFE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1077">El manifiesto RC está dañado con datos no utilizados o con una versión no admitida o con un elemento necesario que falta.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1077">The RC Manifest is corrupted with garbage data or unsupported version or missing required item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERROR \_ en \_ \_ el nombre de configuración regional no válido de MUI \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERROR\_MUI\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1079">15103 (0x3AFF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1079">15103 (0x3AFF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1080">El manifiesto RC tiene un nombre de referencia cultural no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1080">The RC Manifest has invalid culture name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERROR \_ : \_ \_ nombre de ULTIMATEFALLBACK no válido de MUI \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERROR\_MUI\_INVALID\_ULTIMATEFALLBACK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1082">15104 (0x3B00)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1082">15104 (0x3B00)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1083">El manifiesto RC tiene un nombre ultimatefallback no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1083">The RC Manifest has invalid ultimatefallback name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERROR \_ de \_ archivo mui \_ no \_ cargado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERROR\_MUI\_FILE\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1085">15105 (0x3B01)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1085">15105 (0x3B01)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1086">La caché del cargador de recursos no tiene una entrada de MUI cargada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1086">The resource loader cache doesn't have loaded MUI entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**\_detención de \_ usuario de enumeración de recurso de \_ error \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**ERROR\_RESOURCE\_ENUM\_USER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1088">15106 (0x3B02)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1088">15106 (0x3B02)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1089">El usuario detuvo la enumeración de recursos.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1089">User stopped resource enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERROR de \_ mui \_ INTLSETTINGS \_ UILANG \_ no \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERROR\_MUI\_INTLSETTINGS\_UILANG\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1091">15107 (0x3B03)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1091">15107 (0x3B03)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1092">Error en la instalación del idioma de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1092">UI language installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERROR \_ de \_ mui \_ INTLSETTINGS \_ nombre de configuración regional no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERROR\_MUI\_INTLSETTINGS\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1094">15108 (0x3B04)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1094">15108 (0x3B04)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1095">Error en la instalación de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1095">Locale installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERROR \_ \_ en el tiempo \_ de ejecución de MRM sin \_ \_ recurso predeterminado o \_ neutro \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERROR\_MRM\_RUNTIME\_NO\_DEFAULT\_OR\_NEUTRAL\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1097">15110 (0x3B06)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1097">15110 (0x3B06)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1098">Un recurso no tiene un valor predeterminado o neutro.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1098">A resource does not have default or neutral value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERROR \_ MRM \_ archivo priconfig no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERROR\_MRM\_INVALID\_PRICONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1100">15111 (0x3B07)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1100">15111 (0x3B07)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1101">Archivo de configuración de PRI no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1101">Invalid PRI config file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERROR \_ MRM \_ \_ tipo de archivo no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERROR\_MRM\_INVALID\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1103">15112 (0x3B08)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1103">15112 (0x3B08)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1104">Tipo de archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1104">Invalid file type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERROR \_ MRM \_ desconocido \_ Qualifier**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERROR\_MRM\_UNKNOWN\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1106">15113 (0x3B09)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1106">15113 (0x3B09)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1107">Calificador desconocido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1107">Unknown qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERROR \_ MRM \_ \_ valor de calificador no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1109">15114 (0x3B0A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1109">15114 (0x3B0A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1110">Valor de calificador no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1110">Invalid qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERROR \_ MRM \_ sin \_ candidato**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERROR\_MRM\_NO\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1112">15115 (0x3B0B)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1112">15115 (0x3B0B)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1113">No se encontró ningún candidato.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1113">No Candidate found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERROR \_ MRM \_ sin \_ coincidencia \_ o \_ \_ candidato predeterminado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERROR\_MRM\_NO\_MATCH\_OR\_DEFAULT\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1115">15116 (0x3B0C)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1115">15116 (0x3B0C)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1116">ResourceMap o NamedResource tiene un elemento que no tiene recursos predeterminados o neutros.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1116">The ResourceMap or NamedResource has an item that does not have default or neutral resource..</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de tipo de recurso de MRM \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERROR\_MRM\_RESOURCE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1118">15117 (0x3B0D)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1118">15117 (0x3B0D)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1119">Tipo de ResourceCandidate no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1119">Invalid ResourceCandidate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERROR \_ MRM \_ \_ nombre de asignación duplicado \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERROR\_MRM\_DUPLICATE\_MAP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1121">15118 (0x3B0E)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1121">15118 (0x3B0E)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1122">Asignación de recursos duplicada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1122">Duplicate Resource Map.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERROR \_ de \_ MRM \_ entrada duplicada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERROR\_MRM\_DUPLICATE\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1124">15119 (0x3B0F)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1124">15119 (0x3B0F)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1125">Entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1125">Duplicate Entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERROR \_ MRM \_ \_ identificador de recurso no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERROR\_MRM\_INVALID\_RESOURCE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1127">15120 (0x3B10)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1127">15120 (0x3B10)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1128">Identificador de recurso no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1128">Invalid Resource Identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERROR \_ MRM \_ FILEPATH \_ Too \_ Long**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERROR\_MRM\_FILEPATH\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1130">15121 (0x3B11)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1130">15121 (0x3B11)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1131">Filepath es demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1131">Filepath too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERROR \_ MRM \_ tipo de directorio no compatible \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERROR\_MRM\_UNSUPPORTED\_DIRECTORY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1133">15122 (0x3B12)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1133">15122 (0x3B12)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1134">Tipo de directorio no compatible.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1134">Unsupported directory type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERROR \_ MRM \_ \_ archivo PRI no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERROR\_MRM\_INVALID\_PRI\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1136">15126 (0x3B16)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1136">15126 (0x3B16)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1137">Archivo PRI no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1137">Invalid PRI File.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERROR \_ MRM \_ denominado \_ recurso \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERROR\_MRM\_NAMED\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1139">15127 (0x3B17)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1139">15127 (0x3B17)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1140">No se encontró NamedResource.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1140">NamedResource Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**\_ \_ \_ no \_ se encontró la asignación de error MRM**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**ERROR\_MRM\_MAP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1142">15135 (0x3B1F)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1142">15135 (0x3B1F)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1143">No se encontró ResourceMap.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1143">ResourceMap Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERROR \_ MRM \_ tipo de perfil no admitido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERROR\_MRM\_UNSUPPORTED\_PROFILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1145">15136 (0x3B20)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1145">15136 (0x3B20)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1146">Tipo de Perfil de MRT no compatible.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1146">Unsupported MRT profile type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERROR \_ MRM \_ \_ operador de calificador no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1148">15137 (0x3B21)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1148">15137 (0x3B21)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1149">Operador de calificador no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1149">Invalid qualifier operator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERROR en el \_ \_ \_ valor de calificador indeterminado \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERROR\_MRM\_INDETERMINATE\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1151">15138 (0x3B22)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1151">15138 (0x3B22)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1152">No se puede determinar el valor de calificador o el valor de calificador no se ha establecido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1152">Unable to determine qualifier value or qualifier value has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERROR \_ de \_ fusión mediante combinación automerge \_ habilitada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERROR\_MRM\_AUTOMERGE\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1154">15139 (0x3B23)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1154">15139 (0x3B23)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1155">Fusionar mediante combinación automáticamente está habilitado en el archivo PRI.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1155">Automerge is enabled in the PRI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERROR \_ MRM \_ demasiados \_ \_ recursos**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERROR\_MRM\_TOO\_MANY\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1157">15140 (0x3B24)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1157">15140 (0x3B24)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1158">Demasiados recursos definidos para el paquete.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1158">Too many resources defined for package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERROR \_ de \_ \_ cadena de funcionalidades no válidas MCA \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERROR\_MCA\_INVALID\_CAPABILITIES\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1160">15200 (0x3B60)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1160">15200 (0x3B60)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1161">El monitor devolvió una cadena de funcionalidades DDC/CI que no cumplía con las especificaciones ACCESS. bus 3,0, DDC/CI 1,1 o MCCS 2 revisión 1.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1161">The monitor returned a DDC/CI capabilities string that did not comply with the ACCESS.bus 3.0, DDC/CI 1.1 or MCCS 2 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERROR \_ MCA \_ \_ versión de VCP no válida \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERROR\_MCA\_INVALID\_VCP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1163">15201 (0x3B61)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1163">15201 (0x3B61)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1164">El código VCP de la versión VCP del monitor (0xDF) devolvió un valor de versión no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1164">The monitor's VCP Version (0xDF) VCP code returned an invalid version value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERROR: el \_ \_ monitor MCA infringe la \_ \_ especificación de MCCS \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERROR\_MCA\_MONITOR\_VIOLATES\_MCCS\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1166">15202 (0x3B62)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1166">15202 (0x3B62)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1167">El monitor no cumple con la especificación de MCCS que notifica que es compatible.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1167">The monitor does not comply with the MCCS specification it claims to support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERROR \_ no coincidente de la \_ versión MCCS de MCA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERROR\_MCA\_MCCS\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1169">15203 (0x3B63)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1169">15203 (0x3B63)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1170">La versión MCCS de la funcionalidad MCCS ver de un monitor \_ no coincide con la versión MCCS que el monitor notifica cuando se usa el código VCP de la versión VCP (0xDF).</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1170">The MCCS version in a monitor's mccs\_ver capability does not match the MCCS version the monitor reports when the VCP Version (0xDF) VCP code is used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERROR \_ MCA \_ versión de MCCS no admitida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERROR\_MCA\_UNSUPPORTED\_MCCS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1172">15204 (0x3B64)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1172">15204 (0x3B64)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1173">La API de configuración de monitor solo funciona con monitores que admiten la especificación MCCS 1,0, MCCS 2,0 Specification o la especificación MCCS 2,0 revisión 1.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1173">The Monitor Configuration API only works with monitors that support the MCCS 1.0 specification, MCCS 2.0 specification or the MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**error \_ interno de MCA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**ERROR\_MCA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1175">15205 (0x3B65)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1175">15205 (0x3B65)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1176">Se ha producido un error interno de API de configuración de monitor.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1176">An internal Monitor Configuration API error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERROR \_ MCA \_ tipo de tecnología no válido \_ \_ \_ devuelto**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERROR\_MCA\_INVALID\_TECHNOLOGY\_TYPE\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1178">15206 (0x3B66)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1178">15206 (0x3B66)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1179">El monitor devolvió un tipo de tecnología de monitor no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1179">The monitor returned an invalid monitor technology type.</span></span> <span data-ttu-id="1b6f6-1180">CRT, plasma y LCD (TFT) son ejemplos de tipos de tecnología de supervisión.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1180">CRT, Plasma and LCD (TFT) are examples of monitor technology types.</span></span> <span data-ttu-id="1b6f6-1181">Este error implica que el monitor infringió la especificación MCCS 2,0 o MCCS 2,0 revisión 1.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1181">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERROR \_ : \_ temperatura de color no compatible con MCA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERROR\_MCA\_UNSUPPORTED\_COLOR\_TEMPERATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1183">15207 (0x3B67)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1183">15207 (0x3B67)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1184">El autor de la llamada de [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) especificó una temperatura de color no compatible con el monitor actual.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1184">The caller of [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) specified a color temperature that the current monitor did not support.</span></span> <span data-ttu-id="1b6f6-1185">Este error implica que el monitor infringió la especificación MCCS 2,0 o MCCS 2,0 revisión 1.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1185">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERROR \_ de \_ dispositivo de sistema ambiguo \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERROR\_AMBIGUOUS\_SYSTEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1187">15250 (0x3B92)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1187">15250 (0x3B92)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1188">No se puede identificar el dispositivo del sistema solicitado debido a que varios dispositivos indistinguibles coinciden potencialmente con los criterios de identificación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1188">The requested system device cannot be identified due to multiple indistinguishable devices potentially matching the identification criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERROR \_ de \_ dispositivo de sistema \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERROR\_SYSTEM\_DEVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1190">15299 (0x3BC3)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1190">15299 (0x3BC3)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1191">No se encuentra el dispositivo del sistema solicitado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1191">The requested system device cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**\_no se \_ \_ admite el hash de error**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**ERROR\_HASH\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1193">15300 (0x3BC4)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1193">15300 (0x3BC4)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1194">La generación de hash para la versión hash y el tipo hash especificados no está habilitada en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1194">Hash generation for the specified hash version and hash type is not enabled on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**HASH de ERROR \_ \_ no \_ presente**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**ERROR\_HASH\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1196">15301 (0x3BC5)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1196">15301 (0x3BC5)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1197">El hash solicitado desde el servidor no está disponible o ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1197">The hash requested from the server is not available or no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERROR \_ de \_ proveedor de CI secundario \_ \_ no \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERROR\_SECONDARY\_IC\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1199">15321 (0x3BD9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1199">15321 (0x3BD9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1200">La instancia de controlador de interrupción secundaria que administra la interrupción especificada no está registrada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1200">The secondary interrupt controller instance that manages the specified interrupt is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERROR \_ de \_ información del cliente GPIO \_ \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERROR\_GPIO\_CLIENT\_INFORMATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1202">15322 (0x3BDA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1202">15322 (0x3BDA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1203">La información proporcionada por el controlador de cliente GPIO no es válida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1203">The information supplied by the GPIO client driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**\_no se \_ admite la versión de GPIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERROR\_GPIO\_VERSION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1205">15323 (0x3BDB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1205">15323 (0x3BDB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1206">No se admite la versión especificada por el controlador cliente GPIO.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1206">The version specified by the GPIO client driver is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERROR \_ GPIO \_ : \_ paquete de registro no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERROR\_GPIO\_INVALID\_REGISTRATION\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1208">15324 (0x3BDC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1208">15324 (0x3BDC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1209">El paquete de registro proporcionado por el controlador cliente GPIO no es válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1209">The registration packet supplied by the GPIO client driver is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERROR \_ de \_ operación de GPIO \_ denegada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERROR\_GPIO\_OPERATION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1211">15325 (0x3BDD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1211">15325 (0x3BDD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1212">La operación solicitada no es compatible con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1212">The requested operation is not supported for the specified handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERROR \_ GPIO \_ modo de \_ conexión incompatible \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERROR\_GPIO\_INCOMPATIBLE\_CONNECT\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1214">15326 (0x3BDE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1214">15326 (0x3BDE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1215">El modo de conexión solicitado entra en conflicto con un modo existente en uno o varios de los pin especificados.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1215">The requested connect mode conflicts with an existing mode on one or more of the specified pins.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERROR \_ de \_ interrupción de GPIO ya sin \_ \_ máscara**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERROR\_GPIO\_INTERRUPT\_ALREADY\_UNMASKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1217">15327 (0x3BDF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1217">15327 (0x3BDF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1218">La interrupción solicitada para desenmascarar no se enmascara.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1218">The interrupt requested to be unmasked is not masked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERROR \_ no se puede \_ cambiar \_ nivel**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERROR\_CANNOT\_SWITCH\_RUNLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1220">15400 (0x3C28)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1220">15400 (0x3C28)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1221">No se puede completar correctamente el cambio de nivel de ejecución solicitado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1221">The requested run level switch cannot be completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERROR \_ de \_ configuración de nivel no válida \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERROR\_INVALID\_RUNLEVEL\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1223">15401 (0x3C29)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1223">15401 (0x3C29)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1224">El servicio tiene un valor de nivel de ejecución no válido.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1224">The service has an invalid run level setting.</span></span> <span data-ttu-id="1b6f6-1225">El nivel de ejecución de un servicio no debe ser mayor que el nivel de ejecución de sus servicios dependientes.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1225">The run level for a service must not be higher than the run level of its dependent services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERROR \_ de \_ tiempo de espera del modificador nivel \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1227">15402 (0x3C2A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1227">15402 (0x3C2A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1228">No se puede completar correctamente el cambio de nivel de ejecución solicitado porque uno o varios servicios no se detendrán o se reiniciarán dentro del tiempo de espera especificado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1228">The requested run level switch cannot be completed successfully since one or more services will not stop or restart within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERROR \_ nivel \_ cambiar \_ el \_ tiempo de espera del agente**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_AGENT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1230">15403 (0x3C2B)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1230">15403 (0x3C2B)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1231">Un agente de cambio de nivel de ejecución no respondió dentro del tiempo de espera especificado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1231">A run level switch agent did not respond within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERROR \_ \_ en el modificador nivel \_ en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERROR\_RUNLEVEL\_SWITCH\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1233">15404 (0x3C2C)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1233">15404 (0x3C2C)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1234">Hay un modificador de nivel de ejecución en curso.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1234">A run level switch is currently in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**ERROR de los servicios de errores de \_ \_ \_ AUTOSTART**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**ERROR\_SERVICES\_FAILED\_AUTOSTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1236">15405 (0x3C2D)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1236">15405 (0x3C2D)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1237">No se pudo iniciar uno o varios servicios durante la fase de inicio del servicio de un modificador de nivel de ejecución.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1237">One or more services failed to start during the service startup phase of a run level switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERROR de la \_ tarea com de \_ \_ detención \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERROR\_COM\_TASK\_STOP\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1239">15501 (0x3C8D)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1239">15501 (0x3C8D)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1240">La solicitud de detención de tarea no se puede completar inmediatamente porque la tarea necesita más tiempo para cerrarse.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1240">The task stop request cannot be completed immediately since task needs more time to shutdown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERROR \_ al instalar el \_ \_ paquete abierto \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERROR\_INSTALL\_OPEN\_PACKAGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1242">15600 (0x3CF0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1242">15600 (0x3CF0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1243">No se pudo abrir el paquete.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1243">Package could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERROR al \_ instalar el \_ paquete \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERROR\_INSTALL\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1245">15601 (0x3CF1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1245">15601 (0x3CF1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1246">No se encontró el paquete.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1246">Package was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERROR al \_ instalar el \_ paquete no válido \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERROR\_INSTALL\_INVALID\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1248">15602 (0x3CF2)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1248">15602 (0x3CF2)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1249">Los datos del paquete no son válidos.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1249">Package data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERROR \_ al instalar la \_ dependencia de resolución \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERROR\_INSTALL\_RESOLVE\_DEPENDENCY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1251">15603 (0x3CF3)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1251">15603 (0x3CF3)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1252">Error de actualización del paquete, dependencia o validación de conflictos.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1252">Package failed updates, dependency or conflict validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERROR al \_ instalar \_ espacio insuficiente en \_ \_ disco \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERROR\_INSTALL\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1254">15604 (0x3CF4)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1254">15604 (0x3CF4)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1255">No hay suficiente espacio en disco en el equipo.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1255">There is not enough disk space on your computer.</span></span> <span data-ttu-id="1b6f6-1256">Libere espacio y vuelva a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1256">Please free up some space and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERROR de instalación de ERROR de \_ \_ red \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERROR\_INSTALL\_NETWORK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1258">15605 (0x3CF5)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1258">15605 (0x3CF5)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1259">Se produjo un problema al descargar el producto.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1259">There was a problem downloading your product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERROR de \_ registro de instalación de error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERROR\_INSTALL\_REGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1261">15606 (0x3CF6)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1261">15606 (0x3CF6)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1262">No se pudo registrar el paquete.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1262">Package could not be registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERROR \_ al \_ anular el registro de la instalación \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERROR\_INSTALL\_DEREGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1264">15607 (0x3CF7)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1264">15607 (0x3CF7)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1265">No se pudo anular el registro del paquete.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1265">Package could not be unregistered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERROR al \_ instalar \_ cancelar**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERROR\_INSTALL\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1267">15608 (0x3CF8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1267">15608 (0x3CF8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1268">El usuario canceló la solicitud de instalación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1268">User cancelled the install request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERROR en la instalación del ERROR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERROR\_INSTALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1270">15609 (0x3CF9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1270">15609 (0x3CF9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1271">Error de instalación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1271">Install failed.</span></span> <span data-ttu-id="1b6f6-1272">Póngase en contacto con su proveedor de software.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1272">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**ERROR \_ al quitar errores \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**ERROR\_REMOVE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1274">15610 (0x3CFA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1274">15610 (0x3CFA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1275">No se pudo quitar.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1275">Removal failed.</span></span> <span data-ttu-id="1b6f6-1276">Póngase en contacto con su proveedor de software.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1276">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**el \_ paquete de error \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**ERROR\_PACKAGE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1278">15611 (0x3CFB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1278">15611 (0x3CFB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1279">El paquete proporcionado ya está instalado y se ha bloqueado la reinstalación del paquete.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1279">The provided package is already installed, and reinstallation of the package was blocked.</span></span> <span data-ttu-id="1b6f6-1280">Busque detalles en el registro de eventos de AppXDeployment-Server.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1280">Check the AppXDeployment-Server event log for details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**el ERROR \_ debe \_ corregirse**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERROR\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1282">15612 (0x3CFC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1282">15612 (0x3CFC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1283">No se puede iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1283">The application cannot be started.</span></span> <span data-ttu-id="1b6f6-1284">Intente volver a instalar la aplicación para corregir el problema.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1284">Try reinstalling the application to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERROR \_ al instalar el \_ requisito previo de instalación \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERROR\_INSTALL\_PREREQUISITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1286">15613 (0x3CFD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1286">15613 (0x3CFD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1287">No se pudo satisfacer un requisito previo para una instalación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1287">A Prerequisite for an install could not be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**el \_ repositorio del paquete de errores \_ \_ está dañado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**ERROR\_PACKAGE\_REPOSITORY\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1289">15614 (0x3CFE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1289">15614 (0x3CFE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1290">El repositorio de paquetes está dañado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1290">The package repository is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERROR al \_ instalar la \_ directiva \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERROR\_INSTALL\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1292">15615 (0x3CFF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1292">15615 (0x3CFF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1293">Para instalar esta aplicación, necesita una licencia de desarrollador de Windows o un sistema habilitado para instalación de prueba.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1293">To install this application you need either a Windows developer license or a sideloading-enabled system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**\_actualización de paquetes de errores \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**ERROR\_PACKAGE\_UPDATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1295">15616 (0x3D00)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1295">15616 (0x3D00)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1296">No se puede iniciar la aplicación porque se está actualizando actualmente.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1296">The application cannot be started because it is currently updating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**\_implementación \_ de error bloqueada por la \_ \_ Directiva**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**ERROR\_DEPLOYMENT\_BLOCKED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1298">15617 (0x3D01)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1298">15617 (0x3D01)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1299">La Directiva bloquea la operación de implementación de paquetes.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1299">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="1b6f6-1300">Póngase en contacto con el administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1300">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_paquetes \_ de error en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**ERROR\_PACKAGES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1302">15618 (0x3D02)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1302">15618 (0x3D02)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1303">No se pudo instalar el paquete porque los recursos modificados están actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1303">The package could not be installed because resources it modifies are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**el \_ archivo de recuperación de errores \_ \_ está dañado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**ERROR\_RECOVERY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1305">15619 (0x3D03)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1305">15619 (0x3D03)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1306">No se pudo recuperar el paquete porque los datos necesarios para la recuperación están dañados.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1306">The package could not be recovered because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERROR \_ de \_ firma preconfigurada no válida \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERROR\_INVALID\_STAGED\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1308">15620 (0x3D04)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1308">15620 (0x3D04)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1309">La firma no es válida.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1309">The signature is invalid.</span></span> <span data-ttu-id="1b6f6-1310">Para registrarse en modo de desarrollador, AppxSignature. p7x y AppxBlockMap.xml deben ser válidos o no deben estar presentes.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1310">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or should not be present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERROR \_ al eliminar \_ el \_ almacén de APPLICATIONDATA existente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERROR\_DELETING\_EXISTING\_APPLICATIONDATA\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1312">15621 (0x3D05)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1312">15621 (0x3D05)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1313">Se produjo un error al eliminar los datos de aplicación existentes anteriormente del paquete.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1313">An error occurred while deleting the package's previously existing application data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERROR al \_ instalar la \_ degradación del paquete \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERROR\_INSTALL\_PACKAGE\_DOWNGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1315">15622 (0x3D06)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1315">15622 (0x3D06)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1316">No se pudo instalar el paquete porque ya hay instalada una versión superior de este paquete.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1316">The package could not be installed because a higher version of this package is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**el \_ sistema de errores \_ necesita \_ corrección**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**ERROR\_SYSTEM\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1318">15623 (0x3D07)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1318">15623 (0x3D07)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1319">Se detectó un error en un archivo binario del sistema.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1319">An error in a system binary was detected.</span></span> <span data-ttu-id="1b6f6-1320">Intente actualizar el equipo para corregir el problema.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1320">Try refreshing the PC to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERROR de integridad de appx error de \_ \_ \_ \_ CLR \_ ngen**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERROR\_APPX\_INTEGRITY\_FAILURE\_CLR\_NGEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1322">15624 (0x3D08)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1322">15624 (0x3D08)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1323">Se detectó un binario CLR NGEN dañado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1323">A corrupted CLR NGEN binary was detected on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**archivo de resistencia de errores \_ \_ \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**ERROR\_RESILIENCY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1325">15625 (0x3D09)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1325">15625 (0x3D09)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1326">No se pudo reanudar la operación porque los datos necesarios para la recuperación están dañados.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1326">The operation could not be resumed because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERROR al \_ instalar el \_ servicio de Firewall no se \_ \_ \_ está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERROR\_INSTALL\_FIREWALL\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1328">15626 (0x3D0A)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1328">15626 (0x3D0A)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1329">No se pudo instalar el paquete porque el servicio Firewall de Windows no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1329">The package could not be installed because the Windows Firewall service is not running.</span></span> <span data-ttu-id="1b6f6-1330">Habilite el servicio Firewall de Windows e inténtelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1330">Enable the Windows Firewall service and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**\_ \_ no hay ningún paquete de error de APPMODEL \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**APPMODEL\_ERROR\_NO\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1332">15700 (0x3D54)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1332">15700 (0x3D54)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1333">El proceso no tiene ninguna identidad de paquete.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1333">The process has no package identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**tiempo de ejecución del paquete de errores de APPMODEL \_ \_ \_ \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_RUNTIME\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1335">15701 (0x3D55)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1335">15701 (0x3D55)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1336">La información del tiempo de ejecución del paquete está dañada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1336">The package runtime information is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**la \_ identidad del paquete de errores de APPMODEL \_ \_ \_ está dañada**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_IDENTITY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1338">15702 (0x3D56)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1338">15702 (0x3D56)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1339">La identidad del paquete está dañada.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1339">The package identity is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**APPMODEL \_ error \_ sin \_ aplicación**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**APPMODEL\_ERROR\_NO\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1341">15703 (0x3D57)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1341">15703 (0x3D57)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1342">El proceso no tiene identidad de aplicación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1342">The process has no application identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**error en el almacén de carga de \_ estado \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**ERROR\_STATE\_LOAD\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1344">15800 (0x3DB8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1344">15800 (0x3DB8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1345">No se pudo cargar el almacén de estado.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1345">Loading the state store failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**error \_ \_ al obtener la \_ versión \_ de estado de error**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**ERROR\_STATE\_GET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1347">15801 (0x3DB9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1347">15801 (0x3DB9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1348">Error al recuperar la versión de estado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1348">Retrieving the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**error en la versión del conjunto de \_ estado \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**ERROR\_STATE\_SET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1350">15802 (0x3DBA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1350">15802 (0x3DBA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1351">No se pudo establecer la versión de estado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1351">Setting the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**error \_ de \_ restablecimiento estructurado de estado \_ de error \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**ERROR\_STATE\_STRUCTURED\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1353">15803 (0x3DBB)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1353">15803 (0x3DBB)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1354">No se pudo restablecer el estado estructurado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1354">Resetting the structured state of the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERROR en el \_ \_ \_ contenedor \_ abierto de estado de error**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERROR\_STATE\_OPEN\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1356">15804 (0x3DBC)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1356">15804 (0x3DBC)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1357">El administrador de estado no pudo abrir el contenedor.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1357">State Manager failed to open the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERROR \_ \_ al crear el \_ contenedor \_ de estado de error**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERROR\_STATE\_CREATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1359">15805 (0x3DBD)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1359">15805 (0x3DBD)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1360">El administrador de estado no pudo crear el contenedor.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1360">State Manager failed to create the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**ERROR \_ \_ al eliminar el \_ contenedor \_ de estado de error**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**ERROR\_STATE\_DELETE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1362">15806 (0x3DBE)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1362">15806 (0x3DBE)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1363">State Manager no pudo eliminar el contenedor.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1363">State Manager failed to delete the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**error \_ de \_ configuración de lectura de estado de \_ error \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**ERROR\_STATE\_READ\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1365">15807 (0x3DBF)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1365">15807 (0x3DBF)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1366">El administrador de estado no pudo leer la configuración.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1366">State Manager failed to read the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**error \_ de \_ configuración de escritura de estado de \_ error \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**ERROR\_STATE\_WRITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1368">15808 (0x3DC0)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1368">15808 (0x3DC0)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1369">El administrador de estado no pudo escribir la configuración.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1369">State Manager failed to write the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**error \_ de \_ configuración de eliminación de estado de \_ error \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**ERROR\_STATE\_DELETE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1371">15809 (0x3DC1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1371">15809 (0x3DC1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1372">El administrador de estado no pudo eliminar la configuración.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1372">State Manager failed to delete the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**error \_ al \_ establecer la consulta de estado de \_ error \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**ERROR\_STATE\_QUERY\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1374">15810 (0x3DC2)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1374">15810 (0x3DC2)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1375">El administrador de estado no pudo consultar la configuración.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1375">State Manager failed to query the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**error \_ de \_ \_ configuración compuesta de lectura de \_ Estado de \_ error**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**ERROR\_STATE\_READ\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1377">15811 (0x3DC3)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1377">15811 (0x3DC3)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1378">El administrador de estado no pudo leer la configuración compuesta.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1378">State Manager failed to read the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**error \_ de \_ \_ configuración compuesta de escritura de \_ Estado de \_ error**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**ERROR\_STATE\_WRITE\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1380">15812 (0x3DC4)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1380">15812 (0x3DC4)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1381">El administrador de estado no pudo escribir la configuración compuesta.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1381">State Manager failed to write the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**error en el \_ \_ contenedor de enumeración de estado de \_ error \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**ERROR\_STATE\_ENUMERATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1383">15813 (0x3DC5)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1383">15813 (0x3DC5)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1384">State Manager no pudo enumerar los contenedores.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1384">State Manager failed to enumerate the containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**error \_ \_ al enumerar la \_ configuración \_ de estado de error**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**ERROR\_STATE\_ENUMERATE\_SETTINGS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1386">15814 (0x3DC6)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1386">15814 (0x3DC6)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1387">State Manager no pudo enumerar la configuración.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1387">State Manager failed to enumerate the settings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**Estado de ERROR se \_ \_ \_ \_ \_ \_ superó el límite de tamaño del valor de configuración compuesta \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_COMPOSITE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1389">15815 (0x3DC7)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1389">15815 (0x3DC7)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1390">El tamaño del valor de configuración compuesta del administrador de Estado ha superado el límite.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1390">The size of the state manager composite setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**se \_ \_ \_ \_ \_ superó el límite de tamaño del valor de \_ Estado de error**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1392">15816 (0x3DC8)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1392">15816 (0x3DC8)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1393">El tamaño del valor de configuración del administrador de Estado ha superado el límite.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1393">The size of the state manager setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**se \_ \_ \_ \_ \_ superó el límite de \_ tamaño de la configuración de estado de error**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1395">15817 (0x3DC9)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1395">15817 (0x3DC9)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1396">La longitud del nombre de la configuración del administrador de Estado ha superado el límite.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1396">The length of the state manager setting name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**Estado de ERROR se \_ \_ \_ \_ \_ superó el límite de tamaño del contenedor \_**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**ERROR\_STATE\_CONTAINER\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1398">15818 (0x3DCA)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1398">15818 (0x3DCA)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1399">La longitud del nombre del contenedor del administrador de Estado ha superado el límite.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1399">The length of the state manager container name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b6f6-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**ERROR de \_ API \_ no disponible**</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**ERROR\_API\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6f6-1401">15841 (0x3DE1)</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1401">15841 (0x3DE1)</span></span>
</dt> <dt>



<span data-ttu-id="1b6f6-1402">Esta API no se puede usar en el contexto del tipo de aplicación del llamador.</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1402">This API cannot be used in the context of the caller's application type.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b6f6-1403">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1403">Requirements</span></span>



| <span data-ttu-id="1b6f6-1404">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1404">Requirement</span></span> | <span data-ttu-id="1b6f6-1405">Value</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1405">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b6f6-1406">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1406">Minimum supported client</span></span><br/> | <span data-ttu-id="1b6f6-1407">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1407">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1b6f6-1408">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1408">Minimum supported server</span></span><br/> | <span data-ttu-id="1b6f6-1409">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1409">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b6f6-1410">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1410">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b6f6-1411"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b6f6-1411"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b6f6-1412">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1412">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b6f6-1413">Códigos de error del sistema</span><span class="sxs-lookup"><span data-stu-id="1b6f6-1413">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
