---
title: Compatibilidad con directivas
description: Wsutil procesa la Directiva especificada en los metadatos de entrada y genera rutinas auxiliares para la compatibilidad con el modelo de servicio.
ms.assetid: 9c4fb485-2392-4117-b4a7-7a51786d60b9
keywords:
- Servicios Web de compatibilidad de directivas para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aafcd481fd4ea8a8cc6782a5dc50655fb9255c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357370"
---
# <a name="policy-support"></a>Compatibilidad con directivas

Wsutil procesa la Directiva especificada en los metadatos de entrada y genera rutinas auxiliares para la compatibilidad con el modelo de servicio.

## <a name="how-to-use-policy-support-in-wsutil"></a>Cómo usar la compatibilidad con directivas en wsutil

Los desarrolladores deben seguir los pasos siguientes para usar la compatibilidad de la Directiva en el compilador wsutil:

-   Recopile todos los archivos de metadatos de entrada necesarios para el servicio Web de destino.
-   Compile todos los archivos WSDL/XSD/Policy recopilados mediante wsutil.exe. Wsutil genera un conjunto de archivos de código auxiliar y un archivo de encabezado para cada archivo WSDL y XSD de entrada.
-   Inspeccione el archivo de encabezado generado, todos los nombres de rutina de la aplicación auxiliar de Directiva se enumeran en la sección de comentarios al principio del archivo de encabezado.
-   Use la \_ rutina auxiliar bindingName CreateServiceProxy para crear el proxy de servicio.
-   Use la \_ rutina auxiliar bindingName CreateServiceEndpoint para crear el punto de conexión de servicio.
-   Rellene \_ \_ la estructura de plantilla de enlace WS bindingTemplateType \_ especificada en la Signatura del método. Los desarrolladores pueden proporcionar propiedades de canal adicionales y/o propiedades de seguridad según sea necesario.
-   Llame a las rutinas auxiliares, en el proxy de servicio de devolución correcto o en el extremo de servicio creado.

En las secciones siguientes se describen los temas relacionados en detalle.

## <a name="handle-policy-input"></a>Controlar entrada de Directiva

Las siguientes son [Opciones del compilador](web-service-compiler-tool.md) relacionadas con el procesamiento de directivas.

De forma predeterminada, wsutil siempre generará plantillas de directiva a menos que se llame con la opción "/nopolicy". La Directiva se puede incrustar como parte de un archivo WSDL o se puede crear por separado como un archivo de metadatos de directiva que wsutil toma como entrada. La opción del compilador "/WSP:" se usa para indicar que los metadatos de entrada especificados son un archivo de directiva. Wsutil genera posibles aplicaciones auxiliares relacionadas con la Directiva con la siguiente compilación:

**wsutil/WSDL: Trusted. wsdl/WSDL: trusted1. wsdl**

**wstuil/WSDL: Input. wsdl/WSP: Policy. wsp**

No se generan aplicaciones auxiliares de directivas cuando se usa la opción "/nopolicy" como en el ejemplo siguiente.

**wsutil/nopolicy/WSDL: Trusted. wsdl/WSDL: trusted1. wsdl**

## <a name="policy-related-code-generated-by-the-wsutil-compiler"></a>Código relacionado con la Directiva generado por el compilador wsutil

La página de [asignación de metadatos](metadata-mapping.md) detalla la asignación entre construcciones de metadatos con distintos tipos de enlaces.

Se pueden especificar tres categorías de configuración de directiva en la configuración de la Directiva:

-   Propiedades del canal. Actualmente solo se admiten las siguientes propiedades de canal: [**codificación de propiedades de canal de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id), **versión de direccionamiento de \_ \_ propiedades \_ \_ de canal** de WS y versión de **sobre de propiedades de canal de WS \_ \_ \_ \_**.
-   Propiedades de seguridad. Actualmente solo se admiten las siguientes propiedades de seguridad: el uso de la marca de tiempo de la propiedad [**WS \_ Security \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id), el diseño del encabezado de seguridad de la **\_ \_ propiedad \_ \_ \_ WS Security**, el **\_ \_ \_ \_ \_ nivel de protección de propiedades WS Security** y la **\_ propiedad WS Security \_ \_ \_ \_**.
-   Enlace de seguridad. Actualmente solo se admiten los siguientes enlaces de seguridad: el [**enlace de seguridad de \_ autenticación de \_ encabezado \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding), enlace de [**seguridad de \_ transporte WS SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding), enlace de seguridad de [**\_ \_ \_ transporte SSPI \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)de WS TCP, enlace de seguridad de [**mensaje de WS \_ username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding), enlace de seguridad de [**\_ mensajes WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)y enlace de [**seguridad de mensaje de contexto de WS- \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).

Tipo de plantilla de enlace

Hay un número limitado de enlaces que se admiten en wsutil. Todas las combinaciones admitidas de estos enlaces se muestran en la definición de [**\_ tipo de \_ plantilla \_ de enlace WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) . Por ejemplo, para el siguiente enlace en WSDL

``` syntax
<soap:binding style="document" transport="http://schemas.xmlsoap.org/soap/http" />
```

Wsutil genera el tipo de plantilla de enlace de [**\_ tipo de \_ \_ plantilla \_ de enlace http WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) para este enlace.

Descripciones de Directiva

Con la configuración de la Directiva de entrada, wsutil genera un conjunto de descripciones de directiva que describen la Directiva de entrada, incluido el tipo de plantilla, así como los valores especificados en la Directiva. Por ejemplo, para la entrada

``` syntax
<wsdl:binding...>
  <soap11:binding.../> =< WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

wsutil genera una descripción de la propiedad de canal como:

``` syntax
WS_ENVELOPE_VERSION_SOAP_1_1,
{
  WS_CHANNEL_PROPERTY_ENVELOPE_VERSION,
  (void*)&locaDefinitions.policies.bindHostedClientSoap.envelopeVersion, //points to the WS_ENVELOPE_VERSION_SOAP_1_1 value above
  sizeof(&localDefinitions.policies.bindHostedClientSoap.envelopeVersion),
},
```

Todas las configuraciones de directiva (propiedades de canal, propiedades de seguridad y propiedades de enlace de seguridad) de un enlace se agregan a una estructura de descripción de directiva de WS \_ bindingTemplateType \_ \_ . [**WS \_ \_ \_ Tipo de plantilla de enlace**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) especifica las distintas combinaciones de directivas de enlace que wsutil admite.

Estructura de plantilla que va a rellenar la aplicación

La descripción de la Directiva contiene toda la información de la Directiva especificada en los metadatos de entrada de un enlace determinado, pero hay información que no se puede representar en la Directiva, pero que requiere la intervención del usuario al usar esas directivas para crear el proxy de servicio o el punto de conexión de servicio. Por ejemplo, la aplicación debe proporcionar credenciales para la autenticación del encabezado HTTP.

La aplicación debe rellenar la estructura de plantilla, denominada \_ \_ plantilla de enlace WS bindingTemplateType \_ para cada tipo de plantilla de enlace diferente, definido en webservices. h:

``` syntax
struct WS_bindingTemplateType_BINDING_TEMPLATE
{
  WS_CHANNEL_PROPERTIES channelProperties;
  WS_SECURITY_PROPERTIES securityProperties;
  possible_list_of_SECURITY_BINDING_TEMPLATEs;
  ...
};
```

La lista de plantillas de enlace de seguridad es opcional depende del enlace de seguridad coincidente. Por ejemplo, el campo de [**plantilla de enlace de \_ \_ seguridad de transporte \_ \_ \_ SSL de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template) se presenta en la [**\_ \_ \_ \_ plantilla de enlace SSL de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) para que la aplicación proporcione información de enlace de seguridad relacionada con SSL, incluida la información de credenciales.

La aplicación debe rellenar todos los campos de esta estructura antes de llamar a las API de plantilla de WebService. Las propiedades de seguridad adicionales, así como las propiedades de enlace de seguridad que no se pueden representar en la Directiva deben rellenarse, y las API de webservices combinan los dos conjuntos de propiedades en tiempo de ejecución. Los campos se pueden establecer como ceros si no se aplican. Por ejemplo, securityProperties se puede establecer como cero si no se necesitan propiedades de seguridad adicionales.

Rutinas auxiliares y declaración de descripción de directivas en archivos de encabezado

wsutil crea una rutina auxiliar para facilitar una mejor compatibilidad en el nivel de modelo de servicio, de modo que la aplicación pueda crear un proxy de servicio y un punto de conexión de servicio más fácil. La descripción de la Directiva también se expone de forma que la aplicación pueda usarlas directamente. Una rutina de ayuda de CreateSerivceProxy tiene el siguiente aspecto:

``` syntax
HRESULT bindingName_CreateServiceProxy(
  __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
  __in const ULONG propertyCount,
  __in WS_constraintName_BINDING_TEMPLATE* templateValue,
  __deref_out WS_SERVICE_PROXY** serviceProxy,
  __in_opt WS_ERROR* error);
```

Se recomienda a los desarrolladores que utilicen esas rutinas auxiliares, aunque también pueden usar directamente la rutina en tiempo de ejecución que proporciona webservices.dll. No se recomienda a los desarrolladores usar las descripciones de la Directiva directamente al programar con el nivel de [modelo de servicio](service-model-layer-overview.md) .

Las referencias de la descripción de la Directiva también se generan en el encabezado para usuario avanzado. Si los desarrolladores no usan las funcionalidades del modelo de servicio, pueden usar las descripciones de la Directiva directamente.

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

Prototipos de definición en archivos stub

En la estructura del prototipo local se crea un campo de estructura de descripción de una sola directiva por enlace y sus descripciones de la aplicación auxiliar a las que se hace referencia internamente. Las descripciones de la Directiva se generan en el archivo donde se genera la [**\_ \_ Descripción del contrato de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) . Por lo general, los desarrolladores no necesitan inspeccionar el archivo de código auxiliar durante el desarrollo, aunque el archivo de código auxiliar contiene todos los detalles sobre las especificaciones de la Directiva.

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

Implementación de rutinas auxiliares en los archivos stub

Wsutil genera rutinas auxiliares para simplificar las llamadas a la aplicación a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) y crear la base del [**punto de \_ \_ conexión del servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) en la información proporcionada en la configuración de la Directiva.

Depende de las restricciones de enlace especificadas para el puerto determinado, el primer argumento es diferente según la estructura de la plantilla. En el ejemplo siguiente se da por supuesto el transporte HTTP, la firma para la creación de proxy de servicio es similar con un parámetro de tipo de canal adicional.

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

En la tabla siguiente se enumeran todos los tipos de plantilla de enlace admitidos, los enlaces de seguridad de coincidencia necesarios en el tipo, la estructura de plantilla que va a rellenar la aplicación para el tipo y el tipo de Descripción coincidente. La aplicación debe rellenar la estructura de la plantilla, mientras que el desarrollador de la aplicación debe comprender cuáles son los enlaces de seguridad necesarios en la Directiva especificada.



| [**\_tipo de \_ plantilla de enlace de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                                | Combinaciones de enlace de seguridad                                                                                                                                                                                                                                                                                                               | estructura de plantilla que va a rellenar la aplicación                                                                                            | Descripción de la Directiva                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo de \_ plantilla de enlace http \_ de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                          |                                                                                                                                                                                                                                                                                                                                             | [**\_plantilla de \_ enlace \_ http de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)                                                                              | [**Descripción de la \_ Directiva http de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)                                                                              |
| [**\_tipo de \_ \_ plantilla de enlace SSL http \_ de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**\_enlace de \_ seguridad de transporte WS SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)                                                                                                                                                                                                                                                          | [**\_plantilla de \_ \_ enlace SSL \_ de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)                                                                     | [**\_Descripción de \_ la \_ directiva \_ SSL de http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)                                                                     |
| [**\_tipo de \_ \_ plantilla de enlace de autenticación de encabezado \_ http \_ de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                            | [**\_enlace de \_ \_ seguridad de autenticación de encabezado HTTP \_ de \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                                                                                                                   | [**\_plantilla de \_ \_ enlace de autenticación de encabezado HTTP \_ de \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)                                                    | [**Descripción de la \_ Directiva de autenticación de encabezado HTTP de WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)                                                    |
| [**\_tipo de \_ \_ plantilla de \_ enlace de autenticación de encabezado SSL \_ \_ http de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                       | [**WS \_ Enlace \_ de \_ seguridad \_ de transporte SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) y [ **enlace de seguridad de \_ autenticación de \_ encabezado \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                            | [**\_plantilla de \_ \_ enlace de \_ autenticación de encabezado SSL \_ http \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)                                           | [**Descripción de la \_ Directiva de autenticación de \_ encabezado SSL http \_ \_ \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)                                           |
| [**\_tipo de \_ \_ plantilla de enlace de nombre de usuario SSL \_ \_ \_ de WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ Enlace \_ de \_ seguridad \_ de transporte SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) y [ **enlace de seguridad de \_ \_ mensajes \_ \_ WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                             | [**\_plantilla de \_ \_ enlace de nombre de usuario SSL \_ \_ de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)                                                  | [**Descripción de la \_ \_ Directiva de nombre de usuario SSL de http de WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)                                                  |
| [**\_tipo de \_ \_ plantilla de \_ \_ enlace APREQ \_ SSL de Kerberos \_ de WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ Enlace \_ de \_ seguridad \_ de transporte SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) y [ **enlace de seguridad de \_ mensajes WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                                | [**\_plantilla de \_ \_ \_ enlace APREQ de Kerberos SSL \_ \_ de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)                                     | [**\_Descripción de \_ la \_ \_ Directiva APREQ \_ de Kerberos SSL \_ de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)                                     |
| [**\_tipo de \_ plantilla de enlace TCP \_ de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                           |                                                                                                                                                                                                                                                                                                                                             | [**plantilla de enlace de WS \_ TCP \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)                                                                                | [**Descripción de la \_ Directiva WS TCP \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)                                                                                |
| [**\_tipo de \_ \_ plantilla de enlace SSPI \_ \_ de WS TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**\_enlace de \_ \_ seguridad de transporte SSPI \_ \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)                                                                                                                                                                                                                                               | [**\_plantilla de \_ \_ enlace SSPI \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)                                                                     | [**\_Descripción de \_ la \_ directiva \_ SSPI de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)                                                                     |
| [**\_tipo de \_ \_ plantilla de enlace de nombre de usuario SSPI \_ \_ \_ de WS TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ Enlace \_ de \_ \_ seguridad de \_ transporte de TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) y [ **\_ \_ \_ \_ enlace de seguridad de mensaje de WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                  | [**\_plantilla de \_ \_ enlace de nombre de usuario SSPI \_ \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)                                                  | [**Descripción de la \_ \_ Directiva de nombre de \_ usuario SSPI \_ \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)                                                  |
| [**\_tipo de \_ \_ plantilla de \_ enlace APREQ de Kerberos \_ SSPI \_ de WS \_ TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ Enlace \_ de \_ \_ seguridad de \_ transporte de TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) y [ **\_ \_ \_ \_ \_ enlace de seguridad de mensajes WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                     | [**\_plantilla de \_ \_ \_ enlace APREQ de Kerberos SSPI \_ \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)                                     | [**\_Descripción de \_ la \_ \_ Directiva APREQ \_ de Kerberos SSPI \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)                                     |
| [**\_tipo de \_ \_ plantilla de \_ \_ enlace de contexto de seguridad \_ de \_ nombre \_ de usuario SSL de WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ Enlace \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) de seguridad de transporte de SSL y enlace de seguridad de [**mensaje de contexto de WS \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con el [**enlace de seguridad de mensaje de WS \_ username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) en el canal de bootstrap                         | [**\_plantilla de \_ \_ enlace de \_ contexto de seguridad de nombre de usuario SSL \_ \_ \_ de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)              | [**Descripción de la \_ \_ Directiva de \_ contexto de \_ seguridad \_ \_ SSL \_ de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)              |
| [**\_tipo de \_ \_ plantilla de \_ \_ enlace de \_ contexto de seguridad \_ \_ APREQ \_ de Kerberos SSL de WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ Enlace \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) de seguridad de transporte de SSL y enlace de [**seguridad de mensaje de contexto de WS \_ seguridad \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con [**WS \_ Kerberos \_ APREQ \_ \_ \_ enlace**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) de seguridad de mensajes en el canal de bootstrap            | [**\_plantilla de \_ \_ enlace de \_ \_ contexto de seguridad APREQ \_ \_ de Kerberos \_ SSL de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template) | [**Descripción de la \_ \_ Directiva de \_ \_ \_ contexto de seguridad APREQ \_ \_ de Kerberos \_ SSL de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description) |
| [**\_tipo de \_ \_ plantilla de \_ \_ enlace de contexto de seguridad \_ del \_ nombre \_ de usuario SSPI de WS TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ Enlace de seguridad de transporte de TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) y enlace de seguridad de [**mensaje de contexto de WS \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con el enlace de seguridad de [**mensaje de WS \_ username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) en el canal de bootstrap              | [**\_plantilla de \_ \_ enlace de \_ contexto de seguridad de nombre de usuario SSPI \_ \_ \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)              | [**Descripción de la Directiva de contexto de seguridad de WS \_ TCP \_ SSPI \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)              |
| [**\_tipo de \_ \_ plantilla de \_ \_ enlace de \_ contexto de seguridad \_ \_ APREQ \_ de Kerberos SSPI de WS TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ Enlace de seguridad de transporte de TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) y enlace de [**seguridad de mensaje de contexto de WS \_ \_ \_ \_ \_ Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con el enlace de [**\_ seguridad de mensaje WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) en el canal de bootstrap | [**\_plantilla de \_ \_ enlace de \_ \_ contexto de seguridad APREQ \_ \_ de Kerberos \_ SSPI de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template) | [**Descripción de la \_ \_ Directiva de \_ \_ \_ contexto de seguridad APREQ \_ \_ de Kerberos \_ SSPI de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description) |



 

Por ejemplo, [**el \_ \_ tipo de \_ \_ plantilla de \_ enlace SSL http de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) indica que la Directiva de entrada para el enlace especifica el transporte http y el [**\_ \_ \_ \_ enlace de seguridad de transporte WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). La aplicación debe rellenar la estructura de [**\_ \_ \_ \_ plantilla de enlace SSL http de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) antes de llamar a las rutinas auxiliares y la descripción de la Directiva de coincidencia es [**WS \_ http \_ SSL \_ \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description). Más concretamente, la sección de enlace de WSDL contiene los siguientes segmentos:

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

## <a name="security-context-support"></a>Compatibilidad con el contexto de seguridad

En el [contexto de seguridad](security-context.md), el canal de arranque se crea para establecer la conversación segura en el canal de servicio. Wsutil solo admite el escenario en el que el canal de arranque es el mismo que el canal de servicio, con las mismas propiedades de canal y propiedades de seguridad. La seguridad de transporte es necesaria para el enlace de mensajes de contexto de seguridad; wsutil admite canales de arranque con otros enlaces de seguridad de mensajes, pero solo admite el contexto de seguridad como único enlace de seguridad de mensaje en el canal de servicio, sin combinación con otros enlaces de seguridad de mensajes. Los desarrolladores pueden admitir esas combinaciones fuera de la compatibilidad con plantillas de directiva.

La siguiente enumeración forma parte de la compatibilidad con directivas:

-   [**\_tipo de \_ plantilla de enlace de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)

Las siguientes funciones forman parte de la compatibilidad con directivas:

-   [**WsCreateServiceEndpointFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceendpointfromtemplate)
-   [**WsCreateServiceProxyFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxyfromtemplate)

Las siguientes estructuras forman parte de la compatibilidad con directivas:

-   [**\_plantilla de \_ enlace \_ http de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)
-   [**\_plantilla de \_ \_ enlace de autenticación de encabezado HTTP \_ de \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)
-   [**Descripción de la \_ Directiva de autenticación de encabezado HTTP de WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)
-   [**\_Descripción de \_ \_ Directiva de \_ enlace de seguridad de autenticación de \_ \_ encabezado HTTP \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_policy_description)
-   [**\_plantilla de \_ \_ enlace de seguridad de autenticación de encabezado \_ http \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_template)
-   [**Descripción de la \_ Directiva http de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)
-   [**\_plantilla de \_ \_ enlace SSL \_ de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)
-   [**\_plantilla de \_ \_ enlace de \_ autenticación de encabezado SSL \_ http \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)
-   [**Descripción de la \_ Directiva de autenticación de \_ encabezado SSL http \_ \_ \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)
-   [**\_plantilla de \_ \_ \_ enlace APREQ de Kerberos SSL \_ \_ de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)
-   [**\_Descripción de \_ la \_ \_ Directiva APREQ \_ de Kerberos SSL \_ de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)
-   [**\_plantilla de \_ \_ enlace de \_ \_ contexto de seguridad APREQ \_ \_ de Kerberos \_ SSL de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template)
-   [**Descripción de la \_ \_ Directiva de \_ \_ \_ contexto de seguridad APREQ \_ \_ de Kerberos \_ SSL de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description)
-   [**\_Descripción de \_ la \_ directiva \_ SSL de http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)
-   [**\_plantilla de \_ \_ enlace de nombre de usuario SSL \_ \_ de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)
-   [**Descripción de la \_ \_ Directiva de nombre de usuario SSL de http de WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)
-   [**\_plantilla de \_ \_ enlace de \_ contexto de seguridad de nombre de usuario SSL \_ \_ \_ de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)
-   [**Descripción de la \_ \_ Directiva de \_ contexto de \_ seguridad \_ \_ SSL \_ de WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)
-   [**Descripción de la \_ Directiva de enlace de seguridad de mensaje WS Kerberos \_ APREQ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_policy_description)
-   [**\_plantilla de \_ \_ enlace de \_ seguridad de mensajes \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_template)
-   [**Descripción de la Directiva de enlace de seguridad de mensaje de contexto de WS \_ Security \_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_policy_description)
-   [**\_plantilla de \_ \_ enlace de seguridad de mensaje de contexto \_ de \_ WS Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_template)
-   [**Descripción de la Directiva de enlace de seguridad del contexto de WS \_ Security \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_policy_description)
-   [**\_plantilla de \_ enlace de seguridad del contexto \_ \_ de WS Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_template)
-   [**Descripción de la \_ Directiva de enlace de seguridad de transporte WS SSL \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_policy_description)
-   [**\_plantilla de \_ enlace de seguridad de transporte WS SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template)
-   [**Descripción de la \_ Directiva de enlace de seguridad de transporte SSPI de WS \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_sspi_transport_security_binding_policy_description)
-   [**plantilla de enlace de WS \_ TCP \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)
-   [**Descripción de la \_ Directiva WS TCP \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)
-   [**\_plantilla de \_ \_ enlace SSPI \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)
-   [**\_plantilla de \_ \_ \_ enlace APREQ de Kerberos SSPI \_ \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)
-   [**\_Descripción de \_ la \_ \_ Directiva APREQ \_ de Kerberos SSPI \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)
-   [**\_plantilla de \_ \_ enlace de \_ \_ contexto de seguridad APREQ \_ \_ de Kerberos \_ SSPI de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template)
-   [**Descripción de la \_ \_ Directiva de \_ \_ \_ contexto de seguridad APREQ \_ \_ de Kerberos \_ SSPI de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description)
-   [**\_Descripción de \_ la \_ directiva \_ SSPI de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)
-   [**\_plantilla de \_ \_ enlace de seguridad de transporte SSPI \_ \_ de WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_template)
-   [**\_plantilla de \_ \_ enlace de nombre de usuario SSPI \_ \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)
-   [**Descripción de la \_ \_ Directiva de nombre de \_ usuario SSPI \_ \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)
-   [**\_plantilla de \_ \_ enlace de \_ contexto de seguridad de nombre de usuario SSPI \_ \_ \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)
-   [**Descripción de la Directiva de contexto de seguridad de WS \_ TCP \_ SSPI \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)
-   [**Descripción de la Directiva de enlace de seguridad de mensaje de WS \_ username \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_policy_description)
-   [**\_plantilla de \_ enlace de seguridad de mensaje \_ \_ de WS username \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_template)

 

 




