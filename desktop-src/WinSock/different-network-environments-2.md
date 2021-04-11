---
description: Varios entornos de red afectan al comportamiento en red de una aplicación.
ms.assetid: 4a530a17-5e61-4730-95f5-233261b4ceb0
title: Entornos de red diferentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dca7eacd48973a9106e6a1e3a4eb5959afcfef
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104279757"
---
# <a name="different-network-environments"></a><span data-ttu-id="90ba1-103">Entornos de red diferentes</span><span class="sxs-lookup"><span data-stu-id="90ba1-103">Different Network Environments</span></span>

<span data-ttu-id="90ba1-104">Varios entornos de red afectan al comportamiento en red de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="90ba1-104">Several network environments affect the networked behavior of an application.</span></span> <span data-ttu-id="90ba1-105">Las propiedades que diferencian los entornos de red incluyen el ancho de banda bajo y alto, y el RTT bajo y alto.</span><span class="sxs-lookup"><span data-stu-id="90ba1-105">Properties that differentiate network environments include low versus high bandwidth, and low versus high RTT.</span></span> <span data-ttu-id="90ba1-106">Los entornos de red afectan a las aplicaciones transaccionales y de streaming de maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="90ba1-106">Network environments affect transactional and streaming applications in different ways.</span></span> <span data-ttu-id="90ba1-107">Las aplicaciones transaccionales son más sensibles a RTT; las aplicaciones de streaming son más sensibles a los productos de retraso de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="90ba1-107">Transactional applications are more sensitive to RTT; streaming applications are more sensitive to bandwidth-delay products.</span></span>

![Diagrama que muestra cómo los distintos entornos de red afectan al comportamiento de red de una aplicación.](images/hperf-1.png)

<span data-ttu-id="90ba1-109">Las redes de acceso telefónico y algunas redes inalámbricas tienen un RTT variable.</span><span class="sxs-lookup"><span data-stu-id="90ba1-109">Dial-up networks and some wireless networks have a variable RTT.</span></span> <span data-ttu-id="90ba1-110">Por lo general, las redes satélite tienen un ancho de banda asimétrico entre el nivel ascendente y el inferior.</span><span class="sxs-lookup"><span data-stu-id="90ba1-110">Satellite networks generally have an asymmetric bandwidth between upstream and downstream.</span></span> <span data-ttu-id="90ba1-111">LAN inalámbrica y xDSL son buenos ejemplos de redes con productos de retraso de ancho de banda similares al de Fast Ethernet.</span><span class="sxs-lookup"><span data-stu-id="90ba1-111">Wireless LAN and xDSL are good examples of networks with bandwidth-delay products similar to that of Fast Ethernet.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90ba1-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90ba1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90ba1-113">Aplicaciones de Windows Sockets de alto rendimiento</span><span class="sxs-lookup"><span data-stu-id="90ba1-113">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="90ba1-114">Dimensiones de rendimiento</span><span class="sxs-lookup"><span data-stu-id="90ba1-114">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



