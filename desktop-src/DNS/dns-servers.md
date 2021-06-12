---
title: Servidores DNS
description: Obtenga información sobre los servidores DNS. Un servidor DNS es un equipo que completa el proceso de resolución de nombres en DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Servidores DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe2415c50cdd2472b20e8f14123afa2aa919d26
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011258"
---
# <a name="dns-servers"></a><span data-ttu-id="a4b3e-105">Servidores DNS</span><span class="sxs-lookup"><span data-stu-id="a4b3e-105">DNS Servers</span></span>

<span data-ttu-id="a4b3e-106">Un *servidor DNS* es un equipo que completa el proceso de resolución de nombres en DNS.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-106">A *DNS Server* is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="a4b3e-107">Los servidores DNS contienen [*archivos de zona*](z-gly.md) que les permiten resolver nombres en direcciones IP y direcciones IP en nombres.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-107">DNS Servers contain [*zone files*](z-gly.md) that enable them to resolve names to IP addresses and IP addresses to names.</span></span> <span data-ttu-id="a4b3e-108">Cuando se consulta, un servidor DNS responderá de una de estas tres maneras:</span><span class="sxs-lookup"><span data-stu-id="a4b3e-108">When queried, a DNS Server will respond in one of three ways:</span></span>

-   <span data-ttu-id="a4b3e-109">El servidor devuelve los datos de resolución de nombres o resolución de IP solicitados.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-109">The server returns the requested name-resolution or IP-resolution data.</span></span>
-   <span data-ttu-id="a4b3e-110">El servidor devuelve un puntero a otro servidor DNS que puede dar servicio a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-110">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="a4b3e-111">El servidor indica que no tiene los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-111">The server indicates that it does not have the requested data.</span></span>

<span data-ttu-id="a4b3e-112">Durante la preparación de la preparación para devolver los datos de resolución solicitados, los servidores DNS pueden consultar otros servidores DNS, pero más allá de eso, los servidores DNS no realizan ninguna otra operación.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-112">DNS Servers might, during the course of preparing to return the requested resolution data, query other DNS Servers, but beyond that, DNS Servers do not perform any other operations.</span></span>

<span data-ttu-id="a4b3e-113">Hay tres tipos principales de servidores DNS: servidores principales, servidores secundarios y servidores de almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-113">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span>

## <a name="primary-server"></a><span data-ttu-id="a4b3e-114">Servidor principal</span><span class="sxs-lookup"><span data-stu-id="a4b3e-114">Primary Server</span></span>

<span data-ttu-id="a4b3e-115">El *servidor principal* es el servidor autoritativo de la zona.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-115">The *primary server* is the authoritative server for the zone.</span></span> <span data-ttu-id="a4b3e-116">Todas las tareas administrativas asociadas a la zona (como la creación de subdominios dentro de la zona u otras tareas administrativas similares) deben realizarse en el servidor principal.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-116">All administrative tasks associated with the zone (such as creating subdomains within the zone, or other similar administrative tasks) must be performed on the primary server.</span></span> <span data-ttu-id="a4b3e-117">Además, los cambios asociados a la zona o las modificaciones o adiciones a RR en los archivos de zona deben realizarse en el servidor principal.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-117">In addition, any changes associated with the zone or any modifications or additions to RRs in the zone files must be made on the primary server.</span></span> <span data-ttu-id="a4b3e-118">Para cualquier zona determinada, hay un servidor principal, excepto cuando se integran Active Directory servicios y el servidor DNS de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-118">For any given zone, there is one primary server, except when you integrate Active Directory services and Microsoft DNS Server.</span></span>

## <a name="secondary-servers"></a><span data-ttu-id="a4b3e-119">Servidores secundarios</span><span class="sxs-lookup"><span data-stu-id="a4b3e-119">Secondary Servers</span></span>

<span data-ttu-id="a4b3e-120">*Los servidores secundarios son* servidores DNS de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-120">*Secondary servers* are backup DNS Servers.</span></span> <span data-ttu-id="a4b3e-121">Los servidores secundarios reciben todos sus archivos de zona de los archivos de zona del servidor principal en una transferencia de zona.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-121">Secondary servers receive all of their zone files from the primary server zone files in a zone transfer.</span></span> <span data-ttu-id="a4b3e-122">Pueden existir varios servidores secundarios para cualquier zona determinada, tantos como sea necesario para proporcionar equilibrio de [*carga,*](l-gly.md)tolerancia a errores y reducción del tráfico. [](f-gly.md)</span><span class="sxs-lookup"><span data-stu-id="a4b3e-122">Multiple secondary servers can exist for any given zone — as many as necessary to provide [*load balancing*](l-gly.md), [*fault tolerance*](f-gly.md), and traffic reduction.</span></span> <span data-ttu-id="a4b3e-123">Además, cualquier servidor DNS determinado puede ser un servidor secundario para varias zonas.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-123">Additionally, any given DNS Server can be a secondary server for multiple zones.</span></span>

<span data-ttu-id="a4b3e-124">Además de los servidores DNS principales y secundarios, se pueden usar roles de servidor DNS adicionales cuando estos servidores son adecuados para una infraestructura DNS.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-124">In addition to primary and secondary DNS Servers, additional DNS Server roles can be used when such servers are appropriate for a DNS infrastructure.</span></span> <span data-ttu-id="a4b3e-125">Estos servidores adicionales son servidores de almacenamiento en caché y [*reenviadores.*](f-gly.md)</span><span class="sxs-lookup"><span data-stu-id="a4b3e-125">These additional servers are caching servers and [*forwarders*](f-gly.md).</span></span>

## <a name="caching-servers"></a><span data-ttu-id="a4b3e-126">Servidores de almacenamiento en caché</span><span class="sxs-lookup"><span data-stu-id="a4b3e-126">Caching Servers</span></span>

<span data-ttu-id="a4b3e-127">[*Los servidores de almacenamiento en*](c-gly.md)caché, también conocidos como servidores de solo almacenamiento en caché, se realizan como sugiere su nombre. proporcionan solo el servicio de consulta en caché para las respuestas DNS.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-127">[*Caching servers*](c-gly.md), also known as caching-only servers, perform as their name suggests; they provide only cached-query service for DNS responses.</span></span> <span data-ttu-id="a4b3e-128">En lugar de mantener archivos de zona como lo hacen otros servidores secundarios, los servidores DNS de almacenamiento en caché realizan consultas, almacenan en caché las respuestas y devuelven los resultados al cliente de consulta.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-128">Rather than maintaining zone files like other secondary servers do, caching DNS Servers perform queries, cache the answers, and return the results to the querying client.</span></span> <span data-ttu-id="a4b3e-129">La principal diferencia entre los servidores de almacenamiento en caché y otros servidores secundarios es que otros servidores secundarios mantienen archivos de zona (y hacen transferencias de zona cuando corresponda, generando así tráfico de red asociado a la transferencia), los servidores de almacenamiento en caché no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-129">The primary difference between caching servers and other secondary servers is that other secondary servers maintain zone files (and do zone transfers when appropriate, thereby generating network traffic associated with the transfer), caching servers do not.</span></span>

 

 




