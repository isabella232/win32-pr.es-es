---
title: Reenviador
description: El reenviador es el componente de modo kernel del enrutador que es responsable de reenviar los datos de una interfaz de enrutador a los demás.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52885000a9f1fcc117cd1fefc207531b9b524e74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075770"
---
# <a name="forwarder"></a><span data-ttu-id="fb04b-103">Reenviador</span><span class="sxs-lookup"><span data-stu-id="fb04b-103">Forwarder</span></span>

<span data-ttu-id="fb04b-104">El reenviador es el componente de modo kernel del enrutador que es responsable de reenviar los datos de una interfaz de enrutador a los demás.</span><span class="sxs-lookup"><span data-stu-id="fb04b-104">The forwarder is the kernel-mode component of the router that is responsible for forwarding data from one router interface to the others.</span></span> <span data-ttu-id="fb04b-105">El reenviador también decide si un paquete está destinado a la entrega local, si está destinado a reenviarse fuera de otra interfaz o a ambos.</span><span class="sxs-lookup"><span data-stu-id="fb04b-105">The forwarder also decides whether a packet is destined for local delivery, whether it is destined to be forwarded out of another interface, or both.</span></span>

<span data-ttu-id="fb04b-106">Hay dos reenviadores de modo kernel: unidifusión y multidifusión.</span><span class="sxs-lookup"><span data-stu-id="fb04b-106">There are two kernel-mode forwarders: unicast and multicast.</span></span>

<span data-ttu-id="fb04b-107">El administrador de enrutadores obtiene las mejores rutas a todos los destinos del administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="fb04b-107">The router manager obtains the best routes to all destinations from the routing table manager.</span></span> <span data-ttu-id="fb04b-108">Estas rutas se pasan al reenviador de unidifusión.</span><span class="sxs-lookup"><span data-stu-id="fb04b-108">These routes are passed to the unicast forwarder.</span></span> <span data-ttu-id="fb04b-109">El reenviador de unidifusión utiliza estas rutas para realizar el reenvío real de datos de unidifusión.</span><span class="sxs-lookup"><span data-stu-id="fb04b-109">The unicast forwarder uses these routes to perform the actual forwarding of unicast data.</span></span> <span data-ttu-id="fb04b-110">De esta manera, el reenviador de unidifusión mantiene una memoria caché de las mejores rutas en la vista de unidifusión de la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="fb04b-110">In this manner, the unicast forwarder maintains a cache of the best routes in the unicast view of the routing table.</span></span>

<span data-ttu-id="fb04b-111">El administrador de grupos de multidifusión usa información de la vista multidifusión de la tabla de enrutamiento para agregar entradas de reenvío de multidifusión al reenviador de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="fb04b-111">The multicast group manager uses information from the multicast view of the routing table to add multicast forwarding entries to the multicast forwarder.</span></span>

 

 




