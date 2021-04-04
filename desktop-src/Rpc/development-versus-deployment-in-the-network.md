---
title: Desarrollo frente a implementación en la red
description: La mayoría de los desarrolladores escriben y prueban el software en una LAN de confianza rápida.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075598"
---
# <a name="development-vs-deployment-in-the-network"></a><span data-ttu-id="64ee6-103">Desarrollo frente a implementación en la red</span><span class="sxs-lookup"><span data-stu-id="64ee6-103">Development vs. Deployment in the Network</span></span>

<span data-ttu-id="64ee6-104">La mayoría de los desarrolladores escriben y prueban el software en una LAN de confianza rápida.</span><span class="sxs-lookup"><span data-stu-id="64ee6-104">Most developers write and test their software on a fast reliable LAN.</span></span> <span data-ttu-id="64ee6-105">El cliente y el servidor suelen estar en el mismo segmento de red.</span><span class="sxs-lookup"><span data-stu-id="64ee6-105">Their client and server are often on the same network segment.</span></span> <span data-ttu-id="64ee6-106">En tales circunstancias, la red rara vez no responde y la conectividad rara vez se pierde.</span><span class="sxs-lookup"><span data-stu-id="64ee6-106">In such circumstances the network is rarely unresponsive, and connectivity rarely lost.</span></span> <span data-ttu-id="64ee6-107">Sin embargo, cuando se implementa en un entorno de cliente, el cliente y el servidor suelen estar en distintos segmentos de red, posiblemente de forma geográfica remota, y el servidor está muy cargado con otros clientes.</span><span class="sxs-lookup"><span data-stu-id="64ee6-107">When deployed in a customer environment however, client and server are often on different network segments, possibly geographically remote, and the server is heavily loaded with other clients.</span></span> <span data-ttu-id="64ee6-108">En otras palabras: no se puede asumir la capacidad de respuesta de red.</span><span class="sxs-lookup"><span data-stu-id="64ee6-108">In other words: network responsiveness cannot be assumed.</span></span>

<span data-ttu-id="64ee6-109">En este artículo se explica cómo construir sólidas arquitecturas de cliente/servidor en caso de incertidumbre introducida por una red intrínsecamente confiable y servidores potencialmente no disponibles.</span><span class="sxs-lookup"><span data-stu-id="64ee6-109">This article explains how to construct robust client/server architectures in the face of uncertainty introduced by an intrinsically unreliable network and potentially unavailable servers.</span></span>

 

 




