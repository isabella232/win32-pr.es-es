---
description: 'Colección UsersInRole: contiene un objeto para cada usuario del rol con el que está relacionada la colección.'
ms.assetid: e7d9e5e8-1927-42b2-bdd5-0c49a562c31f
title: Colección UsersInRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b73c495a1af1dec9114e5a59274e457c1d09694
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105543"
---
# <a name="usersinrole-collection"></a><span data-ttu-id="30efe-103">Colección UsersInRole</span><span class="sxs-lookup"><span data-stu-id="30efe-103">UsersInRole collection</span></span>

<span data-ttu-id="30efe-104">Contiene un objeto para cada usuario del rol con el que está relacionada la colección.</span><span class="sxs-lookup"><span data-stu-id="30efe-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="30efe-105">Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)</span><span class="sxs-lookup"><span data-stu-id="30efe-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="30efe-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="30efe-106">Members</span></span>

<span data-ttu-id="30efe-107">La **colección UsersInRole** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="30efe-107">The **UsersInRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="30efe-108">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="30efe-108">Related Collections</span></span>

<span data-ttu-id="30efe-109">Puede navegar desde esta colección a cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="30efe-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="30efe-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="30efe-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="30efe-111">**Propertyinfo**</span><span class="sxs-lookup"><span data-stu-id="30efe-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="30efe-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="30efe-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="30efe-113">Puede navegar a esta colección desde las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="30efe-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="30efe-114">**Roles**</span><span class="sxs-lookup"><span data-stu-id="30efe-114">**Roles**</span></span>](roles.md)

## <a name="properties"></a><span data-ttu-id="30efe-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="30efe-115">Properties</span></span>

<span data-ttu-id="30efe-116">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades dentro de la colección:</span><span class="sxs-lookup"><span data-stu-id="30efe-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="30efe-117">User</span><span class="sxs-lookup"><span data-stu-id="30efe-117">User</span></span>](#usersinrole-collection)

### <a name="user"></a><span data-ttu-id="30efe-118">Usuario</span><span class="sxs-lookup"><span data-stu-id="30efe-118">User</span></span>



| <span data-ttu-id="30efe-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="30efe-119">Entry</span></span> | <span data-ttu-id="30efe-120">Valor</span><span class="sxs-lookup"><span data-stu-id="30efe-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30efe-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="30efe-121">Description</span></span>    | <span data-ttu-id="30efe-122">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="30efe-122">The user name.</span></span> <span data-ttu-id="30efe-123">Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="30efe-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="30efe-124">Access</span><span class="sxs-lookup"><span data-stu-id="30efe-124">Access</span></span>         | <span data-ttu-id="30efe-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="30efe-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="30efe-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="30efe-126">Type</span></span>           | <span data-ttu-id="30efe-127">String</span><span class="sxs-lookup"><span data-stu-id="30efe-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="30efe-128">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="30efe-128">Default</span></span>        | <span data-ttu-id="30efe-129">"Nuevo usuario"</span><span class="sxs-lookup"><span data-stu-id="30efe-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="30efe-130">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="30efe-130">Minimum system</span></span> | <span data-ttu-id="30efe-131">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="30efe-131">Windows 2000</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="30efe-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="30efe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30efe-133">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="30efe-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
