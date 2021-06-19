---
description: WinHttpQueryHeaders usa estos atributos y modificadores.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Marcas de información de consulta (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8a7f95f0e093f175901e4bed30f4055a04b8
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396630"
---
# <a name="query-info-flags-winhttph"></a><span data-ttu-id="18ba8-103">Marcas de información de consulta (Winhttp.h)</span><span class="sxs-lookup"><span data-stu-id="18ba8-103">Query Info Flags (Winhttp.h)</span></span>

<span data-ttu-id="18ba8-104">[**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders)usa estos atributos y modificadores.</span><span class="sxs-lookup"><span data-stu-id="18ba8-104">These attributes and modifiers are used by [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

<span data-ttu-id="18ba8-105">[**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) usa las marcas de atributo para indicar qué información se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="18ba8-105">The attribute flags are used by [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) to indicate what information to retrieve.</span></span> <span data-ttu-id="18ba8-106">La mayoría de las marcas de atributo se asignan directamente a un encabezado HTTP específico.</span><span class="sxs-lookup"><span data-stu-id="18ba8-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="18ba8-107">También hay algunas marcas especiales, como WINHTTP \_ QUERY \_ RAW \_ HEADERS, que no están relacionadas con un encabezado específico.</span><span class="sxs-lookup"><span data-stu-id="18ba8-107">There are also some special flags, such as WINHTTP\_QUERY\_RAW\_HEADERS, that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="18ba8-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**ACEPTACIÓN \_ DE CONSULTAS \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-109">Recupera los tipos de medios aceptables para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18ba8-109">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ CHARSET**</span><span class="sxs-lookup"><span data-stu-id="18ba8-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-111">Recupera los juegos de caracteres aceptables para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18ba8-111">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**CODIFICACIÓN \_ DE \_ ACEPTACIÓN DE CONSULTAS \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-113">Recupera los valores de codificación de contenido aceptables para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18ba8-113">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**LENGUAJE DE \_ ACEPTACIÓN \_ DE CONSULTAS WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-115">Recupera los lenguajes naturales aceptables para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18ba8-115">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**INTERVALOS DE \_ \_ ACEPTACIÓN \_ DE CONSULTAS WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-117">Recupera los tipos de solicitudes de intervalo que se aceptan para un recurso.</span><span class="sxs-lookup"><span data-stu-id="18ba8-117">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**\_ANTIGÜEDAD DE CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WINHTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-119">Recupera el campo Age response-header ,que contiene la estimación del remitente de la cantidad de tiempo desde que se generó la respuesta en el servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="18ba8-119">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP \_ QUERY \_ ALLOW**</span><span class="sxs-lookup"><span data-stu-id="18ba8-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-121">Recibe los [**verbos HTTP admitidos**](glossary.md) por el servidor.</span><span class="sxs-lookup"><span data-stu-id="18ba8-121">Receives the [**HTTP verbs**](glossary.md) supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**INFORMACIÓN DE \_ AUTENTICACIÓN \_ DE CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**WINHTTP\_QUERY\_AUTHENTICATION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-123">Recupera el Authentication-Info encabezado.</span><span class="sxs-lookup"><span data-stu-id="18ba8-123">Retrieves the Authentication-Info header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**AUTORIZACIÓN DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WINHTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-125">Recupera las credenciales de autorización usadas para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="18ba8-125">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**CONTROL DE CACHÉ DE CONSULTAS WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WINHTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-127">Recupera las directivas de control de caché.</span><span class="sxs-lookup"><span data-stu-id="18ba8-127">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**CONEXIÓN DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WINHTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-129">Recupera las opciones especificadas para una conexión determinada y no deben comunicarse mediante servidores proxy a través de conexiones adicionales.</span><span class="sxs-lookup"><span data-stu-id="18ba8-129">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**BASE DE \_ CONTENIDO DE \_ CONSULTA WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**WINHTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-131">Recupera el identificador uniforme de recursos (URI) base para resolver las direcciones URL relativas dentro de la entidad.</span><span class="sxs-lookup"><span data-stu-id="18ba8-131">Retrieves the base Uniform Resource Identifier (URI) to resolve relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**DESCRIPCIÓN DEL \_ CONTENIDO DE LA CONSULTA \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**WINHTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-133">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="18ba8-133">Obsolete.</span></span> <span data-ttu-id="18ba8-134">Se mantiene para la compatibilidad de aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="18ba8-134">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**DISPOSICIÓN DE \_ CONTENIDO DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**WINHTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-136">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="18ba8-136">Obsolete.</span></span> <span data-ttu-id="18ba8-137">Se mantiene para la compatibilidad de aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="18ba8-137">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**CODIFICACIÓN DE \_ CONTENIDO \_ DE CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-139">Recupera la codificación de contenido adicional que se ha aplicado a todo el recurso.</span><span class="sxs-lookup"><span data-stu-id="18ba8-139">Retrieves additional content coding that has been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**IDENTIFICADOR DE \_ CONTENIDO DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WINHTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-141">Recupera la identificación del contenido.</span><span class="sxs-lookup"><span data-stu-id="18ba8-141">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**LENGUAJE DE \_ CONTENIDO DE \_ CONSULTA WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**WINHTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-143">Recupera el idioma en el que se escribe el contenido.</span><span class="sxs-lookup"><span data-stu-id="18ba8-143">Retrieves the language that the content is written in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**LONGITUD DEL \_ CONTENIDO DE LA CONSULTA \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**WINHTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-145">Recupera el tamaño del recurso, en bytes.</span><span class="sxs-lookup"><span data-stu-id="18ba8-145">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**UBICACIÓN DEL \_ CONTENIDO DE LA CONSULTA \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**WINHTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-147">Recupera la ubicación del recurso para la entidad incluida en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="18ba8-147">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**CONTENIDO DE \_ CONSULTA \_ WINHTTP \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="18ba8-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-149">Recupera una síntesis MD5 del cuerpo de la entidad con el fin de proporcionar una comprobación de integridad de mensajes de un extremo a otro para el cuerpo de la entidad.</span><span class="sxs-lookup"><span data-stu-id="18ba8-149">Retrieves an MD5 digest of the entity body for the purpose of providing an end-to-end message integrity check for the entity body.</span></span> <span data-ttu-id="18ba8-150">Para obtener más información, [vea RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span><span class="sxs-lookup"><span data-stu-id="18ba8-150">For more information, see [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**INTERVALO DE CONTENIDO \_ DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**WINHTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-152">Recupera la ubicación en el cuerpo completo de la entidad donde se debe insertar el cuerpo parcial de la entidad y el tamaño total del cuerpo completo de la entidad.</span><span class="sxs-lookup"><span data-stu-id="18ba8-152">Retrieves the location in the full entity body where the partial entity body should be inserted and the total size of the full entity body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**CODIFICACIÓN DE \_ TRANSFERENCIA DE CONTENIDO DE CONSULTA \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-154">Recupera una transformación de codificación aplicable a un cuerpo de entidad.</span><span class="sxs-lookup"><span data-stu-id="18ba8-154">Retrieves an encoding transformation applicable to an entity-body.</span></span> <span data-ttu-id="18ba8-155">Es posible que ya se haya aplicado, que tenga que aplicarse o que sea opcionalmente aplicable.</span><span class="sxs-lookup"><span data-stu-id="18ba8-155">It may already have been applied, may need to be applied, or may be optionally applicable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**TIPO DE \_ CONTENIDO DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WINHTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-157">Recibe el tipo de contenido del recurso, como texto o html.</span><span class="sxs-lookup"><span data-stu-id="18ba8-157">Receives the content type of the resource, such as text or html.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**COOKIE DE CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WINHTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-159">Recupera las cookies asociadas a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18ba8-159">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**COSTO DE CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WINHTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-161">No compatible.</span><span class="sxs-lookup"><span data-stu-id="18ba8-161">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**CONSULTA WINHTTP \_ \_ PERSONALIZADA**</span><span class="sxs-lookup"><span data-stu-id="18ba8-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-163">Hace [**que WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) busque el nombre de encabezado especificado en el parámetro *pwszName* y almacene la información de encabezado *en lpBuffer*.</span><span class="sxs-lookup"><span data-stu-id="18ba8-163">Causes [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) to search for the header name specified in the *pwszName* parameter and store the header information in *lpBuffer*.</span></span> <span data-ttu-id="18ba8-164">Una aplicación puede usar **WINHTTP \_ OPTION RECEIVE RESPONSE \_ \_ \_ TIMEOUT** para limitar el tiempo máximo que esta consulta espera a que se reciban todos los encabezados.</span><span class="sxs-lookup"><span data-stu-id="18ba8-164">An application can use **WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT** to limit the maximum time this query waits for all headers to be received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**FECHA DE CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-166">Recibe la fecha y hora en que se originó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="18ba8-166">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**CONSULTA WINHTTP \_ \_ DERIVADA \_ DE**</span><span class="sxs-lookup"><span data-stu-id="18ba8-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**WINHTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-168">No compatible.</span><span class="sxs-lookup"><span data-stu-id="18ba8-168">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**ETAG DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-170">Recupera la etiqueta de entidad para la entidad asociada.</span><span class="sxs-lookup"><span data-stu-id="18ba8-170">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP \_ QUERY \_ EXPECT**</span><span class="sxs-lookup"><span data-stu-id="18ba8-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-172">Recupera el encabezado Expect, que indica si la aplicación cliente debe esperar 100 respuestas de la serie.</span><span class="sxs-lookup"><span data-stu-id="18ba8-172">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**LA CONSULTA WINHTTP \_ \_ EXPIRA**</span><span class="sxs-lookup"><span data-stu-id="18ba8-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WINHTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-174">Recibe la fecha y hora después de la cual el recurso debe considerarse obsoleto.</span><span class="sxs-lookup"><span data-stu-id="18ba8-174">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**CONSULTA WINHTTP \_ \_ REENVIADA**</span><span class="sxs-lookup"><span data-stu-id="18ba8-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**WINHTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-176">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="18ba8-176">Obsolete.</span></span> <span data-ttu-id="18ba8-177">Se mantiene para la compatibilidad de aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="18ba8-177">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**CONSULTA WINHTTP \_ \_ DESDE**</span><span class="sxs-lookup"><span data-stu-id="18ba8-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-179">Recupera la dirección de correo electrónico del usuario que controla el agente de usuario solicitante [*si*](glossary.md) se ha dado el encabezado From.</span><span class="sxs-lookup"><span data-stu-id="18ba8-179">Retrieves the e-mail address for the user who controls the requesting [*user agent*](glossary.md) if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**HOST DE CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WINHTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-181">Recupera el host de Internet y el número de puerto del recurso que se solicita.</span><span class="sxs-lookup"><span data-stu-id="18ba8-181">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**CONSULTA WINHTTP \_ \_ IF \_ MATCH**</span><span class="sxs-lookup"><span data-stu-id="18ba8-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-183">Recupera el contenido del If-Match de encabezado de solicitud.</span><span class="sxs-lookup"><span data-stu-id="18ba8-183">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**CONSULTA WINHTTP \_ SI \_ SE MODIFICA \_ \_ DESDE**</span><span class="sxs-lookup"><span data-stu-id="18ba8-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**WINHTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-185">Recupera el contenido del encabezado If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="18ba8-185">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**CONSULTA WINHTTP \_ \_ SI NINGUNA \_ \_ COINCIDE**</span><span class="sxs-lookup"><span data-stu-id="18ba8-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**WINHTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-187">Recupera el contenido del campo de encabezado de solicitud If-None-Match.</span><span class="sxs-lookup"><span data-stu-id="18ba8-187">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**CONSULTA WINHTTP \_ \_ IF \_ RANGE**</span><span class="sxs-lookup"><span data-stu-id="18ba8-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-189">Recupera el contenido del If-Range de encabezado de solicitud.</span><span class="sxs-lookup"><span data-stu-id="18ba8-189">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="18ba8-190">Este encabezado permite a la aplicación cliente comprobar si la entidad relacionada con una copia parcial de la entidad en la memoria caché de la aplicación cliente no se ha actualizado.</span><span class="sxs-lookup"><span data-stu-id="18ba8-190">This header allows the client application to check if the entity related to a partial copy of the entity in the client application's cache has not been updated.</span></span> <span data-ttu-id="18ba8-191">Si la entidad no se ha actualizado, envíe los elementos que faltan en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="18ba8-191">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="18ba8-192">Si la entidad se ha actualizado, envíe toda la entidad actualizada.</span><span class="sxs-lookup"><span data-stu-id="18ba8-192">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**CONSULTA WINHTTP \_ SI NO SE HA CAMBIADO \_ \_ \_ DESDE**</span><span class="sxs-lookup"><span data-stu-id="18ba8-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WINHTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-194">Recupera el contenido del campo de encabezado de solicitud If-Unmodified-Since.</span><span class="sxs-lookup"><span data-stu-id="18ba8-194">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**VÍNCULO DE CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WINHTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-196">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="18ba8-196">Obsolete.</span></span> <span data-ttu-id="18ba8-197">Se mantiene para la compatibilidad de aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="18ba8-197">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**ÚLTIMA MODIFICACIÓN \_ DE \_ LA CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**WINHTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-199">Recibe la fecha y hora en que se modificó por última vez el recurso.</span><span class="sxs-lookup"><span data-stu-id="18ba8-199">Receives the date and time at which the resource was last modified.</span></span> <span data-ttu-id="18ba8-200">El servidor determina la fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="18ba8-200">The date and time are determined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**UBICACIÓN DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WINHTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-202">Recupera el URI absoluto usado en un encabezado de respuesta Location.</span><span class="sxs-lookup"><span data-stu-id="18ba8-202">Retrieves the absolute URI used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP \_ QUERY \_ MAX**</span><span class="sxs-lookup"><span data-stu-id="18ba8-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-204">Indica el valor máximo de un valor DE CONSULTA \_ \_ \* WINHTTP.</span><span class="sxs-lookup"><span data-stu-id="18ba8-204">Indicates the maximum value of a WINHTTP\_QUERY\_\* value.</span></span> <span data-ttu-id="18ba8-205">No es una marca de consulta.</span><span class="sxs-lookup"><span data-stu-id="18ba8-205">Not a query flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**REENVÍOS \_ \_ MÁXIMOS DE CONSULTAS \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-207">Recupera el número de servidores proxy o puertas de enlace que pueden reenviar la solicitud al siguiente servidor de entrada.</span><span class="sxs-lookup"><span data-stu-id="18ba8-207">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**IDENTIFICADOR DE MENSAJE \_ DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WINHTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-209">No compatible.</span><span class="sxs-lookup"><span data-stu-id="18ba8-209">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**VERSIÓN MIME \_ DE CONSULTA \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WINHTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-211">Recibe la versión del protocolo Multipurpose Internet Mail Extensions (MIME) que se usó para construir el mensaje.</span><span class="sxs-lookup"><span data-stu-id="18ba8-211">Receives the version of the Multipurpose Internet Mail Extensions (MIME) protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**URI DE \_ ORIG DE CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**WINHTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-213">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="18ba8-213">Obsolete.</span></span> <span data-ttu-id="18ba8-214">Se mantiene para la compatibilidad de aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="18ba8-214">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**\_PRAGMA DE CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-216">Recibe las directivas específicas de la implementación que podrían aplicarse a cualquier destinatario a lo largo de la cadena de solicitud/respuesta.</span><span class="sxs-lookup"><span data-stu-id="18ba8-216">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**AUTENTICACIÓN DEL \_ \_ PROXY DE CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**WINHTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-218">Recupera el esquema de autenticación y el dominio kerberos devueltos por el proxy.</span><span class="sxs-lookup"><span data-stu-id="18ba8-218">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**AUTORIZACIÓN DEL \_ PROXY DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WINHTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-220">Recupera el encabezado que se usa para identificar al usuario en un proxy que requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="18ba8-220">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="18ba8-221">Este encabezado solo se puede recuperar antes de que la solicitud se envíe al servidor.</span><span class="sxs-lookup"><span data-stu-id="18ba8-221">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**CONEXIÓN DE \_ PROXY DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WINHTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-223">Recupera el Proxy-Connection encabezado.</span><span class="sxs-lookup"><span data-stu-id="18ba8-223">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**COMPATIBILIDAD CON \_ EL PROXY DE CONSULTA \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**WINHTTP\_QUERY\_PROXY\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-225">Recupera el Proxy-Support encabezado.</span><span class="sxs-lookup"><span data-stu-id="18ba8-225">Retrieves the Proxy-Support header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**CONSULTA WINHTTP \_ \_ PÚBLICA**</span><span class="sxs-lookup"><span data-stu-id="18ba8-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-227">Recibe verbos HTTP disponibles en este servidor.</span><span class="sxs-lookup"><span data-stu-id="18ba8-227">Receives HTTP verbs available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**INTERVALO DE CONSULTAS WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WINHTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-229">Recupera el intervalo de bytes de una entidad.</span><span class="sxs-lookup"><span data-stu-id="18ba8-229">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**ENCABEZADOS SIN \_ \_ PROCESAR DE CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**WINHTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-231">Recibe todos los encabezados devueltos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="18ba8-231">Receives all the headers returned by the server.</span></span> <span data-ttu-id="18ba8-232">Cada encabezado termina con \\ "0".</span><span class="sxs-lookup"><span data-stu-id="18ba8-232">Each header is terminated by "\\0".</span></span> <span data-ttu-id="18ba8-233">Un \\ "0" adicional finaliza la lista de encabezados.</span><span class="sxs-lookup"><span data-stu-id="18ba8-233">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**ENCABEZADOS SIN PROCESAR DE CONSULTA \_ \_ \_ \_ WINHTTP CRLF**</span><span class="sxs-lookup"><span data-stu-id="18ba8-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-235">Recibe todos los encabezados devueltos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="18ba8-235">Receives all the headers returned by the server.</span></span> <span data-ttu-id="18ba8-236">Cada encabezado está separado por una secuencia de retorno de carro/avance de línea (CR/LF).</span><span class="sxs-lookup"><span data-stu-id="18ba8-236">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**REFERENCIA DE CONSULTAS WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WINHTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-238">Recibe el URI del recurso donde se obtuvo el URI solicitado.</span><span class="sxs-lookup"><span data-stu-id="18ba8-238">Receives the URI of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**ACTUALIZACIÓN DE \_ CONSULTAS \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WINHTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-240">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="18ba8-240">Obsolete.</span></span> <span data-ttu-id="18ba8-241">Se mantiene para la compatibilidad de aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="18ba8-241">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**MÉTODO DE SOLICITUD \_ \_ DE CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WINHTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-243">Recibe el verbo HTTP que se usa en la solicitud, normalmente GET o POST.</span><span class="sxs-lookup"><span data-stu-id="18ba8-243">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**REINTENTO DE CONSULTA WINHTTP \_ \_ \_ DESPUÉS**</span><span class="sxs-lookup"><span data-stu-id="18ba8-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-245">Recupera la cantidad de tiempo que se espera que el servicio no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="18ba8-245">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**SERVIDOR DE CONSULTAS WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WINHTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-247">Recupera información sobre el software utilizado por el servidor de origen para controlar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18ba8-247">Retrieves information about the software used by the originating server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**COOKIE DEL \_ CONJUNTO DE \_ CONSULTAS WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WINHTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-249">Recibe el valor del conjunto de cookies para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18ba8-249">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**CÓDIGO DE ESTADO \_ DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WINHTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-251">Recibe el código de estado devuelto por el servidor.</span><span class="sxs-lookup"><span data-stu-id="18ba8-251">Receives the status code returned by the server.</span></span> <span data-ttu-id="18ba8-252">Para obtener una lista de valores posibles, vea [**Códigos de estado HTTP**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="18ba8-252">For a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**TEXTO DE ESTADO \_ \_ DE CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**WINHTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-254">Recibe texto adicional devuelto por el servidor en la línea de respuesta.</span><span class="sxs-lookup"><span data-stu-id="18ba8-254">Receives additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**TÍTULO DE CONSULTA \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WINHTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-256">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="18ba8-256">Obsolete.</span></span> <span data-ttu-id="18ba8-257">Se mantiene para la compatibilidad de aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="18ba8-257">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**CODIFICACIÓN DE \_ TRANSFERENCIA \_ DE CONSULTAS \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**WINHTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-259">Recupera el tipo de transformación que se ha aplicado al cuerpo del mensaje para que se pueda transferir de forma segura entre el remitente y el destinatario.</span><span class="sxs-lookup"><span data-stu-id="18ba8-259">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**CONSULTA WINHTTP \_ A MENOS QUE SE MODIFIQUE \_ \_ \_ DESDE**</span><span class="sxs-lookup"><span data-stu-id="18ba8-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**WINHTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-261">Recupera el encabezado Unless-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="18ba8-261">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**ACTUALIZACIÓN DE \_ CONSULTAS \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WINHTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-263">Recupera los protocolos de comunicación adicionales admitidos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="18ba8-263">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**URI DE CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WINHTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-265">Recibe parte o todo el URI por el que se puede identificar el recurso Request-URI.</span><span class="sxs-lookup"><span data-stu-id="18ba8-265">Receives some or all of the URI by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**AGENTE DE USUARIO \_ DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WINHTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-267">Recupera información sobre el agente de usuario que realizó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18ba8-267">Retrieves information about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**LAS CONSULTAS WINHTTP \_ \_ VARÍAN**</span><span class="sxs-lookup"><span data-stu-id="18ba8-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-269">Recupera el encabezado que indica que la entidad se seleccionó de una serie de representaciones disponibles de la respuesta mediante la negociación controlada por el servidor.</span><span class="sxs-lookup"><span data-stu-id="18ba8-269">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**VERSIÓN DE CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18ba8-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WINHTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-271">Recupera la versión HTTP que está presente en la línea de estado.</span><span class="sxs-lookup"><span data-stu-id="18ba8-271">Retrieves the HTTP version that is present in the status line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**CONSULTA WINHTTP \_ A \_ TRAVÉS DE**</span><span class="sxs-lookup"><span data-stu-id="18ba8-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WINHTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-273">Recupera los protocolos intermedios y los destinatarios entre el agente de usuario y el servidor en las solicitudes, y entre el servidor de origen y el cliente en las respuestas.</span><span class="sxs-lookup"><span data-stu-id="18ba8-273">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**ADVERTENCIA DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WINHTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-275">Recupera información adicional sobre el estado de una respuesta que podría no reflejarse en el código de estado de respuesta.</span><span class="sxs-lookup"><span data-stu-id="18ba8-275">Retrieves additional information about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**AUTENTICACIÓN WWW DE \_ LA \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-277">Recupera el esquema de autenticación y el dominio kerberos devueltos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="18ba8-277">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="18ba8-278">Las marcas modificadoras se usan junto con una marca de atributo para modificar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18ba8-278">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="18ba8-279">Las marcas modificadoras modifican el formato de los datos devueltos o indican dónde debe buscar la información [**la función WinHttpQueryHeaders.**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders)</span><span class="sxs-lookup"><span data-stu-id="18ba8-279">Modifier flags either modify the format of the data returned or indicate where the [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) function should search for the information.</span></span>

<dl> <dt>

<span data-ttu-id="18ba8-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**NÚMERO DE MARCA \_ \_ DE CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WINHTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-281">Devuelve los datos como un número de 32 bits para los encabezados cuyo valor es un número, como el código de estado.</span><span class="sxs-lookup"><span data-stu-id="18ba8-281">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**ENCABEZADOS DE \_ SOLICITUD DE MARCA DE CONSULTA \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WINHTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-283">Consulta solo encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="18ba8-283">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ba8-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**MARCA DE CONSULTA WINHTTP \_ \_ \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="18ba8-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WINHTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18ba8-285">Devuelve el valor de encabezado como [**una estructura SYSTEMTIME,**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que no requiere que la aplicación analice los datos.</span><span class="sxs-lookup"><span data-stu-id="18ba8-285">Returns the header value as a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="18ba8-286">Se usa para los encabezados cuyo valor es una cadena de fecha y hora, como "Hora de última modificación".</span><span class="sxs-lookup"><span data-stu-id="18ba8-286">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="18ba8-287"><span id="WINHTTP_QUERY_FLAG_TRAILERS"></span><span id="winhttp_query_flag_trailers"></span>**FINALIZADORES DE \_ MARCA \_ DE \_ CONSULTA WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-287"><span id="WINHTTP_QUERY_FLAG_TRAILERS"></span><span id="winhttp_query_flag_trailers"></span>**WINHTTP\_QUERY\_FLAG\_TRAILERS**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="18ba8-288">Consulta los finalizadores de respuesta.</span><span class="sxs-lookup"><span data-stu-id="18ba8-288">Queries response trailers.</span></span> <span data-ttu-id="18ba8-289">Antes de consultar los finalizadores de respuesta, debe llamar [**a WinHttpReadData**](/windows/win32/api/Winhttp/nf-winhttp-winhttpreaddata) hasta que devuelva 0 bytes leídos.</span><span class="sxs-lookup"><span data-stu-id="18ba8-289">Prior to querying response trailers, you must call [**WinHttpReadData**](/windows/win32/api/Winhttp/nf-winhttp-winhttpreaddata) until it returns 0 bytes read.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="18ba8-290"><span id="WINHTTP_QUERY_FLAG_WIRE_ENCODING"></span><span id="winhttp_query_flag_wire_encoding"></span>**CODIFICACIÓN DE \_ CONEXIÓN DE LA MARCA DE CONSULTA \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="18ba8-290"><span id="WINHTTP_QUERY_FLAG_WIRE_ENCODING"></span><span id="winhttp_query_flag_wire_encoding"></span>**WINHTTP\_QUERY\_FLAG\_WIRE\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="18ba8-291">De forma predeterminada, [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) realiza una conversión Unicode antes de devolver el encabezado que se ha consultado.</span><span class="sxs-lookup"><span data-stu-id="18ba8-291">By default, [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) performs a Unicode conversion before returning the header that was queried.</span></span> <span data-ttu-id="18ba8-292">Si se establece esta marca, WinHttp devuelve el encabezado al autor de la llamada sin realizar esta conversión.</span><span class="sxs-lookup"><span data-stu-id="18ba8-292">If this flag is set, WinHttp returns the header to the caller without performing this conversion.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18ba8-293">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18ba8-293">Requirements</span></span>

| <span data-ttu-id="18ba8-294">Requisito</span><span class="sxs-lookup"><span data-stu-id="18ba8-294">Requirement</span></span> | <span data-ttu-id="18ba8-295">Valor</span><span class="sxs-lookup"><span data-stu-id="18ba8-295">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="18ba8-296">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18ba8-296">Minimum supported client</span></span> | <span data-ttu-id="18ba8-297">Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]</span><span class="sxs-lookup"><span data-stu-id="18ba8-297">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>      |
| <span data-ttu-id="18ba8-298">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18ba8-298">Minimum supported server</span></span> | <span data-ttu-id="18ba8-299">Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="18ba8-299">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>   |
| <span data-ttu-id="18ba8-300">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18ba8-300">Header</span></span>                   | <dl> <span data-ttu-id="18ba8-301"><dt>Winhttp.h</dt></span><span class="sxs-lookup"><span data-stu-id="18ba8-301"><dt>Winhttp.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="18ba8-302">Vea también</span><span class="sxs-lookup"><span data-stu-id="18ba8-302">See also</span></span>

* [<span data-ttu-id="18ba8-303">Versiones winHTTP</span><span class="sxs-lookup"><span data-stu-id="18ba8-303">WinHTTP Versions</span></span>](winhttp-versions.md)
