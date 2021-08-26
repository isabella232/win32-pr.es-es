---
title: Marcas de información de consulta (Wininet.h)
description: Las listas siguientes contienen los atributos y modificadores utilizados por HttpQueryInfo y QueryInfo.
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
ms.openlocfilehash: 0fb2e52a30aa10161963f215e9045db006a82fee482a67947017d20372cefbdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955555"
---
# <a name="query-info-flags-winineth"></a>Marcas de información de consulta (Wininet.h)

Las listas siguientes contienen los atributos y modificadores utilizados por [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) y [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).

HttpQueryInfo (o [**QueryInfo)**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) usa [](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))las marcas de atributo para indicar qué datos se van a recuperar. La mayoría de las marcas de atributo se asignan directamente a un encabezado HTTP específico. También hay algunas marcas especiales, como [HTTP \_ QUERY RAW \_ \_ HEADERS](/windows), que no están relacionadas con un encabezado específico.

<dl> <dt>

<span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**HTTP \_ QUERY \_ ACCEPT**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Recupera los tipos de medios aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**HTTP \_ QUERY \_ ACCEPT \_ CHARSET**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Recupera los juegos de caracteres aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**HTTP \_ QUERY \_ ACCEPT \_ ENCODING**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Recupera los valores de codificación de contenido aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP \_ QUERY \_ ACCEPT \_ LANGUAGE**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Recupera los lenguajes naturales aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**INTERVALOS \_ DE \_ ACEPTACIÓN DE \_ CONSULTAS HTTP**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



Recupera los tipos de solicitudes de intervalo que se aceptan para un recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**\_ANTIGÜEDAD DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



Recupera el campo Age response-header ,que contiene la estimación del remitente de la cantidad de tiempo desde que se generó la respuesta en el servidor de origen.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP \_ QUERY \_ ALLOW**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Recibe los verbos HTTP admitidos por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**AUTORIZACIÓN \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Recupera las credenciales de autorización usadas para una solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**CONTROL DE \_ CACHÉ \_ DE CONSULTAS \_ HTTP**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



Recupera las directivas de control de caché.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**CONEXIÓN \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Recupera las opciones especificadas para una conexión determinada y no deben comunicarse mediante servidores proxy a través de conexiones adicionales.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**BASE \_ DE CONTENIDO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



Recupera el URI base (identificador uniforme de recursos) para resolver direcciones URL relativas dentro de la entidad.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**DESCRIPCIÓN \_ DEL CONTENIDO DE LA CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Obsoleto. Se mantiene solo para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**DISPOSICIÓN \_ DE CONTENIDO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

47
</dt> <dt>



Obsoleto. Se mantiene solo para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**CODIFICACIÓN \_ DE CONTENIDO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Recupera cualquier codificación de contenido adicional que se haya aplicado a todo el recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**IDENTIFICADOR \_ DE CONTENIDO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Recupera la identificación del contenido.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**LENGUAJE \_ DE CONTENIDO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Recupera el idioma en el que se encuentra el contenido.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**LONGITUD \_ DEL CONTENIDO DE LA CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Recupera el tamaño del recurso, en bytes.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**UBICACIÓN \_ DEL CONTENIDO DE LA CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



Recupera la ubicación del recurso para la entidad incluida en el mensaje.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**CONTENIDO DE CONSULTA HTTP \_ \_ \_ MD5**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



Recupera una síntesis MD5 del cuerpo de la entidad con el fin de proporcionar una comprobación de integridad de mensajes de un extremo a otro (MIC) para el cuerpo de la entidad. Para obtener más información, vea RFC1864, El campo de encabezado Content-MD5, en [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**INTERVALO \_ DE CONTENIDO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



Recupera la ubicación en el cuerpo completo de la entidad donde se debe insertar el cuerpo parcial de la entidad y el tamaño total del cuerpo completo de la entidad.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**CODIFICACIÓN \_ DE TRANSFERENCIA DE CONTENIDO DE CONSULTA \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Recibe la codificación de contenido adicional que se ha aplicado al recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**TIPO \_ DE CONTENIDO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Recibe el tipo de contenido del recurso (por ejemplo, text/html).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**COOKIE \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



Recupera las cookies asociadas a la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**COSTO \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Ya no se admite.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**CONSULTA HTTP \_ \_ PERSONALIZADA**
</dt> <dd> <dl> <dt>

65535
</dt> <dt>



Hace [**que HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) busque el nombre de encabezado especificado en *lpvBuffer* y almacene los datos de encabezado en *lpvBuffer.*


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**FECHA \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Recibe la fecha y hora en que se originó el mensaje.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**CONSULTA HTTP \_ \_ DERIVADA \_ DE**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Ya no se admite.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**ENCABEZADOS \_ DE ECO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



No implementado actualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**ENCABEZADOS DE ECO DE CONSULTA HTTP \_ \_ \_ \_ CRLF**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



No implementado actualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**RESPUESTA \_ DE ECO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

72
</dt> <dt>



No implementado actualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**SOLICITUD \_ DE ECO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

71
</dt> <dt>



No implementado actualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP \_ QUERY \_ ETAG**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



Recupera la etiqueta de entidad para la entidad asociada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**HTTP \_ QUERY \_ EXPECT**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



Recupera el encabezado Expect, que indica si la aplicación cliente debe esperar 100 respuestas de la serie.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**EXPIRA \_ LA CONSULTA HTTP \_**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Recibe la fecha y hora después de la cual el recurso debe considerarse obsoleto.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**CONSULTA HTTP \_ \_ REENVIADA**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Obsoleto. Se mantiene solo para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**CONSULTA HTTP \_ \_ DESDE**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



Recupera la dirección de correo electrónico del usuario humano que controla el agente de usuario solicitante si se da el encabezado From.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HOST \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



Recupera el host de Internet y el número de puerto del recurso que se solicita.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**CONSULTA HTTP \_ \_ IF \_ MATCH**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



Recupera el contenido del If-Match de encabezado de solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**CONSULTA HTTP \_ \_ SI SE MODIFICA \_ \_ DESDE**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



Recupera el contenido del encabezado If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**CONSULTA HTTP \_ \_ SI NINGUNA \_ \_ COINCIDE**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



Recupera el contenido del campo request-header If-None-Match.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP \_ QUERY \_ IF \_ RANGE**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



Recupera el contenido del If-Range de encabezado de solicitud. Este encabezado permite a la aplicación cliente comprobar que no se ha actualizado la entidad relacionada con una copia parcial de la entidad en la memoria caché de la aplicación cliente. Si la entidad no se ha actualizado, envíe los elementos que faltan en la aplicación cliente. Si la entidad se ha actualizado, envíe toda la entidad actualizada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**CONSULTA HTTP \_ SI NO SE HA CAMBIADO \_ \_ \_ DESDE**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



Recupera el contenido del campo de encabezado de solicitud If-Unmodified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**ÚLTIMA \_ MODIFICACIÓN DE LA CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Recibe la fecha y hora en que el servidor cree que el recurso se modificó por última vez.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**VÍNCULO \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Obsoleto. Se mantiene solo para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**UBICACIÓN \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



Recupera el identificador uniforme de recursos (URI) absoluto que se usa en un encabezado de respuesta Location.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**HTTP \_ QUERY \_ MAX**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



No es una marca de consulta. Indica el valor máximo de un valor DE \_ CONSULTA \_ \* HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**REENVÍOS \_ \_ MÁXIMOS DE \_ CONSULTAS HTTP**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



Recupera el número de servidores proxy o puertas de enlace que pueden reenviar la solicitud al siguiente servidor de entrada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**IDENTIFICADOR \_ DE MENSAJE DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Ya no se admite.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**HTTP \_ QUERY \_ MIME \_ VERSION**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Recibe la versión del protocolo MIME que se usó para construir el mensaje.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**URI \_ DE \_ ORIG DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



Obsoleto. Se mantiene solo para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**\_PRAGMA DE CONSULTA HTTP \_**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Recibe las directivas específicas de la implementación que podrían aplicarse a cualquier destinatario a lo largo de la cadena de solicitud/respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**AUTENTICACIÓN \_ DEL PROXY DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



Recupera el esquema de autenticación y el dominio kerberos devueltos por el proxy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**AUTORIZACIÓN \_ DE PROXY DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

61
</dt> <dt>



Recupera el encabezado que se usa para identificar al usuario en un proxy que requiere autenticación. Este encabezado solo se puede recuperar antes de que la solicitud se envíe al servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**CONEXIÓN \_ DE PROXY DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



Recupera el Proxy-Connection encabezado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**CONSULTA HTTP \_ \_ PÚBLICA**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Recibe los métodos disponibles en este servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**INTERVALO \_ DE CONSULTAS \_ HTTP**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



Recupera el intervalo de bytes de una entidad.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**ENCABEZADOS \_ HTTP QUERY \_ RAW \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Recibe todos los encabezados devueltos por el servidor. Cada encabezado termina con \\ "0". Un \\ "0" adicional finaliza la lista de encabezados.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**ENCABEZADOS \_ HTTP QUERY RAW \_ \_ \_ CRLF**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Recibe todos los encabezados devueltos por el servidor. Cada encabezado está separado por una secuencia de retorno de carro/avance de línea (CR/LF).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**REFERENCIA \_ DE CONSULTA HTTP \_**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



Recibe el identificador uniforme de recursos (URI) del recurso donde se obtuvo el URI solicitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**ACTUALIZACIÓN \_ DE CONSULTAS \_ HTTP**
</dt> <dd> <dl> <dt>

46
</dt> <dt>



Obsoleto. Se mantiene solo para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**MÉTODO \_ DE SOLICITUD DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



Recibe el verbo HTTP que se usa en la solicitud, normalmente GET o POST.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**REINTENTO DE CONSULTA HTTP \_ \_ \_ DESPUÉS**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



Recupera la cantidad de tiempo que se espera que el servicio no esté disponible.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**SERVIDOR \_ DE CONSULTAS \_ HTTP**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



Recupera datos sobre el software utilizado por el servidor de origen para controlar la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP \_ QUERY \_ SET \_ COOKIE**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



Recibe el valor del conjunto de cookies para la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**CÓDIGO \_ DE ESTADO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Recibe el código de estado devuelto por el servidor. Para obtener más información y una lista de valores posibles, vea [**Códigos de estado HTTP**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**TEXTO \_ DE ESTADO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Recibe cualquier texto adicional devuelto por el servidor en la línea de respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**TÍTULO \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



Obsoleto. Se mantiene solo para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**CODIFICACIÓN \_ DE TRANSFERENCIA DE CONSULTAS \_ \_ HTTP**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



Recupera el tipo de transformación que se ha aplicado al cuerpo del mensaje para que se pueda transferir de forma segura entre el remitente y el destinatario.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**CONSULTA HTTP \_ A MENOS QUE SE MODIFIQUE \_ \_ \_ DESDE**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



Recupera el encabezado Unless-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**ACTUALIZACIÓN \_ DE CONSULTAS \_ HTTP**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



Recupera los protocolos de comunicación adicionales admitidos por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**URI \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Recibe algunos o todos los identificadores uniformes de recursos (URI) por los que se puede identificar el recurso Request-URI.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**AGENTE \_ DE USUARIO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



Recupera datos sobre el agente de usuario que realizó la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**HTTP \_ QUERY \_ VARY**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



Recupera el encabezado que indica que la entidad se seleccionó de una serie de representaciones disponibles de la respuesta mediante la negociación controlada por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**VERSIÓN \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Recibe el último código de respuesta devuelto por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**CONSULTA HTTP \_ \_ A TRAVÉS DE**
</dt> <dd> <dl> <dt>

66
</dt> <dt>



Recupera los protocolos intermedios y los destinatarios entre el agente de usuario y el servidor en las solicitudes, y entre el servidor de origen y el cliente en las respuestas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**ADVERTENCIA \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



Recupera datos adicionales sobre el estado de una respuesta que podría no reflejarse en el código de estado de respuesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP \_ QUERY \_ WWW \_ AUTHENTICATE**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



Recupera el esquema de autenticación y el dominio kerberos devueltos por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**OPCIONES DE TIPO DE CONTENIDO DE CONSULTA \_ \_ HTTP X \_ \_ \_**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



Recupera el valor del encabezado X-Content-Type-Options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**HTTP \_ QUERY \_ P3P**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



Recupera el valor del encabezado P3P.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP \_ QUERY \_ X \_ P2P \_ PEERDIST**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



Recupera el valor del encabezado X-P2P-PeerDist.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**TRADUCCIÓN \_ DE CONSULTAS \_ HTTP**
</dt> <dd> <dl> <dt>

82
</dt> <dt>



Recupera el valor del encabezado translate.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP \_ QUERY \_ X \_ UA \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

83
</dt> <dt>



Recupera el valor del encabezado X-UA-Compatible.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**ESTILO \_ PREDETERMINADO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



Recupera el valor Default-Style encabezado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**OPCIONES \_ DE MARCO X DE CONSULTA \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>

85
</dt> <dt>



Recupera el valor del encabezado X-Frame-Options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP \_ QUERY \_ X \_ XSS \_ PROTECTION**
</dt> <dd> <dl> <dt>

86
</dt> <dt>



Recupera el valor del encabezado X-XSS-Protection.


</dt> </dl> </dd> </dl>

Las marcas modificadoras se usan junto con una marca de atributo para modificar la solicitud. Las marcas modificadoras modifican el formato de los datos devueltos o indican dónde [**httpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (o [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) deben buscar los datos.

<dl> <dt>

<span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**USO \_ DE LA MARCA DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Sin implementar.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**NÚMERO \_ DE MARCA DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Devuelve los datos como un número de 32 bits para los encabezados cuyo valor es un número, como el código de estado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**ENCABEZADOS \_ DE SOLICITUD DE MARCA DE CONSULTA \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Consulta solo encabezados de solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**MARCA DE CONSULTA HTTP \_ \_ \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Devuelve el valor de encabezado como [**una estructura SYSTEMTIME,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que no requiere que la aplicación analice los datos. Se usa para los encabezados cuyo valor es una cadena de fecha y hora, como "Hora de última modificación".


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para implementaciones de servidor o servicios, use [Microsoft Windows SERVICIOS HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



 

