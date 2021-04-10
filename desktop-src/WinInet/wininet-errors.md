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
# <a name="error-messages-winineth"></a>Mensajes de error (Wininet. h)

Las funciones WinINet devuelven códigos de error cuando corresponda. Los errores siguientes son específicos de las funciones de WinINet.

<dl> <dt>

<span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERROR de \_ FTP \_ eliminado**
</dt> <dd> <dl> <dt>

12111
</dt> <dt>



No se completó la operación FTP porque se anuló la sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERROR \_ FTP \_ no \_ \_ modo pasivo**
</dt> <dd> <dl> <dt>

12112
</dt> <dt>



El modo pasivo no está disponible en el servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERROR \_ \_ en la transferencia FTP \_ en \_ curso**
</dt> <dd> <dl> <dt>

12110
</dt> <dt>



No se puede realizar la operación solicitada en el identificador de sesión FTP porque ya hay una operación en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**\_ \_ \_ no \_ se encontró el atributo Gopher de error**
</dt> <dd> <dl> <dt>

12137
</dt> <dt>



No se pudo encontrar el atributo solicitado.

> [!Note]  
> Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**error \_ de \_ datos de Gopher \_**
</dt> <dd> <dl> <dt>

12132
</dt> <dt>



Se detectó un error al recibir datos del servidor gopher.

> [!Note]  
> Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERROR \_ \_ de fin \_ de \_ datos de Gopher**
</dt> <dd> <dl> <dt>

12133
</dt> <dt>



Se ha alcanzado el final de los datos.

> [!Note]  
> Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERROR \_ de \_ \_ tipo de localizador incorrecto de Gopher \_**
</dt> <dd> <dl> <dt>

12135
</dt> <dt>



El tipo del localizador no es correcto para esta operación.

> [!Note]  
> Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERROR \_ de \_ localizador Gopher no válido \_**
</dt> <dd> <dl> <dt>

12134
</dt> <dt>



El localizador proporcionado no es válido.

> [!Note]  
> Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERROR: \_ Gopher no es un \_ \_ archivo**
</dt> <dd> <dl> <dt>

12131
</dt> <dt>



La solicitud se debe realizar para un localizador de archivos.

> [!Note]  
> Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERROR \_ Gopher \_ no \_ Gopher \_ Plus**
</dt> <dd> <dl> <dt>

12136
</dt> <dt>



La operación solicitada solo se puede realizar en un servidor gopher + o con un localizador que especifique una operación Gopher +.

> [!Note]  
> Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**error \_ de \_ Protocolo \_ Gopher**
</dt> <dd> <dl> <dt>

12130
</dt> <dt>



Se detectó un error al analizar los datos devueltos desde el servidor gopher.

> [!Note]  
> Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**\_localizador de error Gopher \_ desconocido \_**
</dt> <dd> <dl> <dt>

12138
</dt> <dt>



Se desconoce el tipo de localizador.

> [!Note]  
> Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERROR \_ de \_ cookie HTTP \_ rechazada**
</dt> <dd> <dl> <dt>

12162
</dt> <dt>



El servidor rechazó la cookie HTTP.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERROR \_ la \_ cookie HTTP \_ requiere \_ confirmación**
</dt> <dd> <dl> <dt>

12161
</dt> <dt>



La cookie HTTP requiere confirmación.

> [!Note]  
> Windows Vista y Windows Server 2008 y versiones anteriores solo.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERROR \_ de \_ servidor de nivel inferior http \_**
</dt> <dd> <dl> <dt>

12151
</dt> <dt>



El servidor no devolvió ningún encabezado.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**el \_ encabezado HTTP de error \_ \_ ya \_ existe**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



No se pudo agregar el encabezado porque ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**\_ \_ \_ no \_ se encontró el encabezado HTTP de error**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



No se pudo encontrar el encabezado solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERROR en el \_ \_ encabezado HTTP no válido \_**
</dt> <dd> <dl> <dt>

12153
</dt> <dt>



El encabezado proporcionado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERROR \_ de \_ \_ solicitud de consulta no válida http \_**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



La solicitud realizada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERROR \_ de \_ \_ respuesta del servidor HTTP no válida \_**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



No se pudo analizar la respuesta del servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERROR \_ \_ no \_ Redirigido http**
</dt> <dd> <dl> <dt>

12160
</dt> <dt>



No se redirigió la solicitud HTTP.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERROR \_ de \_ redirección \_ http**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Se produjo un error en el redireccionamiento porque el esquema ha cambiado (por ejemplo, HTTP a FTP) o todos los intentos de redirigir el error (el valor predeterminado es cinco intentos).


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERROR \_ el \_ redireccionamiento http \_ necesita \_ confirmación**
</dt> <dd> <dl> <dt>

12168
</dt> <dt>



La redirección requiere confirmación del usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERROR \_ de \_ \_ subproceso asincrónico de Internet \_**
</dt> <dd> <dl> <dt>

12047
</dt> <dt>



La aplicación no pudo iniciar un subproceso asincrónico.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERROR en el \_ \_ \_ script de proxy automático incorrecto \_ \_ de Internet**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Se produjo un error en el script de configuración automática del proxy.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERROR \_ de \_ \_ longitud de opción incorrecta de Internet \_**
</dt> <dd> <dl> <dt>

12010
</dt> <dt>



La longitud de una opción proporcionada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) no es correcta para el tipo de opción especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**\_parámetro de \_ error \_ del registro de Internet incorrecto \_**
</dt> <dd> <dl> <dt>

12022
</dt> <dt>



Se encontró un valor de registro necesario, pero es de un tipo incorrecto o tiene un valor no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERROR \_ Internet \_ no se puede \_ conectar**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Error al intentar conectarse al servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERROR el \_ envío de correo de Internet \_ \_ \_ \_ no es \_ seguro**
</dt> <dd> <dl> <dt>

12042
</dt> <dt>



La aplicación está publicando e intentando cambiar varias líneas de texto en un servidor que no es seguro.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERROR \_ de \_ certificado de autenticación de cliente de Internet \_ \_ \_ necesario**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



El servidor está solicitando la autenticación del cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERROR \_ \_ no se \_ \_ ha \_ configurado la autenticación de cliente de Internet**
</dt> <dd> <dl> <dt>

12046
</dt> <dt>



La autorización del cliente no está configurada en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERROR \_ de \_ conexión a Internet \_ anulada**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



La conexión con el servidor ha finalizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERROR \_ de \_ restablecimiento de conexión a Internet \_**
</dt> <dd> <dl> <dt>

12031
</dt> <dt>



Se ha restablecido la conexión con el servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERROR \_ de \_ descodificación de Internet \_**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



WinINet no pudo realizar la descodificación de contenido en la respuesta. Para obtener más información, vea el tema sobre [**codificación de contenido**](content-encoding.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**ERROR en el \_ cuadro de diálogo de Internet \_ \_ pendiente**
</dt> <dd> <dl> <dt>

12049
</dt> <dt>



Otro subproceso tiene un cuadro de diálogo de contraseña en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERROR de \_ Internet \_ desconectado**
</dt> <dd> <dl> <dt>

12163
</dt> <dt>



Se perdió la conexión a Internet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**error de error \_ extendido de Internet \_ \_**
</dt> <dd> <dl> <dt>

12003
</dt> <dt>



Se devolvió un error extendido desde el servidor. Suele ser una cadena o un búfer que contiene un mensaje de error detallado. Llame a [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) para recuperar el texto del error.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERROR \_ de \_ Internet \_ DUETOSECURITYCHECK**
</dt> <dd> <dl> <dt>

12171
</dt> <dt>



Error de la función debido a una comprobación de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERROR \_ de \_ reintento de Internet Force \_**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



La función debe rehacer la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERROR \_ de \_ Inicio de sesión de Fortezza de Internet \_ \_ necesario**
</dt> <dd> <dl> <dt>

12054
</dt> <dt>



El recurso solicitado requiere autenticación Fortezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERROR \_ el \_ identificador de Internet \_ existe**
</dt> <dd> <dl> <dt>

12036
</dt> <dt>



No se pudo realizar la solicitud porque el identificador ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERROR \_ de Internet de \_ http \_ a \_ https \_ en \_ redir**
</dt> <dd> <dl> <dt>

12039
</dt> <dt>



La aplicación se mueve de una conexión que no es SSL a una conexión SSL debido a una redirección.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERROR \_ de \_ envío de http de \_ envío http de HTTPS de \_ Internet \_**
</dt> <dd> <dl> <dt>

12052
</dt> <dt>



Los datos que se envían a una conexión SSL se redirigen a una conexión que no es SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERROR \_ \_ de Internet HTTPS \_ a \_ http \_ en \_ redir**
</dt> <dd> <dl> <dt>

12040
</dt> <dt>



La aplicación se mueve de un SSL a una conexión que no es SSL debido a una redirección.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERROR de Internet con un \_ \_ \_ formato incorrecto**
</dt> <dd> <dl> <dt>

12027
</dt> <dt>



El formato de la solicitud no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERROR \_ de \_ \_ Estado de identificador incorrecto de Internet \_**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



No se puede realizar la operación solicitada porque el identificador proporcionado no tiene el estado correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERROR \_ de \_ \_ tipo de identificador incorrecto de Internet \_**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



El tipo de identificador proporcionado no es correcto para esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERROR de \_ Internet: \_ \_ contraseña incorrecta**
</dt> <dd> <dl> <dt>

12014
</dt> <dt>



No se pudo completar la solicitud de conexión e inicio de sesión en un servidor FTP porque la contraseña proporcionada es incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERROR \_ de \_ \_ nombre de usuario incorrecto de Internet \_**
</dt> <dd> <dl> <dt>

12013
</dt> <dt>



No se pudo completar la solicitud de conexión e inicio de sesión en un servidor FTP porque el nombre de usuario proporcionado no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERROR de \_ Internet \_ Insert \_ CDROM**
</dt> <dd> <dl> <dt>

12053
</dt> <dt>



La solicitud requiere que se inserte un CD-ROM en la unidad de CD-ROM para localizar el recurso solicitado.

> [!Note]  
> Windows Vista y Windows Server 2008 y versiones anteriores solo.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**error interno de ERROR de \_ Internet \_ \_**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Se ha producido un error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERROR \_ de \_ CA no válida de Internet \_**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



La función no está familiarizada con la entidad de certificación que generó el certificado del servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERROR en una \_ \_ operación no válida de Internet \_**
</dt> <dd> <dl> <dt>

12016
</dt> <dt>



La operación solicitada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERROR \_ de \_ opción no válida de Internet \_**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Una solicitud a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) especificó un valor de opción no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERROR \_ de \_ \_ solicitud de proxy no válida de Internet \_**
</dt> <dd> <dl> <dt>

12033
</dt> <dt>



La solicitud al proxy no era válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERROR \_ de \_ dirección URL no válida de Internet \_**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



La dirección URL no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERROR \_ \_ \_ no \_ se encontró el elemento de Internet**
</dt> <dd> <dl> <dt>

12028
</dt> <dt>



No se encontró el elemento solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERROR \_ de \_ Inicio de sesión en Internet \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Error en la solicitud de conexión e inicio de sesión en un servidor FTP.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERROR de \_ Inicio de sesión en Internet \_ \_ \_ Mostrar \_ cuerpo de entidad \_**
</dt> <dd> <dl> <dt>

12174
</dt> <dt>



El encabezado de Resumen de MS-Logoff se ha devuelto desde el sitio Web. Este encabezado indica específicamente el paquete de síntesis para purgar las credenciales del territorio asociado. Este error solo se devolverá si se ha establecido la opción error de [Inicio de sesión para mostrar el \_ \_ \_ \_ \_ \_ \_ cuerpo](option-flags.md) de la entidad en Internet. de lo contrario, se devolverá **un error de \_ Inicio de \_ sesión \_ de Internet** .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERROR \_ de \_ seguridad mixta de Internet \_**
</dt> <dd> <dl> <dt>

12041
</dt> <dt>



El contenido no es totalmente seguro. Es posible que parte del contenido que se está viendo proviene de servidores no seguros.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERROR \_ de \_ nombre de Internet \_ no \_ resuelto**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



No se pudo resolver el nombre del servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERROR de \_ Internet: \_ \_ \_ paquete SSPI de MSN \_**
</dt> <dd> <dl> <dt>

12173
</dt> <dt>



No implementado actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERROR de Internet con la \_ \_ interfaz de \_ usuario**
</dt> <dd> <dl> <dt>

12034
</dt> <dt>



Se ha solicitado una interfaz de usuario u otra operación de bloqueo.

> [!Note]  
> Windows Vista y Windows Server 2008 y versiones anteriores solo.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERROR de \_ Internet \_ sin devolución de \_ llamada**
</dt> <dd> <dl> <dt>

12025
</dt> <dt>



No se pudo realizar una solicitud asincrónica porque no se ha establecido una función de devolución de llamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERROR de \_ Internet \_ sin \_ contexto**
</dt> <dd> <dl> <dt>

12024
</dt> <dt>



No se pudo realizar una solicitud asincrónica porque se proporcionó un valor de contexto cero.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERROR \_ de \_ Internet \_ sin \_ acceso directo**
</dt> <dd> <dl> <dt>

12023
</dt> <dt>



No se puede realizar el acceso directo a la red en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERROR \_ Internet \_ no \_ inicializado**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



No se ha producido la inicialización de la API WinINet. Indica que aún no se ha llamado a una función de nivel superior, como [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERROR \_ de \_ \_ solicitud de proxy \_ de Internet**
</dt> <dd> <dl> <dt>

12020
</dt> <dt>



No se puede realizar la solicitud a través de un proxy.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERROR \_ de \_ operación de Internet \_ cancelada**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



La operación se canceló, normalmente porque el identificador en el que estaba funcionando la solicitud se cerró antes de que se completara la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERROR \_ de \_ opción de Internet \_ no \_ configurable**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



No se puede establecer la opción solicitada, solo se consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERROR \_ \_ de Internet \_ sin \_ identificadores**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



No se pueden generar más identificadores en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERROR: la \_ publicación en Internet \_ \_ \_ no es \_ segura**
</dt> <dd> <dl> <dt>

12043
</dt> <dt>



La aplicación está publicando datos en un servidor que no es seguro.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERROR \_ de \_ Protocolo de Internet \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

12008
</dt> <dt>



No se pudo encontrar el protocolo solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERROR no se \_ \_ \_ \_ puede tener acceso al servidor proxy de Internet**
</dt> <dd> <dl> <dt>

12165
</dt> <dt>



No se puede establecer contacto con el servidor proxy designado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERROR \_ de \_ cambio de esquema de redirección de Internet \_ \_**
</dt> <dd> <dl> <dt>

12048
</dt> <dt>



La función no pudo controlar el redireccionamiento porque el esquema ha cambiado (por ejemplo, HTTP a FTP).


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró el valor del registro de Internet**
</dt> <dd> <dl> <dt>

12021
</dt> <dt>



No se pudo encontrar un valor del registro requerido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**ERROR \_ de \_ solicitud de Internet \_ pendiente**
</dt> <dd> <dl> <dt>

12026
</dt> <dt>



No se pudo completar la operación necesaria porque una o varias solicitudes están pendientes.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**cuadro de diálogo ERROR de \_ \_ reintento de Internet \_**
</dt> <dd> <dl> <dt>

12050
</dt> <dt>



Se debe reintentar el cuadro de diálogo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERROR \_ de \_ \_ certificado CN de Internet \_ \_ no válido**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



El nombre común del certificado SSL (campo Nombre de host) es incorrecto por ejemplo, si escribió www.server.com y el nombre común en el certificado indica www.different.com.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERROR la \_ fecha de certificado de Internet \_ s \_ \_ \_ no es válida**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



La fecha del certificado SSL que se recibió del servidor es incorrecta. El certificado ha expirado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**errores de certificado de ERROR de \_ Internet \_ s \_ \_**
</dt> <dd> <dl> <dt>

12055
</dt> <dt>



El certificado SSL contiene errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERROR de Internet en el \_ \_ \_ certificado. \_ no \_ Rev**
</dt> <dd> <dl> <dt>

12056
</dt> <dt>



No se revocó el certificado SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERROR de ERROR de \_ revisión de certificado por Internet \_ s \_ \_ \_**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



No se pudo revocar el certificado SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERROR \_ Internet \_ s \_ certificado \_ revocado**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Se revocó el certificado SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERROR en \_ Internet: \_ \_ certificado no válido \_**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



El certificado SSL no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**error \_ de \_ canal de seguridad de Internet error \_ \_**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



La aplicación experimentó un error interno al cargar las bibliotecas SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERROR \_ de \_ servidor de Internet \_ inaccesible**
</dt> <dd> <dl> <dt>

12164
</dt> <dt>



No se puede tener acceso al sitio web o servidor indicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERROR \_ de \_ apagado por Internet**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



La compatibilidad con WinINet se está cerrando o descargando.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERROR de \_ Internet \_ TCPIP \_ no \_ instalado**
</dt> <dd> <dl> <dt>

12159
</dt> <dt>



La pila de protocolos necesaria no está cargada y la aplicación no puede iniciar WinSock.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**ERROR \_ de \_ tiempo de espera de Internet**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



La solicitud ha agotado el tiempo de espera.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERROR: \_ Internet \_ no puede \_ almacenar en caché el \_ \_ archivo**
</dt> <dd> <dl> <dt>

12158
</dt> <dt>



La función no pudo almacenar en caché el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERROR \_ Internet \_ no se puede \_ \_ descargar el \_ script**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



No se pudo descargar el script de configuración automática del proxy. La marca de INTERNET \_ \_ debe \_ almacenar la marca de solicitud en caché \_ .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERROR \_ : \_ esquema desconocido de Internet \_**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



No se reconoció el esquema de la dirección URL o no se admite.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR \_ de \_ identificador no válido**
</dt> <dd> <dl> <dt>



El identificador que se pasó a la API se ha invalidado o cerrado.

**Encabezado:** Declarado en Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR \_ más \_ datos**
</dt> <dd> <dl> <dt>



More data is available (Hyper-V no pudo generar el conjunto de instantáneas de VSS para la máquina virtual: hay más datos disponibles).

**Encabezado:** Declarado en Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR: \_ no hay \_ más \_ archivos**
</dt> <dd> <dl> <dt>



No se encontraron más archivos.

**Encabezado:** Declarado en Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**\_no hay \_ más \_ elementos de error**
</dt> <dd> <dl> <dt>



No se han encontrado más elementos.

**Encabezado:** Declarado en Winerror. h


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



 

