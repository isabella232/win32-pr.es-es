---
description: Recupera información sobre las propiedades que admite una colección especificada.
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: PropertyInfo (colección)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: bd9fdd2262d4499efd6a86fbc5b99bae786016f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153197"
---
# <a name="propertyinfo-collection"></a><span data-ttu-id="30127-103">PropertyInfo (colección)</span><span class="sxs-lookup"><span data-stu-id="30127-103">PropertyInfo collection</span></span>

<span data-ttu-id="30127-104">Recupera información sobre las propiedades que admite una colección especificada.</span><span class="sxs-lookup"><span data-stu-id="30127-104">Retrieves information about the properties that a specified collection supports.</span></span> <span data-ttu-id="30127-105">La colección **PropertyInfo** es accesible desde cualquier objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) mediante el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) .</span><span class="sxs-lookup"><span data-stu-id="30127-105">The **PropertyInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="30127-106">La colección **PropertyInfo** contiene un objeto para cada propiedad admitida por la colección original.</span><span class="sxs-lookup"><span data-stu-id="30127-106">The **PropertyInfo** collection contains one object for each property that is supported by the original collection.</span></span>

## <a name="members"></a><span data-ttu-id="30127-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="30127-107">Members</span></span>

<span data-ttu-id="30127-108">La colección **PropertyInfo** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="30127-108">The **PropertyInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="30127-109">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="30127-109">Related Collections</span></span>

<span data-ttu-id="30127-110">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="30127-110">You can navigate from this collection to any of the following collections:</span></span>

-   <span data-ttu-id="30127-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="30127-111">**PropertyInfo**</span></span>
-   [<span data-ttu-id="30127-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="30127-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="30127-113">Puede navegar a esta colección desde cada colección.</span><span class="sxs-lookup"><span data-stu-id="30127-113">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="30127-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="30127-114">Properties</span></span>

<span data-ttu-id="30127-115">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="30127-115">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="30127-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="30127-116">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="30127-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="30127-117">Name</span></span>



| <span data-ttu-id="30127-118">Entrada</span><span class="sxs-lookup"><span data-stu-id="30127-118">Entry</span></span> | <span data-ttu-id="30127-119">Value</span><span class="sxs-lookup"><span data-stu-id="30127-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30127-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="30127-120">Description</span></span>    | <span data-ttu-id="30127-121">Nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="30127-121">The name of the property.</span></span> <span data-ttu-id="30127-122">Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="30127-122">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="30127-123">Access</span><span class="sxs-lookup"><span data-stu-id="30127-123">Access</span></span>         | <span data-ttu-id="30127-124">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="30127-124">ReadOnly</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="30127-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="30127-125">Type</span></span>           | <span data-ttu-id="30127-126">String</span><span class="sxs-lookup"><span data-stu-id="30127-126">String</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="30127-127">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="30127-127">Default</span></span>        | <span data-ttu-id="30127-128">None</span><span class="sxs-lookup"><span data-stu-id="30127-128">None</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="30127-129">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="30127-129">Minimum system</span></span> | <span data-ttu-id="30127-130">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="30127-130">Windows 2000</span></span>                                                                                                                                                                                     |



 

## <a name="see-also"></a><span data-ttu-id="30127-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="30127-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30127-132">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="30127-132">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
