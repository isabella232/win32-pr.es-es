---
description: Toda la configuración de IPv6 se realiza con la herramienta Ipv6.exe.
ms.assetid: cb701070-cb7f-472a-97c7-1de9c0ddec0f
title: Ipv6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e6fb0266609d22116cc72151e0db26006c415a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275396"
---
# <a name="ipv6exe"></a>Ipv6.exe

Toda la configuración de IPv6 se realiza con la herramienta Ipv6.exe. Esta herramienta se utiliza principalmente para la consulta y configuración de interfaces, direcciones, memorias caché y rutas de IPv6. A continuación se indican los subcomandos IPv6:

<dl> <dt>

<span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**IPv6 si** \[ Cuando\#\]
</dt> <dd>

Muestra información sobre las interfaces. Si se especifica un número de interfaz, solo se muestra información sobre esa interfaz. De lo contrario, se muestra información sobre todas las interfaces. La salida incluye la dirección de nivel de vínculo de la interfaz y la lista de direcciones IPv6 asignadas a la interfaz, incluida la MTU actual de la interfaz y la MTU máxima (true) que la interfaz puede admitir.

\#La interfaz 1 es una pseudo-interfaz que se usa para bucle invertido. \#La interfaz 2 es una pseudo-interfaz que se usa para la tunelización configurada, la tunelización automática y la tunelización 6to4. Otras interfaces se numeran secuencialmente en el orden en que se crean. Este orden varía de un equipo a otro.

Las direcciones de nivel de vínculo del formato *AA* - *BB* - *CC* - *DD* - *EE* - *FF* son direcciones Ethernet. Dirección de nivel de vínculo en *un*. *b*. *c*. el formulario *d* son entre 6 y 4 interfaces. Para obtener más información acerca de 6 a 4, consulte RFC 2529.

Las dos pseudo interfaces no usan la detección de vecinos IPv6.

</dd> <dt>

<span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**IPv6 IFC** si \# \[ reenvía \] \[ anunciaciones \] \[ -reenvíos \] \[ -anuncia \] \[ bytes MTU de sitio \# \] \[ -identificador\]
</dt> <dd>

Controla los atributos de la interfaz. Las interfaces se pueden reenviar, en cuyo caso reenvían paquetes con direcciones de destino no asignadas a la interfaz. Las interfaces se pueden anunciar, en cuyo caso envían anuncios de enrutador. Estos atributos se pueden controlar de forma independiente. Una interfaz envía solicitudes de enrutador y recibe anuncios de enrutador, o recibe solicitudes de enrutador y envía anuncios de enrutador.

Dado que las dos pseudo interfaces no usan la detección de vecinos, no se pueden configurar para enviar anuncios de enrutador.

Los reenvíos se pueden abreviar como forw y anunciarse como ADV.

También se puede establecer la MTU de la interfaz. La nueva MTU debe ser menor o igual que la MTU máxima (true) del vínculo (indicada por IPv6 si) y mayor o igual que la MTU de IPv6 mínima (1280 bytes).

También se puede cambiar el identificador de sitio de una interfaz. Los identificadores de sitio se utilizan en \_ el \_ campo ID. de ámbito sin6 con direcciones locales del sitio.

</dd> <dt>

<span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**IFD de IPv6** si\#
</dt> <dd>

Elimina una interfaz. Las pseudo-interfaces de bucle invertido y de túnel no se pueden eliminar.

</dd> <dt>

<span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**NC** \[ de IPv6 Si \# \[ dirección\]\]
</dt> <dd>

Muestra el contenido de la caché de vecinos. Si se especifica un número de interfaz, solo se muestra el contenido de la memoria caché de vecinos de la interfaz. De lo contrario, se mostrará el contenido de todas las memorias caché de vecinos de la interfaz. Si se especifica una interfaz, se puede especificar una dirección IPv6 para mostrar solo esa entrada de caché de vecino.

Para cada entrada de caché de vecino, se muestran la interfaz, la dirección IPv6, la dirección de nivel de vínculo y el estado de alcance.

</dd> <dt>

<span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**NCF** \[ de IPv6 Si \# \[ dirección\]\]
</dt> <dd>

Vacía las entradas de caché de vecinos especificadas. Solo se purgan las entradas de la caché de vecinos sin referencias. Dado que las entradas de la caché de ruta contienen referencias a las entradas de la memoria caché de vecinos, primero se debe vaciar la caché de ruta. Las entradas de la tabla de enrutamiento también pueden contener referencias a entradas de la caché de vecinos.

</dd> <dt>

<span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**RC** \[ de IPv6 Si \# dirección\]
</dt> <dd>

Muestra el contenido de la caché de rutas. La caché de rutas es el nombre de implementación de Microsoft IPv6 para la caché de destino. Si se especifica una interfaz y una dirección, se muestra la entrada de caché de ruta para llegar a la dirección a través de la interfaz. De lo contrario, se muestran todas las entradas de la caché de ruta.

Para cada entrada de la caché de ruta, se muestran la dirección IPv6 y la interfaz de próximo salto y la dirección de vecino actuales. La dirección de origen preferida para su uso con este destino, la MTU de la ruta de acceso actual para alcanzar este destino a través de la interfaz y la determinación de si se trata de una entrada específica de la interfaz: se muestra también la entrada de la caché de ruta. También se muestra cualquier dirección de atención (para la movilidad) de la dirección de destino.

Una dirección de destino puede tener varias entradas de caché de ruta, tanto como una para cada interfaz de salida. Sin embargo, una dirección de destino puede tener un máximo de una entrada de caché de ruta que no sea específica de la interfaz. Una interfaz específica: la entrada de la caché de ruta solo se usa si la aplicación especifica explícitamente esa interfaz de salida.

</dd> <dt>

<span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**RCF IPv6** \[ Si \# \[ dirección\]\]
</dt> <dd>

Vacía las entradas de la memoria caché de ruta especificada.

</dd> <dt>

<span id="ipv6_bc"></span><span id="IPV6_BC"></span>**BC de IPv6**
</dt> <dd>

Muestra el contenido de la caché de enlace, que contiene enlaces entre las direcciones de inicio y las direcciones de atención para IPv6 móvil.

Para cada enlace, se muestran la dirección de inicio, la dirección de atención, el número de secuencia de enlace y la duración.

</dd> <dt>

<span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**IPv6 ADU** si \# la \[ \[ \] \] \[ \] unidifusión de difusión por proximidad \[ de/PL de la duración de/Address\]
</dt> <dd>

Agrega o quita una asignación de dirección de difusión o unidifusión en una interfaz. La dirección de unidifusión actúa a menos que se especifique Anycast.

La duración es infinita si no se especifica. Si solo se especifica una duración válida, la vigencia preferida es igual a la duración válida. Se puede especificar una duración infinita o un valor finito en segundos. La duración preferida debe ser menor o igual que la duración válida. Si se especifica una duración de cero, se quitará la dirección.

Puede abreviar la duración como vida.

En el caso de las direcciones de difusión por proximidad, los únicos valores válidos de vigencia son cero y infinito.

</dd> <dt>

<span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**en el mismo en IPv6**
</dt> <dd>

Muestra el contenido actual de la tabla de prefijos de sitio.

Para cada prefijo de sitio, el comando muestra el prefijo, la interfaz a la que se aplica el prefijo del sitio y la duración del prefijo en segundos.

Normalmente, los prefijos de sitio se configuran automáticamente a partir de anuncios de enrutador. Se usan en la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) para filtrar las direcciones locales de sitio inadecuadas.

</dd> <dt>

<span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>Prefijo de la **SPU de IPv6** si la \# \[ duración es L\]
</dt> <dd>

Agrega, quita o actualiza un prefijo en la tabla de prefijos de sitio.

El prefijo y el número de interfaz son obligatorios. La duración del prefijo del sitio, especificada en segundos, tiene como valor predeterminado infinito si no se especifica. Si se especifica una duración de cero, se elimina el prefijo del sitio.

Este comando no es necesario para la configuración normal de hosts o enrutadores.

</dd> <dt>

<span id="ipv6_rt"></span><span id="IPV6_RT"></span>**RT de IPv6**
</dt> <dd>

Muestra el contenido actual de la tabla de enrutamiento.

Para cada entrada de la tabla de enrutamiento, el comando muestra el prefijo de ruta, una interfaz de vínculo o un vecino de próximo salto en una interfaz, un valor de preferencia (se prefiere más pequeño) y una duración en segundos.

Las entradas de la tabla de enrutamiento también pueden tener atributos de **publicación** y **caducidad** . De forma predeterminada, caducan (la duración se recuenta, en lugar de la constante restante) y no se publican (no se usan en la creación de anuncios de enrutador).

En los hosts, las entradas de la tabla de enrutamiento normalmente se configuran automáticamente desde los anuncios de enrutador.

</dd> <dt>

<span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>Prefijo de **RTU de IPv6** si \# \[ \] \[ \] \[ la duración \] \[ \] \[ \] \[ de la/NextHop\]
</dt> <dd>

Agrega o quita una ruta en la tabla de enrutamiento. El prefijo de ruta es obligatorio. El prefijo puede estar vinculado a una interfaz especificada o al próximo salto, especificado con una dirección de vecino en una interfaz. La ruta puede tener una duración en segundos, con el valor infinito predeterminado, y una preferencia, con el valor predeterminado de cero o el más preferido. Si se especifica una duración de cero, se elimina la ruta.

Si la ruta se especifica como publicada, lo que indica que se usará para crear anuncios de enrutador, no caduca. La duración de la ruta no se cuenta y, por lo tanto, es realmente infinita, pero el valor se usa en los anuncios de enrutador. Opcionalmente, una ruta se puede especificar como una ruta publicada que también envejece. Una ruta no publicada de forma predeterminada siempre caduca.

La subopción SPL opcional se puede usar para especificar una longitud de prefijo de sitio asociada a la ruta. La longitud del prefijo del sitio se usa solo al enviar anuncios de enrutador.

La duración se puede abreviar como vida, preferencia como Pref y publicar como pub.

</dd> </dl>

 

 



