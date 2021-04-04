---
description: Los servicios HTTP de Microsoft Windows (WinHTTP) exponen un conjunto de funciones de C/C++ que permiten a la aplicación tener acceso a recursos HTTP en la Web. En este tema se proporciona información general sobre cómo se usan estas funciones para interactuar con un servidor HTTP.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Información general sobre las sesiones de WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98dc8116dff75f279b87cb5f5ee6af607034176f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154316"
---
# <a name="winhttp-sessions-overview"></a><span data-ttu-id="8c2e0-104">Información general sobre las sesiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="8c2e0-104">WinHTTP Sessions Overview</span></span>

<span data-ttu-id="8c2e0-105">Los servicios HTTP de Microsoft Windows (WinHTTP) exponen un conjunto de funciones de C/C++ que permiten a la aplicación tener acceso a recursos HTTP en la Web.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-105">The Microsoft Windows HTTP Services (WinHTTP) exposes a set of C/C++ functions that enable your application to access HTTP resources on the Web.</span></span> <span data-ttu-id="8c2e0-106">En este tema se proporciona información general sobre cómo se usan estas funciones para interactuar con un servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-106">This topic provides an overview of how these functions are used to interact with an HTTP server.</span></span>

-   [<span data-ttu-id="8c2e0-107">Uso de la API de WinHTTP para tener acceso a la web</span><span class="sxs-lookup"><span data-stu-id="8c2e0-107">Using the WinHTTP API to Access the Web</span></span>](#using-the-winhttp-api-to-access-the-web)
-   [<span data-ttu-id="8c2e0-108">Inicializando WinHTTP</span><span class="sxs-lookup"><span data-stu-id="8c2e0-108">Initializing WinHTTP</span></span>](#initializing-winhttp)
-   [<span data-ttu-id="8c2e0-109">Abrir una solicitud</span><span class="sxs-lookup"><span data-stu-id="8c2e0-109">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="8c2e0-110">Agregar encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8c2e0-110">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="8c2e0-111">Envío de una solicitud</span><span class="sxs-lookup"><span data-stu-id="8c2e0-111">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="8c2e0-112">Publicar datos en el servidor</span><span class="sxs-lookup"><span data-stu-id="8c2e0-112">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="8c2e0-113">Obtención de información acerca de una solicitud</span><span class="sxs-lookup"><span data-stu-id="8c2e0-113">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="8c2e0-114">Descargar recursos de la web</span><span class="sxs-lookup"><span data-stu-id="8c2e0-114">Downloading Resources from the Web</span></span>](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a><span data-ttu-id="8c2e0-115">Uso de la API de WinHTTP para tener acceso a la web</span><span class="sxs-lookup"><span data-stu-id="8c2e0-115">Using the WinHTTP API to Access the Web</span></span>

<span data-ttu-id="8c2e0-116">En el diagrama siguiente se muestra el orden en el que normalmente se llama a las funciones WinHTTP al interactuar con un servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-116">The following diagram shows the order in which WinHTTP functions are typically called when interacting with an HTTP server.</span></span> <span data-ttu-id="8c2e0-117">Los cuadros sombreados representan funciones que generan un identificador [HINTERNET](hinternet-handles-in-winhttp.md) , mientras que los cuadros simples representan funciones que utilizan esos controladores.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-117">The shaded boxes represent functions that generate an [HINTERNET](hinternet-handles-in-winhttp.md) handle, while the plain boxes represent functions that use those handles.</span></span>

![funciones que crean identificadores](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a><span data-ttu-id="8c2e0-119">Inicializando WinHTTP</span><span class="sxs-lookup"><span data-stu-id="8c2e0-119">Initializing WinHTTP</span></span>

<span data-ttu-id="8c2e0-120">Antes de interactuar con un servidor, se debe inicializar WinHTTP llamando a [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen).</span><span class="sxs-lookup"><span data-stu-id="8c2e0-120">Before interacting with a server, WinHTTP must be initialized by calling [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen).</span></span> <span data-ttu-id="8c2e0-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) crea un contexto de sesión para mantener los detalles sobre la sesión http y devuelve un identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) creates a session context to maintain details about the HTTP session, and returns a session handle.</span></span> <span data-ttu-id="8c2e0-122">Con este identificador, la función [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) puede especificar un servidor http o de protocolo seguro de transferencia de hipertexto (https) de destino.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-122">Using this handle, the [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) function is then able to specify a target HTTP or Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

> [!Note]  
> <span data-ttu-id="8c2e0-123">Una llamada a [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) no produce una conexión real con el servidor http hasta que se realiza una solicitud para un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-123">A call to [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) does not result in an actual connection to the HTTP server until a request is made for a specific resource.</span></span>

 

## <a name="opening-a-request"></a><span data-ttu-id="8c2e0-124">Abrir una solicitud</span><span class="sxs-lookup"><span data-stu-id="8c2e0-124">Opening a Request</span></span>

<span data-ttu-id="8c2e0-125">La función [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) abre una solicitud HTTP para un recurso determinado y devuelve un identificador [HINTERNET](hinternet-handles-in-winhttp.md) que pueden usar las otras funciones http.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-125">The [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function opens an HTTP request for a particular resource and returns an [HINTERNET](hinternet-handles-in-winhttp.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="8c2e0-126">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) no envía la solicitud al servidor cuando se le llama.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-126">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) does not send the request to the server when called.</span></span> <span data-ttu-id="8c2e0-127">La función [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) establece realmente una conexión a través de la red y envía la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-127">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function actually establishes a connection over the network and sends the request.</span></span>

<span data-ttu-id="8c2e0-128">En el ejemplo siguiente se muestra una llamada de ejemplo a [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) que usa las opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-128">The following example shows a sample call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) that uses the default options.</span></span>

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a><span data-ttu-id="8c2e0-129">Agregar encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8c2e0-129">Adding Request Headers</span></span>

<span data-ttu-id="8c2e0-130">La función [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) permite a una aplicación anexar encabezados de solicitud de formato libre adicionales al identificador de la solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-130">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function allows an application to append additional free-format request headers to the HTTP request handle.</span></span> <span data-ttu-id="8c2e0-131">Está diseñado para aplicaciones sofisticadas que requieren un control preciso de las solicitudes enviadas al servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-131">It is intended for use by sophisticated applications that require precise control over the requests sent to the HTTP server.</span></span>

<span data-ttu-id="8c2e0-132">La función [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) requiere un identificador de solicitud HTTP creado por [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), una cadena que contiene los encabezados, la longitud de los encabezados y los modificadores.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-132">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function requires an HTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), a string that contains the headers, the length of the headers, and any modifiers.</span></span>

<span data-ttu-id="8c2e0-133">Los modificadores siguientes se pueden usar con [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span><span class="sxs-lookup"><span data-stu-id="8c2e0-133">The following modifiers can be used with [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>



| <span data-ttu-id="8c2e0-134">Modificador</span><span class="sxs-lookup"><span data-stu-id="8c2e0-134">Modifier</span></span>                                                                                         | <span data-ttu-id="8c2e0-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c2e0-135">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c2e0-136">**incorporación de la \_ marca WinHTTP ADDREQ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8c2e0-136">**WINHTTP\_ADDREQ\_FLAG\_ADD**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | <span data-ttu-id="8c2e0-137">Agrega el encabezado si no existe.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-137">Adds the header if it does not exist.</span></span> <span data-ttu-id="8c2e0-138">Se usa con la [**\_ \_ marca \_ Replace de ADDREQ de WinHTTP**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span><span class="sxs-lookup"><span data-stu-id="8c2e0-138">Used with [**WINHTTP\_ADDREQ\_FLAG\_REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="8c2e0-139">**la \_ marca de WinHTTP ADDREQ \_ \_ agregar \_ si es \_ nueva**</span><span class="sxs-lookup"><span data-stu-id="8c2e0-139">**WINHTTP\_ADDREQ\_FLAG\_ADD\_IF\_NEW**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | <span data-ttu-id="8c2e0-140">Agrega el encabezado solo si aún no existe; de lo contrario, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-140">Adds the header only if it does not already exist; otherwise, an error is returned.</span></span>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="8c2e0-141">**incorporación de marcas de WINHTTP \_ ADDREQ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8c2e0-141">**WINHTTP\_ADDREQ\_FLAG\_COALESCE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | <span data-ttu-id="8c2e0-142">Combina los encabezados del mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-142">Merges headers of the same name.</span></span>                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="8c2e0-143">**\_ \_ incorporación de la marca de WinHTTP ADDREQ \_ \_ con \_ coma**</span><span class="sxs-lookup"><span data-stu-id="8c2e0-143">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_COMMA**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | <span data-ttu-id="8c2e0-144">Combina los encabezados del mismo nombre mediante una coma.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-144">Merges headers of the same name using a comma.</span></span> <span data-ttu-id="8c2e0-145">Por ejemplo, al agregar "Accept: Text/ \* " seguido de "Accept: audio/ \* " con esta marca, se forma el encabezado único "Accept: Text/ \* , audio/ \* ", lo que hace que se combine el primer encabezado.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-145">For example, adding "Accept: text/\*" followed by "Accept: audio/\*" with this flag forms the single header "Accept: text/\*, audio/\*", causing the first header found to be merged.</span></span> <span data-ttu-id="8c2e0-146">Depende de la aplicación que realiza la llamada garantizar un esquema coherente con respecto a los encabezados combinados/independientes.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-146">It is up to the calling application to ensure a cohesive scheme with respect to merged/separate headers.</span></span> |
| [<span data-ttu-id="8c2e0-147">**la \_ marca de WinHTTP ADDREQ se \_ \_ combina \_ con un \_ punto y coma**</span><span class="sxs-lookup"><span data-stu-id="8c2e0-147">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_SEMICOLON**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | <span data-ttu-id="8c2e0-148">Combina los encabezados del mismo nombre con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-148">Merges headers of the same name using a semicolon.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="8c2e0-149">**ADDREQ de la marca de WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8c2e0-149">**WINHTTP\_ADDREQ\_FLAG\_REPLACE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | <span data-ttu-id="8c2e0-150">Reemplaza o quita un encabezado.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-150">Replaces or removes a header.</span></span> <span data-ttu-id="8c2e0-151">Si el valor del encabezado está vacío y se encuentra el encabezado, se quita.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-151">If the header value is empty and the header is found, it is removed.</span></span> <span data-ttu-id="8c2e0-152">Si el valor del encabezado no está vacío, se reemplaza el valor del encabezado.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-152">If the header value is not empty, the header value is replaced.</span></span>                                                                                                                                                                            |



 

## <a name="sending-a-request"></a><span data-ttu-id="8c2e0-153">Envío de una solicitud</span><span class="sxs-lookup"><span data-stu-id="8c2e0-153">Sending a Request</span></span>

<span data-ttu-id="8c2e0-154">La función [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) establece una conexión con el servidor y envía la solicitud al sitio especificado.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-154">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function establishes a connection to the server and sends the request to the specified site.</span></span> <span data-ttu-id="8c2e0-155">Esta función requiere un identificador de [HINTERNET](hinternet-handles-in-winhttp.md) creado por [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span><span class="sxs-lookup"><span data-stu-id="8c2e0-155">This function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span> <span data-ttu-id="8c2e0-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) también puede enviar encabezados adicionales u información opcional.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) can also send additional headers or optional information.</span></span> <span data-ttu-id="8c2e0-157">La información opcional se utiliza generalmente para las operaciones que escriben información en el servidor, como PUT y POST.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-157">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="8c2e0-158">Después de que la función [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) envíe la solicitud, la aplicación puede usar las funciones [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) y [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) en el controlador [HINTERNET](hinternet-handles-in-winhttp.md) para descargar los recursos del servidor.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-158">After the [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function sends the request, the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions on the [HINTERNET](hinternet-handles-in-winhttp.md) handle to download the server's resources.</span></span>

## <a name="posting-data-to-the-server"></a><span data-ttu-id="8c2e0-159">Publicar datos en el servidor</span><span class="sxs-lookup"><span data-stu-id="8c2e0-159">Posting Data to the Server</span></span>

<span data-ttu-id="8c2e0-160">Para publicar datos en un servidor, el [*verbo http*](glossary.md) de la llamada a [**WINHTTPOPENREQUEST**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) debe ser post o Put.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-160">To post data to a server, the [*HTTP verb*](glossary.md) in the call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) must be either POST or PUT.</span></span> <span data-ttu-id="8c2e0-161">Cuando se llama a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) , el parámetro *dwTotalLength* debe establecerse en el tamaño de los datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-161">When [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) is called, the *dwTotalLength* parameter should be set to the size of the data in bytes.</span></span> <span data-ttu-id="8c2e0-162">A continuación, use [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) para enviar los datos al servidor.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-162">Then use [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) to post the data to the server.</span></span>

<span data-ttu-id="8c2e0-163">Como alternativa, establezca el parámetro *lpOptional* de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) en la dirección de un búfer que contenga los datos que se van a publicar en el servidor.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-163">Alternatively, set the *lpOptional* parameter of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to the address of a buffer that contains data to post to the server.</span></span> <span data-ttu-id="8c2e0-164">Al usar esta técnica, debe establecer los parámetros *dwOptionalLength* y *dwTotalLength* de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) para que sea el tamaño de los datos que se van a exponer.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-164">When using this technique, you must set both the *dwOptionalLength* and *dwTotalLength* parameters of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to be the size of the data being posted.</span></span> <span data-ttu-id="8c2e0-165">La llamada a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) de esta manera elimina la necesidad de llamar a [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).</span><span class="sxs-lookup"><span data-stu-id="8c2e0-165">Calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in this manner eliminates the need to call [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).</span></span>

## <a name="getting-information-about-a-request"></a><span data-ttu-id="8c2e0-166">Obtención de información acerca de una solicitud</span><span class="sxs-lookup"><span data-stu-id="8c2e0-166">Getting Information About a Request</span></span>

<span data-ttu-id="8c2e0-167">La función [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) permite que una aplicación recupere información acerca de una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-167">The [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) function allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="8c2e0-168">La función requiere un identificador [HINTERNET](hinternet-handles-in-winhttp.md) creado por [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), un valor de nivel de información y una longitud de búfer.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-168">The function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), an information level value, and a buffer length.</span></span> <span data-ttu-id="8c2e0-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) también acepta un búfer que almacena la información y un índice de encabezado basado en cero que enumera varios encabezados con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

<span data-ttu-id="8c2e0-170">Use cualquiera de los valores de nivel de información que se encuentran en la página [**marcas de información de consulta**](query-info-flags.md) con un modificador para controlar el formato en el que se almacena la información en el parámetro *lpvBuffer* de [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="8c2e0-170">Use any of the information level values found on the [**Query Info Flags**](query-info-flags.md) page with a modifier to control the format in which the information is stored in the *lpvBuffer* parameter of [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

## <a name="downloading-resources-from-the-web"></a><span data-ttu-id="8c2e0-171">Descargar recursos de la web</span><span class="sxs-lookup"><span data-stu-id="8c2e0-171">Downloading Resources from the Web</span></span>

<span data-ttu-id="8c2e0-172">Después de abrir una solicitud con la función [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , enviarla al servidor con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)y preparar el identificador de solicitud para recibir una respuesta con [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), la aplicación puede usar las funciones [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) y [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) para descargar el recurso desde el servidor http.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-172">After opening a request with the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function, sending it to the server with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), and preparing the request handle to receive a response with [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="8c2e0-173">En el código de ejemplo siguiente se muestra cómo descargar un recurso con semántica de transacciones seguras.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-173">The following sample code shows how to download a resource with secure transaction semantics.</span></span> <span data-ttu-id="8c2e0-174">El código de ejemplo inicializa la interfaz de programación de aplicaciones (API) de WinHTTP, selecciona un servidor HTTPS de destino y, a continuación, abre y envía una solicitud para este recurso seguro.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-174">The sample code initializes the WinHTTP application programming interface (API), selects a target HTTPS server, and then opens and sends a request for this secure resource.</span></span> <span data-ttu-id="8c2e0-175">[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) se usa con el identificador de solicitud para determinar la cantidad de datos disponibles para su descarga y, a continuación, se usa [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) para leer los datos.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-175">[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) is used with the request handle to determine how much data is available for download, and then [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) is used to read that data.</span></span> <span data-ttu-id="8c2e0-176">Este proceso se repite hasta que se ha recuperado y mostrado todo el documento.</span><span class="sxs-lookup"><span data-stu-id="8c2e0-176">This process is repeated until the entire document has been retrieved and displayed.</span></span>


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



