---
title: Asignación de metadatos
description: El contenido de un documento de metadatos se asigna a la API de metadatos de las maneras que se explican en las secciones siguientes.
ms.assetid: 266f8319-b7ac-497f-8eb7-8e2c7bcede33
keywords:
- Servicios web de asignación de metadatos para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e6577e05f1d51ec13cc917465c306b94c403827149b086f252a38964997ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841495"
---
# <a name="metadata-mapping"></a>Asignación de metadatos

El contenido de un documento de metadatos se asigna a la API de metadatos de las maneras que se explican en las secciones siguientes.


En esta documentación se usan los siguientes prefijos de espacio de nombres:

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

En las secciones siguientes se describen las construcciones de API junto con las construcciones de metadatos (WSDL o Directiva) a las que se corresponden.

La familiaridad con las especificaciones de metadatos, como WSDL y Policy, ayudará a comprender esta sección.

## <a name="endpoint-address"></a>Dirección del punto de conexión

La dirección de un punto de conexión (vea DIRECCIÓN DEL PUNTO DE CONEXIÓN de [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) se obtiene de un elemento de extensibilidad dentro del elemento wsdl:port del documento WSDL. Se admiten los siguientes elementos de extensibilidad para especificar la dirección :

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

## <a name="ws_channel_binding"></a>ENLACE DE \_ CANAL WS \_

El enlace de canal (vea [**WS \_ CHANNEL \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) viene determinado por el transporte que usa el enlace soap, como se muestra a continuación:

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a>VERSIÓN DEL SOBRE \_ \_ DE PROPIEDAD DEL \_ CANAL \_ WS

La versión del sobre (vea [**WS \_ CHANNEL PROPERTY ENVELOPE \_ \_ \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) viene determinada por el enlace soap que se usa, como se muestra a continuación:

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

## <a name="addressing-version"></a>Versión de direccionamiento

La versión de direccionamiento (consulte [**WS \_ CHANNEL PROPERTY \_ \_ ADDRESSING \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) viene determinada por las aserciones siguientes en la directiva de punto de conexión:

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

Si no hay ninguna aserción de direccionamiento, se supone [**que WS \_ ADDRESSING \_ VERSION \_ TRANSPORT.**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)

## <a name="message-encoding"></a>Codificación de mensajes

La codificación del mensaje (vea [**WS \_ CHANNEL PROPERTY \_ \_ ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) viene determinada por las aserciones siguientes en la directiva de punto de conexión:

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

Tenga en cuenta que la aserción de la directiva de codificación binaria no incluye información sobre si la codificación binaria tiene sesión o no tiene sesión. Esto viene determinado por la restricción de propiedad de codificación (que debe ser adecuada en función de si el tipo de canal de [**WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) que se usa tiene sesión o no).

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

Si no hay ninguna de las aserciones anteriores, se usa una codificación de texto: [**WS \_ ENCODING XML \_ \_ UTF8,**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) **WS ENCODING XML \_ \_ \_ UTF16LE,** **WS ENCODING XML \_ \_ \_ UTF16BE**.

Tenga en cuenta que la directiva no incluye información sobre el juego de caracteres para MTOM o codificaciones de texto (ya sea UTF8, UTF16LE o UTF16BE). El valor real del juego de caracteres utilizado viene determinado por la restricción de propiedad de codificación.

## <a name="constraints-with-http-header-authentication"></a>Restricciones con autenticación de encabezado HTTP

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad [**WS \_ HTTP HEADER \_ \_ AUTH SECURITY BINDING \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

Este enlace de seguridad se indica en la directiva mediante distintas aserciones que indican que se debe usar la autenticación de encabezado HTTP y que se debe usar un esquema de autenticación determinado. Las aserciones de directiva corresponden a los valores de [**WS \_ SECURITY BINDING PROPERTY HTTP HEADER \_ \_ \_ \_ \_ AUTH \_ SCHEME**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) como se muestra a continuación:

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

## <a name="constraints-with-sll-transport-security"></a>Restricciones con seguridad de transporte de SLL

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad [**WS \_ SSL TRANSPORT SECURITY BINDING \_ \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) En este caso, se usan las aserciones de directiva siguientes:

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

## <a name="constraints-with-sspi-transport-security"></a>Restricciones con seguridad de transporte de SSPI

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad [**TRANSPORT BINDING \_ \_ \_ \_ \_ \_ CONSTRAINT de WS TCP SSPI.**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) En este caso, se usan las aserciones de directiva siguientes:

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

## <a name="constrains-with-transport-security"></a>Restricciones con seguridad de transporte

La [**restricción de propiedad WS SECURITY PROPERTY TRANSPORT PROTECTION \_ \_ \_ \_ \_ LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) se puede especificar si se especifica alguna de las restricciones de enlace de seguridad:

-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE TRANSPORTE SSL \_ \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    El valor de la directiva siempre es [**WS \_ PROTECTION LEVEL SIGN AND \_ \_ \_ \_ ENCRYPT**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

-   [**RESTRICCIÓN DE ENLACE DE SEGURIDAD DE TRANSPORTE DE WS \_ TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    El valor de la directiva se especifica como parte de la aserción de WindowsTransportSecurity, como se indica a continuación:

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE \_ \_ AUTH DEL \_ ENCABEZADO \_ \_ HTTP WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    El valor de la directiva siempre es [**WS \_ PROTECTION LEVEL \_ \_ NONE**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

## <a name="constraints-with-kerberos-apreq-security-binding"></a>Restricciones con el enlace de seguridad APREQ de Kerberos

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad [**MESSAGE BINDING CONSTRAINT de WS \_ KERBEROS \_ APREQ. \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) En este caso, se usan las aserciones de directiva siguientes:

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a>Restricciones con enlace de seguridad de mensajes

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad [**WS \_ USERNAME MESSAGE SECURITY BINDING \_ \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) En este caso, se usan las aserciones de directiva siguientes:

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a>RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE \_ \_ \_ \_ CERTIFICADO WS

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad [**WS \_ CERT MESSAGE SECURITY BINDING \_ \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) En este caso, se usan las aserciones de directiva siguientes:

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a>RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE TOKEN \_ \_ \_ \_ \_ EMITIDOS POR WS

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad [**WS \_ ISSUED \_ TOKEN MESSAGE \_ SECURITY \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) En este caso, se usan las aserciones de directiva siguientes:

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

A continuación se describe la asignación de campos de la RESTRICCIÓN DE ENLACE DE SEGURIDAD DE MENSAJES DE TOKEN EMITIDOS por [**WS \_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) a la directiva anterior:

-   El campo claimConstraints se usa para comprobar el conjunto de URI de tipo de notificación que aparecen en el elemento wsi:ClaimType anterior.

-   El campo issuerAddress corresponde al elemento wsp:Issuer anterior, que es la dirección DEL PUNTO DE CONEXIÓN de [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) del servicio que puede emitir el token.

-   El campo requestSecurityTokenTemplate corresponde a los elementos secundarios del elemento wsp:RequestSecurityTokenTemplate.

## <a name="ws_security_context_message_security_binding_constraint"></a>RESTRICCIÓN DE ENLACE DE SEGURIDAD DEL MENSAJE DE CONTEXTO DE SEGURIDAD DE \_ \_ \_ \_ \_ \_ WS

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad [**WS \_ SECURITY CONTEXT MESSAGE SECURITY BINDING \_ \_ \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) En este caso, se usan las aserciones de directiva siguientes:

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

El modo de entropía viene determinado por la <sp:Trust10> aserción. <sp:RequireClientEntropy/> y <sp:RequireServerEntropy/> => [**WS \_ SECURITY KEY \_ \_ ENTROPY MODE \_ \_ COMBINED**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <sp:RequireClientEntropy/> => **WS SECURITY KEY \_ \_ \_ ENTROPY \_ MODE \_ CLIENT \_ ONLY** <sp:RequireServerEntropy/> => **WS SECURITY KEY \_ \_ \_ ENTROPY \_ MODE SERVER \_ \_ ONLY**

## <a name="ws_request_security_token_property_trust_version"></a>VERSIÓN DE CONFIANZA DE LA PROPIEDAD DEL TOKEN DE SEGURIDAD DE WS \_ \_ \_ \_ \_ \_ REQUEST

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad [**WS \_ ISSUED \_ TOKEN MESSAGE \_ SECURITY \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) Las aserciones de directiva siguientes se usan para identificar la [**versión de WS \_ TRUST \_ y**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) las opciones asociadas.

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

La versión de confianza se puede especificar mediante [**WS \_ REQUEST SECURITY TOKEN PROPERTY \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) con un identificador de propiedad de [**WS REQUEST SECURITY TOKEN \_ PROPERTY TRUST \_ \_ \_ \_ \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).

## <a name="ws_security_property_security_header_version"></a>VERSIÓN DEL ENCABEZADO \_ DE SEGURIDAD DE LA \_ \_ PROPIEDAD WS \_ SECURITY \_

Esta sección se aplica cuando se usa cualquiera de las siguientes restricciones de enlace:

-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE WS KERBEROS \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**RESTRICCIÓN DE ENLACE \_ DE SEGURIDAD DE MENSAJES DE NOMBRE DE \_ \_ \_ USUARIO DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE \_ \_ \_ \_ CERTIFICADO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE TOKEN \_ \_ \_ \_ \_ EMITIDOS POR WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

La versión de seguridad del encabezado (especificada por [**WS \_ SECURITY PROPERTY SECURITY HEADER \_ \_ \_ \_ VERSION)**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)viene determinada por una de las aserciones de directiva siguientes:

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a>Restricciones con diseño de seguridad de encabezado

Esta sección se aplica cuando se usa cualquiera de las siguientes restricciones de enlace:

-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE WS KERBEROS \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**RESTRICCIÓN DE ENLACE \_ DE SEGURIDAD DE MENSAJES DE NOMBRE DE \_ \_ \_ USUARIO DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE \_ \_ \_ \_ CERTIFICADO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE TOKEN \_ \_ \_ \_ \_ EMITIDOS POR WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

El diseño del encabezado de seguridad (especificado por [**WS \_ SECURITY PROPERTY SECURITY HEADER \_ \_ \_ \_ LAYOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) viene determinado por una de las aserciones de directiva siguientes:

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

## <a name="constraints-with-timestamp-security"></a>Restricciones con seguridad de marca de tiempo

Esta sección se aplica cuando se usa cualquiera de las siguientes restricciones de enlace:

-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE WS KERBEROS \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**RESTRICCIÓN DE ENLACE \_ DE SEGURIDAD DE MENSAJES DE NOMBRE DE \_ \_ \_ USUARIO DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE \_ \_ \_ \_ CERTIFICADO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE TOKEN \_ \_ \_ \_ \_ EMITIDOS POR WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

La presencia de sp:IncludeTimestamp en la ubicación siguiente determina si se incluye o no una marca de tiempo en el encabezado de seguridad (como se especifica en [**WS \_ SECURITY PROPERTY \_ TIMESTAMP \_ \_ USAGE):**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

Si la aserción sp:IncludeTimestamp está presente, el valor de la directiva es [**WS \_ SECURITY TIMESTAMP USAGE \_ \_ \_ ALWAYS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

Si la aserción sp:IncludeTimestamp no está presente, el valor de la directiva es [**WS \_ SECURITY TIMESTAMP USAGE \_ \_ \_ NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

 

 




