---
title: Crear manualmente un proxy de servicio para un servicio WCF
description: La forma más fácil de crear un proxy de servicio de cliente para un servicio de Windows Communication Foundation (WCF) es la capa de modelo de servicio con la herramienta WsUtil, como se describe en el tema crear un cliente.
ms.assetid: ef545090-382b-44bd-b7ab-f5a285b6e202
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e061fda95298986ee6336dee0662d80c89a0a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695376"
---
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a><span data-ttu-id="bde10-103">Crear manualmente un proxy de servicio para un servicio WCF</span><span class="sxs-lookup"><span data-stu-id="bde10-103">Manually Creating a Service Proxy for a WCF Service</span></span>

<span data-ttu-id="bde10-104">La forma más fácil de crear un proxy de servicio de cliente para un servicio de Windows Communication Foundation (WCF) es la capa de [modelo de servicio](service-model-layer-overview.md) con la herramienta WsUtil, como se describe en el tema [crear un cliente](creating-a-client.md) .</span><span class="sxs-lookup"><span data-stu-id="bde10-104">The easiest way to create a client service proxy for a Windows Communication Foundation (WCF) service is at the [Service Model](service-model-layer-overview.md) layer with the WsUtil tool, as described in the [Creating a Client](creating-a-client.md) topic.</span></span> <span data-ttu-id="bde10-105">Sin embargo, si es necesario, también puede crear manualmente un proxy de servicio.</span><span class="sxs-lookup"><span data-stu-id="bde10-105">However, if necessary, you can also create a service proxy manually.</span></span> <span data-ttu-id="bde10-106">Esta API incluye una función [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) para crear el proxy de servicio, así como estructuras, enumeraciones, etc. para establecer las propiedades necesarias para interoperar con WCF.</span><span class="sxs-lookup"><span data-stu-id="bde10-106">This API includes a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function for creating the service proxy as well as structures, enumerations, and so on for setting the properties necessary to interoperate with WCF.</span></span>

<span data-ttu-id="bde10-107">WCF proporciona una serie de enlaces estándar y cada uno de ellos tiene como destino un escenario de uso específico.</span><span class="sxs-lookup"><span data-stu-id="bde10-107">WCF provides a number of standard bindings, each targeting a specific usage scenario.</span></span> <span data-ttu-id="bde10-108">El enlace que utiliza el servicio al que intenta conectarse, a su vez, determina qué propiedades de canal se deben personalizar para que el proxy de servicio se comunique con el servicio.</span><span class="sxs-lookup"><span data-stu-id="bde10-108">Which binding the service you are trying to connect to uses, in turn, determines which channel properties you need to customize for your service proxy to communicate with the service.</span></span>

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a><span data-ttu-id="bde10-109">Creación de un proxy de servicio para WSHttpBinding de WCF</span><span class="sxs-lookup"><span data-stu-id="bde10-109">Creating a Service Proxy for WCF's WSHttpBinding</span></span>

<span data-ttu-id="bde10-110">WSHttpBinding es para el escenario principal de servicios Web de Internet.</span><span class="sxs-lookup"><span data-stu-id="bde10-110">WSHttpBinding is for the mainline Internet web services scenario.</span></span> <span data-ttu-id="bde10-111">Usa la versión de SOAP 1,2 y WS-Addressing versión 1,0 más recientes y habilita una amplia gama de opciones de seguridad en los transportes HTTP y HTTPS públicos.</span><span class="sxs-lookup"><span data-stu-id="bde10-111">It uses the newer SOAP version 1.2 and WS-Addressing version 1.0 and enables a wide range of security settings over the public HTTP and HTTPS transports.</span></span> <span data-ttu-id="bde10-112">WWSAPI no tiene un equivalente de WSHttpBinding (o cualquiera de los enlaces estándar de WCF, en ese caso), pero como su versión predeterminada de SOAP, WS-Addressing versión y el formato de codificación coinciden con los de WSHttpBinding, la creación de un proxy de servicio para un servicio que usa WSHttpBinding es sencilla.</span><span class="sxs-lookup"><span data-stu-id="bde10-112">WWSAPI does not have an equivalent of the WSHttpBinding (or any of the WCF standard bindings, for that matter), but since its default SOAP version, WS-Addressing version, and encoding format match those in WSHttpBinding, creating a service proxy for a service that uses the WSHttpBinding is straightforward.</span></span> <span data-ttu-id="bde10-113">Por ejemplo, para crear un proxy de servicio para comunicarse con un punto de conexión WSHttpBinding sin seguridad, puede usar simplemente código como el fragmento de código siguiente (declaración de variables, y se omite la creación de montones y errores).</span><span class="sxs-lookup"><span data-stu-id="bde10-113">For example, to create a service proxy to talk to a WSHttpBinding endpoint without security, you can simply use code like following snippet (variable declaration, and heap and error creation are omitted).</span></span> <span data-ttu-id="bde10-114">Observe que no se ha especificado ninguna propiedad de canal ni Descripción de seguridad en la llamada a la función [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="bde10-114">Notice that no channel properties or security description is specified in the call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span>


```C++
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        NULL, // channel properties
        0, // channel property count
        &proxy, 
        error);
```



<span data-ttu-id="bde10-115">La función crea el proxy de servicio y devuelve un puntero a él en el parámetro *serviceProxy* (&proxy en la llamada de función anterior).</span><span class="sxs-lookup"><span data-stu-id="bde10-115">The function creates the service proxy and returns a pointer to it in the *serviceProxy* parameter (&proxy in the function call above).</span></span>

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a><span data-ttu-id="bde10-116">Creación de un proxy de servicio para BasicHttpBinding de WCF</span><span class="sxs-lookup"><span data-stu-id="bde10-116">Creating a Service Proxy for WCF's BasicHttpBinding</span></span>

<span data-ttu-id="bde10-117">Sin embargo, al crear manualmente un proxy de servicio para un servicio WCF que utiliza un enlace BasicHttpBinding, es necesario establecer la versión de SOAP y WS-Addressing las propiedades del canal.</span><span class="sxs-lookup"><span data-stu-id="bde10-117">When you manually create a service proxy for a WCF service that uses a BasicHttpBinding binding, however, it is necessary to set the SOAP version and WS-Addressing properties of the channel.</span></span> <span data-ttu-id="bde10-118">Esto se debe a que el valor predeterminado de WWSAPI es SOAP versión 1,2 y WS-Addressing 1,0.</span><span class="sxs-lookup"><span data-stu-id="bde10-118">This is because WWSAPI defaults to SOAP version 1.2 and WS-Addressing 1.0.</span></span> <span data-ttu-id="bde10-119">El BasicHttpBinding de WCF, por otro lado, usa la versión 1,1 de SOAP y no WS-Addressing.</span><span class="sxs-lookup"><span data-stu-id="bde10-119">WCF's BasicHttpBinding, on the other hand, uses SOAP version 1.1 and no WS-Addressing.</span></span>

<span data-ttu-id="bde10-120">Para establecer la versión de SOAP y WS-Addrssing las propiedades del canal, declare una matriz de estructuras de [**\_ \_ propiedades de canal de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) para que contenga las propiedades de canal y la información relacionada.</span><span class="sxs-lookup"><span data-stu-id="bde10-120">To set the SOAP version and WS-Addrssing properties of the channel, declare an array of [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) structures to hold the channel properties and related information.</span></span>


```
WS_CHANNEL_PROPERTY channelProperties[4]; // Array to hold up to 4 channel properties

ULONG channelPropertyCount = 0; // Count of properties set
 
WS_ENVELOPE_VERSION soapVersion = WS_ENVELOPE_VERSION_SOAP_1_1; // Set required SOAP version
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ENVELOPE_VERSION; // Type of first channel property
channelProperties[channelPropertyCount].value = &soapVersion; // Address of the SOAP version value
channelProperties[channelPropertyCount].valueSize = sizeof(soapVersion); // Size of the value
channelPropertyCount++; // Increment property count
 
WS_ADDRESSING_VERSION addressingVersion = WS_ADDRESSING_VERSION_TRANSPORT; // Set required WS-Addressing value
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ADDRESSING_VERSION; // Type of second channel property
channelProperties[channelPropertyCount].value = &addressingVersion ; // Address of the WS-Addressing value
channelProperties[channelPropertyCount].valueSize = sizeof(addressingVersion ); // Size of the value
channelPropertyCount++; // Increment property count
 
// add more channel properties here

```



<span data-ttu-id="bde10-121">A continuación, pase la matriz de propiedades de canal (channelProperties) y el recuento de propiedades (channelPropertyCount) a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (o [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) si está trabajando en la capa de canal).</span><span class="sxs-lookup"><span data-stu-id="bde10-121">Then pass the array of channel properties (channelProperties) and the count of properties (channelPropertyCount) to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (or [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) if you are working at channel layer).</span></span>


```
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        channelProperties, // channel properties
        channelPropertyCount, // channel property count
        &proxy, 
        error);
```



<span data-ttu-id="bde10-122">La matriz que declaró para contener las propiedades se copia en **WsCreateServiceProxy** y, como resultado, puede liberar la memoria de la matriz de propiedades inmediatamente después de llamar a la función.</span><span class="sxs-lookup"><span data-stu-id="bde10-122">The array you declared to hold the properties is copied in **WsCreateServiceProxy**, and as a result, you can free the memory for the property array immediately after calling the function.</span></span> <span data-ttu-id="bde10-123">Además, si asigna la memoria de la pila (como el fragmento de código anterior), también puede devolver desde la función inmediatamente después de la llamada.</span><span class="sxs-lookup"><span data-stu-id="bde10-123">Also, if you allocate the memory from the stack (like the code snippet above), you can also return from the function immediately after the call.</span></span>

## <a name="other-bindings"></a><span data-ttu-id="bde10-124">Otros enlaces</span><span class="sxs-lookup"><span data-stu-id="bde10-124">Other Bindings</span></span>

<span data-ttu-id="bde10-125">Además, WWSAPI proporciona mecanismos para crear proxies de servicio para comunicarse con los servicios WCF mediante otros enlaces, como NetTcpBinding y WSFederationHttpBinding.</span><span class="sxs-lookup"><span data-stu-id="bde10-125">In addition, WWSAPI provides mechanisms for creating service proxies to communicate with WCF services using other bindings, such as NetTcpBinding and WSFederationHttpBinding.</span></span> <span data-ttu-id="bde10-126">Muchos de estos enlaces requieren el establecimiento de propiedades adicionales del canal, como descriptores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bde10-126">Many of these binding require setting additional channel properties, such as security descriptors.</span></span> <span data-ttu-id="bde10-127">Para obtener ejemplos que ilustran el uso de otros enlaces, consulte la sección ejemplos de [servicios Web de Windows](windows-web-services-examples.md), en concreto los ejemplos de capas de canales [TCP](tcp-channel-layer-examples.md), ejemplos de [capas de canales http](http-channel-layer-examples.md)y [ejemplos de capas](security-channel-layer-examples.md) de canales de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bde10-127">For examples that illustrate using other bindings, see the [Windows Web Services Examples](windows-web-services-examples.md), section, in particular the [TCP Channel Layer Examples](tcp-channel-layer-examples.md), [HTTP Channel Layer Examples](http-channel-layer-examples.md), and [Security Channel Layer Examples](security-channel-layer-examples.md) subsections.</span></span>

 

 




