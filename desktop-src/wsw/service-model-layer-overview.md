---
title: Información general sobre la capa de modelo de servicio
description: La API del modelo de servicio WWSAPI modela la comunicación entre un cliente y un servicio como llamadas a métodos, en lugar de como mensajes de datos.
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- Servicios Web de información general de nivel de modelo de servicio para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74861f0e2ed13b35e308d1314aec2a33dc28c31
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104361822"
---
# <a name="service-model-layer-overview"></a>Información general sobre la capa de modelo de servicio

La API del modelo de servicio WWSAPI modela la comunicación entre un cliente y un servicio como llamadas a métodos, en lugar de como mensajes de datos. A diferencia de la [capa del canal](channel-layer-overview.md), que admite intercambios de [mensajes](message.md) más tradicionales entre el cliente y el servicio, el modelo de servicio administra automáticamente la comunicación por medio de un proxy de servicio en el cliente y un host de servicio en el servicio. Esto significa que el cliente llama a las funciones generadas y el servidor implementa las devoluciones de llamada.


Por ejemplo, considere un servicio de calculadora que realiza la suma y resta de dos números. Las operaciones de suma y resta se representan de forma natural como llamadas a métodos.

![Diagrama que muestra cómo un servicio de calculadora se comunica con un cliente mediante llamadas a métodos para la suma y la resta.](images/servicemodelintro.png)

El modelo de servicio representa la comunicación entre el cliente y el servicio como llamadas a métodos declarados, por lo que oculta los detalles de comunicación de la capa del canal subyacente de la aplicación, lo que facilita la implementación del servicio.

## <a name="specifying-a-service"></a>Especificar un servicio

Se debe especificar un servicio en cuanto a sus patrones de intercambio de mensajes, así como su representación de datos de red. En el caso de los servicios, esta especificación se proporciona normalmente como documento de esquemas XML y WSDL.

El documento WSDL es un documento XML que contiene el enlace de canal y los patrones de intercambio de mensajes del servicio, mientras que el documento de esquema XML es un documento XML que define la representación de los datos de los mensajes individuales.

Para el servicio de calculadora y sus operaciones de suma y resta, el documento WSDL podría ser similar al ejemplo siguiente:

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

El modelo de servicio proporciona el [WsUtil.exe](web-service-compiler-tool.md) como una herramienta para procesar estos documentos de metadatos, convirtiendo un archivo WSDL en un encabezado y archivos de código fuente de C.

![Diagrama que muestra cómo WsUtil.exe convierte un archivo WSDL en un encabezado y archivos de código fuente de C.](images/doctotool.png)

El [WsUtil.exe](web-service-compiler-tool.md) genera el encabezado y los orígenes para la implementación del servicio, así como las operaciones de servicio del lado cliente para el cliente.

## <a name="calling-the-calculator-service-from-a-client&quot;></a>Llamar al servicio de calculadora desde un cliente

Al igual que con la implementación del servicio, el cliente debe incluir el encabezado o encabezados generados.

``` syntax
#include &quot;CalculatorProxyStub.h&quot;
```

Ahora, la aplicación cliente puede crear y abrir un proxy de servicio para comenzar la comunicación con el servicio de calculadora.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L&quot;http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

La aplicación puede llamar a la operación de agregar en el servicio de calculadora con el código siguiente:

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

Consulte el ejemplo de código en [HttpCalculatorClientExample](httpcalculatorclientexample.md) para obtener la implementación completa del servicio de calculadora.

## <a name="service-model-components"></a>Componentes del modelo de servicio

La interacción de los componentes individuales del modelo de servicio de WWSAPI en el ejemplo de la calculadora es la siguiente:

-   El cliente crea un [proxy de servicio](service-proxy.md) y lo abre.
-   El cliente llama a la función Add del servicio y pasa el proxy del servicio.
-   El mensaje se serializa de acuerdo con los metadatos de serialización en el encabezado y los archivos de código fuente generados por la herramienta de metadatos ([WsUtil.exe](web-service-compiler-tool.md)).
-   El mensaje se escribe en el canal y se transmite a través de la red al servicio.
-   En el lado del servidor, el servicio se hospeda dentro de un host de servicio y tiene un punto de conexión que escucha para el contrato de ICalculator.
-   Mediante el uso de los metadatos del modelo de servicio en el código auxiliar, el servicio deserializa el mensaje del cliente y lo envía al código auxiliar.
-   El servicio del lado servidor llama al método Add y le pasa el contexto de la operación. Este contexto de operación contiene la referencia al mensaje entrante.

![Diagrama que muestra la interacción de los componentes individuales del modelo de servicio de WWSAPI.](images/servicemodellayout.png)

Componentes

-   [Host de servicio](service-host.md): hospeda un servicio.
-   [Proxy de servicio](service-proxy.md): define el modo en que un cliente se comunica con un servicio.
-   [Context](context.md): contenedor de propiedades para hacer que la información específica del estado esté disponible para una operación de servicio.
-   [Contrato](contract.md): la definición de interfaz de un servicio. Por ejemplo, ICalculator representa un contrato para el servicio de calculadora en nuestro código de ejemplo.
-   [WsUtil.exe](web-service-compiler-tool.md): herramienta de metadatos del modelo de servicio para generar servidores proxy y códigos auxiliares.

 

 




