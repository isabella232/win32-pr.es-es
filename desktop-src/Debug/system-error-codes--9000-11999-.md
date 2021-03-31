---
description: Describe los códigos de error 9000-11999 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: Códigos de error del sistema (9000-11999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807435"
---
# <a name="system-error-codes-9000-11999"></a><span data-ttu-id="11e41-103">Códigos de error del sistema (9000-11999)</span><span class="sxs-lookup"><span data-stu-id="11e41-103">System Error Codes (9000-11999)</span></span>

> [!NOTE]
> <span data-ttu-id="11e41-104">Esta información está destinada a los desarrolladores que depuran errores del sistema.</span><span class="sxs-lookup"><span data-stu-id="11e41-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="11e41-105">En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="11e41-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="11e41-106">En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) (errores 9000 a 11999).</span><span class="sxs-lookup"><span data-stu-id="11e41-106">The following list describes [system error codes](system-error-codes.md) (errors 9000 to 11999).</span></span> <span data-ttu-id="11e41-107">La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="11e41-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="11e41-108">Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.</span><span class="sxs-lookup"><span data-stu-id="11e41-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="11e41-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**\_error de \_ formato de RCODE de error de DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**DNS\_ERROR\_RCODE\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-110">9001 (0x2329)</span><span class="sxs-lookup"><span data-stu-id="11e41-110">9001 (0x2329)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-111">El servidor DNS no puede interpretar el formato.</span><span class="sxs-lookup"><span data-stu-id="11e41-111">DNS server unable to interpret format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**error de DNS del \_ \_ \_ servidor RCODE \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**DNS\_ERROR\_RCODE\_SERVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-113">9002 (0x232A)</span><span class="sxs-lookup"><span data-stu-id="11e41-113">9002 (0x232A)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-114">Error de servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-114">DNS server failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**error \_ de \_ nombre de RCODE de error de \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**DNS\_ERROR\_RCODE\_NAME\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-116">9003 (0x232B)</span><span class="sxs-lookup"><span data-stu-id="11e41-116">9003 (0x232B)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-117">El nombre DNS no existe.</span><span class="sxs-lookup"><span data-stu-id="11e41-117">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**ERROR de DNS \_ \_ RCODE \_ no \_ implementado**</span><span class="sxs-lookup"><span data-stu-id="11e41-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**DNS\_ERROR\_RCODE\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-119">9004 (0x232C)</span><span class="sxs-lookup"><span data-stu-id="11e41-119">9004 (0x232C)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-120">La solicitud DNS no es compatible con el servidor de nombres.</span><span class="sxs-lookup"><span data-stu-id="11e41-120">DNS request not supported by name server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**RCODE de error de DNS \_ \_ \_ rechazado**</span><span class="sxs-lookup"><span data-stu-id="11e41-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**DNS\_ERROR\_RCODE\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-122">9005 (0x232D)</span><span class="sxs-lookup"><span data-stu-id="11e41-122">9005 (0x232D)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-123">Operación DNS rechazada.</span><span class="sxs-lookup"><span data-stu-id="11e41-123">DNS operation refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**ERROR de DNS \_ \_ RCODE \_ YXDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="11e41-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**DNS\_ERROR\_RCODE\_YXDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-125">9006 (0x232E)</span><span class="sxs-lookup"><span data-stu-id="11e41-125">9006 (0x232E)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-126">Existe un nombre DNS que no existe.</span><span class="sxs-lookup"><span data-stu-id="11e41-126">DNS name that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**ERROR de DNS \_ \_ RCODE \_ YXRRSET**</span><span class="sxs-lookup"><span data-stu-id="11e41-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**DNS\_ERROR\_RCODE\_YXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-128">9007 (0x232F)</span><span class="sxs-lookup"><span data-stu-id="11e41-128">9007 (0x232F)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-129">El conjunto de RR DNS no existe.</span><span class="sxs-lookup"><span data-stu-id="11e41-129">DNS RR set that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**ERROR de DNS \_ \_ RCODE \_ NXRRSET**</span><span class="sxs-lookup"><span data-stu-id="11e41-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**DNS\_ERROR\_RCODE\_NXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-131">9008 (0x2330)</span><span class="sxs-lookup"><span data-stu-id="11e41-131">9008 (0x2330)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-132">El valor de RR de DNS establecido debe existir, no existe.</span><span class="sxs-lookup"><span data-stu-id="11e41-132">DNS RR set that ought to exist, does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**ERROR de DNS \_ \_ RCODE \_ NOTAUTH**</span><span class="sxs-lookup"><span data-stu-id="11e41-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**DNS\_ERROR\_RCODE\_NOTAUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-134">9009 (0x2331)</span><span class="sxs-lookup"><span data-stu-id="11e41-134">9009 (0x2331)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-135">El servidor DNS no es autoritativo para la zona.</span><span class="sxs-lookup"><span data-stu-id="11e41-135">DNS server not authoritative for zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**ERROR de DNS \_ \_ RCODE \_ NOTZONE**</span><span class="sxs-lookup"><span data-stu-id="11e41-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**DNS\_ERROR\_RCODE\_NOTZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-137">9010 (0x2332)</span><span class="sxs-lookup"><span data-stu-id="11e41-137">9010 (0x2332)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-138">El nombre DNS de la actualización o prereq no está en la zona.</span><span class="sxs-lookup"><span data-stu-id="11e41-138">DNS name in update or prereq is not in zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**ERROR de DNS \_ \_ RCODE \_ BADSIG**</span><span class="sxs-lookup"><span data-stu-id="11e41-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**DNS\_ERROR\_RCODE\_BADSIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-140">9016 (0x2338)</span><span class="sxs-lookup"><span data-stu-id="11e41-140">9016 (0x2338)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-141">No se pudo comprobar la firma DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-141">DNS signature failed to verify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**ERROR de DNS \_ \_ RCODE \_ BADKEY**</span><span class="sxs-lookup"><span data-stu-id="11e41-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**DNS\_ERROR\_RCODE\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-143">9017 (0x2339)</span><span class="sxs-lookup"><span data-stu-id="11e41-143">9017 (0x2339)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-144">Clave incorrecta de DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-144">DNS bad key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**ERROR de DNS \_ \_ RCODE \_ BADTIME**</span><span class="sxs-lookup"><span data-stu-id="11e41-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**DNS\_ERROR\_RCODE\_BADTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-146">9018 (0x233A)</span><span class="sxs-lookup"><span data-stu-id="11e41-146">9018 (0x233A)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-147">Expiró la validez de la firma DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-147">DNS signature validity expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**Maestro de error de DNS \_ \_ \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="11e41-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**DNS\_ERROR\_KEYMASTER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-149">9101 (0x238D)</span><span class="sxs-lookup"><span data-stu-id="11e41-149">9101 (0x238D)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-150">Solo el servidor DNS que actúa como maestro de claves para la zona puede realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="11e41-150">Only the DNS server acting as the key master for the zone may perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**\_error \_ de DNS no \_ permitido en la \_ \_ zona firmada \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_SIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-152">9102 (0x238E)</span><span class="sxs-lookup"><span data-stu-id="11e41-152">9102 (0x238E)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-153">Esta operación no se permite en una zona firmada o con claves de firma.</span><span class="sxs-lookup"><span data-stu-id="11e41-153">This operation is not allowed on a zone that is signed or has signing keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**\_Error \_ de DNS NSEC3 \_ incompatible \_ con \_ RSA \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="11e41-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS\_ERROR\_NSEC3\_INCOMPATIBLE\_WITH\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-155">9103 (0x238F)</span><span class="sxs-lookup"><span data-stu-id="11e41-155">9103 (0x238F)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-156">NSEC3 no es compatible con el algoritmo RSA-SHA-1.</span><span class="sxs-lookup"><span data-stu-id="11e41-156">NSEC3 is not compatible with the RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="11e41-157">Elija un algoritmo diferente o use NSEC.</span><span class="sxs-lookup"><span data-stu-id="11e41-157">Choose a different algorithm or use NSEC.</span></span>

<span data-ttu-id="11e41-158">Este valor también se denominaba **DNS \_ error de \_ \_ NSEC3 \_ parámetros no válidos** .</span><span class="sxs-lookup"><span data-stu-id="11e41-158">This value was also named **DNS\_ERROR\_INVALID\_NSEC3\_PARAMETERS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**ERROR de DNS \_ \_ no \_ hay suficientes \_ \_ descriptores de clave de firma \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**DNS\_ERROR\_NOT\_ENOUGH\_SIGNING\_KEY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-160">9104 (0x2390)</span><span class="sxs-lookup"><span data-stu-id="11e41-160">9104 (0x2390)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-161">La zona no tiene suficientes claves de firma.</span><span class="sxs-lookup"><span data-stu-id="11e41-161">The zone does not have enough signing keys.</span></span> <span data-ttu-id="11e41-162">Debe haber al menos una clave de firma de clave (KSK) y al menos una clave de firma de zona (ZSK).</span><span class="sxs-lookup"><span data-stu-id="11e41-162">There must be at least one key signing key (KSK) and at least one zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**algoritmo de error de DNS \_ \_ no admitido \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**DNS\_ERROR\_UNSUPPORTED\_ALGORITHM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-164">9105 (0x2391)</span><span class="sxs-lookup"><span data-stu-id="11e41-164">9105 (0x2391)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-165">No se admite el algoritmo especificado.</span><span class="sxs-lookup"><span data-stu-id="11e41-165">The specified algorithm is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**ERROR de DNS \_ \_ tamaño de clave no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**DNS\_ERROR\_INVALID\_KEY\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-167">9106 (0x2392)</span><span class="sxs-lookup"><span data-stu-id="11e41-167">9106 (0x2392)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-168">No se admite el tamaño de clave especificado.</span><span class="sxs-lookup"><span data-stu-id="11e41-168">The specified key size is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**clave de firma de error de DNS \_ \_ \_ \_ no \_ accesible**</span><span class="sxs-lookup"><span data-stu-id="11e41-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**DNS\_ERROR\_SIGNING\_KEY\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-170">9107 (0x2393)</span><span class="sxs-lookup"><span data-stu-id="11e41-170">9107 (0x2393)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-171">Una o varias de las claves de firma para una zona no son accesibles para el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-171">One or more of the signing keys for a zone are not accessible to the DNS server.</span></span> <span data-ttu-id="11e41-172">La firma de zona no estará operativa hasta que se solucione este error.</span><span class="sxs-lookup"><span data-stu-id="11e41-172">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**el \_ KSP error de DNS no \_ admite la \_ \_ \_ \_ protección**</span><span class="sxs-lookup"><span data-stu-id="11e41-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**DNS\_ERROR\_KSP\_DOES\_NOT\_SUPPORT\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-174">9108 (0x2394)</span><span class="sxs-lookup"><span data-stu-id="11e41-174">9108 (0x2394)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-175">El proveedor de almacenamiento de claves especificado no admite la protección de datos de DPAPI + +.</span><span class="sxs-lookup"><span data-stu-id="11e41-175">The specified key storage provider does not support DPAPI++ data protection.</span></span> <span data-ttu-id="11e41-176">La firma de zona no estará operativa hasta que se solucione este error.</span><span class="sxs-lookup"><span data-stu-id="11e41-176">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**error \_ de \_ \_ protección de datos inesperado de error \_ de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**DNS\_ERROR\_UNEXPECTED\_DATA\_PROTECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-178">9109 (0x2395)</span><span class="sxs-lookup"><span data-stu-id="11e41-178">9109 (0x2395)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-179">Se encontró un error de DPAPI + + inesperado.</span><span class="sxs-lookup"><span data-stu-id="11e41-179">An unexpected DPAPI++ error was encountered.</span></span> <span data-ttu-id="11e41-180">La firma de zona no estará operativa hasta que se solucione este error.</span><span class="sxs-lookup"><span data-stu-id="11e41-180">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**error de error de \_ \_ CNG inesperado de DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**DNS\_ERROR\_UNEXPECTED\_CNG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-182">9110 (0x2396)</span><span class="sxs-lookup"><span data-stu-id="11e41-182">9110 (0x2396)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-183">Se encontró un error de cifrado inesperado.</span><span class="sxs-lookup"><span data-stu-id="11e41-183">An unexpected crypto error was encountered.</span></span> <span data-ttu-id="11e41-184">Es posible que la firma de zona no esté operativa hasta que se solucione este error.</span><span class="sxs-lookup"><span data-stu-id="11e41-184">Zone signing may not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**ERROR de DNS \_ \_ versión de \_ parámetro de firma desconocida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**DNS\_ERROR\_UNKNOWN\_SIGNING\_PARAMETER\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-186">9111 (0x2397)</span><span class="sxs-lookup"><span data-stu-id="11e41-186">9111 (0x2397)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-187">El servidor DNS encontró una clave de firma con una versión desconocida.</span><span class="sxs-lookup"><span data-stu-id="11e41-187">The DNS server encountered a signing key with an unknown version.</span></span> <span data-ttu-id="11e41-188">La firma de zona no estará operativa hasta que se solucione este error.</span><span class="sxs-lookup"><span data-stu-id="11e41-188">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**\_KSP error de DNS \_ \_ no \_ accesible**</span><span class="sxs-lookup"><span data-stu-id="11e41-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**DNS\_ERROR\_KSP\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-190">9112 (0x2398)</span><span class="sxs-lookup"><span data-stu-id="11e41-190">9112 (0x2398)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-191">El servidor DNS no puede abrir el proveedor de servicios de claves especificado.</span><span class="sxs-lookup"><span data-stu-id="11e41-191">The specified key service provider cannot be opened by the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**ERROR de DNS \_ \_ demasiados \_ \_ SKDS**</span><span class="sxs-lookup"><span data-stu-id="11e41-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**DNS\_ERROR\_TOO\_MANY\_SKDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-193">9113 (0x2399)</span><span class="sxs-lookup"><span data-stu-id="11e41-193">9113 (0x2399)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-194">El servidor DNS no puede aceptar más claves de firma con el algoritmo especificado y el valor de la marca de KSK para esta zona.</span><span class="sxs-lookup"><span data-stu-id="11e41-194">The DNS server cannot accept any more signing keys with the specified algorithm and KSK flag value for this zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**ERROR de DNS \_ \_ período de sustitución no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**DNS\_ERROR\_INVALID\_ROLLOVER\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-196">9114 (0x239A)</span><span class="sxs-lookup"><span data-stu-id="11e41-196">9114 (0x239A)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-197">El período de sustitución especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-197">The specified rollover period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**ERROR de DNS \_ \_ \_ desplazamiento de sustitución inicial no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**DNS\_ERROR\_INVALID\_INITIAL\_ROLLOVER\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-199">9115 (0x239B)</span><span class="sxs-lookup"><span data-stu-id="11e41-199">9115 (0x239B)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-200">El desplazamiento de sustitución inicial especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-200">The specified initial rollover offset is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**\_ \_ sustitución de errores \_ de DNS en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="11e41-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**DNS\_ERROR\_ROLLOVER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-202">9116 (0x239C)</span><span class="sxs-lookup"><span data-stu-id="11e41-202">9116 (0x239C)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-203">La clave de firma especificada ya está en proceso de revertir las claves.</span><span class="sxs-lookup"><span data-stu-id="11e41-203">The specified signing key is already in process of rolling over keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**ERROR de DNS en \_ \_ espera de \_ clave \_ no \_ presente**</span><span class="sxs-lookup"><span data-stu-id="11e41-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**DNS\_ERROR\_STANDBY\_KEY\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-205">9117 (0x239D)</span><span class="sxs-lookup"><span data-stu-id="11e41-205">9117 (0x239D)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-206">La clave de firma especificada no tiene una clave de espera para revocar.</span><span class="sxs-lookup"><span data-stu-id="11e41-206">The specified signing key does not have a standby key to revoke.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_error \_ de DNS no \_ permitido \_ en \_ ZSK**</span><span class="sxs-lookup"><span data-stu-id="11e41-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ZSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-208">9118 (0x239E)</span><span class="sxs-lookup"><span data-stu-id="11e41-208">9118 (0x239E)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-209">Esta operación no se permite en una clave de firma de zona (ZSK).</span><span class="sxs-lookup"><span data-stu-id="11e41-209">This operation is not allowed on a zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_error \_ de DNS no \_ permitido en el \_ \_ \_ SKD activo**</span><span class="sxs-lookup"><span data-stu-id="11e41-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ACTIVE\_SKD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-211">9119 (0x239F)</span><span class="sxs-lookup"><span data-stu-id="11e41-211">9119 (0x239F)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-212">Esta operación no se permite en una clave de firma activa.</span><span class="sxs-lookup"><span data-stu-id="11e41-212">This operation is not allowed on an active signing key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**sustitución de errores de DNS \_ \_ \_ ya \_ en cola**</span><span class="sxs-lookup"><span data-stu-id="11e41-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**DNS\_ERROR\_ROLLOVER\_ALREADY\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-214">9120 (0x23A0)</span><span class="sxs-lookup"><span data-stu-id="11e41-214">9120 (0x23A0)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-215">La clave de firma especificada ya está en cola para la sustitución.</span><span class="sxs-lookup"><span data-stu-id="11e41-215">The specified signing key is already queued for rollover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_error \_ de DNS no \_ permitido en la \_ \_ zona sin firmar \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_UNSIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-217">9121 (0x23A1)</span><span class="sxs-lookup"><span data-stu-id="11e41-217">9121 (0x23A1)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-218">Esta operación no se permite en una zona sin firmar.</span><span class="sxs-lookup"><span data-stu-id="11e41-218">This operation is not allowed on an unsigned zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**\_error de \_ DNS \_ maestro erróneo**</span><span class="sxs-lookup"><span data-stu-id="11e41-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**DNS\_ERROR\_BAD\_KEYMASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-220">9122 (0x23A2)</span><span class="sxs-lookup"><span data-stu-id="11e41-220">9122 (0x23A2)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-221">No se pudo completar esta operación porque el servidor DNS que aparece como el maestro de claves actual para esta zona está inactivo o no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="11e41-221">This operation could not be completed because the DNS server listed as the current key master for this zone is down or misconfigured.</span></span> <span data-ttu-id="11e41-222">Resuelva el problema en el maestro de claves actual para esta zona o use otro servidor DNS para asumir el rol de maestro de claves.</span><span class="sxs-lookup"><span data-stu-id="11e41-222">Resolve the problem on the current key master for this zone or use another DNS server to seize the key master role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**ERROR de DNS \_ \_ período de validez de firma no válido \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**DNS\_ERROR\_INVALID\_SIGNATURE\_VALIDITY\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-224">9123 (0x23A3)</span><span class="sxs-lookup"><span data-stu-id="11e41-224">9123 (0x23A3)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-225">El período de validez de la firma especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-225">The specified signature validity period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**\_Error de \_ DNS \_ \_ recuento de iteraciones de NSEC3 no válido \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**DNS\_ERROR\_INVALID\_NSEC3\_ITERATION\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-227">9124 (0x23A4)</span><span class="sxs-lookup"><span data-stu-id="11e41-227">9124 (0x23A4)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-228">El número de iteraciones de NSEC3 especificado es mayor que el permitido por la longitud de clave mínima usada en la zona.</span><span class="sxs-lookup"><span data-stu-id="11e41-228">The specified NSEC3 iteration count is higher than allowed by the minimum key length used in the zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**ERROR de DNS \_ \_ DNSSEC \_ \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="11e41-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**DNS\_ERROR\_DNSSEC\_IS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-230">9125 (0x23A5)</span><span class="sxs-lookup"><span data-stu-id="11e41-230">9125 (0x23A5)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-231">No se pudo completar esta operación porque el servidor DNS se ha configurado con las características DNSSEC deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="11e41-231">This operation could not be completed because the DNS server has been configured with DNSSEC features disabled.</span></span> <span data-ttu-id="11e41-232">Habilite DNSSEC en el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-232">Enable DNSSEC on the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**ERROR de DNS \_ \_ XML no válido \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**DNS\_ERROR\_INVALID\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-234">9126 (0x23A6)</span><span class="sxs-lookup"><span data-stu-id="11e41-234">9126 (0x23A6)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-235">No se pudo completar esta operación porque el flujo XML recibido está vacío o no es válido sintácticamente.</span><span class="sxs-lookup"><span data-stu-id="11e41-235">This operation could not be completed because the XML stream received is empty or syntactically invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**ERROR de DNS \_ \_ sin \_ \_ anclajes de veracidad válidos \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**DNS\_ERROR\_NO\_VALID\_TRUST\_ANCHORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-237">9127 (0x23A7)</span><span class="sxs-lookup"><span data-stu-id="11e41-237">9127 (0x23A7)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-238">Esta operación se completó, pero no se agregaron anclajes de veracidad porque todos los anclajes de veracidad recibidos no eran válidos, no se admitían, expiraron o no eran válidos en menos de 30 días.</span><span class="sxs-lookup"><span data-stu-id="11e41-238">This operation completed, but no trust anchors were added because all of the trust anchors received were either invalid, unsupported, expired, or would not become valid in less than 30 days.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**sustitución de error de DNS \_ \_ \_ no se pudo escribir \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**DNS\_ERROR\_ROLLOVER\_NOT\_POKEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-240">9128 (0x23A8)</span><span class="sxs-lookup"><span data-stu-id="11e41-240">9128 (0x23A8)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-241">La clave de firma especificada no está esperando la actualización del DS parental.</span><span class="sxs-lookup"><span data-stu-id="11e41-241">The specified signing key is not waiting for parental DS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**Colisión de nombre de error de DNS \_ \_ NSEC3 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**DNS\_ERROR\_NSEC3\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-243">9129 (0x23A9)</span><span class="sxs-lookup"><span data-stu-id="11e41-243">9129 (0x23A9)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-244">Colisión de hash detectada durante la firma de NSEC3.</span><span class="sxs-lookup"><span data-stu-id="11e41-244">Hash collision detected during NSEC3 signing.</span></span> <span data-ttu-id="11e41-245">Especifique un valor Salt proporcionado por el usuario diferente o use un valor Salt generado aleatoriamente e intente volver a firmar la zona.</span><span class="sxs-lookup"><span data-stu-id="11e41-245">Specify a different user-provided salt, or use a randomly generated salt, and attempt to sign the zone again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**\_Error \_ de DNS NSEC \_ incompatible \_ con el \_ \_ RSA \_ SHA1 de NSEC3**</span><span class="sxs-lookup"><span data-stu-id="11e41-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**DNS\_ERROR\_NSEC\_INCOMPATIBLE\_WITH\_NSEC3\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-247">9130 (0x23AA)</span><span class="sxs-lookup"><span data-stu-id="11e41-247">9130 (0x23AA)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-248">NSEC no es compatible con el algoritmo NSEC3-RSA-SHA-1.</span><span class="sxs-lookup"><span data-stu-id="11e41-248">NSEC is not compatible with the NSEC3-RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="11e41-249">Elija un algoritmo diferente o use NSEC3.</span><span class="sxs-lookup"><span data-stu-id="11e41-249">Choose a different algorithm or use NSEC3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**\_ \_ no hay registros de información de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**DNS\_INFO\_NO\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-251">9501 (0x251D)</span><span class="sxs-lookup"><span data-stu-id="11e41-251">9501 (0x251D)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-252">No se ha encontrado ningún registro para la consulta DNS especificada.</span><span class="sxs-lookup"><span data-stu-id="11e41-252">No records found for given DNS query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**ERROR de DNS en el \_ \_ \_ paquete incorrecto**</span><span class="sxs-lookup"><span data-stu-id="11e41-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**DNS\_ERROR\_BAD\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-254">9502 (0x251E)</span><span class="sxs-lookup"><span data-stu-id="11e41-254">9502 (0x251E)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-255">Paquete DNS incorrecto.</span><span class="sxs-lookup"><span data-stu-id="11e41-255">Bad DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**ERROR de DNS \_ \_ sin \_ paquete**</span><span class="sxs-lookup"><span data-stu-id="11e41-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**DNS\_ERROR\_NO\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-257">9503 (0x251F)</span><span class="sxs-lookup"><span data-stu-id="11e41-257">9503 (0x251F)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-258">No hay ningún paquete DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-258">No DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**\_RCODE de error de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**DNS\_ERROR\_RCODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-260">9504 (0x2520)</span><span class="sxs-lookup"><span data-stu-id="11e41-260">9504 (0x2520)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-261">Error de DNS, compruebe RCODE.</span><span class="sxs-lookup"><span data-stu-id="11e41-261">DNS error, check rcode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**ERROR de DNS \_ : \_ paquete no seguro \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**DNS\_ERROR\_UNSECURE\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-263">9505 (0x2521)</span><span class="sxs-lookup"><span data-stu-id="11e41-263">9505 (0x2521)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-264">Paquete DNS no seguro.</span><span class="sxs-lookup"><span data-stu-id="11e41-264">Unsecured DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**solicitud de DNS \_ \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="11e41-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**DNS\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-266">9506 (0x2522)</span><span class="sxs-lookup"><span data-stu-id="11e41-266">9506 (0x2522)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-267">La solicitud de consulta DNS está pendiente.</span><span class="sxs-lookup"><span data-stu-id="11e41-267">DNS query request is pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**tipo de error de DNS \_ \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**DNS\_ERROR\_INVALID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-269">9551 (0x254F)</span><span class="sxs-lookup"><span data-stu-id="11e41-269">9551 (0x254F)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-270">Tipo de DNS no válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-270">Invalid DNS type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**ERROR de DNS de \_ \_ \_ dirección IP no válida \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**DNS\_ERROR\_INVALID\_IP\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-272">9552 (0x2550)</span><span class="sxs-lookup"><span data-stu-id="11e41-272">9552 (0x2550)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-273">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="11e41-273">Invalid IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**\_propiedad error de DNS \_ no válida \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**DNS\_ERROR\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-275">9553 (0x2551)</span><span class="sxs-lookup"><span data-stu-id="11e41-275">9553 (0x2551)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-276">Propiedad no válida.</span><span class="sxs-lookup"><span data-stu-id="11e41-276">Invalid property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**ERROR de DNS \_ \_ inténtelo de \_ nuevo \_ más tarde**</span><span class="sxs-lookup"><span data-stu-id="11e41-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**DNS\_ERROR\_TRY\_AGAIN\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-278">9554 (0x2552)</span><span class="sxs-lookup"><span data-stu-id="11e41-278">9554 (0x2552)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-279">Vuelva a intentar la operación DNS más tarde.</span><span class="sxs-lookup"><span data-stu-id="11e41-279">Try DNS operation again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**ERROR de DNS \_ \_ no \_ único**</span><span class="sxs-lookup"><span data-stu-id="11e41-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**DNS\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-281">9555 (0x2553)</span><span class="sxs-lookup"><span data-stu-id="11e41-281">9555 (0x2553)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-282">El registro para el nombre y el tipo especificados no es único.</span><span class="sxs-lookup"><span data-stu-id="11e41-282">Record for given name and type is not unique.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**ERROR de DNS \_ \_ no \_ \_ nombre RFC**</span><span class="sxs-lookup"><span data-stu-id="11e41-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**DNS\_ERROR\_NON\_RFC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-284">9556 (0x2554)</span><span class="sxs-lookup"><span data-stu-id="11e41-284">9556 (0x2554)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-285">El nombre DNS no cumple las especificaciones RFC.</span><span class="sxs-lookup"><span data-stu-id="11e41-285">DNS name does not comply with RFC specifications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**\_FQDN de estado de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**DNS\_STATUS\_FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-287">9557 (0x2555)</span><span class="sxs-lookup"><span data-stu-id="11e41-287">9557 (0x2555)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-288">Nombre DNS es un nombre DNS completo.</span><span class="sxs-lookup"><span data-stu-id="11e41-288">DNS name is a fully-qualified DNS name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**\_nombre con \_ puntos de estado de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**DNS\_STATUS\_DOTTED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-290">9558 (0x2556)</span><span class="sxs-lookup"><span data-stu-id="11e41-290">9558 (0x2556)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-291">El nombre DNS tiene puntos (varias etiquetas).</span><span class="sxs-lookup"><span data-stu-id="11e41-291">DNS name is dotted (multi-label).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**\_nombre de \_ una sola \_ parte \_ de estado de DNS**</span><span class="sxs-lookup"><span data-stu-id="11e41-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**DNS\_STATUS\_SINGLE\_PART\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-293">9559 (0x2557)</span><span class="sxs-lookup"><span data-stu-id="11e41-293">9559 (0x2557)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-294">El nombre DNS es un nombre de una sola parte.</span><span class="sxs-lookup"><span data-stu-id="11e41-294">DNS name is a single-part name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**ERROR de DNS \_ \_ nombre no válido \_ \_ Char**</span><span class="sxs-lookup"><span data-stu-id="11e41-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**DNS\_ERROR\_INVALID\_NAME\_CHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-296">9560 (0x2558)</span><span class="sxs-lookup"><span data-stu-id="11e41-296">9560 (0x2558)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-297">El nombre DNS contiene un carácter no válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-297">DNS name contains an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**\_ \_ nombre numérico del error de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**DNS\_ERROR\_NUMERIC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-299">9561 (0x2559)</span><span class="sxs-lookup"><span data-stu-id="11e41-299">9561 (0x2559)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-300">El nombre DNS es totalmente numérico.</span><span class="sxs-lookup"><span data-stu-id="11e41-300">DNS name is entirely numeric.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**\_error \_ de DNS no \_ permitido en el \_ \_ \_ servidor raíz**</span><span class="sxs-lookup"><span data-stu-id="11e41-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ROOT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-302">9562 (0x255A)</span><span class="sxs-lookup"><span data-stu-id="11e41-302">9562 (0x255A)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-303">La operación solicitada no se permite en un servidor raíz DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-303">The operation requested is not permitted on a DNS root server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**\_error \_ de DNS no \_ permitido en la \_ \_ delegación**</span><span class="sxs-lookup"><span data-stu-id="11e41-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DELEGATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-305">9563 (0x255B)</span><span class="sxs-lookup"><span data-stu-id="11e41-305">9563 (0x255B)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-306">No se pudo crear el registro porque esta parte del espacio de nombres DNS se ha delegado en otro servidor.</span><span class="sxs-lookup"><span data-stu-id="11e41-306">The record could not be created because this part of the DNS namespace has been delegated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**ERROR de DNS \_ \_ no se \_ encuentran \_ sugerencias de raíz \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**DNS\_ERROR\_CANNOT\_FIND\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-308">9564 (0x255C)</span><span class="sxs-lookup"><span data-stu-id="11e41-308">9564 (0x255C)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-309">El servidor DNS no encontró un conjunto de sugerencias de raíz.</span><span class="sxs-lookup"><span data-stu-id="11e41-309">The DNS server could not find a set of root hints.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**ERROR de DNS \_ : \_ sugerencias de raíz incoherentes \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**DNS\_ERROR\_INCONSISTENT\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-311">9565 (0x255D)</span><span class="sxs-lookup"><span data-stu-id="11e41-311">9565 (0x255D)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-312">El servidor DNS encontró sugerencias de raíz pero no eran coherentes en todos los adaptadores.</span><span class="sxs-lookup"><span data-stu-id="11e41-312">The DNS server found root hints but they were not consistent across all adapters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**\_valor DWORD de error de DNS \_ \_ \_ demasiado \_ pequeño**</span><span class="sxs-lookup"><span data-stu-id="11e41-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-314">9566 (0x255E)</span><span class="sxs-lookup"><span data-stu-id="11e41-314">9566 (0x255E)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-315">El valor especificado es demasiado pequeño para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="11e41-315">The specified value is too small for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**\_valor DWORD de error de DNS \_ \_ \_ demasiado \_ grande**</span><span class="sxs-lookup"><span data-stu-id="11e41-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-317">9567 (0x255F)</span><span class="sxs-lookup"><span data-stu-id="11e41-317">9567 (0x255F)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-318">El valor especificado es demasiado grande para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="11e41-318">The specified value is too large for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**\_ \_ carga en segundo plano de error de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**DNS\_ERROR\_BACKGROUND\_LOADING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-320">9568 (0x2560)</span><span class="sxs-lookup"><span data-stu-id="11e41-320">9568 (0x2560)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-321">Esta operación no está permitida mientras el servidor DNS está cargando zonas en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="11e41-321">This operation is not allowed while the DNS server is loading zones in the background.</span></span> <span data-ttu-id="11e41-322">Vuelva a intentarlo más tarde.</span><span class="sxs-lookup"><span data-stu-id="11e41-322">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**\_error \_ de DNS no \_ permitido \_ en \_ RODC**</span><span class="sxs-lookup"><span data-stu-id="11e41-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_RODC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-324">9569 (0x2561)</span><span class="sxs-lookup"><span data-stu-id="11e41-324">9569 (0x2561)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-325">La operación solicitada no se permite en un servidor DNS que se ejecuta en un controlador de dominio de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="11e41-325">The operation requested is not permitted on against a DNS server running on a read-only DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**\_error \_ de DNS no \_ permitido \_ en \_ dname**</span><span class="sxs-lookup"><span data-stu-id="11e41-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-327">9570 (0x2562)</span><span class="sxs-lookup"><span data-stu-id="11e41-327">9570 (0x2562)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-328">No se permite la existencia de datos debajo de un registro DNAME.</span><span class="sxs-lookup"><span data-stu-id="11e41-328">No data is allowed to exist underneath a DNAME record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**se \_ \_ requiere la delegación de error de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**DNS\_ERROR\_DELEGATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-330">9571 (0x2563)</span><span class="sxs-lookup"><span data-stu-id="11e41-330">9571 (0x2563)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-331">Esta operación requiere la delegación de credenciales.</span><span class="sxs-lookup"><span data-stu-id="11e41-331">This operation requires credentials delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**ERROR de DNS en la \_ \_ tabla de directivas no válida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**DNS\_ERROR\_INVALID\_POLICY\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-333">9572 (0x2564)</span><span class="sxs-lookup"><span data-stu-id="11e41-333">9572 (0x2564)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-334">La tabla de directivas de resolución de nombres está dañada.</span><span class="sxs-lookup"><span data-stu-id="11e41-334">Name resolution policy table has been corrupted.</span></span> <span data-ttu-id="11e41-335">Se producirá un error en la resolución de DNS hasta que se corrija.</span><span class="sxs-lookup"><span data-stu-id="11e41-335">DNS resolution will fail until it is fixed.</span></span> <span data-ttu-id="11e41-336">Póngase en contacto con el administrador de red.</span><span class="sxs-lookup"><span data-stu-id="11e41-336">Contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**\_ \_ \_ \_ no \_ existe la zona de errores de DNS**</span><span class="sxs-lookup"><span data-stu-id="11e41-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**DNS\_ERROR\_ZONE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-338">9601 (0x2581)</span><span class="sxs-lookup"><span data-stu-id="11e41-338">9601 (0x2581)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-339">La zona DNS no existe.</span><span class="sxs-lookup"><span data-stu-id="11e41-339">DNS zone does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**ERROR de DNS \_ \_ no hay \_ información de zona \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**DNS\_ERROR\_NO\_ZONE\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-341">9602 (0x2582)</span><span class="sxs-lookup"><span data-stu-id="11e41-341">9602 (0x2582)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-342">Información de zona DNS no disponible.</span><span class="sxs-lookup"><span data-stu-id="11e41-342">DNS zone information not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**ERROR de DNS \_ \_ operación de zona no válida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**DNS\_ERROR\_INVALID\_ZONE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-344">9603 (0x2583)</span><span class="sxs-lookup"><span data-stu-id="11e41-344">9603 (0x2583)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-345">Operación no válida para la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-345">Invalid operation for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**\_error de \_ configuración de zona de error de DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**DNS\_ERROR\_ZONE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-347">9604 (0x2584)</span><span class="sxs-lookup"><span data-stu-id="11e41-347">9604 (0x2584)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-348">Configuración de zona DNS no válida.</span><span class="sxs-lookup"><span data-stu-id="11e41-348">Invalid DNS zone configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**la \_ zona de errores de DNS \_ \_ \_ no tiene ningún \_ \_ registro SOA**</span><span class="sxs-lookup"><span data-stu-id="11e41-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_SOA\_RECORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-350">9605 (0x2585)</span><span class="sxs-lookup"><span data-stu-id="11e41-350">9605 (0x2585)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-351">La zona DNS no tiene registro de inicio de autoridad (SOA).</span><span class="sxs-lookup"><span data-stu-id="11e41-351">DNS zone has no start of authority (SOA) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**la \_ zona de errores de DNS \_ \_ \_ no tiene \_ \_ registros NS**</span><span class="sxs-lookup"><span data-stu-id="11e41-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_NS\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-353">9606 (0x2586)</span><span class="sxs-lookup"><span data-stu-id="11e41-353">9606 (0x2586)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-354">La zona DNS no tiene un registro de servidor de nombres (NS).</span><span class="sxs-lookup"><span data-stu-id="11e41-354">DNS zone has no Name Server (NS) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**zona de errores de DNS \_ \_ \_ bloqueada**</span><span class="sxs-lookup"><span data-stu-id="11e41-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**DNS\_ERROR\_ZONE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-356">9607 (0x2587)</span><span class="sxs-lookup"><span data-stu-id="11e41-356">9607 (0x2587)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-357">La zona DNS está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="11e41-357">DNS zone is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**\_ \_ \_ \_ no se pudo crear la zona de errores de DNS**</span><span class="sxs-lookup"><span data-stu-id="11e41-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**DNS\_ERROR\_ZONE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-359">9608 (0x2588)</span><span class="sxs-lookup"><span data-stu-id="11e41-359">9608 (0x2588)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-360">No se pudo crear la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-360">DNS zone creation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**\_ \_ \_ ya existe una zona de errores de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**DNS\_ERROR\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-362">9609 (0x2589)</span><span class="sxs-lookup"><span data-stu-id="11e41-362">9609 (0x2589)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-363">La zona DNS ya existe.</span><span class="sxs-lookup"><span data-stu-id="11e41-363">DNS zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**ERROR de DNS \_ \_ AutoZone \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="11e41-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**DNS\_ERROR\_AUTOZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-365">9610 (0x258A)</span><span class="sxs-lookup"><span data-stu-id="11e41-365">9610 (0x258A)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-366">La zona automática DNS ya existe.</span><span class="sxs-lookup"><span data-stu-id="11e41-366">DNS automatic zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**ERROR de DNS \_ \_ tipo de zona no válida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**DNS\_ERROR\_INVALID\_ZONE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-368">9611 (0x258B)</span><span class="sxs-lookup"><span data-stu-id="11e41-368">9611 (0x258B)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-369">Tipo de zona DNS no válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-369">Invalid DNS zone type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**el \_ secundario de error de DNS \_ requiere una \_ \_ \_ dirección IP maestra**</span><span class="sxs-lookup"><span data-stu-id="11e41-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**DNS\_ERROR\_SECONDARY\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-371">9612 (0x258C)</span><span class="sxs-lookup"><span data-stu-id="11e41-371">9612 (0x258C)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-372">La zona DNS secundaria requiere una dirección IP maestra.</span><span class="sxs-lookup"><span data-stu-id="11e41-372">Secondary DNS zone requires master IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**zona de errores de DNS \_ \_ \_ no \_ secundaria**</span><span class="sxs-lookup"><span data-stu-id="11e41-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**DNS\_ERROR\_ZONE\_NOT\_SECONDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-374">9613 (0x258D)</span><span class="sxs-lookup"><span data-stu-id="11e41-374">9613 (0x258D)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-375">Zona DNS no secundaria.</span><span class="sxs-lookup"><span data-stu-id="11e41-375">DNS zone not secondary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**los \_ errores de DNS \_ necesitan \_ direcciones secundarias \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**DNS\_ERROR\_NEED\_SECONDARY\_ADDRESSES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-377">9614 (0x258E)</span><span class="sxs-lookup"><span data-stu-id="11e41-377">9614 (0x258E)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-378">Se necesita una dirección IP secundaria.</span><span class="sxs-lookup"><span data-stu-id="11e41-378">Need secondary IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**\_ \_ \_ \_ no se pudo inicializar el error de DNS WINS init**</span><span class="sxs-lookup"><span data-stu-id="11e41-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**DNS\_ERROR\_WINS\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-380">9615 (0x258F)</span><span class="sxs-lookup"><span data-stu-id="11e41-380">9615 (0x258F)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-381">Error de inicialización de WINS.</span><span class="sxs-lookup"><span data-stu-id="11e41-381">WINS initialization failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**\_los errores de DNS \_ necesitan \_ \_ servidores WINS**</span><span class="sxs-lookup"><span data-stu-id="11e41-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**DNS\_ERROR\_NEED\_WINS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-383">9616 (0x2590)</span><span class="sxs-lookup"><span data-stu-id="11e41-383">9616 (0x2590)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-384">Necesita servidores WINS.</span><span class="sxs-lookup"><span data-stu-id="11e41-384">Need WINS servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**error de DNS \_ \_ NBSTAT \_ init \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**DNS\_ERROR\_NBSTAT\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-386">9617 (0x2591)</span><span class="sxs-lookup"><span data-stu-id="11e41-386">9617 (0x2591)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-387">Error en la llamada de inicialización de NBTSTAT.</span><span class="sxs-lookup"><span data-stu-id="11e41-387">NBTSTAT initialization call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**ERROR de DNS \_ \_ SOA de \_ eliminación \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="11e41-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**DNS\_ERROR\_SOA\_DELETE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-389">9618 (0x2592)</span><span class="sxs-lookup"><span data-stu-id="11e41-389">9618 (0x2592)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-390">Eliminación de inicio de autoridad (SOA) no válida.</span><span class="sxs-lookup"><span data-stu-id="11e41-390">Invalid delete of start of authority (SOA).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**el \_ reenviador de errores de DNS \_ \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="11e41-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**DNS\_ERROR\_FORWARDER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-392">9619 (0x2593)</span><span class="sxs-lookup"><span data-stu-id="11e41-392">9619 (0x2593)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-393">Ya existe una zona de reenvío condicional para ese nombre.</span><span class="sxs-lookup"><span data-stu-id="11e41-393">A conditional forwarding zone already exists for that name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**la \_ zona de errores de DNS \_ requiere una \_ \_ \_ dirección IP maestra**</span><span class="sxs-lookup"><span data-stu-id="11e41-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**DNS\_ERROR\_ZONE\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-395">9620 (0x2594)</span><span class="sxs-lookup"><span data-stu-id="11e41-395">9620 (0x2594)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-396">Esta zona debe estar configurada con una o más direcciones IP de servidor DNS maestro.</span><span class="sxs-lookup"><span data-stu-id="11e41-396">This zone must be configured with one or more master DNS server IP addresses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**la \_ zona de errores de DNS \_ \_ está \_ apagada**</span><span class="sxs-lookup"><span data-stu-id="11e41-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**DNS\_ERROR\_ZONE\_IS\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-398">9621 (0x2595)</span><span class="sxs-lookup"><span data-stu-id="11e41-398">9621 (0x2595)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-399">No se puede realizar la operación porque esta zona está apagada.</span><span class="sxs-lookup"><span data-stu-id="11e41-399">The operation cannot be performed because this zone is shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**\_ \_ zona de errores \_ de DNS bloqueada \_ para \_ firmar**</span><span class="sxs-lookup"><span data-stu-id="11e41-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**DNS\_ERROR\_ZONE\_LOCKED\_FOR\_SIGNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-401">9622 (0x2596)</span><span class="sxs-lookup"><span data-stu-id="11e41-401">9622 (0x2596)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-402">No se puede realizar esta operación porque la zona se está firmando actualmente.</span><span class="sxs-lookup"><span data-stu-id="11e41-402">This operation cannot be performed because the zone is currently being signed.</span></span> <span data-ttu-id="11e41-403">Vuelva a intentarlo más tarde.</span><span class="sxs-lookup"><span data-stu-id="11e41-403">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**el \_ error de DNS \_ principal \_ requiere un archivo de \_ archivos**</span><span class="sxs-lookup"><span data-stu-id="11e41-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**DNS\_ERROR\_PRIMARY\_REQUIRES\_DATAFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-405">9651 (0x25B3)</span><span class="sxs-lookup"><span data-stu-id="11e41-405">9651 (0x25B3)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-406">La zona DNS principal requiere un archivo de archivos.</span><span class="sxs-lookup"><span data-stu-id="11e41-406">Primary DNS zone requires datafile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**ERROR de DNS \_ \_ nombre de archivo de archivos no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**DNS\_ERROR\_INVALID\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-408">9652 (0x25B4)</span><span class="sxs-lookup"><span data-stu-id="11e41-408">9652 (0x25B4)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-409">Nombre de archivo de la zona DNS no válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-409">Invalid datafile name for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**error \_ de \_ apertura de archivo de archivo de errores de \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**DNS\_ERROR\_DATAFILE\_OPEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-411">9653 (0x25B5)</span><span class="sxs-lookup"><span data-stu-id="11e41-411">9653 (0x25B5)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-412">No se pudo abrir el archivo de archivos para la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-412">Failed to open datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**\_error de \_ \_ escritura diferida del archivo de error de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**DNS\_ERROR\_FILE\_WRITEBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-414">9654 (0x25B6)</span><span class="sxs-lookup"><span data-stu-id="11e41-414">9654 (0x25B6)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-415">No se pudo escribir el archivo de archivos para la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-415">Failed to write datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**\_análisis de \_ archivos de errores de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**DNS\_ERROR\_DATAFILE\_PARSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-417">9655 (0x25B7)</span><span class="sxs-lookup"><span data-stu-id="11e41-417">9655 (0x25B7)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-418">Error al leer el archivo de archivos para la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-418">Failure while reading datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**el registro de errores de DNS no \_ \_ \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="11e41-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**DNS\_ERROR\_RECORD\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-420">9701 (0x25E5)</span><span class="sxs-lookup"><span data-stu-id="11e41-420">9701 (0x25E5)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-421">El registro DNS no existe.</span><span class="sxs-lookup"><span data-stu-id="11e41-421">DNS record does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**\_formato de \_ registro de errores de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**DNS\_ERROR\_RECORD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-423">9702 (0x25E6)</span><span class="sxs-lookup"><span data-stu-id="11e41-423">9702 (0x25E6)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-424">Error de formato de registro DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-424">DNS record format error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**\_ \_ \_ \_ no se pudo crear el nodo de error de DNS**</span><span class="sxs-lookup"><span data-stu-id="11e41-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**DNS\_ERROR\_NODE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-426">9703 (0x25E7)</span><span class="sxs-lookup"><span data-stu-id="11e41-426">9703 (0x25E7)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-427">Error de creación de nodo en DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-427">Node creation failure in DNS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**\_tipo de registro de error desconocido de DNS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**DNS\_ERROR\_UNKNOWN\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-429">9704 (0x25E8)</span><span class="sxs-lookup"><span data-stu-id="11e41-429">9704 (0x25E8)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-430">Tipo de registro DNS desconocido.</span><span class="sxs-lookup"><span data-stu-id="11e41-430">Unknown DNS record type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**se \_ \_ \_ agotó el tiempo de espera del registro de errores de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**DNS\_ERROR\_RECORD\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-432">9705 (0x25E9)</span><span class="sxs-lookup"><span data-stu-id="11e41-432">9705 (0x25E9)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-433">El registro DNS agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="11e41-433">DNS record timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**\_ \_ nombre de error \_ de DNS no \_ en \_ zona**</span><span class="sxs-lookup"><span data-stu-id="11e41-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**DNS\_ERROR\_NAME\_NOT\_IN\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-435">9706 (0x25EA)</span><span class="sxs-lookup"><span data-stu-id="11e41-435">9706 (0x25EA)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-436">El nombre no está en la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-436">Name not in DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**\_ \_ bucle CNAME de error de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**DNS\_ERROR\_CNAME\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-438">9707 (0x25EB)</span><span class="sxs-lookup"><span data-stu-id="11e41-438">9707 (0x25EB)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-439">Se detectó un bucle CNAME.</span><span class="sxs-lookup"><span data-stu-id="11e41-439">CNAME loop detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**el \_ nodo de error de DNS \_ \_ es \_ CNAME**</span><span class="sxs-lookup"><span data-stu-id="11e41-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**DNS\_ERROR\_NODE\_IS\_CNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-441">9708 (0x25EC)</span><span class="sxs-lookup"><span data-stu-id="11e41-441">9708 (0x25EC)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-442">El nodo es un registro DNS CNAME.</span><span class="sxs-lookup"><span data-stu-id="11e41-442">Node is a CNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**\_ \_ colisión CNAME de error de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**DNS\_ERROR\_CNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-444">9709 (0x25ED)</span><span class="sxs-lookup"><span data-stu-id="11e41-444">9709 (0x25ED)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-445">Ya existe un registro CNAME para el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="11e41-445">A CNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**\_ \_ registro de error \_ de DNS solo \_ en la raíz de la \_ zona \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**DNS\_ERROR\_RECORD\_ONLY\_AT\_ZONE\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-447">9710 (0x25EE)</span><span class="sxs-lookup"><span data-stu-id="11e41-447">9710 (0x25EE)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-448">Registre solo en la raíz de la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-448">Record only at DNS zone root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**el \_ registro de errores de DNS \_ \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="11e41-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**DNS\_ERROR\_RECORD\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-450">9711 (0x25EF)</span><span class="sxs-lookup"><span data-stu-id="11e41-450">9711 (0x25EF)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-451">El registro DNS ya existe.</span><span class="sxs-lookup"><span data-stu-id="11e41-451">DNS record already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**\_ \_ datos secundarios de error de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**DNS\_ERROR\_SECONDARY\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-453">9712 (0x25F0)</span><span class="sxs-lookup"><span data-stu-id="11e41-453">9712 (0x25F0)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-454">Error de datos de la zona DNS secundaria.</span><span class="sxs-lookup"><span data-stu-id="11e41-454">Secondary DNS zone data error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**ERROR de DNS \_ \_ no \_ crear \_ datos de caché \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**DNS\_ERROR\_NO\_CREATE\_CACHE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-456">9713 (0x25F1)</span><span class="sxs-lookup"><span data-stu-id="11e41-456">9713 (0x25F1)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-457">No se pudieron crear los datos de caché DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-457">Could not create DNS cache data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**\_ \_ \_ \_ no \_ existe el nombre de error de DNS**</span><span class="sxs-lookup"><span data-stu-id="11e41-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**DNS\_ERROR\_NAME\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-459">9714 (0x25F2)</span><span class="sxs-lookup"><span data-stu-id="11e41-459">9714 (0x25F2)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-460">El nombre DNS no existe.</span><span class="sxs-lookup"><span data-stu-id="11e41-460">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**\_error de \_ creación de PTR de advertencia de DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**DNS\_WARNING\_PTR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-462">9715 (0x25F3)</span><span class="sxs-lookup"><span data-stu-id="11e41-462">9715 (0x25F3)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-463">No se pudo crear el registro de puntero (PTR).</span><span class="sxs-lookup"><span data-stu-id="11e41-463">Could not create pointer (PTR) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**dominio de advertencia de DNS no \_ \_ \_ eliminado**</span><span class="sxs-lookup"><span data-stu-id="11e41-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS\_WARNING\_DOMAIN\_UNDELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-465">9716 (0x25F4)</span><span class="sxs-lookup"><span data-stu-id="11e41-465">9716 (0x25F4)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-466">Se ha cancelado la eliminación del dominio DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-466">DNS domain was undeleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**ERROR de DNS \_ \_ DS \_ no disponible**</span><span class="sxs-lookup"><span data-stu-id="11e41-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**DNS\_ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-468">9717 (0x25F5)</span><span class="sxs-lookup"><span data-stu-id="11e41-468">9717 (0x25F5)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-469">El servicio de directorio no está disponible.</span><span class="sxs-lookup"><span data-stu-id="11e41-469">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**la \_ zona DS error de DNS \_ \_ \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="11e41-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**DNS\_ERROR\_DS\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-471">9718 (0x25F6)</span><span class="sxs-lookup"><span data-stu-id="11e41-471">9718 (0x25F6)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-472">La zona DNS ya existe en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="11e41-472">DNS zone already exists in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**ERROR de DNS \_ \_ no de \_ arranque si la \_ \_ \_ zona DS**</span><span class="sxs-lookup"><span data-stu-id="11e41-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**DNS\_ERROR\_NO\_BOOTFILE\_IF\_DS\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-474">9719 (0x25F7)</span><span class="sxs-lookup"><span data-stu-id="11e41-474">9719 (0x25F7)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-475">El servidor DNS no está creando o leyendo el archivo de arranque para la zona DNS integrada del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="11e41-475">DNS server not creating or reading the boot file for the directory service integrated DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**el \_ nodo de error de DNS \_ \_ es \_ dname**</span><span class="sxs-lookup"><span data-stu-id="11e41-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**DNS\_ERROR\_NODE\_IS\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-477">9720 (0x25F8)</span><span class="sxs-lookup"><span data-stu-id="11e41-477">9720 (0x25F8)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-478">El nodo es un registro DNS DNAME.</span><span class="sxs-lookup"><span data-stu-id="11e41-478">Node is a DNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**\_ \_ colisión dname de error de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**DNS\_ERROR\_DNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-480">9721 (0x25F9)</span><span class="sxs-lookup"><span data-stu-id="11e41-480">9721 (0x25F9)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-481">Ya existe un registro DNAME para el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="11e41-481">A DNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**\_bucle de \_ alias de error de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**DNS\_ERROR\_ALIAS\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-483">9722 (0x25FA)</span><span class="sxs-lookup"><span data-stu-id="11e41-483">9722 (0x25FA)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-484">Se ha detectado un bucle de alias con registros CNAME o DNAME.</span><span class="sxs-lookup"><span data-stu-id="11e41-484">An alias loop has been detected with either CNAME or DNAME records.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**información de DNS \_ \_ AXFR \_ completada**</span><span class="sxs-lookup"><span data-stu-id="11e41-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**DNS\_INFO\_AXFR\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-486">9751 (0x2617)</span><span class="sxs-lookup"><span data-stu-id="11e41-486">9751 (0x2617)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-487">DNS AXFR (transferencia de zona) completo.</span><span class="sxs-lookup"><span data-stu-id="11e41-487">DNS AXFR (zone transfer) complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**ERROR de DNS \_ \_ AXFR**</span><span class="sxs-lookup"><span data-stu-id="11e41-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**DNS\_ERROR\_AXFR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-489">9752 (0x2618)</span><span class="sxs-lookup"><span data-stu-id="11e41-489">9752 (0x2618)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-490">No se pudo realizar la transferencia de zona DNS.</span><span class="sxs-lookup"><span data-stu-id="11e41-490">DNS zone transfer failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**información de DNS \_ \_ agregada en el \_ \_ servidor WINS local**</span><span class="sxs-lookup"><span data-stu-id="11e41-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**DNS\_INFO\_ADDED\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-492">9753 (0x2619)</span><span class="sxs-lookup"><span data-stu-id="11e41-492">9753 (0x2619)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-493">Se ha agregado el servidor WINS local.</span><span class="sxs-lookup"><span data-stu-id="11e41-493">Added local WINS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**el \_ Estado de DNS \_ continúa siendo \_ necesario**</span><span class="sxs-lookup"><span data-stu-id="11e41-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**DNS\_STATUS\_CONTINUE\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-495">9801 (0x2649)</span><span class="sxs-lookup"><span data-stu-id="11e41-495">9801 (0x2649)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-496">La llamada de actualización segura debe continuar con la solicitud de actualización.</span><span class="sxs-lookup"><span data-stu-id="11e41-496">Secure update call needs to continue update request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**ERROR de DNS \_ \_ sin \_ TCPIP**</span><span class="sxs-lookup"><span data-stu-id="11e41-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**DNS\_ERROR\_NO\_TCPIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-498">9851 (0x267B)</span><span class="sxs-lookup"><span data-stu-id="11e41-498">9851 (0x267B)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-499">El protocolo de red TCP/IP no está instalado.</span><span class="sxs-lookup"><span data-stu-id="11e41-499">TCP/IP network protocol not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**ERROR de DNS \_ \_ sin \_ \_ servidores DNS**</span><span class="sxs-lookup"><span data-stu-id="11e41-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**DNS\_ERROR\_NO\_DNS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-501">9852 (0x267C)</span><span class="sxs-lookup"><span data-stu-id="11e41-501">9852 (0x267C)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-502">No hay servidores DNS configurados para el sistema local.</span><span class="sxs-lookup"><span data-stu-id="11e41-502">No DNS servers configured for local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**el DP de error de DNS no \_ \_ \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="11e41-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**DNS\_ERROR\_DP\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-504">9901 (0x26AD)</span><span class="sxs-lookup"><span data-stu-id="11e41-504">9901 (0x26AD)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-505">La partición de directorio especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="11e41-505">The specified directory partition does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**el \_ error de DNS \_ DP \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="11e41-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**DNS\_ERROR\_DP\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-507">9902 (0x26AE)</span><span class="sxs-lookup"><span data-stu-id="11e41-507">9902 (0x26AE)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-508">La partición de directorio especificada ya existe.</span><span class="sxs-lookup"><span data-stu-id="11e41-508">The specified directory partition already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**no se ha dado de \_ alta el DP de error de DNS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**DNS\_ERROR\_DP\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-510">9903 (0x26AF)</span><span class="sxs-lookup"><span data-stu-id="11e41-510">9903 (0x26AF)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-511">Este servidor DNS no está dado de alta en la partición de directorio especificada.</span><span class="sxs-lookup"><span data-stu-id="11e41-511">This DNS server is not enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**ERROR de DNS \_ \_ DP ya dado de \_ \_ alta**</span><span class="sxs-lookup"><span data-stu-id="11e41-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**DNS\_ERROR\_DP\_ALREADY\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-513">9904 (0x26B0)</span><span class="sxs-lookup"><span data-stu-id="11e41-513">9904 (0x26B0)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-514">Este servidor DNS ya está dado de alta en la partición de directorio especificada.</span><span class="sxs-lookup"><span data-stu-id="11e41-514">This DNS server is already enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**el \_ DP de error de DNS \_ \_ no \_ está disponible**</span><span class="sxs-lookup"><span data-stu-id="11e41-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**DNS\_ERROR\_DP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-516">9905 (0x26B1)</span><span class="sxs-lookup"><span data-stu-id="11e41-516">9905 (0x26B1)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-517">La partición de directorio no está disponible en este momento.</span><span class="sxs-lookup"><span data-stu-id="11e41-517">The directory partition is not available at this time.</span></span> <span data-ttu-id="11e41-518">Espere unos minutos y vuelva a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="11e41-518">Please wait a few minutes and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**error \_ de \_ FSMO de DP de error de \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**DNS\_ERROR\_DP\_FSMO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-520">9906 (0x26B2)</span><span class="sxs-lookup"><span data-stu-id="11e41-520">9906 (0x26B2)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-521">No se pudo realizar la operación porque no se pudo alcanzar el rol FSMO del maestro de nomenclatura de dominios.</span><span class="sxs-lookup"><span data-stu-id="11e41-521">The operation failed because the domain naming master FSMO role could not be reached.</span></span> <span data-ttu-id="11e41-522">El controlador de dominio que contiene el rol FSMO del maestro de nombres de dominio está inactivo o no puede atender la solicitud o no está ejecutando Windows Server 2003 o posterior.</span><span class="sxs-lookup"><span data-stu-id="11e41-522">The domain controller holding the domain naming master FSMO role is down or unable to service the request or is not running Windows Server 2003 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="11e41-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-524">10004 (0x2714)</span><span class="sxs-lookup"><span data-stu-id="11e41-524">10004 (0x2714)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-525">Una operación de bloqueo fue interrumpida por una llamada a WSACancelBlockingCall.</span><span class="sxs-lookup"><span data-stu-id="11e41-525">A blocking operation was interrupted by a call to WSACancelBlockingCall.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**</span><span class="sxs-lookup"><span data-stu-id="11e41-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-527">10009 (0x2719)</span><span class="sxs-lookup"><span data-stu-id="11e41-527">10009 (0x2719)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-528">El identificador de archivo proporcionado no es válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-528">The file handle supplied is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="11e41-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-530">10013 (0x271D)</span><span class="sxs-lookup"><span data-stu-id="11e41-530">10013 (0x271D)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-531">Se intentó tener acceso a un socket de una manera prohibida por sus permisos de acceso.</span><span class="sxs-lookup"><span data-stu-id="11e41-531">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="11e41-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-533">10014 (0x271E)</span><span class="sxs-lookup"><span data-stu-id="11e41-533">10014 (0x271E)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-534">El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada.</span><span class="sxs-lookup"><span data-stu-id="11e41-534">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="11e41-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-536">10022 (0x2726)</span><span class="sxs-lookup"><span data-stu-id="11e41-536">10022 (0x2726)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-537">Se proporcionó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-537">An invalid argument was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**</span><span class="sxs-lookup"><span data-stu-id="11e41-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-539">10024 (0x2728)</span><span class="sxs-lookup"><span data-stu-id="11e41-539">10024 (0x2728)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-540">Demasiados Sockets abiertos.</span><span class="sxs-lookup"><span data-stu-id="11e41-540">Too many open sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span><span class="sxs-lookup"><span data-stu-id="11e41-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-542">10035 (0x2733)</span><span class="sxs-lookup"><span data-stu-id="11e41-542">10035 (0x2733)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-543">No se pudo completar de inmediato una operación de socket que no sea de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="11e41-543">A non-blocking socket operation could not be completed immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="11e41-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-545">10036 (0x2734)</span><span class="sxs-lookup"><span data-stu-id="11e41-545">10036 (0x2734)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-546">Se está ejecutando una operación de bloqueo actualmente.</span><span class="sxs-lookup"><span data-stu-id="11e41-546">A blocking operation is currently executing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**</span><span class="sxs-lookup"><span data-stu-id="11e41-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-548">10037 (0x2735)</span><span class="sxs-lookup"><span data-stu-id="11e41-548">10037 (0x2735)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-549">Se ha intentado una operación en un socket que no es de bloqueo y que ya tenía una operación en marcha.</span><span class="sxs-lookup"><span data-stu-id="11e41-549">An operation was attempted on a non-blocking socket that already had an operation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="11e41-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-551">10038 (0x2736)</span><span class="sxs-lookup"><span data-stu-id="11e41-551">10038 (0x2736)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-552">Se intentó realizar una operación en algo que no es un socket.</span><span class="sxs-lookup"><span data-stu-id="11e41-552">An operation was attempted on something that is not a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span><span class="sxs-lookup"><span data-stu-id="11e41-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-554">10039 (0x2737)</span><span class="sxs-lookup"><span data-stu-id="11e41-554">10039 (0x2737)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-555">Se ha omitido una dirección necesaria de una operación en un socket.</span><span class="sxs-lookup"><span data-stu-id="11e41-555">A required address was omitted from an operation on a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="11e41-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-557">10040 (0x2738)</span><span class="sxs-lookup"><span data-stu-id="11e41-557">10040 (0x2738)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-558">Un mensaje enviado en un socket de datagrama es más largo que el búfer de mensajes interno o que algún otro límite de la red, o bien el búfer usado para recibir un datagrama es más pequeño que el datagrama.</span><span class="sxs-lookup"><span data-stu-id="11e41-558">A message sent on a datagram socket was larger than the internal message buffer or some other network limit, or the buffer used to receive a datagram into was smaller than the datagram itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span><span class="sxs-lookup"><span data-stu-id="11e41-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-560">10041 (0x2739)</span><span class="sxs-lookup"><span data-stu-id="11e41-560">10041 (0x2739)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-561">Se especificó un protocolo en la llamada de función de socket que no admite la semántica del tipo de socket solicitado.</span><span class="sxs-lookup"><span data-stu-id="11e41-561">A protocol was specified in the socket function call that does not support the semantics of the socket type requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="11e41-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-563">10042 (0x273A)</span><span class="sxs-lookup"><span data-stu-id="11e41-563">10042 (0x273A)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-564">Se especificó una opción o un nivel desconocido, no válido o no admitido en una llamada a getsockopt o a un método.</span><span class="sxs-lookup"><span data-stu-id="11e41-564">An unknown, invalid, or unsupported option or level was specified in a getsockopt or setsockopt call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="11e41-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-566">10043 (0x273B)</span><span class="sxs-lookup"><span data-stu-id="11e41-566">10043 (0x273B)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-567">El protocolo solicitado no se ha configurado en el sistema o no existe ninguna implementación para él.</span><span class="sxs-lookup"><span data-stu-id="11e41-567">The requested protocol has not been configured into the system, or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="11e41-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-569">10044 (0x273C)</span><span class="sxs-lookup"><span data-stu-id="11e41-569">10044 (0x273C)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-570">Esta familia de direcciones no es compatible con el tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="11e41-570">The support for the specified socket type does not exist in this address family.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="11e41-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-572">10045 (0x273D)</span><span class="sxs-lookup"><span data-stu-id="11e41-572">10045 (0x273D)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-573">La operación intentada no se admite para el tipo de objeto al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="11e41-573">The attempted operation is not supported for the type of object referenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="11e41-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-575">10046 (0x273E)</span><span class="sxs-lookup"><span data-stu-id="11e41-575">10046 (0x273E)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-576">La familia de protocolos no se ha configurado en el sistema o no existe ninguna implementación para ella.</span><span class="sxs-lookup"><span data-stu-id="11e41-576">The protocol family has not been configured into the system or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="11e41-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-578">10047 (0x273F)</span><span class="sxs-lookup"><span data-stu-id="11e41-578">10047 (0x273F)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-579">Se usó una dirección no compatible con el protocolo solicitado.</span><span class="sxs-lookup"><span data-stu-id="11e41-579">An address incompatible with the requested protocol was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span><span class="sxs-lookup"><span data-stu-id="11e41-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-581">10048 (0x2740)</span><span class="sxs-lookup"><span data-stu-id="11e41-581">10048 (0x2740)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-582">Only one usage of each socket address (protocol/network address/port) is normally permitted.</span><span class="sxs-lookup"><span data-stu-id="11e41-582">Only one usage of each socket address (protocol/network address/port) is normally permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**</span><span class="sxs-lookup"><span data-stu-id="11e41-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-584">10049 (0x2741)</span><span class="sxs-lookup"><span data-stu-id="11e41-584">10049 (0x2741)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-585">La dirección solicitada no es válida en su contexto.</span><span class="sxs-lookup"><span data-stu-id="11e41-585">The requested address is not valid in its context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="11e41-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-587">10050 (0x2742)</span><span class="sxs-lookup"><span data-stu-id="11e41-587">10050 (0x2742)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-588">Una operación de socket encontró una red inactiva.</span><span class="sxs-lookup"><span data-stu-id="11e41-588">A socket operation encountered a dead network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**</span><span class="sxs-lookup"><span data-stu-id="11e41-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-590">10051 (0x2743)</span><span class="sxs-lookup"><span data-stu-id="11e41-590">10051 (0x2743)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-591">Se intentó realizar una operación de socket en una red inaccesible.</span><span class="sxs-lookup"><span data-stu-id="11e41-591">A socket operation was attempted to an unreachable network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**</span><span class="sxs-lookup"><span data-stu-id="11e41-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-593">10052 (0x2744)</span><span class="sxs-lookup"><span data-stu-id="11e41-593">10052 (0x2744)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-594">La conexión se ha interrumpido debido a que la actividad Keep-Alive detecta un error mientras la operación estaba en curso.</span><span class="sxs-lookup"><span data-stu-id="11e41-594">The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span><span class="sxs-lookup"><span data-stu-id="11e41-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-596">10053 (0x2745)</span><span class="sxs-lookup"><span data-stu-id="11e41-596">10053 (0x2745)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-597">El software del equipo host anuló una conexión establecida.</span><span class="sxs-lookup"><span data-stu-id="11e41-597">An established connection was aborted by the software in your host machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span><span class="sxs-lookup"><span data-stu-id="11e41-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-599">10054 (0x2746)</span><span class="sxs-lookup"><span data-stu-id="11e41-599">10054 (0x2746)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-600">El host remoto forzó el cierre de la conexión existente.</span><span class="sxs-lookup"><span data-stu-id="11e41-600">An existing connection was forcibly closed by the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="11e41-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-602">10055 (0x2747)</span><span class="sxs-lookup"><span data-stu-id="11e41-602">10055 (0x2747)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-603">No se pudo realizar una operación en un socket porque el sistema no tenía suficiente espacio de búfer o porque la cola estaba llena.</span><span class="sxs-lookup"><span data-stu-id="11e41-603">An operation on a socket could not be performed because the system lacked sufficient buffer space or because a queue was full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**</span><span class="sxs-lookup"><span data-stu-id="11e41-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-605">10056 (0x2748)</span><span class="sxs-lookup"><span data-stu-id="11e41-605">10056 (0x2748)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-606">Se realizó una solicitud de conexión en un socket que ya está conectado.</span><span class="sxs-lookup"><span data-stu-id="11e41-606">A connect request was made on an already connected socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="11e41-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-608">10057 (0x2749)</span><span class="sxs-lookup"><span data-stu-id="11e41-608">10057 (0x2749)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-609">No se permitió una solicitud de envío o recepción de datos debido a que el socket no está conectado y no se especificó ninguna dirección al realizar el envío en un socket de datagrama mediante una llamada sendto.</span><span class="sxs-lookup"><span data-stu-id="11e41-609">A request to send or receive data was disallowed because the socket is not connected and (when sending on a datagram socket using a sendto call) no address was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span><span class="sxs-lookup"><span data-stu-id="11e41-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-611">10058 (0x274A)</span><span class="sxs-lookup"><span data-stu-id="11e41-611">10058 (0x274A)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-612">No se ha permitido la solicitud para enviar o recibir datos porque el socket ya se había apagado en esa dirección con una llamada de apagado previa.</span><span class="sxs-lookup"><span data-stu-id="11e41-612">A request to send or receive data was disallowed because the socket had already been shut down in that direction with a previous shutdown call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**</span><span class="sxs-lookup"><span data-stu-id="11e41-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-614">10059 (0x274B)</span><span class="sxs-lookup"><span data-stu-id="11e41-614">10059 (0x274B)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-615">Demasiadas referencias a algún objeto de kernel.</span><span class="sxs-lookup"><span data-stu-id="11e41-615">Too many references to some kernel object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span><span class="sxs-lookup"><span data-stu-id="11e41-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-617">10060 (0x274C)</span><span class="sxs-lookup"><span data-stu-id="11e41-617">10060 (0x274C)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-618">No se pudo realizar un intento de conexión porque la parte conectada no respondió correctamente después de un período de tiempo, o bien se produjo un error en la conexión establecida porque el host conectado no respondió.</span><span class="sxs-lookup"><span data-stu-id="11e41-618">A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**</span><span class="sxs-lookup"><span data-stu-id="11e41-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-620">10061 (0x274D)</span><span class="sxs-lookup"><span data-stu-id="11e41-620">10061 (0x274D)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-621">No se pudo establecer ninguna conexión porque el equipo de destino la rechazó activamente.</span><span class="sxs-lookup"><span data-stu-id="11e41-621">No connection could be made because the target machine actively refused it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**</span><span class="sxs-lookup"><span data-stu-id="11e41-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-623">10062 (0x274E)</span><span class="sxs-lookup"><span data-stu-id="11e41-623">10062 (0x274E)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-624">No se puede convertir el nombre.</span><span class="sxs-lookup"><span data-stu-id="11e41-624">Cannot translate name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**</span><span class="sxs-lookup"><span data-stu-id="11e41-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-626">10063 (0x274F)</span><span class="sxs-lookup"><span data-stu-id="11e41-626">10063 (0x274F)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-627">El nombre o el componente de nombre era demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="11e41-627">Name component or name was too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**</span><span class="sxs-lookup"><span data-stu-id="11e41-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-629">10064 (0x2750)</span><span class="sxs-lookup"><span data-stu-id="11e41-629">10064 (0x2750)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-630">No se pudo realizar una operación de socket porque el host de destino estaba inactivo.</span><span class="sxs-lookup"><span data-stu-id="11e41-630">A socket operation failed because the destination host was down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**</span><span class="sxs-lookup"><span data-stu-id="11e41-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-632">10065 (0x2751)</span><span class="sxs-lookup"><span data-stu-id="11e41-632">10065 (0x2751)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-633">Se intentó realizar una operación de socket a un host inalcanzable.</span><span class="sxs-lookup"><span data-stu-id="11e41-633">A socket operation was attempted to an unreachable host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**</span><span class="sxs-lookup"><span data-stu-id="11e41-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-635">10066 (0x2752)</span><span class="sxs-lookup"><span data-stu-id="11e41-635">10066 (0x2752)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-636">No se puede quitar un directorio que no esté vacío.</span><span class="sxs-lookup"><span data-stu-id="11e41-636">Cannot remove a directory that is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**</span><span class="sxs-lookup"><span data-stu-id="11e41-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-638">10067 (0x2753)</span><span class="sxs-lookup"><span data-stu-id="11e41-638">10067 (0x2753)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-639">Una implementación de Windows Sockets puede tener un límite en cuanto al número de aplicaciones que pueden usarla simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="11e41-639">A Windows Sockets implementation may have a limit on the number of applications that may use it simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**</span><span class="sxs-lookup"><span data-stu-id="11e41-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-641">10068 (0x2754)</span><span class="sxs-lookup"><span data-stu-id="11e41-641">10068 (0x2754)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-642">Se agotó la cuota.</span><span class="sxs-lookup"><span data-stu-id="11e41-642">Ran out of quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**</span><span class="sxs-lookup"><span data-stu-id="11e41-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-644">10069 (0x2755)</span><span class="sxs-lookup"><span data-stu-id="11e41-644">10069 (0x2755)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-645">Se agotó la cuota de disco.</span><span class="sxs-lookup"><span data-stu-id="11e41-645">Ran out of disk quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**</span><span class="sxs-lookup"><span data-stu-id="11e41-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-647">10070 (0x2756)</span><span class="sxs-lookup"><span data-stu-id="11e41-647">10070 (0x2756)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-648">La referencia de identificador de archivo ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="11e41-648">File handle reference is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**</span><span class="sxs-lookup"><span data-stu-id="11e41-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-650">10071 (0x2757)</span><span class="sxs-lookup"><span data-stu-id="11e41-650">10071 (0x2757)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-651">El elemento no está disponible localmente.</span><span class="sxs-lookup"><span data-stu-id="11e41-651">Item is not available locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**</span><span class="sxs-lookup"><span data-stu-id="11e41-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-653">10091 (0x276B)</span><span class="sxs-lookup"><span data-stu-id="11e41-653">10091 (0x276B)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-654">WSAStartup no funciona en este momento porque el sistema subyacente que usa para proporcionar servicios de red no está disponible actualmente.</span><span class="sxs-lookup"><span data-stu-id="11e41-654">WSAStartup cannot function at this time because the underlying system it uses to provide network services is currently unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**</span><span class="sxs-lookup"><span data-stu-id="11e41-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-656">10092 (0x276C)</span><span class="sxs-lookup"><span data-stu-id="11e41-656">10092 (0x276C)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-657">No se admite la versión de Windows Sockets solicitada.</span><span class="sxs-lookup"><span data-stu-id="11e41-657">The Windows Sockets version requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**</span><span class="sxs-lookup"><span data-stu-id="11e41-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-659">10093 (0x276D)</span><span class="sxs-lookup"><span data-stu-id="11e41-659">10093 (0x276D)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-660">Es posible que la aplicación no haya llamado a WSAStartup o que se haya producido un error en WSAStartup.</span><span class="sxs-lookup"><span data-stu-id="11e41-660">Either the application has not called WSAStartup, or WSAStartup failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**</span><span class="sxs-lookup"><span data-stu-id="11e41-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-662">10101 (0x2775)</span><span class="sxs-lookup"><span data-stu-id="11e41-662">10101 (0x2775)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-663">Devuelto por WSARecv o WSARecvFrom para indicar que la parte remota ha iniciado una secuencia de cierre estable.</span><span class="sxs-lookup"><span data-stu-id="11e41-663">Returned by WSARecv or WSARecvFrom to indicate the remote party has initiated a graceful shutdown sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**</span><span class="sxs-lookup"><span data-stu-id="11e41-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-665">10102 (0x2776)</span><span class="sxs-lookup"><span data-stu-id="11e41-665">10102 (0x2776)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-666">WSALookupServiceNext no puede devolver más resultados.</span><span class="sxs-lookup"><span data-stu-id="11e41-666">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**</span><span class="sxs-lookup"><span data-stu-id="11e41-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-668">10103 (0x2777)</span><span class="sxs-lookup"><span data-stu-id="11e41-668">10103 (0x2777)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-669">Se realizó una llamada a WSALookupServiceEnd mientras esta llamada todavía se estaba procesando.</span><span class="sxs-lookup"><span data-stu-id="11e41-669">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="11e41-670">Se canceló la llamada.</span><span class="sxs-lookup"><span data-stu-id="11e41-670">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**</span><span class="sxs-lookup"><span data-stu-id="11e41-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-672">10104 (0x2778)</span><span class="sxs-lookup"><span data-stu-id="11e41-672">10104 (0x2778)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-673">La tabla de llamadas a procedimientos no es válida.</span><span class="sxs-lookup"><span data-stu-id="11e41-673">The procedure call table is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**</span><span class="sxs-lookup"><span data-stu-id="11e41-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-675">10105 (0x2779)</span><span class="sxs-lookup"><span data-stu-id="11e41-675">10105 (0x2779)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-676">El proveedor de servicios solicitado no es válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-676">The requested service provider is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**</span><span class="sxs-lookup"><span data-stu-id="11e41-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-678">10106 (0x277A)</span><span class="sxs-lookup"><span data-stu-id="11e41-678">10106 (0x277A)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-679">No se pudo cargar o inicializar el proveedor de servicios solicitado.</span><span class="sxs-lookup"><span data-stu-id="11e41-679">The requested service provider could not be loaded or initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span><span class="sxs-lookup"><span data-stu-id="11e41-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-681">10107 (0x277B)</span><span class="sxs-lookup"><span data-stu-id="11e41-681">10107 (0x277B)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-682">Error en una llamada del sistema.</span><span class="sxs-lookup"><span data-stu-id="11e41-682">A system call has failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**\_no \_ se encontró WSASERVICE**</span><span class="sxs-lookup"><span data-stu-id="11e41-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-684">10108 (0x277C)</span><span class="sxs-lookup"><span data-stu-id="11e41-684">10108 (0x277C)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-685">No se conoce este servicio.</span><span class="sxs-lookup"><span data-stu-id="11e41-685">No such service is known.</span></span> <span data-ttu-id="11e41-686">No se encuentra el servicio en el espacio de nombres especificado.</span><span class="sxs-lookup"><span data-stu-id="11e41-686">The service cannot be found in the specified name space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**\_no \_ se encontró WSATYPE**</span><span class="sxs-lookup"><span data-stu-id="11e41-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-688">10109 (0x277D)</span><span class="sxs-lookup"><span data-stu-id="11e41-688">10109 (0x277D)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-689">No se encontró la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="11e41-689">The specified class was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ no \_ más**</span><span class="sxs-lookup"><span data-stu-id="11e41-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA\_E\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-691">10110 (0x277E)</span><span class="sxs-lookup"><span data-stu-id="11e41-691">10110 (0x277E)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-692">WSALookupServiceNext no puede devolver más resultados.</span><span class="sxs-lookup"><span data-stu-id="11e41-692">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="11e41-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA\_E\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-694">10111 (0x277F)</span><span class="sxs-lookup"><span data-stu-id="11e41-694">10111 (0x277F)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-695">Se realizó una llamada a WSALookupServiceEnd mientras esta llamada todavía se estaba procesando.</span><span class="sxs-lookup"><span data-stu-id="11e41-695">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="11e41-696">Se canceló la llamada.</span><span class="sxs-lookup"><span data-stu-id="11e41-696">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**</span><span class="sxs-lookup"><span data-stu-id="11e41-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-698">10112 (0x2780)</span><span class="sxs-lookup"><span data-stu-id="11e41-698">10112 (0x2780)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-699">Error en una consulta de base de datos porque se rechazó activamente.</span><span class="sxs-lookup"><span data-stu-id="11e41-699">A database query failed because it was actively refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**\_no \_ se encontró WSAHOST**</span><span class="sxs-lookup"><span data-stu-id="11e41-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-701">11001 (0x2AF9)</span><span class="sxs-lookup"><span data-stu-id="11e41-701">11001 (0x2AF9)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-702">Se desconoce el host.</span><span class="sxs-lookup"><span data-stu-id="11e41-702">No such host is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY de \_ nuevo**</span><span class="sxs-lookup"><span data-stu-id="11e41-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-704">11002 (0x2AFA)</span><span class="sxs-lookup"><span data-stu-id="11e41-704">11002 (0x2AFA)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-705">Éste es normalmente un error temporal durante la resolución de nombres de host y significa que el servidor local no recibió una respuesta de un servidor autorizado.</span><span class="sxs-lookup"><span data-stu-id="11e41-705">This is usually a temporary error during hostname resolution and means that the local server did not receive a response from an authoritative server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**recuperación de WSANO \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**WSANO\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-707">11003 (0x2AFB)</span><span class="sxs-lookup"><span data-stu-id="11e41-707">11003 (0x2AFB)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-708">Se produjo un error no recuperable durante una búsqueda de base de datos.</span><span class="sxs-lookup"><span data-stu-id="11e41-708">A non-recoverable error occurred during a database lookup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**datos de WSANO \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**WSANO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-710">11004 (0x2AFC)</span><span class="sxs-lookup"><span data-stu-id="11e41-710">11004 (0x2AFC)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-711">El nombre solicitado es válido, pero no se encontró ningún dato del tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="11e41-711">The requested name is valid, but no data of the requested type was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**\_receptores de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**WSA\_QOS\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-713">11005 (0x2AFD)</span><span class="sxs-lookup"><span data-stu-id="11e41-713">11005 (0x2AFD)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-714">Ha llegado al menos una reserva.</span><span class="sxs-lookup"><span data-stu-id="11e41-714">At least one reserve has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**\_remitentes de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**WSA\_QOS\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-716">11006 (0x2AFE)</span><span class="sxs-lookup"><span data-stu-id="11e41-716">11006 (0x2AFE)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-717">Ha llegado al menos una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="11e41-717">At least one path has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**\_calidad de QoS WSA \_ sin \_ remitentes**</span><span class="sxs-lookup"><span data-stu-id="11e41-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA\_QOS\_NO\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-719">11007 (0x2AFF)</span><span class="sxs-lookup"><span data-stu-id="11e41-719">11007 (0x2AFF)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-720">No hay remitentes.</span><span class="sxs-lookup"><span data-stu-id="11e41-720">There are no senders.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**\_QoS WSA \_ sin \_ destinatarios**</span><span class="sxs-lookup"><span data-stu-id="11e41-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA\_QOS\_NO\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-722">11008 (0x2B00)</span><span class="sxs-lookup"><span data-stu-id="11e41-722">11008 (0x2B00)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-723">No hay ningún receptor.</span><span class="sxs-lookup"><span data-stu-id="11e41-723">There are no receivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**\_solicitud de QoS WSA \_ \_ confirmada**</span><span class="sxs-lookup"><span data-stu-id="11e41-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**WSA\_QOS\_REQUEST\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-725">11009 (0x2B01)</span><span class="sxs-lookup"><span data-stu-id="11e41-725">11009 (0x2B01)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-726">Se ha confirmado la reserva.</span><span class="sxs-lookup"><span data-stu-id="11e41-726">Reserve has been confirmed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**\_error de \_ admisión de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**WSA\_QOS\_ADMISSION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-728">11010 (0x2B02)</span><span class="sxs-lookup"><span data-stu-id="11e41-728">11010 (0x2B02)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-729">Error debido a la falta de recursos.</span><span class="sxs-lookup"><span data-stu-id="11e41-729">Error due to lack of resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**error de la \_ Directiva de QoS WSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**WSA\_QOS\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-731">11011 (0x2B03)</span><span class="sxs-lookup"><span data-stu-id="11e41-731">11011 (0x2B03)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-732">Rechazado por motivos administrativos: Credenciales incorrectas.</span><span class="sxs-lookup"><span data-stu-id="11e41-732">Rejected for administrative reasons - bad credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**\_ \_ estilo incorrecto de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**WSA\_QOS\_BAD\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-734">11012 (0x2B04)</span><span class="sxs-lookup"><span data-stu-id="11e41-734">11012 (0x2B04)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-735">Estilo desconocido o en conflicto.</span><span class="sxs-lookup"><span data-stu-id="11e41-735">Unknown or conflicting style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**\_ \_ objeto incorrecto de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**WSA\_QOS\_BAD\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-737">11013 (0x2B05)</span><span class="sxs-lookup"><span data-stu-id="11e41-737">11013 (0x2B05)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-738">Problema con alguna parte del búfer de FILTERSPEC o ProviderSpecific en general.</span><span class="sxs-lookup"><span data-stu-id="11e41-738">Problem with some part of the filterspec or providerspecific buffer in general.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**\_error de \_ control de tráfico de QoS WSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**WSA\_QOS\_TRAFFIC\_CTRL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-740">11014 (0x2B06)</span><span class="sxs-lookup"><span data-stu-id="11e41-740">11014 (0x2B06)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-741">Problema con alguna parte del elemento FLOWSPEC.</span><span class="sxs-lookup"><span data-stu-id="11e41-741">Problem with some part of the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**\_ \_ error genérico de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**WSA\_QOS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-743">11015 (0x2B07)</span><span class="sxs-lookup"><span data-stu-id="11e41-743">11015 (0x2B07)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-744">Error general de QOS.</span><span class="sxs-lookup"><span data-stu-id="11e41-744">General QOS error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**\_ESERVICETYPE de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA\_QOS\_ESERVICETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-746">11016 (0x2B08)</span><span class="sxs-lookup"><span data-stu-id="11e41-746">11016 (0x2B08)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-747">Se encontró un tipo de servicio no válido o no reconocido en el FLOWSPEC.</span><span class="sxs-lookup"><span data-stu-id="11e41-747">An invalid or unrecognized service type was found in the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**\_EFLOWSPEC de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA\_QOS\_EFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-749">11017 (0x2B09)</span><span class="sxs-lookup"><span data-stu-id="11e41-749">11017 (0x2B09)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-750">Se encontró un FLOWSPEC no válido o incoherente en la estructura de QOS.</span><span class="sxs-lookup"><span data-stu-id="11e41-750">An invalid or inconsistent flowspec was found in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**\_EPROVSPECBUF de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA\_QOS\_EPROVSPECBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-752">11018 (0x2B0A)</span><span class="sxs-lookup"><span data-stu-id="11e41-752">11018 (0x2B0A)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-753">Búfer específico del proveedor QOS no válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-753">Invalid QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**\_EFILTERSTYLE de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA\_QOS\_EFILTERSTYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-755">11019 (0x2B0B)</span><span class="sxs-lookup"><span data-stu-id="11e41-755">11019 (0x2B0B)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-756">Se usó un estilo de filtro QOS no válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-756">An invalid QOS filter style was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**\_EFILTERTYPE de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA\_QOS\_EFILTERTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-758">11020 (0x2B0C)</span><span class="sxs-lookup"><span data-stu-id="11e41-758">11020 (0x2B0C)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-759">Se usó un tipo de filtro QOS no válido.</span><span class="sxs-lookup"><span data-stu-id="11e41-759">An invalid QOS filter type was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**\_EFILTERCOUNT de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA\_QOS\_EFILTERCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-761">11021 (0x2B0D)</span><span class="sxs-lookup"><span data-stu-id="11e41-761">11021 (0x2B0D)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-762">Se especificó un número incorrecto de FILTERSPECs de QOS en FLOWDESCRIPTOR.</span><span class="sxs-lookup"><span data-stu-id="11e41-762">An incorrect number of QOS FILTERSPECs were specified in the FLOWDESCRIPTOR.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**\_EOBJLENGTH de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA\_QOS\_EOBJLENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-764">11022 (0x2B0E)</span><span class="sxs-lookup"><span data-stu-id="11e41-764">11022 (0x2B0E)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-765">Se especificó un objeto con un campo ObjectLength no válido en el búfer específico del proveedor QOS.</span><span class="sxs-lookup"><span data-stu-id="11e41-765">An object with an invalid ObjectLength field was specified in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**\_EFLOWCOUNT de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA\_QOS\_EFLOWCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-767">11023 (0x2B0F)</span><span class="sxs-lookup"><span data-stu-id="11e41-767">11023 (0x2B0F)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-768">Se especificó un número incorrecto de descriptores de flujo en la estructura de QOS.</span><span class="sxs-lookup"><span data-stu-id="11e41-768">An incorrect number of flow descriptors was specified in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**\_EUNKOWNPSOBJ de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA\_QOS\_EUNKOWNPSOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-770">11024 (0x2B10)</span><span class="sxs-lookup"><span data-stu-id="11e41-770">11024 (0x2B10)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-771">Se encontró un objeto desconocido en el búfer específico del proveedor QOS.</span><span class="sxs-lookup"><span data-stu-id="11e41-771">An unrecognized object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**\_EPOLICYOBJ de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA\_QOS\_EPOLICYOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-773">11025 (0x2B11)</span><span class="sxs-lookup"><span data-stu-id="11e41-773">11025 (0x2B11)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-774">Se encontró un objeto de Directiva no válido en el búfer específico del proveedor QOS.</span><span class="sxs-lookup"><span data-stu-id="11e41-774">An invalid policy object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**\_EFLOWDESC de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA\_QOS\_EFLOWDESC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-776">11026 (0x2B12)</span><span class="sxs-lookup"><span data-stu-id="11e41-776">11026 (0x2B12)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-777">Se encontró un descriptor de flujo de QOS no válido en la lista de descriptores de flujo.</span><span class="sxs-lookup"><span data-stu-id="11e41-777">An invalid QOS flow descriptor was found in the flow descriptor list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**\_EPSFLOWSPEC de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA\_QOS\_EPSFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-779">11027 (0x2B13)</span><span class="sxs-lookup"><span data-stu-id="11e41-779">11027 (0x2B13)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-780">Se encontró un FLOWSPEC no válido o incoherente en el búfer específico del proveedor QOS.</span><span class="sxs-lookup"><span data-stu-id="11e41-780">An invalid or inconsistent flowspec was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**\_EPSFILTERSPEC de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA\_QOS\_EPSFILTERSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-782">11028 (0x2B14)</span><span class="sxs-lookup"><span data-stu-id="11e41-782">11028 (0x2B14)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-783">Se encontró un FILTERSPEC no válido en el búfer específico del proveedor QOS.</span><span class="sxs-lookup"><span data-stu-id="11e41-783">An invalid FILTERSPEC was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**\_ESDMODEOBJ de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA\_QOS\_ESDMODEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-785">11029 (0x2B15)</span><span class="sxs-lookup"><span data-stu-id="11e41-785">11029 (0x2B15)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-786">Se encontró un objeto de modo discard de forma no válido en el búfer específico del proveedor QOS.</span><span class="sxs-lookup"><span data-stu-id="11e41-786">An invalid shape discard mode object was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**\_ESHAPERATEOBJ de QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA\_QOS\_ESHAPERATEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-788">11030 (0x2B16)</span><span class="sxs-lookup"><span data-stu-id="11e41-788">11030 (0x2B16)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-789">Se encontró un objeto de frecuencia de forma no válido en el búfer específico del proveedor QOS.</span><span class="sxs-lookup"><span data-stu-id="11e41-789">An invalid shaping rate object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**\_ \_ clave reservada de QoS WSA \_ PETYPE**</span><span class="sxs-lookup"><span data-stu-id="11e41-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**WSA\_QOS\_RESERVED\_PETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-791">11031 (0x2B17)</span><span class="sxs-lookup"><span data-stu-id="11e41-791">11031 (0x2B17)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-792">Se encontró un elemento de directiva reservado en el búfer específico del proveedor QOS.</span><span class="sxs-lookup"><span data-stu-id="11e41-792">A reserved policy element was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**\_ \_ \_ no \_ se encontró el host seguro WSA**</span><span class="sxs-lookup"><span data-stu-id="11e41-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**WSA\_SECURE\_HOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-794">11032 (0x2B18)</span><span class="sxs-lookup"><span data-stu-id="11e41-794">11032 (0x2B18)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-795">No se conoce este host de forma segura.</span><span class="sxs-lookup"><span data-stu-id="11e41-795">No such host is known securely.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11e41-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**\_error de \_ Directiva de nombre de IPSec WSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11e41-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**WSA\_IPSEC\_NAME\_POLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e41-797">11033 (0x2B19)</span><span class="sxs-lookup"><span data-stu-id="11e41-797">11033 (0x2B19)</span></span>
</dt> <dt>



<span data-ttu-id="11e41-798">No se pudo agregar la directiva IPSEC basada en nombres.</span><span class="sxs-lookup"><span data-stu-id="11e41-798">Name based IPSEC policy could not be added.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="11e41-799">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11e41-799">Requirements</span></span>



| <span data-ttu-id="11e41-800">Requisito</span><span class="sxs-lookup"><span data-stu-id="11e41-800">Requirement</span></span> | <span data-ttu-id="11e41-801">Value</span><span class="sxs-lookup"><span data-stu-id="11e41-801">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11e41-802">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11e41-802">Minimum supported client</span></span><br/> | <span data-ttu-id="11e41-803">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="11e41-803">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="11e41-804">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11e41-804">Minimum supported server</span></span><br/> | <span data-ttu-id="11e41-805">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="11e41-805">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11e41-806">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11e41-806">Header</span></span><br/>                   | <dl> <span data-ttu-id="11e41-807"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="11e41-807"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11e41-808">Vea también</span><span class="sxs-lookup"><span data-stu-id="11e41-808">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e41-809">Códigos de error del sistema</span><span class="sxs-lookup"><span data-stu-id="11e41-809">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




