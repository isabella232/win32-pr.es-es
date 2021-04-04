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
# <a name="urlprefix-strings"></a>Cadenas de UrlPrefix

En la API del servidor HTTP, un *UrlPrefix* es una cadena Unicode de caracteres anchos (UTF-16) con una forma canónica que especifica una sección del espacio de nombres de la dirección URL. Se usa para reservar una sección del espacio de nombres de la dirección URL para una cuenta de usuario o para registrar una sección del espacio de nombres de la dirección URL para un proceso.

## <a name="urlprefix-format"></a>Formato UrlPrefix

Un UrlPrefix tiene la siguiente sintaxis:

"Scheme:on: Puerto/relativeURI"

Los elementos de esquema, host y puerto de un UrlPrefix deben estar presentes y no estar vacíos, y deben cumplir las reglas siguientes:

<dl> <dt>

<span id="scheme"></span><span id="SCHEME"></span>regímenes
</dt> <dd>

Debe ser http o https, todo en minúsculas.

</dd> <dt>

<span id="host"></span><span id="HOST"></span>organizar
</dt> <dd>

Debe ser un nombre de dominio completo, una cadena literal IPv4 o IPv6 o un carácter comodín. A diferencia del esquema, que debe estar en minúsculas, la parte del host no distingue mayúsculas de minúsculas. En función de cómo se especifique su parte de host, una UrlPrefix se encuentra en una de las cuatro categorías de enrutamiento siguientes, que se describen con más detalle a continuación:

<dl> <dd>Carácter comodín seguro</dd> <dd>Explícita</dd> <dd>Carácter comodín débil enlazado a IP</dd> <dd>Carácter comodín débil</dd> </dl> </dd> <dt>

<span id="port"></span><span id="PORT"></span>casilla
</dt> <dd>

Cadena numérica decimal que no comienza por cero y que representa un número de puerto TCP válido (de 1 a 65.535). Este valor no puede ser un carácter comodín.

</dd> <dt>

<span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI
</dt> <dd>

El elemento relativeURI es opcional, pero si está presente siempre debe ir seguido de un carácter de barra diagonal ("/"). Se trata de una cadena de prefijo que indica un subárbol dentro del espacio de nombres de la máquina especificado en relación con los valores de esquema, host y puerto. A diferencia del esquema, que debe estar en minúsculas, la parte del relativeURI no distingue entre mayúsculas y minúsculas.

</dd> </dl>

Ejemplos de UrlPrefixes con formato correcto:

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a>Host-Specifier categorías

Para ofrecer flexibilidad y facilidad de uso, la API del servidor HTTP admite cuatro maneras diferentes de especificar hosts. Las cuatro categorías de especificador de host se enumeran a continuación en orden de prioridad:

<dl> <dt>

<span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Carácter comodín seguro (signo más)
</dt> <dd>

Cuando el elemento host de un UrlPrefix consta de un signo más (+), el UrlPrefix coincide con todos los nombres de host posibles en el contexto de su esquema, los elementos Port y relativeURI y entra en la categoría de caracteres comodín seguros.

Un carácter comodín seguro es útil cuando una aplicación necesita atender solicitudes dirigidas a una o más relativeURIs, independientemente de cómo lleguen esas solicitudes en el equipo o qué sitio especifiquen en sus encabezados de host. El uso de un carácter comodín fuerte en esta situación evita la necesidad de especificar una lista exhaustiva de hosts o direcciones IP.

</dd> <dt>

<span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explícita
</dt> <dd>

Un nombre de host explícito, como un nombre de dominio completo en el elemento host, coloca un UrlPrefix en la categoría Explicit. Este tipo de elemento host coincide directamente con los encabezados de host de las solicitudes entrantes.

Las especificaciones de host explícitas son útiles para las aplicaciones de varios sitios, como los servidores web que proporcionan contenido diferente en función del sitio al que se dirigió la solicitud.

</dd> <dt>

<span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>Carácter comodín débil enlazado a IP
</dt> <dd>

Cuando una dirección IP aparece como el elemento host, el UrlPrefix se encuentra en la categoría de carácter comodín débil de IP enlazada. Este tipo de UrlPrefix coincide con cualquier nombre de host para la interfaz IP especificada con el esquema especificado, el puerto y el relativeURI, y que aún no coincide con un carácter comodín seguro o un UrlPrefix explícito. La dirección IP adopta una de dos formas en el elemento host:

<dl> <dt>

<span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>Cadena literal IPv4
</dt> <dd>

Un literal IPv4 consta de cuatro números decimales con puntos, cada uno en el intervalo 0-255, como 192.168.0.0.

</dd> <dt>

<span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>Cadena literal IPv6
</dt> <dd>

Una cadena literal IPv6 está entre corchetes y contiene números hexadecimales separados por dos puntos. por ejemplo: \[ :: 1 \] o \[ 3ffe: ffff:: 6ECB: 0101 \] .

</dd> </dl>

Los especificadores de host de comodín no seguros con enlace IP están diseñados para aplicaciones que varían el contenido que sirven en función de la ruta tomada por las solicitudes entrantes. No se base en especificadores de host de comodín sin comodín enlazados a IP para aplicar la seguridad.

</dd> <dt>

<span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Carácter comodín no seguro (asterisco)
</dt> <dd>

Cuando un asterisco ( \* ) aparece como el elemento host, el UrlPrefix se encuentra en la categoría de caracteres comodín débiles. Este tipo de UrlPrefix coincide con cualquier nombre de host asociado con el esquema especificado, el puerto y el objeto relativeURI que no ha coincidido con un UrlPrefix de comodín débil, explícito o enlazado con IP.

Esta especificación de host se puede usar como una instrucción Catch predeterminada en algunas circunstancias, o bien se puede usar para especificar una sección grande del espacio de nombres de la dirección URL sin tener que usar muchos UrlPrefixes.

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a>Detección de conflictos de UrlPrefix durante la reserva y el registro

En lo que respecta a la reserva y el registro, las cuatro categorías diferentes de UrlPrefix se tratan por separado, sin ninguna referencia entre sí. Es posible registrar UrlPrefixes en conflicto, siempre y cuando se encuentren en distintas categorías. Solo dentro de la misma categoría se produce un conflicto, lo que provoca un error de un intento de reserva.

Por ejemplo, sería posible reservar el UrlPrefix explícito `https://www.adatum.com:80/vroot/` y el UrlPrefix de comodín seguro `https://+:80/vroot/` en conflicto, ya que pertenecen a distintas categorías. Sin embargo, un intento posterior de reserva https://+:80/vroot/ para un usuario diferente produciría un error porque entraría en conflicto con una reserva existente en su propia categoría.

## <a name="routing-behavior"></a>Comportamiento del enrutamiento

Al enrutar una solicitud HTTP entrante, la API del servidor HTTP se inicia con la categoría de caracteres comodín seguros y compara la dirección URL entrante con los UrlPrefixes registrados y reservados de esa categoría.

Si la dirección URL de entrada coincide con una reserva pero no con un registro, la API del servidor HTTP produce un error en la solicitud. De esta forma, se evita que los registros de menor prioridad puedan recoger las solicitudes que no se pretenden. El estado en caso de error es 400 ("solicitud incorrecta") en lugar de 503 ("servicio no disponible"), porque las puertas de enlace de equilibrio de carga en ocasiones interpretan erróneamente una devolución de 503 como indica que el servidor está sobrecargado.

Si se encuentra un registro coincidente dentro de la categoría, la solicitud se enruta a la cola de solicitudes asociada a ese registro. La solicitud siempre se enruta a la cola asociada a la UrlPrefix coincidente más larga dentro de una categoría.

Si no se encuentra ninguna coincidencia en la categoría, la API del servidor HTTP continúa con la categoría explícita y repite el mismo procedimiento. En Resumen, el orden en el que se examinan las categorías es el siguiente:

1.  Carácter comodín seguro
2.  Explícita
3.  IP-Bound carácter comodín débil
4.  Carácter comodín débil

Si no se encuentra ninguna coincidencia en ninguna de las categorías, la API del servidor HTTP envía una respuesta con un código de estado 400 para indicar que no se puede enrutar la solicitud.

## <a name="longest-match-rule"></a>Regla de coincidencia más larga

Dentro de cada categoría UrlPrefix, la API del servidor HTTP enruta una solicitud a la cola asociada a la UrlPrefix coincidente más larga. Por ejemplo, supongamos que los dos UrlPrefixes siguientes se registran en diferentes colas:

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

La API del servidor HTTP enruta una solicitud de `https://www.adatum.com:80/default.htm` a Queue1 y una solicitud para `https://www.adatum.com:80/dir/sna/snadefault.htm` a Queue2. Enruta una solicitud de `https://www.adatum.com:80/dir/app.htm` a Queue1 porque la coincidencia completa más larga es con `https://www.adatum.com:80/` UrlPrefix, no con `https://www.adatum.com:80/dir/sna` UrlPrefix.

 

 




