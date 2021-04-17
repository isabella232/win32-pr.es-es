---
description: En este tema se tratan las consideraciones de programación específicas al usar la infraestructura del mismo nivel.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Consideraciones de programación (punto a punto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89956cbdbbc8d2ed89226a490bbae505862ab18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667385"
---
# <a name="programming-considerations-peer-to-peer"></a><span data-ttu-id="d1fe4-103">Consideraciones de programación (punto a punto)</span><span class="sxs-lookup"><span data-stu-id="d1fe4-103">Programming Considerations (Peer-to-Peer)</span></span>

<span data-ttu-id="d1fe4-104">En este tema se tratan las consideraciones de programación específicas al usar la infraestructura del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-104">This topic discusses specific programming considerations when using the Peer Infrastructure.</span></span>

<span data-ttu-id="d1fe4-105">Al usar la infraestructura del mismo nivel para desarrollar aplicaciones del mismo nivel, debe tener en cuenta las siguientes consideraciones de programación:</span><span class="sxs-lookup"><span data-stu-id="d1fe4-105">When using the Peer Infrastructure to develop peer applications, you must take the following programming considerations into account:</span></span>

-   <span data-ttu-id="d1fe4-106">IPv6</span><span class="sxs-lookup"><span data-stu-id="d1fe4-106">IPv6</span></span>

    <span data-ttu-id="d1fe4-107">La infraestructura del mismo nivel requiere que IPv6 esté instalado e iniciado para permitir que funcionen las aplicaciones de redes del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-107">The Peer Infrastructure requires that IPv6 be installed and started to enable peer networking applications to function.</span></span>

-   <span data-ttu-id="d1fe4-108">Puertos de Firewall</span><span class="sxs-lookup"><span data-stu-id="d1fe4-108">Firewall Ports</span></span>

    <span data-ttu-id="d1fe4-109">Cuando se usa un firewall en una red (como el Firewall de conexión a Internet IPv6), se deben abrir puertos específicos para permitir que la infraestructura del mismo nivel funcione.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-109">When a firewall is being used on a network (such as the IPv6 Internet Connection firewall), specific ports must be opened to allow the Peer Infrastructure to function.</span></span> <span data-ttu-id="d1fe4-110">Los siguientes puertos deben estar abiertos:</span><span class="sxs-lookup"><span data-stu-id="d1fe4-110">The following ports must be open:</span></span>

    <span data-ttu-id="d1fe4-111">Puerto TCP 3587 para la infraestructura de agrupación del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-111">TCP port 3587 for the Peer Grouping Infrastructure.</span></span>

    <span data-ttu-id="d1fe4-112">Puerto UDP 3540 para la infraestructura de gráficos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-112">UDP port 3540 for the Peer Graphing Infrastructure.</span></span>

    > [!Note]  
    > <span data-ttu-id="d1fe4-113">Las aplicaciones que usan la infraestructura de gráficos del mismo nivel en TCP eligen su propio puerto TCP al llamar a [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span><span class="sxs-lookup"><span data-stu-id="d1fe4-113">Applications that use the Peer Graphing Infrastructure over TCP choose their own TCP port when calling [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span></span>

     

-   <span data-ttu-id="d1fe4-114">Opción de socket</span><span class="sxs-lookup"><span data-stu-id="d1fe4-114">Socket Option</span></span>

    <span data-ttu-id="d1fe4-115">Al intentar conectarse a otros nodos IPv6 del mismo nivel directamente (sin usar la infraestructura del mismo nivel), asegúrese de que la opción de socket \_ nivel de protección IPv6 \_ está establecida en **nivel de protección \_ \_ sin restricciones**.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-115">When attempting to connect to other IPv6 peer nodes directly (without using the Peer Infrastructure), ensure that the socket option IPV6\_PROTECTION\_LEVEL is set to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

-   <span data-ttu-id="d1fe4-116">Ancho de banda</span><span class="sxs-lookup"><span data-stu-id="d1fe4-116">Bandwidth</span></span>

    <span data-ttu-id="d1fe4-117">Cuando se usa PNRP, una aplicación puede publicar uno o más [nombres del mismo nivel](peer-names.md) que se pueden resolver.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-117">When using PNRP, an application can publish one or more [peer names](peer-names.md) that can be resolved.</span></span> <span data-ttu-id="d1fe4-118">Para cada nombre del mismo nivel registrado con PNRP, existe un aumento en el ancho de banda de red que usa PNRP para publicar el nombre del mismo nivel y mantenerlo disponible para ser resuelto por otros nodos.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-118">For each peer name registered with PNRP, there is an increase in the network bandwidth that PNRP uses to publish the peer name, and keep it available to be resolved by other nodes.</span></span>

    <span data-ttu-id="d1fe4-119">Para evitar el uso de demasiado ancho de banda, las aplicaciones deben evitar el registro de un gran número de nombres de mismo nivel en un equipo.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-119">To prevent using too much bandwidth, applications should avoid registering large numbers of peer names on a computer.</span></span> <span data-ttu-id="d1fe4-120">Por ejemplo, una aplicación que publica imágenes no debe crear un nombre de mismo nivel para cada imagen, sino que debe crear un nombre del mismo nivel para el servicio que publica imágenes, y usar un protocolo diferente para que los clientes consulten imágenes específicas en el servicio.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-120">For example, an application that publishes pictures should not create a peer name for each picture, but should create one peer name for the service that publishes pictures, and use a different protocol for clients to query the service for specific pictures.</span></span>

-   <span data-ttu-id="d1fe4-121">Registro de nombre del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="d1fe4-121">Peer Name Registration</span></span>

    <span data-ttu-id="d1fe4-122">Es posible que se necesiten algunas aplicaciones para registrar el mismo [nombre del mismo nivel](peer-names.md) en más de un equipo.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-122">Some applications may be required to register the same [peer name](peer-names.md) on more than one computer.</span></span> <span data-ttu-id="d1fe4-123">Normalmente, esto sucede si un nombre del mismo nivel está asociado a una persona que usa más de un equipo.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-123">Typically, this happens if a peer name is associated with a person who uses more than one computer.</span></span> <span data-ttu-id="d1fe4-124">Un método que puede usar para registrar el mismo nombre del mismo nivel en varios equipos es crear un grupo del mismo nivel para la persona y conectarse a ese grupo desde todos los equipos.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-124">One method that you can use to register the same peer name on multiple computers is to create a peer group for the person, and connect to that group from all computers.</span></span> <span data-ttu-id="d1fe4-125">Otro método consiste en crear una identidad del mismo nivel y el nombre del mismo nivel en un equipo, exportar la identidad del mismo nivel desde ese equipo e importarlo en otros equipos.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-125">Another method is to create a peer identity and peer name on one computer, export the peer identity from that computer, and import it on other computers.</span></span> <span data-ttu-id="d1fe4-126">Esto permite crear el mismo nombre seguro del mismo nivel en todos los equipos que han importado la identidad del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-126">This allows the same secure peer name to be created on all the computers that have imported the peer identity.</span></span>

 

 



