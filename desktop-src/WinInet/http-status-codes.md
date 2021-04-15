---
title: Códigos de Estado HTTP (Wininet. h)
description: La tabla siguiente contiene las constantes y los valores correspondientes para los códigos de Estado HTTP devueltos por los servidores en Internet.
ms.assetid: 28a5e889-c8f3-4996-a1ca-c48866fa59d7
topic_type:
- apiref
api_name:
- HTTP_STATUS_CONTINUE
- HTTP_STATUS_SWITCH_PROTOCOLS
- HTTP_STATUS_OK
- HTTP_STATUS_CREATED
- HTTP_STATUS_ACCEPTED
- HTTP_STATUS_PARTIAL
- HTTP_STATUS_NO_CONTENT
- HTTP_STATUS_RESET_CONTENT
- HTTP_STATUS_PARTIAL_CONTENT
- HTTP_STATUS_AMBIGUOUS
- HTTP_STATUS_MOVED
- HTTP_STATUS_REDIRECT
- HTTP_STATUS_REDIRECT_METHOD
- HTTP_STATUS_NOT_MODIFIED
- HTTP_STATUS_USE_PROXY
- HTTP_STATUS_REDIRECT_KEEP_VERB
- HTTP_STATUS_BAD_REQUEST
- HTTP_STATUS_DENIED
- HTTP_STATUS_PAYMENT_REQ
- HTTP_STATUS_FORBIDDEN
- HTTP_STATUS_NOT_FOUND
- HTTP_STATUS_BAD_METHOD
- HTTP_STATUS_NONE_ACCEPTABLE
- HTTP_STATUS_PROXY_AUTH_REQ
- HTTP_STATUS_REQUEST_TIMEOUT
- HTTP_STATUS_CONFLICT
- HTTP_STATUS_GONE
- HTTP_STATUS_LENGTH_REQUIRED
- HTTP_STATUS_PRECOND_FAILED
- HTTP_STATUS_REQUEST_TOO_LARGE
- HTTP_STATUS_URI_TOO_LONG
- HTTP_STATUS_UNSUPPORTED_MEDIA
- HTTP_STATUS_RETRY_WITH
- HTTP_STATUS_SERVER_ERROR
- HTTP_STATUS_NOT_SUPPORTED
- HTTP_STATUS_BAD_GATEWAY
- HTTP_STATUS_SERVICE_UNAVAIL
- HTTP_STATUS_GATEWAY_TIMEOUT
- HTTP_STATUS_VERSION_NOT_SUP
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6933617b0488e059c029dd783af238a3ddbb3ecb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422596"
---
# <a name="http-status-codes-winineth"></a><span data-ttu-id="e2995-103">Códigos de Estado HTTP (Wininet. h)</span><span class="sxs-lookup"><span data-stu-id="e2995-103">HTTP Status Codes (Wininet.h)</span></span>

<span data-ttu-id="e2995-104">La tabla siguiente contiene las constantes y los valores correspondientes para los códigos de Estado HTTP devueltos por los servidores en Internet.</span><span class="sxs-lookup"><span data-stu-id="e2995-104">The following table contains the constants and corresponding values for the HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="e2995-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**\_continuación de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-106">100</span><span class="sxs-lookup"><span data-stu-id="e2995-106">100</span></span>
</dt> <dt>



<span data-ttu-id="e2995-107">La solicitud puede continuar.</span><span class="sxs-lookup"><span data-stu-id="e2995-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_protocolos de \_ cambio de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-109">101</span><span class="sxs-lookup"><span data-stu-id="e2995-109">101</span></span>
</dt> <dt>



<span data-ttu-id="e2995-110">El servidor ha cambiado los protocolos en un encabezado de actualización.</span><span class="sxs-lookup"><span data-stu-id="e2995-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**\_Estado HTTP \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="e2995-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-112">200</span><span class="sxs-lookup"><span data-stu-id="e2995-112">200</span></span>
</dt> <dt>



<span data-ttu-id="e2995-113">La solicitud se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e2995-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**\_Estado HTTP \_ creado**</span><span class="sxs-lookup"><span data-stu-id="e2995-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-115">201</span><span class="sxs-lookup"><span data-stu-id="e2995-115">201</span></span>
</dt> <dt>



<span data-ttu-id="e2995-116">La solicitud se ha completado y ha dado lugar a la creación de un nuevo recurso.</span><span class="sxs-lookup"><span data-stu-id="e2995-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_Estado HTTP \_ aceptado**</span><span class="sxs-lookup"><span data-stu-id="e2995-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-118">202</span><span class="sxs-lookup"><span data-stu-id="e2995-118">202</span></span>
</dt> <dt>



<span data-ttu-id="e2995-119">Se aceptó la solicitud para el procesamiento, pero no se ha completado el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="e2995-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**Estado de HTTP \_ \_ parcial**</span><span class="sxs-lookup"><span data-stu-id="e2995-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-121">203</span><span class="sxs-lookup"><span data-stu-id="e2995-121">203</span></span>
</dt> <dt>



<span data-ttu-id="e2995-122">La metainformación devuelta en el encabezado de entidad no es el conjunto definitivo disponible en el servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="e2995-122">The returned meta information in the entity-header is not the definitive set available from the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**\_Estado HTTP \_ sin \_ contenido**</span><span class="sxs-lookup"><span data-stu-id="e2995-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-124">204</span><span class="sxs-lookup"><span data-stu-id="e2995-124">204</span></span>
</dt> <dt>



<span data-ttu-id="e2995-125">El servidor ha completado la solicitud, pero no hay información nueva que devolver.</span><span class="sxs-lookup"><span data-stu-id="e2995-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_contenido de \_ restablecimiento de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-127">205</span><span class="sxs-lookup"><span data-stu-id="e2995-127">205</span></span>
</dt> <dt>



<span data-ttu-id="e2995-128">La solicitud se ha completado y el programa cliente debe restablecer la vista de documento que hizo que se enviara la solicitud para permitir que el usuario iniciara fácilmente otra acción de entrada.</span><span class="sxs-lookup"><span data-stu-id="e2995-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ contenido parcial de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-130">206</span><span class="sxs-lookup"><span data-stu-id="e2995-130">206</span></span>
</dt> <dt>



<span data-ttu-id="e2995-131">El servidor ha completado la solicitud de obtención parcial para el recurso.</span><span class="sxs-lookup"><span data-stu-id="e2995-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_Estado HTTP \_ ambiguo**</span><span class="sxs-lookup"><span data-stu-id="e2995-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-133">300</span><span class="sxs-lookup"><span data-stu-id="e2995-133">300</span></span>
</dt> <dt>



<span data-ttu-id="e2995-134">El servidor no pudo decidir qué devolver.</span><span class="sxs-lookup"><span data-stu-id="e2995-134">The server couldn't decide what to return.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_Estado HTTP \_ transferido**</span><span class="sxs-lookup"><span data-stu-id="e2995-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-136">301</span><span class="sxs-lookup"><span data-stu-id="e2995-136">301</span></span>
</dt> <dt>



<span data-ttu-id="e2995-137">El recurso solicitado se ha asignado a un nuevo URI permanente (identificador uniforme de recursos) y todas las referencias futuras a este recurso deben realizarse mediante uno de los URI devueltos.</span><span class="sxs-lookup"><span data-stu-id="e2995-137">The requested resource has been assigned to a new permanent URI (Uniform Resource Identifier), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**redirección de \_ Estado HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-139">302</span><span class="sxs-lookup"><span data-stu-id="e2995-139">302</span></span>
</dt> <dt>



<span data-ttu-id="e2995-140">El recurso solicitado reside temporalmente en un URI diferente (identificador uniforme de recursos).</span><span class="sxs-lookup"><span data-stu-id="e2995-140">The requested resource resides temporarily under a different URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_método de \_ redirección de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-142">303</span><span class="sxs-lookup"><span data-stu-id="e2995-142">303</span></span>
</dt> <dt>



<span data-ttu-id="e2995-143">La respuesta a la solicitud se puede encontrar en un URI diferente (identificador uniforme de recursos) y debe recuperarse con un verbo HTTP GET en ese recurso.</span><span class="sxs-lookup"><span data-stu-id="e2995-143">The response to the request can be found under a different URI (Uniform Resource Identifier) and should be retrieved using a GET HTTP verb on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_Estado HTTP \_ no \_ modificado**</span><span class="sxs-lookup"><span data-stu-id="e2995-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-145">304</span><span class="sxs-lookup"><span data-stu-id="e2995-145">304</span></span>
</dt> <dt>



<span data-ttu-id="e2995-146">No se ha modificado el recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="e2995-146">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**Estado HTTP- \_ \_ usar \_ proxy**</span><span class="sxs-lookup"><span data-stu-id="e2995-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-148">305</span><span class="sxs-lookup"><span data-stu-id="e2995-148">305</span></span>
</dt> <dt>



<span data-ttu-id="e2995-149">Se debe tener acceso al recurso solicitado a través del proxy proporcionado por el campo Ubicación.</span><span class="sxs-lookup"><span data-stu-id="e2995-149">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_verbo de \_ redirección de estado http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-151">307</span><span class="sxs-lookup"><span data-stu-id="e2995-151">307</span></span>
</dt> <dt>



<span data-ttu-id="e2995-152">La solicitud redirigida mantiene el mismo verbo HTTP.</span><span class="sxs-lookup"><span data-stu-id="e2995-152">The redirected request keeps the same HTTP verb.</span></span> <span data-ttu-id="e2995-153">Comportamiento de HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="e2995-153">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_Estado de \_ http \_ Solicitud incorrecta**</span><span class="sxs-lookup"><span data-stu-id="e2995-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-155">400</span><span class="sxs-lookup"><span data-stu-id="e2995-155">400</span></span>
</dt> <dt>



<span data-ttu-id="e2995-156">El servidor no pudo procesar la solicitud debido a una sintaxis no válida.</span><span class="sxs-lookup"><span data-stu-id="e2995-156">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**\_Estado HTTP \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="e2995-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-158">401</span><span class="sxs-lookup"><span data-stu-id="e2995-158">401</span></span>
</dt> <dt>



<span data-ttu-id="e2995-159">El recurso solicitado requiere autenticación de usuarios.</span><span class="sxs-lookup"><span data-stu-id="e2995-159">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**\_solicitud de \_ pago de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-161">402</span><span class="sxs-lookup"><span data-stu-id="e2995-161">402</span></span>
</dt> <dt>



<span data-ttu-id="e2995-162">No se implementa actualmente en el protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="e2995-162">Not currently implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**\_Estado HTTP \_ prohibido**</span><span class="sxs-lookup"><span data-stu-id="e2995-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-164">403</span><span class="sxs-lookup"><span data-stu-id="e2995-164">403</span></span>
</dt> <dt>



<span data-ttu-id="e2995-165">El servidor entendió la solicitud, pero rechaza su cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="e2995-165">The server understood the request, but is refusing to fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_ \_ no \_ se encontró el estado http**</span><span class="sxs-lookup"><span data-stu-id="e2995-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-167">404</span><span class="sxs-lookup"><span data-stu-id="e2995-167">404</span></span>
</dt> <dt>



<span data-ttu-id="e2995-168">El servidor no ha encontrado nada que coincida con el URI (identificador uniforme de recursos) solicitado.</span><span class="sxs-lookup"><span data-stu-id="e2995-168">The server has not found anything matching the requested URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP \_ status ( \_ método incorrecto) \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-170">405</span><span class="sxs-lookup"><span data-stu-id="e2995-170">405</span></span>
</dt> <dt>



<span data-ttu-id="e2995-171">No se permite el verbo HTTP utilizado.</span><span class="sxs-lookup"><span data-stu-id="e2995-171">The HTTP verb used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_Estado HTTP \_ ninguno \_ aceptable**</span><span class="sxs-lookup"><span data-stu-id="e2995-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-173">406</span><span class="sxs-lookup"><span data-stu-id="e2995-173">406</span></span>
</dt> <dt>



<span data-ttu-id="e2995-174">No se encontró ninguna respuesta aceptable para el cliente.</span><span class="sxs-lookup"><span data-stu-id="e2995-174">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**\_solicitud de \_ autenticación de proxy de estado http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-176">407</span><span class="sxs-lookup"><span data-stu-id="e2995-176">407</span></span>
</dt> <dt>



<span data-ttu-id="e2995-177">Se requiere autenticación de proxy.</span><span class="sxs-lookup"><span data-stu-id="e2995-177">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_tiempo de \_ espera de solicitud de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-179">408</span><span class="sxs-lookup"><span data-stu-id="e2995-179">408</span></span>
</dt> <dt>



<span data-ttu-id="e2995-180">El servidor agotó el tiempo de espera para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2995-180">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_conflicto de estado de http \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-182">409</span><span class="sxs-lookup"><span data-stu-id="e2995-182">409</span></span>
</dt> <dt>



<span data-ttu-id="e2995-183">No se pudo completar la solicitud debido a un conflicto con el estado actual del recurso.</span><span class="sxs-lookup"><span data-stu-id="e2995-183">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="e2995-184">El usuario debe volver a enviar con más información.</span><span class="sxs-lookup"><span data-stu-id="e2995-184">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**el estado de HTTP ha \_ \_ desaparecido**</span><span class="sxs-lookup"><span data-stu-id="e2995-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-186">410</span><span class="sxs-lookup"><span data-stu-id="e2995-186">410</span></span>
</dt> <dt>



<span data-ttu-id="e2995-187">El recurso solicitado ya no está disponible en el servidor y no se conoce ninguna dirección de reenvío.</span><span class="sxs-lookup"><span data-stu-id="e2995-187">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**se \_ \_ requiere una longitud de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-189">411</span><span class="sxs-lookup"><span data-stu-id="e2995-189">411</span></span>
</dt> <dt>



<span data-ttu-id="e2995-190">El servidor rechaza la aceptación de la solicitud sin una longitud de contenido definida.</span><span class="sxs-lookup"><span data-stu-id="e2995-190">The server refuses to accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**\_error de \_ precond de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-192">412</span><span class="sxs-lookup"><span data-stu-id="e2995-192">412</span></span>
</dt> <dt>



<span data-ttu-id="e2995-193">La condición previa proporcionada en uno o varios campos de encabezado de solicitud se evaluó como false cuando se probó en el servidor.</span><span class="sxs-lookup"><span data-stu-id="e2995-193">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_solicitud de estado http \_ \_ demasiado \_ grande**</span><span class="sxs-lookup"><span data-stu-id="e2995-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-195">413</span><span class="sxs-lookup"><span data-stu-id="e2995-195">413</span></span>
</dt> <dt>



<span data-ttu-id="e2995-196">El servidor rechaza el procesamiento de una solicitud porque la entidad de solicitud es más grande de lo que el servidor está dispuesto a procesar.</span><span class="sxs-lookup"><span data-stu-id="e2995-196">The server is refusing to process a request because the request entity is larger than the server is willing or able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI de estado http \_ \_ demasiado \_ largo**</span><span class="sxs-lookup"><span data-stu-id="e2995-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-198">414</span><span class="sxs-lookup"><span data-stu-id="e2995-198">414</span></span>
</dt> <dt>



<span data-ttu-id="e2995-199">El servidor rechaza la solicitud porque el URI de solicitud (identificador uniforme de recursos) es más largo de lo que el servidor está dispuesto a interpretar.</span><span class="sxs-lookup"><span data-stu-id="e2995-199">The server is refusing to service the request because the request URI (Uniform Resource Identifier) is longer than the server is willing to interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_Estado HTTP \_ no admitido \_ multimedia**</span><span class="sxs-lookup"><span data-stu-id="e2995-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-201">415</span><span class="sxs-lookup"><span data-stu-id="e2995-201">415</span></span>
</dt> <dt>



<span data-ttu-id="e2995-202">El servidor rechaza la solicitud porque la entidad de la solicitud tiene un formato no admitido por el recurso solicitado para el método solicitado.</span><span class="sxs-lookup"><span data-stu-id="e2995-202">The server is refusing to service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_reintento \_ de estado http \_ con**</span><span class="sxs-lookup"><span data-stu-id="e2995-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-204">449</span><span class="sxs-lookup"><span data-stu-id="e2995-204">449</span></span>
</dt> <dt>



<span data-ttu-id="e2995-205">La solicitud debe volver a intentarse después de realizar la acción adecuada.</span><span class="sxs-lookup"><span data-stu-id="e2995-205">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_error de \_ servidor de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-207">500</span><span class="sxs-lookup"><span data-stu-id="e2995-207">500</span></span>
</dt> <dt>



<span data-ttu-id="e2995-208">El servidor detectó una condición inesperada que le impidió satisfacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2995-208">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_Estado HTTP \_ no \_ admitido**</span><span class="sxs-lookup"><span data-stu-id="e2995-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-210">501</span><span class="sxs-lookup"><span data-stu-id="e2995-210">501</span></span>
</dt> <dt>



<span data-ttu-id="e2995-211">El servidor no admite la funcionalidad necesaria para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2995-211">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**Estado HTTP de \_ \_ puerta de \_ enlace incorrecta**</span><span class="sxs-lookup"><span data-stu-id="e2995-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-213">502</span><span class="sxs-lookup"><span data-stu-id="e2995-213">502</span></span>
</dt> <dt>



<span data-ttu-id="e2995-214">El servidor, mientras actuaba como puerta de enlace o proxy, recibió una respuesta no válida del servidor que precede en la cadena al que tuvo acceso al intentar completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2995-214">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**servicio de Estado HTTP no \_ \_ \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="e2995-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-216">503</span><span class="sxs-lookup"><span data-stu-id="e2995-216">503</span></span>
</dt> <dt>



<span data-ttu-id="e2995-217">El servicio está sobrecargado temporalmente.</span><span class="sxs-lookup"><span data-stu-id="e2995-217">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**tiempo de espera de puerta de \_ enlace de estado http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2995-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-219">504</span><span class="sxs-lookup"><span data-stu-id="e2995-219">504</span></span>
</dt> <dt>



<span data-ttu-id="e2995-220">Se agotó el tiempo de espera de una puerta de enlace para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2995-220">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2995-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_versión de estado http \_ \_ no \_ SUP**</span><span class="sxs-lookup"><span data-stu-id="e2995-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2995-222">505</span><span class="sxs-lookup"><span data-stu-id="e2995-222">505</span></span>
</dt> <dt>



<span data-ttu-id="e2995-223">El servidor no admite o rechaza la versión del protocolo HTTP que se usó en el mensaje de solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2995-223">The server does not support, or refuses to support, the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2995-224">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2995-224">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e2995-225">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="e2995-225">WinINet does not support server implementations.</span></span> <span data-ttu-id="e2995-226">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="e2995-226">In addition, it should not be used from a service.</span></span> <span data-ttu-id="e2995-227">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="e2995-227">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2995-228">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2995-228">Requirements</span></span>



| <span data-ttu-id="e2995-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2995-229">Requirement</span></span> | <span data-ttu-id="e2995-230">Value</span><span class="sxs-lookup"><span data-stu-id="e2995-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e2995-231">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2995-231">Minimum supported client</span></span><br/> | <span data-ttu-id="e2995-232">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e2995-232">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e2995-233">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2995-233">Minimum supported server</span></span><br/> | <span data-ttu-id="e2995-234">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e2995-234">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e2995-235">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2995-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2995-236"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2995-236"><dt>Wininet.h</dt></span></span> </dl> |



 

