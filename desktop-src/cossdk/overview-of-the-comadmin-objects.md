---
description: Los objetos COMAdmin ofrecen un modelo de objetos simple que proporciona acceso al catálogo de COM+.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Información general de los objetos COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22837cbe0548b623463234d1a03d17288eba2149
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153582"
---
# <a name="overview-of-the-comadmin-objects"></a><span data-ttu-id="45cd2-103">Información general de los objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="45cd2-103">Overview of the COMAdmin Objects</span></span>

<span data-ttu-id="45cd2-104">Los objetos COMAdmin ofrecen un modelo de objetos simple que proporciona acceso al catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="45cd2-104">The COMAdmin objects offer a simple object model that provides you with access to the COM+ catalog.</span></span> <span data-ttu-id="45cd2-105">Al hacerlo, sirven para modelar toda la funcionalidad proporcionada por la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="45cd2-105">In doing so, they serve to model all the functionality provided by the Component Services administrative tool.</span></span> <span data-ttu-id="45cd2-106">Siempre que realice cualquier tipo de administración de COM+, podrá interactuar con el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="45cd2-106">Whenever you do any kind of COM+ administration, you are interacting with the COM+ catalog.</span></span> <span data-ttu-id="45cd2-107">Para obtener una descripción del catálogo, vea [obtener acceso al catálogo de com+](accessing-the-com--catalog.md).</span><span class="sxs-lookup"><span data-stu-id="45cd2-107">For a description of the catalog, see [Accessing the COM+ Catalog](accessing-the-com--catalog.md).</span></span>

<span data-ttu-id="45cd2-108">La información que se obtiene de la herramienta administrativa Servicios de componentes o mediante el uso de los objetos COMAdmin está estructurada de forma similar, y las acciones que se realizan en ambos contexto son análogas.</span><span class="sxs-lookup"><span data-stu-id="45cd2-108">The information you obtain either from the Component Services administrative tool or by using the COMAdmin objects is structured similarly, and the actions you perform in either context are analogous.</span></span> <span data-ttu-id="45cd2-109">La correlación básica entre el uso del complemento Servicios de componentes y la administración mediante programación es que las carpetas del árbol de consola del complemento se corresponden con las recopilaciones del catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="45cd2-109">The basic correlation between using the Component Services snap-in and programmatic administration is that folders in the console tree of the snap-in correspond to collections in the COM+ catalog.</span></span> <span data-ttu-id="45cd2-110">Es decir, al igual que cada carpeta del complemento contiene elementos de todo tipo; por ejemplo, **las aplicaciones com+** retienen las aplicaciones com+ instaladas: cada colección del catálogo com+ contiene elementos de una clase uniforme.</span><span class="sxs-lookup"><span data-stu-id="45cd2-110">That is, just as each folder in the snap-in contains items all of a kind; for example, **COM+ Applications** holds installed COM+ applications—each collection in the COM+ catalog holds items of a uniform kind.</span></span> <span data-ttu-id="45cd2-111">Además, al igual que cada elemento de una carpeta tiene propiedades que se pueden establecer en una hoja de propiedades, cada elemento de una colección expone propiedades que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="45cd2-111">Further, just as each item in a folder has properties that you can set on a property sheet, each item in a collection exposes properties that you can set.</span></span>

<span data-ttu-id="45cd2-112">Para que pueda configurar objetos dentro de esta estructura, los objetos COMAdmin proporcionan los medios para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="45cd2-112">To enable you to configure objects within this structure, the COMAdmin objects provide you with the means to do the following:</span></span>

-   <span data-ttu-id="45cd2-113">Acceder al catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="45cd2-113">Access the COM+ catalog</span></span>
-   <span data-ttu-id="45cd2-114">Obtener acceso a las recopilaciones en el catálogo</span><span class="sxs-lookup"><span data-stu-id="45cd2-114">Access collections in the catalog</span></span>
-   <span data-ttu-id="45cd2-115">Obtener acceso a los elementos de las colecciones</span><span class="sxs-lookup"><span data-stu-id="45cd2-115">Access items in collections</span></span>
-   <span data-ttu-id="45cd2-116">Obtener acceso a las propiedades de los elementos de las colecciones</span><span class="sxs-lookup"><span data-stu-id="45cd2-116">Access properties on the items in the collections</span></span>

<span data-ttu-id="45cd2-117">Para admitir estas acciones, la biblioteca COMAdmin proporciona las tres clases siguientes:</span><span class="sxs-lookup"><span data-stu-id="45cd2-117">To support these actions, the COMAdmin Library provides the following three classes:</span></span>

-   <span data-ttu-id="45cd2-118">[**COMAdminCatalog**](comadmincatalog.md), que representa el catálogo en sí.</span><span class="sxs-lookup"><span data-stu-id="45cd2-118">[**COMAdminCatalog**](comadmincatalog.md), which represents the catalog itself.</span></span>
-   <span data-ttu-id="45cd2-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md), que representa cualquier colección.</span><span class="sxs-lookup"><span data-stu-id="45cd2-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md), which represents any collection.</span></span>
-   <span data-ttu-id="45cd2-120">[**COMAdminCatalogObject**](comadmincatalogobject.md), que representa cualquier elemento de una colección.</span><span class="sxs-lookup"><span data-stu-id="45cd2-120">[**COMAdminCatalogObject**](comadmincatalogobject.md), which represents any item in a collection.</span></span>

<span data-ttu-id="45cd2-121">Para obtener descripciones más detalladas de estas clases, vea [la Descripción resumida de las clases COMAdmin](summary-description-of-the-comadmin-classes.md) en esta sección.</span><span class="sxs-lookup"><span data-stu-id="45cd2-121">For fuller descriptions of these classes, see [Summary Description of the COMAdmin Classes](summary-description-of-the-comadmin-classes.md) in this section.</span></span>

<span data-ttu-id="45cd2-122">Para obtener una idea rápida de las acciones típicas que realiza en la administración mediante programación, consulte [el ejemplo de introducción al uso del catálogo de administración de com+](introductory-example-using-the-com--administration-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="45cd2-122">To get a quick idea of typical actions you perform in programmatic administration, see [Introductory Example Using the COM+ Administration Catalog](introductory-example-using-the-com--administration-catalog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="45cd2-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45cd2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45cd2-124">Operaciones de administración de COM+ en transacciones</span><span class="sxs-lookup"><span data-stu-id="45cd2-124">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="45cd2-125">Control de errores de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="45cd2-125">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="45cd2-126">Ejemplo introductorio con el catálogo de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="45cd2-126">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="45cd2-127">Recuperar recopilaciones en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="45cd2-127">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="45cd2-128">Establecer propiedades y guardar cambios en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="45cd2-128">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



