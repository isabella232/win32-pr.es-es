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
# <a name="service-model-layer-overview"></a><span data-ttu-id="d8bb7-106">Información general sobre la capa de modelo de servicio</span><span class="sxs-lookup"><span data-stu-id="d8bb7-106">Service Model Layer Overview</span></span>

<span data-ttu-id="d8bb7-107">La API del modelo de servicio WWSAPI modela la comunicación entre un cliente y un servicio como llamadas a métodos, en lugar de como mensajes de datos.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-107">The WWSAPI Service Model API models the communication between a client and a service as method calls, rather than as data messages.</span></span> <span data-ttu-id="d8bb7-108">A diferencia de la [capa del canal](channel-layer-overview.md), que admite intercambios de [mensajes](message.md) más tradicionales entre el cliente y el servicio, el modelo de servicio administra automáticamente la comunicación por medio de un proxy de servicio en el cliente y un host de servicio en el servicio.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-108">In contrast to the [channel layer](channel-layer-overview.md), which supports more traditional [message](message.md) exchanges between client and service, the Service Model automatically manages communication by means of a service proxy on the client and a service host on the service.</span></span> <span data-ttu-id="d8bb7-109">Esto significa que el cliente llama a las funciones generadas y el servidor implementa las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-109">This means that the client calls generated functions and the server implements callbacks.</span></span>


<span data-ttu-id="d8bb7-110">Por ejemplo, considere un servicio de calculadora que realiza la suma y resta de dos números.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-110">For example, consider a calculator service which performs addition and subtraction on two numbers.</span></span> <span data-ttu-id="d8bb7-111">Las operaciones de suma y resta se representan de forma natural como llamadas a métodos.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-111">Addition and subtraction are operations naturally represented as method calls.</span></span>

![Diagrama que muestra cómo un servicio de calculadora se comunica con un cliente mediante llamadas a métodos para la suma y la resta.](images/servicemodelintro.png)

<span data-ttu-id="d8bb7-113">El modelo de servicio representa la comunicación entre el cliente y el servicio como llamadas a métodos declarados, por lo que oculta los detalles de comunicación de la capa del canal subyacente de la aplicación, lo que facilita la implementación del servicio.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-113">The service model represents the communication between client and the service as declared method calls, and so conceals the communication details of the underlying channel layer from the application, making the service easier to implement.</span></span>

## <a name="specifying-a-service"></a><span data-ttu-id="d8bb7-114">Especificar un servicio</span><span class="sxs-lookup"><span data-stu-id="d8bb7-114">Specifying a Service</span></span>

<span data-ttu-id="d8bb7-115">Se debe especificar un servicio en cuanto a sus patrones de intercambio de mensajes, así como su representación de datos de red.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-115">A service must be specified in terms of its message exchange patterns as well as its network data representation.</span></span> <span data-ttu-id="d8bb7-116">En el caso de los servicios, esta especificación se proporciona normalmente como documento de esquemas XML y WSDL.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-116">For services, this specification is usually provided as WSDL and XML schema documents.</span></span>

<span data-ttu-id="d8bb7-117">El documento WSDL es un documento XML que contiene el enlace de canal y los patrones de intercambio de mensajes del servicio, mientras que el documento de esquema XML es un documento XML que define la representación de los datos de los mensajes individuales.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-117">The WSDL document is an XML document which contains the channel binding and the message exchange patterns of the service, whereas the XML schema document is an XML document that defines the data representation of the individual messages.</span></span>

<span data-ttu-id="d8bb7-118">Para el servicio de calculadora y sus operaciones de suma y resta, el documento WSDL podría ser similar al ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d8bb7-118">For the calculator service and its addition and subtraction operations, the WSDL document might look like the following example:</span></span>

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

<span data-ttu-id="d8bb7-119">Del mismo modo, su esquema XML se puede definir de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d8bb7-119">Likewise, its XML schema can be defined as follows:</span></span>

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

## <a name="converting-metadata-to-code"></a><span data-ttu-id="d8bb7-120">Convertir metadatos en código</span><span class="sxs-lookup"><span data-stu-id="d8bb7-120">Converting Metadata to Code</span></span>

<span data-ttu-id="d8bb7-121">El modelo de servicio proporciona el [WsUtil.exe](web-service-compiler-tool.md) como una herramienta para procesar estos documentos de metadatos, convirtiendo un archivo WSDL en un encabezado y archivos de código fuente de C.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-121">The service model provides the [WsUtil.exe](web-service-compiler-tool.md) as a tool to process these metadata documents, converting a WSDL file into a C header and source files.</span></span>

![Diagrama que muestra cómo WsUtil.exe convierte un archivo WSDL en un encabezado y archivos de código fuente de C.](images/doctotool.png)

<span data-ttu-id="d8bb7-123">El [WsUtil.exe](web-service-compiler-tool.md) genera el encabezado y los orígenes para la implementación del servicio, así como las operaciones de servicio del lado cliente para el cliente.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-123">The [WsUtil.exe](web-service-compiler-tool.md) generates header and sources for service implementation as well as client-side service operations for the client .</span></span>

## <a name="calling-the-calculator-service-from-a-client"></a><span data-ttu-id="d8bb7-124">Llamar al servicio de calculadora desde un cliente</span><span class="sxs-lookup"><span data-stu-id="d8bb7-124">Calling the Calculator Service From a Client</span></span>

<span data-ttu-id="d8bb7-125">Al igual que con la implementación del servicio, el cliente debe incluir el encabezado o encabezados generados.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-125">As with the service implementation, the client must include the generated header or headers.</span></span>

``` syntax
#include "CalculatorProxyStub.h"
```

<span data-ttu-id="d8bb7-126">Ahora, la aplicación cliente puede crear y abrir un proxy de servicio para comenzar la comunicación con el servicio de calculadora.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-126">Now, The client application can create and open a service proxy to begin communication with the calculator service.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L"http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

<span data-ttu-id="d8bb7-127">La aplicación puede llamar a la operación de agregar en el servicio de calculadora con el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="d8bb7-127">The application can call the Add operation on the calculator service with the following code:</span></span>

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

<span data-ttu-id="d8bb7-128">Consulte el ejemplo de código en [HttpCalculatorClientExample](httpcalculatorclientexample.md) para obtener la implementación completa del servicio de calculadora.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-128">Please refer to the code example at [HttpCalculatorClientExample](httpcalculatorclientexample.md) for full implementation of the calculator service.</span></span>

## <a name="service-model-components"></a><span data-ttu-id="d8bb7-129">Componentes del modelo de servicio</span><span class="sxs-lookup"><span data-stu-id="d8bb7-129">Service Model Components</span></span>

<span data-ttu-id="d8bb7-130">La interacción de los componentes individuales del modelo de servicio de WWSAPI en el ejemplo de la calculadora es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="d8bb7-130">The interaction of the individual WWSAPI Service Model components within the Calculator example is as follows:</span></span>

-   <span data-ttu-id="d8bb7-131">El cliente crea un [proxy de servicio](service-proxy.md) y lo abre.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-131">The client creates a [service proxy](service-proxy.md) and opens it.</span></span>
-   <span data-ttu-id="d8bb7-132">El cliente llama a la función Add del servicio y pasa el proxy del servicio.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-132">The client calls the Add function of the service, and passes in the service proxy.</span></span>
-   <span data-ttu-id="d8bb7-133">El mensaje se serializa de acuerdo con los metadatos de serialización en el encabezado y los archivos de código fuente generados por la herramienta de metadatos ([WsUtil.exe](web-service-compiler-tool.md)).</span><span class="sxs-lookup"><span data-stu-id="d8bb7-133">The message is serialized according to the serialization metadata in the header and source files generated by the metadata tool ([WsUtil.exe](web-service-compiler-tool.md)).</span></span>
-   <span data-ttu-id="d8bb7-134">El mensaje se escribe en el canal y se transmite a través de la red al servicio.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-134">The message is written to the channel and is transmitted over the network to the service.</span></span>
-   <span data-ttu-id="d8bb7-135">En el lado del servidor, el servicio se hospeda dentro de un host de servicio y tiene un punto de conexión que escucha para el contrato de ICalculator.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-135">On the server side, the service is hosted inside a service host, and has an endpoint listening for the ICalculator contract.</span></span>
-   <span data-ttu-id="d8bb7-136">Mediante el uso de los metadatos del modelo de servicio en el código auxiliar, el servicio deserializa el mensaje del cliente y lo envía al código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-136">Using the Service Model metadata in the stub, the service deserializes the message from the client and dispatches it to the stub.</span></span>
-   <span data-ttu-id="d8bb7-137">El servicio del lado servidor llama al método Add y le pasa el contexto de la operación.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-137">The server-side service calls the Add method, passing it the operation context.</span></span> <span data-ttu-id="d8bb7-138">Este contexto de operación contiene la referencia al mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-138">This operation context contains the reference to the incoming message.</span></span>

![Diagrama que muestra la interacción de los componentes individuales del modelo de servicio de WWSAPI.](images/servicemodellayout.png)

<span data-ttu-id="d8bb7-140">Componentes</span><span class="sxs-lookup"><span data-stu-id="d8bb7-140">Components</span></span>

-   <span data-ttu-id="d8bb7-141">[Host de servicio](service-host.md): hospeda un servicio.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-141">[Service host](service-host.md): Hosts a service.</span></span>
-   <span data-ttu-id="d8bb7-142">[Proxy de servicio](service-proxy.md): define el modo en que un cliente se comunica con un servicio.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-142">[Service proxy](service-proxy.md): Defines how a client communicates with a service.</span></span>
-   <span data-ttu-id="d8bb7-143">[Context](context.md): contenedor de propiedades para hacer que la información específica del estado esté disponible para una operación de servicio.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-143">[Context](context.md): Property bag for making state-specific information available to a service operation.</span></span>
-   <span data-ttu-id="d8bb7-144">[Contrato](contract.md): la definición de interfaz de un servicio.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-144">[Contract](contract.md): The interface definition of a service.</span></span> <span data-ttu-id="d8bb7-145">Por ejemplo, ICalculator representa un contrato para el servicio de calculadora en nuestro código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-145">For example, ICalculator represents a contract for the calculator service in our example code.</span></span>
-   <span data-ttu-id="d8bb7-146">[WsUtil.exe](web-service-compiler-tool.md): herramienta de metadatos del modelo de servicio para generar servidores proxy y códigos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="d8bb7-146">[WsUtil.exe](web-service-compiler-tool.md): The Service Model metadata tool for generating proxies and stubs.</span></span>

 

 




