---
description: 'Uso de equipos con revolución HTTP: permite a los usuarios usar un explorador Web para facilitar el acceso a la información de un servidor remoto a través de una red.'
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: Introducción al servicio SOAP de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93ce7d80753f306777d3ac0b77dc46dc4e08d22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666189"
---
# <a name="com-soap-service-overview"></a><span data-ttu-id="7a96a-103">Introducción al servicio SOAP de COM+</span><span class="sxs-lookup"><span data-stu-id="7a96a-103">COM+ SOAP Service Overview</span></span>

<span data-ttu-id="7a96a-104">Uso de equipos con revolución HTTP: permite a los usuarios usar un explorador Web para facilitar el acceso a la información de un servidor remoto a través de una red.</span><span class="sxs-lookup"><span data-stu-id="7a96a-104">HTTP revolutionized computer use by allowing people to use a Web browser for easy access to information on a remote server over a network.</span></span> <span data-ttu-id="7a96a-105">Los servicios Web XML ahora han revolucionado el desarrollo de aplicaciones, ya que permiten a las aplicaciones cliente llamar fácilmente a métodos remotos a través de una red.</span><span class="sxs-lookup"><span data-stu-id="7a96a-105">XML web services have now revolutionized application development by allowing client applications to easily call remote methods over a network.</span></span>

<span data-ttu-id="7a96a-106">A menudo resulta útil que una aplicación cliente pueda llamar a un método implementado en un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="7a96a-106">It is often useful for a client application to be able to call a method implemented on a remote server.</span></span> <span data-ttu-id="7a96a-107">A veces, el método usa la información volátil almacenada en el servidor remoto (por ejemplo, un método que devuelve el precio actual de las acciones correspondientes a un símbolo de indicador determinado).</span><span class="sxs-lookup"><span data-stu-id="7a96a-107">Sometimes the method makes use of volatile information stored on the remote server (for example, a method that returns the current price of the stock corresponding to a given ticker symbol).</span></span> <span data-ttu-id="7a96a-108">En otras ocasiones, el desarrollador desea tener la capacidad de actualizar la implementación de los métodos sin tener que volver a implementar todas las aplicaciones que lo usan.</span><span class="sxs-lookup"><span data-stu-id="7a96a-108">At other times, the developer wants the ability to upgrade the methods implementation without having to redeploy all the applications that use it.</span></span>

<span data-ttu-id="7a96a-109">Al igual que las páginas web, se tiene acceso a los servicios Web XML a través de un servidor Web, como IIS, mediante HTTP.</span><span class="sxs-lookup"><span data-stu-id="7a96a-109">Like webpages, XML web services are accessed via a web server, such as IIS, using HTTP.</span></span> <span data-ttu-id="7a96a-110">Sin embargo, en lugar de las páginas web codificadas en HTML, estos paquetes HTTP contienen los parámetros de entrada y salida de las llamadas a un método implementado en el servidor, codificados en SOAP.</span><span class="sxs-lookup"><span data-stu-id="7a96a-110">However, instead of webpages encoded in HTML, these HTTP packets contain the input and output parameters of calls to a method implemented on the server, encoded in SOAP.</span></span>

<span data-ttu-id="7a96a-111">Para usar un servicio Web XML, debe conocer la dirección URL en la que se expone el servicio y el nombre del método al que desea llamar, y debe proporcionar los parámetros de entrada al método.</span><span class="sxs-lookup"><span data-stu-id="7a96a-111">To use an XML web service, you need to know the URL where the service is exposed and the name of the method you want to call, and you must provide the input parameters to the method.</span></span> <span data-ttu-id="7a96a-112">[El estándar SOAP 1,1](https://www.w3.org/TR/SOAP/) proporciona el siguiente ejemplo de un paquete http que contiene una llamada remota a un servicio Web XML en https://www.stockquoteserver.com/StockQuote , que devuelve el precio actual de las acciones correspondientes a un símbolo de indicador determinado.</span><span class="sxs-lookup"><span data-stu-id="7a96a-112">[The SOAP 1.1 standard](https://www.w3.org/TR/SOAP/) provides the following example of an HTTP packet containing a remote call to an XML web service at https://www.stockquoteserver.com/StockQuote, which returns the current price of the stock corresponding to a given ticker symbol.</span></span>

``` syntax
POST /StockQuote HTTP/1.1
Host: www.stockquoteserver.com
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn
SOAPAction: "Some-URI"

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding/">
<SOAP-ENV:Body>
<m:GetLastTradePrice xmlns:m="Some-URI">
<symbol>DIS</symbol>
</m:GetLastTradePrice>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="7a96a-113">Como se muestra en el ejemplo anterior, SOAP es una instancia de XML que se puede incrustar en una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="7a96a-113">As the preceding example illustrates, SOAP is an XML instance that can be embedded in an HTTP request.</span></span> <span data-ttu-id="7a96a-114">Del mismo modo, el resultado se devuelve como un paquete HTTP con una carga de SOAP, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="7a96a-114">Similarly, the result is returned as an HTTP packet with a SOAP payload, as shown in the following example.</span></span>

``` syntax
HTTP/1.1 200 OK
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding//">
<SOAP-ENV:Body>
<m:GetLastTradePriceResponse xmlns:m="Some-URI">
<Price>34.5</Price>
</m:GetLastTradePriceResponse>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="7a96a-115">Aunque es útil conocer la infraestructura que subyace a los servicios Web XML, COM+ facilita la creación y el uso de servicios Web XML que no suele tener que profundizar en este nivel.</span><span class="sxs-lookup"><span data-stu-id="7a96a-115">While it is helpful to have some understanding of the infrastructure that underlies XML web services, COM+ makes it so easy to create and use XML web services that you won't often have to delve to this level.</span></span>

<span data-ttu-id="7a96a-116">Puede exponer los métodos de las interfaces predeterminadas de los componentes COM configurados en cualquier aplicación COM+ como un servicio Web XML.</span><span class="sxs-lookup"><span data-stu-id="7a96a-116">You can expose the methods in the default interfaces of the configured COM components in any COM+ application as an XML web service.</span></span> <span data-ttu-id="7a96a-117">No es necesario tener en cuenta ninguna consideración de programación especial al escribir los componentes de, salvo que los métodos que desea exponer deben estar en la interfaz predeterminada y el componente debe estar configurado (en el catálogo de COM+ del servidor).</span><span class="sxs-lookup"><span data-stu-id="7a96a-117">No special programming considerations are necessary when writing the components, except that the methods you want to expose must be in the default interface and the component must be configured (in your server's COM+ catalog).</span></span> <span data-ttu-id="7a96a-118">No es necesario escribir código para comunicarse a través de una interfaz de red o para analizar SOAP.</span><span class="sxs-lookup"><span data-stu-id="7a96a-118">You need not write code to communicate via a network interface or to parse SOAP.</span></span> <span data-ttu-id="7a96a-119">Para obtener instrucciones detalladas acerca del uso del servicio SOAP de COM+ para crear un servicio Web XML, vea [crear servicios Web XML](creating-xml-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="7a96a-119">For detailed instructions about using the COM+ SOAP service to create an XML web service, see [Creating XML Web Services](creating-xml-web-services.md).</span></span>

<span data-ttu-id="7a96a-120">Al exponer una aplicación COM+ como un servicio Web XML, se publica automáticamente información detallada acerca de la sintaxis de todos los métodos disponibles en un servicio Web XML mediante el lenguaje de descripción de servicios web (WSDL).</span><span class="sxs-lookup"><span data-stu-id="7a96a-120">When you expose a COM+ application as an XML web service, detailed information about the syntax of all the methods available from an XML web service is published automatically, using the Web Services Description Language (WSDL).</span></span> <span data-ttu-id="7a96a-121">Esta información la usan los clientes que usan el servicio Web XML.</span><span class="sxs-lookup"><span data-stu-id="7a96a-121">This information is used by clients that use your XML web service.</span></span>

<span data-ttu-id="7a96a-122">COM+ proporciona dos maneras de obtener acceso y utilizar un servicio Web XML remoto, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="7a96a-122">COM+ provides two ways for you to access and use a remote XML web service, as follows:</span></span>

-   <span data-ttu-id="7a96a-123">El modo *de objeto conocido* (WKO) se puede utilizar para tener acceso a cualquier servicio Web XML que publique su sintaxis mediante WSDL, incluso si ese servicio Web XML no se creó con com+ o incluso Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7a96a-123">The *well-known object* (WKO) mode can be used to access any XML web service that publishes its syntax using WSDL, even if that XML web service was not created using COM+ or even Microsoft Windows.</span></span>
-   <span data-ttu-id="7a96a-124">El modo *objeto activado* en el cliente (CaO) solo se puede utilizar para tener acceso a los servicios Web XML creados mediante la exposición de aplicaciones com+.</span><span class="sxs-lookup"><span data-stu-id="7a96a-124">The *client-activated object* (CAO) mode can be used only to access XML web services created by exposing COM+ applications.</span></span> <span data-ttu-id="7a96a-125">El modo CAO aumenta el rendimiento mediante el uso de conexiones persistentes, una característica no admitida por el estándar SOAP actual.</span><span class="sxs-lookup"><span data-stu-id="7a96a-125">CAO mode increases performance by using persistent connections, a feature not supported by the current SOAP standard.</span></span>

<span data-ttu-id="7a96a-126">Ambos métodos permiten a las aplicaciones cliente llamar a los métodos de servicios Web XML de forma remota de un modo sencillo, sin tener que escribir código para comunicarse a través de una interfaz de red o analizar SOAP.</span><span class="sxs-lookup"><span data-stu-id="7a96a-126">Both methods allow client applications to call the methods of XML web services remotely in a straightforward fashion, without having to write code to communicate via a network interface or parse SOAP.</span></span> <span data-ttu-id="7a96a-127">Para obtener más información sobre cómo obtener acceso a los servicios Web XML en cualquier modo, vea obtener acceso a los servicios [Web XML en modo de Cao](accessing-xml-web-services-in-cao-mode.md) y [obtener acceso a los servicios Web XML en el modo WKO](accessing-xml-web-services-in-wko-mode.md).</span><span class="sxs-lookup"><span data-stu-id="7a96a-127">For details about how to access XML web services in either mode, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md) and [Accessing XML Web Services in WKO Mode](accessing-xml-web-services-in-wko-mode.md).</span></span>

> [!Note]  
> <span data-ttu-id="7a96a-128">COM+ solo admite la especificación SOAP-RPC, no la especificación SOAP-Document.</span><span class="sxs-lookup"><span data-stu-id="7a96a-128">COM+ supports only the SOAP-RPC specification, not the SOAP-Document specification.</span></span>

 

<span data-ttu-id="7a96a-129">COM+ facilita el uso de servicios Web XML, ya que permite usar aplicaciones COM+ existentes como servicios Web XML en el modo de CAO de una manera completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="7a96a-129">COM+ makes using XML web services especially easy by allowing you to use existing COM+ applications as XML web services in CAO mode in a completely transparent fashion.</span></span> <span data-ttu-id="7a96a-130">Si [exporta](exporting-a-soap-enabled-application.md) una aplicación com+ que se ha expuesto como un servicio Web XML desde su servidor, cualquier cliente que [importe](importing-a-soap-enabled-application.md) la aplicación puede usar de forma transparente el servicio Web XML del servidor siempre que se use la aplicación importada.</span><span class="sxs-lookup"><span data-stu-id="7a96a-130">If you [export](exporting-a-soap-enabled-application.md) a COM+ application that has been exposed as an XML web service from your server, any client that [imports](importing-a-soap-enabled-application.md) the application can transparently use the server's XML web service whenever the imported application is used.</span></span> <span data-ttu-id="7a96a-131">Esta característica hace que la conversión de las aplicaciones COM+ existentes en servicios Web XML y la implementación de esos servicios a través de una red sea muy sencilla.</span><span class="sxs-lookup"><span data-stu-id="7a96a-131">This facility makes the conversion of existing COM+ applications to XML web services and the deployment of those services over a network very easy.</span></span>

<span data-ttu-id="7a96a-132">El uso de servicios Web XML tiene varias ventajas exclusivas sobre implementaciones alternativas de llamadas a procedimientos remotos (RPC), entre las que se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="7a96a-132">Using XML web services has several unique advantages over alternative implementations of remote procedure calls (RPC), including the following:</span></span>

-   <span data-ttu-id="7a96a-133">SOAP es una verdadera implementación de RPC multiplataforma, lo que aumenta la interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="7a96a-133">SOAP is a true cross-platform RPC implementation, which increases interoperability.</span></span>
-   <span data-ttu-id="7a96a-134">Los servicios Web XML admiten métodos con parámetros de entrada y de salida.</span><span class="sxs-lookup"><span data-stu-id="7a96a-134">XML web services support methods with both input and output parameters.</span></span>
-   <span data-ttu-id="7a96a-135">Los servicios Web XML se ejecutan a través de HTTP, que normalmente pueden penetrar en firewalls que podrían bloquear otras implementaciones de RPC.</span><span class="sxs-lookup"><span data-stu-id="7a96a-135">XML web services run over HTTP, which can usually penetrate firewalls that might block other RPC implementations.</span></span>
-   <span data-ttu-id="7a96a-136">Cuando se implementa un servicio Web XML mediante COM+, el desarrollador no tiene que escribir ningún código especializado; Esta es una gran ventaja sobre los mecanismos de RPC alternativos.</span><span class="sxs-lookup"><span data-stu-id="7a96a-136">When an XML web service is implemented using COM+, the developer does not have to write any specialized code; this is a tremendous advantage over alternative RPC mechanisms.</span></span>

> [!Note]  
> <span data-ttu-id="7a96a-137">Los servicios Web XML no admiten llamadas transaccionales asincrónicas o de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="7a96a-137">XML web services do not support asynchronous or transparently transactional calls.</span></span> <span data-ttu-id="7a96a-138">Use el servicio de [componentes en cola de com+](com--queued-components.md) cuando necesite esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="7a96a-138">Use the [COM+ Queued Components](com--queued-components.md) service when you require this functionality.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7a96a-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a96a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a96a-140">Consideraciones de seguridad del servicio SOAP de COM+</span><span class="sxs-lookup"><span data-stu-id="7a96a-140">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



