---
description: Una aplicación combina dos regiones mediante una llamada a la función CombineRgn.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Combinar regiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51db22daea448acfb02120844ca2859a5ba11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556964"
---
# <a name="combining-regions"></a><span data-ttu-id="04c35-103">Combinar regiones</span><span class="sxs-lookup"><span data-stu-id="04c35-103">Combining Regions</span></span>

<span data-ttu-id="04c35-104">Una aplicación combina dos regiones mediante una llamada a la función [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) .</span><span class="sxs-lookup"><span data-stu-id="04c35-104">An application combines two regions by calling the [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) function.</span></span> <span data-ttu-id="04c35-105">Mediante esta función, una aplicación puede combinar las partes de intersección de dos regiones, excepto las partes que interseccionan de dos regiones, las dos regiones originales en su totalidad, etc.</span><span class="sxs-lookup"><span data-stu-id="04c35-105">Using this function, an application can combine the intersecting parts of two regions, all but the intersecting parts of two regions, the two original regions in their entirety, and so on.</span></span> <span data-ttu-id="04c35-106">A continuación se muestran cinco valores que definen las combinaciones de regiones.</span><span class="sxs-lookup"><span data-stu-id="04c35-106">Following are five values that define the region combinations.</span></span>



| <span data-ttu-id="04c35-107">Value</span><span class="sxs-lookup"><span data-stu-id="04c35-107">Value</span></span>     | <span data-ttu-id="04c35-108">Significado</span><span class="sxs-lookup"><span data-stu-id="04c35-108">Meaning</span></span>                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04c35-109">RGN \_ y</span><span class="sxs-lookup"><span data-stu-id="04c35-109">RGN\_AND</span></span>  | <span data-ttu-id="04c35-110">Las partes de intersección de dos regiones originales definen una nueva región.</span><span class="sxs-lookup"><span data-stu-id="04c35-110">The intersecting parts of two original regions define a new region.</span></span>                   |
| <span data-ttu-id="04c35-111">copia de RGN \_</span><span class="sxs-lookup"><span data-stu-id="04c35-111">RGN\_COPY</span></span> | <span data-ttu-id="04c35-112">Una copia de la primera (de las dos regiones originales) define una nueva región.</span><span class="sxs-lookup"><span data-stu-id="04c35-112">A copy of the first (of the two original regions) defines a new region.</span></span>               |
| <span data-ttu-id="04c35-113">RGN ( \_ diferencia)</span><span class="sxs-lookup"><span data-stu-id="04c35-113">RGN\_DIFF</span></span> | <span data-ttu-id="04c35-114">La parte de la primera región que no forma una intersección con la segunda define una nueva región.</span><span class="sxs-lookup"><span data-stu-id="04c35-114">The part of the first region that does not intersect the second defines a new region.</span></span> |
| <span data-ttu-id="04c35-115">RGN \_ o</span><span class="sxs-lookup"><span data-stu-id="04c35-115">RGN\_OR</span></span>   | <span data-ttu-id="04c35-116">Las dos regiones originales definen una nueva región.</span><span class="sxs-lookup"><span data-stu-id="04c35-116">The two original regions define a new region.</span></span>                                         |
| <span data-ttu-id="04c35-117">RGN \_ XOR</span><span class="sxs-lookup"><span data-stu-id="04c35-117">RGN\_XOR</span></span>  | <span data-ttu-id="04c35-118">Las partes de las dos regiones originales que no se superponen definen una nueva región.</span><span class="sxs-lookup"><span data-stu-id="04c35-118">Those parts of the two original regions that do not overlap define a new region.</span></span>      |



 

<span data-ttu-id="04c35-119">En la ilustración siguiente se muestran las cinco combinaciones posibles de un cuadrado y una región circular resultante de una llamada a [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).</span><span class="sxs-lookup"><span data-stu-id="04c35-119">The following illustration shows the five possible combinations of a square and a circular region resulting from a call to [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).</span></span>

![Ilustración en la que se muestran los resultados descritos en la tabla anterior](images/csrgn-02.png)

 

 



