---
title: Límite de tamaño con IDirectorySearch
description: El cliente puede centrarse en un pequeño número de objetos devueltos desde el servidor y omitir el resto del conjunto de resultados.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Límite de tamaño con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, límite de tamaño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25127ea945edcf669e71d7d5b3f969d9eb2cb112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656148"
---
# <a name="size-limit-with-idirectorysearch"></a><span data-ttu-id="fe0a8-105">Límite de tamaño con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="fe0a8-105">Size Limit with IDirectorySearch</span></span>

<span data-ttu-id="fe0a8-106">Para reducir los requisitos de memoria o para otros propósitos, el cliente puede centrarse en un pequeño número de objetos devueltos desde el servidor y omitir el resto del conjunto de resultados que no son de interés.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-106">To reduce the memory requirement or for other purposes, the client can focus on a small number of objects returned from the server and ignore the rest of the result set that are not of interest.</span></span> <span data-ttu-id="fe0a8-107">Para ello, el cliente especifica el límite de tamaño de búsqueda y otros criterios de búsqueda adecuados.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-107">To accomplish this, the client specifies the search size limit and other appropriate search criteria.</span></span> <span data-ttu-id="fe0a8-108">Por ejemplo, si el directorio almacena las puntuaciones de pruebas de un distrito escolar, puede consultar los diez estudiantes principales con las puntuaciones de prueba más altas especificando un límite de tamaño de diez (10) y un criterio de ordenación descendente.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-108">For example, if the directory stores the test scores of a school district, you can query the top ten students with the highest test scores by specifying a size limit of ten (10) and a descending sort order.</span></span>

<span data-ttu-id="fe0a8-109">El valor predeterminado para el límite de tamaño es sin límite.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-109">The default for size limit is no limit.</span></span> <span data-ttu-id="fe0a8-110">Para establecer un límite de tamaño, establezca una opción de búsqueda de límite de tamaño de SEARCHPREF de ADS con un valor **\_ entero de ADSTYPE** que contenga el tamaño máximo de la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fe0a8-110">To set a size limit, set an **ADS\_SEARCHPREF\_SIZE\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the maximum size in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="fe0a8-111">En el ejemplo de código siguiente se muestra cómo establecer el límite de tamaño.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-111">The following code example shows how to set the size limit.</span></span> <span data-ttu-id="fe0a8-112">Un valor de límite de tamaño de cero indica que no hay límite de tamaño.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-112">A size limit value of zero indicates no size limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="fe0a8-113">Por Active Directory, el límite de tamaño especifica el número máximo de objetos que se devolverán en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-113">For Active Directory, the size limit specifies the maximum number of objects to be returned by the search.</span></span> <span data-ttu-id="fe0a8-114">Además, para Active Directory, el número máximo de objetos devueltos por una búsqueda es 1000 objetos.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-114">Also for Active Directory, the maximum number of objects returned by a search is 1000 objects.</span></span>

 

 




