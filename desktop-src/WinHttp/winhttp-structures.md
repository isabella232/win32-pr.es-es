---
description: En este tema se identifican las estructuras que usa WinHTTP.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: Estructuras WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f09615e721b9d34243bd20074e83837e48a6803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275416"
---
# <a name="winhttp-structures"></a><span data-ttu-id="8423f-103">Estructuras WinHTTP</span><span class="sxs-lookup"><span data-stu-id="8423f-103">WinHTTP structures</span></span>

<span data-ttu-id="8423f-104">WinHTTP utiliza las siguientes estructuras:</span><span class="sxs-lookup"><span data-stu-id="8423f-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="8423f-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="8423f-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="8423f-106">Contiene la versión global de HTTP.</span><span class="sxs-lookup"><span data-stu-id="8423f-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="8423f-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="8423f-108">Contiene las partes constituyentes de una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="8423f-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="8423f-109">Esta estructura se usa con las funciones [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) y [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) .</span><span class="sxs-lookup"><span data-stu-id="8423f-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="8423f-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="8423f-111">Contiene el resultado de una llamada a una función asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8423f-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="8423f-112">Esta estructura se usa con el [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototipo.</span><span class="sxs-lookup"><span data-stu-id="8423f-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="8423f-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="8423f-114">Se usa para indicar a la función [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) si se debe especificar la dirección URL del archivo de configuración automática de proxy (PAC) o si se va a buscar automáticamente la dirección URL con consultas DHCP o DNS en la red.</span><span class="sxs-lookup"><span data-stu-id="8423f-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="8423f-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="8423f-116">Contiene información de certificado devuelta por el servidor.</span><span class="sxs-lookup"><span data-stu-id="8423f-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="8423f-117">La función [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="8423f-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-118">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="8423f-118">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="8423f-119">Contiene la dirección IP de origen y de destino de la solicitud que generó la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8423f-119">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-120">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="8423f-120">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="8423f-121">Contiene información de credenciales de usuario usada para la autenticación de servidor y proxy.</span><span class="sxs-lookup"><span data-stu-id="8423f-121">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="8423f-122">Esta estructura está en desuso.</span><span class="sxs-lookup"><span data-stu-id="8423f-122">This structure has been deprecated.</span></span> <span data-ttu-id="8423f-123">En su lugar, se recomienda el uso de la estructura [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) .</span><span class="sxs-lookup"><span data-stu-id="8423f-123">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-124">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="8423f-124">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="8423f-125">Contiene información de credenciales de usuario usada para la autenticación de servidor y proxy.</span><span class="sxs-lookup"><span data-stu-id="8423f-125">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-126">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="8423f-126">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="8423f-127">Contiene la información de configuración de proxy de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8423f-127">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-128">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="8423f-128">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="8423f-129">Contiene la configuración de la sesión o el proxy predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8423f-129">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-130">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="8423f-130">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="8423f-131">Colección de entradas de resultados de proxy proporcionadas por [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="8423f-131">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-132">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="8423f-132">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="8423f-133">Entrada de resultados de una llamada a [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="8423f-133">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-134">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="8423f-134">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="8423f-135">Contiene las estadísticas de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="8423f-135">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-136">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="8423f-136">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="8423f-137">Contiene información de tiempo para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="8423f-137">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-138">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="8423f-138">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="8423f-139">Contiene la información de conexión y cifrado de SChannel para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="8423f-139">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-140">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="8423f-140">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="8423f-141">Estado de resultado de una operación de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="8423f-141">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="8423f-142">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="8423f-142">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="8423f-143">Estado de una operación de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="8423f-143">Status of a WebSocket operation.</span></span>

</dd> </dl>
