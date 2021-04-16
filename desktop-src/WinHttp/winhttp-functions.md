---
description: En este tema se identifican las funciones que proporciona WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Funciones WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6511d2e66acc923072cc7a961aae3cb572b8e466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705672"
---
# <a name="winhttp-functions"></a><span data-ttu-id="346dc-103">Funciones WinHTTP</span><span class="sxs-lookup"><span data-stu-id="346dc-103">WinHTTP Functions</span></span>

<span data-ttu-id="346dc-104">WinHTTP proporciona las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="346dc-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="346dc-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="346dc-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="346dc-106">Agrega uno o más encabezados de solicitud HTTP al identificador de la solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="346dc-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-107">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="346dc-107">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="346dc-108">Determina si WinHTTP admite la plataforma actual.</span><span class="sxs-lookup"><span data-stu-id="346dc-108">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-109">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="346dc-109">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="346dc-110">Cierra un único identificador de [HINTERNET](hinternet-handles-in-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="346dc-110">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-111">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="346dc-111">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="346dc-112">Especifica el servidor de destino inicial de una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="346dc-112">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-113">**WinHttpCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="346dc-113">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="346dc-114">Separa una dirección URL en sus partes componentes, por ejemplo, nombre de host y ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="346dc-114">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-115">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="346dc-115">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="346dc-116">Crea un identificador para su uso por parte de [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="346dc-116">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-117">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="346dc-117">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="346dc-118">Crea una dirección URL a partir de partes componentes, por ejemplo, el nombre de host y la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="346dc-118">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-119">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="346dc-119">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="346dc-120">Busca la dirección URL del archivo de configuración automática de proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="346dc-120">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="346dc-121">Esta función informa de la dirección URL del archivo PAC, pero no descarga el archivo.</span><span class="sxs-lookup"><span data-stu-id="346dc-121">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-122">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="346dc-122">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="346dc-123">Libera los datos recuperados de una llamada anterior a [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="346dc-123">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-124">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="346dc-124">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="346dc-125">Recupera la configuración predeterminada del proxy WinHTTP del registro.</span><span class="sxs-lookup"><span data-stu-id="346dc-125">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-126">**WinHTTPGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="346dc-126">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="346dc-127">Obtiene la configuración del proxy de Internet Explorer (IE) para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="346dc-127">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-128">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="346dc-128">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="346dc-129">Recupera la información de proxy para la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="346dc-129">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-130">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="346dc-130">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="346dc-131">Recupera la información de proxy para la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="346dc-131">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-132">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="346dc-132">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="346dc-133">Recupera los resultados de una llamada a [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="346dc-133">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-134">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="346dc-134">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="346dc-135">Inicializa el uso de una aplicación de las funciones de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="346dc-135">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-136">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="346dc-136">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="346dc-137">Crea un identificador de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="346dc-137">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-138">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="346dc-138">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="346dc-139">Devuelve los esquemas de autorización que admite el servidor.</span><span class="sxs-lookup"><span data-stu-id="346dc-139">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-140">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="346dc-140">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="346dc-141">Devuelve el número de bytes de datos que están disponibles inmediatamente para ser leídos con [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span><span class="sxs-lookup"><span data-stu-id="346dc-141">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-142">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="346dc-142">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="346dc-143">Recupera información de encabezado asociada a una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="346dc-143">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-144">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="346dc-144">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="346dc-145">Consulta una opción de Internet en el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="346dc-145">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-146">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="346dc-146">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="346dc-147">Lee datos de un identificador abierto por la función [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) .</span><span class="sxs-lookup"><span data-stu-id="346dc-147">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-148">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="346dc-148">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="346dc-149">Finaliza una solicitud HTTP iniciada por [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="346dc-149">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-150">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="346dc-150">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="346dc-151">Restablece el proxy automático.</span><span class="sxs-lookup"><span data-stu-id="346dc-151">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-152">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="346dc-152">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="346dc-153">Envía la solicitud especificada al servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="346dc-153">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-154">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="346dc-154">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="346dc-155">Pasa las credenciales de autorización necesarias al servidor.</span><span class="sxs-lookup"><span data-stu-id="346dc-155">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-156">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="346dc-156">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="346dc-157">Establece la configuración predeterminada del proxy WinHTTP en el registro.</span><span class="sxs-lookup"><span data-stu-id="346dc-157">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-158">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="346dc-158">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="346dc-159">Establece una opción de Internet.</span><span class="sxs-lookup"><span data-stu-id="346dc-159">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-160">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="346dc-160">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="346dc-161">Configura una función de devolución de llamada a la que WinHTTP puede llamar como progreso durante una operación.</span><span class="sxs-lookup"><span data-stu-id="346dc-161">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-162">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="346dc-162">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="346dc-163">Establece los distintos tiempos de espera implicados en las transacciones HTTP.</span><span class="sxs-lookup"><span data-stu-id="346dc-163">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-164">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="346dc-164">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="346dc-165">Da formato a una fecha y hora según la especificación HTTP versión 1,0.</span><span class="sxs-lookup"><span data-stu-id="346dc-165">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-166">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="346dc-166">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="346dc-167">Toma una cadena de fecha y hora HTTP y la convierte en una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="346dc-167">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-168">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="346dc-168">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="346dc-169">Escribe los datos de la solicitud en un servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="346dc-169">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-170">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="346dc-170">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="346dc-171">Cierra una conexión WebSocket.</span><span class="sxs-lookup"><span data-stu-id="346dc-171">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-172">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="346dc-172">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="346dc-173">Completa un protocolo de enlace de WebSocket Iniciado por [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="346dc-173">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-174">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="346dc-174">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="346dc-175">Obtiene el estado de cierre enviado por un servidor.</span><span class="sxs-lookup"><span data-stu-id="346dc-175">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-176">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="346dc-176">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="346dc-177">Recibe datos de una conexión de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="346dc-177">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-178">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="346dc-178">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="346dc-179">Envía datos a través de una conexión de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="346dc-179">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="346dc-180">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="346dc-180">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="346dc-181">Envía un marco de cierre a una conexión de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="346dc-181">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>

 

 
