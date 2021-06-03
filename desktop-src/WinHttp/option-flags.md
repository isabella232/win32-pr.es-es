---
Description: Las marcas de opción siguientes son compatibles con WinHttpQueryOption y WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Marcas de opción (Winhttp.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: f9405d604318205b4e951d28d5b0c304a5f7ab71
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349984"
---
# <a name="option-flags"></a>Marcas de opción

Las siguientes marcas de opción son compatibles [**con WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) y [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)

<dl> <dt>

<span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**OPCIÓN WINHTTP \_ QUE GARANTIZA DEVOLUCIONES DE LLAMADA SIN \_ \_ \_ \_ BLOQUEO**
</dt> <dd> <dl> <dt>



El valor predeterminado es FALSE. Si se establece en TRUE, WinHTTP no garantiza el progreso si la aplicación cliente bloquea las devoluciones de llamada de estado.

La aplicación cliente debe tener especial cuidado para realizar operaciones mínimas dentro de la devolución de llamada sin bloqueo, devolviendo lo antes posible y, en concreto, no debe esperar ninguna llamada WinHTTP posterior. Si no sigue estas directrices, es probable que haya un impacto negativo en el rendimiento o que una posible aplicación se desasoye. Si se usa de la manera prescrita, esta opción puede mejorar el rendimiento.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**DIRECTIVA DE \_ INICIO DE SESIÓN AUTOMÁTICO DE LA OPCIÓN \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece un valor entero largo sin signo que especifica la directiva [de inicio](authentication-in-winhttp.md) de sesión automático con uno de los valores siguientes.

| Término | Descripción |
|-|-|
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>NIVEL DE \_ SEGURIDAD ALTO DE WINHTTP AUTOLOGON \_ \_ \_ | No se usan credenciales predeterminadas. Tenga en cuenta que esta marca solo tiene efecto si especifica el servidor por el nombre real de la máquina. No tendrá efecto si especifica el servidor por "localhost" o dirección IP. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>NIVEL DE \_ SEGURIDAD BAJO DE WINHTTP AUTOLOGON \_ \_ \_ | Se realiza un inicio de sesión autenticado con las credenciales predeterminadas para todas las solicitudes. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>MEDIO DE \_ NIVEL DE SEGURIDAD DE WINHTTP AUTOLOGON \_ \_ \_ | Un inicio de sesión autenticado con las credenciales predeterminadas solo se realiza para las solicitudes en la intranet local. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**DEVOLUCIÓN DE LLAMADA \_ DE \_ LA OPCIÓN WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el puntero al conjunto de funciones de devolución de llamada [**con WinHttpSetStatusCallback.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**CONTEXTO DE CERTIFICADO \_ DE CLIENTE DE LA OPCIÓN \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece el contexto del certificado de cliente. Si una aplicación recibe [**ERROR \_ WINHTTP \_ CLIENT \_ AUTH CERT \_ \_ NEEDED**](error-messages.md), debe llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para proporcionar un certificado antes de reintentar la solicitud. Como parte del procesamiento de esta opción, WinHttp llama a [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) en el contexto de certificado proporcionado por el autor de la llamada para que el autor de la llamada pueda liberar el contexto del certificado de forma independiente.

> [!Note]
> La aplicación no debe intentar cerrar el almacén de certificados con la marca CERT CLOSE STORE FORCE FLAG en la llamada a \_ \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) en el almacén de certificados del que se recuperó el contexto del certificado. Puede producirse una infracción de acceso.

Cuando el servidor solicita un certificado de cliente, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve un [**error ERROR \_ WINHTTP CLIENT \_ \_ AUTH CERT \_ \_ NEEDED.**](error-messages.md) Si el servidor solicita el certificado pero no lo requiere, la aplicación puede especificar esta opción para indicar que no tiene un certificado. El servidor puede elegir otro esquema de autenticación o permitir el acceso anónimo al servidor. La aplicación proporciona la macro **WINHTTP \_ NO CLIENT \_ CERT \_ \_ CONTEXT** en el parámetro *lpBuffer* de [**WinHttpSetOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) como se muestra en el ejemplo de código siguiente.

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

Si el servidor requiere un certificado de cliente, puede enviar un código de estado HTTP 403 en respuesta. Para obtener más información, vea la **opción WINHTTP \_ OPTION CLIENT \_ CERT \_ \_ ISSUER \_ LIST.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**LISTA DE \_ \_ EMISORES DE \_ CERTIFICADOS DE CLIENTE DE LA \_ OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera una [**estructura \_ IssuerListInfoEx de SecPkgContext**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) cuando el error de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) es **ERROR \_ WINHTTP CLIENT \_ \_ AUTH CERT \_ \_ NEEDED**. La lista de emisores de la estructura contiene una lista de las autoridades de certificación (CA) aceptables del servidor. La aplicación cliente puede filtrar la lista de ca para recuperar el certificado de cliente para la autenticación SSL.

Como alternativa, si el servidor solicita el certificado de cliente, pero no lo requiere, la aplicación puede llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la opción **\_ WINHTTP OPTION \_ CLIENT CERT \_ \_ CONTEXT.** Para obtener más información, vea la **opción WINHTTP \_ OPTION CLIENT \_ CERT \_ \_ CONTEXT.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**PÁGINA DE CÓDIGOS \_ DE \_ LA OPCIÓN WINHTTP**
</dt> <dd> <dl> <dt>



Establece la [*página de códigos*](glossary.md) que se usa para procesar la dirección URL (es decir, cadena de consulta). El valor predeterminado es UTF8.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**OPCIÓN WINHTTP \_ \_ CONFIGURAR LA \_ \_ AUTENTICACIÓN DE PASSPORT**
</dt> <dd> <dl> <dt>



Establece un valor entero largo sin signo que especifica si está habilitada la autenticación [de Passport en la autenticación WinHTTP.](passport-authentication-in-winhttp.md) El valor puede ser uno de los siguientes:

| Término | Descripción |
|-|-|
| <span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ DISABLE \_ PASSPORT \_ AUTH | Microsoft Passport autenticación está deshabilitada. Este es el valor predeterminado. |
| <span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ DISABLE \_ PASSPORT \_ KEYRING | El llavero de Passport está deshabilitado. Este es el valor predeterminado. |
| <span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>HABILITACIÓN \_ DE \_ LA AUTENTICACIÓN DE PASSPORT EN \_ WINHTTP | La autenticación de Passport está habilitada. |
| <span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ KEYRING | El llavero de Passport está habilitado. |

</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**REINTENTOS DE \_ CONEXIÓN DE LA OPCIÓN \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el número de veces queWinHTTP intenta conectarse a un host. Servicios HTTP de Microsoft Windows (WinHTTP) solo intenta una vez por dirección ip (Protocolo de Internet). Por ejemplo, si intenta conectarse a un host multihome que tiene 10 direcciones IP y **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** se establece en 7, WinHTTP solo intenta conectarse a las siete primeras direcciones IP. Dado el mismo conjunto de 10 direcciones IP, si **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** está establecido en 20, WinHTTP intenta cada una de las 10 solo una vez. Si un intento de conexión sigue generando un error después del número especificado de intentos, o si el tiempo de espera de conexión expiró antes, se cancela la solicitud. El valor predeterminado de **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** es de cinco intentos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**TIEMPO DE ESPERA \_ DE CONEXIÓN DE LA OPCIÓN \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos. Al establecer esta opción en infinito (0xFFFFFFFF) se deshabilitará este temporizador.

Si una solicitud de conexión TCP tarda más tiempo que este valor de tiempo de espera, se cancela la solicitud. El tiempo de espera predeterminado es de 60 segundos. Cuando intenta conectarse a varias direcciones IP para un único host (un host de varios locales), el límite de tiempo de espera es para cada conexión individual.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**INFORMACIÓN DE CONEXIÓN \_ DE \_ LA OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera la dirección IP de origen y destino y el puerto de la solicitud que generó la respuesta cuando [**winHttpReceiveResponse vuelve.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) La aplicación llama [**a WinHttpQueryOption con**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) la opción **WINHTTP OPTION CONNECTION \_ \_ \_ INFO** y proporciona la estructura DE INFORMACIÓN DE CONEXIÓN [**WINHTTP \_ \_**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) en el *parámetro lpBuffer.* Para obtener más información, **vea WINHTTP \_ CONNECTION \_ INFO**.

**Windows Server 2003 con SP1 y Windows XP con SP2:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0**
</dt> <dd> <dl> <dt>



Reenvía la [**estructura TCP \_ INFO \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) para la conexión subyacente utilizada por la solicitud. La estructura devuelta puede contener estadísticas de solicitudes anteriores enviadas a través de la misma conexión.

> [!Note]
> Esta opción se ha reemplazado por **WINHTTP \_ OPTION CONNECTION \_ STATS \_ \_ V1**.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1**
</dt> <dd> <dl> <dt>



Reenvía la [**estructura TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) para la conexión subyacente utilizada por la solicitud. La estructura devuelta puede contener estadísticas de solicitudes anteriores enviadas a través de la misma conexión.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**VALOR DE CONTEXTO \_ DE \_ LA OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera un **DWORD \_ PTR** que contiene un puntero al valor de contexto asociado a este [identificador HINTERNET.](hinternet-handles-in-winhttp.md) Se usa el valor almacenado en el búfer y se asigna un nuevo valor a la marca de opción **WINHTTP \_ OPTION CONTEXT \_ \_ VALUE.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**DESCOMPRESIÓN DE \_ LA OPCIÓN WINHTTP \_**
</dt> <dd> <dl> <dt>



Establece un DWORD de marcas que determinan si WinHTTP descomprime automáticamente los cuerpos de respuesta con codificaciones de contenido comprimidas. WinHTTP también establecerá un encabezado de Accept-Encoding adecuado, reemplazando los proporcionados por el autor de la llamada. Los valores admitidos son:

| Término | Descripción |
|-|-|
| <span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>MARCA \_ DE DESCOMPRESIÓN \_ \_ WINHTTP GZIP | Descomprimir Content-Encoding: respuestas gzip. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>DEFLATE DE LA \_ \_ MARCA DE DESCOMPRESIÓN \_ WINHTTP | Descomprimir Content-Encoding: deflate las respuestas. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>MARCA \_ DE DESCOMPRESIÓN WINHTTP \_ \_ ALL | Descomprime las respuestas con cualquier codificación de contenido compatible. |

De forma predeterminada, WinHTTP entregará respuestas comprimidas al autor de la llamada sin modificar.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**CARACTERÍSTICA DESHABILITAR OPCIÓN WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Establece un valor entero largo sin signo que especifica qué características están deshabilitadas con una o varias de las marcas siguientes. Tenga en cuenta que esta característica solo debe pasarse a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) en los identificadores de solicitud después de crear el identificador de solicitud con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)y antes de que la solicitud se envíe [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

| Término | Descripción |
|-|-|
| <span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>AUTENTICACIÓN \_ DESHABILITADA DE \_ WINHTTP | La autenticación automática está deshabilitada. |
| <span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ DISABLE \_ COOKIES | La adición automática de encabezados de cookie a las solicitudes está deshabilitada. Además, las cookies devueltas no se agregan automáticamente a la base de datos de cookies. Deshabilitar las cookies puede provocar un rendimiento deficiente para la autenticación de Passport. |
| <span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE | Deshabilita la semántica de conexión keep-alive para la conexión. La semántica de conexión continua es necesaria para MSN, NTLM y otros tipos de autenticación. |
| <span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>REDIRECCIONAMIENTOS \_ DE DESHABILITACIÓN DE WINHTTP \_ | El redireccionamiento automático está deshabilitado al enviar solicitudes [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Si el redireccionamiento automático está deshabilitado, una aplicación debe registrar una función de devolución de llamada para que la autenticación de Passport se haga correctamente. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**OPCIÓN WINHTTP \_ DESHABILITAR LA RESERVA DE PROTOCOLO \_ \_ \_ \_ SEGURO**
</dt> <dd> <dl> <dt>



Impide que WinHTTP vuelva a intentar una conexión con una versión inferior del protocolo de seguridad cuando se produce un error en la negociación inicial del protocolo.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**OPCIÓN WINHTTP \_ DISABLE \_ STREAM \_ \_ QUEUE**
</dt> <dd> <dl> <dt>



Permite que las nuevas solicitudes abran una conexión HTTP/2 adicional cuando se alcanza el límite máximo de secuencias simultáneas, en lugar de esperar a la siguiente secuencia disponible en una conexión existente.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**CARACTERÍSTICA HABILITAR OPCIÓN WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Establece un valor entero largo sin signo que especifica las características habilitadas actualmente. Puede ser uno de los siguientes valores.

| Término | Descripción |
|-|-|
| <span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION | Si está habilitada, WinHTTP revierte temporalmente la suplantación de cliente mientras duren las operaciones de autenticación de certificados SSL. Este valor solo se puede establecer en el identificador de sesión. |
| <span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVOCATION | Si está habilitado, WinHTTP permite la revocación SSL. Este valor solo se puede establecer en el identificador de solicitud. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**OPCIÓN WINHTTP \_ HABILITAR \_ PROTOCOLO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Establece una máscara de bits DWORD de versiones HTTP avanzadas aceptables. Los valores posibles son:

| Término | Descripción |
|-|-|
| <span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>MARCA DE PROTOCOLO WINHTTP \_ \_ \_ HTTP2 (0x1) | Habilita HTTP/2 para la solicitud. |
| Ninguno (0x0) | Restringe la solicitud a HTTP/1.1 y versiones anteriores. |

Las versiones heredadas de HTTP (1.1 y anteriores) no se pueden deshabilitar con esta opción. El valor predeterminado es 0x0.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**OPCIÓN WINHTTP \_ \_ ENABLETRACING**
</dt> <dd> <dl> <dt>



Establece un **valor BOOL** que especifica si el seguimiento está habilitado actualmente. Para obtener más información sobre la instalación de seguimiento en WinHTTP, vea [Instalación de seguimiento winHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md). Esta opción solo se puede establecer en un **identificador NULL** **HINTERNET.**


</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**CODIFICACIÓN \_ ADICIONAL DE LA \_ OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Habilita la codificación de porcentaje de dirección URL para la ruta de acceso y la cadena de consulta.

Como alternativa, puede codificar por porcentaje antes de llamar a WinHttp.

</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**LA OPCIÓN WINHTTP \_ \_ EXPIRA LA \_ CONEXIÓN**
</dt> <dd> <dl> <dt>



Esta opción solo se puede establecer en un identificador de solicitud que sigue activo (enviando o recibiendo). Al establecer esta opción se le pedirá a WinHttp que deje de atender solicitudes en la conexión asociada con el identificador de solicitud pasado. La conexión se cerrará una vez completado el identificador de solicitud con el que se llama a esta opción. Esta opción no toma ningún parámetro.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERROR EXTENDIDO DE LA OPCIÓN WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera un valor entero largo sin signo que contiene un código de error de Microsoft Windows Sockets que se asignó a los mensajes de error ERROR WINHTTP devueltos por última vez en este \_ \_ \* contexto de subproceso. Puede pasar **NULL como** valor de identificador.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**\_CREDS DE PROXY GLOBAL DE LA OPCIÓN \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Toma un puntero a una [**estructura DE WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con el parámetro de función *hInternet* establecido en **NULL.** Esta opción requiere la clave del Registro **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**. Si no se establece esta clave del Registro, WinHTTP devolverá **el error ERROR \_ WINHTTP INVALID \_ \_ OPTION**. Esta clave del Registro no está presente de forma predeterminada. Cuando se establece, WinINet enviará las credenciales a WinHTTP. Cada vez que WinHttp obtiene un desafío de autenticación y no hay ninguna credencial establecida en el identificador actual, usará las credenciales proporcionadas por WinINet. Para compartir las credenciales del servidor además de las credenciales de proxy, los usuarios deben establecer **LA OPCIÓN WINHTTP \_ USAR CREDENCIALES DE SERVIDOR \_ \_ \_ \_ GLOBAL** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_CREDS DE SERVIDOR GLOBAL DE LA OPCIÓN \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Toma un puntero a una [**estructura DE WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con el parámetro de función *hInternet* establecido en **NULL.** Esta opción requiere la clave del Registro **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**. Si no se establece esta clave del Registro, WinHTTP devolverá **el error ERROR \_ WINHTTP INVALID \_ \_ OPTION**. Esta clave del Registro no está presente de forma predeterminada. Cuando se establece, WinINet enviará las credenciales a WinHTTP. Cada vez que WinHttp obtiene un desafío de autenticación y no hay ninguna credencial establecida en el identificador actual, usará las credenciales proporcionadas por WinINet. Para compartir las credenciales del servidor además de las credenciales de proxy, los usuarios deben establecer **LA OPCIÓN WINHTTP \_ USAR CREDENCIALES DE SERVIDOR \_ \_ \_ \_ GLOBAL** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TIPO DE IDENTIFICADOR \_ DE \_ OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera un valor entero largo sin signo que contiene el tipo del identificador [HINTERNET](hinternet-handles-in-winhttp.md) pasado. El valor devuelto puede ser cualquiera de los siguientes:

| Término | Descripción |
|-|-|
| <span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP \_ HANDLE \_ TYPE \_ CONNECT | El identificador es un identificador de conexión. |
| <span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>SOLICITUD DE TIPO \_ DE \_ IDENTIFICADOR \_ WINHTTP | El identificador es un identificador de solicitud. |
| <span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SESIÓN DE TIPO \_ DE \_ IDENTIFICADOR \_ WINHTTP | El identificador es un identificador de sesión. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**SE REQUIERE EL PROTOCOLO HTTP DE \_ \_ LA OPCIÓN \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Impide que se utilicen versiones de protocolo distintas de las habilitadas **por WINHTTP \_ OPTION ENABLE \_ HTTP \_ \_ PROTOCOL** para la solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**OPCIÓN WINHTTP \_ \_ PROTOCOLO HTTP \_ \_ USADO**
</dt> <dd> <dl> <dt>



Obtiene un DWORD que indica qué versión avanzada de HTTP se usó en una solicitud determinada. Para obtener una lista de los valores posibles, **vea WINHTTP \_ OPTION ENABLE \_ HTTP \_ \_ PROTOCOL**.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**VERSIÓN HTTP DE \_ LA OPCIÓN \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera una estructura [**HTTP \_ VERSION \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) que contiene la versión HTTP que se admite. Se trata de una opción para todo el proceso; use **NULL** para el identificador.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**OPCIÓN WINHTTP \_ OMITIR \_ \_ REVOCACIÓN \_ DE CERTIFICADOS \_ SIN CONEXIÓN**
</dt> <dd> <dl> <dt>



Permite que las conexiones seguras usen certificados de seguridad para los que no se pudo descargar la lista de revocación de certificados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**OPCIÓN WINHTTP \_ \_ IPV6 \_ FAST \_ FALLBACK**
</dt> <dd> <dl> <dt>



Habilita la reserva rápida de IPv6 (eyeballs desasosidores) para la conexión. Este comportamiento es similar al comportamiento de Happy Eyeballs descrito en [RFC 6555](https://tools.ietf.org/html/rfc6555) para mejorar los tiempos de conexión en redes donde IPv6 no es confiable.
- Si las direcciones IPv6 e IPv4 se resuelven para un host determinado, WinHttp comenzará conectándose a la primera dirección IPv6 resuelta con un tiempo de espera corto (300 ms).
- Si se producirá un error en la conexión, WinHttp intentará conectarse a la primera dirección IPv4 resuelta con el tiempo de espera estándar.
- Si se producirá un error en la segunda conexión, WinHttp volverá a intentar la primera dirección IPv6 resuelta con el tiempo de espera estándar.
- Si se producirá un error en la tercera conexión, WinHttp revertirá al comportamiento predeterminado de las direcciones restantes, intentando una conexión a cada una con el tiempo de espera estándar hasta que se establece una conexión o no quedan direcciones.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**LA OPCIÓN WINHTTP \_ ES RESPUESTA DE CONEXIÓN DE \_ \_ \_ \_ PROXY**
</dt> <dd> <dl> <dt>



Obtiene si se puede recuperar o no una respuesta de conexión de devolución de proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**OPCIÓN WINHTTP \_ \_ NÚMERO MÁXIMO DE \_ CONNS \_ POR \_ 1 \_ 0 \_ SERVIDOR**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por servidor HTTP/1.0. El valor predeterminado es **INFINITE.**

**Windows Vista con SP1 y Windows Server 2008:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**OPCIÓN WINHTTP \_ \_ NÚMERO MÁXIMO DE \_ \_ CONNS POR \_ SERVIDOR**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por servidor. El valor predeterminado es **INFINITE.**

Cuando esta opción se establece en cero, WinHTTP establece el límite en el número de conexiones en 2.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**OPCIÓN WINHTTP \_ \_ MAX HTTP AUTOMATIC \_ \_ \_ REDIRECTS**
</dt> <dd> <dl> <dt>



Establece el número máximo de redirecciones que sigue WinHTTP; el valor predeterminado es 10. Este límite impide que sitios no autorizados haga que el cliente WinHTTP se detenga después de un gran número de redirecciones.

**Windows XP con SP1 y Windows 2000 con SP3:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**OPCIÓN WINHTTP \_ \_ MAX HTTP STATUS \_ \_ \_ CONTINUE**
</dt> <dd> <dl> <dt>



Número máximo de respuestas de código de estado informativo 100-199 omitido antes de devolver el código de estado final al cliente WinHTTP. El servidor puede enviar códigos de estado informativos 100-199 antes del código de estado final y se describen en la especificación de HTTP/1.1 (para obtener más información, vea [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)). El valor predeterminado es 10.

**Windows XP con SP1 y Windows 2000 con SP3:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**TAMAÑO MÁXIMO DE PURGA DE RESPUESTA DE LA \_ \_ \_ \_ OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Enlazado a la cantidad de datos purgados de las respuestas para reutilizar una conexión, especificada en bytes. El valor predeterminado es 1 MB.

**Windows XP con SP1 y Windows 2000 con SP3:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**TAMAÑO MÁXIMO DE ENCABEZADO DE RESPUESTA DE LA \_ \_ OPCIÓN \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Un conjunto enlazado en el tamaño máximo de la parte de encabezado de la respuesta del servidor, especificado en bytes. Este límite protege al cliente de un servidor no autorizado que intenta detener el cliente mediante el envío de una respuesta con una cantidad infinita de datos de encabezado. El valor predeterminado es 64 KB.

**Windows XP con SP1 y Windows 2000 con SP3:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**IDENTIFICADOR PRIMARIO DE LA OPCIÓN WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera el identificador primario de este identificador.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**TEXTO DE MARCA DE PASSPORT DE LA \_ \_ \_ OPCIÓN WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera una cadena que contiene el texto [*de marca*](glossary.md) que proporciona el servidor de inicio de sesión de Passport. Esta opción debe recuperarse inmediatamente después de que el servidor de inicio de sesión responda con un código de estado 401. Una aplicación debe pasar un tamaño de búfer, en bytes, lo suficientemente grande como para contener la cadena devuelta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**DIRECCIÓN URL DE \_ \_ \_ COBRANDING DE LA OPCIÓN WINHTTP PASSPORT \_**
</dt> <dd> <dl> <dt>



Recupera una cadena que contiene una dirección URL para un [*gráfico de marca*](glossary.md) de marca proporcionado por el servidor de inicio de sesión de Passport. Esta opción debe recuperarse inmediatamente después de que el servidor de inicio de sesión responda con un código de estado 401. Una aplicación debe pasar un tamaño de búfer, en bytes, lo suficientemente grande como para contener la cadena devuelta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**DIRECCIÓN URL DE RETORNO DE PASSPORT DE LA \_ \_ OPCIÓN WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Establece una opción de solo lectura en un identificador de solicitud que recupera la dirección URL de devolución de Passport.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**OPCIÓN WINHTTP \_ \_ PASSPORT SIGN \_ \_ OUT**
</dt> <dd> <dl> <dt>



Establece la opción en un identificador de sesión para cerrar sesión de los inicios de sesión de Passport. Una aplicación debe pasar la dirección URL de devolución de Passport que se recuperó con **WINHTTP \_ OPTION PASSPORT RETURN \_ \_ \_ URL**. Se borran todas las cookies relacionadas con la dirección URL de devolución.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**CONTRASEÑA DE LA OPCIÓN WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor de cadena que contiene la contraseña asociada a un identificador de solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**PROXY DE OPCIÓN \_ WINHTTP \_**
</dt> <dd> <dl> <dt>



Establece o recupera una estructura [**DE INFORMACIÓN DE \_ PROXY \_ WINHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contiene los datos de proxy en un identificador de sesión o identificador de solicitud existente. Al recuperar datos de proxy, una aplicación debe liberar las cadenas **lpszProxy** y **lpszProxyBypass** contenidas en esta estructura (si no son **NULL)** mediante la [**función GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree) Una aplicación puede consultar los datos de proxy global (el proxy predeterminado) pasando un **identificador NULL.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**CONTRASEÑA DE \_ PROXY DE OPCIÓN \_ WINHTTP \_**
</dt> <dd> <dl> <dt>



Establece o recupera un valor de cadena que contiene la contraseña usada para acceder al proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**SPN DE \_ \_ PROXY DE OPCIÓN \_ WINHTTP \_ USADO**
</dt> <dd> <dl> <dt>



Obtiene el nombre principal del servidor proxy que WinHTTP proporcionó a SSPI durante la autenticación. Este valor de cadena se usa para pasar a [**SspiPromptForCredentials después**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) de un error de autenticación.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**NOMBRE DE USUARIO \_ DEL PROXY DE OPCIÓN \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera un valor de cadena que contiene el nombre de usuario utilizado para acceder al proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**TAMAÑO DEL BÚFER \_ DE LECTURA DE LA OPCIÓN \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Esta opción ha quedado en desuso; no tiene ningún efecto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**RESPUESTA DE CONEXIÓN DE \_ PROXY DE RECEPCIÓN DE LA OPCIÓN \_ \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece si se puede recuperar o no la entidad de respuesta del proxy. Esta opción está deshabilitada de forma predeterminada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**TIEMPO DE ESPERA \_ DE RESPUESTA DE RECEPCIÓN DE LA OPCIÓN \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para esperar a recibir todos los encabezados de respuesta a una solicitud. Si WinHTTP no recibe todos los encabezados dentro de este período de tiempo de espera, se cancela la solicitud. El valor de tiempo de espera predeterminado es de 90 segundos.

Este tiempo de espera solo se comprueba cuando se reciben datos del socket. Como resultado, cuando expira el tiempo de espera, la aplicación cliente no se notifica hasta que llegan más datos del servidor. Si no llegan datos del servidor, el retraso entre la expiración del tiempo de espera y la notificación de la aplicación cliente podría ser tan grande como el valor de tiempo de espera establecido mediante el parámetro *dwReceiveTimeout* de la función [**WinHttpSetTimeouts.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**TIEMPO DE ESPERA \_ DE RECEPCIÓN DE LA OPCIÓN \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para recibir una respuesta parcial a una solicitud o leer algunos datos. Si la respuesta tarda más que este valor de tiempo de espera, se cancela la solicitud. El valor predeterminado del tiempo de espera es de 30 segundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES WINHTTP \_**
</dt> <dd> <dl> <dt>



Establece el comportamiento de WinHTTP con respecto al control de un código de estado de redirección HTTP 30x. Esta opción se puede establecer en un identificador de sesión o solicitud en uno de los valores siguientes:

| Término | Descripción |
|-|-|
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES WINHTTP \_ \_ SIEMPRE | Todas las redirecciones se siguen automáticamente. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>LA DIRECTIVA DE \_ REDIRECCIÓN \_ DE OPCIONES WINHTTP NO PERMITE \_ HTTPS A \_ \_ \_ \_ HTTP | Se siguen todas las redirecciones, excepto las que se originan desde una dirección URL segura (https) a una dirección URL no segura (http). Esta es la configuración predeterminada. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES WINHTTP \_ \_ NUNCA | Las redirecciones nunca se siguen. El estado 30x se devuelve a la aplicación. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**OPCIÓN WINHTTP \_ \_ RECHAZAR \_ USERPWD \_ EN \_ URL**
</dt> <dd> <dl> <dt>



Rechaza las direcciones URL que contienen un nombre de usuario y una contraseña. Esta opción también rechaza las direcciones URL que contienen la semántica *username:password,* incluso si no se especifica ningún nombre de usuario o contraseña. Por ejemplo, " ", " ", " " y " " se marcarán como u:p@hostname :@hostname no u:@hostname :p@hostname válidos. Si se pasa una dirección URL no válida a la función, devuelve [ERROR \_ WINHTTP \_ INVALID \_ URL](error-messages.md). Esta opción está desactivada de forma predeterminada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**PRIORIDAD DE SOLICITUD \_ DE \_ LA OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Esta opción ha quedado en desuso; no tiene ningún efecto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**ESTADÍSTICAS DE SOLICITUD \_ DE \_ OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Retraives statistics for the request( Retreives statistics for the request( Retreives statistics for the request).  Para obtener una lista de las estadísticas disponibles, vea [**ESTADÍSTICAS DE SOLICITUDES WINHTTP \_ \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**TIEMPOS DE SOLICITUD \_ DE \_ LA OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Retraive la información de tiempo de la solicitud. Para obtener una lista de los intervalos disponibles, vea [**WINHTTP \_ REQUEST \_ TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**OPCIÓN WINHTTP \_ RESOLVER \_ TIEMPO DE \_ ESPERA**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para resolver un nombre de host. El valor de tiempo de espera predeterminado **es INFINITE.** Si se especifica un valor no predeterminado, hay una sobrecarga de una creación de subprocesos por resolución de nombres.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**PROTOCOLOS SEGUROS \_ DE \_ LA OPCIÓN WINHTTP \_**
</dt> <dd> <dl> <dt>



Establece un valor entero largo sin signo que especifica qué protocolos seguros son aceptables. De forma predeterminada, solo SSL3 y TLS1 están habilitados en Windows 7 y Windows 8. De forma predeterminada, solo SSL3, TLS1.0, TLS1.1 y TLS1.2 están habilitados en Windows 8.1 y Windows 10. El valor puede ser una combinación de uno o varios de los valores siguientes.

| Término | Descripción |
|-|-|
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>PROTOCOLO SEGURO DE MARCA WINHTTP \_ \_ \_ \_ ALL | Se pueden Capa de sockets seguros (SSL) 2.0, SSL 3.0 y seguridad de la capa de transporte (TLS) 1.0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP SSL2 | Se puede usar el protocolo SSL 2.0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP SSL3 | Se puede usar el protocolo SSL 3.0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP TLS1 | Se puede usar el protocolo TLS 1.0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP TLS1 \_ 1 | Se puede usar el protocolo TLS 1.1. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP TLS1 \_ 2 | Se puede usar el protocolo TLS 1.2. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**ESTRUCTURA DE CERTIFICADO \_ DE SEGURIDAD DE LA OPCIÓN \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el certificado de un servidor SSL/TLS en la [**estructura WINHTTP \_ CERTIFICATE \_ INFO.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) La aplicación debe liberar los **miembros lpszSubjectInfo** y **lpszIssuerInfo** con [**LocalFree.**](/windows/desktop/api/winbase/nf-winbase-localfree)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**MARCAS DE \_ SEGURIDAD DE \_ LA \_ OPCIÓN WINHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene las marcas de seguridad de un identificador. Puede ser una combinación de estos valores:

| Término | Descripción |
|-|-|
| <span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>LA MARCA \_ DE SEGURIDAD OMITIR CN DE CERTIFICADO NO ES \_ \_ \_ \_ VÁLIDA |Permite un nombre común no válido en un certificado; es decir, el nombre de servidor especificado por la aplicación no coincide con el nombre común del certificado. Si se establece esta marca, la aplicación no recibe una devolución de llamada **WINHTTP \_ CALLBACK \_ STATUS FLAG CERT CN \_ \_ \_ \_ INVALID.** |
| <span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>LA MARCA \_ DE SEGURIDAD OMITIR LA FECHA DE CERTIFICADO NO ES \_ \_ \_ \_ VÁLIDA |Permite una fecha de certificado no válida, es decir, un certificado expirado o aún no efectivo. Si se establece esta marca, la aplicación no recibe una devolución de llamada **CERT \_ DATE \_ \_ \_ \_ \_ INVALID** DE MARCA DE ESTADO DE DEVOLUCIÓN DE LLAMADA WINHTTP. |
| <span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>MARCA DE \_ SEGURIDAD \_ OMITIR CA \_ \_ DESCONOCIDA | Permite una entidad de certificación no válida. Si se establece esta marca, la aplicación no recibe una devolución de llamada DE CA NO VÁLIDA DE LA MARCA DE ESTADO DE DEVOLUCIÓN DE LLAMADA **WINHTTP. \_ \_ \_ \_ \_** |
| <span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>MARCA DE \_ SEGURIDAD OMITIR EL USO INCORRECTO DEL \_ \_ \_ \_ CERTIFICADO | Permite establecer la identidad de un servidor con un certificado que no es de servidor (por ejemplo, un certificado de cliente). |
| <span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>MARCA DE \_ SEGURIDAD \_ OMITIR FIRMA \_ \_ DÉBIL | Permite omitir una firma débil.<br/>Esta marca está disponible en la actualización de acumulación para cada sistema operativo a partir de Windows 7 y Windows Server 2008 R2. |
| <span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>MARCA \_ DE SEGURIDAD \_ SEGURA | Usa transferencias seguras. Esto solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>MEDIO \_ DE INTENSIDAD DE LA MARCA DE \_ \_ SEGURIDAD | Usa cifrado medio (56 bits). Esto solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SEGURIDAD \_ FUERTE DE LA \_ MARCA \_ | Usa un cifrado seguro (de 128 bits). Esto solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SEGURIDAD \_ DÉBIL DE LA INTENSIDAD DE LA \_ \_ MARCA | Usa un cifrado débil (de 40 bits). Esto solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**INFORMACIÓN DE SEGURIDAD \_ DE LA \_ OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Retraive la conexión de SChannel y la información de cifrado de una solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**VALOR DE BITS \_ DE CLAVE DE SEGURIDAD DE LA OPCIÓN \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera un valor entero largo sin signo que contiene la intensidad de cifrado de la clave de cifrado. Un número mayor indica un cifrado más seguro de la intensidad del cifrado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**OPCIÓN WINHTTP \_ ENVIAR \_ TIEMPO DE \_ ESPERA**
</dt> <dd> <dl> <dt>



Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para enviar una solicitud o escribir algunos datos. Si el envío de la solicitud tarda más tiempo que el tiempo de espera, se cancela la operación de envío. El tiempo de expiración predeterminado es de 30 segundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ OPTION \_ SERVER \_ CBT**
</dt> <dd> <dl> <dt>



Obtiene un puntero a [**la estructura Enlaces SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) que especifica un token de enlace de canal (CBT).

Un token de enlace de canal es una propiedad de un canal de transporte seguro y se usa para enlazar un canal de autenticación al canal de transporte seguro. Este token solo se puede obtener con esta opción una vez establecida una conexión SSL.

> [!Note]
> Si se pasa esta opción y un valor **NULL** para *lpBuffer* a [**WinHttpQueryOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) se devolverá ERROR INSUFFICIENT BUFFER y el tamaño de byte necesario para el búfer en el parámetro \_ \_ *lpdwBufferLength.* Este valor de tamaño de búfer devuelto se puede pasar en una llamada posterior para consultar el token de enlace de canal. Estos pasos son necesarios al controlar LA SOLICITUD DE ESTADO DE DEVOLUCIÓN DE LLAMADA DE WINHTTP si desea modificar los encabezados de solicitud \_ en función del token de enlace de \_ \_ canal. Tenga en cuenta que Windows XP y Vista no admiten la modificación de encabezados de solicitud durante esta devolución de llamada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**CONTEXTO DE CADENA \_ DE CERTIFICADOS DE SERVIDOR DE \_ \_ OPCIÓN \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el contexto de la cadena de certificación del servidor. **WINHTTP \_ OPTION \_ SERVER CERT CHAIN \_ \_ \_ CONTEXT** se puede pasar para obtener un puntero duplicado a **CERT CHAIN \_ \_ CONTEXT** para una cadena de certificados de servidor recibida durante una conexión SSL negociada. El cliente debe llamar [**a CertFreeCertificateContext en**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) el puntero DE CONTEXTO DE PCCERT \_ devuelto que se rellena en el búfer.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**CONTEXTO DE CERTIFICADO \_ DE SERVIDOR DE LA OPCIÓN \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el contexto de certificación del servidor. **WINHTTP \_ OPTION \_ SERVER CERT CONTEXT \_ \_ se** puede pasar para obtener un puntero duplicado al [**CONTEXTO DE CERT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) para un certificado de servidor recibido durante una conexión SSL negociada. El cliente debe llamar [**a CertFreeCertificateContext en**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) el puntero DE CONTEXTO DE PCCERT \_ devuelto que se rellena en el búfer.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**OPCIÓN WINHTTP \_ \_ SERVIDOR \_ SPN \_ USADO**
</dt> <dd> <dl> <dt>



Obtiene el nombre principal del servidor que WinHTTP proporcionó a SSPI durante la autenticación. Este valor de cadena se puede pasar a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) después de un error de autenticación.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**SPN DE \_ OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Incluye o quita el número de puerto del servidor cuando se ha creado el SPN (nombre principal de servicio) para la autenticación Kerberos o Negotiate Kerberos. Esta marca es uno de los siguientes valores:

| Término | Descripción |
|-|-|
| <span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ DISABLE \_ SPN \_ SERVER \_ PORT | Quita el número de puerto del servidor. |
| <span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ ENABLE \_ SPN \_ SERVER \_ PORT | Incluye el número de puerto del servidor. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**OPCIÓN WINHTTP \_ \_ TCP FAST \_ \_ OPEN**
</dt> <dd> <dl> <dt>



Habilita TCP Fast Open para la conexión.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**OPCIÓN WINHTTP \_ \_ TLS FALSE \_ \_ START**
</dt> <dd> <dl> <dt>



Habilita TLS False Start para la conexión.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**EVENTO UNLOAD \_ NOTIFY DE LA OPCIÓN \_ WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Toma un evento que se establecerá cuando se haya completado la última devolución de llamada para una sesión determinada. Esta marca debe usarse en un identificador de sesión. El evento no se puede cerrar hasta que WinHTTP lo haya establecido.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**ANÁLISIS DE ENCABEZADOS NO SEGUROS \_ DE LA \_ OPCIÓN \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Esta opción está reservada para uso interno y no se debe llamar a .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**ACTUALIZACIÓN DE LA OPCIÓN WINHTTP \_ \_ AL SOCKET \_ \_ \_ WEB**
</dt> <dd> <dl> <dt>



Indica a la pila que inicie un proceso de protocolo de enlace webSocket [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Esta opción no toma ningún parámetro.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**DIRECCIÓN URL DE LA OPCIÓN WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera un valor de cadena que contiene la dirección URL completa de un recurso descargado. Si la dirección URL original contenía datos adicionales, como cadenas de búsqueda o delimitadores, o si se redirija la llamada, la dirección URL devuelta difiere del original. La aplicación debe pasar un búfer, con un tamaño en bytes, lo suficientemente grande como para contener la dirección URL devuelta en caracteres anchos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**OPCIÓN WINHTTP \_ USAR CREDENCIALES DE SERVIDOR \_ \_ \_ \_ GLOBAL**
</dt> <dd> <dl> <dt>



Toma un **valor BOOL** y solo se puede establecer un identificador de sesión. Solo se propagará hacia abajo a los identificadores creados a partir del identificador de sesión una vez establecida la opción. Si **es TRUE,** esta opción provoca como último recurso el uso de credenciales de servidor globales que se insertaron desde WinInet. El valor predeterminado de esta opción es **FALSE.** Esta opción requiere la clave del Registro **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**. Esta clave del Registro no está presente de forma predeterminada. Cuando se establece, WinINet enviará las credenciales a WinHTTP. Cada vez que WinHttp obtiene un desafío de autenticación y no hay ninguna credencial establecida en el identificador actual, usará las credenciales proporcionadas por WinINet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**AGENTE DE USUARIO DE \_ \_ LA OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera [](glossary.md) la cadena del agente de usuario en los identificadores proporcionados por [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) y usados en funciones [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) posteriores, siempre y cuando no se invalide por un encabezado agregado por [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) o **WinHttpSendRequest**. Al recuperar un agente de usuario, la aplicación debe pasar un búfer, con un tamaño en bytes, lo suficientemente grande como para contener la dirección URL devuelta en caracteres anchos. Al establecer el agente de usuario, el tamaño del búfer es la longitud de la cadena, en caracteres, más el **terminador NULL.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**NOMBRE DE USUARIO DE \_ LA OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera una cadena que contiene el nombre de usuario.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**OPCIÓN WINHTTP \_ TIEMPO DE ESPERA DE CIERRE DE SOCKET \_ \_ \_ \_ WEB**
</dt> <dd> <dl> <dt>



Establece el tiempo, en milisegundos, que [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) debe esperar para completar el protocolo de enlace de cierre. El valor predeterminado es 10 segundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**OPCIÓN WINHTTP \_ \_ WEB SOCKET \_ \_ KEEPALIVE \_ INTERVAL**
</dt> <dd> <dl> <dt>



Establece el intervalo, en milisegundos, para enviar un paquete keep-alive a través de la conexión. El intervalo predeterminado es 30 000 (30 segundos). El intervalo mínimo es 15 000 (15 segundos). El [**uso de WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para establecer un valor inferior a 15000 devolverá **con ERROR INVALID \_ \_ PARAMETER**.

> [!Note]
> El valor predeterminado de **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** se lee en **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval**. Si no se establece un valor, se usará el valor predeterminado 30000. No es posible tener un intervalo de keepalive inferior a 15 000 milisegundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**TAMAÑO DEL BÚFER \_ DE RECEPCIÓN DE LA OPCIÓN WINHTTP \_ \_ WEB SOCKET \_ \_ \_**
</dt> <dd> <dl> <dt>



Establece o recupera un DWORD que especifica el tamaño del búfer de recepción que se va a usar en las conexiones de WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**TAMAÑO DEL BÚFER DE ENVÍO DE SOCKET WEB DE LA \_ \_ \_ \_ \_ OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece o recupera un DWORD que especifica el tamaño del búfer de envío que se va a usar en las conexiones de WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**RECUENTO DE \_ SUBPROCESOS \_ DE TRABAJO DE LA \_ OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Establece un valor entero largo sin signo que especifica el número de subprocesos de trabajo que el grupo de subprocesos debe usar para las finalizaciones asincrónicas. El valor predeterminado de esta opción es cero, que especifica que el número de subprocesos de trabajo es igual al número de CPU del sistema. Esta opción solo se puede establecer en un **identificador NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) antes de que se haya producido una operación asincrónica. Esta opción solo se puede establecer una vez.

**Windows Server 2008 R2 y Windows 7:** Esta marca está obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**TAMAÑO DEL BÚFER \_ DE ESCRITURA DE LA \_ \_ OPCIÓN \_ WINHTTP**
</dt> <dd> <dl> <dt>



Esta opción está en desuso; no tiene ningún efecto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

En la tabla siguiente se enumeran las marcas de opción especificando sobre qué identificadores pueden actuar, si se pueden consultar y establecer, y el tipo de datos utilizado. Una "X" indica que la marca de opción es válida para su uso con la función o el identificador, mientras que "-" especifica que la marca de opción no es válida.

Si intenta establecer o consultar una marca de opción en una versión de Windows en la que no se admite, se producirá **el error \_ WINHTTP INVALID \_ \_ OPTION**.

| Marca de opción y tipo de datos | Identificador de sesión | Identificador de solicitud | Opción de consulta | Opción SET | Versión mínima de Windows |
|-|-|-|-|-|-|
| OPCIÓN WINHTTP \_ QUE GARANTIZA DEVOLUCIONES DE LLAMADA SIN \_ \_ \_ \_ BLOQUEO<br/>**Bool** | X | \- | \- | X | \- |
| DIRECTIVA DE \_ INICIO DE SESIÓN AUTOMÁTICO DE LA OPCIÓN \_ \_ WINHTTP<br/>**DWORD** | \- | X | \- | X | \- |
| DEVOLUCIÓN DE LLAMADA \_ DE \_ LA OPCIÓN WINHTTP<br/>**LPVOID** | X | X | X | X | \- |
| CONTEXTO DE CERTIFICADO \_ DE CLIENTE DE LA OPCIÓN \_ \_ \_ WINHTTP<br/>[**CONTEXTO \_ DE CERTIFICADO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | \- | X | Windows Vista |
| LISTA DE \_ \_ EMISORES DE \_ CERTIFICADOS DE CLIENTE DE LA \_ OPCIÓN \_ WINHTTP<br/>[**SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | X | X | \- | Windows Vista |
| PÁGINA DE CÓDIGOS \_ DE \_ LA OPCIÓN WINHTTP<br/>**DWORD** | X | \- | \- | X | \- |
| OPCIÓN WINHTTP \_ CONFIGURAR \_ LA \_ \_ AUTENTICACIÓN DE PASSPORT<br/>**DWORD** | X | \- | \- | X | \- |
| REINTENTOS DE \_ CONEXIÓN DE LA OPCIÓN \_ \_ WINHTTP<br/>**DWORD** | X | X | X | X | \- |
| OPCIÓN WINHTTP \_ CONNECT \_ \_ TIMEOUT<br/>**DWORD** | X | X | X | X | \- |
| INFORMACIÓN DE CONEXIÓN \_ DE LA \_ OPCIÓN \_ WINHTTP<br/>[**INFORMACIÓN DE CONEXIÓN \_ \_ WINHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | X | X | \- | \- |
| WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0<br/>[**TCP \_ INFO \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | X | X | \- | Windows 10 versión 1903 |
| ESTADÍSTICAS DE CONEXIÓN DE LA OPCIÓN WINHTTP \_ \_ \_ \_ V1<br/>[**TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | X | X | \- | Windows 10 versión 2004 |
| VALOR DE CONTEXTO \_ DE LA \_ OPCIÓN \_ WINHTTP<br/>**DWORD \_ PTR** | X | X | X | X | \- |
| \_DESCOMPRESIÓN DE LA OPCIÓN WINHTTP \_<br/>**DWORD** | X | X | \- | X | Windows 8.1 |
| CARACTERÍSTICA DESHABILITAR OPCIÓN WINHTTP \_ \_ \_<br/>**DWORD** | \- | X | \- | X | \- |
| OPCIÓN WINHTTP \_ DESHABILITAR RESERVA DE PROTOCOLO \_ \_ \_ \_ SEGURO<br/>**Bool** | X | \- | \- | X | Windows 10 versión 1903 |
| OPCIÓN WINHTTP \_ DESHABILITAR \_ COLA DE \_ \_ TRANSMISIONES<br/>**Bool** | X | X | \- | X | Windows 10 versión 1809 |
| CARACTERÍSTICA HABILITAR OPCIÓN WINHTTP \_ \_ \_<br/>**DWORD** | \* | \* | \- | X | \- |
| OPCIÓN WINHTTP \_ HABILITAR \_ PROTOCOLO \_ \_ HTTP<br/>**DWORD** | X | X | \- | X | Windows 10 Versión 1607 |
| HABILITACIÓN \_ DE LA OPCIÓN \_ WINHTTPTRACING<br/>**DWORD** | \- | \- | X | X | \- |
| CODIFICACIÓN \_ ADICIONAL DE LA \_ OPCIÓN \_ WINHTTP<br/>**Bool** | X | X | \- | X | Windows 10 versión 1803 |
| OPCIÓN WINHTTP \_ \_ EXPIRE \_ CONNECTION<br/>N/D | \- | X | \- | X | Windows 10 versión 1903 |
| ERROR EXTENDIDO DE LA OPCIÓN WINHTTP \_ \_ \_<br/>**DWORD** | X | X | X | \- | \- |
| CREDS DE PROXY GLOBAL DE \_ \_ LA OPCIÓN \_ \_ WINHTTP<br/>[**WINHTTP \_ CREDS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | X | X | \- | X | \- |
| WINHTTP \_ OPTION \_ GLOBAL \_ SERVER \_ CREDS<br/>[**WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | X | X | \- | X | \- |
| TIPO DE IDENTIFICADOR \_ DE OPCIÓN \_ WINHTTP \_<br/>**DWORD** | X | X | X | \- | \- |
| SE REQUIERE \_ EL PROTOCOLO HTTP DE LA OPCIÓN \_ \_ \_ WINHTTP<br/>**Bool** | X | X | \- | X | Windows 10 versión 1903 |
| SE USA EL PROTOCOLO HTTP DE \_ \_ LA OPCIÓN WINHTTP \_ \_<br/>**DWORD** | \- | X | X | \- | Windows 10 Versión 1607 |
| VERSIÓN HTTP DE \_ LA OPCIÓN \_ \_ WINHTTP<br/>[**INFORMACIÓN \_ DE VERSIÓN \_ HTTP**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | X | X | X | X | \- |
| OPCIÓN WINHTTP \_ OMITIR \_ \_ REVOCACIÓN \_ DE CERTIFICADOS \_ SIN CONEXIÓN<br/>**Bool** | \- | X | \- | X | Windows 10 versión 2004 |
| OPCIÓN WINHTTP \_ \_ IPV6 \_ FAST \_ FALLBACK<br/>**Bool** | X | \- | \- | X | Windows 10 versión 1903 |
| LA OPCIÓN WINHTTP \_ ES RESPUESTA DE CONEXIÓN DE \_ \_ \_ \_ PROXY<br/>**Bool** | X | X | X | \- | \- |
| OPCIÓN WINHTTP \_ \_ NÚMERO MÁXIMO DE \_ CONN POR \_ \_ 1 \_ SERVIDOR 0 \_<br/>**DWORD** | X | \- | X | X | \- |
| OPCIÓN WINHTTP \_ \_ NÚMERO MÁXIMO DE \_ CONN POR \_ \_ SERVIDOR<br/>**DWORD** | X | \- | X | X | \- |
| OPCIÓN WINHTTP \_ \_ MAX HTTP AUTOMATIC \_ \_ \_ REDIRECTS<br/>**DWORD** | X | X | X | X | \- |
| OPCIÓN WINHTTP \_ \_ MAX HTTP STATUS \_ \_ \_ CONTINUE<br/>**DWORD** | X | X | X | X | \- |
| TAMAÑO MÁXIMO DE PURGA DE RESPUESTA DE LA \_ \_ \_ \_ OPCIÓN \_ WINHTTP<br/>**DWORD** | X | X | X | X | \- |
| TAMAÑO MÁXIMO \_ DE ENCABEZADO DE RESPUESTA DE LA \_ \_ \_ OPCIÓN \_ WINHTTP<br/>**DWORD** | X | X | X | X | \- |
| IDENTIFICADOR PRIMARIO DE \_ LA \_ OPCIÓN \_ WINHTTP<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | X | X | \- | \- |
| TEXTO DE MARCA DE PASSPORT DE LA \_ \_ \_ OPCIÓN WINHTTP \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| DIRECCIÓN URL DE \_ \_ COBRANDING DE LA OPCIÓN WINHTTP PASSPORT \_ \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| DIRECCIÓN URL DE \_ RETORNO DE PASSPORT DE LA \_ OPCIÓN WINHTTP \_ \_<br/>**LPVOID** | \- | X | X | \- | \- |
| OPCIÓN WINHTTP \_ \_ PASSPORT SIGN \_ \_ OUT<br/>**LPVOID** | X | \- | \- | X | \- |
| CONTRASEÑA DE LA OPCIÓN WINHTTP \_ \_<br/>**LPWSTR** | \- | X | X | X | \- |
| PROXY DE \_ OPCIÓN WINHTTP \_<br/>[**INFORMACIÓN DEL PROXY WINHTTP \_ \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | X | X | X | X | \- |
| CONTRASEÑA DE \_ PROXY DE \_ OPCIÓN \_ WINHTTP<br/>**LPWSTR** | \- | X | X | X | \- |
| SPN DE \_ \_ PROXY DE OPCIÓN \_ WINHTTP \_ USADO<br/>**LPWSTR** | \- | X | X | \- | \- |
| NOMBRE DE USUARIO \_ DEL PROXY DE OPCIÓN \_ \_ WINHTTP<br/>**LPWSTR** | \- | X | X | X | \- |
| TAMAÑO DEL BÚFER \_ DE LECTURA DE LA OPCIÓN \_ \_ \_ WINHTTP<br/>**DWORD** | \- | X | X | X | \- |
| RESPUESTA DE CONEXIÓN DE \_ PROXY DE RECEPCIÓN DE LA OPCIÓN \_ \_ \_ \_ WINHTTP<br/>**Bool** | X | X | \- | X | \- |
| TIEMPO DE ESPERA \_ DE RESPUESTA DE RECEPCIÓN DE LA OPCIÓN \_ \_ \_ WINHTTP<br/>**DWORD** | X | X | X | X | \- |
| TIEMPO DE ESPERA \_ DE RECEPCIÓN DE LA OPCIÓN \_ \_ WINHTTP<br/>**DWORD** | X | X | X | X | \- |
| DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES WINHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| OPCIÓN WINHTTP \_ \_ RECHAZAR \_ USERPWD \_ EN \_ URL<br/>**Bool** | \- | X | \- | X | \- |
| PRIORIDAD DE SOLICITUD \_ DE \_ LA OPCIÓN \_ WINHTTP<br/>**DWORD** | \- | X | X | X | \- |
| ESTADÍSTICAS DE SOLICITUD \_ DE \_ OPCIÓN \_ WINHTTP<br/>[**ESTADÍSTICAS DE \_ SOLICITUDES \_ WINHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | X | X | \- | Windows 10 versión 1903 |
| TIEMPOS DE SOLICITUD \_ DE \_ LA OPCIÓN \_ WINHTTP<br/>[**TIEMPOS DE \_ SOLICITUD \_ WINHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | X | X | \- | Windows 10 versión 1903 |
| OPCIÓN WINHTTP \_ RESOLVER \_ TIEMPO DE \_ ESPERA<br/>**DWORD** | X | X | X | X | \- |
| PROTOCOLOS SEGUROS \_ DE \_ LA OPCIÓN WINHTTP \_<br/>**DWORD** | X | \- | \- | X | \- |
| ESTRUCTURA DE CERTIFICADO \_ DE SEGURIDAD DE LA OPCIÓN \_ \_ \_ WINHTTP<br/>[**INFORMACIÓN DEL \_ CERTIFICADO \_ WINHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | X | X | \- | \- |
| MARCAS DE \_ SEGURIDAD DE \_ LA \_ OPCIÓN WINHTTP<br/>**DWORD** | \- | X | X | X | \- |
| INFORMACIÓN DE SEGURIDAD \_ DE LA \_ OPCIÓN \_ WINHTTP<br/>[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | X | X | \- | Windows 10 versión 2004 |
| VALOR DE BITS \_ DE CLAVE DE SEGURIDAD DE LA OPCIÓN \_ \_ \_ WINHTTP<br/>**DWORD** | \- | X | X | \- | \- |
| OPCIÓN WINHTTP \_ ENVIAR TIEMPO DE \_ \_ ESPERA<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ SERVER \_ CBT<br/>[**Enlaces \_ SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\* | \- | X | X | \- | \- |
| CONTEXTO DE CADENA \_ DE CERTIFICADOS DE SERVIDOR DE \_ \_ OPCIÓN \_ \_ WINHTTP<br/>[**CERT_CHAIN_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | X | X | \- | Windows 10 versión 2004 |
| CONTEXTO DE CERTIFICADO \_ DE SERVIDOR DE LA OPCIÓN \_ \_ \_ WINHTTP<br/>[**CONTEXTO DE CERT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | X | \- | \- |
| OPCIÓN WINHTTP \_ \_ SERVIDOR \_ SPN \_ USADO<br/>**LPWSTR** | \- | X | X | \- | \- |
| SPN DE \_ OPCIÓN \_ WINHTTP<br/>**DWORD** | \- | X | \- | X | \- |
| OPCIÓN WINHTTP \_ \_ TCP FAST \_ \_ OPEN<br/>**Bool** | X | \- | \- | X | Windows 10 versión 2004 |
| OPCIÓN WINHTTP \_ \_ TLS FALSE \_ \_ START<br/>**Bool** | X | \- | \- | X | Windows 10 versión 2004 |
| EVENTO DE \_ NOTIFICACIÓN DE DESCARGA DE LA OPCIÓN \_ WINHTTP \_ \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | \- | \- | X | \- |
| ANÁLISIS DE ENCABEZADOS NO SEGUROS DE LA \_ \_ \_ \_ OPCIÓN WINHTTP<br/>**DWORD** | \- | X | \- | X | \- |
| ACTUALIZACIÓN DE LA OPCIÓN WINHTTP \_ \_ AL SOCKET \_ \_ \_ WEB<br/>N/D | \- | X | \- | X | \- |
| DIRECCIÓN URL DE LA OPCIÓN WINHTTP \_ \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| OPCIÓN WINHTTP \_ USAR CREDENCIALES DE SERVIDOR \_ \_ \_ \_ GLOBAL<br/>**Bool** | X | X | \- | X | \- |
| AGENTE DE USUARIO \_ DE LA \_ OPCIÓN \_ WINHTTP<br/>**LPWSTR** | X | \- | X | X | \- |
| NOMBRE DE USUARIO DE LA OPCIÓN WINHTTP \_ \_<br/>**LPWSTR** | \- | X | X | X | \- |
| TIEMPO DE ESPERA \_ DE CIERRE DE SOCKET WEB DE LA \_ \_ \_ OPCIÓN \_ WINHTTP<br/>**DWORD** | \- | \- | X | X | \- |
| OPCIÓN WINHTTP \_ \_ WEB SOCKET \_ \_ \_ KEEPALIVE INTERVAL<br/>**DWORD** | \- | \- | X | X | \- |
| TAMAÑO DEL BÚFER DE RECEPCIÓN DE LA OPCIÓN WINHTTP \_ \_ WEB \_ SOCKET \_ \_ \_<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| TAMAÑO DEL BÚFER DE ENVÍO DE SOCKET WEB DE LA \_ \_ \_ \_ \_ OPCIÓN \_ WINHTTP<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| RECUENTO DE \_ SUBPROCESOS \_ DE TRABAJO DE LA \_ OPCIÓN \_ WINHTTP<br/>**DWORD** | \- | \- | \- | X | \- |
| TAMAÑO DEL BÚFER \_ DE ESCRITURA DE LA \_ \_ OPCIÓN \_ WINHTTP<br/>**DWORD** | \- | X | X | X | \- |

> [!Note]
> Para Windows XP y Windows 2000, consulte [Requisitos en tiempo de ejecución.](winhttp-start-page.md)

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]            |
| Servidor mínimo compatible | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]         |
| Redistribuible          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000. |
| Encabezado                   | Winhttp.h                                                                       |

## <a name="see-also"></a>Consulte también

[Versiones de WinHTTP](winhttp-versions.md)
