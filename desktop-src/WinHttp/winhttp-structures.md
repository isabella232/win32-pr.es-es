---
description: En este tema se identifican las estructuras que usa WinHTTP.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: Estructuras WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d6f0cdbb467e916b1a6ac54b90491cbee9efdb
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587978"
---
# <a name="winhttp-structures"></a><span data-ttu-id="5c7fe-103">Estructuras WinHTTP</span><span class="sxs-lookup"><span data-stu-id="5c7fe-103">WinHTTP structures</span></span>

<span data-ttu-id="5c7fe-104">WinHTTP usa las estructuras siguientes:</span><span class="sxs-lookup"><span data-stu-id="5c7fe-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="5c7fe-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="5c7fe-106">Contiene la versión http global.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="5c7fe-108">Contiene las partes constituyentes de una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="5c7fe-109">Esta estructura se usa con las [**funciones WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) [**y WinHttpCreateUrl.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)</span><span class="sxs-lookup"><span data-stu-id="5c7fe-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="5c7fe-111">Contiene el resultado de una llamada a una función asincrónica.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="5c7fe-112">Esta estructura se usa con el [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototipo.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="5c7fe-114">Se usa para indicar a la función [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) si se debe especificar la dirección URL del archivo de configuración automática de proxy (PAC) o buscar automáticamente la dirección URL con consultas DHCP o DNS en la red.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="5c7fe-116">Contiene información de certificado devuelta desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="5c7fe-117">La función [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-118">**WINHTTP_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-118">**WINHTTP_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

<span data-ttu-id="5c7fe-119">Representa un grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-119">Represents a connection group.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-120">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-120">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="5c7fe-121">Contiene la dirección IP de origen y destino de la solicitud que generó la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-121">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-122">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-122">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="5c7fe-123">Contiene información de credenciales de usuario utilizada para la autenticación de servidor y proxy.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-123">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="5c7fe-124">Esta estructura ha quedado en desuso.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-124">This structure has been deprecated.</span></span> <span data-ttu-id="5c7fe-125">En su lugar, se recomienda [**el uso de WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) estructura.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-125">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-126">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-126">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="5c7fe-127">Contiene información de credenciales de usuario utilizada para la autenticación de servidor y proxy.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-127">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="5c7fe-129">Contiene la información Internet Explorer de configuración del proxy.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-129">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-130">**WINHTTP_HOST_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-130">**WINHTTP_HOST_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

<span data-ttu-id="5c7fe-131">Representa una colección de grupos de conexiones.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-131">Represents a collection of connection groups.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-132">**WINHTTP_MATCH_CONNECTION_GUID**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-132">**WINHTTP_MATCH_CONNECTION_GUID**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

<span data-ttu-id="5c7fe-133">Representa el GUID de una conexión, para fines de coincidencia de conexión.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-133">Represents the GUID of a connection, for purposes of connection-matching.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-134">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-134">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="5c7fe-135">Contiene la configuración de proxy predeterminada o de sesión.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-135">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-136">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-136">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="5c7fe-137">Colección de entradas de resultado de proxy proporcionadas [**por WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)</span><span class="sxs-lookup"><span data-stu-id="5c7fe-137">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-138">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-138">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="5c7fe-139">Entrada de resultado de una llamada a [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="5c7fe-139">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-140">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-140">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

<span data-ttu-id="5c7fe-141">Representa una descripción del estado actual de las conexiones de WinHttp.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-141">Represents a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-142">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-142">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="5c7fe-143">Contiene estadísticas de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-143">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-144">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-144">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="5c7fe-145">Contiene información de tiempo para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-145">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-146">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-146">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="5c7fe-147">Contiene información de cifrado y conexión SChannel para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-147">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-148">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-148">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="5c7fe-149">Estado del resultado de una operación de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-149">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="5c7fe-150">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="5c7fe-150">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="5c7fe-151">Estado de una operación de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="5c7fe-151">Status of a WebSocket operation.</span></span>

</dd> </dl>
