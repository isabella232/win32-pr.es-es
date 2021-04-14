---
description: Obtener y establecer propiedades
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Obtener y establecer propiedades (servicios de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151b08293cd32a35cd27bdba4dd3a37cdebfa4f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496337"
---
# <a name="getting-and-setting-properties-component-services"></a><span data-ttu-id="11181-103">Obtener y establecer propiedades (servicios de componentes)</span><span class="sxs-lookup"><span data-stu-id="11181-103">Getting and Setting Properties (Component Services)</span></span>

<span data-ttu-id="11181-104">Para poder leer o escribir propiedades concretas expuestas por un elemento de una colección, debe realizar los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="11181-104">Before you can read or write particular properties exposed by an item in a collection, you must take the following steps:</span></span>

1.  <span data-ttu-id="11181-105">Recupere la colección.</span><span class="sxs-lookup"><span data-stu-id="11181-105">Retrieve the collection.</span></span>
2.  <span data-ttu-id="11181-106">Rellene la colección para leer los datos del catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="11181-106">Populate the collection to read in data for it from the COM+ catalog.</span></span>
3.  <span data-ttu-id="11181-107">Recupere el elemento específico de la colección, que lo representa con un objeto de la clase [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="11181-107">Retrieve the specific item in the collection, representing it with an object from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="11181-108">Para obtener un ejemplo en el que se ilustran estos pasos, consulte [navegar por la jerarquía de la colección de com+](navigating-the-com--collection-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="11181-108">For an example that illustrates these steps, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="11181-109">Dado que las propiedades concretas expuestas pueden variar en función de lo que representa el elemento; es decir, un elemento que representa un componente tiene propiedades diferentes de las que representan una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="11181-109">Because the particular properties exposed can vary depending on what the item represents; that is, an item representing a component has different properties than one representing a COM+ application.</span></span> <span data-ttu-id="11181-110">Establezca cualquiera de estas propiedades mediante una única propiedad genérica, la propiedad Value, en [**COMAdminCatalogObject**](comadmincatalogobject.md).</span><span class="sxs-lookup"><span data-stu-id="11181-110">Set any of these properties using a single generic property, the Value property, on [**COMAdminCatalogObject**](comadmincatalogobject.md).</span></span>

<span data-ttu-id="11181-111">La propiedad Value permite obtener o establecer cualquier propiedad con nombre específica expuesta por un elemento, devolver un valor para una propiedad con nombre al obtener y tomar un nombre y un valor al establecer.</span><span class="sxs-lookup"><span data-stu-id="11181-111">The Value property enables you to get or set any specific named property exposed by an item, returning a value for a named property when getting, and taking a name and value when setting.</span></span>

<span data-ttu-id="11181-112">En realidad, no se registra ningún cambio en el catálogo de COM+ hasta que no se guardan explícitamente los cambios mediante el método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en el objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="11181-112">No changes are actually recorded to the COM+ catalog until you explicitly save changes using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="11181-113">Los cambios pendientes de todas las propiedades de todos los elementos de una colección determinada se guardan de una vez.</span><span class="sxs-lookup"><span data-stu-id="11181-113">Pending changes for all properties on all items in a given collection are saved all at once.</span></span> <span data-ttu-id="11181-114">Para obtener más información, consulte [Guardar o descartar cambios](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="11181-114">For details, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="11181-115">No se aceptarán todos los cambios que realice.</span><span class="sxs-lookup"><span data-stu-id="11181-115">Not all changes that you make will be accepted.</span></span> <span data-ttu-id="11181-116">El catálogo de COM+ exige cierta lógica de coherencia para asegurarse de que se configuran de forma razonable.</span><span class="sxs-lookup"><span data-stu-id="11181-116">The COM+ catalog enforces some coherency logic to ensure that you configure things in a reasonable way.</span></span> <span data-ttu-id="11181-117">Además, al cambiar algunas propiedades, otras podrían cambiar automáticamente por la misma lógica de coherencia.</span><span class="sxs-lookup"><span data-stu-id="11181-117">Additionally, when you change some properties, others might change automatically by the same coherency logic.</span></span> <span data-ttu-id="11181-118">Estos efectos aparecen al intentar guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="11181-118">These effects show up when you attempt to save changes.</span></span>

> [!Note]  
> <span data-ttu-id="11181-119">Es posible que tenga contención con otro escritor en el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="11181-119">It is possible for you to be in contention with another writer to the COM+ catalog.</span></span> <span data-ttu-id="11181-120">Entre las llamadas a [**rellenar**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) y [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para una colección determinada, no hay ningún bloqueo en ninguno de los datos del catálogo.</span><span class="sxs-lookup"><span data-stu-id="11181-120">Between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) for a given collection, you do not have a lock on any of that data in the catalog.</span></span> <span data-ttu-id="11181-121">Es posible que varias partes estén configurando los elementos de forma simultánea en una colección determinada y que puedan estar subiendo al guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="11181-121">Multiple parties may simultaneously be configuring items in a given collection and could be contending when they save changes.</span></span> <span data-ttu-id="11181-122">Esto significa que otra persona podría cambiar la configuración de un objeto antes o después de hacerlo, ya sea mediante la ejecución de algún tipo de programa con los objetos COMAdmin o mediante la herramienta administrativa Servicios de componentes, ya sea de forma local o remota.</span><span class="sxs-lookup"><span data-stu-id="11181-122">This means that someone else might change settings on an object before or after you do, either running some kind of program using the COMAdmin objects or using the Component Services administrative tool, either locally or remotely.</span></span> <span data-ttu-id="11181-123">La regla general con la escritura de objetos en el catálogo es que todas las propiedades de un objeto se escriben a la vez.</span><span class="sxs-lookup"><span data-stu-id="11181-123">The general rule with writing objects on the catalog is that all properties on an object are written at once.</span></span> <span data-ttu-id="11181-124">Es decir, el último escritor gana: el objeto se guarda en el catálogo exactamente como el último escritor lo configuró.</span><span class="sxs-lookup"><span data-stu-id="11181-124">That is, the last writer wins—the object is saved in the catalog precisely as the last writer configured it.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="11181-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11181-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11181-126">Interdependencias entre propiedades</span><span class="sxs-lookup"><span data-stu-id="11181-126">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="11181-127">Consultar las propiedades disponibles</span><span class="sxs-lookup"><span data-stu-id="11181-127">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="11181-128">Guardar o descartar cambios</span><span class="sxs-lookup"><span data-stu-id="11181-128">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



