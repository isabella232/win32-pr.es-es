---
description: Cuando se instala en un servidor de aplicaciones, COM+ crea automáticamente una partición, conocida como la partición global.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Implementación de particiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714867"
---
# <a name="partition-implementation"></a><span data-ttu-id="fcba0-103">Implementación de particiones</span><span class="sxs-lookup"><span data-stu-id="fcba0-103">Partition Implementation</span></span>

<span data-ttu-id="fcba0-104">Cuando se instala en un servidor de aplicaciones, COM+ crea automáticamente una partición, conocida como la *partición global*.</span><span class="sxs-lookup"><span data-stu-id="fcba0-104">When installed on an application server, COM+ automatically creates a partition, known as the *global partition*.</span></span> <span data-ttu-id="fcba0-105">La partición global incluye un conjunto estándar de aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="fcba0-105">The global partition includes a standard set of COM+ applications.</span></span> <span data-ttu-id="fcba0-106">Las aplicaciones COM+ que están instaladas en la partición global están disponibles automáticamente para todos los usuarios del servidor.</span><span class="sxs-lookup"><span data-stu-id="fcba0-106">COM+ applications that are installed in the global partition are automatically available to all users on the server.</span></span> <span data-ttu-id="fcba0-107">Si tiene otras aplicaciones COM+ que le gustaría poner a disposición de todos los usuarios del servidor, puede agregarlas a la partición global.</span><span class="sxs-lookup"><span data-stu-id="fcba0-107">If you have other COM+ applications that you would like to make available to all users on the server, you can add them into the global partition.</span></span>

<span data-ttu-id="fcba0-108">Además de la partición global, puede crear otras particiones solo para los usuarios de ese servidor o para los usuarios de todo el dominio.</span><span class="sxs-lookup"><span data-stu-id="fcba0-108">In addition to the global partition, you can create other partitions for users on that server only, or for users throughout the domain.</span></span> <span data-ttu-id="fcba0-109">La creación de particiones adicionales y la instalación de varias configuraciones de una aplicación COM+ en ellas permite que los usuarios ejecuten esas configuraciones de aplicación simultáneamente en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="fcba0-109">Creating additional partitions and installing multiple configurations of a COM+ application into them allows your users to execute those application configurations simultaneously on the same computer.</span></span> <span data-ttu-id="fcba0-110">Además, al instalar las aplicaciones COM+ en una partición distinta de la partición global, puede controlar el acceso del usuario a esas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fcba0-110">Also, by installing COM+ applications into a partition other than the global partition, you can control user access to those applications.</span></span>

<span data-ttu-id="fcba0-111">**Windows XP:** La capacidad de crear, configurar o delegar particiones COM+ no está disponible.</span><span class="sxs-lookup"><span data-stu-id="fcba0-111">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="fcba0-112">La partición global es la única partición de COM+ disponible.</span><span class="sxs-lookup"><span data-stu-id="fcba0-112">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="fcba0-113">Para obtener más información sobre las particiones locales y las particiones definidas en Active Directory, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="fcba0-113">For more information on local partitions and partitions defined within Active Directory, see the following topics:</span></span>

-   [<span data-ttu-id="fcba0-114">Particiones locales</span><span class="sxs-lookup"><span data-stu-id="fcba0-114">Local Partitions</span></span>](local-partitions.md)
-   [<span data-ttu-id="fcba0-115">Particiones y Active Directory</span><span class="sxs-lookup"><span data-stu-id="fcba0-115">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
-   [<span data-ttu-id="fcba0-116">Particiones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="fcba0-116">Default Partitions</span></span>](default-partitions.md)
-   [<span data-ttu-id="fcba0-117">La partición global</span><span class="sxs-lookup"><span data-stu-id="fcba0-117">The Global Partition</span></span>](the-global-partition.md)
-   [<span data-ttu-id="fcba0-118">Propiedades de la partición</span><span class="sxs-lookup"><span data-stu-id="fcba0-118">Partition Properties</span></span>](partition-properties.md)

## <a name="related-topics"></a><span data-ttu-id="fcba0-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fcba0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcba0-120">Restricciones de diseño de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fcba0-120">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="fcba0-121">Particiones y componentes en cola de COM+</span><span class="sxs-lookup"><span data-stu-id="fcba0-121">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="fcba0-122">Registro y activación de componentes en particiones</span><span class="sxs-lookup"><span data-stu-id="fcba0-122">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="fcba0-123">¿Qué son las particiones COM+?</span><span class="sxs-lookup"><span data-stu-id="fcba0-123">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



