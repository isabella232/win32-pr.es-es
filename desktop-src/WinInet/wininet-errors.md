---
title: Mensajes de error (Wininet. h)
description: Las funciones WinINet devuelven códigos de error cuando corresponda. Los errores siguientes son específicos de las funciones de WinINet.
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151212"
---
# <a name="error-messages-winineth"></a><span data-ttu-id="3e25c-104">Mensajes de error (Wininet. h)</span><span class="sxs-lookup"><span data-stu-id="3e25c-104">Error Messages (Wininet.h)</span></span>

<span data-ttu-id="3e25c-105">Las funciones WinINet devuelven códigos de error cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="3e25c-105">The WinINet functions return error codes where appropriate.</span></span> <span data-ttu-id="3e25c-106">Los errores siguientes son específicos de las funciones de WinINet.</span><span class="sxs-lookup"><span data-stu-id="3e25c-106">The following errors are specific to the WinINet functions.</span></span>

<dl> <dt>

<span data-ttu-id="3e25c-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERROR de \_ FTP \_ eliminado**</span><span class="sxs-lookup"><span data-stu-id="3e25c-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERROR\_FTP\_DROPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-108">12111</span><span class="sxs-lookup"><span data-stu-id="3e25c-108">12111</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-109">No se completó la operación FTP porque se anuló la sesión.</span><span class="sxs-lookup"><span data-stu-id="3e25c-109">The FTP operation was not completed because the session was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERROR \_ FTP \_ no \_ \_ modo pasivo**</span><span class="sxs-lookup"><span data-stu-id="3e25c-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERROR\_FTP\_NO\_PASSIVE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-111">12112</span><span class="sxs-lookup"><span data-stu-id="3e25c-111">12112</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-112">El modo pasivo no está disponible en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3e25c-112">Passive mode is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERROR \_ \_ en la transferencia FTP \_ en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="3e25c-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERROR\_FTP\_TRANSFER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-114">12110</span><span class="sxs-lookup"><span data-stu-id="3e25c-114">12110</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-115">No se puede realizar la operación solicitada en el identificador de sesión FTP porque ya hay una operación en curso.</span><span class="sxs-lookup"><span data-stu-id="3e25c-115">The requested operation cannot be made on the FTP session handle because an operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**\_ \_ \_ no \_ se encontró el atributo Gopher de error**</span><span class="sxs-lookup"><span data-stu-id="3e25c-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERROR\_GOPHER\_ATTRIBUTE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-117">12137</span><span class="sxs-lookup"><span data-stu-id="3e25c-117">12137</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-118">No se pudo encontrar el atributo solicitado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-118">The requested attribute could not be located.</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-119">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3e25c-119">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**error \_ de \_ datos de Gopher \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**ERROR\_GOPHER\_DATA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-121">12132</span><span class="sxs-lookup"><span data-stu-id="3e25c-121">12132</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-122">Se detectó un error al recibir datos del servidor gopher.</span><span class="sxs-lookup"><span data-stu-id="3e25c-122">An error was detected while receiving data from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-123">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3e25c-123">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERROR \_ \_ de fin \_ de \_ datos de Gopher**</span><span class="sxs-lookup"><span data-stu-id="3e25c-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERROR\_GOPHER\_END\_OF\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-125">12133</span><span class="sxs-lookup"><span data-stu-id="3e25c-125">12133</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-126">Se ha alcanzado el final de los datos.</span><span class="sxs-lookup"><span data-stu-id="3e25c-126">The end of the data has been reached.</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-127">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3e25c-127">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERROR \_ de \_ \_ tipo de localizador incorrecto de Gopher \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERROR\_GOPHER\_INCORRECT\_LOCATOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-129">12135</span><span class="sxs-lookup"><span data-stu-id="3e25c-129">12135</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-130">El tipo del localizador no es correcto para esta operación.</span><span class="sxs-lookup"><span data-stu-id="3e25c-130">The type of the locator is not correct for this operation.</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-131">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3e25c-131">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERROR \_ de \_ localizador Gopher no válido \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERROR\_GOPHER\_INVALID\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-133">12134</span><span class="sxs-lookup"><span data-stu-id="3e25c-133">12134</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-134">El localizador proporcionado no es válido.</span><span class="sxs-lookup"><span data-stu-id="3e25c-134">The supplied locator is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-135">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3e25c-135">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERROR: \_ Gopher no es un \_ \_ archivo**</span><span class="sxs-lookup"><span data-stu-id="3e25c-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERROR\_GOPHER\_NOT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-137">12131</span><span class="sxs-lookup"><span data-stu-id="3e25c-137">12131</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-138">La solicitud se debe realizar para un localizador de archivos.</span><span class="sxs-lookup"><span data-stu-id="3e25c-138">The request must be made for a file locator.</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-139">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3e25c-139">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERROR \_ Gopher \_ no \_ Gopher \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="3e25c-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERROR\_GOPHER\_NOT\_GOPHER\_PLUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-141">12136</span><span class="sxs-lookup"><span data-stu-id="3e25c-141">12136</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-142">La operación solicitada solo se puede realizar en un servidor gopher + o con un localizador que especifique una operación Gopher +.</span><span class="sxs-lookup"><span data-stu-id="3e25c-142">The requested operation can be made only against a Gopher+ server, or with a locator that specifies a Gopher+ operation.</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-143">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3e25c-143">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**error \_ de \_ Protocolo \_ Gopher**</span><span class="sxs-lookup"><span data-stu-id="3e25c-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**ERROR\_GOPHER\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-145">12130</span><span class="sxs-lookup"><span data-stu-id="3e25c-145">12130</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-146">Se detectó un error al analizar los datos devueltos desde el servidor gopher.</span><span class="sxs-lookup"><span data-stu-id="3e25c-146">An error was detected while parsing data returned from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-147">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3e25c-147">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**\_localizador de error Gopher \_ desconocido \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERROR\_GOPHER\_UNKNOWN\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-149">12138</span><span class="sxs-lookup"><span data-stu-id="3e25c-149">12138</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-150">Se desconoce el tipo de localizador.</span><span class="sxs-lookup"><span data-stu-id="3e25c-150">The locator type is unknown.</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-151">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3e25c-151">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERROR \_ de \_ cookie HTTP \_ rechazada**</span><span class="sxs-lookup"><span data-stu-id="3e25c-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERROR\_HTTP\_COOKIE\_DECLINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-153">12162</span><span class="sxs-lookup"><span data-stu-id="3e25c-153">12162</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-154">El servidor rechazó la cookie HTTP.</span><span class="sxs-lookup"><span data-stu-id="3e25c-154">The HTTP cookie was declined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERROR \_ la \_ cookie HTTP \_ requiere \_ confirmación**</span><span class="sxs-lookup"><span data-stu-id="3e25c-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERROR\_HTTP\_COOKIE\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-156">12161</span><span class="sxs-lookup"><span data-stu-id="3e25c-156">12161</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-157">La cookie HTTP requiere confirmación.</span><span class="sxs-lookup"><span data-stu-id="3e25c-157">The HTTP cookie requires confirmation.</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-158">Windows Vista y Windows Server 2008 y versiones anteriores solo.</span><span class="sxs-lookup"><span data-stu-id="3e25c-158">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERROR \_ de \_ servidor de nivel inferior http \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERROR\_HTTP\_DOWNLEVEL\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-160">12151</span><span class="sxs-lookup"><span data-stu-id="3e25c-160">12151</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-161">El servidor no devolvió ningún encabezado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-161">The server did not return any headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**el \_ encabezado HTTP de error \_ \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="3e25c-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**ERROR\_HTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-163">12155</span><span class="sxs-lookup"><span data-stu-id="3e25c-163">12155</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-164">No se pudo agregar el encabezado porque ya existe.</span><span class="sxs-lookup"><span data-stu-id="3e25c-164">The header could not be added because it already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**\_ \_ \_ no \_ se encontró el encabezado HTTP de error**</span><span class="sxs-lookup"><span data-stu-id="3e25c-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**ERROR\_HTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-166">12150</span><span class="sxs-lookup"><span data-stu-id="3e25c-166">12150</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-167">No se pudo encontrar el encabezado solicitado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-167">The requested header could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERROR en el \_ \_ encabezado HTTP no válido \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERROR\_HTTP\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-169">12153</span><span class="sxs-lookup"><span data-stu-id="3e25c-169">12153</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-170">El encabezado proporcionado no es válido.</span><span class="sxs-lookup"><span data-stu-id="3e25c-170">The supplied header is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERROR \_ de \_ \_ solicitud de consulta no válida http \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERROR\_HTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-172">12154</span><span class="sxs-lookup"><span data-stu-id="3e25c-172">12154</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-173">La solicitud realizada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) no es válida.</span><span class="sxs-lookup"><span data-stu-id="3e25c-173">The request made to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERROR \_ de \_ \_ respuesta del servidor HTTP no válida \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERROR\_HTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-175">12152</span><span class="sxs-lookup"><span data-stu-id="3e25c-175">12152</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-176">No se pudo analizar la respuesta del servidor.</span><span class="sxs-lookup"><span data-stu-id="3e25c-176">The server response could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERROR \_ \_ no \_ Redirigido http**</span><span class="sxs-lookup"><span data-stu-id="3e25c-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERROR\_HTTP\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-178">12160</span><span class="sxs-lookup"><span data-stu-id="3e25c-178">12160</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-179">No se redirigió la solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="3e25c-179">The HTTP request was not redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERROR \_ de \_ redirección \_ http**</span><span class="sxs-lookup"><span data-stu-id="3e25c-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERROR\_HTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-181">12156</span><span class="sxs-lookup"><span data-stu-id="3e25c-181">12156</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-182">Se produjo un error en el redireccionamiento porque el esquema ha cambiado (por ejemplo, HTTP a FTP) o todos los intentos de redirigir el error (el valor predeterminado es cinco intentos).</span><span class="sxs-lookup"><span data-stu-id="3e25c-182">The redirection failed because either the scheme changed (for example, HTTP to FTP) or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERROR \_ el \_ redireccionamiento http \_ necesita \_ confirmación**</span><span class="sxs-lookup"><span data-stu-id="3e25c-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERROR\_HTTP\_REDIRECT\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-184">12168</span><span class="sxs-lookup"><span data-stu-id="3e25c-184">12168</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-185">La redirección requiere confirmación del usuario.</span><span class="sxs-lookup"><span data-stu-id="3e25c-185">The redirection requires user confirmation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERROR \_ de \_ \_ subproceso asincrónico de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERROR\_INTERNET\_ASYNC\_THREAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-187">12047</span><span class="sxs-lookup"><span data-stu-id="3e25c-187">12047</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-188">La aplicación no pudo iniciar un subproceso asincrónico.</span><span class="sxs-lookup"><span data-stu-id="3e25c-188">The application could not start an asynchronous thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERROR en el \_ \_ \_ script de proxy automático incorrecto \_ \_ de Internet**</span><span class="sxs-lookup"><span data-stu-id="3e25c-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERROR\_INTERNET\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-190">12166</span><span class="sxs-lookup"><span data-stu-id="3e25c-190">12166</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-191">Se produjo un error en el script de configuración automática del proxy.</span><span class="sxs-lookup"><span data-stu-id="3e25c-191">There was an error in the automatic proxy configuration script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERROR \_ de \_ \_ longitud de opción incorrecta de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERROR\_INTERNET\_BAD\_OPTION\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-193">12010</span><span class="sxs-lookup"><span data-stu-id="3e25c-193">12010</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-194">La longitud de una opción proporcionada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) no es correcta para el tipo de opción especificada.</span><span class="sxs-lookup"><span data-stu-id="3e25c-194">The length of an option supplied to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) is incorrect for the type of option specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**\_parámetro de \_ error \_ del registro de Internet incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERROR\_INTERNET\_BAD\_REGISTRY\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-196">12022</span><span class="sxs-lookup"><span data-stu-id="3e25c-196">12022</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-197">Se encontró un valor de registro necesario, pero es de un tipo incorrecto o tiene un valor no válido.</span><span class="sxs-lookup"><span data-stu-id="3e25c-197">A required registry value was located but is an incorrect type or has an invalid value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERROR \_ Internet \_ no se puede \_ conectar**</span><span class="sxs-lookup"><span data-stu-id="3e25c-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERROR\_INTERNET\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-199">12029</span><span class="sxs-lookup"><span data-stu-id="3e25c-199">12029</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-200">Error al intentar conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="3e25c-200">The attempt to connect to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERROR el \_ envío de correo de Internet \_ \_ \_ \_ no es \_ seguro**</span><span class="sxs-lookup"><span data-stu-id="3e25c-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERROR\_INTERNET\_CHG\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-202">12042</span><span class="sxs-lookup"><span data-stu-id="3e25c-202">12042</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-203">La aplicación está publicando e intentando cambiar varias líneas de texto en un servidor que no es seguro.</span><span class="sxs-lookup"><span data-stu-id="3e25c-203">The application is posting and attempting to change multiple lines of text on a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERROR \_ de \_ certificado de autenticación de cliente de Internet \_ \_ \_ necesario**</span><span class="sxs-lookup"><span data-stu-id="3e25c-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-205">12044</span><span class="sxs-lookup"><span data-stu-id="3e25c-205">12044</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-206">El servidor está solicitando la autenticación del cliente.</span><span class="sxs-lookup"><span data-stu-id="3e25c-206">The server is requesting client authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERROR \_ \_ no se \_ \_ ha \_ configurado la autenticación de cliente de Internet**</span><span class="sxs-lookup"><span data-stu-id="3e25c-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_NOT\_SETUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-208">12046</span><span class="sxs-lookup"><span data-stu-id="3e25c-208">12046</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-209">La autorización del cliente no está configurada en este equipo.</span><span class="sxs-lookup"><span data-stu-id="3e25c-209">Client authorization is not set up on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERROR \_ de \_ conexión a Internet \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="3e25c-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERROR\_INTERNET\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-211">12030</span><span class="sxs-lookup"><span data-stu-id="3e25c-211">12030</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-212">La conexión con el servidor ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-212">The connection with the server has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERROR \_ de \_ restablecimiento de conexión a Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERROR\_INTERNET\_CONNECTION\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-214">12031</span><span class="sxs-lookup"><span data-stu-id="3e25c-214">12031</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-215">Se ha restablecido la conexión con el servidor.</span><span class="sxs-lookup"><span data-stu-id="3e25c-215">The connection with the server has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERROR \_ de \_ descodificación de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERROR\_INTERNET\_DECODING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-217">12175</span><span class="sxs-lookup"><span data-stu-id="3e25c-217">12175</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-218">WinINet no pudo realizar la descodificación de contenido en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e25c-218">WinINet failed to perform content decoding on the response.</span></span> <span data-ttu-id="3e25c-219">Para obtener más información, vea el tema sobre [**codificación de contenido**](content-encoding.md) .</span><span class="sxs-lookup"><span data-stu-id="3e25c-219">For more information, see the [**Content Encoding**](content-encoding.md) topic.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**ERROR en el \_ cuadro de diálogo de Internet \_ \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="3e25c-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**ERROR\_INTERNET\_DIALOG\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-221">12049</span><span class="sxs-lookup"><span data-stu-id="3e25c-221">12049</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-222">Otro subproceso tiene un cuadro de diálogo de contraseña en curso.</span><span class="sxs-lookup"><span data-stu-id="3e25c-222">Another thread has a password dialog box in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERROR de \_ Internet \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="3e25c-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERROR\_INTERNET\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-224">12163</span><span class="sxs-lookup"><span data-stu-id="3e25c-224">12163</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-225">Se perdió la conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="3e25c-225">The Internet connection has been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**error de error \_ extendido de Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**ERROR\_INTERNET\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-227">12003</span><span class="sxs-lookup"><span data-stu-id="3e25c-227">12003</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-228">Se devolvió un error extendido desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="3e25c-228">An extended error was returned from the server.</span></span> <span data-ttu-id="3e25c-229">Suele ser una cadena o un búfer que contiene un mensaje de error detallado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-229">This is typically a string or buffer containing a verbose error message.</span></span> <span data-ttu-id="3e25c-230">Llame a [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) para recuperar el texto del error.</span><span class="sxs-lookup"><span data-stu-id="3e25c-230">Call [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) to retrieve the error text.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERROR \_ de \_ Internet \_ DUETOSECURITYCHECK**</span><span class="sxs-lookup"><span data-stu-id="3e25c-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERROR\_INTERNET\_FAILED\_DUETOSECURITYCHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-232">12171</span><span class="sxs-lookup"><span data-stu-id="3e25c-232">12171</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-233">Error de la función debido a una comprobación de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3e25c-233">The function failed due to a security check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERROR \_ de \_ reintento de Internet Force \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERROR\_INTERNET\_FORCE\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-235">12032</span><span class="sxs-lookup"><span data-stu-id="3e25c-235">12032</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-236">La función debe rehacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3e25c-236">The function needs to redo the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERROR \_ de \_ Inicio de sesión de Fortezza de Internet \_ \_ necesario**</span><span class="sxs-lookup"><span data-stu-id="3e25c-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERROR\_INTERNET\_FORTEZZA\_LOGIN\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-238">12054</span><span class="sxs-lookup"><span data-stu-id="3e25c-238">12054</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-239">El recurso solicitado requiere autenticación Fortezza.</span><span class="sxs-lookup"><span data-stu-id="3e25c-239">The requested resource requires Fortezza authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERROR \_ el \_ identificador de Internet \_ existe**</span><span class="sxs-lookup"><span data-stu-id="3e25c-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERROR\_INTERNET\_HANDLE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-241">12036</span><span class="sxs-lookup"><span data-stu-id="3e25c-241">12036</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-242">No se pudo realizar la solicitud porque el identificador ya existe.</span><span class="sxs-lookup"><span data-stu-id="3e25c-242">The request failed because the handle already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERROR \_ de Internet de \_ http \_ a \_ https \_ en \_ redir**</span><span class="sxs-lookup"><span data-stu-id="3e25c-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-244">12039</span><span class="sxs-lookup"><span data-stu-id="3e25c-244">12039</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-245">La aplicación se mueve de una conexión que no es SSL a una conexión SSL debido a una redirección.</span><span class="sxs-lookup"><span data-stu-id="3e25c-245">The application is moving from a non-SSL to an SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERROR \_ de \_ envío de http de \_ envío http de HTTPS de \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERROR\_INTERNET\_HTTPS\_HTTP\_SUBMIT\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-247">12052</span><span class="sxs-lookup"><span data-stu-id="3e25c-247">12052</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-248">Los datos que se envían a una conexión SSL se redirigen a una conexión que no es SSL.</span><span class="sxs-lookup"><span data-stu-id="3e25c-248">The data being submitted to an SSL connection is being redirected to a non-SSL connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERROR \_ \_ de Internet HTTPS \_ a \_ http \_ en \_ redir**</span><span class="sxs-lookup"><span data-stu-id="3e25c-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-250">12040</span><span class="sxs-lookup"><span data-stu-id="3e25c-250">12040</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-251">La aplicación se mueve de un SSL a una conexión que no es SSL debido a una redirección.</span><span class="sxs-lookup"><span data-stu-id="3e25c-251">The application is moving from an SSL to an non-SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERROR de Internet con un \_ \_ \_ formato incorrecto**</span><span class="sxs-lookup"><span data-stu-id="3e25c-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERROR\_INTERNET\_INCORRECT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-253">12027</span><span class="sxs-lookup"><span data-stu-id="3e25c-253">12027</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-254">El formato de la solicitud no es válido.</span><span class="sxs-lookup"><span data-stu-id="3e25c-254">The format of the request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERROR \_ de \_ \_ Estado de identificador incorrecto de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-256">12019</span><span class="sxs-lookup"><span data-stu-id="3e25c-256">12019</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-257">No se puede realizar la operación solicitada porque el identificador proporcionado no tiene el estado correcto.</span><span class="sxs-lookup"><span data-stu-id="3e25c-257">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERROR \_ de \_ \_ tipo de identificador incorrecto de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-259">12018</span><span class="sxs-lookup"><span data-stu-id="3e25c-259">12018</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-260">El tipo de identificador proporcionado no es correcto para esta operación.</span><span class="sxs-lookup"><span data-stu-id="3e25c-260">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERROR de \_ Internet: \_ \_ contraseña incorrecta**</span><span class="sxs-lookup"><span data-stu-id="3e25c-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERROR\_INTERNET\_INCORRECT\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-262">12014</span><span class="sxs-lookup"><span data-stu-id="3e25c-262">12014</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-263">No se pudo completar la solicitud de conexión e inicio de sesión en un servidor FTP porque la contraseña proporcionada es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="3e25c-263">The request to connect and log on to an FTP server could not be completed because the supplied password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERROR \_ de \_ \_ nombre de usuario incorrecto de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERROR\_INTERNET\_INCORRECT\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-265">12013</span><span class="sxs-lookup"><span data-stu-id="3e25c-265">12013</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-266">No se pudo completar la solicitud de conexión e inicio de sesión en un servidor FTP porque el nombre de usuario proporcionado no es correcto.</span><span class="sxs-lookup"><span data-stu-id="3e25c-266">The request to connect and log on to an FTP server could not be completed because the supplied user name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERROR de \_ Internet \_ Insert \_ CDROM**</span><span class="sxs-lookup"><span data-stu-id="3e25c-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERROR\_INTERNET\_INSERT\_CDROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-268">12053</span><span class="sxs-lookup"><span data-stu-id="3e25c-268">12053</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-269">La solicitud requiere que se inserte un CD-ROM en la unidad de CD-ROM para localizar el recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-269">The request requires a CD-ROM to be inserted in the CD-ROM drive to locate the resource requested.</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-270">Windows Vista y Windows Server 2008 y versiones anteriores solo.</span><span class="sxs-lookup"><span data-stu-id="3e25c-270">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**error interno de ERROR de \_ Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**ERROR\_INTERNET\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-272">12004</span><span class="sxs-lookup"><span data-stu-id="3e25c-272">12004</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-273">Se ha producido un error interno.</span><span class="sxs-lookup"><span data-stu-id="3e25c-273">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERROR \_ de \_ CA no válida de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERROR\_INTERNET\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-275">12045</span><span class="sxs-lookup"><span data-stu-id="3e25c-275">12045</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-276">La función no está familiarizada con la entidad de certificación que generó el certificado del servidor.</span><span class="sxs-lookup"><span data-stu-id="3e25c-276">The function is unfamiliar with the Certificate Authority that generated the server's certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERROR en una \_ \_ operación no válida de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERROR\_INTERNET\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-278">12016</span><span class="sxs-lookup"><span data-stu-id="3e25c-278">12016</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-279">La operación solicitada no es válida.</span><span class="sxs-lookup"><span data-stu-id="3e25c-279">The requested operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERROR \_ de \_ opción no válida de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERROR\_INTERNET\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-281">12009</span><span class="sxs-lookup"><span data-stu-id="3e25c-281">12009</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-282">Una solicitud a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) especificó un valor de opción no válido.</span><span class="sxs-lookup"><span data-stu-id="3e25c-282">A request to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERROR \_ de \_ \_ solicitud de proxy no válida de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERROR\_INTERNET\_INVALID\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-284">12033</span><span class="sxs-lookup"><span data-stu-id="3e25c-284">12033</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-285">La solicitud al proxy no era válida.</span><span class="sxs-lookup"><span data-stu-id="3e25c-285">The request to the proxy was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERROR \_ de \_ dirección URL no válida de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERROR\_INTERNET\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-287">12005</span><span class="sxs-lookup"><span data-stu-id="3e25c-287">12005</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-288">La dirección URL no es válida.</span><span class="sxs-lookup"><span data-stu-id="3e25c-288">The URL is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERROR \_ \_ \_ no \_ se encontró el elemento de Internet**</span><span class="sxs-lookup"><span data-stu-id="3e25c-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERROR\_INTERNET\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-290">12028</span><span class="sxs-lookup"><span data-stu-id="3e25c-290">12028</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-291">No se encontró el elemento solicitado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-291">The requested item could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERROR \_ de \_ Inicio de sesión en Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-293">12015</span><span class="sxs-lookup"><span data-stu-id="3e25c-293">12015</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-294">Error en la solicitud de conexión e inicio de sesión en un servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="3e25c-294">The request to connect and log on to an FTP server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERROR de \_ Inicio de sesión en Internet \_ \_ \_ Mostrar \_ cuerpo de entidad \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-296">12174</span><span class="sxs-lookup"><span data-stu-id="3e25c-296">12174</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-297">El encabezado de Resumen de MS-Logoff se ha devuelto desde el sitio Web.</span><span class="sxs-lookup"><span data-stu-id="3e25c-297">The MS-Logoff digest header has been returned from the website.</span></span> <span data-ttu-id="3e25c-298">Este encabezado indica específicamente el paquete de síntesis para purgar las credenciales del territorio asociado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-298">This header specifically instructs the digest package to purge credentials for the associated realm.</span></span> <span data-ttu-id="3e25c-299">Este error solo se devolverá si se ha establecido la opción error de [Inicio de sesión para mostrar el \_ \_ \_ \_ \_ \_ \_ cuerpo](option-flags.md) de la entidad en Internet. de lo contrario, se devolverá **un error de \_ Inicio de \_ sesión \_ de Internet** .</span><span class="sxs-lookup"><span data-stu-id="3e25c-299">This error will only be returned if [INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY](option-flags.md) option has been set; otherwise, **ERROR\_INTERNET\_LOGIN\_FAILURE** is returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERROR \_ de \_ seguridad mixta de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERROR\_INTERNET\_MIXED\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-301">12041</span><span class="sxs-lookup"><span data-stu-id="3e25c-301">12041</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-302">El contenido no es totalmente seguro.</span><span class="sxs-lookup"><span data-stu-id="3e25c-302">The content is not entirely secure.</span></span> <span data-ttu-id="3e25c-303">Es posible que parte del contenido que se está viendo proviene de servidores no seguros.</span><span class="sxs-lookup"><span data-stu-id="3e25c-303">Some of the content being viewed may have come from unsecured servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERROR \_ de \_ nombre de Internet \_ no \_ resuelto**</span><span class="sxs-lookup"><span data-stu-id="3e25c-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERROR\_INTERNET\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-305">12007</span><span class="sxs-lookup"><span data-stu-id="3e25c-305">12007</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-306">No se pudo resolver el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="3e25c-306">The server name could not be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERROR de \_ Internet: \_ \_ \_ paquete SSPI de MSN \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERROR\_INTERNET\_NEED\_MSN\_SSPI\_PKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-308">12173</span><span class="sxs-lookup"><span data-stu-id="3e25c-308">12173</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-309">No implementado actualmente.</span><span class="sxs-lookup"><span data-stu-id="3e25c-309">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERROR de Internet con la \_ \_ interfaz de \_ usuario**</span><span class="sxs-lookup"><span data-stu-id="3e25c-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERROR\_INTERNET\_NEED\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-311">12034</span><span class="sxs-lookup"><span data-stu-id="3e25c-311">12034</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-312">Se ha solicitado una interfaz de usuario u otra operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="3e25c-312">A user interface or other blocking operation has been requested.</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-313">Windows Vista y Windows Server 2008 y versiones anteriores solo.</span><span class="sxs-lookup"><span data-stu-id="3e25c-313">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERROR de \_ Internet \_ sin devolución de \_ llamada**</span><span class="sxs-lookup"><span data-stu-id="3e25c-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERROR\_INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-315">12025</span><span class="sxs-lookup"><span data-stu-id="3e25c-315">12025</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-316">No se pudo realizar una solicitud asincrónica porque no se ha establecido una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3e25c-316">An asynchronous request could not be made because a callback function has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERROR de \_ Internet \_ sin \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="3e25c-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERROR\_INTERNET\_NO\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-318">12024</span><span class="sxs-lookup"><span data-stu-id="3e25c-318">12024</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-319">No se pudo realizar una solicitud asincrónica porque se proporcionó un valor de contexto cero.</span><span class="sxs-lookup"><span data-stu-id="3e25c-319">An asynchronous request could not be made because a zero context value was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERROR \_ de \_ Internet \_ sin \_ acceso directo**</span><span class="sxs-lookup"><span data-stu-id="3e25c-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERROR\_INTERNET\_NO\_DIRECT\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-321">12023</span><span class="sxs-lookup"><span data-stu-id="3e25c-321">12023</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-322">No se puede realizar el acceso directo a la red en este momento.</span><span class="sxs-lookup"><span data-stu-id="3e25c-322">Direct network access cannot be made at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERROR \_ Internet \_ no \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="3e25c-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERROR\_INTERNET\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-324">12172</span><span class="sxs-lookup"><span data-stu-id="3e25c-324">12172</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-325">No se ha producido la inicialización de la API WinINet.</span><span class="sxs-lookup"><span data-stu-id="3e25c-325">Initialization of the WinINet API has not occurred.</span></span> <span data-ttu-id="3e25c-326">Indica que aún no se ha llamado a una función de nivel superior, como [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="3e25c-326">Indicates that a higher-level function, such as [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), has not been called yet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERROR \_ de \_ \_ solicitud de proxy \_ de Internet**</span><span class="sxs-lookup"><span data-stu-id="3e25c-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERROR\_INTERNET\_NOT\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-328">12020</span><span class="sxs-lookup"><span data-stu-id="3e25c-328">12020</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-329">No se puede realizar la solicitud a través de un proxy.</span><span class="sxs-lookup"><span data-stu-id="3e25c-329">The request cannot be made via a proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERROR \_ de \_ operación de Internet \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="3e25c-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERROR\_INTERNET\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-331">12017</span><span class="sxs-lookup"><span data-stu-id="3e25c-331">12017</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-332">La operación se canceló, normalmente porque el identificador en el que estaba funcionando la solicitud se cerró antes de que se completara la operación.</span><span class="sxs-lookup"><span data-stu-id="3e25c-332">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERROR \_ de \_ opción de Internet \_ no \_ configurable**</span><span class="sxs-lookup"><span data-stu-id="3e25c-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERROR\_INTERNET\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-334">12011</span><span class="sxs-lookup"><span data-stu-id="3e25c-334">12011</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-335">No se puede establecer la opción solicitada, solo se consulta.</span><span class="sxs-lookup"><span data-stu-id="3e25c-335">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERROR \_ \_ de Internet \_ sin \_ identificadores**</span><span class="sxs-lookup"><span data-stu-id="3e25c-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERROR\_INTERNET\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-337">12001</span><span class="sxs-lookup"><span data-stu-id="3e25c-337">12001</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-338">No se pueden generar más identificadores en este momento.</span><span class="sxs-lookup"><span data-stu-id="3e25c-338">No more handles could be generated at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERROR: la \_ publicación en Internet \_ \_ \_ no es \_ segura**</span><span class="sxs-lookup"><span data-stu-id="3e25c-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-340">12043</span><span class="sxs-lookup"><span data-stu-id="3e25c-340">12043</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-341">La aplicación está publicando datos en un servidor que no es seguro.</span><span class="sxs-lookup"><span data-stu-id="3e25c-341">The application is posting data to a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERROR \_ de \_ Protocolo de Internet \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="3e25c-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERROR\_INTERNET\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-343">12008</span><span class="sxs-lookup"><span data-stu-id="3e25c-343">12008</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-344">No se pudo encontrar el protocolo solicitado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-344">The requested protocol could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERROR no se \_ \_ \_ \_ puede tener acceso al servidor proxy de Internet**</span><span class="sxs-lookup"><span data-stu-id="3e25c-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERROR\_INTERNET\_PROXY\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-346">12165</span><span class="sxs-lookup"><span data-stu-id="3e25c-346">12165</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-347">No se puede establecer contacto con el servidor proxy designado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-347">The designated proxy server cannot be reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERROR \_ de \_ cambio de esquema de redirección de Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERROR\_INTERNET\_REDIRECT\_SCHEME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-349">12048</span><span class="sxs-lookup"><span data-stu-id="3e25c-349">12048</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-350">La función no pudo controlar el redireccionamiento porque el esquema ha cambiado (por ejemplo, HTTP a FTP).</span><span class="sxs-lookup"><span data-stu-id="3e25c-350">The function could not handle the redirection, because the scheme changed (for example, HTTP to FTP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró el valor del registro de Internet**</span><span class="sxs-lookup"><span data-stu-id="3e25c-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERROR\_INTERNET\_REGISTRY\_VALUE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-352">12021</span><span class="sxs-lookup"><span data-stu-id="3e25c-352">12021</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-353">No se pudo encontrar un valor del registro requerido.</span><span class="sxs-lookup"><span data-stu-id="3e25c-353">A required registry value could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**ERROR \_ de \_ solicitud de Internet \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="3e25c-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**ERROR\_INTERNET\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-355">12026</span><span class="sxs-lookup"><span data-stu-id="3e25c-355">12026</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-356">No se pudo completar la operación necesaria porque una o varias solicitudes están pendientes.</span><span class="sxs-lookup"><span data-stu-id="3e25c-356">The required operation could not be completed because one or more requests are pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**cuadro de diálogo ERROR de \_ \_ reintento de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**ERROR\_INTERNET\_RETRY\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-358">12050</span><span class="sxs-lookup"><span data-stu-id="3e25c-358">12050</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-359">Se debe reintentar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3e25c-359">The dialog box should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERROR \_ de \_ \_ certificado CN de Internet \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="3e25c-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-361">12038</span><span class="sxs-lookup"><span data-stu-id="3e25c-361">12038</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-362">El nombre común del certificado SSL (campo Nombre de host) es incorrecto por ejemplo, si escribió www.server.com y el nombre común en el certificado indica www.different.com.</span><span class="sxs-lookup"><span data-stu-id="3e25c-362">SSL certificate common name (host name field) is incorrect for example, if you entered www.server.com and the common name on the certificate says www.different.com.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERROR la \_ fecha de certificado de Internet \_ s \_ \_ \_ no es válida**</span><span class="sxs-lookup"><span data-stu-id="3e25c-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-364">12037</span><span class="sxs-lookup"><span data-stu-id="3e25c-364">12037</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-365">La fecha del certificado SSL que se recibió del servidor es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="3e25c-365">SSL certificate date that was received from the server is bad.</span></span> <span data-ttu-id="3e25c-366">El certificado ha expirado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-366">The certificate is expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**errores de certificado de ERROR de \_ Internet \_ s \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-368">12055</span><span class="sxs-lookup"><span data-stu-id="3e25c-368">12055</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-369">El certificado SSL contiene errores.</span><span class="sxs-lookup"><span data-stu-id="3e25c-369">The SSL certificate contains errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERROR de Internet en el \_ \_ \_ certificado. \_ no \_ Rev**</span><span class="sxs-lookup"><span data-stu-id="3e25c-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERROR\_INTERNET\_SEC\_CERT\_NO\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-371">12056</span><span class="sxs-lookup"><span data-stu-id="3e25c-371">12056</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-372">No se revocó el certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="3e25c-372">The SSL certificate was not revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERROR de ERROR de \_ revisión de certificado por Internet \_ s \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERROR\_INTERNET\_SEC\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-374">12057</span><span class="sxs-lookup"><span data-stu-id="3e25c-374">12057</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-375">No se pudo revocar el certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="3e25c-375">Revocation of the SSL certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERROR \_ Internet \_ s \_ certificado \_ revocado**</span><span class="sxs-lookup"><span data-stu-id="3e25c-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERROR\_INTERNET\_SEC\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-377">12170</span><span class="sxs-lookup"><span data-stu-id="3e25c-377">12170</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-378">Se revocó el certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="3e25c-378">The SSL certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERROR en \_ Internet: \_ \_ certificado no válido \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERROR\_INTERNET\_SEC\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-380">12169</span><span class="sxs-lookup"><span data-stu-id="3e25c-380">12169</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-381">El certificado SSL no es válido.</span><span class="sxs-lookup"><span data-stu-id="3e25c-381">The SSL certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**error \_ de \_ canal de seguridad de Internet error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**ERROR\_INTERNET\_SECURITY\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-383">12157</span><span class="sxs-lookup"><span data-stu-id="3e25c-383">12157</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-384">La aplicación experimentó un error interno al cargar las bibliotecas SSL.</span><span class="sxs-lookup"><span data-stu-id="3e25c-384">The application experienced an internal error loading the SSL libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERROR \_ de \_ servidor de Internet \_ inaccesible**</span><span class="sxs-lookup"><span data-stu-id="3e25c-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERROR\_INTERNET\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-386">12164</span><span class="sxs-lookup"><span data-stu-id="3e25c-386">12164</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-387">No se puede tener acceso al sitio web o servidor indicado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-387">The website or server indicated is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERROR \_ de \_ apagado por Internet**</span><span class="sxs-lookup"><span data-stu-id="3e25c-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERROR\_INTERNET\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-389">12012</span><span class="sxs-lookup"><span data-stu-id="3e25c-389">12012</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-390">La compatibilidad con WinINet se está cerrando o descargando.</span><span class="sxs-lookup"><span data-stu-id="3e25c-390">WinINet support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERROR de \_ Internet \_ TCPIP \_ no \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="3e25c-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERROR\_INTERNET\_TCPIP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-392">12159</span><span class="sxs-lookup"><span data-stu-id="3e25c-392">12159</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-393">La pila de protocolos necesaria no está cargada y la aplicación no puede iniciar WinSock.</span><span class="sxs-lookup"><span data-stu-id="3e25c-393">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**ERROR \_ de \_ tiempo de espera de Internet**</span><span class="sxs-lookup"><span data-stu-id="3e25c-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**ERROR\_INTERNET\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-395">12002</span><span class="sxs-lookup"><span data-stu-id="3e25c-395">12002</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-396">La solicitud ha agotado el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="3e25c-396">The request has timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERROR: \_ Internet \_ no puede \_ almacenar en caché el \_ \_ archivo**</span><span class="sxs-lookup"><span data-stu-id="3e25c-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERROR\_INTERNET\_UNABLE\_TO\_CACHE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-398">12158</span><span class="sxs-lookup"><span data-stu-id="3e25c-398">12158</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-399">La función no pudo almacenar en caché el archivo.</span><span class="sxs-lookup"><span data-stu-id="3e25c-399">The function was unable to cache the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERROR \_ Internet \_ no se puede \_ \_ descargar el \_ script**</span><span class="sxs-lookup"><span data-stu-id="3e25c-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERROR\_INTERNET\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-401">12167</span><span class="sxs-lookup"><span data-stu-id="3e25c-401">12167</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-402">No se pudo descargar el script de configuración automática del proxy.</span><span class="sxs-lookup"><span data-stu-id="3e25c-402">The automatic proxy configuration script could not be downloaded.</span></span> <span data-ttu-id="3e25c-403">La marca de INTERNET \_ \_ debe \_ almacenar la marca de solicitud en caché \_ .</span><span class="sxs-lookup"><span data-stu-id="3e25c-403">The INTERNET\_FLAG\_MUST\_CACHE\_REQUEST flag was set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERROR \_ : \_ esquema desconocido de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="3e25c-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERROR\_INTERNET\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e25c-405">12006</span><span class="sxs-lookup"><span data-stu-id="3e25c-405">12006</span></span>
</dt> <dt>



<span data-ttu-id="3e25c-406">No se reconoció el esquema de la dirección URL o no se admite.</span><span class="sxs-lookup"><span data-stu-id="3e25c-406">The URL scheme could not be recognized, or is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR \_ de \_ identificador no válido**</span><span class="sxs-lookup"><span data-stu-id="3e25c-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3e25c-408">El identificador que se pasó a la API se ha invalidado o cerrado.</span><span class="sxs-lookup"><span data-stu-id="3e25c-408">The handle that was passed to the API has been either invalidated or closed.</span></span>

<span data-ttu-id="3e25c-409">**Encabezado:** Declarado en Winerror. h</span><span class="sxs-lookup"><span data-stu-id="3e25c-409">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR \_ más \_ datos**</span><span class="sxs-lookup"><span data-stu-id="3e25c-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3e25c-411">More data is available (Hyper-V no pudo generar el conjunto de instantáneas de VSS para la máquina virtual: hay más datos disponibles).</span><span class="sxs-lookup"><span data-stu-id="3e25c-411">More data is available.</span></span>

<span data-ttu-id="3e25c-412">**Encabezado:** Declarado en Winerror. h</span><span class="sxs-lookup"><span data-stu-id="3e25c-412">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR: \_ no hay \_ más \_ archivos**</span><span class="sxs-lookup"><span data-stu-id="3e25c-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3e25c-414">No se encontraron más archivos.</span><span class="sxs-lookup"><span data-stu-id="3e25c-414">No more files have been found.</span></span>

<span data-ttu-id="3e25c-415">**Encabezado:** Declarado en Winerror. h</span><span class="sxs-lookup"><span data-stu-id="3e25c-415">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e25c-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**\_no hay \_ más \_ elementos de error**</span><span class="sxs-lookup"><span data-stu-id="3e25c-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3e25c-417">No se han encontrado más elementos.</span><span class="sxs-lookup"><span data-stu-id="3e25c-417">No more items have been found.</span></span>

<span data-ttu-id="3e25c-418">**Encabezado:** Declarado en Winerror. h</span><span class="sxs-lookup"><span data-stu-id="3e25c-418">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e25c-419">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e25c-419">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3e25c-420">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="3e25c-420">WinINet does not support server implementations.</span></span> <span data-ttu-id="3e25c-421">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="3e25c-421">In addition, it should not be used from a service.</span></span> <span data-ttu-id="3e25c-422">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="3e25c-422">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3e25c-423">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e25c-423">Requirements</span></span>



| <span data-ttu-id="3e25c-424">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e25c-424">Requirement</span></span> | <span data-ttu-id="3e25c-425">Value</span><span class="sxs-lookup"><span data-stu-id="3e25c-425">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3e25c-426">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e25c-426">Minimum supported client</span></span><br/> | <span data-ttu-id="3e25c-427">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3e25c-427">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3e25c-428">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e25c-428">Minimum supported server</span></span><br/> | <span data-ttu-id="3e25c-429">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e25c-429">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3e25c-430">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e25c-430">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e25c-431"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e25c-431"><dt>Wininet.h</dt></span></span> </dl> |



 

