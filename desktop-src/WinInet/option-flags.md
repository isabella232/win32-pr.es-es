---
title: Marcas de opciones (Wininet. h)
description: Las marcas de opciones siguientes se usan con las funciones InternetQueryOption y InternetSetOption. Todas las marcas de opciones válidas tienen un valor mayor o igual que INTERNET \_ primera \_ opción y menor o igual que Internet \_ última \_ opción.
ms.assetid: 708510b8-468a-4287-849b-cba3d7001ea8
topic_type:
- apiref
api_name:
- INTERNET_OPTION_ALTER_IDENTITY
- INTERNET_OPTION_ASYNC
- INTERNET_OPTION_ASYNC_ID
- INTERNET_OPTION_ASYNC_PRIORITY
- INTERNET_OPTION_BYPASS_EDITED_ENTRY
- INTERNET_OPTION_CACHE_STREAM_HANDLE
- INTERNET_OPTION_CACHE_TIMESTAMPS
- INTERNET_OPTION_CALLBACK
- INTERNET_OPTION_CALLBACK_FILTER
- INTERNET_OPTION_CLIENT_CERT_CONTEXT
- INTERNET_OPTION_CODEPAGE
- INTERNET_OPTION_CODEPAGE_PATH
- INTERNET_OPTION_CODEPAGE_EXTRA
- INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH
- INTERNET_OPTION_CONNECT_BACKOFF
- INTERNET_OPTION_CONNECT_RETRIES
- INTERNET_OPTION_CONNECT_TIME
- INTERNET_OPTION_CONNECT_TIMEOUT
- INTERNET_OPTION_CONNECTED_STATE
- INTERNET_OPTION_CONTEXT_VALUE
- INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT
- INTERNET_OPTION_CONTROL_SEND_TIMEOUT
- INTERNET_OPTION_DATA_RECEIVE_TIMEOUT
- INTERNET_OPTION_DATA_SEND_TIMEOUT
- INTERNET_OPTION_DATAFILE_NAME
- INTERNET_OPTION_DATAFILE_EXT
- INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO
- INTERNET_OPTION_DIGEST_AUTH_UNLOAD
- INTERNET_OPTION_DISABLE_AUTODIAL
- INTERNET_OPTION_DISCONNECTED_TIMEOUT
- INTERNET_OPTION_ENABLE_HTTP_PROTOCOL
- INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ
- INTERNET_OPTION_ENCODE_EXTRA
- INTERNET_OPTION_END_BROWSER_SESSION
- INTERNET_OPTION_ERROR_MASK
- INTERNET_OPTION_ENTERPRISE_CONTEXT
- INTERNET_OPTION_EXTENDED_ERROR
- INTERNET_OPTION_FROM_CACHE_TIMEOUT
- INTERNET_OPTION_HANDLE_TYPE
- INTERNET_OPTION_HSTS
- INTERNET_OPTION_HTTP_DECODING
- INTERNET_OPTION_HTTP_PROTOCOL_USED
- INTERNET_OPTION_HTTP_VERSION
- INTERNET_OPTION_IDENTITY
- INTERNET_OPTION_IDLE_STATE
- INTERNET_OPTION_IDN
- INTERNET_OPTION_IGNORE_OFFLINE
- INTERNET_OPTION_KEEP_CONNECTION
- INTERNET_OPTION_LISTEN_TIMEOUT
- INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER
- INTERNET_OPTION_MAX_CONNS_PER_PROXY
- INTERNET_OPTION_MAX_CONNS_PER_SERVER
- INTERNET_OPTION_OFFLINE_MODE
- INTERNET_OPTION_OFFLINE_SEMANTICS
- INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE
- INTERNET_OPTION_PARENT_HANDLE
- INTERNET_OPTION_PASSWORD
- INTERNET_OPTION_PER_CONNECTION_OPTION
- INTERNET_OPTION_POLICY
- INTERNET_OPTION_PROXY
- INTERNET_OPTION_PROXY_PASSWORD
- INTERNET_OPTION_PROXY_SETTINGS_CHANGED
- INTERNET_OPTION_PROXY_USERNAME
- INTERNET_OPTION_READ_BUFFER_SIZE
- INTERNET_OPTION_RECEIVE_THROUGHPUT
- INTERNET_OPTION_RECEIVE_TIMEOUT
- INTERNET_OPTION_REFRESH
- INTERNET_OPTION_REMOVE_IDENTITY
- INTERNET_OPTION_REQUEST_FLAGS
- INTERNET_OPTION_REQUEST_PRIORITY
- INTERNET_OPTION_RESET_URLCACHE_SESSION
- INTERNET_OPTION_SECONDARY_CACHE_KEY
- INTERNET_OPTION_SECURITY_CERTIFICATE
- INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT
- INTERNET_OPTION_SECURITY_FLAGS
- INTERNET_OPTION_SECURITY_KEY_BITNESS
- INTERNET_OPTION_SEND_THROUGHPUT
- INTERNET_OPTION_SEND_TIMEOUT
- INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT
- INTERNET_OPTION_SETTINGS_CHANGED
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- INTERNET_OPTION_SUPPRESS_BEHAVIOR
- INTERNET_OPTION_URL
- INTERNET_OPTION_USER_AGENT
- INTERNET_OPTION_USERNAME
- INTERNET_OPTION_VERSION
- INTERNET_OPTION_WRITE_BUFFER_SIZE
api_location:
- Wininet.h
- Winineti.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c99ca6f12836c620ed7c952e0ceb1844aee3b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677011"
---
# <a name="option-flags-winineth"></a><span data-ttu-id="bf775-104">Marcas de opciones (Wininet. h)</span><span class="sxs-lookup"><span data-stu-id="bf775-104">Option Flags (Wininet.h)</span></span>

<span data-ttu-id="bf775-105">Las marcas de opciones siguientes se usan con las funciones [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) .</span><span class="sxs-lookup"><span data-stu-id="bf775-105">The following option flags are used with the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) functions.</span></span> <span data-ttu-id="bf775-106">Todas las marcas de opciones válidas tienen un valor mayor o igual que **Internet \_ primera \_ opción** y menor o igual que **Internet \_ última \_ opción**.</span><span class="sxs-lookup"><span data-stu-id="bf775-106">All valid option flags have a value greater than or equal to **INTERNET\_FIRST\_OPTION** and less than or equal to **INTERNET\_LAST\_OPTION**.</span></span>

<dl> <dt>

<span data-ttu-id="bf775-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**opción de INTERNET \_ \_ ALTER \_ Identity**</span><span class="sxs-lookup"><span data-stu-id="bf775-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**INTERNET\_OPTION\_ALTER\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-108">80</span><span class="sxs-lookup"><span data-stu-id="bf775-108">80</span></span>
</dt> <dt>



<span data-ttu-id="bf775-109">No implementado</span><span class="sxs-lookup"><span data-stu-id="bf775-109">Not implemented</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**opción de INTERNET \_ \_ Async**</span><span class="sxs-lookup"><span data-stu-id="bf775-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**INTERNET\_OPTION\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-111">30</span><span class="sxs-lookup"><span data-stu-id="bf775-111">30</span></span>
</dt> <dt>



<span data-ttu-id="bf775-112">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-112">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**\_ \_ identificador asincrónico de la opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**INTERNET\_OPTION\_ASYNC\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-114">15</span><span class="sxs-lookup"><span data-stu-id="bf775-114">15</span></span>
</dt> <dt>



<span data-ttu-id="bf775-115">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-115">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**\_opción de \_ Internet \_ prioridad asincrónica**</span><span class="sxs-lookup"><span data-stu-id="bf775-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**INTERNET\_OPTION\_ASYNC\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-117">16</span><span class="sxs-lookup"><span data-stu-id="bf775-117">16</span></span>
</dt> <dt>



<span data-ttu-id="bf775-118">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-118">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**opción de INTERNET \_ \_ omitir \_ entrada editada \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**INTERNET\_OPTION\_BYPASS\_EDITED\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-120">64</span><span class="sxs-lookup"><span data-stu-id="bf775-120">64</span></span>
</dt> <dt>



<span data-ttu-id="bf775-121">Establece o recupera el valor booleano que determina si el sistema debe comprobar si el contenido de la red es más reciente y sobrescribir las entradas de caché editadas si se encuentra una versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="bf775-121">Sets or retrieves the Boolean value that determines if the system should check the network for newer content and overwrite edited cache entries if a newer version is found.</span></span> <span data-ttu-id="bf775-122">Si se establece en true, el sistema comprueba si el contenido de la red **es** más reciente y sobrescribe la entrada de caché editada con la versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="bf775-122">If set to **True**, the system checks the network for newer content and overwrites the edited cache entry with the newer version.</span></span> <span data-ttu-id="bf775-123">El valor predeterminado es **false**, que indica que la entrada de caché modificada debe usarse sin comprobar la red.</span><span class="sxs-lookup"><span data-stu-id="bf775-123">The default is **False**, which indicates that the edited cache entry should be used without checking the network.</span></span> <span data-ttu-id="bf775-124">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-124">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="bf775-125">Solo es válido en Microsoft Internet Explorer 5 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-125">It is valid only in Microsoft Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**opción de INTERNET \_ \_ identificador de secuencia de caché \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**INTERNET\_OPTION\_CACHE\_STREAM\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-127">27</span><span class="sxs-lookup"><span data-stu-id="bf775-127">27</span></span>
</dt> <dt>



<span data-ttu-id="bf775-128">Ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf775-128">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**marcas de tiempo de opciones de INTERNET de \_ \_ caché \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**INTERNET\_OPTION\_CACHE\_TIMESTAMPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-130">69</span><span class="sxs-lookup"><span data-stu-id="bf775-130">69</span></span>
</dt> <dt>



<span data-ttu-id="bf775-131">Recupera una estructura [**de \_ \_ marcas**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) de tiempo de la caché de Internet que contiene la hora de la LastModified y expira el tiempo del recurso almacenado en la caché de Internet.</span><span class="sxs-lookup"><span data-stu-id="bf775-131">Retrieves an [**INTERNET\_CACHE\_TIMESTAMPS**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) structure that contains the LastModified time and Expires time from the resource stored in the Internet cache.</span></span> <span data-ttu-id="bf775-132">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)usa este valor.</span><span class="sxs-lookup"><span data-stu-id="bf775-132">This value is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**devolución de llamada de \_ opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**INTERNET\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-134">1</span><span class="sxs-lookup"><span data-stu-id="bf775-134">1</span></span>
</dt> <dt>



<span data-ttu-id="bf775-135">Establece o recupera la dirección de la función de devolución de llamada definida para este identificador.</span><span class="sxs-lookup"><span data-stu-id="bf775-135">Sets or retrieves the address of the callback function defined for this handle.</span></span> <span data-ttu-id="bf775-136">Esta opción se puede usar en todos los identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="bf775-136">This option can be used on all [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="bf775-137">Usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-137">Used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**\_filtro de \_ devolución de llamada de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**INTERNET\_OPTION\_CALLBACK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-139">54</span><span class="sxs-lookup"><span data-stu-id="bf775-139">54</span></span>
</dt> <dt>



<span data-ttu-id="bf775-140">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-140">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**\_contexto de \_ certificado de cliente de opción de Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**INTERNET\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-142">84</span><span class="sxs-lookup"><span data-stu-id="bf775-142">84</span></span>
</dt> <dt>



<span data-ttu-id="bf775-143">Esta marca no es compatible con [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-143">This flag is not supported by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="bf775-144">El parámetro *lpBuffer* debe ser un puntero a una estructura de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) y no un puntero a un puntero de **\_ contexto de certificado** .</span><span class="sxs-lookup"><span data-stu-id="bf775-144">The *lpBuffer* parameter must be a pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure and not a pointer to a **CERT\_CONTEXT** pointer.</span></span> <span data-ttu-id="bf775-145">Si una aplicación recibe el error se necesita el **\_ \_ certificado de autenticación de cliente \_ \_ \_ de Internet**, debe llamar a [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) o usar [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para proporcionar un certificado antes de volver a intentar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf775-145">If an application receives **ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**, it must call [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or use [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="bf775-146">A continuación, se llama a [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) para que la aplicación pueda publicar de forma independiente el contexto de certificado que se pasa.</span><span class="sxs-lookup"><span data-stu-id="bf775-146">[**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) is then called so that the certificate context passed can be independently released by the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**Página de códigos de la opción de INTERNET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**INTERNET\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-148">68</span><span class="sxs-lookup"><span data-stu-id="bf775-148">68</span></span>
</dt> <dt>



<span data-ttu-id="bf775-149">De forma predeterminada, la parte de host o de autoridad de la dirección URL de Unicode se codifica según la especificación de IDN.</span><span class="sxs-lookup"><span data-stu-id="bf775-149">By default, the host or authority portion of the Unicode URL is encoded according to the IDN specification.</span></span> <span data-ttu-id="bf775-150">Al establecer esta opción en la solicitud o el identificador de conexión, cuando se deshabilita IDN, se especifica un esquema de codificación de página de códigos para la parte del host de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="bf775-150">Setting this option on the request, or connection handle, when IDN is disabled, specifies a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="bf775-151">El parámetro *lpBuffer* de la llamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contiene la página de códigos DBCS deseada.</span><span class="sxs-lookup"><span data-stu-id="bf775-151">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS code page.</span></span> <span data-ttu-id="bf775-152">Si no se especifica ninguna página de códigos en *lpBuffer*, WinInet utiliza la página de códigos predeterminada del sistema (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="bf775-152">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span> <span data-ttu-id="bf775-153">Nota: esta opción se omite si no se deshabilita IDN.</span><span class="sxs-lookup"><span data-stu-id="bf775-153">Note: This option is ignored if IDN is not disabled.</span></span> <span data-ttu-id="bf775-154">Para obtener más información sobre cómo deshabilitar IDN, consulte la opción de **Internet \_ \_ IDN** .</span><span class="sxs-lookup"><span data-stu-id="bf775-154">For more information about how to disable IDN, see the **INTERNET\_OPTION\_IDN** option.</span></span>

<span data-ttu-id="bf775-155">**Windows XP con SP2 y Windows Server 2003 con SP1:** Esta marca no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf775-155">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="bf775-156">**Versión:** Requiere Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="bf775-156">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**\_ruta de \_ acceso de página de la opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**INTERNET\_OPTION\_CODEPAGE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-158">100</span><span class="sxs-lookup"><span data-stu-id="bf775-158">100</span></span>
</dt> <dt>



<span data-ttu-id="bf775-159">De forma predeterminada, la parte de la ruta de acceso de la dirección URL está codificada en UTF8.</span><span class="sxs-lookup"><span data-stu-id="bf775-159">By default, the path portion of the URL is UTF8 encoded.</span></span> <span data-ttu-id="bf775-160">La API WinINet realiza el carácter de escape (%) codificación en los caracteres de bit alto.</span><span class="sxs-lookup"><span data-stu-id="bf775-160">The WinINet API performs escape character (%) encoding on the high-bit characters.</span></span> <span data-ttu-id="bf775-161">Al establecer esta opción en la solicitud o el identificador de conexión, se deshabilita la codificación UTF8 y se establece una página de códigos específica.</span><span class="sxs-lookup"><span data-stu-id="bf775-161">Setting this option on the request, or connection handle, disables the UTF8 encoding and sets a specific code page.</span></span> <span data-ttu-id="bf775-162">El parámetro *lpBuffer* de la llamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contiene la página de códigos DBCS deseada para la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="bf775-162">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the path.</span></span> <span data-ttu-id="bf775-163">Si no se especifica ninguna página de códigos en *lpBuffer*, WinInet usa el CP \_ UTF8 predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bf775-163">If no code page is specified in *lpBuffer*, WinINet uses the default CP\_UTF8.</span></span>

<span data-ttu-id="bf775-164">**Windows XP con SP2 y Windows Server 2003 con SP1:** Esta marca no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf775-164">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="bf775-165">**Versión:** Requiere Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="bf775-165">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**Página de códigos de opciones de INTERNET \_ \_ \_ extra**</span><span class="sxs-lookup"><span data-stu-id="bf775-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**INTERNET\_OPTION\_CODEPAGE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-167">101</span><span class="sxs-lookup"><span data-stu-id="bf775-167">101</span></span>
</dt> <dt>



<span data-ttu-id="bf775-168">De forma predeterminada, la parte de la ruta de acceso de la dirección URL es la página de códigos predeterminada del sistema (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="bf775-168">By default, the path portion of the URL is the default system code page (CP\_ACP).</span></span> <span data-ttu-id="bf775-169">El carácter de escape (%) no se realizan conversiones en la parte adicional.</span><span class="sxs-lookup"><span data-stu-id="bf775-169">The escape character (%) conversions are not performed on the extra portion.</span></span> <span data-ttu-id="bf775-170">Si se establece esta opción en la solicitud o el identificador de conexión, se deshabilita la \_ codificación CP ACP.</span><span class="sxs-lookup"><span data-stu-id="bf775-170">Setting this option on the request, or connection handle disables the CP\_ACP encoding.</span></span> <span data-ttu-id="bf775-171">El parámetro *lpBuffer* de la llamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contiene la página de códigos DBCS deseada para la parte adicional de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="bf775-171">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the extra portion of the URL.</span></span> <span data-ttu-id="bf775-172">Si no se especifica ninguna página de códigos en *lpBuffer*, WinInet utiliza la página de códigos predeterminada del sistema (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="bf775-172">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="bf775-173">**Windows XP con SP2 y Windows Server 2003 con SP1:** Esta marca no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf775-173">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="bf775-174">**Versión:** Requiere Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="bf775-174">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**\_longitud de \_ \_ contenido comprimido \_ de la opción de Internet**</span><span class="sxs-lookup"><span data-stu-id="bf775-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**INTERNET\_OPTION\_COMPRESSED\_CONTENT\_LENGTH**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-176">147</span><span class="sxs-lookup"><span data-stu-id="bf775-176">147</span></span>
</dt> <dt>



<span data-ttu-id="bf775-177">En el caso de una solicitud en la que WinInet descomprimió la codificación de contenido suministrada por el servidor, recupera la longitud del contenido del cuerpo de la respuesta como ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="bf775-177">For a request where WinInet decompressed the server s supplied Content-Encoding, retrieves the server-reported Content-Length of the response body as a ULONGLONG.</span></span> <span data-ttu-id="bf775-178">Compatible con Windows 10, versión 1507 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-178">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**\_retroceso de \_ conexión de opciones de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**INTERNET\_OPTION\_CONNECT\_BACKOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-180">4</span><span class="sxs-lookup"><span data-stu-id="bf775-180">4</span></span>
</dt> <dt>



<span data-ttu-id="bf775-181">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-181">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**reintentos de conexión de opciones de INTERNET \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**INTERNET\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-183">3</span><span class="sxs-lookup"><span data-stu-id="bf775-183">3</span></span>
</dt> <dt>



<span data-ttu-id="bf775-184">Establece o recupera un valor entero largo sin signo que contiene el número de veces que WinINet intenta resolver y conectarse a un host.</span><span class="sxs-lookup"><span data-stu-id="bf775-184">Sets or retrieves an unsigned long integer value that contains the number of times WinINet attempts to resolve and connect to a host.</span></span> <span data-ttu-id="bf775-185">Solo se intenta una vez por cada dirección IP.</span><span class="sxs-lookup"><span data-stu-id="bf775-185">It only attempts once per IP address.</span></span> <span data-ttu-id="bf775-186">Por ejemplo, si intenta conectarse a un host multihome que tiene diez direcciones IP y \_ la opción Internet \_ Connect \_ reintentos está establecida en siete, WinInet solo intenta resolver y conectarse a las siete primeras direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="bf775-186">For example, if you attempt to connect to a multihome host that has ten IP addresses and INTERNET\_OPTION\_CONNECT\_RETRIES is set to seven, WinINet only attempts to resolve and connect to the first seven IP addresses.</span></span> <span data-ttu-id="bf775-187">Por el contrario, dado el mismo conjunto de diez direcciones IP, si la \_ opción \_ de Internet conectar \_ reintentos está establecida en 20, WinInet intenta cada una de las diez solo una vez.</span><span class="sxs-lookup"><span data-stu-id="bf775-187">Conversely, given the same set of ten IP addresses, if INTERNET\_OPTION\_CONNECT\_RETRIES is set to 20, WinINet attempts each of the ten only once.</span></span> <span data-ttu-id="bf775-188">Si un host solo tiene una dirección IP y se produce un error en el primer intento de conexión, no hay más intentos.</span><span class="sxs-lookup"><span data-stu-id="bf775-188">If a host has only one IP address and the first connection attempt fails, there are no further attempts.</span></span> <span data-ttu-id="bf775-189">Si un intento de conexión sigue sin funcionar después del número especificado de intentos, se cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf775-189">If a connection attempt still fails after the specified number of attempts, the request is canceled.</span></span> <span data-ttu-id="bf775-190">El valor predeterminado para la \_ opción de Internet \_ Connect \_ reintentos es de cinco intentos.</span><span class="sxs-lookup"><span data-stu-id="bf775-190">The default value for INTERNET\_OPTION\_CONNECT\_RETRIES is five attempts.</span></span> <span data-ttu-id="bf775-191">Esta opción se puede utilizar en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluido un identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="bf775-191">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="bf775-192">Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-192">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**tiempo de conexión de la opción de INTERNET \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**INTERNET\_OPTION\_CONNECT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-194">55</span><span class="sxs-lookup"><span data-stu-id="bf775-194">55</span></span>
</dt> <dt>



<span data-ttu-id="bf775-195">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-195">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**\_tiempo de \_ espera de conexión de opciones de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**INTERNET\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-197">2</span><span class="sxs-lookup"><span data-stu-id="bf775-197">2</span></span>
</dt> <dt>



<span data-ttu-id="bf775-198">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, que se va a usar para las solicitudes de conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="bf775-198">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to use for Internet connection requests.</span></span> <span data-ttu-id="bf775-199">Si se establece esta opción en infinita (0xFFFFFFFF), se deshabilitará este temporizador.</span><span class="sxs-lookup"><span data-stu-id="bf775-199">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="bf775-200">Si una solicitud de conexión tarda más que este valor de tiempo de espera, se cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf775-200">If a connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="bf775-201">Al intentar conectarse a varias direcciones IP para un único host (un host de múltiples hosts), el límite de tiempo de espera es acumulativo para todas las direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="bf775-201">When attempting to connect to multiple IP addresses for a single host (a multihome host), the timeout limit is cumulative for all of the IP addresses.</span></span> <span data-ttu-id="bf775-202">Esta opción se puede utilizar en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluido un identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="bf775-202">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="bf775-203">Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-203">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**Estado de conexión de la opción de INTERNET \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**INTERNET\_OPTION\_CONNECTED\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-205">50</span><span class="sxs-lookup"><span data-stu-id="bf775-205">50</span></span>
</dt> <dt>



<span data-ttu-id="bf775-206">Establece o recupera un valor entero largo sin signo que contiene el estado conectado.</span><span class="sxs-lookup"><span data-stu-id="bf775-206">Sets or retrieves an unsigned long integer value that contains the connected state.</span></span> <span data-ttu-id="bf775-207">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-207">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**\_valor de \_ contexto de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**INTERNET\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-209">45</span><span class="sxs-lookup"><span data-stu-id="bf775-209">45</span></span>
</dt> <dt>



<span data-ttu-id="bf775-210">Establece o recupera un valor de DWORD \_ ptr que contiene la dirección del valor de contexto asociado a este identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="bf775-210">Sets or retrieves a DWORD\_PTR that contains the address of the context value associated with this [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="bf775-211">Esta opción puede usarse en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="bf775-211">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="bf775-212">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-212">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="bf775-213">Anteriormente, esto establece el valor de contexto en la dirección almacenada en el puntero **lpBuffer** .</span><span class="sxs-lookup"><span data-stu-id="bf775-213">Previously, this set the context value to the address stored in the **lpBuffer** pointer.</span></span> <span data-ttu-id="bf775-214">Esto se ha corregido para que se utilice el valor almacenado en el búfer y se asigne un nuevo valor a la marca de [valor de contexto de opción de Internet \_ \_ \_ ](/windows) .</span><span class="sxs-lookup"><span data-stu-id="bf775-214">This has been corrected so that the value stored in the buffer is used and the [INTERNET\_OPTION\_CONTEXT\_VALUE](/windows) flag is assigned a new value.</span></span> <span data-ttu-id="bf775-215">El valor anterior, 10, se ha conservado para que las aplicaciones escritas para el comportamiento anterior sigan siendo compatibles.</span><span class="sxs-lookup"><span data-stu-id="bf775-215">The old value, 10, has been preserved so that applications written for the old behavior are still supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**\_tiempo de \_ espera de recepción del control de opciones de \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**INTERNET\_OPTION\_CONTROL\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-217">6</span><span class="sxs-lookup"><span data-stu-id="bf775-217">6</span></span>
</dt> <dt>



<span data-ttu-id="bf775-218">Idéntico al [ \_ tiempo de \_ \_ espera de recepción](/windows)de la opción de Internet.</span><span class="sxs-lookup"><span data-stu-id="bf775-218">Identical to [INTERNET\_OPTION\_RECEIVE\_TIMEOUT](/windows).</span></span> <span data-ttu-id="bf775-219">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-219">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**\_tiempo de \_ espera de envío de control de opciones de \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**INTERNET\_OPTION\_CONTROL\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-221">5</span><span class="sxs-lookup"><span data-stu-id="bf775-221">5</span></span>
</dt> <dt>



<span data-ttu-id="bf775-222">Idéntico a la [opción de Internet de tiempo de \_ \_ \_ espera de envío](/windows).</span><span class="sxs-lookup"><span data-stu-id="bf775-222">Identical to [INTERNET\_OPTION\_SEND\_TIMEOUT](/windows).</span></span> <span data-ttu-id="bf775-223">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-223">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**\_tiempo de \_ espera de recepción de datos de opción de \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**INTERNET\_OPTION\_DATA\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-225">8</span><span class="sxs-lookup"><span data-stu-id="bf775-225">8</span></span>
</dt> <dt>



<span data-ttu-id="bf775-226">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para recibir una respuesta a una solicitud del canal de datos de una transacción FTP.</span><span class="sxs-lookup"><span data-stu-id="bf775-226">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="bf775-227">Si la respuesta tarda más que este valor de tiempo de espera, se cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf775-227">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="bf775-228">Esta opción se puede utilizar en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluido un identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="bf775-228">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="bf775-229">Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-229">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="bf775-230">Esta marca no tiene ningún impacto en la funcionalidad HTTP.</span><span class="sxs-lookup"><span data-stu-id="bf775-230">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**\_tiempo de \_ espera de envío de datos de opción de \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**INTERNET\_OPTION\_DATA\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-232">7</span><span class="sxs-lookup"><span data-stu-id="bf775-232">7</span></span>
</dt> <dt>



<span data-ttu-id="bf775-233">Establece o recupera un valor entero largo sin signo, en milisegundos, que contiene el valor de tiempo de espera para enviar una solicitud para el canal de datos de una transacción FTP.</span><span class="sxs-lookup"><span data-stu-id="bf775-233">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="bf775-234">Si el envío tarda más que este valor de tiempo de espera, se cancela el envío.</span><span class="sxs-lookup"><span data-stu-id="bf775-234">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="bf775-235">Esta opción se puede utilizar en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluido un identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="bf775-235">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="bf775-236">Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-236">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="bf775-237">Esta marca no tiene ningún impacto en la funcionalidad HTTP.</span><span class="sxs-lookup"><span data-stu-id="bf775-237">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**nombre de archivo de la opción de INTERNET \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**INTERNET\_OPTION\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-239">33</span><span class="sxs-lookup"><span data-stu-id="bf775-239">33</span></span>
</dt> <dt>



<span data-ttu-id="bf775-240">Recupera un valor de cadena que contiene el nombre del archivo que realiza la copia de seguridad de una entidad descargada.</span><span class="sxs-lookup"><span data-stu-id="bf775-240">Retrieves a string value that contains the name of the file backing a downloaded entity.</span></span> <span data-ttu-id="bf775-241">Esta marca es válida después de que se completen [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="bf775-241">This flag is valid after [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) has completed.</span></span> <span data-ttu-id="bf775-242">Esta opción solo puede ser consultada por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-242">This option can only be queried by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**opción de INTERNET \_ \_ archivo de archivo de archivos \_ ext**</span><span class="sxs-lookup"><span data-stu-id="bf775-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**INTERNET\_OPTION\_DATAFILE\_EXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-244">96</span><span class="sxs-lookup"><span data-stu-id="bf775-244">96</span></span>
</dt> <dt>



<span data-ttu-id="bf775-245">Establece un valor de cadena que contiene la extensión del archivo que realiza la copia de seguridad de una entidad descargada.</span><span class="sxs-lookup"><span data-stu-id="bf775-245">Sets a string value that contains the extension of the file backing a downloaded entity.</span></span> <span data-ttu-id="bf775-246">Esta marca se debe establecer antes de llamar a [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="bf775-246">This flag should be set before calling [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="bf775-247">Esta opción solo se puede establecer mediante [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-247">This option can only be set by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**opción de INTERNET \_ \_ información del socket de diagnóstico \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**INTERNET\_OPTION\_DIAGNOSTIC\_SOCKET\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-249">67</span><span class="sxs-lookup"><span data-stu-id="bf775-249">67</span></span>
</dt> <dt>



<span data-ttu-id="bf775-250">Recupera una estructura [**de \_ \_ \_ información del socket de diagnóstico de Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) que contiene datos sobre una solicitud HTTP especificada.</span><span class="sxs-lookup"><span data-stu-id="bf775-250">Retrieves an [**INTERNET\_DIAGNOSTIC\_SOCKET\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) structure that contains data about a specified HTTP Request.</span></span> <span data-ttu-id="bf775-251">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="bf775-251">This flag is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

<span data-ttu-id="bf775-252">**Windows 7:** Esta opción ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf775-252">**Windows 7:** This option is no longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**\_descarga de \_ \_ autenticación implícita de opción \_ de Internet**</span><span class="sxs-lookup"><span data-stu-id="bf775-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**INTERNET\_OPTION\_DIGEST\_AUTH\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-254">76</span><span class="sxs-lookup"><span data-stu-id="bf775-254">76</span></span>
</dt> <dt>



<span data-ttu-id="bf775-255">Hace que el sistema cierre la sesión del paquete SSPI de autenticación implícita, y purga todas las credenciales creadas para el proceso.</span><span class="sxs-lookup"><span data-stu-id="bf775-255">Causes the system to log off the Digest authentication SSPI package, purging all of the credentials created for the process.</span></span> <span data-ttu-id="bf775-256">No se requiere ningún búfer para esta opción.</span><span class="sxs-lookup"><span data-stu-id="bf775-256">No buffer is required for this option.</span></span> <span data-ttu-id="bf775-257">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)lo usa.</span><span class="sxs-lookup"><span data-stu-id="bf775-257">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**opción de INTERNET \_ \_ deshabilitar \_ marcado automático**</span><span class="sxs-lookup"><span data-stu-id="bf775-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**INTERNET\_OPTION\_DISABLE\_AUTODIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-259">70</span><span class="sxs-lookup"><span data-stu-id="bf775-259">70</span></span>
</dt> <dt>



<span data-ttu-id="bf775-260">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-260">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**tiempo de espera de la opción de INTERNET \_ \_ desconectado \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**INTERNET\_OPTION\_DISCONNECTED\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-262">49</span><span class="sxs-lookup"><span data-stu-id="bf775-262">49</span></span>
</dt> <dt>



<span data-ttu-id="bf775-263">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-263">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**opción de INTERNET \_ \_ habilitar \_ \_ protocolo http**</span><span class="sxs-lookup"><span data-stu-id="bf775-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**INTERNET\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-265">148</span><span class="sxs-lookup"><span data-stu-id="bf775-265">148</span></span>
</dt> <dt>



<span data-ttu-id="bf775-266">Establece una máscara de máscara DWORD de versiones de HTTP avanzadas aceptables.</span><span class="sxs-lookup"><span data-stu-id="bf775-266">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="bf775-267">Se puede establecer en cualquier tipo de identificador.</span><span class="sxs-lookup"><span data-stu-id="bf775-267">May be set on any handle type.</span></span> <span data-ttu-id="bf775-268">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="bf775-268">Possible values are:</span></span>

-   <span data-ttu-id="bf775-269">\_Marca de protocolo HTTP \_ \_ HTTP2 (0X2).</span><span class="sxs-lookup"><span data-stu-id="bf775-269">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="bf775-270">Compatible con Windows 10, versión 1507 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-270">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="bf775-271">Las versiones heredadas de HTTP (1,1 y anteriores) no se pueden deshabilitar con esta opción.</span><span class="sxs-lookup"><span data-stu-id="bf775-271">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="bf775-272">El valor predeterminado es 0X0.</span><span class="sxs-lookup"><span data-stu-id="bf775-272">The default is 0x0.</span></span> <span data-ttu-id="bf775-273">Compatible con Windows 10, versión 1507 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-273">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**opción de INTERNET \_ Habilitar la lectura de \_ caché de \_ redireccionamiento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**INTERNET\_OPTION\_ENABLE\_REDIRECT\_CACHE\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-275">122</span><span class="sxs-lookup"><span data-stu-id="bf775-275">122</span></span>
</dt> <dt>



<span data-ttu-id="bf775-276">En un identificador de solicitud, establece un valor booleano que controla si las redirecciones se devolverán desde la memoria caché de WinInet para una solicitud determinada.</span><span class="sxs-lookup"><span data-stu-id="bf775-276">On a request handle, sets a Boolean controlling whether redirects will be returned from the WinInet cache for a given request.</span></span> <span data-ttu-id="bf775-277">El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="bf775-277">The default is FALSE.</span></span> <span data-ttu-id="bf775-278">Compatible con Windows 8 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-278">Supported in Windows 8 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**opción de INTERNET \_ \_ codificación \_ adicional**</span><span class="sxs-lookup"><span data-stu-id="bf775-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**INTERNET\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-280">155</span><span class="sxs-lookup"><span data-stu-id="bf775-280">155</span></span>
</dt> <dt>



<span data-ttu-id="bf775-281">Obtiene o establece un valor BOOLEANO que indica si los caracteres no ASCII de la cadena de consulta deben estar codificados por porcentaje.</span><span class="sxs-lookup"><span data-stu-id="bf775-281">Gets/sets a BOOL indicating whether non-ASCII characters in the query string should be percent-encoded.</span></span> <span data-ttu-id="bf775-282">El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="bf775-282">The default is FALSE.</span></span> <span data-ttu-id="bf775-283">Se admite en Windows 8.1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-283">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**opción de INTERNET \_ \_ finalizar \_ sesión del explorador \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**INTERNET\_OPTION\_END\_BROWSER\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-285">42</span><span class="sxs-lookup"><span data-stu-id="bf775-285">42</span></span>
</dt> <dt>



<span data-ttu-id="bf775-286">Vacía las entradas que no están en uso desde la memoria caché de contraseñas de la unidad de disco duro.</span><span class="sxs-lookup"><span data-stu-id="bf775-286">Flushes entries not in use from the password cache on the hard disk drive.</span></span> <span data-ttu-id="bf775-287">También restablece el tiempo de caché utilizado cuando el modo de sincronización es una vez por sesión.</span><span class="sxs-lookup"><span data-stu-id="bf775-287">Also resets the cache time used when the synchronization mode is once-per-session.</span></span> <span data-ttu-id="bf775-288">No se requiere ningún búfer para esta opción.</span><span class="sxs-lookup"><span data-stu-id="bf775-288">No buffer is required for this option.</span></span> <span data-ttu-id="bf775-289">Se usa en [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-289">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**\_máscara de \_ error de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**INTERNET\_OPTION\_ERROR\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-291">62</span><span class="sxs-lookup"><span data-stu-id="bf775-291">62</span></span>
</dt> <dt>



<span data-ttu-id="bf775-292">Establece un valor entero largo sin signo que contiene las máscaras de error que puede controlar la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="bf775-292">Sets an unsigned long integer value that contains the error masks that can be handled by the client application.</span></span> <span data-ttu-id="bf775-293">Puede ser una combinación de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="bf775-293">This can be a combination of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bf775-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>certificado de máscara de error de INTERNET \_ \_ \_ combinado \_ s \_</span><span class="sxs-lookup"><span data-stu-id="bf775-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>INTERNET\_ERROR\_MASK\_COMBINED\_SEC\_CERT</span></span>
</dt> <dd>

<span data-ttu-id="bf775-295">0x2</span><span class="sxs-lookup"><span data-stu-id="bf775-295">0x2</span></span>

<span data-ttu-id="bf775-296">Indica que se van a informar de todos los errores de certificado con el mismo error de devolución, es decir, **\_ \_ \_ \_ errores de certificado por Internet**.</span><span class="sxs-lookup"><span data-stu-id="bf775-296">Indicates that all certificate errors are to be reported using the same error return, namely **ERROR\_INTERNET\_SEC\_CERT\_ERRORS**.</span></span> <span data-ttu-id="bf775-297">Si se establece esta marca, llame a **InternetErrorDlg** tras recibir el error errores de **certificado de \_ Internet \_ s \_ \_** por error, de modo que el usuario pueda responder a un cuadro de diálogo conocido que describa el problema.</span><span class="sxs-lookup"><span data-stu-id="bf775-297">If this flag is set, call **InternetErrorDlg** upon receiving the **ERROR\_INTERNET\_SEC\_CERT\_ERRORS** error, so that the user can respond to a familiar dialog describing the problem.</span></span>

> [!Caution]  
> <span data-ttu-id="bf775-298">Si no se informa al usuario de este error, expone al usuario a posibles ataques de suplantación de identidad.</span><span class="sxs-lookup"><span data-stu-id="bf775-298">Failing to inform the user of this error exposes the user to potential spoofing attacks.</span></span>

 

</dd> <dt>

<span data-ttu-id="bf775-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>carátula de error de INTERNET \_ \_ \_ Insertar \_ CDROM</span><span class="sxs-lookup"><span data-stu-id="bf775-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>INTERNET\_ERROR\_MASK\_INSERT\_CDROM</span></span>
</dt> <dd>

<span data-ttu-id="bf775-300">0x1</span><span class="sxs-lookup"><span data-stu-id="bf775-300">0x1</span></span>

<span data-ttu-id="bf775-301">Indica que la aplicación cliente puede controlar el código de error de **\_ Internet \_ Insert \_ CDROM** .</span><span class="sxs-lookup"><span data-stu-id="bf775-301">Indicates that the client application can handle the **ERROR\_INTERNET\_INSERT\_CDROM** error code.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>error de inicio de sesión de máscara de error de INTERNET \_ \_ \_ \_ \_ Mostrar \_ cuerpo de entidad \_</span><span class="sxs-lookup"><span data-stu-id="bf775-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY</span></span>
</dt> <dd>

<span data-ttu-id="bf775-303">0x8</span><span class="sxs-lookup"><span data-stu-id="bf775-303">0x8</span></span>

<span data-ttu-id="bf775-304">Indica que la aplicación cliente puede controlar el error de inicio de sesión de Internet mostrar el código de error **\_ \_ \_ \_ \_ \_ del cuerpo** de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bf775-304">Indicates that the client application can handle the **ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY** error code.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>la \_ máscara de error de Internet \_ necesita el \_ \_ \_ paquete SSPI de MSN \_</span><span class="sxs-lookup"><span data-stu-id="bf775-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>INTERNET\_ERROR\_MASK\_NEED\_MSN\_SSPI\_PKG</span></span>
</dt> <dd>

<span data-ttu-id="bf775-306">0x4</span><span class="sxs-lookup"><span data-stu-id="bf775-306">0x4</span></span>

<span data-ttu-id="bf775-307">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-307">Not implemented.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="bf775-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**contexto de la opción de INTERNET \_ \_ Enterprise \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**INTERNET\_OPTION\_ENTERPRISE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-309">159</span><span class="sxs-lookup"><span data-stu-id="bf775-309">159</span></span>
</dt> <dt>



<span data-ttu-id="bf775-310">Establece un PWSTR que contiene el identificador de empresa (vea https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) lo que se aplica a la solicitud).</span><span class="sxs-lookup"><span data-stu-id="bf775-310">Sets a PWSTR containing the Enterprise ID (see https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) which applies to the request.</span></span> <span data-ttu-id="bf775-311">Compatible con Windows 10, versión 1507 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-311">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**\_ \_ error extendido de la opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**INTERNET\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-313">24</span><span class="sxs-lookup"><span data-stu-id="bf775-313">24</span></span>
</dt> <dt>



<span data-ttu-id="bf775-314">Recupera un valor entero largo sin signo que contiene un código de error de Winsock asignado al error de los mensajes de error de **\_ Internet \_** devueltos por última vez en este contexto de subproceso.</span><span class="sxs-lookup"><span data-stu-id="bf775-314">Retrieves an unsigned long integer value that contains a Winsock error code mapped to the **ERROR\_INTERNET\_** error messages last returned in this thread context.</span></span> <span data-ttu-id="bf775-315">Esta opción se usa en un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) **nulo** por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-315">This option is used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**\_opción \_ de Internet del \_ tiempo de espera de caché \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**INTERNET\_OPTION\_FROM\_CACHE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-317">63</span><span class="sxs-lookup"><span data-stu-id="bf775-317">63</span></span>
</dt> <dt>



<span data-ttu-id="bf775-318">Establece o recupera el valor entero largo sin signo de A1n que contiene la cantidad de tiempo que el sistema debe esperar una respuesta a una solicitud de red antes de comprobar si hay una copia del recurso en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="bf775-318">Sets or retrieves a1n unsigned long integer value that contains the amount of time the system should wait for a response to a network request before checking the cache for a copy of the resource.</span></span> <span data-ttu-id="bf775-319">Si una solicitud de red tarda más tiempo del especificado y el recurso solicitado está disponible en la memoria caché, el recurso se recupera de la caché.</span><span class="sxs-lookup"><span data-stu-id="bf775-319">If a network request takes longer than the time specified and the requested resource is available in the cache, the resource is retrieved from the cache.</span></span> <span data-ttu-id="bf775-320">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-320">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**\_tipo de \_ identificador de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**INTERNET\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-322">9</span><span class="sxs-lookup"><span data-stu-id="bf775-322">9</span></span>
</dt> <dt>



<span data-ttu-id="bf775-323">Recupera un valor entero largo sin signo que contiene el tipo de los identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) pasados.</span><span class="sxs-lookup"><span data-stu-id="bf775-323">Retrieves an unsigned long integer value that contains the type of the [**HINTERNET**](appendix-a-hinternet-handles.md) handles passed in.</span></span> <span data-ttu-id="bf775-324">Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) en cualquier identificador de [HINTERNET](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="bf775-324">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) on any [HINTERNET](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="bf775-325">Entre los posibles valores devueltos se incluyen los siguientes.</span><span class="sxs-lookup"><span data-stu-id="bf775-325">Possible return values include the following.</span></span>

<dl> <dt>

<span data-ttu-id="bf775-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>tipo de identificador de INTERNET \_ \_ \_ Connect \_ FTP</span><span class="sxs-lookup"><span data-stu-id="bf775-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_FTP</span></span>
</dt> <dd>

<span data-ttu-id="bf775-327">2</span><span class="sxs-lookup"><span data-stu-id="bf775-327">2</span></span>

</dd> <dt>

<span data-ttu-id="bf775-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>tipo de identificador de INTERNET \_ \_ \_ Connect \_ Gopher</span><span class="sxs-lookup"><span data-stu-id="bf775-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_GOPHER</span></span>
</dt> <dd>

<span data-ttu-id="bf775-329">3</span><span class="sxs-lookup"><span data-stu-id="bf775-329">3</span></span>

</dd> <dt>

<span data-ttu-id="bf775-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>tipo de identificador de INTERNET \_ \_ \_ Connect \_ http</span><span class="sxs-lookup"><span data-stu-id="bf775-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="bf775-331">4</span><span class="sxs-lookup"><span data-stu-id="bf775-331">4</span></span>

</dd> <dt>

<span data-ttu-id="bf775-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>\_solicitud de \_ archivo de tipo de identificador de Internet \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf775-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>INTERNET\_HANDLE\_TYPE\_FILE\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="bf775-333">14</span><span class="sxs-lookup"><span data-stu-id="bf775-333">14</span></span>

</dd> <dt>

<span data-ttu-id="bf775-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>tipo de identificador de INTERNET \_ \_ \_ \_ archivo FTP</span><span class="sxs-lookup"><span data-stu-id="bf775-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="bf775-335">7</span><span class="sxs-lookup"><span data-stu-id="bf775-335">7</span></span>

</dd> <dt>

<span data-ttu-id="bf775-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>tipo de identificador de INTERNET \_ \_ \_ \_ archivo FTP \_ HTML</span><span class="sxs-lookup"><span data-stu-id="bf775-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="bf775-337">8</span><span class="sxs-lookup"><span data-stu-id="bf775-337">8</span></span>

</dd> <dt>

<span data-ttu-id="bf775-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>tipo de identificador de INTERNET \_ \_ \_ búsqueda de FTP \_</span><span class="sxs-lookup"><span data-stu-id="bf775-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="bf775-339">5</span><span class="sxs-lookup"><span data-stu-id="bf775-339">5</span></span>

</dd> <dt>

<span data-ttu-id="bf775-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>tipo de identificador de INTERNET \_ \_ búsqueda de \_ \_ \_ HTML</span><span class="sxs-lookup"><span data-stu-id="bf775-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="bf775-341">6</span><span class="sxs-lookup"><span data-stu-id="bf775-341">6</span></span>

</dd> <dt>

<span data-ttu-id="bf775-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>tipo de identificador de INTERNET ( \_ \_ \_ \_ archivo Gopher)</span><span class="sxs-lookup"><span data-stu-id="bf775-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="bf775-343">11</span><span class="sxs-lookup"><span data-stu-id="bf775-343">11</span></span>

</dd> <dt>

<span data-ttu-id="bf775-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>tipo de identificador de INTERNET \_ \_ \_ \_ archivo Gopher \_ HTML</span><span class="sxs-lookup"><span data-stu-id="bf775-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="bf775-345">12</span><span class="sxs-lookup"><span data-stu-id="bf775-345">12</span></span>

</dd> <dt>

<span data-ttu-id="bf775-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>búsqueda de tipo de identificador de INTERNET \_ \_ \_ Gopher \_</span><span class="sxs-lookup"><span data-stu-id="bf775-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="bf775-347">9</span><span class="sxs-lookup"><span data-stu-id="bf775-347">9</span></span>

</dd> <dt>

<span data-ttu-id="bf775-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>tipo de identificador de INTERNET de la \_ \_ búsqueda de \_ \_ \_ HTML Gopher</span><span class="sxs-lookup"><span data-stu-id="bf775-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="bf775-349">10</span><span class="sxs-lookup"><span data-stu-id="bf775-349">10</span></span>

</dd> <dt>

<span data-ttu-id="bf775-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>\_ \_ solicitud HTTP de tipo de identificador de \_ Internet \_</span><span class="sxs-lookup"><span data-stu-id="bf775-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>INTERNET\_HANDLE\_TYPE\_HTTP\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="bf775-351">13</span><span class="sxs-lookup"><span data-stu-id="bf775-351">13</span></span>

</dd> <dt>

<span data-ttu-id="bf775-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>tipo de identificador de INTERNET \_ \_ \_ Internet</span><span class="sxs-lookup"><span data-stu-id="bf775-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>INTERNET\_HANDLE\_TYPE\_INTERNET</span></span>
</dt> <dd>

<span data-ttu-id="bf775-353">1</span><span class="sxs-lookup"><span data-stu-id="bf775-353">1</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="bf775-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**opción de INTERNET \_ \_ HSTS**</span><span class="sxs-lookup"><span data-stu-id="bf775-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**INTERNET\_OPTION\_HSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-355">157</span><span class="sxs-lookup"><span data-stu-id="bf775-355">157</span></span>
</dt> <dt>



<span data-ttu-id="bf775-356">Obtiene o establece un valor BOOLEANO que indica si WinInet debe seguir las directivas de seguridad de transporte estricto HTTP (HSTS) de los servidores.</span><span class="sxs-lookup"><span data-stu-id="bf775-356">Gets/sets a BOOL indicating whether WinInet should follow HTTP Strict Transport Security (HSTS) directives from servers.</span></span> <span data-ttu-id="bf775-357">Si está habilitada, las solicitudes de combinación de https://a los dominios que tienen una directiva de HSTS almacenada en caché por WinInet se redirigirán a las direcciones URL de https://coincidentes.</span><span class="sxs-lookup"><span data-stu-id="bf775-357">If enabled, https:// schemed requests to domains which have an HSTS policy cached by WinInet will be redirected to matching https:// URLs.</span></span> <span data-ttu-id="bf775-358">El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="bf775-358">The default is FALSE.</span></span> <span data-ttu-id="bf775-359">Se admite en Windows 8.1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-359">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**descodificación http de la opción de INTERNET \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**INTERNET\_OPTION\_HTTP\_DECODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-361">65</span><span class="sxs-lookup"><span data-stu-id="bf775-361">65</span></span>
</dt> <dt>



<span data-ttu-id="bf775-362">Permite que WinINet realice la descodificación para los esquemas de codificación gzip y DEFLATE.</span><span class="sxs-lookup"><span data-stu-id="bf775-362">Enables WinINet to perform decoding for the gzip and deflate encoding schemes.</span></span> <span data-ttu-id="bf775-363">Para obtener más información, consulte [**codificación de contenido**](content-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="bf775-363">For more information, see [**Content Encoding**](content-encoding.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**protocolo http de la opción de INTERNET \_ \_ \_ \_ usado**</span><span class="sxs-lookup"><span data-stu-id="bf775-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**INTERNET\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-365">149</span><span class="sxs-lookup"><span data-stu-id="bf775-365">149</span></span>
</dt> <dt>



<span data-ttu-id="bf775-366">Obtiene un valor DWORD que indica qué versión de HTTP avanzada se usó en una solicitud determinada.</span><span class="sxs-lookup"><span data-stu-id="bf775-366">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="bf775-367">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="bf775-367">Possible values are:</span></span>

-   <span data-ttu-id="bf775-368">\_Marca de protocolo HTTP \_ \_ HTTP2 (0X2).</span><span class="sxs-lookup"><span data-stu-id="bf775-368">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="bf775-369">Compatible con Windows 10, versión 1507 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-369">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="bf775-370">0X0 indica HTTP/1.1 o anterior; consulte \_ opción \_ de Internet \_ versión de http si se necesita más precisión sobre la versión heredada.</span><span class="sxs-lookup"><span data-stu-id="bf775-370">0x0 indicates HTTP/1.1 or earlier; see INTERNET\_OPTION\_HTTP\_VERSION if more precision is needed about which legacy version was used.</span></span> <span data-ttu-id="bf775-371">Compatible con Windows 10, versión 1507 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-371">Supported on Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**opción de INTERNET \_ \_ versión de http \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**INTERNET\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-373">59</span><span class="sxs-lookup"><span data-stu-id="bf775-373">59</span></span>
</dt> <dt>



<span data-ttu-id="bf775-374">Establece o recupera una estructura [**de \_ \_ información de versión de http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) que contiene la versión de http admitida.</span><span class="sxs-lookup"><span data-stu-id="bf775-374">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure that contains the supported HTTP version.</span></span> <span data-ttu-id="bf775-375">Debe usarse en un identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="bf775-375">This must be used on a **NULL** handle.</span></span> <span data-ttu-id="bf775-376">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-376">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="bf775-377">En Windows 7, Windows Server 2008 R2 y versiones posteriores, la configuración de Internet Explorer invalida el valor del miembro **dwMinorVersion** de la estructura de [**\_ \_ información de versión http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) .</span><span class="sxs-lookup"><span data-stu-id="bf775-377">On Windows 7, Windows Server 2008 R2, and later, the value of the **dwMinorVersion** member in the [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure is overridden by Internet Explorer settings.</span></span> <span data-ttu-id="bf775-378">**EnableHttp1 \_ 1** es un valor del registro en **HKLM \\ software \\ Microsoft \\ InternetExplorer \\ AdvacnedOptions \\ http \\ GENABLE** controlado por opciones de Internet establecidas en Internet Explorer para el sistema.</span><span class="sxs-lookup"><span data-stu-id="bf775-378">**EnableHttp1\_1** is a registry value under **HKLM\\Software\\Microsoft\\InternetExplorer\\AdvacnedOptions\\HTTP\\GENABLE** controlled by Internet Options set in Internet Explorer for the system.</span></span> <span data-ttu-id="bf775-379">El valor predeterminado de **EnableHttp1 \_ 1** es 1.</span><span class="sxs-lookup"><span data-stu-id="bf775-379">The **EnableHttp1\_1** value defaults to 1.</span></span> <span data-ttu-id="bf775-380">La estructura de **\_ \_ información de la versión http** se omite para cualquier versión http inferior a 1,1 si **EnableHttp1 \_ 1** está establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="bf775-380">The **HTTP\_VERSION\_INFO** structure is ignored for any HTTP version less than 1.1 if **EnableHttp1\_1** is set to 1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**identidad de la opción de INTERNET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**INTERNET\_OPTION\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-382">78</span><span class="sxs-lookup"><span data-stu-id="bf775-382">78</span></span>
</dt> <dt>



<span data-ttu-id="bf775-383">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-383">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**\_Estado de \_ inactividad de la opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**INTERNET\_OPTION\_IDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-385">51</span><span class="sxs-lookup"><span data-stu-id="bf775-385">51</span></span>
</dt> <dt>



<span data-ttu-id="bf775-386">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-386">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**Opciones de INTERNET \_ \_ IDN**</span><span class="sxs-lookup"><span data-stu-id="bf775-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**INTERNET\_OPTION\_IDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-388">102</span><span class="sxs-lookup"><span data-stu-id="bf775-388">102</span></span>
</dt> <dt>



<span data-ttu-id="bf775-389">De forma predeterminada, la parte de host o de autoridad de la dirección URL se codifica según la especificación de IDN para conexiones directas y proxy.</span><span class="sxs-lookup"><span data-stu-id="bf775-389">By default, the host or authority portion of the URL is encoded according to the IDN specification for both direct and proxy connections.</span></span> <span data-ttu-id="bf775-390">Esta opción se puede usar en la solicitud o en el identificador de conexión para habilitar o deshabilitar IDN.</span><span class="sxs-lookup"><span data-stu-id="bf775-390">This option can be used on the request, or connection handle to enable or disable IDN.</span></span> <span data-ttu-id="bf775-391">Cuando se deshabilita IDN, WinINet utiliza la página de códigos del sistema para codificar la parte de host o de autoridad de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="bf775-391">When IDN is disabled, WinINet uses the system codepage to encode the host or authority portion of the URL.</span></span> <span data-ttu-id="bf775-392">Para deshabilitar la conversión de hosts IDN, establezca el parámetro *lpBuffer* en la llamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) en cero.</span><span class="sxs-lookup"><span data-stu-id="bf775-392">To disable IDN host conversion, set the *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to zero.</span></span> <span data-ttu-id="bf775-393">Para habilitar la conversión IDN solo en la conexión directa, especifique **Internet \_ Flag \_ IDN \_ Direct** en el parámetro *lpBuffer* en la llamada a **InternetSetOption**.</span><span class="sxs-lookup"><span data-stu-id="bf775-393">To enable IDN conversion on only the direct connection, specify **INTERNET\_FLAG\_IDN\_DIRECT** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span> <span data-ttu-id="bf775-394">Para habilitar la conversión de IDN solo en la conexión del proxy, especifique el **\_ \_ \_ proxy IDN de marca de Internet** en el parámetro *lpBuffer* en la llamada a **InternetSetOption**.</span><span class="sxs-lookup"><span data-stu-id="bf775-394">To enable IDN conversion on only the proxy connection, specify **INTERNET\_FLAG\_IDN\_PROXY** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span>

<span data-ttu-id="bf775-395">**Windows XP con SP2 y Windows Server 2003 con SP1:** Esta marca no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf775-395">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="bf775-396">**Versión:** Requiere Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="bf775-396">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**opción de INTERNET \_ \_ omitir \_ sin conexión**</span><span class="sxs-lookup"><span data-stu-id="bf775-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**INTERNET\_OPTION\_IGNORE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-398">77</span><span class="sxs-lookup"><span data-stu-id="bf775-398">77</span></span>
</dt> <dt>



<span data-ttu-id="bf775-399">Establece o recupera si se debe omitir el indicador global sin conexión para el identificador de solicitud especificado.</span><span class="sxs-lookup"><span data-stu-id="bf775-399">Sets or retrieves whether the global offline flag should be ignored for the specified request handle.</span></span> <span data-ttu-id="bf775-400">No se requiere ningún búfer para esta opción.</span><span class="sxs-lookup"><span data-stu-id="bf775-400">No buffer is required for this option.</span></span> <span data-ttu-id="bf775-401">Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con un identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf775-401">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with a request handle.</span></span> <span data-ttu-id="bf775-402">Esta opción solo es válida en Internet Explorer 5 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-402">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**opción de INTERNET \_ \_ mantener \_ conexión**</span><span class="sxs-lookup"><span data-stu-id="bf775-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**INTERNET\_OPTION\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-404">22</span><span class="sxs-lookup"><span data-stu-id="bf775-404">22</span></span>
</dt> <dt>



<span data-ttu-id="bf775-405">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-405">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**\_tiempo de \_ espera de escucha de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**INTERNET\_OPTION\_LISTEN\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-407">11</span><span class="sxs-lookup"><span data-stu-id="bf775-407">11</span></span>
</dt> <dt>



<span data-ttu-id="bf775-408">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-408">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**Opción de INTERNET \_ \_ Max \_ Conex \_ . \_ por \_ servidor 1 0 \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-410">74</span><span class="sxs-lookup"><span data-stu-id="bf775-410">74</span></span>
</dt> <dt>



<span data-ttu-id="bf775-411">Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por servidor HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="bf775-411">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="bf775-412">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-412">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="bf775-413">Esta opción solo es válida en Internet Explorer 5 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-413">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**opción de INTERNET \_ \_ Max \_ Conex. \_ por \_ proxy**</span><span class="sxs-lookup"><span data-stu-id="bf775-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-415">103</span><span class="sxs-lookup"><span data-stu-id="bf775-415">103</span></span>
</dt> <dt>



<span data-ttu-id="bf775-416">Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por cada proxy de CERN.</span><span class="sxs-lookup"><span data-stu-id="bf775-416">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per CERN proxy.</span></span> <span data-ttu-id="bf775-417">Cuando se establece o recupera esta opción, el parámetro *hInternet* debe establecerse en un valor de identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="bf775-417">When this option is set or retrieved, the *hInternet* parameter must set to a **null** handle value.</span></span> <span data-ttu-id="bf775-418">Un valor de identificador **null** indica que la opción se debe establecer o consultar para el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="bf775-418">A **null** handle value indicates that the option should be set or queried for the current process.</span></span> <span data-ttu-id="bf775-419">Cuando se llama a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con esta opción, todos los objetos proxy existentes recibirán el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="bf775-419">When calling [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with this option, all existing proxy objects will receive the new value.</span></span> <span data-ttu-id="bf775-420">Este valor se limita a un intervalo de 2 a 128, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="bf775-420">This value is limited to a range of 2 to 128, inclusive.</span></span>

<span data-ttu-id="bf775-421">**Versión:** Requiere Internet Explorer 8,0.</span><span class="sxs-lookup"><span data-stu-id="bf775-421">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**opción de INTERNET \_ \_ Max \_ Conex. \_ por \_ servidor**</span><span class="sxs-lookup"><span data-stu-id="bf775-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-423">73</span><span class="sxs-lookup"><span data-stu-id="bf775-423">73</span></span>
</dt> <dt>



<span data-ttu-id="bf775-424">Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por servidor.</span><span class="sxs-lookup"><span data-stu-id="bf775-424">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="bf775-425">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-425">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="bf775-426">Esta opción solo es válida en Internet Explorer 5 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-426">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**\_ \_ modo sin conexión de opciones de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**INTERNET\_OPTION\_OFFLINE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-428">26</span><span class="sxs-lookup"><span data-stu-id="bf775-428">26</span></span>
</dt> <dt>



<span data-ttu-id="bf775-429">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-429">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**\_ \_ semántica sin conexión de opciones de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**INTERNET\_OPTION\_OFFLINE\_SEMANTICS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-431">52</span><span class="sxs-lookup"><span data-stu-id="bf775-431">52</span></span>
</dt> <dt>



<span data-ttu-id="bf775-432">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-432">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**\_opción \_ de Internet participar en una \_ \_ \_ firma débil**</span><span class="sxs-lookup"><span data-stu-id="bf775-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**INTERNET\_OPTION\_OPT\_IN\_WEAK\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-434">176</span><span class="sxs-lookup"><span data-stu-id="bf775-434">176</span></span>
</dt> <dt>



<span data-ttu-id="bf775-435">Optar por la firma débil (por ejemplo, SHA-1) para que se trate como no segura.</span><span class="sxs-lookup"><span data-stu-id="bf775-435">Opt-in for weak signatures (e.g. SHA-1) to be treated as insecure.</span></span> <span data-ttu-id="bf775-436">Esto indicará a WinInet que llame a [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) mediante el parámetro **de la \_ \_ \_ \_ \_ firma débil de la cadena de certificados** .</span><span class="sxs-lookup"><span data-stu-id="bf775-436">This will instruct WinInet to call [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) using the **CERT\_CHAIN\_OPT\_IN\_WEAK\_SIGNATURE** parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**\_ \_ identificador primario de la opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**INTERNET\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-438">21</span><span class="sxs-lookup"><span data-stu-id="bf775-438">21</span></span>
</dt> <dt>



<span data-ttu-id="bf775-439">Recupera el identificador primario de este identificador.</span><span class="sxs-lookup"><span data-stu-id="bf775-439">Retrieves the parent handle to this handle.</span></span> <span data-ttu-id="bf775-440">Esta opción puede usarse en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) de [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-440">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**contraseña de la opción de INTERNET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**INTERNET\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-442">29</span><span class="sxs-lookup"><span data-stu-id="bf775-442">29</span></span>
</dt> <dt>



<span data-ttu-id="bf775-443">Establece o recupera un valor de cadena que contiene la contraseña asociada a un identificador devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="bf775-443">Sets or retrieves a string value that contains the password associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="bf775-444">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-444">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**opción de INTERNET \_ \_ por \_ opción de conexión \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-446">75</span><span class="sxs-lookup"><span data-stu-id="bf775-446">75</span></span>
</dt> <dt>



<span data-ttu-id="bf775-447">Establece o recupera una estructura [**de \_ \_ \_ \_ lista**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) de opciones de Internet por conexión que especifica una lista de opciones para una conexión determinada.</span><span class="sxs-lookup"><span data-stu-id="bf775-447">Sets or retrieves an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure that specifies a list of options for a particular connection.</span></span> <span data-ttu-id="bf775-448">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-448">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="bf775-449">Esta opción solo es válida en Internet Explorer 5 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf775-449">This option is only valid in Internet Explorer 5 and later.</span></span>

> [!Note]  
> <span data-ttu-id="bf775-450">**Internet \_ de La \_ opción \_ por \_ conexión** hace que la configuración se cambie en todo el sistema cuando se usa un identificador **null** en la llamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-450">**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION** causes the settings to be changed on a system-wide basis when a **NULL** handle is used in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="bf775-451">Para actualizar la configuración de proxy global, debe llamar a **InternetSetOption** con la marca de opción de **\_ \_ actualización de opciones de Internet** .</span><span class="sxs-lookup"><span data-stu-id="bf775-451">To refresh the global proxy settings, you must call **InternetSetOption** with the **INTERNET\_OPTION\_REFRESH** option flag.</span></span>

 

> [!Note]  
> <span data-ttu-id="bf775-452">Para cambiar la información de proxy para todo el proceso sin que ello afecte a la configuración global de Internet Explorer 5 y versiones posteriores, use esta opción en el identificador devuelto por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="bf775-452">To change proxy information for the entire process without affecting the global settings in Internet Explorer 5 and later, use this option on the handle that is returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="bf775-453">En el siguiente ejemplo de código se cambia el proxy para todo el proceso, aunque el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) esté cerrado y no se use en ninguna solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf775-453">The following code example changes the proxy for the whole process even though the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is closed and is not used by any requests.</span></span>

 

<span data-ttu-id="bf775-454">Para obtener más información y ejemplos de código, consulte el [artículo de KB 226473](https://support.microsoft.com/kb/226473).</span><span class="sxs-lookup"><span data-stu-id="bf775-454">For more information and code examples, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**\_Directiva de opciones de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**INTERNET\_OPTION\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-456">48</span><span class="sxs-lookup"><span data-stu-id="bf775-456">48</span></span>
</dt> <dt>



<span data-ttu-id="bf775-457">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-457">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**\_proxy de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**INTERNET\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-459">38</span><span class="sxs-lookup"><span data-stu-id="bf775-459">38</span></span>
</dt> <dt>



<span data-ttu-id="bf775-460">Establece o recupera una estructura [**de \_ \_ información de proxy de Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) que contiene los datos de proxy para un identificador de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) existente cuando el identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) no es **null**.</span><span class="sxs-lookup"><span data-stu-id="bf775-460">Sets or retrieves an [**INTERNET\_PROXY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) structure that contains the proxy data for an existing [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) handle when the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is not **NULL**.</span></span> <span data-ttu-id="bf775-461">Si el identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) es **null**, la función establece o consulta los datos de proxy globales.</span><span class="sxs-lookup"><span data-stu-id="bf775-461">If the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is **NULL**, the function sets or queries the global proxy data.</span></span> <span data-ttu-id="bf775-462">Esta opción se puede utilizar en el identificador devuelto por **InternetOpen**.</span><span class="sxs-lookup"><span data-stu-id="bf775-462">This option can be used on the handle returned by **InternetOpen**.</span></span> <span data-ttu-id="bf775-463">Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-463">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

> [!Note]  
> <span data-ttu-id="bf775-464">Se recomienda usar la opción \_ \_ de Internet por cada \_ \_ opción de conexión en lugar del \_ proxy de opción de Internet \_ .</span><span class="sxs-lookup"><span data-stu-id="bf775-464">It is recommended that INTERNET\_OPTION\_PER\_CONNECTION\_OPTION be used instead of INTERNET\_OPTION\_PROXY.</span></span> <span data-ttu-id="bf775-465">Para obtener más información, consulte el [artículo 226473 de Knowledge Base](https://support.microsoft.com/kb/226473).</span><span class="sxs-lookup"><span data-stu-id="bf775-465">For more information, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**\_contraseña de \_ proxy de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**INTERNET\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-467">44</span><span class="sxs-lookup"><span data-stu-id="bf775-467">44</span></span>
</dt> <dt>



<span data-ttu-id="bf775-468">Establece o recupera un valor de cadena que contiene la contraseña utilizada para tener acceso al proxy.</span><span class="sxs-lookup"><span data-stu-id="bf775-468">Sets or retrieves a string value that contains the password used to access the proxy.</span></span> <span data-ttu-id="bf775-469">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-469">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="bf775-470">Esta opción se puede establecer en el identificador devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="bf775-470">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**configuración de proxy de opción de INTERNET \_ \_ \_ \_ cambiada**</span><span class="sxs-lookup"><span data-stu-id="bf775-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**INTERNET\_OPTION\_PROXY\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-472">95</span><span class="sxs-lookup"><span data-stu-id="bf775-472">95</span></span> 
</dt> <dt>



<span data-ttu-id="bf775-473">Alerta a la instancia actual de WinInet de que la configuración de proxy ha cambiado y que debe actualizar con la nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="bf775-473">Alerts the current WinInet instance that proxy settings have changed and that they must update with the new settings.</span></span> <span data-ttu-id="bf775-474">Para avisar de todas las instancias de WinInet disponibles, establezca el parámetro *buffer* de [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) en **null** y *BufferLength* en 0 al pasar esta opción.</span><span class="sxs-lookup"><span data-stu-id="bf775-474">To alert all available WinInet instances, set the *Buffer* parameter of [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to **NULL** and *BufferLength* to 0 when passing this option.</span></span> <span data-ttu-id="bf775-475">Esta opción se puede establecer en el identificador devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="bf775-475">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**\_nombre de \_ usuario de proxy de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**INTERNET\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-477">43</span><span class="sxs-lookup"><span data-stu-id="bf775-477">43</span></span>
</dt> <dt>



<span data-ttu-id="bf775-478">Establece o recupera un valor de cadena que contiene el nombre de usuario utilizado para tener acceso al proxy.</span><span class="sxs-lookup"><span data-stu-id="bf775-478">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span> <span data-ttu-id="bf775-479">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-479">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="bf775-480">Esta opción se puede establecer en el identificador devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="bf775-480">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**\_tamaño de \_ búfer de lectura de opción de Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**INTERNET\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-482">12</span><span class="sxs-lookup"><span data-stu-id="bf775-482">12</span></span>
</dt> <dt>



<span data-ttu-id="bf775-483">Establece o recupera un valor entero largo sin signo que contiene el tamaño del búfer de lectura.</span><span class="sxs-lookup"><span data-stu-id="bf775-483">Sets or retrieves an unsigned long integer value that contains the size of the read buffer.</span></span> <span data-ttu-id="bf775-484">Esta opción se puede usar en los identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) devueltos por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)y [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (solo sesión FTP).</span><span class="sxs-lookup"><span data-stu-id="bf775-484">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="bf775-485">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)usan esta opción.</span><span class="sxs-lookup"><span data-stu-id="bf775-485">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**rendimiento de la opción de INTERNET \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**INTERNET\_OPTION\_RECEIVE\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-487">57</span><span class="sxs-lookup"><span data-stu-id="bf775-487">57</span></span>
</dt> <dt>



<span data-ttu-id="bf775-488">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-488">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**\_tiempo de \_ espera de recepción de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**INTERNET\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-490">6</span><span class="sxs-lookup"><span data-stu-id="bf775-490">6</span></span>
</dt> <dt>



<span data-ttu-id="bf775-491">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para recibir una respuesta a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf775-491">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request.</span></span> <span data-ttu-id="bf775-492">Si la respuesta tarda más que este valor de tiempo de espera, se cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf775-492">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="bf775-493">Esta opción se puede utilizar en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluido un identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="bf775-493">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="bf775-494">Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-494">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="bf775-495">Esta opción no está pensada para representar un tiempo de espera muy específico y inmediato.</span><span class="sxs-lookup"><span data-stu-id="bf775-495">This option is not intended to represent a fine-grained, immediate timeout.</span></span> <span data-ttu-id="bf775-496">Puede esperar que el tiempo de espera se produzca hasta seis segundos después del valor de tiempo de espera establecido.</span><span class="sxs-lookup"><span data-stu-id="bf775-496">You can expect the timeout to occur up to six seconds after the set timeout value.</span></span>

<span data-ttu-id="bf775-497">Cuando se utiliza en referencia a una transacción FTP, esta opción hace referencia al canal de control.</span><span class="sxs-lookup"><span data-stu-id="bf775-497">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**actualización de la opción de INTERNET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**INTERNET\_OPTION\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-499">37</span><span class="sxs-lookup"><span data-stu-id="bf775-499">37</span></span>
</dt> <dt>



<span data-ttu-id="bf775-500">Hace que los datos de proxy se relean desde el registro para un identificador.</span><span class="sxs-lookup"><span data-stu-id="bf775-500">Causes the proxy data to be reread from the registry for a handle.</span></span> <span data-ttu-id="bf775-501">No se requiere ningún búfer.</span><span class="sxs-lookup"><span data-stu-id="bf775-501">No buffer is required.</span></span> <span data-ttu-id="bf775-502">Esta opción se puede usar en el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) devuelto por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="bf775-502">This option can be used on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="bf775-503">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)lo usa.</span><span class="sxs-lookup"><span data-stu-id="bf775-503">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**opción de INTERNET \_ \_ quitar \_ identidad**</span><span class="sxs-lookup"><span data-stu-id="bf775-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**INTERNET\_OPTION\_REMOVE\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-505">79</span><span class="sxs-lookup"><span data-stu-id="bf775-505">79</span></span>
</dt> <dt>



<span data-ttu-id="bf775-506">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-506">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**\_marcas de \_ solicitud de opciones de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**INTERNET\_OPTION\_REQUEST\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-508">23</span><span class="sxs-lookup"><span data-stu-id="bf775-508">23</span></span>
</dt> <dt>



<span data-ttu-id="bf775-509">Recupera un valor entero largo sin signo que contiene las marcas de estado especiales que indican el estado de la descarga en curso.</span><span class="sxs-lookup"><span data-stu-id="bf775-509">Retrieves an unsigned long integer value that contains the special status flags that indicate the status of the download in progress.</span></span> <span data-ttu-id="bf775-510">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-510">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="bf775-511">La opción de marcas de solicitud de opciones de Internet puede ser uno de los siguientes valores: [ \_ \_ \_ ](/windows)</span><span class="sxs-lookup"><span data-stu-id="bf775-511">The [INTERNET\_OPTION\_REQUEST\_FLAGS](/windows) option can be one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bf775-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET \_ REQFLAG \_ Async</span><span class="sxs-lookup"><span data-stu-id="bf775-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET\_REQFLAG\_ASYNC</span></span>
</dt> <dd>

<span data-ttu-id="bf775-513">0x00000002</span><span class="sxs-lookup"><span data-stu-id="bf775-513">0x00000002</span></span>

<span data-ttu-id="bf775-514">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-514">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>escritura de caché de INTERNET \_ REQFLAG \_ \_ \_ deshabilitada</span><span class="sxs-lookup"><span data-stu-id="bf775-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>INTERNET\_REQFLAG\_CACHE\_WRITE\_DISABLED</span></span>
</dt> <dd>

<span data-ttu-id="bf775-516">0x00000040</span><span class="sxs-lookup"><span data-stu-id="bf775-516">0x00000040</span></span>

<span data-ttu-id="bf775-517">No se puede almacenar en caché la solicitud de Internet (por ejemplo, una solicitud HTTPS).</span><span class="sxs-lookup"><span data-stu-id="bf775-517">Internet request cannot be cached (an HTTPS request, for example).</span></span>

</dd> <dt>

<span data-ttu-id="bf775-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET \_ REQFLAG \_ de la \_ caché</span><span class="sxs-lookup"><span data-stu-id="bf775-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET\_REQFLAG\_FROM\_CACHE</span></span>
</dt> <dd>

<span data-ttu-id="bf775-519">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bf775-519">0x00000001</span></span>

<span data-ttu-id="bf775-520">La respuesta procedía de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="bf775-520">Response came from the cache.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>tiempo de espera de INTERNET \_ REQFLAG \_ net \_</span><span class="sxs-lookup"><span data-stu-id="bf775-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>INTERNET\_REQFLAG\_NET\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="bf775-522">0x00000080</span><span class="sxs-lookup"><span data-stu-id="bf775-522">0x00000080</span></span>

<span data-ttu-id="bf775-523">Se agotó el tiempo de espera de la solicitud de Internet.</span><span class="sxs-lookup"><span data-stu-id="bf775-523">Internet request timed out.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>REQFLAG de INTERNET \_ \_ sin \_ encabezados</span><span class="sxs-lookup"><span data-stu-id="bf775-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>INTERNET\_REQFLAG\_NO\_HEADERS</span></span>
</dt> <dd>

<span data-ttu-id="bf775-525">0x00000008</span><span class="sxs-lookup"><span data-stu-id="bf775-525">0x00000008</span></span>

<span data-ttu-id="bf775-526">La respuesta original no contenía encabezados.</span><span class="sxs-lookup"><span data-stu-id="bf775-526">Original response contained no headers.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET \_ REQFLAG \_ passive</span><span class="sxs-lookup"><span data-stu-id="bf775-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET\_REQFLAG\_PASSIVE</span></span>
</dt> <dd>

<span data-ttu-id="bf775-528">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf775-528">0x00000010</span></span>

<span data-ttu-id="bf775-529">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-529">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>REQFLAG de INTERNET \_ \_ a través de \_ proxy</span><span class="sxs-lookup"><span data-stu-id="bf775-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>INTERNET\_REQFLAG\_VIA\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="bf775-531">0x00000004</span><span class="sxs-lookup"><span data-stu-id="bf775-531">0x00000004</span></span>

<span data-ttu-id="bf775-532">La solicitud se realizó a través de un proxy.</span><span class="sxs-lookup"><span data-stu-id="bf775-532">Request was made through a proxy.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="bf775-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**\_prioridad de \_ solicitud de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**INTERNET\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-534">58</span><span class="sxs-lookup"><span data-stu-id="bf775-534">58</span></span>
</dt> <dt>



<span data-ttu-id="bf775-535">Establece o recupera un valor entero largo sin signo que contiene la prioridad de las solicitudes que compiten por una conexión en un identificador HTTP.</span><span class="sxs-lookup"><span data-stu-id="bf775-535">Sets or retrieves an unsigned long integer value that contains the priority of requests that compete for a connection on an HTTP handle.</span></span> <span data-ttu-id="bf775-536">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-536">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**\_ \_ sesión URLCACHE de restablecimiento de opción de \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**INTERNET\_OPTION\_RESET\_URLCACHE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-538">60</span><span class="sxs-lookup"><span data-stu-id="bf775-538">60</span></span>
</dt> <dt>



<span data-ttu-id="bf775-539">Inicia una nueva sesión de caché para el proceso.</span><span class="sxs-lookup"><span data-stu-id="bf775-539">Starts a new cache session for the process.</span></span> <span data-ttu-id="bf775-540">No se requiere ningún búfer.</span><span class="sxs-lookup"><span data-stu-id="bf775-540">No buffer is required.</span></span> <span data-ttu-id="bf775-541">Se usa en [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-541">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="bf775-542">Esta opción solo se reserva para uso interno.</span><span class="sxs-lookup"><span data-stu-id="bf775-542">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**\_clave de \_ \_ caché secundaria de opción \_ de Internet**</span><span class="sxs-lookup"><span data-stu-id="bf775-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**INTERNET\_OPTION\_SECONDARY\_CACHE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-544">53</span><span class="sxs-lookup"><span data-stu-id="bf775-544">53</span></span>
</dt> <dt>



<span data-ttu-id="bf775-545">Establece o recupera un valor de cadena que contiene la clave de caché secundaria.</span><span class="sxs-lookup"><span data-stu-id="bf775-545">Sets or retrieves a string value that contains the secondary cache key.</span></span> <span data-ttu-id="bf775-546">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-546">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="bf775-547">Esta opción solo se reserva para uso interno.</span><span class="sxs-lookup"><span data-stu-id="bf775-547">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**certificado de seguridad de la opción de INTERNET \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-549">35</span><span class="sxs-lookup"><span data-stu-id="bf775-549">35</span></span>
</dt> <dt>



<span data-ttu-id="bf775-550">Recupera el certificado de un servidor SSL/PCT (tecnología de comunicaciones privada Capa de sockets seguros) en una cadena con formato.</span><span class="sxs-lookup"><span data-stu-id="bf775-550">Retrieves the certificate for an SSL/PCT (Secure Sockets Layer/Private Communications Technology) server into a formatted string.</span></span> <span data-ttu-id="bf775-551">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-551">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**\_struct de \_ certificado de seguridad de opción de Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-553">32</span><span class="sxs-lookup"><span data-stu-id="bf775-553">32</span></span>
</dt> <dt>



<span data-ttu-id="bf775-554">Recupera el certificado para un servidor SSL/PCT en la estructura de \_ información de certificado de Internet \_ .</span><span class="sxs-lookup"><span data-stu-id="bf775-554">Retrieves the certificate for an SSL/PCT server into the INTERNET\_CERTIFICATE\_INFO structure.</span></span> <span data-ttu-id="bf775-555">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-555">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**\_marcas de \_ seguridad de opciones de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**INTERNET\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-557">31</span><span class="sxs-lookup"><span data-stu-id="bf775-557">31</span></span>
</dt> <dt>



<span data-ttu-id="bf775-558">Recupera un valor entero largo sin signo que contiene las marcas de seguridad para un identificador.</span><span class="sxs-lookup"><span data-stu-id="bf775-558">Retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="bf775-559">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)usa esta opción.</span><span class="sxs-lookup"><span data-stu-id="bf775-559">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="bf775-560">Puede ser una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bf775-560">It can be a combination of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bf775-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>Marca de seguridad \_ \_ 128 bits</span><span class="sxs-lookup"><span data-stu-id="bf775-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>SECURITY\_FLAG\_128BIT</span></span>
</dt> <dd>

<span data-ttu-id="bf775-562">0x20000000</span><span class="sxs-lookup"><span data-stu-id="bf775-562">0x20000000</span></span>

<span data-ttu-id="bf775-563">Es idéntico a la intensidad de la marca de seguridad de valor preferido. [ \_ \_ \_ ](/windows)</span><span class="sxs-lookup"><span data-stu-id="bf775-563">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_STRONG](/windows).</span></span> <span data-ttu-id="bf775-564">Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-564">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="bf775-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>Marca de seguridad \_ \_ 40BIT</span><span class="sxs-lookup"><span data-stu-id="bf775-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>SECURITY\_FLAG\_40BIT</span></span>
</dt> <dd>

<span data-ttu-id="bf775-566">0x10000000</span><span class="sxs-lookup"><span data-stu-id="bf775-566">0x10000000</span></span>

<span data-ttu-id="bf775-567">Es idéntico a la intensidad de la marca de seguridad del valor preferido. [ \_ \_ \_ ](/windows)</span><span class="sxs-lookup"><span data-stu-id="bf775-567">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="bf775-568">Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-568">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="bf775-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>Marca de seguridad \_ \_ 56BIT</span><span class="sxs-lookup"><span data-stu-id="bf775-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>SECURITY\_FLAG\_56BIT</span></span>
</dt> <dd>

<span data-ttu-id="bf775-570">0x40000000</span><span class="sxs-lookup"><span data-stu-id="bf775-570">0x40000000</span></span>

<span data-ttu-id="bf775-571">Idéntico al [ \_ \_ \_ medio](/windows)de la marca de seguridad del valor preferido.</span><span class="sxs-lookup"><span data-stu-id="bf775-571">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_MEDIUM](/windows).</span></span> <span data-ttu-id="bf775-572">Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-572">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="bf775-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>\_Fortezza de marca de seguridad \_</span><span class="sxs-lookup"><span data-stu-id="bf775-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>SECURITY\_FLAG\_FORTEZZA</span></span>
</dt> <dd>

<span data-ttu-id="bf775-574">0x08000000</span><span class="sxs-lookup"><span data-stu-id="bf775-574">0x08000000</span></span>

<span data-ttu-id="bf775-575">Indica que se ha utilizado Fortezza para proporcionar confidencialidad, autenticación o integridad para la conexión especificada.</span><span class="sxs-lookup"><span data-stu-id="bf775-575">Indicates Fortezza has been used to provide secrecy, authentication, and/or integrity for the specified connection.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>Marca de seguridad \_ \_ IETFSSL4</span><span class="sxs-lookup"><span data-stu-id="bf775-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>SECURITY\_FLAG\_IETFSSL4</span></span>
</dt> <dd>

<span data-ttu-id="bf775-577">0x00000020</span><span class="sxs-lookup"><span data-stu-id="bf775-577">0x00000020</span></span>

<span data-ttu-id="bf775-578">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-578">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>marca de seguridad \_ \_ omitir \_ CN de certificado \_ \_ no válido</span><span class="sxs-lookup"><span data-stu-id="bf775-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="bf775-580">0x00001000</span><span class="sxs-lookup"><span data-stu-id="bf775-580">0x00001000</span></span>

<span data-ttu-id="bf775-581">Omite el mensaje de error Error de [ \_ CN de certificado de Internet \_ s \_ \_ \_ no válido](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="bf775-581">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>marca de seguridad \_ \_ omitir \_ fecha de certificado \_ \_ no válida</span><span class="sxs-lookup"><span data-stu-id="bf775-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="bf775-583">0x00002000</span><span class="sxs-lookup"><span data-stu-id="bf775-583">0x00002000</span></span>

<span data-ttu-id="bf775-584">Omite el mensaje de error de la [fecha del certificado de Internet de error \_ \_ \_ \_ \_ no válido](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="bf775-584">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>\_marca \_ de seguridad omitir \_ redirección \_ a \_ http</span><span class="sxs-lookup"><span data-stu-id="bf775-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="bf775-586">0x00008000</span><span class="sxs-lookup"><span data-stu-id="bf775-586">0x00008000</span></span>

<span data-ttu-id="bf775-587">Omite el [error de \_ Internet \_ https \_ a \_ http \_ en el mensaje de error de \_ redir](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="bf775-587">Ignores the [ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>\_marca \_ de seguridad omitir \_ redirección \_ a \_ https</span><span class="sxs-lookup"><span data-stu-id="bf775-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS</span></span>
</dt> <dd>

<span data-ttu-id="bf775-589">0x00004000</span><span class="sxs-lookup"><span data-stu-id="bf775-589">0x00004000</span></span>

<span data-ttu-id="bf775-590">Omite el [error de \_ Internet \_ http \_ a \_ https \_ en el mensaje de error de \_ redir](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="bf775-590">Ignores the [ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>marca de seguridad \_ \_ omitir \_ revocación</span><span class="sxs-lookup"><span data-stu-id="bf775-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>SECURITY\_FLAG\_IGNORE\_REVOCATION</span></span>
</dt> <dd>

<span data-ttu-id="bf775-592">0x00000080</span><span class="sxs-lookup"><span data-stu-id="bf775-592">0x00000080</span></span>

<span data-ttu-id="bf775-593">Omite los problemas de revocación de certificados.</span><span class="sxs-lookup"><span data-stu-id="bf775-593">Ignores certificate revocation problems.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>marca de seguridad \_ \_ omitir \_ \_ CA desconocida</span><span class="sxs-lookup"><span data-stu-id="bf775-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span>
</dt> <dd>

<span data-ttu-id="bf775-595">0x00000100</span><span class="sxs-lookup"><span data-stu-id="bf775-595">0x00000100</span></span>

<span data-ttu-id="bf775-596">Omite problemas de entidad de certificación desconocidos.</span><span class="sxs-lookup"><span data-stu-id="bf775-596">Ignores unknown certificate authority problems.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>la \_ marca de seguridad \_ omite la \_ \_ firma débil</span><span class="sxs-lookup"><span data-stu-id="bf775-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span>
</dt> <dd>

<span data-ttu-id="bf775-598">0x00010000</span><span class="sxs-lookup"><span data-stu-id="bf775-598">0x00010000</span></span>

<span data-ttu-id="bf775-599">Omite problemas de firma de certificado débil.</span><span class="sxs-lookup"><span data-stu-id="bf775-599">Ignores weak certificate signature problems.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>la \_ marca de seguridad \_ omite el \_ \_ uso incorrecto</span><span class="sxs-lookup"><span data-stu-id="bf775-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_WRONG\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="bf775-601">0x00000200</span><span class="sxs-lookup"><span data-stu-id="bf775-601">0x00000200</span></span>

<span data-ttu-id="bf775-602">Omite problemas de uso incorrectos.</span><span class="sxs-lookup"><span data-stu-id="bf775-602">Ignores incorrect usage problems.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>marca de seguridad \_ \_ NORMALBITNESS</span><span class="sxs-lookup"><span data-stu-id="bf775-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>SECURITY\_FLAG\_NORMALBITNESS</span></span>
</dt> <dd>

<span data-ttu-id="bf775-604">0x10000000</span><span class="sxs-lookup"><span data-stu-id="bf775-604">0x10000000</span></span>

<span data-ttu-id="bf775-605">Es idéntico a la [intensidad de la marca de seguridad Value \_ \_ \_ débil](/windows).</span><span class="sxs-lookup"><span data-stu-id="bf775-605">Identical to the value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="bf775-606">Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-606">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="bf775-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>marca de seguridad \_ \_ PCT</span><span class="sxs-lookup"><span data-stu-id="bf775-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>SECURITY\_FLAG\_PCT</span></span>
</dt> <dd>

<span data-ttu-id="bf775-608">0x00000008</span><span class="sxs-lookup"><span data-stu-id="bf775-608">0x00000008</span></span>

<span data-ttu-id="bf775-609">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-609">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>Marca de seguridad \_ \_ PCT4</span><span class="sxs-lookup"><span data-stu-id="bf775-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>SECURITY\_FLAG\_PCT4</span></span>
</dt> <dd>

<span data-ttu-id="bf775-611">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf775-611">0x00000010</span></span>

<span data-ttu-id="bf775-612">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-612">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>marca de seguridad \_ \_ segura</span><span class="sxs-lookup"><span data-stu-id="bf775-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span>
</dt> <dd>

<span data-ttu-id="bf775-614">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bf775-614">0x00000001</span></span>

<span data-ttu-id="bf775-615">Utiliza transferencias seguras.</span><span class="sxs-lookup"><span data-stu-id="bf775-615">Uses secure transfers.</span></span> <span data-ttu-id="bf775-616">Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-616">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="bf775-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>marca de seguridad \_ \_ SSL</span><span class="sxs-lookup"><span data-stu-id="bf775-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>SECURITY\_FLAG\_SSL</span></span>
</dt> <dd>

<span data-ttu-id="bf775-618">0x00000002</span><span class="sxs-lookup"><span data-stu-id="bf775-618">0x00000002</span></span>

<span data-ttu-id="bf775-619">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-619">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>Indicador de seguridad \_ \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="bf775-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>SECURITY\_FLAG\_SSL3</span></span>
</dt> <dd>

<span data-ttu-id="bf775-621">0x00000004</span><span class="sxs-lookup"><span data-stu-id="bf775-621">0x00000004</span></span>

<span data-ttu-id="bf775-622">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-622">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>nivel de intensidad de marca de seguridad \_ \_ \_ medio</span><span class="sxs-lookup"><span data-stu-id="bf775-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span>
</dt> <dd>

<span data-ttu-id="bf775-624">0x40000000</span><span class="sxs-lookup"><span data-stu-id="bf775-624">0x40000000</span></span>

<span data-ttu-id="bf775-625">Usa el cifrado medio (56 bits).</span><span class="sxs-lookup"><span data-stu-id="bf775-625">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="bf775-626">Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-626">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="bf775-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>intensidad de marca de seguridad \_ \_ \_ fuerte</span><span class="sxs-lookup"><span data-stu-id="bf775-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span>
</dt> <dd>

<span data-ttu-id="bf775-628">0x20000000</span><span class="sxs-lookup"><span data-stu-id="bf775-628">0x20000000</span></span>

<span data-ttu-id="bf775-629">Usa el cifrado seguro (128 bits).</span><span class="sxs-lookup"><span data-stu-id="bf775-629">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="bf775-630">Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-630">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="bf775-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>intensidad de marca de seguridad \_ \_ \_ débil</span><span class="sxs-lookup"><span data-stu-id="bf775-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span>
</dt> <dd>

<span data-ttu-id="bf775-632">0x10000000</span><span class="sxs-lookup"><span data-stu-id="bf775-632">0x10000000</span></span>

<span data-ttu-id="bf775-633">Usa el cifrado débil (40 bits).</span><span class="sxs-lookup"><span data-stu-id="bf775-633">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="bf775-634">Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-634">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="bf775-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>marca de seguridad \_ \_ UNKNOWNBIT</span><span class="sxs-lookup"><span data-stu-id="bf775-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>SECURITY\_FLAG\_UNKNOWNBIT</span></span>
</dt> <dd>

<span data-ttu-id="bf775-636">0x80000000</span><span class="sxs-lookup"><span data-stu-id="bf775-636">0x80000000</span></span>

<span data-ttu-id="bf775-637">Se desconoce el tamaño de bits utilizado en el cifrado.</span><span class="sxs-lookup"><span data-stu-id="bf775-637">The bit size used in the encryption is unknown.</span></span> <span data-ttu-id="bf775-638">Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-638">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> </dl>

<span data-ttu-id="bf775-639">Tenga en cuenta que los datos recuperados de esta manera se relacionan con una transacción que se ha producido, cuyo nivel de seguridad ya no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="bf775-639">Be aware that the data retrieved this way relates to a transaction that has occurred, whose security level can no longer be changed.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="bf775-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**bits de la clave de seguridad de \_ opción de Internet \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**INTERNET\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-641">36</span><span class="sxs-lookup"><span data-stu-id="bf775-641">36</span></span>
</dt> <dt>



<span data-ttu-id="bf775-642">Recupera un valor entero largo sin signo que contiene el tamaño de bits de la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="bf775-642">Retrieves an unsigned long integer value that contains the bit size of the encryption key.</span></span> <span data-ttu-id="bf775-643">Cuanto mayor sea el número, mayor será la intensidad de cifrado utilizada.</span><span class="sxs-lookup"><span data-stu-id="bf775-643">The larger the number, the greater the encryption strength used.</span></span> <span data-ttu-id="bf775-644">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-644">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="bf775-645">Tenga en cuenta que los datos recuperados de esta manera se relacionan con una transacción que ya se ha producido, cuyo nivel de seguridad ya no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="bf775-645">Be aware that the data retrieved this way relates to a transaction that has already occurred, whose security level can no longer be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**\_rendimiento de \_ envío de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**INTERNET\_OPTION\_SEND\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-647">56</span><span class="sxs-lookup"><span data-stu-id="bf775-647">56</span></span>
</dt> <dt>



<span data-ttu-id="bf775-648">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bf775-648">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**\_tiempo de \_ espera de envío de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**INTERNET\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-650">5</span><span class="sxs-lookup"><span data-stu-id="bf775-650">5</span></span>
</dt> <dt>



<span data-ttu-id="bf775-651">Establece o recupera un valor entero largo sin signo, en milisegundos, que contiene el valor de tiempo de espera para enviar una solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf775-651">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request.</span></span> <span data-ttu-id="bf775-652">Si el envío tarda más que este valor de tiempo de espera, se cancela el envío.</span><span class="sxs-lookup"><span data-stu-id="bf775-652">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="bf775-653">Esta opción se puede utilizar en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluido un identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="bf775-653">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="bf775-654">Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-654">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="bf775-655">Cuando se utiliza en referencia a una transacción FTP, esta opción hace referencia al canal de control.</span><span class="sxs-lookup"><span data-stu-id="bf775-655">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**contexto de la cadena de certificados del servidor de opciones de INTERNET \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**INTERNET\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-657">105</span><span class="sxs-lookup"><span data-stu-id="bf775-657">105</span></span>
</dt> <dt>



<span data-ttu-id="bf775-658">Recupera el contexto de la cadena de certificados del servidor como un [contexto de \_ cadena \_ de PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context)duplicado.</span><span class="sxs-lookup"><span data-stu-id="bf775-658">Retrieves the server s certificate-chain context as a duplicated [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="bf775-659">Puede pasar este contexto duplicado a cualquier función de la API de cifrado que toma un [ \_ \_ contexto de cadena de PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span><span class="sxs-lookup"><span data-stu-id="bf775-659">You may pass this duplicated context to any Crypto API function which takes a [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="bf775-660">Debe llamar a [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) en el [contexto de \_ cadena \_ de PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) devuelto cuando haya terminado con el contexto de la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="bf775-660">You must call [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) on the returned [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) when you are done with the certificate-chain context.</span></span>

<span data-ttu-id="bf775-661">**Versión:** Requiere Internet Explorer 8,0.</span><span class="sxs-lookup"><span data-stu-id="bf775-661">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**configuración de opciones de INTERNET \_ \_ \_ cambiada**</span><span class="sxs-lookup"><span data-stu-id="bf775-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**INTERNET\_OPTION\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-663">39</span><span class="sxs-lookup"><span data-stu-id="bf775-663">39</span></span>
</dt> <dt>



<span data-ttu-id="bf775-664">Notifica al sistema que se ha cambiado la configuración del registro para que Compruebe la configuración de la siguiente llamada a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="bf775-664">Notifies the system that the registry settings have been changed so that it verifies the settings on the next call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="bf775-665">Se usa en [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-665">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**opción de INTERNET \_ \_ suprimir \_ autenticación de servidor \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-667">104</span><span class="sxs-lookup"><span data-stu-id="bf775-667">104</span></span>
</dt> <dt>



<span data-ttu-id="bf775-668">Establece un objeto de solicitud HTTP que no iniciará sesión en los servidores de origen, pero realizará el inicio de sesión automático en los servidores proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="bf775-668">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="bf775-669">Esta opción difiere de la marca de solicitud **Internet \_ marca \_ no \_ auth**, lo que impide la autenticación en los servidores proxy y los servidores de origen.</span><span class="sxs-lookup"><span data-stu-id="bf775-669">This option differs from the Request flag **INTERNET\_FLAG\_NO\_AUTH**, which prevents authentication to both proxy servers and origin servers.</span></span>

<span data-ttu-id="bf775-670">Si se establece este modo, se suprimirá el uso de cualquier material de credencial (ya sea el nombre de usuario o la contraseña previamente o el certificado SSL de cliente) al comunicarse con un servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="bf775-670">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="bf775-671">Sin embargo, si la solicitud debe estar en tránsito a través de un proxy de autenticación, WinINet seguirá realizando la autenticación automática en el proxy HTTP según la configuración de la zona de intranet del usuario.</span><span class="sxs-lookup"><span data-stu-id="bf775-671">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="bf775-672">La configuración de la zona de intranet predeterminada es permitir el inicio de sesión automático con las credenciales predeterminadas del usuario.</span><span class="sxs-lookup"><span data-stu-id="bf775-672">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span>

<span data-ttu-id="bf775-673">Para garantizar la supresión de toda la información de identificación, el autor de la llamada debe combinar la **opción de Internet \_ \_ suprimir \_ \_ autenticación de servidor** con la marca de solicitud **\_ marcar \_ sin \_ cookies** .</span><span class="sxs-lookup"><span data-stu-id="bf775-673">To ensure suppression of all identifying information, the caller should combine **INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH** with the **INTERNET\_FLAG\_NO\_COOKIES** request flag.</span></span>

<span data-ttu-id="bf775-674">Esta opción solo se puede establecer en los objetos de solicitud antes de que se hayan enviado.</span><span class="sxs-lookup"><span data-stu-id="bf775-674">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="bf775-675">Si se intenta establecer esta opción una vez enviada la solicitud, se devolverá el **\_ \_ \_ \_ Estado de identificador incorrecto de Internet**.</span><span class="sxs-lookup"><span data-stu-id="bf775-675">Attempts to set this option after the request has been sent will return **ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**.</span></span>

<span data-ttu-id="bf775-676">No se requiere ningún búfer para esta opción.</span><span class="sxs-lookup"><span data-stu-id="bf775-676">No buffer is required for this option.</span></span> <span data-ttu-id="bf775-677">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) lo usa solo en los identificadores devueltos por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="bf775-677">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) on handles returned by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) only.</span></span>

<span data-ttu-id="bf775-678">**Versión:** Requiere Internet Explorer 8,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="bf775-678">**Version:** Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**opción de INTERNET \_ \_ suprimir \_ comportamiento**</span><span class="sxs-lookup"><span data-stu-id="bf775-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**INTERNET\_OPTION\_SUPPRESS\_BEHAVIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-680">81</span><span class="sxs-lookup"><span data-stu-id="bf775-680">81</span></span>
</dt> <dt>



<span data-ttu-id="bf775-681">Opción de uso general que se usa para suprimir comportamientos en todo el proceso.</span><span class="sxs-lookup"><span data-stu-id="bf775-681">A general purpose option that is used to suppress behaviors on a process-wide basis.</span></span> <span data-ttu-id="bf775-682">El parámetro *lpBuffer* de la función debe ser un puntero a un valor DWORD que contenga el comportamiento específico que se va a suprimir.</span><span class="sxs-lookup"><span data-stu-id="bf775-682">The *lpBuffer* parameter of the function must be a pointer to a DWORD containing the specific behavior to suppress.</span></span> <span data-ttu-id="bf775-683">Esta opción no se puede consultar con [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-683">This option cannot be queried with [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="bf775-684">Los valores permitidos son:</span><span class="sxs-lookup"><span data-stu-id="bf775-684">The permitted values are:</span></span>

<dl> <dt>

<span data-ttu-id="bf775-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>INTERNET \_ suprimir \_ restablecer \_ todo</span><span class="sxs-lookup"><span data-stu-id="bf775-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>INTERNET\_SUPPRESS\_RESET\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="bf775-686">0</span><span class="sxs-lookup"><span data-stu-id="bf775-686">0</span></span>

<span data-ttu-id="bf775-687">Deshabilita todas las supresiones, volviendo a habilitar el comportamiento predeterminado y configurado.</span><span class="sxs-lookup"><span data-stu-id="bf775-687">Disables all suppressions, re-enabling default and configured behavior.</span></span> <span data-ttu-id="bf775-688">Esta opción es equivalente a la configuración de **Internet \_ suprimir la Directiva de \_ cookies \_ \_** y de suprimir el restablecimiento de **\_ \_ cookies \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="bf775-688">This option is the equivalent of setting **INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET** and **INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET** individually.</span></span>

<span data-ttu-id="bf775-689">**Versión:** Requiere Internet Explorer 6,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="bf775-689">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>\_Directiva de supresión de \_ cookies de Internet \_</span><span class="sxs-lookup"><span data-stu-id="bf775-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY</span></span> 
</dt> <dd>

<span data-ttu-id="bf775-691">1</span><span class="sxs-lookup"><span data-stu-id="bf775-691">1</span></span>

<span data-ttu-id="bf775-692">Omite las directivas de cookies configuradas y permite establecer las cookies.</span><span class="sxs-lookup"><span data-stu-id="bf775-692">Ignores any configured cookie policies and allows cookies to be set.</span></span>

<span data-ttu-id="bf775-693">**Versión:** Requiere Internet Explorer 6,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="bf775-693">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>anular \_ \_ restablecimiento de directiva de cookies de \_ Internet \_</span><span class="sxs-lookup"><span data-stu-id="bf775-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET</span></span> 
</dt> <dd>

<span data-ttu-id="bf775-695">2</span><span class="sxs-lookup"><span data-stu-id="bf775-695">2</span></span>

<span data-ttu-id="bf775-696">Deshabilita la supresión de la **\_ \_ \_ Directiva de cookies** de supresión de Internet, lo que permite la evaluación de cookies según la Directiva de cookies configurada.</span><span class="sxs-lookup"><span data-stu-id="bf775-696">Disables the **INTERNET\_SUPPRESS\_COOKIE\_POLICY** suppression, permitting the evaluation of cookies according to the configured cookie policy.</span></span>

<span data-ttu-id="bf775-697">**Versión:** Requiere Internet Explorer 6,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="bf775-697">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span>\_supresión de \_ cookies de Internet \_</span><span class="sxs-lookup"><span data-stu-id="bf775-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span> INTERNET\_SUPPRESS\_COOKIE\_PERSIST</span></span>
</dt> <dd>

<span data-ttu-id="bf775-699">3</span><span class="sxs-lookup"><span data-stu-id="bf775-699">3</span></span>

<span data-ttu-id="bf775-700">Suprime la persistencia de las cookies, incluso si el servidor las ha especificado como persistentes.</span><span class="sxs-lookup"><span data-stu-id="bf775-700">Suppresses the persistence of cookies, even if the server has specified them as persistent.</span></span>

<span data-ttu-id="bf775-701">**Versión:** Requiere Internet Explorer 8,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="bf775-701">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="bf775-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>supresión de cookies de eliminación de \_ \_ cookies de \_ Internet \_</span><span class="sxs-lookup"><span data-stu-id="bf775-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="bf775-703">4</span><span class="sxs-lookup"><span data-stu-id="bf775-703">4</span></span>

<span data-ttu-id="bf775-704">Deshabilita la supresión de la cookie de supresión de **\_ \_ cookies \_ de Internet** y vuelve a habilitar la persistencia de las cookies.</span><span class="sxs-lookup"><span data-stu-id="bf775-704">Disables the **INTERNET\_SUPPRESS\_COOKIE\_PERSIST** suppression, re-enabling the persistence of cookies.</span></span> <span data-ttu-id="bf775-705">Las cookies suprimidas anteriormente no serán persistentes.</span><span class="sxs-lookup"><span data-stu-id="bf775-705">Any previously suppressed cookies will not become persistent.</span></span>

<span data-ttu-id="bf775-706">**Versión:** Requiere Internet Explorer 8,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="bf775-706">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="bf775-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**\_ \_ dirección URL de la opción de Internet**</span><span class="sxs-lookup"><span data-stu-id="bf775-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**INTERNET\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-708">34</span><span class="sxs-lookup"><span data-stu-id="bf775-708">34</span></span>
</dt> <dt>



<span data-ttu-id="bf775-709">Recupera un valor de cadena que contiene la dirección URL completa de un recurso descargado.</span><span class="sxs-lookup"><span data-stu-id="bf775-709">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="bf775-710">Si la dirección URL original contenía datos adicionales, como cadenas de búsqueda o delimitadores, o si se redirigió la llamada, la dirección URL devuelta difiere de la original.</span><span class="sxs-lookup"><span data-stu-id="bf775-710">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="bf775-711">Esta opción es válida en los identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) devueltos por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="bf775-711">This option is valid on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="bf775-712">Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-712">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**agente de usuario de la opción de INTERNET \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**INTERNET\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-714">41</span><span class="sxs-lookup"><span data-stu-id="bf775-714">41</span></span>
</dt> <dt>



<span data-ttu-id="bf775-715">Establece o recupera la cadena de agente de usuario en los identificadores proporcionados por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) y se usa en las funciones de [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) subsiguientes, siempre y cuando no se reemplace por un encabezado agregado por [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) o [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="bf775-715">Sets or retrieves the user agent string on handles supplied by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) and used in subsequent [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions, as long as it is not overridden by a header added by [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) or [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="bf775-716">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-716">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**opción de INTERNET \_ \_ nombre de usuario**</span><span class="sxs-lookup"><span data-stu-id="bf775-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**INTERNET\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-718">28</span><span class="sxs-lookup"><span data-stu-id="bf775-718">28</span></span>
</dt> <dt>



<span data-ttu-id="bf775-719">Establece o recupera una cadena que contiene el nombre de usuario asociado a un identificador devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="bf775-719">Sets or retrieves a string that contains the user name associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="bf775-720">Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-720">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**\_versión de opción de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**INTERNET\_OPTION\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-722">40</span><span class="sxs-lookup"><span data-stu-id="bf775-722">40</span></span>
</dt> <dt>



<span data-ttu-id="bf775-723">Recupera una estructura **de \_ \_ información de versión de Internet** que contiene el número de versión de Wininet.dll.</span><span class="sxs-lookup"><span data-stu-id="bf775-723">Retrieves an **INTERNET\_VERSION\_INFO** structure that contains the version number of Wininet.dll.</span></span> <span data-ttu-id="bf775-724">Esta opción puede usarse en un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) **nulo** por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-724">This option can be used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf775-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**\_tamaño de \_ búfer de escritura de opciones de Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf775-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**INTERNET\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf775-726">13</span><span class="sxs-lookup"><span data-stu-id="bf775-726">13</span></span>
</dt> <dt>



<span data-ttu-id="bf775-727">Establece o recupera un valor entero largo sin signo que contiene el tamaño, en bytes, del búfer de escritura.</span><span class="sxs-lookup"><span data-stu-id="bf775-727">Sets or retrieves an unsigned long integer value that contains the size, in bytes, of the write buffer.</span></span> <span data-ttu-id="bf775-728">Esta opción se puede usar en los identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) devueltos por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) y [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (solo sesión FTP).</span><span class="sxs-lookup"><span data-stu-id="bf775-728">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="bf775-729">Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="bf775-729">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf775-730">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf775-730">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bf775-731">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="bf775-731">WinINet does not support server implementations.</span></span> <span data-ttu-id="bf775-732">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="bf775-732">In addition, it should not be used from a service.</span></span> <span data-ttu-id="bf775-733">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="bf775-733">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf775-734">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf775-734">Requirements</span></span>



| <span data-ttu-id="bf775-735">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf775-735">Requirement</span></span> | <span data-ttu-id="bf775-736">Value</span><span class="sxs-lookup"><span data-stu-id="bf775-736">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf775-737">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf775-737">Minimum supported client</span></span><br/> | <span data-ttu-id="bf775-738">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bf775-738">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="bf775-739">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf775-739">Minimum supported server</span></span><br/> | <span data-ttu-id="bf775-740">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf775-740">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                   |
| <span data-ttu-id="bf775-741">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf775-741">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf775-742"><dt>Wininet. h; </dt> <dt>Winineti. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf775-742"><dt>Wininet.h; </dt> <dt>Winineti.h</dt></span></span> </dl> |



 

