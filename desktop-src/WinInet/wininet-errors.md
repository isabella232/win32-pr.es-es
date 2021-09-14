---
title: Mensajes de error (Wininet.h)
description: Las funciones de WinINet devuelven códigos de error cuando corresponda. Los errores siguientes son específicos de las funciones de WinINet.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073125"
---
# <a name="error-messages-winineth"></a>Mensajes de error (Wininet.h)

Las funciones de WinINet devuelven códigos de error cuando corresponda. Los errores siguientes son específicos de las funciones de WinINet.

<dl> <dt>

<span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERROR \_ FTP \_ ELIMINADO**
</dt> <dd> <dl> <dt>

12111
</dt> <dt>



La operación FTP no se completó porque se anuló la sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERROR \_ FTP SIN MODO \_ \_ \_ PASIVO**
</dt> <dd> <dl> <dt>

12112
</dt> <dt>



El modo pasivo no está disponible en el servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERROR \_ TRANSFERENCIA FTP EN \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

12110
</dt> <dt>



La operación solicitada no se puede realizar en el identificador de sesión FTP porque ya hay una operación en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL ATRIBUTO \_ \_ \_ GOPHER**
</dt> <dd> <dl> <dt>

12137
</dt> <dt>



No se pudo encontrar el atributo solicitado.

> [!Note]  
> Windows XP y Windows Server 2003 R2 y versiones anteriores solo.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**ERROR \_ GOPHER \_ DATA \_ ERROR**
</dt> <dd> <dl> <dt>

12132
</dt> <dt>



Se detectó un error al recibir datos del servidor Gopher.

> [!Note]  
> Windows XP y Windows Server 2003 R2 y versiones anteriores solo.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERROR \_ GOPHER \_ END \_ OF \_ DATA**
</dt> <dd> <dl> <dt>

12133
</dt> <dt>



Se ha alcanzado el final de los datos.

> [!Note]  
> Windows XP y Windows Server 2003 R2 y versiones anteriores solo.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERROR \_ GOPHER \_ INCORRECT \_ LOCATOR \_ TYPE**
</dt> <dd> <dl> <dt>

12135
</dt> <dt>



El tipo del localizador no es correcto para esta operación.

> [!Note]  
> Windows XP y Windows Server 2003 R2 y versiones anteriores solo.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERROR \_ GOPHER \_ INVALID \_ LOCATOR**
</dt> <dd> <dl> <dt>

12134
</dt> <dt>



El localizador proporcionado no es válido.

> [!Note]  
> Windows XP y Windows Server 2003 R2 y versiones anteriores solo.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERROR \_ GOPHER \_ NOT \_ FILE**
</dt> <dd> <dl> <dt>

12131
</dt> <dt>



La solicitud debe realizarse para un localizador de archivos.

> [!Note]  
> Windows XP y Windows Server 2003 R2 y versiones anteriores solo.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERROR \_ GOPHER \_ NOT \_ GOPHER \_ PLUS**
</dt> <dd> <dl> <dt>

12136
</dt> <dt>



La operación solicitada solo se puede realizar en un servidor Gopher+ o con un localizador que especifique una operación Gopher+.

> [!Note]  
> Windows XP y Windows Server 2003 R2 y versiones anteriores solo.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**ERROR \_ DE PROTOCOLO GOPHER \_ \_**
</dt> <dd> <dl> <dt>

12130
</dt> <dt>



Se detectó un error al analizar los datos devueltos desde el servidor Gopher.

> [!Note]  
> Windows XP y Windows Server 2003 R2 y versiones anteriores solo.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERROR \_ GOPHER \_ UNKNOWN \_ LOCATOR**
</dt> <dd> <dl> <dt>

12138
</dt> <dt>



El tipo de localizador es desconocido.

> [!Note]  
> Windows XP y Windows Server 2003 R2 y versiones anteriores solo.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERROR \_ HTTP \_ COOKIE \_ RECHAZADA**
</dt> <dd> <dl> <dt>

12162
</dt> <dt>



El servidor rechazó la cookie HTTP.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERROR \_ HTTP \_ COOKIE \_ NEEDS \_ CONFIRMATION**
</dt> <dd> <dl> <dt>

12161
</dt> <dt>



La cookie HTTP requiere confirmación.

> [!Note]  
> Windows Vista y Windows Server 2008 y versiones anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERROR \_ HTTP \_ DOWNLEVEL \_ SERVER**
</dt> <dd> <dl> <dt>

12151
</dt> <dt>



El servidor no deseó ningún encabezado.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**EL \_ ENCABEZADO HTTP DE ERROR YA \_ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



No se pudo agregar el encabezado porque ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**ERROR \_ ENCABEZADO HTTP NO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



No se pudo encontrar el encabezado solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERROR \_ HTTP \_ INVALID \_ HEADER**
</dt> <dd> <dl> <dt>

12153
</dt> <dt>



El encabezado proporcionado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERROR \_ HTTP \_ INVALID \_ QUERY \_ REQUEST**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



La solicitud realizada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERROR \_ HTTP \_ INVALID \_ SERVER \_ RESPONSE**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



No se pudo analizar la respuesta del servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERROR \_ HTTP \_ NO \_ REDIRIGIDO**
</dt> <dd> <dl> <dt>

12160
</dt> <dt>



No se redirija la solicitud HTTP.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERROR \_ HTTP \_ REDIRECT \_ FAILED**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Error de redirección porque el esquema ha cambiado (por ejemplo, HTTP a FTP) o todos los intentos realizados para redirigir no se pudieron realizar (el valor predeterminado es cinco intentos).


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERROR \_ HTTP \_ REDIRECT \_ NEEDS \_ CONFIRMATION**
</dt> <dd> <dl> <dt>

12168
</dt> <dt>



El redireccionamiento requiere confirmación del usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERROR \_ INTERNET \_ ASYNC \_ THREAD \_ FAILED**
</dt> <dd> <dl> <dt>

12047
</dt> <dt>



La aplicación no pudo iniciar un subproceso asincrónico.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERROR \_ INTERNET \_ BAD \_ AUTO \_ PROXY \_ SCRIPT**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Se produjo un error en el script de configuración automática del proxy.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERROR \_ INTERNET \_ BAD \_ OPTION \_ LENGTH**
</dt> <dd> <dl> <dt>

12010
</dt> <dt>



La longitud de una opción proporcionada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) es incorrecta para el tipo de opción especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERROR \_ INTERNET \_ BAD \_ REGISTRY \_ PARAMETER**
</dt> <dd> <dl> <dt>

12022
</dt> <dt>



Se ha localizado un valor del Registro necesario, pero es un tipo incorrecto o tiene un valor no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERROR \_ INTERNET NO SE PUEDE \_ \_ CONECTAR**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Error al intentar conectarse al servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERROR \_ INTERNET \_ CHG \_ POST \_ IS \_ NON \_ SECURE**
</dt> <dd> <dl> <dt>

12042
</dt> <dt>



La aplicación está publicando e intentando cambiar varias líneas de texto en un servidor que no es seguro.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERROR \_ SE NECESITA EL CERTIFICADO DE \_ \_ AUTENTICACIÓN DE CLIENTE DE \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



El servidor solicita la autenticación de cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERROR: \_ NO SE HA CONFIGURADO LA \_ \_ AUTENTICACIÓN DE CLIENTE DE \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

12046
</dt> <dt>



La autorización de cliente no está configurada en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERROR DE \_ CONEXIÓN A INTERNET \_ \_ ANULADA**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



La conexión con el servidor ha finalizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERROR DE \_ \_ RESTABLECIMIENTO DE CONEXIÓN A \_ INTERNET**
</dt> <dd> <dl> <dt>

12031
</dt> <dt>



Se ha restablecido la conexión con el servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERROR AL \_ \_ DESCODAR INTERNET \_**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



WinINet no pudo realizar la decodificación de contenido en la respuesta. Para obtener más información, vea el [**tema Codificación de**](content-encoding.md) contenido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**CUADRO DE \_ DIÁLOGO DE INTERNET DE ERROR \_ \_ PENDIENTE**
</dt> <dd> <dl> <dt>

12049
</dt> <dt>



Otro subproceso tiene un cuadro de diálogo de contraseña en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERROR \_ INTERNET \_ DESCONECTADO**
</dt> <dd> <dl> <dt>

12163
</dt> <dt>



Se ha perdido la conexión a Internet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**ERROR \_ INTERNET \_ EXTENDED \_ ERROR**
</dt> <dd> <dl> <dt>

12003
</dt> <dt>



Se devolvió un error extendido desde el servidor. Suele ser una cadena o búfer que contiene un mensaje de error detallado. Llame [**a InternetGetLastResponseInfo para**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) recuperar el texto del error.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERROR \_ ERROR DE INTERNET \_ \_ DUETOSECURITYCHECK**
</dt> <dd> <dl> <dt>

12171
</dt> <dt>



Error en la función debido a una comprobación de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERROR \_ INTERNET \_ FORCE \_ RETRY**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



La función debe volver a hacer la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERROR \_ INTERNET \_ FORTEZZA \_ LOGIN \_ NEEDED**
</dt> <dd> <dl> <dt>

12054
</dt> <dt>



El recurso solicitado requiere la autenticación de Fortezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERROR EXISTE \_ EL IDENTIFICADOR DE INTERNET \_ \_**
</dt> <dd> <dl> <dt>

12036
</dt> <dt>



Error en la solicitud porque el identificador ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERROR \_ DE HTTP DE INTERNET A HTTPS EN \_ \_ \_ \_ \_ REDIR**
</dt> <dd> <dl> <dt>

12039
</dt> <dt>



La aplicación se está moviendo de un no SSL a una conexión SSL debido a una redirección.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERROR \_ INTERNET \_ HTTPS \_ HTTP \_ SUBMIT \_ REDIR**
</dt> <dd> <dl> <dt>

12052
</dt> <dt>



Los datos que se envían a una conexión SSL se redirigen a una conexión no SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERROR \_ HTTPS DE INTERNET A HTTP EN \_ \_ \_ \_ \_ REDIR**
</dt> <dd> <dl> <dt>

12040
</dt> <dt>



La aplicación se está moviendo de una conexión SSL a una conexión no SSL debido a una redirección.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERROR \_ DE FORMATO INCORRECTO DE \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

12027
</dt> <dt>



El formato de la solicitud no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERROR \_ ESTADO DE IDENTIFICADOR INCORRECTO DE \_ \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



No se puede realizar la operación solicitada porque el identificador proporcionado no está en el estado correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERROR \_ INTERNET INCORRECT HANDLE TYPE (TIPO DE IDENTIFICADOR INCORRECTO DE INTERNET DE \_ \_ \_ ERROR)**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



El tipo de identificador proporcionado es incorrecto para esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERROR \_ DE CONTRASEÑA INCORRECTA DE \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

12014
</dt> <dt>



No se pudo completar la solicitud de conexión e inicio de sesión en un servidor FTP porque la contraseña proporcionada es incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERROR \_ NOMBRE DE USUARIO INCORRECTO DE \_ \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

12013
</dt> <dt>



No se pudo completar la solicitud de conexión e inicio de sesión en un servidor FTP porque el nombre de usuario proporcionado es incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERROR \_ INTERNET \_ INSERT \_ CDROM**
</dt> <dd> <dl> <dt>

12053
</dt> <dt>



La solicitud requiere que se inserte un CD-ROM en la unidad de CD-ROM para localizar el recurso solicitado.

> [!Note]  
> Windows Vista y Windows Server 2008 y versiones anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**ERROR \_ ERROR INTERNO DE \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Se ha producido un error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERROR \_ INTERNET \_ INVALID \_ CA**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



La función no está familiar con la entidad de certificación que generó el certificado del servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERROR \_ OPERACIÓN DE INTERNET NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

12016
</dt> <dt>



La operación solicitada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERROR \_ INTERNET \_ INVALID \_ OPTION**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Una solicitud a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) especificó un valor de opción no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERROR \_ SOLICITUD DE PROXY NO VÁLIDA DE \_ \_ INTERNET \_**
</dt> <dd> <dl> <dt>

12033
</dt> <dt>



La solicitud al proxy no era válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERROR \_ DIRECCIÓN URL NO VÁLIDA DE \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



La dirección URL no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL ELEMENTO DE \_ \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

12028
</dt> <dt>



No se pudo encontrar el elemento solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERROR DE \_ INICIO DE SESIÓN DE INTERNET \_ \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Error en la solicitud de conexión e inicio de sesión en un servidor FTP.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERROR DE \_ INICIO DE SESIÓN DE INTERNET MOSTRAR CUERPO DE LA \_ \_ \_ \_ \_ ENTIDAD**
</dt> <dd> <dl> <dt>

12174
</dt> <dt>



El MS-Logoff de resumen se ha devuelto desde el sitio web. Este encabezado indica específicamente al paquete de resumen que purgue las credenciales para el dominio kerberos asociado. Este error solo se devolverá si se ha establecido la opción [INTERNET ERROR MASK LOGIN FAILURE DISPLAY ENTITY \_ \_ \_ \_ \_ \_ \_ BODY;](option-flags.md) de lo contrario, se devuelve **ERROR INTERNET LOGIN \_ \_ \_ FAILURE.**


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERROR \_ SEGURIDAD MIXTA DE INTERNET \_ \_**
</dt> <dd> <dl> <dt>

12041
</dt> <dt>



El contenido no es completamente seguro. Parte del contenido que se está visualizando puede haber procede de servidores no seguros.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERROR \_ NOMBRE DE INTERNET NO \_ \_ \_ RESUELTO**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



No se pudo resolver el nombre del servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERROR \_ INTERNET \_ NEED \_ MSN \_ SSPI \_ PKG**
</dt> <dd> <dl> <dt>

12173
</dt> <dt>



No implementado actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERROR \_ INTERNET \_ NEED \_ UI**
</dt> <dd> <dl> <dt>

12034
</dt> <dt>



Se ha solicitado una interfaz de usuario u otra operación de bloqueo.

> [!Note]  
> Windows Vista y Windows Server 2008 y versiones anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERROR \_ INTERNET \_ NO \_ CALLBACK**
</dt> <dd> <dl> <dt>

12025
</dt> <dt>



No se pudo realizar una solicitud asincrónica porque no se ha establecido una función de devolución de llamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERROR \_ INTERNET \_ NO \_ CONTEXT**
</dt> <dd> <dl> <dt>

12024
</dt> <dt>



No se pudo realizar una solicitud asincrónica porque se proporcionó un valor de contexto cero.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERROR \_ INTERNET \_ NO \_ DIRECT \_ ACCESS**
</dt> <dd> <dl> <dt>

12023
</dt> <dt>



En este momento no se puede realizar el acceso directo a la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERROR \_ INTERNET \_ NO \_ INICIALIZADO**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



No se ha producido la inicialización de la API de WinINet. Indica que aún no se ha llamado a una función de nivel superior, [**como InternetOpen.**](/windows/desktop/api/Wininet/nf-wininet-internetopena)


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERROR \_ INTERNET \_ NOT \_ PROXY \_ REQUEST**
</dt> <dd> <dl> <dt>

12020
</dt> <dt>



La solicitud no se puede realizar a través de un proxy.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERROR \_ OPERACIÓN DE INTERNET \_ \_ CANCELADA**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



La operación se canceló, normalmente porque el identificador en el que estaba funcionando la solicitud se cerró antes de que se completara la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERROR \_ INTERNET \_ OPTION \_ NOT \_ SETTABLE**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



No se puede establecer la opción solicitada, solo se consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERROR \_ INTERNET FUERA DE \_ \_ \_ IDENTIFICADORES**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



En este momento no se podrían generar más identificadores.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERROR \_ INTERNET \_ POST \_ IS \_ NON \_ SECURE**
</dt> <dd> <dl> <dt>

12043
</dt> <dt>



La aplicación está publicando datos en un servidor que no es seguro.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERROR \_ PROTOCOLO DE INTERNET NO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

12008
</dt> <dt>



No se pudo encontrar el protocolo solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERROR \_ AL QUE NO SE PUEDE ACCEDER AL SERVIDOR PROXY DE \_ \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

12165
</dt> <dt>



No se puede acceder al servidor proxy designado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERROR \_ INTERNET \_ REDIRECT \_ SCHEME \_ CHANGE**
</dt> <dd> <dl> <dt>

12048
</dt> <dt>



La función no pudo controlar el redireccionamiento porque el esquema cambió (por ejemplo, HTTP a FTP).


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL VALOR DEL REGISTRO DE \_ \_ \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

12021
</dt> <dt>



No se pudo encontrar un valor del Registro necesario.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**SOLICITUD DE \_ INTERNET DE ERROR \_ \_ PENDIENTE**
</dt> <dd> <dl> <dt>

12026
</dt> <dt>



No se pudo completar la operación necesaria porque una o varias solicitudes están pendientes.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**CUADRO DE \_ DIÁLOGO DE REINTENTO DE INTERNET DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

12050
</dt> <dt>



El cuadro de diálogo debe reinterse.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERROR \_ INTERNET \_ SEC \_ CERT \_ CN \_ INVALID**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



El nombre común del certificado SSL (campo de nombre de host) es incorrecto, por ejemplo, si escribió www.server.com y el nombre común del certificado indica www.different.com.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERROR \_ INTERNET \_ SEC \_ CERT \_ DATE \_ INVALID**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



La fecha de certificado SSL que se recibió del servidor es mala. El certificado ha expirado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**ERROR \_ ERRORES DE CERTIFICADO DE INTERNET \_ SEC \_ \_**
</dt> <dd> <dl> <dt>

12055
</dt> <dt>



El certificado SSL contiene errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERROR \_ INTERNET \_ SEC \_ CERT \_ NO \_ REV**
</dt> <dd> <dl> <dt>

12056
</dt> <dt>



No se revocó el certificado SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERROR \_ INTERNET \_ SEC \_ CERT \_ REV \_ FAILED**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Error de revocación del certificado SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERROR \_ INTERNET \_ SEC \_ CERT \_ REVOKED**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Se revocó el certificado SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERROR \_ INTERNET \_ SEC \_ INVALID \_ CERT**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



El certificado SSL no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**ERROR DE \_ CANAL DE SEGURIDAD DE \_ \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



La aplicación experimentó un error interno al cargar las bibliotecas SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERROR \_ INTERNET \_ SERVER \_ UNREACHABLE**
</dt> <dd> <dl> <dt>

12164
</dt> <dt>



El sitio web o servidor indicado no es accesible.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERROR \_ DE APAGADO DE \_ INTERNET**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



La compatibilidad con WinINet se está apagando o descargando.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERROR \_ \_ TCPIP DE INTERNET \_ \_ NO INSTALADO**
</dt> <dd> <dl> <dt>

12159
</dt> <dt>



No se carga la pila de protocolos necesaria y la aplicación no puede iniciar WinSock.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**ERROR \_ INTERNET \_ TIMEOUT**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



La solicitud ha agotado el tiempo de espera.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERROR \_ INTERNET \_ UNABLE \_ TO \_ CACHE \_ FILE**
</dt> <dd> <dl> <dt>

12158
</dt> <dt>



La función no pudo almacenar en caché el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERROR \_ INTERNET NO PUEDE DESCARGAR EL \_ \_ \_ \_ SCRIPT**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



No se pudo descargar el script de configuración automática del proxy. Se estableció la marca \_ INTERNET FLAG MUST CACHE \_ \_ \_ REQUEST.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERROR \_ INTERNET \_ UNRECOGNIZED \_ SCHEME**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



No se pudo reconocer el esquema de dirección URL o no se admite.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**IDENTIFICADOR \_ DE ERROR NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>



El identificador que se pasó a la API se ha invalidado o cerrado.

**Encabezado:** Declarado en Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR \_ MÁS \_ DATOS**
</dt> <dd> <dl> <dt>



More data is available (Hyper-V no pudo generar el conjunto de instantáneas de VSS para la máquina virtual: hay más datos disponibles).

**Encabezado:** Declarado en Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR \_ NO \_ MÁS \_ ARCHIVOS**
</dt> <dd> <dl> <dt>



No se han encontrado más archivos.

**Encabezado:** Declarado en Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR \_ NO \_ MÁS \_ ELEMENTOS**
</dt> <dd> <dl> <dt>



No se han encontrado más elementos.

**Encabezado:** Declarado en Winerror.h


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para implementaciones de servidor o servicios, use [Microsoft Windows servicios HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



 

