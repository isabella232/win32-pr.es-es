---
title: Usar el método SetSearchPreference
description: La llamada al método IDirectorySearch SetSearchPreference cambia la manera en que se obtienen los resultados de la búsqueda y se presentan a través de la interfaz IDirectorySearch.
ms.assetid: 37583276-8372-4478-82aa-3e456cc0f8f1
ms.tgt_platform: multiple
keywords:
- SetSearchPreference ADSI, usar el método SetSearchPreference
- ADSI ADSI, código de ejemplo C/C++, usar el método SetSearchPreference
- consulta ADSI mediante SetSearchPreference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c357fd331ae8589bffdd3ff7a834a7bc9e0430
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075052"
---
# <a name="using-the-setsearchpreference-method"></a><span data-ttu-id="41d12-106">Usar el método SetSearchPreference</span><span class="sxs-lookup"><span data-stu-id="41d12-106">Using the SetSearchPreference Method</span></span>

<span data-ttu-id="41d12-107">La llamada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) cambia la manera en que se obtienen los resultados de la búsqueda y se presentan a través de la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="41d12-107">Calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method changes the way in which the search results are obtained and presented through the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="41d12-108">La documentación del SDK define [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="41d12-108">The SDK documentation defines [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) as follows:</span></span>


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



<span data-ttu-id="41d12-109">Se pueden establecer varias preferencias si se pasa una matriz como primer parámetro y el tamaño de la matriz como el segundo parámetro.</span><span class="sxs-lookup"><span data-stu-id="41d12-109">Multiple preferences may be set by passing an array as the first parameter and the array size as the second parameter.</span></span>


```C++
ADS_SEARCHPREF_INFO arSearchPrefs[2];
 
arSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_PAGESIZE; 
arSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
arSearchPrefs[0].vValue.Integer = 100;
 
arSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE; 
arSearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER; 
arSearchPrefs[1].vValue.Integer = ADS_SCOPE_SUBTREE; 
 
hr = pDSearch->SetSearchPreference(&arSearchPrefs, 2);
```



<span data-ttu-id="41d12-110">En este ejemplo se establece el tamaño de página en 100 filas y el ámbito en el \_ tipo de subárbol del ámbito de ADS \_ .</span><span class="sxs-lookup"><span data-stu-id="41d12-110">This example sets the page size to 100 rows and the scope to the ADS\_SCOPE\_SUBTREE type.</span></span> <span data-ttu-id="41d12-111">La configuración de tamaño de página hace que el servidor devuelva datos inmediatamente al cliente, después de que se hayan calculado 100 filas.</span><span class="sxs-lookup"><span data-stu-id="41d12-111">The page size setting causes the server to immediately return data to the client, after 100 rows have been calculated.</span></span> <span data-ttu-id="41d12-112">La \_ configuración del \_ subárbol del ámbito de ADS hace que la búsqueda abarque todas las ramas del árbol debajo del punto en el que se ejecuta la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="41d12-112">The ADS\_SCOPE\_SUBTREE setting causes the search to encompass all branches in the tree below the point from which the search is being executed.</span></span>

 

 




