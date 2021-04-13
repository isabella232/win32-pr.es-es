---
title: Usar formas predefinidas
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Web Workshop, formas predefinidas
- diseñar páginas web, formas predefinidas
- Lenguaje de marcado de vectores (VML), formas predefinidas
- VML (Lenguaje de marcado de vectores), formas predefinidas
- gráficos vectoriales, formas predefinidas
- Formas VML, predefinidas
- formas predefinidas
- Lenguaje de marcado de vectores (VML), elemento Rect
- VML (Lenguaje de marcado de vectores), elemento Rect
- gráficos vectoriales, elemento Rect
- elemento Rect
- Elementos VML, Rect
- Lenguaje de marcado de vectores (VML), elemento roundrect
- VML (Lenguaje de marcado de vectores), elemento roundrect
- graphics Vector, elemento roundrect
- elemento roundrect
- Elementos VML, roundrect
- Lenguaje de marcado de vectores (VML), elemento de línea
- VML (Lenguaje de marcado de vectores), elemento de línea
- Vector Graphics, line (elemento)
- elemento line
- Elementos VML, línea
- Lenguaje de marcado de vectores (VML), elemento Polyline
- VML (Lenguaje de marcado de vectores), elemento Polyline
- Vector Graphics, Polyline (elemento)
- Polyline (elemento)
- Elementos VML, Polyline
- Elemento Curve de Lenguaje de marcado de vectores (VML)
- VML (Lenguaje de marcado de vectores), elemento Curve
- gráficos vectoriales, elemento Curve
- elemento Curve
- Elementos VML, curva
- Lenguaje de marcado de vectores (VML), elemento Arc
- VML (Lenguaje de marcado de vectores), elemento Arc
- gráficos vectoriales, elemento Arc
- elemento Arc
- Elementos VML, arco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c1cafacf00f6f3f9129c29c56837f3f485aa3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533268"
---
# <a name="using-predefined-shapes"></a><span data-ttu-id="12c7d-141">Usar formas predefinidas</span><span class="sxs-lookup"><span data-stu-id="12c7d-141">Using Predefined Shapes</span></span>

<span data-ttu-id="12c7d-142">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="12c7d-142">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="12c7d-143">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="12c7d-143">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="12c7d-144">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="12c7d-144">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="12c7d-145">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="12c7d-145">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="12c7d-146">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="12c7d-146">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="12c7d-147">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="12c7d-147">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="12c7d-148">Como ha aprendido, puede usar el `<oval>` elemento de VML para crear un óvalo sencillo.</span><span class="sxs-lookup"><span data-stu-id="12c7d-148">As you've learned, you can use the `<oval>` element of VML to create a simple oval.</span></span> <span data-ttu-id="12c7d-149">VML proporciona varios elementos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="12c7d-149">VML provides several other predefined elements.</span></span> <span data-ttu-id="12c7d-150">En este tema, se muestra cómo dibujar gráficos mediante estos elementos.</span><span class="sxs-lookup"><span data-stu-id="12c7d-150">In this topic, we will illustrate how to draw graphics by using these elements.</span></span>

<span data-ttu-id="12c7d-151">En este tema:</span><span class="sxs-lookup"><span data-stu-id="12c7d-151">In this topic:</span></span>

-   [<span data-ttu-id="12c7d-152">Rect</span><span class="sxs-lookup"><span data-stu-id="12c7d-152">rect</span></span>](#roundrect)
-   [<span data-ttu-id="12c7d-153">roundrect</span><span class="sxs-lookup"><span data-stu-id="12c7d-153">roundrect</span></span>](#roundrect)
-   [<span data-ttu-id="12c7d-154">Ondula</span><span class="sxs-lookup"><span data-stu-id="12c7d-154">line</span></span>](#polyline)
-   [<span data-ttu-id="12c7d-155">Polyline</span><span class="sxs-lookup"><span data-stu-id="12c7d-155">polyline</span></span>](#polyline)
-   [<span data-ttu-id="12c7d-156">curva</span><span class="sxs-lookup"><span data-stu-id="12c7d-156">curve</span></span>](#curve)
-   [<span data-ttu-id="12c7d-157">vería</span><span class="sxs-lookup"><span data-stu-id="12c7d-157">arc</span></span>](#arc)
-   [<span data-ttu-id="12c7d-158">Resumen</span><span class="sxs-lookup"><span data-stu-id="12c7d-158">Summary</span></span>](#summary)

## <a name="rect"></a><span data-ttu-id="12c7d-159">rect</span><span class="sxs-lookup"><span data-stu-id="12c7d-159">rect</span></span>

<span data-ttu-id="12c7d-160">Puede usar el `<rect>` elemento para dibujar un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="12c7d-160">You can use the `<rect>` element to draw a rectangle.</span></span> <span data-ttu-id="12c7d-161">Después, puede personalizar el rectángulo especificando distintos atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="12c7d-161">You can then customize the rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="12c7d-162">Por ejemplo, puede dibujar un rectángulo relleno con azul especificando **fillColor**= "Blue" y póngale un contorno rojo de 3,5 puntos especificando **StrokeColor**= "red" **strokeweight**= "3.5 PT", como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="12c7d-162">For example, you can draw a rectangle that is filled with blue by specifying **fillcolor**="blue", and give it a 3.5-point red outline by specifying **strokecolor**="red" **strokeweight**="3.5pt", as shown in the following VML representation:</span></span>

![rect1.gif (485 bytes)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





<span data-ttu-id="12c7d-164">Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="12c7d-164">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span> <span data-ttu-id="12c7d-165">(Nota: la especificación de VML no tiene un marcador para el `<rect>` elemento).</span><span class="sxs-lookup"><span data-stu-id="12c7d-165">(Note: The VML specification doesn't have a bookmark for the `<rect>` element.)</span></span>

<span data-ttu-id="12c7d-166">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="12c7d-166">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="roundrect"></a><span data-ttu-id="12c7d-167">roundrect</span><span class="sxs-lookup"><span data-stu-id="12c7d-167">roundrect</span></span>

<span data-ttu-id="12c7d-168">Puede usar el `<roundrect>` elemento para dibujar un rectángulo con esquinas redondeadas.</span><span class="sxs-lookup"><span data-stu-id="12c7d-168">You can use the `<roundrect>` element to draw a rectangle with rounded corners.</span></span> <span data-ttu-id="12c7d-169">Después, puede personalizar el rectángulo redondeado especificando distintos atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="12c7d-169">You can then customize the rounded rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="12c7d-170">Por ejemplo, puede dibujar un rectángulo con esquinas redondeadas del 30% de la mitad de la dimensión más pequeña del rectángulo mediante la especificación de la función de 0,3 "StrokeColor", para rellenarlo con amarillo; para ello, especifique **fillColor**= "Yellow" y asígnele un contorno rojo de 2 puntos especificando = "red" **strokeweight**= "2PT", como se muestra en la siguiente representación</span><span class="sxs-lookup"><span data-stu-id="12c7d-170">For example, you can draw a rectangle that has rounded corners 30% of half the smaller dimension of the rectangle by specifying **arcsize**="0.3", fill it with yellow by specifying **fillcolor**="yellow", and give it a 2-point red outline by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![roundrect1.gif (622 bytes)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="12c7d-172">Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="12c7d-172">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span>

<span data-ttu-id="12c7d-173">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="12c7d-173">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="line"></a><span data-ttu-id="12c7d-174">line</span><span class="sxs-lookup"><span data-stu-id="12c7d-174">line</span></span>

<span data-ttu-id="12c7d-175">Puede usar el `<line>` elemento para crear una línea recta.</span><span class="sxs-lookup"><span data-stu-id="12c7d-175">You can use the `<line>` element to create a straight line.</span></span> <span data-ttu-id="12c7d-176">Después, puede personalizar la línea especificando distintos atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="12c7d-176">You can then customize the line by specifying different property attributes.</span></span>

<span data-ttu-id="12c7d-177">Por ejemplo, puede dibujar una línea horizontal especificando **from**= "20 PT, 20 PT" **en**= "100pt, 20 PT" y conviértalo en 2 puntos y en rojo especificando **StrokeColor**= "red" **strokeweight**= "2PT", tal y como se muestra en la siguiente representación en VML:</span><span class="sxs-lookup"><span data-stu-id="12c7d-177">For example, you can draw a horizontal line by specifying **from**="20pt,20pt" **to**="100pt,20pt", and make it 2-point and red by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![line1.gif (88 bytes)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="12c7d-179">Puede dibujar una línea vertical o diagonal simplemente especificando valores diferentes para los atributos **de propiedad From** y **to** , tal y como se muestra en la siguiente representación VML:</span><span class="sxs-lookup"><span data-stu-id="12c7d-179">You can draw a vertical or diagonal line by simply specifying different values for the **from** and **to** property attributes, as shown in the following VML representation:</span></span>

![line2.gif (86 bytes)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="12c7d-181">Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span><span class="sxs-lookup"><span data-stu-id="12c7d-181">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span></span>

<span data-ttu-id="12c7d-182">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="12c7d-182">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="polyline"></a><span data-ttu-id="12c7d-183">Polyline</span><span class="sxs-lookup"><span data-stu-id="12c7d-183">polyline</span></span>

<span data-ttu-id="12c7d-184">Puede usar el `<polyline>` elemento para definir formas que se crean a partir de segmentos de línea conectados.</span><span class="sxs-lookup"><span data-stu-id="12c7d-184">You can use the `<polyline>` element to define shapes that are created from connected line segments.</span></span> <span data-ttu-id="12c7d-185">Después, puede personalizar la forma especificando distintos atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="12c7d-185">You can then customize the shape by specifying different property attributes.</span></span>

<span data-ttu-id="12c7d-186">Por ejemplo, para dibujar la forma que se muestra en la siguiente imagen, puede escribir la siguiente representación en VML:</span><span class="sxs-lookup"><span data-stu-id="12c7d-186">For example, to draw the shape shown in the following picture, you can type the following VML representation:</span></span>

![polyline1.gif (957 bytes)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="12c7d-188">Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span><span class="sxs-lookup"><span data-stu-id="12c7d-188">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span></span>

<span data-ttu-id="12c7d-189">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="12c7d-189">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="curve"></a><span data-ttu-id="12c7d-190">curva</span><span class="sxs-lookup"><span data-stu-id="12c7d-190">curve</span></span>

<span data-ttu-id="12c7d-191">Puede usar el `<curve>` elemento para dibujar una curva Bézier cúbica.</span><span class="sxs-lookup"><span data-stu-id="12c7d-191">You can use the `<curve>` element to draw a cubic bézier curve.</span></span> <span data-ttu-id="12c7d-192">Después, puede personalizar la curva especificando distintos atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="12c7d-192">You can then customize the curve by specifying different property attributes.</span></span>

<span data-ttu-id="12c7d-193">Por ejemplo, para dibujar una curva como se muestra en la siguiente imagen, puede escribir la siguiente representación en VML:</span><span class="sxs-lookup"><span data-stu-id="12c7d-193">For example, to draw a curve as shown in the following picture, you can type the following VML representation:</span></span>

![curve1.gif (992 bytes)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





<span data-ttu-id="12c7d-195">Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span><span class="sxs-lookup"><span data-stu-id="12c7d-195">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span></span>

<span data-ttu-id="12c7d-196">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="12c7d-196">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="arc"></a><span data-ttu-id="12c7d-197">arc</span><span class="sxs-lookup"><span data-stu-id="12c7d-197">arc</span></span>

<span data-ttu-id="12c7d-198">Puede usar el `<arc>` elemento para dibujar un arco que se define como un segmento de una elipse.</span><span class="sxs-lookup"><span data-stu-id="12c7d-198">You can use the `<arc>` element to draw an arc that is defined as a segment of an oval.</span></span> <span data-ttu-id="12c7d-199">El arco se define mediante la intersección de la elipse con los vectores de radio inicial y final dados por los ángulos.</span><span class="sxs-lookup"><span data-stu-id="12c7d-199">The arc is defined by the intersection of the oval with the start and end radius vectors given by the angles.</span></span> <span data-ttu-id="12c7d-200">Los ángulos se calculan mediante las propiedades de un círculo (ancho igual a alto) y, a continuación, se escalan de forma anisotrópico al ancho y el alto deseados.</span><span class="sxs-lookup"><span data-stu-id="12c7d-200">The angles are calculated by using the properties of a circle (width equal to height), then scaled anisotropically to the desired width and height.</span></span>

<span data-ttu-id="12c7d-201">Por ejemplo, puede dibujar un arco que empiece en 0 grados y termine en 90 grados especificando **startAngle**= "0" imponed = " **90",** como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="12c7d-201">For example, you can draw an arc that starts at 0 degrees and ends at 90 degrees by specifying **startangle**="0" **endangle**="90", as shown in the following VML representation:</span></span>

![arc1.gif (410 bytes)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="12c7d-203">Puede cambiar el arco especificando distintos valores de **startAngle** y  impuestos, tal y como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="12c7d-203">You can change the arc by specifying different **startangle** and **endangle** values, as shown in the following VML representation:</span></span>

![arc2.gif (608 bytes)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 bytes)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="12c7d-206">Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span><span class="sxs-lookup"><span data-stu-id="12c7d-206">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span></span>

<span data-ttu-id="12c7d-207">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="12c7d-207">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="12c7d-208">Resumen</span><span class="sxs-lookup"><span data-stu-id="12c7d-208">Summary</span></span>

<span data-ttu-id="12c7d-209">Puede usar elementos predefinidos de VML como `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` y `<arc>` para dibujar fácilmente gráficos en una página web y, a continuación, personalizar esos gráficos cambiando sus atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="12c7d-209">You can use VML predefined elements such as `<oval>`, `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` to easily draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span>

 

 