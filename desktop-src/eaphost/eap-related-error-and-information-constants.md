---
title: Constantes de información y errores relacionados con EAP (Eaphosterror. h)
description: Grupos individuales de constantes de información y errores relacionados con EAP comunes a todas las tecnologías de API de EAPHost.
ms.assetid: 081b7a72-abe3-4cbb-9b6c-07bb6717fbfe
topic_type:
- apiref
api_name:
- EAP_E_EAPHOST_FIRST
- EAP_E_EAPHOST_LAST
- EAP_I_EAPHOST_FIRST
- EAP_I_EAPHOST_LAST
- EAP_E_CERT_STORE_INACCESSIBLE
- EAP_E_EAPHOST_METHOD_NOT_INSTALLED
- EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET
- EAP_E_EAPHOST_EAPQEC_INACCESSIBLE
- EAP_E_EAPHOST_IDENTITY_UNKNOWN
- EAP_E_AUTHENTICATION_FAILED
- EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED
- EAP_E_EAPHOST_METHOD_INVALID_PACKET
- EAP_E_EAPHOST_REMOTE_INVALID_PACKET
- EAP_E_EAPHOST_XML_MALFORMED
- EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO
- EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED
- EAP_E_USER_FIRST
- EAP_E_USER_LAST
- EAP_I_USER_FIRST
- EAP_I_USER_LAST
- EAP_E_USER_CERT_NOT_FOUND
- EAP_E_USER_CERT_INVALID
- EAP_E_USER_CERT_EXPIRED
- EAP_E_USER_CERT_REVOKED
- EAP_E_USER_CERT_OTHER_ERROR
- EAP_E_USER_CERT_REJECTED
- EAP_I_USER_ACCOUNT_OTHER_ERROR
- EAP_E_USER_CREDENTIALS_REJECTED
- EAP_E_USER_NAME_PASSWORD_REJECTED
- EAP_E_NO_SMART_CARD_READER
- EAP_E_SERVER_FIRST
- EAP_E_SERVER_LAST
- EAP_E_SERVER_CERT_NOT_FOUND
- EAP_E_SERVER_CERT_INVALID
- EAP_E_SERVER_CERT_EXPIRED
- EAP_E_SERVER_CERT_REVOKED
- EAP_E_SERVER_CERT_OTHER_ERROR
- EAP_E_USER_ROOT_CERT_FIRST
- EAP_E_USER_ROOT_CERT_LAST
- EAP_E_USER_ROOT_CERT_NOT_FOUND
- EAP_E_USER_ROOT_CERT_INVALID
- EAP_E_USER_ROOT_CERT_EXPIRED
- EAP_E_SERVER_ROOT_CERT_FIRST
- EAP_E_SERVER_ROOT_CERT_LAST
- EAP_E_SERVER_ROOT_CERT_NOT_FOUND
- EAP_E_SERVER_ROOT_CERT_INVALID
- EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd7b829cd4c5ba550fd88242ffb8c34572648d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079462"
---
# <a name="eap-related-error-and-information-constants"></a><span data-ttu-id="e6591-103">Constantes de información y errores relacionados con EAP</span><span class="sxs-lookup"><span data-stu-id="e6591-103">EAP Related Error and Information Constants</span></span>

<span data-ttu-id="e6591-104">Grupos individuales de constantes de información y errores relacionados con EAP comunes a todas las tecnologías de API de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="e6591-104">Individual groups of EAP related error and information constants common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="e6591-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHOST \_ primero**</span><span class="sxs-lookup"><span data-stu-id="e6591-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP\_E\_EAPHOST\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-106">0x80420000L</span><span class="sxs-lookup"><span data-stu-id="e6591-106">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="e6591-107">Define el límite de los informes de errores; cualquier error relacionado con EAPHost se producirá **\_ \_ \_ primero entre EAP e** EAPHost y **EAP \_ e \_ EAPHost en \_ último** lugar.</span><span class="sxs-lookup"><span data-stu-id="e6591-107">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHOST en \_ último lugar**</span><span class="sxs-lookup"><span data-stu-id="e6591-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP\_E\_EAPHOST\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-109">0x804200FFL</span><span class="sxs-lookup"><span data-stu-id="e6591-109">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="e6591-110">Define el límite de los informes de errores; cualquier error relacionado con EAPHost se producirá **\_ \_ \_ primero entre EAP e** EAPHost y **EAP \_ e \_ EAPHost en \_ último** lugar.</span><span class="sxs-lookup"><span data-stu-id="e6591-110">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**\_primero EAP I \_ EAPHOST \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP\_I\_EAPHOST\_FIRST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-112">0x80420000L</span><span class="sxs-lookup"><span data-stu-id="e6591-112">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="e6591-113">Define el límite de los informes de información; cualquier registro de eventos informativo relacionado con EAPHost se producirá primero entre el **EAP \_ i \_ EAPHost \_** y el **EAP \_ i EAPHost en \_ \_ último** lugar.</span><span class="sxs-lookup"><span data-stu-id="e6591-113">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ en \_ último lugar**</span><span class="sxs-lookup"><span data-stu-id="e6591-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP\_I\_EAPHOST\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-115">0x804200FFL</span><span class="sxs-lookup"><span data-stu-id="e6591-115">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="e6591-116">Define el límite de los informes de información; cualquier registro de eventos informativo relacionado con EAPHost se producirá primero entre el **EAP \_ i \_ EAPHost \_** y el **EAP \_ i EAPHost en \_ \_ último** lugar.</span><span class="sxs-lookup"><span data-stu-id="e6591-116">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**no \_ se \_ \_ \_ puede obtener acceso al almacén de certificados EAP E**</span><span class="sxs-lookup"><span data-stu-id="e6591-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**EAP\_E\_CERT\_STORE\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-118">0x80420011</span><span class="sxs-lookup"><span data-stu-id="e6591-118">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="e6591-119">Ni el autenticador ni el mismo nivel pueden tener acceso al almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="e6591-119">Neither the authenticator or peer can access the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**\_ \_ \_ \_ no está instalado el método \_ EAPHOST de EAP E**</span><span class="sxs-lookup"><span data-stu-id="e6591-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**EAP\_E\_EAPHOST\_METHOD\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-121">0x80420011</span><span class="sxs-lookup"><span data-stu-id="e6591-121">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="e6591-122">El método EAP solicitado no está instalado.</span><span class="sxs-lookup"><span data-stu-id="e6591-122">The requested EAP method is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**\_ \_ \_ método THIRDPARTY de \_ \_ host \_ de EAPHost de EAP E**</span><span class="sxs-lookup"><span data-stu-id="e6591-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP\_E\_EAPHOST\_THIRDPARTY\_METHOD\_HOST\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-124">0x80420012</span><span class="sxs-lookup"><span data-stu-id="e6591-124">0x80420012</span></span>
</dt> <dt>



<span data-ttu-id="e6591-125">El host del método de terceros no responde y se reinició automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e6591-125">The host of the third party method is not responding and was restarted automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAPQEC de EAPHost de EAP \_ E \_ \_ \_ inaccesible**</span><span class="sxs-lookup"><span data-stu-id="e6591-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP\_E\_EAPHOST\_EAPQEC\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-127">0x80420013</span><span class="sxs-lookup"><span data-stu-id="e6591-127">0x80420013</span></span>
</dt> <dt>



<span data-ttu-id="e6591-128">EAPHost no puede comunicarse con el [cliente de cumplimiento de cuarentena](/windows/desktop/NAP/nap-client-architecture) de EAP (qec) en un cliente habilitado para protección de [acceso a redes](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span><span class="sxs-lookup"><span data-stu-id="e6591-128">EAPHost not able to communicate with EAP [quarantine enforcement client](/windows/desktop/NAP/nap-client-architecture) (QEC) on a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) enabled client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**\_identidad EAP \_ E \_ EAPHOST \_ desconocida**</span><span class="sxs-lookup"><span data-stu-id="e6591-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**EAP\_E\_EAPHOST\_IDENTITY\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-130">0x80420014</span><span class="sxs-lookup"><span data-stu-id="e6591-130">0x80420014</span></span>
</dt> <dt>



<span data-ttu-id="e6591-131">EAPHost devuelve este error si el autenticador no supera la autenticación después de enviar la identidad del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="e6591-131">EAPHost returns this error if the authenticator fails the authentication after the peer identity was submitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**error de autenticación de EAP \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**EAP\_E\_AUTHENTICATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-133">0x80420015</span><span class="sxs-lookup"><span data-stu-id="e6591-133">0x80420015</span></span> 
</dt> <dt>



<span data-ttu-id="e6591-134">EAPHost devuelve este error en caso de error de autenticación.</span><span class="sxs-lookup"><span data-stu-id="e6591-134">EAPHost returns this error on authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**\_ \_ \_ \_ \_ no se pudo negociar EAP de EAPHost de EAP**</span><span class="sxs-lookup"><span data-stu-id="e6591-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**EAP\_I\_EAPHOST\_EAP\_NEGOTIATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-136">0x40420016</span><span class="sxs-lookup"><span data-stu-id="e6591-136">0x40420016</span></span>
</dt> <dt>



<span data-ttu-id="e6591-137">EAPHost registra este evento de información cuando el cliente y el servidor no están configurados con tipos de EAP compatibles.</span><span class="sxs-lookup"><span data-stu-id="e6591-137">EAPHost logs this information event when the client and server aren't configured with compatible EAP types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**\_ \_ \_ \_ paquete no válido del método EAPHOST de EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-139">0x80420017</span><span class="sxs-lookup"><span data-stu-id="e6591-139">0x80420017</span></span>
</dt> <dt>



<span data-ttu-id="e6591-140">Un método EAP recibió un paquete EAP que no se puede procesar.</span><span class="sxs-lookup"><span data-stu-id="e6591-140">An EAP method received an EAP packet that cannot be processed.</span></span> <span data-ttu-id="e6591-141">Otro nombre para **el \_ \_ \_ \_ \_ paquete no válido del método EAPHost de EAP E** es un **\_ \_ \_ paquete no válido del método EAP**.</span><span class="sxs-lookup"><span data-stu-id="e6591-141">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**\_paquete remoto de EAPHost de EAP E \_ \_ \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-143">0x80420018</span><span class="sxs-lookup"><span data-stu-id="e6591-143">0x80420018</span></span>
</dt> <dt>



<span data-ttu-id="e6591-144">EAPHost recibió un paquete que no se puede procesar.</span><span class="sxs-lookup"><span data-stu-id="e6591-144">EAPHost received a packet that cannot be processed.</span></span> <span data-ttu-id="e6591-145">Otro nombre para **el \_ \_ \_ \_ \_ paquete remoto no válido de EAPHost de EAP E** es un **\_ \_ paquete no válido de EAP**.</span><span class="sxs-lookup"><span data-stu-id="e6591-145">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**XML de EAPHost de EAP \_ E \_ \_ \_ incorrecto**</span><span class="sxs-lookup"><span data-stu-id="e6591-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP\_E\_EAPHOST\_XML\_MALFORMED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-147">0x80420019</span><span class="sxs-lookup"><span data-stu-id="e6591-147">0x80420019</span></span>
</dt> <dt>



<span data-ttu-id="e6591-148">Error en la validación del esquema de configuración de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="e6591-148">The EAPHost configuration schema validation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**la \_ configuración del método EAP E no es \_ \_ \_ \_ \_ compatible con \_ SSO**</span><span class="sxs-lookup"><span data-stu-id="e6591-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**EAP\_E\_METHOD\_CONFIG\_DOES\_NOT\_SUPPORT\_SSO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-150">0x8042001A</span><span class="sxs-lookup"><span data-stu-id="e6591-150">0x8042001A</span></span>
</dt> <dt>



<span data-ttu-id="e6591-151">Windows 7 o posterior: el método EAP no admite el inicio de sesión único (SSO) para la configuración proporcionada.</span><span class="sxs-lookup"><span data-stu-id="e6591-151">Windows 7 or later: The EAP method does not support single sign on (SSO) for the provided configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_no se \_ \_ \_ \_ admite la operación de método EAPHOST de EAP \_ E**</span><span class="sxs-lookup"><span data-stu-id="e6591-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**EAP\_E\_EAPHOST\_METHOD\_OPERATION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-153">0x80420020</span><span class="sxs-lookup"><span data-stu-id="e6591-153">0x80420020</span></span>
</dt> <dt>



<span data-ttu-id="e6591-154">EAPHost devuelve este error cuando un método EAP configurado no admite una operación solicitada (llamada a procedimiento).</span><span class="sxs-lookup"><span data-stu-id="e6591-154">EAPHost returns this error when a configured EAP method does not support a requested operation (procedure call).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**\_ \_ primer usuario de EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP\_E\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-156">0x80420100L</span><span class="sxs-lookup"><span data-stu-id="e6591-156">0x80420100L</span></span>
</dt> <dt>



<span data-ttu-id="e6591-157">Define el límite de los informes de errores; cualquier error relacionado con el usuario se producirá primero entre los usuarios de **EAP \_ e \_ \_** **EAP \_ \_ \_** e.</span><span class="sxs-lookup"><span data-stu-id="e6591-157">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**\_ \_ último usuario de EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP\_E\_USER\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-159">0x804201FFL</span><span class="sxs-lookup"><span data-stu-id="e6591-159">0x804201FFL</span></span>
</dt> <dt>



<span data-ttu-id="e6591-160">Define el límite de los informes de errores; cualquier error relacionado con el usuario se producirá primero entre los usuarios de **EAP \_ e \_ \_** **EAP \_ \_ \_** e.</span><span class="sxs-lookup"><span data-stu-id="e6591-160">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP \_ I \_ \_ primero**</span><span class="sxs-lookup"><span data-stu-id="e6591-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP\_I\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-162">0x40420100L</span><span class="sxs-lookup"><span data-stu-id="e6591-162">0x40420100L</span></span>
</dt> <dt>



<span data-ttu-id="e6591-163">Define el límite de los informes de información; cualquier registro de eventos informativos relacionado con EAP se producirá entre el usuario de **EAP \_ i \_ \_ primero** y el **usuario de EAP \_ i en \_ \_ último** lugar.</span><span class="sxs-lookup"><span data-stu-id="e6591-163">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**\_ \_ último usuario de \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="e6591-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP\_I\_USER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-165">0x404201FFL</span><span class="sxs-lookup"><span data-stu-id="e6591-165">0x404201FFL</span></span>
</dt> <dt>



<span data-ttu-id="e6591-166">Define el límite de los informes de información; cualquier registro de eventos informativos relacionado con EAP se producirá entre el usuario de **EAP \_ i \_ \_ primero** y el **usuario de EAP \_ i en \_ \_ último** lugar.</span><span class="sxs-lookup"><span data-stu-id="e6591-166">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**certificado de usuario de EAP \_ E \_ \_ \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="e6591-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**EAP\_E\_USER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-168">0x80420100</span><span class="sxs-lookup"><span data-stu-id="e6591-168">0x80420100</span></span>
</dt> <dt>



<span data-ttu-id="e6591-169">EAPHost no encontró un certificado de usuario para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="e6591-169">EAPHost could not find a user certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**certificado de usuario de EAP \_ E \_ \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="e6591-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP\_E\_USER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-171">0x80420101</span><span class="sxs-lookup"><span data-stu-id="e6591-171">0x80420101</span></span>
</dt> <dt>



<span data-ttu-id="e6591-172">El certificado de usuario para la autenticación no tiene un conjunto de uso mejorado de clave (EKU) adecuado.</span><span class="sxs-lookup"><span data-stu-id="e6591-172">The user certificate being user for authentication does not have proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**certificado de usuario de EAP \_ E \_ \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="e6591-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP\_E\_USER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-174">0x80420102</span><span class="sxs-lookup"><span data-stu-id="e6591-174">0x80420102</span></span>
</dt> <dt>



<span data-ttu-id="e6591-175">EAPhost encontró un certificado de usuario expirado.</span><span class="sxs-lookup"><span data-stu-id="e6591-175">EAPhost found an expired user certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**certificado de usuario de EAP \_ E \_ \_ \_ revocado**</span><span class="sxs-lookup"><span data-stu-id="e6591-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**EAP\_E\_USER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-177">0x80420103</span><span class="sxs-lookup"><span data-stu-id="e6591-177">0x80420103</span></span>
</dt> <dt>



<span data-ttu-id="e6591-178">Se ha revocado el certificado de usuario que se usa para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="e6591-178">The user certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**\_error de \_ \_ otro certificado \_ de \_ usuario de EAP E**</span><span class="sxs-lookup"><span data-stu-id="e6591-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**EAP\_E\_USER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-180">0x80420104</span><span class="sxs-lookup"><span data-stu-id="e6591-180">0x80420104</span></span>
</dt> <dt>



<span data-ttu-id="e6591-181">Se produjo un error desconocido con la certificación de usuario usada para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="e6591-181">An unknown error occurred with the user certification being used for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**certificado de usuario de EAP \_ E \_ \_ \_ rechazado**</span><span class="sxs-lookup"><span data-stu-id="e6591-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**EAP\_E\_USER\_CERT\_REJECTED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-183">0x80420105</span><span class="sxs-lookup"><span data-stu-id="e6591-183">0x80420105</span></span>
</dt> <dt>



<span data-ttu-id="e6591-184">El autenticador rechazó la certificación del usuario.</span><span class="sxs-lookup"><span data-stu-id="e6591-184">The authenticator rejected the user certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**ERROR en la cuenta de usuario de EAP \_ I \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**EAP\_I\_USER\_ACCOUNT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-186">0x40420110</span><span class="sxs-lookup"><span data-stu-id="e6591-186">0x40420110</span></span>
</dt> <dt>



<span data-ttu-id="e6591-187">Se recibió un error de EAP después de un intercambio de identidades que indica la probabilidad de que se produzca un problema con la cuenta del usuario que realiza la autenticación.</span><span class="sxs-lookup"><span data-stu-id="e6591-187">An EAP failure was received after an identity exchange, indicating the likelihood of a problem with the authenticating user's account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**\_credenciales de usuario de EAP E \_ \_ \_ rechazadas**</span><span class="sxs-lookup"><span data-stu-id="e6591-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**EAP\_E\_USER\_CREDENTIALS\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-189">0x80420111</span><span class="sxs-lookup"><span data-stu-id="e6591-189">0x80420111</span></span>
</dt> <dt>



<span data-ttu-id="e6591-190">El autenticador rechazó las credenciales de usuario para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="e6591-190">The authenticator rejected user credentials for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**contraseña del nombre de usuario de EAP \_ E \_ \_ \_ \_ rechazada**</span><span class="sxs-lookup"><span data-stu-id="e6591-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**EAP\_E\_USER\_NAME\_PASSWORD\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-192">0x80420112</span><span class="sxs-lookup"><span data-stu-id="e6591-192">0x80420112</span></span>
</dt> <dt>



<span data-ttu-id="e6591-193">Windows 7 o posterior: error de autenticación.</span><span class="sxs-lookup"><span data-stu-id="e6591-193">Windows 7 or later: Authentication failed.</span></span> <span data-ttu-id="e6591-194">El autenticador rechazó las credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="e6591-194">The authenticator rejected the user credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ no \_ \_ lector de tarjeta inteligente \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP\_E\_NO\_SMART\_CARD\_READER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-196">0x80420113</span><span class="sxs-lookup"><span data-stu-id="e6591-196">0x80420113</span></span>
</dt> <dt>



<span data-ttu-id="e6591-197">Windows 7 o posterior: no se encontró ningún lector de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="e6591-197">Windows 7 or later: No smart card reader found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP \_ E \_ servidor \_ primero**</span><span class="sxs-lookup"><span data-stu-id="e6591-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP\_E\_SERVER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-199">0x80420200L</span><span class="sxs-lookup"><span data-stu-id="e6591-199">0x80420200L</span></span>
</dt> <dt>



<span data-ttu-id="e6591-200">Define el límite de los informes de errores; cualquier error relacionado con el servidor se producirá primero entre el **\_ \_ servidor \_ EAP e** y el **\_ servidor EAP e \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="e6591-200">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**\_ \_ último servidor EAP \_ E**</span><span class="sxs-lookup"><span data-stu-id="e6591-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP\_E\_SERVER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-202">0x804202FFL</span><span class="sxs-lookup"><span data-stu-id="e6591-202">0x804202FFL</span></span>
</dt> <dt>



<span data-ttu-id="e6591-203">Define el límite de los informes de errores; cualquier error relacionado con el servidor se producirá primero entre el **\_ \_ servidor \_ EAP e** y el **\_ servidor EAP e \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="e6591-203">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**\_ \_ \_ \_ no se encontró el certificado \_ del servidor EAP E**</span><span class="sxs-lookup"><span data-stu-id="e6591-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**EAP\_E\_SERVER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-205">0x80420200</span><span class="sxs-lookup"><span data-stu-id="e6591-205">0x80420200</span></span>
</dt> <dt>



<span data-ttu-id="e6591-206">EAPHost no encontró el certificado de servidor para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="e6591-206">EAPHost could not find the server certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**\_certificado de servidor EAP E \_ \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="e6591-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP\_E\_SERVER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-208">0x80420201</span><span class="sxs-lookup"><span data-stu-id="e6591-208">0x80420201</span></span>
</dt> <dt>



<span data-ttu-id="e6591-209">El certificado de servidor que se va a usar para la autenticación no tiene un conjunto de uso mejorado de clave (EKU) adecuado.</span><span class="sxs-lookup"><span data-stu-id="e6591-209">The server certificate being user for authentication does not have a proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**el \_ certificado del servidor EAP E ha \_ \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="e6591-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EAP\_E\_SERVER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-211">0x80420202</span><span class="sxs-lookup"><span data-stu-id="e6591-211">0x80420202</span></span>
</dt> <dt>



<span data-ttu-id="e6591-212">EAPhost encontró un certificado de servidor expirado.</span><span class="sxs-lookup"><span data-stu-id="e6591-212">EAPhost found an expired server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**se \_ ha \_ \_ revocado el certificado de servidor EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP\_E\_SERVER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-214">0x80420203</span><span class="sxs-lookup"><span data-stu-id="e6591-214">0x80420203</span></span>
</dt> <dt>



<span data-ttu-id="e6591-215">Se ha revocado el certificado de servidor que se usa para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="e6591-215">The server certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**\_error de \_ \_ otro certificado \_ de servidor EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**EAP\_E\_SERVER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-217">0x80420204</span><span class="sxs-lookup"><span data-stu-id="e6591-217">0x80420204</span></span>
</dt> <dt>



<span data-ttu-id="e6591-218">Se produjo un error desconocido con el certificado de servidor.</span><span class="sxs-lookup"><span data-stu-id="e6591-218">An unknown error occurred with the server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**\_ \_ \_ \_ primero certificado raíz de usuario de EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP\_E\_USER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-220">0x80420300L</span><span class="sxs-lookup"><span data-stu-id="e6591-220">0x80420300L</span></span>
</dt> <dt>



<span data-ttu-id="e6591-221">Define el límite de los informes de errores; cualquier error relacionado con el certificado raíz de usuario se producirá **\_ \_ \_ \_ \_ primero** entre el certificado **raíz de usuario de EAP \_ \_ \_ \_ \_ e** y el certificado raíz de usuario de EAP e.</span><span class="sxs-lookup"><span data-stu-id="e6591-221">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**\_ \_ \_ \_ último certificado raíz de usuario de EAP \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP\_E\_USER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-223">0x804203FFL</span><span class="sxs-lookup"><span data-stu-id="e6591-223">0x804203FFL</span></span>
</dt> <dt>



<span data-ttu-id="e6591-224">Define el límite de los informes de errores; cualquier error relacionado con el certificado raíz de usuario se producirá **\_ \_ \_ \_ \_ primero** entre el certificado **raíz de usuario de EAP \_ \_ \_ \_ \_ e** y el certificado raíz de usuario de EAP e.</span><span class="sxs-lookup"><span data-stu-id="e6591-224">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**\_ \_ \_ \_ \_ no \_ se encontró el certificado raíz de usuario de EAP.**</span><span class="sxs-lookup"><span data-stu-id="e6591-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**EAP\_E\_USER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-226">0x80420300</span><span class="sxs-lookup"><span data-stu-id="e6591-226">0x80420300</span></span>
</dt> <dt>



<span data-ttu-id="e6591-227">EAPHost no encontró un certificado en un almacén de certificados raíz de confianza para la validación de la certificación de usuario.</span><span class="sxs-lookup"><span data-stu-id="e6591-227">EAPHost could not find a certificate in a trusted root certificate store for user certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**\_certificado raíz de usuario de EAP E \_ \_ \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="e6591-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP\_E\_USER\_ROOT\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-229">0x80420301</span><span class="sxs-lookup"><span data-stu-id="e6591-229">0x80420301</span></span>
</dt> <dt>



<span data-ttu-id="e6591-230">Error de autenticación porque el certificado raíz utilizado para esta red no es válido.</span><span class="sxs-lookup"><span data-stu-id="e6591-230">The authentication failed because the root certificate used for this network is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**\_certificado raíz de usuario de EAP E \_ \_ \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="e6591-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP\_E\_USER\_ROOT\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-232">0x80420302</span><span class="sxs-lookup"><span data-stu-id="e6591-232">0x80420302</span></span>
</dt> <dt>



<span data-ttu-id="e6591-233">El certificado raíz de confianza necesario para la validación de certificado de usuario ha expirado.</span><span class="sxs-lookup"><span data-stu-id="e6591-233">The trusted root certificate needed for user certificate validation has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**\_ \_ certificado raíz de servidor EAP E \_ \_ \_ primero**</span><span class="sxs-lookup"><span data-stu-id="e6591-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-235">0x80420400L</span><span class="sxs-lookup"><span data-stu-id="e6591-235">0x80420400L</span></span>
</dt> <dt>



<span data-ttu-id="e6591-236">Define el límite de los informes de errores; cualquier error relacionado con el certificado raíz del servidor se producirá primero entre el certificado **\_ raíz del servidor EAP e \_ \_ \_ \_** y el certificado **\_ raíz del servidor EAP e \_ \_ \_ \_ EAP**.</span><span class="sxs-lookup"><span data-stu-id="e6591-236">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**\_ \_ \_ \_ último certificado raíz de servidor EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="e6591-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-238">0x804204FFL</span><span class="sxs-lookup"><span data-stu-id="e6591-238">0x804204FFL</span></span>
</dt> <dt>



<span data-ttu-id="e6591-239">Define el límite de los informes de errores; cualquier error relacionado con el certificado raíz del servidor se producirá primero entre el certificado **\_ raíz del servidor EAP e \_ \_ \_ \_** y el certificado **\_ raíz del servidor EAP e \_ \_ \_ \_ EAP**.</span><span class="sxs-lookup"><span data-stu-id="e6591-239">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**\_ \_ \_ \_ \_ no \_ se encontró el certificado raíz del servidor EAP E**</span><span class="sxs-lookup"><span data-stu-id="e6591-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-241">0x80420400</span><span class="sxs-lookup"><span data-stu-id="e6591-241">0x80420400</span></span>
</dt> <dt>



<span data-ttu-id="e6591-242">EAPHost no encontró un certificado raíz en un almacén de certificados raíz de confianza para la validación de la certificación del servidor.</span><span class="sxs-lookup"><span data-stu-id="e6591-242">EAPHost could not find a root certificate in a trusted root certificate store for the server certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**\_ \_ certificado raíz del servidor EAP E \_ \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="e6591-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_INVALID**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-244">0x80420401</span><span class="sxs-lookup"><span data-stu-id="e6591-244">0x80420401</span></span>
</dt> <dt>



<span data-ttu-id="e6591-245">No se pudo realizar la autenticación porque el certificado de servidor necesario para esta red en el equipo servidor no es válido.</span><span class="sxs-lookup"><span data-stu-id="e6591-245">The authentication failed because the server certificate required for this network on the server computer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e6591-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**\_nombre de \_ certificado raíz del servidor EAP E \_ \_ \_ \_ necesario**</span><span class="sxs-lookup"><span data-stu-id="e6591-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6591-247">0x80420406</span><span class="sxs-lookup"><span data-stu-id="e6591-247">0x80420406</span></span>
</dt> <dt>



<span data-ttu-id="e6591-248">No se pudo realizar la autenticación porque el certificado del equipo servidor no tiene especificado un nombre de servidor.</span><span class="sxs-lookup"><span data-stu-id="e6591-248">The authentication failed because the certificate on the server computer does not have a server name specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6591-249">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6591-249">Remarks</span></span>

<span data-ttu-id="e6591-250">Hay nombres alternativos para determinados errores:</span><span class="sxs-lookup"><span data-stu-id="e6591-250">There are alternate names for certain errors:</span></span>

-   <span data-ttu-id="e6591-251">Otro nombre para **el \_ \_ \_ \_ \_ paquete no válido del método EAPHost de EAP E** es un **\_ \_ \_ paquete no válido del método EAP**.</span><span class="sxs-lookup"><span data-stu-id="e6591-251">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>
-   <span data-ttu-id="e6591-252">Otro nombre para **el \_ \_ \_ \_ \_ paquete remoto no válido de EAPHost de EAP E** es un **\_ \_ paquete no válido de EAP**.</span><span class="sxs-lookup"><span data-stu-id="e6591-252">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6591-253">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6591-253">Requirements</span></span>



| <span data-ttu-id="e6591-254">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6591-254">Requirement</span></span> | <span data-ttu-id="e6591-255">Value</span><span class="sxs-lookup"><span data-stu-id="e6591-255">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6591-256">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6591-256">Minimum supported client</span></span><br/> | <span data-ttu-id="e6591-257">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e6591-257">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e6591-258">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6591-258">Minimum supported server</span></span><br/> | <span data-ttu-id="e6591-259">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6591-259">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e6591-260">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6591-260">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6591-261"><dt>Eaphosterror. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6591-261"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6591-262">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6591-262">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6591-263">Constantes de EAPHost comunes</span><span class="sxs-lookup"><span data-stu-id="e6591-263">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

