---
title: Comportamiento de la replicación en Active Directory Domain Services
description: El comportamiento de la replicación es coherente y predecible. dado un conjunto de cambios en una réplica determinada, el resultado se puede predecir \ 8212; los cambios se propagarán a todas las demás réplicas.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory de Active Directory Domain Services, replicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41009a733f99366e499a25baca989f4f28794aea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903095"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a><span data-ttu-id="46022-104">Comportamiento de la replicación en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="46022-104">Replication Behavior in Active Directory Domain Services</span></span>

<span data-ttu-id="46022-105">El comportamiento de la replicación es coherente y predecible. dado un conjunto de cambios en una réplica determinada, se puede predecir el resultado; los cambios se propagarán a todas las demás réplicas.</span><span class="sxs-lookup"><span data-stu-id="46022-105">Replication behavior is consistent and predictable; given a set of changes to a given replica, the outcome can be predicted—the changes will be propagated to all other replicas.</span></span> <span data-ttu-id="46022-106">La idea de un modelo general confiable para predecir cuándo se aplicarán los cambios en el resto de réplicas, o en una réplica determinada, no es posible, ya que no se puede conocer el estado futuro del sistema distribuido como un todo.</span><span class="sxs-lookup"><span data-stu-id="46022-106">Devising a reliable general model for predicting when the changes will be applied at all other replicas, or at a particular replica, is impossible, because the future state of the distributed system as a whole cannot be known.</span></span> <span data-ttu-id="46022-107">Esto se denomina "latencia no determinista" y las aplicaciones que usan el directorio deben comprender y permitirlo.</span><span class="sxs-lookup"><span data-stu-id="46022-107">This is called "nondeterministic latency," and applications that use the directory must understand and allow for it.</span></span>

<span data-ttu-id="46022-108">La situación no es tan compleja en el caso de que aparezca.</span><span class="sxs-lookup"><span data-stu-id="46022-108">The situation is not as complex at it might appear.</span></span> <span data-ttu-id="46022-109">Hay solo tres Estados que una aplicación debe acomodar:</span><span class="sxs-lookup"><span data-stu-id="46022-109">There are only three states that an application must accommodate:</span></span>

-   <span data-ttu-id="46022-110">Sesgo de versión: ninguno de los cambios que se aplican a una réplica de origen determinada se ha propagado a una réplica de destino determinada.</span><span class="sxs-lookup"><span data-stu-id="46022-110">Version Skew: None of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="46022-111">Una aplicación que lee la réplica de origen ve la nueva versión de la información, mientras que una aplicación que lee el destino ve la versión anterior (o nada, si la nueva información se agregó por primera vez).</span><span class="sxs-lookup"><span data-stu-id="46022-111">An application reading the source replica sees the new version of the information, while an application reading the destination sees the old version (or nothing, if the new information was added for the first time).</span></span> <span data-ttu-id="46022-112">El sesgo de versión se aplica a todos los consumidores del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="46022-112">Version skew applies to all directory service consumers.</span></span>
-   <span data-ttu-id="46022-113">Actualización parcial: algunos de los cambios que se aplican a una réplica de origen determinada se han propagado a una réplica de destino determinada.</span><span class="sxs-lookup"><span data-stu-id="46022-113">Partial Update: Some of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="46022-114">Una aplicación que lee la réplica de origen ve la nueva información, mientras que una aplicación que lee el destino ve una mezcla de información antigua y nueva (o solo parte de la nueva información, si la nueva información se agregó por primera vez).</span><span class="sxs-lookup"><span data-stu-id="46022-114">An application reading the source replica sees the new information, while an application reading the destination sees a mix of old and new information (or only some of the new information, if the new information was added for the first time).</span></span> <span data-ttu-id="46022-115">La actualización parcial se aplica a los consumidores del servicio de directorio que usan dos o más objetos relacionados para almacenar su información.</span><span class="sxs-lookup"><span data-stu-id="46022-115">Partial update applies to directory service consumers that use two or more related objects to store their information.</span></span>
-   <span data-ttu-id="46022-116">Estado totalmente replicado: todos los cambios que se aplican a una réplica de origen determinada se propagan a una réplica de destino determinada.</span><span class="sxs-lookup"><span data-stu-id="46022-116">Fully Replicated State: All of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="46022-117">Las aplicaciones en las réplicas de origen y de destino ven la misma información.</span><span class="sxs-lookup"><span data-stu-id="46022-117">Applications at the source and destination replicas see the same information.</span></span>

 

 




