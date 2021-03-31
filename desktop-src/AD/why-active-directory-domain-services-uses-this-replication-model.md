---
title: Por qué Active Directory Domain Services usa este modelo de replicación
description: En este tema se explican los motivos del sistema de forma libre usado por Active Directory Domain Services para un modelo de replicación.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Active Directory del modelo de replicación, ventajas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903088"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a><span data-ttu-id="8ab90-104">Por qué Active Directory Domain Services usa este modelo de replicación</span><span class="sxs-lookup"><span data-stu-id="8ab90-104">Why Active Directory Domain Services Uses This Replication Model</span></span>

<span data-ttu-id="8ab90-105">En este tema se explican los motivos del sistema de forma libre usado por Active Directory Domain Services para un modelo de replicación.</span><span class="sxs-lookup"><span data-stu-id="8ab90-105">This topic explains the reasons for the free-form system used by Active Directory Domain Services for a replication model.</span></span>

<span data-ttu-id="8ab90-106">Active Directory Domain Services son un sistema de forma libre por los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="8ab90-106">Active Directory Domain Services are a free-form system for the following reasons:</span></span>

-   <span data-ttu-id="8ab90-107">Los clientes requieren una solución muy distribuida en la que se puedan distribuir partes del directorio en sus redes y administrarse localmente.</span><span class="sxs-lookup"><span data-stu-id="8ab90-107">Customers require a highly distributed solution in which parts of the directory can be spread across their networks and administered locally.</span></span>
-   <span data-ttu-id="8ab90-108">A menudo, los clientes de gran tamaño crecen hasta millones de objetos, cientos o miles de réplicas, o ambos.</span><span class="sxs-lookup"><span data-stu-id="8ab90-108">Large customers often grow to millions of objects, hundreds or thousands of replicas, or both.</span></span>
-   <span data-ttu-id="8ab90-109">Muchas redes de clientes solo proporcionan conectividad intermitente a algunas ubicaciones; por ejemplo, las plataformas de perforación de petróleo remoto y se distribuyen al mar, por lo que el sistema debe ser tolerante a las operaciones parcialmente conectadas o desconectadas.</span><span class="sxs-lookup"><span data-stu-id="8ab90-109">Many customer networks provide only intermittent connectivity to some locations; for example, remote oil drilling platforms and ships at sea, so the system must be tolerant of partly connected or disconnected operations.</span></span>

<span data-ttu-id="8ab90-110">No hay ninguna manera de garantizar el conocimiento completo del estado actual o futuro de un sistema distribuido, ya que el conocimiento de los cambios de estado se debe propagar y la propagación lleva tiempo, durante el cual pueden producirse más cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="8ab90-110">There is no way to guarantee complete awareness of the current or future state of a distributed system because knowledge of state changes must be propagated and propagation takes time, during which more state changes may occur.</span></span>

<span data-ttu-id="8ab90-111">Los sistemas estrechamente acoplados controlan la incertidumbre al intentar eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="8ab90-111">Tightly coupled systems handle uncertainty by attempting to eliminate it.</span></span> <span data-ttu-id="8ab90-112">Esto se logra a través de las restricciones en las actualizaciones, que requieren que todos los nodos o la mayoría de los nodos estén disponibles antes de que se puedan realizar actualizaciones, mediante esquemas de bloqueo distribuidos o un solo maestro para los recursos críticos, restringiendo todos los nodos para que estén bien conectados o alguna combinación de estas técnicas.</span><span class="sxs-lookup"><span data-stu-id="8ab90-112">This is accomplished through constraints on updates, requiring all nodes or some majority of nodes to be available before updates can be performed, using distributed locking schemes or single-mastering for critical resources, constraining all nodes to be well-connected, or some combination of these techniques.</span></span> <span data-ttu-id="8ab90-113">Cuanto más estrechamente se acoplan los nodos informáticos en un sistema distribuido, menor es el límite de escalado.</span><span class="sxs-lookup"><span data-stu-id="8ab90-113">The more tightly coupled the computing nodes in a distributed system are, the lower the scaling limit.</span></span>

<span data-ttu-id="8ab90-114">Los sistemas de forma libre controlan la incertidumbre al tolerarlas.</span><span class="sxs-lookup"><span data-stu-id="8ab90-114">Free-form systems handle uncertainty by tolerating it.</span></span> <span data-ttu-id="8ab90-115">Un sistema de forma libre permite que los nodos tengan vistas diferentes del estado general del sistema y proporciona algoritmos para resolver conflictos.</span><span class="sxs-lookup"><span data-stu-id="8ab90-115">A free-form system enables the nodes to have differing views of the overall system state and provides algorithms for resolving conflicts.</span></span>

<span data-ttu-id="8ab90-116">Las soluciones estrechamente acopladas se rechazaron como inadecuadas para Active Directory Domain Services debido a los requisitos de administración local, operación desconectada y escalabilidad a un gran número de nodos.</span><span class="sxs-lookup"><span data-stu-id="8ab90-116">Tightly coupled solutions were rejected as unsuitable for Active Directory Domain Services because of the requirements for local administration, disconnected operation, and scalability to very large numbers of nodes.</span></span> <span data-ttu-id="8ab90-117">El modelo de acoplamiento flexible elegido, coherencia flexible de varios maestros con convergencia, satisface todos los requisitos.</span><span class="sxs-lookup"><span data-stu-id="8ab90-117">The loosely coupled model chosen, multi-master loose consistency with convergence, satisfies all requirements.</span></span>

 

 




