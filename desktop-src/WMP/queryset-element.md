---
title: Elemento querySet
description: El elemento querySet contiene elementos que definen qué elementos multimedia se seleccionarán de la biblioteca.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- Elemento querySet Media Player Windows
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4971c2a7f601132640d7654a95dd288f1740a467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709069"
---
# <a name="queryset-element"></a><span data-ttu-id="c8182-104">Elemento querySet</span><span class="sxs-lookup"><span data-stu-id="c8182-104">querySet Element</span></span>

<span data-ttu-id="c8182-105">El elemento **querySet** contiene elementos que definen qué elementos multimedia se seleccionarán de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c8182-105">The **querySet** element contains elements that define which media items will be selected from the library.</span></span>

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a><span data-ttu-id="c8182-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8182-106">Attributes</span></span>

<span data-ttu-id="c8182-107">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="c8182-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="c8182-108">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="c8182-108">Parent/Child Elements</span></span>



| <span data-ttu-id="c8182-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="c8182-109">Hierarchy</span></span> | <span data-ttu-id="c8182-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="c8182-110">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="c8182-111">Parent</span><span class="sxs-lookup"><span data-stu-id="c8182-111">Parent</span></span>    | [<span data-ttu-id="c8182-112">smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="c8182-112">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="c8182-113">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="c8182-113">Child</span></span>     | [<span data-ttu-id="c8182-114">sourceFilter</span><span class="sxs-lookup"><span data-stu-id="c8182-114">sourceFilter</span></span>](sourcefilter-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="c8182-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8182-115">Remarks</span></span>

<span data-ttu-id="c8182-116">El elemento **querySet** especifica qué elementos multimedia deben seleccionarse de la biblioteca, sin tener en cuenta el tamaño del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c8182-116">The **querySet** element specifies which media items should be selected from the library, without regard for the size of the result set.</span></span> <span data-ttu-id="c8182-117">Por otro lado, el elemento **Filter** limita el tamaño del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c8182-117">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="c8182-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c8182-118">Examples</span></span>


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
```



## <a name="requirements"></a><span data-ttu-id="c8182-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8182-119">Requirements</span></span>



| <span data-ttu-id="c8182-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8182-120">Requirement</span></span> | <span data-ttu-id="c8182-121">Value</span><span class="sxs-lookup"><span data-stu-id="c8182-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="c8182-122">Versión</span><span class="sxs-lookup"><span data-stu-id="c8182-122">Version</span></span><br/> | <span data-ttu-id="c8182-123">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="c8182-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8182-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8182-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8182-125">**Elemento argument**</span><span class="sxs-lookup"><span data-stu-id="c8182-125">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="c8182-126">**Elemento Filter**</span><span class="sxs-lookup"><span data-stu-id="c8182-126">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="c8182-127">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="c8182-127">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="c8182-128">**Elemento smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="c8182-128">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="c8182-129">**Elemento sourceFilter**</span><span class="sxs-lookup"><span data-stu-id="c8182-129">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="c8182-130">**Referencia de elementos de lista de reproducción de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c8182-130">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





