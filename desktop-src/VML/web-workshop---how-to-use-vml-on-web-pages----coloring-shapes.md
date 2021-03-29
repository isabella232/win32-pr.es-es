---
title: Colorear formas
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Web Workshop, colorear formas
- diseñar páginas web, colorear formas
- Lenguaje de marcado de vectores (VML), colorear formas
- VML (Lenguaje de marcado de vectores), formas coloreadas
- gráficos vectoriales, formas coloreadas
- Formas VML, colorear
- colorear formas
- Lenguaje de marcado de vectores (VML), nombres de colores de palabras clave
- VML (Lenguaje de marcado de vectores), nombres de colores de palabras clave
- gráficos vectoriales, nombres de colores de palabras clave
- nombres de colores de palabras clave
- Lenguaje de marcado de vectores (VML), triples RGB
- VML (Lenguaje de marcado de vectores), triples RGB
- gráficos vectoriales, triples RGB
- Triples RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1257c5f5b0cf8021658820f09de6e87099f0a52b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078055"
---
# <a name="coloring-shapes"></a><span data-ttu-id="6651d-119">Colorear formas</span><span class="sxs-lookup"><span data-stu-id="6651d-119">Coloring Shapes</span></span>

<span data-ttu-id="6651d-120">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6651d-120">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6651d-121">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="6651d-121">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6651d-122">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="6651d-122">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6651d-123">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="6651d-123">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6651d-124">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6651d-124">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6651d-125">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6651d-125">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6651d-126">Como hemos mencionado en las secciones anteriores, puede usar "rojo" para representar un color rojo, "azul" para representar un color en azul, etc.</span><span class="sxs-lookup"><span data-stu-id="6651d-126">As we mentioned in earlier sections, you can use "red" to represent a color in red, "blue" to represent a color in blue, and so on.</span></span> <span data-ttu-id="6651d-127">En este tema, se muestra cómo dibujar formas en cualquier color que desee.</span><span class="sxs-lookup"><span data-stu-id="6651d-127">In this topic, we will illustrate how to draw shapes in any color you want.</span></span>

<span data-ttu-id="6651d-128">VML extiende la sintaxis de color HTML y CSS.</span><span class="sxs-lookup"><span data-stu-id="6651d-128">VML extends HTML and CSS color syntax.</span></span> <span data-ttu-id="6651d-129">Cuando el tipo de atributo de un elemento VML es color, como **fillColor** y **StrokeColor** , puede expresar el color mediante un nombre de [color de palabra clave](#keyword-color-name) o un [tripledo RGB](#rgb-triplet).</span><span class="sxs-lookup"><span data-stu-id="6651d-129">When the attribute type of a VML element is color -- such as **fillcolor** and **strokecolor** -- you can express the color by using either a [keyword color name](#keyword-color-name) or an [RGB triplet](#rgb-triplet).</span></span>

<span data-ttu-id="6651d-130">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="6651d-130">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="keyword-color-name"></a><span data-ttu-id="6651d-131">Nombre de color de palabra clave</span><span class="sxs-lookup"><span data-stu-id="6651d-131">Keyword Color Name</span></span>

<span data-ttu-id="6651d-132">HTML 4,0 define una lista de nombres de colores de palabras clave.</span><span class="sxs-lookup"><span data-stu-id="6651d-132">HTML 4.0 defines a list of keyword color names.</span></span> <span data-ttu-id="6651d-133">Son aguamarina, Black, Blue, Fuchsia, Gray, Green, Lima, granate, Navy, oliva, violeta, rojo, plata, verde azulado, blanco y amarillo.</span><span class="sxs-lookup"><span data-stu-id="6651d-133">They are aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, and yellow.</span></span> <span data-ttu-id="6651d-134">El valor RGB de estos 16 colores se define en la [especificación HTML 4,0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span><span class="sxs-lookup"><span data-stu-id="6651d-134">The RGB value for these 16 colors are defined in [HTML 4.0 specification](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span></span>

<span data-ttu-id="6651d-135">Por ejemplo, puede dibujar un rectángulo relleno con amarillo especificando `fillcolor="yellow"` y póngale un contorno azul especificando `strokecolor="blue"` , tal y como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="6651d-135">For example, you can draw a rectangle filled with yellow by specifying `fillcolor="yellow"`, and give it a blue outline by specifying `strokecolor="blue"`, as shown in the following VML representation:</span></span>

![color1.gif (305 bytes)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





<span data-ttu-id="6651d-137">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="6651d-137">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rgb-triplet"></a><span data-ttu-id="6651d-138">Tripledo RGB</span><span class="sxs-lookup"><span data-stu-id="6651d-138">RGB Triplet</span></span>

<span data-ttu-id="6651d-139">Si el color no es un [nombre de color de palabra clave](#keyword-color-name), puede expresar el color como un tripledor decimal RGB o un tripledo hexadecimal RGB.</span><span class="sxs-lookup"><span data-stu-id="6651d-139">If the color is not a [keyword color name](#keyword-color-name), you can express the color as either an RGB decimal triplet or an RGB hexadecimal triplet.</span></span> <span data-ttu-id="6651d-140">Con los triples RGB, puede especificar valores para los componentes rojo, verde y azul del color, estableciendo cada componente en un valor comprendido entre 0 y 255 en decimal, o de 00 a FF en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="6651d-140">With RGB triplets, you can specify values for the red, green, and blue components of the color, setting each component to a value ranging from 0 through 255 in decimal, or 00 through FF in hexadecimal.</span></span>

<span data-ttu-id="6651d-141">Por ejemplo, puede crear un rectángulo que se rellene con un color personalizado con un valor RGB de 253, 249, 186 en formato decimal especificando `fillcolor="rgb(253,249, 186)"` o `fillcolor="#FDF9BA"` , tal y como se muestra en la siguiente representación de VML.</span><span class="sxs-lookup"><span data-stu-id="6651d-141">For example, you can create a rectangle that is filled with a customized color with an RGB value of 253, 249, 186 in decimal by specifying either `fillcolor="rgb(253,249, 186)"` or `fillcolor="#FDF9BA"`, as shown in the following VML representation.</span></span> <span data-ttu-id="6651d-142">En hexadecimal, el valor 253 se convierte en FD, 249 se convierte en F9 y 186 se convierte en BA.</span><span class="sxs-lookup"><span data-stu-id="6651d-142">In hexadecimal, the value 253 becomes FD, 249 becomes F9, and 186 becomes BA.</span></span>

![color2.gif (305 bytes)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





<span data-ttu-id="6651d-144">Si el color RGB en hexadecimal tiene un patrón como XXYYZZ, puede abreviarlo como XYZ.</span><span class="sxs-lookup"><span data-stu-id="6651d-144">If the RGB in hexadecimal has a pattern such as XXYYZZ, you can abbreviate it to XYZ.</span></span> <span data-ttu-id="6651d-145">Por ejemplo, " \# 66FF99" se puede escribir como " \# 6F9".</span><span class="sxs-lookup"><span data-stu-id="6651d-145">For example, "\#66FF99" can be written out as "\#6F9".</span></span>

<span data-ttu-id="6651d-146">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="6651d-146">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="6651d-147">Resumen</span><span class="sxs-lookup"><span data-stu-id="6651d-147">Summary</span></span>

<span data-ttu-id="6651d-148">En VML, puede representar un color en uno de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="6651d-148">In VML, you can represent a color in one of the following formats:</span></span>

1.  <span data-ttu-id="6651d-149">fillColor = "Blue"</span><span class="sxs-lookup"><span data-stu-id="6651d-149">fillcolor="blue"</span></span>
2.  <span data-ttu-id="6651d-150">fillColor = "RGB (0, 0255)"</span><span class="sxs-lookup"><span data-stu-id="6651d-150">fillcolor="rgb(0,0,255)"</span></span>
3.  <span data-ttu-id="6651d-151">fillColor = " \# 0000FF"</span><span class="sxs-lookup"><span data-stu-id="6651d-151">fillcolor="\#0000ff"</span></span>

 

 