---
title: Usar formas predefinidas
description: En este artículo se describe el uso de formas predefinidas en VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Taller web, formas predefinidas
- diseñar páginas web, formas predefinidas
- Lenguaje de marcado de vectores (VML), formas predefinidas
- VML (Lenguaje de marcado de vectores), formas predefinidas
- gráficos vectoriales, formas predefinidas
- Formas de VML predefinidas
- formas predefinidas
- Lenguaje de marcado de vectores (VML), elemento rect
- VML (Lenguaje de marcado de vectores), elemento rect
- vector graphics,rect element
- elemento rect
- Elementos VML, rect
- Lenguaje de marcado de vectores (VML), elemento roundrect
- VML (Lenguaje de marcado de vectores), elemento roundrect
- vector graphics,roundrect element
- roundrect, elemento
- Elementos VML,roundrect
- Lenguaje de marcado de vectores (VML),elemento line
- VML (Lenguaje de marcado de vectores),elemento line
- gráficos vectoriales, elemento de línea
- elemento line
- Elementos de VML, línea
- Lenguaje de marcado de vectores (VML), elemento de polilínea
- VML (Lenguaje de marcado de vectores),elemento de polilínea
- gráficos vectoriales, elemento de polilínea
- elemento de polilínea
- Elementos vml, polilínea
- Lenguaje de marcado de vectores (VML),elemento curve
- VML (Lenguaje de marcado de vectores),elemento curve
- gráficos vectoriales, elemento de curva
- elemento curve
- Elementos de VML, curva
- Lenguaje de marcado de vectores (VML),elemento arc
- VML (Lenguaje de marcado de vectores),arc element
- vector graphics,arc element
- arc, elemento
- Elementos de VML, arc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b410cf288a3ba63e4c1d745fd962a445b0b220b8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407688"
---
# <a name="using-predefined-shapes"></a><span data-ttu-id="0ee31-140">Usar formas predefinidas</span><span class="sxs-lookup"><span data-stu-id="0ee31-140">Using Predefined Shapes</span></span>

<span data-ttu-id="0ee31-141">En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0ee31-141">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0ee31-142">Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="0ee31-142">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0ee31-143">A partir de diciembre de 2011, este tema se archivó.</span><span class="sxs-lookup"><span data-stu-id="0ee31-143">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0ee31-144">Como resultado, ya no se mantiene activamente.</span><span class="sxs-lookup"><span data-stu-id="0ee31-144">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0ee31-145">Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="0ee31-145">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0ee31-146">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0ee31-146">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0ee31-147">Como ha aprendido, puede usar el elemento `<oval>` de VML para crear un óvalo simple.</span><span class="sxs-lookup"><span data-stu-id="0ee31-147">As you've learned, you can use the `<oval>` element of VML to create a simple oval.</span></span> <span data-ttu-id="0ee31-148">VML proporciona otros elementos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="0ee31-148">VML provides several other predefined elements.</span></span> <span data-ttu-id="0ee31-149">En este tema, se ilustrará cómo dibujar gráficos mediante estos elementos.</span><span class="sxs-lookup"><span data-stu-id="0ee31-149">In this topic, we will illustrate how to draw graphics by using these elements.</span></span>

<span data-ttu-id="0ee31-150">En este tema:</span><span class="sxs-lookup"><span data-stu-id="0ee31-150">In this topic:</span></span>

-   [<span data-ttu-id="0ee31-151">Rect</span><span class="sxs-lookup"><span data-stu-id="0ee31-151">rect</span></span>](#roundrect)
-   [<span data-ttu-id="0ee31-152">roundrect</span><span class="sxs-lookup"><span data-stu-id="0ee31-152">roundrect</span></span>](#roundrect)
-   [<span data-ttu-id="0ee31-153">line</span><span class="sxs-lookup"><span data-stu-id="0ee31-153">line</span></span>](#polyline)
-   [<span data-ttu-id="0ee31-154">Polilínea</span><span class="sxs-lookup"><span data-stu-id="0ee31-154">polyline</span></span>](#polyline)
-   [<span data-ttu-id="0ee31-155">curva</span><span class="sxs-lookup"><span data-stu-id="0ee31-155">curve</span></span>](#curve)
-   [<span data-ttu-id="0ee31-156">Arco</span><span class="sxs-lookup"><span data-stu-id="0ee31-156">arc</span></span>](#arc)
-   [<span data-ttu-id="0ee31-157">Resumen</span><span class="sxs-lookup"><span data-stu-id="0ee31-157">Summary</span></span>](#summary)

## <a name="rect"></a><span data-ttu-id="0ee31-158">rect</span><span class="sxs-lookup"><span data-stu-id="0ee31-158">rect</span></span>

<span data-ttu-id="0ee31-159">Puede usar el elemento `<rect>` para dibujar un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="0ee31-159">You can use the `<rect>` element to draw a rectangle.</span></span> <span data-ttu-id="0ee31-160">A continuación, puede personalizar el rectángulo especificando atributos de propiedad diferentes.</span><span class="sxs-lookup"><span data-stu-id="0ee31-160">You can then customize the rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="0ee31-161">Por ejemplo, puede dibujar un rectángulo que se rellena con azul especificando **fillcolor**="blue" y darle un contorno rojo de 3,5 puntos especificando **strokecolor**="red" **strokeweight**="3.5pt", como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="0ee31-161">For example, you can draw a rectangle that is filled with blue by specifying **fillcolor**="blue", and give it a 3.5-point red outline by specifying **strokecolor**="red" **strokeweight**="3.5pt", as shown in the following VML representation:</span></span>

![rect1.gif (485 bytes)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





<span data-ttu-id="0ee31-163">Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="0ee31-163">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span> <span data-ttu-id="0ee31-164">(Nota: La especificación de VML no tiene un marcador para el `<rect>` elemento).</span><span class="sxs-lookup"><span data-stu-id="0ee31-164">(Note: The VML specification doesn't have a bookmark for the `<rect>` element.)</span></span>

<span data-ttu-id="0ee31-165">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="0ee31-165">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="roundrect"></a><span data-ttu-id="0ee31-166">roundrect</span><span class="sxs-lookup"><span data-stu-id="0ee31-166">roundrect</span></span>

<span data-ttu-id="0ee31-167">Puede usar el elemento `<roundrect>` para dibujar un rectángulo con esquinas redondeadas.</span><span class="sxs-lookup"><span data-stu-id="0ee31-167">You can use the `<roundrect>` element to draw a rectangle with rounded corners.</span></span> <span data-ttu-id="0ee31-168">A continuación, puede personalizar el rectángulo redondeado especificando atributos de propiedad diferentes.</span><span class="sxs-lookup"><span data-stu-id="0ee31-168">You can then customize the rounded rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="0ee31-169">Por ejemplo, puede dibujar un rectángulo que tenga esquinas redondeadas al 30 % de la mitad de la dimensión más pequeña del rectángulo especificando **arcsize**="0.3", rellenarlo con amarillo especificando **fillcolor**="yellow" y darle un contorno rojo de 2 puntos especificando **strokecolor**="red" **strokeweight**="2pt", como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="0ee31-169">For example, you can draw a rectangle that has rounded corners 30% of half the smaller dimension of the rectangle by specifying **arcsize**="0.3", fill it with yellow by specifying **fillcolor**="yellow", and give it a 2-point red outline by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![roundrect1.gif (622 bytes)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="0ee31-171">Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="0ee31-171">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span>

<span data-ttu-id="0ee31-172">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="0ee31-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="line"></a><span data-ttu-id="0ee31-173">line</span><span class="sxs-lookup"><span data-stu-id="0ee31-173">line</span></span>

<span data-ttu-id="0ee31-174">Puede usar el elemento `<line>` para crear una línea recta.</span><span class="sxs-lookup"><span data-stu-id="0ee31-174">You can use the `<line>` element to create a straight line.</span></span> <span data-ttu-id="0ee31-175">A continuación, puede personalizar la línea especificando atributos de propiedad diferentes.</span><span class="sxs-lookup"><span data-stu-id="0ee31-175">You can then customize the line by specifying different property attributes.</span></span>

<span data-ttu-id="0ee31-176">Por ejemplo, puede dibujar una línea horizontal especificando de ="20pt,20pt" a ="100pt,20pt", y hacerlo de 2 puntos y rojo especificando **strokecolor**="red" **strokeweight**="2pt", como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="0ee31-176">For example, you can draw a horizontal line by specifying **from**="20pt,20pt" **to**="100pt,20pt", and make it 2-point and red by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![line1.gif (88 bytes)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="0ee31-178">Puede dibujar una línea vertical o diagonal simplemente  especificando valores diferentes para los atributos de propiedad from y **to,** como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="0ee31-178">You can draw a vertical or diagonal line by simply specifying different values for the **from** and **to** property attributes, as shown in the following VML representation:</span></span>

![line2.gif (86 bytes)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="0ee31-180">Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span><span class="sxs-lookup"><span data-stu-id="0ee31-180">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span></span>

<span data-ttu-id="0ee31-181">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="0ee31-181">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="polyline"></a><span data-ttu-id="0ee31-182">Polilínea</span><span class="sxs-lookup"><span data-stu-id="0ee31-182">polyline</span></span>

<span data-ttu-id="0ee31-183">Puede usar el elemento para definir formas que se crean a partir `<polyline>` de segmentos de línea conectados.</span><span class="sxs-lookup"><span data-stu-id="0ee31-183">You can use the `<polyline>` element to define shapes that are created from connected line segments.</span></span> <span data-ttu-id="0ee31-184">A continuación, puede personalizar la forma especificando atributos de propiedad diferentes.</span><span class="sxs-lookup"><span data-stu-id="0ee31-184">You can then customize the shape by specifying different property attributes.</span></span>

<span data-ttu-id="0ee31-185">Por ejemplo, para dibujar la forma que se muestra en la siguiente imagen, puede escribir la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="0ee31-185">For example, to draw the shape shown in the following picture, you can type the following VML representation:</span></span>

![polyline1.gif (957 bytes)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="0ee31-187">Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span><span class="sxs-lookup"><span data-stu-id="0ee31-187">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span></span>

<span data-ttu-id="0ee31-188">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="0ee31-188">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="curve"></a><span data-ttu-id="0ee31-189">curva</span><span class="sxs-lookup"><span data-stu-id="0ee31-189">curve</span></span>

<span data-ttu-id="0ee31-190">Puede usar el elemento `<curve>` para dibujar una curva bézier cúbica.</span><span class="sxs-lookup"><span data-stu-id="0ee31-190">You can use the `<curve>` element to draw a cubic bézier curve.</span></span> <span data-ttu-id="0ee31-191">A continuación, puede personalizar la curva especificando atributos de propiedad diferentes.</span><span class="sxs-lookup"><span data-stu-id="0ee31-191">You can then customize the curve by specifying different property attributes.</span></span>

<span data-ttu-id="0ee31-192">Por ejemplo, para dibujar una curva como se muestra en la siguiente imagen, puede escribir la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="0ee31-192">For example, to draw a curve as shown in the following picture, you can type the following VML representation:</span></span>

![curve1.gif (992 bytes)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





<span data-ttu-id="0ee31-194">Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span><span class="sxs-lookup"><span data-stu-id="0ee31-194">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span></span>

<span data-ttu-id="0ee31-195">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="0ee31-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="arc"></a><span data-ttu-id="0ee31-196">arc</span><span class="sxs-lookup"><span data-stu-id="0ee31-196">arc</span></span>

<span data-ttu-id="0ee31-197">Puede usar el elemento `<arc>` para dibujar un arco que se define como un segmento de un óvalo.</span><span class="sxs-lookup"><span data-stu-id="0ee31-197">You can use the `<arc>` element to draw an arc that is defined as a segment of an oval.</span></span> <span data-ttu-id="0ee31-198">El arco se define mediante la intersección del óvalo con los vectores de radio inicial y final especificados por los ángulos.</span><span class="sxs-lookup"><span data-stu-id="0ee31-198">The arc is defined by the intersection of the oval with the start and end radius vectors given by the angles.</span></span> <span data-ttu-id="0ee31-199">Los ángulos se calculan mediante las propiedades de un círculo (ancho igual a alto) y, a continuación, se escalan anisotropíamente hasta el ancho y alto deseados.</span><span class="sxs-lookup"><span data-stu-id="0ee31-199">The angles are calculated by using the properties of a circle (width equal to height), then scaled anisotropically to the desired width and height.</span></span>

<span data-ttu-id="0ee31-200">Por ejemplo, puede dibujar un arco que comience a 0 grados y termine en 90 grados especificando **startangle**="0" **endangle**="90", como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="0ee31-200">For example, you can draw an arc that starts at 0 degrees and ends at 90 degrees by specifying **startangle**="0" **endangle**="90", as shown in the following VML representation:</span></span>

![arc1.gif (410 bytes)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="0ee31-202">Puede cambiar el arco especificando diferentes valores **startangle** y **endangle,** como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="0ee31-202">You can change the arc by specifying different **startangle** and **endangle** values, as shown in the following VML representation:</span></span>

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





<span data-ttu-id="0ee31-205">Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span><span class="sxs-lookup"><span data-stu-id="0ee31-205">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span></span>

<span data-ttu-id="0ee31-206">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="0ee31-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="0ee31-207">Resumen</span><span class="sxs-lookup"><span data-stu-id="0ee31-207">Summary</span></span>

<span data-ttu-id="0ee31-208">Puede usar elementos predefinidos de VML como , , , , , , y para dibujar gráficos fácilmente en una página web y, a continuación, personalizar esos gráficos simplemente cambiando sus atributos `<oval>` `<line>` de `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` propiedad.</span><span class="sxs-lookup"><span data-stu-id="0ee31-208">You can use VML predefined elements such as `<oval>`, `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` to easily draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span>

 

 