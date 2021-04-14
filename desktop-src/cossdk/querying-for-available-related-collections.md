---
description: Consultar colecciones relacionadas disponibles
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: Consultar colecciones relacionadas disponibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360063"
---
# <a name="querying-for-available-related-collections"></a><span data-ttu-id="736e6-103">Consultar colecciones relacionadas disponibles</span><span class="sxs-lookup"><span data-stu-id="736e6-103">Querying for Available Related Collections</span></span>

<span data-ttu-id="736e6-104">Si está escribiendo una herramienta de administración de uso general, es probable que deba escribir rutinas para navegar por toda la jerarquía de colecciones.</span><span class="sxs-lookup"><span data-stu-id="736e6-104">If you are writing a general-purpose administration tool, it is likely that you will need to write routines for navigating the entire collection hierarchy.</span></span> <span data-ttu-id="736e6-105">Para admitir esto, COM+ tiene una instalación que le permite consultar de forma dinámica las colecciones relacionadas que están disponibles en cualquier colección determinada.</span><span class="sxs-lookup"><span data-stu-id="736e6-105">To support this, COM+ has a facility that enables you to dynamically query for the related collections that are available from any given collection.</span></span>

<span data-ttu-id="736e6-106">La colección [**RelatedCollectionInfo**](relatedcollectioninfo.md) está disponible en cualquier colección que pueda contener y contiene un elemento para cada colección relacionada disponible.</span><span class="sxs-lookup"><span data-stu-id="736e6-106">The [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection is available from any collection that you might be holding and contains an item for each available related collection.</span></span> <span data-ttu-id="736e6-107">Puede enumerar estos elementos para determinar si una colección determinada está disponible.</span><span class="sxs-lookup"><span data-stu-id="736e6-107">You can enumerate through these items to determine whether a given collection is available.</span></span>

<span data-ttu-id="736e6-108">Puede obtener la colección [**RelatedCollectionInfo**](relatedcollectioninfo.md) de cualquier colección que esté conservando mediante el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en el objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , y dejar en blanco el segundo parámetro, donde normalmente especificaría la propiedad clave de un elemento primario.</span><span class="sxs-lookup"><span data-stu-id="736e6-108">You can get the [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="736e6-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="736e6-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="736e6-110">Navegar por la jerarquía de la colección de COM+</span><span class="sxs-lookup"><span data-stu-id="736e6-110">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="736e6-111">Rellenar colecciones de COM+</span><span class="sxs-lookup"><span data-stu-id="736e6-111">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="736e6-112">Recuperar recopilaciones en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="736e6-112">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



