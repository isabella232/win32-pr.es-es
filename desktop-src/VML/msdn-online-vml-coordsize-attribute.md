---
title: Atributo CoordSize de VML
description: Atributo CoordSize de VML
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695618"
---
# <a name="vml-coordsize-attribute"></a><span data-ttu-id="e736d-103">Atributo CoordSize de VML</span><span class="sxs-lookup"><span data-stu-id="e736d-103">VML CoordSize Attribute</span></span>

<span data-ttu-id="e736d-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e736d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e736d-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="e736d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e736d-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="e736d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e736d-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="e736d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e736d-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e736d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e736d-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e736d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e736d-110">Especifica las unidades horizontales y verticales del rectángulo que delimita una forma.</span><span class="sxs-lookup"><span data-stu-id="e736d-110">Specifies the horizontal and vertical units of the rectangle that bounds a shape.</span></span> <span data-ttu-id="e736d-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e736d-111">Read/write.</span></span> <span data-ttu-id="e736d-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="e736d-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="e736d-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="e736d-113">**Applies To**</span></span>

[<span data-ttu-id="e736d-114">Forma</span><span class="sxs-lookup"><span data-stu-id="e736d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e736d-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="e736d-115">**Tag Syntax**</span></span>

<span data-ttu-id="e736d-116"><v: *Element* coordsize = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="e736d-116"><v: *element* coordsize=" *expression* "></span></span>

<span data-ttu-id="e736d-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="e736d-117">**Script Syntax**</span></span>

<span data-ttu-id="e736d-118">*Element* . coordsize = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="e736d-118">*element* .coordsize="*expression*"</span></span>

<span data-ttu-id="e736d-119">*expresión* = de *elemento*. coordsize</span><span class="sxs-lookup"><span data-stu-id="e736d-119">*expression*=*element*.coordsize</span></span>

<span data-ttu-id="e736d-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="e736d-120">**Remarks**</span></span>

<span data-ttu-id="e736d-121">Si no se especifica, el tamaño de la coordenada es el mismo que el del rectángulo de selección de la forma.</span><span class="sxs-lookup"><span data-stu-id="e736d-121">If not specified, the coordinate size is the same as the bounding box of the shape.</span></span>

<span data-ttu-id="e736d-122">Tenga en cuenta que este atributo es un vector y que las unidades son relativas a la longitud y el ancho del rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="e736d-122">Note that this attribute is a vector and that the units are relative to the length and width of the bounding rectangle.</span></span>

<span data-ttu-id="e736d-123">Tenga en cuenta también que la asignación entre **coordsize** y el cuadro de límite se puede convertir en anisotrópico.</span><span class="sxs-lookup"><span data-stu-id="e736d-123">Also note that mapping between **coordsize** and the bounding box can be made anisotropic.</span></span> <span data-ttu-id="e736d-124">Asegúrese de que el **ancho de coordsize** y el **alto de coordsize** coinciden con el ancho y el **alto** de **estilo** si no desea distorsionar la forma.</span><span class="sxs-lookup"><span data-stu-id="e736d-124">Make sure that the **coordsize width** and **coordsize height** is the same as the **style width** and **height** if you don't want to distort the shape.</span></span>

<span data-ttu-id="e736d-125">En scripting, dado que se trata de un vector 2D, puede tener acceso a los valores x e y por separado, y también puede determinar el tipo de unidades que se espera.</span><span class="sxs-lookup"><span data-stu-id="e736d-125">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="e736d-126">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="e736d-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="e736d-127">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="e736d-127">**Example**</span></span>

<span data-ttu-id="e736d-128">La forma es 100 puntos alto y 100 puntos de ancho, pero cada unidad horizontal y vertical del espacio de coordenadas es 1/10 de un punto.</span><span class="sxs-lookup"><span data-stu-id="e736d-128">The shape is 100 points high and 100 points wide, but each horizontal and vertical unit in the coordinate space is 1/10 of a point.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="e736d-129">[Ejemplo del atributo CoordSize](/previous-versions/bb229665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e736d-129">[CoordSize Attribute Example](/previous-versions/bb229665(v=vs.85)).</span></span> <span data-ttu-id="e736d-130">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="e736d-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 