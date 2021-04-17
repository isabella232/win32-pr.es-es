---
description: Rellenar colecciones de COM+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Rellenar colecciones de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d85521eb7e3750d06920a570ddeaf4d7e9b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360049"
---
# <a name="populating-com-collections"></a><span data-ttu-id="fb9ea-103">Rellenar colecciones de COM+</span><span class="sxs-lookup"><span data-stu-id="fb9ea-103">Populating COM+ Collections</span></span>

<span data-ttu-id="fb9ea-104">Una vez que haya recuperado una colección y antes de poder trabajar directamente con los elementos que contiene, debe rellenar la colección mediante el método [**rellenar**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) .</span><span class="sxs-lookup"><span data-stu-id="fb9ea-104">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection by using the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method.</span></span> <span data-ttu-id="fb9ea-105">Obtiene datos para el contenido de la colección desde el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-105">This fetches data for the collection's contents from the COM+ catalog.</span></span>

<span data-ttu-id="fb9ea-106">Es importante comprender que cada vez que se usan los objetos COMAdmin para manipular elementos o datos en colecciones, está trabajando realmente en datos almacenados en caché de forma transitoria; no está trabajando directamente con el catálogo guardado.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-106">It is important to understand that whenever you use the COMAdmin objects to manipulate items or data in collections, you are really working on transiently cached data; you are not working directly with the persisted catalog.</span></span> <span data-ttu-id="fb9ea-107">Nada que haga con una colección o con cualquiera de sus elementos se refleja en el catálogo hasta que llame a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en la colección.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-107">Nothing that you do with a collection or any of its items is reflected on the catalog until you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the collection.</span></span> <span data-ttu-id="fb9ea-108">Para obtener más información, consulte [Guardar o descartar cambios](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="fb9ea-108">For more detail, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="fb9ea-109">Todas las llamadas subsiguientes que se [**rellenan**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), antes de llamar a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), tienen el efecto de descartar los cambios pendientes en todos los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-109">Any subsequent calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), prior to calling [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), has the effect of discarding pending changes to all items in the collection.</span></span> <span data-ttu-id="fb9ea-110">**Rellenar** siempre rellena la caché en la que se está trabajando con los datos que se conservan en el almacén de datos del catálogo subyacente.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-110">**Populate** always populates the cache you're working in with whatever data is persisted on the underlying catalog data store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb9ea-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb9ea-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb9ea-112">Navegar por la jerarquía de la colección de COM+</span><span class="sxs-lookup"><span data-stu-id="fb9ea-112">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="fb9ea-113">Consultar colecciones relacionadas disponibles</span><span class="sxs-lookup"><span data-stu-id="fb9ea-113">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="fb9ea-114">Recuperar recopilaciones en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="fb9ea-114">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



