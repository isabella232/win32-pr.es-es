---
title: Atributo Flip de VML
description: Atributo Flip de VML
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793761"
---
# <a name="vml-flip-attribute"></a><span data-ttu-id="304ea-103">Atributo Flip de VML</span><span class="sxs-lookup"><span data-stu-id="304ea-103">VML Flip Attribute</span></span>

<span data-ttu-id="304ea-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="304ea-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="304ea-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="304ea-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="304ea-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="304ea-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="304ea-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="304ea-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="304ea-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="304ea-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="304ea-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="304ea-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="304ea-110">Cambia la orientación de una forma.</span><span class="sxs-lookup"><span data-stu-id="304ea-110">Switches the orientation of a shape.</span></span> <span data-ttu-id="304ea-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="304ea-111">Read/write.</span></span> <span data-ttu-id="304ea-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="304ea-112">**String**.</span></span>

<span data-ttu-id="304ea-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="304ea-113">**Applies To**</span></span>

[<span data-ttu-id="304ea-114">Forma</span><span class="sxs-lookup"><span data-stu-id="304ea-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="304ea-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="304ea-115">**Tag Syntax**</span></span>

<span data-ttu-id="304ea-116"><v: *Element* style = "Flip: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="304ea-116"><v: *element* style="flip: *expression* "></span></span>

<span data-ttu-id="304ea-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="304ea-117">**Script Syntax**</span></span>

<span data-ttu-id="304ea-118">*Element* . Style. Flip = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="304ea-118">*element* .style.flip="*expression*"</span></span>

<span data-ttu-id="304ea-119">*expresión* = de *elemento*. Style. flip</span><span class="sxs-lookup"><span data-stu-id="304ea-119">*expression*=*element*.style.flip</span></span>

<span data-ttu-id="304ea-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="304ea-120">**Remarks**</span></span>

<span data-ttu-id="304ea-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="304ea-121">Values include:</span></span>



| <span data-ttu-id="304ea-122">Value</span><span class="sxs-lookup"><span data-stu-id="304ea-122">Value</span></span> | <span data-ttu-id="304ea-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="304ea-123">Description</span></span>                                           |
|-------|-------------------------------------------------------|
| <span data-ttu-id="304ea-124">x</span><span class="sxs-lookup"><span data-stu-id="304ea-124">x</span></span>     | <span data-ttu-id="304ea-125">Se voltea a lo largo del eje y, invirtiendo las coordenadas *x*.</span><span class="sxs-lookup"><span data-stu-id="304ea-125">Flip along the y-axis, reversing the *x*-coordinates.</span></span> |
| <span data-ttu-id="304ea-126">y</span><span class="sxs-lookup"><span data-stu-id="304ea-126">y</span></span>     | <span data-ttu-id="304ea-127">Se voltea a lo largo del eje *x* y se invierten las coordenadas y.</span><span class="sxs-lookup"><span data-stu-id="304ea-127">Flip along the *x*-axis, reversing the y-coordinates.</span></span> |
| <span data-ttu-id="304ea-128">xy</span><span class="sxs-lookup"><span data-stu-id="304ea-128">xy</span></span>    | <span data-ttu-id="304ea-129">Se voltea a lo largo del eje y y del eje *x*.</span><span class="sxs-lookup"><span data-stu-id="304ea-129">Flip along both the y- and *x*-axis.</span></span>                  |
| <span data-ttu-id="304ea-130">YX</span><span class="sxs-lookup"><span data-stu-id="304ea-130">yx</span></span>    | <span data-ttu-id="304ea-131">Se *voltea a lo* largo del eje *x* e y.</span><span class="sxs-lookup"><span data-stu-id="304ea-131">Flip along both the *x*- and *y*-axis.</span></span>                |



 

<span data-ttu-id="304ea-132">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="304ea-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="304ea-133">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="304ea-133">**See Also**</span></span>

[<span data-ttu-id="304ea-134">VgFlipOrientation</span><span class="sxs-lookup"><span data-stu-id="304ea-134">VgFlipOrientation</span></span>](msdn-online-vector-markup-language-object-model-reference.md)

<span data-ttu-id="304ea-135">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="304ea-135">**Example**</span></span>

<span data-ttu-id="304ea-136">La forma se voltea a lo largo del eje *y* invirtiendo las coordenadas *x* .</span><span class="sxs-lookup"><span data-stu-id="304ea-136">The shape is flipped along the *y* -axis by reversing the *x* -coordinates.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



<span data-ttu-id="304ea-137">[Ejemplo de atributo Flip](/previous-versions/bb229670(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="304ea-137">[Flip Attribute Example](/previous-versions/bb229670(v=vs.85)).</span></span> <span data-ttu-id="304ea-138">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="304ea-138">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 