---
title: Ordenar los resultados de la búsqueda con IDirectorySearch
description: De forma predeterminada, los resultados de una búsqueda se devuelven sin ningún orden garantizado. La \_ \_ \_ preferencia ordenar por SEARCHPREF de ADS indica al servidor que ordene el conjunto de resultados en un valor de atributo especificado antes de que se devuelva al cliente.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Ordenar los resultados de la búsqueda con IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, ordenar los resultados de la búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433d24b06ac4d361d6520d8af3376ea12acac1f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793828"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a><span data-ttu-id="f6de9-106">Ordenar los resultados de la búsqueda con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f6de9-106">Sorting the Search Results with IDirectorySearch</span></span>

<span data-ttu-id="f6de9-107">De forma predeterminada, los resultados de una búsqueda se devuelven sin ningún orden garantizado.</span><span class="sxs-lookup"><span data-stu-id="f6de9-107">By default, the results of a search are returned in no guaranteed order.</span></span> <span data-ttu-id="f6de9-108">La **preferencia \_ \_ ordenar \_ por SEARCHPREF de ADS** indica al servidor que ordene el conjunto de resultados en un valor de atributo especificado antes de que se devuelva al cliente.</span><span class="sxs-lookup"><span data-stu-id="f6de9-108">The **ADS\_SEARCHPREF\_SORT\_ON** preference instructs the server to sort the result set on a specified attribute value before it is returned to the client.</span></span>

<span data-ttu-id="f6de9-109">Se recomienda utilizar atributos indexados para la ordenación.</span><span class="sxs-lookup"><span data-stu-id="f6de9-109">It is recommended that indexed attributes be used for sorting.</span></span> <span data-ttu-id="f6de9-110">De lo contrario, el servidor debe recuperar el conjunto de resultados completo y ordenarlo antes de enviar los resultados al cliente.</span><span class="sxs-lookup"><span data-stu-id="f6de9-110">Otherwise, the server must retrieve the complete result set and sort it before sending any results to the client.</span></span> <span data-ttu-id="f6de9-111">Esto también se aplica a las búsquedas paginadas.</span><span class="sxs-lookup"><span data-stu-id="f6de9-111">This also applies to paged searches.</span></span> <span data-ttu-id="f6de9-112">Tenga en cuenta que se aumentará el rendimiento de una búsqueda ordenada si el filtro incluye un atributo indexado y ese atributo se especifica como criterio de ordenación; en este caso, Active Directory puede satisfacer la ordenación mientras se procesa el filtro.</span><span class="sxs-lookup"><span data-stu-id="f6de9-112">Be aware that performance of a sorted search will be increased if the filter includes an indexed attribute and that attribute is specified as the sort key; in this case, Active Directory can satisfy the sort while processing the filter.</span></span> <span data-ttu-id="f6de9-113">Por ejemplo, una consulta de ordenación eficaz para un conjunto de usuarios podría tener un filtro incluido (SN>Smith) y un criterio de ordenación de SN.</span><span class="sxs-lookup"><span data-stu-id="f6de9-113">For example, an efficient sort query for a set of users could have a filter that included (sn>smith) and a sort key of sn.</span></span>

<span data-ttu-id="f6de9-114">La ordenación del lado servidor con la opción de búsqueda **\_ \_ ordenar \_ por SEARCHPREF de ADS** reducirá el rendimiento del servidor.</span><span class="sxs-lookup"><span data-stu-id="f6de9-114">Server-side sorting with the **ADS\_SEARCHPREF\_SORT\_ON** search option will reduce the performance of the server.</span></span> <span data-ttu-id="f6de9-115">Si va a realizar muchas búsquedas, considere la posibilidad de ordenar los resultados manualmente en el lado del cliente para reducir la carga de trabajo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="f6de9-115">If you will be performing many searches, consider sorting the results manually on the client side to reduce the workload on the server.</span></span>

<span data-ttu-id="f6de9-116">De forma predeterminada, la ordenación de los resultados está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="f6de9-116">By default, result sorting is disabled.</span></span> <span data-ttu-id="f6de9-117">Para habilitar la ordenación de resultados, establezca una opción **ADS \_ SEARCHPREF \_ Sort \_ on** Search con un valor **\_ \_ específico de ADSTYPE Prov** que señale a una estructura [**\_ SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) de ADS en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="f6de9-117">To enable result sorting, set an **ADS\_SEARCHPREF\_SORT\_ON** search option with an **ADSTYPE\_PROV\_SPECIFIC** that points to an [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="f6de9-118">La **estructura \_ SORTKEY de ADS** se usa para especificar el atributo por el que se va a ordenar y el orden de la ordenación.</span><span class="sxs-lookup"><span data-stu-id="f6de9-118">The **ADS\_SORTKEY** structure is used to specify the attribute to sort on and the order of the sort.</span></span>

<span data-ttu-id="f6de9-119">En el ejemplo de código siguiente se muestra cómo habilitar la ordenación de resultados.</span><span class="sxs-lookup"><span data-stu-id="f6de9-119">The following code example shows how to enable result sorting.</span></span>


```C++
ADS_SORTKEY SortKey;
SortKey.pszAttrType = L"cn";
SortKey.pszReserved = NULL;
SortKey.fReverseorder = FALSE;

ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SORT_ON;
SearchPref.vValue.dwType = ADSTYPE_PROV_SPECIFIC;
SearchPref.vValue.ProviderSpecific.dwLength = sizeof(SortKey);
SearchPref.vValue.ProviderSpecific.lpValue = (LPBYTE)&SortKey;
```



<span data-ttu-id="f6de9-120">Active Directory no admite la ordenación de atributos construidos, por lo que no es posible especificar un atributo construido para la ordenación.</span><span class="sxs-lookup"><span data-stu-id="f6de9-120">Active Directory does not support sorting on constructed attributes, so it is not possible to specify a constructed attribute for sorting.</span></span> <span data-ttu-id="f6de9-121">El atributo [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) tampoco se puede usar para ordenar.</span><span class="sxs-lookup"><span data-stu-id="f6de9-121">The [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) attribute also cannot be used for sorting.</span></span> <span data-ttu-id="f6de9-122">Active Directory tampoco permite la ordenación en más de un atributo, por lo que la opción **\_ \_ de ordenación \_ de la búsqueda de SEARCHPREF de anuncios** solo puede contener una estructura de tipo [**\_ SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) .</span><span class="sxs-lookup"><span data-stu-id="f6de9-122">Active Directory also does not allow sorting on more than one attribute, so the **ADS\_SEARCHPREF\_SORT\_ON** search option can only contain one [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure.</span></span>

 

 