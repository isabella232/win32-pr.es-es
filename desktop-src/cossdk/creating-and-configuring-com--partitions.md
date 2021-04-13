---
description: Los administradores pueden utilizar COM+ para crear y configurar particiones COM+ mediante programación.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Crear y configurar particiones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf654c25c75cc2e12f55b7ee826184fdeb04a214
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538823"
---
# <a name="creating-and-configuring-com-partitions"></a><span data-ttu-id="6395b-103">Crear y configurar particiones COM+</span><span class="sxs-lookup"><span data-stu-id="6395b-103">Creating and Configuring COM+ Partitions</span></span>

<span data-ttu-id="6395b-104">Los administradores pueden utilizar COM+ para crear y configurar particiones COM+ mediante programación.</span><span class="sxs-lookup"><span data-stu-id="6395b-104">Administrators can use COM+ to programmatically create and configure COM+ partitions.</span></span> <span data-ttu-id="6395b-105">De hecho, todas las tareas de creación y configuración que puede realizar un administrador desde los servicios de componentes o las herramientas administrativas de Active Directory usuarios y equipos se pueden realizar mediante colecciones, objetos e interfaces COM+ o a través de la interfaz del sistema Active Directory (ADSI).</span><span class="sxs-lookup"><span data-stu-id="6395b-105">In fact, all creation and configuration tasks that an administrator can do from the Component Services or the Active Directory Users and Computers administrative tools can be done by using COM+ collections, objects, and interfaces or through the Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="6395b-106">**Windows XP:** La capacidad de crear, configurar o delegar particiones COM+ no está disponible.</span><span class="sxs-lookup"><span data-stu-id="6395b-106">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="6395b-107">La partición global es la única partición de COM+ disponible.</span><span class="sxs-lookup"><span data-stu-id="6395b-107">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="6395b-108">\* \* Windows 2000: \* \* el servicio de particiones COM+ no está disponible en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6395b-108">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>

> [!Note]  
> <span data-ttu-id="6395b-109">El servicio de particiones COM+ no está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6395b-109">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="6395b-110">Para usar el servicio de particiones de COM+, debe habilitarlo mediante la herramienta de administración de servicios de componentes o cambiando la propiedad PartitionsEnabled de la colección [**LocalComputer**](localcomputer.md) a true.</span><span class="sxs-lookup"><span data-stu-id="6395b-110">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="6395b-111">Para realizar tareas relacionadas con las particiones, COM+ proporciona los siguientes elementos de programación:</span><span class="sxs-lookup"><span data-stu-id="6395b-111">To accomplish partition-related tasks, COM+ provides the following programming elements:</span></span>

-   <span data-ttu-id="6395b-112">Métodos y propiedades de la interfaz [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) en la clase [**COMAdminCatalog**](comadmincatalog.md) :</span><span class="sxs-lookup"><span data-stu-id="6395b-112">Methods and properties of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface on the [**COMAdminCatalog**](comadmincatalog.md) class:</span></span>
    -   <span data-ttu-id="6395b-113">Propiedad [**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) .</span><span class="sxs-lookup"><span data-stu-id="6395b-113">[**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) property.</span></span>
    -   <span data-ttu-id="6395b-114">Propiedad [**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="6395b-114">[**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) property.</span></span>
    -   <span data-ttu-id="6395b-115">Propiedad [**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) .</span><span class="sxs-lookup"><span data-stu-id="6395b-115">[**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) property.</span></span>
    -   <span data-ttu-id="6395b-116">Método [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .</span><span class="sxs-lookup"><span data-stu-id="6395b-116">[**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>
    -   <span data-ttu-id="6395b-117">Método [**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="6395b-117">[**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) method.</span></span>
    -   <span data-ttu-id="6395b-118">Método [**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) .</span><span class="sxs-lookup"><span data-stu-id="6395b-118">[**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) method.</span></span>
    -   <span data-ttu-id="6395b-119">Propiedad [**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="6395b-119">[**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) property.</span></span>
-   <span data-ttu-id="6395b-120">Un conjunto de objetos COM+ para crear y administrar particiones en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6395b-120">A set of COM+ objects for creating and managing partitions in Active Directory.</span></span>
-   <span data-ttu-id="6395b-121">Una clave del registro de COM+, **PartitionCache**, para cambiar el tamaño de la memoria caché de la partición.</span><span class="sxs-lookup"><span data-stu-id="6395b-121">A COM+ registry key, **PartitionCache**, for changing the partition cache size.</span></span>
-   <span data-ttu-id="6395b-122">Un conjunto de colecciones de administración de [com+](com--administration-collections.md)relacionadas con las particiones:</span><span class="sxs-lookup"><span data-stu-id="6395b-122">A set of partitions-related [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="6395b-123">Colección de [**particiones**](partitions.md) .</span><span class="sxs-lookup"><span data-stu-id="6395b-123">[**Partitions**](partitions.md) collection.</span></span>
    -   <span data-ttu-id="6395b-124">Colección [**PartitionUsers**](partitionusers.md) .</span><span class="sxs-lookup"><span data-stu-id="6395b-124">[**PartitionUsers**](partitionusers.md) collection.</span></span>
    -   <span data-ttu-id="6395b-125">Colección [**RolesForPartition**](rolesforpartition.md) .</span><span class="sxs-lookup"><span data-stu-id="6395b-125">[**RolesForPartition**](rolesforpartition.md) collection.</span></span>
    -   <span data-ttu-id="6395b-126">Colección [**UsersInPartitionRole**](usersinpartitionrole.md) .</span><span class="sxs-lookup"><span data-stu-id="6395b-126">[**UsersInPartitionRole**](usersinpartitionrole.md) collection.</span></span>
-   <span data-ttu-id="6395b-127">Propiedades de otras [colecciones de administración de com+](com--administration-collections.md):</span><span class="sxs-lookup"><span data-stu-id="6395b-127">Properties of other [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="6395b-128">Propiedad PartitionID de la colección [**ApplicationInstances**](applicationinstances.md) .</span><span class="sxs-lookup"><span data-stu-id="6395b-128">PartitionID property on the [**ApplicationInstances**](applicationinstances.md) collection.</span></span>
    -   <span data-ttu-id="6395b-129">Propiedad AppPartitionID en la colección [**Applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="6395b-129">AppPartitionID property on the [**Applications**](applications.md) collection.</span></span>
    -   <span data-ttu-id="6395b-130">Propiedades PartitionDescription, PartitionID y PartitionName en la colección [**FilesForImport**](filesforimport.md) .</span><span class="sxs-lookup"><span data-stu-id="6395b-130">PartitionDescription, PartitionID, and PartitionName properties on the [**FilesForImport**](filesforimport.md) collection.</span></span>
    -   <span data-ttu-id="6395b-131">Propiedades DSPartitionLookupEnabled, LocalPartitionLookupEnabled y PartitionsEnabled en la colección [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="6395b-131">DSPartitionLookupEnabled, LocalPartitionLookupEnabled, and PartitionsEnabled properties on the [**LocalComputer**](localcomputer.md) collection.</span></span>
    -   <span data-ttu-id="6395b-132">Propiedades EventClassPartitionID y SubscriberPartitionID en la colección [**SubscriptionsForComponent**](subscriptionsforcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="6395b-132">EventClassPartitionID and SubscriberPartitionID properties on the [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>
    -   <span data-ttu-id="6395b-133">Propiedades EventClassPartitionID y SubscriberPartitionID en la colección [**TransientSubscriptions**](transientsubscriptions.md) .</span><span class="sxs-lookup"><span data-stu-id="6395b-133">EventClassPartitionID and SubscriberPartitionID properties on the [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6395b-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6395b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6395b-135">Recopilación de métricas de partición</span><span class="sxs-lookup"><span data-stu-id="6395b-135">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="6395b-136">Configuración de la memoria caché de partición</span><span class="sxs-lookup"><span data-stu-id="6395b-136">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="6395b-137">Agrupar aplicaciones en particiones</span><span class="sxs-lookup"><span data-stu-id="6395b-137">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="6395b-138">Administrar particiones locales</span><span class="sxs-lookup"><span data-stu-id="6395b-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="6395b-139">Administrar particiones en Active Directory</span><span class="sxs-lookup"><span data-stu-id="6395b-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="6395b-140">Establecer derechos administrativos para una partición</span><span class="sxs-lookup"><span data-stu-id="6395b-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



