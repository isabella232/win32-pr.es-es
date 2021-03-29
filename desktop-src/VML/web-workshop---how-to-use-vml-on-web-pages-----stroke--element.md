---
title: Usar el elemento stroke
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Web Workshop, Stroke (elemento)
- diseñar páginas web, elemento stroke
- Lenguaje de marcado de vectores (VML), elemento stroke
- VML (Lenguaje de marcado de vectores), elemento stroke
- Vector Graphics, Stroke (elemento)
- elemento stroke
- Elementos VML, trazo
- Formas VML, elemento stroke
- Lenguaje de marcado de vectores (VML), atributo de propiedad DashStyle
- VML (Lenguaje de marcado de vectores), atributo de propiedad DashStyle
- gráficos vectoriales, atributo de propiedad DashStyle
- DashStyle (atributo de propiedad)
- Lenguaje de marcado de vectores (VML), atributo de propiedad Opacity
- VML (Lenguaje de marcado de vectores), atributo de propiedad Opacity
- gráficos vectoriales, atributo de propiedad Opacity
- atributo de propiedad Opacity
- Lenguaje de marcado de vectores (VML), atributo de propiedad lineStyle
- VML (Lenguaje de marcado de vectores), atributo de propiedad lineStyle
- gráficos vectoriales, atributo de propiedad lineStyle
- atributo de propiedad lineStyle
- Lenguaje de marcado de vectores (VML), atributo de propiedad joinstyle
- VML (Lenguaje de marcado de vectores), atributo de propiedad joinstyle
- gráficos vectoriales, atributo de propiedad joinstyle
- atributo de propiedad joinstyle
- Lenguaje de marcado de vectores (VML), atributo de propiedad filltype
- VML (Lenguaje de marcado de vectores), atributo de propiedad filltype
- gráficos vectoriales, atributo de propiedad filltype
- atributo de propiedad filltype
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b58e02945884ea63ad1be01e67cfc156951cd5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359380"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="a3ad5-132">Usar el elemento stroke</span><span class="sxs-lookup"><span data-stu-id="a3ad5-132">Using the Stroke Element</span></span>

<span data-ttu-id="a3ad5-133">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-133">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a3ad5-134">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-134">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a3ad5-135">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-135">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a3ad5-136">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-136">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a3ad5-137">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a3ad5-137">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a3ad5-138">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a3ad5-138">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a3ad5-139">Usar `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="a3ad5-139">Using `<stroke>`</span></span>

<span data-ttu-id="a3ad5-140">Como ha aprendido, puede usar los atributos de la propiedad **StrokeColor** y **strokeweight** de una forma predefinida, como `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` , `<arc>` --para especificar el color y el grosor del contorno de una forma.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-140">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="a3ad5-141">En este tema, se muestra cómo dibujar una forma que tiene un esquema más avanzado.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-141">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="a3ad5-142">Puede colocar el `<stroke>` subelemento dentro de `<shape>` , o `<shapetype>` , o cualquier elemento de forma predefinido para describir cómo dibujar el contorno de la forma.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-142">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="a3ad5-143">Después, puede usar los atributos de propiedad (por ejemplo, [DashStyle](#dashstyle), [Opacity](#opacity), [LineStyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) ) del `<stroke>` subelemento para personalizar el esquema.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-143">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="a3ad5-144">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="a3ad5-144">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="a3ad5-145">DashStyle</span><span class="sxs-lookup"><span data-stu-id="a3ad5-145">dashstyle</span></span>

<span data-ttu-id="a3ad5-146">Puede usar el atributo de propiedad **DashStyle** del `<stroke>` subelemento para dibujar un contorno con varios estilos de guión.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-146">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="a3ad5-147">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="a3ad5-147">**Examples:**</span></span>

<span data-ttu-id="a3ad5-148">Si especifica `<v:stroke dashstyle="solid" />` dentro del `<line>` elemento, puede crear una línea sólida, tal como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-148">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 bytes)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="a3ad5-150">Si cambia el atributo de la propiedad **DashStyle** a "dot", puede crear una línea de puntos, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-150">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 bytes)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="a3ad5-152">Si cambia el atributo de la propiedad **DashStyle** a "Dash", puede crear una línea de guiones, tal y como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-152">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 bytes)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="a3ad5-154">Si cambia el atributo de la propiedad **DashStyle** a "dashDot", puede crear una línea con un estilo de puntos y guiones, tal y como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-154">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 bytes)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="a3ad5-156">Si cambia el atributo de la propiedad **DashStyle** a "longdash", puede crear una línea con un estilo largo discontinuo, tal como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-156">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 bytes)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="a3ad5-158">Si cambia el atributo de la propiedad **DashStyle** a "longdashdot", puede crear una línea con un estilo de puntos y guiones largos, tal y como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-158">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 bytes)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="a3ad5-160">Si coloca `<v:stroke dashstyle="dashdot" />` dentro del `<rect>` elemento, puede crear un rectángulo con un contorno discontinuo y punteado, tal y como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-160">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 bytes)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="a3ad5-162">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="a3ad5-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="a3ad5-163">opacidad</span><span class="sxs-lookup"><span data-stu-id="a3ad5-163">opacity</span></span>

<span data-ttu-id="a3ad5-164">Puede usar el atributo de propiedad **Opacity** del `<stroke>` subelemento para dibujar un contorno con varios estilos de opacidad.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-164">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="a3ad5-165">El valor del atributo de la propiedad **Opacity** puede ser cualquier número entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-165">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="a3ad5-166">De forma predeterminada, es 1, lo que indica una opacidad completa.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-166">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="a3ad5-167">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="a3ad5-167">**Examples:**</span></span>

<span data-ttu-id="a3ad5-168">La siguiente representación de VML crea una línea con una opacidad completa:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-168">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 bytes)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="a3ad5-170">Si agrega `<v:stroke opacity="0.5" />` dentro del `<line>` elemento, puede crear una línea con una opacidad del 50%, tal como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-170">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 bytes)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="a3ad5-172">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="a3ad5-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="a3ad5-173">lineStyle</span><span class="sxs-lookup"><span data-stu-id="a3ad5-173">linestyle</span></span>

<span data-ttu-id="a3ad5-174">Puede usar el atributo de propiedad **LineStyle** del `<stroke>` subelemento para dibujar un contorno con varios estilos de línea.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-174">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="a3ad5-175">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="a3ad5-175">**Examples:**</span></span>

<span data-ttu-id="a3ad5-176">Si especifica `<v:stroke linestyle="single" />` dentro del `<rect>` elemento, puede crear un rectángulo con un solo esquema, tal y como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-176">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 bytes)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="a3ad5-178">Si cambia el atributo de la propiedad **LineStyle** a "thinthin", puede crear un rectángulo con el contorno (1:1:1), tal y como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-178">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 bytes)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="a3ad5-180">Si cambia el atributo de la propiedad **LineStyle** a "thinthick", puede crear un rectángulo con el contorno (1:1:2), tal y como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-180">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 bytes)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="a3ad5-182">Si cambia el atributo de la propiedad **LineStyle** a "thickthin", puede crear un rectángulo con el contorno (2:1:1), tal y como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-182">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 bytes)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="a3ad5-184">Si cambia el atributo de la propiedad **LineStyle** a "thickbetweenthin", puede crear un rectángulo con el contorno (1:1:2:1:1), tal y como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-184">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 bytes)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="a3ad5-186">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="a3ad5-186">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="a3ad5-187">joinstyle</span><span class="sxs-lookup"><span data-stu-id="a3ad5-187">joinstyle</span></span>

<span data-ttu-id="a3ad5-188">Puede usar el atributo **joinstyle** del `<stroke>` subelemento para definir cómo se unen las líneas.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-188">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="a3ad5-189">Por ejemplo, para crear una forma que tenga el esquema de combinación redonda, tal y como se muestra en la siguiente ilustración, puede especificar `<v:stroke joinstyle="round" />` dentro del `<polyline>` elemento, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-189">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 bytes)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="a3ad5-191">Si cambia el atributo de la propiedad **joinstyle** a "Bevel", puede crear una forma que tenga el contorno de la unión biselada, tal como se muestra en la siguiente representación VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-191">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 bytes)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="a3ad5-193">Si cambia el atributo de la propiedad **joinstyle** a "inglete", puede crear una forma que tenga el contorno de unión angular, tal como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-193">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 bytes)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="a3ad5-195">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="a3ad5-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="a3ad5-196">filltype</span><span class="sxs-lookup"><span data-stu-id="a3ad5-196">filltype</span></span>

<span data-ttu-id="a3ad5-197">Puede usar el atributo de la propiedad **filltype** del `<stroke>` subelemento para dibujar un contorno con varios efectos de relleno.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-197">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="a3ad5-198">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="a3ad5-198">**Examples:**</span></span>

<span data-ttu-id="a3ad5-199">Si especifica `<v:stroke filltype="solid" />` dentro del `<roundrect>` elemento, puede crear un rectángulo redondeado con el contorno sólido relleno, tal como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-199">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 bytes)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="a3ad5-201">Si cambia el atributo de la propiedad **filltype** a "pattern", apunte el atributo de propiedad **src** a la ubicación del archivo de imagen de patrón y establezca el atributo de propiedad **color2** en el segundo color de patrón, puede crear un rectángulo redondeado con un contorno de patrón, tal como se muestra en la siguiente representación VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-201">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 bytes)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="a3ad5-203">Si cambia el atributo de la propiedad **filltype** a "Tile" y apunta el atributo de propiedad **src** a la ubicación del archivo de imagen, puede crear un rectángulo redondeado con un esquema en mosaico, tal como se muestra en la siguiente representación VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-203">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 bytes)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="a3ad5-205">Si cambia el atributo de la propiedad **filltype** a "Frame" y apunta el atributo de propiedad **src** a la ubicación del archivo de imagen, puede crear un rectángulo redondeado con un contorno de imagen, como se muestra en la siguiente representación VML:</span><span class="sxs-lookup"><span data-stu-id="a3ad5-205">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 bytes)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="a3ad5-207">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span><span class="sxs-lookup"><span data-stu-id="a3ad5-207">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 