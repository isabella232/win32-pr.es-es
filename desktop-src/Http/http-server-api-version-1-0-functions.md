---
title: Funciones de la API del servidor HTTP versión 1,0
description: La API del servidor HTTP proporciona las siguientes funciones para escribir aplicaciones.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- Funciones de la API del servidor HTTP versión 1,0
- Functions HTTP, API del servidor HTTP versión 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050821e40695268d6e3fa2c946d2e8859748db2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269214"
---
# <a name="http-server-api-version-10-functions"></a><span data-ttu-id="a0255-105">Funciones de la API del servidor HTTP versión 1,0</span><span class="sxs-lookup"><span data-stu-id="a0255-105">HTTP Server API Version 1.0 Functions</span></span>

<span data-ttu-id="a0255-106">La API del servidor HTTP proporciona las siguientes funciones para escribir aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a0255-106">The HTTP Server API provides the following functions for writing applications.</span></span>

## <a name="general"></a><span data-ttu-id="a0255-107">General</span><span class="sxs-lookup"><span data-stu-id="a0255-107">General</span></span>



| <span data-ttu-id="a0255-108">Función</span><span class="sxs-lookup"><span data-stu-id="a0255-108">Function</span></span>                                             | <span data-ttu-id="a0255-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0255-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0255-110">**HttpCreateHttpHandle**</span><span class="sxs-lookup"><span data-stu-id="a0255-110">**HttpCreateHttpHandle**</span></span>](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | <span data-ttu-id="a0255-111">Crea una cola de solicitudes HTTP y devuelve un identificador a ella.</span><span class="sxs-lookup"><span data-stu-id="a0255-111">Creates an HTTP request queue and returns a handle to it.</span></span>                                                                         |
| [<span data-ttu-id="a0255-112">**HttpInitialize**</span><span class="sxs-lookup"><span data-stu-id="a0255-112">**HttpInitialize**</span></span>](/windows/desktop/api/Http/nf-http-httpinitialize)             | <span data-ttu-id="a0255-113">Inicializa la API del servidor HTTP para que la use el proceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="a0255-113">Initializes the HTTP Server API for use by the calling process.</span></span>                                                                   |
| [<span data-ttu-id="a0255-114">**HttpPrepareUrl**</span><span class="sxs-lookup"><span data-stu-id="a0255-114">**HttpPrepareUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpprepareurl)             | <span data-ttu-id="a0255-115">Analiza, analiza y normaliza una dirección URL Unicode o Punycode no normalizada, por lo que es segura y válida para su uso en otras funciones HTTP.</span><span class="sxs-lookup"><span data-stu-id="a0255-115">Parses, analyzes, and normalizes a non-normalized Unicode or punycode URL so it is safe and valid to use in other HTTP functions.</span></span> |
| [<span data-ttu-id="a0255-116">**HttpTerminate**</span><span class="sxs-lookup"><span data-stu-id="a0255-116">**HttpTerminate**</span></span>](/windows/desktop/api/Http/nf-http-httpterminate)               | <span data-ttu-id="a0255-117">Dirige la API del servidor HTTP para limpiar los recursos asociados a un proceso determinado.</span><span class="sxs-lookup"><span data-stu-id="a0255-117">Directs the HTTP Server API to clean up any resources associated with a particular process.</span></span>                                       |



 

## <a name="cache-management"></a><span data-ttu-id="a0255-118">Administración de caché</span><span class="sxs-lookup"><span data-stu-id="a0255-118">Cache Management</span></span>



| <span data-ttu-id="a0255-119">Función</span><span class="sxs-lookup"><span data-stu-id="a0255-119">Function</span></span>                                                       | <span data-ttu-id="a0255-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0255-120">Description</span></span>                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0255-121">**HttpAddFragmentToCache**</span><span class="sxs-lookup"><span data-stu-id="a0255-121">**HttpAddFragmentToCache**</span></span>](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | <span data-ttu-id="a0255-122">Almacena en memoria caché un fragmento de datos para que se pueda usar para crear una respuesta dinámica sin leer el disco.</span><span class="sxs-lookup"><span data-stu-id="a0255-122">Caches a data fragment so that it can be used to compose a dynamic response without reading from disk.</span></span> |
| [<span data-ttu-id="a0255-123">**HttpFlushResponseCache**</span><span class="sxs-lookup"><span data-stu-id="a0255-123">**HttpFlushResponseCache**</span></span>](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | <span data-ttu-id="a0255-124">Quita los fragmentos almacenados en caché especificados de la memoria caché HTTP.</span><span class="sxs-lookup"><span data-stu-id="a0255-124">Removes specified cached fragments from the HTTP cache.</span></span>                                                |
| [<span data-ttu-id="a0255-125">**HttpReadFragmentFromCache**</span><span class="sxs-lookup"><span data-stu-id="a0255-125">**HttpReadFragmentFromCache**</span></span>](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | <span data-ttu-id="a0255-126">Recupera un fragmento de respuesta almacenado en memoria caché especificado.</span><span class="sxs-lookup"><span data-stu-id="a0255-126">Retrieves a specified cached response fragment.</span></span>                                                        |



 

## <a name="configuration"></a><span data-ttu-id="a0255-127">Configuración</span><span class="sxs-lookup"><span data-stu-id="a0255-127">Configuration</span></span>



| <span data-ttu-id="a0255-128">Función</span><span class="sxs-lookup"><span data-stu-id="a0255-128">Function</span></span>                                                                 | <span data-ttu-id="a0255-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0255-129">Description</span></span>                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="a0255-130">**HttpDeleteServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="a0255-130">**HttpDeleteServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | <span data-ttu-id="a0255-131">Elimina la información especificada del almacén de configuración HTTP.</span><span class="sxs-lookup"><span data-stu-id="a0255-131">Deletes specified information from the HTTP configuration store.</span></span>  |
| [<span data-ttu-id="a0255-132">**HttpQueryServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="a0255-132">**HttpQueryServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | <span data-ttu-id="a0255-133">Consulta el almacén de configuración HTTP para obtener la información especificada.</span><span class="sxs-lookup"><span data-stu-id="a0255-133">Queries the HTTP configuration store for specified information.</span></span>   |
| [<span data-ttu-id="a0255-134">**HttpSetServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="a0255-134">**HttpSetServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | <span data-ttu-id="a0255-135">Establece los valores especificados en el almacén de configuración de la API del servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="a0255-135">Sets specified values in the HTTP Server API configuration store.</span></span> |



 

## <a name="input-and-output"></a><span data-ttu-id="a0255-136">Entrada y salida</span><span class="sxs-lookup"><span data-stu-id="a0255-136">Input and Output</span></span>



| <span data-ttu-id="a0255-137">Función</span><span class="sxs-lookup"><span data-stu-id="a0255-137">Function</span></span>                                                             | <span data-ttu-id="a0255-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0255-138">Description</span></span>                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="a0255-139">**HttpReceiveHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="a0255-139">**HttpReceiveHttpRequest**</span></span>](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | <span data-ttu-id="a0255-140">Recupera una solicitud HTTP de una cola de solicitudes especificada.</span><span class="sxs-lookup"><span data-stu-id="a0255-140">Retrieves an HTTP request from a specified request queue.</span></span>      |
| [<span data-ttu-id="a0255-141">**HttpReceiveRequestEntityBody**</span><span class="sxs-lookup"><span data-stu-id="a0255-141">**HttpReceiveRequestEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | <span data-ttu-id="a0255-142">Recupera los datos del cuerpo de entidad de una solicitud HTTP determinada.</span><span class="sxs-lookup"><span data-stu-id="a0255-142">Retrieves entity-body data of a particular HTTP request.</span></span>       |
| [<span data-ttu-id="a0255-143">**HttpSendHttpResponse**</span><span class="sxs-lookup"><span data-stu-id="a0255-143">**HttpSendHttpResponse**</span></span>](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | <span data-ttu-id="a0255-144">Envía una respuesta HTTP para una solicitud HTTP determinada.</span><span class="sxs-lookup"><span data-stu-id="a0255-144">Sends an HTTP response for a particular HTTP request.</span></span>          |
| [<span data-ttu-id="a0255-145">**HttpSendResponseEntityBody**</span><span class="sxs-lookup"><span data-stu-id="a0255-145">**HttpSendResponseEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | <span data-ttu-id="a0255-146">Envía datos de cuerpo de entidad de una respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="a0255-146">Sends entity-body data of an HTTP response.</span></span>                    |
| [<span data-ttu-id="a0255-147">**HttpWaitForDisconnect**</span><span class="sxs-lookup"><span data-stu-id="a0255-147">**HttpWaitForDisconnect**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | <span data-ttu-id="a0255-148">Notifica a la aplicación cuando un cliente HTTP se ha desconectado.</span><span class="sxs-lookup"><span data-stu-id="a0255-148">Notifies the application when an HTTP client has disconnected.</span></span> |



 

## <a name="ssl"></a><span data-ttu-id="a0255-149">SSL</span><span class="sxs-lookup"><span data-stu-id="a0255-149">SSL</span></span>



| <span data-ttu-id="a0255-150">Función</span><span class="sxs-lookup"><span data-stu-id="a0255-150">Function</span></span>                                                             | <span data-ttu-id="a0255-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0255-151">Description</span></span>                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="a0255-152">**HttpReceiveClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="a0255-152">**HttpReceiveClientCertificate**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | <span data-ttu-id="a0255-153">Recupera el certificado de cliente para una conexión SSL.</span><span class="sxs-lookup"><span data-stu-id="a0255-153">Retrieves the client certificate for an SSL connection.</span></span> |



 

## <a name="url-registration"></a><span data-ttu-id="a0255-154">Registro de direcciones URL</span><span class="sxs-lookup"><span data-stu-id="a0255-154">URL Registration</span></span>



| <span data-ttu-id="a0255-155">Función</span><span class="sxs-lookup"><span data-stu-id="a0255-155">Function</span></span>                               | <span data-ttu-id="a0255-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0255-156">Description</span></span>                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0255-157">**HttpAddUrl**</span><span class="sxs-lookup"><span data-stu-id="a0255-157">**HttpAddUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurl)       | <span data-ttu-id="a0255-158">Registra una dirección URL para que las solicitudes HTTP correspondientes se enruten a una cola de solicitudes especificada.</span><span class="sxs-lookup"><span data-stu-id="a0255-158">Registers a URL so that HTTP requests for it are routed to a specified request queue.</span></span>           |
| [<span data-ttu-id="a0255-159">**HttpRemoveUrl**</span><span class="sxs-lookup"><span data-stu-id="a0255-159">**HttpRemoveUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurl) | <span data-ttu-id="a0255-160">Anula el registro de una dirección URL especificada, de modo que las solicitudes para ella ya no se enruten a una cola especificada.</span><span class="sxs-lookup"><span data-stu-id="a0255-160">Unregisters a specified URL, so that requests for it are no longer routed to a specified queue.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a0255-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0255-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0255-162">Estructuras 1,0 de la API del servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="a0255-162">HTTP Server API Version 1.0 Structures</span></span>](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




