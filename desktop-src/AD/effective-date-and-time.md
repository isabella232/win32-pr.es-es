---
title: Fecha y hora efectivas
description: La fecha y hora efectivas es una estrategia de prevención que evita el sesgo de la versión y las actualizaciones parciales al aplazar los datos efectivos de la información a algún punto del futuro cuando el cambio tiene una alta probabilidad de que se replique por completo.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448941b7ab0d85d50123985a120beb04f256d877
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075138"
---
# <a name="effective-date-and-time"></a><span data-ttu-id="be778-103">Fecha y hora efectivas</span><span class="sxs-lookup"><span data-stu-id="be778-103">Effective Date and Time</span></span>

<span data-ttu-id="be778-104">La *fecha y hora efectivas* es una estrategia de prevención que evita el sesgo de la versión y las actualizaciones parciales al aplazar los datos efectivos de la información a algún punto del futuro cuando el cambio tiene una alta probabilidad de que se replique por completo.</span><span class="sxs-lookup"><span data-stu-id="be778-104">*Effective date and time* is an avoidance strategy that prevents version skew and partial updates by deferring the effective data of information to some point in the future when the change has a high probability of being fully replicated.</span></span> <span data-ttu-id="be778-105">Para implementar fechas efectivas, los objetos de aplicación deben incluir una marca de tiempo de fecha efectiva, que se rellena cuando se crea o cambia el objeto.</span><span class="sxs-lookup"><span data-stu-id="be778-105">To implement effective dates, the application objects must include an effective date timestamp, which is filled in when the object is created or changed.</span></span> <span data-ttu-id="be778-106">Los consumidores de los objetos comprueban la marca de tiempo y aplazan el uso de los objetos hasta que se alcanza esa fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="be778-106">Consumers of the objects verify the timestamp and defer use of the objects until that date and time are reached.</span></span>

<span data-ttu-id="be778-107">Algunas consideraciones importantes:</span><span class="sxs-lookup"><span data-stu-id="be778-107">Some important considerations:</span></span>

-   <span data-ttu-id="be778-108">Las aplicaciones que eligen este enfoque deben asegurarse de que haya un conjunto de datos aplicables para usar hasta que los objetos actualizados surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="be778-108">Applications that choose this approach must ensure that there is a set of applicable data to use until the updated objects become effective.</span></span>
-   <span data-ttu-id="be778-109">El servicio de hora distribuida en Windows NT 4,0 mantiene sincronizados los relojes de la sincronización de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="be778-109">Distributed time service in Windows NT 4.0 keeps the clocks of the connected Windows 2000 synchronized.</span></span> <span data-ttu-id="be778-110">Sin embargo, no hay ningún servicio de hora perfecto, por lo que hay una pequeña ventana para el sesgo de la versión.</span><span class="sxs-lookup"><span data-stu-id="be778-110">No time service is perfect, however, so there is a small window for version skew.</span></span>
-   <span data-ttu-id="be778-111">La configuración de una buena fecha efectiva presupone el conocimiento de la latencia general de replicación para el sistema distribuido en cuestión.</span><span class="sxs-lookup"><span data-stu-id="be778-111">Setting a good effective date presumes knowledge of the overall replication latency for the distributed system in question.</span></span> <span data-ttu-id="be778-112">En una red estable, una buena regla general para las fechas efectivas es la (hora de la actualización) + (2 \* (latencia total media)).</span><span class="sxs-lookup"><span data-stu-id="be778-112">In a stable network a good rule of thumb for effective dates is the (time of the update) + (2\*(average overall latency)).</span></span> <span data-ttu-id="be778-113">Por lo tanto, para un sistema cuya latencia total promedio sea de 4 horas, un retraso de 8 horas es razonable.</span><span class="sxs-lookup"><span data-stu-id="be778-113">So, for a system whose overall latency averages 4 hours, a delay of 8 hours is reasonable.</span></span>
-   <span data-ttu-id="be778-114">En una red inestable, es mucho más difícil determinar un valor "bueno" para las fechas efectivas, ya que la latencia puede ser muy variable.</span><span class="sxs-lookup"><span data-stu-id="be778-114">In an unstable network, determining a "good" value for effective dates is much more difficult, since the latency may be highly variable.</span></span> <span data-ttu-id="be778-115">La fecha efectiva es la más "efectiva" en una red inestable cuando se combina con otras estrategias de prevención o detección, como sumas de comprobación o GUID de coherencia.</span><span class="sxs-lookup"><span data-stu-id="be778-115">Effective date is most "effective" in an unstable network when combined with other avoidance or detection strategies such as checksums or consistency GUIDs.</span></span> <span data-ttu-id="be778-116">Para obtener más información, vea [sumas de comprobación y recuentos de objetos](checksums-and-object-counts.md).</span><span class="sxs-lookup"><span data-stu-id="be778-116">For more information, see [Checksums and Object Counts](checksums-and-object-counts.md).</span></span>

 

 




