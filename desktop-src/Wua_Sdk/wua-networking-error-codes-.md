---
description: 'Más información acerca de: códigos de error de red de WUA'
ms.assetid: 07ff2ed7-09bc-4af7-84f9-66a921c0f53f
title: Códigos de error de red de WUA (Wuerror. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fb2c027939afda3fe5817a8a860469fc90b766
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709020"
---
# <a name="wua-networking-error-codes"></a>Códigos de error de red de WUA

La API del agente de Windows Update (WUA) puede devolver los siguientes códigos de error al realizar operaciones de red, como buscar actualizaciones:



| Constante o valor                                                                                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WU_E_WINHTTP_INVALID_FILE"></span><span id="wu_e_winhttp_invalid_file"></span><dl> <dt>**Wu \_ E \_ WinHTTP \_ \_ archivo no válido**</dt> <dt>0x80240038</dt> </dl>                                  | El archivo descargado tiene un tipo de contenido inesperado.<br/>                                                                                                                               |
| <span id="WU_E_PT_HTTP_STATUS_BAD_REQUEST"></span><span id="wu_e_pt_http_status_bad_request"></span><dl> <dt>**Wu \_ E \_ PT \_ http \_ estado \_ http \_ Solicitud incorrecta**</dt> <dt>0x80244016</dt> </dl>              | Igual que estado HTTP 400: el servidor no pudo procesar la solicitud debido a una sintaxis no válida.<br/>                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_DENIED"></span><span id="wu_e_pt_http_status_denied"></span><dl> <dt>**Wu \_ E \_ PT \_ http de \_ estado \_ denegado**</dt> <dt>0x80244017</dt> </dl>                              | Igual que estado HTTP 401: el recurso solicitado requiere autenticación de usuario.<br/>                                                                                                    |
| <span id="WU_E_PT_HTTP_STATUS_FORBIDDEN"></span><span id="wu_e_pt_http_status_forbidden"></span><dl> <dt>**Wu \_ E \_ PT \_ http \_ estado \_ prohibido**</dt> <dt>0x80244018</dt> </dl>                     | Igual que estado HTTP 403: el servidor entendió la solicitud, pero rechaza su cumplimiento.<br/>                                                                                              |
| <span id="WU_E_PT_HTTP_STATUS_NOT_FOUND"></span><span id="wu_e_pt_http_status_not_found"></span><dl> <dt>**Wu \_ \_ \_ \_ \_ No \_ se encontró el estado http de E PT**</dt> <dt>0x80244019</dt> </dl>                    | Igual que estado HTTP 404: el servidor no encuentra el URI (identificador uniforme de recursos) solicitado.<br/>                                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_BAD_METHOD"></span><span id="wu_e_pt_http_status_bad_method"></span><dl> <dt>**Wu \_ E \_ PT \_ http \_ Estado HTTP \_ incorrecto \_ método**</dt> <dt>0x8024401A</dt> </dl>                 | Igual que estado HTTP 405: no se permite el método HTTP.<br/>                                                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="wu_e_pt_http_status_proxy_auth_req"></span><dl> <dt>**Wu \_ E \_ PT \_ http de \_ Estado HTTP \_ \_ auth \_ req**</dt> <dt>0x8024401B</dt> </dl>    | Igual que estado HTTP 407: se requiere autenticación proxy.<br/>                                                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="wu_e_pt_http_status_request_timeout"></span><dl> <dt>**Wu \_ E \_ PT \_ \_ tiempo de \_ \_ espera de solicitud de estado http**</dt> <dt>0x8024401C</dt> </dl>  | Igual que estado HTTP 408: se agotó el tiempo de espera del servidor mientras se esperaba la solicitud.<br/>                                                                                                           |
| <span id="WU_E_PT_HTTP_STATUS_CONFLICT"></span><span id="wu_e_pt_http_status_conflict"></span><dl> <dt>**Wu \_ E \_ PT \_ \_ \_ conflicto de estado http**</dt> <dt>0x8024401D</dt> </dl>                        | Igual que estado HTTP 409: la solicitud no se completó debido a un conflicto con el estado actual del recurso.<br/>                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_GONE"></span><span id="wu_e_pt_http_status_gone"></span><dl> <dt>**Wu \_ E \_ PT \_ \_ Estado HTTP \_**</dt> <dt>0x8024401E</dt> </dl>                                    | Igual que estado HTTP 410: el recurso solicitado ya no está disponible en el servidor.<br/>                                                                                                |
| <span id="WU_E_PT_HTTP_STATUS_SERVER_ERROR"></span><span id="wu_e_pt_http_status_server_error"></span><dl> <dt>**Wu \_ E \_ PT \_ http \_ de \_ \_ error del servidor de estado**</dt> <dt>0x8024401F</dt> </dl>           | Igual que estado HTTP 500: un error interno del servidor impidió que se completara la solicitud.<br/>                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_NOT_SUPPORTED"></span><span id="wu_e_pt_http_status_not_supported"></span><dl> <dt>**Wu \_ E \_ PT \_ \_ Estado HTTP \_ no \_ admitido**</dt> <dt>0x80244020</dt> </dl>        | Igual que estado HTTP 501: el servidor no admite la funcionalidad necesaria para completar la solicitud. <br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_BAD_GATEWAY"></span><span id="wu_e_pt_http_status_bad_gateway"></span><dl> <dt>**Wu \_ E \_ PT \_ http de estado http 0x80244021 de \_ puerta de \_ \_ enlace incorrecta**</dt> <dt></dt> </dl>              | Igual que estado HTTP 502: el servidor, mientras actuaba como puerta de enlace o proxy, recibió una respuesta no válida del servidor que precede en la cadena al que tuvo acceso al intentar completar la solicitud.<br/> |
| <span id="WU_E_PT_HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="wu_e_pt_http_status_service_unavail"></span><dl> <dt>**Wu \_ E \_ PT \_ servicio de estado http no \_ \_ \_ disponible**</dt> <dt>0x80244022</dt> </dl>  | Igual que estado HTTP 503: el servicio está sobrecargado temporalmente.<br/>                                                                                                                  |
| <span id="WU_E_PT_HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="wu_e_pt_http_status_gateway_timeout"></span><dl> <dt>**Wu \_ E \_ PT \_ http \_ de \_ estado \_**</dt> de <dt>0x80244023</dt> de tiempo de espera de puerta de enlace </dl>  | Igual que estado HTTP 504: se agotó el tiempo de espera de la solicitud mientras se esperaba una puerta de enlace.<br/>                                                                                                        |
| <span id="WU_E_PT_HTTP_STATUS_VERSION_NOT_SUP"></span><span id="wu_e_pt_http_status_version_not_sup"></span><dl> <dt>**Wu \_ E \_ PT \_ http \_ estado \_ versión \_ no \_**</dt> <dt>0x80244024</dt> SUP </dl> | Igual que estado HTTP 505: el servidor no admite la versión del protocolo HTTP usada para la solicitud.<br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_NOT_MAPPED"></span><span id="wu_e_pt_http_status_not_mapped"></span><dl> <dt>**Wu \_ E \_ PT \_ \_ Estado HTTP \_ no \_ asignado**</dt> <dt>0x8024402B</dt> </dl>                 | No se pudo completar la solicitud y el motivo no se corresponde con ninguno de los códigos de error http de WU \_ E \_ PT \_ \_ \* .<br/>                                                               |
| <span id="WU_E_PT_WINHTTP_NAME_NOT_RESOLVED"></span><span id="wu_e_pt_winhttp_name_not_resolved"></span><dl> <dt>**Wu \_ E \_ PT \_ \_ nombre WinHTTP \_ no \_ resuelto**</dt> <dt>0x8024402C</dt> </dl>        | Igual que \_ el error WinHTTP \_ nombre \_ no \_ resuelto: no se puede resolver el nombre del servidor proxy o el servidor de destino.<br/>                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wuerror. h</dt> </dl> |



 

 




