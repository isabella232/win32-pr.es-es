---
title: Marcas de API (Wininet. h)
description: Muchas de las funciones WinINet aceptan una matriz de marcas como parámetro. La siguiente es una breve descripción de las marcas definidas.
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714605"
---
# <a name="api-flags"></a>Marcas de API

Muchas de las funciones WinINet aceptan una matriz de marcas como parámetro. La siguiente es una breve descripción de las marcas definidas.

<dl> <dt>

<span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**COOKIE de INTERNET \_ \_ evaluar \_ P3P**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Indica que se va a asociar un encabezado de plataforma para la protección de la privacidad (P3P) a una cookie.


</dt> </dl> </dd> <dt>

<span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**COOKIE de INTERNET de \_ \_ terceros \_**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Indica que se está configurando o recuperando una cookie de terceros.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**marca de INTERNET \_ \_ Async**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Realiza solo solicitudes asincrónicas en identificadores que descienden del identificador devuelto por esta función. Solo la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**caché de marcas de INTERNET \_ \_ \_ asincrónica**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Permite una escritura diferida de caché.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**caché de marcas de INTERNET \_ \_ si se \_ \_ \_ produce un error de red**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Devuelve el recurso de la memoria caché si se produce un error en la solicitud de red para el recurso debido a un [error de restablecimiento de \_ \_ conexión \_ a Internet](wininet-errors.md) o error [ \_ Internet \_ no puede \_ conectar](wininet-errors.md) . [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)usa esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**marca de INTERNET no \_ \_ \_ almacenar en caché**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



No agrega la entidad devuelta a la memoria caché. Es idéntico al valor preferido, [Internet \_ Flag \_ no \_ \_ escribir en caché](/windows).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**\_marca de \_ Internet \_ conexión existente**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Intenta usar un objeto [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) existente si existe uno con los mismos atributos necesarios para realizar la solicitud. Esto solo es útil con las operaciones FTP, ya que FTP es el único protocolo que realiza normalmente varias operaciones durante la misma sesión. WinINet almacena en caché un único identificador de conexión para cada identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) generado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Las funciones [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) y **InternetConnect** usan esta marca para las conexiones http y FTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**\_envío de \_ formularios de marcas de Internet \_**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Indica que se trata de un envío de formularios.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**\_marca \_ de Internet de la \_ caché**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



No realiza solicitudes de red. Todas las entidades se devuelven desde la memoria caché. Si el elemento solicitado no está en la memoria caché, se devuelve un error adecuado, como archivo de ERROR \_ \_ no \_ encontrado. Solo la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**indicador de INTERNET de \_ \_ FWD \_ back**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indica que la función debe usar la copia del recurso que se encuentra actualmente en la caché de Internet. La fecha de expiración y otra información sobre el recurso no se comprueban. Si el elemento solicitado no se encuentra en la caché de Internet, el sistema intentará localizar el recurso en la red. Este valor se presentó en Microsoft Internet Explorer 5 y está asociado a las operaciones de botón **adelante** y **atrás** de Internet Explorer.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**hipervínculo de marca de INTERNET \_ \_**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Fuerza una recarga si no hay ninguna hora de expiración y no se devuelve ninguna hora LastModified del servidor al determinar si se debe recargar el elemento de la red. Esta marca puede ser utilizada por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se usa en [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**marca de INTERNET \_ \_ omitir \_ CN de certificado \_ \_ no válido**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Deshabilita la comprobación de certificados basados en SSL/PCT que se devuelven desde el servidor con el nombre de host proporcionado en la solicitud. WinINet utiliza una comprobación simple de los certificados comparando los nombres de host coincidentes y las reglas de carácter comodín simples. Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**marca de INTERNET \_ \_ omitir \_ fecha de certificado \_ \_ no válida**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Deshabilita la comprobación de certificados basados en SSL/PCT para las fechas de validez adecuadas. Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**\_marca \_ de Internet omitir \_ redirección \_ a \_ http**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Deshabilita la detección de este tipo especial de redirección. Cuando se usa esta marca, WinINet permite redirigir de manera transparente a las direcciones URL de HTTPS a HTTP. Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**\_marca \_ de Internet omitir \_ redirección \_ a \_ https**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Deshabilita la detección de este tipo especial de redirección. Cuando se usa esta marca, WinINet permite redirigir de forma transparente las direcciones URL de HTTP a HTTPS. Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**marca de INTERNET \_ \_ mantener \_ conexión**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Usa la semántica Keep-Alive, si está disponible, para la conexión. Esta marca la usan [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP). Esta marca es necesaria para Microsoft Network (MSN), NTLM y otros tipos de autenticación.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**marca de INTERNET para \_ \_ hacer \_ persistente**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Ya no se admite.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**la \_ marca de Internet \_ debe \_ almacenar en caché la \_ solicitud**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Es idéntico al valor preferido, **el \_ \_ \_ archivo** de la marca de Internet. Hace que se cree un archivo temporal si el archivo no se puede almacenar en caché. Esta marca puede ser utilizada por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se usa en [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**\_archivo de \_ necesidad de marca de Internet \_**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Hace que se cree un archivo temporal si el archivo no se puede almacenar en caché. Esta marca puede ser utilizada por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se usa en [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**marca de INTERNET \_ \_ sin \_ autenticación**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



No intenta realizar la autenticación automáticamente. Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**marca de INTERNET \_ \_ sin \_ \_ redirección automática**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



No controla automáticamente la redirección en [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Esta marca también la puede usar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para las solicitudes HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**marca de INTERNET \_ \_ sin \_ escritura de caché \_**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



No agrega la entidad devuelta a la memoria caché. Esta marca se usa en, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se usa en [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**marca de INTERNET \_ \_ sin \_ cookies**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



No agrega automáticamente encabezados de cookies a las solicitudes y no agrega automáticamente las cookies devueltas a la base de datos de cookies. Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para las solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**marca de INTERNET \_ \_ sin \_ interfaz de usuario**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Deshabilita el cuadro de diálogo cookie. Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo solicitudes HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**marca de INTERNET \_ \_ sin conexión**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Idéntico a **la \_ marca \_ de Internet de la \_ caché**. No realiza solicitudes de red. Todas las entidades se devuelven desde la memoria caché. Si el elemento solicitado no está en la memoria caché, se devuelve un error adecuado, como archivo de ERROR \_ \_ no \_ encontrado. Solo la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**marca de INTERNET \_ \_ pasivo**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Usa semántica de FTP pasivo. Solo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usan esta marca. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa esta marca para las solicitudes FTP y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa esta marca para los archivos y directorios FTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**marca de INTERNET \_ \_ pragma \_ nocache**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Fuerza la resolución de la solicitud por el servidor de origen, incluso si existe una copia almacenada en caché en el proxy. La función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo en solicitudes HTTP y https) y la función [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usan esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**\_ \_ datos sin procesar de marca de Internet \_**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Devuelve los datos como una estructura de [**\_ \_ datos de búsqueda de Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) al recuperar la información de directorio FTP. Si no se especifica esta marca o si la llamada se realiza a través de un proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) devuelve la versión HTML del directorio. Solo la función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa esta marca.

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También devuelve una estructura de [**\_ \_ datos de búsqueda Gopher**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) al recuperar la información del directorio Gopher.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**\_ \_ captura previa de lectura de marca de Internet \_**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Esta marca está deshabilitada actualmente.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**RECARGA de la marca de INTERNET \_ \_**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Fuerza una descarga del archivo, el objeto o el listado de directorio solicitado del servidor de origen, no de la memoria caché. Las funciones [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usan esta marca.

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se usa en [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**\_ \_ zona restringida de marca de Internet \_**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indica que la cookie que se está configurando está asociada a un sitio que no es de confianza.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**marca de INTERNET volver a \_ \_ sincronizar**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Vuelve a cargar los recursos HTTP si el recurso se ha modificado desde la última vez que se descargó. Se recargan todos los recursos FTP. Esta marca puede ser utilizada por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También lo usan [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) y [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), y se recargan los recursos Gopher.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**marca de INTERNET \_ \_ segura**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



Usa semántica de transacción segura. Esto se traduce en el uso de la tecnología de comunicaciones privadas (SSL/PCT) de Capa de sockets seguros y solo es significativo en las solicitudes HTTP. [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)usan esta marca, pero es redundante si https://aparece en la dirección URL. La función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa esta marca para las conexiones http; todos los identificadores de solicitud creados en esta conexión heredarán esta marca.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**INTERNET \_ Flag \_ Transfer \_ ASCII**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Transfiere el archivo como ASCII (solo FTP). Esta marca puede ser utilizada por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)y [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**\_ \_ binario de transferencia de marca de Internet \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Transfiere el archivo como binario (solo FTP). Esta marca puede ser utilizada por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)y [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**\_sin devolución de llamada de Internet \_**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Indica que no se deben realizar devoluciones de llamada para esa API. Se usa para el parámetro *dxContext* de las funciones que permiten operaciones asincrónicas.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**opción de INTERNET \_ \_ suprimir \_ autenticación de servidor \_**
</dt> <dd> <dl> <dt>

104
</dt> <dt>



Establece un objeto de solicitud HTTP que no iniciará sesión en los servidores de origen, pero realizará el inicio de sesión automático en los servidores proxy HTTP. Esta opción difiere de la marca de solicitud INTERNET \_ marca \_ no \_ auth, lo que impide la autenticación en los servidores proxy y los servidores de origen. Si se establece este modo, se suprimirá el uso de cualquier material de credencial (ya sea el nombre de usuario o la contraseña previamente o el certificado SSL de cliente) al comunicarse con un servidor de origen. Sin embargo, si la solicitud debe estar en tránsito a través de un proxy de autenticación, WinINet seguirá realizando la autenticación automática en el proxy HTTP según la configuración de la zona de intranet del usuario. La configuración de la zona de intranet predeterminada es permitir el inicio de sesión automático con las credenciales predeterminadas del usuario. Para garantizar la supresión de toda la información de identificación, el autor de la llamada debe combinar la opción de INTERNET \_ \_ suprimir \_ autenticación de servidor \_ con la \_ marca de \_ solicitud marcar sin \_ cookies. Esta opción solo se puede establecer en los objetos de solicitud antes de que se hayan enviado. Si se intenta establecer esta opción una vez enviada la solicitud, se devolverá el \_ \_ Estado de identificador incorrecto de Internet \_ \_ . No se requiere ningún búfer para esta opción. InternetSetOption lo usa solo en los identificadores devueltos por HttpOpenRequest. Versión: requiere Internet Explorer 8,0 o posterior.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**\_marca de API WinInet \_ \_ asincrónica**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Fuerza las operaciones asincrónicas.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**\_sincronización de \_ marca de API de WinInet \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Fuerza las operaciones sincrónicas.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**marca de API de WININET \_ \_ \_ usar \_ contexto**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Fuerza a la API a usar el valor de contexto, incluso si se establece en cero.


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



 

