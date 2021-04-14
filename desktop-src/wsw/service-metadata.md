---
title: Metadatos de servicio
description: El host de servicio WWSAPI admite WS-MetadataExchange para sus extremos.
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- Metadatos de servicio nativos-Web-Services
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488567"
---
# <a name="service-metadata"></a><span data-ttu-id="41fb2-106">Metadatos de servicio</span><span class="sxs-lookup"><span data-stu-id="41fb2-106">Service Metadata</span></span>

<span data-ttu-id="41fb2-107">El host de servicio WWSAPI admite WS-MetadataExchange para sus extremos.</span><span class="sxs-lookup"><span data-stu-id="41fb2-107">The WWSAPI service host supports WS-MetadataExchange for its endpoints.</span></span> <span data-ttu-id="41fb2-108">Habilite este intercambio de metadatos en el host de servicio con los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="41fb2-108">You enable such metadata exchange on the service host with the following steps:</span></span>

-   <span data-ttu-id="41fb2-109">Especifique los documentos de metadatos en la propiedad de [**\_ \_ metadatos del servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) en el [ \_ \_ host del servicio WS](ws-service-host.md).</span><span class="sxs-lookup"><span data-stu-id="41fb2-109">Specify metadata documents in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="41fb2-110">Especifique el nombre del servicio en la propiedad de [**\_ \_ metadatos del servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) en el [ \_ \_ host del servicio WS](ws-service-host.md).</span><span class="sxs-lookup"><span data-stu-id="41fb2-110">Specify the service name in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="41fb2-111">Especifique el puerto para los puntos de conexión individuales mediante la propiedad de [**\_ \_ \_ \_ metadatos de la propiedad de punto de conexión de servicio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) en el [**\_ \_ extremo del servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="41fb2-111">Specify the port for individual endpoints by using the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>
-   <span data-ttu-id="41fb2-112">Habilite una o varias estructuras de [**\_ \_ extremos de servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) para atender las solicitudes de WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="41fb2-112">Enable one or more [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures to service the WS-MetadataExchange requests.</span></span>
-   <span data-ttu-id="41fb2-113">Opcionalmente, especifique el sufijo de la **\_ \_ \_ \_ \_ \_ dirección URL de \_ intercambio de metadatos de la propiedad de punto de conexión de WS Service** en la enumeración identificador de la [**\_ \_ \_ propiedad \_ de punto de conexión de servicio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) para atender solicitudes Ws-MetadataExchange en una dirección</span><span class="sxs-lookup"><span data-stu-id="41fb2-113">Optionally, specify **WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA\_EXCHANGE\_URL\_SUFFIX** in the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) enumeration for servicing Ws-MetadataExchange requests on a specific address.</span></span>


<span data-ttu-id="41fb2-114">Especificación de documentos de metadatos/nombre de servicio en el host de servicio</span><span class="sxs-lookup"><span data-stu-id="41fb2-114">Specifying Metadata documents / Service name on the Service Host</span></span>

<span data-ttu-id="41fb2-115">El primer paso es especificar los documentos de metadatos en el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="41fb2-115">The first step is to specify the metadata documents on the service host.</span></span> <span data-ttu-id="41fb2-116">Para ello, recopile los documentos individuales como una matriz de las \_ cadenas XML de WS \_ \* .</span><span class="sxs-lookup"><span data-stu-id="41fb2-116">Do this by gathering the individual documents as an array of WS\_XML\_STRING\*'s.</span></span> <span data-ttu-id="41fb2-117">Estas cadenas pueden ser esquemas XML, WSDL o WS-Policy documento.</span><span class="sxs-lookup"><span data-stu-id="41fb2-117">These strings can be XML Schema, WSDL or WS-Policy document.</span></span> <span data-ttu-id="41fb2-118">Esto se especifica mediante la [**propiedad \_ \_ \_ metadatos de la propiedad de servicio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .</span><span class="sxs-lookup"><span data-stu-id="41fb2-118">This is specified through the [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span>

<span data-ttu-id="41fb2-119">Opcionalmente, una aplicación también puede especificar el nombre del servicio y el espacio de nombres como parte de los [**\_ \_ metadatos del servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata).</span><span class="sxs-lookup"><span data-stu-id="41fb2-119">Optionally, an application can also specify the service name and namespace as part of the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata).</span></span> <span data-ttu-id="41fb2-120">Si el documento de metadatos no especifica el elemento de servicio para el nombre de servicio determinado, el modelo de servicio generará un elemento de servicio con los puertos WSDL correspondientes para el servicio.</span><span class="sxs-lookup"><span data-stu-id="41fb2-120">If the metadata document does not specify the service element for the given service name, the service model will generate a service element with the corresponding WSDL ports for the service.</span></span>

``` syntax
WS_SERVICE_METADATA_DOCUMENT document = {0};
WS_STRING documentName = WS_STRING_VALUE(L&quot;a.wsdl&quot;);
document.name = &documentName;
document.content = &wsdlDocument
WS_SERVICE_METADATA_DOCUMENT** metadataDocuments [] = {&document};
WS_SERVICE_METADATA serviceMetadata = {0};
// Specify Metadata documents
serviceMetadata.count = WsCountOf(metadataDocuments);
serviceMetadata.documents = &metadataDocuments;
// Specify service name
serviceMetadata.serviceName = &serviceName;
serviceMetadata.serviceNs = &serviceNamespace;


WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_METADATA;
serviceProperties[0].value =  &serviceMetadata;
serviceProperties[0].ValueSize = sizeof(serviceMetadata);
```

<span data-ttu-id="41fb2-121">Tenga en cuenta que no se realizará ninguna comprobación de los documentos de metadatos individuales en los documentos.</span><span class="sxs-lookup"><span data-stu-id="41fb2-121">Note that no verification of the individual metadata documents will be performed on the documents.</span></span> <span data-ttu-id="41fb2-122">Es responsabilidad de la aplicación validar el contenido de los documentos y asegurarse de que todas las rutas de acceso de las importaciones se especifican de forma relativa.</span><span class="sxs-lookup"><span data-stu-id="41fb2-122">It is the responsiblity of the application to validate contents of the documents and ensure that all the imports paths are relatively specified.</span></span>

<span data-ttu-id="41fb2-123">El espacio de nombres especificado se utiliza para buscar el documento en el que el host de servicio agregará el elemento de servicio.</span><span class="sxs-lookup"><span data-stu-id="41fb2-123">The namespace specified is used to locate the document in which the service element will be added by the service host.</span></span>

<span data-ttu-id="41fb2-124">Adición del elemento de servicio al documento WSDL</span><span class="sxs-lookup"><span data-stu-id="41fb2-124">Addition of service element to the WSDL document</span></span>

<span data-ttu-id="41fb2-125">El host de servicio proporciona el recurso para que la aplicación agregue un elemento de servicio en su nombre si aún no se ha especificado ninguno.</span><span class="sxs-lookup"><span data-stu-id="41fb2-125">The service host provides facility for the application to add a service element on its behalf if one is not already specified.</span></span> <span data-ttu-id="41fb2-126">Para habilitar este comportamiento, una aplicación debe especificar los campos serivceName y servicens en la estructura de [**\_ \_ metadatos del servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) .</span><span class="sxs-lookup"><span data-stu-id="41fb2-126">In order to enable this behavior an application must specify serivceName and serviceNs fields on the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) structure.</span></span> <span data-ttu-id="41fb2-127">Si serviceName y servicens son **null** , no se agrega ningún elemento de servicio al documento WSDL.</span><span class="sxs-lookup"><span data-stu-id="41fb2-127">If serviceName and serviceNs are both **NULL** no service element is added to the WSDL document.</span></span> <span data-ttu-id="41fb2-128">Ambos se usan para identificar el documento en el que se va a agregar el serviceElement.</span><span class="sxs-lookup"><span data-stu-id="41fb2-128">Both these are used to identify document in which the serviceElement is going to be added.</span></span>

<span data-ttu-id="41fb2-129">Si no se especifica la propiedad de [**\_ \_ \_ metadatos de la propiedad de servicio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) , no se producirá ningún metadato en el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="41fb2-129">If [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property is not specified no metadata exhange will take place on the service host.</span></span>

<span data-ttu-id="41fb2-130">Especificar el puerto en el extremo del \_ servicio \_ WS</span><span class="sxs-lookup"><span data-stu-id="41fb2-130">Specifying the port on the WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="41fb2-131">Para que [**un \_ punto de \_ conexión de servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) esté disponible como un puerto dentro del elemento de servicio en el documento WSDL, la aplicación debe especificar en él la propiedad de [**\_ \_ \_ \_ metadatos de la propiedad de punto de conexión de servicio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) .</span><span class="sxs-lookup"><span data-stu-id="41fb2-131">For a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) to be available as a port inside the service element in the WSDL document, the application must specify [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on it.</span></span>

``` syntax
WS_SERVICE_ENDPOINT_METADATA endpointPort = {0}
endpointPort.name = &portName;
endpointPort.bindingName = &bindingName;
endpointPort.bindingNs = &bindingNs;

WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA;
serviceProperties[0].value =  &endpointPort;
serviceProperties[0].valueSize = sizeof(endpointPort);
```

<span data-ttu-id="41fb2-132">Se supone que la referencia al nombre de enlace y espacio de nombres existe en los documentos especificados en el host de servicio como parte de los metadatos de la propiedad de servicio de WS \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="41fb2-132">It is assumed that the reference to the binding name and namespace exists in the documents specified on the service host as part of WS\_SERVICE\_PROPERTY\_METADATA.</span></span> <span data-ttu-id="41fb2-133">El tiempo de ejecución no lo comprueba en nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41fb2-133">The runtime does not verify this on behalf of the application.</span></span>

<span data-ttu-id="41fb2-134">Habilitar el servicio de WS-MetadataExchange en el punto de conexión de \_ servicio WS \_</span><span class="sxs-lookup"><span data-stu-id="41fb2-134">Enable WS-MetadataExchange servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="41fb2-135">Para atender las solicitudes de WS-MetadataExchange, el host del servicio debe tener al menos un punto de conexión habilitado para atender las solicitudes de WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="41fb2-135">In order to service WS-MetadataExchange requests,the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="41fb2-136">Esto se hace estableciendo la versión adecuada para WS-MetadataExchange en el [**extremo del \_ servicio \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="41fb2-136">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="41fb2-137">Habilitar el servicio GET de HTTP en el punto de conexión de \_ servicio WS \_</span><span class="sxs-lookup"><span data-stu-id="41fb2-137">Enable HTTP GET servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="41fb2-138">Para serviceHTTP solicitudes GET, el host del servicio debe tener al menos un punto de conexión habilitado para atender las solicitudes de WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="41fb2-138">In order to serviceHTTP GET requests, the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="41fb2-139">Esto se hace estableciendo la versión adecuada para WS-MetadataExchange en el [**extremo del \_ servicio \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="41fb2-139">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="41fb2-140">Especificar el sufijo de dirección URL para solicitudes de Ws-MetadataExchange</span><span class="sxs-lookup"><span data-stu-id="41fb2-140">Specifying URL suffix for Ws-MetadataExchange requests</span></span>

<span data-ttu-id="41fb2-141">Opcionalmente, una aplicación puede habilitar solo aceptar solicitudes de WS-MetadataExchange en una ruta de acceso específica.</span><span class="sxs-lookup"><span data-stu-id="41fb2-141">An application can optionally enable only accepting requests for WS-MetadataExchange on a specific path.</span></span> <span data-ttu-id="41fb2-142">Esto se hace especificando un sufijo para el punto de conexión de servicio de WS determinado \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="41fb2-142">This is done by specifying a suffix for the given WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="41fb2-143">Este sufijo se concatena tal cual con la dirección URL real del punto de conexión de servicio de WS \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="41fb2-143">This suffix is concatenated as-is to the actual URL for the WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="41fb2-144">La cadena concatenada se utiliza como la dirección URL correspondiente al encabezado ' to ' recibido.</span><span class="sxs-lookup"><span data-stu-id="41fb2-144">The concatenated string is used as the matching URL to the 'to' header received.</span></span>

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

<span data-ttu-id="41fb2-145">Los siguientes elementos de la API se relacionan con el servicio basan.</span><span class="sxs-lookup"><span data-stu-id="41fb2-145">The following API elements relate to service metada.</span></span>

| <span data-ttu-id="41fb2-146">Enumeración</span><span class="sxs-lookup"><span data-stu-id="41fb2-146">Enumeration</span></span>                                                       | <span data-ttu-id="41fb2-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="41fb2-147">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="41fb2-148">**\_tipo de intercambio de metadatos de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41fb2-148">**WS\_METADATA\_EXCHANGE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | <span data-ttu-id="41fb2-149">Habilita o deshabilita WS-MetadataExchange y el servicio GET de HTTP en el punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="41fb2-149">Enables or disables WS-MetadataExchange and HTTP GET servicing on the endpoint.</span></span> |



 



| <span data-ttu-id="41fb2-150">Estructura</span><span class="sxs-lookup"><span data-stu-id="41fb2-150">Structure</span></span>                                                               | <span data-ttu-id="41fb2-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="41fb2-151">Description</span></span>                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="41fb2-152">**metadatos de \_ punto de conexión de servicio WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41fb2-152">**WS\_SERVICE\_ENDPOINT\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | <span data-ttu-id="41fb2-153">Representa el elemento Port para el extremo.</span><span class="sxs-lookup"><span data-stu-id="41fb2-153">Represents the port element for the endpoint.</span></span>                         |
| [<span data-ttu-id="41fb2-154">**metadatos del \_ servicio WS \_**</span><span class="sxs-lookup"><span data-stu-id="41fb2-154">**WS\_SERVICE\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | <span data-ttu-id="41fb2-155">Especifica la matriz de documentos de metadatos de servicio.</span><span class="sxs-lookup"><span data-stu-id="41fb2-155">Specifies the service metadata documents array.</span></span>                       |
| [<span data-ttu-id="41fb2-156">**\_documento de \_ metadatos del servicio WS \_**</span><span class="sxs-lookup"><span data-stu-id="41fb2-156">**WS\_SERVICE\_METADATA\_DOCUMENT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | <span data-ttu-id="41fb2-157">Especifica los documentos individuales que componen los metadatos del servicio.</span><span class="sxs-lookup"><span data-stu-id="41fb2-157">Specifies the individual documents that make up the service metadata.</span></span> |



 

 

 




