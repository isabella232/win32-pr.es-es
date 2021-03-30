---
description: GetLastError devuelve los valores de error identificados en este tema cuando se produce un error en una de las funciones de servicios HTTP de Microsoft Windows (WinHTTP).
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Mensajes de error (winhttp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910850"
---
# <a name="error-messages-winhttph"></a>Mensajes de error (winhttp. h)

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los valores de error enumerados a continuación cuando se produce un error en una de las funciones de los servicios http de Microsoft Windows (WinHTTP) y también se devuelven en los 16 bits inferiores del error [**HRESULT**](../com/structure-of-com-error-codes.md) del objeto [**WinHttpRequest**](winhttprequest.md) .

Los valores de error cuyos nombres empiezan por "ERROR \_ WinHTTP \_ " son específicos de las funciones winhttp. Las funciones WinHTTP también devuelven mensajes de error de Windows cuando corresponda.

<dl> <dt>

<span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**error \_ de \_ \_ servicio de proxy automático \_ de WinHTTP \_**
</dt> <dd> <dl> <dt>

12178
</dt> <dt>



Devuelto por [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) cuando no se puede encontrar un proxy para la dirección URL especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERROR en la \_ \_ detección automática de WinHTTP \_**
</dt> <dd> <dl> <dt>

12180
</dt> <dt>



Devuelto por [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) si WinHTTP no pudo detectar la dirección URL del archivo de configuración automática de proxy (PAC).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERROR en el \_ script WinHTTP de \_ \_ proxy automático incorrecto \_ \_**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Error al ejecutar el código de script en el archivo de configuración automática de proxy (PAC).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERROR \_ WinHTTP \_ no puede \_ llamar \_ después de \_ Open**
</dt> <dd> <dl> <dt>

12103
</dt> <dt>



Lo devuelve el objeto [**HttpRequest**](winhttprequest.md) si una opción especificada no se puede solicitar una vez que se ha llamado al método [**Open**](iwinhttprequest-open.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERROR \_ WinHTTP \_ no puede \_ llamar \_ después del \_ envío**
</dt> <dd> <dl> <dt>

12102
</dt> <dt>



Lo devuelve el objeto [**HttpRequest**](winhttprequest.md) si una operación solicitada no se puede realizar después de llamar al método [**send**](iwinhttprequest-send.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERROR \_ WinHTTP \_ no se puede \_ llamar a \_ antes de \_ abrir**
</dt> <dd> <dl> <dt>

12100
</dt> <dt>



Lo devuelve el objeto [**HttpRequest**](winhttprequest.md) si una operación solicitada no se puede realizar antes de llamar al método [**Open**](iwinhttprequest-open.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERROR \_ WinHTTP \_ no se puede \_ llamar a \_ antes de \_ Enviar**
</dt> <dd> <dl> <dt>

12101
</dt> <dt>



Lo devuelve el objeto [**HttpRequest**](winhttprequest.md) si una operación solicitada no se puede realizar antes de llamar al método [**send**](iwinhttprequest-send.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERROR \_ WinHTTP \_ no se puede \_ conectar**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Se devuelve si se produce un error en la conexión al servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR \_ de \_ certificado de autenticación de cliente WinHTTP \_ \_ \_ necesario**
</dt> <dd> <dl> <dt>



El servidor requiere la autenticación del cliente SSL. La aplicación recupera la lista de emisores de certificados mediante una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con la opción **WinHTTP \_ \_ \_ \_ \_ lista de emisores** de certificados de cliente. Para obtener más información, consulte la opción **WinHTTP \_ \_ \_ \_ \_ lista de emisores de certificados de cliente** .

Si el servidor solicita el certificado de cliente, pero no lo requiere, la aplicación puede llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) de manera alternativa con la opción de contexto de certificado de cliente de la **\_ opción \_ \_ \_ WinHTTP** . En este caso, la aplicación especifica la \_ macro de \_ \_ contexto de certificado WinHTTP no Client \_ en el parámetro *lpBuffer* de **WinHttpSetOption**. Para obtener más información, vea la opción **WinHTTP \_ contexto de \_ \_ certificado \_ de cliente** .

**Windows Server 2003 con SP1 y Windows XP con SP2:** Este error no se admite.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERROR \_ : \_ \_ no se \_ \_ puede obtener acceso a la \_ \_ clave privada del certificado de cliente WinHTTP**
</dt> <dd> <dl> <dt>



La aplicación no tiene los privilegios necesarios para tener acceso a la clave privada asociada con el certificado de cliente.

**Windows Server 2003 con SP1 y Windows XP con SP2:** Este error no se admite.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERROR \_ de \_ certificado de cliente WinHTTP \_ \_ sin \_ \_ clave privada**
</dt> <dd> <dl> <dt>



El contexto para el certificado de cliente SSL no tiene una clave privada asociada. Es posible que el certificado de cliente se haya importado al equipo sin la clave privada.

**Windows Server 2003 con SP1 y Windows XP con SP2:** Este error no se admite.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERROR \_ de \_ desbordamiento de \_ tamaño de \_ encabezado de codificación \_ fragmentada de WinHTTP \_**
</dt> <dd> <dl> <dt>

12183
</dt> <dt>



Devuelto por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) cuando se encuentra una condición de desbordamiento en el transcurso del análisis de la codificación fragmentada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR \_ de \_ certificado de autenticación de cliente WinHTTP \_ \_ \_ necesario**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Devuelto por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) cuando el servidor solicita la autenticación del cliente.

**Windows Server 2003 con SP1 y Windows XP con SP2:** Este error no se admite.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**error \_ de \_ conexión de WinHTTP \_**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



La conexión con el servidor se ha restablecido o finalizado o se ha encontrado un protocolo SSL incompatible. Por ejemplo, la versión 5,1 de WinHTTP no admite SSL2 a menos que el cliente lo habilite específicamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**el \_ encabezado WinHTTP del error \_ \_ ya \_ existe**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Obsoleto ya no se usa.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**se \_ \_ \_ superó el número de encabezados WinHTTP de error \_**
</dt> <dd> <dl> <dt>

12181
</dt> <dt>



Devuelto por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) cuando un número mayor de encabezados estaba presente en una respuesta a la que WinHTTP podría recibir.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**\_ \_ \_ no \_ se encontró el encabezado WinHTTP del error**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



No se puede encontrar el encabezado solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERROR \_ de \_ \_ desbordamiento de tamaño de encabezado WinHTTP \_**
</dt> <dd> <dl> <dt>

12182
</dt> <dt>



Devuelto por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) cuando el tamaño de los encabezados recibidos supera el límite para el identificador de solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERROR \_ de \_ \_ Estado de identificador incorrecto de WinHTTP \_**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



No se puede realizar la operación solicitada porque el identificador proporcionado no tiene el estado correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERROR \_ de \_ \_ tipo de identificador incorrecto de WinHTTP \_**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



El tipo de identificador proporcionado no es correcto para esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**error \_ interno de WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Se ha producido un error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERROR \_ WinHTTP \_ opción no válida \_**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Una solicitud a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) especificó un valor de opción no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERROR \_ en \_ WinHTTP \_ solicitud de consulta no válida \_**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



Obsoleto ya no se usa.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERROR \_ WinHTTP \_ \_ respuesta del servidor no válida \_**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



No se puede analizar la respuesta del servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERROR \_ de \_ WinHTTP \_ dirección URL no válida**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



La URL no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERROR \_ de \_ Inicio de sesión de WinHTTP \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Error en el intento de inicio de sesión. Cuando se encuentra este error, el identificador de solicitud debe cerrarse con [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle). Se debe crear un nuevo identificador de solicitud antes de volver a intentar la función que generó originalmente este error.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERROR \_ \_ el nombre WinHTTP \_ no se \_ resolvió**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



No se puede resolver el nombre del servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERROR \_ WinHTTP \_ no \_ inicializado**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Obsoleto ya no se usa.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERROR \_ de \_ operación WinHTTP \_ cancelada**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



La operación se canceló, normalmente porque el identificador en el que estaba funcionando la solicitud se cerró antes de que se completara la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERROR de la \_ \_ opción WinHTTP \_ no \_ configurable**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



No se puede establecer la opción solicitada, solo se consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERROR \_ WinHTTP \_ fuera \_ de los \_ identificadores**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Obsoleto ya no se usa.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERROR \_ de \_ redirección de WinHTTP \_**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



No se pudo realizar la redirección porque se produjo un error en el esquema cambiado o en todos los intentos realizados para la redirección (el valor predeterminado es cinco intentos).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERROR \_ de \_ solicitud de reenvío de WinHTTP \_**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



Error en la función WinHTTP. Se puede reintentar la función deseada en el mismo identificador de solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERROR de desbordamiento de la \_ \_ respuesta WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12184
</dt> <dt>



Se devuelve cuando una respuesta entrante supera un límite de tamaño de WinHTTP interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**error \_ de \_ ejecución del script WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12177
</dt> <dt>



Se encontró un error al ejecutar un script.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERROR \_ WinHTTP \_ Secure \_ CERT \_ CN \_ no válido**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Se devuelve cuando el nombre de un certificado CN no coincide con el valor pasado (equivalente a un error del **certificado \_ E \_ CN \_ no \_ coincide** ).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERROR en la \_ \_ fecha del certificado de seguridad WinHTTP \_ \_ \_ no válida**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



Indica que un certificado necesario no se encuentra dentro de su período de validez al comprobar con el reloj del sistema actual o la marca de tiempo del archivo firmado, o que los períodos de validez de la cadena de certificación no se anidan correctamente (equivalente a un **certificado \_ e \_ caducado** o a un error de **certificado \_ e \_ VALIDITYPERIODNESTING** ).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERROR WinHTTP ERROR en la \_ \_ revisión del certificado de seguridad \_ \_ \_**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Indica que no se puede comprobar la revocación porque el servidor de revocación estaba sin conexión (equivalente a la **REvocación de cifrado \_ E \_ \_ sin conexión**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERROR \_ WinHTTP \_ \_ certificado seguro \_ revocado**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Indica que se ha revocado un certificado (equivalente a **cifrado \_ E \_ revocado**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERROR \_ de \_ \_ \_ uso incorrecto de certificado de seguridad WinHTTP \_**
</dt> <dd> <dl> <dt>

12179
</dt> <dt>



Indica que un certificado no es válido para el uso solicitado (equivalente al **uso del certificado \_ E \_ incorrecto \_**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**error \_ de \_ canal seguro de WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Indica que se produjo un error al tener que hacer con un canal seguro (equivalente a códigos de error que comienzan por "SEC \_ e \_ " y "s \_ I \_ " enumerados en el archivo de encabezado "Winerror. h").


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERROR \_ WinHTTP \_ Secure \_ error**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



Se encontraron uno o varios errores en el certificado Capa de sockets seguros (SSL) enviado por el servidor. Para determinar qué tipo de error se encontró, busque una notificación [**de \_ \_ error de \_ protección \_ del estado de devolución de llamada de WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) en una función de devolución de llamada de estado. Para obtener más información, vea la [**\_ devolución de \_ llamada de estado de WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERROR \_ WinHTTP \_ seguro \_ CA no válido \_**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



Indica que se procesó una cadena de certificados, pero termina en un certificado raíz que no es de confianza para el proveedor de confianza (equivalente a **CERT \_ E \_ UNTRUSTEDROOT**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERROR \_ WinHTTP \_ seguro \_ certificado no válido \_**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Indica que un certificado no es válido (lo que equivale a errores como el **\_ \_ rol CERT e**, **CERT \_ e \_ PATHLENCONST**, **CERT e \_ \_ Critical**, **CERT y \_ \_ purpose**, **CERT \_ e \_ ISSUERCHAINING**, el **certificado e es \_ \_ incorrecto** y el **\_ \_ encadenamiento de certificados e**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERROR \_ de \_ apagado de WinHTTP**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



La compatibilidad con la función WinHTTP se está cerrando o descargando.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERROR \_ de \_ tiempo de espera de WinHTTP**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



La solicitud ha agotado el tiempo de espera.

Este error se puede devolver como resultado del comportamiento de tiempo de espera de TCP/IP, independientemente de los valores de tiempo de espera establecidos en los servicios HTTP de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERROR \_ WinHTTP \_ no se puede \_ \_ descargar el \_ script**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



No se puede descargar el archivo PAC. Por ejemplo, puede que el servidor al que hace referencia la dirección URL de PAC no sea accesible o que el servidor devuelva una respuesta 404 no encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERROR \_ de \_ tipo de script WinHTTP no controlado \_ \_**
</dt> <dd> <dl> <dt>

12176
</dt> <dt>



No se admite el tipo de script.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERROR en el \_ \_ esquema WinHTTP desconocido \_**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



La dirección URL especificó un esquema distinto de "http:" o "https:".


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR \_ de \_ memoria insuficiente \_**
</dt> <dd> <dl> <dt>



No había suficiente memoria disponible para completar la operación solicitada.

**Encabezado:** Declarado en Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR \_ de \_ búfer insuficiente**
</dt> <dd> <dl> <dt>



El tamaño, en bytes, del búfer proporcionado a una función no era suficiente para contener los datos devueltos. Para obtener más información, vea la función específica.

**Encabezado:** Declarado en Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR \_ de \_ identificador no válido**
</dt> <dd> <dl> <dt>



El identificador pasado a la interfaz de programación de aplicaciones (API) se ha invalidado o cerrado.

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


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR \_ no \_ admitido**
</dt> <dd> <dl> <dt>



La pila de protocolos necesaria no está cargada y la aplicación no puede iniciar WinSock.

**Encabezado:** Declarado en Winerror. h


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.<br/> |
| Encabezado<br/>                   | <dl> <dt>Winhttp. h</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

