---
description: Particiones predeterminadas
ms.assetid: ce6ad7c1-d4a1-4573-860e-f7859c588773
title: Particiones predeterminadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b6b2480958c78a53c264804eb1f292808545
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275092"
---
# <a name="default-partitions"></a><span data-ttu-id="5e9a1-103">Particiones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="5e9a1-103">Default Partitions</span></span>

<span data-ttu-id="5e9a1-104">Cuando se asigna una partición predeterminada a un usuario, COM+ intenta activar primero los componentes de esa partición.</span><span class="sxs-lookup"><span data-stu-id="5e9a1-104">When a default partition is assigned to a user, COM+ attempts to activate components in that partition first.</span></span> <span data-ttu-id="5e9a1-105">Si se produce un error en la activación, COM+ busca en la partición global el componente que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="5e9a1-105">If the activation fails, COM+ searches the global partition for the component to activate.</span></span> <span data-ttu-id="5e9a1-106">La excepción a este proceso se produce cuando el componente COM+ incluye un moniker de partición, que especifica explícitamente la partición en la que se encuentra el componente.</span><span class="sxs-lookup"><span data-stu-id="5e9a1-106">The exception to this process occurs when the COM+ component includes a partition moniker, which explicitly specifies the partition in which the component is located.</span></span> <span data-ttu-id="5e9a1-107">En este caso, el moniker de la partición tiene prioridad sobre cualquier configuración de partición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5e9a1-107">In this case, the partition moniker takes precedence over any default partition configuration.</span></span>

<span data-ttu-id="5e9a1-108">Cuando se usan particiones locales, la partición predeterminada se asigna a los usuarios mediante la carpeta **com+ Partition users** de la herramienta administrativa Servicios de componentes en el servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5e9a1-108">When using local partitions, the default partition is assigned to users using the **COM+ Partition Users** folder in the Component Services administrative tool on the application server.</span></span> <span data-ttu-id="5e9a1-109">Cuando se usan conjuntos de particiones en el Active Directory, la partición predeterminada del usuario viene determinada por el conjunto de particiones del usuario.</span><span class="sxs-lookup"><span data-stu-id="5e9a1-109">When using partition sets in the Active Directory, the user's default partition is determined by the user's partition set.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e9a1-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e9a1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e9a1-111">Particiones locales</span><span class="sxs-lookup"><span data-stu-id="5e9a1-111">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="5e9a1-112">Propiedades de la partición</span><span class="sxs-lookup"><span data-stu-id="5e9a1-112">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="5e9a1-113">Particiones y Active Directory</span><span class="sxs-lookup"><span data-stu-id="5e9a1-113">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> <dt>

[<span data-ttu-id="5e9a1-114">La partición global</span><span class="sxs-lookup"><span data-stu-id="5e9a1-114">The Global Partition</span></span>](the-global-partition.md)
</dt> </dl>

 

 



