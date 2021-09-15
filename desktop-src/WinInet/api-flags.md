---
title: Marcas de API (Wininet.h)
description: Muchas de las funciones de WinINet aceptan una matriz de marcas como parámetro. A continuación se muestra una breve descripción de las marcas definidas.
ms.assetid: 63027a3b-dc59-41c4-a22a-5d6e841159aa
topic_type:
- apiref
api_name:
- INTERNET_COOKIE_EVALUATE_P3P
- INTERNET_COOKIE_THIRD_PARTY
- INTERNET_FLAG_ASYNC
- INTERNET_FLAG_CACHE_ASYNC
- INTERNET_FLAG_CACHE_IF_NET_FAIL
- INTERNET_FLAG_DONT_CACHE
- INTERNET_FLAG_EXISTING_CONNECT
- INTERNET_FLAG_FORMS_SUBMIT
- INTERNET_FLAG_FROM_CACHE
- INTERNET_FLAG_FWD_BACK
- INTERNET_FLAG_HYPERLINK
- INTERNET_FLAG_IGNORE_CERT_CN_INVALID
- INTERNET_FLAG_IGNORE_CERT_DATE_INVALID
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS
- INTERNET_FLAG_KEEP_CONNECTION
- INTERNET_FLAG_MAKE_PERSISTENT
- INTERNET_FLAG_MUST_CACHE_REQUEST
- INTERNET_FLAG_NEED_FILE
- INTERNET_FLAG_NO_AUTH
- INTERNET_FLAG_NO_AUTO_REDIRECT
- INTERNET_FLAG_NO_CACHE_WRITE
- INTERNET_FLAG_NO_COOKIES
- INTERNET_FLAG_NO_UI
- INTERNET_FLAG_OFFLINE
- INTERNET_FLAG_PASSIVE
- INTERNET_FLAG_PRAGMA_NOCACHE
- INTERNET_FLAG_RAW_DATA
- INTERNET_FLAG_READ_PREFETCH
- INTERNET_FLAG_RELOAD
- INTERNET_FLAG_RESTRICTED_ZONE
- INTERNET_FLAG_RESYNCHRONIZE
- INTERNET_FLAG_SECURE
- INTERNET_FLAG_TRANSFER_ASCII
- INTERNET_FLAG_TRANSFER_BINARY
- INTERNET_NO_CALLBACK
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- WININET_API_FLAG_ASYNC
- WININET_API_FLAG_SYNC
- WININET_API_FLAG_USE_CONTEXT
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111bf418e6cf599f99c9dfa34ca0f5025a1d779
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568149"
---
# <a name="api-flags"></a>Marcas de API

Muchas de las funciones de WinINet aceptan una matriz de marcas como parámetro. A continuación se muestra una breve descripción de las marcas definidas.

<dl> <dt>

<span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**INTERNET \_ COOKIE \_ EVALUATE \_ P3P**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Indica que un encabezado de la Plataforma para la protección de la privacidad (P3P) se va a asociar a una cookie.


</dt> </dl> </dd> <dt>

<span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**INTERNET \_ COOKIE \_ THIRD \_ PARTY**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Indica que se está configurando o recuperando una cookie de terceros.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**INTERNET \_ FLAG \_ ASYNC**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Realiza solo solicitudes asincrónicas en identificadores descendientes del identificador devuelto por esta función. Solo la [**función InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**INTERNET \_ FLAG \_ CACHE \_ ASYNC**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Permite una escritura de caché diferida.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**INTERNET \_ FLAG \_ CACHE \_ IF \_ NET \_ FAIL**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Devuelve el recurso de la memoria caché si se produce un error en la solicitud de red del recurso debido a un [ERROR DE INTERNET CONNECTION \_ \_ \_ RESET](wininet-errors.md) o [ERROR INTERNET CANNOT \_ \_ \_ CONNECT.](wininet-errors.md) HttpOpenRequest usa esta [**marca.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**INTERNET \_ FLAG \_ DONT \_ CACHE**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



No agrega la entidad devuelta a la memoria caché. Es idéntico al valor preferido, [INTERNET FLAG NO CACHE \_ \_ \_ \_ WRITE](/windows).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**CONEXIÓN \_ EXISTENTE DE MARCA DE \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Intenta usar un objeto [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) existente si existe uno con los mismos atributos necesarios para realizar la solicitud. Esto solo es útil con las operaciones FTP, ya que FTP es el único protocolo que normalmente realiza varias operaciones durante la misma sesión. WinINet almacena en caché un identificador de conexión único para cada identificador [**HINTERNET**](appendix-a-hinternet-handles.md) generado [**por InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Las [**funciones InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) **e InternetConnect** usan esta marca para las conexiones Http y Ftp.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**ENVÍO \_ DE FORMULARIOS \_ DE MARCA DE \_ INTERNET**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Indica que se trata de un envío de formularios.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**INTERNET \_ FLAG \_ FROM \_ CACHE**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



No realiza solicitudes de red. Todas las entidades se devuelven de la memoria caché. Si el elemento solicitado no está en la memoria caché, se devuelve un error adecuado, como ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO. Solo la [**función InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**INTERNET \_ FLAG \_ FWD \_ BACK**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indica que la función debe usar la copia del recurso que se encuentra actualmente en la caché de Internet. No se comprueba la fecha de expiración ni otra información sobre el recurso. Si el elemento solicitado no se encuentra en la caché de Internet, el sistema intenta localizar el recurso en la red. Este valor se introdujo en Microsoft Internet Explorer 5  y  está asociado a las operaciones de botón Reenviar y Atrás de Internet Explorer.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**HIPERVÍNCULO \_ DE MARCA DE \_ INTERNET**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Fuerza una recarga si no hay ninguna hora de expiración y ninguna hora LastModified devuelta desde el servidor al determinar si se debe volver a cargar el elemento de la red. [**FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**FtpGetFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpPutFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)pueden usar esta marca.

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También lo usan [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile.**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**INTERNET \_ FLAG \_ IGNORE \_ CERT \_ CN \_ INVALID**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Deshabilita la comprobación de los certificados basados en SSL/PCT que se devuelven desde el servidor con el nombre de host especificado en la solicitud. WinINet usa una comprobación sencilla de los certificados mediante la comparación de nombres de host y reglas de caracteres comodín simples. HttpOpenRequest e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) [](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pueden usar esta marca (para solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**INTERNET \_ FLAG \_ IGNORE \_ CERT \_ DATE \_ INVALID**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Deshabilita la comprobación de los certificados basados en SSL/PCT para las fechas de validez adecuadas. HttpOpenRequest e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) [](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pueden usar esta marca (para solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**INTERNET \_ FLAG \_ IGNORE \_ REDIRECT \_ TO \_ HTTP**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Deshabilita la detección de este tipo especial de redirección. Cuando se usa esta marca, WinINet permite de forma transparente redirecciones de HTTPS a direcciones URL HTTP. HttpOpenRequest e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) [](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pueden usar esta marca (para solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**INTERNET \_ FLAG \_ IGNORE \_ REDIRECT \_ TO \_ HTTPS**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Deshabilita la detección de este tipo especial de redirección. Cuando se usa esta marca, WinINet permite de forma transparente redirecciones de direcciones URL HTTP a HTTPS. HttpOpenRequest e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) [](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pueden usar esta marca (para solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**INTERNET \_ FLAG \_ KEEP \_ CONNECTION**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Usa la semántica keep-alive, si está disponible, para la conexión. [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usan esta marca (para solicitudes HTTP). Esta marca es necesaria para Microsoft Network (MSN), NTLM y otros tipos de autenticación.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**MARCA DE INTERNET \_ \_ MAKE \_ PERSISTENT**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Ya no se admite.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**LA MARCA DE INTERNET \_ DEBE ALMACENAR EN CACHÉ LA \_ \_ \_ SOLICITUD**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Idéntico al valor preferido, **INTERNET \_ FLAG NEED \_ \_ FILE**. Hace que se cree un archivo temporal si el archivo no se puede almacenar en caché. [**FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**FtpGetFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpPutFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)pueden usar esta marca.

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También lo usan [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile.**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**INTERNET \_ FLAG \_ NEED \_ FILE**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Hace que se cree un archivo temporal si el archivo no se puede almacenar en caché. [**FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**FtpGetFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpPutFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)pueden usar esta marca.

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También lo usan [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile.**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**INTERNET \_ FLAG \_ NO \_ AUTH**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



No intenta la autenticación automáticamente. HttpOpenRequest e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) [](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pueden usar esta marca (para solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**INTERNET \_ FLAG \_ NO \_ AUTO \_ REDIRECT**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



No controla automáticamente el redireccionamiento en [**HttpSendRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) también puede usar esta marca para las solicitudes HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**MARCA DE INTERNET \_ \_ SIN ESCRITURA EN \_ \_ CACHÉ**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



No agrega la entidad devuelta a la memoria caché. Esta marca la usan , [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)también usan .


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**INTERNET \_ FLAG \_ NO \_ COOKIES**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



No agrega automáticamente encabezados de cookie a las solicitudes y no agrega automáticamente las cookies devueltas a la base de datos de cookies. [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pueden usar esta marca (para solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**INTERNET \_ FLAG \_ NO \_ UI**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Deshabilita el cuadro de diálogo cookie. [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pueden usar esta marca (solo solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**INTERNET \_ FLAG \_ OFFLINE**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Idéntico a **INTERNET \_ FLAG FROM \_ \_ CACHE.** No realiza solicitudes de red. Todas las entidades se devuelven desde la memoria caché. Si el elemento solicitado no está en la memoria caché, se devuelve un error adecuado, como ERROR \_ FILE \_ NOT \_ FOUND. Solo la [**función InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**INTERNET \_ FLAG \_ PASSIVE**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Usa semántica de FTP pasiva. Solo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usan esta marca. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa esta marca para las solicitudes FTP e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa esta marca para los directorios y archivos FTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**MARCA DE INTERNET \_ \_ PRAGMA \_ NOCACHE**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Obliga a que el servidor de origen resuelva la solicitud, incluso si existe una copia almacenada en caché en el proxy. La [**función InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo en solicitudes HTTP y HTTPS) y la [**función HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usan esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**DATOS \_ SIN PROCESAR DE LA MARCA DE \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Devuelve los datos como una estructura [**\_ FIND \_ DATA de WIN32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) al recuperar información del directorio FTP. Si no se especifica esta marca o si la llamada se realiza a través de un proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) devuelve la versión HTML del directorio. Solo la [**función InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa esta marca.

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También devuelve una [**estructura GOPHER \_ FIND \_ DATA**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) al recuperar información del directorio de Gopher.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**INTERNET \_ FLAG \_ READ \_ PREFETCH**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Esta marca está deshabilitada actualmente.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**RECARGA \_ DE LA MARCA DE \_ INTERNET**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Fuerza una descarga del archivo, el objeto o el listado de directorio solicitado del servidor de origen, no de la memoria caché. Las [**funciones FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpPutFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usan esta marca.

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)también usan .


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**ZONA \_ RESTRINGIDA DE LA MARCA DE \_ \_ INTERNET**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indica que la cookie que se establece está asociada a un sitio que no es de confianza.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**RESINCRONIZACIÓN DE \_ LA MARCA DE \_ INTERNET**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Vuelve a cargar los recursos HTTP si el recurso se ha modificado desde la última vez que se descargó. Todos los recursos de FTP se vuelven a cargar. [**FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**FtpGetFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpPutFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)pueden usar esta marca.

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)también usan , y los recursos de Gopher se vuelven a cargar.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**INTERNET \_ FLAG \_ SECURE**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



Usa semántica de transacción segura. Esto se traduce en el uso Capa de sockets seguros tecnología de comunicaciones privadas (SSL/PCT) y solo es significativo en las solicitudes HTTP. HttpOpenRequest e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usan esta marca, pero esto es redundante si https:// aparece en la dirección URL. [](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) La [**función InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa esta marca para las conexiones HTTP; todos los identificadores de solicitud creados en esta conexión heredarán esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**INTERNET \_ FLAG \_ TRANSFER \_ ASCII**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Transfiere el archivo como ASCII (solo FTP). [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)y [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)pueden usar esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**INTERNET \_ FLAG \_ TRANSFER \_ BINARY**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Transfiere el archivo como binario (solo FTP). [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)y [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)pueden usar esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET \_ SIN \_ DEVOLUCIÓN DE LLAMADA**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Indica que no se debe realizar ninguna devolución de llamada para esa API. Se usa para el parámetro *dxContext* de las funciones que permiten operaciones asincrónicas.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**OPCIÓN DE INTERNET \_ \_ SUPRIMIR \_ \_ AUTENTICACIÓN DE SERVIDOR**
</dt> <dd> <dl> <dt>

104
</dt> <dt>



Establece un objeto de solicitud HTTP de modo que no inicie sesión en los servidores de origen, pero realizará el inicio de sesión automático en los servidores proxy HTTP. Esta opción difiere de la marca de solicitud INTERNET \_ FLAG \_ NO AUTH, que impide la autenticación en servidores \_ proxy y servidores de origen. Al establecer este modo, se suprimirá el uso de cualquier material de credencial (ya sea el nombre de usuario o la contraseña proporcionados previamente o el certificado SSL de cliente) al comunicarse con un servidor de origen. Sin embargo, si la solicitud debe transitar a través de un proxy de autenticación, WinINet seguirá autenticando automáticamente el proxy HTTP según la configuración de la zona de intranet del usuario. La configuración predeterminada de zona de intranet es permitir el inicio de sesión automático con las credenciales predeterminadas del usuario. Para garantizar la supresión de toda la información de identificación, el autor de la llamada debe combinar INTERNET OPTION SUPPRESS SERVER AUTH con la marca \_ de solicitud INTERNET FLAG NO \_ \_ \_ \_ \_ \_ COOKIES. Esta opción solo se puede establecer en objetos de solicitud antes de que se hayan enviado. Los intentos de establecer esta opción una vez enviada la solicitud devolveráN ERROR \_ INTERNET \_ INCORRECT HANDLE \_ \_ STATE. No se requiere ningún búfer para esta opción. InternetSetOption lo usa solo en los identificadores devueltos por HttpOpenRequest. Versión: requiere Internet Explorer 8.0 o posterior.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**ASYNC DE \_ MARCA DE API \_ \_ DE WININET**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Fuerza las operaciones asincrónicas.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**SINCRONIZACIÓN DE MARCA \_ DE API \_ DE WININET \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Fuerza las operaciones sincrónicas.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**CONTEXTO DE USO \_ DE LA MARCA DE API \_ \_ DE \_ WININET**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Obliga a la API a usar el valor de contexto, incluso si se establece en cero.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para implementaciones de servidor o servicios, use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



 

