---
title: Proxy de servicio
description: Un proxy de servicio es el proxy de cliente para un servicio.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Servicios Web de proxy de servicio para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac82509fa155084cbb4ca3e6b9437728c6f853a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "105689616"
---
# <a name="service-proxy"></a>Proxy de servicio

Un proxy de servicio es el proxy de cliente para un servicio. El proxy de servicio permite a las aplicaciones enviar y recibir [mensajes](message.md) a través de un [canal](channel.md) como llamadas a métodos.

Los proxies de servicio se crean según sea necesario, se abren, se usan para llamar a un servicio y se cierran cuando ya no se necesitan. Como alternativa, una aplicación puede volver a usar un proxy de servicio para conectarse repetidamente al mismo servicio sin el tiempo y los recursos necesarios para inicializar un proxy de servicio más de una vez. En el diagrama siguiente se ilustra el flujo de los posibles estados del proxy de servicio y las llamadas de función o eventos que conducen de un estado a otro.

![Diagrama que muestra los Estados de proxy de servicio y las llamadas de función o eventos que conducen de un estado a otro.](images/serviceproxystates.png)

Estos Estados de proxy de servicio se enumeran en la enumeración de [**Estado de proxy de servicio de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .

Como se muestra en el diagrama anterior y en el código siguiente, se crea un proxy de servicio mediante una llamada a la función [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) . Como parámetros para esta llamada, WWSAPI proporciona las siguientes enumeraciones:

-   [**\_tipo de canal de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [**\_enlace de canal de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

También acepta parámetros opcionales mediante los siguientes tipos de datos:

-   [**identificador de la propiedad de proxy de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [**Descripción de WS \_ Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

Una vez creado el proxy de servicio, la función **WsCreateServiceProxy** devuelve una referencia al proxy de servicio, [el \_ \_ proxy de servicio WS](ws-service-proxy.md), a través de un parámetro de salida.

``` syntax
WS_SERVICE_PROXY* serviceProxy = NULL;
hr = WsCreateServiceProxy (
    WS_TCP_CHANNEL_BINDING, 
    WS_CHANNEL_TYPE_DUPLEX_SESSION, 
    NULL, 
    NULL, 
    0, 
    NULL,
    0,
    &serviceProxy, 
    error);
```

Cuando se ha creado el proxy de servicio, la aplicación puede abrir el proxy de servicio para la comunicación con un servicio llamando a la función [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) , pasando una estructura de [**direcciones**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) que contiene la dirección de red del extremo de servicio al que se va a conectar.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

Cuando se ha abierto el proxy del servicio, la aplicación puede utilizarlo para realizar llamadas al servicio.

``` syntax
hr = Add(
    serviceProxy, 
    1, 
    2, 
    &result, 
    NULL, 
    0, 
    NULL, 
    error);
```

Cuando la aplicación ya no necesita el proxy del servicio, cierra el proxy del servicio mediante una llamada a la función [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) . También libera la memoria asociada mediante una llamada a [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).

``` syntax
hr = WsCloseServiceProxy(
    serviceProxy, 
    NULL, 
    error);
```

``` syntax
hr = WsFreeServiceProxy(
    serviceProxy, 
    error);
```

## <a name="reusing-the-service-proxy"></a>Reutilización del proxy de servicio

Como alternativa, después de llamar a [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) , una aplicación puede volver a usar el proxy de servicio mediante una llamada a la función [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) .

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

Para obtener más información sobre cómo se usan los proxies de servicio en distintos contextos, vea los temas siguientes:

-   [Proxy de servicio y sesiones](service-proxy-and-sessions.md)
-   [Operación de servicio](service-operation.md)
-   [Operaciones de servicio del lado cliente](client-side-service-operations.md)
-   [HttpCalculatorClientExample](httpcalculatorclientexample.md)

### <a name="security"></a>Seguridad

Las siguientes consideraciones sobre el diseño de la aplicación se deben anotar cuidadosamente al usar la API del proxy del servicio WWSAPI:

-   El proxy de servicio no llevará a cabo ninguna validación de los datos más allá de la validación básica del perfil 2,0 y la serialización XML. Es responsabilidad de la aplicación validar los datos contenidos en los parámetros que recibe como parte de la llamada.
-   Al configurar el número máximo de llamadas pendientes en el proxy de servicio, se usa el valor de enumeración [**\_ \_ \_ ID. de propiedad del proxy WS**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) valor de enumeración de **WS \_ proxy \_ propiedad número de \_ \_ \_ llamadas pendientes**, que proporciona protección contra un servidor de ejecución lenta. El valor máximo predeterminado es 100. Las aplicaciones deben tener cuidado al modificar los valores predeterminados.
-   El proxy de servicio no proporciona ninguna garantía de seguridad más allá de las especificadas en la estructura de [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) usada para comunicarse con el servidor.
-   Tenga cuidado al modificar los valores predeterminados de [mensajes](message.md) y [canales](channel.md) en el proxy de servicio. Lea las consideraciones de seguridad asociadas a los mensajes y canales antes de modificar cualquiera de las propiedades relacionadas.
-   El proxy del servicio cifra todas las credenciales que mantiene en la memoria.

Los siguientes elementos de la API se relacionan con los proxies de servicio.

| Devolución de llamada                                                          | Descripción                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**\_devolución de \_ llamada de mensaje de proxy WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | Se invoca cuando los encabezados del mensaje de entrada están a punto de enviarse a través de o cuando se reciben los encabezados de un mensaje de salida. |



 



| Enumeración                                                 | Descripción                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**identificador de la \_ propiedad de llamada WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | Enumera los parámetros opcionales para configurar una llamada en una operación de servicio del lado cliente. |
| [**identificador de la propiedad de proxy de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | Enumera los parámetros opcionales para configurar el proxy de servicio.                         |
| [**\_Estado del \_ proxy de servicio WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | El estado del proxy de servicio.                                                           |



 



| Función                                                       | Descripción                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | Abandona una llamada especificada en un proxy de servicio especificado.                           |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | Cancela todas las entradas y salidas pendientes en un proxy de servicio especificado.                |
| [**WsCall**](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | Solo interno. Serializa los argumentos en un mensaje y lo envía a través del canal. |
| [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | Cierra un proxy de servicio para la comunicación.                                         |
| [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | Crea un proxy de servicio.                                                          |
| [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | Libera la memoria asociada a un proxy de servicio.                              |
| [**WsGetServiceProxyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | Recupera una propiedad de proxy de servicio especificada.                                     |
| [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | Abre un proxy de servicio en un punto de conexión de servicio.                                      |
| [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | Restablece el proxy del servicio.                                                             |



 



| Handle                                     | Descripción                                       |
|--------------------------------------------|---------------------------------------------------|
| [\_proxy de servicio WS \_](ws-service-proxy.md) | Tipo opaco que se usa para hacer referencia a un proxy de servicio. |



 



| Estructura                                         | Descripción                 |
|---------------------------------------------------|-----------------------------|
| [**\_propiedad de llamada WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | Especifica una propiedad de llamada.  |
| [**WS \_ \_propiedad de proxy**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property). | Especifica una propiedad de proxy. |



 

 

 




