---
description: La infraestructura del mismo nivel es un conjunto de varias API que son eficaces y flexibles.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: ¿Qué es la infraestructura del mismo nivel?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667368"
---
# <a name="what-is-the-peer-infrastructure"></a><span data-ttu-id="fb926-103">¿Qué es la infraestructura del mismo nivel?</span><span class="sxs-lookup"><span data-stu-id="fb926-103">What is the Peer Infrastructure?</span></span>

<span data-ttu-id="fb926-104">La infraestructura del mismo nivel es un conjunto de varias API que son eficaces y flexibles.</span><span class="sxs-lookup"><span data-stu-id="fb926-104">The Peer Infrastructure is a set of several APIs that are powerful and flexible.</span></span> <span data-ttu-id="fb926-105">Entre los componentes principales se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="fb926-105">The major components include the following:</span></span>

-   [<span data-ttu-id="fb926-106">API de gráficos del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="fb926-106">Peer Graphing API</span></span>](#peer-graphing-api)
-   [<span data-ttu-id="fb926-107">API de agrupación del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="fb926-107">Peer Grouping API</span></span>](#peer-grouping-api)
-   [<span data-ttu-id="fb926-108">API del administrador de identidades del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="fb926-108">Peer Identity Manager API</span></span>](#peer-identity-manager-api)
-   [<span data-ttu-id="fb926-109">API del proveedor de espacio de nombres PNRP</span><span class="sxs-lookup"><span data-stu-id="fb926-109">PNRP Namespace Provider API</span></span>](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a><span data-ttu-id="fb926-110">API de gráficos del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="fb926-110">Peer Graphing API</span></span>

<span data-ttu-id="fb926-111">La infraestructura del mismo nivel proporciona una tecnología de gráficos que puede pasar información de forma eficaz y confiable entre los elementos del mismo nivel en un grafo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="fb926-111">The Peer Infrastructure provides a graphing technology that can pass information efficiently and reliably between peers in a peer graph.</span></span> <span data-ttu-id="fb926-112">La [API de gráficos del mismo nivel](graphing-api.md) garantiza que cada nodo tiene una vista coherente de los datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="fb926-112">The [Peer Graphing API](graphing-api.md) ensures that each node has a consistent view of the data in a graph.</span></span>

<span data-ttu-id="fb926-113">Puede usar la [API de gráficos del mismo nivel](graphing-api.md) para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb926-113">You can use the [Peer Graphing API](graphing-api.md) to do the following:</span></span>

-   <span data-ttu-id="fb926-114">Crear y administrar gráficos del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="fb926-114">Create and manage peer graphs</span></span>
-   <span data-ttu-id="fb926-115">Enumerar e interactuar con otros elementos del mismo nivel en un grafo del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="fb926-115">Enumerate and interact with other peers in a peer graph</span></span>
-   <span data-ttu-id="fb926-116">Enviar datos en forma de un [registro](records.md) a cada nodo de un grafo del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="fb926-116">Send data in the form of a [record](records.md) to each node in a peer graph</span></span>

## <a name="peer-grouping-api"></a><span data-ttu-id="fb926-117">API de agrupación del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="fb926-117">Peer Grouping API</span></span>

<span data-ttu-id="fb926-118">La [API de agrupación del mismo nivel](grouping-api.md) combina y mejora las API [PNRP](#pnrp-namespace-provider-api) y de [gráficos](#peer-graphing-api) del mismo nivel, y agrega los dos componentes siguientes:</span><span class="sxs-lookup"><span data-stu-id="fb926-118">The [Peer Grouping API](grouping-api.md) combines and enhances the Peer [PNRP](#pnrp-namespace-provider-api) and [Graphing](#peer-graphing-api) APIs, and adds the following two components:</span></span>

-   <span data-ttu-id="fb926-119">Una capa de multiplexación que permite que varias aplicaciones que se ejecutan en una entidad del mismo nivel se conecten a un grupo</span><span class="sxs-lookup"><span data-stu-id="fb926-119">A multiplexing layer that allows multiple applications running on one peer entity to connect to a group</span></span>
-   <span data-ttu-id="fb926-120">Un modelo de seguridad específico que garantiza que solo los elementos del mismo nivel invitados a un grupo pueden conectarse al grupo a través de la duración del grupo.</span><span class="sxs-lookup"><span data-stu-id="fb926-120">A specific security model that ensures only peers invited to a group can connect to the group through the lifetime of the group</span></span>

<span data-ttu-id="fb926-121">Puede usar la API de agrupación del mismo nivel para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb926-121">You can use the Peer Grouping API to do the following:</span></span>

-   <span data-ttu-id="fb926-122">Crear y administrar grupos de pares seguros</span><span class="sxs-lookup"><span data-stu-id="fb926-122">Create and manage secure peer groups</span></span>
-   <span data-ttu-id="fb926-123">Enumerar e interactuar con otros elementos del mismo nivel en un grupo</span><span class="sxs-lookup"><span data-stu-id="fb926-123">Enumerate and interact with other peers in a group</span></span>
-   <span data-ttu-id="fb926-124">Enviar datos en forma de un [registro](records.md) a cada nodo de un grupo del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="fb926-124">Send data in the form of a [record](records.md) to each node in a peer group</span></span>

## <a name="peer-identity-manager-api"></a><span data-ttu-id="fb926-125">API del administrador de identidades del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="fb926-125">Peer Identity Manager API</span></span>

<span data-ttu-id="fb926-126">Mediante el uso de la [API del administrador de identidad del mismo nivel](identity-manager-api.md) , puede crear [nombres de mismo nivel](peer-names.md) seguros que PNRP pueda usar para asegurarse de que una persona que publica un nombre posee oficialmente el nombre.</span><span class="sxs-lookup"><span data-stu-id="fb926-126">By using the [Peer Identity Manager API](identity-manager-api.md) you can create secure [peer names](peer-names.md) that PNRP can use to ensure that a person publishing a name officially owns the name.</span></span> <span data-ttu-id="fb926-127">Los nombres de mismo nivel también se denominan identidades y se utilizan en la API de agrupación del mismo nivel para identificar a los usuarios de un grupo.</span><span class="sxs-lookup"><span data-stu-id="fb926-127">Peer names are also called identities, and they are used in the Peer Grouping API to identify the individuals in a group.</span></span>

<span data-ttu-id="fb926-128">Puede usar la [API del administrador de identidades del mismo nivel](identity-manager-api.md) para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb926-128">You can use the [Peer Identity Manager API](identity-manager-api.md) to do the following:</span></span>

-   <span data-ttu-id="fb926-129">Crear, enumerar y administrar identidades del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="fb926-129">Create, enumerate, and manage peer identities.</span></span>

## <a name="pnrp-namespace-provider-api"></a><span data-ttu-id="fb926-130">API del proveedor de espacio de nombres PNRP</span><span class="sxs-lookup"><span data-stu-id="fb926-130">PNRP Namespace Provider API</span></span>

<span data-ttu-id="fb926-131">La infraestructura del mismo nivel proporciona una tecnología de resolución de nombres sin servidor denominada [API del proveedor de espacio de nombres PNRP](pnrp-namespace-provider-api.md).</span><span class="sxs-lookup"><span data-stu-id="fb926-131">The Peer Infrastructure provides a serverless name resolution technology called the [PNRP Namespace Provider API](pnrp-namespace-provider-api.md).</span></span> <span data-ttu-id="fb926-132">Mediante el uso de la API del proveedor de espacio de nombres PNRP de Winsock 2, un punto de conexión del mismo nivel, servicio, dispositivo informático y punto de conexión de grupo del mismo nivel puede administrar, registrar, anular el registro y resolver otro punto de conexión en una [nube](clouds.md)PNRP.</span><span class="sxs-lookup"><span data-stu-id="fb926-132">By using the Winsock 2 PNRP Namespace Provider API, a peer, service, computing device, and peer group endpoint can manage, register, unregister, and resolve another endpoint in a PNRP [cloud](clouds.md).</span></span>

> [!Note]  
> <span data-ttu-id="fb926-133">PNRP es un acrónimo del **Protocolo de resolución de nombres de mismo nivel**.</span><span class="sxs-lookup"><span data-stu-id="fb926-133">PNRP is an acronym for **peer name resolution protocol**.</span></span>

 

 

 



