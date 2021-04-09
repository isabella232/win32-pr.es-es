---
title: Enlaces de seguridad
description: Un enlace de seguridad es la especificación de un token de seguridad e indica al tiempo de ejecución cómo obtener y usar un token de seguridad para la seguridad del canal.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Servicios Web de enlaces de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104149734"
---
# <a name="security-bindings"></a><span data-ttu-id="41bc2-106">Enlaces de seguridad</span><span class="sxs-lookup"><span data-stu-id="41bc2-106">Security Bindings</span></span>

<span data-ttu-id="41bc2-107">Un enlace de seguridad es la especificación de un token de seguridad e indica al tiempo de ejecución cómo obtener y usar un token de seguridad para la seguridad del canal.</span><span class="sxs-lookup"><span data-stu-id="41bc2-107">A security binding is the specification of a security token, and tells the runtime how to obtain and use a security token for channel security.</span></span> <span data-ttu-id="41bc2-108">El token de seguridad contiene información que garantiza el derecho a tener acceso a los recursos.</span><span class="sxs-lookup"><span data-stu-id="41bc2-108">The security token contains information that vouches for the right to access resources.</span></span> <span data-ttu-id="41bc2-109">También puede tener una clave criptográfica asociada para realizar firmas y cifrado.</span><span class="sxs-lookup"><span data-stu-id="41bc2-109">It may also have an associated cryptographic key for performing signatures and encryption.</span></span>


<span data-ttu-id="41bc2-110">Cada enlace de seguridad contiene su propia colección de [Opciones de enlace de seguridad](security-binding-settings.md) opcionales cuyo ámbito es el token de seguridad que define.</span><span class="sxs-lookup"><span data-stu-id="41bc2-110">Each security binding contains its own collection of optional [security binding settings](security-binding-settings.md) that are scoped to the security token it defines.</span></span> <span data-ttu-id="41bc2-111">También contiene [credenciales de seguridad](security-credentials.md), que representan la evidencia de seguridad (como el nombre de usuario y contraseñas o los certificados) necesarios para crear tokens de seguridad.</span><span class="sxs-lookup"><span data-stu-id="41bc2-111">It also contains [security credentials](security-credentials.md), representing the security evidence (such as username and passwords, or certificates) needed to create security tokens.</span></span>

<span data-ttu-id="41bc2-112">Las siguientes devoluciones de llamada forman parte del enlace de seguridad:</span><span class="sxs-lookup"><span data-stu-id="41bc2-112">The following callbacks are part of the security binding:</span></span>

-   [<span data-ttu-id="41bc2-113">**\_devolución de \_ llamada de SAML Validate de WS \_**</span><span class="sxs-lookup"><span data-stu-id="41bc2-113">**WS\_VALIDATE\_SAML\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

<span data-ttu-id="41bc2-114">Las enumeraciones siguientes forman parte del enlace de seguridad:</span><span class="sxs-lookup"><span data-stu-id="41bc2-114">The following enumerations are part of the security binding:</span></span>

-   [<span data-ttu-id="41bc2-115">**\_uso de \_ seguridad de mensajes de WS \_**</span><span class="sxs-lookup"><span data-stu-id="41bc2-115">**WS\_MESSAGE\_SECURITY\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [<span data-ttu-id="41bc2-116">**\_tipo de \_ autenticador \_ SAML de WS**</span><span class="sxs-lookup"><span data-stu-id="41bc2-116">**WS\_SAML\_AUTHENTICATOR\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [<span data-ttu-id="41bc2-117">**tipo de enlace de WS \_ Security \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41bc2-117">**WS\_SECURITY\_BINDING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [<span data-ttu-id="41bc2-118">**\_tipo de \_ identificador de clave \_ \_ de WS Security**</span><span class="sxs-lookup"><span data-stu-id="41bc2-118">**WS\_SECURITY\_KEY\_HANDLE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

<span data-ttu-id="41bc2-119">Las siguientes funciones forman parte del enlace de seguridad:</span><span class="sxs-lookup"><span data-stu-id="41bc2-119">The following functions are part of the security binding:</span></span>

-   [<span data-ttu-id="41bc2-120">**WsCreateXmlSecurityToken**</span><span class="sxs-lookup"><span data-stu-id="41bc2-120">**WsCreateXmlSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [<span data-ttu-id="41bc2-121">**WsFreeSecurityToken**</span><span class="sxs-lookup"><span data-stu-id="41bc2-121">**WsFreeSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

<span data-ttu-id="41bc2-122">Las siguientes estructuras forman parte del enlace de seguridad:</span><span class="sxs-lookup"><span data-stu-id="41bc2-122">The following structures are part of the security binding:</span></span>

-   [<span data-ttu-id="41bc2-123">**\_identificador de \_ \_ clave de seguridad asimétrica \_ \_ de WS CAPI**</span><span class="sxs-lookup"><span data-stu-id="41bc2-123">**WS\_CAPI\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [<span data-ttu-id="41bc2-124">**\_ \_ \_ autenticador SAML firmado de certificado WS \_**</span><span class="sxs-lookup"><span data-stu-id="41bc2-124">**WS\_CERT\_SIGNED\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [<span data-ttu-id="41bc2-125">**\_enlace de \_ \_ seguridad de autenticación de encabezado HTTP \_ de \_ WS**</span><span class="sxs-lookup"><span data-stu-id="41bc2-125">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [<span data-ttu-id="41bc2-126">**\_enlace de \_ \_ seguridad de mensajes WS Kerberos APREQ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41bc2-126">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [<span data-ttu-id="41bc2-127">**\_enlace de \_ \_ seguridad de transporte SSPI \_ \_ de WS NAMEDPIPE**</span><span class="sxs-lookup"><span data-stu-id="41bc2-127">**WS\_NAMEDPIPE\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="41bc2-128">**\_identificador de \_ \_ clave de seguridad asimétrica \_ \_ de WS NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="41bc2-128">**WS\_NCRYPT\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [<span data-ttu-id="41bc2-129">**\_identificador de \_ \_ clave de seguridad simétrica sin \_ procesar \_ de WS**</span><span class="sxs-lookup"><span data-stu-id="41bc2-129">**WS\_RAW\_SYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [<span data-ttu-id="41bc2-130">**\_autenticador de SAML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="41bc2-130">**WS\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [<span data-ttu-id="41bc2-131">**\_enlace de \_ seguridad de mensajes SAML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="41bc2-131">**WS\_SAML\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [<span data-ttu-id="41bc2-132">**\_enlace de seguridad de WS \_**</span><span class="sxs-lookup"><span data-stu-id="41bc2-132">**WS\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [<span data-ttu-id="41bc2-133">**\_enlace de \_ seguridad de mensaje de contexto \_ \_ de WS Security \_**</span><span class="sxs-lookup"><span data-stu-id="41bc2-133">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [<span data-ttu-id="41bc2-134">**identificador de clave de WS \_ Security \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41bc2-134">**WS\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [<span data-ttu-id="41bc2-135">**\_enlace de \_ seguridad de transporte WS SSL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41bc2-135">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [<span data-ttu-id="41bc2-136">**\_enlace de \_ \_ seguridad de transporte SSPI \_ \_ de WS TCP**</span><span class="sxs-lookup"><span data-stu-id="41bc2-136">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [<span data-ttu-id="41bc2-137">**\_enlace de \_ seguridad de mensaje \_ \_ de WS username**</span><span class="sxs-lookup"><span data-stu-id="41bc2-137">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [<span data-ttu-id="41bc2-138">**\_enlace de \_ seguridad de mensaje de token \_ \_ de WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="41bc2-138">**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




