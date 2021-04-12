---
title: Almacenamiento en caché de resultados con IDirectorySearch
description: La \_ \_ preferencia resultados de la caché de SEARCHPREF ADS \_ almacena en caché el conjunto de resultados en el cliente.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Almacenamiento en caché de resultados con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, almacenamiento en caché de resultados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95016699eb4de36344b7e40f35e1a4a9cce761b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356696"
---
# <a name="result-caching-with-idirectorysearch"></a><span data-ttu-id="3b1ad-105">Almacenamiento en caché de resultados con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="3b1ad-105">Result Caching with IDirectorySearch</span></span>

<span data-ttu-id="3b1ad-106">La preferencia resultados de la **\_ caché de SEARCHPREF \_ \_ ADS** almacena en caché el conjunto de resultados en el cliente.</span><span class="sxs-lookup"><span data-stu-id="3b1ad-106">The **ADS\_SEARCHPREF\_CACHE\_RESULTS** preference caches the result set on the client.</span></span> <span data-ttu-id="3b1ad-107">El almacenamiento en caché de resultados permite que una aplicación retenga un conjunto de resultados recuperado y vuelva a pasar por las filas recuperadas.</span><span class="sxs-lookup"><span data-stu-id="3b1ad-107">Result caching enables an application to retain a retrieved result set and go through the retrieved rows again.</span></span> <span data-ttu-id="3b1ad-108">También habilita la compatibilidad con cursores en la que se pueden usar los métodos [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) y [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) para moverse hacia arriba y hacia abajo por el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="3b1ad-108">It also enables cursor support where the [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) and [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) methods can be used to move up and down the result set.</span></span>

<span data-ttu-id="3b1ad-109">De forma predeterminada, el almacenamiento en caché de resultados está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="3b1ad-109">By default, result caching is disabled.</span></span> <span data-ttu-id="3b1ad-110">El almacenamiento en caché de resultados debe estar habilitado si se cumple alguna de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="3b1ad-110">Result caching should be enabled if any one of the following is true:</span></span>

-   <span data-ttu-id="3b1ad-111">Si el mismo conjunto de resultados se debe enumerar varias veces sin realizar la búsqueda de nuevo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3b1ad-111">If the same result set must be enumerated multiple times without performing the search again on the server.</span></span>
-   <span data-ttu-id="3b1ad-112">Si realiza la búsqueda con un uso intensivo de recursos en el servidor (conexión lenta, conjunto de resultados grande o consulta compleja).</span><span class="sxs-lookup"><span data-stu-id="3b1ad-112">If performing the search is resource-intensive on the server (slow connection, large result set, or complex query).</span></span>
-   <span data-ttu-id="3b1ad-113">Si se requiere compatibilidad con cursores.</span><span class="sxs-lookup"><span data-stu-id="3b1ad-113">If cursor support is required.</span></span>

<span data-ttu-id="3b1ad-114">Desactive el almacenamiento en caché si la aplicación debe reducir los requisitos de memoria para almacenar en caché un conjunto de resultados grande en el cliente.</span><span class="sxs-lookup"><span data-stu-id="3b1ad-114">Turn off caching if your application must reduce memory requirements for caching a large result set at the client.</span></span>

<span data-ttu-id="3b1ad-115">El almacenamiento en caché de resultados aumenta los requisitos de memoria en el cliente, por lo que se debe deshabilitar el almacenamiento en caché de resultados si esto supone un problema.</span><span class="sxs-lookup"><span data-stu-id="3b1ad-115">Result caching increases the memory requirements on the client, so result caching should be disabled if this is a concern.</span></span>

<span data-ttu-id="3b1ad-116">Para habilitar el almacenamiento en caché de resultados, establezca una opción de búsqueda de **\_ \_ \_ resultados de caché ADS SEARCHPREF** con un valor **\_ booleano ADSTYPE** de **true** en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="3b1ad-116">To enable result caching, set an **ADS\_SEARCHPREF\_CACHE\_RESULTS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="3b1ad-117">En el ejemplo de código siguiente se muestra cómo habilitar el almacenamiento en caché de resultados.</span><span class="sxs-lookup"><span data-stu-id="3b1ad-117">The following code example shows how to enable result caching.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




