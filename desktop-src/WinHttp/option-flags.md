---
Description: Las marcas de opciones siguientes son compatibles con WinHttpQueryOption y WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Marcas de opciones (winhttp. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 56eea8e528c445c5ce6f852ff8841073dd74d6a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718983"
---
# <a name="option-flags"></a>Marcas de opciones

Las marcas de opciones siguientes son compatibles con [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) y [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).

<dl> <dt>

<span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_opción WinHTTP \_ garantizada \_ \_ \_ devoluciones de llamada sin bloqueo**
</dt> <dd> <dl> <dt>



El valor predeterminado es FALSE. Si se establece en TRUE, WinHTTP no garantiza el progreso si la aplicación cliente bloquea las devoluciones de llamada de estado.

La aplicación cliente debe prestar especial atención para realizar operaciones mínimas dentro de la devolución de llamada sin bloqueos, devolviendo lo más rápido posible y, en particular, no debe esperar a las llamadas WinHTTP posteriores. Si no sigue estas instrucciones, es probable que se produzca un impacto negativo en el rendimiento o un posible bloqueo de la aplicación. Si se usa de la manera prescrita, esta opción puede mejorar el rendimiento.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**\_opción WinHTTP \_ Directiva de inicio de sesión automático \_**
</dt> <dd> <dl> <dt>



Establece un valor entero largo sin signo que especifica la Directiva de [Inicio de sesión automático](authentication-in-winhttp.md) con uno de los valores siguientes.

| Término | Descripción |
|-|-|
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>\_nivel de seguridad de inicio de sesión automático de WinHTTP \_ \_ \_ alto | No se usan credenciales predeterminadas. Tenga en cuenta que esta marca solo surte efecto si especifica el servidor por el nombre de equipo real. No surtirá efecto si especifica el servidor "localhost" o la dirección IP. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>\_nivel de seguridad de inicio de sesión automático de WinHTTP \_ \_ \_ bajo | Se realiza un inicio de sesión autenticado con las credenciales predeterminadas para todas las solicitudes. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>\_nivel de seguridad de inicio de sesión automático de WinHTTP \_ \_ \_ medio | Un inicio de sesión autenticado con las credenciales predeterminadas solo se realiza para las solicitudes en la Intranet local. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**devolución de llamada de la \_ opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el puntero a la función de devolución de llamada establecida con [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_contexto de \_ certificado de cliente de opción WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Establece el contexto del certificado de cliente. Si una aplicación recibe el [**error \_ WinHTTP \_ Client \_ auth \_ CERT \_ necesario**](error-messages.md), debe llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para proporcionar un certificado antes de reintentar la solicitud. Como parte del procesamiento de esta opción, WinHttp llama a [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) en el contexto de certificado proporcionado por el llamador para que el autor de la llamada pueda liberar el contexto del certificado de forma independiente.

> [!Note]
> La aplicación no debe intentar cerrar el almacén de certificados con la \_ marca de \_ marca de forzar el almacén de cierre de certificado \_ \_ en la llamada a [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) en el almacén de certificados desde el que se recuperó el contexto de certificado. Se puede producir una infracción de acceso.

Cuando el servidor solicita un certificado de cliente, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve un error de certificado de [**\_ \_ autenticación de cliente \_ \_ \_ WinHTTP**](error-messages.md) . Si el servidor solicita el certificado pero no lo requiere, la aplicación puede especificar esta opción para indicar que no tiene un certificado. El servidor puede elegir otro esquema de autenticación o permitir el acceso anónimo al servidor. La aplicación proporciona la macro de **contexto de certificado de \_ \_ cliente WinHTTP \_ \_ no** en el parámetro *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , tal y como se muestra en el ejemplo de código siguiente.

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

Si el servidor requiere un certificado de cliente, puede enviar un código de Estado HTTP 403 como respuesta. Para obtener más información, consulte la opción **WinHTTP \_ \_ \_ \_ \_ lista de emisores de certificados de cliente** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_opción WinHTTP \_ \_ lista de \_ emisores de certificados de cliente \_**
</dt> <dd> <dl> <dt>



Recupera una estructura [**de \_ IssuerListInfoEx de SecPkgContext**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) cuando el error [**de WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) es un error de certificado de **autenticación de \_ cliente WinHTTP \_ \_ \_ \_ necesario**. La lista de emisores de la estructura contiene una lista de entidades de certificación (CA) aceptables del servidor. La aplicación cliente puede filtrar la lista de CA para recuperar el certificado de cliente para la autenticación SSL.

Como alternativa, si el servidor solicita el certificado de cliente, pero no lo requiere, la aplicación puede llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la opción **WinHTTP contexto de \_ \_ \_ certificado \_ de cliente Option** . Para obtener más información, vea la opción **WinHTTP \_ contexto de \_ \_ certificado \_ de cliente** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**Página de códigos de la \_ opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece la [*Página de códigos*](glossary.md) que se usa para procesar la dirección URL (es decir, la cadena de consulta). El valor predeterminado es UTF8.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_opción WinHTTP \_ configurar \_ la \_ autenticación de Passport**
</dt> <dd> <dl> <dt>



Establece un valor entero largo sin signo que especifica si está habilitada la [autenticación de Passport en](passport-authentication-in-winhttp.md) la autenticación winhttp. El valor puede ser uno de los siguientes:

| Término | Descripción |
|-|-|
| <span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ deshabilitar la \_ autenticación de Passport \_ | Microsoft Passport la autenticación está deshabilitada. Este es el valor predeterminado. |
| <span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ deshabilitar el propio \_ vínculo de Passport \_ | El ID. de la cuenta de Passport está deshabilitado. Este es el valor predeterminado. |
| <span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ habilitar \_ autenticación de Passport \_ | La autenticación de Passport está habilitada. |
| <span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ Habilitar el \_ claves de contraseñas de Passport \_ | El ID. de cuenta de Passport está habilitado. |

</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**reintentos de conexión de la \_ opción WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el número de intentos de timesWinHTTP para conectarse a un host. Los servicios HTTP de Microsoft Windows (WinHTTP) solo intentan una vez por dirección de protocolo de Internet (IP). Por ejemplo, si intenta conectarse a un host de host múltiple que tiene 10 direcciones IP y **WinHTTP \_ Options \_ Connect \_ reintentos** está establecido en 7, WinHTTP solo intenta conectarse a las siete primeras direcciones IP. Dado el mismo conjunto de 10 direcciones IP, si **la \_ opción WinHTTP \_ Connect \_ reintentos** está establecida en 20, WinHTTP intentará cada una de las 10 solo una vez. Si un intento de conexión sigue sin funcionar después del número especificado de intentos, o si el tiempo de espera de conexión ha expirado antes de entonces, se cancela la solicitud. El valor predeterminado de **los \_ \_ \_ reintentos de la opción WinHTTP** es cinco intentos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**\_tiempo de \_ espera de conexión de la opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos. Si se establece esta opción en infinita (0xFFFFFFFF), se deshabilitará este temporizador.

Si una solicitud de conexión TCP tarda más que este valor de tiempo de espera, se cancela la solicitud. El tiempo de espera predeterminado es de 60 segundos. Cuando intenta conectarse a varias direcciones IP para un único host (un host de host múltiple), el límite de tiempo de espera es para cada conexión individual.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**información de conexión de la \_ opción WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera la dirección IP de origen y de destino, y el puerto de la solicitud que generó la respuesta cuando [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve. La aplicación llama a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con la opción de información de conexión de la **\_ opción \_ \_ WinHTTP** y proporciona la estructura de  [**información de \_ conexión \_ de WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) en el parámetro lpBuffer. Para obtener más información, **consulte \_ \_ información de conexión de WinHTTP**.

**Windows Server 2003 con SP1 y Windows XP con SP2:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**Opciones de WINHTTP \_ \_ conexiones de conexión \_ \_ v0**
</dt> <dd> <dl> <dt>



Recupera la estructura de [**TCP \_ info \_ V0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) para la conexión subyacente utilizada por la solicitud. La estructura devuelta puede contener estadísticas de solicitudes anteriores enviadas a través de la misma conexión.

> [!Note]
> Esta opción se ha sustituido por **la \_ opción de WinHTTP estadísticas de \_ conexión \_ \_ v1**.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**Opciones de WINHTTP \_ \_ conexiones de conexión \_ \_ v1**
</dt> <dd> <dl> <dt>



Recupera la estructura de [**TCP \_ info \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) para la conexión subyacente utilizada por la solicitud. La estructura devuelta puede contener estadísticas de solicitudes anteriores enviadas a través de la misma conexión.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**valor de contexto de la \_ opción WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor de **DWORD \_ ptr** que contiene un puntero al valor de contexto asociado a este identificador de [HINTERNET](hinternet-handles-in-winhttp.md) . Se utiliza el valor almacenado en el búfer y se asigna un nuevo valor al marcador de opción de valor de contexto de la **\_ opción \_ \_ WinHTTP** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**descompresión de la \_ opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece un valor DWORD de marcas que determinan si WinHTTP descomprime automáticamente los cuerpos de respuesta con codificaciones de contenido comprimido. WinHTTP también establecerá un encabezado de Accept-Encoding adecuado, invalidando cualquier proporcionado por el autor de la llamada. Los valores admitidos son:

| Término | Descripción |
|-|-|
| <span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_marca de descompresión WinHTTP \_ \_ gzip | Descomprimir la codificación de contenido: respuestas gzip. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>\_marca de DEScompresión de WinHTTP \_ \_ DEFLATE | Descomprimir contenido-codificación: DEFLATE las respuestas. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_marca de descompresión WinHTTP \_ \_ | Descomprima las respuestas con cualquier codificación de contenido compatible. |

De forma predeterminada, WinHTTP proporcionará respuestas comprimidas al autor de la llamada sin modificar.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**\_característica de \_ deshabilitación de WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece un valor entero largo sin signo que especifica qué características están deshabilitadas con una o varias de las marcas siguientes. Tenga en cuenta que esta característica solo se debe pasar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) en los identificadores de solicitud después de que el identificador de solicitud se cree con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)y antes de que la solicitud se envíe con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

| Término | Descripción |
|-|-|
| <span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ deshabilitar \_ autenticación | La autenticación automática está deshabilitada. |
| <span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ deshabilitar \_ cookies | La adición automática de encabezados de cookies a solicitudes está deshabilitada. Además, las cookies devueltas no se agregan automáticamente a la base de datos de cookies. Deshabilitar las cookies puede dar lugar a un rendimiento deficiente de la autenticación de Passport. |
| <span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ deshabilitar \_ Keep \_ Alive | Deshabilita la semántica Keep-Alive para la conexión. La semántica Keep-Alive es necesaria para MSN, NTLM y otros tipos de autenticación. |
| <span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>\_deshabilitar \_ redirecciones de WinHTTP | La redirección automática se deshabilita al enviar solicitudes con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Si la redirección automática está deshabilitada, una aplicación debe registrar una función de devolución de llamada para que la autenticación de Passport se realice correctamente. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_opción WinHTTP \_ deshabilitar la \_ reserva de \_ protocolo seguro \_**
</dt> <dd> <dl> <dt>



Impide que WinHTTP vuelva a intentar una conexión con una versión inferior del Protocolo de seguridad cuando se produce un error en la negociación inicial del protocolo.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**\_opción WinHTTP \_ deshabilitar la \_ cola de Stream \_**
</dt> <dd> <dl> <dt>



Permite que las nuevas solicitudes abran una conexión HTTP/2 adicional cuando se alcanza el límite máximo de flujos simultáneos, en lugar de esperar a la siguiente secuencia disponible en una conexión existente.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**\_característica de \_ habilitación de WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece un valor entero largo sin signo que especifica las características habilitadas actualmente. Puede ser uno de los valores siguientes.

| Término | Descripción |
|-|-|
| <span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ habilitar \_ la \_ \_ suplantación de SSL | Si está habilitada, WinHTTP revierte temporalmente la suplantación del cliente por la duración de las operaciones de autenticación de certificado SSL. Este valor solo se puede establecer en el identificador de sesión. |
| <span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ habilitar \_ \_ revocación de SSL | Si está habilitada, WinHTTP permite la revocación de SSL. Este valor solo se puede establecer en el identificador de solicitud. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**\_opción WinHTTP \_ habilitar \_ \_ protocolo http**
</dt> <dd> <dl> <dt>



Establece una máscara de máscara DWORD de versiones de HTTP avanzadas aceptables. Los valores posibles son:

| Término | Descripción |
|-|-|
| <span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_Marca de protocolo WinHTTP \_ \_ HTTP2 (0x1) | Habilita HTTP/2 para la solicitud. |
| Ninguno (0X0) | Restringe la solicitud a HTTP/1.1 y versiones anteriores. |

Las versiones heredadas de HTTP (1,1 y anteriores) no se pueden deshabilitar con esta opción. El valor predeterminado es 0X0.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_opción WinHTTP \_ enabletracing (**
</dt> <dd> <dl> <dt>



Establece un valor **booleano** que especifica si el seguimiento está habilitado actualmente. Para obtener más información acerca de la utilidad de seguimiento en WinHTTP, consulte [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md). Esta opción solo se puede establecer en un identificador **HINTERNET** **nulo** .


</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**opción de WINHTTP \_ \_ codificación \_ adicional**
</dt> <dd> <dl> <dt>



Habilita la codificación porcentual de la dirección URL para la ruta de acceso y la cadena de consulta.

Como alternativa, puede codificar por porcentaje antes de llamar a WinHttp.

</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**\_ \_ error extendido de la opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera un valor entero largo sin signo que contiene un código de error de Microsoft Windows Sockets que se asignó al ERROR \_ WinHTTP \_ \* mensajes de error devueltos en este contexto de subproceso. Puede pasar **null** como valor de identificador.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**\_Opciones WinHTTP \_ de \_ credenciales de proxy global \_**
</dt> <dd> <dl> <dt>



Toma un puntero a una estructura de [**\_ credenciales de WinHTTP \_ ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con el parámetro de la función *hInternet* establecido en **null**. Esta opción requiere la clave del registro **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings! ShareCredsWithWinHttp**. Si esta clave del registro no está establecida, WinHTTP devolverá un error de error **\_ WinHTTP \_ no válido \_**. Esta clave del registro no está presente de forma predeterminada. Cuando se establece, WinINet enviará las credenciales a WinHTTP. Siempre que WinHttp obtiene un desafío de autenticación y si no hay ninguna credencial establecida en el identificador actual, utilizará las credenciales proporcionadas por WinINet. Para compartir las credenciales del servidor además de las credenciales del proxy, los usuarios deben establecer la **\_ opción WinHTTP \_ usar \_ \_ \_ credenciales de servidor globales** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_Opciones de \_ WinHTTP \_ credenciales de servidor global \_**
</dt> <dd> <dl> <dt>



Toma un puntero a una estructura de [**\_ credenciales de WinHTTP \_ ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con el parámetro de la función *hInternet* establecido en **null**. Esta opción requiere la clave del registro **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings! ShareCredsWithWinHttp**. Si esta clave del registro no está establecida, WinHTTP devolverá un error de error **\_ WinHTTP \_ no válido \_**. Esta clave del registro no está presente de forma predeterminada. Cuando se establece, WinINet enviará las credenciales a WinHTTP. Siempre que WinHttp obtiene un desafío de autenticación y si no hay ninguna credencial establecida en el identificador actual, utilizará las credenciales proporcionadas por WinINet. Para compartir las credenciales del servidor además de las credenciales del proxy, los usuarios deben establecer la **\_ opción WinHTTP \_ usar \_ \_ \_ credenciales de servidor globales** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**\_tipo de \_ identificador de opción de WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera un valor entero largo sin signo que contiene el tipo del identificador de [HINTERNET](hinternet-handles-in-winhttp.md) que se ha pasado. El valor devuelto puede ser cualquiera de los siguientes:

| Término | Descripción |
|-|-|
| <span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>tipo de identificador de WINHTTP \_ \_ \_ Connect | El identificador es un identificador de conexión. |
| <span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_solicitud de \_ tipo de control de WinHTTP \_ | El identificador es un identificador de solicitud. |
| <span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>\_sesión de \_ tipo de controlador de WinHTTP \_ | El identificador es un identificador de sesión. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**se \_ requiere la opción WinHTTP \_ \_ protocolo HTTP \_**
</dt> <dd> <dl> <dt>



Impide que las versiones de protocolo que no estén habilitadas por la **\_ opción WinHTTP \_ habiliten el \_ \_ protocolo http** para la solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**se \_ usó la opción WinHTTP \_ \_ protocolo HTTP \_**
</dt> <dd> <dl> <dt>



Obtiene un valor DWORD que indica qué versión de HTTP avanzada se usó en una solicitud determinada. Para obtener una lista de los valores posibles, consulte la **opción de WinHTTP \_ Habilitar el \_ \_ \_ protocolo http**.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_ \_ versión http de la opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece o recupera una estructura [**de \_ \_ información de versión de http**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) que contiene la versión de http que se admite. Se trata de una opción para todo el proceso; Use **null** para el identificador.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**\_opción WinHTTP \_ omitir la \_ \_ revocación de certificados \_ sin conexión**
</dt> <dd> <dl> <dt>



Permite que las conexiones seguras utilicen certificados de seguridad para los que no se pudo descargar la lista de revocación de certificados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_Opción WinHTTP \_ de \_ reserva rápida IPv6 \_**
</dt> <dd> <dl> <dt>



Habilita la reserva rápida IPv6 (los ojos más felices) para la conexión. Este comportamiento es similar al comportamiento de los ojos que se describe en [RFC 6555](https://tools.ietf.org/html/rfc6555) para mejorar los tiempos de conexión en redes en las que IPv6 no es confiable.
- Si se resuelven direcciones IPv6 e IPv4 para un host determinado, WinHttp comenzará conectándose a la primera dirección IPv6 resuelta con un tiempo de espera corto (300 ms).
- En caso de que se produzca un error en la conexión, WinHttp intentará conectarse a la primera dirección IPv4 resuelta con el tiempo de espera estándar.
- Si se produce un error en la segunda conexión, WinHttp volverá a intentar la primera dirección IPv6 resuelta con el tiempo de espera estándar.
- Si se produce un error en la tercera conexión, WinHttp revertirá al comportamiento predeterminado de las direcciones restantes, intentando una conexión a cada una de ellas con el tiempo de espera estándar hasta que se realice una conexión o no se mantenga ninguna dirección.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**la \_ opción \_ WinHTTP \_ es \_ respuesta de conexión de proxy \_**
</dt> <dd> <dl> <dt>



Obtiene si se puede recuperar o no una respuesta de conexión de devolución de proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_Opción WinHTTP \_ Max \_ Conex. \_ por \_ \_ servidor 1 0 \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por servidor HTTP/1.0. El valor predeterminado es **infinito**.

**Windows Vista con SP1 y Windows Server 2008:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_opción WinHTTP \_ Max \_ Conex. \_ por \_ servidor**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por servidor. El valor predeterminado es **infinito**.

Cuando esta opción se establece en cero, WinHTTP establece el límite del número de conexiones en 2.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**\_ \_ número máximo de \_ \_ \_ redirecciones HTTP automáticas de la opción WinHTTP**
</dt> <dd> <dl> <dt>



Establece el número máximo de redirecciones que sigue WinHTTP; el valor predeterminado es 10. Este límite evita que sitios no autorizados realicen la pausa del cliente WinHTTP después de un gran número de redirecciones.

**Windows XP con SP1 y windows 2000 con SP3:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_opción WinHTTP \_ Max \_ http \_ status \_ continue**
</dt> <dd> <dl> <dt>



El número máximo de respuestas de código de estado 100-199 informativas omitidas antes de devolver el código de estado final al cliente WinHTTP. El servidor puede enviar códigos de estado informativos 100-199 antes del código de estado final y se describen en la especificación de HTTP/1.1 (para obtener más información, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)). El valor predeterminado es 10.

**Windows XP con SP1 y windows 2000 con SP3:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**tamaño máximo de límite de respuesta de la \_ opción WinHTTP \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Un límite en la cantidad de datos purgados de las respuestas para reutilizar una conexión, que se especifica en bytes. El valor predeterminado es 1 MB.

**Windows XP con SP1 y windows 2000 con SP3:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**\_ \_ tamaño máximo del \_ encabezado de respuesta \_ \_ de la opción WinHTTP**
</dt> <dd> <dl> <dt>



Conjunto enlazado en el tamaño máximo de la parte del encabezado de la respuesta del servidor, especificado en bytes. Este enlace protege el cliente de un servidor no autorizado que intenta detenerse el cliente mediante el envío de una respuesta con una cantidad infinita de datos de encabezado. El valor predeterminado es 64 KB.

**Windows XP con SP1 y windows 2000 con SP3:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ identificador primario de la opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el identificador primario de este identificador.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**\_opción WinHTTP \_ \_ texto de personalización de marca de Passport \_**
</dt> <dd> <dl> <dt>



Recupera una cadena que contiene el texto de [*Personalización de marca*](glossary.md) proporcionado por el servidor de inicio de sesión de Passport. Esta opción debe recuperarse inmediatamente después de que el servidor de inicio de sesión responda con un código de estado 401. Una aplicación debe pasar un tamaño de búfer, en bytes, que es lo suficientemente grande como para contener la cadena devuelta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_ \_ \_ dirección URL de copersonalización de Passport \_ de la opción WinHTTP**
</dt> <dd> <dl> <dt>



Recupera una cadena que contiene una dirección URL para un gráfico de [*cobranding*](glossary.md) proporcionado por el servidor de inicio de sesión de Passport. Esta opción debe recuperarse inmediatamente después de que el servidor de inicio de sesión responda con un código de estado 401. Una aplicación debe pasar un tamaño de búfer, en bytes, que es lo suficientemente grande como para contener la cadena devuelta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_ \_ \_ dirección URL de retorno de Passport \_ de la opción WinHTTP**
</dt> <dd> <dl> <dt>



Establece una opción de solo lectura en un identificador de solicitud que recupera la dirección URL de retorno de Passport.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**opción de WINHTTP \_ \_ Inicio de sesión de Passport \_ \_**
</dt> <dd> <dl> <dt>



Establece la opción en un identificador de sesión para cerrar la sesión de cualquier inicio de sesión de Passport. Una aplicación debe pasar la dirección URL de retorno de Passport que se recuperó con la **\_ opción WinHTTP \_ \_ \_ dirección URL de retorno de Passport**. Se borran todas las cookies relacionadas con la dirección URL de retorno.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**contraseña de la \_ opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor de cadena que contiene la contraseña asociada a un identificador de solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_proxy de opción de WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece o recupera una estructura [**de \_ \_ información del proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contiene los datos de proxy en un identificador de sesión o identificador de solicitud existente. Al recuperar datos de proxy, una aplicación debe liberar las cadenas **lpszProxy** y **lpszProxyBypass** contenidas en esta estructura (si no son **null**) mediante la función [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) . Una aplicación puede consultar los datos de proxy global (el proxy predeterminado) pasando un identificador **nulo** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**contraseña del proxy de la \_ opción WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor de cadena que contiene la contraseña utilizada para tener acceso al proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**se \_ \_ usó el \_ SPN del proxy \_ de la opción WinHTTP**
</dt> <dd> <dl> <dt>



Obtiene el nombre de entidad de seguridad del servidor proxy que WinHTTP proporcionó a SSPI durante la autenticación. Este valor de cadena se usefor pasando a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) después de un error de autenticación.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_nombre de \_ usuario de proxy de opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor de cadena que contiene el nombre de usuario utilizado para tener acceso al proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_tamaño del \_ búfer de lectura \_ \_ de la opción WinHTTP**
</dt> <dd> <dl> <dt>



Esta opción está en desuso; no tiene ningún efecto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**\_opción WinHTTP \_ recibir \_ respuesta de conexión de proxy \_ \_**
</dt> <dd> <dl> <dt>



Establece si se puede recuperar o no la entidad de respuesta del proxy. Esta opción está deshabilitada de forma predeterminada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**\_tiempo de \_ espera de respuesta de recepción \_ \_ de la opción WinHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, que se va a esperar para recibir todos los encabezados de respuesta a una solicitud. Si WinHTTP no recibe todos los encabezados dentro de este período de tiempo de espera, se cancela la solicitud. El valor de tiempo de espera predeterminado es de 90 segundos.

Este tiempo de espera solo se comprueba cuando se reciben datos del socket. Como resultado, cuando el tiempo de espera expira, no se notifica a la aplicación cliente hasta que llegan más datos desde el servidor. Si no llega ningún dato del servidor, el retraso entre la expiración del tiempo de espera y la notificación de la aplicación cliente podría ser tan grande como el valor de tiempo de espera establecido mediante el parámetro *dwReceiveTimeout* de la función [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_tiempo de \_ espera de recepción de la opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para recibir una respuesta parcial a una solicitud o leer algunos datos. Si la respuesta tarda más que este valor de tiempo de espera, se cancela la solicitud. El valor predeterminado del tiempo de espera es de 30 segundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**\_Directiva de \_ redirección de la opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece el comportamiento de WinHTTP con respecto a la administración de un código de estado de redirección HTTP de 30 veces. Esta opción se puede establecer en una sesión o en un identificador de solicitud a uno de los siguientes valores:

| Término | Descripción |
|-|-|
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>\_Directiva de \_ redireccionamiento de la opción WinHTTP \_ \_ siempre | Todas las redirecciones se siguen automáticamente. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>la \_ Directiva de REdirección de la opción WinHTTP no \_ \_ \_ permite \_ https \_ a \_ http | Se siguen todas las redirecciones, excepto las que se originan desde una dirección URL segura (https) a una dirección URL no segura (http). Esta es la configuración predeterminada. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>\_Directiva de REdirección de la opción WinHTTP \_ \_ \_ nunca | Nunca se siguen las redirecciones. El estado 30 se devuelve a la aplicación. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_opción \_ de WinHTTP rechazar \_ USERPWD en la \_ \_ dirección URL**
</dt> <dd> <dl> <dt>



Rechaza las direcciones URL que contienen un nombre de usuario y una contraseña. Esta opción también rechaza las direcciones URL que contienen el *nombre de usuario:* la semántica de contraseña, aunque no se especifique ningún nombre de usuario ni contraseña. Por ejemplo, " u:p@hostname ", " :@hostname ", " u:@hostname " y " :p@hostname " se marcarían como no válidos. Si se pasa una dirección URL no válida a la función, devuelve el [error \_ WinHTTP \_ \_ URL no válida](error-messages.md). Esta opción está desactivada de forma predeterminada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**prioridad de solicitud de la \_ opción WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Esta opción está en desuso; no tiene ningún efecto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**estadísticas de solicitud de la \_ opción WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera estadísticas de la solicitud.  Para obtener una lista de las estadísticas disponibles, consulte estadísticas de [**solicitud de WinHTTP \_ \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**tiempos de solicitud de la \_ opción WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera información de tiempo para la solicitud. Para obtener una lista de los intervalos disponibles, consulte [**los \_ \_ tiempos de solicitud de WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**\_tiempo de \_ espera de resolución de la opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para resolver un nombre de host. El valor de tiempo de espera predeterminado es **infinito**. Si se especifica un valor no predeterminado, se produce una sobrecarga en la creación de un subproceso por cada resolución de nombres.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**\_ \_ protocolos seguros de la opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece un valor entero largo sin signo que especifica los protocolos seguros que son aceptables. De forma predeterminada, solo se habilitan SSL3 y TLS1 en Windows 7 y Windows 8. De forma predeterminada, solo se habilitan SSL3, TLS 1.0, TLS 1.1 y TLS 1.2 en Windows 8.1 y Windows 10. El valor puede ser una combinación de uno o varios de los valores siguientes.

| Término | Descripción |
|-|-|
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>\_ \_ protocolo seguro de marca WinHTTP \_ \_ | Se pueden usar los protocolos Capa de sockets seguros (SSL) 2,0, SSL 3,0 y seguridad de la capa de transporte (TLS) 1,0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>\_Protocolo seguro de marca WinHTTP \_ \_ \_ SSL2 | Se puede usar el protocolo SSL 2,0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>\_Protocolo de seguridad de marca WinHTTP \_ \_ \_ SSL3 | Se puede usar el protocolo SSL 3,0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>\_Protocolo seguro de marca WinHTTP \_ \_ \_ TLS1 | Se puede usar el protocolo TLS 1,0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>\_Protocolo seguro de marca WinHTTP \_ \_ \_ TLS1 \_ 1 | Se puede usar el protocolo TLS 1,1. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>\_Protocolo seguro de marca de WinHTTP \_ \_ \_ TLS1 \_ 2 | Se puede usar el protocolo TLS 1,2. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_opción WinHTTP \_ certificado de seguridad ( \_ \_ struct)**
</dt> <dd> <dl> <dt>



Recupera el certificado para un servidor SSL/TLS en la estructura [**de \_ \_ información del certificado WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) . La aplicación debe liberar los miembros **lpszSubjectInfo** y **lpszIssuerInfo** con [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**marcas de seguridad de la \_ opción WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene las marcas de seguridad para un identificador. Puede ser una combinación de estos valores:

| Término | Descripción |
|-|-|
| <span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>marca de seguridad \_ \_ omitir \_ CN de certificado \_ \_ no válido |Permite un nombre común no válido en un certificado; es decir, el nombre de servidor especificado por la aplicación no coincide con el nombre común del certificado. Si se establece esta marca, la aplicación no recibirá una **marca de estado de devolución de llamada de WinHTTP de \_ \_ \_ \_ certificado \_ CN \_ no válida** . |
| <span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>marca de seguridad \_ \_ omitir \_ fecha de certificado \_ \_ no válida |Permite una fecha de certificado no válida, es decir, un certificado expirado o no vigente. Si se establece esta marca, la aplicación no recibirá un indicador de estado de devolución de llamada de WinHTTP fecha de certificado de devolución de llamada **\_ \_ \_ \_ \_ \_ no válida** . |
| <span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>marca de seguridad \_ \_ omitir \_ \_ CA desconocida | Permite una entidad de certificación no válida. Si se establece esta marca, la aplicación no recibe un marcador de estado de devolución de llamada de WinHTTP llamada de **\_ \_ \_ \_ \_ CA no válida** . |
| <span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>la \_ marca de seguridad \_ omite el \_ \_ uso incorrecto de certificados \_ | Permite establecer la identidad de un servidor con un certificado que no sea de servidor (por ejemplo, un certificado de cliente). |
| <span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>la \_ marca de seguridad \_ omite la \_ \_ firma débil | Permite omitir una firma débil.<br/>Esta marca está disponible en la actualización de acumulación para cada sistema operativo a partir de Windows 7 y Windows Server 2008 R2. |
| <span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>marca de seguridad \_ \_ segura | Utiliza transferencias seguras. Solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>nivel de intensidad de marca de seguridad \_ \_ \_ medio | Usa el cifrado medio (56 bits). Solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>intensidad de marca de seguridad \_ \_ \_ fuerte | Usa el cifrado seguro (128 bits). Solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>intensidad de marca de seguridad \_ \_ \_ débil | Usa el cifrado débil (40 bits). Solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**información de seguridad de la \_ opción WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera la conexión SChannel y la información de cifrado de una solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**\_bits de \_ clave de seguridad \_ \_ de la opción WinHTTP**
</dt> <dd> <dl> <dt>



Recupera un valor entero largo sin signo que contiene la intensidad de cifrado de la clave de cifrado. Un número mayor indica un cifrado de intensidad de cifrado más seguro.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**\_tiempo de \_ espera de envío de opción de WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para enviar una solicitud o escribir algunos datos. Si el envío de la solicitud tarda más que el tiempo de espera, se cancela la operación de envío. El tiempo de expiración predeterminado es de 30 segundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ OPTION \_ Server \_ CBT**
</dt> <dd> <dl> <dt>



Obtiene un puntero a la estructura de [**\_ enlaces de SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) que especifica un token de enlace de canal (CBT).

Un token de enlace de canal es una propiedad de un canal de transporte seguro y se utiliza para enlazar un canal de autenticación con el canal de transporte seguro. Este token solo se puede obtener mediante esta opción una vez establecida una conexión SSL.

> [!Note]
> Si se pasa esta opción y un valor **null** para *lpBuffer* a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) , se devolverá un error de \_ búfer insuficiente \_ y el tamaño de bytes necesario para el búfer en el parámetro *lpdwBufferLength* . Este valor de tamaño de búfer devuelto se puede pasar en una llamada subsiguiente a la consulta para el token de enlace de canal. Estos pasos son necesarios para controlar \_ \_ \_ la solicitud de estado de devolución de llamada de WinHTTP si desea modificar los encabezados de solicitud basados en el token de enlace de canal. Tenga en cuenta que Windows XP y vista no admiten la modificación de encabezados de solicitud durante esta devolución de llamada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**el \_ contexto de la cadena de certificados del servidor de opciones WinHTTP \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera el contexto de la cadena de certificación del servidor. **WinHTTP \_ OPTION \_ Server \_ el \_ \_ contexto** de la cadena de certificados se puede pasar para obtener un puntero duplicado al **\_ \_ contexto** de la cadena de certificados de una cadena de certificados de servidor recibida durante una conexión SSL negociada. El cliente debe llamar a [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) en el puntero de contexto PCCERT devuelto \_ que se rellena en el búfer.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**\_contexto de \_ certificado de servidor de opciones WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera el contexto de certificación del servidor. **WinHTTP \_ Se puede pasar el \_ \_ \_ contexto de certificado de servidor de opción** para obtener un puntero duplicado al [**contexto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificado para un certificado de servidor recibido durante una conexión SSL negociada. El cliente debe llamar a [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) en el puntero de contexto PCCERT devuelto \_ que se rellena en el búfer.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**se \_ \_ usó el \_ SPN del servidor de opciones WinHTTP \_**
</dt> <dd> <dl> <dt>



Obtiene el nombre de la entidad de seguridad del servidor que WinHTTP proporcionó a SSPI durante la autenticación. Este valor de cadena se puede pasar a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) después de un error de autenticación.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**opción WINHTTP de \_ \_ SPN**
</dt> <dd> <dl> <dt>



Incluye o quita el número de puerto del servidor cuando el SPN (nombre de entidad de seguridad de servicio) se crea para Kerberos o para negociar la autenticación Kerberos. Esta marca es uno de los valores siguientes:

| Término | Descripción |
|-|-|
| <span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ deshabilitar el \_ \_ Puerto del servidor SPN \_ | Quita el número de puerto del servidor. |
| <span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ habilitar \_ \_ Puerto de servidor SPN \_ | Incluye el número de puerto del servidor. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**\_opción WinHTTP \_ TCP \_ Fast \_ Open**
</dt> <dd> <dl> <dt>



Habilita TCP Fast Open para la conexión.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**\_opción WinHTTP \_ TLS \_ false \_ Start**
</dt> <dd> <dl> <dt>



Habilita el inicio de TLS falso para la conexión.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**opción de WINHTTP \_ \_ Descargar \_ evento de notificación \_**
</dt> <dd> <dl> <dt>



Toma un evento que se establecerá cuando se haya completado la última devolución de llamada para una sesión determinada. Esta marca debe usarse en un identificador de sesión. El evento no se puede cerrar hasta que WinHTTP lo haya establecido.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**\_análisis de \_ encabezado no \_ seguro \_ de la opción WinHTTP**
</dt> <dd> <dl> <dt>



Esta opción está reservada para uso interno y no debe llamarse.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**\_actualización de la opción WinHTTP \_ \_ al \_ \_ socket Web**
</dt> <dd> <dl> <dt>



Indica a la pila que inicie un proceso de protocolo de enlace de WebSocket con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Esta opción no toma ningún parámetro.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**\_ \_ dirección URL de la opción WinHTTP**
</dt> <dd> <dl> <dt>



Recupera un valor de cadena que contiene la dirección URL completa de un recurso descargado. Si la dirección URL original contenía datos adicionales, como cadenas de búsqueda o delimitadores, o si se redirigió la llamada, la dirección URL devuelta difiere de la original. La aplicación debe pasar un búfer, con el tamaño en bytes, que es lo suficientemente grande como para contener la dirección URL devuelta en caracteres anchos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_opción WinHTTP \_ usar \_ \_ credenciales de servidor globales \_**
</dt> <dd> <dl> <dt>



Toma un valor **booleano** y solo se puede establecer un identificador de sesión. Solo se propagará hacia abajo hasta los identificadores creados desde el identificador de sesión después de que se haya establecido la opción. Si **es true**, esta opción hace que se reordene el uso de las credenciales de servidor globales que se han insertado desde Wininet. El valor predeterminado para esta opción es **false**. Esta opción requiere la clave del registro **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings! ShareCredsWithWinHttp**. Esta clave del registro no está presente de forma predeterminada. Cuando se establece, WinINet enviará las credenciales a WinHTTP. Siempre que WinHttp obtiene un desafío de autenticación y si no hay ninguna credencial establecida en el identificador actual, utilizará las credenciales proporcionadas por WinINet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**agente de usuario de la \_ opción WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Establece o recupera la cadena [*de agente de usuario*](glossary.md) en los identificadores proporcionados por [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) y se usa en las funciones de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) subsiguientes, siempre y cuando no se reemplace por un encabezado agregado por [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) o **WinHttpSendRequest**. Al recuperar un agente de usuario, la aplicación debe pasar un búfer, con un tamaño en bytes, que es lo suficientemente grande como para contener la dirección URL devuelta en caracteres anchos. Al establecer el agente de usuario, el tamaño del búfer es la longitud de la cadena, en caracteres, más el terminador **nulo** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**nombre de usuario de la \_ opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece o recupera una cadena que contiene el nombre de usuario.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_tiempo de \_ \_ espera de cierre de socket Web \_ de la opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece el tiempo, en milisegundos, que [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) debe esperar para completar el protocolo de enlace de cierre. El valor predeterminado es 10 segundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**\_intervalo de \_ \_ KEEPALIVE de socket Web \_ \_ de la opción WinHTTP**
</dt> <dd> <dl> <dt>



Establece el intervalo, en milisegundos, para enviar un paquete Keep-Alive a través de la conexión. El intervalo predeterminado es 30000 (30 segundos). El intervalo mínimo es 15000 (15 segundos). El uso de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para establecer un valor inferior a 15000 devolverá un **\_ \_ parámetro no válido**.

> [!Note]
> El valor predeterminado de **la \_ opción \_ WinHTTP \_ \_ \_ intervalo de KEEPALIVE de socket web** se lee desde **HKLM: \\ software \\ Microsoft \\ WebSocket \\ KeepaliveInterval**. Si no se establece un valor, se usará el valor predeterminado de 30000. No es posible tener un intervalo de KeepAlive inferior de 15000 milisegundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**\_tamaño del \_ \_ búfer de recepción de socket Web \_ \_ de la opción \_ WinHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera un valor DWORD que especifica el tamaño del búfer de recepción que se va a usar en las conexiones de WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**\_tamaño del \_ \_ búfer de envío del socket Web \_ \_ de la opción \_ WinHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera un valor DWORD que especifica el tamaño del búfer de envío que se va a usar en las conexiones de WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**\_recuento \_ de \_ subprocesos de trabajador de la opción WinHTTP \_**
</dt> <dd> <dl> <dt>



Establece un valor entero largo sin signo que especifica el número de subprocesos de trabajo que el grupo de subprocesos debe utilizar para las finalizaciones asincrónicas. El valor predeterminado de esta opción es cero, que especifica que el número de subprocesos de trabajo es igual al número de CPU del sistema. Esta opción solo se puede establecer en un identificador [HINTERNET](hinternet-handles-in-winhttp.md) **nulo** antes de que se haya producido una operación asincrónica.   Esta opción solo se puede establecer una vez.

**Windows Server 2008 R2 y Windows 7:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_tamaño del \_ búfer de escritura \_ \_ de la opción WinHTTP**
</dt> <dd> <dl> <dt>



Esta opción está en desuso; no tiene ningún efecto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

En la tabla siguiente se enumeran las marcas de opciones mediante la especificación de los identificadores en los que pueden actuar, si se pueden consultar y establecer, y el tipo de datos utilizado. Una "X" indica que la marca de opción es válida para su uso con la función o el identificador, mientras que "-" especifica que el marcador de opción no es válido.

Si intenta establecer o consultar una marca de opción en una versión de Windows en la que no se admite, se producirá un error en la **\_ \_ \_ opción WinHTTP no válido**.

| Marca de opción y tipo de datos | Identificador de sesión | Identificador de solicitud | Opción de consulta | Opción SET | Versión mínima de Windows |
|-|-|-|-|-|-|
| \_opción WinHTTP \_ garantizada \_ \_ \_ devoluciones de llamada sin bloqueo<br/>**BOOLEANO** | X | \- | \- | X | \- |
| \_opción WinHTTP \_ Directiva de inicio de sesión automático \_<br/>**DWORD** | \- | X | \- | X | \- |
| devolución de llamada de la \_ opción WinHTTP \_<br/>**LPVOID** | X | X | X | X | \- |
| \_contexto de \_ certificado de cliente de opción WinHTTP \_ \_<br/>[**contexto de certificado \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | \- | X | Windows Vista |
| \_opción WinHTTP \_ \_ lista de \_ emisores de certificados de cliente \_<br/>[**SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | X | X | \- | Windows Vista |
| Página de códigos de la \_ opción WinHTTP \_<br/>**DWORD** | X | \- | \- | X | \- |
| \_opción WinHTTP \_ configurar \_ la \_ autenticación de Passport<br/>**DWORD** | X | \- | \- | X | \- |
| reintentos de conexión de la \_ opción WinHTTP \_ \_<br/>**DWORD** | X | X | X | X | \- |
| \_tiempo de \_ espera de conexión de la opción WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| información de conexión de la \_ opción WinHTTP \_ \_<br/>[**\_información de conexión de WinHTTP \_**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | X | X | \- | \- |
| Opciones de WINHTTP \_ \_ conexiones de conexión \_ \_ v0<br/>[**Información de TCP \_ \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | X | X | \- | Windows 10 versión 1903 |
| Opciones de WINHTTP \_ \_ conexiones de conexión \_ \_ v1<br/>[**Información de TCP \_ \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | X | X | \- | Windows 10 versión 2004 |
| valor de contexto de la \_ opción WinHTTP \_ \_<br/>**DWORD \_ ptr** | X | X | X | X | \- |
| descompresión de la \_ opción WinHTTP \_<br/>**DWORD** | X | X | \- | X | Windows 8.1 |
| \_característica de \_ deshabilitación de WinHTTP \_<br/>**DWORD** | \- | X | \- | X | \- |
| \_opción WinHTTP \_ deshabilitar la \_ reserva de \_ protocolo seguro \_<br/>**BOOLEANO** | X | \- | \- | X | Windows 10 versión 1903 |
| \_opción WinHTTP \_ deshabilitar la \_ cola de Stream \_<br/>**BOOLEANO** | X | X | \- | X | Windows 10 versión 1809 |
| \_característica de \_ habilitación de WinHTTP \_<br/>**DWORD** | \* | \* | \- | X | \- |
| \_opción WinHTTP \_ habilitar \_ \_ protocolo http<br/>**DWORD** | X | X | \- | X | Windows 10 Versión 1607 |
| \_opción WinHTTP \_ enabletracing (<br/>**DWORD** | \- | \- | X | X | \- |
| opción de WINHTTP \_ \_ codificación \_ adicional<br/>**BOOLEANO** | X | X | \- | X | Windows 10 versión 1803 |
| \_ \_ error extendido de la opción WinHTTP \_<br/>**DWORD** | X | X | X | \- | \- |
| \_Opciones WinHTTP \_ de \_ credenciales de proxy global \_<br/>[**\_credenciales de WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | X | X | \- | X | \- |
| \_Opciones de \_ WinHTTP \_ credenciales de servidor global \_<br/>[**\_credenciales de WinHTTP \_ ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | X | X | \- | X | \- |
| \_tipo de \_ identificador de opción de WinHTTP \_<br/>**DWORD** | X | X | X | \- | \- |
| se \_ requiere la opción WinHTTP \_ \_ protocolo HTTP \_<br/>**BOOLEANO** | X | X | \- | X | Windows 10 versión 1903 |
| se \_ usó la opción WinHTTP \_ \_ protocolo HTTP \_<br/>**DWORD** | \- | X | X | \- | Windows 10 Versión 1607 |
| \_ \_ versión http de la opción WinHTTP \_<br/>[**\_información de versión de http \_**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | X | X | X | X | \- |
| \_opción WinHTTP \_ omitir la \_ \_ revocación de certificados \_ sin conexión<br/>**BOOLEANO** | \- | X | \- | X | Windows 10 versión 2004 |
| \_Opción WinHTTP \_ de \_ reserva rápida IPv6 \_<br/>**BOOLEANO** | X | \- | \- | X | Windows 10 versión 1903 |
| la \_ opción \_ WinHTTP \_ es \_ respuesta de conexión de proxy \_<br/>**BOOLEANO** | X | X | X | \- | \- |
| \_Opción WinHTTP \_ Max \_ Conex. \_ por \_ \_ servidor 1 0 \_<br/>**DWORD** | X | \- | X | X | \- |
| \_opción WinHTTP \_ Max \_ Conex. \_ por \_ servidor<br/>**DWORD** | X | \- | X | X | \- |
| \_ \_ número máximo de \_ \_ \_ redirecciones HTTP automáticas de la opción WinHTTP<br/>**DWORD** | X | X | X | X | \- |
| \_opción WinHTTP \_ Max \_ http \_ status \_ continue<br/>**DWORD** | X | X | X | X | \- |
| tamaño máximo de límite de respuesta de la \_ opción WinHTTP \_ \_ \_ \_<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ tamaño máximo del \_ encabezado de respuesta \_ \_ de la opción WinHTTP<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ identificador primario de la opción WinHTTP \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | X | X | \- | \- |
| \_opción WinHTTP \_ \_ texto de personalización de marca de Passport \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_ \_ \_ dirección URL de copersonalización de Passport \_ de la opción WinHTTP<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_ \_ \_ dirección URL de retorno de Passport \_ de la opción WinHTTP<br/>**LPVOID** | \- | X | X | \- | \- |
| opción de WINHTTP \_ \_ Inicio de sesión de Passport \_ \_<br/>**LPVOID** | X | \- | \- | X | \- |
| contraseña de la \_ opción WinHTTP \_<br/>**LPWSTR** | \- | X | X | X | \- |
| \_proxy de opción de WinHTTP \_<br/>[**\_información del proxy WinHTTP \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | X | X | X | X | \- |
| contraseña del proxy de la \_ opción WinHTTP \_ \_<br/>**LPWSTR** | \- | X | X | X | \- |
| se \_ \_ usó el \_ SPN del proxy \_ de la opción WinHTTP<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_nombre de \_ usuario de proxy de opción WinHTTP \_<br/>**LPWSTR** | \- | X | X | X | \- |
| \_tamaño del \_ búfer de lectura \_ \_ de la opción WinHTTP<br/>**DWORD** | \- | X | X | X | \- |
| \_opción WinHTTP \_ recibir \_ respuesta de conexión de proxy \_ \_<br/>**BOOLEANO** | X | X | \- | X | \- |
| \_tiempo de \_ espera de respuesta de recepción \_ \_ de la opción WinHTTP<br/>**DWORD** | X | X | X | X | \- |
| \_tiempo de \_ espera de recepción de la opción WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_Directiva de \_ redirección de la opción WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_opción \_ de WinHTTP rechazar \_ USERPWD en la \_ \_ dirección URL<br/>**BOOLEANO** | \- | X | \- | X | \- |
| prioridad de solicitud de la \_ opción WinHTTP \_ \_<br/>**DWORD** | \- | X | X | X | \- |
| estadísticas de solicitud de la \_ opción WinHTTP \_ \_<br/>[**\_estadísticas de solicitud de WinHTTP \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | X | X | \- | Windows 10 versión 1903 |
| tiempos de solicitud de la \_ opción WinHTTP \_ \_<br/>[**\_tiempos de solicitud de WinHTTP \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | X | X | \- | Windows 10 versión 1903 |
| \_tiempo de \_ espera de resolución de la opción WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ protocolos seguros de la opción WinHTTP \_<br/>**DWORD** | X | \- | \- | X | \- |
| \_opción WinHTTP \_ certificado de seguridad ( \_ \_ struct)<br/>[**\_información del certificado WinHTTP \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | X | X | \- | \- |
| marcas de seguridad de la \_ opción WinHTTP \_ \_<br/>**DWORD** | \- | X | X | X | \- |
| información de seguridad de la \_ opción WinHTTP \_ \_<br/>[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | X | X | \- | Windows 10 versión 2004 |
| \_bits de \_ clave de seguridad \_ \_ de la opción WinHTTP<br/>**DWORD** | \- | X | X | \- | \- |
| \_tiempo de \_ espera de envío de opción de WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ Server \_ CBT<br/>[**Enlaces de SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\* | \- | X | X | \- | \- |
| el \_ contexto de la cadena de certificados del servidor de opciones WinHTTP \_ \_ \_ \_<br/>[**CERT_CHAIN_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | X | X | \- | Windows 10 versión 2004 |
| \_contexto de \_ certificado de servidor de opciones WinHTTP \_ \_<br/>[**CONTEXTO DE CERTIFICADO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | X | \- | \- |
| se \_ \_ usó el \_ SPN del servidor de opciones WinHTTP \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| opción WINHTTP de \_ \_ SPN<br/>**DWORD** | \- | X | \- | X | \- |
| \_opción WinHTTP \_ TCP \_ Fast \_ Open<br/>**BOOLEANO** | X | \- | \- | X | Windows 10 versión 2004 |
| \_opción WinHTTP \_ TLS \_ false \_ Start<br/>**BOOLEANO** | X | \- | \- | X | Windows 10 versión 2004 |
| opción de WINHTTP \_ \_ Descargar \_ evento de notificación \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | \- | \- | X | \- |
| \_análisis de \_ encabezado no \_ seguro \_ de la opción WinHTTP<br/>**DWORD** | \- | X | \- | X | \- |
| \_actualización de la opción WinHTTP \_ \_ al \_ \_ socket Web<br/>N/D | \- | X | \- | X | \- |
| \_ \_ dirección URL de la opción WinHTTP<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_opción WinHTTP \_ usar \_ \_ credenciales de servidor globales \_<br/>**BOOLEANO** | X | X | \- | X | \- |
| agente de usuario de la \_ opción WinHTTP \_ \_<br/>**LPWSTR** | X | \- | X | X | \- |
| nombre de usuario de la \_ opción WinHTTP \_<br/>**LPWSTR** | \- | X | X | X | \- |
| \_tiempo de \_ \_ espera de cierre de socket Web \_ de la opción WinHTTP \_<br/>**DWORD** | \- | \- | X | X | \- |
| \_intervalo de \_ \_ KEEPALIVE de socket Web \_ \_ de la opción WinHTTP<br/>**DWORD** | \- | \- | X | X | \- |
| \_tamaño del \_ \_ búfer de recepción de socket Web \_ \_ de la opción \_ WinHTTP<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| \_tamaño del \_ \_ búfer de envío del socket Web \_ \_ de la opción \_ WinHTTP<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| \_recuento \_ de \_ subprocesos de trabajador de la opción WinHTTP \_<br/>**DWORD** | \- | \- | \- | X | \- |
| \_tamaño del \_ búfer de escritura \_ \_ de la opción WinHTTP<br/>**DWORD** | \- | X | X | X | \- |

> [!Note]
> En Windows XP y Windows 2000, consulte [requisitos de tiempo de ejecución](winhttp-start-page.md).

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]            |
| Servidor mínimo compatible | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]         |
| Redistribuible          | WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000. |
| Encabezado                   | Winhttp. h                                                                       |

## <a name="see-also"></a>Vea también

[Versiones de WinHTTP](winhttp-versions.md)
