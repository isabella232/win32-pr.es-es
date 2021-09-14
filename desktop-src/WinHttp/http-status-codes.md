---
description: Estas constantes y los valores correspondientes indican códigos de estado HTTP devueltos por los servidores en Internet.
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: Códigos de estado HTTP (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf4103cdc382bd5ab0d582fe99212083e2780ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068349"
---
# <a name="http-status-codes-winhttph"></a>Códigos de estado HTTP (Winhttp.h)

Estas constantes y los valores correspondientes indican códigos de estado HTTP devueltos por los servidores en Internet.

<dl> <dt>

<span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP \_ STATUS \_ CONTINUE**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



La solicitud se puede continuar.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**PROTOCOLOS \_ DE CONMUTADOR DE ESTADO \_ \_ HTTP**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



El servidor ha cambiado los protocolos en un encabezado de actualización.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**ESTADO HTTP \_ \_ CORRECTO**
</dt> <dd> <dl> <dt>

200
</dt> <dt>



La solicitud se completó correctamente.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**ESTADO HTTP \_ \_ CREADO**
</dt> <dd> <dl> <dt>

201
</dt> <dt>



La solicitud se ha realizado y ha dado lugar a la creación de un nuevo recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**ESTADO HTTP \_ \_ ACEPTADO**
</dt> <dd> <dl> <dt>

202
</dt> <dt>



La solicitud se ha aceptado para su procesamiento, pero el procesamiento no se ha completado.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**ESTADO HTTP \_ \_ PARCIAL**
</dt> <dd> <dl> <dt>

203
</dt> <dt>



La metanálisis devuelta en el encabezado de entidad no es el conjunto definitiva disponible en el servidor de origen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**ESTADO HTTP \_ \_ SIN \_ CONTENIDO**
</dt> <dd> <dl> <dt>

204
</dt> <dt>



El servidor ha cumplido la solicitud, pero no hay información nueva que devolver.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**CONTENIDO DE \_ \_ RESTABLECIMIENTO DE ESTADO \_ HTTP**
</dt> <dd> <dl> <dt>

205
</dt> <dt>



La solicitud se ha completado y el programa cliente debe restablecer la vista de documento que hizo que la solicitud se enviara para permitir al usuario iniciar fácilmente otra acción de entrada.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**CONTENIDO \_ PARCIAL DE ESTADO \_ \_ HTTP**
</dt> <dd> <dl> <dt>

206
</dt> <dt>



El servidor ha cumplido la solicitud GET parcial del recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**ESTADO HTTP \_ \_ WEBDAV \_ MULTI \_ STATUS**
</dt> <dd> <dl> <dt>

207
</dt> <dt>



Durante una World Wide Web de creación y control de versiones distribuidos (WebDAV), esto indica varios códigos de estado para una única respuesta. El cuerpo de la respuesta lenguaje de marcado extensible (XML) que describe los códigos de estado. Para obtener más información, [vea Extensiones HTTP para la creación distribuida.](../webdav/webdav-portal.md)


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**ESTADO HTTP \_ \_ AMBIGUO**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



El recurso solicitado está disponible en una o varias ubicaciones.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**ESTADO HTTP \_ \_ MOVIDO**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



El recurso solicitado se ha asignado a un nuevo identificador uniforme de recursos (URI) permanente y las referencias futuras a este recurso deben realizarse mediante uno de los URI devueltos.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**REDIRECCIÓN \_ DE ESTADO \_ HTTP**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



El recurso solicitado reside temporalmente en un URI diferente.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**MÉTODO DE \_ REDIRECCIÓN \_ DE ESTADO \_ HTTP**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



La respuesta a la solicitud se puede encontrar en un URI diferente y debe recuperarse mediante un [*verbo HTTP*](glossary.md) GET en ese recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**ESTADO HTTP \_ \_ NO \_ MODIFICADO**
</dt> <dd> <dl> <dt>

304
</dt> <dt>



El recurso solicitado no se ha modificado.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**ESTADO HTTP \_ \_ USE \_ PROXY**
</dt> <dd> <dl> <dt>

305
</dt> <dt>



Se debe acceder al recurso solicitado a través del proxy que proporciona el campo de ubicación.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**VERBO KEEP KEEP DE REDIRECCIÓN DE ESTADO \_ \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>

307
</dt> <dt>



La solicitud redirigida mantiene el mismo [*verbo HTTP*](glossary.md). Comportamiento http/1.1.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**SOLICITUD \_ DE ESTADO HTTP NO \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

400
</dt> <dt>



El servidor no pudo procesar la solicitud debido a una sintaxis no válida.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**ESTADO HTTP \_ \_ DENEGADO**
</dt> <dd> <dl> <dt>

401
</dt> <dt>



El recurso solicitado requiere autenticación de usuarios.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**SOLICITUD DE \_ PAGO \_ DE ESTADO \_ HTTP**
</dt> <dd> <dl> <dt>

402
</dt> <dt>



No se implementa en el protocolo HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**ESTADO HTTP \_ \_ PROHIBIDO**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



El servidor entiende la solicitud, pero no puede satisfacerla.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**ESTADO HTTP \_ \_ NO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



El servidor no ha encontrado nada que coincida con el URI solicitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP \_ STATUS \_ BAD \_ METHOD**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



No [*se permite el*](glossary.md) verbo HTTP utilizado.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**ESTADO HTTP \_ \_ NO \_ ACEPTABLE**
</dt> <dd> <dl> <dt>

406
</dt> <dt>



No se encontraron respuestas aceptables para el cliente.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**SOLICITUD DE \_ \_ AUTENTICACIÓN DE PROXY \_ DE ESTADO \_ HTTP**
</dt> <dd> <dl> <dt>

407
</dt> <dt>



Se requiere autenticación de proxy.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**TIEMPO DE \_ ESPERA DE SOLICITUD DE ESTADO \_ \_ HTTP**
</dt> <dd> <dl> <dt>

408
</dt> <dt>



El servidor agotó el tiempo de espera para la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**CONFLICTO \_ DE ESTADO \_ HTTP**
</dt> <dd> <dl> <dt>

409
</dt> <dt>



No se pudo completar la solicitud debido a un conflicto con el estado actual del recurso. El usuario debe volver a enviar con más información.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**ESTADO HTTP \_ \_ DESAPARECIDO**
</dt> <dd> <dl> <dt>

410
</dt> <dt>



El recurso solicitado ya no está disponible en el servidor y no se conoce ninguna dirección de reenvío.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**LONGITUD \_ DE ESTADO HTTP \_ \_ REQUERIDA**
</dt> <dd> <dl> <dt>

411
</dt> <dt>



El servidor no puede aceptar la solicitud sin una longitud de contenido definida.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**ERROR \_ EN \_ EL PRECOND DE ESTADO \_ HTTP**
</dt> <dd> <dl> <dt>

412
</dt> <dt>



La condición previa dada en uno o varios de los campos de encabezado de solicitud se evaluó como false cuando se probó en el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**SOLICITUD DE ESTADO HTTP \_ \_ DEMASIADO \_ \_ GRANDE**
</dt> <dd> <dl> <dt>

413
</dt> <dt>



El servidor no puede procesar la solicitud porque la entidad de solicitud es mayor que la que el servidor puede procesar.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**URI \_ DE ESTADO HTTP DEMASIADO \_ \_ \_ LARGO**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



El servidor no puede dar servicio a la solicitud porque el URI de la solicitud es mayor de lo que el servidor puede interpretar.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**MEDIOS DE ESTADO HTTP \_ \_ NO \_ ADMITIDOS**
</dt> <dd> <dl> <dt>

415
</dt> <dt>



El servidor no puede dar servicio a la solicitud porque la entidad de la solicitud está en un formato no admitido por el recurso solicitado para el método solicitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**REINTENTO DE ESTADO HTTP \_ \_ \_ CON**
</dt> <dd> <dl> <dt>

449
</dt> <dt>



La solicitud debe reinterse después de realizar la acción adecuada.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**ERROR \_ DEL SERVIDOR DE ESTADO \_ \_ HTTP**
</dt> <dd> <dl> <dt>

500
</dt> <dt>



El servidor encontró una condición inesperada que le impedía cumplir la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**ESTADO HTTP \_ \_ NO \_ ADMITIDO**
</dt> <dd> <dl> <dt>

501
</dt> <dt>



El servidor no admite la funcionalidad necesaria para satisfacer la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**PUERTA \_ DE ENLACE DE ESTADO HTTP NO \_ \_ SEGURA**
</dt> <dd> <dl> <dt>

502
</dt> <dt>



El servidor, mientras actuaba como puerta de enlace o proxy, recibió una respuesta no válida del servidor ascendente al que tuvo acceso al intentar satisfacer la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP \_ STATUS \_ SERVICE \_ UNAVAIL**
</dt> <dd> <dl> <dt>

503
</dt> <dt>



El servicio está sobrecargado temporalmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**TIEMPO DE \_ ESPERA DE LA PUERTA DE ENLACE DE ESTADO \_ \_ HTTP**
</dt> <dd> <dl> <dt>

504
</dt> <dt>



Se agotó el tiempo de espera de una puerta de enlace para la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**VERSIÓN DE ESTADO HTTP \_ \_ NO \_ \_ SUP**
</dt> <dd> <dl> <dt>

505
</dt> <dt>



El servidor no admite la versión del protocolo HTTP que se usó en el mensaje de solicitud.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>      |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>   |
| Encabezado<br/>                   | <dl> <dt>Winhttp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

