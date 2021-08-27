---
title: Cadenas de UrlPrefix
description: En la API del servidor HTTP, urlPrefix es una cadena Unicode de caracteres anchos (UTF-16) con un formato canónico que especifica una sección del espacio de nombres de dirección URL.
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- UrlPrefix strings HTTP Server API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fad89bf7abd52ee3681beaa8069a7f5e4ee25b482cd065f880263852690fce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047045"
---
# <a name="urlprefix-strings"></a>Cadenas de UrlPrefix

En la API del servidor HTTP, *urlPrefix* es una cadena Unicode de caracteres anchos (UTF-16) con un formato canónico que especifica una sección del espacio de nombres de dirección URL. Se usa para reservar una sección de espacio de nombres de dirección URL para una cuenta de usuario o registrar una sección del espacio de nombres de dirección URL para un proceso.

## <a name="urlprefix-format"></a>Formato UrlPrefix

UrlPrefix tiene la sintaxis siguiente:

"scheme://host:port/relativeURI"

Los elementos de esquema, host y puerto de urlPrefix deben estar presentes y no vacíos, y deben cumplir las reglas siguientes:

<dl> <dt>

<span id="scheme"></span><span id="SCHEME"></span>Esquema
</dt> <dd>

Debe ser http o https, todo en minúsculas.

</dd> <dt>

<span id="host"></span><span id="HOST"></span>Host
</dt> <dd>

Debe ser un nombre de dominio completo, una cadena literal IPv4 o IPv6 o un carácter comodín. A diferencia del esquema, que debe estar en minúsculas, la parte del host no tiene en cuenta las mayúsculas y minúsculas. En función de cómo se especifique su parte del host, una urlPrefix se divide en una de las cuatro categorías de enrutamiento siguientes, que se describen con más detalle a continuación:

<dl> <dd>Carácter comodín fuerte</dd> <dd>Explícita</dd> <dd>Carácter comodín débil enlazado a IP</dd> <dd>Carácter comodín débil</dd> </dl> </dd> <dt>

<span id="port"></span><span id="PORT"></span>Puerto
</dt> <dd>

Cadena numérica decimal que no empieza por cero y que representa un número de puerto TCP válido (de 1 a 65 535). Este valor no puede ser un carácter comodín.

</dd> <dt>

<span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI
</dt> <dd>

El elemento relativeURI es opcional, pero si está presente siempre debe ir seguido de un carácter de barra diagonal ("/"). Se trata de una cadena de prefijo que indica un subárbol dentro del espacio de nombres de la máquina especificado en relación con los valores de esquema, host y puerto. A diferencia del esquema, que debe estar en minúsculas, la parte relativeURI no tiene en cuenta las mayúsculas y minúsculas.

</dd> </dl>

Algunos ejemplos de urlPrefixes con el formato correcto son:

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a>Host-Specifier categorías

Para mayor flexibilidad y facilidad de uso, la API del servidor HTTP admite cuatro maneras diferentes de especificar hosts. Las cuatro categorías de especificador de host se enumeran a continuación en orden de prioridad:

<dl> <dt>

<span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Carácter comodín fuerte (signo más)
</dt> <dd>

Cuando el elemento host de una urlPrefix consta de un único signo más (+), UrlPrefix coincide con todos los nombres de host posibles en el contexto de su esquema, puerto y elementos relativeURI, y entra en la categoría de caracteres comodín seguro.

Un carácter comodín fuerte es útil cuando una aplicación necesita atender solicitudes dirigidas a uno o varios relativeURIs, independientemente de cómo lleguen esas solicitudes a la máquina o del sitio que especifiquen en sus encabezados host. El uso de un carácter comodín fuerte en esta situación evita la necesidad de especificar una lista exhaustiva de direcciones IP o host.

</dd> <dt>

<span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explícito
</dt> <dd>

Un nombre de host explícito, como un nombre de dominio completo en el elemento host, coloca una dirección UrlPrefix en la categoría explícita. Este tipo de elemento host se compara directamente con los encabezados host de las solicitudes entrantes.

Las especificaciones de host explícitas son útiles para aplicaciones de varios sitios, como servidores web que entregan contenido diferente en función del sitio al que se dirige la solicitud.

</dd> <dt>

<span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>Carácter comodín débil enlazado a IP
</dt> <dd>

Cuando una dirección IP aparece como el elemento host, UrlPrefix entra en la categoría Carácter comodín débil enlazado a IP. Este tipo de UrlPrefix coincide con cualquier nombre de host de la interfaz IP especificada con el esquema, el puerto y relativeURI especificados, y que aún no ha coincidido con un carácter comodín seguro o urlPrefix explícito. La dirección IP toma una de estas dos formas en el elemento host:

<dl> <dt>

<span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>Cadena literal IPv4
</dt> <dd>

Un literal IPv4 consta de cuatro números decimales de puntos, cada uno en el intervalo 0-255, como 192.168.0.0.

</dd> <dt>

<span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>Cadena literal IPv6
</dt> <dd>

Una cadena literal IPv6 se incluye entre corchetes y contiene números hexadecimales separados por dos puntos; por ejemplo: \[ ::1 \] o \[ 3ffe:ffff::6ECB:0101 \] .

</dd> </dl>

Los especificadores de host con caracteres comodín débiles enlazados a IP están diseñados para aplicaciones que varían el contenido que sirven en función de la ruta realizada por las solicitudes entrantes. No se base en especificadores de host con caracteres comodín débiles enlazados a IP para aplicar la seguridad.

</dd> <dt>

<span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Carácter comodín débil (asterisco)
</dt> <dd>

Cuando aparece un asterisco ( \* ) como elemento host, UrlPrefix entra en la categoría de caracteres comodín débiles. Este tipo de UrlPrefix coincide con cualquier nombre de host asociado al esquema, puerto y relativeURI especificados que aún no hayan coincidido con un urlPrefix con caracteres comodín seguro, explícito o con caracteres comodín débiles enlazados a IP.

Esta especificación de host se puede usar como un punto de conexión predeterminado en algunas circunstancias, o se puede usar para especificar una sección grande del espacio de nombres de dirección URL sin tener que usar muchos UrlPrefixes.

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a>Detección de conflictos de UrlPrefix durante la reserva y el registro

Con fines de reserva y registro, las cuatro categorías diferentes de UrlPrefix se tratan por separado, sin hacer referencia entre sí. Es posible registrar urlPrefixes en conflicto siempre que estén en categorías diferentes. Solo dentro de la misma categoría, un conflicto provoca un error en un intento de reserva.

Por ejemplo, sería posible reservar tanto urlprefix explícito como el carácter comodín fuerte en conflicto UrlPrefix , ya que pertenecen `https://www.adatum.com:80/vroot/` `https://+:80/vroot/` a distintas categorías. Sin embargo, se produciría un error en un intento posterior de reserva a otro usuario porque entraba en conflicto con una https://+:80/vroot/ reserva existente en su propia categoría.

## <a name="routing-behavior"></a>Comportamiento de enrutamiento

Al enrutar una solicitud HTTP entrante, la API del servidor HTTP comienza con la categoría de caracteres comodín seguro y compara la dirección URL entrante con urlprefijos registrados y reservados en esa categoría.

Si la dirección URL entrante coincide con una reserva, pero no con un registro, la API del servidor HTTP produce un error en la solicitud. Esto evita que los registros de prioridad inferior puedan recoger las solicitudes que no están pensadas para él. El estado en caso de error es 400 ("Solicitud no correcta") en lugar de 503 ("Servicio no disponible"), porque una devolución 503 a veces se interpreta erróneamente por las puertas de enlace de equilibrio de carga como que indica que el servidor estaba sobrecargado.

Si se encuentra un registro correspondiente dentro de la categoría , la solicitud se enruta a la cola de solicitudes asociada a ese registro. La solicitud siempre se enruta a la cola asociada con la urlPrefix que coincida más tiempo dentro de una categoría.

Si no se encuentra ninguna coincidencia en la categoría, la API del servidor HTTP continúa a la categoría explícita y repite el mismo procedimiento. En resumen, el orden en el que se examinan las categorías es el siguiente:

1.  Carácter comodín fuerte
2.  Explícita
3.  IP-Bound carácter comodín débil
4.  Carácter comodín débil

Si no se encuentra ninguna coincidencia en ninguna de las categorías, la API del servidor HTTP envía una respuesta con un código de estado 400 para indicar que no se puede enrutar la solicitud.

## <a name="longest-match-rule"></a>Regla de coincidencia más larga

Dentro de cada categoría UrlPrefix, la API del servidor HTTP enruta una solicitud a la cola asociada con la urlPrefix que coincida más tiempo. Por ejemplo, supongamos que los dos UrlPrefixes siguientes están registrados en colas diferentes:

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

La API del servidor HTTP enruta una solicitud de `https://www.adatum.com:80/default.htm` a Queue1 y una solicitud de a `https://www.adatum.com:80/dir/sna/snadefault.htm` Queue2. Enruta una solicitud de a Queue1 porque la coincidencia completa más larga es con `https://www.adatum.com:80/dir/app.htm` `https://www.adatum.com:80/` UrlPrefix, no con `https://www.adatum.com:80/dir/sna` UrlPrefix.

 

 




