---
description: Contiene una lista de los equipos de la carpeta equipos de la herramienta de administración de servicios de componentes. Contiene un objeto para cada equipo.
ms.assetid: 56e32b47-a9f5-4888-b727-71ad0499da00
title: Colección ComputerList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComputerList
api_type:
- COM
api_location: ''
ms.openlocfilehash: 379e5e07a86d06961de3f8f3936a260451bf43ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496169"
---
# <a name="computerlist-collection"></a><span data-ttu-id="b9bc4-104">Colección ComputerList</span><span class="sxs-lookup"><span data-stu-id="b9bc4-104">ComputerList collection</span></span>

<span data-ttu-id="b9bc4-105">Contiene una lista de los equipos de la carpeta **equipos** de la herramienta de administración de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-105">Contains a list of the computers in the **Computers** folder of the Component Services administration tool.</span></span> <span data-ttu-id="b9bc4-106">Contiene un objeto para cada equipo.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-106">It contains an object for each computer.</span></span>

<span data-ttu-id="b9bc4-107">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b9bc4-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="b9bc4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b9bc4-108">Members</span></span>

<span data-ttu-id="b9bc4-109">La colección **ComputerList** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-109">The **ComputerList** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b9bc4-110">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="b9bc4-110">Related Collections</span></span>

<span data-ttu-id="b9bc4-111">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="b9bc4-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="b9bc4-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b9bc4-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="b9bc4-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b9bc4-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="b9bc4-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="b9bc4-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="b9bc4-115">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="b9bc4-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="b9bc4-116">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="b9bc4-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="b9bc4-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9bc4-117">Properties</span></span>

<span data-ttu-id="b9bc4-118">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="b9bc4-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b9bc4-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="b9bc4-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="b9bc4-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b9bc4-120">Name</span></span>



| <span data-ttu-id="b9bc4-121">Entrada</span><span class="sxs-lookup"><span data-stu-id="b9bc4-121">Entry</span></span> | <span data-ttu-id="b9bc4-122">Value</span><span class="sxs-lookup"><span data-stu-id="b9bc4-122">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9bc4-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9bc4-123">Description</span></span>    | <span data-ttu-id="b9bc4-124">Nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-124">The name of the computer.</span></span> <span data-ttu-id="b9bc4-125">Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-125">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b9bc4-126">Access</span><span class="sxs-lookup"><span data-stu-id="b9bc4-126">Access</span></span>         | <span data-ttu-id="b9bc4-127">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="b9bc4-127">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="b9bc4-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9bc4-128">Type</span></span>           | <span data-ttu-id="b9bc4-129">String</span><span class="sxs-lookup"><span data-stu-id="b9bc4-129">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b9bc4-130">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b9bc4-130">Default</span></span>        | <span data-ttu-id="b9bc4-131">"Nuevo equipo"</span><span class="sxs-lookup"><span data-stu-id="b9bc4-131">"New Computer"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b9bc4-132">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b9bc4-132">Minimum system</span></span> | <span data-ttu-id="b9bc4-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b9bc4-133">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="b9bc4-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9bc4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9bc4-135">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="b9bc4-135">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
