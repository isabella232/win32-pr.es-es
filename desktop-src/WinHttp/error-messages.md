---
description: GetLastError devuelve los valores de error identificados en este tema cuando se produce un error en una de las funciones Windows Servicios HTTP de Microsoft (WinHTTP).
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Mensajes de error (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160547"
---
# <a name="error-messages-winhttph"></a>Mensajes de error (Winhttp.h)

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los valores de error que se enumeran a continuación cuando se produce un error en una de las funciones de servicios HTTP de Microsoft Windows (WinHTTP) y también se devuelven en los 16 bits inferiores del error [**HRESULT**](../com/structure-of-com-error-codes.md) devueltos desde el [**objeto WinHttpRequest.**](winhttprequest.md)

Los valores de error cuyos nombres comienzan por "ERROR \_ \_ WINHTTP" son específicos de las funciones WinHTTP. Las funciones WinHTTP también devuelven Windows de error cuando corresponda.

<dl> <dt>

<span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERROR \_ WINHTTP \_ AUTO \_ PROXY \_ SERVICE \_ ERROR**
</dt> <dd> <dl> <dt>

12178
</dt> <dt>



Lo devuelve [**WinHttpGetProxyForUrl cuando**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) no se encuentra un proxy para la dirección URL especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERROR \_ WINHTTP \_ AUTODETECTION \_ FAILED**
</dt> <dd> <dl> <dt>

12180
</dt> <dt>



Lo devuelve [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) si WinHTTP no pudo detectar la dirección URL del archivo de configuración automática de proxy (PAC).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERROR \_ WINHTTP \_ BAD \_ AUTO \_ PROXY \_ SCRIPT**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Se produjo un error al ejecutar el código de script en el archivo de configuración automática de proxy (PAC).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERROR \_ WINHTTP \_ CANNOT \_ CALL \_ AFTER \_ OPEN**
</dt> <dd> <dl> <dt>

12103
</dt> <dt>



Devuelto por el [**objeto HttpRequest**](winhttprequest.md) si no se puede solicitar una opción especificada después [**de**](iwinhttprequest-open.md) llamar al método Open.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERROR \_ WINHTTP \_ CANNOT \_ CALL \_ AFTER \_ SEND**
</dt> <dd> <dl> <dt>

12102
</dt> <dt>



Devuelto por el [**objeto HttpRequest**](winhttprequest.md) si no se puede realizar una operación solicitada después de llamar al [**método Send.**](iwinhttprequest-send.md)


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERROR \_ WINHTTP \_ CANNOT \_ CALL \_ BEFORE \_ OPEN**
</dt> <dd> <dl> <dt>

12100
</dt> <dt>



Devuelto por el [**objeto HttpRequest**](winhttprequest.md) si no se puede realizar una operación solicitada antes de llamar al [**método Open.**](iwinhttprequest-open.md)


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERROR \_ WINHTTP \_ CANNOT \_ CALL \_ BEFORE \_ SEND**
</dt> <dd> <dl> <dt>

12101
</dt> <dt>



Devuelto por el [**objeto HttpRequest**](winhttprequest.md) si no se puede realizar una operación solicitada antes de llamar al [**método Send.**](iwinhttprequest-send.md)


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERROR \_ WINHTTP \_ CANNOT \_ CONNECT**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Se devuelve si se ha podido conectar al servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR \_ WINHTTP \_ CLIENT \_ AUTH \_ CERT \_ NEEDED**
</dt> <dd> <dl> <dt>



El servidor requiere autenticación de cliente SSL. La aplicación recupera la lista de emisores de certificados mediante una llamada [**a WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con la opción **\_ WINHTTP OPTION \_ CLIENT CERT \_ \_ ISSUER \_ LIST.** Para obtener más información, vea la **opción WINHTTP \_ OPTION CLIENT \_ CERT \_ \_ ISSUER \_ LIST.**

Si el servidor solicita el certificado de cliente, pero no lo requiere, la aplicación puede llamar alternativamente a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la opción **\_ WINHTTP OPTION \_ CLIENT CERT \_ \_ CONTEXT.** En este caso, la aplicación especifica la macro WINHTTP NO CLIENT CERT CONTEXT en el parámetro \_ \_ \_ \_ *lpBuffer* **de WinHttpSetOption**. Para obtener más información, vea la **opción WINHTTP \_ OPTION CLIENT \_ CERT \_ \_ CONTEXT.**

**Windows Server 2003 con SP1 y Windows XP con SP2:** Este error no se admite.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERROR \_ WINHTTP \_ CLIENT \_ CERT \_ NO \_ ACCESS \_ PRIVATE \_ KEY**
</dt> <dd> <dl> <dt>



La aplicación no tiene los privilegios necesarios para acceder a la clave privada asociada al certificado de cliente.

**Windows Server 2003 con SP1 y Windows XP con SP2:** Este error no se admite.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERROR \_ WINHTTP \_ CLIENT \_ CERT \_ NO \_ PRIVATE \_ KEY**
</dt> <dd> <dl> <dt>



El contexto del certificado de cliente SSL no tiene una clave privada asociada. Es posible que el certificado de cliente se haya importado al equipo sin la clave privada.

**Windows Server 2003 con SP1 y Windows XP con SP2:** Este error no se admite.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERROR \_ WINHTTP \_ CHUNKED \_ ENCODING \_ HEADER \_ SIZE \_ OVERFLOW**
</dt> <dd> <dl> <dt>

12183
</dt> <dt>



[**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve cuando se encuentra una condición de desbordamiento durante el análisis de la codificación fragmentada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR \_ WINHTTP \_ CLIENT \_ AUTH \_ CERT \_ NEEDED**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



[**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) lo devuelve cuando el servidor solicita la autenticación de cliente.

**Windows Server 2003 con SP1 y Windows XP con SP2:** Este error no se admite.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**ERROR \_ DE CONEXIÓN WINHTTP \_ \_**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



La conexión con el servidor se ha restablecido o finalizado, o se encontró un protocolo SSL incompatible. Por ejemplo, la versión 5.1 de WinHTTP no admite SSL2 a menos que el cliente lo permita específicamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**EL ENCABEZADO WINHTTP DE ERROR \_ \_ YA \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Obsoleto; ya no se usa.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERROR \_ WINHTTP \_ HEADER \_ COUNT \_ EXCEEDED**
</dt> <dd> <dl> <dt>

12181
</dt> <dt>



Lo devuelve [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) cuando había un número mayor de encabezados presentes en una respuesta de la que WinHTTP podía recibir.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL ENCABEZADO \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



No se puede encontrar el encabezado solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERROR \_ WINHTTP \_ HEADER \_ SIZE \_ OVERFLOW**
</dt> <dd> <dl> <dt>

12182
</dt> <dt>



[**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve cuando el tamaño de los encabezados recibidos supera el límite del identificador de solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERROR \_ WINHTTP \_ ESTADO DE IDENTIFICADOR \_ \_ INCORRECTO**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



La operación solicitada no se puede llevar a cabo porque el identificador proporcionado no está en el estado correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERROR \_ WINHTTP \_ INCORRECT \_ HANDLE \_ TYPE**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



El tipo de identificador proporcionado es incorrecto para esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**ERROR \_ WINHTTP \_ INTERNAL \_ ERROR**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Se ha producido un error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERROR \_ WINHTTP \_ INVALID \_ OPTION**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Una solicitud a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) especificó un valor de opción no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERROR \_ WINHTTP \_ INVALID \_ QUERY \_ REQUEST**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



Obsoleto; ya no se usa.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERROR \_ WINHTTP \_ INVALID \_ SERVER \_ RESPONSE**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



No se puede analizar la respuesta del servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERROR \_ WINHTTP \_ DIRECCIÓN URL NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



La URL no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERROR \_ DE INICIO DE SESIÓN \_ WINHTTP \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Error en el intento de inicio de sesión. Cuando se produce este error, el identificador de solicitud debe cerrarse [**con WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle). Se debe crear un nuevo identificador de solicitud antes de reintentar la función que generó originalmente este error.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERROR \_ WINHTTP \_ NAME \_ NOT \_ RESOLVED**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



No se puede resolver el nombre del servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERROR \_ WINHTTP \_ NO \_ INICIALIZADO**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Obsoleto; ya no se usa.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERROR \_ OPERACIÓN WINHTTP \_ \_ CANCELADA**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



La operación se canceló, normalmente porque el identificador en el que estaba funcionando la solicitud se cerró antes de que se completara la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERROR \_ WINHTTP \_ OPTION \_ NOT \_ SETTABLE**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



No se puede establecer la opción solicitada, solo se consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERROR \_ WINHTTP \_ FUERA DE \_ \_ IDENTIFICADORES**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Obsoleto; ya no se usa.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERROR \_ WINHTTP \_ REDIRECT \_ FAILED**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



No se pudo realizar el redireccionamiento porque el esquema cambió o todos los intentos realizados para redirigir no se pudieron realizar (el valor predeterminado es cinco intentos).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERROR \_ WINHTTP \_ RESEND \_ REQUEST**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



Error en la función WinHTTP. La función deseada se puede reinterír en el mismo identificador de solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERROR \_ WINHTTP \_ RESPONSE \_ DRAIN \_ OVERFLOW**
</dt> <dd> <dl> <dt>

12184
</dt> <dt>



Se devuelve cuando una respuesta entrante supera un límite de tamaño interno de WinHTTP.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**ERROR \_ WINHTTP \_ SCRIPT \_ EXECUTION \_ ERROR**
</dt> <dd> <dl> <dt>

12177
</dt> <dt>



Se encontró un error al ejecutar un script.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERROR \_ WINHTTP \_ SECURE \_ CERT \_ CN \_ INVALID**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Se devuelve cuando un nombre CN de certificado no coincide con el valor pasado (equivalente a un error **CERT E CN NO \_ \_ \_ \_ MATCH).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERROR \_ WINHTTP \_ SECURE \_ CERT \_ DATE \_ INVALID**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



Indica que un certificado necesario no está dentro de su período de validez al comprobar con el reloj del sistema actual o la marca de tiempo en el archivo firmado, o que los períodos de validez de la cadena de certificación no se anidan correctamente (equivalente a un **ERROR CERT \_ E \_ EXPIRED** o **CERT E \_ \_ VALIDITYPERIODNESTING).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERROR \_ WINHTTP \_ SECURE \_ CERT \_ REV \_ FAILED**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Indica que no se puede comprobar la revocación porque el servidor de revocación estaba sin conexión (equivalente a **CRYPT \_ E \_ REVOCATION \_ OFFLINE**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERROR \_ WINHTTP \_ SECURE \_ CERT \_ REVOKED**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Indica que se ha revocado un certificado (equivalente a **CRYPT \_ E \_ REVOKED).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERROR \_ WINHTTP \_ SECURE \_ CERT \_ WRONG \_ USAGE**
</dt> <dd> <dl> <dt>

12179
</dt> <dt>



Indica que un certificado no es válido para el uso solicitado (equivalente a **CERT \_ E WRONG \_ \_ USAGE**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**ERROR \_ WINHTTP \_ SECURE \_ CHANNEL \_ ERROR**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Indica que se ha producido un error que tiene que ver con un canal seguro (equivalente a los códigos de error que comienzan por "SEC E" y "SEC I" enumerados en el archivo de encabezado \_ \_ \_ \_ "winerror.h").


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERROR \_ WINHTTP \_ SECURE \_ FAILURE**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



Se encontraron uno o varios errores en el certificado Capa de sockets seguros (SSL) enviado por el servidor. Para determinar qué tipo de error se encontró, compruebe si hay una notificación [**WINHTTP \_ CALLBACK \_ STATUS SECURE \_ \_ FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) en una función de devolución de llamada de estado. Para obtener más información, vea [**WINHTTP \_ STATUS \_ CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERROR \_ WINHTTP \_ SECURE \_ INVALID \_ CA**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



Indica que se procesó una cadena de certificados, pero finalizó en un certificado raíz que no es de confianza para el proveedor de confianza (equivalente a **CERT \_ E \_ UNTRUSTEDROOT**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERROR \_ WINHTTP \_ SECURE \_ INVALID \_ CERT**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Indica que un certificado no es válido (equivalente a errores como **CERT \_ E \_ ROLE**, **CERT E \_ \_ PATHLENCONST,** **CERT E \_ \_ CRITICAL,** **CERT E \_ \_ PURPOSE**, **CERT E \_ \_ ISSUERCHAINING**, **CERT E \_ \_ MALFORMED** y **CERT E \_ \_ CHAINING).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERROR \_ WINHTTP \_ SHUTDOWN**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



La compatibilidad con la función WinHTTP se está apagando o descargando.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERROR \_ WINHTTP \_ TIMEOUT**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



La solicitud ha agotado el tiempo de espera.

Este error se puede devolver como resultado del comportamiento de tiempo de espera de TCP/IP, independientemente de los valores de tiempo de espera establecidos Windows servicios HTTP.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERROR \_ WINHTTP \_ NO SE PUEDE DESCARGAR EL \_ \_ \_ SCRIPT**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



No se puede descargar el archivo PAC. Por ejemplo, es posible que no se haya podido acceder al servidor al que hace referencia la dirección URL de PAC o que el servidor haya devuelto una respuesta 404 NOT FOUND.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERROR \_ WINHTTP \_ UNHANDLED \_ SCRIPT \_ TYPE**
</dt> <dd> <dl> <dt>

12176
</dt> <dt>



No se admite el tipo de script.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERROR \_ WINHTTP \_ UNRECOGNIZED \_ SCHEME**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



La dirección URL especificó un esquema distinto de "http:" o "https:".


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**
</dt> <dd> <dl> <dt>



No había suficiente memoria disponible para completar la operación solicitada.

**Encabezado:** Declarado en Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR \_ BÚFER \_ INSUFICIENTE**
</dt> <dd> <dl> <dt>



El tamaño, en bytes, del búfer proporcionado a una función no era suficiente para contener los datos devueltos. Para obtener más información, vea la función específica.

**Encabezado:** Declarado en Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**IDENTIFICADOR \_ DE ERROR NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>



El identificador pasado a la interfaz de programación de aplicaciones (API) se ha invalidado o cerrado.

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


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR \_ NO \_ ADMITIDO**
</dt> <dd> <dl> <dt>



No se carga la pila de protocolos necesaria y la aplicación no puede iniciar WinSock.

**Encabezado:** Declarado en Winerror.h


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHttp.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| Encabezado<br/>                   | <dl> <dt>Winhttp.h</dt> </dl>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

