---
description: Contiene las colecciones de nivel superior en el catálogo.
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: Colección raíz
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Root
api_type:
- COM
api_location: ''
ms.openlocfilehash: ad896c69ab6fad75179c9bb30668143aa2ea741e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696102"
---
# <a name="root-collection"></a><span data-ttu-id="a2a4c-103">Colección raíz</span><span class="sxs-lookup"><span data-stu-id="a2a4c-103">Root collection</span></span>

<span data-ttu-id="a2a4c-104">Contiene las colecciones de nivel superior en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="a2a4c-104">Contains the top-level collections in the catalog.</span></span> <span data-ttu-id="a2a4c-105">No contiene ningún objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) ni admite ninguna propiedad.</span><span class="sxs-lookup"><span data-stu-id="a2a4c-105">It does not contain any [**COMAdminCatalogObject**](comadmincatalogobject.md) objects or support any properties.</span></span>

<span data-ttu-id="a2a4c-106">La colección **raíz** no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="a2a4c-106">The **Root** collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

<span data-ttu-id="a2a4c-107">No se puede navegar a la colección **raíz** desde cualquier colección.</span><span class="sxs-lookup"><span data-stu-id="a2a4c-107">You cannot navigate to the **Root** collection from any collection.</span></span>

## <a name="members"></a><span data-ttu-id="a2a4c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2a4c-108">Members</span></span>

<span data-ttu-id="a2a4c-109">La colección **raíz** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="a2a4c-109">The **Root** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="a2a4c-110">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="a2a4c-110">Related Collections</span></span>

<span data-ttu-id="a2a4c-111">A continuación se muestran las colecciones de nivel superior del catálogo:</span><span class="sxs-lookup"><span data-stu-id="a2a4c-111">The following are the top-level collections in the catalog:</span></span>

-   [<span data-ttu-id="a2a4c-112">**ApplicationCluster**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-112">**ApplicationCluster**</span></span>](applicationcluster.md)
-   [<span data-ttu-id="a2a4c-113">**ApplicationInstances**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-113">**ApplicationInstances**</span></span>](applicationinstances.md)
-   [<span data-ttu-id="a2a4c-114">**APLICACIONES**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-114">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="a2a4c-115">**ComputerList**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-115">**ComputerList**</span></span>](computerlist.md)
-   [<span data-ttu-id="a2a4c-116">**DCOMProtocols**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-116">**DCOMProtocols**</span></span>](dcomprotocols.md)
-   [<span data-ttu-id="a2a4c-117">**EventClassesForIID**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-117">**EventClassesForIID**</span></span>](eventclassesforiid.md)
-   [<span data-ttu-id="a2a4c-118">**FilesForImport**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-118">**FilesForImport**</span></span>](filesforimport.md)
-   [<span data-ttu-id="a2a4c-119">**InprocServers**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-119">**InprocServers**</span></span>](inprocservers.md)
-   [<span data-ttu-id="a2a4c-120">**LegacyServers**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-120">**LegacyServers**</span></span>](legacyservers.md)
-   [<span data-ttu-id="a2a4c-121">**LocalComputer**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-121">**LocalComputer**</span></span>](localcomputer.md)
-   [<span data-ttu-id="a2a4c-122">**Particiones**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-122">**Partitions**</span></span>](partitions.md)
-   [<span data-ttu-id="a2a4c-123">**PartitionUsers**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-123">**PartitionUsers**</span></span>](partitionusers.md)
-   [<span data-ttu-id="a2a4c-124">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-124">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="a2a4c-125">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-125">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="a2a4c-126">**TransientSubscriptions**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-126">**TransientSubscriptions**</span></span>](transientsubscriptions.md)
-   [<span data-ttu-id="a2a4c-127">**WOWInprocServers**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-127">**WOWInprocServers**</span></span>](wowinprocservers.md)
-   [<span data-ttu-id="a2a4c-128">**WOWLegacyServers**</span><span class="sxs-lookup"><span data-stu-id="a2a4c-128">**WOWLegacyServers**</span></span>](wowlegacyservers.md)

## <a name="see-also"></a><span data-ttu-id="a2a4c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2a4c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2a4c-130">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="a2a4c-130">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
