---
title: Asignación de metadatos
description: El contenido de un documento de metadatos se asigna a la API de metadatos de las maneras que se explican en las secciones siguientes.
ms.assetid: 266f8319-b7ac-497f-8eb7-8e2c7bcede33
keywords:
- Servicios Web de asignación de metadatos para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb9da067768569e78ba6bb98ee219e11917d3201
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105695806"
---
# <a name="metadata-mapping"></a><span data-ttu-id="8716b-106">Asignación de metadatos</span><span class="sxs-lookup"><span data-stu-id="8716b-106">Metadata Mapping</span></span>

<span data-ttu-id="8716b-107">El contenido de un documento de metadatos se asigna a la API de metadatos de las maneras que se explican en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="8716b-107">The contents of a metadata document map to the metadata API in the ways explained in the following sections.</span></span>


<span data-ttu-id="8716b-108">En esta documentación se usan los siguientes prefijos de espacio de nombres:</span><span class="sxs-lookup"><span data-stu-id="8716b-108">The following namespace prefixes are used throughout this documentation:</span></span>

``` syntax
wsdl   => http://schemas.xmlsoap.org/wsdl/
soap11 => http://schemas.xmlsoap.org/wsdl/soap/
soap12 => http://schemas.xmlsoap.org/wsdl/soap12/
wsa09  => http://schemas.xmlsoap.org/ws/2004/08/addressing
wsa10  => http://www.w3.org/2005/08/addressing
wsa09p => http://schemas.xmlsoap.org/ws/2004/08/addressing/policy
wsa10p => http://www.w3.org/2006/05/addressing/wsdl
binp   => http://schemas.microsoft.com/ws/06/2004/mspolicy/netbinary1
mtomp  => http://schemas.xmlsoap.org/ws/2004/09/policy/optimizedmimeserialization
sp     => http://schemas.xmlsoap.org/ws/2005/07/securitypolicy
wsp    => http://schemas.xmlsoap.org/ws/2004/09/policy
netf   => http://schemas.microsoft.com/ws/2006/05/framing/policy
httpp  => http://schemas.microsoft.com/ws/06/2004/policy/http
wst10  => http://schemas.xmlsoap.org/ws/2005/02/trust
wsi    => http://schemas.xmlsoap.org/ws/2005/05/identity
```

<span data-ttu-id="8716b-109">En las secciones siguientes se describen las construcciones de API junto con qué construcciones de metadatos (WSDL o Directiva) corresponden.</span><span class="sxs-lookup"><span data-stu-id="8716b-109">The subsequent sections describe API constructs along with what metadata constructs (WSDL or Policy) they correspond to.</span></span>

<span data-ttu-id="8716b-110">Familiarizarse con las especificaciones de metadatos, como WSDL y Policy, ayudará a comprender esta sección.</span><span class="sxs-lookup"><span data-stu-id="8716b-110">Familiarity with metadata specifications such as WSDL and Policy will aid in understanding this section.</span></span>

## <a name="endpoint-address"></a><span data-ttu-id="8716b-111">Dirección del extremo</span><span class="sxs-lookup"><span data-stu-id="8716b-111">Endpoint address</span></span>

<span data-ttu-id="8716b-112">La dirección de un punto de conexión (vea [**\_ \_ dirección del punto de conexión de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) se obtiene de un elemento de extensibilidad dentro del elemento wsdl: Port del documento WSDL.</span><span class="sxs-lookup"><span data-stu-id="8716b-112">The address of an endpoint (see [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) is obtained from an extensibility element within the wsdl:port element of the WSDL document.</span></span> <span data-ttu-id="8716b-113">Se admiten los siguientes elementos de extensibilidad para especificar la dirección:</span><span class="sxs-lookup"><span data-stu-id="8716b-113">The following extensibility elements are supported for specifying the address:</span></span>

``` syntax
<wsdl:port...>
    <soap11:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <soap12:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa09:EndpointReference.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa10:EndpointReference.../>
</wsdl:port>
```

## <a name="ws_channel_binding"></a><span data-ttu-id="8716b-114">\_enlace de canal de WS \_</span><span class="sxs-lookup"><span data-stu-id="8716b-114">WS\_CHANNEL\_BINDING</span></span>

<span data-ttu-id="8716b-115">El enlace de canal (consulte [**WS \_ Channel \_ Binding**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) viene determinado por el transporte que se usa en el enlace SOAP, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8716b-115">The channel binding (see [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) is determined by the transport the soap binding used, as follows:</span></span>

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a><span data-ttu-id="8716b-116">\_versión de \_ sobre de propiedades de canal de WS \_ \_</span><span class="sxs-lookup"><span data-stu-id="8716b-116">WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION</span></span>

<span data-ttu-id="8716b-117">La versión de sobre (vea la versión de sobre de propiedad de canal de WS) viene determinada por el enlace SOAP que se utiliza, como se indica a continuación: [**\_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)</span><span class="sxs-lookup"><span data-stu-id="8716b-117">The envelope version (see [**WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by which soap binding is used, as follows:</span></span>

``` syntax
<wsdl:binding...>
    <soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

``` syntax
<wsdl:binding...>
    <soap12:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_2
</wsdl:binding>
```

## <a name="addressing-version"></a><span data-ttu-id="8716b-118">Versión de direccionamiento</span><span class="sxs-lookup"><span data-stu-id="8716b-118">Addressing Version</span></span>

<span data-ttu-id="8716b-119">La versión de direccionamiento (vea [**WS \_ Channel \_ Property \_ Addressing \_ version**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) viene determinada por las siguientes aserciones en la Directiva de punto de conexión:</span><span class="sxs-lookup"><span data-stu-id="8716b-119">The addressing version (see [**WS\_CHANNEL\_PROPERTY\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

``` syntax
<wsp:Policy...>
    <wsa09p:UsingAddressing.../> => WS_ADDRESSING_VERSION_0_9
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <wsa10p:UsingAddressing.../> => WS_ADDRESSING_VERSION_1_0
</wsp:Policy>
```

<span data-ttu-id="8716b-120">Si no hay ninguna aserción de direccionamiento, se supone el transporte de la [**versión de WS \_ Addressing \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .</span><span class="sxs-lookup"><span data-stu-id="8716b-120">If an addressing assertion is not present, then [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) is assumed.</span></span>

## <a name="message-encoding"></a><span data-ttu-id="8716b-121">Codificación de mensajes</span><span class="sxs-lookup"><span data-stu-id="8716b-121">Message Encoding</span></span>

<span data-ttu-id="8716b-122">La codificación del mensaje (consulte codificación de [**\_ propiedades de \_ \_ canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) viene determinada por las siguientes aserciones de la Directiva de extremo:</span><span class="sxs-lookup"><span data-stu-id="8716b-122">The encoding of the message (see [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

<span data-ttu-id="8716b-123">Tenga en cuenta que la aserción de directiva de codificación binaria no incluye información sobre si la codificación binaria es con sesión o sin sesión.</span><span class="sxs-lookup"><span data-stu-id="8716b-123">Note that the binary encoding policy assertion does not include information about whether the binary encoding is sessionful or sessionless.</span></span> <span data-ttu-id="8716b-124">Esto viene determinado por la restricción de propiedad de codificación (que debe ser adecuada según si el [**\_ \_ tipo de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) que se está usando es o no con sesión).</span><span class="sxs-lookup"><span data-stu-id="8716b-124">This is determined by the encoding property constraint (which should be appropriate according to whether or not the [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) being used is sessionful or not).</span></span>

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

<span data-ttu-id="8716b-125">Si ninguna de las aserciones anteriores está presente, se usa una codificación de texto: [**WS \_ codificación \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ codificación \_ XML \_ UTF16LE**, **WS \_ codificación \_ XML \_ UTF16BE**.</span><span class="sxs-lookup"><span data-stu-id="8716b-125">If neither of the above assertions are present, then a text encoding is used: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS\_ENCODING\_XML\_UTF16LE**, **WS\_ENCODING\_XML\_UTF16BE**.</span></span>

<span data-ttu-id="8716b-126">Tenga en cuenta que la Directiva no incluye información sobre el juego de caracteres para MTOM o codificaciones de texto (ya sea UTF8, UTF16LE o UTF16BE).</span><span class="sxs-lookup"><span data-stu-id="8716b-126">Note that policy does not include information about the character set for MTOM or text encodings (whether it is UTF8, UTF16LE or UTF16BE).</span></span> <span data-ttu-id="8716b-127">El valor del juego de caracteres real utilizado está determinado por la restricción de la propiedad de codificación.</span><span class="sxs-lookup"><span data-stu-id="8716b-127">The actual character set value used is determined by the encoding property constraint.</span></span>

## <a name="constraints-with-http-header-authentication"></a><span data-ttu-id="8716b-128">Restricciones con autenticación de encabezado HTTP</span><span class="sxs-lookup"><span data-stu-id="8716b-128">Constraints with HTTP Header Authentication</span></span>

<span data-ttu-id="8716b-129">Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**\_ \_ autenticación del encabezado \_ \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="8716b-129">This section applies when the [**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) security binding constraint is specified.</span></span>

<span data-ttu-id="8716b-130">Este enlace de seguridad se indica en la Directiva mediante aserciones diferentes que indica que se debe usar la autenticación de encabezado HTTP y que se debe usar un esquema de autenticación determinado.</span><span class="sxs-lookup"><span data-stu-id="8716b-130">This security binding is indicated in the policy by different assertions that states both that HTTP header authentication should be used, and that a particular authentication scheme should be used.</span></span> <span data-ttu-id="8716b-131">Las aserciones de Directiva se corresponden con los valores del [**\_ esquema de \_ \_ autenticación de \_ \_ encabezado HTTP \_ \_ de la propiedad de enlace WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8716b-131">The policy assertions correspond to the values of the [**WS\_SECURITY\_BINDING\_PROPERTY\_HTTP\_HEADER\_AUTH\_SCHEME**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) as follows:</span></span>

``` syntax
<wsp:Policy...>
    <httpp:BasicAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_BASIC
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NegotiateAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NtlmAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NTLM
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:DigestAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_DIGEST
</wsp:Policy>
```

## <a name="constraints-with-sll-transport-security"></a><span data-ttu-id="8716b-132">Restricciones con seguridad de transporte de SSL</span><span class="sxs-lookup"><span data-stu-id="8716b-132">Constraints with SLL Transport Security</span></span>

<span data-ttu-id="8716b-133">Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la [**restricción de enlace de \_ seguridad de \_ transporte \_ \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="8716b-133">This section applies when the [**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8716b-134">En este caso, se usan las siguientes aserciones de directiva:</span><span class="sxs-lookup"><span data-stu-id="8716b-134">The following policy assertions are used in this case:</span></span>

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <sp:HttpsToken.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constraints-with-sspi-transport-security"></a><span data-ttu-id="8716b-135">Restricciones con seguridad de transporte SSPI</span><span class="sxs-lookup"><span data-stu-id="8716b-135">Constraints with SSPI Transport Security</span></span>

<span data-ttu-id="8716b-136">Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**\_ \_ \_ \_ \_ \_ transporte SSPI de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="8716b-136">This section applies when the [**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8716b-137">En este caso, se usan las siguientes aserciones de directiva:</span><span class="sxs-lookup"><span data-stu-id="8716b-137">The following policy assertions are used in this case:</span></span>

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <netf:WindowsTransportSecurity.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constrains-with-transport-security"></a><span data-ttu-id="8716b-138">Restricciones con seguridad de transporte</span><span class="sxs-lookup"><span data-stu-id="8716b-138">Constrains with Transport Security</span></span>

<span data-ttu-id="8716b-139">Se puede especificar la restricción de propiedad de [**nivel de protección de transporte de propiedades de WS \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) si se especifica cualquiera de las restricciones de enlace de seguridad:</span><span class="sxs-lookup"><span data-stu-id="8716b-139">The [**WS\_SECURITY\_PROPERTY\_TRANSPORT\_PROTECTION\_LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) property constraint can be specified if any of the security binding constraints are specified:</span></span>

-   [<span data-ttu-id="8716b-140">**\_restricción de \_ \_ enlace de seguridad de transporte SSL \_ de \_ WS**</span><span class="sxs-lookup"><span data-stu-id="8716b-140">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    <span data-ttu-id="8716b-141">El valor de la Directiva siempre es el [**\_ nivel de protección WS y el \_ \_ \_ \_ cifrado**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span><span class="sxs-lookup"><span data-stu-id="8716b-141">The value from policy is always [**WS\_PROTECTION\_LEVEL\_SIGN\_AND\_ENCRYPT**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

-   [<span data-ttu-id="8716b-142">**\_restricción de \_ \_ enlace de seguridad de transporte SSPI \_ \_ de WS TCP \_**</span><span class="sxs-lookup"><span data-stu-id="8716b-142">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    <span data-ttu-id="8716b-143">El valor de la Directiva se especifica como parte de la aserción WindowsTransportSecurity, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8716b-143">The value from policy is specified as part of the WindowsTransportSecurity assertion, as follows:</span></span>

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [<span data-ttu-id="8716b-144">**\_restricción de \_ \_ enlace de seguridad de autenticación de encabezado \_ http \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="8716b-144">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    <span data-ttu-id="8716b-145">El valor de la Directiva siempre es el [**\_ \_ nivel \_ de protección WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span><span class="sxs-lookup"><span data-stu-id="8716b-145">The value from policy is always [**WS\_PROTECTION\_LEVEL\_NONE**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

## <a name="constraints-with-kerberos-apreq-security-binding"></a><span data-ttu-id="8716b-146">Restricciones con el enlace de seguridad de Kerberos APREQ</span><span class="sxs-lookup"><span data-stu-id="8716b-146">Constraints with Kerberos APREQ Security Binding</span></span>

<span data-ttu-id="8716b-147">Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**\_ mensajes WS Kerberos \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="8716b-147">This section applies when the [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8716b-148">En este caso, se usan las siguientes aserciones de directiva:</span><span class="sxs-lookup"><span data-stu-id="8716b-148">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a><span data-ttu-id="8716b-149">Restricciones con el enlace de seguridad de mensajes</span><span class="sxs-lookup"><span data-stu-id="8716b-149">Constraints with Message Security Binding</span></span>

<span data-ttu-id="8716b-150">Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**mensajes de WS \_ username \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="8716b-150">This section applies when the [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8716b-151">En este caso, se usan las siguientes aserciones de directiva:</span><span class="sxs-lookup"><span data-stu-id="8716b-151">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a><span data-ttu-id="8716b-152">\_restricción de \_ enlace de seguridad de mensajes de certificado WS \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="8716b-152">WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="8716b-153">Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**\_ \_ mensajes \_ \_ \_ WS CERT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="8716b-153">This section applies when the [**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8716b-154">En este caso, se usan las siguientes aserciones de directiva:</span><span class="sxs-lookup"><span data-stu-id="8716b-154">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a><span data-ttu-id="8716b-155">\_restricción de \_ \_ enlace de seguridad de mensaje de token \_ emitido \_ de WS \_</span><span class="sxs-lookup"><span data-stu-id="8716b-155">WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="8716b-156">Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**\_ \_ mensaje de token \_ \_ \_ \_ emitido de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="8716b-156">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8716b-157">En este caso, se usan las siguientes aserciones de directiva:</span><span class="sxs-lookup"><span data-stu-id="8716b-157">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:IssuedToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:RequestSecurityTokenTemplate TrustVersion='xs:anyURI&quot;?>
                ...
                <wst10:Claims>
                    <wsi:ClaimType Optional='xs:boolean'?>xs:anyURI<wt:ClaimType>*
                </wst10:Claims>
                ...
            </wsp:RequestSecurityTokenTemplate>
            <wsp:Policy>
                <sp:RequireDerivedKeys/> ?
                <sp:RequireExternalReference/> ?
                <sp:RequireInternalReference/> ?
            </wsp:Policy> ?
        </sp:IssuedToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

<span data-ttu-id="8716b-158">A continuación se describe la asignación de campos de [**la \_ \_ restricción de \_ \_ enlace de \_ \_ seguridad de mensaje de token emitido de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) a la directiva anterior:</span><span class="sxs-lookup"><span data-stu-id="8716b-158">The following describes the mapping of fields of the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) to the above policy:</span></span>

-   <span data-ttu-id="8716b-159">El campo claimConstraints se usa para comprobar el conjunto de identificadores URI de tipo de demanda que aparecen en el elemento WSI: ClaimType anterior.</span><span class="sxs-lookup"><span data-stu-id="8716b-159">The claimConstraints field is used to verify the set of claim type URIs that appear within the wsi:ClaimType element above.</span></span>

-   <span data-ttu-id="8716b-160">El campo issuerAddress se corresponde con el elemento WSP: issuer anterior, que es [**la \_ \_ dirección del punto de conexión de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) del servicio que puede emitir el token.</span><span class="sxs-lookup"><span data-stu-id="8716b-160">The issuerAddress field corresponds to the wsp:Issuer element above, which is the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) of the service that can issue the token.</span></span>

-   <span data-ttu-id="8716b-161">El campo requestSecurityTokenTemplate se corresponde con los elementos secundarios del elemento WSP: RequestSecurityTokenTemplate.</span><span class="sxs-lookup"><span data-stu-id="8716b-161">The requestSecurityTokenTemplate field corresponds to the child elements of the wsp:RequestSecurityTokenTemplate element.</span></span>

## <a name="ws_security_context_message_security_binding_constraint"></a><span data-ttu-id="8716b-162">\_restricción de \_ \_ enlace de seguridad de mensaje de contexto \_ de \_ WS Security \_</span><span class="sxs-lookup"><span data-stu-id="8716b-162">WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="8716b-163">Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de restricción de enlace de seguridad de [**mensaje de contexto de WS \_ \_ \_ \_ \_ \_ Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="8716b-163">This section applies when the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8716b-164">En este caso, se usan las siguientes aserciones de directiva:</span><span class="sxs-lookup"><span data-stu-id="8716b-164">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:SecureConversationToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:Policy>
                <sp:RequireDerivedKeys.../>?
                <sp:RequireExternalUriReference.../>?
                <sp:SC10SecurityContextToken.../>? => WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005
                <sp:BootstrapPolicy... >?
                   <wsp:Policy> ...  </wsp:Policy> => WS_SECURITY_CONSTRAINTS
                </sp:BootstrapPolicy>
            </wsp:Policy>
        </wsp:SecureConversationToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

<span data-ttu-id="8716b-165">El modo de entropía viene determinado por la aserción <SP: Trust10>.</span><span class="sxs-lookup"><span data-stu-id="8716b-165">The entropy mode is determined by the <sp:Trust10> assertion.</span></span> <span data-ttu-id="8716b-166"><SP: RequireClientEntropy/> y <SP: RequireServerEntropy/> => [**\_ modo de entropía de clave de seguridad ws \_ \_ \_ \_ combinado**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <SP: RequireClientEntropy/> => el **modo de entropía de clave de seguridad de WS \_ \_ \_ \_ \_ \_ solo** <SP: RequireServerEntropy/> => **WS \_ Security \_ \_ \_ \_ \_ solo servidor de modo de entropía de clave**</span><span class="sxs-lookup"><span data-stu-id="8716b-166"><sp:RequireClientEntropy/> and <sp:RequireServerEntropy/> => [**WS\_SECURITY\_KEY\_ENTROPY\_MODE\_COMBINED**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <sp:RequireClientEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_CLIENT\_ONLY** <sp:RequireServerEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_SERVER\_ONLY**</span></span>

## <a name="ws_request_security_token_property_trust_version"></a><span data-ttu-id="8716b-167">versión de confianza de la \_ propiedad de token de seguridad de solicitud WS \_ \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="8716b-167">WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION</span></span>

<span data-ttu-id="8716b-168">Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**\_ \_ mensaje de token \_ \_ \_ \_ emitido de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="8716b-168">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8716b-169">Las aserciones de directiva siguientes se usan para identificar la [**\_ \_ versión de WS Trust**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) y las opciones asociadas.</span><span class="sxs-lookup"><span data-stu-id="8716b-169">The following policy assertions are used to identify the [**WS\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) and associated options.</span></span>

``` syntax
<sp:Trust10> => WS_TRUST_VERSION_FEBRUARY_2005
    <sp:Policy>
        <sp:MustSupportClientChallenge/> ?
        <sp:MustSupportServerChallenge/> ?
        <sp:RequireClientEntropy/> ?
        <sp:RequireServerEntropy/> ?
        <sp:MustSupportIssuedTokens/> ?
    </sp:Policy>
</sp:Trust10>
```

<span data-ttu-id="8716b-170">La versión de confianza se puede especificar mediante [**la \_ \_ restricción de \_ \_ propiedad del \_ token de seguridad**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) de la solicitud de WS con un identificador de propiedad de la versión de confianza de la propiedad del token de seguridad de la [**\_ solicitud \_ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).</span><span class="sxs-lookup"><span data-stu-id="8716b-170">The trust version can be specified using the [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) with a property id of [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).</span></span>

## <a name="ws_security_property_security_header_version"></a><span data-ttu-id="8716b-171">\_versión del \_ \_ encabezado de \_ seguridad \_ de la propiedad WS Security</span><span class="sxs-lookup"><span data-stu-id="8716b-171">WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION</span></span>

<span data-ttu-id="8716b-172">Esta sección se aplica cuando se usa cualquiera de las siguientes restricciones de enlace:</span><span class="sxs-lookup"><span data-stu-id="8716b-172">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="8716b-173">**\_restricción de \_ \_ enlace de \_ seguridad de mensaje \_ \_ WS Kerberos APREQ**</span><span class="sxs-lookup"><span data-stu-id="8716b-173">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="8716b-174">**\_restricción de \_ enlace de seguridad de mensaje \_ \_ de WS username \_**</span><span class="sxs-lookup"><span data-stu-id="8716b-174">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="8716b-175">**\_restricción de \_ enlace de seguridad de mensajes de certificado WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8716b-175">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="8716b-176">**\_restricción de \_ \_ enlace de seguridad de mensaje de token \_ emitido \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="8716b-176">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="8716b-177">La versión de seguridad del encabezado (especificada por la versión de encabezado de seguridad de la [**propiedad de WS \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) se determina mediante una de las siguientes aserciones de directiva:</span><span class="sxs-lookup"><span data-stu-id="8716b-177">The header security version (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a><span data-ttu-id="8716b-178">Restricciones con el diseño de seguridad de encabezado</span><span class="sxs-lookup"><span data-stu-id="8716b-178">Constraints with Header Security Layout</span></span>

<span data-ttu-id="8716b-179">Esta sección se aplica cuando se usa cualquiera de las siguientes restricciones de enlace:</span><span class="sxs-lookup"><span data-stu-id="8716b-179">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="8716b-180">**\_restricción de \_ \_ enlace de \_ seguridad de mensaje \_ \_ WS Kerberos APREQ**</span><span class="sxs-lookup"><span data-stu-id="8716b-180">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="8716b-181">**\_restricción de \_ enlace de seguridad de mensaje \_ \_ de WS username \_**</span><span class="sxs-lookup"><span data-stu-id="8716b-181">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="8716b-182">**\_restricción de \_ enlace de seguridad de mensajes de certificado WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8716b-182">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="8716b-183">**\_restricción de \_ \_ enlace de seguridad de mensaje de token \_ emitido \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="8716b-183">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="8716b-184">El diseño del encabezado de seguridad (tal y como se especifica en el diseño del encabezado de seguridad de la [**propiedad de WS \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) viene determinado por una de las siguientes aserciones de la Directiva:</span><span class="sxs-lookup"><span data-stu-id="8716b-184">The security header layout (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_LAYOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Lax.../> => WS_SECURITY_HEADER_LAYOUT_LAX
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Strict.../> => WS_SECURITY_HEADER_LAYOUT_STRICT
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsFirst.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsLast.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

## <a name="constraints-with-timestamp-security"></a><span data-ttu-id="8716b-185">Restricciones con seguridad de marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="8716b-185">Constraints with Timestamp Security</span></span>

<span data-ttu-id="8716b-186">Esta sección se aplica cuando se usa cualquiera de las siguientes restricciones de enlace:</span><span class="sxs-lookup"><span data-stu-id="8716b-186">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="8716b-187">**\_restricción de \_ \_ enlace de \_ seguridad de mensaje \_ \_ WS Kerberos APREQ**</span><span class="sxs-lookup"><span data-stu-id="8716b-187">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="8716b-188">**\_restricción de \_ enlace de seguridad de mensaje \_ \_ de WS username \_**</span><span class="sxs-lookup"><span data-stu-id="8716b-188">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="8716b-189">**\_restricción de \_ enlace de seguridad de mensajes de certificado WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8716b-189">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="8716b-190">**\_restricción de \_ \_ enlace de seguridad de mensaje de token \_ emitido \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="8716b-190">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="8716b-191">El hecho de que una marca de tiempo se incluya en el encabezado de seguridad (tal y como se especifica en el uso de la marca de tiempo de la [**propiedad de WS \_ Security \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) viene determinada por la presencia de SP: IncludeTimestamp en la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="8716b-191">Whether or not a timestamp is included in the security header (as specified by [**WS\_SECURITY\_PROPERTY\_TIMESTAMP\_USAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by the presence of the sp:IncludeTimestamp in the following location:</span></span>

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

<span data-ttu-id="8716b-192">Si la aserción SP: IncludeTimestamp está presente, el valor de la Directiva es el uso de la marca de tiempo de [**WS \_ Security \_ \_ \_ siempre**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span><span class="sxs-lookup"><span data-stu-id="8716b-192">If the sp:IncludeTimestamp assertion is present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_ALWAYS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

<span data-ttu-id="8716b-193">Si la aserción SP: IncludeTimestamp no está presente, el valor de la Directiva es el uso de la marca de tiempo de [**WS \_ Security \_ \_ \_ nunca**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span><span class="sxs-lookup"><span data-stu-id="8716b-193">If the sp:IncludeTimestamp assertion is not present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

 

 




