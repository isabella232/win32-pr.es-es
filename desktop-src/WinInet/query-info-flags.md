---
title: Marcas de información de consulta (Wininet. h)
description: Las listas siguientes contienen los atributos y modificadores usados por HttpQueryInfo y QueryInfo.
ms.assetid: b1613193-ae03-411e-bf05-de42f471cd8c
topic_type:
- apiref
api_name:
- HTTP_QUERY_ACCEPT
- HTTP_QUERY_ACCEPT_CHARSET
- HTTP_QUERY_ACCEPT_ENCODING
- HTTP_QUERY_ACCEPT_LANGUAGE
- HTTP_QUERY_ACCEPT_RANGES
- HTTP_QUERY_AGE
- HTTP_QUERY_ALLOW
- HTTP_QUERY_AUTHORIZATION
- HTTP_QUERY_CACHE_CONTROL
- HTTP_QUERY_CONNECTION
- HTTP_QUERY_CONTENT_BASE
- HTTP_QUERY_CONTENT_DESCRIPTION
- HTTP_QUERY_CONTENT_DISPOSITION
- HTTP_QUERY_CONTENT_ENCODING
- HTTP_QUERY_CONTENT_ID
- HTTP_QUERY_CONTENT_LANGUAGE
- HTTP_QUERY_CONTENT_LENGTH
- HTTP_QUERY_CONTENT_LOCATION
- HTTP_QUERY_CONTENT_MD5
- HTTP_QUERY_CONTENT_RANGE
- HTTP_QUERY_CONTENT_TRANSFER_ENCODING
- HTTP_QUERY_CONTENT_TYPE
- HTTP_QUERY_COOKIE
- HTTP_QUERY_COST
- HTTP_QUERY_CUSTOM
- HTTP_QUERY_DATE
- HTTP_QUERY_DERIVED_FROM
- HTTP_QUERY_ECHO_HEADERS
- HTTP_QUERY_ECHO_HEADERS_CRLF
- HTTP_QUERY_ECHO_REPLY
- HTTP_QUERY_ECHO_REQUEST
- HTTP_QUERY_ETAG
- HTTP_QUERY_EXPECT
- HTTP_QUERY_EXPIRES
- HTTP_QUERY_FORWARDED
- HTTP_QUERY_FROM
- HTTP_QUERY_HOST
- HTTP_QUERY_IF_MATCH
- HTTP_QUERY_IF_MODIFIED_SINCE
- HTTP_QUERY_IF_NONE_MATCH
- HTTP_QUERY_IF_RANGE
- HTTP_QUERY_IF_UNMODIFIED_SINCE
- HTTP_QUERY_LAST_MODIFIED
- HTTP_QUERY_LINK
- HTTP_QUERY_LOCATION
- HTTP_QUERY_MAX
- HTTP_QUERY_MAX_FORWARDS
- HTTP_QUERY_MESSAGE_ID
- HTTP_QUERY_MIME_VERSION
- HTTP_QUERY_ORIG_URI
- HTTP_QUERY_PRAGMA
- HTTP_QUERY_PROXY_AUTHENTICATE
- HTTP_QUERY_PROXY_AUTHORIZATION
- HTTP_QUERY_PROXY_CONNECTION
- HTTP_QUERY_PUBLIC
- HTTP_QUERY_RANGE
- HTTP_QUERY_RAW_HEADERS
- HTTP_QUERY_RAW_HEADERS_CRLF
- HTTP_QUERY_REFERER
- HTTP_QUERY_REFRESH
- HTTP_QUERY_REQUEST_METHOD
- HTTP_QUERY_RETRY_AFTER
- HTTP_QUERY_SERVER
- HTTP_QUERY_SET_COOKIE
- HTTP_QUERY_STATUS_CODE
- HTTP_QUERY_STATUS_TEXT
- HTTP_QUERY_TITLE
- HTTP_QUERY_TRANSFER_ENCODING
- HTTP_QUERY_UNLESS_MODIFIED_SINCE
- HTTP_QUERY_UPGRADE
- HTTP_QUERY_URI
- HTTP_QUERY_USER_AGENT
- HTTP_QUERY_VARY
- HTTP_QUERY_VERSION
- HTTP_QUERY_VIA
- HTTP_QUERY_WARNING
- HTTP_QUERY_WWW_AUTHENTICATE
- HTTP_QUERY_X_CONTENT_TYPE_OPTIONS
- HTTP_QUERY_P3P
- HTTP_QUERY_X_P2P_PEERDIST
- HTTP_QUERY_TRANSLATE
- HTTP_QUERY_X_UA_COMPATIBLE
- HTTP_QUERY_DEFAULT_STYLE
- HTTP_QUERY_X_FRAME_OPTIONS
- HTTP_QUERY_X_XSS_PROTECTION
- HTTP_QUERY_FLAG_COALESCE
- HTTP_QUERY_FLAG_NUMBER
- HTTP_QUERY_FLAG_REQUEST_HEADERS
- HTTP_QUERY_FLAG_SYSTEMTIME
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f3a6166c59e158d041e730d2198f6e1b066a8b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696060"
---
# <a name="query-info-flags-winineth"></a>Marcas de información de consulta (Wininet. h)

Las listas siguientes contienen los atributos y modificadores usados por [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) y [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).

[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (o [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) utiliza las marcas de atributo para indicar qué datos se van a recuperar. La mayoría de las marcas de atributo se asignan directamente a un encabezado HTTP específico. También hay algunas marcas especiales, como encabezados de [ \_ consulta HTTP \_ sin \_ formato](/windows), que no están relacionadas con un encabezado específico.

<dl> <dt>

<span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**\_aceptación de consulta HTTP \_**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Recupera los tipos de medios aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**\_consulta HTTP \_ Accept \_ CharSet**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Recupera los juegos de caracteres aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**la \_ consulta HTTP \_ acepta la \_ codificación**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Recupera los valores de codificación de contenido aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**\_idioma de \_ aceptación de consulta HTTP \_**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Recupera los idiomas naturales aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**\_intervalos de \_ aceptación de consulta HTTP \_**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



Recupera los tipos de solicitudes de intervalo que se aceptan para un recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**antigüedad de la \_ consulta HTTP \_**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



Recupera el campo de encabezado de respuesta de edad, que contiene la estimación del remitente de la cantidad de tiempo transcurrido desde que se generó la respuesta en el servidor de origen.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**\_permitir consulta \_ http**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Recibe los verbos HTTP admitidos por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**\_autorización de consulta HTTP \_**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Recupera las credenciales de autorización usadas para una solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**\_control de \_ caché de consulta HTTP \_**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



Recupera las directivas de control de caché.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**\_conexión de consulta HTTP \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Recupera todas las opciones que se especifican para una conexión determinada y que los servidores proxy no deben comunicar con otras conexiones.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**\_base de \_ contenido de consulta HTTP \_**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



Recupera el URI base (identificador uniforme de recursos) para resolver las direcciones URL relativas dentro de la entidad.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**Descripción del contenido de la \_ consulta HTTP \_ \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Obsoleto. Se mantiene únicamente por compatibilidad con aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**\_disposición de \_ contenido de consulta HTTP \_**
</dt> <dd> <dl> <dt>

47
</dt> <dt>



Obsoleto. Se mantiene únicamente por compatibilidad con aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**\_codificación de \_ contenido de consulta HTTP \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Recupera cualquier codificación de contenido adicional que se haya aplicado a todo el recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**\_identificador de \_ contenido de consulta HTTP \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Recupera la identificación del contenido.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**\_lenguaje de \_ contenido de consulta HTTP \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Recupera el idioma en el que se encuentra el contenido.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**\_longitud del \_ contenido de consulta HTTP \_**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Recupera el tamaño del recurso, en bytes.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**\_Ubicación de \_ contenido de consulta HTTP \_**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



Recupera la ubicación del recurso para la entidad que se encuentra en el mensaje.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**\_Contenido de consulta HTTP \_ \_ MD5**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



Recupera un resumen MD5 del cuerpo de la entidad con el fin de proporcionar una comprobación de integridad del mensaje (MIC) de un extremo a otro para el cuerpo de la entidad. Para obtener más información, vea RFC1864, el campo Content-MD5 header, en [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**\_intervalo de \_ contenido de consulta HTTP \_**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



Recupera la ubicación en el cuerpo de entidad completo donde se debe insertar el cuerpo de entidad parcial y el tamaño total del cuerpo de entidad completo.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**\_codificación de \_ transferencia de contenido de consulta HTTP \_ \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Recibe la codificación de contenido adicional que se ha aplicado al recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**\_tipo de \_ contenido de consulta HTTP \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Recibe el tipo de contenido del recurso (por ejemplo, texto/HTML).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**\_cookie de consulta HTTP \_**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



Recupera las cookies asociadas a la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**\_costo de consulta HTTP \_**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Ya no se admite.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**\_consulta HTTP \_ personalizada**
</dt> <dd> <dl> <dt>

65535
</dt> <dt>



Hace que [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) busque el nombre de encabezado especificado en *lpvBuffer* y almacene los datos de encabezado en *lpvBuffer*.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**\_fecha de consulta HTTP \_**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Recibe la fecha y hora en que se originó el mensaje.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**\_consulta HTTP \_ derivada \_ de**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Ya no se admite.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_encabezados de \_ eco de consulta HTTP \_**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



No implementado actualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**consulta HTTP- \_ \_ encabezados de eco \_ \_ CRLF**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



No implementado actualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**\_respuesta de \_ eco de consulta HTTP \_**
</dt> <dd> <dl> <dt>

72
</dt> <dt>



No implementado actualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**\_solicitud de \_ eco de consulta HTTP \_**
</dt> <dd> <dl> <dt>

71
</dt> <dt>



No implementado actualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**\_ETag de consulta HTTP \_**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



Recupera la etiqueta de entidad para la entidad asociada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**\_espera de consulta HTTP \_**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



Recupera el encabezado Expect, que indica si la aplicación cliente debe esperar respuestas de la serie 100.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**la \_ consulta HTTP \_ expira**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Recibe la fecha y hora después de la cual el recurso debe considerarse obsoleto.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**\_consulta HTTP \_ reenviada**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Obsoleto. Se mantiene únicamente por compatibilidad con aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**\_consulta HTTP \_ desde**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



Recupera la dirección de correo electrónico del usuario humano que controla el agente de usuario solicitante si se proporciona el encabezado From.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**\_host de consulta HTTP \_**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



Recupera el host de Internet y el número de puerto del recurso que se solicita.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**\_consulta HTTP \_ si \_ coincide**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



Recupera el contenido del If-Match campo de encabezado de la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**\_consulta HTTP \_ si se \_ modificó \_ desde**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



Recupera el contenido del encabezado If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**consulta HTTP si no hay \_ \_ \_ ninguna \_ coincidencia**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



Recupera el contenido del campo de encabezado de solicitud if-None-Match.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**\_consulta HTTP \_ si \_ intervalo**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



Recupera el contenido del If-Range campo de encabezado de la solicitud. Este encabezado permite a la aplicación cliente comprobar que la entidad relacionada con una copia parcial de la entidad en la memoria caché de la aplicación cliente no se ha actualizado. Si la entidad no se ha actualizado, envíe las partes que faltan en la aplicación cliente. Si la entidad se ha actualizado, envíe toda la entidad actualizada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**consulta HTTP si no se ha \_ \_ \_ modificado \_ desde**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



Recupera el contenido del campo de encabezado de solicitud if-Unmodified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_ \_ última \_ modificación de la consulta http**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Recibe la fecha y hora en que el servidor considera que el recurso se modificó por última vez.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**\_vínculo de consulta HTTP \_**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Obsoleto. Se mantiene únicamente por compatibilidad con aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**Ubicación de la \_ consulta HTTP \_**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



Recupera el identificador uniforme de recursos (URI) absoluto usado en un encabezado de respuesta de ubicación.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**\_consulta HTTP \_ máxima**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



No es una marca de consulta. Indica el valor máximo de un \_ valor de consulta HTTP \_ \* .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**\_ \_ número máximo de \_ reenvíos de consultas http**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



Recupera el número de servidores proxy o puertas de enlace que pueden reenviar la solicitud al siguiente servidor entrante.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**\_identificador de \_ mensaje de consulta HTTP \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Ya no se admite.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**\_ \_ versión MIME de consulta HTTP \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Recibe la versión del protocolo MIME que se usó para construir el mensaje.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**\_ \_ URI original de consulta HTTP \_**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



Obsoleto. Se mantiene únicamente por compatibilidad con aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**\_pragma de consulta HTTP \_**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Recibe las directivas específicas de la implementación que se pueden aplicar a cualquier destinatario a lo largo de la cadena de solicitud/respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**\_autenticación de \_ proxy de consulta HTTP \_**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



Recupera el esquema de autenticación y el dominio Kerberos que devuelve el proxy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**\_autorización de \_ proxy de consulta HTTP \_**
</dt> <dd> <dl> <dt>

61
</dt> <dt>



Recupera el encabezado que se usa para identificar al usuario en un proxy que requiere autenticación. Este encabezado solo se puede recuperar antes de que se envíe la solicitud al servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**\_conexión del \_ proxy de consulta HTTP \_**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



Recupera el encabezado de Proxy-Connection.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**\_consulta HTTP \_ pública**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Recibe los métodos disponibles en este servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**\_intervalo de consulta HTTP \_**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



Recupera el intervalo de bytes de una entidad.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_encabezados de consulta HTTP \_ sin formato \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Recibe todos los encabezados devueltos por el servidor. Cada encabezado termina en " \\ 0". Un " \\ 0" adicional finaliza la lista de encabezados.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**\_ \_ hipertítulos sin formato de consulta HTTP \_ \_ CRLF**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Recibe todos los encabezados devueltos por el servidor. Cada encabezado está separado por una secuencia de retorno de carro/avance de línea (CR/LF).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**\_referencia de consulta HTTP \_**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



Recibe el identificador uniforme de recursos (URI) del recurso en el que se obtuvo el URI solicitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**\_actualización de consulta HTTP \_**
</dt> <dd> <dl> <dt>

46
</dt> <dt>



Obsoleto. Se mantiene únicamente por compatibilidad con aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**\_método de \_ solicitud de consulta HTTP \_**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



Recibe el verbo HTTP que se usa en la solicitud, normalmente GET o POST.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**reintento de \_ consulta HTTP \_ \_ tras**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



Recupera la cantidad de tiempo que se espera que el servicio no esté disponible.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**\_servidor de consultas http \_**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



Recupera datos sobre el software usado por el servidor de origen para controlar la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**\_cookie de \_ conjunto de consultas http \_**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



Recibe el valor del conjunto de cookies para la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**\_código de \_ Estado de consulta HTTP \_**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Recibe el código de estado devuelto por el servidor. Para obtener más información y una lista de valores posibles, consulte [**códigos de estado http**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**\_texto de \_ Estado de consulta HTTP \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Recibe cualquier texto adicional devuelto por el servidor en la línea de respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**título de la \_ consulta HTTP \_**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



Obsoleto. Se mantiene únicamente por compatibilidad con aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**\_codificación de \_ transferencia de consulta HTTP \_**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



Recupera el tipo de transformación que se ha aplicado al cuerpo del mensaje para que se pueda transferir de forma segura entre el remitente y el destinatario.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**\_consulta HTTP \_ a menos que se \_ modifique \_ desde**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



Recupera el encabezado a menos que-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**\_actualización de consulta HTTP \_**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



Recupera los protocolos de comunicación adicionales admitidos por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**\_URI de consulta HTTP \_**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Recibe algunos o todos los identificadores uniformes de recursos (URI) mediante los cuales se puede identificar el recurso de URI de solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**\_agente de \_ usuario de consulta HTTP \_**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



Recupera datos sobre el agente de usuario que realizó la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**la \_ consulta HTTP \_ varía**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



Recupera el encabezado que indica que la entidad se ha seleccionado de varias representaciones disponibles de la respuesta mediante la negociación controlada por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**\_versión de consulta HTTP \_**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Recibe el último código de respuesta devuelto por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**\_consulta HTTP \_ a través de**
</dt> <dd> <dl> <dt>

66
</dt> <dt>



Recupera los protocolos y destinatarios intermedios entre el agente de usuario y el servidor en las solicitudes, y entre el servidor de origen y el cliente en las respuestas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**\_Advertencia de consulta HTTP \_**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



Recupera datos adicionales sobre el estado de una respuesta que podría no reflejarse en el código de estado de la respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP \_ query \_ www \_ Authenticate**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



Recupera el esquema de autenticación y el dominio Kerberos devueltos por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**\_Opciones de \_ \_ tipo de contenido X de consulta \_ http \_**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



Recupera el valor del encabezado X-Content-Type-Options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**\_Consulta HTTP \_ P3P**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



Recupera el valor del encabezado P3P.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**\_Consulta HTTP \_ X \_ P2P \_ PEERDIST**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



Recupera el valor del encabezado X-P2P-PeerDist.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**\_traducción de consulta HTTP \_**
</dt> <dd> <dl> <dt>

82
</dt> <dt>



Recupera el valor de encabezado translate.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**\_consulta HTTP \_ X \_ UA \_ compatible**
</dt> <dd> <dl> <dt>

83
</dt> <dt>



Recupera el valor del encabezado X-UA-compatible.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**\_ \_ estilo predeterminado de consulta HTTP \_**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



Recupera el valor del encabezado Default-Style.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**\_Opciones de \_ \_ fotograma X de consulta HTTP \_**
</dt> <dd> <dl> <dt>

85
</dt> <dt>



Recupera el valor del encabezado X-Frame-Options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**\_consulta HTTP \_ X \_ \_ protección XSS**
</dt> <dd> <dl> <dt>

86
</dt> <dt>



Recupera el valor del encabezado X-XSS-Protection.


</dt> </dl> </dd> </dl>

Las marcas modificadoras se usan junto con una marca de atributo para modificar la solicitud. Las marcas modificadoras modifican el formato de los datos devueltos o indican dónde [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (o [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) deben buscar los datos.

<dl> <dt>

<span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**fusión de la \_ marca de consulta HTTP \_ \_**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**\_número de \_ marca de consulta HTTP \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Devuelve los datos como un número de 32 bits para los encabezados cuyo valor es un número, como el código de estado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**\_encabezados de \_ solicitud de marca de consulta HTTP \_ \_**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Solo solicita encabezados de solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**\_marca de consulta HTTP \_ \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Devuelve el valor de encabezado como una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , que no requiere que la aplicación analice los datos. Se usa para los encabezados cuyo valor es una cadena de fecha y hora, como "Last-Modified-Time".


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



 

