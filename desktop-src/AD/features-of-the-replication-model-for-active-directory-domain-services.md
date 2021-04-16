---
title: Características del modelo de replicación para Active Directory Domain Services
description: El modelo de replicación usado en Active Directory Domain Services se denomina coherencia flexible de varios maestros con convergencia.
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, modelo de replicación
- Características del modelo de replicación Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923c49dd648063ebd6afd086be3729f28f1e4080
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656234"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a><span data-ttu-id="bb398-105">Características del modelo de replicación para Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="bb398-105">Features of the Replication Model for Active Directory Domain Services</span></span>

<span data-ttu-id="bb398-106">El modelo de replicación usado en Active Directory Domain Services se denomina *coherencia flexible de varios maestros con convergencia*.</span><span class="sxs-lookup"><span data-stu-id="bb398-106">The replication model used in Active Directory Domain Services is called *multi-master loose consistency with convergence*.</span></span> <span data-ttu-id="bb398-107">En este modelo, el directorio puede tener muchas réplicas; un sistema de replicación propaga los cambios realizados en una réplica determinada a todas las demás réplicas.</span><span class="sxs-lookup"><span data-stu-id="bb398-107">In this model, the directory can have many replicas; a replication system propagates changes made at any given replica to all other replicas.</span></span> <span data-ttu-id="bb398-108">No se garantiza que las réplicas sean coherentes entre sí en un momento determinado ("coherencia relajada"), ya que los cambios se pueden aplicar a cualquier réplica en cualquier momento ("varios maestros").</span><span class="sxs-lookup"><span data-stu-id="bb398-108">The replicas are not guaranteed to be consistent with each other at any particular time ("loose consistency"), because changes can be applied to any replica at any time ("multi-master").</span></span> <span data-ttu-id="bb398-109">Si el sistema puede llegar a un estado estable, en el que no se están produciendo nuevas actualizaciones y todas las actualizaciones anteriores se han replicado por completo, se garantiza que todas las réplicas convergen en el mismo conjunto de valores ("convergencia").</span><span class="sxs-lookup"><span data-stu-id="bb398-109">If the system is allowed to reach a steady state, in which no new updates are occurring and all previous updates have been completely replicated, all replicas are guaranteed to converge on the same set of values ("convergence").</span></span>

 

 




