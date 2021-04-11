---
description: WinHttpQueryHeaders usa estos atributos y modificadores.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Marcas de información de consulta (winhttp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9ffc8f4ba4a947fe6fb277617c99460c43ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082869"
---
# <a name="query-info-flags-winhttph"></a>Marcas de información de consulta (winhttp. h)

[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)usa estos atributos y modificadores.

[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) usa las marcas de atributo para indicar qué información se va a recuperar. La mayoría de las marcas de atributo se asignan directamente a un encabezado HTTP específico. También hay algunas marcas especiales, como los encabezados de \_ consulta WinHTTP, \_ \_ que no están relacionadas con un encabezado específico.

<dl> <dt>

<span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**\_aceptación de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera los tipos de medios aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**la \_ consulta WinHTTP \_ acepta \_ CharSet**
</dt> <dd> <dl> <dt>



Recupera los juegos de caracteres aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**la \_ consulta WinHTTP \_ acepta la \_ codificación**
</dt> <dd> <dl> <dt>



Recupera los valores de codificación de contenido aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**\_idioma de \_ aceptación de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera los idiomas naturales aceptables para la respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**\_intervalos de \_ aceptación de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera los tipos de solicitudes de intervalo que se aceptan para un recurso.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**antigüedad de la \_ consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el campo de encabezado de respuesta de edad, que contiene la estimación del remitente de la cantidad de tiempo transcurrido desde que se generó la respuesta en el servidor de origen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**\_permitir consulta \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recibe el [*verbo http*](glossary.md)s compatible con el servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**\_información de \_ autenticación de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el encabezado de Authentication-Info.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**\_autorización de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera las credenciales de autorización usadas para una solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**\_control de \_ caché de consultas WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera las directivas de control de caché.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**\_conexión de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera todas las opciones que se especifican para una conexión determinada y que los servidores proxy no deben comunicar con otras conexiones.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**\_base de \_ contenido de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el identificador uniforme de recursos (URI) base para resolver las direcciones URL relativas dentro de la entidad.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**Descripción del contenido de la \_ consulta WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**\_disposición de \_ contenido de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**\_codificación de \_ contenido de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera la codificación de contenido adicional que se ha aplicado a todo el recurso.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**\_identificador de \_ contenido de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera la identificación del contenido.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**\_idioma del \_ contenido de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el idioma en el que se escribe el contenido.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**\_longitud del \_ contenido de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el tamaño del recurso, en bytes.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**\_Ubicación del \_ contenido de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera la ubicación del recurso para la entidad que se encuentra en el mensaje.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**\_Contenido de consulta WinHTTP \_ \_ MD5**
</dt> <dd> <dl> <dt>



Recupera una síntesis MD5 del cuerpo de la entidad con el fin de proporcionar una comprobación de integridad de mensajes de un extremo a otro para el cuerpo de la entidad. Para obtener más información, consulte [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**\_intervalo de \_ contenido de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera la ubicación en el cuerpo de la entidad completa donde se debe insertar el cuerpo de la entidad parcial y el tamaño total del cuerpo de la entidad completo.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**\_codificación de \_ transferencia de contenido de consulta WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera una transformación de codificación aplicable a un cuerpo de entidad. Es posible que ya se haya aplicado, puede que deba aplicarse o que se pueda aplicar opcionalmente.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**\_tipo de \_ contenido de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recibe el tipo de contenido del recurso, como texto o HTML.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**\_cookie de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera las cookies asociadas a la solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**\_costo de consulta de WinHTTP \_**
</dt> <dd> <dl> <dt>



No se admite.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**\_consulta WinHTTP \_ personalizada**
</dt> <dd> <dl> <dt>



Hace que [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) busque el nombre de encabezado especificado en el parámetro *pwszName* y almacene la información de encabezado en *lpBuffer*. Una aplicación puede usar **la \_ opción WinHTTP \_ Receive \_ Response \_ timeout** para limitar el tiempo máximo que esta consulta espera a que se reciban todos los encabezados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**\_fecha de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recibe la fecha y hora en que se originó el mensaje.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**\_consulta WinHTTP \_ derivada \_ de**
</dt> <dd> <dl> <dt>



No se admite.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**\_ETag de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera la etiqueta de entidad para la entidad asociada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**\_espera de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el encabezado Expect, que indica si la aplicación cliente debe esperar respuestas de la serie 100.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**la \_ consulta WinHTTP \_ expira**
</dt> <dd> <dl> <dt>



Recibe la fecha y hora después de la cual el recurso debe considerarse obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**\_consulta WinHTTP \_ reenviada**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**\_consulta WinHTTP \_ desde**
</dt> <dd> <dl> <dt>



Recupera la dirección de correo electrónico del usuario que controla el agente de [*usuario*](glossary.md) solicitante si se proporciona el encabezado From.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**\_host de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el host de Internet y el número de puerto del recurso que se solicita.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**\_consulta WinHTTP \_ si \_ coincide**
</dt> <dd> <dl> <dt>



Recupera el contenido del If-Match campo de encabezado de la solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**\_consulta WinHTTP \_ si se \_ modificó \_ desde**
</dt> <dd> <dl> <dt>



Recupera el contenido del encabezado If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**\_consulta WinHTTP \_ si \_ ninguna \_ coincide**
</dt> <dd> <dl> <dt>



Recupera el contenido del campo de encabezado de solicitud if-None-Match.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**\_consulta WinHTTP \_ si el \_ intervalo**
</dt> <dd> <dl> <dt>



Recupera el contenido del If-Range campo de encabezado de la solicitud. Este encabezado permite que la aplicación cliente Compruebe si la entidad relacionada con una copia parcial de la entidad en la memoria caché de la aplicación cliente no se ha actualizado. Si la entidad no se ha actualizado, envíe las partes que faltan en la aplicación cliente. Si la entidad se ha actualizado, envíe toda la entidad actualizada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**consulta WINHTTP si no se ha \_ \_ \_ modificado \_ desde**
</dt> <dd> <dl> <dt>



Recupera el contenido del campo de encabezado de solicitud if-Unmodified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**\_vínculo de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_ \_ última \_ modificación de la consulta WinHTTP**
</dt> <dd> <dl> <dt>



Recibe la fecha y hora en que se modificó por última vez el recurso. La fecha y la hora vienen determinadas por el servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**Ubicación de la \_ consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el URI absoluto usado en un encabezado de respuesta de ubicación.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**\_número máximo de consultas WinHTTP \_**
</dt> <dd> <dl> <dt>



Indica el valor máximo de un \_ valor de consulta WinHTTP \_ \* . No es una marca de consulta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**\_ \_ número máximo de \_ reenvíos de consultas WinHTTP**
</dt> <dd> <dl> <dt>



Recupera el número de servidores proxy o puertas de enlace que pueden reenviar la solicitud al siguiente servidor entrante.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**\_identificador del \_ mensaje de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



No se admite.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**\_ \_ versión MIME de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recibe la versión del protocolo Extensiones multipropósito de correo Internet (MIME) que se utilizó para crear el mensaje.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**\_ \_ URI orig. consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**\_pragma de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recibe las directivas específicas de la implementación que se pueden aplicar a cualquier destinatario a lo largo de la cadena de solicitud/respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**\_autenticación de \_ proxy de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el esquema de autenticación y el dominio Kerberos que devuelve el proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**\_autorización del \_ proxy de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el encabezado que se usa para identificar al usuario en un proxy que requiere autenticación. Este encabezado solo se puede recuperar antes de que se envíe la solicitud al servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**\_conexión del \_ proxy de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el encabezado de Proxy-Connection.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**\_ \_ compatibilidad con el proxy de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el encabezado de Proxy-Support.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**\_consulta WinHTTP \_ pública**
</dt> <dd> <dl> <dt>



Recibe los verbos HTTP disponibles en este servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**\_intervalo de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el intervalo de bytes de una entidad.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**\_encabezados de consulta WinHTTP \_ sin formato \_**
</dt> <dd> <dl> <dt>



Recibe todos los encabezados devueltos por el servidor. Cada encabezado termina en " \\ 0". Un " \\ 0" adicional finaliza la lista de encabezados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**Los encabezados de consulta WINHTTP no tienen el carácter \_ \_ \_ \_ CRLF**
</dt> <dd> <dl> <dt>



Recibe todos los encabezados devueltos por el servidor. Cada encabezado está separado por una secuencia de retorno de carro/avance de línea (CR/LF).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**referencia a WINHTTP \_ consulta \_**
</dt> <dd> <dl> <dt>



Recibe el URI del recurso en el que se obtuvo el URI solicitado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**\_actualización de consultas WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**\_método de \_ solicitud de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recibe el verbo HTTP que se usa en la solicitud, normalmente GET o POST.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**reintento de consulta de WINHTTP \_ \_ \_ después de**
</dt> <dd> <dl> <dt>



Recupera la cantidad de tiempo que se espera que el servicio no esté disponible.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**\_servidor de consultas WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera información sobre el software usado por el servidor de origen para controlar la solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**\_cookie de \_ conjunto de consultas WinHTTP \_**
</dt> <dd> <dl> <dt>



Recibe el valor del conjunto de cookies para la solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**\_código de \_ Estado de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recibe el código de estado devuelto por el servidor. Para obtener una lista de los valores posibles, consulte [**códigos de estado http**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**\_texto de \_ Estado de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recibe texto adicional devuelto por el servidor en la línea de respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**título de la \_ consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Se mantiene para la compatibilidad de aplicaciones heredada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**\_codificación de \_ transferencia de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el tipo de transformación que se ha aplicado al cuerpo del mensaje para que se pueda transferir de forma segura entre el remitente y el destinatario.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**\_consulta WinHTTP \_ a menos que se \_ modifique \_ desde**
</dt> <dd> <dl> <dt>



Recupera el encabezado a menos que-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**\_actualización de consultas WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera los protocolos de comunicación adicionales admitidos por el servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**\_URI de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recibe parte o todo el URI por el que se puede identificar el recurso de URI de solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**\_agente de \_ usuario de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera información sobre el agente de usuario que realizó la solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**variación de la \_ consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera el encabezado que indica que la entidad se ha seleccionado de varias representaciones disponibles de la respuesta mediante la negociación controlada por el servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**\_versión de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera la versión HTTP que se encuentra en la línea de estado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**\_consulta WinHTTP \_ a través de**
</dt> <dd> <dl> <dt>



Recupera los protocolos y destinatarios intermedios entre el agente de usuario y el servidor en las solicitudes, y entre el servidor de origen y el cliente en las respuestas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**\_Advertencia de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera información adicional sobre el estado de una respuesta que podría no reflejarse en el código de estado de la respuesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**\_consulta WinHTTP \_ de \_ autenticación www**
</dt> <dd> <dl> <dt>



Recupera el esquema de autenticación y el dominio Kerberos devueltos por el servidor.


</dt> </dl> </dd> </dl>

Las marcas modificadoras se usan junto con una marca de atributo para modificar la solicitud. Las marcas modificadoras modifican el formato de los datos devueltos o indican dónde debe buscar la información la función [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) .

<dl> <dt>

<span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**\_número de \_ marca de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Devuelve los datos como un número de 32 bits para los encabezados cuyo valor es un número, como el código de estado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**\_encabezados de \_ solicitud de marca de consulta WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Solo solicita encabezados de solicitud.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**la \_ marca de consulta WinHTTP \_ \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>



Devuelve el valor de encabezado como una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , que no requiere que la aplicación analice los datos. Se usa para los encabezados cuyo valor es una cadena de fecha y hora, como "Last-Modified-Time".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>      |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>   |
| Encabezado<br/>                   | <dl> <dt>Winhttp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

