---
title: Usar el elemento Stroke
description: En este artículo se describe el uso del elemento Stroke de VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Taller web, elemento de trazo
- diseñar páginas web, elemento de trazo
- Lenguaje de marcado de vectores (VML), elemento stroke
- VML (Lenguaje de marcado de vectores),elemento stroke
- gráficos vectoriales, elemento de trazo
- elemento stroke
- Elementos vml, trazo
- Formas de VML, elemento de trazo
- Lenguaje de marcado de vectores (VML),atributo de propiedad dashstyle
- VML (Lenguaje de marcado de vectores),atributo de propiedad dashstyle
- vector graphics,dashstyle property attribute
- atributo de propiedad dashstyle
- Lenguaje de marcado de vectores (VML),atributo de propiedad opacity
- VML (Lenguaje de marcado de vectores),atributo de propiedad opacity
- vector graphics,opacity property attribute
- Atributo de propiedad opacity
- Lenguaje de marcado de vectores (VML),atributo de propiedad linestyle
- VML (Lenguaje de marcado de vectores),atributo de propiedad linestyle
- vector graphics,linestyle property attribute
- Atributo de propiedad linestyle
- Lenguaje de marcado de vectores (VML),atributo de propiedad joinstyle
- VML (Lenguaje de marcado de vectores),atributo de propiedad joinstyle
- vector graphics,joinstyle property attribute
- atributo de propiedad joinstyle
- Lenguaje de marcado de vectores (VML),atributo de propiedad filltype
- VML (Lenguaje de marcado de vectores),atributo de propiedad filltype
- vector graphics,filltype property attribute
- atributo de propiedad filltype
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dff7a4b3bc654063fe8156476cc9c52453247a0b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407848"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="20581-131">Usar el elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="20581-131">Using the Stroke Element</span></span>

<span data-ttu-id="20581-132">En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="20581-132">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="20581-133">Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="20581-133">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="20581-134">A partir de diciembre de 2011, este tema se archivó.</span><span class="sxs-lookup"><span data-stu-id="20581-134">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="20581-135">Como resultado, ya no se mantiene activamente.</span><span class="sxs-lookup"><span data-stu-id="20581-135">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="20581-136">Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="20581-136">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="20581-137">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="20581-137">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="20581-138">Usar `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="20581-138">Using `<stroke>`</span></span>

<span data-ttu-id="20581-139">Como ha aprendido, puede usar los atributos de propiedad **strokecolor** y **strokeweight** de una forma predefinida( como , , , , , , , ) para especificar el color y el peso del contorno de una `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma.</span><span class="sxs-lookup"><span data-stu-id="20581-139">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="20581-140">En este tema, se muestra cómo dibujar una forma que tiene un esquema más avanzado.</span><span class="sxs-lookup"><span data-stu-id="20581-140">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="20581-141">Puede colocar el sub element dentro de , o , o cualquier elemento de forma predefinido para describir cómo dibujar el `<stroke>` `<shape>` contorno de la `<shapetype>` forma.</span><span class="sxs-lookup"><span data-stu-id="20581-141">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="20581-142">A continuación, puede usar los atributos de propiedad ( por ejemplo, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype)](#filltype) del `<stroke>` sub-elemento para personalizar el esquema.</span><span class="sxs-lookup"><span data-stu-id="20581-142">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="20581-143">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="20581-143">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="20581-144">dashstyle</span><span class="sxs-lookup"><span data-stu-id="20581-144">dashstyle</span></span>

<span data-ttu-id="20581-145">Puede usar el atributo **de propiedad dashstyle** del `<stroke>` sub elemento para dibujar un esquema con varios estilos de guion.</span><span class="sxs-lookup"><span data-stu-id="20581-145">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="20581-146">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="20581-146">**Examples:**</span></span>

<span data-ttu-id="20581-147">Si especifica dentro `<v:stroke dashstyle="solid" />` del elemento , puede crear una línea `<line>` sólida, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-147">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 bytes)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="20581-149">Si cambia el atributo de **propiedad dashstyle** a "punto", puede crear una línea de puntos, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-149">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 bytes)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="20581-151">Si cambia el atributo de **propiedad dashstyle** a "dash", puede crear una línea de guiones, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-151">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 bytes)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="20581-153">Si cambia el atributo de propiedad **dashstyle** a "dashdot", puede crear una línea con un estilo discontinuo y de puntos, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-153">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 bytes)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="20581-155">Si cambia el atributo de propiedad **dashstyle** a "longdash", puede crear una línea con un estilo discontinuo largo, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-155">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 bytes)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="20581-157">Si cambia el atributo de propiedad **dashstyle** a "longdashdot", puede crear una línea con un estilo largo discontinuo y de puntos, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-157">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 bytes)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="20581-159">Si coloca dentro del elemento , puede crear un rectángulo que tenga un contorno discontinuo y de puntos, como se muestra `<v:stroke dashstyle="dashdot" />` en la siguiente representación de `<rect>` VML:</span><span class="sxs-lookup"><span data-stu-id="20581-159">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 bytes)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="20581-161">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="20581-161">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="20581-162">opacidad</span><span class="sxs-lookup"><span data-stu-id="20581-162">opacity</span></span>

<span data-ttu-id="20581-163">Puede usar el atributo **de propiedad de** opacidad del sub elemento para dibujar un esquema con varios estilos de `<stroke>` opacidad.</span><span class="sxs-lookup"><span data-stu-id="20581-163">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="20581-164">El valor del atributo **de propiedad de** opacidad puede ser cualquier número entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="20581-164">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="20581-165">De forma predeterminada, es 1, lo que indica una opacidad completa.</span><span class="sxs-lookup"><span data-stu-id="20581-165">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="20581-166">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="20581-166">**Examples:**</span></span>

<span data-ttu-id="20581-167">La siguiente representación de VML crea una línea con opacidad completa:</span><span class="sxs-lookup"><span data-stu-id="20581-167">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 bytes)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="20581-169">Si agrega dentro del elemento , puede crear una línea con una opacidad del 50 %, como se muestra `<v:stroke opacity="0.5" />` en la siguiente representación de `<line>` VML:</span><span class="sxs-lookup"><span data-stu-id="20581-169">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 bytes)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="20581-171">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="20581-171">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="20581-172">linestyle</span><span class="sxs-lookup"><span data-stu-id="20581-172">linestyle</span></span>

<span data-ttu-id="20581-173">Puede usar el atributo **de propiedad linestyle** del `<stroke>` sub elemento para dibujar un contorno con varios estilos de línea.</span><span class="sxs-lookup"><span data-stu-id="20581-173">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="20581-174">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="20581-174">**Examples:**</span></span>

<span data-ttu-id="20581-175">Si especifica dentro del elemento , puede crear un rectángulo con un único contorno, como se `<v:stroke linestyle="single" />` muestra en la siguiente representación de `<rect>` VML:</span><span class="sxs-lookup"><span data-stu-id="20581-175">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 bytes)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="20581-177">Si cambia el atributo de propiedad **linestyle** a "thinthin", puede crear un rectángulo con el contorno (1:1:1), como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-177">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 bytes)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="20581-179">Si cambia el atributo de propiedad **linestyle** a "thinthick", puede crear un rectángulo con el contorno (1:1:2), como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-179">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 bytes)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="20581-181">Si cambia el atributo de propiedad **linestyle** a "thickthin", puede crear un rectángulo con el contorno (2:1:1), como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-181">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 bytes)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="20581-183">Si cambia el atributo de propiedad **linestyle** a "thickbetweenthin", puede crear un rectángulo con el contorno (1:1:2:1:1), como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-183">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 bytes)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="20581-185">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="20581-185">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="20581-186">joinstyle</span><span class="sxs-lookup"><span data-stu-id="20581-186">joinstyle</span></span>

<span data-ttu-id="20581-187">Puede usar el atributo **joinstyle** del `<stroke>` sub-elemento para definir cómo se unen las líneas.</span><span class="sxs-lookup"><span data-stu-id="20581-187">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="20581-188">Por ejemplo, para crear una forma que tenga el contorno de combinación redondeada, como se muestra en la ilustración siguiente, puede especificar dentro del elemento , como se muestra en la siguiente representación `<v:stroke joinstyle="round" />` `<polyline>` de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-188">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 bytes)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="20581-190">Si cambia el atributo de propiedad **joinstyle** a "bevel", puede crear una forma que tenga el contorno bevel-join, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-190">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 bytes)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="20581-192">Si cambia el atributo de propiedad **joinstyle** a "miter", puede crear una forma que tenga el contorno de combinación de miter, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-192">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 bytes)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="20581-194">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="20581-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="20581-195">filltype</span><span class="sxs-lookup"><span data-stu-id="20581-195">filltype</span></span>

<span data-ttu-id="20581-196">Puede usar el atributo **de propiedad filltype** del `<stroke>` sub elemento para dibujar un esquema con varios efectos de relleno.</span><span class="sxs-lookup"><span data-stu-id="20581-196">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="20581-197">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="20581-197">**Examples:**</span></span>

<span data-ttu-id="20581-198">Si especifica dentro del elemento , puede crear un rectángulo redondeado con el contorno relleno sólido, como se muestra `<v:stroke filltype="solid" />` en la siguiente representación de `<roundrect>` VML:</span><span class="sxs-lookup"><span data-stu-id="20581-198">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 bytes)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="20581-200">Si cambia el atributo de propiedad **filltype** a "pattern", apunta el atributo de propiedad **src** a la ubicación del archivo de imagen de patrón y establece el atributo de propiedad **color2** en el segundo color de patrón, puede crear un rectángulo redondeado con un contorno de patrón, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-200">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 bytes)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="20581-202">Si cambia el atributo de propiedad **filltype** a "tile" y apunta el atributo de propiedad **src** a la ubicación del archivo de imagen, puede crear un rectángulo redondeado con un contorno en mosaico, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-202">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 bytes)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="20581-204">Si cambia el atributo de propiedad **filltype** a "frame" y apunta el atributo de propiedad **src** a la ubicación del archivo de imagen, puede crear un rectángulo redondeado con un contorno de imagen, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="20581-204">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 bytes)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="20581-206">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span><span class="sxs-lookup"><span data-stu-id="20581-206">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 