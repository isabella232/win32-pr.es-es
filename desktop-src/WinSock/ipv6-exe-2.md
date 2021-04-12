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
# <a name="ipv6exe"></a><span data-ttu-id="7517b-103">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="7517b-103">Ipv6.exe</span></span>

<span data-ttu-id="7517b-104">Toda la configuración de IPv6 se realiza con la herramienta Ipv6.exe.</span><span class="sxs-lookup"><span data-stu-id="7517b-104">All IPv6 configuration is done with the Ipv6.exe tool.</span></span> <span data-ttu-id="7517b-105">Esta herramienta se utiliza principalmente para la consulta y configuración de interfaces, direcciones, memorias caché y rutas de IPv6.</span><span class="sxs-lookup"><span data-stu-id="7517b-105">This tool is primarily used for the querying and configuring of IPv6 interfaces, addresses, caches, and routes.</span></span> <span data-ttu-id="7517b-106">A continuación se indican los subcomandos IPv6:</span><span class="sxs-lookup"><span data-stu-id="7517b-106">The following are IPv6 subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="7517b-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**IPv6 si** \[ Cuando\#\]</span><span class="sxs-lookup"><span data-stu-id="7517b-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**ipv6 if** \[if\#\]</span></span>
</dt> <dd>

<span data-ttu-id="7517b-108">Muestra información sobre las interfaces.</span><span class="sxs-lookup"><span data-stu-id="7517b-108">Displays information about interfaces.</span></span> <span data-ttu-id="7517b-109">Si se especifica un número de interfaz, solo se muestra información sobre esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="7517b-109">If an interface number is specified, only information about that interface is displayed.</span></span> <span data-ttu-id="7517b-110">De lo contrario, se muestra información sobre todas las interfaces.</span><span class="sxs-lookup"><span data-stu-id="7517b-110">Otherwise, information about all interfaces is displayed.</span></span> <span data-ttu-id="7517b-111">La salida incluye la dirección de nivel de vínculo de la interfaz y la lista de direcciones IPv6 asignadas a la interfaz, incluida la MTU actual de la interfaz y la MTU máxima (true) que la interfaz puede admitir.</span><span class="sxs-lookup"><span data-stu-id="7517b-111">The output includes the interface's link-layer address and the list of IPv6 addresses assigned to the interface, including the interface's current MTU and the maximum (true) MTU that the interface can support.</span></span>

<span data-ttu-id="7517b-112">\#La interfaz 1 es una pseudo-interfaz que se usa para bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="7517b-112">Interface \#1 is a pseudo-interface used for loopback.</span></span> <span data-ttu-id="7517b-113">\#La interfaz 2 es una pseudo-interfaz que se usa para la tunelización configurada, la tunelización automática y la tunelización 6to4.</span><span class="sxs-lookup"><span data-stu-id="7517b-113">Interface \#2 is a pseudo-interface used for configured tunneling, automatic tunneling, and 6to4 tunneling.</span></span> <span data-ttu-id="7517b-114">Otras interfaces se numeran secuencialmente en el orden en que se crean.</span><span class="sxs-lookup"><span data-stu-id="7517b-114">Other interfaces are numbered sequentially in the order in which they are created.</span></span> <span data-ttu-id="7517b-115">Este orden varía de un equipo a otro.</span><span class="sxs-lookup"><span data-stu-id="7517b-115">This order varies from one computer to another.</span></span>

<span data-ttu-id="7517b-116">Las direcciones de nivel de vínculo del formato *AA* - *BB* - *CC* - *DD* - *EE* - *FF* son direcciones Ethernet.</span><span class="sxs-lookup"><span data-stu-id="7517b-116">Link-layer addresses in *aa*-*bb*-*cc*-*dd*-*ee*-*ff* format are Ethernet addresses.</span></span> <span data-ttu-id="7517b-117">Dirección de nivel de vínculo en *un*. *b*. *c*. el formulario *d* son entre 6 y 4 interfaces.</span><span class="sxs-lookup"><span data-stu-id="7517b-117">Link-layer address in *a*.*b*.*c*.*d* form are 6-over-4 interfaces.</span></span> <span data-ttu-id="7517b-118">Para obtener más información acerca de 6 a 4, consulte RFC 2529.</span><span class="sxs-lookup"><span data-stu-id="7517b-118">For more information on 6-over-4, see RFC 2529.</span></span>

<span data-ttu-id="7517b-119">Las dos pseudo interfaces no usan la detección de vecinos IPv6.</span><span class="sxs-lookup"><span data-stu-id="7517b-119">The two pseudo-interfaces do not use IPv6 Neighbor Discovery.</span></span>

</dd> <dt>

<span data-ttu-id="7517b-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**IPv6 IFC** si \# \[ reenvía \] \[ anunciaciones \] \[ -reenvíos \] \[ -anuncia \] \[ bytes MTU de sitio \# \] \[ -identificador\]</span><span class="sxs-lookup"><span data-stu-id="7517b-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**ipv6 ifc** if\# \[forwards\] \[advertises\] \[-forwards\] \[-advertises\] \[mtu \#bytes\] \[site site-identifier\]</span></span>
</dt> <dd>

<span data-ttu-id="7517b-121">Controla los atributos de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7517b-121">Controls interface attributes.</span></span> <span data-ttu-id="7517b-122">Las interfaces se pueden reenviar, en cuyo caso reenvían paquetes con direcciones de destino no asignadas a la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7517b-122">Interfaces can be forwarding, in which case they forward packets with destination addresses not assigned to the interface.</span></span> <span data-ttu-id="7517b-123">Las interfaces se pueden anunciar, en cuyo caso envían anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="7517b-123">Interfaces can be advertising, in which case they send router advertisements.</span></span> <span data-ttu-id="7517b-124">Estos atributos se pueden controlar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="7517b-124">These attributes can be independently controlled.</span></span> <span data-ttu-id="7517b-125">Una interfaz envía solicitudes de enrutador y recibe anuncios de enrutador, o recibe solicitudes de enrutador y envía anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="7517b-125">An interface either sends router solicitations and receives router advertisements, or receives router solicitations and sends router advertisements.</span></span>

<span data-ttu-id="7517b-126">Dado que las dos pseudo interfaces no usan la detección de vecinos, no se pueden configurar para enviar anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="7517b-126">Because the two pseudo-interfaces do not use Neighbor Discovery, they cannot be configured to send router advertisements.</span></span>

<span data-ttu-id="7517b-127">Los reenvíos se pueden abreviar como forw y anunciarse como ADV.</span><span class="sxs-lookup"><span data-stu-id="7517b-127">Forwards can be abbreviated as forw, and advertised as adv.</span></span>

<span data-ttu-id="7517b-128">También se puede establecer la MTU de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7517b-128">The MTU for the interface can also be set.</span></span> <span data-ttu-id="7517b-129">La nueva MTU debe ser menor o igual que la MTU máxima (true) del vínculo (indicada por IPv6 si) y mayor o igual que la MTU de IPv6 mínima (1280 bytes).</span><span class="sxs-lookup"><span data-stu-id="7517b-129">The new MTU must be less than or equal to the link's maximum (true) MTU (as reported by ipv6 if) and greater than or equal to the minimum IPv6 MTU (1280 bytes).</span></span>

<span data-ttu-id="7517b-130">También se puede cambiar el identificador de sitio de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="7517b-130">The site-identifier for an interface can also be changed.</span></span> <span data-ttu-id="7517b-131">Los identificadores de sitio se utilizan en \_ el \_ campo ID. de ámbito sin6 con direcciones locales del sitio.</span><span class="sxs-lookup"><span data-stu-id="7517b-131">Site identifiers are used in the sin6\_scope\_id field with site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="7517b-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**IFD de IPv6** si\#</span><span class="sxs-lookup"><span data-stu-id="7517b-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**ipv6 ifd** if\#</span></span>
</dt> <dd>

<span data-ttu-id="7517b-133">Elimina una interfaz.</span><span class="sxs-lookup"><span data-stu-id="7517b-133">Deletes an interface.</span></span> <span data-ttu-id="7517b-134">Las pseudo-interfaces de bucle invertido y de túnel no se pueden eliminar.</span><span class="sxs-lookup"><span data-stu-id="7517b-134">The loopback and tunnel pseudo-interfaces cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="7517b-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**NC** \[ de IPv6 Si \# \[ dirección\]\]</span><span class="sxs-lookup"><span data-stu-id="7517b-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**ipv6 nc** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="7517b-136">Muestra el contenido de la caché de vecinos.</span><span class="sxs-lookup"><span data-stu-id="7517b-136">Displays the contents of the neighbor cache.</span></span> <span data-ttu-id="7517b-137">Si se especifica un número de interfaz, solo se muestra el contenido de la memoria caché de vecinos de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7517b-137">If an interface number is specified, only the contents of that interface's neighbor cache are displayed.</span></span> <span data-ttu-id="7517b-138">De lo contrario, se mostrará el contenido de todas las memorias caché de vecinos de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7517b-138">Otherwise, the contents of all the interface's neighbor caches are displayed.</span></span> <span data-ttu-id="7517b-139">Si se especifica una interfaz, se puede especificar una dirección IPv6 para mostrar solo esa entrada de caché de vecino.</span><span class="sxs-lookup"><span data-stu-id="7517b-139">If an interface is specified, an IPv6 address can be specified to display only that neighbor cache entry.</span></span>

<span data-ttu-id="7517b-140">Para cada entrada de caché de vecino, se muestran la interfaz, la dirección IPv6, la dirección de nivel de vínculo y el estado de alcance.</span><span class="sxs-lookup"><span data-stu-id="7517b-140">For each neighbor cache entry, the interface, IPv6 address, link-layer address, and reach state are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="7517b-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**NCF** \[ de IPv6 Si \# \[ dirección\]\]</span><span class="sxs-lookup"><span data-stu-id="7517b-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**ipv6 ncf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="7517b-142">Vacía las entradas de caché de vecinos especificadas.</span><span class="sxs-lookup"><span data-stu-id="7517b-142">Flushes the specified neighbor cache entries.</span></span> <span data-ttu-id="7517b-143">Solo se purgan las entradas de la caché de vecinos sin referencias.</span><span class="sxs-lookup"><span data-stu-id="7517b-143">Only neighbor cache entries without references are purged.</span></span> <span data-ttu-id="7517b-144">Dado que las entradas de la caché de ruta contienen referencias a las entradas de la memoria caché de vecinos, primero se debe vaciar la caché de ruta.</span><span class="sxs-lookup"><span data-stu-id="7517b-144">Because route cache entries hold references to neighbor cache entries, the route cache should be flushed first.</span></span> <span data-ttu-id="7517b-145">Las entradas de la tabla de enrutamiento también pueden contener referencias a entradas de la caché de vecinos.</span><span class="sxs-lookup"><span data-stu-id="7517b-145">Routing table entries can also hold references to neighbor cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="7517b-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**RC** \[ de IPv6 Si \# dirección\]</span><span class="sxs-lookup"><span data-stu-id="7517b-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**ipv6 rc** \[if\# address\]</span></span>
</dt> <dd>

<span data-ttu-id="7517b-147">Muestra el contenido de la caché de rutas.</span><span class="sxs-lookup"><span data-stu-id="7517b-147">Displays the contents of the route cache.</span></span> <span data-ttu-id="7517b-148">La caché de rutas es el nombre de implementación de Microsoft IPv6 para la caché de destino.</span><span class="sxs-lookup"><span data-stu-id="7517b-148">The route cache is the Microsoft IPv6 implementation name for the destination cache.</span></span> <span data-ttu-id="7517b-149">Si se especifica una interfaz y una dirección, se muestra la entrada de caché de ruta para llegar a la dirección a través de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7517b-149">If an interface and address are specified, the route cache entry for reaching the address through the interface is displayed.</span></span> <span data-ttu-id="7517b-150">De lo contrario, se muestran todas las entradas de la caché de ruta.</span><span class="sxs-lookup"><span data-stu-id="7517b-150">Otherwise, all route cache entries are displayed.</span></span>

<span data-ttu-id="7517b-151">Para cada entrada de la caché de ruta, se muestran la dirección IPv6 y la interfaz de próximo salto y la dirección de vecino actuales.</span><span class="sxs-lookup"><span data-stu-id="7517b-151">For each route cache entry, the IPv6 address and the current next-hop interface and neighbor address are displayed.</span></span> <span data-ttu-id="7517b-152">La dirección de origen preferida para su uso con este destino, la MTU de la ruta de acceso actual para alcanzar este destino a través de la interfaz y la determinación de si se trata de una entrada específica de la interfaz: se muestra también la entrada de la caché de ruta.</span><span class="sxs-lookup"><span data-stu-id="7517b-152">The preferred source address for use with this destination, the current path MTU for reaching this destination through the interface, and the determination of whether this is an interface specific–route cache entry are also displayed.</span></span> <span data-ttu-id="7517b-153">También se muestra cualquier dirección de atención (para la movilidad) de la dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="7517b-153">Any care-of address (for mobility) for the destination address is displayed as well.</span></span>

<span data-ttu-id="7517b-154">Una dirección de destino puede tener varias entradas de caché de ruta, tanto como una para cada interfaz de salida.</span><span class="sxs-lookup"><span data-stu-id="7517b-154">A destination address can have multiple route cache entries—as many as one for each outgoing interface.</span></span> <span data-ttu-id="7517b-155">Sin embargo, una dirección de destino puede tener un máximo de una entrada de caché de ruta que no sea específica de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7517b-155">However, a destination address can have a maximum of one route cache entry that is not interface-specific.</span></span> <span data-ttu-id="7517b-156">Una interfaz específica: la entrada de la caché de ruta solo se usa si la aplicación especifica explícitamente esa interfaz de salida.</span><span class="sxs-lookup"><span data-stu-id="7517b-156">An interface specific–route cache entry is only used if the application explicitly specifies that outgoing interface.</span></span>

</dd> <dt>

<span data-ttu-id="7517b-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**RCF IPv6** \[ Si \# \[ dirección\]\]</span><span class="sxs-lookup"><span data-stu-id="7517b-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**ipv6 rcf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="7517b-158">Vacía las entradas de la memoria caché de ruta especificada.</span><span class="sxs-lookup"><span data-stu-id="7517b-158">Flushes the specified route cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="7517b-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**BC de IPv6**</span><span class="sxs-lookup"><span data-stu-id="7517b-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**ipv6 bc**</span></span>
</dt> <dd>

<span data-ttu-id="7517b-160">Muestra el contenido de la caché de enlace, que contiene enlaces entre las direcciones de inicio y las direcciones de atención para IPv6 móvil.</span><span class="sxs-lookup"><span data-stu-id="7517b-160">Displays the contents of the binding cache, which holds bindings between home addresses and care-of addresses for mobile IPv6.</span></span>

<span data-ttu-id="7517b-161">Para cada enlace, se muestran la dirección de inicio, la dirección de atención, el número de secuencia de enlace y la duración.</span><span class="sxs-lookup"><span data-stu-id="7517b-161">For each binding, the home address, care-of address, binding sequence number, and lifetime are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="7517b-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**IPv6 ADU** si \# la \[ \[ \] \] \[ \] unidifusión de difusión por proximidad \[ de/PL de la duración de/Address\]</span><span class="sxs-lookup"><span data-stu-id="7517b-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**ipv6 adu** if\#/address \[lifetime VL\[/PL\]\] \[anycast\] \[unicast\]</span></span>
</dt> <dd>

<span data-ttu-id="7517b-163">Agrega o quita una asignación de dirección de difusión o unidifusión en una interfaz.</span><span class="sxs-lookup"><span data-stu-id="7517b-163">Adds or removes a unicast or anycast address assignment on an interface.</span></span> <span data-ttu-id="7517b-164">La dirección de unidifusión actúa a menos que se especifique Anycast.</span><span class="sxs-lookup"><span data-stu-id="7517b-164">The unicast address is acted upon unless anycast is specified.</span></span>

<span data-ttu-id="7517b-165">La duración es infinita si no se especifica.</span><span class="sxs-lookup"><span data-stu-id="7517b-165">Lifetime is infinite if unspecified.</span></span> <span data-ttu-id="7517b-166">Si solo se especifica una duración válida, la vigencia preferida es igual a la duración válida.</span><span class="sxs-lookup"><span data-stu-id="7517b-166">If only a valid lifetime is specified, the preferred lifetime is equal to the valid lifetime.</span></span> <span data-ttu-id="7517b-167">Se puede especificar una duración infinita o un valor finito en segundos.</span><span class="sxs-lookup"><span data-stu-id="7517b-167">An infinite lifetime may be specified, or a finite value in seconds.</span></span> <span data-ttu-id="7517b-168">La duración preferida debe ser menor o igual que la duración válida.</span><span class="sxs-lookup"><span data-stu-id="7517b-168">The preferred lifetime must be less than or equal to the valid lifetime.</span></span> <span data-ttu-id="7517b-169">Si se especifica una duración de cero, se quitará la dirección.</span><span class="sxs-lookup"><span data-stu-id="7517b-169">Specifying a lifetime of zero causes the address to be removed.</span></span>

<span data-ttu-id="7517b-170">Puede abreviar la duración como vida.</span><span class="sxs-lookup"><span data-stu-id="7517b-170">You can abbreviate lifetime as life.</span></span>

<span data-ttu-id="7517b-171">En el caso de las direcciones de difusión por proximidad, los únicos valores válidos de vigencia son cero y infinito.</span><span class="sxs-lookup"><span data-stu-id="7517b-171">For anycast addresses, the only valid lifetime values are zero and infinite.</span></span>

</dd> <dt>

<span data-ttu-id="7517b-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**en el mismo en IPv6**</span><span class="sxs-lookup"><span data-stu-id="7517b-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**ipv6 spt**</span></span>
</dt> <dd>

<span data-ttu-id="7517b-173">Muestra el contenido actual de la tabla de prefijos de sitio.</span><span class="sxs-lookup"><span data-stu-id="7517b-173">Displays the current contents of the site prefix table.</span></span>

<span data-ttu-id="7517b-174">Para cada prefijo de sitio, el comando muestra el prefijo, la interfaz a la que se aplica el prefijo del sitio y la duración del prefijo en segundos.</span><span class="sxs-lookup"><span data-stu-id="7517b-174">For each site prefix, the command displays the prefix, the interface to which the site prefix applies, and the prefix lifetime in seconds.</span></span>

<span data-ttu-id="7517b-175">Normalmente, los prefijos de sitio se configuran automáticamente a partir de anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="7517b-175">Site prefixes are normally auto-configured from router advertisements.</span></span> <span data-ttu-id="7517b-176">Se usan en la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) para filtrar las direcciones locales de sitio inadecuadas.</span><span class="sxs-lookup"><span data-stu-id="7517b-176">They are used in the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function to filter inappropriate site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="7517b-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>Prefijo de la **SPU de IPv6** si la \# \[ duración es L\]</span><span class="sxs-lookup"><span data-stu-id="7517b-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>**ipv6 spu** prefix if\# \[lifetime L\]</span></span>
</dt> <dd>

<span data-ttu-id="7517b-178">Agrega, quita o actualiza un prefijo en la tabla de prefijos de sitio.</span><span class="sxs-lookup"><span data-stu-id="7517b-178">Adds, removes, or updates a prefix in the site prefix table.</span></span>

<span data-ttu-id="7517b-179">El prefijo y el número de interfaz son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="7517b-179">The prefix and interface number are required.</span></span> <span data-ttu-id="7517b-180">La duración del prefijo del sitio, especificada en segundos, tiene como valor predeterminado infinito si no se especifica.</span><span class="sxs-lookup"><span data-stu-id="7517b-180">The site prefix lifetime, specified in seconds, defaults to infinite if not specified.</span></span> <span data-ttu-id="7517b-181">Si se especifica una duración de cero, se elimina el prefijo del sitio.</span><span class="sxs-lookup"><span data-stu-id="7517b-181">Specifying a lifetime of zero deletes the site prefix.</span></span>

<span data-ttu-id="7517b-182">Este comando no es necesario para la configuración normal de hosts o enrutadores.</span><span class="sxs-lookup"><span data-stu-id="7517b-182">This command is unnecessary for the normal configuration of hosts or routers.</span></span>

</dd> <dt>

<span data-ttu-id="7517b-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**RT de IPv6**</span><span class="sxs-lookup"><span data-stu-id="7517b-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**ipv6 rt**</span></span>
</dt> <dd>

<span data-ttu-id="7517b-184">Muestra el contenido actual de la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="7517b-184">Displays the current contents of the routing table.</span></span>

<span data-ttu-id="7517b-185">Para cada entrada de la tabla de enrutamiento, el comando muestra el prefijo de ruta, una interfaz de vínculo o un vecino de próximo salto en una interfaz, un valor de preferencia (se prefiere más pequeño) y una duración en segundos.</span><span class="sxs-lookup"><span data-stu-id="7517b-185">For each routing table entry, the command displays the route prefix, an on-link interface or a next-hop neighbor on an interface, a preference value (smaller is preferred), and a lifetime in seconds.</span></span>

<span data-ttu-id="7517b-186">Las entradas de la tabla de enrutamiento también pueden tener atributos de **publicación** y **caducidad** .</span><span class="sxs-lookup"><span data-stu-id="7517b-186">Routing table entries may also have **publish** and **aging** attributes.</span></span> <span data-ttu-id="7517b-187">De forma predeterminada, caducan (la duración se recuenta, en lugar de la constante restante) y no se publican (no se usan en la creación de anuncios de enrutador).</span><span class="sxs-lookup"><span data-stu-id="7517b-187">By default, they age (the lifetime counts down, rather than remaining constant) and are not published (not used in constructing router advertisements).</span></span>

<span data-ttu-id="7517b-188">En los hosts, las entradas de la tabla de enrutamiento normalmente se configuran automáticamente desde los anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="7517b-188">On hosts, routing table entries are normally auto-configured from router advertisements.</span></span>

</dd> <dt>

<span data-ttu-id="7517b-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>Prefijo de **RTU de IPv6** si \# \[ \] \[ \] \[ la duración \] \[ \] \[ \] \[ de la/NextHop\]</span><span class="sxs-lookup"><span data-stu-id="7517b-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>**ipv6 rtu** prefix if\#\[/nexthop\] \[lifetime L\] \[preference P\] \[publish\] \[age\] \[spl site-prefix-length\]</span></span>
</dt> <dd>

<span data-ttu-id="7517b-190">Agrega o quita una ruta en la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="7517b-190">Adds or removes a route in the routing table.</span></span> <span data-ttu-id="7517b-191">El prefijo de ruta es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7517b-191">The route prefix is required.</span></span> <span data-ttu-id="7517b-192">El prefijo puede estar vinculado a una interfaz especificada o al próximo salto, especificado con una dirección de vecino en una interfaz.</span><span class="sxs-lookup"><span data-stu-id="7517b-192">The prefix can be on-link to a specified interface, or next-hop, specified with a neighbor address on an interface.</span></span> <span data-ttu-id="7517b-193">La ruta puede tener una duración en segundos, con el valor infinito predeterminado, y una preferencia, con el valor predeterminado de cero o el más preferido.</span><span class="sxs-lookup"><span data-stu-id="7517b-193">The route can have a lifetime in seconds, with the default infinite, and a preference, with the default of zero, or most preferred.</span></span> <span data-ttu-id="7517b-194">Si se especifica una duración de cero, se elimina la ruta.</span><span class="sxs-lookup"><span data-stu-id="7517b-194">Specifying a lifetime of zero deletes the route.</span></span>

<span data-ttu-id="7517b-195">Si la ruta se especifica como publicada, lo que indica que se usará para crear anuncios de enrutador, no caduca.</span><span class="sxs-lookup"><span data-stu-id="7517b-195">If the route is specified as published, indicating it will be used in constructing router advertisements, it does not age.</span></span> <span data-ttu-id="7517b-196">La duración de la ruta no se cuenta y, por lo tanto, es realmente infinita, pero el valor se usa en los anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="7517b-196">The route's lifetime does not count down and therefore is effectively infinite, but the value is used in router advertisements.</span></span> <span data-ttu-id="7517b-197">Opcionalmente, una ruta se puede especificar como una ruta publicada que también envejece.</span><span class="sxs-lookup"><span data-stu-id="7517b-197">Optionally, a route can be specified as a published route that also ages.</span></span> <span data-ttu-id="7517b-198">Una ruta no publicada de forma predeterminada siempre caduca.</span><span class="sxs-lookup"><span data-stu-id="7517b-198">A nonpublished route by default always ages.</span></span>

<span data-ttu-id="7517b-199">La subopción SPL opcional se puede usar para especificar una longitud de prefijo de sitio asociada a la ruta.</span><span class="sxs-lookup"><span data-stu-id="7517b-199">The optional spl suboption can be used to specify a site prefix length associated with the route.</span></span> <span data-ttu-id="7517b-200">La longitud del prefijo del sitio se usa solo al enviar anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="7517b-200">The site prefix length is used only when sending router advertisements.</span></span>

<span data-ttu-id="7517b-201">La duración se puede abreviar como vida, preferencia como Pref y publicar como pub.</span><span class="sxs-lookup"><span data-stu-id="7517b-201">Lifetime can be abbreviated as life, preference as pref, and publish as pub.</span></span>

</dd> </dl>

 

 



