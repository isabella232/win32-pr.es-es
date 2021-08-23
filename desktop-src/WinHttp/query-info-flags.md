---
description: WinHttpQueryHeaders usa estos atributos y modificadores.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Marcas de información de consulta (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c66fd75ad1258123c3047dee4cafa4e57cb4dadd6675eb02deaa307085acbd55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051963"
---
# <a name="query-info-flags-winhttph"></a>Marcas de información de consulta (Winhttp.h)

[**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders)usa estos atributos y modificadores.

[**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) usa las marcas de atributo para indicar qué información se va a recuperar. La mayoría de las marcas de atributo se asignan directamente a un encabezado HTTP específico. También hay algunas marcas especiales, como WINHTTP \_ QUERY \_ RAW \_ HEADERS, que no están relacionadas con un encabezado específico.

<dl> <dt>

<span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**ACEPTACIÓN \_ DE CONSULTAS \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera los tipos de medios aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ CHARSET**
</dt> <dd> <dl> <dt>



Recupera los juegos de caracteres aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**CODIFICACIÓN \_ DE \_ ACEPTACIÓN DE CONSULTAS \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera los valores de codificación de contenido aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**LENGUAJE DE \_ ACEPTACIÓN \_ DE CONSULTAS WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera los lenguajes naturales aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**INTERVALOS DE \_ \_ ACEPTACIÓN \_ DE CONSULTAS WINHTTP**
</dt> <dd> <dl> <dt>



Recupera los tipos de solicitudes de intervalo que se aceptan para un recurso.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**\_ANTIGÜEDAD DE CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el campo Age response-header ,que contiene la estimación del remitente de la cantidad de tiempo desde que se generó la respuesta en el servidor de origen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP \_ QUERY \_ ALLOW**
</dt> <dd> <dl> <dt>



Recibe los [**verbos HTTP admitidos**](glossary.md) por el servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**INFORMACIÓN DE \_ AUTENTICACIÓN \_ DE CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el Authentication-Info encabezado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**AUTORIZACIÓN DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera las credenciales de autorización usadas para una solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**CONTROL DE CACHÉ DE CONSULTAS WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera las directivas de control de caché.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**CONEXIÓN DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera las opciones especificadas para una conexión determinada y no deben comunicarse mediante servidores proxy a través de conexiones adicionales.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**BASE DE \_ CONTENIDO DE \_ CONSULTA WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el identificador uniforme de recursos (URI) base para resolver las direcciones URL relativas dentro de la entidad.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**DESCRIPCIÓN DEL \_ CONTENIDO DE LA CONSULTA \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**DISPOSICIÓN DE \_ CONTENIDO DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**CODIFICACIÓN DE \_ CONTENIDO \_ DE CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera la codificación de contenido adicional que se ha aplicado a todo el recurso.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**IDENTIFICADOR DE \_ CONTENIDO DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera la identificación del contenido.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**LENGUAJE DE \_ CONTENIDO DE \_ CONSULTA WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el idioma en el que se escribe el contenido.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**LONGITUD DEL \_ CONTENIDO DE LA CONSULTA \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el tamaño del recurso, en bytes.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**UBICACIÓN DEL \_ CONTENIDO DE LA CONSULTA \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera la ubicación del recurso para la entidad incluida en el mensaje.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**CONTENIDO DE \_ CONSULTA \_ WINHTTP \_ MD5**
</dt> <dd> <dl> <dt>



Recupera una síntesis MD5 del cuerpo de la entidad con el fin de proporcionar una comprobación de integridad de mensajes de un extremo a otro para el cuerpo de la entidad. Para obtener más información, [vea RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**INTERVALO DE CONTENIDO \_ DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera la ubicación en el cuerpo completo de la entidad donde se debe insertar el cuerpo parcial de la entidad y el tamaño total del cuerpo completo de la entidad.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**CODIFICACIÓN DE \_ TRANSFERENCIA DE CONTENIDO DE CONSULTA \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera una transformación de codificación aplicable a un cuerpo de entidad. Es posible que ya se haya aplicado, que tenga que aplicarse o que sea opcionalmente aplicable.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**TIPO DE \_ CONTENIDO DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recibe el tipo de contenido del recurso, como texto o html.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**COOKIE DE CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera las cookies asociadas a la solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**COSTO DE CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



No compatible.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**CONSULTA WINHTTP \_ \_ PERSONALIZADA**
</dt> <dd> <dl> <dt>



Hace [**que WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) busque el nombre de encabezado especificado en el parámetro *pwszName* y almacene la información de encabezado *en lpBuffer*. Una aplicación puede usar **WINHTTP \_ OPTION RECEIVE RESPONSE \_ \_ \_ TIMEOUT** para limitar el tiempo máximo que esta consulta espera a que se reciban todos los encabezados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**FECHA DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recibe la fecha y hora en que se originó el mensaje.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**CONSULTA WINHTTP \_ \_ DERIVADA \_ DE**
</dt> <dd> <dl> <dt>



No compatible.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**ETAG DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera la etiqueta de entidad para la entidad asociada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP \_ QUERY \_ EXPECT**
</dt> <dd> <dl> <dt>



Recupera el encabezado Expect, que indica si la aplicación cliente debe esperar respuestas de la serie 100.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**LA CONSULTA WINHTTP \_ \_ EXPIRA**
</dt> <dd> <dl> <dt>



Recibe la fecha y hora después de la cual el recurso debe considerarse obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**CONSULTA WINHTTP \_ \_ REENVIADA**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**CONSULTA WINHTTP \_ \_ DESDE**
</dt> <dd> <dl> <dt>



Recupera la dirección de correo electrónico del usuario que controla el agente de usuario solicitante [*si*](glossary.md) se ha dado el encabezado From.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**HOST DE CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera el host de Internet y el número de puerto del recurso que se solicita.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**CONSULTA WINHTTP \_ \_ IF \_ MATCH**
</dt> <dd> <dl> <dt>



Recupera el contenido del If-Match campo request-header.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**CONSULTA WINHTTP \_ SI \_ SE MODIFICA \_ \_ DESDE**
</dt> <dd> <dl> <dt>



Recupera el contenido del encabezado If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**CONSULTA WINHTTP \_ \_ SI NINGUNA \_ \_ COINCIDE**
</dt> <dd> <dl> <dt>



Recupera el contenido del campo de encabezado de solicitud If-None-Match.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**CONSULTA WINHTTP \_ \_ IF \_ RANGE**
</dt> <dd> <dl> <dt>



Recupera el contenido del If-Range campo request-header. Este encabezado permite a la aplicación cliente comprobar si la entidad relacionada con una copia parcial de la entidad en la memoria caché de la aplicación cliente no se ha actualizado. Si la entidad no se ha actualizado, envíe los elementos que faltan en la aplicación cliente. Si la entidad se ha actualizado, envíe toda la entidad actualizada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**CONSULTA WINHTTP \_ SI NO SE HA CAMBIADO \_ \_ \_ DESDE**
</dt> <dd> <dl> <dt>



Recupera el contenido del campo de encabezado de solicitud If-Unmodified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**VÍNCULO DE CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**ÚLTIMA MODIFICACIÓN \_ DE \_ LA CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recibe la fecha y hora en que se modificó por última vez el recurso. El servidor determina la fecha y hora.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**UBICACIÓN DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el URI absoluto usado en un encabezado de respuesta location.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP \_ QUERY \_ MAX**
</dt> <dd> <dl> <dt>



Indica el valor máximo de un valor DE CONSULTA \_ \_ \* WINHTTP. No es una marca de consulta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**REENVÍOS \_ MÁXIMOS \_ DE CONSULTAS WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el número de servidores proxy o puertas de enlace que pueden reenviar la solicitud al siguiente servidor de entrada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**IDENTIFICADOR DE MENSAJE \_ DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



No compatible.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**VERSIÓN MIME \_ DE CONSULTA \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recibe la versión del protocolo Mime (Multipurpose Internet Mail Extensions) que se usó para construir el mensaje.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**URI DE \_ ORIG DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**\_PRAGMA DE \_ CONSULTA WINHTTP**
</dt> <dd> <dl> <dt>



Recibe las directivas específicas de la implementación que se pueden aplicar a cualquier destinatario a lo largo de la cadena de solicitud/respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**AUTENTICACIÓN DEL \_ \_ PROXY DE CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el esquema de autenticación y el dominio kerberos devueltos por el proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**AUTORIZACIÓN DE \_ \_ PROXY DE CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el encabezado que se usa para identificar al usuario en un proxy que requiere autenticación. Este encabezado solo se puede recuperar antes de que la solicitud se envíe al servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**CONEXIÓN DE \_ PROXY DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el Proxy-Connection encabezado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**COMPATIBILIDAD CON PROXY \_ DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el Proxy-Support encabezado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**CONSULTA WINHTTP \_ \_ PÚBLICA**
</dt> <dd> <dl> <dt>



Recibe verbos HTTP disponibles en este servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**INTERVALO DE \_ CONSULTAS \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el intervalo de bytes de una entidad.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**ENCABEZADOS SIN \_ PROCESAR \_ DE CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recibe todos los encabezados devueltos por el servidor. Cada encabezado finaliza con \\ "0". Un \\ "0" adicional finaliza la lista de encabezados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**ENCABEZADOS SIN PROCESAR DE CONSULTA \_ \_ \_ \_ WINHTTP CRLF**
</dt> <dd> <dl> <dt>



Recibe todos los encabezados devueltos por el servidor. Cada encabezado está separado por una secuencia de retorno de carro/avance de línea (CR/LF).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**REFERENCIA DE CONSULTAS WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recibe el URI del recurso donde se obtuvo el URI solicitado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**ACTUALIZACIÓN DE \_ CONSULTAS \_ WINHTTP**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**MÉTODO DE SOLICITUD \_ \_ DE CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recibe el verbo HTTP que se usa en la solicitud, normalmente GET o POST.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**REINTENTO DE CONSULTA WINHTTP \_ \_ \_ DESPUÉS**
</dt> <dd> <dl> <dt>



Recupera la cantidad de tiempo que se espera que el servicio no esté disponible.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**SERVIDOR DE CONSULTAS WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera información sobre el software utilizado por el servidor de origen para controlar la solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**COOKIE DEL \_ CONJUNTO DE \_ CONSULTAS WINHTTP \_**
</dt> <dd> <dl> <dt>



Recibe el valor del conjunto de cookies para la solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**CÓDIGO DE ESTADO \_ DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recibe el código de estado devuelto por el servidor. Para obtener una lista de valores posibles, vea [**Códigos de estado HTTP**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**TEXTO DE ESTADO \_ DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recibe texto adicional devuelto por el servidor en la línea de respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**TÍTULO DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredadas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**CODIFICACIÓN DE \_ TRANSFERENCIA \_ DE CONSULTAS \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el tipo de transformación que se ha aplicado al cuerpo del mensaje para que se pueda transferir de forma segura entre el remitente y el destinatario.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**CONSULTA WINHTTP \_ A MENOS QUE SE MODIFIQUE \_ \_ \_ DESDE**
</dt> <dd> <dl> <dt>



Recupera el encabezado Unless-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**ACTUALIZACIÓN DE \_ CONSULTAS \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera los protocolos de comunicación adicionales admitidos por el servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**URI DE CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recibe parte o todo el URI por el que se puede identificar el recurso Request-URI.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**AGENTE DE USUARIO \_ DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera información sobre el agente de usuario que realizó la solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**VARIAR LA \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera el encabezado que indica que la entidad se seleccionó de una serie de representaciones disponibles de la respuesta mediante la negociación controlada por el servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**VERSIÓN DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera la versión HTTP que está presente en la línea de estado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**CONSULTA WINHTTP \_ \_ A TRAVÉS DE**
</dt> <dd> <dl> <dt>



Recupera los protocolos intermedios y los destinatarios entre el agente de usuario y el servidor en las solicitudes, y entre el servidor de origen y el cliente en las respuestas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**ADVERTENCIA DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera información adicional sobre el estado de una respuesta que podría no reflejarse en el código de estado de respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**CONSULTA WINHTTP \_ \_ WWW \_ AUTHENTICATE**
</dt> <dd> <dl> <dt>



Recupera el esquema de autenticación y el dominio kerberos devueltos por el servidor.


</dt> </dl> </dd> </dl>

Las marcas modificadoras se usan junto con una marca de atributo para modificar la solicitud. Las marcas modificadoras modifican el formato de los datos devueltos o indican dónde debe buscar la información la función [**WinHttpQueryHeaders.**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders)

<dl> <dt>

<span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**NÚMERO DE MARCA \_ DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Devuelve los datos como un número de 32 bits para los encabezados cuyo valor es un número, como el código de estado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**ENCABEZADOS DE \_ SOLICITUD DE MARCA DE CONSULTA \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Consulta solo encabezados de solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**MARCA DE \_ CONSULTA \_ \_ WINHTTP SYSTEMTIME**
</dt> <dd> <dl> <dt>



Devuelve el valor de encabezado como [**una estructura SYSTEMTIME,**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que no requiere que la aplicación analice los datos. Se usa para los encabezados cuyo valor es una cadena de fecha y hora, como "Hora de última modificación".


</dt> </dl> </dd> </dl>

<span id="WINHTTP_QUERY_FLAG_TRAILERS"></span><span id="winhttp_query_flag_trailers"></span>**FINALIZADORES DE \_ MARCA \_ DE \_ CONSULTA WINHTTP**
</dt> <dd> <dl> <dt>


Consulta los finalizadores de respuesta. Antes de consultar los finalizadores de respuesta, debe llamar a [**WinHttpReadData**](/windows/win32/api/Winhttp/nf-winhttp-winhttpreaddata) hasta que devuelva 0 bytes leídos.


</dt> </dl> </dd> </dl>

<span id="WINHTTP_QUERY_FLAG_WIRE_ENCODING"></span><span id="winhttp_query_flag_wire_encoding"></span>**CODIFICACIÓN DE \_ CONEXIÓN DE LA MARCA DE CONSULTA \_ \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>


De forma predeterminada, [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) realiza una conversión Unicode antes de devolver el encabezado que se ha consultado. Si se establece esta marca, WinHttp devuelve el encabezado al autor de la llamada sin realizar esta conversión.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio SP3 \[\]      |
| Servidor mínimo compatible | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]   |
| Header                   | <dl> <dt>Winhttp.h</dt> </dl> |

## <a name="see-also"></a>Vea también

* [Versiones winHTTP](winhttp-versions.md)
