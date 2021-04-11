---
description: Recupera información sobre otras colecciones relacionadas con la colección desde la que se llama.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: Colección RelatedCollectionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 21a9a1905d75c81d605f30a3f6cffced8837034d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274947"
---
# <a name="relatedcollectioninfo-collection"></a><span data-ttu-id="74a7e-103">Colección RelatedCollectionInfo</span><span class="sxs-lookup"><span data-stu-id="74a7e-103">RelatedCollectionInfo collection</span></span>

<span data-ttu-id="74a7e-104">Recupera información sobre otras colecciones relacionadas con la colección desde la que se llama.</span><span class="sxs-lookup"><span data-stu-id="74a7e-104">Retrieves information about other collections related to the collection from which it is called.</span></span> <span data-ttu-id="74a7e-105">Se puede acceder a la colección **RelatedCollectionInfo** desde cualquier objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) mediante el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) .</span><span class="sxs-lookup"><span data-stu-id="74a7e-105">The **RelatedCollectionInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="74a7e-106">La colección **RelatedCollectionInfo** contiene un objeto para cada colección que es accesible desde la colección original.</span><span class="sxs-lookup"><span data-stu-id="74a7e-106">The **RelatedCollectionInfo** collection contains one object for each collection that is accessible from the original collection.</span></span> <span data-ttu-id="74a7e-107">Las colecciones relacionadas siguen la jerarquía de colecciones de herramientas de administración de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="74a7e-107">Related collections follow the Component Services administration tool collection hierarchy.</span></span>

<span data-ttu-id="74a7e-108">Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="74a7e-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="74a7e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="74a7e-109">Members</span></span>

<span data-ttu-id="74a7e-110">La colección **RelatedCollectionInfo** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="74a7e-110">The **RelatedCollectionInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="74a7e-111">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="74a7e-111">Related Collections</span></span>

<span data-ttu-id="74a7e-112">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="74a7e-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="74a7e-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="74a7e-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   <span data-ttu-id="74a7e-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="74a7e-114">**RelatedCollectionInfo**</span></span>

<span data-ttu-id="74a7e-115">Puede navegar a esta colección desde cada colección.</span><span class="sxs-lookup"><span data-stu-id="74a7e-115">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="74a7e-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="74a7e-116">Properties</span></span>

<span data-ttu-id="74a7e-117">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="74a7e-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="74a7e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="74a7e-118">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="74a7e-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="74a7e-119">Name</span></span>



| <span data-ttu-id="74a7e-120">Entrada</span><span class="sxs-lookup"><span data-stu-id="74a7e-120">Entry</span></span> | <span data-ttu-id="74a7e-121">Value</span><span class="sxs-lookup"><span data-stu-id="74a7e-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74a7e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="74a7e-122">Description</span></span>    | <span data-ttu-id="74a7e-123">Nombre de la colección relacionada.</span><span class="sxs-lookup"><span data-stu-id="74a7e-123">The name of the related collection.</span></span> <span data-ttu-id="74a7e-124">Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="74a7e-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="74a7e-125">Access</span><span class="sxs-lookup"><span data-stu-id="74a7e-125">Access</span></span>         | <span data-ttu-id="74a7e-126">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="74a7e-126">ReadOnly</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="74a7e-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="74a7e-127">Type</span></span>           | <span data-ttu-id="74a7e-128">String</span><span class="sxs-lookup"><span data-stu-id="74a7e-128">String</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="74a7e-129">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="74a7e-129">Default</span></span>        | <span data-ttu-id="74a7e-130">None</span><span class="sxs-lookup"><span data-stu-id="74a7e-130">None</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="74a7e-131">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="74a7e-131">Minimum system</span></span> | <span data-ttu-id="74a7e-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="74a7e-132">Windows 2000</span></span>                                                                                                                                                                                               |



 

## <a name="see-also"></a><span data-ttu-id="74a7e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="74a7e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74a7e-134">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="74a7e-134">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
