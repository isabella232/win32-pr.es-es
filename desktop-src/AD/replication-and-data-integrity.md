---
title: Replicación e integridad de los datos
description: Active Directory Domain Services proporcionar una actualización de varios maestros.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, uso, la replicación y la integridad de los datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f7e2c3193a280d009f53521e7a94fa3b89c5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656219"
---
# <a name="replication-and-data-integrity"></a><span data-ttu-id="10ecd-104">Replicación e integridad de los datos</span><span class="sxs-lookup"><span data-stu-id="10ecd-104">Replication and Data Integrity</span></span>

<span data-ttu-id="10ecd-105">Active Directory Domain Services proporcionar *una actualización de varios maestros*.</span><span class="sxs-lookup"><span data-stu-id="10ecd-105">Active Directory Domain Services provide *multi-master update*.</span></span> <span data-ttu-id="10ecd-106">La actualización de varios maestros significa que se pueden escribir todas las réplicas completas de una partición determinada (las réplicas parciales en los servidores de catálogo global no se pueden escribir). La actualización de varios maestros significa que las actualizaciones no se bloquean aunque algunas réplicas no funcionen.</span><span class="sxs-lookup"><span data-stu-id="10ecd-106">Multi-master update means that all full replicas of a given partition are writable (the partial replicas on global catalog servers are not writable.) Multi-master update means that updates are not blocked even when some replicas are inoperable.</span></span> <span data-ttu-id="10ecd-107">El servidor de Active Directory propaga los cambios de la réplica actualizada a todas las demás réplicas.</span><span class="sxs-lookup"><span data-stu-id="10ecd-107">The Active Directory server propagates the changes from the updated replica to all other replicas.</span></span> <span data-ttu-id="10ecd-108">La replicación es automática y transparente.</span><span class="sxs-lookup"><span data-stu-id="10ecd-108">Replication is automatic and transparent.</span></span>

<span data-ttu-id="10ecd-109">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="10ecd-109">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="10ecd-110">El modelo de replicación en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="10ecd-110">The Replication Model in Active Directory Domain Services</span></span>](replication-model-in-active-directory-domain-services.md)
-   [<span data-ttu-id="10ecd-111">Comportamiento de la replicación en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="10ecd-111">Replication Behavior in Active Directory Domain Services</span></span>](replication-behavior-in-active-directory-domain-services.md)
-   [<span data-ttu-id="10ecd-112">Detección y prevención de la latencia de replicación</span><span class="sxs-lookup"><span data-stu-id="10ecd-112">Detecting and Avoiding Replication Latency</span></span>](detecting-and-avoiding-replication-latency.md)

 

 




