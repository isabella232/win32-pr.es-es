---
description: Recuperar recopilaciones en el catálogo de COM+
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Recuperar recopilaciones en el catálogo de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807172"
---
# <a name="retrieving-collections-on-the-com-catalog"></a><span data-ttu-id="7a2fc-103">Recuperar recopilaciones en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="7a2fc-103">Retrieving Collections on the COM+ Catalog</span></span>

<span data-ttu-id="7a2fc-104">Los datos del catálogo de COM+ se almacenan en una jerarquía de colecciones.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-104">Data on the COM+ catalog is stored within a hierarchy of collections.</span></span> <span data-ttu-id="7a2fc-105">En la herramienta administrativa Servicios de componentes, muchas de estas colecciones aparecen como carpetas en el árbol de consola.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-105">In the Component Services administrative tool, many of these collections appear as folders in the console tree.</span></span> <span data-ttu-id="7a2fc-106">Solo se puede tener acceso a las colecciones que no aparecen como carpetas mediante programación.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-106">Collections that don't appear as folders can be accessed only programmatically.</span></span> <span data-ttu-id="7a2fc-107">Las colecciones sirven como contenedores para los elementos.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-107">Collections serve as containers for items.</span></span> <span data-ttu-id="7a2fc-108">Los elementos de una colección determinada son de un tipo coherente; es decir, todos representan el mismo tipo de elemento y puede haber un número arbitrario de elementos en una colección.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-108">The items in a given collection are all of a consistent type; that is, they all represent the same kind of element, and there can be an arbitrary number of items in a collection.</span></span> <span data-ttu-id="7a2fc-109">Por ejemplo, la colección de [**aplicaciones**](applications.md) contiene un elemento para cada aplicación com+ instalada en la máquina.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-109">For example, the [**Applications**](applications.md) collection contains an item for each COM+ application that is installed on the machine.</span></span> <span data-ttu-id="7a2fc-110">Esta colección aparece en la herramienta administrativa como la carpeta **aplicaciones com+** .</span><span class="sxs-lookup"><span data-stu-id="7a2fc-110">This collection appears in the administrative tool as the **COM+ Applications** folder.</span></span>

<span data-ttu-id="7a2fc-111">Las colecciones se producen en una estructura jerárquica porque los elementos que contienen siguen un orden INNATE de inclusión.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-111">The collections occur in a hierarchical structure because the elements they contain follow an innate order of inclusion.</span></span> <span data-ttu-id="7a2fc-112">Por ejemplo, dado que los componentes se instalan en una aplicación COM+, la colección de [**componentes**](components.md) se encuentra lógicamente en la colección de [**aplicaciones**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="7a2fc-112">For example, because components are installed into a COM+ application, the [**Components**](components.md) collection is logically subsumed under the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="7a2fc-113">En particular, para contener los componentes instalados en esa aplicación concreta, existe una colección de **componentes** distintos para cada elemento de la colección de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="7a2fc-113">More particularly, to hold the components installed into that particular application, there is a distinct **Components** collection for each item in the **Applications** collection.</span></span>

<span data-ttu-id="7a2fc-114">Debe obtener una colección en el catálogo siempre que desee recuperar un elemento y establecer sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-114">You must get a collection on the catalog whenever you want to retrieve an item and set properties on it.</span></span> <span data-ttu-id="7a2fc-115">En el caso general, debe recorrer varias colecciones para llegar al elemento que desee.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-115">In the general case, you need to step through several collections to get to the element you want.</span></span> <span data-ttu-id="7a2fc-116">Para ver el procedimiento para hacerlo, consulte [navegación por la jerarquía de la colección de com+](navigating-the-com--collection-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="7a2fc-116">For the procedure for doing this, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="7a2fc-117">Una vez que haya recuperado una colección y antes de poder trabajar directamente con los elementos que contiene, debe rellenar la colección, que captura los datos para el contenido de la colección desde el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-117">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection, which fetches data for the collection's contents from the COM+ catalog.</span></span> <span data-ttu-id="7a2fc-118">Para obtener más información, vea [rellenar colecciones de com+](populating-com--collections.md).</span><span class="sxs-lookup"><span data-stu-id="7a2fc-118">For details, see [Populating COM+ Collections](populating-com--collections.md).</span></span>

<span data-ttu-id="7a2fc-119">Además, existe una utilidad que permite realizar consultas de forma dinámica para ver qué colecciones relacionadas están disponibles en una colección determinada que se está conteniendo.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-119">Additionally, there is a facility you can use that enables you to dynamically query to see what related collections are available from a given collection you are holding.</span></span> <span data-ttu-id="7a2fc-120">Para obtener más información, consulte [consultar las colecciones relacionadas disponibles](querying-for-available-related-collections.md).</span><span class="sxs-lookup"><span data-stu-id="7a2fc-120">For details, see [Querying for Available Related Collections](querying-for-available-related-collections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a2fc-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a2fc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a2fc-122">Operaciones de administración de COM+ en transacciones</span><span class="sxs-lookup"><span data-stu-id="7a2fc-122">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="7a2fc-123">Control de errores de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="7a2fc-123">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="7a2fc-124">Ejemplo introductorio con el catálogo de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="7a2fc-124">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="7a2fc-125">Información general de los objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="7a2fc-125">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="7a2fc-126">Establecer propiedades y guardar cambios en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="7a2fc-126">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



