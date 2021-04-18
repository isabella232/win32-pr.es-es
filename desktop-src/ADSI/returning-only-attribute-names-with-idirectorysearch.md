---
title: Devolver solo nombres de atributo con IDirectorySearch
description: Puede realizar una búsqueda para determinar qué tipo de datos están disponibles para un objeto determinado.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Devolver solo nombres de atributo con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch y otras opciones de búsqueda, devolviendo únicamente nombres de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656153"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a><span data-ttu-id="0d85e-105">Devolver solo nombres de atributo con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="0d85e-105">Returning Only Attribute Names with IDirectorySearch</span></span>

<span data-ttu-id="0d85e-106">Puede realizar una búsqueda para determinar qué tipo de datos están disponibles para un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="0d85e-106">You can perform a search to determine what type of data is available for a particular object.</span></span> <span data-ttu-id="0d85e-107">En este caso, solo está interesado en los nombres de los atributos, no en los valores de atributo del objeto.</span><span class="sxs-lookup"><span data-stu-id="0d85e-107">In this case, you are only interested in the attributes names, not the attribute values of the object.</span></span> <span data-ttu-id="0d85e-108">La opción **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ solo** hace que el servidor devuelva solo los nombres de atributo y no los valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="0d85e-108">The **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option causes the server to only return the attribute names and not the attribute values.</span></span> <span data-ttu-id="0d85e-109">Sin embargo, el conjunto de resultados incluye solo los atributos que tienen valores asignados.</span><span class="sxs-lookup"><span data-stu-id="0d85e-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="0d85e-110">Por ejemplo, considere un objeto con los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="0d85e-110">For example, consider an object with the following attributes:</span></span>

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

<span data-ttu-id="0d85e-111">Cuando se establece la opción **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ Only** , el conjunto de resultados incluye:</span><span class="sxs-lookup"><span data-stu-id="0d85e-111">When the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option is set, the result set includes:</span></span>

``` syntax
name
sn
department
phone
```

<span data-ttu-id="0d85e-112">El valor predeterminado es para que se devuelvan los nombres y los valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="0d85e-112">The default is for both attribute values and names to be returned.</span></span>

<span data-ttu-id="0d85e-113">Para recuperar solo los nombres de atributo, establezca una opción de búsqueda **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ Only** con un valor **\_ booleano ADSTYPE** de **true** en la matriz [**ADS \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) que se pasa al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="0d85e-113">To retrieve only attribute names, set an **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="0d85e-114">En el ejemplo de código siguiente se muestra cómo recuperar solo los nombres de atributo.</span><span class="sxs-lookup"><span data-stu-id="0d85e-114">The following code example shows how to retrieve attribute names only.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



<span data-ttu-id="0d85e-115">Para obtener más información y un ejemplo de código que muestra cómo usar la opción de búsqueda **\_ \_ \_ solo ATTRIBTYPES de ADS SEARCHPREF** , consulte el [código de ejemplo para buscar atributos](example-code-for-searching-for-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0d85e-115">For more information and a code example that shows how to use the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option, see [Example Code for Searching for Attributes](example-code-for-searching-for-attributes.md).</span></span>

 

 




