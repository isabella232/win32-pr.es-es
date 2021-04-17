---
title: Marcas de opciones (Wininet. h)
description: Las marcas de opciones siguientes se usan con las funciones InternetQueryOption y InternetSetOption. Todas las marcas de opciones válidas tienen un valor mayor o igual que INTERNET \_ primera \_ opción y menor o igual que Internet \_ última \_ opción.
ms.assetid: 708510b8-468a-4287-849b-cba3d7001ea8
topic_type:
- apiref
api_name:
- INTERNET_OPTION_ALTER_IDENTITY
- INTERNET_OPTION_ASYNC
- INTERNET_OPTION_ASYNC_ID
- INTERNET_OPTION_ASYNC_PRIORITY
- INTERNET_OPTION_BYPASS_EDITED_ENTRY
- INTERNET_OPTION_CACHE_STREAM_HANDLE
- INTERNET_OPTION_CACHE_TIMESTAMPS
- INTERNET_OPTION_CALLBACK
- INTERNET_OPTION_CALLBACK_FILTER
- INTERNET_OPTION_CLIENT_CERT_CONTEXT
- INTERNET_OPTION_CODEPAGE
- INTERNET_OPTION_CODEPAGE_PATH
- INTERNET_OPTION_CODEPAGE_EXTRA
- INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH
- INTERNET_OPTION_CONNECT_BACKOFF
- INTERNET_OPTION_CONNECT_RETRIES
- INTERNET_OPTION_CONNECT_TIME
- INTERNET_OPTION_CONNECT_TIMEOUT
- INTERNET_OPTION_CONNECTED_STATE
- INTERNET_OPTION_CONTEXT_VALUE
- INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT
- INTERNET_OPTION_CONTROL_SEND_TIMEOUT
- INTERNET_OPTION_DATA_RECEIVE_TIMEOUT
- INTERNET_OPTION_DATA_SEND_TIMEOUT
- INTERNET_OPTION_DATAFILE_NAME
- INTERNET_OPTION_DATAFILE_EXT
- INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO
- INTERNET_OPTION_DIGEST_AUTH_UNLOAD
- INTERNET_OPTION_DISABLE_AUTODIAL
- INTERNET_OPTION_DISCONNECTED_TIMEOUT
- INTERNET_OPTION_ENABLE_HTTP_PROTOCOL
- INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ
- INTERNET_OPTION_ENCODE_EXTRA
- INTERNET_OPTION_END_BROWSER_SESSION
- INTERNET_OPTION_ERROR_MASK
- INTERNET_OPTION_ENTERPRISE_CONTEXT
- INTERNET_OPTION_EXTENDED_ERROR
- INTERNET_OPTION_FROM_CACHE_TIMEOUT
- INTERNET_OPTION_HANDLE_TYPE
- INTERNET_OPTION_HSTS
- INTERNET_OPTION_HTTP_DECODING
- INTERNET_OPTION_HTTP_PROTOCOL_USED
- INTERNET_OPTION_HTTP_VERSION
- INTERNET_OPTION_IDENTITY
- INTERNET_OPTION_IDLE_STATE
- INTERNET_OPTION_IDN
- INTERNET_OPTION_IGNORE_OFFLINE
- INTERNET_OPTION_KEEP_CONNECTION
- INTERNET_OPTION_LISTEN_TIMEOUT
- INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER
- INTERNET_OPTION_MAX_CONNS_PER_PROXY
- INTERNET_OPTION_MAX_CONNS_PER_SERVER
- INTERNET_OPTION_OFFLINE_MODE
- INTERNET_OPTION_OFFLINE_SEMANTICS
- INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE
- INTERNET_OPTION_PARENT_HANDLE
- INTERNET_OPTION_PASSWORD
- INTERNET_OPTION_PER_CONNECTION_OPTION
- INTERNET_OPTION_POLICY
- INTERNET_OPTION_PROXY
- INTERNET_OPTION_PROXY_PASSWORD
- INTERNET_OPTION_PROXY_SETTINGS_CHANGED
- INTERNET_OPTION_PROXY_USERNAME
- INTERNET_OPTION_READ_BUFFER_SIZE
- INTERNET_OPTION_RECEIVE_THROUGHPUT
- INTERNET_OPTION_RECEIVE_TIMEOUT
- INTERNET_OPTION_REFRESH
- INTERNET_OPTION_REMOVE_IDENTITY
- INTERNET_OPTION_REQUEST_FLAGS
- INTERNET_OPTION_REQUEST_PRIORITY
- INTERNET_OPTION_RESET_URLCACHE_SESSION
- INTERNET_OPTION_SECONDARY_CACHE_KEY
- INTERNET_OPTION_SECURITY_CERTIFICATE
- INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT
- INTERNET_OPTION_SECURITY_FLAGS
- INTERNET_OPTION_SECURITY_KEY_BITNESS
- INTERNET_OPTION_SEND_THROUGHPUT
- INTERNET_OPTION_SEND_TIMEOUT
- INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT
- INTERNET_OPTION_SETTINGS_CHANGED
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- INTERNET_OPTION_SUPPRESS_BEHAVIOR
- INTERNET_OPTION_URL
- INTERNET_OPTION_USER_AGENT
- INTERNET_OPTION_USERNAME
- INTERNET_OPTION_VERSION
- INTERNET_OPTION_WRITE_BUFFER_SIZE
api_location:
- Wininet.h
- Winineti.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c99ca6f12836c620ed7c952e0ceb1844aee3b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677011"
---
# <a name="option-flags-winineth"></a>Marcas de opciones (Wininet. h)

Las marcas de opciones siguientes se usan con las funciones [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) . Todas las marcas de opciones válidas tienen un valor mayor o igual que **Internet \_ primera \_ opción** y menor o igual que **Internet \_ última \_ opción**.

<dl> <dt>

<span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**opción de INTERNET \_ \_ ALTER \_ Identity**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



No implementado


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**opción de INTERNET \_ \_ Async**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**\_ \_ identificador asincrónico de la opción de Internet \_**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**\_opción de \_ Internet \_ prioridad asincrónica**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**opción de INTERNET \_ \_ omitir \_ entrada editada \_**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



Establece o recupera el valor booleano que determina si el sistema debe comprobar si el contenido de la red es más reciente y sobrescribir las entradas de caché editadas si se encuentra una versión más reciente. Si se establece en true, el sistema comprueba si el contenido de la red **es** más reciente y sobrescribe la entrada de caché editada con la versión más reciente. El valor predeterminado es **false**, que indica que la entrada de caché modificada debe usarse sin comprobar la red. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Solo es válido en Microsoft Internet Explorer 5 y versiones posteriores.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**opción de INTERNET \_ \_ identificador de secuencia de caché \_ \_**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Ya no se admite.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**marcas de tiempo de opciones de INTERNET de \_ \_ caché \_**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



Recupera una estructura [**de \_ \_ marcas**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) de tiempo de la caché de Internet que contiene la hora de la LastModified y expira el tiempo del recurso almacenado en la caché de Internet. [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)usa este valor.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**devolución de llamada de \_ opción de Internet \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Establece o recupera la dirección de la función de devolución de llamada definida para este identificador. Esta opción se puede usar en todos los identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) . Usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**\_filtro de \_ devolución de llamada de opción de Internet \_**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**\_contexto de \_ certificado de cliente de opción de Internet \_ \_**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



Esta marca no es compatible con [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). El parámetro *lpBuffer* debe ser un puntero a una estructura de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) y no un puntero a un puntero de **\_ contexto de certificado** . Si una aplicación recibe el error se necesita el **\_ \_ certificado de autenticación de cliente \_ \_ \_ de Internet**, debe llamar a [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) o usar [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para proporcionar un certificado antes de volver a intentar la solicitud. A continuación, se llama a [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) para que la aplicación pueda publicar de forma independiente el contexto de certificado que se pasa.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**Página de códigos de la opción de INTERNET \_ \_**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



De forma predeterminada, la parte de host o de autoridad de la dirección URL de Unicode se codifica según la especificación de IDN. Al establecer esta opción en la solicitud o el identificador de conexión, cuando se deshabilita IDN, se especifica un esquema de codificación de página de códigos para la parte del host de la dirección URL. El parámetro *lpBuffer* de la llamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contiene la página de códigos DBCS deseada. Si no se especifica ninguna página de códigos en *lpBuffer*, WinInet utiliza la página de códigos predeterminada del sistema (CP \_ ACP). Nota: esta opción se omite si no se deshabilita IDN. Para obtener más información sobre cómo deshabilitar IDN, consulte la opción de **Internet \_ \_ IDN** .

**Windows XP con SP2 y Windows Server 2003 con SP1:** Esta marca no se admite.

**Versión:** Requiere Internet Explorer 7,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**\_ruta de \_ acceso de página de la opción de Internet \_**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



De forma predeterminada, la parte de la ruta de acceso de la dirección URL está codificada en UTF8. La API WinINet realiza el carácter de escape (%) codificación en los caracteres de bit alto. Al establecer esta opción en la solicitud o el identificador de conexión, se deshabilita la codificación UTF8 y se establece una página de códigos específica. El parámetro *lpBuffer* de la llamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contiene la página de códigos DBCS deseada para la ruta de acceso. Si no se especifica ninguna página de códigos en *lpBuffer*, WinInet usa el CP \_ UTF8 predeterminado.

**Windows XP con SP2 y Windows Server 2003 con SP1:** Esta marca no se admite.

**Versión:** Requiere Internet Explorer 7,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**Página de códigos de opciones de INTERNET \_ \_ \_ extra**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



De forma predeterminada, la parte de la ruta de acceso de la dirección URL es la página de códigos predeterminada del sistema (CP \_ ACP). El carácter de escape (%) no se realizan conversiones en la parte adicional. Si se establece esta opción en la solicitud o el identificador de conexión, se deshabilita la \_ codificación CP ACP. El parámetro *lpBuffer* de la llamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contiene la página de códigos DBCS deseada para la parte adicional de la dirección URL. Si no se especifica ninguna página de códigos en *lpBuffer*, WinInet utiliza la página de códigos predeterminada del sistema (CP \_ ACP).

**Windows XP con SP2 y Windows Server 2003 con SP1:** Esta marca no se admite.

**Versión:** Requiere Internet Explorer 7,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**\_longitud de \_ \_ contenido comprimido \_ de la opción de Internet** 
</dt> <dd> <dl> <dt>

147
</dt> <dt>



En el caso de una solicitud en la que WinInet descomprimió la codificación de contenido suministrada por el servidor, recupera la longitud del contenido del cuerpo de la respuesta como ULONGLONG. Compatible con Windows 10, versión 1507 y versiones posteriores.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**\_retroceso de \_ conexión de opciones de Internet \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**reintentos de conexión de opciones de INTERNET \_ \_ \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Establece o recupera un valor entero largo sin signo que contiene el número de veces que WinINet intenta resolver y conectarse a un host. Solo se intenta una vez por cada dirección IP. Por ejemplo, si intenta conectarse a un host multihome que tiene diez direcciones IP y \_ la opción Internet \_ Connect \_ reintentos está establecida en siete, WinInet solo intenta resolver y conectarse a las siete primeras direcciones IP. Por el contrario, dado el mismo conjunto de diez direcciones IP, si la \_ opción \_ de Internet conectar \_ reintentos está establecida en 20, WinInet intenta cada una de las diez solo una vez. Si un host solo tiene una dirección IP y se produce un error en el primer intento de conexión, no hay más intentos. Si un intento de conexión sigue sin funcionar después del número especificado de intentos, se cancela la solicitud. El valor predeterminado para la \_ opción de Internet \_ Connect \_ reintentos es de cinco intentos. Esta opción se puede utilizar en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluido un identificador **nulo** . Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**tiempo de conexión de la opción de INTERNET \_ \_ \_**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**\_tiempo de \_ espera de conexión de opciones de Internet \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, que se va a usar para las solicitudes de conexión a Internet. Si se establece esta opción en infinita (0xFFFFFFFF), se deshabilitará este temporizador.

Si una solicitud de conexión tarda más que este valor de tiempo de espera, se cancela la solicitud. Al intentar conectarse a varias direcciones IP para un único host (un host de múltiples hosts), el límite de tiempo de espera es acumulativo para todas las direcciones IP. Esta opción se puede utilizar en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluido un identificador **nulo** . Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**Estado de conexión de la opción de INTERNET \_ \_ \_**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



Establece o recupera un valor entero largo sin signo que contiene el estado conectado. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**\_valor de \_ contexto de opción de Internet \_**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



Establece o recupera un valor de DWORD \_ ptr que contiene la dirección del valor de contexto asociado a este identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) . Esta opción puede usarse en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) . Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Anteriormente, esto establece el valor de contexto en la dirección almacenada en el puntero **lpBuffer** . Esto se ha corregido para que se utilice el valor almacenado en el búfer y se asigne un nuevo valor a la marca de [valor de contexto de opción de Internet \_ \_ \_ ](/windows) . El valor anterior, 10, se ha conservado para que las aplicaciones escritas para el comportamiento anterior sigan siendo compatibles.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**\_tiempo de \_ espera de recepción del control de opciones de \_ Internet \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Idéntico al [ \_ tiempo de \_ \_ espera de recepción](/windows)de la opción de Internet. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**\_tiempo de \_ espera de envío de control de opciones de \_ Internet \_**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Idéntico a la [opción de Internet de tiempo de \_ \_ \_ espera de envío](/windows). Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**\_tiempo de \_ espera de recepción de datos de opción de \_ Internet \_**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para recibir una respuesta a una solicitud del canal de datos de una transacción FTP. Si la respuesta tarda más que este valor de tiempo de espera, se cancela la solicitud. Esta opción se puede utilizar en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluido un identificador **nulo** . Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Esta marca no tiene ningún impacto en la funcionalidad HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**\_tiempo de \_ espera de envío de datos de opción de \_ Internet \_**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Establece o recupera un valor entero largo sin signo, en milisegundos, que contiene el valor de tiempo de espera para enviar una solicitud para el canal de datos de una transacción FTP. Si el envío tarda más que este valor de tiempo de espera, se cancela el envío. Esta opción se puede utilizar en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluido un identificador **nulo** . Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Esta marca no tiene ningún impacto en la funcionalidad HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**nombre de archivo de la opción de INTERNET \_ \_ \_**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



Recupera un valor de cadena que contiene el nombre del archivo que realiza la copia de seguridad de una entidad descargada. Esta marca es válida después de que se completen [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) . Esta opción solo puede ser consultada por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**opción de INTERNET \_ \_ archivo de archivo de archivos \_ ext**
</dt> <dd> <dl> <dt>

96
</dt> <dt>



Establece un valor de cadena que contiene la extensión del archivo que realiza la copia de seguridad de una entidad descargada. Esta marca se debe establecer antes de llamar a [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). Esta opción solo se puede establecer mediante [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**opción de INTERNET \_ \_ información del socket de diagnóstico \_ \_**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



Recupera una estructura [**de \_ \_ \_ información del socket de diagnóstico de Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) que contiene datos sobre una solicitud HTTP especificada. [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)usa esta marca.

**Windows 7:** Esta opción ya no se admite.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**\_descarga de \_ \_ autenticación implícita de opción \_ de Internet**
</dt> <dd> <dl> <dt>

76
</dt> <dt>



Hace que el sistema cierre la sesión del paquete SSPI de autenticación implícita, y purga todas las credenciales creadas para el proceso. No se requiere ningún búfer para esta opción. [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)lo usa.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**opción de INTERNET \_ \_ deshabilitar \_ marcado automático**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**tiempo de espera de la opción de INTERNET \_ \_ desconectado \_**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**opción de INTERNET \_ \_ habilitar \_ \_ protocolo http**
</dt> <dd> <dl> <dt>

148
</dt> <dt>



Establece una máscara de máscara DWORD de versiones de HTTP avanzadas aceptables. Se puede establecer en cualquier tipo de identificador. Los valores posibles son:

-   \_Marca de protocolo HTTP \_ \_ HTTP2 (0X2). Compatible con Windows 10, versión 1507 y versiones posteriores.

Las versiones heredadas de HTTP (1,1 y anteriores) no se pueden deshabilitar con esta opción. El valor predeterminado es 0X0. Compatible con Windows 10, versión 1507 y versiones posteriores.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**opción de INTERNET \_ Habilitar la lectura de \_ caché de \_ redireccionamiento \_ \_**
</dt> <dd> <dl> <dt>

122
</dt> <dt>



En un identificador de solicitud, establece un valor booleano que controla si las redirecciones se devolverán desde la memoria caché de WinInet para una solicitud determinada. El valor predeterminado es FALSE. Compatible con Windows 8 y versiones posteriores.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**opción de INTERNET \_ \_ codificación \_ adicional**
</dt> <dd> <dl> <dt>

155
</dt> <dt>



Obtiene o establece un valor BOOLEANO que indica si los caracteres no ASCII de la cadena de consulta deben estar codificados por porcentaje. El valor predeterminado es FALSE. Se admite en Windows 8.1 y versiones posteriores.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**opción de INTERNET \_ \_ finalizar \_ sesión del explorador \_**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



Vacía las entradas que no están en uso desde la memoria caché de contraseñas de la unidad de disco duro. También restablece el tiempo de caché utilizado cuando el modo de sincronización es una vez por sesión. No se requiere ningún búfer para esta opción. Se usa en [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**\_máscara de \_ error de opción de Internet \_**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



Establece un valor entero largo sin signo que contiene las máscaras de error que puede controlar la aplicación cliente. Puede ser una combinación de los siguientes valores:

<dl> <dt>

<span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>certificado de máscara de error de INTERNET \_ \_ \_ combinado \_ s \_
</dt> <dd>

0x2

Indica que se van a informar de todos los errores de certificado con el mismo error de devolución, es decir, **\_ \_ \_ \_ errores de certificado por Internet**. Si se establece esta marca, llame a **InternetErrorDlg** tras recibir el error errores de **certificado de \_ Internet \_ s \_ \_** por error, de modo que el usuario pueda responder a un cuadro de diálogo conocido que describa el problema.

> [!Caution]  
> Si no se informa al usuario de este error, expone al usuario a posibles ataques de suplantación de identidad.

 

</dd> <dt>

<span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>carátula de error de INTERNET \_ \_ \_ Insertar \_ CDROM
</dt> <dd>

0x1

Indica que la aplicación cliente puede controlar el código de error de **\_ Internet \_ Insert \_ CDROM** .

</dd> <dt>

<span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>error de inicio de sesión de máscara de error de INTERNET \_ \_ \_ \_ \_ Mostrar \_ cuerpo de entidad \_
</dt> <dd>

0x8

Indica que la aplicación cliente puede controlar el error de inicio de sesión de Internet mostrar el código de error **\_ \_ \_ \_ \_ \_ del cuerpo** de la entidad.

</dd> <dt>

<span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>la \_ máscara de error de Internet \_ necesita el \_ \_ \_ paquete SSPI de MSN \_
</dt> <dd>

0x4

Sin implementar.

</dd> </dl>

</dl> </dd> <dt>

<span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**contexto de la opción de INTERNET \_ \_ Enterprise \_**
</dt> <dd> <dl> <dt>

159
</dt> <dt>



Establece un PWSTR que contiene el identificador de empresa (vea https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) lo que se aplica a la solicitud). Compatible con Windows 10, versión 1507 y versiones posteriores.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**\_ \_ error extendido de la opción de Internet \_**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Recupera un valor entero largo sin signo que contiene un código de error de Winsock asignado al error de los mensajes de error de **\_ Internet \_** devueltos por última vez en este contexto de subproceso. Esta opción se usa en un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) **nulo** por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**\_opción \_ de Internet del \_ tiempo de espera de caché \_**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



Establece o recupera el valor entero largo sin signo de A1n que contiene la cantidad de tiempo que el sistema debe esperar una respuesta a una solicitud de red antes de comprobar si hay una copia del recurso en la memoria caché. Si una solicitud de red tarda más tiempo del especificado y el recurso solicitado está disponible en la memoria caché, el recurso se recupera de la caché. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**\_tipo de \_ identificador de opción de Internet \_**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Recupera un valor entero largo sin signo que contiene el tipo de los identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) pasados. Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) en cualquier identificador de [HINTERNET](appendix-a-hinternet-handles.md) . Entre los posibles valores devueltos se incluyen los siguientes.

<dl> <dt>

<span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>tipo de identificador de INTERNET \_ \_ \_ Connect \_ FTP
</dt> <dd>

2

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>tipo de identificador de INTERNET \_ \_ \_ Connect \_ Gopher
</dt> <dd>

3

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>tipo de identificador de INTERNET \_ \_ \_ Connect \_ http
</dt> <dd>

4

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>\_solicitud de \_ archivo de tipo de identificador de Internet \_ \_
</dt> <dd>

14

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>tipo de identificador de INTERNET \_ \_ \_ \_ archivo FTP
</dt> <dd>

7

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>tipo de identificador de INTERNET \_ \_ \_ \_ archivo FTP \_ HTML
</dt> <dd>

8

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>tipo de identificador de INTERNET \_ \_ \_ búsqueda de FTP \_
</dt> <dd>

5

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>tipo de identificador de INTERNET \_ \_ búsqueda de \_ \_ \_ HTML
</dt> <dd>

6

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>tipo de identificador de INTERNET ( \_ \_ \_ \_ archivo Gopher)
</dt> <dd>

11

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>tipo de identificador de INTERNET \_ \_ \_ \_ archivo Gopher \_ HTML
</dt> <dd>

12

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>búsqueda de tipo de identificador de INTERNET \_ \_ \_ Gopher \_
</dt> <dd>

9

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>tipo de identificador de INTERNET de la \_ \_ búsqueda de \_ \_ \_ HTML Gopher
</dt> <dd>

10

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>\_ \_ solicitud HTTP de tipo de identificador de \_ Internet \_
</dt> <dd>

13

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>tipo de identificador de INTERNET \_ \_ \_ Internet
</dt> <dd>

1

</dd> </dl>

</dl> </dd> <dt>

<span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**opción de INTERNET \_ \_ HSTS**
</dt> <dd> <dl> <dt>

157
</dt> <dt>



Obtiene o establece un valor BOOLEANO que indica si WinInet debe seguir las directivas de seguridad de transporte estricto HTTP (HSTS) de los servidores. Si está habilitada, las solicitudes de combinación de https://a los dominios que tienen una directiva de HSTS almacenada en caché por WinInet se redirigirán a las direcciones URL de https://coincidentes. El valor predeterminado es FALSE. Se admite en Windows 8.1 y versiones posteriores.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**descodificación http de la opción de INTERNET \_ \_ \_**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



Permite que WinINet realice la descodificación para los esquemas de codificación gzip y DEFLATE. Para obtener más información, consulte [**codificación de contenido**](content-encoding.md).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**protocolo http de la opción de INTERNET \_ \_ \_ \_ usado**
</dt> <dd> <dl> <dt>

149
</dt> <dt>



Obtiene un valor DWORD que indica qué versión de HTTP avanzada se usó en una solicitud determinada. Los valores posibles son:

-   \_Marca de protocolo HTTP \_ \_ HTTP2 (0X2). Compatible con Windows 10, versión 1507 y versiones posteriores.

0X0 indica HTTP/1.1 o anterior; consulte \_ opción \_ de Internet \_ versión de http si se necesita más precisión sobre la versión heredada. Compatible con Windows 10, versión 1507 y versiones posteriores.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**opción de INTERNET \_ \_ versión de http \_**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



Establece o recupera una estructura [**de \_ \_ información de versión de http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) que contiene la versión de http admitida. Debe usarse en un identificador **nulo** . Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

En Windows 7, Windows Server 2008 R2 y versiones posteriores, la configuración de Internet Explorer invalida el valor del miembro **dwMinorVersion** de la estructura de [**\_ \_ información de versión http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) . **EnableHttp1 \_ 1** es un valor del registro en **HKLM \\ software \\ Microsoft \\ InternetExplorer \\ AdvacnedOptions \\ http \\ GENABLE** controlado por opciones de Internet establecidas en Internet Explorer para el sistema. El valor predeterminado de **EnableHttp1 \_ 1** es 1. La estructura de **\_ \_ información de la versión http** se omite para cualquier versión http inferior a 1,1 si **EnableHttp1 \_ 1** está establecido en 1.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**identidad de la opción de INTERNET \_ \_**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**\_Estado de \_ inactividad de la opción de Internet \_**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**Opciones de INTERNET \_ \_ IDN**
</dt> <dd> <dl> <dt>

102
</dt> <dt>



De forma predeterminada, la parte de host o de autoridad de la dirección URL se codifica según la especificación de IDN para conexiones directas y proxy. Esta opción se puede usar en la solicitud o en el identificador de conexión para habilitar o deshabilitar IDN. Cuando se deshabilita IDN, WinINet utiliza la página de códigos del sistema para codificar la parte de host o de autoridad de la dirección URL. Para deshabilitar la conversión de hosts IDN, establezca el parámetro *lpBuffer* en la llamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) en cero. Para habilitar la conversión IDN solo en la conexión directa, especifique **Internet \_ Flag \_ IDN \_ Direct** en el parámetro *lpBuffer* en la llamada a **InternetSetOption**. Para habilitar la conversión de IDN solo en la conexión del proxy, especifique el **\_ \_ \_ proxy IDN de marca de Internet** en el parámetro *lpBuffer* en la llamada a **InternetSetOption**.

**Windows XP con SP2 y Windows Server 2003 con SP1:** Esta marca no se admite.

**Versión:** Requiere Internet Explorer 7,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**opción de INTERNET \_ \_ omitir \_ sin conexión**
</dt> <dd> <dl> <dt>

77
</dt> <dt>



Establece o recupera si se debe omitir el indicador global sin conexión para el identificador de solicitud especificado. No se requiere ningún búfer para esta opción. Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con un identificador de solicitud. Esta opción solo es válida en Internet Explorer 5 y versiones posteriores.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**opción de INTERNET \_ \_ mantener \_ conexión**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**\_tiempo de \_ espera de escucha de opción de Internet \_**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**Opción de INTERNET \_ \_ Max \_ Conex \_ . \_ por \_ servidor 1 0 \_**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por servidor HTTP/1.0. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Esta opción solo es válida en Internet Explorer 5 y versiones posteriores.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**opción de INTERNET \_ \_ Max \_ Conex. \_ por \_ proxy**
</dt> <dd> <dl> <dt>

103
</dt> <dt>



Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por cada proxy de CERN. Cuando se establece o recupera esta opción, el parámetro *hInternet* debe establecerse en un valor de identificador **nulo** . Un valor de identificador **null** indica que la opción se debe establecer o consultar para el proceso actual. Cuando se llama a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con esta opción, todos los objetos proxy existentes recibirán el nuevo valor. Este valor se limita a un intervalo de 2 a 128, ambos inclusive.

**Versión:** Requiere Internet Explorer 8,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**opción de INTERNET \_ \_ Max \_ Conex. \_ por \_ servidor**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por servidor. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Esta opción solo es válida en Internet Explorer 5 y versiones posteriores.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**\_ \_ modo sin conexión de opciones de Internet \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**\_ \_ semántica sin conexión de opciones de Internet \_**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**\_opción \_ de Internet participar en una \_ \_ \_ firma débil**
</dt> <dd> <dl> <dt>

176
</dt> <dt>



Optar por la firma débil (por ejemplo, SHA-1) para que se trate como no segura. Esto indicará a WinInet que llame a [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) mediante el parámetro **de la \_ \_ \_ \_ \_ firma débil de la cadena de certificados** .


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**\_ \_ identificador primario de la opción de Internet \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Recupera el identificador primario de este identificador. Esta opción puede usarse en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) de [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**contraseña de la opción de INTERNET \_ \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Establece o recupera un valor de cadena que contiene la contraseña asociada a un identificador devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**opción de INTERNET \_ \_ por \_ opción de conexión \_**
</dt> <dd> <dl> <dt>

75
</dt> <dt>



Establece o recupera una estructura [**de \_ \_ \_ \_ lista**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) de opciones de Internet por conexión que especifica una lista de opciones para una conexión determinada. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Esta opción solo es válida en Internet Explorer 5 y versiones posteriores.

> [!Note]  
> **Internet \_ de La \_ opción \_ por \_ conexión** hace que la configuración se cambie en todo el sistema cuando se usa un identificador **null** en la llamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Para actualizar la configuración de proxy global, debe llamar a **InternetSetOption** con la marca de opción de **\_ \_ actualización de opciones de Internet** .

 

> [!Note]  
> Para cambiar la información de proxy para todo el proceso sin que ello afecte a la configuración global de Internet Explorer 5 y versiones posteriores, use esta opción en el identificador devuelto por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). En el siguiente ejemplo de código se cambia el proxy para todo el proceso, aunque el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) esté cerrado y no se use en ninguna solicitud.

 

Para obtener más información y ejemplos de código, consulte el [artículo de KB 226473](https://support.microsoft.com/kb/226473).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**\_Directiva de opciones de Internet \_**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**\_proxy de opción de Internet \_**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



Establece o recupera una estructura [**de \_ \_ información de proxy de Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) que contiene los datos de proxy para un identificador de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) existente cuando el identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) no es **null**. Si el identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) es **null**, la función establece o consulta los datos de proxy globales. Esta opción se puede utilizar en el identificador devuelto por **InternetOpen**. Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

> [!Note]  
> Se recomienda usar la opción \_ \_ de Internet por cada \_ \_ opción de conexión en lugar del \_ proxy de opción de Internet \_ . Para obtener más información, consulte el [artículo 226473 de Knowledge Base](https://support.microsoft.com/kb/226473).

 


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**\_contraseña de \_ proxy de opción de Internet \_**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



Establece o recupera un valor de cadena que contiene la contraseña utilizada para tener acceso al proxy. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Esta opción se puede establecer en el identificador devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**configuración de proxy de opción de INTERNET \_ \_ \_ \_ cambiada**
</dt> <dd> <dl> <dt>

95 
</dt> <dt>



Alerta a la instancia actual de WinInet de que la configuración de proxy ha cambiado y que debe actualizar con la nueva configuración. Para avisar de todas las instancias de WinInet disponibles, establezca el parámetro *buffer* de [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) en **null** y *BufferLength* en 0 al pasar esta opción. Esta opción se puede establecer en el identificador devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**\_nombre de \_ usuario de proxy de opción de Internet \_**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



Establece o recupera un valor de cadena que contiene el nombre de usuario utilizado para tener acceso al proxy. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Esta opción se puede establecer en el identificador devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**\_tamaño de \_ búfer de lectura de opción de Internet \_ \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Establece o recupera un valor entero largo sin signo que contiene el tamaño del búfer de lectura. Esta opción se puede usar en los identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) devueltos por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)y [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (solo sesión FTP). [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)usan esta opción.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**rendimiento de la opción de INTERNET \_ \_ \_**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**\_tiempo de \_ espera de recepción de opción de Internet \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para recibir una respuesta a una solicitud. Si la respuesta tarda más que este valor de tiempo de espera, se cancela la solicitud. Esta opción se puede utilizar en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluido un identificador **nulo** . Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Esta opción no está pensada para representar un tiempo de espera muy específico y inmediato. Puede esperar que el tiempo de espera se produzca hasta seis segundos después del valor de tiempo de espera establecido.

Cuando se utiliza en referencia a una transacción FTP, esta opción hace referencia al canal de control.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**actualización de la opción de INTERNET \_ \_**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



Hace que los datos de proxy se relean desde el registro para un identificador. No se requiere ningún búfer. Esta opción se puede usar en el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) devuelto por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)lo usa.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**opción de INTERNET \_ \_ quitar \_ identidad**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**\_marcas de \_ solicitud de opciones de Internet \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Recupera un valor entero largo sin signo que contiene las marcas de estado especiales que indican el estado de la descarga en curso. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). La opción de marcas de solicitud de opciones de Internet puede ser uno de los siguientes valores: [ \_ \_ \_ ](/windows)

<dl> <dt>

<span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET \_ REQFLAG \_ Async
</dt> <dd>

0x00000002

Sin implementar.

</dd> <dt>

<span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>escritura de caché de INTERNET \_ REQFLAG \_ \_ \_ deshabilitada
</dt> <dd>

0x00000040

No se puede almacenar en caché la solicitud de Internet (por ejemplo, una solicitud HTTPS).

</dd> <dt>

<span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET \_ REQFLAG \_ de la \_ caché
</dt> <dd>

0x00000001

La respuesta procedía de la memoria caché.

</dd> <dt>

<span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>tiempo de espera de INTERNET \_ REQFLAG \_ net \_
</dt> <dd>

0x00000080

Se agotó el tiempo de espera de la solicitud de Internet.

</dd> <dt>

<span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>REQFLAG de INTERNET \_ \_ sin \_ encabezados
</dt> <dd>

0x00000008

La respuesta original no contenía encabezados.

</dd> <dt>

<span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET \_ REQFLAG \_ passive
</dt> <dd>

0x00000010

Sin implementar.

</dd> <dt>

<span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>REQFLAG de INTERNET \_ \_ a través de \_ proxy
</dt> <dd>

0x00000004

La solicitud se realizó a través de un proxy.

</dd> </dl>

</dl> </dd> <dt>

<span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**\_prioridad de \_ solicitud de opción de Internet \_**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



Establece o recupera un valor entero largo sin signo que contiene la prioridad de las solicitudes que compiten por una conexión en un identificador HTTP. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**\_ \_ sesión URLCACHE de restablecimiento de opción de \_ Internet \_**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



Inicia una nueva sesión de caché para el proceso. No se requiere ningún búfer. Se usa en [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Esta opción solo se reserva para uso interno.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**\_clave de \_ \_ caché secundaria de opción \_ de Internet**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



Establece o recupera un valor de cadena que contiene la clave de caché secundaria. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Esta opción solo se reserva para uso interno.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**certificado de seguridad de la opción de INTERNET \_ \_ \_**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



Recupera el certificado de un servidor SSL/PCT (tecnología de comunicaciones privada Capa de sockets seguros) en una cadena con formato. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**\_struct de \_ certificado de seguridad de opción de Internet \_ \_**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



Recupera el certificado para un servidor SSL/PCT en la estructura de \_ información de certificado de Internet \_ . Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**\_marcas de \_ seguridad de opciones de Internet \_**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



Recupera un valor entero largo sin signo que contiene las marcas de seguridad para un identificador. [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)usa esta opción. Puede ser una combinación de los valores siguientes.

<dl> <dt>

<span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>Marca de seguridad \_ \_ 128 bits
</dt> <dd>

0x20000000

Es idéntico a la intensidad de la marca de seguridad de valor preferido. [ \_ \_ \_ ](/windows) Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>Marca de seguridad \_ \_ 40BIT
</dt> <dd>

0x10000000

Es idéntico a la intensidad de la marca de seguridad del valor preferido. [ \_ \_ \_ ](/windows) Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>Marca de seguridad \_ \_ 56BIT
</dt> <dd>

0x40000000

Idéntico al [ \_ \_ \_ medio](/windows)de la marca de seguridad del valor preferido. Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>\_Fortezza de marca de seguridad \_
</dt> <dd>

0x08000000

Indica que se ha utilizado Fortezza para proporcionar confidencialidad, autenticación o integridad para la conexión especificada.

</dd> <dt>

<span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>Marca de seguridad \_ \_ IETFSSL4
</dt> <dd>

0x00000020

Sin implementar.

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>marca de seguridad \_ \_ omitir \_ CN de certificado \_ \_ no válido
</dt> <dd>

0x00001000

Omite el mensaje de error Error de [ \_ CN de certificado de Internet \_ s \_ \_ \_ no válido](wininet-errors.md) .

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>marca de seguridad \_ \_ omitir \_ fecha de certificado \_ \_ no válida
</dt> <dd>

0x00002000

Omite el mensaje de error de la [fecha del certificado de Internet de error \_ \_ \_ \_ \_ no válido](wininet-errors.md) .

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>\_marca \_ de seguridad omitir \_ redirección \_ a \_ http
</dt> <dd>

0x00008000

Omite el [error de \_ Internet \_ https \_ a \_ http \_ en el mensaje de error de \_ redir](wininet-errors.md) .

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>\_marca \_ de seguridad omitir \_ redirección \_ a \_ https
</dt> <dd>

0x00004000

Omite el [error de \_ Internet \_ http \_ a \_ https \_ en el mensaje de error de \_ redir](wininet-errors.md) .

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>marca de seguridad \_ \_ omitir \_ revocación
</dt> <dd>

0x00000080

Omite los problemas de revocación de certificados.

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>marca de seguridad \_ \_ omitir \_ \_ CA desconocida
</dt> <dd>

0x00000100

Omite problemas de entidad de certificación desconocidos.

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>la \_ marca de seguridad \_ omite la \_ \_ firma débil
</dt> <dd>

0x00010000

Omite problemas de firma de certificado débil.

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>la \_ marca de seguridad \_ omite el \_ \_ uso incorrecto
</dt> <dd>

0x00000200

Omite problemas de uso incorrectos.

</dd> <dt>

<span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>marca de seguridad \_ \_ NORMALBITNESS
</dt> <dd>

0x10000000

Es idéntico a la [intensidad de la marca de seguridad Value \_ \_ \_ débil](/windows). Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>marca de seguridad \_ \_ PCT
</dt> <dd>

0x00000008

Sin implementar.

</dd> <dt>

<span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>Marca de seguridad \_ \_ PCT4
</dt> <dd>

0x00000010

Sin implementar.

</dd> <dt>

<span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>marca de seguridad \_ \_ segura
</dt> <dd>

0x00000001

Utiliza transferencias seguras. Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>marca de seguridad \_ \_ SSL
</dt> <dd>

0x00000002

Sin implementar.

</dd> <dt>

<span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>Indicador de seguridad \_ \_ SSL3
</dt> <dd>

0x00000004

Sin implementar.

</dd> <dt>

<span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>nivel de intensidad de marca de seguridad \_ \_ \_ medio
</dt> <dd>

0x40000000

Usa el cifrado medio (56 bits). Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>intensidad de marca de seguridad \_ \_ \_ fuerte
</dt> <dd>

0x20000000

Usa el cifrado seguro (128 bits). Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>intensidad de marca de seguridad \_ \_ \_ débil
</dt> <dd>

0x10000000

Usa el cifrado débil (40 bits). Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>marca de seguridad \_ \_ UNKNOWNBIT
</dt> <dd>

0x80000000

Se desconoce el tamaño de bits utilizado en el cifrado. Solo se devuelve en una llamada a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> </dl>

Tenga en cuenta que los datos recuperados de esta manera se relacionan con una transacción que se ha producido, cuyo nivel de seguridad ya no se puede cambiar.

</dl> </dd> <dt>

<span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**bits de la clave de seguridad de \_ opción de Internet \_ \_ \_**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



Recupera un valor entero largo sin signo que contiene el tamaño de bits de la clave de cifrado. Cuanto mayor sea el número, mayor será la intensidad de cifrado utilizada. Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). Tenga en cuenta que los datos recuperados de esta manera se relacionan con una transacción que ya se ha producido, cuyo nivel de seguridad ya no se puede cambiar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**\_rendimiento de \_ envío de opción de Internet \_**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**\_tiempo de \_ espera de envío de opción de Internet \_**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Establece o recupera un valor entero largo sin signo, en milisegundos, que contiene el valor de tiempo de espera para enviar una solicitud. Si el envío tarda más que este valor de tiempo de espera, se cancela el envío. Esta opción se puede utilizar en cualquier identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluido un identificador **nulo** . Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Cuando se utiliza en referencia a una transacción FTP, esta opción hace referencia al canal de control.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**contexto de la cadena de certificados del servidor de opciones de INTERNET \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

105
</dt> <dt>



Recupera el contexto de la cadena de certificados del servidor como un [contexto de \_ cadena \_ de PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context)duplicado. Puede pasar este contexto duplicado a cualquier función de la API de cifrado que toma un [ \_ \_ contexto de cadena de PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context). Debe llamar a [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) en el [contexto de \_ cadena \_ de PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) devuelto cuando haya terminado con el contexto de la cadena de certificados.

**Versión:** Requiere Internet Explorer 8,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**configuración de opciones de INTERNET \_ \_ \_ cambiada**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



Notifica al sistema que se ha cambiado la configuración del registro para que Compruebe la configuración de la siguiente llamada a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Se usa en [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**opción de INTERNET \_ \_ suprimir \_ autenticación de servidor \_**
</dt> <dd> <dl> <dt>

104
</dt> <dt>



Establece un objeto de solicitud HTTP que no iniciará sesión en los servidores de origen, pero realizará el inicio de sesión automático en los servidores proxy HTTP. Esta opción difiere de la marca de solicitud **Internet \_ marca \_ no \_ auth**, lo que impide la autenticación en los servidores proxy y los servidores de origen.

Si se establece este modo, se suprimirá el uso de cualquier material de credencial (ya sea el nombre de usuario o la contraseña previamente o el certificado SSL de cliente) al comunicarse con un servidor de origen. Sin embargo, si la solicitud debe estar en tránsito a través de un proxy de autenticación, WinINet seguirá realizando la autenticación automática en el proxy HTTP según la configuración de la zona de intranet del usuario. La configuración de la zona de intranet predeterminada es permitir el inicio de sesión automático con las credenciales predeterminadas del usuario.

Para garantizar la supresión de toda la información de identificación, el autor de la llamada debe combinar la **opción de Internet \_ \_ suprimir \_ \_ autenticación de servidor** con la marca de solicitud **\_ marcar \_ sin \_ cookies** .

Esta opción solo se puede establecer en los objetos de solicitud antes de que se hayan enviado. Si se intenta establecer esta opción una vez enviada la solicitud, se devolverá el **\_ \_ \_ \_ Estado de identificador incorrecto de Internet**.

No se requiere ningún búfer para esta opción. [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) lo usa solo en los identificadores devueltos por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .

**Versión:** Requiere Internet Explorer 8,0 o posterior.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**opción de INTERNET \_ \_ suprimir \_ comportamiento**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



Opción de uso general que se usa para suprimir comportamientos en todo el proceso. El parámetro *lpBuffer* de la función debe ser un puntero a un valor DWORD que contenga el comportamiento específico que se va a suprimir. Esta opción no se puede consultar con [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). Los valores permitidos son:

<dl> <dt>

<span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>INTERNET \_ suprimir \_ restablecer \_ todo
</dt> <dd>

0

Deshabilita todas las supresiones, volviendo a habilitar el comportamiento predeterminado y configurado. Esta opción es equivalente a la configuración de **Internet \_ suprimir la Directiva de \_ cookies \_ \_** y de suprimir el restablecimiento de **\_ \_ cookies \_ \_** .

**Versión:** Requiere Internet Explorer 6,0 o posterior.

</dd> <dt>

<span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>\_Directiva de supresión de \_ cookies de Internet \_ 
</dt> <dd>

1

Omite las directivas de cookies configuradas y permite establecer las cookies.

**Versión:** Requiere Internet Explorer 6,0 o posterior.

</dd> <dt>

<span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>anular \_ \_ restablecimiento de directiva de cookies de \_ Internet \_ 
</dt> <dd>

2

Deshabilita la supresión de la **\_ \_ \_ Directiva de cookies** de supresión de Internet, lo que permite la evaluación de cookies según la Directiva de cookies configurada.

**Versión:** Requiere Internet Explorer 6,0 o posterior.

</dd> <dt>

<span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span>\_supresión de \_ cookies de Internet \_
</dt> <dd>

3

Suprime la persistencia de las cookies, incluso si el servidor las ha especificado como persistentes.

**Versión:** Requiere Internet Explorer 8,0 o posterior.

</dd> <dt>

<span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>supresión de cookies de eliminación de \_ \_ cookies de \_ Internet \_
</dt> <dd>

4

Deshabilita la supresión de la cookie de supresión de **\_ \_ cookies \_ de Internet** y vuelve a habilitar la persistencia de las cookies. Las cookies suprimidas anteriormente no serán persistentes.

**Versión:** Requiere Internet Explorer 8,0 o posterior.

</dd> </dl>

</dl> </dd> <dt>

<span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**\_ \_ dirección URL de la opción de Internet**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



Recupera un valor de cadena que contiene la dirección URL completa de un recurso descargado. Si la dirección URL original contenía datos adicionales, como cadenas de búsqueda o delimitadores, o si se redirigió la llamada, la dirección URL devuelta difiere de la original. Esta opción es válida en los identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) devueltos por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**agente de usuario de la opción de INTERNET \_ \_ \_**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



Establece o recupera la cadena de agente de usuario en los identificadores proporcionados por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) y se usa en las funciones de [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) subsiguientes, siempre y cuando no se reemplace por un encabezado agregado por [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) o [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**opción de INTERNET \_ \_ nombre de usuario**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Establece o recupera una cadena que contiene el nombre de usuario asociado a un identificador devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Se usa en [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**\_versión de opción de Internet \_**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



Recupera una estructura **de \_ \_ información de versión de Internet** que contiene el número de versión de Wininet.dll. Esta opción puede usarse en un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) **nulo** por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**\_tamaño de \_ búfer de escritura de opciones de Internet \_ \_**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Establece o recupera un valor entero largo sin signo que contiene el tamaño, en bytes, del búfer de escritura. Esta opción se puede usar en los identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) devueltos por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) y [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (solo sesión FTP). Lo usa [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) y [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                   |
| Encabezado<br/>                   | <dl> <dt>Wininet. h; </dt> <dt>Winineti. h</dt> </dl> |



 

