---
title: Especificar otras opciones de búsqueda con IDirectorySearch
description: La interfaz IDirectorySearch proporciona control adicional sobre cómo se realiza la búsqueda mediante el uso de opciones de búsqueda.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Especificar otras opciones de búsqueda con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch y otras opciones de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7064a291c3a299a5435ec454a17b1a666f20d0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993838"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a><span data-ttu-id="b36c2-105">Especificar otras opciones de búsqueda con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b36c2-105">Specifying Other Search Options with IDirectorySearch</span></span>

<span data-ttu-id="b36c2-106">La interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) proporciona control adicional sobre cómo se realiza la búsqueda mediante el uso de opciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b36c2-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provide additional control over how the search is performed through the use of search options.</span></span> <span data-ttu-id="b36c2-107">Estas opciones de búsqueda se establecen al rellenar una matriz de estructuras de [**\_ \_ información SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) y llamar al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="b36c2-107">These search options are set by filling in an array of [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) structures and calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="b36c2-108">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="b36c2-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b36c2-109">Usar el método SetSearchPreference</span><span class="sxs-lookup"><span data-stu-id="b36c2-109">Using the SetSearchPreference Method</span></span>](using-the-setsearchpreference-method.md)
-   [<span data-ttu-id="b36c2-110">Búsquedas sincrónicas y asincrónicas con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b36c2-110">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="b36c2-111">Paginación con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b36c2-111">Paging with IDirectorySearch</span></span>](paging-with-idirectorysearch.md)
-   [<span data-ttu-id="b36c2-112">Almacenamiento en caché de resultados con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b36c2-112">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="b36c2-113">Realización de una consulta de ámbito de atributo</span><span class="sxs-lookup"><span data-stu-id="b36c2-113">Performing an Attribute Scope Query</span></span>](performing-an-attribute-scoped-query.md)
-   [<span data-ttu-id="b36c2-114">Ordenar los resultados de la búsqueda con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b36c2-114">Sorting the Search Results with IDirectorySearch</span></span>](sorting-the-search-results-with-idirectorysearch.md)
-   [<span data-ttu-id="b36c2-115">Referencia sobre el seguimiento con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b36c2-115">Referral Chasing with IDirectorySearch</span></span>](referral-chasing-with-idirectorysearch.md)
-   [<span data-ttu-id="b36c2-116">Límite de tamaño con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b36c2-116">Size Limit with IDirectorySearch</span></span>](size-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="b36c2-117">Límite de tiempo del servidor con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b36c2-117">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="b36c2-118">Límite de tiempo de cliente con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b36c2-118">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="b36c2-119">Devolver solo nombres de atributo con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b36c2-119">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)

 

 




