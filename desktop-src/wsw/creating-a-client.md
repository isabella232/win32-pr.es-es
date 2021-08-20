---
title: Creación de un cliente
description: La creación de un cliente para servicios web se simplifica en gran medida en WWSAPI mediante service model API y WsUtil.exe herramienta.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ca04ef5fbbeef76cd32a0b6523391deb19957479cd5f332715972f3b5bfbc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026563"
---
# <a name="creating-a-client"></a>Creación de un cliente

La creación de un cliente para servicios web se simplifica en gran medida en WWSAPI mediante [service model](service-model-layer-overview.md) API y [WsUtil.exe](wsutil-compiler-tool.md) herramienta. El modelo de servicio proporciona una API que permite al cliente enviar y recibir [mensajes](message.md) a través de un [canal como](channel.md) llamadas al método C. La herramienta WsUtil genera encabezados y asistentes para implementar el cliente. Estos encabezados incluyen los tipos y prototipos de función para las funciones de C que representan los servicios ofrecidos por el servicio web de destino. Los asistentes se usan para crear el proxy de servicio, que contiene la información de enlace y [la](endpoint-address.md) dirección del punto de conexión para el servicio.

## <a name="using-wsutil-to-generate-headers-and-helpers"></a>Usar WsUtil para generar encabezados y asistentes

Para generar los encabezados y los asistentes, WsUtil abre y lee los archivos de metadatos del servicio de destino (archivos wsdl y xsd) y los convierte en encabezados. por lo tanto, es necesario recuperar los archivos de metadatos para el servicio de destino de antemano, por ejemplo mediante SvcUtil, una parte de Windows Communication Foundation. Por motivos de seguridad, es fundamental que las copias de estos archivos sean de confianza. (Para obtener más información, vea la sección "Seguridad" del tema [WsUtil Compiler Tool).](wsutil-compiler-tool.md)

Para ejecutar WsUtil, use la siguiente sintaxis de línea de comandos si los archivos WSDL y XSD del servicio están en su propio directorio: `WsUtil.exe *.wsdl *.xsd` . Como alternativa, puede especificar los archivos por nombre completo.

WsUtil generalmente genera dos archivos para cada archivo de metadatos: un encabezado y un archivo C. Agregue estos archivos al proyecto de codificación y use instrucciones \# include para incluirlos en el código del cliente. (Los archivos XSD representan tipos y los archivos WSDL representan operaciones).

## <a name="creating-the-service-proxy"></a>Creación del proxy de servicio

El encabezado generado por WsUtil contiene una rutina auxiliar para crear el proxy de servicio con el enlace necesario. Esta rutina se incluye en la sección "Rutinas del asistente de directivas" del archivo de encabezado generado. Por ejemplo, el encabezado generado para el servicio de calculadora que se muestra en el ejemplo [httpcalculatorclientexample](httpcalculatorclientexample.md) contendrá el siguiente prototipo de función.


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



Incorpore este asistente en el código y pase un identificador proxy de servicio de [WS \_ \_ ](ws-service-proxy.md) para recibir el identificador al proxy de servicio creado. En el escenario más sencillo, en el que solo se pasan un identificador de proxy de servicio y un objeto de error a la función, la llamada tiene un aspecto similar al siguiente.


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



Para crear la parte de la dirección del proxy de servicio, llame a [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) con un identificador para el proxy de servicio y un puntero a una dirección de punto de conexión de [**\_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) que contenga la dirección del punto de conexión de servicio a la que desea conectarse.

## <a name="implementing-the-client-with-function-prototypes"></a>Implementación del cliente con prototipos de función

Los encabezados generados a partir de los archivos WSDL de servicio también contienen prototipos de función de C que representan los servicios disponibles en el servicio web y específicos del enlace necesario. Por ejemplo, un encabezado generado para el servicio de calculadora que se muestra en HttpCalculatorServiceExample contendrá el siguiente prototipo para la operación de multiplicación de ese servicio.

``` syntax
HRESULT BasicHttpBinding_ICalculator_Multiply(
    __in WS_SERVICE_PROXY* _serviceProxy,
    __in double n1,
    __in double n2,
    __out double* MultiplyResult,
    __in WS_HEAP* _heap,
    __in_ecount_opt(_callPropertyCount) const WS_CALL_PROPERTY* _callProperties,
    __in const ULONG _callPropertyCount,
    __in_opt const WS_ASYNC_CONTEXT* _asyncContext,
    __in_opt WS_ERROR* _error);
```

Puede copiar los prototipos y usarlos como plantillas para codificar las llamadas de función en el cliente, en cada caso pasando el identificador al proxy de servicio. Cuando haya terminado con el proxy de servicio, llame a [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).

 

 




