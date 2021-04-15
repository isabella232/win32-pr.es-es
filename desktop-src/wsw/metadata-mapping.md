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

En las secciones siguientes se describen las construcciones de API junto con qué construcciones de metadatos (WSDL o Directiva) corresponden.

Familiarizarse con las especificaciones de metadatos, como WSDL y Policy, ayudará a comprender esta sección.

## <a name="endpoint-address"></a>Dirección del extremo

La dirección de un punto de conexión (vea [**\_ \_ dirección del punto de conexión de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) se obtiene de un elemento de extensibilidad dentro del elemento wsdl: Port del documento WSDL. Se admiten los siguientes elementos de extensibilidad para especificar la dirección:

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

## <a name="ws_channel_binding"></a>\_enlace de canal de WS \_

El enlace de canal (consulte [**WS \_ Channel \_ Binding**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) viene determinado por el transporte que se usa en el enlace SOAP, como se indica a continuación:

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a>\_versión de \_ sobre de propiedades de canal de WS \_ \_

La versión de sobre (vea la versión de sobre de propiedad de canal de WS) viene determinada por el enlace SOAP que se utiliza, como se indica a continuación: [**\_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)

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

La versión de direccionamiento (vea [**WS \_ Channel \_ Property \_ Addressing \_ version**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) viene determinada por las siguientes aserciones en la Directiva de punto de conexión:

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

Si no hay ninguna aserción de direccionamiento, se supone el transporte de la [**versión de WS \_ Addressing \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .

## <a name="message-encoding"></a>Codificación de mensajes

La codificación del mensaje (consulte codificación de [**\_ propiedades de \_ \_ canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) viene determinada por las siguientes aserciones de la Directiva de extremo:

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

Tenga en cuenta que la aserción de directiva de codificación binaria no incluye información sobre si la codificación binaria es con sesión o sin sesión. Esto viene determinado por la restricción de propiedad de codificación (que debe ser adecuada según si el [**\_ \_ tipo de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) que se está usando es o no con sesión).

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

Si ninguna de las aserciones anteriores está presente, se usa una codificación de texto: [**WS \_ codificación \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ codificación \_ XML \_ UTF16LE**, **WS \_ codificación \_ XML \_ UTF16BE**.

Tenga en cuenta que la Directiva no incluye información sobre el juego de caracteres para MTOM o codificaciones de texto (ya sea UTF8, UTF16LE o UTF16BE). El valor del juego de caracteres real utilizado está determinado por la restricción de la propiedad de codificación.

## <a name="constraints-with-http-header-authentication"></a>Restricciones con autenticación de encabezado HTTP

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**\_ \_ autenticación del encabezado \_ \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) .

Este enlace de seguridad se indica en la Directiva mediante aserciones diferentes que indica que se debe usar la autenticación de encabezado HTTP y que se debe usar un esquema de autenticación determinado. Las aserciones de Directiva se corresponden con los valores del [**\_ esquema de \_ \_ autenticación de \_ \_ encabezado HTTP \_ \_ de la propiedad de enlace WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) como se indica a continuación:

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

## <a name="constraints-with-sll-transport-security"></a>Restricciones con seguridad de transporte de SSL

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la [**restricción de enlace de \_ seguridad de \_ transporte \_ \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) . En este caso, se usan las siguientes aserciones de directiva:

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

## <a name="constraints-with-sspi-transport-security"></a>Restricciones con seguridad de transporte SSPI

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**\_ \_ \_ \_ \_ \_ transporte SSPI de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) . En este caso, se usan las siguientes aserciones de directiva:

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

Se puede especificar la restricción de propiedad de [**nivel de protección de transporte de propiedades de WS \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) si se especifica cualquiera de las restricciones de enlace de seguridad:

-   [**\_restricción de \_ \_ enlace de seguridad de transporte SSL \_ de \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    El valor de la Directiva siempre es el [**\_ nivel de protección WS y el \_ \_ \_ \_ cifrado**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

-   [**\_restricción de \_ \_ enlace de seguridad de transporte SSPI \_ \_ de WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    El valor de la Directiva se especifica como parte de la aserción WindowsTransportSecurity, como se indica a continuación:

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [**\_restricción de \_ \_ enlace de seguridad de autenticación de encabezado \_ http \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    El valor de la Directiva siempre es el [**\_ \_ nivel \_ de protección WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

## <a name="constraints-with-kerberos-apreq-security-binding"></a>Restricciones con el enlace de seguridad de Kerberos APREQ

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**\_ mensajes WS Kerberos \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) . En este caso, se usan las siguientes aserciones de directiva:

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a>Restricciones con el enlace de seguridad de mensajes

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**mensajes de WS \_ username \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) . En este caso, se usan las siguientes aserciones de directiva:

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a>\_restricción de \_ enlace de seguridad de mensajes de certificado WS \_ \_ \_

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**\_ \_ mensajes \_ \_ \_ WS CERT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) . En este caso, se usan las siguientes aserciones de directiva:

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a>\_restricción de \_ \_ enlace de seguridad de mensaje de token \_ emitido \_ de WS \_

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**\_ \_ mensaje de token \_ \_ \_ \_ emitido de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) . En este caso, se usan las siguientes aserciones de directiva:

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

A continuación se describe la asignación de campos de [**la \_ \_ restricción de \_ \_ enlace de \_ \_ seguridad de mensaje de token emitido de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) a la directiva anterior:

-   El campo claimConstraints se usa para comprobar el conjunto de identificadores URI de tipo de demanda que aparecen en el elemento WSI: ClaimType anterior.

-   El campo issuerAddress se corresponde con el elemento WSP: issuer anterior, que es [**la \_ \_ dirección del punto de conexión de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) del servicio que puede emitir el token.

-   El campo requestSecurityTokenTemplate se corresponde con los elementos secundarios del elemento WSP: RequestSecurityTokenTemplate.

## <a name="ws_security_context_message_security_binding_constraint"></a>\_restricción de \_ \_ enlace de seguridad de mensaje de contexto \_ de \_ WS Security \_

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de restricción de enlace de seguridad de [**mensaje de contexto de WS \_ \_ \_ \_ \_ \_ Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) . En este caso, se usan las siguientes aserciones de directiva:

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

El modo de entropía viene determinado por la aserción <SP: Trust10>. <SP: RequireClientEntropy/> y <SP: RequireServerEntropy/> => [**\_ modo de entropía de clave de seguridad ws \_ \_ \_ \_ combinado**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <SP: RequireClientEntropy/> => el **modo de entropía de clave de seguridad de WS \_ \_ \_ \_ \_ \_ solo** <SP: RequireServerEntropy/> => **WS \_ Security \_ \_ \_ \_ \_ solo servidor de modo de entropía de clave**

## <a name="ws_request_security_token_property_trust_version"></a>versión de confianza de la \_ propiedad de token de seguridad de solicitud WS \_ \_ \_ \_ \_

Esta sección se aplica cuando se especifica la restricción de enlace de seguridad de la restricción de enlace de seguridad de [**\_ \_ mensaje de token \_ \_ \_ \_ emitido de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) . Las aserciones de directiva siguientes se usan para identificar la [**\_ \_ versión de WS Trust**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) y las opciones asociadas.

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

La versión de confianza se puede especificar mediante [**la \_ \_ restricción de \_ \_ propiedad del \_ token de seguridad**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) de la solicitud de WS con un identificador de propiedad de la versión de confianza de la propiedad del token de seguridad de la [**\_ solicitud \_ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).

## <a name="ws_security_property_security_header_version"></a>\_versión del \_ \_ encabezado de \_ seguridad \_ de la propiedad WS Security

Esta sección se aplica cuando se usa cualquiera de las siguientes restricciones de enlace:

-   [**\_restricción de \_ \_ enlace de \_ seguridad de mensaje \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_restricción de \_ enlace de seguridad de mensaje \_ \_ de WS username \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_restricción de \_ enlace de seguridad de mensajes de certificado WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_restricción de \_ \_ enlace de seguridad de mensaje de token \_ emitido \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

La versión de seguridad del encabezado (especificada por la versión de encabezado de seguridad de la [**propiedad de WS \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) se determina mediante una de las siguientes aserciones de directiva:

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a>Restricciones con el diseño de seguridad de encabezado

Esta sección se aplica cuando se usa cualquiera de las siguientes restricciones de enlace:

-   [**\_restricción de \_ \_ enlace de \_ seguridad de mensaje \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_restricción de \_ enlace de seguridad de mensaje \_ \_ de WS username \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_restricción de \_ enlace de seguridad de mensajes de certificado WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_restricción de \_ \_ enlace de seguridad de mensaje de token \_ emitido \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

El diseño del encabezado de seguridad (tal y como se especifica en el diseño del encabezado de seguridad de la [**propiedad de WS \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) viene determinado por una de las siguientes aserciones de la Directiva:

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

-   [**\_restricción de \_ \_ enlace de \_ seguridad de mensaje \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_restricción de \_ enlace de seguridad de mensaje \_ \_ de WS username \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_restricción de \_ enlace de seguridad de mensajes de certificado WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_restricción de \_ \_ enlace de seguridad de mensaje de token \_ emitido \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

El hecho de que una marca de tiempo se incluya en el encabezado de seguridad (tal y como se especifica en el uso de la marca de tiempo de la [**propiedad de WS \_ Security \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) viene determinada por la presencia de SP: IncludeTimestamp en la siguiente ubicación:

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

Si la aserción SP: IncludeTimestamp está presente, el valor de la Directiva es el uso de la marca de tiempo de [**WS \_ Security \_ \_ \_ siempre**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

Si la aserción SP: IncludeTimestamp no está presente, el valor de la Directiva es el uso de la marca de tiempo de [**WS \_ Security \_ \_ \_ nunca**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

 

 




