---
title: Funciones de devolución de llamada de servicios Web de Windows
description: Las devoluciones de llamada permiten a una aplicación llamar a una función definida en otra capa o nivel.
ms.assetid: 7398ec42-388a-494c-9fe4-5bd62aa009cb
keywords:
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a385ca21d00e8845f89bda0d9b04221a922ba421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148763"
---
# <a name="windows-web-services-callback-functions"></a>Funciones de devolución de llamada de servicios Web de Windows

Las devoluciones de llamada permiten a una aplicación llamar a una función definida en otra capa o nivel. La aplicación registra el argumento de la función como un controlador que se va a llamar de forma asincrónica en un momento posterior, según sea necesario. Se invoca la devolución de llamada si la función se completa de forma asincrónica, lo que indica que la función se ha ejecutado correctamente o error. No se llama a la devolución de llamada si la operación se completa de forma sincrónica.

La API de servicios Web de Windows incluye las siguientes funciones de devolución de llamada:

-   [**\_devolución de \_ llamada de mensajes de abandono de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)
-   [**\_devolución de \_ llamada de canal de ANULAción WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)
-   [**\_devolución de \_ llamada de agente de escucha de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**\_devolución de \_ llamada de canal de aceptación de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**devolución de llamada de WS \_ Async \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
-   [**función de WS \_ Async \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function)
-   [**\_devolución de \_ llamada de \_ notificación de lista de emisores de \_ certificados \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_cert_issuer_list_notification_callback)
-   [**\_devolución de \_ llamada de validación de certificado WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_certificate_validation_callback)
-   [**\_devolución de \_ llamada de canal de cierre WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)
-   [**\_devolución de \_ llamada del agente de escucha de WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**\_devolución de \_ llamada de canal de creación WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)
-   [**WS \_ Create \_ Channel \_ para \_ devolución de llamada del agente de escucha \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**\_devolución de \_ llamada del descodificador de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)
-   [**\_devolución de \_ llamada del codificador de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)
-   [**\_devolución de \_ llamada de agente de escucha de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**devolución de llamada de descodificación de WS \_ DEScodificador \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)
-   [**devolución de llamada de final del \_ DEScodificador de WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)
-   [**devolución de llamada de \_ \_ tipo de \_ contenido de \_ decodificador WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback)
-   [**devolución de llamada de inicio del \_ DEScodificador de WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)
-   [**\_devolución de \_ llamada de comparación de WS Duration \_**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**\_devolución de \_ llamada de cadena dinámica de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**devolución de llamada de codificación de WS \_ Encoder \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)
-   [**devolución de llamada de final del \_ codificador de WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)
-   [**devolución de llamada de \_ \_ tipo de contenido get del codificador de WS \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback)
-   [**devolución de llamada de inicio del \_ codificador WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)
-   [**\_devolución de \_ llamada de canal gratis de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)
-   [**\_devolución de \_ llamada del descodificador gratuito de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)
-   [**\_devolución de \_ llamada del codificador gratis de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)
-   [**\_devolución de \_ llamada de agente de escucha gratuito de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**devolución de llamada de WS \_ Get \_ CERT \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)
-   [**devolución de llamada de la propiedad de canal WS \_ Get \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)
-   [**\_devolución de \_ llamada de \_ propiedad de agente de escucha de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**\_devolución de \_ llamada de redirección http de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)
-   [**\_devolución de \_ \_ llamada de valor predeterminado \_ de WS**](/windows/desktop/api/WebServices/nc-webservices-ws_is_default_value_callback)
-   [**\_devolución de \_ \_ llamada de mensaje WS**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback)
-   [**\_devolución de \_ llamada de canal abierto de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)
-   [**\_devolución de \_ llamada de agente de escucha abierto WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**\_devolución de \_ llamada de cancelación de operación WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)
-   [**\_devolución de \_ \_ llamada de estado libre de operación WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)
-   [**\_devolución de \_ llamada de mensaje de proxy WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback)
-   [**\_devolución de \_ llamada de bytes de extracción de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**\_devolución de \_ llamada de bytes de inserciones de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**devolución de llamada de \_ lectura de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)
-   [**\_devolución de \_ llamada de final del mensaje \_ \_ de WS**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)
-   [**\_devolución de \_ llamada de inicio de mensaje \_ \_ de WS**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)
-   [**\_devolución de \_ llamada de tipo de lectura de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**\_devolución de \_ llamada de canal de restablecimiento de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)
-   [**\_devolución de \_ llamada del agente de escucha de WS RESET \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**servicio WS- \_ \_ devolución de \_ llamada de canal \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback)
-   [**\_devolución de \_ llamada de canal de cierre de servicio WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)
-   [**\_devolución de \_ llamada de recepción de mensaje del servicio WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**\_devolución de \_ llamada de seguridad del servicio WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   [**\_devolución de \_ llamada de stub de servicio WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)
-   [**\_devolución de \_ llamada de propiedad de canal \_ \_ de WS**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)
-   [**\_devolución de \_ llamada de \_ propiedad del agente de escucha de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)
-   [**\_devolución de \_ llamada de canal de sesión de cierre de \_ WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)
-   [**devolución de llamada de validación de contraseña de WS \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback)
-   [**\_devolución de \_ llamada de SAML Validate de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)
-   [**devolución de llamada de WS- \_ Write \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)
-   [**\_devolución de \_ llamada de final del mensaje de escritura de \_ WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)
-   [**\_devolución de \_ llamada de inicio del mensaje de escritura de \_ WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)
-   [**\_devolución de \_ llamada de tipo de escritura de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

 

 




