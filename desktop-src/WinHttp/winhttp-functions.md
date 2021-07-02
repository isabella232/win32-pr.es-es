---
description: En este tema se identifican las funciones que proporciona WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Funciones WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e45289230c1cc22a7f8799dfbbe1dafddccf38
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174975"
---
# <a name="winhttp-functions"></a><span data-ttu-id="4f487-103">Funciones WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4f487-103">WinHTTP Functions</span></span>

<span data-ttu-id="4f487-104">WinHTTP proporciona las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="4f487-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="4f487-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="4f487-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="4f487-106">Agrega uno o varios encabezados de solicitud HTTP al identificador de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f487-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-107">**WinHttpAddRequestHeadersEx**</span><span class="sxs-lookup"><span data-stu-id="4f487-107">**WinHttpAddRequestHeadersEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheadersex)
</dt> <dd>

<span data-ttu-id="4f487-108">Agrega uno o varios encabezados de solicitud HTTP a un identificador de solicitud HTTP, lo que le permite usar cadenas de nombre y valor independientes.</span><span class="sxs-lookup"><span data-stu-id="4f487-108">Adds one or more HTTP request headers to an HTTP request handle, allowing you to use separate name/value strings.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-109">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="4f487-109">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="4f487-110">Determina si WinHTTP admite la plataforma actual.</span><span class="sxs-lookup"><span data-stu-id="4f487-110">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-111">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="4f487-111">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="4f487-112">Cierra un único identificador [HINTERNET.](hinternet-handles-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="4f487-112">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-113">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="4f487-113">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="4f487-114">Especifica el servidor de destino inicial de una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f487-114">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-115">**WinHttpCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="4f487-115">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="4f487-116">Separa una dirección URL en sus elementos componentes, por ejemplo, el nombre de host y la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="4f487-116">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-117">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="4f487-117">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="4f487-118">Crea un identificador para que [**lo use WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="4f487-118">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-119">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="4f487-119">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="4f487-120">Crea una dirección URL a partir de elementos componentes, por ejemplo, el nombre de host y la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="4f487-120">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-121">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="4f487-121">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="4f487-122">Busca la dirección URL del archivo de configuración automática (PAC) del proxy.</span><span class="sxs-lookup"><span data-stu-id="4f487-122">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="4f487-123">Esta función notifica la dirección URL del archivo PAC, pero no descarga el archivo.</span><span class="sxs-lookup"><span data-stu-id="4f487-123">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-124">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="4f487-124">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="4f487-125">Libera los datos recuperados de una llamada anterior a [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="4f487-125">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-126">**WinHttpFreeQueryConnectionGroupResult**</span><span class="sxs-lookup"><span data-stu-id="4f487-126">**WinHttpFreeQueryConnectionGroupResult**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

<span data-ttu-id="4f487-127">Libera la memoria asignada por una llamada anterior a [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span><span class="sxs-lookup"><span data-stu-id="4f487-127">Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-128">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="4f487-128">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="4f487-129">Recupera la configuración predeterminada del proxy WinHTTP del Registro.</span><span class="sxs-lookup"><span data-stu-id="4f487-129">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-130">**WinHTTPGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="4f487-130">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="4f487-131">Obtiene la configuración Internet Explorer (IE) del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="4f487-131">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-132">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="4f487-132">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="4f487-133">Recupera la información del proxy para la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="4f487-133">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-134">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="4f487-134">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="4f487-135">Recupera la información del proxy para la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="4f487-135">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-136">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="4f487-136">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="4f487-137">Recupera los resultados de una llamada a [**WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="4f487-137">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-138">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="4f487-138">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="4f487-139">Inicializa el uso de las funciones WinHTTP de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4f487-139">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-140">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="4f487-140">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="4f487-141">Crea un identificador de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f487-141">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-142">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="4f487-142">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="4f487-143">Devuelve los esquemas de autorización que admite el servidor.</span><span class="sxs-lookup"><span data-stu-id="4f487-143">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-144">**WinHttpQueryConnectionGroup**</span><span class="sxs-lookup"><span data-stu-id="4f487-144">**WinHttpQueryConnectionGroup**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

<span data-ttu-id="4f487-145">Recupera una descripción del estado actual de las conexiones de WinHttp.</span><span class="sxs-lookup"><span data-stu-id="4f487-145">Retrieves a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-146">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="4f487-146">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="4f487-147">Devuelve el número de bytes de datos que están disponibles inmediatamente para leerse [**con WinHttpReadData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)</span><span class="sxs-lookup"><span data-stu-id="4f487-147">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-148">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="4f487-148">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="4f487-149">Recupera la información de encabezado asociada a una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f487-149">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-150">**WinHttpQueryHeadersEx**</span><span class="sxs-lookup"><span data-stu-id="4f487-150">**WinHttpQueryHeadersEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheadersex)
</dt> <dd>

<span data-ttu-id="4f487-151">Recupera información de encabezado asociada a una solicitud HTTP; ofrece una manera de recuperar cadenas de nombre de encabezado y valor analizadas.</span><span class="sxs-lookup"><span data-stu-id="4f487-151">Retrieves header information associated with an HTTP request; offers a way to retrieve parsed header name and value strings.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-152">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="4f487-152">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="4f487-153">Consulta una opción de Internet en el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="4f487-153">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-154">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="4f487-154">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="4f487-155">Lee datos de un identificador abierto por la [**función WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)</span><span class="sxs-lookup"><span data-stu-id="4f487-155">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-156">**WinHttpReadDataEx**</span><span class="sxs-lookup"><span data-stu-id="4f487-156">**WinHttpReadDataEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddataex)
</dt> <dd>

<span data-ttu-id="4f487-157">Lee datos de un identificador abierto por la [**función WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)</span><span class="sxs-lookup"><span data-stu-id="4f487-157">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-158">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="4f487-158">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="4f487-159">Finaliza una solicitud HTTP iniciada por [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="4f487-159">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-160">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="4f487-160">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="4f487-161">Restablece el proxy automático.</span><span class="sxs-lookup"><span data-stu-id="4f487-161">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-162">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="4f487-162">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="4f487-163">Envía la solicitud especificada al servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f487-163">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-164">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="4f487-164">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="4f487-165">Pasa las credenciales de autorización necesarias al servidor.</span><span class="sxs-lookup"><span data-stu-id="4f487-165">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-166">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="4f487-166">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="4f487-167">Establece la configuración predeterminada del proxy WinHTTP en el Registro.</span><span class="sxs-lookup"><span data-stu-id="4f487-167">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-168">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="4f487-168">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="4f487-169">Establece una opción de Internet.</span><span class="sxs-lookup"><span data-stu-id="4f487-169">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-170">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="4f487-170">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="4f487-171">Configura una función de devolución de llamada a la que WinHTTP puede llamar a medida que se realiza el progreso durante una operación.</span><span class="sxs-lookup"><span data-stu-id="4f487-171">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-172">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="4f487-172">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="4f487-173">Establece los distintos tiempos de espera que intervienen en las transacciones HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f487-173">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-174">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="4f487-174">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="4f487-175">Da formato a una fecha y hora según la especificación http versión 1.0.</span><span class="sxs-lookup"><span data-stu-id="4f487-175">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-176">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="4f487-176">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="4f487-177">Toma una cadena de fecha y hora HTTP y la convierte en una [**estructura SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)</span><span class="sxs-lookup"><span data-stu-id="4f487-177">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-178">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="4f487-178">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="4f487-179">Escribe datos de solicitud en un servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f487-179">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-180">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="4f487-180">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="4f487-181">Cierra una conexión de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="4f487-181">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-182">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="4f487-182">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="4f487-183">Completa un protocolo de enlace WebSocket iniciado [**por WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="4f487-183">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-184">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="4f487-184">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="4f487-185">Obtiene el estado de cierre enviado por un servidor.</span><span class="sxs-lookup"><span data-stu-id="4f487-185">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-186">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="4f487-186">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="4f487-187">Recibe datos de una conexión webSocket.</span><span class="sxs-lookup"><span data-stu-id="4f487-187">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-188">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="4f487-188">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="4f487-189">Envía datos a través de una conexión de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="4f487-189">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="4f487-190">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="4f487-190">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="4f487-191">Envía un fotograma cercano a una conexión de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="4f487-191">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>


