---
description: Contiene una lista de los equipos servidor del clúster de aplicaciones. Contiene un objeto para cada servidor.
ms.assetid: 8722080a-cf95-4c29-9eb7-99c6df93611f
title: Colección ApplicationCluster
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationCluster
api_type:
- COM
api_location: ''
ms.openlocfilehash: 00a54f5c79bcbaf4ef61b130db556fc27f264101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153028"
---
# <a name="applicationcluster-collection"></a><span data-ttu-id="5abd3-104">Colección ApplicationCluster</span><span class="sxs-lookup"><span data-stu-id="5abd3-104">ApplicationCluster collection</span></span>

<span data-ttu-id="5abd3-105">Contiene una lista de los equipos servidor del clúster de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5abd3-105">Contains a list of the server computers in the application cluster.</span></span> <span data-ttu-id="5abd3-106">Contiene un objeto para cada servidor.</span><span class="sxs-lookup"><span data-stu-id="5abd3-106">It contains an object for each server.</span></span> <span data-ttu-id="5abd3-107">Se trata de una colección de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="5abd3-107">This is a top-level collection.</span></span>

<span data-ttu-id="5abd3-108">El clúster de aplicación se define para los fines del servicio de equilibrio de carga de componentes (CLB).</span><span class="sxs-lookup"><span data-stu-id="5abd3-108">The application cluster is defined for purposes of the component load balancing (CLB) service.</span></span> <span data-ttu-id="5abd3-109">Para que se use la colección de clústeres de aplicación, el servicio CLB debe estar instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="5abd3-109">For the application cluster collection to be used, the CLB service must be installed on the computer.</span></span>

<span data-ttu-id="5abd3-110">Designe un enrutador en el clúster de aplicaciones con la propiedad IsRouter en el objeto de colección [**LocalComputer**](localcomputer.md) y designe que un componente determinado debe tener equilibrio de carga con la propiedad LoadBalancingSupported en un objeto de colección [**Components**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="5abd3-110">You designate a router in the application cluster with the IsRouter property on the [**LocalComputer**](localcomputer.md) collection object, and you designate that a given component should be load balanced with the LoadBalancingSupported property on a [**Components**](components.md) collection object.</span></span>

<span data-ttu-id="5abd3-111">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="5abd3-111">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="5abd3-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="5abd3-112">Members</span></span>

<span data-ttu-id="5abd3-113">La colección **ApplicationCluster** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="5abd3-113">The **ApplicationCluster** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="5abd3-114">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="5abd3-114">Related Collections</span></span>

<span data-ttu-id="5abd3-115">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="5abd3-115">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="5abd3-116">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5abd3-116">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="5abd3-117">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="5abd3-117">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="5abd3-118">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="5abd3-118">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="5abd3-119">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="5abd3-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="5abd3-120">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="5abd3-120">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="5abd3-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5abd3-121">Properties</span></span>

<span data-ttu-id="5abd3-122">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="5abd3-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="5abd3-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="5abd3-123">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="5abd3-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="5abd3-124">Name</span></span>



| <span data-ttu-id="5abd3-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="5abd3-125">Entry</span></span> | <span data-ttu-id="5abd3-126">Value</span><span class="sxs-lookup"><span data-stu-id="5abd3-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5abd3-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="5abd3-127">Description</span></span>    | <span data-ttu-id="5abd3-128">Nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="5abd3-128">The name of the server.</span></span> <span data-ttu-id="5abd3-129">Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="5abd3-129">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="5abd3-130">Access</span><span class="sxs-lookup"><span data-stu-id="5abd3-130">Access</span></span>         | <span data-ttu-id="5abd3-131">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="5abd3-131">WriteOnce</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="5abd3-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="5abd3-132">Type</span></span>           | <span data-ttu-id="5abd3-133">String</span><span class="sxs-lookup"><span data-stu-id="5abd3-133">String</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="5abd3-134">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="5abd3-134">Default</span></span>        | <span data-ttu-id="5abd3-135">"Nuevo equipo"</span><span class="sxs-lookup"><span data-stu-id="5abd3-135">"New Computer"</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="5abd3-136">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="5abd3-136">Minimum system</span></span> | <span data-ttu-id="5abd3-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5abd3-137">Windows 2000</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="5abd3-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="5abd3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5abd3-139">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="5abd3-139">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
