---
title: Formas de posicionamiento
description: En este artículo se describe el posicionamiento de formas en VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Taller web, colocación de formas
- diseñar páginas web, colocar formas
- Lenguaje de marcado de vectores (VML),formas de posicionamiento
- VML (Lenguaje de marcado de vectores), formas de posicionamiento
- gráficos vectoriales, formas de posicionamiento
- Formas de VML, posicionamiento
- formas de posicionamiento
- Lenguaje de marcado de vectores (VML), estilo de posición estática
- VML (Lenguaje de marcado de vectores), estilo de posición estática
- gráficos vectoriales, estilo de posición estática
- estilo de posición estática
- Lenguaje de marcado de vectores (VML), estilo de posición relativa
- VML (Lenguaje de marcado de vectores), estilo de posición relativa
- gráficos vectoriales, estilo de posición relativa
- estilo de posición relativa
- Lenguaje de marcado de vectores (VML), estilo de posición absoluta
- VML (Lenguaje de marcado de vectores), estilo de posición absoluta
- gráficos vectoriales, estilo de posición absoluta
- estilo de posición absoluta
- Lenguaje de marcado de vectores (VML), estilo de posición de índice z
- VML (Lenguaje de marcado de vectores), estilo de posición de índice z
- gráficos vectoriales, estilo de posición de índice z
- Estilo de posición de índice z
- Lenguaje de marcado de vectores (VML), estilo de posición de rotación
- VML (Lenguaje de marcado de vectores), estilo de posición de rotación
- gráficos vectoriales, estilo de posición de rotación
- estilo de posición de rotación
- Lenguaje de marcado de vectores (VML), estilo de posición de volteo
- VML (Lenguaje de marcado de vectores), estilo de posición de volteo
- gráficos vectoriales, estilo de posición de volteo
- estilo de posición de volteo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c96a8de891ed1bbd1b9bfee9eff52ede946247b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407718"
---
# <a name="positioning-shapes"></a><span data-ttu-id="9bbdb-134">Formas de posicionamiento</span><span class="sxs-lookup"><span data-stu-id="9bbdb-134">Positioning Shapes</span></span>

<span data-ttu-id="9bbdb-135">En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-135">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9bbdb-136">Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-136">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9bbdb-137">A partir de diciembre de 2011, este tema se archivó.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-137">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9bbdb-138">Como resultado, ya no se mantiene activamente.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-138">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9bbdb-139">Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="9bbdb-139">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9bbdb-140">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9bbdb-140">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9bbdb-141">Ha aprendido a dibujar y colorear formas en una página web mediante VML.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-141">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="9bbdb-142">En este tema, usará VML para colocar con precisión los gráficos en una página web.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-142">In this topic, you'll use VML to precisely position graphics on a Web page.</span></span>

<span data-ttu-id="9bbdb-143">VML usa la misma sintaxis definida en las secciones [Modelo de Box](https://www.w3.org/TR/PR-CSS2/box.mdl) y Modelo de Representación [visual](https://www.w3.org/TR/PR-CSS2/visuren.mdl) de [CSS2](https://www.w3.org/TR/PR-CSS2/) para colocar formas en una página web.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-143">VML uses the same syntax defined in the [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) and [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) sections of [CSS2](https://www.w3.org/TR/PR-CSS2/) to position shapes on a Web page.</span></span> <span data-ttu-id="9bbdb-144">Puede usar [estáticos,](#static) [relativos](#relative)o [absolutos](#absolute) para determinar dónde se encuentra el punto base en una página web.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-144">You can use [static](#static), [relative](#relative), or [absolute](#absolute) to determine where the base point is located on a Web page.</span></span> <span data-ttu-id="9bbdb-145">A continuación, puede  usar **los** atributos de estilo superior e izquierdo para especificar el desplazamiento desde el punto base en el que se colocará el cuadro de contenido de la forma.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-145">You can then use the **top** and **left** style attributes to specify the offset from the base point at which the containing box for the shape will be positioned.</span></span>

<span data-ttu-id="9bbdb-146">También puede usar [z-index para](#z-index) especificar el orden Z de las formas en una página web.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-146">You can also use [z-index](#z-index) to specify the z-order of shapes on a Web page.</span></span>

<span data-ttu-id="9bbdb-147">Además, VML proporciona rotación [y](#rotation) [volteo para](#flip) girar o voltear formas.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-147">In addition, VML provides [rotation](#rotation) and [flip](#flip) to rotate or flip shapes.</span></span>

<span data-ttu-id="9bbdb-148">En este tema:</span><span class="sxs-lookup"><span data-stu-id="9bbdb-148">In this topic:</span></span>

-   [<span data-ttu-id="9bbdb-149">static</span><span class="sxs-lookup"><span data-stu-id="9bbdb-149">static</span></span>](#static)
-   [<span data-ttu-id="9bbdb-150">relative</span><span class="sxs-lookup"><span data-stu-id="9bbdb-150">relative</span></span>](#relative)
-   [<span data-ttu-id="9bbdb-151">absolute</span><span class="sxs-lookup"><span data-stu-id="9bbdb-151">absolute</span></span>](#absolute)
-   [<span data-ttu-id="9bbdb-152">z-index</span><span class="sxs-lookup"><span data-stu-id="9bbdb-152">z-index</span></span>](#z-index)
-   [<span data-ttu-id="9bbdb-153">Rotación</span><span class="sxs-lookup"><span data-stu-id="9bbdb-153">rotation</span></span>](#rotation)
-   [<span data-ttu-id="9bbdb-154">flip</span><span class="sxs-lookup"><span data-stu-id="9bbdb-154">flip</span></span>](#flip)
-   [<span data-ttu-id="9bbdb-155">Resumen</span><span class="sxs-lookup"><span data-stu-id="9bbdb-155">Summary</span></span>](#summary)

## <a name="static"></a><span data-ttu-id="9bbdb-156">static</span><span class="sxs-lookup"><span data-stu-id="9bbdb-156">static</span></span>

<span data-ttu-id="9bbdb-157">El estilo de posición predeterminado es estático, que indica a los exploradores que coloquen la forma  en  el punto actual (el punto base) en el flujo de texto y omitan la configuración de los atributos de estilo superior e izquierdo.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-157">The default position style is static, which instructs browsers to position the shape at the current point (the base point) in the text flow and ignore the settings in the **top** and **left** style attributes.</span></span>

<span data-ttu-id="9bbdb-158">Por ejemplo, en la siguiente representación de VML, el óvalo rojo se coloca inmediatamente después del texto "Principio de la forma:", como se muestra en la siguiente imagen:</span><span class="sxs-lookup"><span data-stu-id="9bbdb-158">For example, in the following VML representation, the red oval is positioned immediately after the text "Beginning of the shape:", as shown in the following picture:</span></span>

![shape1 \-ps.gif (2123 bytes)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="9bbdb-160">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="9bbdb-160">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="relative"></a><span data-ttu-id="9bbdb-161">relative</span><span class="sxs-lookup"><span data-stu-id="9bbdb-161">relative</span></span>

<span data-ttu-id="9bbdb-162">Establecer el atributo de estilo de posición en "relativo" permite colocar el cuadro de contenido con un desplazamiento desde el punto actual (el punto base) en el flujo de texto.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-162">Setting the position style attribute to "relative" allows you to place the containing box with an offset from the current point (the base point) in the text flow.</span></span> <span data-ttu-id="9bbdb-163">El desplazamiento viene determinado por la configuración de los **atributos de** estilo superior **e** izquierdo.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-163">The offset is determined by the settings in the **top** and **left** style attributes.</span></span> <span data-ttu-id="9bbdb-164">Tenga en cuenta que el cuadro de contenido que se coloca como relativo ocupa espacio en el flujo de texto.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-164">Be aware that the containing box that is positioned as relative takes up space in the text flow.</span></span>

<span data-ttu-id="9bbdb-165">Por ejemplo, en la siguiente representación de VML, el óvalo rojo se coloca a 20 puntos de la izquierda y a 10 puntos de la parte superior con respecto al punto actual del flujo de texto, como se muestra en la siguiente imagen:</span><span class="sxs-lookup"><span data-stu-id="9bbdb-165">For example, in the following VML representation, the red oval is positioned 20 points from the left and 10 points from the top relative to the current point in the text flow, as shown in the following picture:</span></span>

![shape3.gif (2048 bytes)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="9bbdb-167">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="9bbdb-167">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="absolute"></a><span data-ttu-id="9bbdb-168">absolute</span><span class="sxs-lookup"><span data-stu-id="9bbdb-168">absolute</span></span>

<span data-ttu-id="9bbdb-169">Establecer el atributo de estilo de posición en "absoluto" permite colocar el cuadro contenedor a una distancia exacta desde la esquina superior izquierda (el punto base) de su elemento primario (el elemento posicionado que contiene la forma).</span><span class="sxs-lookup"><span data-stu-id="9bbdb-169">Setting the position style attribute to "absolute" allows you to place the containing box an exact distance from the top left corner (the base point) of its parent element (the positioned element that contains the shape).</span></span> <span data-ttu-id="9bbdb-170">Tenga en cuenta que el cuadro de contenido que se coloca como absoluto no ocupa espacio en el flujo de texto.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-170">Be aware that the containing box that is positioned as absolute doesn't take up space in the text flow.</span></span>

<span data-ttu-id="9bbdb-171">Por ejemplo, en la siguiente representación de VML, el óvalo rojo se encuentra dentro del elemento (toda la página web); por lo tanto, el punto base está en la esquina superior izquierda de la `<body>` página web.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-171">For example, in the following VML representation, the red oval is contained within the `<body>` element (the entire Web page); therefore, the base point is at the top left corner of the Web page.</span></span> <span data-ttu-id="9bbdb-172">El cuadro de contenido del óvalo se coloca exactamente a 20 puntos de la izquierda y a 10 puntos de la parte superior, con respecto a la esquina superior izquierda de la página web, como se muestra en la siguiente imagen:</span><span class="sxs-lookup"><span data-stu-id="9bbdb-172">The containing box for the oval is positioned exactly 20 points from the left and 10 points from the top, relative to the top left corner of the Web page, as shown in the following picture:</span></span>

![shape2.gif (2006 bytes)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="9bbdb-174">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="9bbdb-174">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="z-index"></a><span data-ttu-id="9bbdb-175">z-index</span><span class="sxs-lookup"><span data-stu-id="9bbdb-175">z-index</span></span>

<span data-ttu-id="9bbdb-176">Es posible colocar una forma que se superponga a otra forma.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-176">It is possible to position a shape that overlaps another shape.</span></span> <span data-ttu-id="9bbdb-177">Normalmente, el gráfico que aparece en último lugar en el código HTML aparece en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-177">Normally, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="9bbdb-178">En VML, puede controlar el orden z mediante el atributo **de estilo z-index.**</span><span class="sxs-lookup"><span data-stu-id="9bbdb-178">In VML, you can control the z-order by using the **z-index** style attribute.</span></span> <span data-ttu-id="9bbdb-179">El valor de este atributo puede ser cero, un entero positivo o un entero negativo.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-179">The value of this attribute can be zero, a positive integer, or a negative integer.</span></span> <span data-ttu-id="9bbdb-180">El gráfico que tiene un valor de índice z mayor se muestra encima del gráfico que tiene un valor de índice z más pequeño.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-180">The graphic that has a larger z-index value is displayed on top of the graphic that has a smaller z-index value.</span></span> <span data-ttu-id="9bbdb-181">Cuando ambos gráficos tienen el mismo valor de índice Z, el gráfico que aparece en último lugar en el código HTML aparece en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-181">When both graphics have the same z-index value, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="9bbdb-182">Por ejemplo, en la siguiente representación de VML, el óvalo rojo se muestra encima del rectángulo azul.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-182">For example, in the following VML representation, the red oval is displayed on top of the blue rectangle.</span></span> <span data-ttu-id="9bbdb-183">Esto se debe a que el valor de índice z del óvalo rojo es mayor que el valor de índice z del rectángulo azul.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-183">This is because the z-index value of the red oval is greater than the z-index value of the blue rectangle.</span></span>

![shape4.gif (572 bytes)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





<span data-ttu-id="9bbdb-185">Si cambia el índice z, como se muestra en la siguiente representación de VML, el óvalo rojo se movería detrás del rectángulo azul.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-185">If you change the z-index, as shown in the following VML representation, the red oval would move behind the blue rectangle.</span></span>

![shape5.gif (469 bytes)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





<span data-ttu-id="9bbdb-187">Si proporciona un entero negativo, puede usar el índice z para colocar los gráficos detrás del flujo de texto normal, como se muestra en la siguiente representación de VML.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-187">If you supply a negative integer, you can use z-index to position graphics behind the normal text flow, as shown in the following VML representation.</span></span>

![shape6.gif (2125 bytes)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="9bbdb-189">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="9bbdb-189">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rotation"></a><span data-ttu-id="9bbdb-190">giro</span><span class="sxs-lookup"><span data-stu-id="9bbdb-190">rotation</span></span>

<span data-ttu-id="9bbdb-191">Puede usar el atributo **de** estilo de rotación para especificar cuántos grados desea que una forma active su eje.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-191">You can use the **rotation** style attribute to specify how many degrees you want a shape to turn on its axis.</span></span> <span data-ttu-id="9bbdb-192">Un valor positivo indica una rotación en el sentido de las agujas del reloj; un valor negativo indica una rotación en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-192">A positive value indicates a clockwise rotation; a negative value indicates a counter-clockwise rotation.</span></span>

<span data-ttu-id="9bbdb-193">Por ejemplo, si especifica **style**='... rotation:90', puede girar la forma 90 grados en el sentido de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-193">For example, if you specify **style**='... rotation:90', you can rotate the shape 90 degrees clockwise.</span></span>

<span data-ttu-id="9bbdb-194">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="9bbdb-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="flip"></a><span data-ttu-id="9bbdb-195">voltear</span><span class="sxs-lookup"><span data-stu-id="9bbdb-195">flip</span></span>

<span data-ttu-id="9bbdb-196">Puede usar el atributo **de estilo de** volteo para voltear una forma en su eje x o y según la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="9bbdb-196">You can use the **flip** style attribute to flip a shape on its x or y axis according to the following table:</span></span>



| <span data-ttu-id="9bbdb-197">Valor</span><span class="sxs-lookup"><span data-stu-id="9bbdb-197">Value</span></span> | <span data-ttu-id="9bbdb-198">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bbdb-198">Description</span></span>                                                  |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="9bbdb-199">x</span><span class="sxs-lookup"><span data-stu-id="9bbdb-199">x</span></span>     | <span data-ttu-id="9bbdb-200">Voltear la forma girada sobre el eje y (invertir x ordinates)</span><span class="sxs-lookup"><span data-stu-id="9bbdb-200">Flip the rotated shape about the y axis (invert x ordinates)</span></span> |
| <span data-ttu-id="9bbdb-201">y</span><span class="sxs-lookup"><span data-stu-id="9bbdb-201">y</span></span>     | <span data-ttu-id="9bbdb-202">Voltear la forma girada sobre el eje x (invertir las ordinales y)</span><span class="sxs-lookup"><span data-stu-id="9bbdb-202">Flip the rotated shape about the x axis (invert y ordinates)</span></span> |



 

<span data-ttu-id="9bbdb-203">Se pueden especificar x e y en la propiedad flip.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-203">Both x and y may be specified in the flip property.</span></span>

<span data-ttu-id="9bbdb-204">Por ejemplo, si escribe **style**='... flip:x y', se voltea la forma en sus ejes x e y.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-204">For example, if you type **style**='... flip:x y', you will flip the shape on both its x and y axis.</span></span>

<span data-ttu-id="9bbdb-205">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="9bbdb-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="9bbdb-206">Resumen</span><span class="sxs-lookup"><span data-stu-id="9bbdb-206">Summary</span></span>

<span data-ttu-id="9bbdb-207">En función de lo que ha aprendido, puede colocar con precisión una forma en una página web siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="9bbdb-207">Based on what you've learned, you can precisely position a shape on a Web page by following these steps:</span></span>

1.  <span data-ttu-id="9bbdb-208">Decida dónde desea que la forma aparezca en una página web y el tamaño de la forma.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-208">Decide where you want the shape to appear on a Web page, and the size of the shape.</span></span>
2.  <span data-ttu-id="9bbdb-209">Especifique **style**='position:relative (o relative)' para determinar el punto base.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-209">Specify **style**='position:relative (or relative)' to determine the base point.</span></span>
3.  <span data-ttu-id="9bbdb-210">Use **izquierda** y **superior** para especificar el desplazamiento desde el punto base.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-210">Use **left** and **top** to specify the offset from the base point.</span></span>
4.  <span data-ttu-id="9bbdb-211">Use **width** y **height** para especificar el tamaño del cuadro de contenido de la forma.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-211">Use **width** and **height** to specify the size of the containing box for the shape.</span></span>
5.  <span data-ttu-id="9bbdb-212">Use **z-index para** especificar el orden Z de la forma.</span><span class="sxs-lookup"><span data-stu-id="9bbdb-212">Use **z-index** to specify the z-order of the shape.</span></span>

 

 