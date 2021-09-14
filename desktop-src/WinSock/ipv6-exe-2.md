---
description: Toda la configuración de IPv6 se realiza con Ipv6.exe herramienta.
ms.assetid: cb701070-cb7f-472a-97c7-1de9c0ddec0f
title: Ipv6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e6fb0266609d22116cc72151e0db26006c415a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174913"
---
# <a name="ipv6exe"></a>Ipv6.exe

Toda la configuración de IPv6 se realiza con Ipv6.exe herramienta. Esta herramienta se usa principalmente para consultar y configurar interfaces, direcciones, cachés y rutas IPv6. Estos son los subcomandos IPv6:

<dl> <dt>

<span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**ipv6 si** \[ Si\#\]
</dt> <dd>

Muestra información sobre las interfaces. Si se especifica un número de interfaz, solo se muestra información sobre esa interfaz. De lo contrario, se muestra información sobre todas las interfaces. La salida incluye la dirección del nivel de vínculo de la interfaz y la lista de direcciones IPv6 asignadas a la interfaz, incluida la MTU actual de la interfaz y la MTU máxima (true) que la interfaz puede admitir.

La \# interfaz 1 es una pseudo interface que se usa para el bucleback. La interfaz 2 es una pseudo interface que se usa para la tunelización configurada, la tunelización automática y la \# tunelización 6to4. Otras interfaces se numeran secuencialmente en el orden en que se crean. Este orden varía de un equipo a otro.

Las direcciones de capa de vínculo en *formato aa* - *bb* - *cc* - *dd* - *ee* - *ff* son direcciones Ethernet. Dirección de la capa de vínculo *en un*. *b*. *c*. *d* form son interfaces de 6 sobre 4. Para obtener más información sobre 6 sobre 4, vea RFC 2529.

Las dos pseudo interfaces no usan la detección de vecino IPv6.

</dd> <dt>

<span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**ipv6 ifc** \# \[ ifs \] \[ advertises \] \[ -forwards \] \[ -advertises \] \[ mtu \# bytes \] \[ site-identifier\]
</dt> <dd>

Controla los atributos de interfaz. Las interfaces pueden reenviarse, en cuyo caso reenvía paquetes con direcciones de destino no asignadas a la interfaz. Las interfaces pueden ser publicidad, en cuyo caso envían anuncios de enrutador. Estos atributos se pueden controlar de forma independiente. Una interfaz envía solicitudes de enrutador y recibe anuncios de enrutador, o bien recibe solicitudes de enrutador y envía anuncios de enrutador.

Dado que las dos pseudo interfaces no usan la detección de vecinos, no se pueden configurar para enviar anuncios de enrutador.

Los reenvíos se pueden abreviar como forw y anunciarse como adv.

También se puede establecer la MTU de la interfaz. La nueva MTU debe ser menor o igual que la MTU máxima (true) del vínculo (como se notifica en ipv6 si) y mayor o igual que la MTU de IPv6 mínima (1280 bytes).

También se puede cambiar el identificador de sitio de una interfaz. Los identificadores de sitio se usan en el campo id. de ámbito sin6 \_ con direcciones locales del \_ sitio.

</dd> <dt>

<span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**ifd de ipv6** si\#
</dt> <dd>

Elimina una interfaz. No se pueden eliminar las pseudo interfaces de bucleback y túnel.

</dd> <dt>

<span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**ipv6 nc** \[ if \# \[ address\]\]
</dt> <dd>

Muestra el contenido de la caché del vecino. Si se especifica un número de interfaz, solo se muestra el contenido de la caché de vecino de esa interfaz. De lo contrario, se muestra el contenido de todas las memorias caché de vecinos de la interfaz. Si se especifica una interfaz, se puede especificar una dirección IPv6 para mostrar solo esa entrada de caché de vecino.

Para cada entrada de caché de vecino, se muestran la interfaz, la dirección IPv6, la dirección de la capa de vínculo y el estado de alcance.

</dd> <dt>

<span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**ipv6 ncf** \[ if \# \[ address\]\]
</dt> <dd>

Vacía las entradas de caché de vecino especificadas. Solo se purgan las entradas de caché de vecino sin referencias. Dado que las entradas de la caché de rutas incluyen referencias a entradas de caché vecinos, la caché de rutas debe vaciarse primero. Las entradas de tabla de enrutamiento también pueden contener referencias a entradas de caché de vecino.

</dd> <dt>

<span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**ipv6 rc** \[ if \# address\]
</dt> <dd>

Muestra el contenido de la caché de rutas. La caché de rutas es el nombre de implementación de IPv6 de Microsoft para la caché de destino. Si se especifican una interfaz y una dirección, se muestra la entrada de la caché de rutas para llegar a la dirección a través de la interfaz. De lo contrario, se muestran todas las entradas de la caché de rutas.

Para cada entrada de la caché de rutas, se muestran la dirección IPv6 y la interfaz del próximo salto actual y la dirección del vecino. También se muestra la dirección de origen preferida para su uso con este destino, la ruta de acceso actual MTU para llegar a este destino a través de la interfaz y la determinación de si se trata de una entrada de caché específica de la interfaz o de ruta. También se muestra cualquier dirección de asistencia (para movilidad) para la dirección de destino.

Una dirección de destino puede tener varias entradas de caché de rutas, hasta una para cada interfaz saliente. Sin embargo, una dirección de destino puede tener un máximo de una entrada de caché de rutas que no sea específica de la interfaz. Solo se usa una entrada de caché específica de la interfaz de ruta si la aplicación especifica explícitamente esa interfaz saliente.

</dd> <dt>

<span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**ipv6 rcf** \[ if \# \[ address\]\]
</dt> <dd>

Vacía las entradas de la caché de rutas especificadas.

</dd> <dt>

<span id="ipv6_bc"></span><span id="IPV6_BC"></span>**ipv6 bc**
</dt> <dd>

Muestra el contenido de la caché de enlaces, que contiene enlaces entre las direcciones de inicio y las direcciones de asistencia para IPv6 móvil.

Para cada enlace, se muestran la dirección principal, la dirección de asistencia, el número de secuencia de enlace y la duración.

</dd> <dt>

<span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**ipv6 adu** if \# /address \[ lifetime VL \[ /PL \] \] \[ anycast \] \[ uncast\]
</dt> <dd>

Agrega o quita una asignación de dirección de unidifusión o cualquier difusión en una interfaz. Se actúa sobre la dirección de unidifusión a menos que se especifique anycast.

La duración es infinita si no se especifica. Si solo se especifica una duración válida, la duración preferida es igual a la duración válida. Se puede especificar una duración infinita o un valor finito en segundos. La duración preferida debe ser menor o igual que la duración válida. La especificación de una duración de cero hace que se quite la dirección.

Puede abreviar la duración como vida.

Para las direcciones anycast, los únicos valores de duración válidos son cero e infinitos.

</dd> <dt>

<span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**ipv6 spt**
</dt> <dd>

Muestra el contenido actual de la tabla de prefijos de sitio.

Para cada prefijo de sitio, el comando muestra el prefijo, la interfaz a la que se aplica el prefijo de sitio y la duración del prefijo en segundos.

Normalmente, los prefijos de sitio se configuran automáticamente a partir de anuncios de enrutador. Se usan en la [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) para filtrar direcciones locales de sitio inadecuados.

</dd> <dt>

<span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>**Prefijo spu de ipv6** si la \# \[ duración L\]
</dt> <dd>

Agrega, quita o actualiza un prefijo en la tabla de prefijos de sitio.

Se requieren el prefijo y el número de interfaz. La duración del prefijo de sitio, especificada en segundos, tiene como valor predeterminado infinito si no se especifica. Si se especifica una duración de cero, se elimina el prefijo del sitio.

Este comando no es necesario para la configuración normal de hosts o enrutadores.

</dd> <dt>

<span id="ipv6_rt"></span><span id="IPV6_RT"></span>**ipv6 rt**
</dt> <dd>

Muestra el contenido actual de la tabla de enrutamiento.

Para cada entrada de tabla de enrutamiento, el comando muestra el prefijo de ruta, una interfaz en el vínculo o un vecino del próximo salto en una interfaz, un valor de preferencia (se prefiere menor) y una duración en segundos.

Las entradas de tabla de enrutamiento también pueden tener **atributos** de publicación **y** de edad. De forma predeterminada, tienen una antigüedad (la duración se cuenta a la baja, en lugar de la constante restante) y no se publican (no se usan en la construcción de anuncios de enrutador).

En los hosts, las entradas de la tabla de enrutamiento normalmente se configuran automáticamente a partir de anuncios de enrutador.

</dd> <dt>

<span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>**Prefijo ipv6 ance** si \# \[ /nexthop \] \[ lifetime L preference P \] \[ publish age \] \[ \] \[ \] \[ spl site-prefix-length\]
</dt> <dd>

Agrega o quita una ruta en la tabla de enrutamiento. Se requiere el prefijo de ruta. El prefijo puede estar en el vínculo a una interfaz especificada, o próximo salto, especificado con una dirección de vecino en una interfaz. La ruta puede tener una duración en segundos, con el valor predeterminado infinito y una preferencia, con el valor predeterminado cero o el más preferido. Si se especifica una duración de cero, se elimina la ruta.

Si la ruta se especifica como publicada, lo que indica que se usará en la construcción de anuncios de enrutador, no tiene antigüedad. La duración de la ruta no se cuenta y, por tanto, es infinita de forma eficaz, pero el valor se usa en los anuncios de enrutador. Opcionalmente, se puede especificar una ruta como una ruta publicada que también sea de edad. De forma predeterminada, una ruta no publicada siempre tiene una edad.

La subopción spl opcional se puede usar para especificar una longitud de prefijo de sitio asociada a la ruta. La longitud del prefijo de sitio solo se usa al enviar anuncios de enrutador.

La duración se puede abreviar como vida, preferencia como valor previo y publicar como pub.

</dd> </dl>

 

 



