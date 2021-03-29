---
title: Colocar formas
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Web Workshop, colocar formas
- diseñar páginas web, colocar formas
- Lenguaje de marcado de vectores (VML), colocar formas
- VML (Lenguaje de marcado de vectores), colocar formas
- gráficos vectoriales, colocar formas
- Formas VML, posición
- colocar formas
- Lenguaje de marcado de vectores (VML), estilo de posición estática
- VML (Lenguaje de marcado de vectores), estilo de posición estática
- gráficos vectoriales, estilo de posición estática
- estilo de posición estática
- Lenguaje de marcado de vectores (VML), estilo de posición relativo
- VML (Lenguaje de marcado de vectores), estilo de posición relativo
- gráficos vectoriales, estilo de posición relativo
- estilo de posición relativa
- Lenguaje de marcado de vectores (VML), estilo de posición absoluta
- VML (Lenguaje de marcado de vectores), estilo de posición absoluta
- gráficos vectoriales, estilo de posición absoluta
- estilo de posición absoluta
- Lenguaje de marcado de vectores (VML), estilo de posición de índice z
- VML (Lenguaje de marcado de vectores), estilo de posición de índice z
- gráficos vectoriales, estilo de posición de índice z
- estilo de posición de índice z
- Lenguaje de marcado de vectores (VML), estilo de posición de giro
- VML (Lenguaje de marcado de vectores), estilo de posición de giro
- gráficos vectoriales, estilo de posición de giro
- estilo de posición de giro
- Lenguaje de marcado de vectores (VML), estilo de posición de volteo
- VML (Lenguaje de marcado de vectores), estilo de posición de volteo
- gráficos vectoriales, estilo de posición de volteo
- estilo de posición de volteo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8e01d0c7962467b1894f0f4c2c6cd1f6b01509
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077909"
---
# <a name="positioning-shapes"></a><span data-ttu-id="579ef-135">Colocar formas</span><span class="sxs-lookup"><span data-stu-id="579ef-135">Positioning Shapes</span></span>

<span data-ttu-id="579ef-136">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="579ef-136">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="579ef-137">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="579ef-137">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="579ef-138">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="579ef-138">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="579ef-139">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="579ef-139">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="579ef-140">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="579ef-140">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="579ef-141">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="579ef-141">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="579ef-142">Ha aprendido cómo dibujar y colorear formas en una página web mediante VML.</span><span class="sxs-lookup"><span data-stu-id="579ef-142">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="579ef-143">En este tema, usará VML para colocar los gráficos de forma precisa en una página web.</span><span class="sxs-lookup"><span data-stu-id="579ef-143">In this topic, you'll use VML to precisely position graphics on a Web page.</span></span>

<span data-ttu-id="579ef-144">VML usa la misma sintaxis definida en las secciones [modelo de cuadro](https://www.w3.org/TR/PR-CSS2/box.mdl) y modelo de [representación visual](https://www.w3.org/TR/PR-CSS2/visuren.mdl) de [CSS2](https://www.w3.org/TR/PR-CSS2/) para colocar formas en una página web.</span><span class="sxs-lookup"><span data-stu-id="579ef-144">VML uses the same syntax defined in the [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) and [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) sections of [CSS2](https://www.w3.org/TR/PR-CSS2/) to position shapes on a Web page.</span></span> <span data-ttu-id="579ef-145">Puede utilizar [static](#static), [relative](#relative)o [Absolute](#absolute) para determinar dónde se encuentra el punto base en una página web.</span><span class="sxs-lookup"><span data-stu-id="579ef-145">You can use [static](#static), [relative](#relative), or [absolute](#absolute) to determine where the base point is located on a Web page.</span></span> <span data-ttu-id="579ef-146">Después, puede usar los atributos de estilo **superior** e **izquierdo** para especificar el desplazamiento desde el punto base en el que se colocará el cuadro contenedor de la forma.</span><span class="sxs-lookup"><span data-stu-id="579ef-146">You can then use the **top** and **left** style attributes to specify the offset from the base point at which the containing box for the shape will be positioned.</span></span>

<span data-ttu-id="579ef-147">También puede utilizar [z-index](#z-index) para especificar el orden z de las formas en una página web.</span><span class="sxs-lookup"><span data-stu-id="579ef-147">You can also use [z-index](#z-index) to specify the z-order of shapes on a Web page.</span></span>

<span data-ttu-id="579ef-148">Además, VML proporciona [rotación](#rotation) y [volteo](#flip) para girar o voltear formas.</span><span class="sxs-lookup"><span data-stu-id="579ef-148">In addition, VML provides [rotation](#rotation) and [flip](#flip) to rotate or flip shapes.</span></span>

<span data-ttu-id="579ef-149">En este tema:</span><span class="sxs-lookup"><span data-stu-id="579ef-149">In this topic:</span></span>

-   [<span data-ttu-id="579ef-150">static</span><span class="sxs-lookup"><span data-stu-id="579ef-150">static</span></span>](#static)
-   [<span data-ttu-id="579ef-151">relative</span><span class="sxs-lookup"><span data-stu-id="579ef-151">relative</span></span>](#relative)
-   [<span data-ttu-id="579ef-152">absolute</span><span class="sxs-lookup"><span data-stu-id="579ef-152">absolute</span></span>](#absolute)
-   [<span data-ttu-id="579ef-153">índice z</span><span class="sxs-lookup"><span data-stu-id="579ef-153">z-index</span></span>](#z-index)
-   [<span data-ttu-id="579ef-154">Rotation</span><span class="sxs-lookup"><span data-stu-id="579ef-154">rotation</span></span>](#rotation)
-   [<span data-ttu-id="579ef-155">flip</span><span class="sxs-lookup"><span data-stu-id="579ef-155">flip</span></span>](#flip)
-   [<span data-ttu-id="579ef-156">Resumen</span><span class="sxs-lookup"><span data-stu-id="579ef-156">Summary</span></span>](#summary)

## <a name="static"></a><span data-ttu-id="579ef-157">static</span><span class="sxs-lookup"><span data-stu-id="579ef-157">static</span></span>

<span data-ttu-id="579ef-158">El estilo de posición predeterminado es estático, que indica a los exploradores que coloquen la forma en el punto actual (el punto base) en el flujo de texto y omitan los valores de los atributos de estilo **superior** e **izquierdo** .</span><span class="sxs-lookup"><span data-stu-id="579ef-158">The default position style is static, which instructs browsers to position the shape at the current point (the base point) in the text flow and ignore the settings in the **top** and **left** style attributes.</span></span>

<span data-ttu-id="579ef-159">Por ejemplo, en la siguiente representación VML, el óvalo rojo se coloca inmediatamente después del texto "Inicio de la forma:", tal como se muestra en la siguiente imagen:</span><span class="sxs-lookup"><span data-stu-id="579ef-159">For example, in the following VML representation, the red oval is positioned immediately after the text "Beginning of the shape:", as shown in the following picture:</span></span>

![\-ps.gif shape1 (2123 bytes)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="579ef-161">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="579ef-161">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="relative"></a><span data-ttu-id="579ef-162">relative</span><span class="sxs-lookup"><span data-stu-id="579ef-162">relative</span></span>

<span data-ttu-id="579ef-163">Establecer el atributo de estilo de posición en "Relative" permite colocar el cuadro contenedor con un desplazamiento desde el punto actual (el punto base) en el flujo de texto.</span><span class="sxs-lookup"><span data-stu-id="579ef-163">Setting the position style attribute to "relative" allows you to place the containing box with an offset from the current point (the base point) in the text flow.</span></span> <span data-ttu-id="579ef-164">El desplazamiento viene determinado por los valores de los atributos de estilo **superior** e **izquierdo** .</span><span class="sxs-lookup"><span data-stu-id="579ef-164">The offset is determined by the settings in the **top** and **left** style attributes.</span></span> <span data-ttu-id="579ef-165">Tenga en cuenta que el cuadro contenedor que se coloca como relativo ocupa espacio en el flujo de texto.</span><span class="sxs-lookup"><span data-stu-id="579ef-165">Be aware that the containing box that is positioned as relative takes up space in the text flow.</span></span>

<span data-ttu-id="579ef-166">Por ejemplo, en la siguiente representación VML, el óvalo rojo se coloca 20 puntos desde la izquierda y 10 puntos desde la parte superior respecto al punto actual en el flujo de texto, tal como se muestra en la siguiente imagen:</span><span class="sxs-lookup"><span data-stu-id="579ef-166">For example, in the following VML representation, the red oval is positioned 20 points from the left and 10 points from the top relative to the current point in the text flow, as shown in the following picture:</span></span>

![shape3.gif (2048 bytes)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="579ef-168">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="579ef-168">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="absolute"></a><span data-ttu-id="579ef-169">absolute</span><span class="sxs-lookup"><span data-stu-id="579ef-169">absolute</span></span>

<span data-ttu-id="579ef-170">Al establecer el atributo de estilo de posición en "Absolute", se puede colocar el cuadro contenedor en una distancia exacta desde la esquina superior izquierda (el punto base) de su elemento primario (el elemento colocado que contiene la forma).</span><span class="sxs-lookup"><span data-stu-id="579ef-170">Setting the position style attribute to "absolute" allows you to place the containing box an exact distance from the top left corner (the base point) of its parent element (the positioned element that contains the shape).</span></span> <span data-ttu-id="579ef-171">Tenga en cuenta que el cuadro contenedor que se coloca como absoluto no ocupa espacio en el flujo de texto.</span><span class="sxs-lookup"><span data-stu-id="579ef-171">Be aware that the containing box that is positioned as absolute doesn't take up space in the text flow.</span></span>

<span data-ttu-id="579ef-172">Por ejemplo, en la siguiente representación VML, el óvalo rojo está contenido dentro del `<body>` elemento (toda la página web); por lo tanto, el punto base se encuentra en la esquina superior izquierda de la Página Web.</span><span class="sxs-lookup"><span data-stu-id="579ef-172">For example, in the following VML representation, the red oval is contained within the `<body>` element (the entire Web page); therefore, the base point is at the top left corner of the Web page.</span></span> <span data-ttu-id="579ef-173">El cuadro contenedor del óvalo está colocado exactamente 20 puntos desde la izquierda y 10 puntos desde la parte superior, con respecto a la esquina superior izquierda de la página web, como se muestra en la siguiente imagen:</span><span class="sxs-lookup"><span data-stu-id="579ef-173">The containing box for the oval is positioned exactly 20 points from the left and 10 points from the top, relative to the top left corner of the Web page, as shown in the following picture:</span></span>

![shape2.gif (2006 bytes)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="579ef-175">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="579ef-175">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="z-index"></a><span data-ttu-id="579ef-176">z-index</span><span class="sxs-lookup"><span data-stu-id="579ef-176">z-index</span></span>

<span data-ttu-id="579ef-177">Es posible colocar una forma que se solape con otra forma.</span><span class="sxs-lookup"><span data-stu-id="579ef-177">It is possible to position a shape that overlaps another shape.</span></span> <span data-ttu-id="579ef-178">Normalmente, el gráfico que aparece en último lugar en el código HTML aparece en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="579ef-178">Normally, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="579ef-179">En VML, puede controlar el orden z mediante el atributo de estilo **z-index** .</span><span class="sxs-lookup"><span data-stu-id="579ef-179">In VML, you can control the z-order by using the **z-index** style attribute.</span></span> <span data-ttu-id="579ef-180">El valor de este atributo puede ser cero, un entero positivo o un entero negativo.</span><span class="sxs-lookup"><span data-stu-id="579ef-180">The value of this attribute can be zero, a positive integer, or a negative integer.</span></span> <span data-ttu-id="579ef-181">El gráfico que tiene un valor de índice z mayor se muestra en la parte superior del gráfico que tiene un valor de índice z más pequeño.</span><span class="sxs-lookup"><span data-stu-id="579ef-181">The graphic that has a larger z-index value is displayed on top of the graphic that has a smaller z-index value.</span></span> <span data-ttu-id="579ef-182">Cuando ambos gráficos tienen el mismo valor de índice z, el gráfico que aparece en último lugar en el código HTML aparece en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="579ef-182">When both graphics have the same z-index value, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="579ef-183">Por ejemplo, en la siguiente representación VML, el óvalo rojo se muestra en la parte superior del rectángulo azul.</span><span class="sxs-lookup"><span data-stu-id="579ef-183">For example, in the following VML representation, the red oval is displayed on top of the blue rectangle.</span></span> <span data-ttu-id="579ef-184">Esto se debe a que el valor de índice z del óvalo rojo es mayor que el valor de índice z del rectángulo azul.</span><span class="sxs-lookup"><span data-stu-id="579ef-184">This is because the z-index value of the red oval is greater than the z-index value of the blue rectangle.</span></span>

![shape4.gif (572 bytes)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





<span data-ttu-id="579ef-186">Si cambia el índice z, tal y como se muestra en la siguiente representación VML, el óvalo rojo se moverá detrás del rectángulo azul.</span><span class="sxs-lookup"><span data-stu-id="579ef-186">If you change the z-index, as shown in the following VML representation, the red oval would move behind the blue rectangle.</span></span>

![shape5.gif (469 bytes)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





<span data-ttu-id="579ef-188">Si proporciona un entero negativo, puede usar el índice z para colocar los gráficos detrás del flujo de texto normal, tal como se muestra en la siguiente representación de VML.</span><span class="sxs-lookup"><span data-stu-id="579ef-188">If you supply a negative integer, you can use z-index to position graphics behind the normal text flow, as shown in the following VML representation.</span></span>

![shape6.gif (2125 bytes)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="579ef-190">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="579ef-190">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rotation"></a><span data-ttu-id="579ef-191">giro</span><span class="sxs-lookup"><span data-stu-id="579ef-191">rotation</span></span>

<span data-ttu-id="579ef-192">Puede usar el atributo de estilo de **rotación** para especificar el número de grados que desea que una forma Active su eje.</span><span class="sxs-lookup"><span data-stu-id="579ef-192">You can use the **rotation** style attribute to specify how many degrees you want a shape to turn on its axis.</span></span> <span data-ttu-id="579ef-193">Un valor positivo indica un giro en el sentido de las agujas del reloj; un valor negativo indica un giro en el sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="579ef-193">A positive value indicates a clockwise rotation; a negative value indicates a counter-clockwise rotation.</span></span>

<span data-ttu-id="579ef-194">Por ejemplo, si especifica **Style**= '... rotación: 90 ', puede girar la forma 90 grados en el sentido de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="579ef-194">For example, if you specify **style**='... rotation:90', you can rotate the shape 90 degrees clockwise.</span></span>

<span data-ttu-id="579ef-195">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="579ef-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="flip"></a><span data-ttu-id="579ef-196">voltear</span><span class="sxs-lookup"><span data-stu-id="579ef-196">flip</span></span>

<span data-ttu-id="579ef-197">Puede usar el atributo de estilo **Flip** para voltear una forma en su eje x o y según la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="579ef-197">You can use the **flip** style attribute to flip a shape on its x or y axis according to the following table:</span></span>



| <span data-ttu-id="579ef-198">Value</span><span class="sxs-lookup"><span data-stu-id="579ef-198">Value</span></span> | <span data-ttu-id="579ef-199">Descripción</span><span class="sxs-lookup"><span data-stu-id="579ef-199">Description</span></span>                                                  |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="579ef-200">x</span><span class="sxs-lookup"><span data-stu-id="579ef-200">x</span></span>     | <span data-ttu-id="579ef-201">Voltear la forma girada sobre el eje y (invertir coordenadas x)</span><span class="sxs-lookup"><span data-stu-id="579ef-201">Flip the rotated shape about the y axis (invert x ordinates)</span></span> |
| <span data-ttu-id="579ef-202">y</span><span class="sxs-lookup"><span data-stu-id="579ef-202">y</span></span>     | <span data-ttu-id="579ef-203">Voltear la forma girada sobre el eje x (invertir las coordenadas y)</span><span class="sxs-lookup"><span data-stu-id="579ef-203">Flip the rotated shape about the x axis (invert y ordinates)</span></span> |



 

<span data-ttu-id="579ef-204">Tanto x como y se pueden especificar en la propiedad flip.</span><span class="sxs-lookup"><span data-stu-id="579ef-204">Both x and y may be specified in the flip property.</span></span>

<span data-ttu-id="579ef-205">Por ejemplo, si escribe **Style**= '... Flip: x y ', se volteará la forma en el eje x e y.</span><span class="sxs-lookup"><span data-stu-id="579ef-205">For example, if you type **style**='... flip:x y', you will flip the shape on both its x and y axis.</span></span>

<span data-ttu-id="579ef-206">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="579ef-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="579ef-207">Resumen</span><span class="sxs-lookup"><span data-stu-id="579ef-207">Summary</span></span>

<span data-ttu-id="579ef-208">En función de lo que haya aprendido, puede colocar una forma con precisión en una página web siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="579ef-208">Based on what you've learned, you can precisely position a shape on a Web page by following these steps:</span></span>

1.  <span data-ttu-id="579ef-209">Decida dónde desea que aparezca la forma en una página web y el tamaño de la forma.</span><span class="sxs-lookup"><span data-stu-id="579ef-209">Decide where you want the shape to appear on a Web page, and the size of the shape.</span></span>
2.  <span data-ttu-id="579ef-210">Especifique **Style**= ' Position: relative (o Relative) ' para determinar el punto base.</span><span class="sxs-lookup"><span data-stu-id="579ef-210">Specify **style**='position:relative (or relative)' to determine the base point.</span></span>
3.  <span data-ttu-id="579ef-211">Use **left** y **Top** para especificar el desplazamiento desde el punto base.</span><span class="sxs-lookup"><span data-stu-id="579ef-211">Use **left** and **top** to specify the offset from the base point.</span></span>
4.  <span data-ttu-id="579ef-212">Use **ancho** y **alto** para especificar el tamaño del cuadro contenedor de la forma.</span><span class="sxs-lookup"><span data-stu-id="579ef-212">Use **width** and **height** to specify the size of the containing box for the shape.</span></span>
5.  <span data-ttu-id="579ef-213">Utilice **z-index** para especificar el orden z de la forma.</span><span class="sxs-lookup"><span data-stu-id="579ef-213">Use **z-index** to specify the z-order of the shape.</span></span>

 

 