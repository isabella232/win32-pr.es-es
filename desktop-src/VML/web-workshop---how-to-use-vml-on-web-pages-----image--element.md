---
title: Usar el elemento Image
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Web Workshop, elemento Image
- diseñar páginas web, elemento de imagen
- Lenguaje de marcado de vectores (VML), elemento Image
- VML (Lenguaje de marcado de vectores), elemento de imagen
- gráficos vectoriales, elemento de imagen
- elemento de imagen
- Elementos VML, imagen
- Formas de VML, elemento de imagen
- Lenguaje de marcado de vectores (VML), recortar atributos de propiedad
- VML (Lenguaje de marcado de vectores), atributos de propiedad de recorte
- gráficos vectoriales, recortar atributos de propiedad
- Formas VML, atributos de propiedad de recorte
- recortar atributos de propiedad
- Lenguaje de marcado de vectores (VML), atributo de propiedad de ganancia
- VML (Lenguaje de marcado de vectores), atributo de propiedad de ganancia
- gráficos vectoriales, atributo de propiedad de ganancia
- Formas VML, atributo de propiedad de ganancia
- atributo de propiedad de ganancia
- Lenguaje de marcado de vectores (VML), contraste
- VML (Lenguaje de marcado de vectores), contraste
- gráficos vectoriales, contraste
- Formas VML, contraste
- Lenguaje de marcado de vectores (VML), atributo de propiedad blacklevel
- VML (Lenguaje de marcado de vectores), atributo de propiedad blacklevel
- gráficos vectoriales, atributo de propiedad blacklevel
- Formas VML, atributo de propiedad blacklevel
- atributo de propiedad blacklevel
- Lenguaje de marcado de vectores (VML), brillo
- VML (Lenguaje de marcado de vectores), brillo
- gráficos vectoriales, brillo
- Formas VML, brillo
- Lenguaje de marcado de vectores (VML), atributo de propiedad de escala de grises
- VML (Lenguaje de marcado de vectores), atributo de propiedad de escala de grises
- gráficos vectoriales, atributo de propiedad de escala de grises
- Formas VML, atributo de propiedad de escala de grises
- atributo de propiedad de escala de grises
- Lenguaje de marcado de vectores (VML), atributo de propiedad gamma
- VML (Lenguaje de marcado de vectores), atributo de propiedad gamma
- Vector Graphics, atributo de propiedad gamma
- Formas VML, atributo de propiedad gamma
- atributo de propiedad gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820039ff76f3685eeea7a65e2bbc01578abbe581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533435"
---
# <a name="using-the-image-element"></a><span data-ttu-id="7856f-145">Usar el elemento Image</span><span class="sxs-lookup"><span data-stu-id="7856f-145">Using the Image Element</span></span>

<span data-ttu-id="7856f-146">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7856f-146">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7856f-147">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="7856f-147">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7856f-148">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="7856f-148">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7856f-149">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="7856f-149">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7856f-150">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7856f-150">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7856f-151">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7856f-151">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7856f-152">Usar `<image>`</span><span class="sxs-lookup"><span data-stu-id="7856f-152">Using `<image>`</span></span>

<span data-ttu-id="7856f-153">En este tema, se muestra cómo usar el `<image>` elemento para mostrar imágenes con distintos efectos especiales.</span><span class="sxs-lookup"><span data-stu-id="7856f-153">In this topic, we will illustrate how to use the `<image>` element to display pictures with various special effects.</span></span>

<span data-ttu-id="7856f-154">Si desea mostrar una imagen que se cargó desde un origen externo, normalmente usaría el `<img>` elemento proporcionado en HTML y, a continuación, apuntaría el atributo de propiedad **src** a la ubicación del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="7856f-154">If you wanted to display a picture that was loaded from an external source, you would usually use the `<img>` element provided in HTML, and then point the **src** property attribute to the location of the image file.</span></span>

<span data-ttu-id="7856f-155">También puede usar el `<image>` elemento proporcionado en VML.</span><span class="sxs-lookup"><span data-stu-id="7856f-155">Alternatively you can use the `<image>` element provided in VML.</span></span> <span data-ttu-id="7856f-156">Cuando se usa el `<image>` elemento, solo se puede crear un archivo de imagen y, a continuación, Mostrar la imagen de forma diferente modificando los atributos de propiedad del `<image>` elemento.</span><span class="sxs-lookup"><span data-stu-id="7856f-156">When you use the `<image>` element, you can create only one image file and then display the image differently by altering the property attributes of the `<image>` element.</span></span> <span data-ttu-id="7856f-157">Además, el `<image>` elemento proporciona varios efectos especiales que no se pueden realizar mediante el uso del `<img>` elemento de HTML, como el [recorte](#crop), el [contraste](#contrast), el [brillo](#brightness), la [gamma](#gamma)y la [escala de grises](#grayscale).</span><span class="sxs-lookup"><span data-stu-id="7856f-157">Also, the `<image>` element provides several special effects that you can't do by simply using the `<img>` element of HTML, such as [cropping](#crop), [contrast](#contrast), [brightness](#brightness), [gamma](#gamma), and [grayscale](#grayscale).</span></span>

<span data-ttu-id="7856f-158">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="7856f-158">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="crop"></a><span data-ttu-id="7856f-159">CropBox</span><span class="sxs-lookup"><span data-stu-id="7856f-159">crop</span></span>

<span data-ttu-id="7856f-160">Puede usar los atributos de propiedad **CropBottom**, **CropTop**, **CropLeft** y **CropRight** del `<image>` elemento para mostrar diferentes imágenes que se recortan del mismo archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="7856f-160">You can use the **cropbottom**, **croptop**, **cropleft**, and **cropright** property attributes of the `<image>` element to display different pictures that are cropped from the same image file.</span></span>

<span data-ttu-id="7856f-161">El valor de estos atributos de recorte representa el porcentaje de corte del borde de la imagen.</span><span class="sxs-lookup"><span data-stu-id="7856f-161">The value of these crop attributes represents the percentage cut from the edge of the picture.</span></span> <span data-ttu-id="7856f-162">El valor puede ser cualquier número comprendido entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="7856f-162">The value can be any number between 0 to 1.</span></span> <span data-ttu-id="7856f-163">De forma predeterminada, el valor se establece en 0, lo que indica que no hay ningún recorte del borde.</span><span class="sxs-lookup"><span data-stu-id="7856f-163">By default, the value is set to 0, indicating no crop from the edge.</span></span> <span data-ttu-id="7856f-164">El valor 0,1 indica un recorte del 10 por ciento del borde, el valor 0,15 indica un recorte del 15 por ciento del borde, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="7856f-164">The value 0.1 indicates a cropping of 10 percent from the edge, The value 0.15 indicates a cropping of 15 percent from the edge, and so on.</span></span>

<span data-ttu-id="7856f-165">Por ejemplo, para mostrar cinco imágenes recortadas del mismo archivo de imagen, puede usar el `<image>` elemento y especificar valores de recorte diferentes, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="7856f-165">For example, to display five pictures that are all cropped from the same image file, you can use the `<image>` element and specify different crop values, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image1 (1969 bytes)](images/image1-2.jpg)![\-3.jpg image1 (1148 bytes)](images/image1-3.jpg)![\-4.jpg image1 (1686 bytes)](images/image1-4.jpg)![\-5.jpg image1 (1364 bytes)](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





<span data-ttu-id="7856f-171">La primera imagen, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , no tiene ningún valor de recorte.</span><span class="sxs-lookup"><span data-stu-id="7856f-171">The first image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />`, doesn't have any crop value.</span></span> <span data-ttu-id="7856f-172">Por lo tanto, el 100 por ciento de la imagen original se muestra en un tamaño de 100 puntos por 80 puntos.</span><span class="sxs-lookup"><span data-stu-id="7856f-172">Therefore, 100 percent of the original image is displayed at a size of 100 points by 80 points.</span></span>

<span data-ttu-id="7856f-173">La segunda imagen, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , tiene algunos valores de recorte.</span><span class="sxs-lookup"><span data-stu-id="7856f-173">The second image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>`, has some crop values.</span></span> <span data-ttu-id="7856f-174">`cropbottom="0.2"` indica que el 20 por ciento de la imagen se recortará de la parte inferior; `cropright="0.15"` indica que el 15 por ciento de la imagen se recortará desde el borde derecho.</span><span class="sxs-lookup"><span data-stu-id="7856f-174">`cropbottom="0.2"` indicates that 20 percent of the picture will be cropped from the bottom; `cropright="0.15"` indicates that 15 percent of the picture will be cropped from the right edge.</span></span> <span data-ttu-id="7856f-175">A continuación, se muestra la imagen restante en un tamaño de 85 puntos por 64 puntos.</span><span class="sxs-lookup"><span data-stu-id="7856f-175">The remaining picture is then displayed at a size of 85 points by 64 points.</span></span>

<span data-ttu-id="7856f-176">Del mismo modo, las imágenes tercera, cuarta y quinta tienen algunos valores de recorte.</span><span class="sxs-lookup"><span data-stu-id="7856f-176">Similarly the third, fourth, and fifth images have some crop values.</span></span> <span data-ttu-id="7856f-177">La imagen original se recorta según los valores de recorte y, a continuación, se muestra según el valor de ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="7856f-177">The original picture is cropped according to the crop values, and is then displayed according to the value of width and height.</span></span>

<span data-ttu-id="7856f-178">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="7856f-178">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="contrast"></a><span data-ttu-id="7856f-179">contraste</span><span class="sxs-lookup"><span data-stu-id="7856f-179">contrast</span></span>

<span data-ttu-id="7856f-180">Puede usar el atributo de propiedad de **ganancia** del `<image>` elemento para mostrar varias imágenes que tienen diferentes valores de contraste.</span><span class="sxs-lookup"><span data-stu-id="7856f-180">You can use the **gain** property attribute of the `<image>` element to display various pictures that have different contrast settings.</span></span>

<span data-ttu-id="7856f-181">El valor del atributo de la propiedad de **ganancia** puede ser cualquier número.</span><span class="sxs-lookup"><span data-stu-id="7856f-181">The value of the **gain** property attribute can be any number.</span></span> <span data-ttu-id="7856f-182">De forma predeterminada, el valor es 1, que indica el uso del mismo contraste que la imagen original.</span><span class="sxs-lookup"><span data-stu-id="7856f-182">By default, the value is 1, indicating the use of the same contrast as the original image.</span></span> <span data-ttu-id="7856f-183">El valor 0 indica que no hay ningún contraste.</span><span class="sxs-lookup"><span data-stu-id="7856f-183">The value 0 indicates no contrast.</span></span> <span data-ttu-id="7856f-184">Cuanto mayor sea el número, mayor será el contraste.</span><span class="sxs-lookup"><span data-stu-id="7856f-184">The larger the number, the higher the contrast.</span></span>

<span data-ttu-id="7856f-185">Por ejemplo, para mostrar cinco imágenes que tienen una configuración de contraste diferente, puede usar el `<image>` elemento y establecer un valor diferente para el atributo de la propiedad de **ganancia** , como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="7856f-185">For example, to display five pictures that have different contrast settings, you can use the `<image>` element and set a different value for the **gain** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image2 (270 bytes)](images/image2-2.jpg)![\-3.jpg image2 (1919 bytes)](images/image2-3.jpg)![\-4.jpg image2 (3143 bytes)](images/image2-4.jpg)![\-5.jpg image2 (1724 bytes)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





<span data-ttu-id="7856f-191">Cuando el atributo de la propiedad de **ganancia** se establece en 0, toda la imagen se vuelve atenuada porque no hay ningún contraste.</span><span class="sxs-lookup"><span data-stu-id="7856f-191">When the **gain** property attribute is set to 0, the entire image becomes gray because there is no contrast.</span></span> <span data-ttu-id="7856f-192">El contraste es más apreciable cuando el atributo de la propiedad de **ganancia** está establecido en 3 que cuando se establece en 0,5.</span><span class="sxs-lookup"><span data-stu-id="7856f-192">The contrast is more noticeable when the **gain** property attribute is set to 3 than when it is set to 0.5.</span></span> <span data-ttu-id="7856f-193">El contraste se invierte cuando el atributo de la propiedad de **ganancia** está establecido en un valor negativo, como-0,4.</span><span class="sxs-lookup"><span data-stu-id="7856f-193">The contrast is reversed when the **gain** property attribute is set to a negative value such as -0.4.</span></span>

<span data-ttu-id="7856f-194">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="7856f-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="brightness"></a><span data-ttu-id="7856f-195">luminosidad</span><span class="sxs-lookup"><span data-stu-id="7856f-195">brightness</span></span>

<span data-ttu-id="7856f-196">Puede usar el atributo de la propiedad **blacklevel** del `<image>` elemento para mostrar varias imágenes que tienen diferentes valores de brillo.</span><span class="sxs-lookup"><span data-stu-id="7856f-196">You can use the **blacklevel** property attribute of the `<image>` element to display various pictures that have different brightness settings.</span></span>

<span data-ttu-id="7856f-197">El valor del atributo de la propiedad **blacklevel** puede ser cualquier valor entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="7856f-197">The value of the **blacklevel** property attribute can be any value between 0 to 1.</span></span> <span data-ttu-id="7856f-198">De forma predeterminada, el valor es 0, lo que indica que se conserva el nivel de brillo de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="7856f-198">By default, the value is 0, indicating that the level of brightness in the original image is preserved.</span></span> <span data-ttu-id="7856f-199">El valor 1 indica el nivel más alto de brillo.</span><span class="sxs-lookup"><span data-stu-id="7856f-199">The value 1 indicates the highest level of brightness.</span></span>

<span data-ttu-id="7856f-200">Por ejemplo, para mostrar cinco imágenes que tienen una configuración de brillo diferente, puede usar el `<image>` elemento y establecer un valor diferente para el atributo de la propiedad **blacklevel** , como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="7856f-200">For example, to display five pictures that have different brightness settings, you can use the `<image>` element and set a different value for the **blacklevel** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image3 (2579 bytes)](images/image3-2.jpg)![\-3.jpg image3 (2330 bytes)](images/image3-3.jpg)![\-4.jpg image3 (2727 bytes)](images/image3-4.jpg)![\-5.jpg image3 (2435 bytes)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





<span data-ttu-id="7856f-206">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="7856f-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="grayscale"></a><span data-ttu-id="7856f-207">escala de grises</span><span class="sxs-lookup"><span data-stu-id="7856f-207">grayscale</span></span>

<span data-ttu-id="7856f-208">Puede usar el atributo de la propiedad de **escala de grises** del `<image>` elemento para mostrar imágenes con o sin escala de grises.</span><span class="sxs-lookup"><span data-stu-id="7856f-208">You can use the **grayscale** property attribute of the `<image>` element to display pictures with or without grayscale.</span></span>

<span data-ttu-id="7856f-209">El valor del atributo de propiedad de **escala de grises** puede ser true o false.</span><span class="sxs-lookup"><span data-stu-id="7856f-209">The value of the **grayscale** property attribute can be either true or false.</span></span> <span data-ttu-id="7856f-210">De forma predeterminada, el valor se establece en false para que la imagen se muestre en color.</span><span class="sxs-lookup"><span data-stu-id="7856f-210">By default, the value is set to false so that the image will be displayed in color.</span></span> <span data-ttu-id="7856f-211">Si el valor se establece en true, la imagen se mostrará en escala de grises.</span><span class="sxs-lookup"><span data-stu-id="7856f-211">If the value is set to true, the image will be displayed in grayscale.</span></span>

<span data-ttu-id="7856f-212">Por ejemplo, como se muestra en la siguiente imagen, la primera imagen utiliza el valor predeterminado (false) del atributo de escala de grises ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span><span class="sxs-lookup"><span data-stu-id="7856f-212">For example, as shown in the following picture, the first image uses the default setting (false)of the grayscale attribute (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span></span> <span data-ttu-id="7856f-213">Por lo tanto, la imagen se muestra en color.</span><span class="sxs-lookup"><span data-stu-id="7856f-213">Therefore, the picture is displayed in color.</span></span>

<span data-ttu-id="7856f-214">La segunda imagen establece el atributo de escala de grises en true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span><span class="sxs-lookup"><span data-stu-id="7856f-214">The second image sets the grayscale attribute to true (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span></span> <span data-ttu-id="7856f-215">Por lo tanto, la imagen se muestra en escala de grises, tal y como se muestra en la siguiente representación VML:</span><span class="sxs-lookup"><span data-stu-id="7856f-215">Therefore, the picture is displayed in grayscale, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg archivo image4 (2138 bytes)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





<span data-ttu-id="7856f-218">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="7856f-218">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="gamma"></a><span data-ttu-id="7856f-219">gamma</span><span class="sxs-lookup"><span data-stu-id="7856f-219">gamma</span></span>

<span data-ttu-id="7856f-220">Puede usar el atributo de propiedad **Gamma** del `<image>` elemento para mostrar las imágenes que tienen una configuración gamma diferente.</span><span class="sxs-lookup"><span data-stu-id="7856f-220">You can use the **gamma** property attribute of the `<image>` element to display pictures that have different gamma settings.</span></span>

<span data-ttu-id="7856f-221">El valor del atributo de propiedad gamma puede ser cualquier valor entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="7856f-221">The value of the gamma property attribute can be any value between 0 and 1.</span></span> <span data-ttu-id="7856f-222">De forma predeterminada, el valor se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="7856f-222">By default, the value is set to 1.</span></span>

<span data-ttu-id="7856f-223">Por ejemplo, para mostrar tres imágenes que tienen una configuración gamma diferente, puede usar el `<image>` elemento y establecer un valor diferente del atributo de propiedad **gamma** , como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="7856f-223">For example, to display three pictures that have different gamma settings, you can use the `<image>` element and set a different value of the **gamma** property attribute, as shown in the following VML representation:</span></span>

![\-1.jpg image5 (2714 bytes)](images/image5-1.jpg)![\-2.jpg image5 (2729 bytes)](images/image5-2.jpg)![\-3.jpg image5 (2726 bytes)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





<span data-ttu-id="7856f-227">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span><span class="sxs-lookup"><span data-stu-id="7856f-227">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span></span>

 

 