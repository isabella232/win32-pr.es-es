---
title: Recuperación de intervalos de atributos
description: Un atributo con varios valores puede tener casi cualquier número de valores. En muchos casos, puede ser ventajoso, o incluso necesario, limitar el intervalo de valores recuperados por una consulta.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- ADSI de recuperación de intervalo de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8787eb0b2aba30d1926b4d9cbb7e566e0f59c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993871"
---
# <a name="attribute-range-retrieval"></a><span data-ttu-id="22368-105">Recuperación de intervalos de atributos</span><span class="sxs-lookup"><span data-stu-id="22368-105">Attribute Range Retrieval</span></span>

<span data-ttu-id="22368-106">Un atributo con varios valores puede tener casi cualquier número de valores.</span><span class="sxs-lookup"><span data-stu-id="22368-106">A multi-valued attribute can have almost any number of values.</span></span> <span data-ttu-id="22368-107">En muchos casos, puede ser ventajoso, o incluso necesario, limitar el intervalo de valores recuperados por una consulta.</span><span class="sxs-lookup"><span data-stu-id="22368-107">In many cases, it may be advantageous, or even necessary, to limit the range of values that are retrieved by a query.</span></span>

<span data-ttu-id="22368-108">La recuperación por rangos implica solicitar un número limitado de valores de atributo en una sola consulta.</span><span class="sxs-lookup"><span data-stu-id="22368-108">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="22368-109">El número de valores solicitados debe ser menor o igual que el número máximo de valores admitidos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="22368-109">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="22368-110">Para reducir el número de veces que la consulta debe ponerse en contacto con el servidor, el número de valores solicitados debe ser lo más cercano posible a este máximo.</span><span class="sxs-lookup"><span data-stu-id="22368-110">To reduce the number of times the query must contact the server, the number of values requested should be as close to this maximum as possible.</span></span> <span data-ttu-id="22368-111">Para permitir que una aplicación funcione correctamente con todos los servidores de Windows, se debe usar un número máximo de 1000.</span><span class="sxs-lookup"><span data-stu-id="22368-111">To enable an application to work correctly with all Windows servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="22368-112">Los especificadores de intervalo para una consulta de propiedad requieren el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="22368-112">The range specifiers for a property query require the following form:</span></span>


```C++
range=<low range>-<high range>
```



<span data-ttu-id="22368-113">donde " &lt; Low Range &gt; " es el índice de base cero del primer valor de propiedad que se va a recuperar y " &lt; High Range &gt; " es el índice de base cero del último valor de propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="22368-113">where "&lt;low range&gt;" is the zero-based index of the first property value to retrieve and "&lt;high range&gt;" is the zero-based index of the last property value to retrieve.</span></span> <span data-ttu-id="22368-114">Se usa cero para &lt; el "intervalo inferior &gt; " para especificar la primera entrada.</span><span class="sxs-lookup"><span data-stu-id="22368-114">Zero is used for "&lt;low range&gt;" to specify the first entry.</span></span> <span data-ttu-id="22368-115">El carácter comodín ( \* ) se puede usar para " &lt; High Range &gt; " a fin de especificar todas las entradas restantes.</span><span class="sxs-lookup"><span data-stu-id="22368-115">The wildcard character (\*) can be used for "&lt;high range&gt;" to specify all remaining entries.</span></span>

<span data-ttu-id="22368-116">En la tabla siguiente se muestran ejemplos de especificadores de intervalo.</span><span class="sxs-lookup"><span data-stu-id="22368-116">The following table lists examples of range specifiers.</span></span>



| <span data-ttu-id="22368-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="22368-117">Example</span></span>      | <span data-ttu-id="22368-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="22368-118">Description</span></span>                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="22368-119">intervalo = 0-\*</span><span class="sxs-lookup"><span data-stu-id="22368-119">range=0-\*</span></span>   | <span data-ttu-id="22368-120">Recupere todos los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="22368-120">Retrieve all property values.</span></span> <span data-ttu-id="22368-121">Esto está sujeto a los límites impuestos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="22368-121">This is subject to limits imposed by the server.</span></span>                |
| <span data-ttu-id="22368-122">intervalo = 0-500</span><span class="sxs-lookup"><span data-stu-id="22368-122">range=0-500</span></span>  | <span data-ttu-id="22368-123">Recupere de 1 a 501st valores inclusivos.</span><span class="sxs-lookup"><span data-stu-id="22368-123">Retrieve from 1st to 501st values inclusively.</span></span>                                                |
| <span data-ttu-id="22368-124">intervalo = 2-3</span><span class="sxs-lookup"><span data-stu-id="22368-124">range=2-3</span></span>    | <span data-ttu-id="22368-125">Recupere los valores 3 y 4.</span><span class="sxs-lookup"><span data-stu-id="22368-125">Retrieve 3rd and 4th values.</span></span>                                                                  |
| <span data-ttu-id="22368-126">intervalo = 501-\*</span><span class="sxs-lookup"><span data-stu-id="22368-126">range=501-\*</span></span> | <span data-ttu-id="22368-127">Recupere el 502nd y todos los valores restantes.</span><span class="sxs-lookup"><span data-stu-id="22368-127">Retrieve the 502nd and all remaining values.</span></span> <span data-ttu-id="22368-128">Esto está sujeto a los límites impuestos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="22368-128">This is subject to limits imposed by the server.</span></span> |



 

<span data-ttu-id="22368-129">Hay varias maneras de recuperar un intervalo de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="22368-129">There are several different ways to retrieve a range of property values.</span></span> <span data-ttu-id="22368-130">El método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) se puede utilizar en un lenguaje de automatización o en C++.</span><span class="sxs-lookup"><span data-stu-id="22368-130">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method can be used in either an automation language or C++.</span></span> <span data-ttu-id="22368-131">El método **IADs. GetInfoEx** es el método preferido para realizar la recuperación de intervalos.</span><span class="sxs-lookup"><span data-stu-id="22368-131">The **IADs.GetInfoEx** method is the preferred method of performing range retrieval.</span></span> <span data-ttu-id="22368-132">Para obtener más información sobre el uso de **IADs. GetInfoEx** para la recuperación de intervalos, vea [usar iAds:: GetInfoEx para la recuperación de intervalos](using-iads--getinfoex-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="22368-132">For more information about using **IADs.GetInfoEx** for range retrieval, see [Using IADs::GetInfoEx for Range Retrieval](using-iads--getinfoex-for-range-retrieval.md).</span></span>

<span data-ttu-id="22368-133">Si se utiliza un lenguaje de automatización, los objetos de directorio ActiveX (ADO) se pueden usar para recuperar un intervalo de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="22368-133">If an automation language is used, the ActiveX Directory Objects (ADO) can be used to retrieve a range of property values.</span></span> <span data-ttu-id="22368-134">Para obtener más información sobre el uso de ADO para la recuperación de intervalos, vea [usar ado para la recuperación por intervalos](using-ado-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="22368-134">For more information about using ADO for range retrieval, see [Using ADO for Range Retrieval](using-ado-for-range-retrieval.md).</span></span>

<span data-ttu-id="22368-135">Si se usa C++, se pueden usar las interfaces [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) y [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para recuperar un intervalo de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="22368-135">If C++ is used, the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) and [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="22368-136">Para obtener más información sobre el uso de **IDirectorySearch** y **IDirectoryObject** para la recuperación de intervalos, vea [usar IDirectorySearch y IDirectoryObject para la recuperación de intervalos](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="22368-136">For more information about using **IDirectorySearch** and **IDirectoryObject** for range retrieval, see [Using IDirectorySearch and IDirectoryObject for Range Retrieval](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span></span>

 

 




