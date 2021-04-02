---
description: La primera configuración no requiere ninguna configuración adicional más allá de la instalación del protocolo Microsoft IPv6 Technology Preview.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 'Configuración 1: subred única con direcciones locales de vínculo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d09feb44c222b7213da18a6745fc632f3903209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082124"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a><span data-ttu-id="d6bfb-103">Configuración 1: subred única con direcciones locales de vínculo</span><span class="sxs-lookup"><span data-stu-id="d6bfb-103">Configuration 1: Single Subnet with Link-local Addresses</span></span>

<span data-ttu-id="d6bfb-104">La primera configuración no requiere ninguna configuración adicional más allá de la instalación del protocolo Microsoft IPv6 Technology Preview.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-104">The first configuration requires no additional configuration beyond installing the Microsoft IPv6 Technology Preview protocol.</span></span> <span data-ttu-id="d6bfb-105">Esta configuración consta de al menos dos nodos en la misma subred.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-105">This configuration consists of at least two nodes on the same subnet.</span></span> <span data-ttu-id="d6bfb-106">En la terminología de IPv6, los dos nodos están en el mismo vínculo sin enrutadores intermedios.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-106">In IPv6 terminology, the two nodes are on the same link with no intermediate routers.</span></span>

<span data-ttu-id="d6bfb-107">En la ilustración siguiente se muestra la configuración de dos nodos en una sola subred mediante direcciones locales de vínculo.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-107">The following illustration shows the configuration of two nodes on a single subnet using link-local addresses.</span></span>

![dos nodos que usan direcciones locales de vínculo.](images/v6mig-1.png)

<span data-ttu-id="d6bfb-109">De forma predeterminada, IPv6 configura las direcciones IP locales de vínculo para cada interfaz correspondiente a los adaptadores de red Ethernet instalados.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-109">By default, IPv6 configures link-local IP addresses for each interface corresponding to installed Ethernet network adapters.</span></span> <span data-ttu-id="d6bfb-110">Las direcciones locales de vínculo tienen el prefijo fe80::/64.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-110">Link-local addresses have the prefix fe80::/64.</span></span> <span data-ttu-id="d6bfb-111">Los últimos 64 bits de la dirección IPv6 se conocen como el identificador de interfaz y se derivan de la dirección MAC de 48 bits del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-111">The last 64 bits of the IPv6 address is known as the interface identifier and is derived from the 48-bit MAC address of the network adapter.</span></span>

<span data-ttu-id="d6bfb-112">Para crear el identificador de interfaz IPv6 a partir de la dirección MAC Ethernet de 48 bits (6 bytes):</span><span class="sxs-lookup"><span data-stu-id="d6bfb-112">To create the IPv6 interface identifier from the 48-bit (6-byte) Ethernet MAC address:</span></span>

-   <span data-ttu-id="d6bfb-113">Los dígitos hexadecimales 0xFF-fe se insertan entre el tercer y el cuarto byte de la dirección MAC.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-113">The hex digits 0xff-fe are inserted between the third and fourth byte of the MAC address.</span></span>
-   <span data-ttu-id="d6bfb-114">Se complementa el bit universal/local, el segundo bit de orden inferior del primer byte de la dirección MAC.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-114">The Universal/Local bit, the second low-order bit of the first byte of the MAC address, is complemented.</span></span> <span data-ttu-id="d6bfb-115">Si es 1, se convierte en 0 y si es un 0, se convierte en 1.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-115">If it is a 1, it is turned to 0, and if it is a 0, it is turned to 1.</span></span>

<span data-ttu-id="d6bfb-116">Por ejemplo, para la dirección MAC 00-60-08-52-F9-D8:</span><span class="sxs-lookup"><span data-stu-id="d6bfb-116">For example, for the MAC address 00-60-08-52-f9-d8:</span></span>

-   <span data-ttu-id="d6bfb-117">Los dígitos hexadecimales 0xFF-fe se insertan entre 0x08 (el tercer byte) y 0x52 (el cuarto byte) de la dirección MAC, formando la dirección de 64 bits 00-60-08-FF-fe-52-F9-D8.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-117">The hex digits 0xff-fe are inserted between 0x08 (the third byte) and 0x52 (the fourth byte) of the MAC address, forming the 64-bit address 00-60-08-ff-fe-52-f9-d8.</span></span>
-   <span data-ttu-id="d6bfb-118">El bit universal/local, el segundo bit de orden inferior de 0x00 (el primer byte) de la dirección MAC se complementa.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-118">The Universal/Local bit, the second low-order bit of 0x00 (the first byte) of the MAC address is complemented.</span></span> <span data-ttu-id="d6bfb-119">El segundo bit de orden inferior de 0x00 es 0, que, cuando se complementa, se convierte en 1.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-119">The second low-order bit of 0x00 is 0 which, when complemented, becomes 1.</span></span> <span data-ttu-id="d6bfb-120">El resultado es que para el primer byte, 0x00 se convierte en 0x02.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-120">The result is that for the first byte, 0x00 becomes 0x02.</span></span>

<span data-ttu-id="d6bfb-121">Por lo tanto, el identificador de la interfaz IPv6 correspondiente a la dirección MAC Ethernet de 00-60-08-52-F9-D8 es 02-60-08-FF-fe-52-F9-D8.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-121">Therefore, the IPv6 interface identifier corresponding to the Ethernet MAC address of 00-60-08-52-f9-d8 is 02-60-08-ff-fe-52-f9-d8.</span></span>

<span data-ttu-id="d6bfb-122">La dirección local del vínculo de un nodo es la combinación del prefijo fe80::/64 y el identificador de la interfaz de 64 bits expresado en la notación hexadecimal con dos puntos de IPv6.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-122">The link-local address of a node is the combination of the prefix fe80::/64 and the 64-bit interface identifier expressed in IPv6 colon-hexadecimal notation.</span></span> <span data-ttu-id="d6bfb-123">Por lo tanto, la dirección local del vínculo de este nodo de ejemplo con el prefijo fe80::/64 y el identificador de interfaz 02-60-08-FF-fe-52-F9-D8 es fe80:: 260:8ff: Fe52: F9D8.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-123">Therefore, the link-local address of this example node with the prefix fe80::/64 and the interface identifier 02-60-08-ff-fe-52-f9-d8 is fe80::260:8ff:fe52:f9d8.</span></span>

<span data-ttu-id="d6bfb-124">Puede ver la dirección local del vínculo mediante IPv6 si, tal y como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d6bfb-124">You can view your link local address by using ipv6 if, as demonstrated in the following example:</span></span>

<span data-ttu-id="d6bfb-125">**IPv6 si**</span><span class="sxs-lookup"><span data-stu-id="d6bfb-125">**ipv6 if**</span></span>

``` syntax
Interface 4 (site 1): Local Area Connection
  uses Neighbor Discovery
  link-level address: 00-10-5a-aa-20-a2
    preferred address fe80::210:5aff:feaa:20a2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ffaa:20a2, 1 refs, last reporter
  link MTU 1500 (true link MTU 1500)
  current hop limit 128
  reachable time 43500ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 3 (site 1): 6-over-4 Virtual Interface
  uses Neighbor Discovery
  link-level address: 10.0.0.2
    preferred address fe80::a00:2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ff00:2, 1 refs, last reporter
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 34000ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 2 (site 0): Tunnel Pseudo-Interface
  does not use Neighbor Discovery
  link-level address: 0.0.0.0
    preferred address ::10.0.0.2, infinite/infinite
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
Interface 1 (site 0): Loopback Pseudo-Interface
  does not use Neighbor Discovery
  link-level address:
    preferred address ::1, infinite/infinite
  link MTU 1500 (true link MTU 1500)
  current hop limit 1
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
```

<span data-ttu-id="d6bfb-126">La interfaz 4 es una interfaz que corresponde a un adaptador Ethernet instalado con una dirección local de vínculo de fe80:: 210:5AfF: feaa: 20a2.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-126">Interface 4 is an interface corresponding to an installed Ethernet adapter with a link-local address of fe80::210:5aff:feaa:20a2.</span></span>

<span data-ttu-id="d6bfb-127">Para obtener más información sobre el direccionamiento IPv6 y una introducción a los conceptos de IPv6, consulte las notas del producto Introducción a IPv6.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-127">For more information on IPv6 addressing and an overview of IPv6 concepts, see the Introduction to IPv6 white paper.</span></span>

## <a name="testing-connectivity-between-two-link-local-hosts"></a><span data-ttu-id="d6bfb-128">Probar la conectividad entre dos hosts locales de vínculo</span><span class="sxs-lookup"><span data-stu-id="d6bfb-128">Testing Connectivity Between Two Link-local Hosts</span></span>

<span data-ttu-id="d6bfb-129">Puede realizar un ping sencillo (un intercambio de mensajes de solicitud de eco ICMPv6 y de respuesta de eco) mediante IPv6 entre dos hosts locales de vínculo.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-129">You can do a simple ping (an exchange of ICMPv6 Echo Request and Echo Reply messages) using IPv6 between two link-local hosts.</span></span>

<span data-ttu-id="d6bfb-130">**Para hacer ping mediante IPv6 entre dos hosts locales de vínculo**</span><span class="sxs-lookup"><span data-stu-id="d6bfb-130">**To ping using IPv6 between two link-local hosts**</span></span>

1.  <span data-ttu-id="d6bfb-131">Instale Microsoft IPv6 Technology Preview para Windows en dos hosts de Windows (el host A y el host B) que se encuentran en el mismo vínculo (subred).</span><span class="sxs-lookup"><span data-stu-id="d6bfb-131">Install the Microsoft IPv6 Technology Preview for Windows on two Windows hosts (Host A and Host B) that are on the same link (subnet).</span></span>
2.  <span data-ttu-id="d6bfb-132">Use IPv6 si en el host a para obtener la dirección local del vínculo para la interfaz Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-132">Use ipv6 if on Host A to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="d6bfb-133">Ejemplo: la dirección local del vínculo del host A es fe80:: 210:5AfF: feaa: 20a2.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-133">Example: The link-local address of Host A is fe80::210:5aff:feaa:20a2.</span></span>

3.  <span data-ttu-id="d6bfb-134">Use IPv6 si en el host B para obtener la dirección local del vínculo para la interfaz Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-134">Use ipv6 if on Host B to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="d6bfb-135">Ejemplo: la dirección local del vínculo del host B es fe80:: 260:97ff: fe02:6ea5.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-135">Example: The link-local address of Host B is fe80::260:97ff:fe02:6ea5.</span></span>

4.  <span data-ttu-id="d6bfb-136">Desde el host A, haga ping al host B mediante Ping6.exe.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-136">From Host A, ping Host B using Ping6.exe.</span></span>

    <span data-ttu-id="d6bfb-137">Ejemplo: ping6 fe80:: 260:97ff: fe02:6ea5</span><span class="sxs-lookup"><span data-stu-id="d6bfb-137">Example: ping6 fe80::260:97ff:fe02:6ea5</span></span>

<span data-ttu-id="d6bfb-138">Para especificar la dirección de origen desde la que se envían los mensajes de solicitud de eco, también puede usar la opción Ping6.exe-s.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-138">To specify the source address from which the Echo Request messages are sent, you can also use the Ping6.exe -s option.</span></span> <span data-ttu-id="d6bfb-139">Por ejemplo, para enviar solicitudes de eco al host B desde la dirección IPv6 de fe80:: 210:5AfF: feaa: 20a2, use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="d6bfb-139">For example, to send Echo Requests to Host B from the IPv6 address of fe80::210:5aff:feaa:20a2, use the following command:</span></span>

<span data-ttu-id="d6bfb-140">**ping6-s fe80:: 210:5AfF: feaa: 20a2% 4 fe80:: 260:97ff: fe02:6ea5**</span><span class="sxs-lookup"><span data-stu-id="d6bfb-140">**ping6 -s fe80::210:5aff:feaa:20a2%4 fe80::260:97ff:fe02:6ea5**</span></span>

<span data-ttu-id="d6bfb-141">Al hacer ping a una dirección local de vínculo o local de sitio, se recomienda especificar el identificador de ámbito para que la dirección de destino no sea ambigua.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-141">When pinging a link-local or site-local address, it is recommended to specify the scope-ID to make the destination address unambiguous.</span></span> <span data-ttu-id="d6bfb-142">La notación para especificar el identificador de ámbito es dirección% de identificador de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-142">The notation to specify the scope-ID is address%scope-ID.</span></span> <span data-ttu-id="d6bfb-143">En el caso de las direcciones locales de vínculo, el identificador de ámbito es igual al número de interfaz, tal y como se muestra en el comando IPv6 if.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-143">For link-local addresses, the scope-ID is equal to the interface number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="d6bfb-144">En el caso de las direcciones locales del sitio, el identificador de ámbito es igual al número de sitio que se muestra en el comando IPv6 if.</span><span class="sxs-lookup"><span data-stu-id="d6bfb-144">For site-local addresses, the scope-ID is equal to the site number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="d6bfb-145">Por ejemplo, para enviar mensajes de solicitud de eco al host B mediante el identificador de ámbito 4, use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="d6bfb-145">For example, to send Echo Request messages to Host B using scope-ID 4, use the following command:</span></span>

<span data-ttu-id="d6bfb-146">**ping6 fe80:: 260:97ff: fe02:6ea5% 4**</span><span class="sxs-lookup"><span data-stu-id="d6bfb-146">**ping6 fe80::260:97ff:fe02:6ea5%4**</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6bfb-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d6bfb-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6bfb-148">Configuraciones recomendadas para IPv6</span><span class="sxs-lookup"><span data-stu-id="d6bfb-148">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> </dl>

 

 



