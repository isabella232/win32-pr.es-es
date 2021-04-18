---
title: Marcas de API (Wininet. h)
description: Muchas de las funciones WinINet aceptan una matriz de marcas como parámetro. La siguiente es una breve descripción de las marcas definidas.
ms.assetid: 63027a3b-dc59-41c4-a22a-5d6e841159aa
topic_type:
- apiref
api_name:
- INTERNET_COOKIE_EVALUATE_P3P
- INTERNET_COOKIE_THIRD_PARTY
- INTERNET_FLAG_ASYNC
- INTERNET_FLAG_CACHE_ASYNC
- INTERNET_FLAG_CACHE_IF_NET_FAIL
- INTERNET_FLAG_DONT_CACHE
- INTERNET_FLAG_EXISTING_CONNECT
- INTERNET_FLAG_FORMS_SUBMIT
- INTERNET_FLAG_FROM_CACHE
- INTERNET_FLAG_FWD_BACK
- INTERNET_FLAG_HYPERLINK
- INTERNET_FLAG_IGNORE_CERT_CN_INVALID
- INTERNET_FLAG_IGNORE_CERT_DATE_INVALID
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS
- INTERNET_FLAG_KEEP_CONNECTION
- INTERNET_FLAG_MAKE_PERSISTENT
- INTERNET_FLAG_MUST_CACHE_REQUEST
- INTERNET_FLAG_NEED_FILE
- INTERNET_FLAG_NO_AUTH
- INTERNET_FLAG_NO_AUTO_REDIRECT
- INTERNET_FLAG_NO_CACHE_WRITE
- INTERNET_FLAG_NO_COOKIES
- INTERNET_FLAG_NO_UI
- INTERNET_FLAG_OFFLINE
- INTERNET_FLAG_PASSIVE
- INTERNET_FLAG_PRAGMA_NOCACHE
- INTERNET_FLAG_RAW_DATA
- INTERNET_FLAG_READ_PREFETCH
- INTERNET_FLAG_RELOAD
- INTERNET_FLAG_RESTRICTED_ZONE
- INTERNET_FLAG_RESYNCHRONIZE
- INTERNET_FLAG_SECURE
- INTERNET_FLAG_TRANSFER_ASCII
- INTERNET_FLAG_TRANSFER_BINARY
- INTERNET_NO_CALLBACK
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- WININET_API_FLAG_ASYNC
- WININET_API_FLAG_SYNC
- WININET_API_FLAG_USE_CONTEXT
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111bf418e6cf599f99c9dfa34ca0f5025a1d779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714605"
---
# <a name="api-flags"></a><span data-ttu-id="2e382-104">Marcas de API</span><span class="sxs-lookup"><span data-stu-id="2e382-104">API Flags</span></span>

<span data-ttu-id="2e382-105">Muchas de las funciones WinINet aceptan una matriz de marcas como parámetro.</span><span class="sxs-lookup"><span data-stu-id="2e382-105">Many of the WinINet functions accept an array of flags as a parameter.</span></span> <span data-ttu-id="2e382-106">La siguiente es una breve descripción de las marcas definidas.</span><span class="sxs-lookup"><span data-stu-id="2e382-106">The following is a brief description of the defined flags.</span></span>

<dl> <dt>

<span data-ttu-id="2e382-107"><span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**COOKIE de INTERNET \_ \_ evaluar \_ P3P**</span><span class="sxs-lookup"><span data-stu-id="2e382-107"><span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**INTERNET\_COOKIE\_EVALUATE\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-108">0x80</span><span class="sxs-lookup"><span data-stu-id="2e382-108">0x80</span></span>
</dt> <dt>



<span data-ttu-id="2e382-109">Indica que se va a asociar un encabezado de plataforma para la protección de la privacidad (P3P) a una cookie.</span><span class="sxs-lookup"><span data-stu-id="2e382-109">Indicates that a Platform for Privacy Protection (P3P) header is to be associated with a cookie.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-110"><span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**COOKIE de INTERNET de \_ \_ terceros \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-110"><span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**INTERNET\_COOKIE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-111">0x10</span><span class="sxs-lookup"><span data-stu-id="2e382-111">0x10</span></span>
</dt> <dt>



<span data-ttu-id="2e382-112">Indica que se está configurando o recuperando una cookie de terceros.</span><span class="sxs-lookup"><span data-stu-id="2e382-112">Indicates that a third-party cookie is being set or retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-113"><span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**marca de INTERNET \_ \_ Async**</span><span class="sxs-lookup"><span data-stu-id="2e382-113"><span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**INTERNET\_FLAG\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-114">0x10000000</span><span class="sxs-lookup"><span data-stu-id="2e382-114">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-115">Realiza solo solicitudes asincrónicas en identificadores que descienden del identificador devuelto por esta función.</span><span class="sxs-lookup"><span data-stu-id="2e382-115">Makes only asynchronous requests on handles descended from the handle returned from this function.</span></span> <span data-ttu-id="2e382-116">Solo la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="2e382-116">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-117"><span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**caché de marcas de INTERNET \_ \_ \_ asincrónica**</span><span class="sxs-lookup"><span data-stu-id="2e382-117"><span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-118">0x00000080</span><span class="sxs-lookup"><span data-stu-id="2e382-118">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="2e382-119">Permite una escritura diferida de caché.</span><span class="sxs-lookup"><span data-stu-id="2e382-119">Allows a lazy cache write.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-120"><span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**caché de marcas de INTERNET \_ \_ si se \_ \_ \_ produce un error de red**</span><span class="sxs-lookup"><span data-stu-id="2e382-120"><span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-121">0x00010000</span><span class="sxs-lookup"><span data-stu-id="2e382-121">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-122">Devuelve el recurso de la memoria caché si se produce un error en la solicitud de red para el recurso debido a un [error de restablecimiento de \_ \_ conexión \_ a Internet](wininet-errors.md) o error [ \_ Internet \_ no puede \_ conectar](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="2e382-122">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="2e382-123">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="2e382-123">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-124"><span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**marca de INTERNET no \_ \_ \_ almacenar en caché**</span><span class="sxs-lookup"><span data-stu-id="2e382-124"><span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**INTERNET\_FLAG\_DONT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-125">0x04000000</span><span class="sxs-lookup"><span data-stu-id="2e382-125">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-126">No agrega la entidad devuelta a la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="2e382-126">Does not add the returned entity to the cache.</span></span> <span data-ttu-id="2e382-127">Es idéntico al valor preferido, [Internet \_ Flag \_ no \_ \_ escribir en caché](/windows).</span><span class="sxs-lookup"><span data-stu-id="2e382-127">This is identical to the preferred value, [INTERNET\_FLAG\_NO\_CACHE\_WRITE](/windows).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-128"><span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**\_marca de \_ Internet \_ conexión existente**</span><span class="sxs-lookup"><span data-stu-id="2e382-128"><span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**INTERNET\_FLAG\_EXISTING\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-129">0x20000000</span><span class="sxs-lookup"><span data-stu-id="2e382-129">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-130">Intenta usar un objeto [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) existente si existe uno con los mismos atributos necesarios para realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2e382-130">Attempts to use an existing [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) object if one exists with the same attributes required to make the request.</span></span> <span data-ttu-id="2e382-131">Esto solo es útil con las operaciones FTP, ya que FTP es el único protocolo que realiza normalmente varias operaciones durante la misma sesión.</span><span class="sxs-lookup"><span data-stu-id="2e382-131">This is useful only with FTP operations, since FTP is the only protocol that typically performs multiple operations during the same session.</span></span> <span data-ttu-id="2e382-132">WinINet almacena en caché un único identificador de conexión para cada identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) generado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="2e382-132">WinINet caches a single connection handle for each [**HINTERNET**](appendix-a-hinternet-handles.md) handle generated by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="2e382-133">Las funciones [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) y **InternetConnect** usan esta marca para las conexiones http y FTP.</span><span class="sxs-lookup"><span data-stu-id="2e382-133">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and **InternetConnect** functions use this flag for Http and Ftp connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-134"><span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**\_envío de \_ formularios de marcas de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-134"><span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**INTERNET\_FLAG\_FORMS\_SUBMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-135">0x00000040</span><span class="sxs-lookup"><span data-stu-id="2e382-135">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="2e382-136">Indica que se trata de un envío de formularios.</span><span class="sxs-lookup"><span data-stu-id="2e382-136">Indicates that this is a Forms submission.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-137"><span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**\_marca \_ de Internet de la \_ caché**</span><span class="sxs-lookup"><span data-stu-id="2e382-137"><span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**INTERNET\_FLAG\_FROM\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-138">0x01000000</span><span class="sxs-lookup"><span data-stu-id="2e382-138">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-139">No realiza solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="2e382-139">Does not make network requests.</span></span> <span data-ttu-id="2e382-140">Todas las entidades se devuelven desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="2e382-140">All entities are returned from the cache.</span></span> <span data-ttu-id="2e382-141">Si el elemento solicitado no está en la memoria caché, se devuelve un error adecuado, como archivo de ERROR \_ \_ no \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="2e382-141">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="2e382-142">Solo la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="2e382-142">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-143"><span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**indicador de INTERNET de \_ \_ FWD \_ back**</span><span class="sxs-lookup"><span data-stu-id="2e382-143"><span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**INTERNET\_FLAG\_FWD\_BACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-144">0x00000020</span><span class="sxs-lookup"><span data-stu-id="2e382-144">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="2e382-145">Indica que la función debe usar la copia del recurso que se encuentra actualmente en la caché de Internet.</span><span class="sxs-lookup"><span data-stu-id="2e382-145">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="2e382-146">La fecha de expiración y otra información sobre el recurso no se comprueban.</span><span class="sxs-lookup"><span data-stu-id="2e382-146">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="2e382-147">Si el elemento solicitado no se encuentra en la caché de Internet, el sistema intentará localizar el recurso en la red.</span><span class="sxs-lookup"><span data-stu-id="2e382-147">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="2e382-148">Este valor se presentó en Microsoft Internet Explorer 5 y está asociado a las operaciones de botón **adelante** y **atrás** de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2e382-148">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-149"><span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**hipervínculo de marca de INTERNET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-149"><span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**INTERNET\_FLAG\_HYPERLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-150">0x00000400</span><span class="sxs-lookup"><span data-stu-id="2e382-150">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="2e382-151">Fuerza una recarga si no hay ninguna hora de expiración y no se devuelve ninguna hora LastModified del servidor al determinar si se debe recargar el elemento de la red.</span><span class="sxs-lookup"><span data-stu-id="2e382-151">Forces a reload if there is no Expires time and no LastModified time returned from the server when determining whether to reload the item from the network.</span></span> <span data-ttu-id="2e382-152">Esta marca puede ser utilizada por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="2e382-152">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="2e382-153">**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se usa en [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="2e382-153">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-154"><span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**marca de INTERNET \_ \_ omitir \_ CN de certificado \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="2e382-154"><span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**INTERNET\_FLAG\_IGNORE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-155">0x00001000</span><span class="sxs-lookup"><span data-stu-id="2e382-155">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-156">Deshabilita la comprobación de certificados basados en SSL/PCT que se devuelven desde el servidor con el nombre de host proporcionado en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2e382-156">Disables checking of SSL/PCT-based certificates that are returned from the server against the host name given in the request.</span></span> <span data-ttu-id="2e382-157">WinINet utiliza una comprobación simple de los certificados comparando los nombres de host coincidentes y las reglas de carácter comodín simples.</span><span class="sxs-lookup"><span data-stu-id="2e382-157">WinINet uses a simple check against certificates by comparing for matching host names and simple wildcarding rules.</span></span> <span data-ttu-id="2e382-158">Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).</span><span class="sxs-lookup"><span data-stu-id="2e382-158">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-159"><span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**marca de INTERNET \_ \_ omitir \_ fecha de certificado \_ \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="2e382-159"><span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**INTERNET\_FLAG\_IGNORE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="2e382-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-161">Deshabilita la comprobación de certificados basados en SSL/PCT para las fechas de validez adecuadas.</span><span class="sxs-lookup"><span data-stu-id="2e382-161">Disables checking of SSL/PCT-based certificates for proper validity dates.</span></span> <span data-ttu-id="2e382-162">Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).</span><span class="sxs-lookup"><span data-stu-id="2e382-162">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-163"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**\_marca \_ de Internet omitir \_ redirección \_ a \_ http**</span><span class="sxs-lookup"><span data-stu-id="2e382-163"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**INTERNET\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-164">0x00008000</span><span class="sxs-lookup"><span data-stu-id="2e382-164">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-165">Deshabilita la detección de este tipo especial de redirección.</span><span class="sxs-lookup"><span data-stu-id="2e382-165">Disables detection of this special type of redirect.</span></span> <span data-ttu-id="2e382-166">Cuando se usa esta marca, WinINet permite redirigir de manera transparente a las direcciones URL de HTTPS a HTTP.</span><span class="sxs-lookup"><span data-stu-id="2e382-166">When this flag is used, WinINet transparently allows redirects from HTTPS to HTTP URLs.</span></span> <span data-ttu-id="2e382-167">Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).</span><span class="sxs-lookup"><span data-stu-id="2e382-167">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-168"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**\_marca \_ de Internet omitir \_ redirección \_ a \_ https**</span><span class="sxs-lookup"><span data-stu-id="2e382-168"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**INTERNET\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-169">0x00004000</span><span class="sxs-lookup"><span data-stu-id="2e382-169">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-170">Deshabilita la detección de este tipo especial de redirección.</span><span class="sxs-lookup"><span data-stu-id="2e382-170">Disables detection of this special type of redirect.</span></span> <span data-ttu-id="2e382-171">Cuando se usa esta marca, WinINet permite redirigir de forma transparente las direcciones URL de HTTP a HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2e382-171">When this flag is used, WinINet transparently allow redirects from HTTP to HTTPS URLs.</span></span> <span data-ttu-id="2e382-172">Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).</span><span class="sxs-lookup"><span data-stu-id="2e382-172">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-173"><span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**marca de INTERNET \_ \_ mantener \_ conexión**</span><span class="sxs-lookup"><span data-stu-id="2e382-173"><span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**INTERNET\_FLAG\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-174">0x00400000</span><span class="sxs-lookup"><span data-stu-id="2e382-174">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-175">Usa la semántica Keep-Alive, si está disponible, para la conexión.</span><span class="sxs-lookup"><span data-stu-id="2e382-175">Uses keep-alive semantics, if available, for the connection.</span></span> <span data-ttu-id="2e382-176">Esta marca la usan [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).</span><span class="sxs-lookup"><span data-stu-id="2e382-176">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span> <span data-ttu-id="2e382-177">Esta marca es necesaria para Microsoft Network (MSN), NTLM y otros tipos de autenticación.</span><span class="sxs-lookup"><span data-stu-id="2e382-177">This flag is required for Microsoft Network (MSN), NTLM, and other types of authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-178"><span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**marca de INTERNET para \_ \_ hacer \_ persistente**</span><span class="sxs-lookup"><span data-stu-id="2e382-178"><span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-179">0x02000000</span><span class="sxs-lookup"><span data-stu-id="2e382-179">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-180">Ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="2e382-180">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-181"><span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**la \_ marca de Internet \_ debe \_ almacenar en caché la \_ solicitud**</span><span class="sxs-lookup"><span data-stu-id="2e382-181"><span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e382-182">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="2e382-183">Es idéntico al valor preferido, **el \_ \_ \_ archivo** de la marca de Internet.</span><span class="sxs-lookup"><span data-stu-id="2e382-183">Identical to the preferred value, **INTERNET\_FLAG\_NEED\_FILE**.</span></span> <span data-ttu-id="2e382-184">Hace que se cree un archivo temporal si el archivo no se puede almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="2e382-184">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="2e382-185">Esta marca puede ser utilizada por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="2e382-185">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="2e382-186">**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se usa en [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="2e382-186">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-187"><span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**\_archivo de \_ necesidad de marca de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-187"><span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**INTERNET\_FLAG\_NEED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-188">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e382-188">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="2e382-189">Hace que se cree un archivo temporal si el archivo no se puede almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="2e382-189">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="2e382-190">Esta marca puede ser utilizada por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="2e382-190">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="2e382-191">**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se usa en [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="2e382-191">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-192"><span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**marca de INTERNET \_ \_ sin \_ autenticación**</span><span class="sxs-lookup"><span data-stu-id="2e382-192"><span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**INTERNET\_FLAG\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-193">0x00040000</span><span class="sxs-lookup"><span data-stu-id="2e382-193">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-194">No intenta realizar la autenticación automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2e382-194">Does not attempt authentication automatically.</span></span> <span data-ttu-id="2e382-195">Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).</span><span class="sxs-lookup"><span data-stu-id="2e382-195">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-196"><span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**marca de INTERNET \_ \_ sin \_ \_ redirección automática**</span><span class="sxs-lookup"><span data-stu-id="2e382-196"><span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**INTERNET\_FLAG\_NO\_AUTO\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-197">0x00200000</span><span class="sxs-lookup"><span data-stu-id="2e382-197">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-198">No controla automáticamente la redirección en [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="2e382-198">Does not automatically handle redirection in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="2e382-199">Esta marca también la puede usar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para las solicitudes HTTP.</span><span class="sxs-lookup"><span data-stu-id="2e382-199">This flag can also be used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) for HTTP requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-200"><span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**marca de INTERNET \_ \_ sin \_ escritura de caché \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-200"><span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-201">0x04000000</span><span class="sxs-lookup"><span data-stu-id="2e382-201">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-202">No agrega la entidad devuelta a la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="2e382-202">Does not add the returned entity to the cache.</span></span> <span data-ttu-id="2e382-203">Esta marca se usa en, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="2e382-203">This flag is used by , [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="2e382-204">**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se usa en [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="2e382-204">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-205"><span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**marca de INTERNET \_ \_ sin \_ cookies**</span><span class="sxs-lookup"><span data-stu-id="2e382-205"><span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**INTERNET\_FLAG\_NO\_COOKIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-206">0x00080000</span><span class="sxs-lookup"><span data-stu-id="2e382-206">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-207">No agrega automáticamente encabezados de cookies a las solicitudes y no agrega automáticamente las cookies devueltas a la base de datos de cookies.</span><span class="sxs-lookup"><span data-stu-id="2e382-207">Does not automatically add cookie headers to requests, and does not automatically add returned cookies to the cookie database.</span></span> <span data-ttu-id="2e382-208">Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).</span><span class="sxs-lookup"><span data-stu-id="2e382-208">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-209"><span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**marca de INTERNET \_ \_ sin \_ interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="2e382-209"><span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**INTERNET\_FLAG\_NO\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="2e382-210">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="2e382-211">Deshabilita el cuadro de diálogo cookie.</span><span class="sxs-lookup"><span data-stu-id="2e382-211">Disables the cookie dialog box.</span></span> <span data-ttu-id="2e382-212">Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo solicitudes HTTP).</span><span class="sxs-lookup"><span data-stu-id="2e382-212">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-213"><span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**marca de INTERNET \_ \_ sin conexión**</span><span class="sxs-lookup"><span data-stu-id="2e382-213"><span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**INTERNET\_FLAG\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-214">0x01000000</span><span class="sxs-lookup"><span data-stu-id="2e382-214">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-215">Idéntico a **la \_ marca \_ de Internet de la \_ caché**.</span><span class="sxs-lookup"><span data-stu-id="2e382-215">Identical to **INTERNET\_FLAG\_FROM\_CACHE**.</span></span> <span data-ttu-id="2e382-216">No realiza solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="2e382-216">Does not make network requests.</span></span> <span data-ttu-id="2e382-217">Todas las entidades se devuelven desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="2e382-217">All entities are returned from the cache.</span></span> <span data-ttu-id="2e382-218">Si el elemento solicitado no está en la memoria caché, se devuelve un error adecuado, como archivo de ERROR \_ \_ no \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="2e382-218">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="2e382-219">Solo la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="2e382-219">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-220"><span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**marca de INTERNET \_ \_ pasivo**</span><span class="sxs-lookup"><span data-stu-id="2e382-220"><span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**INTERNET\_FLAG\_PASSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-221">0x08000000</span><span class="sxs-lookup"><span data-stu-id="2e382-221">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-222">Usa semántica de FTP pasivo.</span><span class="sxs-lookup"><span data-stu-id="2e382-222">Uses passive FTP semantics.</span></span> <span data-ttu-id="2e382-223">Solo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usan esta marca.</span><span class="sxs-lookup"><span data-stu-id="2e382-223">Only [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) use this flag.</span></span> <span data-ttu-id="2e382-224">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa esta marca para las solicitudes FTP y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa esta marca para los archivos y directorios FTP.</span><span class="sxs-lookup"><span data-stu-id="2e382-224">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses this flag for FTP requests, and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses this flag for FTP files and directories.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-225"><span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**marca de INTERNET \_ \_ pragma \_ nocache**</span><span class="sxs-lookup"><span data-stu-id="2e382-225"><span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-226">0x00000100</span><span class="sxs-lookup"><span data-stu-id="2e382-226">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="2e382-227">Fuerza la resolución de la solicitud por el servidor de origen, incluso si existe una copia almacenada en caché en el proxy.</span><span class="sxs-lookup"><span data-stu-id="2e382-227">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="2e382-228">La función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo en solicitudes HTTP y https) y la función [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usan esta marca.</span><span class="sxs-lookup"><span data-stu-id="2e382-228">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-229"><span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**\_ \_ datos sin procesar de marca de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-229"><span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**INTERNET\_FLAG\_RAW\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-230">0x40000000</span><span class="sxs-lookup"><span data-stu-id="2e382-230">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-231">Devuelve los datos como una estructura de [**\_ \_ datos de búsqueda de Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) al recuperar la información de directorio FTP.</span><span class="sxs-lookup"><span data-stu-id="2e382-231">Returns the data as a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure when retrieving FTP directory information.</span></span> <span data-ttu-id="2e382-232">Si no se especifica esta marca o si la llamada se realiza a través de un proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) devuelve la versión HTML del directorio.</span><span class="sxs-lookup"><span data-stu-id="2e382-232">If this flag is not specified or if the call is made through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) returns the HTML version of the directory.</span></span> <span data-ttu-id="2e382-233">Solo la función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="2e382-233">Only the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function uses this flag.</span></span>

<span data-ttu-id="2e382-234">**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También devuelve una estructura de [**\_ \_ datos de búsqueda Gopher**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) al recuperar la información del directorio Gopher.</span><span class="sxs-lookup"><span data-stu-id="2e382-234">**Windows XP and Windows Server 2003 R2 and earlier:** Also returns a [**GOPHER\_FIND\_DATA**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) structure when retrieving Gopher directory information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-235"><span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**\_ \_ captura previa de lectura de marca de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-235"><span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**INTERNET\_FLAG\_READ\_PREFETCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-236">0x00100000</span><span class="sxs-lookup"><span data-stu-id="2e382-236">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-237">Esta marca está deshabilitada actualmente.</span><span class="sxs-lookup"><span data-stu-id="2e382-237">This flag is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-238"><span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**RECARGA de la marca de INTERNET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-238"><span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**INTERNET\_FLAG\_RELOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-239">0x80000000</span><span class="sxs-lookup"><span data-stu-id="2e382-239">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-240">Fuerza una descarga del archivo, el objeto o el listado de directorio solicitado del servidor de origen, no de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="2e382-240">Forces a download of the requested file, object, or directory listing from the origin server, not from the cache.</span></span> <span data-ttu-id="2e382-241">Las funciones [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usan esta marca.</span><span class="sxs-lookup"><span data-stu-id="2e382-241">The [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) functions use this flag.</span></span>

<span data-ttu-id="2e382-242">**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se usa en [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="2e382-242">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-243"><span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**\_ \_ zona restringida de marca de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-243"><span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**INTERNET\_FLAG\_RESTRICTED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-244">0x00020000</span><span class="sxs-lookup"><span data-stu-id="2e382-244">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-245">Indica que la cookie que se está configurando está asociada a un sitio que no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="2e382-245">Indicates that the cookie being set is associated with an untrusted site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-246"><span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**marca de INTERNET volver a \_ \_ sincronizar**</span><span class="sxs-lookup"><span data-stu-id="2e382-246"><span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-247">0x00000800</span><span class="sxs-lookup"><span data-stu-id="2e382-247">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="2e382-248">Vuelve a cargar los recursos HTTP si el recurso se ha modificado desde la última vez que se descargó.</span><span class="sxs-lookup"><span data-stu-id="2e382-248">Reloads HTTP resources if the resource has been modified since the last time it was downloaded.</span></span> <span data-ttu-id="2e382-249">Se recargan todos los recursos FTP.</span><span class="sxs-lookup"><span data-stu-id="2e382-249">All FTP resources are reloaded.</span></span> <span data-ttu-id="2e382-250">Esta marca puede ser utilizada por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="2e382-250">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="2e382-251">**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También lo usan [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), y se recargan los recursos Gopher.</span><span class="sxs-lookup"><span data-stu-id="2e382-251">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), and Gopher resources are reloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-252"><span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**marca de INTERNET \_ \_ segura**</span><span class="sxs-lookup"><span data-stu-id="2e382-252"><span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**INTERNET\_FLAG\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-253">0x00800000</span><span class="sxs-lookup"><span data-stu-id="2e382-253">0x00800000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-254">Usa semántica de transacción segura.</span><span class="sxs-lookup"><span data-stu-id="2e382-254">Uses secure transaction semantics.</span></span> <span data-ttu-id="2e382-255">Esto se traduce en el uso de la tecnología de comunicaciones privadas (SSL/PCT) de Capa de sockets seguros y solo es significativo en las solicitudes HTTP.</span><span class="sxs-lookup"><span data-stu-id="2e382-255">This translates to using Secure Sockets Layer/Private Communications Technology (SSL/PCT) and is only meaningful in HTTP requests.</span></span> <span data-ttu-id="2e382-256">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)usan esta marca, pero es redundante si https://aparece en la dirección URL. La función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa esta marca para las conexiones http; todos los identificadores de solicitud creados en esta conexión heredarán esta marca.</span><span class="sxs-lookup"><span data-stu-id="2e382-256">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), but this is redundant if https:// appears in the URL.The [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function uses this flag for HTTP connections; all the request handles created under this connection will inherit this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-257"><span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**INTERNET \_ Flag \_ Transfer \_ ASCII**</span><span class="sxs-lookup"><span data-stu-id="2e382-257"><span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**INTERNET\_FLAG\_TRANSFER\_ASCII**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-258">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2e382-258">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="2e382-259">Transfiere el archivo como ASCII (solo FTP).</span><span class="sxs-lookup"><span data-stu-id="2e382-259">Transfers file as ASCII (FTP only).</span></span> <span data-ttu-id="2e382-260">Esta marca puede ser utilizada por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)y [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="2e382-260">This flag can be used by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), and [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-261"><span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**\_ \_ binario de transferencia de marca de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-261"><span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**INTERNET\_FLAG\_TRANSFER\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-262">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2e382-262">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="2e382-263">Transfiere el archivo como binario (solo FTP).</span><span class="sxs-lookup"><span data-stu-id="2e382-263">Transfers file as binary (FTP only).</span></span> <span data-ttu-id="2e382-264">Esta marca puede ser utilizada por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)y [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="2e382-264">This flag can be used by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), and [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-265"><span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**\_sin devolución de llamada de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-265"><span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e382-266">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="2e382-267">Indica que no se deben realizar devoluciones de llamada para esa API.</span><span class="sxs-lookup"><span data-stu-id="2e382-267">Indicates that no callbacks should be made for that API.</span></span> <span data-ttu-id="2e382-268">Se usa para el parámetro *dxContext* de las funciones que permiten operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="2e382-268">This is used for the *dxContext* parameter of the functions that allow asynchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-269"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**opción de INTERNET \_ \_ suprimir \_ autenticación de servidor \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-269"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-270">104</span><span class="sxs-lookup"><span data-stu-id="2e382-270">104</span></span>
</dt> <dt>



<span data-ttu-id="2e382-271">Establece un objeto de solicitud HTTP que no iniciará sesión en los servidores de origen, pero realizará el inicio de sesión automático en los servidores proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="2e382-271">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="2e382-272">Esta opción difiere de la marca de solicitud INTERNET \_ marca \_ no \_ auth, lo que impide la autenticación en los servidores proxy y los servidores de origen.</span><span class="sxs-lookup"><span data-stu-id="2e382-272">This option differs from the Request flag INTERNET\_FLAG\_NO\_AUTH, which prevents authentication to both proxy servers and origin servers.</span></span> <span data-ttu-id="2e382-273">Si se establece este modo, se suprimirá el uso de cualquier material de credencial (ya sea el nombre de usuario o la contraseña previamente o el certificado SSL de cliente) al comunicarse con un servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="2e382-273">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="2e382-274">Sin embargo, si la solicitud debe estar en tránsito a través de un proxy de autenticación, WinINet seguirá realizando la autenticación automática en el proxy HTTP según la configuración de la zona de intranet del usuario.</span><span class="sxs-lookup"><span data-stu-id="2e382-274">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="2e382-275">La configuración de la zona de intranet predeterminada es permitir el inicio de sesión automático con las credenciales predeterminadas del usuario.</span><span class="sxs-lookup"><span data-stu-id="2e382-275">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span> <span data-ttu-id="2e382-276">Para garantizar la supresión de toda la información de identificación, el autor de la llamada debe combinar la opción de INTERNET \_ \_ suprimir \_ autenticación de servidor \_ con la \_ marca de \_ solicitud marcar sin \_ cookies.</span><span class="sxs-lookup"><span data-stu-id="2e382-276">To ensure suppression of all identifying information, the caller should combine INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH with the INTERNET\_FLAG\_NO\_COOKIES request flag.</span></span> <span data-ttu-id="2e382-277">Esta opción solo se puede establecer en los objetos de solicitud antes de que se hayan enviado.</span><span class="sxs-lookup"><span data-stu-id="2e382-277">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="2e382-278">Si se intenta establecer esta opción una vez enviada la solicitud, se devolverá el \_ \_ Estado de identificador incorrecto de Internet \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2e382-278">Attempts to set this option after the request has been sent will return ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE.</span></span> <span data-ttu-id="2e382-279">No se requiere ningún búfer para esta opción.</span><span class="sxs-lookup"><span data-stu-id="2e382-279">No buffer is required for this option.</span></span> <span data-ttu-id="2e382-280">InternetSetOption lo usa solo en los identificadores devueltos por HttpOpenRequest.</span><span class="sxs-lookup"><span data-stu-id="2e382-280">This is used by InternetSetOption on handles returned by HttpOpenRequest only.</span></span> <span data-ttu-id="2e382-281">Versión: requiere Internet Explorer 8,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2e382-281">Version: Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-282"><span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**\_marca de API WinInet \_ \_ asincrónica**</span><span class="sxs-lookup"><span data-stu-id="2e382-282"><span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**WININET\_API\_FLAG\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2e382-283">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="2e382-284">Fuerza las operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="2e382-284">Forces asynchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-285"><span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**\_sincronización de \_ marca de API de WinInet \_**</span><span class="sxs-lookup"><span data-stu-id="2e382-285"><span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**WININET\_API\_FLAG\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-286">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2e382-286">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="2e382-287">Fuerza las operaciones sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="2e382-287">Forces synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e382-288"><span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**marca de API de WININET \_ \_ \_ usar \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="2e382-288"><span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**WININET\_API\_FLAG\_USE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e382-289">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2e382-289">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="2e382-290">Fuerza a la API a usar el valor de contexto, incluso si se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="2e382-290">Forces the API to use the context value, even if it is set to zero.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e382-291">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e382-291">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2e382-292">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="2e382-292">WinINet does not support server implementations.</span></span> <span data-ttu-id="2e382-293">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="2e382-293">In addition, it should not be used from a service.</span></span> <span data-ttu-id="2e382-294">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="2e382-294">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e382-295">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e382-295">Requirements</span></span>



| <span data-ttu-id="2e382-296">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e382-296">Requirement</span></span> | <span data-ttu-id="2e382-297">Value</span><span class="sxs-lookup"><span data-stu-id="2e382-297">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2e382-298">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e382-298">Minimum supported client</span></span><br/> | <span data-ttu-id="2e382-299">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2e382-299">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2e382-300">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e382-300">Minimum supported server</span></span><br/> | <span data-ttu-id="2e382-301">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e382-301">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2e382-302">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e382-302">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e382-303"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e382-303"><dt>Wininet.h</dt></span></span> </dl> |



 

