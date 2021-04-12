---
description: Estas constantes y los valores correspondientes indican los códigos de Estado HTTP devueltos por los servidores en Internet.
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: Códigos de Estado HTTP (winhttp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf4103cdc382bd5ab0d582fe99212083e2780ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277516"
---
# <a name="http-status-codes-winhttph"></a><span data-ttu-id="bfe27-103">Códigos de Estado HTTP (winhttp. h)</span><span class="sxs-lookup"><span data-stu-id="bfe27-103">HTTP Status Codes (Winhttp.h)</span></span>

<span data-ttu-id="bfe27-104">Estas constantes y los valores correspondientes indican los códigos de Estado HTTP devueltos por los servidores en Internet.</span><span class="sxs-lookup"><span data-stu-id="bfe27-104">These constants and corresponding values indicate HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="bfe27-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**\_continuación de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-106">100</span><span class="sxs-lookup"><span data-stu-id="bfe27-106">100</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-107">La solicitud puede continuar.</span><span class="sxs-lookup"><span data-stu-id="bfe27-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_protocolos de \_ cambio de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-109">101</span><span class="sxs-lookup"><span data-stu-id="bfe27-109">101</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-110">El servidor ha cambiado los protocolos en un encabezado de actualización.</span><span class="sxs-lookup"><span data-stu-id="bfe27-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**\_Estado HTTP \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="bfe27-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-112">200</span><span class="sxs-lookup"><span data-stu-id="bfe27-112">200</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-113">La solicitud se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bfe27-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**\_Estado HTTP \_ creado**</span><span class="sxs-lookup"><span data-stu-id="bfe27-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-115">201</span><span class="sxs-lookup"><span data-stu-id="bfe27-115">201</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-116">La solicitud se ha completado y ha dado lugar a la creación de un nuevo recurso.</span><span class="sxs-lookup"><span data-stu-id="bfe27-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_Estado HTTP \_ aceptado**</span><span class="sxs-lookup"><span data-stu-id="bfe27-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-118">202</span><span class="sxs-lookup"><span data-stu-id="bfe27-118">202</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-119">Se aceptó la solicitud para el procesamiento, pero no se ha completado el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="bfe27-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**Estado de HTTP \_ \_ parcial**</span><span class="sxs-lookup"><span data-stu-id="bfe27-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-121">203</span><span class="sxs-lookup"><span data-stu-id="bfe27-121">203</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-122">La metainformación devuelta en el encabezado de entidad no es el conjunto definitivo disponible en el servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="bfe27-122">The returned meta information in the entity-header is not the definitive set available from the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**\_Estado HTTP \_ sin \_ contenido**</span><span class="sxs-lookup"><span data-stu-id="bfe27-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-124">204</span><span class="sxs-lookup"><span data-stu-id="bfe27-124">204</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-125">El servidor ha completado la solicitud, pero no hay información nueva que devolver.</span><span class="sxs-lookup"><span data-stu-id="bfe27-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_contenido de \_ restablecimiento de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-127">205</span><span class="sxs-lookup"><span data-stu-id="bfe27-127">205</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-128">La solicitud se ha completado y el programa cliente debe restablecer la vista de documento que hizo que se enviara la solicitud para permitir que el usuario iniciara fácilmente otra acción de entrada.</span><span class="sxs-lookup"><span data-stu-id="bfe27-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ contenido parcial de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-130">206</span><span class="sxs-lookup"><span data-stu-id="bfe27-130">206</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-131">El servidor ha completado la solicitud de obtención parcial para el recurso.</span><span class="sxs-lookup"><span data-stu-id="bfe27-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-132"><span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**estado \_ http \_ WebDAV \_ \_ multistatus**</span><span class="sxs-lookup"><span data-stu-id="bfe27-132"><span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**HTTP\_STATUS\_WEBDAV\_MULTI\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-133">207</span><span class="sxs-lookup"><span data-stu-id="bfe27-133">207</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-134">Durante un World Wide Web operación de creación y control de versiones distribuidas (WebDAV), esto indica varios códigos de estado para una sola respuesta.</span><span class="sxs-lookup"><span data-stu-id="bfe27-134">During a World Wide Web Distributed Authoring and Versioning (WebDAV) operation, this indicates multiple status codes for a single response.</span></span> <span data-ttu-id="bfe27-135">El cuerpo de la respuesta contiene lenguaje de marcado extensible (XML) que describe los códigos de estado.</span><span class="sxs-lookup"><span data-stu-id="bfe27-135">The response body contains Extensible Markup Language (XML) that describes the status codes.</span></span> <span data-ttu-id="bfe27-136">Para obtener más información, consulte [extensiones http para la creación distribuida](../webdav/webdav-portal.md).</span><span class="sxs-lookup"><span data-stu-id="bfe27-136">For more information, see [HTTP Extensions for Distributed Authoring](../webdav/webdav-portal.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-137"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_Estado HTTP \_ ambiguo**</span><span class="sxs-lookup"><span data-stu-id="bfe27-137"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-138">300</span><span class="sxs-lookup"><span data-stu-id="bfe27-138">300</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-139">El recurso solicitado está disponible en una o varias ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="bfe27-139">The requested resource is available at one or more locations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-140"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_Estado HTTP \_ transferido**</span><span class="sxs-lookup"><span data-stu-id="bfe27-140"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-141">301</span><span class="sxs-lookup"><span data-stu-id="bfe27-141">301</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-142">El recurso solicitado se ha asignado a un nuevo identificador uniforme de recursos (URI) permanente y todas las referencias futuras a este recurso deben realizarse mediante uno de los URI devueltos.</span><span class="sxs-lookup"><span data-stu-id="bfe27-142">The requested resource has been assigned to a new permanent Uniform Resource Identifier (URI), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-143"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**redirección de \_ Estado HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-143"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-144">302</span><span class="sxs-lookup"><span data-stu-id="bfe27-144">302</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-145">El recurso solicitado reside temporalmente en un URI diferente.</span><span class="sxs-lookup"><span data-stu-id="bfe27-145">The requested resource resides temporarily under a different URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-146"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_método de \_ redirección de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-146"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-147">303</span><span class="sxs-lookup"><span data-stu-id="bfe27-147">303</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-148">La respuesta a la solicitud se puede encontrar en un URI diferente y debe recuperarse mediante un [*verbo http*](glossary.md) get en ese recurso.</span><span class="sxs-lookup"><span data-stu-id="bfe27-148">The response to the request can be found under a different URI and should be retrieved using a GET [*HTTP verb*](glossary.md) on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-149"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_Estado HTTP \_ no \_ modificado**</span><span class="sxs-lookup"><span data-stu-id="bfe27-149"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-150">304</span><span class="sxs-lookup"><span data-stu-id="bfe27-150">304</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-151">No se ha modificado el recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="bfe27-151">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-152"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**Estado HTTP- \_ \_ usar \_ proxy**</span><span class="sxs-lookup"><span data-stu-id="bfe27-152"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-153">305</span><span class="sxs-lookup"><span data-stu-id="bfe27-153">305</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-154">Se debe tener acceso al recurso solicitado a través del proxy proporcionado por el campo Ubicación.</span><span class="sxs-lookup"><span data-stu-id="bfe27-154">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-155"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_verbo de \_ redirección de estado http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-155"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-156">307</span><span class="sxs-lookup"><span data-stu-id="bfe27-156">307</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-157">La solicitud redirigida mantiene el mismo [*verbo http*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="bfe27-157">The redirected request keeps the same [*HTTP verb*](glossary.md).</span></span> <span data-ttu-id="bfe27-158">Comportamiento de HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="bfe27-158">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-159"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_Estado de \_ http \_ Solicitud incorrecta**</span><span class="sxs-lookup"><span data-stu-id="bfe27-159"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-160">400</span><span class="sxs-lookup"><span data-stu-id="bfe27-160">400</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-161">El servidor no pudo procesar la solicitud debido a una sintaxis no válida.</span><span class="sxs-lookup"><span data-stu-id="bfe27-161">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-162"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**\_Estado HTTP \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="bfe27-162"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-163">401</span><span class="sxs-lookup"><span data-stu-id="bfe27-163">401</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-164">El recurso solicitado requiere autenticación de usuarios.</span><span class="sxs-lookup"><span data-stu-id="bfe27-164">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-165"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**\_solicitud de \_ pago de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-165"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-166">402</span><span class="sxs-lookup"><span data-stu-id="bfe27-166">402</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-167">No se implementa en el protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="bfe27-167">Not implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-168"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**\_Estado HTTP \_ prohibido**</span><span class="sxs-lookup"><span data-stu-id="bfe27-168"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-169">403</span><span class="sxs-lookup"><span data-stu-id="bfe27-169">403</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-170">El servidor entendió la solicitud, pero no puede atenderla.</span><span class="sxs-lookup"><span data-stu-id="bfe27-170">The server understood the request, but cannot fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-171"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_ \_ no \_ se encontró el estado http**</span><span class="sxs-lookup"><span data-stu-id="bfe27-171"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-172">404</span><span class="sxs-lookup"><span data-stu-id="bfe27-172">404</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-173">El servidor no ha encontrado nada que coincida con el URI solicitado.</span><span class="sxs-lookup"><span data-stu-id="bfe27-173">The server has not found anything that matches the requested URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-174"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP \_ status ( \_ método incorrecto) \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-174"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-175">405</span><span class="sxs-lookup"><span data-stu-id="bfe27-175">405</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-176">No se permite el [*verbo http*](glossary.md) utilizado.</span><span class="sxs-lookup"><span data-stu-id="bfe27-176">The [*HTTP verb*](glossary.md) used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-177"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_Estado HTTP \_ ninguno \_ aceptable**</span><span class="sxs-lookup"><span data-stu-id="bfe27-177"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-178">406</span><span class="sxs-lookup"><span data-stu-id="bfe27-178">406</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-179">No se encontró ninguna respuesta aceptable para el cliente.</span><span class="sxs-lookup"><span data-stu-id="bfe27-179">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-180"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**\_solicitud de \_ autenticación de proxy de estado http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-180"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-181">407</span><span class="sxs-lookup"><span data-stu-id="bfe27-181">407</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-182">Se requiere autenticación de proxy.</span><span class="sxs-lookup"><span data-stu-id="bfe27-182">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-183"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_tiempo de \_ espera de solicitud de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-183"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-184">408</span><span class="sxs-lookup"><span data-stu-id="bfe27-184">408</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-185">El servidor agotó el tiempo de espera para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfe27-185">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-186"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_conflicto de estado de http \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-186"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-187">409</span><span class="sxs-lookup"><span data-stu-id="bfe27-187">409</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-188">No se pudo completar la solicitud debido a un conflicto con el estado actual del recurso.</span><span class="sxs-lookup"><span data-stu-id="bfe27-188">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="bfe27-189">El usuario debe volver a enviar con más información.</span><span class="sxs-lookup"><span data-stu-id="bfe27-189">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-190"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**el estado de HTTP ha \_ \_ desaparecido**</span><span class="sxs-lookup"><span data-stu-id="bfe27-190"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-191">410</span><span class="sxs-lookup"><span data-stu-id="bfe27-191">410</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-192">El recurso solicitado ya no está disponible en el servidor y no se conoce ninguna dirección de reenvío.</span><span class="sxs-lookup"><span data-stu-id="bfe27-192">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-193"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**se \_ \_ requiere una longitud de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-193"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-194">411</span><span class="sxs-lookup"><span data-stu-id="bfe27-194">411</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-195">El servidor no puede aceptar la solicitud sin una longitud de contenido definida.</span><span class="sxs-lookup"><span data-stu-id="bfe27-195">The server cannot accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-196"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**\_error de \_ precond de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-196"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-197">412</span><span class="sxs-lookup"><span data-stu-id="bfe27-197">412</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-198">La condición previa proporcionada en uno o varios campos de encabezado de solicitud se evaluó como false cuando se probó en el servidor.</span><span class="sxs-lookup"><span data-stu-id="bfe27-198">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-199"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_solicitud de estado http \_ \_ demasiado \_ grande**</span><span class="sxs-lookup"><span data-stu-id="bfe27-199"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-200">413</span><span class="sxs-lookup"><span data-stu-id="bfe27-200">413</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-201">El servidor no puede procesar la solicitud porque la entidad de solicitud es más grande de lo que el servidor puede procesar.</span><span class="sxs-lookup"><span data-stu-id="bfe27-201">The server cannot process the request because the request entity is larger than the server is able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-202"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI de estado http \_ \_ demasiado \_ largo**</span><span class="sxs-lookup"><span data-stu-id="bfe27-202"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-203">414</span><span class="sxs-lookup"><span data-stu-id="bfe27-203">414</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-204">El servidor no puede atender la solicitud porque el URI de la solicitud es más largo que el servidor puede interpretar.</span><span class="sxs-lookup"><span data-stu-id="bfe27-204">The server cannot service the request because the request URI is longer than the server can interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-205"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_Estado HTTP \_ no admitido \_ multimedia**</span><span class="sxs-lookup"><span data-stu-id="bfe27-205"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-206">415</span><span class="sxs-lookup"><span data-stu-id="bfe27-206">415</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-207">El servidor no puede atender la solicitud porque la entidad de la solicitud tiene un formato no admitido por el recurso solicitado para el método solicitado.</span><span class="sxs-lookup"><span data-stu-id="bfe27-207">The server cannot service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-208"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_reintento \_ de estado http \_ con**</span><span class="sxs-lookup"><span data-stu-id="bfe27-208"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-209">449</span><span class="sxs-lookup"><span data-stu-id="bfe27-209">449</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-210">La solicitud debe volver a intentarse después de realizar la acción adecuada.</span><span class="sxs-lookup"><span data-stu-id="bfe27-210">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-211"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_error de \_ servidor de estado http \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-211"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-212">500</span><span class="sxs-lookup"><span data-stu-id="bfe27-212">500</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-213">El servidor detectó una condición inesperada que le impidió satisfacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfe27-213">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-214"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_Estado HTTP \_ no \_ admitido**</span><span class="sxs-lookup"><span data-stu-id="bfe27-214"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-215">501</span><span class="sxs-lookup"><span data-stu-id="bfe27-215">501</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-216">El servidor no admite la funcionalidad necesaria para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfe27-216">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-217"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**Estado HTTP de \_ \_ puerta de \_ enlace incorrecta**</span><span class="sxs-lookup"><span data-stu-id="bfe27-217"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-218">502</span><span class="sxs-lookup"><span data-stu-id="bfe27-218">502</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-219">El servidor, mientras actuaba como puerta de enlace o proxy, recibió una respuesta no válida del servidor que precede en la cadena al que tuvo acceso al intentar completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfe27-219">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-220"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**servicio de Estado HTTP no \_ \_ \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="bfe27-220"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-221">503</span><span class="sxs-lookup"><span data-stu-id="bfe27-221">503</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-222">El servicio está sobrecargado temporalmente.</span><span class="sxs-lookup"><span data-stu-id="bfe27-222">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-223"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**tiempo de espera de puerta de \_ enlace de estado http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bfe27-223"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-224">504</span><span class="sxs-lookup"><span data-stu-id="bfe27-224">504</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-225">Se agotó el tiempo de espera de una puerta de enlace para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfe27-225">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bfe27-226"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_versión de estado http \_ \_ no \_ SUP**</span><span class="sxs-lookup"><span data-stu-id="bfe27-226"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfe27-227">505</span><span class="sxs-lookup"><span data-stu-id="bfe27-227">505</span></span>
</dt> <dt>



<span data-ttu-id="bfe27-228">El servidor no admite la versión del protocolo HTTP que se usó en el mensaje de solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfe27-228">The server does not support the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfe27-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfe27-229">Requirements</span></span>



| <span data-ttu-id="bfe27-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfe27-230">Requirement</span></span> | <span data-ttu-id="bfe27-231">Value</span><span class="sxs-lookup"><span data-stu-id="bfe27-231">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bfe27-232">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfe27-232">Minimum supported client</span></span><br/> | <span data-ttu-id="bfe27-233">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="bfe27-233">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="bfe27-234">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfe27-234">Minimum supported server</span></span><br/> | <span data-ttu-id="bfe27-235">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="bfe27-235">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="bfe27-236">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfe27-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfe27-237"><dt>Winhttp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfe27-237"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfe27-238">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfe27-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfe27-239">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="bfe27-239">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

