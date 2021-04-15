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
# <a name="http-status-codes-winineth"></a>Códigos de Estado HTTP (Wininet. h)

La tabla siguiente contiene las constantes y los valores correspondientes para los códigos de Estado HTTP devueltos por los servidores en Internet.

<dl> <dt>

<span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**\_continuación de estado http \_**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



La solicitud puede continuar.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_protocolos de \_ cambio de estado http \_**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



El servidor ha cambiado los protocolos en un encabezado de actualización.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**\_Estado HTTP \_ correcto**
</dt> <dd> <dl> <dt>

200
</dt> <dt>



La solicitud se completó correctamente.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**\_Estado HTTP \_ creado**
</dt> <dd> <dl> <dt>

201
</dt> <dt>



La solicitud se ha completado y ha dado lugar a la creación de un nuevo recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_Estado HTTP \_ aceptado**
</dt> <dd> <dl> <dt>

202
</dt> <dt>



Se aceptó la solicitud para el procesamiento, pero no se ha completado el procesamiento.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**Estado de HTTP \_ \_ parcial**
</dt> <dd> <dl> <dt>

203
</dt> <dt>



La metainformación devuelta en el encabezado de entidad no es el conjunto definitivo disponible en el servidor de origen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**\_Estado HTTP \_ sin \_ contenido**
</dt> <dd> <dl> <dt>

204
</dt> <dt>



El servidor ha completado la solicitud, pero no hay información nueva que devolver.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_contenido de \_ restablecimiento de estado http \_**
</dt> <dd> <dl> <dt>

205
</dt> <dt>



La solicitud se ha completado y el programa cliente debe restablecer la vista de documento que hizo que se enviara la solicitud para permitir que el usuario iniciara fácilmente otra acción de entrada.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ contenido parcial de estado http \_**
</dt> <dd> <dl> <dt>

206
</dt> <dt>



El servidor ha completado la solicitud de obtención parcial para el recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_Estado HTTP \_ ambiguo**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



El servidor no pudo decidir qué devolver.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_Estado HTTP \_ transferido**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



El recurso solicitado se ha asignado a un nuevo URI permanente (identificador uniforme de recursos) y todas las referencias futuras a este recurso deben realizarse mediante uno de los URI devueltos.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**redirección de \_ Estado HTTP \_**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



El recurso solicitado reside temporalmente en un URI diferente (identificador uniforme de recursos).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_método de \_ redirección de estado http \_**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



La respuesta a la solicitud se puede encontrar en un URI diferente (identificador uniforme de recursos) y debe recuperarse con un verbo HTTP GET en ese recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_Estado HTTP \_ no \_ modificado**
</dt> <dd> <dl> <dt>

304
</dt> <dt>



No se ha modificado el recurso solicitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**Estado HTTP- \_ \_ usar \_ proxy**
</dt> <dd> <dl> <dt>

305
</dt> <dt>



Se debe tener acceso al recurso solicitado a través del proxy proporcionado por el campo Ubicación.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_verbo de \_ redirección de estado http \_ \_**
</dt> <dd> <dl> <dt>

307
</dt> <dt>



La solicitud redirigida mantiene el mismo verbo HTTP. Comportamiento de HTTP/1.1.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_Estado de \_ http \_ Solicitud incorrecta**
</dt> <dd> <dl> <dt>

400
</dt> <dt>



El servidor no pudo procesar la solicitud debido a una sintaxis no válida.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**\_Estado HTTP \_ denegado**
</dt> <dd> <dl> <dt>

401
</dt> <dt>



El recurso solicitado requiere autenticación de usuarios.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**\_solicitud de \_ pago de estado http \_**
</dt> <dd> <dl> <dt>

402
</dt> <dt>



No se implementa actualmente en el protocolo HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**\_Estado HTTP \_ prohibido**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



El servidor entendió la solicitud, pero rechaza su cumplimiento.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_ \_ no \_ se encontró el estado http**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



El servidor no ha encontrado nada que coincida con el URI (identificador uniforme de recursos) solicitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP \_ status ( \_ método incorrecto) \_**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



No se permite el verbo HTTP utilizado.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_Estado HTTP \_ ninguno \_ aceptable**
</dt> <dd> <dl> <dt>

406
</dt> <dt>



No se encontró ninguna respuesta aceptable para el cliente.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**\_solicitud de \_ autenticación de proxy de estado http \_ \_**
</dt> <dd> <dl> <dt>

407
</dt> <dt>



Se requiere autenticación de proxy.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_tiempo de \_ espera de solicitud de estado http \_**
</dt> <dd> <dl> <dt>

408
</dt> <dt>



El servidor agotó el tiempo de espera para la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_conflicto de estado de http \_**
</dt> <dd> <dl> <dt>

409
</dt> <dt>



No se pudo completar la solicitud debido a un conflicto con el estado actual del recurso. El usuario debe volver a enviar con más información.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**el estado de HTTP ha \_ \_ desaparecido**
</dt> <dd> <dl> <dt>

410
</dt> <dt>



El recurso solicitado ya no está disponible en el servidor y no se conoce ninguna dirección de reenvío.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**se \_ \_ requiere una longitud de estado http \_**
</dt> <dd> <dl> <dt>

411
</dt> <dt>



El servidor rechaza la aceptación de la solicitud sin una longitud de contenido definida.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**\_error de \_ precond de estado http \_**
</dt> <dd> <dl> <dt>

412
</dt> <dt>



La condición previa proporcionada en uno o varios campos de encabezado de solicitud se evaluó como false cuando se probó en el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_solicitud de estado http \_ \_ demasiado \_ grande**
</dt> <dd> <dl> <dt>

413
</dt> <dt>



El servidor rechaza el procesamiento de una solicitud porque la entidad de solicitud es más grande de lo que el servidor está dispuesto a procesar.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI de estado http \_ \_ demasiado \_ largo**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



El servidor rechaza la solicitud porque el URI de solicitud (identificador uniforme de recursos) es más largo de lo que el servidor está dispuesto a interpretar.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_Estado HTTP \_ no admitido \_ multimedia**
</dt> <dd> <dl> <dt>

415
</dt> <dt>



El servidor rechaza la solicitud porque la entidad de la solicitud tiene un formato no admitido por el recurso solicitado para el método solicitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_reintento \_ de estado http \_ con**
</dt> <dd> <dl> <dt>

449
</dt> <dt>



La solicitud debe volver a intentarse después de realizar la acción adecuada.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_error de \_ servidor de estado http \_**
</dt> <dd> <dl> <dt>

500
</dt> <dt>



El servidor detectó una condición inesperada que le impidió satisfacer la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_Estado HTTP \_ no \_ admitido**
</dt> <dd> <dl> <dt>

501
</dt> <dt>



El servidor no admite la funcionalidad necesaria para completar la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**Estado HTTP de \_ \_ puerta de \_ enlace incorrecta**
</dt> <dd> <dl> <dt>

502
</dt> <dt>



El servidor, mientras actuaba como puerta de enlace o proxy, recibió una respuesta no válida del servidor que precede en la cadena al que tuvo acceso al intentar completar la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**servicio de Estado HTTP no \_ \_ \_ disponible**
</dt> <dd> <dl> <dt>

503
</dt> <dt>



El servicio está sobrecargado temporalmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**tiempo de espera de puerta de \_ enlace de estado http \_ \_**
</dt> <dd> <dl> <dt>

504
</dt> <dt>



Se agotó el tiempo de espera de una puerta de enlace para la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_versión de estado http \_ \_ no \_ SUP**
</dt> <dd> <dl> <dt>

505
</dt> <dt>



El servidor no admite o rechaza la versión del protocolo HTTP que se usó en el mensaje de solicitud.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



 

