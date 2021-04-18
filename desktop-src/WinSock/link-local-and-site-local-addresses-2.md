---
description: Las direcciones locales de vínculo IPv6 y de sitio se denominan direcciones de ámbito.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: Dirección local de vínculo IPv6 y direcciones locales de sitio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80b8e201adf382b10dd31fe5607de903d6c588
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705605"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a><span data-ttu-id="a89a3-103">Dirección local de vínculo IPv6 y direcciones locales de sitio</span><span class="sxs-lookup"><span data-stu-id="a89a3-103">IPv6 Link-local and Site-local Addresses</span></span>

<span data-ttu-id="a89a3-104">Las direcciones locales de vínculo IPv6 y de sitio se denominan direcciones de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a89a3-104">IPv6 link-local and site-local addresses are called scoped addresses.</span></span> <span data-ttu-id="a89a3-105">La API de Windows Sockets (Winsock) admite el miembro de **\_ \_ identificador de ámbito sin6** en la estructura [**\_ IN6 de sockaddr**](sockaddr-2.md) para su uso con direcciones de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a89a3-105">The Windows Sockets (Winsock) API supports the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure for use with scoped addresses.</span></span> <span data-ttu-id="a89a3-106">En el caso de las direcciones locales de vínculo (fe80::/10 prefijo), el miembro de **\_ \_ identificador de ámbito sin6** de la estructura **sockaddr \_ IN6** es el número de interfaz.</span><span class="sxs-lookup"><span data-stu-id="a89a3-106">For IPv6 link-local addresses (fe80::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is the interface number.</span></span> <span data-ttu-id="a89a3-107">En el caso de las direcciones locales del sitio IPv6 (prefijo FEC0::/10), el miembro **\_ \_ ID. de ámbito sin6** de la estructura **sockaddr \_ IN6** es un identificador de sitio.</span><span class="sxs-lookup"><span data-stu-id="a89a3-107">For IPv6 site-local addresses (fec0::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is a site identifier.</span></span>

<span data-ttu-id="a89a3-108">Un ejemplo de una dirección IPv6 local de vínculo en \# la interfaz 5 es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="a89a3-108">An example of a link-local IPv6 address on interface \#5 is the following:</span></span>

``` syntax
fe80::208:74ff:feda:625c%5
```

<span data-ttu-id="a89a3-109">El siguiente comando está disponible en Windows XP con Service Pack 1 (SP1) y versiones posteriores para consultar y configurar IPv6 en un equipo local:</span><span class="sxs-lookup"><span data-stu-id="a89a3-109">The following command is available on Windows XP with Service Pack 1 (SP1) and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="a89a3-110">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="a89a3-110">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="a89a3-111">Los cambios de configuración realizados con los comandos Netsh.exe son permanentes y no se pierden cuando se reinicia el equipo o el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="a89a3-111">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="a89a3-112">Antes de Windows XP con Service Pack 1 (SP1), la configuración y administración de IPv6 usaba varias herramientas de línea de comandos anteriores (Net.exe, Ipv6.exe y Ipsec6.exe) para configurar y administrar IPv6.</span><span class="sxs-lookup"><span data-stu-id="a89a3-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools (Net.exe, Ipv6.exe, and Ipsec6.exe) to configure and manage IPv6.</span></span> <span data-ttu-id="a89a3-113">Con estas herramientas anteriores, los cambios de IPv6 no son permanentes y se pierden cuando se reinició el equipo o el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="a89a3-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span> <span data-ttu-id="a89a3-114">Estas herramientas de línea de comandos anteriores solo se admiten en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a89a3-114">These older command-line tools are only supported on Windows XP.</span></span>

<span data-ttu-id="a89a3-115">En Windows XP con SP1, el siguiente comando mostrará la lista de interfaces IPv6 en un equipo local, incluidos el índice de la interfaz, el nombre de la interfaz y otras propiedades de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="a89a3-115">On Windows XP with SP1, the following command will display the list of IPv6 interfaces on a local computer including the interface index, the interface name, and various other interface properties.</span></span>

<span data-ttu-id="a89a3-116">**netsh interface ipv6 show interface**</span><span class="sxs-lookup"><span data-stu-id="a89a3-116">**netsh interface ipv6 show interface**</span></span>

<span data-ttu-id="a89a3-117">En Windows XP con SP1, el siguiente comando cambiará el identificador de sitio asociado a un índice de interfaz.</span><span class="sxs-lookup"><span data-stu-id="a89a3-117">On Windows XP with SP1, the following command will change the site identifier associated with an interface index.</span></span>

<span data-ttu-id="a89a3-118">**netsh interface ipv6 set interface <InterfaceIndex or Name> siteID = valor**</span><span class="sxs-lookup"><span data-stu-id="a89a3-118">**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid=value**</span></span>

<span data-ttu-id="a89a3-119">En Windows XP, el siguiente comando anterior también cambiará el identificador del sitio asociado a una dirección local del sitio a 3.</span><span class="sxs-lookup"><span data-stu-id="a89a3-119">On Windows XP, the following older command will also change the site identifier associated with a site-local address to 3.</span></span>

<span data-ttu-id="a89a3-120">**fec0 de RTU de IPv6::/10 3**</span><span class="sxs-lookup"><span data-stu-id="a89a3-120">**ipv6 rtu fec0::/10 3**</span></span>

<span data-ttu-id="a89a3-121">Si está enviando o conectándose a una dirección de ámbito, el miembro **de \_ \_ identificador de ámbito sin6** en la estructura [**\_ IN6 de sockaddr**](sockaddr-2.md) se puede dejar sin especificar (cero), lo que representa una dirección de ámbito ambiguo.</span><span class="sxs-lookup"><span data-stu-id="a89a3-121">If you are sending or connecting to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure can be left unspecified (zero) which represents an ambiguous scoped address.</span></span> <span data-ttu-id="a89a3-122">Por ejemplo, la siguiente dirección local de vínculo es ambigua:</span><span class="sxs-lookup"><span data-stu-id="a89a3-122">For example, the following link-local address is ambiguous:</span></span>

``` syntax
fe80::10
```

<span data-ttu-id="a89a3-123">Si va a enlazar a una dirección de ámbito, el miembro de **\_ \_ identificador de ámbito sin6** en la estructura [**\_ IN6 de sockaddr**](sockaddr-2.md) debe contener un valor distinto de cero que especifique un número de interfaz válido para una dirección local de vínculo o un identificador de sitio para una dirección local del sitio.</span><span class="sxs-lookup"><span data-stu-id="a89a3-123">If you are binding to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure must contain a nonzero value that specifies a valid interface number for a link-local address or a site identifier for a site-local address.</span></span>

## <a name="ambiguous-scoped-addresses"></a><span data-ttu-id="a89a3-124">Direcciones con ámbito ambiguo</span><span class="sxs-lookup"><span data-stu-id="a89a3-124">Ambiguous Scoped Addresses</span></span>

<span data-ttu-id="a89a3-125">Si está enviando o conectándose a una dirección de ámbito y no ha especificado el miembro de **\_ \_ identificador de ámbito sin6** en la estructura [**\_ IN6 de sockaddr**](sockaddr-2.md) , la dirección de ámbito es ambigua.</span><span class="sxs-lookup"><span data-stu-id="a89a3-125">If you are sending or connecting to a scoped address and have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, then the scoped address is ambiguous.</span></span> <span data-ttu-id="a89a3-126">Para resolver este comportamiento, el protocolo IPv6 determina primero si el socket se ha enlazado a una dirección de origen.</span><span class="sxs-lookup"><span data-stu-id="a89a3-126">To resolve this, the IPv6 protocol first determines whether you have bound the socket to a source address.</span></span> <span data-ttu-id="a89a3-127">Si es así, la dirección de origen enlazada resuelve la ambigüedad proporcionando un número de interfaz o un identificador de sitio.</span><span class="sxs-lookup"><span data-stu-id="a89a3-127">If so, the bound source address resolves the ambiguity by supplying an interface number or site identifier.</span></span>

<span data-ttu-id="a89a3-128">Si se envía o se conecta a una dirección de ámbito y no se especifica el miembro de **\_ \_ identificador de ámbito sin6** ni se enlaza una dirección de origen, el protocolo IPv6 comprueba la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="a89a3-128">If you are sending or connecting to a scoped address and have neither specified the **sin6\_scope\_id** member nor bound a source address, then the IPv6 protocol checks the routing table.</span></span> <span data-ttu-id="a89a3-129">Por ejemplo, el siguiente comando mostrará la tabla de enrutamiento IPv6 en un equipo local:</span><span class="sxs-lookup"><span data-stu-id="a89a3-129">For example, the following command will display the IPv6 routing table on a local computer:</span></span>

<span data-ttu-id="a89a3-130">**netsh interface ipv6 show route**</span><span class="sxs-lookup"><span data-stu-id="a89a3-130">**netsh interface ipv6 show route**</span></span>

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

<span data-ttu-id="a89a3-131">Esto indica que las direcciones locales de vínculo se tratan como en vínculo a la interfaz \# 13 y \# 14 de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a89a3-131">This indicates that link-local addresses are treated as on-link to interface \#13 and \#14 by default.</span></span>

<span data-ttu-id="a89a3-132">La ambigüedad se produce cuando un equipo local tiene varios adaptadores de red.</span><span class="sxs-lookup"><span data-stu-id="a89a3-132">Ambiguity arises when a local computer has multiple network adapters.</span></span> <span data-ttu-id="a89a3-133">Por ejemplo, el comando **netsh** anterior indica que hay dos interfaces de red (conexión de área local y conexión de red inalámbrica).</span><span class="sxs-lookup"><span data-stu-id="a89a3-133">For example, the **netsh** command above indicates there are two network interfaces (Local Area Connection and Wireless Network Connection).</span></span> <span data-ttu-id="a89a3-134">Cuando una aplicación especifica una dirección local de vínculo de destino (fe80:: 10, por ejemplo) sin un identificador de ámbito, no queda claro qué adaptador usar para enviar el paquete.</span><span class="sxs-lookup"><span data-stu-id="a89a3-134">When an application specifies a destination link-local address (fe80::10, for example) without a scope ID, it is not clear which adapter to use to send the packet.</span></span> <span data-ttu-id="a89a3-135">Solo una unidifusión local de vínculo (fe80::/64) o una dirección de destino IPv6 de multidifusión del ámbito de vínculo (ff00::/8) pueden verse en que no tienen un identificador de ámbito al enviar un paquete.</span><span class="sxs-lookup"><span data-stu-id="a89a3-135">Only a link-local unicast (fe80::/64) or a link-scope multicast (ff00::/8) IPv6 destination address can suffer from not having a scope ID when sending a packet.</span></span>

## <a name="neighbor-discovery"></a><span data-ttu-id="a89a3-136">Detección de equipos cercanos</span><span class="sxs-lookup"><span data-stu-id="a89a3-136">Neighbor Discovery</span></span>

<span data-ttu-id="a89a3-137">Si no ha especificado el miembro **de \_ \_ identificador de ámbito sin6** en la estructura [**\_ IN6 de sockaddr**](sockaddr-2.md) , no ha enlazado una dirección de origen y no ha especificado una ruta para las direcciones locales del vínculo, el protocolo IPv6 probará la detección de vecinos para resolver la dirección local del vínculo de destino.</span><span class="sxs-lookup"><span data-stu-id="a89a3-137">If you have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, have not bound a source address, and have not specified a route for link-local addresses, then the IPv6 protocol will try Neighbor Discovery to resolve the destination link-local address.</span></span> <span data-ttu-id="a89a3-138">Para un paquete determinado que se está enviando, se intenta una interfaz.</span><span class="sxs-lookup"><span data-stu-id="a89a3-138">For a given packet being sent, one interface is tried.</span></span> <span data-ttu-id="a89a3-139">Esta primera interfaz que se intenta se considera la interfaz más preferida.</span><span class="sxs-lookup"><span data-stu-id="a89a3-139">This first interface that is tried is considered the most preferred interface.</span></span> <span data-ttu-id="a89a3-140">Si la detección de vecinos no puede resolver la dirección local del vínculo en una interfaz, se quita el paquete que se va a enviar y el sistema recuerda que no se puede tener acceso a la dirección local del vínculo de destino a través de esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="a89a3-140">If Neighbor Discovery fails to resolve the link-local address on an interface, the packet to be sent is dropped and the system remembers that the destination link-local address is not reachable over that interface.</span></span> <span data-ttu-id="a89a3-141">En el siguiente paquete que se va a enviar en todas las condiciones, se intenta una interfaz diferente para la detección de vecinos.</span><span class="sxs-lookup"><span data-stu-id="a89a3-141">On the next packet to be sent under all of the same conditions, a different interface is tried for Neighbor Discovery.</span></span> <span data-ttu-id="a89a3-142">Este proceso continúa a través de cada una de las interfaces en un equipo local para cada nuevo paquete hasta que la detección de vecinos responde a la dirección local del vínculo de destino o se han intentado todas las interfaces posibles.</span><span class="sxs-lookup"><span data-stu-id="a89a3-142">This process continues through each of the interfaces on a local computer for each new packet until Neighbor Discovery responds for the destination link-local address or all of the possible interfaces have been tried and failed.</span></span> <span data-ttu-id="a89a3-143">Cada vez que se produce un error al intentar resolver el vecino, se elimina una interfaz para ese vecino.</span><span class="sxs-lookup"><span data-stu-id="a89a3-143">Each time an attempt to resolve the neighbor fails, one interface is eliminated for that neighbor.</span></span>

<span data-ttu-id="a89a3-144">Si se resuelve la dirección local del vínculo de destino, esa interfaz se utiliza para enviar el paquete actual.</span><span class="sxs-lookup"><span data-stu-id="a89a3-144">If the destination link-local address resolves, then that interface is used to send the current packet.</span></span> <span data-ttu-id="a89a3-145">Esta interfaz también se utiliza para los paquetes posteriores de ámbito ambiguo que se envían a la misma dirección de destino local de vínculo.</span><span class="sxs-lookup"><span data-stu-id="a89a3-145">This interface is also used for any subsequent ambiguously-scoped packets that are sent to the same link-local destination address.</span></span>

<span data-ttu-id="a89a3-146">Si la detección de vecinos no puede resolver la dirección local del vínculo de destino en todas las interfaces, el sistema intenta enviar el paquete en la interfaz más preferida (la primera interfaz que se ha intentado).</span><span class="sxs-lookup"><span data-stu-id="a89a3-146">If Neighbor Discovery fails to resolve the destination link-local address on all interfaces, the system then tries to send the packet on the most preferred interface (the first interface tried).</span></span> <span data-ttu-id="a89a3-147">La pila de red sigue intentando resolver la dirección local del vínculo de destino en la interfaz más preferida.</span><span class="sxs-lookup"><span data-stu-id="a89a3-147">The network stack keeps trying to resolve the destination link-local address on the most preferred interface.</span></span> <span data-ttu-id="a89a3-148">Después de un período de tiempo después de que se haya producido un error en la detección de vecinos en todas las interfaces, la pila de red reiniciará el proceso de nuevo e intentará resolver la dirección local del vínculo de destino en todas las interfaces.</span><span class="sxs-lookup"><span data-stu-id="a89a3-148">After a period of time after Neighbor Discovery has failed on all interfaces, the network stack will restart the process again and try to resolve the destination link-local address on all of the interfaces.</span></span> <span data-ttu-id="a89a3-149">Actualmente, este intervalo de tiempo cuando se intenta de nuevo la detección de vecinos en todas las interfaces es de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="a89a3-149">Currently, this time interval when Neighbor Discovery is again tried on all interfaces is 60 seconds.</span></span> <span data-ttu-id="a89a3-150">Sin embargo, este intervalo de tiempo puede cambiar en las versiones de Windows y no debe ser asumida por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="a89a3-150">However, this time interval may change on versions of Windows and should not be assumed by an application.</span></span>

> [!Note]  
> <span data-ttu-id="a89a3-151">Si una aplicación enlaza la misma dirección local de vínculo a una interfaz diferente después de que la detección de vecinos haya resuelto la dirección local del vínculo, no invalidará la interfaz con la dirección de destino local de vínculo devuelta por la detección de vecinos.</span><span class="sxs-lookup"><span data-stu-id="a89a3-151">If an application binds the same link-local address to a different interface after Neighbor Discovery has resolved the link-local address, that will not override the interface with the link-local destination address returned by Neighbor Discovery.</span></span>

 

<span data-ttu-id="a89a3-152">Para obtener más información sobre la detección de vecinos para IP versión 6, consulte [RFC4861](https://tools.ietf.org/html/rfc4861) publicado por IETF.</span><span class="sxs-lookup"><span data-stu-id="a89a3-152">For more information on Neighbor Discovery for IP version 6, see [RFC4861](https://tools.ietf.org/html/rfc4861) published by the IETF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a89a3-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a89a3-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a89a3-154">Prefijos de sitio IPv6</span><span class="sxs-lookup"><span data-stu-id="a89a3-154">IPv6 Site Prefixes</span></span>](site-prefixes-2.md)
</dt> <dt>

[<span data-ttu-id="a89a3-155">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="a89a3-155">Ipv6.exe</span></span>](ipv6-exe-2.md)
</dt> <dt>

[<span data-ttu-id="a89a3-156">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="a89a3-156">Netsh.exe</span></span>](netsh-exe.md)
</dt> <dt>

[<span data-ttu-id="a89a3-157">Usar IPv6</span><span class="sxs-lookup"><span data-stu-id="a89a3-157">Using IPv6</span></span>](using-ipv6-2.md)
</dt> </dl>

 

 



