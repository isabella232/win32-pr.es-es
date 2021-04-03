---
title: Message Queue Server de RPC
description: Message Queuing (MSMQ) permite a los usuarios comunicarse a través de redes y sistemas independientemente del estado actual de las aplicaciones y los sistemas que se comunican.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- RPC llamada a procedimiento remoto, descripción, Message Queue Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b72e9e35ec2aa1cc440c0d0356c681c4fe8548c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076136"
---
# <a name="rpc-message-queuing"></a><span data-ttu-id="87319-104">Message Queue Server de RPC</span><span class="sxs-lookup"><span data-stu-id="87319-104">RPC Message Queuing</span></span>

<span data-ttu-id="87319-105">Message Queuing (MSMQ) permite a los usuarios comunicarse a través de redes y sistemas independientemente del estado actual de las aplicaciones y los sistemas que se comunican.</span><span class="sxs-lookup"><span data-stu-id="87319-105">Message Queuing (MSMQ) lets users communicate across networks and systems regardless of the current state of the communicating applications and systems.</span></span> <span data-ttu-id="87319-106">Las aplicaciones envían y reciben mensajes a través de las colas de mensajes que mantiene MSMQ.</span><span class="sxs-lookup"><span data-stu-id="87319-106">Applications send and receive messages through message queues that MSMQ maintains.</span></span> <span data-ttu-id="87319-107">Las colas de mensajes continúan funcionando incluso cuando la aplicación de cliente o de servidor no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="87319-107">The message queues continue to function even when the client or server application is not running.</span></span> <span data-ttu-id="87319-108">Message Queue Server proporciona:</span><span class="sxs-lookup"><span data-stu-id="87319-108">Message queuing provides:</span></span>

-   <span data-ttu-id="87319-109">**Mensajería asincrónica.**</span><span class="sxs-lookup"><span data-stu-id="87319-109">**Asynchronous messaging.**</span></span> <span data-ttu-id="87319-110">Con la mensajería asincrónica de MSMQ, una aplicación cliente puede enviar un mensaje a un servidor y volver inmediatamente, incluso si el equipo de destino o el programa de servidor no responde.</span><span class="sxs-lookup"><span data-stu-id="87319-110">With MSMQ asynchronous messaging, a client application can send a message to a server and return immediately, even if the target computer or server program is not responding.</span></span>
-   <span data-ttu-id="87319-111">**Entrega de mensajes garantizada.**</span><span class="sxs-lookup"><span data-stu-id="87319-111">**Guaranteed message delivery.**</span></span> <span data-ttu-id="87319-112">Cuando una aplicación envía un mensaje a través de MSMQ, el mensaje llegará a su destino, aunque la aplicación de destino no se ejecute al mismo tiempo o las redes y los sistemas estén sin conexión.</span><span class="sxs-lookup"><span data-stu-id="87319-112">When an application sends a message through MSMQ, the message will reach its destination even if the destination application is not running at the same time or the networks and systems are offline.</span></span>
-   <span data-ttu-id="87319-113">**Enrutamiento y configuración dinámica.**</span><span class="sxs-lookup"><span data-stu-id="87319-113">**Routing and dynamic configuration.**</span></span> <span data-ttu-id="87319-114">MSMQ proporciona enrutamiento flexible a través de redes heterogéneas.</span><span class="sxs-lookup"><span data-stu-id="87319-114">MSMQ provides flexible routing over heterogeneous networks.</span></span> <span data-ttu-id="87319-115">La configuración de estas redes se puede cambiar dinámicamente sin realizar cambios importantes en los sistemas y redes.</span><span class="sxs-lookup"><span data-stu-id="87319-115">The configuration of such networks can be changed dynamically without any major changes to systems and networks themselves.</span></span>
-   <span data-ttu-id="87319-116">**Mensajería sin conexión.**</span><span class="sxs-lookup"><span data-stu-id="87319-116">**Connectionless messaging.**</span></span> <span data-ttu-id="87319-117">Las aplicaciones que usan MSMQ no necesitan configurar sesiones directas con las aplicaciones de destino.</span><span class="sxs-lookup"><span data-stu-id="87319-117">Applications using MSMQ do not need to set up direct sessions with target applications.</span></span>
-   <span data-ttu-id="87319-118">[Seguridad](security.md).</span><span class="sxs-lookup"><span data-stu-id="87319-118">[Security](security.md).</span></span> <span data-ttu-id="87319-119">MSMQ proporciona una comunicación segura basada en la seguridad de Windows y la API de cifrado (CryptoAPI) para el cifrado y las firmas digitales.</span><span class="sxs-lookup"><span data-stu-id="87319-119">MSMQ provides secure communication based on Windows security and the Cryptographic API (CryptoAPI) for encryption and digital signatures.</span></span>
-   <span data-ttu-id="87319-120">**Mensajería con prioridad.**</span><span class="sxs-lookup"><span data-stu-id="87319-120">**Prioritized Messaging.**</span></span> <span data-ttu-id="87319-121">MSMQ transfiere mensajes entre redes según la prioridad, lo que permite una comunicación más rápida para aplicaciones críticas.</span><span class="sxs-lookup"><span data-stu-id="87319-121">MSMQ transfers messages across networks based on priority, allowing faster communication for critical applications.</span></span>

<span data-ttu-id="87319-122">Microsoft RPC extiende el modelo Open Software Foundation – Data Communications Equipment (OSF-DCE) para las llamadas a procedimientos remotos, ya que permite que las aplicaciones distribuidas utilicen MSMQ como transporte y controlen muchas de sus características.</span><span class="sxs-lookup"><span data-stu-id="87319-122">Microsoft RPC extends the Open Software Foundation–Data Communications Equipment (OSF-DCE) model for remote procedure calls by allowing distributed applications to use MSMQ as a transport and to control many of its features.</span></span> <span data-ttu-id="87319-123">Esta funcionalidad está disponible para las aplicaciones RPC convencionales y, a través de la interfaz **IRPCOptions** , a las aplicaciones com.</span><span class="sxs-lookup"><span data-stu-id="87319-123">This functionality is available both to conventional RPC applications and, through the **IRPCOptions** interface, to COM applications.</span></span>

> [!Note]  
> <span data-ttu-id="87319-124">Message Queue Server de RPC solo está disponible en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="87319-124">RPC message queuing is available only on Windows 2000.</span></span> <span data-ttu-id="87319-125">Las versiones posteriores de Windows no admiten Message Queue Server de RPC.</span><span class="sxs-lookup"><span data-stu-id="87319-125">Later versions of Windows do not support RPC message queuing.</span></span>

 

<span data-ttu-id="87319-126">En los temas siguientes se proporciona información general sobre Message Queue Server:</span><span class="sxs-lookup"><span data-stu-id="87319-126">The following topics provide an overview of message queuing:</span></span>

-   [<span data-ttu-id="87319-127">Información general sobre la arquitectura de servicios de Message Queue Server</span><span class="sxs-lookup"><span data-stu-id="87319-127">Overview of Message Queuing Services Architecture</span></span>](overview-of-message-queuing-services-architecture.md)
-   [<span data-ttu-id="87319-128">Propiedades de Message y Message Queue</span><span class="sxs-lookup"><span data-stu-id="87319-128">Message and Message Queue Properties</span></span>](message-and-message-queue-properties.md)
-   [<span data-ttu-id="87319-129">Usar MSMQ como transporte RPC</span><span class="sxs-lookup"><span data-stu-id="87319-129">Using MSMQ as an RPC Transport</span></span>](using-msmq-as-an-rpc-transport.md)
-   [<span data-ttu-id="87319-130">Requisitos del sistema para aplicaciones de Message \_ Queue Server de RPC</span><span class="sxs-lookup"><span data-stu-id="87319-130">System Requirements for RPC-Message\_Queuing Applications</span></span>](system-requirements-for-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="87319-131">Desarrollo de aplicaciones de RPC-Message Queue Server</span><span class="sxs-lookup"><span data-stu-id="87319-131">Developing RPC-Message Queuing Applications</span></span>](developing-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="87319-132">Servicios de seguridad de MSMQ</span><span class="sxs-lookup"><span data-stu-id="87319-132">MSMQ Security Services</span></span>](msmq-security-services.md)

 

 




