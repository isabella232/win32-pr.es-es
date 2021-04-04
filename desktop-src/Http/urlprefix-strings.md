---
title: Cadenas de UrlPrefix
description: En la API del servidor HTTP, un UrlPrefix es una cadena Unicode de caracteres anchos (UTF-16) con una forma canónica que especifica una sección del espacio de nombres de la dirección URL.
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- UrlPrefix Strings HTTP Server API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddc484f26bc1b3de5d20196dadec9201d3ea272
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "103797205"
---
# <a name="urlprefix-strings"></a><span data-ttu-id="62e8a-104">Cadenas de UrlPrefix</span><span class="sxs-lookup"><span data-stu-id="62e8a-104">UrlPrefix Strings</span></span>

<span data-ttu-id="62e8a-105">En la API del servidor HTTP, un *UrlPrefix* es una cadena Unicode de caracteres anchos (UTF-16) con una forma canónica que especifica una sección del espacio de nombres de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="62e8a-105">In the HTTP Server API, a *UrlPrefix* is a wide-character (UTF-16) Unicode string with a canonical form that specifies a section of URL namespace.</span></span> <span data-ttu-id="62e8a-106">Se usa para reservar una sección del espacio de nombres de la dirección URL para una cuenta de usuario o para registrar una sección del espacio de nombres de la dirección URL para un proceso.</span><span class="sxs-lookup"><span data-stu-id="62e8a-106">It is used to reserve a section of URL namespace for a user account or register a section of URL namespace for a process.</span></span>

## <a name="urlprefix-format"></a><span data-ttu-id="62e8a-107">Formato UrlPrefix</span><span class="sxs-lookup"><span data-stu-id="62e8a-107">UrlPrefix Format</span></span>

<span data-ttu-id="62e8a-108">Un UrlPrefix tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="62e8a-108">A UrlPrefix has the following syntax:</span></span>

<span data-ttu-id="62e8a-109">"Scheme:on: Puerto/relativeURI"</span><span class="sxs-lookup"><span data-stu-id="62e8a-109">"scheme://host:port/relativeURI"</span></span>

<span data-ttu-id="62e8a-110">Los elementos de esquema, host y puerto de un UrlPrefix deben estar presentes y no estar vacíos, y deben cumplir las reglas siguientes:</span><span class="sxs-lookup"><span data-stu-id="62e8a-110">The scheme, host and port elements of a UrlPrefix must be present and non-empty, and must obey the following rules:</span></span>

<dl> <dt>

<span data-ttu-id="62e8a-111"><span id="scheme"></span><span id="SCHEME"></span>regímenes</span><span class="sxs-lookup"><span data-stu-id="62e8a-111"><span id="scheme"></span><span id="SCHEME"></span>scheme</span></span>
</dt> <dd>

<span data-ttu-id="62e8a-112">Debe ser http o https, todo en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="62e8a-112">Must be either http or https, all in lowercase.</span></span>

</dd> <dt>

<span data-ttu-id="62e8a-113"><span id="host"></span><span id="HOST"></span>organizar</span><span class="sxs-lookup"><span data-stu-id="62e8a-113"><span id="host"></span><span id="HOST"></span>host</span></span>
</dt> <dd>

<span data-ttu-id="62e8a-114">Debe ser un nombre de dominio completo, una cadena literal IPv4 o IPv6 o un carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="62e8a-114">Must be a fully qualified domain name, an IPv4 or IPv6 literal string, or a wildcard.</span></span> <span data-ttu-id="62e8a-115">A diferencia del esquema, que debe estar en minúsculas, la parte del host no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="62e8a-115">Unlike the scheme, which must be lowercase, the host portion is case-insensitive.</span></span> <span data-ttu-id="62e8a-116">En función de cómo se especifique su parte de host, una UrlPrefix se encuentra en una de las cuatro categorías de enrutamiento siguientes, que se describen con más detalle a continuación:</span><span class="sxs-lookup"><span data-stu-id="62e8a-116">Depending on how its host portion is specified, a UrlPrefix falls into one of the following four routing categories, which are described in more detail below:</span></span>

<dl> <dd><span data-ttu-id="62e8a-117">Carácter comodín seguro</span><span class="sxs-lookup"><span data-stu-id="62e8a-117">Strong wildcard</span></span></dd> <dd><span data-ttu-id="62e8a-118">Explícita</span><span class="sxs-lookup"><span data-stu-id="62e8a-118">Explicit</span></span></dd> <dd><span data-ttu-id="62e8a-119">Carácter comodín débil enlazado a IP</span><span class="sxs-lookup"><span data-stu-id="62e8a-119">IP-bound weak wildcard</span></span></dd> <dd><span data-ttu-id="62e8a-120">Carácter comodín débil</span><span class="sxs-lookup"><span data-stu-id="62e8a-120">Weak wildcard</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="62e8a-121"><span id="port"></span><span id="PORT"></span>casilla</span><span class="sxs-lookup"><span data-stu-id="62e8a-121"><span id="port"></span><span id="PORT"></span>port</span></span>
</dt> <dd>

<span data-ttu-id="62e8a-122">Cadena numérica decimal que no comienza por cero y que representa un número de puerto TCP válido (de 1 a 65.535).</span><span class="sxs-lookup"><span data-stu-id="62e8a-122">A decimal numeric string that does not start with zero and that represents a valid TCP port number (1 to 65,535).</span></span> <span data-ttu-id="62e8a-123">Este valor no puede ser un carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="62e8a-123">This value cannot be a wildcard.</span></span>

</dd> <dt>

<span data-ttu-id="62e8a-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span><span class="sxs-lookup"><span data-stu-id="62e8a-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span></span>
</dt> <dd>

<span data-ttu-id="62e8a-125">El elemento relativeURI es opcional, pero si está presente siempre debe ir seguido de un carácter de barra diagonal ("/").</span><span class="sxs-lookup"><span data-stu-id="62e8a-125">The relativeURI element is optional, but if present must always be followed by a slash character ("/").</span></span> <span data-ttu-id="62e8a-126">Se trata de una cadena de prefijo que indica un subárbol dentro del espacio de nombres de la máquina especificado en relación con los valores de esquema, host y puerto.</span><span class="sxs-lookup"><span data-stu-id="62e8a-126">This is a prefix string that indicates a subtree within the machine's namespace specified relative to the scheme, host and port values.</span></span> <span data-ttu-id="62e8a-127">A diferencia del esquema, que debe estar en minúsculas, la parte del relativeURI no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="62e8a-127">Unlike the scheme, which must be lowercase, the relativeURI portion is case-insensitive.</span></span>

</dd> </dl>

<span data-ttu-id="62e8a-128">Ejemplos de UrlPrefixes con formato correcto:</span><span class="sxs-lookup"><span data-stu-id="62e8a-128">Examples of properly formed UrlPrefixes are:</span></span>

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a><span data-ttu-id="62e8a-129">Host-Specifier categorías</span><span class="sxs-lookup"><span data-stu-id="62e8a-129">Host-Specifier Categories</span></span>

<span data-ttu-id="62e8a-130">Para ofrecer flexibilidad y facilidad de uso, la API del servidor HTTP admite cuatro maneras diferentes de especificar hosts.</span><span class="sxs-lookup"><span data-stu-id="62e8a-130">For flexibility and ease of use, the HTTP Server API supports four different ways to specify hosts.</span></span> <span data-ttu-id="62e8a-131">Las cuatro categorías de especificador de host se enumeran a continuación en orden de prioridad:</span><span class="sxs-lookup"><span data-stu-id="62e8a-131">The four host-specifier categories are listed below in order of precedence:</span></span>

<dl> <dt>

<span data-ttu-id="62e8a-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Carácter comodín seguro (signo más)</span><span class="sxs-lookup"><span data-stu-id="62e8a-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Strong wildcard (Plus Sign)</span></span>
</dt> <dd>

<span data-ttu-id="62e8a-133">Cuando el elemento host de un UrlPrefix consta de un signo más (+), el UrlPrefix coincide con todos los nombres de host posibles en el contexto de su esquema, los elementos Port y relativeURI y entra en la categoría de caracteres comodín seguros.</span><span class="sxs-lookup"><span data-stu-id="62e8a-133">When the host element of a UrlPrefix consists of a single plus sign (+), the UrlPrefix matches all possible host names in the context of its scheme, port and relativeURI elements, and falls into the strong wildcard category.</span></span>

<span data-ttu-id="62e8a-134">Un carácter comodín seguro es útil cuando una aplicación necesita atender solicitudes dirigidas a una o más relativeURIs, independientemente de cómo lleguen esas solicitudes en el equipo o qué sitio especifiquen en sus encabezados de host.</span><span class="sxs-lookup"><span data-stu-id="62e8a-134">A strong wildcard is useful when an application needs to serve requests addressed to one or more relativeURIs, regardless of how those requests arrive on the machine or what site they specify in their Host headers.</span></span> <span data-ttu-id="62e8a-135">El uso de un carácter comodín fuerte en esta situación evita la necesidad de especificar una lista exhaustiva de hosts o direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="62e8a-135">Use of a strong wildcard in this situation avoids the need to specify an exhaustive list of host and/or IP-addresses.</span></span>

</dd> <dt>

<span data-ttu-id="62e8a-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explícita</span><span class="sxs-lookup"><span data-stu-id="62e8a-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explicit</span></span>
</dt> <dd>

<span data-ttu-id="62e8a-137">Un nombre de host explícito, como un nombre de dominio completo en el elemento host, coloca un UrlPrefix en la categoría Explicit.</span><span class="sxs-lookup"><span data-stu-id="62e8a-137">An explicit host name such as a fully qualified domain name in the host element places a UrlPrefix in the explicit category.</span></span> <span data-ttu-id="62e8a-138">Este tipo de elemento host coincide directamente con los encabezados de host de las solicitudes entrantes.</span><span class="sxs-lookup"><span data-stu-id="62e8a-138">This kind of host element is matched directly against the Host headers of incoming requests.</span></span>

<span data-ttu-id="62e8a-139">Las especificaciones de host explícitas son útiles para las aplicaciones de varios sitios, como los servidores web que proporcionan contenido diferente en función del sitio al que se dirigió la solicitud.</span><span class="sxs-lookup"><span data-stu-id="62e8a-139">Explicit host specifications are useful for multi-site applications such as Web servers that deliver different content depending on the site to which the request was directed.</span></span>

</dd> <dt>

<span data-ttu-id="62e8a-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>Carácter comodín débil enlazado a IP</span><span class="sxs-lookup"><span data-stu-id="62e8a-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>IP-bound weak wildcard</span></span>
</dt> <dd>

<span data-ttu-id="62e8a-141">Cuando una dirección IP aparece como el elemento host, el UrlPrefix se encuentra en la categoría de carácter comodín débil de IP enlazada.</span><span class="sxs-lookup"><span data-stu-id="62e8a-141">When an IP address appears as the host element, then the UrlPrefix falls into the IP-bound Weak Wildcard category.</span></span> <span data-ttu-id="62e8a-142">Este tipo de UrlPrefix coincide con cualquier nombre de host para la interfaz IP especificada con el esquema especificado, el puerto y el relativeURI, y que aún no coincide con un carácter comodín seguro o un UrlPrefix explícito.</span><span class="sxs-lookup"><span data-stu-id="62e8a-142">This kind of UrlPrefix matches any host name for the specified IP interface with the specified scheme, port and relativeURI, and that has not already been matched by a strong-wildcard or explicit UrlPrefix.</span></span> <span data-ttu-id="62e8a-143">La dirección IP adopta una de dos formas en el elemento host:</span><span class="sxs-lookup"><span data-stu-id="62e8a-143">The IP address takes one of two forms in the host element:</span></span>

<dl> <dt>

<span data-ttu-id="62e8a-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>Cadena literal IPv4</span><span class="sxs-lookup"><span data-stu-id="62e8a-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>IPv4 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="62e8a-145">Un literal IPv4 consta de cuatro números decimales con puntos, cada uno en el intervalo 0-255, como 192.168.0.0.</span><span class="sxs-lookup"><span data-stu-id="62e8a-145">An IPv4 literal consists of four dotted decimal numbers, each in the range 0-255, such as 192.168.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="62e8a-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>Cadena literal IPv6</span><span class="sxs-lookup"><span data-stu-id="62e8a-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>IPv6 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="62e8a-147">Una cadena literal IPv6 está entre corchetes y contiene números hexadecimales separados por dos puntos. por ejemplo: \[ :: 1 \] o \[ 3ffe: ffff:: 6ECB: 0101 \] .</span><span class="sxs-lookup"><span data-stu-id="62e8a-147">An IPv6 literal string is enclosed in square brackets and contains hex numbers separated by colons; for example: \[::1\] or \[3ffe:ffff::6ECB:0101\].</span></span>

</dd> </dl>

<span data-ttu-id="62e8a-148">Los especificadores de host de comodín no seguros con enlace IP están diseñados para aplicaciones que varían el contenido que sirven en función de la ruta tomada por las solicitudes entrantes.</span><span class="sxs-lookup"><span data-stu-id="62e8a-148">IP-bound weak-wildcard host specifiers are intended for applications that vary the content they serve based on the route taken by incoming requests.</span></span> <span data-ttu-id="62e8a-149">No se base en especificadores de host de comodín sin comodín enlazados a IP para aplicar la seguridad.</span><span class="sxs-lookup"><span data-stu-id="62e8a-149">Do not rely on IP-bound weak-wildcard host specifiers to enforce security.</span></span>

</dd> <dt>

<span data-ttu-id="62e8a-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Carácter comodín no seguro (asterisco)</span><span class="sxs-lookup"><span data-stu-id="62e8a-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Weak wildcard (asterisk)</span></span>
</dt> <dd>

<span data-ttu-id="62e8a-151">Cuando un asterisco ( \* ) aparece como el elemento host, el UrlPrefix se encuentra en la categoría de caracteres comodín débiles.</span><span class="sxs-lookup"><span data-stu-id="62e8a-151">When an asterisk (\*) appears as the host element, then the UrlPrefix falls into the weak wildcard category.</span></span> <span data-ttu-id="62e8a-152">Este tipo de UrlPrefix coincide con cualquier nombre de host asociado con el esquema especificado, el puerto y el objeto relativeURI que no ha coincidido con un UrlPrefix de comodín débil, explícito o enlazado con IP.</span><span class="sxs-lookup"><span data-stu-id="62e8a-152">This kind of UrlPrefix matches any host name associated with the specified scheme, port and relativeURI that has not already been matched by a strong-wildcard, explicit, or IP-bound weak-wildcard UrlPrefix.</span></span>

<span data-ttu-id="62e8a-153">Esta especificación de host se puede usar como una instrucción Catch predeterminada en algunas circunstancias, o bien se puede usar para especificar una sección grande del espacio de nombres de la dirección URL sin tener que usar muchos UrlPrefixes.</span><span class="sxs-lookup"><span data-stu-id="62e8a-153">This host specification can be used as a default catch-all in some circumstances, or can be used to specify a large section of URL namespace without having to use many UrlPrefixes.</span></span>

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a><span data-ttu-id="62e8a-154">Detección de conflictos de UrlPrefix durante la reserva y el registro</span><span class="sxs-lookup"><span data-stu-id="62e8a-154">UrlPrefix Conflict Detection During Reservation and Registration</span></span>

<span data-ttu-id="62e8a-155">En lo que respecta a la reserva y el registro, las cuatro categorías diferentes de UrlPrefix se tratan por separado, sin ninguna referencia entre sí.</span><span class="sxs-lookup"><span data-stu-id="62e8a-155">For reservation and registration purposes, the four different categories of UrlPrefix are treated separately, without reference to one another.</span></span> <span data-ttu-id="62e8a-156">Es posible registrar UrlPrefixes en conflicto, siempre y cuando se encuentren en distintas categorías.</span><span class="sxs-lookup"><span data-stu-id="62e8a-156">It is possible to register conflicting UrlPrefixes as long as they are in different categories.</span></span> <span data-ttu-id="62e8a-157">Solo dentro de la misma categoría se produce un conflicto, lo que provoca un error de un intento de reserva.</span><span class="sxs-lookup"><span data-stu-id="62e8a-157">Only within the same category does a conflict cause a reservation attempt to fail.</span></span>

<span data-ttu-id="62e8a-158">Por ejemplo, sería posible reservar el UrlPrefix explícito `https://www.adatum.com:80/vroot/` y el UrlPrefix de comodín seguro `https://+:80/vroot/` en conflicto, ya que pertenecen a distintas categorías.</span><span class="sxs-lookup"><span data-stu-id="62e8a-158">For example, it would be possible to reserve both the explicit UrlPrefix `https://www.adatum.com:80/vroot/` and the conflicting strong wildcard UrlPrefix `https://+:80/vroot/`, since they belong to different categories.</span></span> <span data-ttu-id="62e8a-159">Sin embargo, un intento posterior de reserva https://+:80/vroot/ para un usuario diferente produciría un error porque entraría en conflicto con una reserva existente en su propia categoría.</span><span class="sxs-lookup"><span data-stu-id="62e8a-159">However, a subsequent attempt to reserve https://+:80/vroot/ to a different user would fail because it would conflict with an existing reservation in its own category.</span></span>

## <a name="routing-behavior"></a><span data-ttu-id="62e8a-160">Comportamiento del enrutamiento</span><span class="sxs-lookup"><span data-stu-id="62e8a-160">Routing Behavior</span></span>

<span data-ttu-id="62e8a-161">Al enrutar una solicitud HTTP entrante, la API del servidor HTTP se inicia con la categoría de caracteres comodín seguros y compara la dirección URL entrante con los UrlPrefixes registrados y reservados de esa categoría.</span><span class="sxs-lookup"><span data-stu-id="62e8a-161">When routing an incoming HTTP request, the HTTP Server API starts with the strong wildcard category and compares the incoming URL with both registered and reserved UrlPrefixes in that category.</span></span>

<span data-ttu-id="62e8a-162">Si la dirección URL de entrada coincide con una reserva pero no con un registro, la API del servidor HTTP produce un error en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="62e8a-162">If the incoming URL matches a reservation but not a registration, the HTTP Server API fails the request.</span></span> <span data-ttu-id="62e8a-163">De esta forma, se evita que los registros de menor prioridad puedan recoger las solicitudes que no se pretenden.</span><span class="sxs-lookup"><span data-stu-id="62e8a-163">This prevents a lower-priority registrations from being able to pick up requests not intended for it.</span></span> <span data-ttu-id="62e8a-164">El estado en caso de error es 400 ("solicitud incorrecta") en lugar de 503 ("servicio no disponible"), porque las puertas de enlace de equilibrio de carga en ocasiones interpretan erróneamente una devolución de 503 como indica que el servidor está sobrecargado.</span><span class="sxs-lookup"><span data-stu-id="62e8a-164">The status on failure is 400 ("Bad Request") rather than 503 ("Service not available"), because a 503 return is sometimes mistakenly interpreted by load-balancing gateways as indicating that the server was overloaded.</span></span>

<span data-ttu-id="62e8a-165">Si se encuentra un registro coincidente dentro de la categoría, la solicitud se enruta a la cola de solicitudes asociada a ese registro.</span><span class="sxs-lookup"><span data-stu-id="62e8a-165">If a matching registration is found within the category, the request is routed to the request queue associated with that registration.</span></span> <span data-ttu-id="62e8a-166">La solicitud siempre se enruta a la cola asociada a la UrlPrefix coincidente más larga dentro de una categoría.</span><span class="sxs-lookup"><span data-stu-id="62e8a-166">The request is always routed to the queue associated with the longest matching UrlPrefix within a category.</span></span>

<span data-ttu-id="62e8a-167">Si no se encuentra ninguna coincidencia en la categoría, la API del servidor HTTP continúa con la categoría explícita y repite el mismo procedimiento.</span><span class="sxs-lookup"><span data-stu-id="62e8a-167">If no match is found in the category, then the HTTP Server API proceeds to the explicit category and repeats the same procedure.</span></span> <span data-ttu-id="62e8a-168">En Resumen, el orden en el que se examinan las categorías es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="62e8a-168">To summarize, the order in which the categories are examined is as follows:</span></span>

1.  <span data-ttu-id="62e8a-169">Carácter comodín seguro</span><span class="sxs-lookup"><span data-stu-id="62e8a-169">Strong wildcard</span></span>
2.  <span data-ttu-id="62e8a-170">Explícita</span><span class="sxs-lookup"><span data-stu-id="62e8a-170">Explicit</span></span>
3.  <span data-ttu-id="62e8a-171">IP-Bound carácter comodín débil</span><span class="sxs-lookup"><span data-stu-id="62e8a-171">IP-Bound weak wildcard</span></span>
4.  <span data-ttu-id="62e8a-172">Carácter comodín débil</span><span class="sxs-lookup"><span data-stu-id="62e8a-172">Weak wildcard</span></span>

<span data-ttu-id="62e8a-173">Si no se encuentra ninguna coincidencia en ninguna de las categorías, la API del servidor HTTP envía una respuesta con un código de estado 400 para indicar que no se puede enrutar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="62e8a-173">If no match is found in any of the categories, the HTTP Server API sends a response with a status code of 400 to indicate that the request cannot be routed.</span></span>

## <a name="longest-match-rule"></a><span data-ttu-id="62e8a-174">Regla de coincidencia más larga</span><span class="sxs-lookup"><span data-stu-id="62e8a-174">Longest Match Rule</span></span>

<span data-ttu-id="62e8a-175">Dentro de cada categoría UrlPrefix, la API del servidor HTTP enruta una solicitud a la cola asociada a la UrlPrefix coincidente más larga.</span><span class="sxs-lookup"><span data-stu-id="62e8a-175">Within each UrlPrefix category, HTTP Server API routes a request to the queue associated with the longest matching UrlPrefix.</span></span> <span data-ttu-id="62e8a-176">Por ejemplo, supongamos que los dos UrlPrefixes siguientes se registran en diferentes colas:</span><span class="sxs-lookup"><span data-stu-id="62e8a-176">For example, suppose the following two UrlPrefixes are registered to different queues:</span></span>

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

<span data-ttu-id="62e8a-177">La API del servidor HTTP enruta una solicitud de `https://www.adatum.com:80/default.htm` a Queue1 y una solicitud para `https://www.adatum.com:80/dir/sna/snadefault.htm` a Queue2.</span><span class="sxs-lookup"><span data-stu-id="62e8a-177">The HTTP Server API routes a request for `https://www.adatum.com:80/default.htm` to Queue1, and a request for `https://www.adatum.com:80/dir/sna/snadefault.htm` to Queue2.</span></span> <span data-ttu-id="62e8a-178">Enruta una solicitud de `https://www.adatum.com:80/dir/app.htm` a Queue1 porque la coincidencia completa más larga es con `https://www.adatum.com:80/` UrlPrefix, no con `https://www.adatum.com:80/dir/sna` UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="62e8a-178">It routes a request for `https://www.adatum.com:80/dir/app.htm` to Queue1 because the longest complete match is with the `https://www.adatum.com:80/` UrlPrefix, not with the `https://www.adatum.com:80/dir/sna` UrlPrefix.</span></span>

 

 




