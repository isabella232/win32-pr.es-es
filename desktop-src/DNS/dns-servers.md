---
title: Servidores DNS
description: Un servidor DNS es un equipo que completa el proceso de resolución de nombres en DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Servidores DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509ceeb811f221560540ae60f269c6ee1b05444f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777778"
---
# <a name="dns-servers"></a><span data-ttu-id="a6eb6-104">Servidores DNS</span><span class="sxs-lookup"><span data-stu-id="a6eb6-104">DNS Servers</span></span>

<span data-ttu-id="a6eb6-105">Un *servidor DNS* es un equipo que completa el proceso de resolución de nombres en DNS.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-105">A *DNS Server* is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="a6eb6-106">Los servidores DNS contienen [*archivos de zona*](z-gly.md) que les permiten resolver nombres en direcciones IP y direcciones IP en nombres.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-106">DNS Servers contain [*zone files*](z-gly.md) that enable them to resolve names to IP addresses and IP addresses to names.</span></span> <span data-ttu-id="a6eb6-107">Cuando se consulta, un servidor DNS responderá de una de estas tres maneras:</span><span class="sxs-lookup"><span data-stu-id="a6eb6-107">When queried, a DNS Server will respond in one of three ways:</span></span>

-   <span data-ttu-id="a6eb6-108">El servidor devuelve los datos solicitados de resolución de nombres o resolución IP.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-108">The server returns the requested name-resolution or IP-resolution data.</span></span>
-   <span data-ttu-id="a6eb6-109">El servidor devuelve un puntero a otro servidor DNS que puede atender la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="a6eb6-110">El servidor indica que no tiene los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-110">The server indicates that it does not have the requested data.</span></span>

<span data-ttu-id="a6eb6-111">Los servidores DNS podrían, durante el transcurso de la preparación de devolver los datos de resolución solicitados, consultar otros servidores DNS, pero más allá de eso, los servidores DNS no realizan ninguna otra operación.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-111">DNS Servers might, during the course of preparing to return the requested resolution data, query other DNS Servers, but beyond that, DNS Servers do not perform any other operations.</span></span>

<span data-ttu-id="a6eb6-112">Hay tres tipos principales de servidores DNS: los servidores principales, los servidores secundarios y los servidores de almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span>

## <a name="primary-server"></a><span data-ttu-id="a6eb6-113">Servidor principal</span><span class="sxs-lookup"><span data-stu-id="a6eb6-113">Primary Server</span></span>

<span data-ttu-id="a6eb6-114">El *servidor principal* es el servidor autoritativo para la zona.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-114">The *primary server* is the authoritative server for the zone.</span></span> <span data-ttu-id="a6eb6-115">Todas las tareas administrativas asociadas a la zona (por ejemplo, la creación de subdominios dentro de la zona u otras tareas administrativas similares) deben realizarse en el servidor principal.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-115">All administrative tasks associated with the zone (such as creating subdomains within the zone, or other similar administrative tasks) must be performed on the primary server.</span></span> <span data-ttu-id="a6eb6-116">Además, los cambios asociados a la zona o las modificaciones o adiciones a los RRs en los archivos de zona deben realizarse en el servidor principal.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-116">In addition, any changes associated with the zone or any modifications or additions to RRs in the zone files must be made on the primary server.</span></span> <span data-ttu-id="a6eb6-117">En el caso de una zona determinada, hay un servidor principal, excepto cuando se integra Active Directory Services y el servidor DNS de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-117">For any given zone, there is one primary server, except when you integrate Active Directory services and Microsoft DNS Server.</span></span>

## <a name="secondary-servers"></a><span data-ttu-id="a6eb6-118">Servidores secundarios</span><span class="sxs-lookup"><span data-stu-id="a6eb6-118">Secondary Servers</span></span>

<span data-ttu-id="a6eb6-119">*Los servidores secundarios* son servidores DNS de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-119">*Secondary servers* are backup DNS Servers.</span></span> <span data-ttu-id="a6eb6-120">Los servidores secundarios reciben todos sus archivos de zona de los archivos de zona del servidor principal en una transferencia de zona.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-120">Secondary servers receive all of their zone files from the primary server zone files in a zone transfer.</span></span> <span data-ttu-id="a6eb6-121">Pueden existir varios servidores secundarios para cualquier zona determinada, tanto como sea necesario para proporcionar [*equilibrio de carga*](l-gly.md), [*tolerancia a errores*](f-gly.md)y reducción del tráfico.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-121">Multiple secondary servers can exist for any given zone — as many as necessary to provide [*load balancing*](l-gly.md), [*fault tolerance*](f-gly.md), and traffic reduction.</span></span> <span data-ttu-id="a6eb6-122">Además, cualquier servidor DNS determinado puede ser un servidor secundario para varias zonas.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-122">Additionally, any given DNS Server can be a secondary server for multiple zones.</span></span>

<span data-ttu-id="a6eb6-123">Además de los servidores DNS principal y secundario, se pueden usar roles de servidor DNS adicionales cuando dichos servidores sean adecuados para una infraestructura DNS.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-123">In addition to primary and secondary DNS Servers, additional DNS Server roles can be used when such servers are appropriate for a DNS infrastructure.</span></span> <span data-ttu-id="a6eb6-124">Estos servidores adicionales son servidores de almacenamiento en caché y [*reenviadores*](f-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a6eb6-124">These additional servers are caching servers and [*forwarders*](f-gly.md).</span></span>

## <a name="caching-servers"></a><span data-ttu-id="a6eb6-125">Servidores de almacenamiento en caché</span><span class="sxs-lookup"><span data-stu-id="a6eb6-125">Caching Servers</span></span>

<span data-ttu-id="a6eb6-126">[*Los servidores de almacenamiento en caché*](c-gly.md), también conocidos como servidores de solo almacenamiento en caché, realizan como su nombre sugiere; solo proporcionan el servicio de consulta en caché para las respuestas DNS.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-126">[*Caching servers*](c-gly.md), also known as caching-only servers, perform as their name suggests; they provide only cached-query service for DNS responses.</span></span> <span data-ttu-id="a6eb6-127">En lugar de mantener archivos de zona como otros servidores secundarios, los servidores DNS de almacenamiento en caché realizan consultas, almacenan en caché las respuestas y devuelven los resultados al cliente que realiza la consulta.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-127">Rather than maintaining zone files like other secondary servers do, caching DNS Servers perform queries, cache the answers, and return the results to the querying client.</span></span> <span data-ttu-id="a6eb6-128">La principal diferencia entre los servidores de almacenamiento en caché y otros servidores secundarios es que otros servidores secundarios mantienen archivos de zona (y realizan transferencias de zona cuando es adecuado, lo que genera tráfico de red asociado a la transferencia), no los servidores de almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="a6eb6-128">The primary difference between caching servers and other secondary servers is that other secondary servers maintain zone files (and do zone transfers when appropriate, thereby generating network traffic associated with the transfer), caching servers do not.</span></span>

 

 




