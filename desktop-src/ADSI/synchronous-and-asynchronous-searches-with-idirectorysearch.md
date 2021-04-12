---
title: Búsquedas sincrónicas y asincrónicas con IDirectorySearch
description: Cuando realiza una búsqueda mediante la interfaz IDirectorySearch, el método ExecuteSearch de IDirectorySearch no envía la solicitud de búsqueda al servidor.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Búsquedas sincrónicas y asincrónicas con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, búsquedas sincrónicas y asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f369d45aaf4453d310c4bac2259bfa9cd089f567
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418347"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a><span data-ttu-id="547cc-105">Búsquedas sincrónicas y asincrónicas con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="547cc-105">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>

<span data-ttu-id="547cc-106">Cuando realiza una búsqueda mediante la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , el método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) no envía la solicitud de búsqueda al servidor.</span><span class="sxs-lookup"><span data-stu-id="547cc-106">When you perform a search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method does not send the search request to the server.</span></span> <span data-ttu-id="547cc-107">Este método solo guarda los parámetros de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="547cc-107">This method only saves the search parameters.</span></span> <span data-ttu-id="547cc-108">La solicitud de búsqueda se envía realmente cuando se llama a [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).</span><span class="sxs-lookup"><span data-stu-id="547cc-108">The search request is actually sent when you call [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).</span></span>

<span data-ttu-id="547cc-109">En el caso de las búsquedas de Active Directory, la diferencia principal entre sincrónicos y asincrónicos es cuando se devuelve la primera fila del resultado, es decir, cuando la primera llamada a [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) devuelve.</span><span class="sxs-lookup"><span data-stu-id="547cc-109">For Active Directory searches, the primary difference between synchronous and asynchronous is when the first row of the result is returned, that is, when the first [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) call returns.</span></span>

<span data-ttu-id="547cc-110">En una búsqueda sincrónica, si la paginación no está habilitada, se devuelve la primera fila cuando el servidor ha construido y devuelto todo el conjunto de resultados al cliente.</span><span class="sxs-lookup"><span data-stu-id="547cc-110">In a synchronous search, if paging is not enabled, the first row is returned when the server has constructed and returned the entire result set to the client.</span></span> <span data-ttu-id="547cc-111">Si la paginación está habilitada, se devuelve la primera fila cuando se devuelve la primera página del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="547cc-111">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="547cc-112">En una búsqueda asincrónica, si la paginación no está habilitada, se devuelve la primera fila cuando el servidor ha construido la primera fila del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="547cc-112">In an asynchronous search, if paging is not enabled, the first row is returned when the server has constructed the first row of the result set.</span></span> <span data-ttu-id="547cc-113">Si la paginación está habilitada, se devuelve la primera fila cuando se devuelve la primera página del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="547cc-113">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="547cc-114">El tipo de búsqueda predeterminado es sincrónico.</span><span class="sxs-lookup"><span data-stu-id="547cc-114">The default search type is synchronous.</span></span> <span data-ttu-id="547cc-115">Para especificar una búsqueda asincrónica, establezca una opción de búsqueda **\_ \_ asincrónica de ADS SEARCHPREF** con un **valor \_ booleano ADSTYPE** de **true** en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="547cc-115">To specify an asynchronous search, set an **ADS\_SEARCHPREF\_ASYNCHRONOUS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="547cc-116">Esta operación se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="547cc-116">This operation is shown in the following code example.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




