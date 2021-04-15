---
title: Usar IDirectorySearch y IDirectoryObject para la recuperación de intervalos
description: Las interfaces IDirectoryObject o IDirectorySearch se pueden usar para recuperar un intervalo de valores de propiedad. Para ello, especifique el atributo y el intervalo de uno de los atributos solicitados en la consulta.
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- IDirectorySearch ADSI, uso de para recuperar miembros de un grupo
- IDirectoryObject ADSI, uso de para recuperar miembros de un grupo
- ADSI de recuperación de intervalos con IDirectorySearch y IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591d2cf7b65b7a8159a92de324f18fbe93164f0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656137"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a><span data-ttu-id="b99bd-107">Usar IDirectorySearch y IDirectoryObject para la recuperación de intervalos</span><span class="sxs-lookup"><span data-stu-id="b99bd-107">Using IDirectorySearch and IDirectoryObject for Range Retrieval</span></span>

<span data-ttu-id="b99bd-108">Las interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) o [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) se pueden usar para recuperar un intervalo de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b99bd-108">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) or [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="b99bd-109">Para ello, especifique el atributo y el intervalo de uno de los atributos solicitados en la consulta.</span><span class="sxs-lookup"><span data-stu-id="b99bd-109">To do this, specify the attribute and range for one of the attributes requested in the query.</span></span>

## <a name="range-retrieval-with-idirectoryobject"></a><span data-ttu-id="b99bd-110">Recuperación de intervalos con IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="b99bd-110">Range Retrieval with IDirectoryObject</span></span>

<span data-ttu-id="b99bd-111">La interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) se puede utilizar para la recuperación de intervalos especificando el atributo y el intervalo de uno de los atributos de la matriz *pAttributesName* al llamar al método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="b99bd-111">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface can be used for range retrieval by specifying the attribute and range for one of the attributes in the *pAttributesName* array when calling the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



<span data-ttu-id="b99bd-112">Para obtener más información y un ejemplo de código que muestra cómo usar la interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para la recuperación de intervalos, vea el [código de ejemplo para el intervalo con IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="b99bd-112">For more information and a code example that shows how to use the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for range retrieval, see [Example Code for Ranging with IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).</span></span>

## <a name="range-retrieval-with-idirectorysearch"></a><span data-ttu-id="b99bd-113">Recuperación de intervalos con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b99bd-113">Range Retrieval with IDirectorySearch</span></span>

<span data-ttu-id="b99bd-114">La interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) se puede usar para la recuperación por rangos especificando el atributo y el intervalo de uno de los atributos recuperados en la matriz *pAttributesName* al llamar al método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="b99bd-114">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface can be used for range retrieval by specifying the attribute and range for one of the retrieved attributes in the *pAttributesName* array when calling the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method.</span></span>


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



<span data-ttu-id="b99bd-115">Cuando se usa la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para la recuperación de intervalos, hay un problema que se debe solucionar de forma específica.</span><span class="sxs-lookup"><span data-stu-id="b99bd-115">When using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="b99bd-116">Cuando el intervalo solicitado supera el número de valores restantes, [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) devolverá la **\_ columna E ADS \_ \_ no \_ establecida**.</span><span class="sxs-lookup"><span data-stu-id="b99bd-116">When the range requested exceeds the number of remaining values, [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="b99bd-117">Para recuperar los valores restantes, es necesario usar el carácter comodín de intervalo ' \* '.</span><span class="sxs-lookup"><span data-stu-id="b99bd-117">To retrieve the remaining values, it is necessary to use the range wildcard '\*'.</span></span> <span data-ttu-id="b99bd-118">Por ejemplo, si un grupo contiene 150 miembros, los valores de miembro 0-100 se pueden recuperar normalmente mediante la recuperación por intervalos.</span><span class="sxs-lookup"><span data-stu-id="b99bd-118">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="b99bd-119">Si después se solicita el intervalo 101-200, **IDirectorySearch:: getcolumn (** devolverá la **\_ columna E ADS \_ \_ no \_ establecida**.</span><span class="sxs-lookup"><span data-stu-id="b99bd-119">If range 101-200 is then requested, **IDirectorySearch::GetColumn** will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="b99bd-120">Este problema se puede evitar mediante el método [**IDirectorySearch:: GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) .</span><span class="sxs-lookup"><span data-stu-id="b99bd-120">This problem can be avoided by using the [**IDirectorySearch::GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) method.</span></span> <span data-ttu-id="b99bd-121">Normalmente, **GetNextColumnName** devolverá la cadena de consulta original.</span><span class="sxs-lookup"><span data-stu-id="b99bd-121">Normally, **GetNextColumnName** will return the original query string.</span></span> <span data-ttu-id="b99bd-122">Sin embargo, cuando el intervalo solicitado supera el número de valores restantes, **GetNextColumnName** devolverá una versión modificada de la cadena de consulta reemplazando el valor de intervalo superior por el comodín de intervalo ' \* '.</span><span class="sxs-lookup"><span data-stu-id="b99bd-122">However, when the range requested exceeds the number of remaining values, **GetNextColumnName** will return a modified version of the query string by replacing the high range value with the range wildcard '\*'.</span></span> <span data-ttu-id="b99bd-123">En el ejemplo anterior, la primera consulta se realizaría con una cadena de atributo de "Member; Range = 0-100" y **GetNextColumnName** devolverá "Member; Range = 0-100".</span><span class="sxs-lookup"><span data-stu-id="b99bd-123">In the example above, the first query would be performed with an attribute string of "member;range=0-100" and **GetNextColumnName** will return "member;range=0-100".</span></span> <span data-ttu-id="b99bd-124">En la segunda consulta, la cadena de atributo sería "Member; Range = 101-200", pero **GetNextColumnName** devolverá "Member; Range = 101- \* ".</span><span class="sxs-lookup"><span data-stu-id="b99bd-124">In the second query, the attribute string would be "member;range=101-200", but **GetNextColumnName** will return "member;range=101-\*".</span></span> <span data-ttu-id="b99bd-125">Este caso se puede determinar comparando la cadena de atributo original con el resultado de **GetNextColumnName**.</span><span class="sxs-lookup"><span data-stu-id="b99bd-125">This case can be determined by comparing the original attribute string to the result of **GetNextColumnName**.</span></span> <span data-ttu-id="b99bd-126">Si las cadenas son diferentes, se debe volver a solicitar el último bloque de valores con el carácter comodín de intervalo.</span><span class="sxs-lookup"><span data-stu-id="b99bd-126">If the strings are different, the last block of values should be requested again with the range wildcard.</span></span>

<span data-ttu-id="b99bd-127">Para obtener más información y un ejemplo de código que muestra cómo usar la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para la recuperación de intervalos, vea el [código de ejemplo para abarcar con IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).</span><span class="sxs-lookup"><span data-stu-id="b99bd-127">For more information and a code example that shows how to use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, see [Example Code for Ranging with IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).</span></span>

 

 




