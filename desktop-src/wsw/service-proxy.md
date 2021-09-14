---
title: Proxy de servicio
description: Un proxy de servicio es el proxy del lado cliente para un servicio.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Servicios web de proxy de servicio para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac82509fa155084cbb4ca3e6b9437728c6f853a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261972"
---
# <a name="service-proxy"></a>Proxy de servicio

Un proxy de servicio es el proxy del lado cliente para un servicio. El proxy de servicio permite a las aplicaciones enviar y recibir [mensajes](message.md) a través de [un canal como](channel.md) llamadas de método.

Los servidores proxy de servicio se crean según sea necesario, se abren, se usan para llamar a un servicio y se cierran cuando ya no son necesarios. Como alternativa, una aplicación puede reutilizar un proxy de servicio para conectarse repetidamente al mismo servicio sin el gasto de tiempo y los recursos necesarios para inicializar un proxy de servicio más de una vez. En el diagrama siguiente se muestra el flujo de los posibles estados del proxy de servicio y las llamadas de función o los eventos que conducen de un estado a otro.

![Diagrama que muestra los estados del proxy de servicio y las llamadas de función o eventos que conducen de un estado a otro.](images/serviceproxystates.png)

Estos estados de proxy de servicio se enumeran en la [**enumeración WS \_ SERVICE PROXY \_ \_ STATE.**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state)

Como se muestra en el diagrama anterior y el código siguiente, una llamada a la función [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) crea un proxy de servicio. Como parámetros para esta llamada, WWSAPI proporciona las enumeraciones siguientes:

-   [**TIPO DE \_ CANAL WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [**ENLACE DE \_ CANAL WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

También acepta parámetros opcionales mediante los siguientes tipos de datos:

-   [**IDENTIFICADOR DE \_ PROPIEDAD DEL PROXY \_ DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [**DESCRIPCIÓN DE SEGURIDAD DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

Cuando se ha creado el proxy de servicio, la función **WsCreateServiceProxy** devuelve una referencia al proxy de servicio, [WS \_ SERVICE \_ PROXY,](ws-service-proxy.md)a través de un parámetro out.

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

Una vez creado el proxy de servicio, la aplicación puede abrir el proxy de servicio para [](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) la comunicación con un servicio mediante una llamada a la función [**WsOpenServiceProxy,**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) pasando una estructura de direcciones que contiene la dirección de red del punto de conexión de servicio al que conectarse.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

Una vez abierto el proxy de servicio, la aplicación puede usarlo para realizar llamadas al servicio.

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

Cuando la aplicación ya no necesita el proxy de servicio, cierra el proxy de servicio mediante una llamada a la [**función WsCloseServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) También libera la memoria asociada llamando a [**WsFreeServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)

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

## <a name="reusing-the-service-proxy"></a>Volver a usar el proxy de servicio

Como alternativa, después de llamar a [**WsCloseServiceProxy,**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) una aplicación puede reutilizar el proxy de servicio llamando a la [**función WsResetServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

Para obtener más información sobre cómo se usan los servidores proxy de servicio en contextos diferentes, vea los temas siguientes:

-   [Proxy de servicio y sesiones](service-proxy-and-sessions.md)
-   [Operación de servicio](service-operation.md)
-   [Operaciones de servicio del lado cliente](client-side-service-operations.md)
-   [HttpCalculatorClientExample](httpcalculatorclientexample.md)

### <a name="security"></a>Seguridad

Las siguientes consideraciones de diseño de aplicaciones deben tenerse en cuenta cuidadosamente al usar la API de proxy del servicio WWSAPI:

-   El proxy de servicio no realizará ninguna validación de los datos más allá de la validación de Basic Profile 2.0 y la serialización XML. Es responsabilidad de la aplicación validar los datos contenidos en los parámetros que recibe como parte de la llamada.
-   La configuración del número máximo de llamadas pendientes en el proxy de servicio, mediante el valor de enumeración WS PROXY PROPERTY **MAX PENDING \_ \_ \_ \_ \_ CALLS** de [**WS \_ \_ \_ PROXY,**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) proporciona protección contra un servidor de ejecución lenta. El máximo predeterminado es 100. Las aplicaciones deben tener cuidado al modificar los valores predeterminados.
-   El proxy de servicio no proporciona ninguna garantía de seguridad más allá de las especificadas en la estructura DE DESCRIPCIÓN DE SEGURIDAD de [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) que se usa para comunicarse con el servidor.
-   Debe tener cuidado al modificar los valores [predeterminados de mensaje](message.md) [y](channel.md) canal en el proxy de servicio. Lea las consideraciones de seguridad asociadas a los mensajes y canales antes de modificar cualquiera de las propiedades relacionadas.
-   El proxy de servicio cifra todas las credenciales que mantiene en memoria.

Los siguientes elementos de API se relacionan con los servidores proxy de servicio.

| Devolución de llamada                                                          | Descripción                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**DEVOLUCIÓN DE LLAMADA \_ DE MENSAJES DE PROXY \_ WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | Se invoca cuando los encabezados del mensaje de entrada están a punto de enviarse a través de o cuando se acaba de recibir un encabezado de mensaje de salida. |



 



| Enumeración                                                 | Descripción                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**WS \_ CALL \_ PROPERTY \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | Enumera los parámetros opcionales para configurar una llamada en una operación de servicio del lado cliente. |
| [**IDENTIFICADOR DE \_ PROPIEDAD DEL PROXY \_ DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | Enumera los parámetros opcionales para configurar el proxy de servicio.                         |
| [**ESTADO DEL \_ \_ PROXY DEL SERVICIO WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | Estado del proxy de servicio.                                                           |



 



| Función                                                       | Descripción                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**WsAbandoneCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | Abandona una llamada especificada en un proxy de servicio especificado.                           |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | Cancela todas las entradas y salidas pendientes en un proxy de servicio especificado.                |
| [**WsCall**](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | Solo interno. Serializa los argumentos en un mensaje y lo envía a través del canal. |
| [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | Cierra un proxy de servicio para la comunicación.                                         |
| [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | Crea un proxy de servicio.                                                          |
| [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | Libera la memoria asociada a un proxy de servicio.                              |
| [**WsGetServiceProxyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | Recupera una propiedad de proxy de servicio especificada.                                     |
| [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | Abre un proxy de servicio en un punto de conexión de servicio.                                      |
| [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | Restablece el proxy de servicio.                                                             |



 



| Handle                                     | Descripción                                       |
|--------------------------------------------|---------------------------------------------------|
| [PROXY DEL \_ SERVICIO \_ WS](ws-service-proxy.md) | Tipo opaco que se usa para hacer referencia a un proxy de servicio. |



 



| Estructura                                         | Descripción                 |
|---------------------------------------------------|-----------------------------|
| [**WS \_ CALL \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | Especifica una propiedad de llamada.  |
| [**WS \_ PROPIEDAD \_ DE PROXY**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property). | Especifica una propiedad de proxy. |



 

 

 




