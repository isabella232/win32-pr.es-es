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
# <a name="query-info-flags-winineth"></a><span data-ttu-id="63206-103">Marcas de información de consulta (Wininet. h)</span><span class="sxs-lookup"><span data-stu-id="63206-103">Query Info Flags (Wininet.h)</span></span>

<span data-ttu-id="63206-104">Las listas siguientes contienen los atributos y modificadores usados por [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) y [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="63206-104">The following lists contain the attributes and modifiers used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) and [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).</span></span>

<span data-ttu-id="63206-105">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (o [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) utiliza las marcas de atributo para indicar qué datos se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="63206-105">The attribute flags are used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) to indicate what data to retrieve.</span></span> <span data-ttu-id="63206-106">La mayoría de las marcas de atributo se asignan directamente a un encabezado HTTP específico.</span><span class="sxs-lookup"><span data-stu-id="63206-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="63206-107">También hay algunas marcas especiales, como encabezados de [ \_ consulta HTTP \_ sin \_ formato](/windows), que no están relacionadas con un encabezado específico.</span><span class="sxs-lookup"><span data-stu-id="63206-107">There are also some special flags, such as [HTTP\_QUERY\_RAW\_HEADERS](/windows), that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="63206-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**\_aceptación de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**HTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-109">24</span><span class="sxs-lookup"><span data-stu-id="63206-109">24</span></span>
</dt> <dt>



<span data-ttu-id="63206-110">Recupera los tipos de medios aceptables para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63206-110">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**\_consulta HTTP \_ Accept \_ CharSet**</span><span class="sxs-lookup"><span data-stu-id="63206-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**HTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-112">25</span><span class="sxs-lookup"><span data-stu-id="63206-112">25</span></span>
</dt> <dt>



<span data-ttu-id="63206-113">Recupera los juegos de caracteres aceptables para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63206-113">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**la \_ consulta HTTP \_ acepta la \_ codificación**</span><span class="sxs-lookup"><span data-stu-id="63206-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**HTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-115">26</span><span class="sxs-lookup"><span data-stu-id="63206-115">26</span></span>
</dt> <dt>



<span data-ttu-id="63206-116">Recupera los valores de codificación de contenido aceptables para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63206-116">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**\_idioma de \_ aceptación de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-118">27</span><span class="sxs-lookup"><span data-stu-id="63206-118">27</span></span>
</dt> <dt>



<span data-ttu-id="63206-119">Recupera los idiomas naturales aceptables para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63206-119">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**\_intervalos de \_ aceptación de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**HTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-121">42</span><span class="sxs-lookup"><span data-stu-id="63206-121">42</span></span>
</dt> <dt>



<span data-ttu-id="63206-122">Recupera los tipos de solicitudes de intervalo que se aceptan para un recurso.</span><span class="sxs-lookup"><span data-stu-id="63206-122">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**antigüedad de la \_ consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**HTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-124">48</span><span class="sxs-lookup"><span data-stu-id="63206-124">48</span></span>
</dt> <dt>



<span data-ttu-id="63206-125">Recupera el campo de encabezado de respuesta de edad, que contiene la estimación del remitente de la cantidad de tiempo transcurrido desde que se generó la respuesta en el servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="63206-125">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**\_permitir consulta \_ http**</span><span class="sxs-lookup"><span data-stu-id="63206-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-127">7</span><span class="sxs-lookup"><span data-stu-id="63206-127">7</span></span>
</dt> <dt>



<span data-ttu-id="63206-128">Recibe los verbos HTTP admitidos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="63206-128">Receives the HTTP verbs supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**\_autorización de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**HTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-130">28</span><span class="sxs-lookup"><span data-stu-id="63206-130">28</span></span>
</dt> <dt>



<span data-ttu-id="63206-131">Recupera las credenciales de autorización usadas para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="63206-131">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**\_control de \_ caché de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**HTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-133">49</span><span class="sxs-lookup"><span data-stu-id="63206-133">49</span></span>
</dt> <dt>



<span data-ttu-id="63206-134">Recupera las directivas de control de caché.</span><span class="sxs-lookup"><span data-stu-id="63206-134">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**\_conexión de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**HTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-136">23</span><span class="sxs-lookup"><span data-stu-id="63206-136">23</span></span>
</dt> <dt>



<span data-ttu-id="63206-137">Recupera todas las opciones que se especifican para una conexión determinada y que los servidores proxy no deben comunicar con otras conexiones.</span><span class="sxs-lookup"><span data-stu-id="63206-137">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**\_base de \_ contenido de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**HTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-139">50</span><span class="sxs-lookup"><span data-stu-id="63206-139">50</span></span>
</dt> <dt>



<span data-ttu-id="63206-140">Recupera el URI base (identificador uniforme de recursos) para resolver las direcciones URL relativas dentro de la entidad.</span><span class="sxs-lookup"><span data-stu-id="63206-140">Retrieves the base URI (Uniform Resource Identifier) for resolving relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**Descripción del contenido de la \_ consulta HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63206-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**HTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-142">4</span><span class="sxs-lookup"><span data-stu-id="63206-142">4</span></span>
</dt> <dt>



<span data-ttu-id="63206-143">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="63206-143">Obsolete.</span></span> <span data-ttu-id="63206-144">Se mantiene únicamente por compatibilidad con aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="63206-144">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**\_disposición de \_ contenido de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**HTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-146">47</span><span class="sxs-lookup"><span data-stu-id="63206-146">47</span></span>
</dt> <dt>



<span data-ttu-id="63206-147">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="63206-147">Obsolete.</span></span> <span data-ttu-id="63206-148">Se mantiene únicamente por compatibilidad con aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="63206-148">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**\_codificación de \_ contenido de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**HTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-150">29</span><span class="sxs-lookup"><span data-stu-id="63206-150">29</span></span>
</dt> <dt>



<span data-ttu-id="63206-151">Recupera cualquier codificación de contenido adicional que se haya aplicado a todo el recurso.</span><span class="sxs-lookup"><span data-stu-id="63206-151">Retrieves any additional content codings that have been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**\_identificador de \_ contenido de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**HTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-153">3</span><span class="sxs-lookup"><span data-stu-id="63206-153">3</span></span>
</dt> <dt>



<span data-ttu-id="63206-154">Recupera la identificación del contenido.</span><span class="sxs-lookup"><span data-stu-id="63206-154">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**\_lenguaje de \_ contenido de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**HTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-156">6</span><span class="sxs-lookup"><span data-stu-id="63206-156">6</span></span>
</dt> <dt>



<span data-ttu-id="63206-157">Recupera el idioma en el que se encuentra el contenido.</span><span class="sxs-lookup"><span data-stu-id="63206-157">Retrieves the language that the content is in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**\_longitud del \_ contenido de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**HTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-159">5</span><span class="sxs-lookup"><span data-stu-id="63206-159">5</span></span>
</dt> <dt>



<span data-ttu-id="63206-160">Recupera el tamaño del recurso, en bytes.</span><span class="sxs-lookup"><span data-stu-id="63206-160">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**\_Ubicación de \_ contenido de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**HTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-162">51</span><span class="sxs-lookup"><span data-stu-id="63206-162">51</span></span>
</dt> <dt>



<span data-ttu-id="63206-163">Recupera la ubicación del recurso para la entidad que se encuentra en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="63206-163">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**\_Contenido de consulta HTTP \_ \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="63206-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**HTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-165">52</span><span class="sxs-lookup"><span data-stu-id="63206-165">52</span></span>
</dt> <dt>



<span data-ttu-id="63206-166">Recupera un resumen MD5 del cuerpo de la entidad con el fin de proporcionar una comprobación de integridad del mensaje (MIC) de un extremo a otro para el cuerpo de la entidad.</span><span class="sxs-lookup"><span data-stu-id="63206-166">Retrieves an MD5 digest of the entity-body for the purpose of providing an end-to-end message integrity check (MIC) for the entity-body.</span></span> <span data-ttu-id="63206-167">Para obtener más información, vea RFC1864, el campo Content-MD5 header, en [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .</span><span class="sxs-lookup"><span data-stu-id="63206-167">For more information, see RFC1864, The Content-MD5 Header Field, at [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**\_intervalo de \_ contenido de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**HTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-169">53</span><span class="sxs-lookup"><span data-stu-id="63206-169">53</span></span>
</dt> <dt>



<span data-ttu-id="63206-170">Recupera la ubicación en el cuerpo de entidad completo donde se debe insertar el cuerpo de entidad parcial y el tamaño total del cuerpo de entidad completo.</span><span class="sxs-lookup"><span data-stu-id="63206-170">Retrieves the location in the full entity-body where the partial entity-body should be inserted and the total size of the full entity-body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**\_codificación de \_ transferencia de contenido de consulta HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63206-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**HTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-172">2</span><span class="sxs-lookup"><span data-stu-id="63206-172">2</span></span>
</dt> <dt>



<span data-ttu-id="63206-173">Recibe la codificación de contenido adicional que se ha aplicado al recurso.</span><span class="sxs-lookup"><span data-stu-id="63206-173">Receives the additional content coding that has been applied to the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**\_tipo de \_ contenido de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**HTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-175">1</span><span class="sxs-lookup"><span data-stu-id="63206-175">1</span></span>
</dt> <dt>



<span data-ttu-id="63206-176">Recibe el tipo de contenido del recurso (por ejemplo, texto/HTML).</span><span class="sxs-lookup"><span data-stu-id="63206-176">Receives the content type of the resource (such as text/html).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**\_cookie de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**HTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-178">44</span><span class="sxs-lookup"><span data-stu-id="63206-178">44</span></span>
</dt> <dt>



<span data-ttu-id="63206-179">Recupera las cookies asociadas a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63206-179">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**\_costo de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**HTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-181">15</span><span class="sxs-lookup"><span data-stu-id="63206-181">15</span></span>
</dt> <dt>



<span data-ttu-id="63206-182">Ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="63206-182">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**\_consulta HTTP \_ personalizada**</span><span class="sxs-lookup"><span data-stu-id="63206-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**HTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-184">65535</span><span class="sxs-lookup"><span data-stu-id="63206-184">65535</span></span>
</dt> <dt>



<span data-ttu-id="63206-185">Hace que [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) busque el nombre de encabezado especificado en *lpvBuffer* y almacene los datos de encabezado en *lpvBuffer*.</span><span class="sxs-lookup"><span data-stu-id="63206-185">Causes [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to search for the header name specified in *lpvBuffer* and store the header data in *lpvBuffer*.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**\_fecha de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**HTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-187">9</span><span class="sxs-lookup"><span data-stu-id="63206-187">9</span></span>
</dt> <dt>



<span data-ttu-id="63206-188">Recibe la fecha y hora en que se originó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="63206-188">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**\_consulta HTTP \_ derivada \_ de**</span><span class="sxs-lookup"><span data-stu-id="63206-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**HTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-190">14</span><span class="sxs-lookup"><span data-stu-id="63206-190">14</span></span>
</dt> <dt>



<span data-ttu-id="63206-191">Ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="63206-191">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_encabezados de \_ eco de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**HTTP\_QUERY\_ECHO\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-193">73</span><span class="sxs-lookup"><span data-stu-id="63206-193">73</span></span>
</dt> <dt>



<span data-ttu-id="63206-194">No implementado actualmente.</span><span class="sxs-lookup"><span data-stu-id="63206-194">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**consulta HTTP- \_ \_ encabezados de eco \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="63206-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**HTTP\_QUERY\_ECHO\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-196">74</span><span class="sxs-lookup"><span data-stu-id="63206-196">74</span></span>
</dt> <dt>



<span data-ttu-id="63206-197">No implementado actualmente.</span><span class="sxs-lookup"><span data-stu-id="63206-197">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**\_respuesta de \_ eco de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**HTTP\_QUERY\_ECHO\_REPLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-199">72</span><span class="sxs-lookup"><span data-stu-id="63206-199">72</span></span>
</dt> <dt>



<span data-ttu-id="63206-200">No implementado actualmente.</span><span class="sxs-lookup"><span data-stu-id="63206-200">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**\_solicitud de \_ eco de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**HTTP\_QUERY\_ECHO\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-202">71</span><span class="sxs-lookup"><span data-stu-id="63206-202">71</span></span>
</dt> <dt>



<span data-ttu-id="63206-203">No implementado actualmente.</span><span class="sxs-lookup"><span data-stu-id="63206-203">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**\_ETag de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-205">54</span><span class="sxs-lookup"><span data-stu-id="63206-205">54</span></span>
</dt> <dt>



<span data-ttu-id="63206-206">Recupera la etiqueta de entidad para la entidad asociada.</span><span class="sxs-lookup"><span data-stu-id="63206-206">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**\_espera de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**HTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-208">68</span><span class="sxs-lookup"><span data-stu-id="63206-208">68</span></span>
</dt> <dt>



<span data-ttu-id="63206-209">Recupera el encabezado Expect, que indica si la aplicación cliente debe esperar respuestas de la serie 100.</span><span class="sxs-lookup"><span data-stu-id="63206-209">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**la \_ consulta HTTP \_ expira**</span><span class="sxs-lookup"><span data-stu-id="63206-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**HTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-211">10</span><span class="sxs-lookup"><span data-stu-id="63206-211">10</span></span>
</dt> <dt>



<span data-ttu-id="63206-212">Recibe la fecha y hora después de la cual el recurso debe considerarse obsoleto.</span><span class="sxs-lookup"><span data-stu-id="63206-212">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**\_consulta HTTP \_ reenviada**</span><span class="sxs-lookup"><span data-stu-id="63206-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**HTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-214">30</span><span class="sxs-lookup"><span data-stu-id="63206-214">30</span></span>
</dt> <dt>



<span data-ttu-id="63206-215">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="63206-215">Obsolete.</span></span> <span data-ttu-id="63206-216">Se mantiene únicamente por compatibilidad con aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="63206-216">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**\_consulta HTTP \_ desde**</span><span class="sxs-lookup"><span data-stu-id="63206-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-218">31</span><span class="sxs-lookup"><span data-stu-id="63206-218">31</span></span>
</dt> <dt>



<span data-ttu-id="63206-219">Recupera la dirección de correo electrónico del usuario humano que controla el agente de usuario solicitante si se proporciona el encabezado From.</span><span class="sxs-lookup"><span data-stu-id="63206-219">Retrieves the email address for the human user who controls the requesting user agent if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**\_host de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-221">55</span><span class="sxs-lookup"><span data-stu-id="63206-221">55</span></span>
</dt> <dt>



<span data-ttu-id="63206-222">Recupera el host de Internet y el número de puerto del recurso que se solicita.</span><span class="sxs-lookup"><span data-stu-id="63206-222">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**\_consulta HTTP \_ si \_ coincide**</span><span class="sxs-lookup"><span data-stu-id="63206-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**HTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-224">56</span><span class="sxs-lookup"><span data-stu-id="63206-224">56</span></span>
</dt> <dt>



<span data-ttu-id="63206-225">Recupera el contenido del If-Match campo de encabezado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63206-225">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**\_consulta HTTP \_ si se \_ modificó \_ desde**</span><span class="sxs-lookup"><span data-stu-id="63206-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**HTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-227">32</span><span class="sxs-lookup"><span data-stu-id="63206-227">32</span></span>
</dt> <dt>



<span data-ttu-id="63206-228">Recupera el contenido del encabezado If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="63206-228">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**consulta HTTP si no hay \_ \_ \_ ninguna \_ coincidencia**</span><span class="sxs-lookup"><span data-stu-id="63206-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**HTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-230">57</span><span class="sxs-lookup"><span data-stu-id="63206-230">57</span></span>
</dt> <dt>



<span data-ttu-id="63206-231">Recupera el contenido del campo de encabezado de solicitud if-None-Match.</span><span class="sxs-lookup"><span data-stu-id="63206-231">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**\_consulta HTTP \_ si \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="63206-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-233">58</span><span class="sxs-lookup"><span data-stu-id="63206-233">58</span></span>
</dt> <dt>



<span data-ttu-id="63206-234">Recupera el contenido del If-Range campo de encabezado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63206-234">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="63206-235">Este encabezado permite a la aplicación cliente comprobar que la entidad relacionada con una copia parcial de la entidad en la memoria caché de la aplicación cliente no se ha actualizado.</span><span class="sxs-lookup"><span data-stu-id="63206-235">This header enables the client application to verify that the entity related to a partial copy of the entity in the client application cache has not been updated.</span></span> <span data-ttu-id="63206-236">Si la entidad no se ha actualizado, envíe las partes que faltan en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="63206-236">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="63206-237">Si la entidad se ha actualizado, envíe toda la entidad actualizada.</span><span class="sxs-lookup"><span data-stu-id="63206-237">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**consulta HTTP si no se ha \_ \_ \_ modificado \_ desde**</span><span class="sxs-lookup"><span data-stu-id="63206-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**HTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-239">59</span><span class="sxs-lookup"><span data-stu-id="63206-239">59</span></span>
</dt> <dt>



<span data-ttu-id="63206-240">Recupera el contenido del campo de encabezado de solicitud if-Unmodified-Since.</span><span class="sxs-lookup"><span data-stu-id="63206-240">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_ \_ última \_ modificación de la consulta http**</span><span class="sxs-lookup"><span data-stu-id="63206-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**HTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-242">11</span><span class="sxs-lookup"><span data-stu-id="63206-242">11</span></span>
</dt> <dt>



<span data-ttu-id="63206-243">Recibe la fecha y hora en que el servidor considera que el recurso se modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="63206-243">Receives the date and time at which the server believes the resource was last modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**\_vínculo de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**HTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-245">16</span><span class="sxs-lookup"><span data-stu-id="63206-245">16</span></span>
</dt> <dt>



<span data-ttu-id="63206-246">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="63206-246">Obsolete.</span></span> <span data-ttu-id="63206-247">Se mantiene únicamente por compatibilidad con aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="63206-247">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**Ubicación de la \_ consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**HTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-249">33</span><span class="sxs-lookup"><span data-stu-id="63206-249">33</span></span>
</dt> <dt>



<span data-ttu-id="63206-250">Recupera el identificador uniforme de recursos (URI) absoluto usado en un encabezado de respuesta de ubicación.</span><span class="sxs-lookup"><span data-stu-id="63206-250">Retrieves the absolute Uniform Resource Identifier (URI) used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**\_consulta HTTP \_ máxima**</span><span class="sxs-lookup"><span data-stu-id="63206-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**HTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-252">78</span><span class="sxs-lookup"><span data-stu-id="63206-252">78</span></span>
</dt> <dt>



<span data-ttu-id="63206-253">No es una marca de consulta.</span><span class="sxs-lookup"><span data-stu-id="63206-253">Not a query flag.</span></span> <span data-ttu-id="63206-254">Indica el valor máximo de un \_ valor de consulta HTTP \_ \* .</span><span class="sxs-lookup"><span data-stu-id="63206-254">Indicates the maximum value of an HTTP\_QUERY\_\* value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**\_ \_ número máximo de \_ reenvíos de consultas http**</span><span class="sxs-lookup"><span data-stu-id="63206-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**HTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-256">60</span><span class="sxs-lookup"><span data-stu-id="63206-256">60</span></span>
</dt> <dt>



<span data-ttu-id="63206-257">Recupera el número de servidores proxy o puertas de enlace que pueden reenviar la solicitud al siguiente servidor entrante.</span><span class="sxs-lookup"><span data-stu-id="63206-257">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**\_identificador de \_ mensaje de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**HTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-259">12</span><span class="sxs-lookup"><span data-stu-id="63206-259">12</span></span>
</dt> <dt>



<span data-ttu-id="63206-260">Ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="63206-260">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**\_ \_ versión MIME de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**HTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-262">0</span><span class="sxs-lookup"><span data-stu-id="63206-262">0</span></span>
</dt> <dt>



<span data-ttu-id="63206-263">Recibe la versión del protocolo MIME que se usó para construir el mensaje.</span><span class="sxs-lookup"><span data-stu-id="63206-263">Receives the version of the MIME protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**\_ \_ URI original de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**HTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-265">34</span><span class="sxs-lookup"><span data-stu-id="63206-265">34</span></span>
</dt> <dt>



<span data-ttu-id="63206-266">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="63206-266">Obsolete.</span></span> <span data-ttu-id="63206-267">Se mantiene únicamente por compatibilidad con aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="63206-267">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**\_pragma de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**HTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-269">17</span><span class="sxs-lookup"><span data-stu-id="63206-269">17</span></span>
</dt> <dt>



<span data-ttu-id="63206-270">Recibe las directivas específicas de la implementación que se pueden aplicar a cualquier destinatario a lo largo de la cadena de solicitud/respuesta.</span><span class="sxs-lookup"><span data-stu-id="63206-270">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**\_autenticación de \_ proxy de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**HTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-272">41</span><span class="sxs-lookup"><span data-stu-id="63206-272">41</span></span>
</dt> <dt>



<span data-ttu-id="63206-273">Recupera el esquema de autenticación y el dominio Kerberos que devuelve el proxy.</span><span class="sxs-lookup"><span data-stu-id="63206-273">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**\_autorización de \_ proxy de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**HTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-275">61</span><span class="sxs-lookup"><span data-stu-id="63206-275">61</span></span>
</dt> <dt>



<span data-ttu-id="63206-276">Recupera el encabezado que se usa para identificar al usuario en un proxy que requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="63206-276">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="63206-277">Este encabezado solo se puede recuperar antes de que se envíe la solicitud al servidor.</span><span class="sxs-lookup"><span data-stu-id="63206-277">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**\_conexión del \_ proxy de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**HTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-279">69</span><span class="sxs-lookup"><span data-stu-id="63206-279">69</span></span>
</dt> <dt>



<span data-ttu-id="63206-280">Recupera el encabezado de Proxy-Connection.</span><span class="sxs-lookup"><span data-stu-id="63206-280">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**\_consulta HTTP \_ pública**</span><span class="sxs-lookup"><span data-stu-id="63206-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**HTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-282">8</span><span class="sxs-lookup"><span data-stu-id="63206-282">8</span></span>
</dt> <dt>



<span data-ttu-id="63206-283">Recibe los métodos disponibles en este servidor.</span><span class="sxs-lookup"><span data-stu-id="63206-283">Receives methods available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**\_intervalo de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**HTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-285">62</span><span class="sxs-lookup"><span data-stu-id="63206-285">62</span></span>
</dt> <dt>



<span data-ttu-id="63206-286">Recupera el intervalo de bytes de una entidad.</span><span class="sxs-lookup"><span data-stu-id="63206-286">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_encabezados de consulta HTTP \_ sin formato \_**</span><span class="sxs-lookup"><span data-stu-id="63206-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**HTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-288">21</span><span class="sxs-lookup"><span data-stu-id="63206-288">21</span></span>
</dt> <dt>



<span data-ttu-id="63206-289">Recibe todos los encabezados devueltos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="63206-289">Receives all the headers returned by the server.</span></span> <span data-ttu-id="63206-290">Cada encabezado termina en " \\ 0".</span><span class="sxs-lookup"><span data-stu-id="63206-290">Each header is terminated by "\\0".</span></span> <span data-ttu-id="63206-291">Un " \\ 0" adicional finaliza la lista de encabezados.</span><span class="sxs-lookup"><span data-stu-id="63206-291">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**\_ \_ hipertítulos sin formato de consulta HTTP \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="63206-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**HTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-293">22</span><span class="sxs-lookup"><span data-stu-id="63206-293">22</span></span>
</dt> <dt>



<span data-ttu-id="63206-294">Recibe todos los encabezados devueltos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="63206-294">Receives all the headers returned by the server.</span></span> <span data-ttu-id="63206-295">Cada encabezado está separado por una secuencia de retorno de carro/avance de línea (CR/LF).</span><span class="sxs-lookup"><span data-stu-id="63206-295">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**\_referencia de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**HTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-297">35</span><span class="sxs-lookup"><span data-stu-id="63206-297">35</span></span>
</dt> <dt>



<span data-ttu-id="63206-298">Recibe el identificador uniforme de recursos (URI) del recurso en el que se obtuvo el URI solicitado.</span><span class="sxs-lookup"><span data-stu-id="63206-298">Receives the Uniform Resource Identifier (URI) of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**\_actualización de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**HTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-300">46</span><span class="sxs-lookup"><span data-stu-id="63206-300">46</span></span>
</dt> <dt>



<span data-ttu-id="63206-301">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="63206-301">Obsolete.</span></span> <span data-ttu-id="63206-302">Se mantiene únicamente por compatibilidad con aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="63206-302">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**\_método de \_ solicitud de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**HTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-304">45</span><span class="sxs-lookup"><span data-stu-id="63206-304">45</span></span>
</dt> <dt>



<span data-ttu-id="63206-305">Recibe el verbo HTTP que se usa en la solicitud, normalmente GET o POST.</span><span class="sxs-lookup"><span data-stu-id="63206-305">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**reintento de \_ consulta HTTP \_ \_ tras**</span><span class="sxs-lookup"><span data-stu-id="63206-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**HTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-307">36</span><span class="sxs-lookup"><span data-stu-id="63206-307">36</span></span>
</dt> <dt>



<span data-ttu-id="63206-308">Recupera la cantidad de tiempo que se espera que el servicio no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="63206-308">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**\_servidor de consultas http \_**</span><span class="sxs-lookup"><span data-stu-id="63206-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**HTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-310">37</span><span class="sxs-lookup"><span data-stu-id="63206-310">37</span></span>
</dt> <dt>



<span data-ttu-id="63206-311">Recupera datos sobre el software usado por el servidor de origen para controlar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63206-311">Retrieves data about the software used by the origin server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**\_cookie de \_ conjunto de consultas http \_**</span><span class="sxs-lookup"><span data-stu-id="63206-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-313">43</span><span class="sxs-lookup"><span data-stu-id="63206-313">43</span></span>
</dt> <dt>



<span data-ttu-id="63206-314">Recibe el valor del conjunto de cookies para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63206-314">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**\_código de \_ Estado de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**HTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-316">19</span><span class="sxs-lookup"><span data-stu-id="63206-316">19</span></span>
</dt> <dt>



<span data-ttu-id="63206-317">Recibe el código de estado devuelto por el servidor.</span><span class="sxs-lookup"><span data-stu-id="63206-317">Receives the status code returned by the server.</span></span> <span data-ttu-id="63206-318">Para obtener más información y una lista de valores posibles, consulte [**códigos de estado http**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="63206-318">For more information and a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**\_texto de \_ Estado de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**HTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-320">20</span><span class="sxs-lookup"><span data-stu-id="63206-320">20</span></span>
</dt> <dt>



<span data-ttu-id="63206-321">Recibe cualquier texto adicional devuelto por el servidor en la línea de respuesta.</span><span class="sxs-lookup"><span data-stu-id="63206-321">Receives any additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**título de la \_ consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**HTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-323">38</span><span class="sxs-lookup"><span data-stu-id="63206-323">38</span></span>
</dt> <dt>



<span data-ttu-id="63206-324">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="63206-324">Obsolete.</span></span> <span data-ttu-id="63206-325">Se mantiene únicamente por compatibilidad con aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="63206-325">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**\_codificación de \_ transferencia de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**HTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-327">63</span><span class="sxs-lookup"><span data-stu-id="63206-327">63</span></span>
</dt> <dt>



<span data-ttu-id="63206-328">Recupera el tipo de transformación que se ha aplicado al cuerpo del mensaje para que se pueda transferir de forma segura entre el remitente y el destinatario.</span><span class="sxs-lookup"><span data-stu-id="63206-328">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**\_consulta HTTP \_ a menos que se \_ modifique \_ desde**</span><span class="sxs-lookup"><span data-stu-id="63206-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-330">70</span><span class="sxs-lookup"><span data-stu-id="63206-330">70</span></span>
</dt> <dt>



<span data-ttu-id="63206-331">Recupera el encabezado a menos que-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="63206-331">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**\_actualización de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**HTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-333">64</span><span class="sxs-lookup"><span data-stu-id="63206-333">64</span></span>
</dt> <dt>



<span data-ttu-id="63206-334">Recupera los protocolos de comunicación adicionales admitidos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="63206-334">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**\_URI de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**HTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-336">13</span><span class="sxs-lookup"><span data-stu-id="63206-336">13</span></span>
</dt> <dt>



<span data-ttu-id="63206-337">Recibe algunos o todos los identificadores uniformes de recursos (URI) mediante los cuales se puede identificar el recurso de URI de solicitud.</span><span class="sxs-lookup"><span data-stu-id="63206-337">Receives some or all of the Uniform Resource Identifiers (URIs) by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**\_agente de \_ usuario de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**HTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-339">39</span><span class="sxs-lookup"><span data-stu-id="63206-339">39</span></span>
</dt> <dt>



<span data-ttu-id="63206-340">Recupera datos sobre el agente de usuario que realizó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63206-340">Retrieves data about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**la \_ consulta HTTP \_ varía**</span><span class="sxs-lookup"><span data-stu-id="63206-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**HTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-342">65</span><span class="sxs-lookup"><span data-stu-id="63206-342">65</span></span>
</dt> <dt>



<span data-ttu-id="63206-343">Recupera el encabezado que indica que la entidad se ha seleccionado de varias representaciones disponibles de la respuesta mediante la negociación controlada por el servidor.</span><span class="sxs-lookup"><span data-stu-id="63206-343">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**\_versión de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**HTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-345">18</span><span class="sxs-lookup"><span data-stu-id="63206-345">18</span></span>
</dt> <dt>



<span data-ttu-id="63206-346">Recibe el último código de respuesta devuelto por el servidor.</span><span class="sxs-lookup"><span data-stu-id="63206-346">Receives the last response code returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**\_consulta HTTP \_ a través de**</span><span class="sxs-lookup"><span data-stu-id="63206-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-348">66</span><span class="sxs-lookup"><span data-stu-id="63206-348">66</span></span>
</dt> <dt>



<span data-ttu-id="63206-349">Recupera los protocolos y destinatarios intermedios entre el agente de usuario y el servidor en las solicitudes, y entre el servidor de origen y el cliente en las respuestas.</span><span class="sxs-lookup"><span data-stu-id="63206-349">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**\_Advertencia de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**HTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-351">67</span><span class="sxs-lookup"><span data-stu-id="63206-351">67</span></span>
</dt> <dt>



<span data-ttu-id="63206-352">Recupera datos adicionales sobre el estado de una respuesta que podría no reflejarse en el código de estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63206-352">Retrieves additional data about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP \_ query \_ www \_ Authenticate**</span><span class="sxs-lookup"><span data-stu-id="63206-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-354">40</span><span class="sxs-lookup"><span data-stu-id="63206-354">40</span></span>
</dt> <dt>



<span data-ttu-id="63206-355">Recupera el esquema de autenticación y el dominio Kerberos devueltos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="63206-355">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**\_Opciones de \_ \_ tipo de contenido X de consulta \_ http \_**</span><span class="sxs-lookup"><span data-stu-id="63206-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**HTTP\_QUERY\_X\_CONTENT\_TYPE\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-357">79</span><span class="sxs-lookup"><span data-stu-id="63206-357">79</span></span>
</dt> <dt>



<span data-ttu-id="63206-358">Recupera el valor del encabezado X-Content-Type-Options.</span><span class="sxs-lookup"><span data-stu-id="63206-358">Retrieves the X-Content-Type-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**\_Consulta HTTP \_ P3P**</span><span class="sxs-lookup"><span data-stu-id="63206-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**HTTP\_QUERY\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-360">80</span><span class="sxs-lookup"><span data-stu-id="63206-360">80</span></span>
</dt> <dt>



<span data-ttu-id="63206-361">Recupera el valor del encabezado P3P.</span><span class="sxs-lookup"><span data-stu-id="63206-361">Retrieves the P3P header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**\_Consulta HTTP \_ X \_ P2P \_ PEERDIST**</span><span class="sxs-lookup"><span data-stu-id="63206-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP\_QUERY\_X\_P2P\_PEERDIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-363">81</span><span class="sxs-lookup"><span data-stu-id="63206-363">81</span></span>
</dt> <dt>



<span data-ttu-id="63206-364">Recupera el valor del encabezado X-P2P-PeerDist.</span><span class="sxs-lookup"><span data-stu-id="63206-364">Retrieves the X-P2P-PeerDist header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**\_traducción de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP\_QUERY\_TRANSLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-366">82</span><span class="sxs-lookup"><span data-stu-id="63206-366">82</span></span>
</dt> <dt>



<span data-ttu-id="63206-367">Recupera el valor de encabezado translate.</span><span class="sxs-lookup"><span data-stu-id="63206-367">Retrieves the translate header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**\_consulta HTTP \_ X \_ UA \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="63206-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP\_QUERY\_X\_UA\_COMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-369">83</span><span class="sxs-lookup"><span data-stu-id="63206-369">83</span></span>
</dt> <dt>



<span data-ttu-id="63206-370">Recupera el valor del encabezado X-UA-compatible.</span><span class="sxs-lookup"><span data-stu-id="63206-370">Retrieves the X-UA-Compatible header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**\_ \_ estilo predeterminado de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**HTTP\_QUERY\_DEFAULT\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-372">84</span><span class="sxs-lookup"><span data-stu-id="63206-372">84</span></span>
</dt> <dt>



<span data-ttu-id="63206-373">Recupera el valor del encabezado Default-Style.</span><span class="sxs-lookup"><span data-stu-id="63206-373">Retrieves the Default-Style header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**\_Opciones de \_ \_ fotograma X de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**HTTP\_QUERY\_X\_FRAME\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-375">85</span><span class="sxs-lookup"><span data-stu-id="63206-375">85</span></span>
</dt> <dt>



<span data-ttu-id="63206-376">Recupera el valor del encabezado X-Frame-Options.</span><span class="sxs-lookup"><span data-stu-id="63206-376">Retrieves the X-Frame-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**\_consulta HTTP \_ X \_ \_ protección XSS**</span><span class="sxs-lookup"><span data-stu-id="63206-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP\_QUERY\_X\_XSS\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-378">86</span><span class="sxs-lookup"><span data-stu-id="63206-378">86</span></span>
</dt> <dt>



<span data-ttu-id="63206-379">Recupera el valor del encabezado X-XSS-Protection.</span><span class="sxs-lookup"><span data-stu-id="63206-379">Retrieves the X-XSS-Protection header value.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="63206-380">Las marcas modificadoras se usan junto con una marca de atributo para modificar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63206-380">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="63206-381">Las marcas modificadoras modifican el formato de los datos devueltos o indican dónde [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (o [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) deben buscar los datos.</span><span class="sxs-lookup"><span data-stu-id="63206-381">Modifier flags either modify the format of the data returned or indicate where [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) should search for the data.</span></span>

<dl> <dt>

<span data-ttu-id="63206-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**fusión de la \_ marca de consulta HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63206-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**HTTP\_QUERY\_FLAG\_COALESCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-383">0x10000000</span><span class="sxs-lookup"><span data-stu-id="63206-383">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="63206-384">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="63206-384">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**\_número de \_ marca de consulta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="63206-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**HTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-386">0x20000000</span><span class="sxs-lookup"><span data-stu-id="63206-386">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="63206-387">Devuelve los datos como un número de 32 bits para los encabezados cuyo valor es un número, como el código de estado.</span><span class="sxs-lookup"><span data-stu-id="63206-387">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**\_encabezados de \_ solicitud de marca de consulta HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63206-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**HTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-389">0x80000000</span><span class="sxs-lookup"><span data-stu-id="63206-389">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="63206-390">Solo solicita encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="63206-390">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="63206-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**\_marca de consulta HTTP \_ \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="63206-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**HTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63206-392">0x40000000</span><span class="sxs-lookup"><span data-stu-id="63206-392">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="63206-393">Devuelve el valor de encabezado como una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , que no requiere que la aplicación analice los datos.</span><span class="sxs-lookup"><span data-stu-id="63206-393">Returns the header value as a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="63206-394">Se usa para los encabezados cuyo valor es una cadena de fecha y hora, como "Last-Modified-Time".</span><span class="sxs-lookup"><span data-stu-id="63206-394">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63206-395">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63206-395">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="63206-396">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="63206-396">WinINet does not support server implementations.</span></span> <span data-ttu-id="63206-397">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="63206-397">In addition, it should not be used from a service.</span></span> <span data-ttu-id="63206-398">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="63206-398">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="63206-399">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63206-399">Requirements</span></span>



| <span data-ttu-id="63206-400">Requisito</span><span class="sxs-lookup"><span data-stu-id="63206-400">Requirement</span></span> | <span data-ttu-id="63206-401">Value</span><span class="sxs-lookup"><span data-stu-id="63206-401">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="63206-402">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63206-402">Minimum supported client</span></span><br/> | <span data-ttu-id="63206-403">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="63206-403">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="63206-404">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63206-404">Minimum supported server</span></span><br/> | <span data-ttu-id="63206-405">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="63206-405">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="63206-406">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63206-406">Header</span></span><br/>                   | <dl> <span data-ttu-id="63206-407"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="63206-407"><dt>Wininet.h</dt></span></span> </dl> |



 

