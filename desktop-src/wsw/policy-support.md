---
title: Compatibilidad con directivas
description: Wsutil procesa la directiva especificada en los metadatos de entrada y genera rutinas auxiliares para la compatibilidad con el modelo de servicio.
ms.assetid: 9c4fb485-2392-4117-b4a7-7a51786d60b9
keywords:
- Servicios web de compatibilidad con directivas para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aafcd481fd4ea8a8cc6782a5dc50655fb9255c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571989"
---
# <a name="policy-support"></a>Compatibilidad con directivas

Wsutil procesa la directiva especificada en los metadatos de entrada y genera rutinas auxiliares para la compatibilidad con el modelo de servicio.

## <a name="how-to-use-policy-support-in-wsutil"></a>Uso de la compatibilidad con directivas en wsutil

Los desarrolladores deben seguir los pasos siguientes para usar la compatibilidad con directivas en el compilador wsutil:

-   Recopile todos los archivos de metadatos de entrada necesarios para el servicio web de destino.
-   Compile todos los archivos WSDL/XSD/policy recopilados mediante wsutil.exe. Wsutil genera un conjunto de archivos de código auxiliar y de encabezado para cada archivo WSDL y XSD de entrada.
-   Inspeccione el archivo de encabezado generado, todos los nombres de rutina del asistente de directivas se enumeran en la sección de comentarios al principio del archivo de encabezado.
-   Use la rutina auxiliar bindingName \_ CreateServiceProxy para crear el proxy de servicio.
-   Use la rutina auxiliar bindingName \_ CreateServiceEndpoint para crear el punto de conexión de servicio.
-   Rellene la estructura bindingTemplateType BINDING TEMPLATE de WS \_ especificada en la firma del \_ \_ método. Los desarrolladores pueden proporcionar propiedades de canal adicionales o propiedades de seguridad según sea necesario.
-   Llame a las rutinas auxiliares y, en caso correcto, se crea el proxy de servicio de devolución o el punto de conexión de servicio.

En las secciones siguientes se describen los temas relacionados en detalle.

## <a name="handle-policy-input"></a>Control de la entrada de directiva

Las siguientes son opciones [del compilador relacionadas](web-service-compiler-tool.md) con el procesamiento de directivas.

De forma predeterminada, wsutil siempre generará plantillas de directiva a menos que se llame con la opción "/nopolicy". La directiva se puede incrustar como parte de un archivo WSDL o se puede crear por separado como un archivo de metadatos de directiva que wsutil toma como entrada. La opción del compilador "/wsp:" se usa para indicar que los metadatos de entrada especificados son un archivo de directiva. Wsutil genera posibles asistentes relacionados con directivas con la siguiente compilación:

**wsutil /wsdl:trusted.wsdl /wsdl:trusted1.wsdl**

**wstuil /wsdl:input.wsdl /wsp:policy.wsp**

No se generan asistentes de directivas cuando se usa la opción "/nopolicy", como en el ejemplo siguiente.

**wsutil /nopolicy /wsdl:trusted.wsdl /wsdl:trusted1.wsdl**

## <a name="policy-related-code-generated-by-the-wsutil-compiler"></a>Código relacionado con directivas generado por el compilador wsutil

[La página Asignación de](metadata-mapping.md) metadatos detalla la asignación entre construcciones de metadatos con tipos de enlace diferentes.

Se pueden especificar tres categorías de configuración de directiva en la configuración de directiva:

-   Propiedades del canal. Actualmente solo se admiten las siguientes propiedades de canal: [**WS \_ CHANNEL PROPERTY \_ \_ ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id), **WS CHANNEL PROPERTY \_ \_ \_ ADDRESSING \_ VERSION** y **WS CHANNEL PROPERTY ENVELOPE \_ \_ \_ \_ VERSION**.
-   Propiedades de seguridad. Actualmente solo se admiten las siguientes propiedades de seguridad: [**WS \_ SECURITY PROPERTY TIMESTAMP \_ \_ \_ USAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id), **WS SECURITY PROPERTY SECURITY \_ \_ HEADER \_ \_ \_ LAYOUT**, **WS SECURITY PROPERTY TRANSPORT \_ PROTECTION \_ \_ \_ \_ LEVEL** y **WS SECURITY PROPERTY SECURITY \_ \_ HEADER \_ \_ \_ VERSION**.
-   Enlace de seguridad. Actualmente solo se admiten los siguientes enlaces de seguridad: [**WS \_ HTTP HEADER \_ \_ AUTH SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding), [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding), [**WS TCP \_ \_ SSPI TRANSPORT SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding), [**WS USERNAME MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding), [**WS KERBEROS \_ \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)y [**WS SECURITY CONTEXT MESSAGE \_ \_ SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).

Tipo de plantilla de enlace

Hay un número limitado de enlaces que se admiten en wsutil. Todas las combinaciones admitidas de estos enlaces se enumeran en [**WS BINDING TEMPLATE TYPE definition (Definición \_ de tipo de plantilla \_ \_ de WS BINDING).**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) Por ejemplo, para el siguiente enlace en wsdl

``` syntax
<soap:binding style="document" transport="http://schemas.xmlsoap.org/soap/http" />
```

Wsutil genera el tipo de plantilla de enlace [**WS \_ HTTP BINDING TEMPLATE \_ \_ \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) para este enlace.

Descripciones de directivas

Con la configuración de directiva de entrada, wsutil genera un conjunto de descripciones de directivas que describen la directiva de entrada, incluido el tipo de plantilla, así como los valores especificados en la directiva. Por ejemplo, para la entrada

``` syntax
<wsdl:binding...>
  <soap11:binding.../> =< WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

wsutil genera la descripción de la propiedad del canal como:

``` syntax
WS_ENVELOPE_VERSION_SOAP_1_1,
{
  WS_CHANNEL_PROPERTY_ENVELOPE_VERSION,
  (void*)&locaDefinitions.policies.bindHostedClientSoap.envelopeVersion, //points to the WS_ENVELOPE_VERSION_SOAP_1_1 value above
  sizeof(&localDefinitions.policies.bindHostedClientSoap.envelopeVersion),
},
```

Toda la configuración de directiva (propiedades de canal, propiedades de seguridad y propiedades de enlace de seguridad) de un enlace se agrega en una estructura WS \_ bindingTemplateType \_ POLICY \_ DESCRIPTION. [**WS \_ BINDING \_ TEMPLATE \_ TYPE especifica**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) las distintas combinaciones de directivas de enlace que admite wsutil.

Estructura de plantilla que va a rellenar la aplicación

La descripción de la directiva contiene toda la información de directiva especificada en los metadatos de entrada para un enlace determinado, pero hay información que no se puede representar en la directiva pero requiere la entrada del usuario al usar la configuración de esas directivas para crear un proxy de servicio o un punto de conexión de servicio. Por ejemplo, la aplicación debe proporcionar credenciales para la autenticación de encabezado HTTP.

La aplicación debe rellenar la estructura de plantilla, denominada WS bindingTemplateType BINDING TEMPLATE para cada tipo de plantilla de enlace diferente, definida \_ \_ en \_ webservices.h:

``` syntax
struct WS_bindingTemplateType_BINDING_TEMPLATE
{
  WS_CHANNEL_PROPERTIES channelProperties;
  WS_SECURITY_PROPERTIES securityProperties;
  possible_list_of_SECURITY_BINDING_TEMPLATEs;
  ...
};
```

La lista de plantillas de enlace de seguridad es opcional depende del enlace de seguridad coincidente. Por ejemplo, el campo [**\_ WS SSL \_ TRANSPORT SECURITY BINDING \_ \_ \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template) se presenta en [**WS \_ HTTP SSL BINDING \_ \_ \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) para que la aplicación proporcione información de enlace de seguridad relacionada con SSL, incluida la información de credenciales.

La aplicación debe rellenar todos los campos de esta estructura antes de llamar a las API de plantilla de servicios web. Es necesario rellenar propiedades de seguridad adicionales, así como propiedades de enlace de seguridad que no se pueden representar en la directiva, y las API de servicios web combinan los dos conjunto de propiedades en tiempo de ejecución. Los campos se pueden establecer en cero si no son aplicables. Por ejemplo, securityProperties se puede establecer en cero si no se necesitan propiedades de seguridad adicionales.

Rutinas auxiliares y declaración de descripción de directiva en archivos de encabezado

wsutil crea una rutina auxiliar para facilitar una mejor compatibilidad en el nivel de modelo de servicio, de modo que la aplicación pueda crear el proxy de servicio y el punto de conexión de servicio más fácilmente. La descripción de la directiva también se expone de forma que la aplicación pueda usarlas directamente. Una rutina de ayuda de CreateSerivceProxy tiene el siguiente aspecto:

``` syntax
HRESULT bindingName_CreateServiceProxy(
  __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
  __in const ULONG propertyCount,
  __in WS_constraintName_BINDING_TEMPLATE* templateValue,
  __deref_out WS_SERVICE_PROXY** serviceProxy,
  __in_opt WS_ERROR* error);
```

Se recomienda a los desarrolladores que usen esas rutinas auxiliares, aunque también pueden usar directamente la rutina en tiempo de ejecución subyacente proporcionada por webservices.dll. No se recomienda a los desarrolladores usar las descripciones de directivas directamente al programar mediante el nivel [de modelo de](service-model-layer-overview.md) servicio.

Las referencias de descripción de directiva también se generan en el encabezado para el usuario avanzado. Si los desarrolladores no usan funcionalidades del modelo de servicio, pueden usar directamente las descripciones de la directiva.

``` syntax
struct {
  ...
  struct {
    ...
    } contracts;
  struct {
    WS_bindingTemplateType_POLICY_DESCRIPTION bindingName;
    ...
    } policies;
  }
```

Prototipos de definición en archivos de código auxiliar

Se crea un único campo de estructura de descripción de directiva por enlace y sus descripciones auxiliares a las que se hace referencia internamente en la estructura del prototipo local. Las descripciones de directiva se generan en el archivo donde se genera [**WS \_ CONTRACT \_ DESCRIPTION.**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) Por lo general, los desarrolladores no necesitan inspeccionar el archivo de código auxiliar durante el desarrollo, aunque el archivo de código auxiliar contiene todos los detalles sobre las especificaciones de directiva.

``` syntax
struct {
  ...
  struct {
  ... } contracts;
  ...
 struct {
      struct {
        hierarchy of policy template descriptions;
        } bindingName;
      ...
      list of bindings in the input wsdl file.
  } policies;
} fileNameLocalDefinitions;
```

Implementación de rutinas auxiliares en los archivos de código auxiliar

Wsutil genera rutinas auxiliares para simplificar las llamadas de aplicación a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) y crear una base de punto de conexión de servicio de [**\_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) según la información proporcionada en la configuración de directiva.

Depende de las restricciones de enlace especificadas para el puerto especificado, el primer argumento es diferente según la estructura de la plantilla. En el ejemplo siguiente se supone que el transporte HTTP, la firma para la creación del proxy de servicio es similar con un parámetro de tipo de canal adicional.

``` syntax
HRESULT bindingName_CreateServiceProxy(
    __in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
    __in const ULONG propertyCount,
    __deref_out WS_SERVICE_PROXY** serviceProxy,
    __in_opt WS_ERROR* error)
{
    return WsCreateServiceProxyFromTemplate(
      WS_CHANNEL_TYPE_REQUEST,    // this is fixed for http, requires input for TCP
      properties,     
      propertyCount, 
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),  
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_constraintName_POLICY_DESCRIPTION),
      serviceProxy,     
      error);     
}
```

``` syntax
HRESULT bindingName_CreateServiceEndpoint(
__in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
__in_opt const WS_STRING* addressUrl,
__in bindingNameFunctionTable* functionTable,
__in WS_SERVICE_SECURITY_CALLBACK authorizationCallback,
__in const WS_SERVICE_ENDPOINT_PROPERTY* properties,
__in ULONG propertyCount,
__in WS_HEAP* heap,
  __deref_out WS_SERVICE_ENDPOINT** serviceEndpoint,
  __in_opt WS_ERROR* error)
{
  WS_SERVICE_CONTRACT serviceContract;
  serviceContract.contractDescription = &fileName.contracts.bindingName;
  serviceContract.defaultMessageHandlerCallback = NULL;
  serviceContract.methodTable = (const void *)functionTable;

  return WsCreateServiceEndpointFromTemplate(
      properties,
      propertyCount,
      addressUrl,    // service endpoint address
      WS_CHANNEL_TYPE_RESPONSE,    // this is fixed for http, requires input for TCP
      &serviceContract,
      authorizationCallback,
      heap,
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_bindingTemplateType_POLICY_DESCRIPTION),
      serviceEndpoint,
      error);
}
```

## <a name="supported-policy-settings"></a>Opciones de configuración de directiva compatibles

En la tabla siguiente se enumeran todos los tipos de plantilla de enlace admitidos, los enlaces de seguridad correspondientes necesarios en el tipo, la estructura de plantilla que va a rellenar la aplicación para el tipo y el tipo de descripción correspondiente. La aplicación debe rellenar la estructura de la plantilla, mientras que el desarrollador de aplicaciones debe comprender cuáles son los enlaces de seguridad necesarios en la directiva dada.



| [**TIPO DE PLANTILLA \_ DE \_ ENLACE DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                                | Combinaciones de enlace de seguridad                                                                                                                                                                                                                                                                                                               | estructura de plantilla que va a rellenar la aplicación                                                                                            | descripción de la directiva                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DE PLANTILLA \_ DE ENLACE HTTP \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                          |                                                                                                                                                                                                                                                                                                                                             | [**PLANTILLA DE ENLACE HTTP DE WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)                                                                              | [**DESCRIPCIÓN DE LA \_ DIRECTIVA HTTP \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)                                                                              |
| [**TIPO DE PLANTILLA \_ DE ENLACE HTTP SSL \_ \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**ENLACE DE \_ SEGURIDAD DE TRANSPORTE SSL \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)                                                                                                                                                                                                                                                          | [**PLANTILLA DE \_ ENLACE \_ HTTP SSL \_ DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)                                                                     | [**DESCRIPCIÓN DE LA \_ \_ DIRECTIVA SSL HTTP \_ DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)                                                                     |
| [**TIPO DE PLANTILLA \_ \_ DE ENLACE DE \_ AUTENTICACIÓN DE ENCABEZADO \_ \_ HTTP WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                            | [**ENLACE DE \_ SEGURIDAD DE AUTENTICACIÓN DE ENCABEZADO HTTP \_ \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                                                                                                                   | [**PLANTILLA DE ENLACE \_ DE AUTENTICACIÓN DE ENCABEZADO HTTP \_ \_ WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)                                                    | [**DESCRIPCIÓN DE LA \_ \_ DIRECTIVA DE \_ AUTENTICACIÓN DE ENCABEZADO \_ HTTP DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)                                                    |
| [**TIPO DE PLANTILLA \_ \_ DE ENLACE DE \_ \_ AUTENTICACIÓN DE ENCABEZADO \_ \_ SSL HTTP \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                       | [**WS \_ ENLACE DE \_ SEGURIDAD DE TRANSPORTE SSL \_ \_ y**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) ENLACE DE SEGURIDAD DE AUTENTICACIÓN DE ENCABEZADO [ **HTTP \_ \_ \_ WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                            | [**PLANTILLA DE ENLACE \_ \_ DE AUTENTICACIÓN DE ENCABEZADO SSL HTTP \_ \_ DE \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)                                           | [**DESCRIPCIÓN DE LA \_ \_ DIRECTIVA DE \_ AUTENTICACIÓN DE ENCABEZADO SSL HTTP \_ \_ \_ DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)                                           |
| [**TIPO DE PLANTILLA \_ DE ENLACE DE NOMBRE DE \_ \_ \_ USUARIO \_ SSL DE \_ WS HTTP**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ ENLACE DE \_ SEGURIDAD DE TRANSPORTE SSL \_ \_ Y**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) [ **ENLACE DE SEGURIDAD DE MENSAJES DE WS \_ USERNAME \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                             | [**PLANTILLA DE ENLACE DE NOMBRE DE USUARIO SSL DE WS \_ HTTP \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)                                                  | [**DESCRIPCIÓN DE LA \_ DIRECTIVA DE NOMBRE DE \_ USUARIO DE SSL DE \_ \_ WS HTTP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)                                                  |
| [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ ENLACE \_ DE SEGURIDAD DE TRANSPORTE SSL \_ \_ Y**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) [ **ENLACE DE SEGURIDAD DE \_ MENSAJES WS KERBEROS \_ \_ \_ \_ APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                                | [**PLANTILLA DE \_ ENLACE \_ WS HTTP SSL \_ KERBEROS \_ APREQ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)                                     | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)                                     |
| [**TIPO DE \_ PLANTILLA DE ENLACE TCP \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                           |                                                                                                                                                                                                                                                                                                                                             | [**PLANTILLA DE \_ ENLACE TCP \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)                                                                                | [**DESCRIPCIÓN DE \_ LA DIRECTIVA TCP \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)                                                                                |
| [**TIPO DE PLANTILLA DE ENLACE \_ \_ SSPI \_ DE \_ \_ WS TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**ENLACE DE SEGURIDAD DE TRANSPORTE DE WS \_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)                                                                                                                                                                                                                                               | [**PLANTILLA DE \_ ENLACE DE WS TCP \_ SSPI \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)                                                                     | [**DESCRIPCIÓN DE LA DIRECTIVA DE SSPI DE TCP \_ \_ WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)                                                                     |
| [**TIPO DE PLANTILLA DE ENLACE DE NOMBRE DE USUARIO DE WS \_ TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ ENLACE DE SEGURIDAD DE TRANSPORTE DE TCP \_ SSPI \_ \_ \_ Y**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) ENLACE DE SEGURIDAD DE MENSAJES DE [ **WS \_ USERNAME \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                  | [**PLANTILLA DE ENLACE DE NOMBRE DE USUARIO DE WS \_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)                                                  | [**DESCRIPCIÓN DE LA DIRECTIVA DE NOMBRE DE USUARIO DE WS \_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)                                                  |
| [**TIPO DE PLANTILLA DE ENLACE \_ \_ \_ \_ APREQ DE WS TCP \_ SSPI KERBEROS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ ENLACE DE SEGURIDAD DE TRANSPORTE DE TCP \_ SSPI \_ \_ \_ Y**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) [ **ENLACE DE SEGURIDAD DE \_ MENSAJES WS KERBEROS \_ \_ \_ \_ APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                     | [**PLANTILLA DE \_ ENLACE \_ \_ \_ APREQ DE KERBEROS DE \_ \_ WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)                                     | [**DESCRIPCIÓN DE \_ LA DIRECTIVA \_ DE \_ \_ APREQ DE WS \_ TCP SSPI KERBEROS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)                                     |
| [**TIPO DE PLANTILLA DE ENLACE DE CONTEXTO DE \_ \_ SEGURIDAD WS HTTP SSL \_ USERNAME \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ ENLACE DE SEGURIDAD DE TRANSPORTE SSL \_ \_ \_ y**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) [**WS \_ SECURITY CONTEXT MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con [**WS USERNAME MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) en el canal de arranque                         | [**PLANTILLA DE ENLACE \_ DE CONTEXTO DE SEGURIDAD DE NOMBRE DE \_ \_ \_ \_ USUARIO \_ \_ SSL DE WS HTTP**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)              | [**DESCRIPCIÓN DE LA \_ DIRECTIVA DE CONTEXTO DE SEGURIDAD DEL NOMBRE DE USUARIO SSL \_ \_ \_ \_ \_ \_ DE WS HTTP**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)              |
| [**TIPO DE PLANTILLA DE ENLACE DE CONTEXTO DE SEGURIDAD \_ WS HTTP \_ SSL KERBEROS \_ \_ APREQ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ ENLACE DE SEGURIDAD DE TRANSPORTE SSL \_ \_ \_ y**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) [**WS \_ SECURITY CONTEXT MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con [**WS KERBEROS \_ \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) en el canal de arranque            | [**PLANTILLA DE ENLACE DE CONTEXTO DE SEGURIDAD DE WS \_ HTTP \_ SSL KERBEROS \_ \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template) | [**DESCRIPCIÓN DE LA DIRECTIVA DE CONTEXTO DE SEGURIDAD DE WS \_ HTTP \_ SSL KERBEROS \_ \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description) |
| [**TIPO DE PLANTILLA DE ENLACE DE CONTEXTO DE SEGURIDAD DE NOMBRE DE USUARIO DE WS \_ TCP \_ SSPI \_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ ENLACE \_ DE SEGURIDAD DE TRANSPORTE \_ DE \_ \_ SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) TCP y ENLACE DE SEGURIDAD DE MENSAJES DE CONTEXTO DE SEGURIDAD [**de WS \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con [**WS USERNAME \_ MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) en el canal de arranque              | [**PLANTILLA DE ENLACE DE CONTEXTO DE SEGURIDAD DE NOMBRE DE USUARIO DE WS \_ TCP \_ SSPI \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)              | [**DESCRIPCIÓN DE LA DIRECTIVA DE CONTEXTO DE SEGURIDAD DEL NOMBRE DE USUARIO DE WS \_ TCP \_ SSPI \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)              |
| [**TIPO DE PLANTILLA DE ENLACE DE CONTEXTO DE SEGURIDAD \_ WS TCP \_ SSPI \_ KERBEROS \_ APREQ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ ENLACE \_ DE SEGURIDAD DE \_ TRANSPORTE \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) DE SSPI TCP y ENLACE DE SEGURIDAD DE MENSAJES DE CONTEXTO DE SEGURIDAD de WS con ENLACE DE SEGURIDAD DE MENSAJES [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) [**\_ \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) de WS KERBEROS en el canal de arranque | [**PLANTILLA DE ENLACE DE CONTEXTO DE SEGURIDAD DE WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template) | [**DESCRIPCIÓN DE LA DIRECTIVA DE CONTEXTO DE SEGURIDAD DE WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description) |



 

Por ejemplo, [**WS \_ HTTP SSL BINDING TEMPLATE \_ \_ \_ \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) indica que la directiva de entrada para el enlace especifica el transporte HTTP y [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). La aplicación debe rellenar la estructura [**WS \_ HTTP SSL BINDING \_ \_ \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) antes de llamar a las rutinas auxiliares y la descripción de la directiva correspondiente es [**WS HTTP SSL POLICY \_ \_ \_ \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description). En concreto, la sección de enlace de WSDL contiene los siguientes segmentos:

``` syntax
<wsp:Policy...>
  <sp:TransportBinding...>
    <wsp:Policy...>
      <sp:TransportToken...>
        <wsp:Policy...>
          <sp:HttpsToken.../>
        </wsp:Policy...>
      </sp:TransportToken...>
    </wsp:Policy>
  </sp:TransportBinding...>
</wsp:Policy>
```

``` syntax
<wsdl:binding...>
<soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

## <a name="security-context-support"></a>Compatibilidad con contexto de seguridad

En [contexto de seguridad](security-context.md), el canal de arranque se crea para establecer la conversación segura en el canal de servicio. Wsutil solo admite el escenario en el que el canal de arranque es el mismo que el canal de servicio, con las mismas propiedades de canal y propiedades de seguridad. La seguridad de transporte es necesaria para el enlace de mensajes de contexto de seguridad; wsutil admite canales de arranque con otros enlaces de seguridad de mensajes, pero solo admite el contexto de seguridad como único enlace de seguridad de mensajes en el canal de servicio, sin combinación con otros enlaces de seguridad de mensajes. Los desarrolladores pueden admitir esas combinaciones fuera de la compatibilidad con la plantilla de directiva.

La enumeración siguiente forma parte de la compatibilidad con directivas:

-   [**TIPO DE PLANTILLA \_ DE \_ ENLACE DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)

Las siguientes funciones forman parte de la compatibilidad con directivas:

-   [**WsCreateServiceEndpointFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceendpointfromtemplate)
-   [**WsCreateServiceProxyFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxyfromtemplate)

Las estructuras siguientes forman parte de la compatibilidad con directivas:

-   [**PLANTILLA DE ENLACE HTTP DE WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)
-   [**PLANTILLA DE ENLACE \_ DE AUTENTICACIÓN DE ENCABEZADO HTTP \_ \_ WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)
-   [**DESCRIPCIÓN DE LA \_ \_ DIRECTIVA DE \_ AUTENTICACIÓN DE ENCABEZADO \_ HTTP DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)
-   [**DESCRIPCIÓN DE LA \_ DIRECTIVA DE ENLACE DE SEGURIDAD DE \_ \_ \_ AUTENTICACIÓN \_ DE \_ \_ ENCABEZADO HTTP WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_policy_description)
-   [**PLANTILLA DE ENLACE \_ \_ DE SEGURIDAD DE \_ AUTENTICACIÓN DE \_ ENCABEZADO \_ \_ HTTP WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_template)
-   [**DESCRIPCIÓN DE LA \_ DIRECTIVA HTTP \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)
-   [**PLANTILLA DE ENLACE \_ \_ HTTP SSL \_ DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)
-   [**PLANTILLA DE ENLACE \_ \_ DE AUTENTICACIÓN DE ENCABEZADO SSL HTTP \_ \_ DE \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)
-   [**DESCRIPCIÓN DE LA \_ \_ DIRECTIVA DE \_ AUTENTICACIÓN DE ENCABEZADO SSL HTTP \_ \_ \_ DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)
-   [**PLANTILLA DE \_ ENLACE \_ WS HTTP SSL \_ KERBEROS \_ APREQ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)
-   [**PLANTILLA DE ENLACE DE CONTEXTO DE SEGURIDAD DE WS \_ HTTP \_ SSL KERBEROS \_ \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template)
-   [**DESCRIPCIÓN DE LA DIRECTIVA DE CONTEXTO DE SEGURIDAD DE WS \_ HTTP \_ SSL KERBEROS \_ \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description)
-   [**DESCRIPCIÓN DE LA \_ \_ DIRECTIVA SSL HTTP \_ DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)
-   [**PLANTILLA DE ENLACE DE NOMBRE DE USUARIO SSL DE WS \_ HTTP \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)
-   [**DESCRIPCIÓN DE LA \_ DIRECTIVA DE NOMBRE DE \_ USUARIO DE SSL DE \_ \_ WS HTTP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)
-   [**PLANTILLA DE ENLACE \_ DE CONTEXTO DE SEGURIDAD DE NOMBRE DE \_ \_ \_ \_ USUARIO \_ \_ SSL DE WS HTTP**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)
-   [**DESCRIPCIÓN DE LA \_ DIRECTIVA DE CONTEXTO DE SEGURIDAD DEL NOMBRE DE USUARIO SSL \_ \_ \_ \_ \_ \_ DE WS HTTP**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)
-   [**DESCRIPCIÓN DE LA DIRECTIVA DE ENLACE DE SEGURIDAD DE MENSAJES DE \_ WS KERBEROS \_ APREQ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_policy_description)
-   [**PLANTILLA DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE WS KERBEROS \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_template)
-   [**DESCRIPCIÓN DE LA \_ DIRECTIVA DE ENLACE DE SEGURIDAD DE MENSAJES DE CONTEXTO DE SEGURIDAD \_ \_ \_ \_ \_ \_ DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_policy_description)
-   [**PLANTILLA DE ENLACE \_ DE SEGURIDAD DE MENSAJES DE CONTEXTO DE \_ \_ \_ \_ \_ SEGURIDAD DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_template)
-   [**DESCRIPCIÓN DE LA \_ DIRECTIVA DE ENLACE DE SEGURIDAD DEL CONTEXTO DE SEGURIDAD \_ \_ \_ \_ \_ DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_policy_description)
-   [**PLANTILLA DE ENLACE \_ DE SEGURIDAD DEL CONTEXTO DE \_ \_ \_ SEGURIDAD DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_template)
-   [**DESCRIPCIÓN DE LA \_ DIRECTIVA DE ENLACE DE SEGURIDAD DE TRANSPORTE \_ \_ \_ \_ DE \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_policy_description)
-   [**PLANTILLA DE \_ ENLACE DE SEGURIDAD DE TRANSPORTE SSL WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template)
-   [**DESCRIPCIÓN DE LA \_ DIRECTIVA DE ENLACE DE SEGURIDAD DE TRANSPORTE \_ \_ \_ \_ DE \_ WS SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_sspi_transport_security_binding_policy_description)
-   [**PLANTILLA DE \_ ENLACE TCP \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)
-   [**DESCRIPCIÓN DE \_ LA DIRECTIVA TCP \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)
-   [**PLANTILLA DE \_ ENLACE DE WS TCP \_ SSPI \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)
-   [**PLANTILLA DE \_ ENLACE \_ \_ \_ APREQ DE KERBEROS DE \_ \_ WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)
-   [**DESCRIPCIÓN DE \_ LA DIRECTIVA \_ DE \_ \_ APREQ DE WS \_ TCP SSPI KERBEROS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)
-   [**PLANTILLA DE ENLACE DE CONTEXTO DE SEGURIDAD DE WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template)
-   [**DESCRIPCIÓN DE LA DIRECTIVA DE CONTEXTO DE SEGURIDAD DE WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description)
-   [**DESCRIPCIÓN DE LA DIRECTIVA DE SSPI DE TCP \_ \_ WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)
-   [**PLANTILLA DE ENLACE DE SEGURIDAD DE TRANSPORTE DE WS \_ TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_template)
-   [**PLANTILLA DE ENLACE DE NOMBRE DE USUARIO DE WS \_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)
-   [**DESCRIPCIÓN DE LA DIRECTIVA DE NOMBRE DE USUARIO DE WS \_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)
-   [**PLANTILLA DE ENLACE DE CONTEXTO DE SEGURIDAD DE NOMBRE DE USUARIO DE WS \_ TCP \_ SSPI \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)
-   [**DESCRIPCIÓN DE LA DIRECTIVA DE CONTEXTO DE SEGURIDAD DEL NOMBRE DE USUARIO DE WS \_ TCP \_ SSPI \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)
-   [**DESCRIPCIÓN DE LA \_ DIRECTIVA DE ENLACE DE SEGURIDAD DE MENSAJES DE \_ \_ \_ WS \_ USERNAME \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_policy_description)
-   [**PLANTILLA DE ENLACE \_ DE SEGURIDAD DE MENSAJES DE NOMBRE DE \_ \_ \_ USUARIO DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_template)

 

 




