---
description: 6to4 es un método para conectar hosts o sitios IPv6 a través de la infraestructura de Internet existente de IPv4.
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: 'Configuración 2: tráfico IPv6 entre nodos de diferentes subredes de una red IPv4 (6to4)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1abd5477005e6a1e71c13aaf19a734e9191097d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497465"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a><span data-ttu-id="5f9ad-103">Configuración 2: tráfico IPv6 entre nodos de diferentes subredes de una red IPv4 (6to4)</span><span class="sxs-lookup"><span data-stu-id="5f9ad-103">Configuration 2: IPv6 Traffic Between Nodes on Different Subnets of an IPv4 Internetwork (6to4)</span></span>

<span data-ttu-id="5f9ad-104">6to4 es un método para conectar hosts o sitios IPv6 a través de la infraestructura de Internet existente de IPv4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-104">6to4 is a method for connecting IPv6 hosts or sites over the existing IPv4 Internet infrastructure.</span></span> <span data-ttu-id="5f9ad-105">Utiliza un prefijo de dirección único para proporcionar a los sitios IPv6 aislados su propio espacio de direcciones IPv6.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-105">It uses a unique address prefix to give isolated IPv6 sites their own IPv6 address space.</span></span> <span data-ttu-id="5f9ad-106">6to4 es como un "pseudo-ISP" que proporciona conectividad IPv6.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-106">6to4 is like a "pseudo-ISP" providing IPv6 connectivity.</span></span> <span data-ttu-id="5f9ad-107">Puede usar 6to4 para comunicarse directamente con otros sitios 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-107">You can use 6to4 to communicate directly with other 6to4 sites.</span></span> <span data-ttu-id="5f9ad-108">6to4 no requiere el uso de enrutadores IPv6 y su tráfico IPv6 se encapsula con un encabezado IPv4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-108">6to4 does not require the use of IPv6 routers and its IPv6 traffic is encapsulated with an IPv4 header.</span></span>

<span data-ttu-id="5f9ad-109">En la ilustración siguiente se muestra la configuración de dos nodos en subredes independientes mediante 6to4 para comunicarse a través de un enrutador IPv4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-109">The following illustration shows the configuration of two nodes on separate subnets using 6to4 to communicate across an IPv4 router.</span></span>

![nodos que usan 6to4 para comunicarse a través de un enrutador IPv4.](images/v6mig-2.png)

<span data-ttu-id="5f9ad-111">El requisito principal para usar 6to4 es una dirección IPv4 globalmente enrutable para el sitio.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-111">The main requirement for using 6to4 is one globally routable IPv4 address for your site.</span></span> <span data-ttu-id="5f9ad-112">Supongamos que el sitio consta de una colección de equipos IPv6 administrados (algunos ejecutan el protocolo IPv6 de Microsoft y otros que ejecutan otras implementaciones de IPv6).</span><span class="sxs-lookup"><span data-stu-id="5f9ad-112">Suppose that your site consists of a collection of IPv6 computers that you manage (some running the Microsoft IPv6 protocol and some running other IPv6 implementations).</span></span> <span data-ttu-id="5f9ad-113">Supongamos también que todos los equipos IPv6 están conectados directamente mediante Ethernet o 6-over-4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-113">Assume also that all IPv6 computers are directly connected using Ethernet or 6-over-4.</span></span> <span data-ttu-id="5f9ad-114">La dirección IPv4 globalmente enrutable debe estar asignada a uno de los equipos que ejecutan el protocolo IPv6 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-114">The globally routable IPv4 address must be assigned to one of your computers running the Microsoft IPv6 protocol.</span></span> <span data-ttu-id="5f9ad-115">Este equipo será la puerta de enlace 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-115">This computer will be your 6to4 gateway.</span></span>

<span data-ttu-id="5f9ad-116">Si tiene una dirección IPv4 que forma parte del espacio de direcciones privadas (10.0.0.0/8, 172.16.0.0/12 o 192.168.0.0/16) o el espacio de direcciones de direcciones IP privadas automáticas (APIPA) de 169.254.0.0/16 utilizado por Windows 2000, no es enrutable globalmente.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-116">If you have an IPv4 address that is part of the private address space (10.0.0.0/8, 172.16.0.0/12, or 192.168.0.0/16) or the Automatic Private IP Addressing (APIPA) address space of 169.254.0.0/16 used by Windows 2000, it is not globally routable.</span></span> <span data-ttu-id="5f9ad-117">De lo contrario, es probable que sea una dirección IP pública y sea enrutable globalmente.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-117">Otherwise, it is probably a public IP address and is globally routable.</span></span> <span data-ttu-id="5f9ad-118">Consulte el tema [depuración](#debugging-6to4-configuration) de la configuración de 6to4 en este documento para obtener más información sobre cómo determinar si la conexión de ISP es compatible con 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-118">See the [Debugging 6to4 Configuration](#debugging-6to4-configuration) topic in this document for more help in determining whether your ISP connection supports 6to4.</span></span>

## <a name="the-6to4cfgexe-tool"></a><span data-ttu-id="5f9ad-119">La herramienta 6to4cfg.exe</span><span class="sxs-lookup"><span data-stu-id="5f9ad-119">The 6to4cfg.exe Tool</span></span>

<span data-ttu-id="5f9ad-120">La herramienta de 6to4cfg.exe automatiza la configuración de 6to4, detecta automáticamente la dirección IPv4 globalmente enrutable y crea un prefijo 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-120">The 6to4cfg.exe tool automates 6to4 configuration, automatically discovering your globally routable IPv4 address and creating a 6to4 prefix.</span></span> <span data-ttu-id="5f9ad-121">Realiza la configuración directamente, o bien puede escribir un script de configuración que puede inspeccionar y ejecutar más adelante.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-121">It either performs the configuration directly, or it can write a configuration script that you can inspect and run later.</span></span>

<span data-ttu-id="5f9ad-122">La sintaxis básica del comando 6to4cfg.exe es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-122">The basic 6to4cfg.exe command syntax is as follows.</span></span>

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span data-ttu-id="5f9ad-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*extensión*\]</span><span class="sxs-lookup"><span data-stu-id="5f9ad-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*filename*\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9ad-124">Escribe el script de configuración en un archivo, si se especifica un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-124">Writes the configuration script to a file, if you specify a file name.</span></span> <span data-ttu-id="5f9ad-125">El script de configuración utiliza Ipv6.exe.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-125">The configuration script uses Ipv6.exe.</span></span>

<span data-ttu-id="5f9ad-126">Puede especificar con para que el nombre de archivo escriba el script de configuración en la salida de la consola, lo que resulta útil para ver lo que 6to4cfg.exe hará en un escenario de prueba.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-126">You can specify con for the file name to write the configuration script to console output, which is useful for seeing what 6to4cfg.exe will do in a test scenario.</span></span>

<span data-ttu-id="5f9ad-127">Si no especifica un nombre de archivo, 6to4cfg.exe actualiza directamente la configuración de IPv6 en el equipo.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-127">If you do not specify a file name, 6to4cfg.exe directly updates the IPv6 configuration on your computer.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ad-128"><span id="-r"></span><span id="-R"></span>-r</span><span class="sxs-lookup"><span data-stu-id="5f9ad-128"><span id="-r"></span><span id="-R"></span>-r</span></span>
</dt> <dd>

<span data-ttu-id="5f9ad-129">Se convierte en un enrutador de puerta de enlace 6to4 para la red local, lo que permite el enrutamiento en todas las interfaces y prefijos de subred asignados.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-129">Becomes a 6to4 gateway router for your local network, enabling routing on all of your interfaces and assigned subnet prefixes.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ad-130"><span id="-s"></span><span id="-S"></span>-s</span><span class="sxs-lookup"><span data-stu-id="5f9ad-130"><span id="-s"></span><span id="-S"></span>-s</span></span>
</dt> <dd>

<span data-ttu-id="5f9ad-131">Habilita el direccionamiento local del sitio en el sitio 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-131">Enables site-local addressing in your 6to4 site.</span></span> <span data-ttu-id="5f9ad-132">Este comando solo es útil cuando se usa junto con-r.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-132">This command is only useful when used in conjunction with -r.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ad-133"><span id="-u"></span><span id="-U"></span>-u</span><span class="sxs-lookup"><span data-stu-id="5f9ad-133"><span id="-u"></span><span id="-U"></span>-u</span></span>
</dt> <dd>

<span data-ttu-id="5f9ad-134">Especifica que se va a invertir la configuración de 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-134">Specifies that the 6to4 configuration be reversed.</span></span> <span data-ttu-id="5f9ad-135">Por lo tanto, 6to4cfg-u invierte el efecto de 6to4cfg y 6to4cfg-r-u invierte el efecto de 6to4cfg-r, etc.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-135">Therefore 6to4cfg -u reverses the effect of 6to4cfg and 6to4cfg -r -u reverses the effect of 6to4cfg -r, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ad-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *Relay*</span><span class="sxs-lookup"><span data-stu-id="5f9ad-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *relay*</span></span>
</dt> <dd>

<span data-ttu-id="5f9ad-137">Especifica el nombre o la dirección IPv4 de un enrutador de retransmisión 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-137">Specifies the name or IPv4 address of a 6to4 relay router.</span></span> <span data-ttu-id="5f9ad-138">El nombre predeterminado es 6to4.ipv6.microsoft.com, el enrutador de retransmisión 6to4 en Internet.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-138">The default name is 6to4.ipv6.microsoft.com, the 6to4 relay router on the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ad-139"><span id="-b"></span><span id="-B"></span>-b</span><span class="sxs-lookup"><span data-stu-id="5f9ad-139"><span id="-b"></span><span id="-B"></span>-b</span></span>
</dt> <dd>

<span data-ttu-id="5f9ad-140">Especifica que 6to4cfg.exe elige la "mejor" dirección de retransmisión en lugar de la primera.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-140">Specifies that 6to4cfg.exe picks the "best" relay address instead of the first.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ad-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *Dirección*</span><span class="sxs-lookup"><span data-stu-id="5f9ad-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *address*</span></span>
</dt> <dd>

<span data-ttu-id="5f9ad-142">Especifica la dirección IPv4 local para el prefijo 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-142">Specifies the local IPv4 address for the 6to4 prefix.</span></span>

</dd> </dl>

## <a name="manual-6to4-configuration"></a><span data-ttu-id="5f9ad-143">Configuración de 6to4 manual</span><span class="sxs-lookup"><span data-stu-id="5f9ad-143">Manual 6to4 Configuration</span></span>

<span data-ttu-id="5f9ad-144">En este ejemplo, la dirección de la puerta de enlace 6to4 es 172.31.42.239.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-144">In this example the address of the 6to4 gateway is 172.31.42.239.</span></span> <span data-ttu-id="5f9ad-145">Necesita su propia dirección IPv4 globalmente enrutable para usar 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-145">You need your own globally routable IPv4 address to use 6to4.</span></span>

> [!Note]  
> <span data-ttu-id="5f9ad-146">La dirección IP 172.31.42.239 se usa solo con fines de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-146">The IP address 172.31.42.239 is used for example purposes only.</span></span> <span data-ttu-id="5f9ad-147">Se trata de una dirección privada y no es enrutable globalmente en Internet.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-147">This is a private address and is not globally routable on the Internet.</span></span>

 

<span data-ttu-id="5f9ad-148">La dirección IPv4 globalmente enrutable de 32 bits se combina con el prefijo 2002::/16 de 16 bits para formar un prefijo de dirección IPv6 de 48 bits para el sitio.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-148">The 32-bit globally routable IPv4 address is combined with the 16-bit prefix 2002::/16 to form a 48-bit IPv6 address prefix for your site.</span></span> <span data-ttu-id="5f9ad-149">En este ejemplo, el prefijo de sitio 6to4 es 2002: ac1f: 2aef::/48.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-149">In this example, the 6to4 site prefix is 2002:ac1f:2aef::/48.</span></span> <span data-ttu-id="5f9ad-150">Tenga en cuenta que ac1f: 2aef es la codificación hexadecimal de 172.31.42.239 (por supuesto, usará un prefijo diferente según su propia dirección IPv4 globalmente enrutable).</span><span class="sxs-lookup"><span data-stu-id="5f9ad-150">Note that ac1f:2aef is the hexadecimal encoding of 172.31.42.239 (of course, you will use a different prefix based on your own globally routable IPv4 address).</span></span> <span data-ttu-id="5f9ad-151">Con el prefijo de sitio 6to4, puede asignar direcciones y prefijos de subred dentro de su sitio.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-151">Using the 6to4 site prefix, you can assign addresses and subnet prefixes inside your site.</span></span>

<span data-ttu-id="5f9ad-152">En este ejemplo se da por supuesto que usa la subred 0 para configurar manualmente una dirección 6to4 en el equipo de puerta de enlace 6to4 y que usa la subred 1 para configurar automáticamente las direcciones en el segmento de red Ethernet.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-152">This example assumes that you use subnet 0 for manually configuring a 6to4 address on your 6to4 gateway computer and that you use subnet 1 for automatically configuring addresses on your Ethernet network segment.</span></span> <span data-ttu-id="5f9ad-153">Sin embargo, son posibles otras opciones.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-153">However, other choices are possible.</span></span>

1.  <span data-ttu-id="5f9ad-154">Use Ipv6.exe para habilitar 6to4 en el equipo de puerta de enlace 6to4:</span><span class="sxs-lookup"><span data-stu-id="5f9ad-154">Use Ipv6.exe to enable 6to4 on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="5f9ad-155">**IPv6 RTU 2002::/16 2**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-155">**ipv6 rtu 2002::/16 2**</span></span>

    <span data-ttu-id="5f9ad-156">El comando **RTU de IPv6** realiza una actualización de la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-156">The **ipv6 rtu** command performs a routing table update.</span></span> <span data-ttu-id="5f9ad-157">Se puede usar para agregar, quitar o actualizar una ruta.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-157">It can be used to add, remove, or update a route.</span></span> <span data-ttu-id="5f9ad-158">En este caso, habilita 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-158">In this case it is enabling 6to4.</span></span>

    <span data-ttu-id="5f9ad-159">El argumento 2002::/16 es el prefijo de la ruta, que especifica el prefijo único de 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-159">The 2002::/16 argument is the prefix of the route, specifying the unique 6to4 prefix.</span></span>

    <span data-ttu-id="5f9ad-160">El argumento 2 especifica la interfaz en vínculo para este prefijo.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-160">The 2 argument specifies the on-link interface for this prefix.</span></span> <span data-ttu-id="5f9ad-161">\#La interfaz 2 es la "pseudo-interfaz" que se usa para los túneles configurados, la tunelización automática y 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-161">Interface \#2 is the "pseudo-interface" used for configured tunnels, automatic tunneling, and 6to4.</span></span> <span data-ttu-id="5f9ad-162">Cuando una dirección de destino IPv6 coincide con el prefijo 2002::/16, los bits 32 que siguen el prefijo de la dirección de destino se extraen para formar una dirección de destino IPv4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-162">When an IPv6 destination address matches the 2002::/16 prefix, the 32 bits that follow the prefix in the destination address are extracted to form an IPv4 destination address.</span></span> <span data-ttu-id="5f9ad-163">El paquete se encapsula con un encabezado IPv4 y se envía a la dirección de destino IPv4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-163">The packet is encapsulated with an IPv4 header and sent to the IPv4 destination address.</span></span>

2.  <span data-ttu-id="5f9ad-164">Configure una dirección 6to4 en el equipo de puerta de enlace 6to4:</span><span class="sxs-lookup"><span data-stu-id="5f9ad-164">Configure a 6to4 address on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="5f9ad-165">**IPv6 ADU 2/2002: ac1f: 2aef:: ac1f: 2aef**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-165">**ipv6 adu 2/2002:ac1f:2aef::ac1f:2aef**</span></span>

    <span data-ttu-id="5f9ad-166">El comando **IPv6 ADU** realiza una actualización de dirección.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-166">The **ipv6 adu** command performs an address update.</span></span> <span data-ttu-id="5f9ad-167">Se puede utilizar para agregar, quitar o actualizar una dirección en una interfaz.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-167">It can be used to add, remove, or update an address on an interface.</span></span> <span data-ttu-id="5f9ad-168">En esta instancia, está configurando la dirección 6to4 del equipo.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-168">In this instance, it is configuring the computer's 6to4 address.</span></span>

    <span data-ttu-id="5f9ad-169">El argumento 2/2002: ac1f: 2aef:: ac1f: 2aef especifica tanto la interfaz como la dirección.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-169">The 2/2002:ac1f:2aef::ac1f:2aef argument specifies both the interface and the address.</span></span> <span data-ttu-id="5f9ad-170">Requiere configurar la dirección 2002: ac1f: 2aef:: ac1f: 2aef en la interfaz \# 2.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-170">It requires configuring address 2002:ac1f:2aef::ac1f:2aef on interface \#2.</span></span> <span data-ttu-id="5f9ad-171">La dirección se crea con el prefijo de sitio 2002: ac1f: 2aef::/48, subred 0 para proporcionar un prefijo de subred 2002: ac1f: 2aef::/64 y un identificador de interfaz de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-171">The address is created using the site prefix 2002:ac1f:2aef::/48, subnet 0 to give a subnet prefix 2002:ac1f:2aef::/64, and a 64-bit interface identifier.</span></span> <span data-ttu-id="5f9ad-172">La Convención mostrada usa la dirección IPv4 del equipo para el identificador de interfaz para las direcciones asignadas a la interfaz \# 2.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-172">The convention demonstrated uses the computer's IPv4 address for the interface identifier for addresses assigned to interface \#2.</span></span> <span data-ttu-id="5f9ad-173">Para su uso, ac1f: 2aef debe reemplazarse por la codificación hexadecimal de su propia dirección IPv4 globalmente enrutable.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-173">For your use, ac1f:2aef should be replaced by the hexadecimal encoding of your own globally routable IPv4 address.</span></span>

<span data-ttu-id="5f9ad-174">Los dos comandos anteriores son suficientes para permitir la comunicación con otros sitios 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-174">The two preceding commands are sufficient to allow communication with other 6to4 sites.</span></span> <span data-ttu-id="5f9ad-175">Por ejemplo, puede intentar hacer ping en el sitio de Microsoft 6to4:</span><span class="sxs-lookup"><span data-stu-id="5f9ad-175">For example, you can try pinging the Microsoft 6to4 site:</span></span>

<span data-ttu-id="5f9ad-176">**ping6 2002:836b: 9820:: 836b: 9820**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-176">**ping6 2002:836b:9820::836b:9820**</span></span>

<span data-ttu-id="5f9ad-177">Para habilitar la comunicación con 6Bone, debe crear un túnel configurado predeterminado para una retransmisión 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-177">To enable communication with the 6bone, you must create a default configured tunnel to a 6to4 relay.</span></span> <span data-ttu-id="5f9ad-178">Puede usar el enrutador de retransmisión 6to4 de Microsoft, 131.107.152.32:</span><span class="sxs-lookup"><span data-stu-id="5f9ad-178">You can use the Microsoft 6to4 relay router, 131.107.152.32:</span></span>

<span data-ttu-id="5f9ad-179">**IPv6 RTU::/0 2/:: 131.107.152.32 pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-179">**ipv6 rtu ::/0 2/::131.107.152.32 pub life 1800**</span></span>

<span data-ttu-id="5f9ad-180">El comando **RTU de IPv6** realiza una actualización de la tabla de enrutamiento, estableciendo, en esta instancia, una ruta predeterminada a la retransmisión 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-180">The **ipv6 rtu** command performs a routing table update, establishing, in this instance, a default route to the 6to4 relay.</span></span>

<span data-ttu-id="5f9ad-181">El argumento::/0 es el prefijo de la ruta.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-181">The ::/0 argument is the route prefix.</span></span> <span data-ttu-id="5f9ad-182">El prefijo de longitud cero indica que se trata de una ruta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-182">The zero-length prefix indicates that it is a default route.</span></span>

<span data-ttu-id="5f9ad-183">El argumento 2/:: 131.107.152.32 especifica el vecino de próximo salto para este prefijo.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-183">The 2/::131.107.152.32 argument specifies the next-hop neighbor for this prefix.</span></span> <span data-ttu-id="5f9ad-184">Requiere que los paquetes que coinciden con el prefijo se reenvíen a Address:: 131.107.152.32 con la interfaz \# 2.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-184">It requires that packets matching the prefix are forwarded to address ::131.107.152.32 using interface \#2.</span></span> <span data-ttu-id="5f9ad-185">Al reenviar un paquete a:: 131.107.152.32 en la interfaz \# 2, se encapsula con un encabezado V4 y se envía a 131.107.152.32.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-185">Forwarding a packet to ::131.107.152.32 on interface \#2 causes it to be encapsulated with a v4 header and sent to 131.107.152.32.</span></span>

<span data-ttu-id="5f9ad-186">El argumento pub hace que esta sea una ruta publicada.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-186">The pub argument makes this a published route.</span></span> <span data-ttu-id="5f9ad-187">Como esto solo es relevante para los enrutadores, no tiene ningún efecto hasta que se habilita el enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-187">Because this is only relevant for routers, it has no effect until routing is enabled.</span></span> <span data-ttu-id="5f9ad-188">Del mismo modo, la duración de 30 minutos solo se aplica si está habilitado el enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-188">Similarly, the 30-minute lifetime pertains only if routing is enabled.</span></span>

<span data-ttu-id="5f9ad-189">Debe poder tener acceso a los sitios de 6Bone y a los sitios 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-189">You should be able to access 6bone sites as well as 6to4 sites.</span></span> <span data-ttu-id="5f9ad-190">Puede usar el siguiente comando para probarlo:</span><span class="sxs-lookup"><span data-stu-id="5f9ad-190">You can use the following command to test this:</span></span>

<span data-ttu-id="5f9ad-191">**ping6 3ffe: 1cff: 0: F5:: 1**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-191">**ping6 3ffe:1cff:0:f5::1**</span></span>

<span data-ttu-id="5f9ad-192">El paso final consiste en habilitar el enrutamiento en la puerta de enlace 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-192">The final step is to enable routing on your 6to4 gateway.</span></span> <span data-ttu-id="5f9ad-193">En este ejemplo se da por supuesto que \# la interfaz 3 del equipo de puerta de enlace es una interfaz Ethernet y la interfaz \# 4 es de 6 a 4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-193">This example assumes that interface \#3 on your gateway computer is an Ethernet interface and interface \#4 is 6-over-4.</span></span> <span data-ttu-id="5f9ad-194">El equipo podría numerar sus interfaces de manera diferente.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-194">Your computer might number its interfaces differently.</span></span> <span data-ttu-id="5f9ad-195">Los dos comandos siguientes asignan prefijos de subred a los dos vínculos.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-195">The following two commands assign subnet prefixes to the two links.</span></span> <span data-ttu-id="5f9ad-196">Los prefijos de subred se derivan del prefijo de 6to4 del sitio 2002: ac1f: 2aef::/48:</span><span class="sxs-lookup"><span data-stu-id="5f9ad-196">The subnet prefixes are derived from the site's 6to4 prefix 2002:ac1f:2aef::/48:</span></span>

<span data-ttu-id="5f9ad-197">**IPv6 RTU 2002: ac1f: 2aef: 1::/64 3 pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-197">**ipv6 rtu 2002:ac1f:2aef:1::/64 3 pub life 1800**</span></span>

<span data-ttu-id="5f9ad-198">**IPv6 RTU 2002: ac1f: 2aef: 2::/64 4 pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-198">**ipv6 rtu 2002:ac1f:2aef:2::/64 4 pub life 1800**</span></span>

<span data-ttu-id="5f9ad-199">El comando **RTU de IPv6** especifica que el prefijo 2002: ac1f: 2aef: 1::/64 está en el vínculo a la interfaz \# 3.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-199">The **ipv6 rtu** command specifies that the prefix 2002:ac1f:2aef:1::/64 is on-link to interface \#3.</span></span> <span data-ttu-id="5f9ad-200">Está configurando el primer prefijo de subred en la interfaz Ethernet.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-200">It is configuring the first subnet prefix on the Ethernet interface.</span></span> <span data-ttu-id="5f9ad-201">La ruta se publica con una duración de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-201">The route is published with a lifetime of 30 minutes.</span></span>

<span data-ttu-id="5f9ad-202">Del mismo modo, el prefijo 2002: ac1f: 2aef: 2::/64 se configura en la interfaz 6 a 4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-202">Similarly, the 2002:ac1f:2aef:2::/64 prefix is configured on the 6-over-4 interface.</span></span>

<span data-ttu-id="5f9ad-203">Los tres comandos siguientes permiten que el equipo de puerta de enlace 6to4 funcione como un enrutador:</span><span class="sxs-lookup"><span data-stu-id="5f9ad-203">The next three commands enable the 6to4 gateway computer to function as a router:</span></span>

<span data-ttu-id="5f9ad-204">**IPv6 IFC 2 forw**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-204">**ipv6 ifc 2 forw**</span></span>

<span data-ttu-id="5f9ad-205">**IPv4 IFC 3 forw ADV**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-205">**ipv6 ifc 3 forw adv**</span></span>

<span data-ttu-id="5f9ad-206">**IPv6 IFC 4 forw ADV**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-206">**ipv6 ifc 4 forw adv**</span></span>

<span data-ttu-id="5f9ad-207">El comando **IFC de IPv6** controla los atributos de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-207">The **ipv6 ifc** command controls attributes of an interface.</span></span> <span data-ttu-id="5f9ad-208">Un enrutador reenvía paquetes y envía anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-208">A router forwards packets and sends router advertisements.</span></span> <span data-ttu-id="5f9ad-209">En la implementación de Microsoft IPv6, estos atributos por interfaz se controlan por separado.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-209">In the Microsoft IPv6 implementation, these per-interface attributes are controlled separately.</span></span>

<span data-ttu-id="5f9ad-210">\#La interfaz 2 no es necesaria para la publicidad porque es una pseudo-interfaz.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-210">Interface \#2 is not needed for advertising because it is a pseudo-interface.</span></span>

<span data-ttu-id="5f9ad-211">Si el equipo tiene interfaces adicionales, también se deben configurar para que se reenvíen y anuncien.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-211">If your computer has additional interfaces, they should also be configured to be forwarding and advertising.</span></span>

<span data-ttu-id="5f9ad-212">Después de ejecutar estos comandos, el protocolo IPv6 de Microsoft configurará automáticamente las direcciones de las interfaces \# 3 y \# 4 con los prefijos de subred respectivos, y las dos interfaces comenzarán a enviar anuncios de enrutador en intervalos de aproximadamente 3 a 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-212">After running these commands, the Microsoft IPv6 protocol will automatically configure addresses on interfaces \#3 and \#4 using the respective subnet prefixes and the two interfaces will start sending router advertisements at approximately 3 to 10 minute intervals.</span></span>

<span data-ttu-id="5f9ad-213">Los hosts que reciben estos anuncios de enrutador se configurarán automáticamente con una ruta predeterminada y una dirección 6to4 derivada del prefijo de subred de su vínculo.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-213">Hosts receiving these router advertisements will automatically configure themselves with a default route and a 6to4 address derived from the subnet prefix of their link.</span></span> <span data-ttu-id="5f9ad-214">Tendrán comunicación con otros sitios 6to4 y 6Bone a través del equipo de puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-214">They will have communication to other 6to4 sites and the 6bone through the gateway computer.</span></span>

## <a name="debugging-6to4-configuration"></a><span data-ttu-id="5f9ad-215">Depuración de la configuración de 6to4</span><span class="sxs-lookup"><span data-stu-id="5f9ad-215">Debugging 6to4 Configuration</span></span>

<span data-ttu-id="5f9ad-216">**Para depurar la configuración de 6to4**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-216">**To debug your 6to4 configuration**</span></span>

1.  <span data-ttu-id="5f9ad-217">Compruebe la conectividad de IPv4 con el enrutador de retransmisión 6to4:</span><span class="sxs-lookup"><span data-stu-id="5f9ad-217">Check your IPv4 connectivity to the 6to4 relay router:</span></span>

    <span data-ttu-id="5f9ad-218">**ping 6to4.ipv6.microsoft.com**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-218">**ping 6to4.ipv6.microsoft.com**</span></span>

    <span data-ttu-id="5f9ad-219">Si se produce un error, no tiene conectividad a Internet global.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-219">If this fails, then you do not have global Internet connectivity.</span></span>

2.  <span data-ttu-id="5f9ad-220">Compruebe la encapsulación de IPv6 mediante la tunelización automática:</span><span class="sxs-lookup"><span data-stu-id="5f9ad-220">Check IPv6 encapsulation by using automatic tunneling:</span></span>

    <span data-ttu-id="5f9ad-221">**ping6:: 131.107.152.32**</span><span class="sxs-lookup"><span data-stu-id="5f9ad-221">**ping6 ::131.107.152.32**</span></span>

    <span data-ttu-id="5f9ad-222">Si se produce un error, es posible que tenga un firewall o un traductor de direcciones de red (NAT) entre el equipo e Internet.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-222">If this fails, then you might have a firewall or network address translator (NAT) between your computer and the Internet.</span></span> <span data-ttu-id="5f9ad-223">Si esto se realiza correctamente, la conexión a Internet puede admitir 6to4.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-223">If this is successful, then your Internet connection can support 6to4.</span></span>

3.  <span data-ttu-id="5f9ad-224">Compruebe la visualización del comando IPv6 RT.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-224">Check the display of the ipv6 rt command.</span></span> <span data-ttu-id="5f9ad-225">Debería ver una ruta 2002::/16-> 2.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-225">You should see a 2002::/16 -> 2 route.</span></span> <span data-ttu-id="5f9ad-226">Compruebe la visualización del comando IPv6 if 2.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-226">Check the display of the ipv6 if 2 command.</span></span> <span data-ttu-id="5f9ad-227">Debería ver una dirección preferida con un prefijo 2002::/16.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-227">You should see a preferred address with a 2002::/16 prefix.</span></span>

> [!Note]  
> <span data-ttu-id="5f9ad-228">La dirección IPv4 del enrutador de retransmisión 6to4 de Microsoft de 131.107.152.32 está sujeta a cambios.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-228">The IPv4 address of the Microsoft 6to4 relay router of 131.107.152.32 is subject to change.</span></span> <span data-ttu-id="5f9ad-229">Si el paso 2 anterior no funciona, Compruebe la salida del comando ping en el paso 1 para comprobar la dirección IPv4 del enrutador de retransmisión 6to4 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-229">If Step 2 above does not work, check the output of the ping command in step 1 to verify the IPv4 address of the Microsoft 6to4 relay router.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5f9ad-230">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f9ad-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f9ad-231">Configuraciones recomendadas para IPv6</span><span class="sxs-lookup"><span data-stu-id="5f9ad-231">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> <dt>

[<span data-ttu-id="5f9ad-232">Subred única con direcciones locales de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f9ad-232">Single subnet with link-local addresses</span></span>](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="5f9ad-233">Usar IPsec entre dos hosts de vínculo local</span><span class="sxs-lookup"><span data-stu-id="5f9ad-233">Using IPsec between two local link hosts</span></span>](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



