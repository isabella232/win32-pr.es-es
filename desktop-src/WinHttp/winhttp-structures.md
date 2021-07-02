---
description: En este tema se identifican las estructuras que usa WinHTTP.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: Estructuras WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ecf91702a2f49e2c0a754fcc69d9d34febf229
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174982"
---
# <a name="winhttp-structures"></a><span data-ttu-id="a9da3-103">Estructuras WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a9da3-103">WinHTTP structures</span></span>

<span data-ttu-id="a9da3-104">WinHTTP usa las estructuras siguientes:</span><span class="sxs-lookup"><span data-stu-id="a9da3-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="a9da3-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="a9da3-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="a9da3-106">Contiene la versión http global.</span><span class="sxs-lookup"><span data-stu-id="a9da3-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="a9da3-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="a9da3-108">Contiene las partes constituyentes de una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="a9da3-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="a9da3-109">Esta estructura se usa con las [**funciones WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) [**y WinHttpCreateUrl.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)</span><span class="sxs-lookup"><span data-stu-id="a9da3-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="a9da3-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="a9da3-111">Contiene el resultado de una llamada a una función asincrónica.</span><span class="sxs-lookup"><span data-stu-id="a9da3-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="a9da3-112">Esta estructura se usa con el [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototipo.</span><span class="sxs-lookup"><span data-stu-id="a9da3-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="a9da3-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="a9da3-114">Se usa para indicar a la función [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) si se debe especificar la dirección URL del archivo de configuración automática de proxy (PAC) o buscar automáticamente la dirección URL con consultas DHCP o DNS en la red.</span><span class="sxs-lookup"><span data-stu-id="a9da3-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="a9da3-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="a9da3-116">Contiene información de certificado devuelta desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="a9da3-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="a9da3-117">La función [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="a9da3-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-118">**WINHTTP_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="a9da3-118">**WINHTTP_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

<span data-ttu-id="a9da3-119">Representa un grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="a9da3-119">Represents a connection group.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-120">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="a9da3-120">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="a9da3-121">Contiene la dirección IP de origen y destino de la solicitud que generó la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a9da3-121">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-122">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="a9da3-122">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="a9da3-123">Contiene información de credenciales de usuario utilizada para la autenticación de servidor y proxy.</span><span class="sxs-lookup"><span data-stu-id="a9da3-123">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="a9da3-124">Esta estructura está en desuso.</span><span class="sxs-lookup"><span data-stu-id="a9da3-124">This structure has been deprecated.</span></span> <span data-ttu-id="a9da3-125">En su lugar, se recomienda [**el uso de la WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) estructura.</span><span class="sxs-lookup"><span data-stu-id="a9da3-125">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-126">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="a9da3-126">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="a9da3-127">Contiene información de credenciales de usuario utilizada para la autenticación de servidor y proxy.</span><span class="sxs-lookup"><span data-stu-id="a9da3-127">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="a9da3-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="a9da3-129">Contiene la información Internet Explorer configuración del proxy.</span><span class="sxs-lookup"><span data-stu-id="a9da3-129">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-130">**WINHTTP_EXTENDED_HEADER**</span><span class="sxs-lookup"><span data-stu-id="a9da3-130">**WINHTTP_EXTENDED_HEADER**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_extended_header)
</dt> <dd>

<span data-ttu-id="a9da3-131">Representa un encabezado de solicitud HTTP como un par de cadenas nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="a9da3-131">Represents an HTTP request header as a name/value string pair.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-132">**WINHTTP_HEADER_NAME**</span><span class="sxs-lookup"><span data-stu-id="a9da3-132">**WINHTTP_HEADER_NAME**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_header_name)
</dt> <dd>

<span data-ttu-id="a9da3-133">Representa un nombre de encabezado de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="a9da3-133">Represents an HTTP request header name.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-134">**WINHTTP_HOST_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="a9da3-134">**WINHTTP_HOST_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

<span data-ttu-id="a9da3-135">Representa una colección de grupos de conexiones.</span><span class="sxs-lookup"><span data-stu-id="a9da3-135">Represents a collection of connection groups.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-136">**WINHTTP_MATCH_CONNECTION_GUID**</span><span class="sxs-lookup"><span data-stu-id="a9da3-136">**WINHTTP_MATCH_CONNECTION_GUID**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

<span data-ttu-id="a9da3-137">Representa el GUID de una conexión, con fines de coincidencia de conexiones.</span><span class="sxs-lookup"><span data-stu-id="a9da3-137">Represents the GUID of a connection, for purposes of connection-matching.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-138">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="a9da3-138">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="a9da3-139">Contiene la configuración de proxy predeterminada o de sesión.</span><span class="sxs-lookup"><span data-stu-id="a9da3-139">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-140">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="a9da3-140">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="a9da3-141">Colección de entradas de resultado de proxy proporcionadas [**por WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="a9da3-141">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-142">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="a9da3-142">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="a9da3-143">Entrada de resultado de una llamada a [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)</span><span class="sxs-lookup"><span data-stu-id="a9da3-143">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-144">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span><span class="sxs-lookup"><span data-stu-id="a9da3-144">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

<span data-ttu-id="a9da3-145">Representa una descripción del estado actual de las conexiones de WinHttp.</span><span class="sxs-lookup"><span data-stu-id="a9da3-145">Represents a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-146">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="a9da3-146">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="a9da3-147">Contiene estadísticas de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a9da3-147">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-148">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="a9da3-148">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="a9da3-149">Contiene información de tiempo para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a9da3-149">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-150">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="a9da3-150">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="a9da3-151">Contiene información de cifrado y conexión SChannel para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a9da3-151">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-152">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="a9da3-152">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="a9da3-153">Estado del resultado de una operación de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="a9da3-153">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="a9da3-154">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="a9da3-154">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="a9da3-155">Estado de una operación de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="a9da3-155">Status of a WebSocket operation.</span></span>

</dd> </dl>
