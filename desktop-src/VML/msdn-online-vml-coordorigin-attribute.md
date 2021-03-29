---
title: Atributo CoordOrigin de VML
description: Atributo CoordOrigin de VML
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb08d35aac7e26cc15aa7699439ea9f7ab4dba94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904630"
---
# <a name="vml-coordorigin-attribute"></a><span data-ttu-id="d763e-103">Atributo CoordOrigin de VML</span><span class="sxs-lookup"><span data-stu-id="d763e-103">VML CoordOrigin Attribute</span></span>

<span data-ttu-id="d763e-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d763e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d763e-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="d763e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d763e-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="d763e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d763e-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="d763e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d763e-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d763e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d763e-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d763e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d763e-110">Especifica el origen de la unidad de coordenadas del rectángulo que delimita una forma.</span><span class="sxs-lookup"><span data-stu-id="d763e-110">Specifies the coordinate unit origin of the rectangle that bounds a shape.</span></span> <span data-ttu-id="d763e-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d763e-111">Read/write.</span></span> <span data-ttu-id="d763e-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d763e-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="d763e-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="d763e-113">**Applies To**</span></span>

[<span data-ttu-id="d763e-114">Forma</span><span class="sxs-lookup"><span data-stu-id="d763e-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d763e-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="d763e-115">**Tag Syntax**</span></span>

<span data-ttu-id="d763e-116"><v: *Element* coordorigin = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="d763e-116"><v: *element* coordorigin=" *expression* "></span></span>

<span data-ttu-id="d763e-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="d763e-117">**Script Syntax**</span></span>

<span data-ttu-id="d763e-118">*Element* . coordorigin = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="d763e-118">*element* .coordorigin="*expression*"</span></span>

<span data-ttu-id="d763e-119">*expresión* = de *elemento*. coordorigin</span><span class="sxs-lookup"><span data-stu-id="d763e-119">*expression*=*element*.coordorigin</span></span>

<span data-ttu-id="d763e-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="d763e-120">**Remarks**</span></span>

<span data-ttu-id="d763e-121">Si no se especifica, las coordenadas de origen son (0,0) en la esquina superior izquierda del cuadro de límite de la forma.</span><span class="sxs-lookup"><span data-stu-id="d763e-121">If not specified, the origin coordinates are (0,0) at the top left corner of the shape bounding box.</span></span>

<span data-ttu-id="d763e-122">El valor x de **CoordSize** se agrega al valor x de **CoordOrigin** para determinar el intervalo de los valores horizontales.</span><span class="sxs-lookup"><span data-stu-id="d763e-122">The x value of **CoordSize** is added to the x value of **CoordOrigin** to determine the range of the horizontal values.</span></span> <span data-ttu-id="d763e-123">Por ejemplo, si el valor x de **CoordOrigin** es-100 y el valor x de **CoordSize** es 200, las unidades horizontales van de-100 a + 100.</span><span class="sxs-lookup"><span data-stu-id="d763e-123">For example,if the x value of **CoordOrigin** is -100 and the x value of **CoordSize** is 200, the horizontal units will range from -100 to +100.</span></span> <span data-ttu-id="d763e-124">Si el valor x de **CoordOrigin** es 100 y el valor x de **CoordSize** es 200, las unidades horizontales van de 100 a 300, todo dentro del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="d763e-124">If the x value of **CoordOrigin** is 100 and the x value of **CoordSize** is 200, the horizontal units will range from 100 to 300, all within the bounding box.</span></span> <span data-ttu-id="d763e-125">Lo mismo se aplica a los valores y.</span><span class="sxs-lookup"><span data-stu-id="d763e-125">The same is true for the y values.</span></span>

<span data-ttu-id="d763e-126">Tenga en cuenta que este atributo es un vector y que las unidades son el mismo tipo de unidad que [CoordSize](msdn-online-vml-coordsize-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="d763e-126">Note that this attribute is a vector and that the units are the same type of unit as [CoordSize](msdn-online-vml-coordsize-attribute.md) .</span></span>

<span data-ttu-id="d763e-127">En scripting, dado que se trata de un vector 2D, puede tener acceso a los valores x e y por separado, y también puede determinar el tipo de unidades que se espera.</span><span class="sxs-lookup"><span data-stu-id="d763e-127">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="d763e-128">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="d763e-128">*VML Standard Attribute*</span></span>

<span data-ttu-id="d763e-129">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="d763e-129">**Example**</span></span>

<span data-ttu-id="d763e-130">El centro del cuadro de límite será el origen (0,0) de la ruta de acceso de la forma.</span><span class="sxs-lookup"><span data-stu-id="d763e-130">The center of the bounding box will be the origin (0,0) of the path for the shape.</span></span> <span data-ttu-id="d763e-131">Dado que **CoordOrigin** es "-500-500" y **CoordSize** es "1000 1000", las unidades horizontales y verticales oscilarán entre-500 y + 500.</span><span class="sxs-lookup"><span data-stu-id="d763e-131">Because **CoordOrigin** is "-500 -500" and **CoordSize** is "1000 1000", the horizontal and vertical units will range from -500 to +500.</span></span> <span data-ttu-id="d763e-132">La esquina izquierda y superior de la ruta de acceso estará en el centro del cuadro de límite definido por los puntos izquierdo y superior, tal como se define en el **estilo**.</span><span class="sxs-lookup"><span data-stu-id="d763e-132">The left and top corner of the path will be at the center of the bounding box defined by the left and top points as defined by **Style**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="d763e-133">[Ejemplo del atributo CoordOrigin](/previous-versions/bb229664(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d763e-133">[CoordOrigin Attribute Example](/previous-versions/bb229664(v=vs.85)).</span></span> <span data-ttu-id="d763e-134">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="d763e-134">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 