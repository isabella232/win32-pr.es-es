---
description: Cada elemento de una colección expone propiedades.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Editar propiedades en el catálogo de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed2bade8886fe08bb7ed1ece179b35677569f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807357"
---
# <a name="editing-properties-in-the-com-catalog"></a><span data-ttu-id="f8bb6-103">Editar propiedades en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="f8bb6-103">Editing Properties in the COM+ Catalog</span></span>

<span data-ttu-id="f8bb6-104">Cada elemento de una colección expone propiedades.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-104">Each item in a collection exposes properties.</span></span> <span data-ttu-id="f8bb6-105">Estas propiedades sirven para almacenar los datos de configuración para cualquier elemento que represente el elemento.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-105">These properties serve to hold configuration data for whatever element the item represents.</span></span> <span data-ttu-id="f8bb6-106">En la herramienta administrativa Servicios de componentes, estas propiedades aparecen en una página de propiedades a la que se tiene acceso haciendo clic con el botón secundario en un elemento de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-106">In the Component Services administrative tool, these properties appear on a property page that you access by right-clicking an item in a folder.</span></span>

<span data-ttu-id="f8bb6-107">Dado que todos los elementos de una colección determinada representan el mismo tipo de elemento, esos elementos exponen un conjunto de propiedades que es coherente en toda la colección.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-107">Because the items in a given collection all represent the same kind of thing, those items expose a set of properties that is consistent across the collection.</span></span> <span data-ttu-id="f8bb6-108">Por ejemplo, la colección de [**aplicaciones**](applications.md) expone una propiedad Name, una propiedad AppID, etc.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-108">For example, the [**Applications**](applications.md) collection exposes a Name property, an AppID property, and so forth.</span></span> <span data-ttu-id="f8bb6-109">Esto es análogo a la forma en que cada aplicación de la herramienta administrativa Servicios de componentes tiene una página de propiedades estructurada coherente.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-109">This is analogous to how each application in the Component Services administrative tool has a consistently structured property page available for it.</span></span> <span data-ttu-id="f8bb6-110">Para obtener una lista de las propiedades disponibles para la colección de **aplicaciones** , vea **aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-110">For a list of properties available to the **Applications** collection, see **Applications**.</span></span> <span data-ttu-id="f8bb6-111">Para obtener una lista de las propiedades disponibles para la colección de [**componentes**](components.md) , vea **componentes**.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-111">For a list of properties available to the [**Components**](components.md) collection, see **Components**.</span></span>

<span data-ttu-id="f8bb6-112">Para obtener una lista completa de las propiedades expuestas por los elementos de cada colección, consulte [colecciones de administración de com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb6-112">For a complete list of properties exposed by items in each collection, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="f8bb6-113">Un elemento de una colección se representa mediante un objeto creado a partir de la clase [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="f8bb6-113">You represent an item in a collection by using an object created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="f8bb6-114">Este objeto le permite establecer y obtener cualquiera de las propiedades expuestas por el elemento.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-114">This object enables you to set and get any of the properties exposed by the item.</span></span> <span data-ttu-id="f8bb6-115">Al establecer las propiedades, también es posible que esté intentando usar otro escritor en el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-115">When setting properties, it is also possible that you might be contending with another writer to the COM+ catalog.</span></span> <span data-ttu-id="f8bb6-116">Para obtener más información, vea [obtener y establecer propiedades](getting-and-setting-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb6-116">For more information, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

<span data-ttu-id="f8bb6-117">Una vez que haya establecido las propiedades, no se confirmarán realmente los cambios hasta que guarde los cambios explícitamente.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-117">After you have set properties, no changes are actually committed until you explicitly save changes.</span></span> <span data-ttu-id="f8bb6-118">Para obtener más información, consulte [Guardar o descartar cambios](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb6-118">For more information, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="f8bb6-119">Cuando se guardan los cambios, el catálogo de COM+ exige cierta lógica de configuración para asegurarse de que no se establece nada en configuraciones incompatibles.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-119">When you save changes, the COM+ catalog enforces some configuration logic to ensure that you don't set things to incompatible configurations.</span></span> <span data-ttu-id="f8bb6-120">También cambia algunas propiedades cuando se cambian explícitamente ciertas otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-120">It also changes some properties for you when you explicitly change certain other properties.</span></span> <span data-ttu-id="f8bb6-121">Para obtener más información, vea [interdependencias entre propiedades](interdependencies-between-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb6-121">For more information, see [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="f8bb6-122">Además, COM+ tiene una utilidad que permite realizar consultas de forma dinámica para ver qué propiedades están disponibles para los elementos de una colección determinada.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-122">Additionally, COM+ has a facility that enables you to dynamically query to see what properties are available for the items in a given collection.</span></span> <span data-ttu-id="f8bb6-123">Para obtener más información, consulte [consultar las propiedades disponibles](querying-for-available-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb6-123">For details, see [Querying for Available Properties](querying-for-available-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8bb6-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8bb6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8bb6-125">Operaciones de administración de COM+ en transacciones</span><span class="sxs-lookup"><span data-stu-id="f8bb6-125">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="f8bb6-126">Control de errores de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="f8bb6-126">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="f8bb6-127">Ejemplo introductorio con el catálogo de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="f8bb6-127">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="f8bb6-128">Información general de los objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="f8bb6-128">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="f8bb6-129">Recuperar recopilaciones en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="f8bb6-129">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



