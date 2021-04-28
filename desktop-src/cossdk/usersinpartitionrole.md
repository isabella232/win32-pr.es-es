---
description: 'Colección UsersInPartitionRole: contiene un objeto para cada usuario del rol con el que está relacionada la colección.'
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: Colección UsersInPartitionRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a4c134ebead08ef576337528a8ef75d8b8be21a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105553"
---
# <a name="usersinpartitionrole-collection"></a><span data-ttu-id="06cc5-103">Colección UsersInPartitionRole</span><span class="sxs-lookup"><span data-stu-id="06cc5-103">UsersInPartitionRole collection</span></span>

<span data-ttu-id="06cc5-104">Contiene un objeto para cada usuario del rol con el que está relacionada la colección.</span><span class="sxs-lookup"><span data-stu-id="06cc5-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="06cc5-105">Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)</span><span class="sxs-lookup"><span data-stu-id="06cc5-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="06cc5-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="06cc5-106">Members</span></span>

<span data-ttu-id="06cc5-107">La **colección UsersInPartitionRole** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="06cc5-107">The **UsersInPartitionRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="06cc5-108">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="06cc5-108">Related Collections</span></span>

<span data-ttu-id="06cc5-109">Puede navegar desde esta colección a cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="06cc5-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="06cc5-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="06cc5-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="06cc5-111">**Propertyinfo**</span><span class="sxs-lookup"><span data-stu-id="06cc5-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="06cc5-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="06cc5-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="06cc5-113">Puede navegar a esta colección desde las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="06cc5-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="06cc5-114">**RolesForPartition**</span><span class="sxs-lookup"><span data-stu-id="06cc5-114">**RolesForPartition**</span></span>](rolesforpartition.md)

## <a name="properties"></a><span data-ttu-id="06cc5-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="06cc5-115">Properties</span></span>

<span data-ttu-id="06cc5-116">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades dentro de la colección:</span><span class="sxs-lookup"><span data-stu-id="06cc5-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="06cc5-117">User</span><span class="sxs-lookup"><span data-stu-id="06cc5-117">User</span></span>](#usersinpartitionrole-collection)

### <a name="user"></a><span data-ttu-id="06cc5-118">Usuario</span><span class="sxs-lookup"><span data-stu-id="06cc5-118">User</span></span>



| <span data-ttu-id="06cc5-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="06cc5-119">Entry</span></span> | <span data-ttu-id="06cc5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="06cc5-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06cc5-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="06cc5-121">Description</span></span>    | <span data-ttu-id="06cc5-122">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="06cc5-122">The user name.</span></span> <span data-ttu-id="06cc5-123">Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="06cc5-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="06cc5-124">Access</span><span class="sxs-lookup"><span data-stu-id="06cc5-124">Access</span></span>         | <span data-ttu-id="06cc5-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="06cc5-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="06cc5-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="06cc5-126">Type</span></span>           | <span data-ttu-id="06cc5-127">String</span><span class="sxs-lookup"><span data-stu-id="06cc5-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="06cc5-128">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="06cc5-128">Default</span></span>        | <span data-ttu-id="06cc5-129">"Nuevo usuario"</span><span class="sxs-lookup"><span data-stu-id="06cc5-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="06cc5-130">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="06cc5-130">Minimum system</span></span> | <span data-ttu-id="06cc5-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="06cc5-131">Windows Server 2003</span></span>                                                                                                                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="06cc5-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="06cc5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06cc5-133">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="06cc5-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
