---
description: GetLastError devuelve los valores de error identificados en este tema cuando se produce un error en una de las funciones de servicios HTTP de Microsoft Windows (WinHTTP).
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Mensajes de error (winhttp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910850"
---
# <a name="error-messages-winhttph"></a><span data-ttu-id="c4a4b-103">Mensajes de error (winhttp. h)</span><span class="sxs-lookup"><span data-stu-id="c4a4b-103">Error Messages (Winhttp.h)</span></span>

<span data-ttu-id="c4a4b-104">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los valores de error enumerados a continuación cuando se produce un error en una de las funciones de los servicios http de Microsoft Windows (WinHTTP) y también se devuelven en los 16 bits inferiores del error [**HRESULT**](../com/structure-of-com-error-codes.md) del objeto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="c4a4b-104">The error values listed below are returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) when one of the Microsoft Windows HTTP Services (WinHTTP) functions fails, and are also returned in the lower 16 bits of [**HRESULT**](../com/structure-of-com-error-codes.md) error returns from the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

<span data-ttu-id="c4a4b-105">Los valores de error cuyos nombres empiezan por "ERROR \_ WinHTTP \_ " son específicos de las funciones winhttp.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-105">Error values whose names begin with "ERROR\_WINHTTP\_" are specific to the WinHTTP functions.</span></span> <span data-ttu-id="c4a4b-106">Las funciones WinHTTP también devuelven mensajes de error de Windows cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-106">The WinHTTP functions also return Windows error messages where appropriate.</span></span>

<dl> <dt>

<span data-ttu-id="c4a4b-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**error \_ de \_ \_ servicio de proxy automático \_ de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERROR\_WINHTTP\_AUTO\_PROXY\_SERVICE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-108">12178</span><span class="sxs-lookup"><span data-stu-id="c4a4b-108">12178</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-109">Devuelto por [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) cuando no se puede encontrar un proxy para la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-109">Returned by [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) when a proxy for the specified URL cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERROR en la \_ \_ detección automática de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERROR\_WINHTTP\_AUTODETECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-111">12180</span><span class="sxs-lookup"><span data-stu-id="c4a4b-111">12180</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-112">Devuelto por [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) si WinHTTP no pudo detectar la dirección URL del archivo de configuración automática de proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="c4a4b-112">Returned by [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) if WinHTTP was unable to discover the URL of the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERROR en el \_ script WinHTTP de \_ \_ proxy automático incorrecto \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERROR\_WINHTTP\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-114">12166</span><span class="sxs-lookup"><span data-stu-id="c4a4b-114">12166</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-115">Error al ejecutar el código de script en el archivo de configuración automática de proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="c4a4b-115">An error occurred executing the script code in the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERROR \_ WinHTTP \_ no puede \_ llamar \_ después de \_ Open**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-117">12103</span><span class="sxs-lookup"><span data-stu-id="c4a4b-117">12103</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-118">Lo devuelve el objeto [**HttpRequest**](winhttprequest.md) si una opción especificada no se puede solicitar una vez que se ha llamado al método [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="c4a4b-118">Returned by the [**HttpRequest**](winhttprequest.md) object if a specified option cannot be requested after the [**Open**](iwinhttprequest-open.md) method has been called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERROR \_ WinHTTP \_ no puede \_ llamar \_ después del \_ envío**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-120">12102</span><span class="sxs-lookup"><span data-stu-id="c4a4b-120">12102</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-121">Lo devuelve el objeto [**HttpRequest**](winhttprequest.md) si una operación solicitada no se puede realizar después de llamar al método [**send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="c4a4b-121">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed after calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERROR \_ WinHTTP \_ no se puede \_ llamar a \_ antes de \_ abrir**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-123">12100</span><span class="sxs-lookup"><span data-stu-id="c4a4b-123">12100</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-124">Lo devuelve el objeto [**HttpRequest**](winhttprequest.md) si una operación solicitada no se puede realizar antes de llamar al método [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="c4a4b-124">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Open**](iwinhttprequest-open.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERROR \_ WinHTTP \_ no se puede \_ llamar a \_ antes de \_ Enviar**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-126">12101</span><span class="sxs-lookup"><span data-stu-id="c4a4b-126">12101</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-127">Lo devuelve el objeto [**HttpRequest**](winhttprequest.md) si una operación solicitada no se puede realizar antes de llamar al método [**send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="c4a4b-127">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERROR \_ WinHTTP \_ no se puede \_ conectar**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERROR\_WINHTTP\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-129">12029</span><span class="sxs-lookup"><span data-stu-id="c4a4b-129">12029</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-130">Se devuelve si se produce un error en la conexión al servidor.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-130">Returned if connection to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR \_ de \_ certificado de autenticación de cliente WinHTTP \_ \_ \_ necesario**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4a4b-132">El servidor requiere la autenticación del cliente SSL.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-132">The server requires SSL client Authentication.</span></span> <span data-ttu-id="c4a4b-133">La aplicación recupera la lista de emisores de certificados mediante una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con la opción **WinHTTP \_ \_ \_ \_ \_ lista de emisores** de certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-133">The application retrieves the list of certificate issuers by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="c4a4b-134">Para obtener más información, consulte la opción **WinHTTP \_ \_ \_ \_ \_ lista de emisores de certificados de cliente** .</span><span class="sxs-lookup"><span data-stu-id="c4a4b-134">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

<span data-ttu-id="c4a4b-135">Si el servidor solicita el certificado de cliente, pero no lo requiere, la aplicación puede llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) de manera alternativa con la opción de contexto de certificado de cliente de la **\_ opción \_ \_ \_ WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="c4a4b-135">If the server requests the client certificate, but does not require it, the application can alternately call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="c4a4b-136">En este caso, la aplicación especifica la \_ macro de \_ \_ contexto de certificado WinHTTP no Client \_ en el parámetro *lpBuffer* de **WinHttpSetOption**.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-136">In this case, the application specifies the WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT macro in the *lpBuffer* parameter of **WinHttpSetOption**.</span></span> <span data-ttu-id="c4a4b-137">Para obtener más información, vea la opción **WinHTTP \_ contexto de \_ \_ certificado \_ de cliente** .</span><span class="sxs-lookup"><span data-stu-id="c4a4b-137">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>

<span data-ttu-id="c4a4b-138">**Windows Server 2003 con SP1 y Windows XP con SP2:** Este error no se admite.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-138">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERROR \_ : \_ \_ no se \_ \_ puede obtener acceso a la \_ \_ clave privada del certificado de cliente WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_ACCESS\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4a4b-140">La aplicación no tiene los privilegios necesarios para tener acceso a la clave privada asociada con el certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-140">The application does not have the required privileges to access the private key associated with the client certificate.</span></span>

<span data-ttu-id="c4a4b-141">**Windows Server 2003 con SP1 y Windows XP con SP2:** Este error no se admite.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-141">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERROR \_ de \_ certificado de cliente WinHTTP \_ \_ sin \_ \_ clave privada**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4a4b-143">El contexto para el certificado de cliente SSL no tiene una clave privada asociada.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-143">The context for the SSL client certificate does not have a private key associated with it.</span></span> <span data-ttu-id="c4a4b-144">Es posible que el certificado de cliente se haya importado al equipo sin la clave privada.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-144">The client certificate may have been imported to the computer without the private key.</span></span>

<span data-ttu-id="c4a4b-145">**Windows Server 2003 con SP1 y Windows XP con SP2:** Este error no se admite.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-145">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERROR \_ de \_ desbordamiento de \_ tamaño de \_ encabezado de codificación \_ fragmentada de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERROR\_WINHTTP\_CHUNKED\_ENCODING\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-147">12183</span><span class="sxs-lookup"><span data-stu-id="c4a4b-147">12183</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-148">Devuelto por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) cuando se encuentra una condición de desbordamiento en el transcurso del análisis de la codificación fragmentada.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-148">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when an overflow condition is encountered in the course of parsing chunked encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR \_ de \_ certificado de autenticación de cliente WinHTTP \_ \_ \_ necesario**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-150">12044</span><span class="sxs-lookup"><span data-stu-id="c4a4b-150">12044</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-151">Devuelto por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) cuando el servidor solicita la autenticación del cliente.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-151">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the server requests client authentication.</span></span>

<span data-ttu-id="c4a4b-152">**Windows Server 2003 con SP1 y Windows XP con SP2:** Este error no se admite.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-152">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**error \_ de \_ conexión de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**ERROR\_WINHTTP\_CONNECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-154">12030</span><span class="sxs-lookup"><span data-stu-id="c4a4b-154">12030</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-155">La conexión con el servidor se ha restablecido o finalizado o se ha encontrado un protocolo SSL incompatible.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-155">The connection with the server has been reset or terminated, or an incompatible SSL protocol was encountered.</span></span> <span data-ttu-id="c4a4b-156">Por ejemplo, la versión 5,1 de WinHTTP no admite SSL2 a menos que el cliente lo habilite específicamente.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-156">For example, WinHTTP version 5.1 does not support SSL2 unless the client specifically enables it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**el \_ encabezado WinHTTP del error \_ \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**ERROR\_WINHTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-158">12155</span><span class="sxs-lookup"><span data-stu-id="c4a4b-158">12155</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-159">Obsoleto ya no se usa.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-159">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**se \_ \_ \_ superó el número de encabezados WinHTTP de error \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERROR\_WINHTTP\_HEADER\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-161">12181</span><span class="sxs-lookup"><span data-stu-id="c4a4b-161">12181</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-162">Devuelto por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) cuando un número mayor de encabezados estaba presente en una respuesta a la que WinHTTP podría recibir.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-162">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when a larger number of headers were present in a response than WinHTTP could receive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**\_ \_ \_ no \_ se encontró el encabezado WinHTTP del error**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERROR\_WINHTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-164">12150</span><span class="sxs-lookup"><span data-stu-id="c4a4b-164">12150</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-165">No se puede encontrar el encabezado solicitado.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-165">The requested header cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERROR \_ de \_ \_ desbordamiento de tamaño de encabezado WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERROR\_WINHTTP\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-167">12182</span><span class="sxs-lookup"><span data-stu-id="c4a4b-167">12182</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-168">Devuelto por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) cuando el tamaño de los encabezados recibidos supera el límite para el identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-168">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the size of headers received exceeds the limit for the request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERROR \_ de \_ \_ Estado de identificador incorrecto de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-170">12019</span><span class="sxs-lookup"><span data-stu-id="c4a4b-170">12019</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-171">No se puede realizar la operación solicitada porque el identificador proporcionado no tiene el estado correcto.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-171">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERROR \_ de \_ \_ tipo de identificador incorrecto de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-173">12018</span><span class="sxs-lookup"><span data-stu-id="c4a4b-173">12018</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-174">El tipo de identificador proporcionado no es correcto para esta operación.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-174">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**error \_ interno de WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**ERROR\_WINHTTP\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-176">12004</span><span class="sxs-lookup"><span data-stu-id="c4a4b-176">12004</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-177">Se ha producido un error interno.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-177">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERROR \_ WinHTTP \_ opción no válida \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERROR\_WINHTTP\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-179">12009</span><span class="sxs-lookup"><span data-stu-id="c4a4b-179">12009</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-180">Una solicitud a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) especificó un valor de opción no válido.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-180">A request to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) or [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERROR \_ en \_ WinHTTP \_ solicitud de consulta no válida \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERROR\_WINHTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-182">12154</span><span class="sxs-lookup"><span data-stu-id="c4a4b-182">12154</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-183">Obsoleto ya no se usa.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-183">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERROR \_ WinHTTP \_ \_ respuesta del servidor no válida \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERROR\_WINHTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-185">12152</span><span class="sxs-lookup"><span data-stu-id="c4a4b-185">12152</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-186">No se puede analizar la respuesta del servidor.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-186">The server response cannot be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERROR \_ de \_ WinHTTP \_ dirección URL no válida**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERROR\_WINHTTP\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-188">12005</span><span class="sxs-lookup"><span data-stu-id="c4a4b-188">12005</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-189">La URL no es válida.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-189">The URL is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERROR \_ de \_ Inicio de sesión de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERROR\_WINHTTP\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-191">12015</span><span class="sxs-lookup"><span data-stu-id="c4a4b-191">12015</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-192">Error en el intento de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-192">The login attempt failed.</span></span> <span data-ttu-id="c4a4b-193">Cuando se encuentra este error, el identificador de solicitud debe cerrarse con [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle).</span><span class="sxs-lookup"><span data-stu-id="c4a4b-193">When this error is encountered, the request handle should be closed with [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle).</span></span> <span data-ttu-id="c4a4b-194">Se debe crear un nuevo identificador de solicitud antes de volver a intentar la función que generó originalmente este error.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-194">A new request handle must be created before retrying the function that originally produced this error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERROR \_ \_ el nombre WinHTTP \_ no se \_ resolvió**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERROR\_WINHTTP\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-196">12007</span><span class="sxs-lookup"><span data-stu-id="c4a4b-196">12007</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-197">No se puede resolver el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-197">The server name cannot be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERROR \_ WinHTTP \_ no \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERROR\_WINHTTP\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-199">12172</span><span class="sxs-lookup"><span data-stu-id="c4a4b-199">12172</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-200">Obsoleto ya no se usa.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-200">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERROR \_ de \_ operación WinHTTP \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERROR\_WINHTTP\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-202">12017</span><span class="sxs-lookup"><span data-stu-id="c4a4b-202">12017</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-203">La operación se canceló, normalmente porque el identificador en el que estaba funcionando la solicitud se cerró antes de que se completara la operación.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-203">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERROR de la \_ \_ opción WinHTTP \_ no \_ configurable**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERROR\_WINHTTP\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-205">12011</span><span class="sxs-lookup"><span data-stu-id="c4a4b-205">12011</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-206">No se puede establecer la opción solicitada, solo se consulta.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-206">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERROR \_ WinHTTP \_ fuera \_ de los \_ identificadores**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERROR\_WINHTTP\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-208">12001</span><span class="sxs-lookup"><span data-stu-id="c4a4b-208">12001</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-209">Obsoleto ya no se usa.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-209">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERROR \_ de \_ redirección de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERROR\_WINHTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-211">12156</span><span class="sxs-lookup"><span data-stu-id="c4a4b-211">12156</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-212">No se pudo realizar la redirección porque se produjo un error en el esquema cambiado o en todos los intentos realizados para la redirección (el valor predeterminado es cinco intentos).</span><span class="sxs-lookup"><span data-stu-id="c4a4b-212">The redirection failed because either the scheme changed or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERROR \_ de \_ solicitud de reenvío de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERROR\_WINHTTP\_RESEND\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-214">12032</span><span class="sxs-lookup"><span data-stu-id="c4a4b-214">12032</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-215">Error en la función WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-215">The WinHTTP function failed.</span></span> <span data-ttu-id="c4a4b-216">Se puede reintentar la función deseada en el mismo identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-216">The desired function can be retried on the same request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERROR de desbordamiento de la \_ \_ respuesta WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERROR\_WINHTTP\_RESPONSE\_DRAIN\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-218">12184</span><span class="sxs-lookup"><span data-stu-id="c4a4b-218">12184</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-219">Se devuelve cuando una respuesta entrante supera un límite de tamaño de WinHTTP interno.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-219">Returned when an incoming response exceeds an internal WinHTTP size limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**error \_ de \_ ejecución del script WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**ERROR\_WINHTTP\_SCRIPT\_EXECUTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-221">12177</span><span class="sxs-lookup"><span data-stu-id="c4a4b-221">12177</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-222">Se encontró un error al ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-222">An error was encountered while executing a script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERROR \_ WinHTTP \_ Secure \_ CERT \_ CN \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-224">12038</span><span class="sxs-lookup"><span data-stu-id="c4a4b-224">12038</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-225">Se devuelve cuando el nombre de un certificado CN no coincide con el valor pasado (equivalente a un error del **certificado \_ E \_ CN \_ no \_ coincide** ).</span><span class="sxs-lookup"><span data-stu-id="c4a4b-225">Returned when a certificate CN name does not match the passed value (equivalent to a **CERT\_E\_CN\_NO\_MATCH** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERROR en la \_ \_ fecha del certificado de seguridad WinHTTP \_ \_ \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-227">12037</span><span class="sxs-lookup"><span data-stu-id="c4a4b-227">12037</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-228">Indica que un certificado necesario no se encuentra dentro de su período de validez al comprobar con el reloj del sistema actual o la marca de tiempo del archivo firmado, o que los períodos de validez de la cadena de certificación no se anidan correctamente (equivalente a un **certificado \_ e \_ caducado** o a un error de **certificado \_ e \_ VALIDITYPERIODNESTING** ).</span><span class="sxs-lookup"><span data-stu-id="c4a4b-228">Indicates that a required certificate is not within its validity period when verifying against the current system clock or the timestamp in the signed file, or that the validity periods of the certification chain do not nest correctly (equivalent to a **CERT\_E\_EXPIRED** or a **CERT\_E\_VALIDITYPERIODNESTING** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERROR WinHTTP ERROR en la \_ \_ revisión del certificado de seguridad \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-230">12057</span><span class="sxs-lookup"><span data-stu-id="c4a4b-230">12057</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-231">Indica que no se puede comprobar la revocación porque el servidor de revocación estaba sin conexión (equivalente a la **REvocación de cifrado \_ E \_ \_ sin conexión**).</span><span class="sxs-lookup"><span data-stu-id="c4a4b-231">Indicates that revocation cannot be checked because the revocation server was offline (equivalent to **CRYPT\_E\_REVOCATION\_OFFLINE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERROR \_ WinHTTP \_ \_ certificado seguro \_ revocado**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-233">12170</span><span class="sxs-lookup"><span data-stu-id="c4a4b-233">12170</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-234">Indica que se ha revocado un certificado (equivalente a **cifrado \_ E \_ revocado**).</span><span class="sxs-lookup"><span data-stu-id="c4a4b-234">Indicates that a certificate has been revoked (equivalent to **CRYPT\_E\_REVOKED**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERROR \_ de \_ \_ \_ uso incorrecto de certificado de seguridad WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_WRONG\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-236">12179</span><span class="sxs-lookup"><span data-stu-id="c4a4b-236">12179</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-237">Indica que un certificado no es válido para el uso solicitado (equivalente al **uso del certificado \_ E \_ incorrecto \_**).</span><span class="sxs-lookup"><span data-stu-id="c4a4b-237">Indicates that a certificate is not valid for the requested usage (equivalent to **CERT\_E\_WRONG\_USAGE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**error \_ de \_ canal seguro de WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**ERROR\_WINHTTP\_SECURE\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-239">12157</span><span class="sxs-lookup"><span data-stu-id="c4a4b-239">12157</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-240">Indica que se produjo un error al tener que hacer con un canal seguro (equivalente a códigos de error que comienzan por "SEC \_ e \_ " y "s \_ I \_ " enumerados en el archivo de encabezado "Winerror. h").</span><span class="sxs-lookup"><span data-stu-id="c4a4b-240">Indicates that an error occurred having to do with a secure channel (equivalent to error codes that begin with "SEC\_E\_" and "SEC\_I\_" listed in the "winerror.h" header file).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERROR \_ WinHTTP \_ Secure \_ error**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERROR\_WINHTTP\_SECURE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-242">12175</span><span class="sxs-lookup"><span data-stu-id="c4a4b-242">12175</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-243">Se encontraron uno o varios errores en el certificado Capa de sockets seguros (SSL) enviado por el servidor.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-243">One or more errors were found in the Secure Sockets Layer (SSL) certificate sent by the server.</span></span> <span data-ttu-id="c4a4b-244">Para determinar qué tipo de error se encontró, busque una notificación [**de \_ \_ error de \_ protección \_ del estado de devolución de llamada de WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) en una función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-244">To determine what type of error was encountered, check for a [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification in a status callback function.</span></span> <span data-ttu-id="c4a4b-245">Para obtener más información, vea la [**\_ devolución de \_ llamada de estado de WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span><span class="sxs-lookup"><span data-stu-id="c4a4b-245">For more information, see [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERROR \_ WinHTTP \_ seguro \_ CA no válido \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-247">12045</span><span class="sxs-lookup"><span data-stu-id="c4a4b-247">12045</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-248">Indica que se procesó una cadena de certificados, pero termina en un certificado raíz que no es de confianza para el proveedor de confianza (equivalente a **CERT \_ E \_ UNTRUSTEDROOT**).</span><span class="sxs-lookup"><span data-stu-id="c4a4b-248">Indicates that a certificate chain was processed, but terminated in a root certificate that is not trusted by the trust provider (equivalent to **CERT\_E\_UNTRUSTEDROOT**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERROR \_ WinHTTP \_ seguro \_ certificado no válido \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-250">12169</span><span class="sxs-lookup"><span data-stu-id="c4a4b-250">12169</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-251">Indica que un certificado no es válido (lo que equivale a errores como el **\_ \_ rol CERT e**, **CERT \_ e \_ PATHLENCONST**, **CERT e \_ \_ Critical**, **CERT y \_ \_ purpose**, **CERT \_ e \_ ISSUERCHAINING**, el **certificado e es \_ \_ incorrecto** y el **\_ \_ encadenamiento de certificados e**).</span><span class="sxs-lookup"><span data-stu-id="c4a4b-251">Indicates that a certificate is invalid (equivalent to errors such as **CERT\_E\_ROLE**, **CERT\_E\_PATHLENCONST**, **CERT\_E\_CRITICAL**, **CERT\_E\_PURPOSE**, **CERT\_E\_ISSUERCHAINING**, **CERT\_E\_MALFORMED** and **CERT\_E\_CHAINING**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERROR \_ de \_ apagado de WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERROR\_WINHTTP\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-253">12012</span><span class="sxs-lookup"><span data-stu-id="c4a4b-253">12012</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-254">La compatibilidad con la función WinHTTP se está cerrando o descargando.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-254">The WinHTTP function support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERROR \_ de \_ tiempo de espera de WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERROR\_WINHTTP\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-256">12002</span><span class="sxs-lookup"><span data-stu-id="c4a4b-256">12002</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-257">La solicitud ha agotado el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-257">The request has timed out.</span></span>

<span data-ttu-id="c4a4b-258">Este error se puede devolver como resultado del comportamiento de tiempo de espera de TCP/IP, independientemente de los valores de tiempo de espera establecidos en los servicios HTTP de Windows.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-258">This error can be returned as a result of TCP/IP time-out behavior, regardless of time-out values set in Windows HTTP Services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERROR \_ WinHTTP \_ no se puede \_ \_ descargar el \_ script**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERROR\_WINHTTP\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-260">12167</span><span class="sxs-lookup"><span data-stu-id="c4a4b-260">12167</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-261">No se puede descargar el archivo PAC.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-261">The PAC file cannot be downloaded.</span></span> <span data-ttu-id="c4a4b-262">Por ejemplo, puede que el servidor al que hace referencia la dirección URL de PAC no sea accesible o que el servidor devuelva una respuesta 404 no encontrada.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-262">For example, the server referenced by the PAC URL may not have been reachable, or the server returned a 404 NOT FOUND response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERROR \_ de \_ tipo de script WinHTTP no controlado \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERROR\_WINHTTP\_UNHANDLED\_SCRIPT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-264">12176</span><span class="sxs-lookup"><span data-stu-id="c4a4b-264">12176</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-265">No se admite el tipo de script.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-265">The script type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERROR en el \_ \_ esquema WinHTTP desconocido \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERROR\_WINHTTP\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a4b-267">12006</span><span class="sxs-lookup"><span data-stu-id="c4a4b-267">12006</span></span>
</dt> <dt>



<span data-ttu-id="c4a4b-268">La dirección URL especificó un esquema distinto de "http:" o "https:".</span><span class="sxs-lookup"><span data-stu-id="c4a4b-268">The URL specified a scheme other than "http:" or "https:".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR \_ de \_ memoria insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4a4b-270">No había suficiente memoria disponible para completar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-270">Not enough memory was available to complete the requested operation.</span></span>

<span data-ttu-id="c4a4b-271">**Encabezado:** Declarado en Winerror. h</span><span class="sxs-lookup"><span data-stu-id="c4a4b-271">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR \_ de \_ búfer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4a4b-273">El tamaño, en bytes, del búfer proporcionado a una función no era suficiente para contener los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-273">The size, in bytes, of the buffer supplied to a function was insufficient to contain the returned data.</span></span> <span data-ttu-id="c4a4b-274">Para obtener más información, vea la función específica.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-274">For more information, see the specific function.</span></span>

<span data-ttu-id="c4a4b-275">**Encabezado:** Declarado en Winerror. h</span><span class="sxs-lookup"><span data-stu-id="c4a4b-275">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR \_ de \_ identificador no válido**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4a4b-277">El identificador pasado a la interfaz de programación de aplicaciones (API) se ha invalidado o cerrado.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-277">The handle passed to the application programming interface (API) has been either invalidated or closed.</span></span>

<span data-ttu-id="c4a4b-278">**Encabezado:** Declarado en Winerror. h</span><span class="sxs-lookup"><span data-stu-id="c4a4b-278">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR: \_ no hay \_ más \_ archivos**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4a4b-280">No se encontraron más archivos.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-280">No more files have been found.</span></span>

<span data-ttu-id="c4a4b-281">**Encabezado:** Declarado en Winerror. h</span><span class="sxs-lookup"><span data-stu-id="c4a4b-281">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**\_no hay \_ más \_ elementos de error**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4a4b-283">No se han encontrado más elementos.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-283">No more items have been found.</span></span>

<span data-ttu-id="c4a4b-284">**Encabezado:** Declarado en Winerror. h</span><span class="sxs-lookup"><span data-stu-id="c4a4b-284">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a4b-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR \_ no \_ admitido**</span><span class="sxs-lookup"><span data-stu-id="c4a4b-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4a4b-286">La pila de protocolos necesaria no está cargada y la aplicación no puede iniciar WinSock.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-286">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>

<span data-ttu-id="c4a4b-287">**Encabezado:** Declarado en Winerror. h</span><span class="sxs-lookup"><span data-stu-id="c4a4b-287">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4a4b-288">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4a4b-288">Remarks</span></span>

<span data-ttu-id="c4a4b-289">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-289">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4a4b-290">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4a4b-290">Requirements</span></span>



| <span data-ttu-id="c4a4b-291">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4a4b-291">Requirement</span></span> | <span data-ttu-id="c4a4b-292">Value</span><span class="sxs-lookup"><span data-stu-id="c4a4b-292">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a4b-293">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4a4b-293">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a4b-294">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="c4a4b-294">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="c4a4b-295">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4a4b-295">Minimum supported server</span></span><br/> | <span data-ttu-id="c4a4b-296">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="c4a4b-296">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="c4a4b-297">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c4a4b-297">Redistributable</span></span><br/>          | <span data-ttu-id="c4a4b-298">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-298">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="c4a4b-299">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4a4b-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4a4b-300"><dt>Winhttp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4a4b-300"><dt>Winhttp.h</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c4a4b-301">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4a4b-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4a4b-302">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c4a4b-302">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

