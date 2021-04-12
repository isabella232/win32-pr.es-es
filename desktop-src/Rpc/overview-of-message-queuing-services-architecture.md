---
title: Información general sobre la arquitectura de servicios de Message Queue Server
description: Los servicios de Message Queue Server (MSMQ) utilizan un modelo de sitio/empresa. Normalmente, un sitio es una ubicación física, como un edificio. Una empresa se compone de uno o varios sitios y representa una organización.
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357445"
---
# <a name="overview-of-message-queuing-services-architecture"></a><span data-ttu-id="8b1cc-105">Información general sobre la arquitectura de servicios de Message Queue Server</span><span class="sxs-lookup"><span data-stu-id="8b1cc-105">Overview of Message Queuing Services Architecture</span></span>

<span data-ttu-id="8b1cc-106">Los servicios de Message Queue Server (MSMQ) utilizan un modelo de sitio/empresa.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-106">Message Queuing Services (MSMQ) uses a site/enterprise model.</span></span> <span data-ttu-id="8b1cc-107">Normalmente, un sitio es una ubicación física, como un edificio.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-107">Typically, a site is a physical location, such as a building.</span></span> <span data-ttu-id="8b1cc-108">Una empresa se compone de uno o varios sitios y representa una organización.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-108">An enterprise consists of one or more sites and represents an organization.</span></span>

<span data-ttu-id="8b1cc-109">En el diagrama siguiente se ilustra la arquitectura del servicio MSMQ.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-109">The following diagram illustrates the architecture of the MSMQ Service.</span></span>

![arquitectura de MSMQ](images/msmq.png)

<span data-ttu-id="8b1cc-111">En esencia, MSMQ es la base de datos del servicio de información de cola de mensajes (MQIS), que se ejecuta sobre SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-111">At the heart of MSMQ is the Message Queue Information Service (MQIS) database, which runs on top of SQL Server.</span></span> <span data-ttu-id="8b1cc-112">Una empresa tiene un solo MQIS maestro, denominado controlador Enterprise principal.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-112">An enterprise has a single master MQIS, called the Primary Enterprise Controller.</span></span> <span data-ttu-id="8b1cc-113">Cada sitio tiene su propio MQIS, denominado *controlador de sitio principal* y cero o más *controladores de sitio de copia de seguridad*.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-113">Each site has its own MQIS, called a *primary site controller* and zero or more *backup site controllers*.</span></span> <span data-ttu-id="8b1cc-114">Por último, hay equipos cliente individuales, cada uno de los cuales tiene su propio administrador de cola, que se implementa como un servicio.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-114">Finally, there are the individual client computers, each of which has its own queue manager, implemented as a service.</span></span> <span data-ttu-id="8b1cc-115">El controlador de empresa principal también puede ser un controlador de sitio principal y cualquier controlador también puede ser un cliente.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-115">The Primary Enterprise Controller can also be a Primary Site Controller, and any controller can also be a client.</span></span>

<span data-ttu-id="8b1cc-116">Las colas de mensajes pueden ser públicas o privadas.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-116">Message queues can be either public or private.</span></span> <span data-ttu-id="8b1cc-117">Las colas públicas se registran en Active Directory y son accesibles a través de la red.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-117">Public queues are registered in Active Directory and are accessible across the network.</span></span> <span data-ttu-id="8b1cc-118">Los mensajes de una cola pública se enrutan por toda la empresa, bajo el control de MSMQ.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-118">Messages in a public queue are routed throughout the enterprise, under the control of MSMQ.</span></span> <span data-ttu-id="8b1cc-119">Los mensajes de aplicación cliente se mueven desde el administrador de cola del cliente a la cola de destino al viajar entre los administradores de cola de los controladores de sitio.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-119">Client application messages move from the client's queue manager to the destination queue by traveling between the queue managers of the site controllers.</span></span>

<span data-ttu-id="8b1cc-120">El administrador de cola local mantiene las colas privadas y no se registran en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-120">Private queues are maintained by the local queue manager and are not registered in Active Directory.</span></span> <span data-ttu-id="8b1cc-121">El ámbito de los mensajes de cola privados se limita al equipo en el que residen.</span><span class="sxs-lookup"><span data-stu-id="8b1cc-121">The scope of private queue messages is limited to the computer on which they reside.</span></span>

 

 




