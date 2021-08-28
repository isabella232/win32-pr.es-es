---
title: Información general sobre la capa de modelo de servicio
description: La API del modelo de servicio WWSAPI modela la comunicación entre un cliente y un servicio como llamadas de método, en lugar de como mensajes de datos.
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- Servicios web de introducción a la capa de modelo de servicio para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b182678568c7825cbf0b18bbbfd132dd5287d3f05b9ae6a372e6e5c70cd06d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962970"
---
# <a name="service-model-layer-overview"></a>Información general sobre la capa de modelo de servicio

La API del modelo de servicio WWSAPI modela la comunicación entre un cliente y un servicio como llamadas de método, en lugar de como mensajes de datos. A diferencia del nivel de canal [](message.md) [,](channel-layer-overview.md)que admite intercambios de mensajes más tradicionales entre el cliente y el servicio, el modelo de servicio administra automáticamente la comunicación mediante un proxy de servicio en el cliente y un host de servicio en el servicio. Esto significa que el cliente llama a funciones generadas y el servidor implementa devoluciones de llamada.


Por ejemplo, considere un servicio de calculadora que realiza suma y resta en dos números. La suma y resta son operaciones representadas de forma natural como llamadas a métodos.

![Diagrama que muestra cómo un servicio de calculadora se comunica con un cliente mediante llamadas de método para sumar y restar.](images/servicemodelintro.png)

El modelo de servicio representa la comunicación entre el cliente y el servicio como llamadas de método declaradas, por lo que oculta los detalles de comunicación de la capa de canal subyacente de la aplicación, lo que facilita la implementación del servicio.

## <a name="specifying-a-service"></a>Especificar un servicio

Un servicio debe especificarse en términos de sus patrones de intercambio de mensajes, así como de su representación de datos de red. En el caso de los servicios, esta especificación normalmente se proporciona como documentos de esquema WSDL y XML.

El documento WSDL es un documento XML que contiene el enlace de canal y los patrones de intercambio de mensajes del servicio, mientras que el documento de esquema XML es un documento XML que define la representación de datos de los mensajes individuales.

Para el servicio de calculadora y sus operaciones de suma y resta, el documento WSDL podría ser parecido al ejemplo siguiente:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Del mismo modo, su esquema XML se puede definir de la siguiente manera:

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="Add">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:element name="AddResponse">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="result" type="xs:int" 
    />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema> 
```

## <a name="converting-metadata-to-code"></a>Convertir metadatos en código

El modelo de servicio proporciona la [WsUtil.exe](web-service-compiler-tool.md) como herramienta para procesar estos documentos de metadatos, convirtiendo un archivo WSDL en un encabezado de C y archivos de código fuente.

![Diagrama que muestra WsUtil.exe convierte un archivo WSDL en un encabezado de C y archivos de código fuente.](images/doctotool.png)

El [WsUtil.exe](web-service-compiler-tool.md) genera el encabezado y los orígenes para la implementación del servicio, así como las operaciones de servicio del lado cliente para el cliente .

## <a name="calling-the-calculator-service-from-a-client"></a>Llamar al servicio calculadora desde un cliente

Al igual que con la implementación del servicio, el cliente debe incluir el encabezado o los encabezados generados.

``` syntax
#include "CalculatorProxyStub.h"
```

Ahora, la aplicación cliente puede crear y abrir un proxy de servicio para iniciar la comunicación con el servicio de calculadora.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L"http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

La aplicación puede llamar a la operación Agregar en el servicio de calculadora con el código siguiente:

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

Consulte el ejemplo de código en [HttpCalculatorClientExample](httpcalculatorclientexample.md) para obtener una implementación completa del servicio de calculadora.

## <a name="service-model-components"></a>Componentes del modelo de servicio

La interacción de los componentes individuales del modelo de servicio WWSAPI en el ejemplo de calculadora es la siguiente:

-   El cliente crea un [proxy de servicio](service-proxy.md) y lo abre.
-   El cliente llama a la función Add del servicio y pasa el proxy de servicio.
-   El mensaje se serializa según los metadatos de serialización en los archivos de encabezado y de origen generados por la herramienta de metadatos ([WsUtil.exe](web-service-compiler-tool.md)).
-   El mensaje se escribe en el canal y se transmite a través de la red al servicio.
-   En el lado servidor, el servicio se hospeda dentro de un host de servicio y tiene un punto de conexión que escucha el contrato ICalculator.
-   Con los metadatos del modelo de servicio en el código auxiliar, el servicio deserializa el mensaje del cliente y lo envía al código auxiliar.
-   El servicio del lado servidor llama al método Add y le pasa el contexto de la operación. Este contexto de operación contiene la referencia al mensaje entrante.

![Diagrama que muestra la interacción de los componentes individuales del modelo de servicio WWSAPI.](images/servicemodellayout.png)

Componentes

-   [Host de servicio:](service-host.md)hospeda un servicio.
-   [Proxy de](service-proxy.md)servicio: define cómo se comunica un cliente con un servicio.
-   [Contexto:](context.md)bolsa de propiedades para hacer que la información específica del estado esté disponible para una operación de servicio.
-   [Contract](contract.md): la definición de interfaz de un servicio. Por ejemplo, ICalculator representa un contrato para el servicio de calculadora en nuestro código de ejemplo.
-   [WsUtil.exe: ](web-service-compiler-tool.md)la herramienta de metadatos del modelo de servicio para generar servidores proxy y códigos auxiliares.

 

 




