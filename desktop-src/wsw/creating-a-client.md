---
title: Creación de un cliente
description: La creación de un cliente para los servicios web se ha simplificado en gran medida en WWSAPI mediante la API del modelo de servicio y la herramienta WsUtil.exe.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606a68f574a9ad79d15f3ddd48247f93a5414250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419136"
---
# <a name="creating-a-client"></a><span data-ttu-id="e0c17-103">Creación de un cliente</span><span class="sxs-lookup"><span data-stu-id="e0c17-103">Creating a Client</span></span>

<span data-ttu-id="e0c17-104">La creación de un cliente para los servicios web se ha simplificado en gran medida en WWSAPI mediante la API del [modelo de servicio](service-model-layer-overview.md) y la herramienta [WsUtil.exe](wsutil-compiler-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="e0c17-104">Creating a client for Web services is greatly simplified in WWSAPI by the [Service Model](service-model-layer-overview.md) API and the [WsUtil.exe](wsutil-compiler-tool.md) tool.</span></span> <span data-ttu-id="e0c17-105">El modelo de servicio proporciona una API que permite al cliente enviar y recibir [mensajes](message.md) a través de un [canal](channel.md) como llamadas a métodos de C.</span><span class="sxs-lookup"><span data-stu-id="e0c17-105">The Service Model provides an API that enables the client to send and receive [messages](message.md) over a [channel](channel.md) as C method calls.</span></span> <span data-ttu-id="e0c17-106">La herramienta WsUtil genera encabezados y aplicaciones auxiliares para implementar el cliente.</span><span class="sxs-lookup"><span data-stu-id="e0c17-106">The WsUtil tool generates headers and helpers for implementing the client.</span></span> <span data-ttu-id="e0c17-107">Estos encabezados incluyen los tipos y prototipos de función para las funciones de C que representan los servicios que ofrece el servicio Web de destino.</span><span class="sxs-lookup"><span data-stu-id="e0c17-107">These headers include the types and function prototypes for C functions representing the services offered by the target Web service.</span></span> <span data-ttu-id="e0c17-108">Las aplicaciones auxiliares se utilizan para crear el proxy del servicio, que contiene la información de enlace y la [dirección del punto de conexión](endpoint-address.md) para el servicio.</span><span class="sxs-lookup"><span data-stu-id="e0c17-108">The helpers are used to create the service proxy, which contains the binding information and [endpoint address](endpoint-address.md) for the service.</span></span>

## <a name="using-wsutil-to-generate-headers-and-helpers"></a><span data-ttu-id="e0c17-109">Uso de WsUtil para generar encabezados y aplicaciones auxiliares</span><span class="sxs-lookup"><span data-stu-id="e0c17-109">Using WsUtil to Generate Headers and Helpers</span></span>

<span data-ttu-id="e0c17-110">Para generar encabezados y aplicaciones auxiliares, WsUtil abre y Lee los archivos de metadatos para el servicio de destino (archivos WSDL y XSD) y los convierte en encabezados. por lo tanto, es necesario recuperar de antemano los archivos de metadatos para el servicio de destino, por ejemplo, mediante SvcUtil, una parte de la Windows Communication Foundation.</span><span class="sxs-lookup"><span data-stu-id="e0c17-110">To generate the headers and helpers, WsUtil opens and reads the metadata files for the target service — wsdl and xsd files— and converts them into headers; therefore, it is necessary to retrieve the metadata files for the target service in advance, for example by using SvcUtil, a part of the Windows Communication Foundation.</span></span> <span data-ttu-id="e0c17-111">Por motivos de seguridad, es imperativo que las copias de estos archivos sean de confianza.</span><span class="sxs-lookup"><span data-stu-id="e0c17-111">For security reasons, it is imperative that your copies of these files are trustworthy.</span></span> <span data-ttu-id="e0c17-112">(Para obtener más información, vea la sección "seguridad" del tema de la [herramienta del compilador WsUtil](wsutil-compiler-tool.md) ).</span><span class="sxs-lookup"><span data-stu-id="e0c17-112">(For more information, see the "Security" section of the [WsUtil Compiler Tool](wsutil-compiler-tool.md) topic.)</span></span>

<span data-ttu-id="e0c17-113">Para ejecutar WsUtil, use la siguiente sintaxis de línea de comandos si los archivos WSDL y XSD para el servicio se encuentran en su propio directorio: `WsUtil.exe *.wsdl *.xsd` .</span><span class="sxs-lookup"><span data-stu-id="e0c17-113">To run WsUtil, use the following command-line syntax if the WSDL and XSD files for the service are in their own directory: `WsUtil.exe *.wsdl *.xsd`.</span></span> <span data-ttu-id="e0c17-114">También puede especificar los archivos por nombre completo.</span><span class="sxs-lookup"><span data-stu-id="e0c17-114">Alternatively, you can specify the files by full name.</span></span>

<span data-ttu-id="e0c17-115">Normalmente, WsUtil genera dos archivos para cada archivo de metadatos: un encabezado y un archivo C.</span><span class="sxs-lookup"><span data-stu-id="e0c17-115">WsUtil generally generates two files for each metadata file: a header and a C file.</span></span> <span data-ttu-id="e0c17-116">Agregue estos archivos al proyecto de codificación y use \# instrucciones include para incluirlos en el código del cliente.</span><span class="sxs-lookup"><span data-stu-id="e0c17-116">Add these files to your coding project, and use \#include statements to include them in the code for your client.</span></span> <span data-ttu-id="e0c17-117">(Los archivos XSD representan tipos y los archivos WSDL representan operaciones).</span><span class="sxs-lookup"><span data-stu-id="e0c17-117">(The XSD files represent types, and the WSDL files represent operations.)</span></span>

## <a name="creating-the-service-proxy"></a><span data-ttu-id="e0c17-118">Creación del proxy de servicio</span><span class="sxs-lookup"><span data-stu-id="e0c17-118">Creating the Service Proxy</span></span>

<span data-ttu-id="e0c17-119">El encabezado generado por WsUtil contiene una rutina auxiliar para crear el proxy de servicio con el enlace necesario.</span><span class="sxs-lookup"><span data-stu-id="e0c17-119">The header generated by WsUtil contains a helper routine for creating the service proxy with the required binding.</span></span> <span data-ttu-id="e0c17-120">Esta rutina se incluye en la sección "rutinas auxiliares de directivas" del archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="e0c17-120">This routine is included in the "Policy helper routines" section of the generated header file.</span></span> <span data-ttu-id="e0c17-121">Por ejemplo, el encabezado generado para el servicio de calculadora mostrado en el ejemplo [httpcalculatorclientexample](httpcalculatorclientexample.md) contendrá el prototipo de función siguiente.</span><span class="sxs-lookup"><span data-stu-id="e0c17-121">For example, the generated header for the calculator service illustrated in the [httpcalculatorclientexample](httpcalculatorclientexample.md) example will contain the following function prototype.</span></span>


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



<span data-ttu-id="e0c17-122">Incorpore esta aplicación auxiliar en el código y pase un identificador de [ \_ \_ proxy de servicio WS](ws-service-proxy.md) para recibir el identificador del proxy de servicio creado.</span><span class="sxs-lookup"><span data-stu-id="e0c17-122">Incorporate this helper in your code and pass a [WS\_SERVICE\_PROXY](ws-service-proxy.md) handle to receive the handle to the created service proxy.</span></span> <span data-ttu-id="e0c17-123">En el escenario más sencillo, en el que solo un identificador de proxy de servicio y un objeto de error se pasan a la función, la llamada es similar a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="e0c17-123">In the simplest scenario, in which only a service proxy handle and an error object are passed to the function, the call looks like the following.</span></span>


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



<span data-ttu-id="e0c17-124">Para crear la parte de la dirección del proxy de servicio, llame a [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) con un identificador al proxy de servicio y un puntero a una [**dirección de \_ extremo \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) que contenga la dirección del punto de conexión de servicio a la que desea conectarse.</span><span class="sxs-lookup"><span data-stu-id="e0c17-124">To create the address portion of the service proxy, call [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) with a handle to the service proxy and a pointer to a [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) containing the service endpoint address to which you wish to connect.</span></span>

## <a name="implementing-the-client-with-function-prototypes"></a><span data-ttu-id="e0c17-125">Implementar el cliente con prototipos de función</span><span class="sxs-lookup"><span data-stu-id="e0c17-125">Implementing the Client with Function Prototypes</span></span>

<span data-ttu-id="e0c17-126">Los encabezados generados a partir de los archivos WSDL de servicio también contienen prototipos de función de C que representan los servicios disponibles del servicio Web y específicos del enlace requerido.</span><span class="sxs-lookup"><span data-stu-id="e0c17-126">The headers generated from the service WSDL files also contain C function prototypes representing the services available from the Web service and specific to the binding required.</span></span> <span data-ttu-id="e0c17-127">Por ejemplo, un encabezado generado para el servicio de calculadora que se muestra en HttpCalculatorServiceExample contendrá el siguiente prototipo para la operación de multiplicación de ese servicio.</span><span class="sxs-lookup"><span data-stu-id="e0c17-127">For example, a header generated for the calculator service illustrated in HttpCalculatorServiceExample will contain the following prototype for that service's multiplication operation.</span></span>

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

<span data-ttu-id="e0c17-128">Puede copiar los prototipos y usarlos como plantillas para codificar las llamadas de función en el cliente, en cada caso pasando el identificador al proxy del servicio.</span><span class="sxs-lookup"><span data-stu-id="e0c17-128">You can copy the prototypes and use them as templates for coding the function calls in your client, in each case passing the handle to service proxy.</span></span> <span data-ttu-id="e0c17-129">Cuando haya terminado con el proxy de servicio, llame a [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="e0c17-129">When you are finished with the service proxy, call [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).</span></span>

 

 




