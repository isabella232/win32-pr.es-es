---
title: Windows Funciones de devolución de llamada de servicios web
description: Las devoluciones de llamada permiten a una aplicación llamar a una función definida en otra capa o nivel.
ms.assetid: 7398ec42-388a-494c-9fe4-5bd62aa009cb
keywords:
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a385ca21d00e8845f89bda0d9b04221a922ba421
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255998"
---
# <a name="windows-web-services-callback-functions"></a>Windows Funciones de devolución de llamada de servicios web

Las devoluciones de llamada permiten a una aplicación llamar a una función definida en otra capa o nivel. La aplicación registra el argumento de función como un controlador al que se llamará de forma asincrónica en un momento posterior según sea necesario. La devolución de llamada se invoca si la función se completa de forma asincrónica, lo que indica que la función se ha completado correctamente o se produce un error. No se llama a la devolución de llamada si la operación se completa de forma sincrónica.

La API Windows Web Services incluye las siguientes funciones de devolución de llamada:

-   [**WS \_ ABANDON \_ MESSAGE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)
-   [**WS \_ ABORT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)
-   [**WS \_ ABORT \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**WS \_ ACCEPT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**DEVOLUCIÓN DE \_ LLAMADA DE WS \_ ASYNC**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
-   [**WS \_ ASYNC \_ (FUNCIÓN)**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function)
-   [**DEVOLUCIÓN DE LLAMADA DE NOTIFICACIÓN DE WS \_ CERT \_ ISSUER \_ LIST \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_cert_issuer_list_notification_callback)
-   [**DEVOLUCIÓN DE \_ LLAMADA DE VALIDACIÓN DE \_ \_ CERTIFICADOS WS**](/windows/desktop/api/WebServices/nc-webservices-ws_certificate_validation_callback)
-   [**DEVOLUCIÓN DE LLAMADA DEL CANAL WS \_ CLOSE \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)
-   [**DEVOLUCIÓN DE LLAMADA DEL AGENTE DE ESCUCHA DE WS \_ \_ \_ CLOSE**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ CREATE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)
-   [**WS \_ CREATE \_ CHANNEL \_ FOR \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**WS \_ CREATE \_ DECODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)
-   [**WS \_ CREATE \_ ENCODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)
-   [**WS \_ CREATE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**DESCODIFICADOR WS \_ \_ DESCODIFICACIÓN \_ DE DEVOLUCIÓN DE LLAMADA**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)
-   [**DEVOLUCIÓN DE LLAMADA \_ \_ FINAL DEL \_ DESCODIFICADOR DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)
-   [**DEVOLUCIÓN DE LLAMADA \_ DEL TIPO DE CONTENIDO GET DEL \_ \_ \_ \_ DESCODIFICADOR DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback)
-   [**DEVOLUCIÓN DE LLAMADA \_ \_ DE INICIO DEL \_ DESCODIFICADOR DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)
-   [**DEVOLUCIÓN DE LLAMADA \_ DE \_ COMPARACIÓN DE \_ DURACIÓN DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**DEVOLUCIÓN DE \_ LLAMADA DE CADENA DINÁMICA \_ DE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**DEVOLUCIÓN DE \_ LLAMADA \_ DE CODIFICACIÓN DEL \_ CODIFICADOR WS**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)
-   [**DEVOLUCIÓN DE LLAMADA \_ DEL \_ EXTREMO DEL CODIFICADOR WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)
-   [**WS \_ ENCODER \_ GET \_ CONTENT \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback)
-   [**DEVOLUCIÓN DE \_ LLAMADA DE INICIO DEL \_ CODIFICADOR WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)
-   [**WS \_ FREE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)
-   [**DEVOLUCIÓN DE \_ LLAMADA DEL \_ \_ DESCODIFICADOR LIBRE DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)
-   [**WS \_ FREE \_ ENCODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)
-   [**WS \_ FREE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**WS \_ GET \_ CERT \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)
-   [**WS \_ GET \_ CHANNEL \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)
-   [**WS \_ GET \_ LISTENER \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**DEVOLUCIÓN DE \_ LLAMADA \_ DE REDIRECCIONAMIENTO HTTP \_ DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)
-   [**WS \_ IS \_ DEFAULT \_ VALUE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_is_default_value_callback)
-   [**DEVOLUCIÓN DE \_ LLAMADA DE WS MESSAGE \_ \_ DONE**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback)
-   [**WS \_ OPEN \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)
-   [**WS \_ OPEN \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**WS \_ OPERATION \_ CANCEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)
-   [**DEVOLUCIÓN DE \_ LLAMADA DE ESTADO LIBRE DE LA \_ \_ \_ OPERACIÓN WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)
-   [**DEVOLUCIÓN DE LLAMADA \_ DE MENSAJES DE PROXY \_ WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback)
-   [**DEVOLUCIÓN DE LLAMADA \_ \_ DE BYTES DE \_ EXTRACCIÓN DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**WS \_ PUSH \_ BYTES \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**WS \_ READ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)
-   [**WS \_ READ \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)
-   [**WS \_ READ \_ MESSAGE \_ START \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)
-   [**WS \_ READ \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**WS \_ RESET \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)
-   [**WS \_ RESET \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**WS \_ SERVICE \_ ACCEPT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback)
-   [**DEVOLUCIÓN DE \_ LLAMADA DEL CANAL DE CIERRE DEL \_ \_ \_ SERVICIO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)
-   [**DEVOLUCIÓN DE \_ LLAMADA DE RECEPCIÓN DE MENSAJES DEL \_ \_ \_ SERVICIO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**DEVOLUCIÓN DE LLAMADA \_ DE \_ SEGURIDAD DEL \_ SERVICIO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   [**DEVOLUCIÓN DE LLAMADA \_ DEL CÓDIGO AUXILIAR DEL \_ \_ SERVICIO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)
-   [**WS \_ SET \_ CHANNEL \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)
-   [**WS \_ SET \_ LISTENER \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)
-   [**WS \_ SHUTDOWN \_ SESSION \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)
-   [**WS \_ VALIDATE \_ PASSWORD \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback)
-   [**WS \_ VALIDATE \_ SAML \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)
-   [**WS \_ WRITE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)
-   [**WS \_ WRITE \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)
-   [**WS \_ WRITE \_ MESSAGE \_ START \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)
-   [**WS \_ WRITE \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

 

 




