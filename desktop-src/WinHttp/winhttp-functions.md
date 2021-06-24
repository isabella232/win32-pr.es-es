---
description: En este tema se identifican las funciones que proporciona WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Funciones WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5f9db8fcde5589a86556111bec6df3b2b18c76
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587747"
---
# <a name="winhttp-functions"></a><span data-ttu-id="90781-103">Funciones WinHTTP</span><span class="sxs-lookup"><span data-stu-id="90781-103">WinHTTP Functions</span></span>

<span data-ttu-id="90781-104">WinHTTP proporciona las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="90781-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="90781-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="90781-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="90781-106">Agrega uno o varios encabezados de solicitud HTTP al identificador de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="90781-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-107">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="90781-107">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="90781-108">Determina si WinHTTP admite la plataforma actual.</span><span class="sxs-lookup"><span data-stu-id="90781-108">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-109">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="90781-109">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="90781-110">Cierra un único identificador [HINTERNET.](hinternet-handles-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="90781-110">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-111">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="90781-111">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="90781-112">Especifica el servidor de destino inicial de una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="90781-112">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-113">**WinHttpCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="90781-113">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="90781-114">Separa una dirección URL en sus elementos componentes, por ejemplo, el nombre de host y la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="90781-114">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-115">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="90781-115">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="90781-116">Crea un identificador para que [**lo use WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="90781-116">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="90781-117">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="90781-117">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="90781-118">Crea una dirección URL a partir de elementos de componente, por ejemplo, el nombre de host y la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="90781-118">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-119">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="90781-119">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="90781-120">Busca la dirección URL del archivo de configuración automática (PAC) del proxy.</span><span class="sxs-lookup"><span data-stu-id="90781-120">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="90781-121">Esta función notifica la dirección URL del archivo PAC, pero no descarga el archivo.</span><span class="sxs-lookup"><span data-stu-id="90781-121">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-122">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="90781-122">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="90781-123">Libera los datos recuperados de una llamada anterior a [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)</span><span class="sxs-lookup"><span data-stu-id="90781-123">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="90781-124">**WinHttpFreeQueryConnectionGroupResult**</span><span class="sxs-lookup"><span data-stu-id="90781-124">**WinHttpFreeQueryConnectionGroupResult**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

<span data-ttu-id="90781-125">Libera la memoria asignada por una llamada anterior a [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span><span class="sxs-lookup"><span data-stu-id="90781-125">Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span></span>

</dd> <dt>

[<span data-ttu-id="90781-126">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="90781-126">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="90781-127">Recupera la configuración predeterminada del proxy WinHTTP del Registro.</span><span class="sxs-lookup"><span data-stu-id="90781-127">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-128">**WinHTTPGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="90781-128">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="90781-129">Obtiene la configuración Internet Explorer proxy (IE) del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="90781-129">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-130">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="90781-130">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="90781-131">Recupera la información de proxy de la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="90781-131">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-132">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="90781-132">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="90781-133">Recupera la información de proxy de la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="90781-133">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-134">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="90781-134">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="90781-135">Recupera los resultados de una llamada a [**WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="90781-135">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="90781-136">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="90781-136">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="90781-137">Inicializa el uso de las funciones WinHTTP de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="90781-137">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-138">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="90781-138">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="90781-139">Crea un identificador de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="90781-139">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-140">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="90781-140">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="90781-141">Devuelve los esquemas de autorización que admite el servidor.</span><span class="sxs-lookup"><span data-stu-id="90781-141">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-142">**WinHttpQueryConnectionGroup**</span><span class="sxs-lookup"><span data-stu-id="90781-142">**WinHttpQueryConnectionGroup**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

<span data-ttu-id="90781-143">Recupera una descripción del estado actual de las conexiones de WinHttp.</span><span class="sxs-lookup"><span data-stu-id="90781-143">Retrieves a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-144">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="90781-144">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="90781-145">Devuelve el número de bytes de datos que están disponibles inmediatamente para leerse [**con WinHttpReadData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)</span><span class="sxs-lookup"><span data-stu-id="90781-145">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="90781-146">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="90781-146">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="90781-147">Recupera la información de encabezado asociada a una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="90781-147">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-148">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="90781-148">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="90781-149">Consulta una opción de Internet en el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="90781-149">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-150">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="90781-150">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="90781-151">Lee datos de un identificador abierto por la [**función WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)</span><span class="sxs-lookup"><span data-stu-id="90781-151">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-152">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="90781-152">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="90781-153">Finaliza una solicitud HTTP iniciada por [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="90781-153">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="90781-154">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="90781-154">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="90781-155">Restablece el proxy automático.</span><span class="sxs-lookup"><span data-stu-id="90781-155">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-156">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="90781-156">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="90781-157">Envía la solicitud especificada al servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="90781-157">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-158">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="90781-158">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="90781-159">Pasa las credenciales de autorización necesarias al servidor.</span><span class="sxs-lookup"><span data-stu-id="90781-159">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-160">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="90781-160">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="90781-161">Establece la configuración predeterminada del proxy WinHTTP en el Registro.</span><span class="sxs-lookup"><span data-stu-id="90781-161">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-162">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="90781-162">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="90781-163">Establece una opción de Internet.</span><span class="sxs-lookup"><span data-stu-id="90781-163">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-164">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="90781-164">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="90781-165">Configura una función de devolución de llamada a la que WinHTTP puede llamar a medida que se realiza el progreso durante una operación.</span><span class="sxs-lookup"><span data-stu-id="90781-165">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-166">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="90781-166">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="90781-167">Establece los distintos tiempos de espera que implican las transacciones HTTP.</span><span class="sxs-lookup"><span data-stu-id="90781-167">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-168">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="90781-168">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="90781-169">Da formato a una fecha y hora según la especificación http versión 1.0.</span><span class="sxs-lookup"><span data-stu-id="90781-169">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-170">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="90781-170">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="90781-171">Toma una cadena de fecha y hora HTTP y la convierte en una [**estructura SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)</span><span class="sxs-lookup"><span data-stu-id="90781-171">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-172">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="90781-172">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="90781-173">Escribe datos de solicitud en un servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="90781-173">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-174">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="90781-174">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="90781-175">Cierra una conexión de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="90781-175">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-176">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="90781-176">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="90781-177">Completa un protocolo de enlace WebSocket iniciado [**por WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="90781-177">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="90781-178">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="90781-178">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="90781-179">Obtiene el estado de cierre enviado por un servidor.</span><span class="sxs-lookup"><span data-stu-id="90781-179">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-180">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="90781-180">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="90781-181">Recibe datos de una conexión webSocket.</span><span class="sxs-lookup"><span data-stu-id="90781-181">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-182">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="90781-182">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="90781-183">Envía datos a través de una conexión webSocket.</span><span class="sxs-lookup"><span data-stu-id="90781-183">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="90781-184">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="90781-184">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="90781-185">Envía un fotograma cercano a una conexión de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="90781-185">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>

 

 
