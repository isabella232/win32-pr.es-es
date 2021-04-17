---
description: Conceptos de particiones COM+
ms.assetid: 9fc35bef-ecc1-4764-bf69-ec89560daff4
title: Conceptos de particiones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 483a34e6186cda8978c1882ed1fdfbe8732f7ec8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496061"
---
# <a name="com-partitions-concepts"></a><span data-ttu-id="9d0f1-103">Conceptos de particiones COM+</span><span class="sxs-lookup"><span data-stu-id="9d0f1-103">COM+ Partitions Concepts</span></span>

<span data-ttu-id="9d0f1-104">En entornos informáticos en los que es necesario utilizar diferentes versiones o configuraciones de una aplicación en el mismo equipo, pueden producirse conflictos cuando una versión de la aplicación requiere componentes diferentes a los otros o cuando una versión requiere un componente en el equipo que no es compatible con la otra versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9d0f1-104">In computing environments where it's necessary to use different versions or configurations of an application on the same computer, conflicts can arise when one version of the application requires different components than the other or when one version requires a component on the computer that is incompatible with the other version of the application.</span></span> <span data-ttu-id="9d0f1-105">En el pasado, la única manera de resolver este problema era mantener varios equipos y ejecutar una versión diferente de la aplicación en cada equipo.</span><span class="sxs-lookup"><span data-stu-id="9d0f1-105">In the past, the only way to solve this problem was to maintain multiple computers and run a different version of the application on each computer.</span></span> <span data-ttu-id="9d0f1-106">Este enfoque es costoso e ineficaz porque aumenta los costos de hardware y la sobrecarga administrativa.</span><span class="sxs-lookup"><span data-stu-id="9d0f1-106">Such an approach is costly and inefficient because it increases hardware costs and administrative overhead.</span></span>

<span data-ttu-id="9d0f1-107">COM+ soluciona este problema proporcionando la característica de particiones de COM+.</span><span class="sxs-lookup"><span data-stu-id="9d0f1-107">COM+ solves this problem by providing the COM+ partitions feature.</span></span> <span data-ttu-id="9d0f1-108">Puede usar particiones COM+ para instalar diferentes versiones de una aplicación COM+ en un equipo y ejecutarlas simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="9d0f1-108">You can use COM+ partitions to install different versions of a COM+ application on a computer and run them simultaneously.</span></span>

<span data-ttu-id="9d0f1-109">Para comprender y usar esta característica, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="9d0f1-109">To understand and use this feature, see the following topics:</span></span>

-   [<span data-ttu-id="9d0f1-110">¿Qué son las particiones COM+?</span><span class="sxs-lookup"><span data-stu-id="9d0f1-110">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
-   [<span data-ttu-id="9d0f1-111">Implementación de particiones</span><span class="sxs-lookup"><span data-stu-id="9d0f1-111">Partition Implementation</span></span>](partition-implementation.md)
-   [<span data-ttu-id="9d0f1-112">Registro y activación de componentes en particiones</span><span class="sxs-lookup"><span data-stu-id="9d0f1-112">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
-   [<span data-ttu-id="9d0f1-113">Particiones y componentes en cola de COM+</span><span class="sxs-lookup"><span data-stu-id="9d0f1-113">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
-   [<span data-ttu-id="9d0f1-114">Restricciones de diseño de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9d0f1-114">Application Design Restrictions</span></span>](application-design-restrictions.md)

## <a name="related-topics"></a><span data-ttu-id="9d0f1-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d0f1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d0f1-116">Tareas de particiones COM+</span><span class="sxs-lookup"><span data-stu-id="9d0f1-116">COM+ Partitions Tasks</span></span>](com--partitions-tasks.md)
</dt> </dl>

 

 



