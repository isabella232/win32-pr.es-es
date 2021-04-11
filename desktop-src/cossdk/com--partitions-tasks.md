---
description: Tareas de particiones COM+
ms.assetid: ebcbfced-7d7a-46dc-a728-cdb920ccb874
title: Tareas de particiones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055976effb5d6a93523bab9d570aec685872ab91
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274897"
---
# <a name="com-partitions-tasks"></a><span data-ttu-id="08305-103">Tareas de particiones COM+</span><span class="sxs-lookup"><span data-stu-id="08305-103">COM+ Partitions Tasks</span></span>

<span data-ttu-id="08305-104">En los siguientes temas de esta sección se proporcionan instrucciones paso a paso para usar las particiones de COM+.</span><span class="sxs-lookup"><span data-stu-id="08305-104">The following topics in this section provide step-by-step instructions for using COM+ partitions.</span></span>

<span data-ttu-id="08305-105">**Windows XP:** La capacidad de crear, configurar o delegar particiones COM+ no está disponible.</span><span class="sxs-lookup"><span data-stu-id="08305-105">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="08305-106">La partición global es la única partición de COM+ disponible.</span><span class="sxs-lookup"><span data-stu-id="08305-106">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="08305-107">\* \* Windows 2000: \* \* el servicio de particiones COM+ no está disponible en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="08305-107">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>



| <span data-ttu-id="08305-108">Tema</span><span class="sxs-lookup"><span data-stu-id="08305-108">Topic</span></span>                                                                                                         | <span data-ttu-id="08305-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="08305-109">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08305-110">Crear y configurar particiones COM+</span><span class="sxs-lookup"><span data-stu-id="08305-110">Creating and Configuring COM+ Partitions</span></span>](creating-and-configuring-com--partitions.md)<br/>           | <span data-ttu-id="08305-111">Describe cómo crear y configurar una partición de COM+.</span><span class="sxs-lookup"><span data-stu-id="08305-111">Describes how to create and configure a COM+ partition.</span></span><br/>                             |
| [<span data-ttu-id="08305-112">Administrar particiones locales</span><span class="sxs-lookup"><span data-stu-id="08305-112">Managing Local Partitions</span></span>](managing-local-partitions.md)<br/>                                         | <span data-ttu-id="08305-113">Describe cómo administrar particiones COM+ que no están dentro de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="08305-113">Describes how to manage COM+ partitions that are not within Active Directory.</span></span><br/>       |
| [<span data-ttu-id="08305-114">Administrar particiones en Active Directory</span><span class="sxs-lookup"><span data-stu-id="08305-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)<br/>     | <span data-ttu-id="08305-115">Describe cómo administrar las particiones COM+ que se especifican en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="08305-115">Describes how to manage COM+ partitions that are specified within Active Directory.</span></span><br/> |
| [<span data-ttu-id="08305-116">Establecer derechos administrativos para una partición</span><span class="sxs-lookup"><span data-stu-id="08305-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)<br/> | <span data-ttu-id="08305-117">Describe cómo establecer privilegios de seguridad para una partición de COM+.</span><span class="sxs-lookup"><span data-stu-id="08305-117">Describes how to set security privileges for a COM+ partition.</span></span><br/>                      |
| [<span data-ttu-id="08305-118">Agrupar aplicaciones en particiones</span><span class="sxs-lookup"><span data-stu-id="08305-118">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)<br/>                 | <span data-ttu-id="08305-119">Describe cómo configurar aplicaciones COM+ para que pertenezcan a una partición COM+.</span><span class="sxs-lookup"><span data-stu-id="08305-119">Describes how to configure COM+ applications to belong to a COM+ partition.</span></span> <br/>        |
| [<span data-ttu-id="08305-120">Recopilación de métricas de partición</span><span class="sxs-lookup"><span data-stu-id="08305-120">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)<br/>                                   | <span data-ttu-id="08305-121">Describe cómo recopilar datos sobre las particiones de COM+.</span><span class="sxs-lookup"><span data-stu-id="08305-121">Describes how to collect data about COM+ partitions.</span></span><br/>                                |
| [<span data-ttu-id="08305-122">Configuración de la memoria caché de partición</span><span class="sxs-lookup"><span data-stu-id="08305-122">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)<br/>                             | <span data-ttu-id="08305-123">Describe cómo configurar la caché de particiones de COM+.</span><span class="sxs-lookup"><span data-stu-id="08305-123">Describes how to configure the COM+ partition cache.</span></span><br/>                                |



 

> [!Note]  
> <span data-ttu-id="08305-124">El servicio de particiones COM+ no está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="08305-124">The COM+ Partitions service is not enabled by default.</span></span> <span data-ttu-id="08305-125">Para usar el servicio de particiones de COM+, debe habilitarlo mediante la herramienta de administración de servicios de componentes o cambiando la propiedad PartitionsEnabled de la colección [**LocalComputer**](localcomputer.md) a true.</span><span class="sxs-lookup"><span data-stu-id="08305-125">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="08305-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08305-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08305-127">Conceptos de particiones COM+</span><span class="sxs-lookup"><span data-stu-id="08305-127">COM+ Partitions Concepts</span></span>](com--partitions-concepts.md)
</dt> </dl>

 

 




