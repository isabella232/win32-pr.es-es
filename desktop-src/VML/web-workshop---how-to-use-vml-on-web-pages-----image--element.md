---
title: Uso del elemento Image
description: En este artículo se describe el uso del elemento Image en VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Taller web, elemento image
- diseñar páginas web, elemento image
- Lenguaje de marcado de vectores (VML),elemento image
- VML (Lenguaje de marcado de vectores),elemento image
- gráficos vectoriales, elemento image
- elemento de imagen
- Elementos de VML, imagen
- Formas de VML, elemento image
- Lenguaje de marcado de vectores (VML), atributos de propiedad de recorte
- VML (Lenguaje de marcado de vectores), atributos de propiedad de recorte
- gráficos vectoriales, atributos de propiedad de recorte
- Formas de VML, atributos de propiedad de recorte
- atributos de propiedad de recorte
- Lenguaje de marcado de vectores (VML),atributo de propiedad gain
- VML (Lenguaje de marcado de vectores),atributo de propiedad gain
- vector graphics,gain property attribute
- Formas de VML, atributo de propiedad gain
- atributo de propiedad gain
- Lenguaje de marcado de vectores (VML),contrast
- VML (Lenguaje de marcado de vectores),contrast
- gráficos vectoriales, contraste
- Formas de VML, contraste
- Lenguaje de marcado de vectores (VML),atributo de propiedad blacklevel
- VML (Lenguaje de marcado de vectores),atributo de propiedad blacklevel
- vector graphics,blacklevel property attribute
- Formas de VML, atributo de propiedad blacklevel
- atributo de propiedad blacklevel
- Lenguaje de marcado de vectores (VML),brillo
- VML (Lenguaje de marcado de vectores),brillo
- gráficos vectoriales, brillo
- Formas de VML, brillo
- Lenguaje de marcado de vectores (VML), atributo de propiedad de escala de grises
- VML (Lenguaje de marcado de vectores), atributo de propiedad de escala de grises
- gráficos vectoriales, atributo de propiedad de escala de grises
- Atributo de propiedad formas de VML, escala de grises
- atributo de propiedad de escala de grises
- Lenguaje de marcado de vectores (VML),atributo de propiedad gamma
- VML (Lenguaje de marcado de vectores),atributo de propiedad gamma
- vector graphics,gamma property attribute
- Formas de VML, atributo de propiedad gamma
- atributo de propiedad gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407808"
---
# <a name="using-the-image-element"></a><span data-ttu-id="46e3c-144">Uso del elemento Image</span><span class="sxs-lookup"><span data-stu-id="46e3c-144">Using the Image Element</span></span>

<span data-ttu-id="46e3c-145">En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="46e3c-145">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="46e3c-146">Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="46e3c-146">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="46e3c-147">A partir de diciembre de 2011, este tema se archivó.</span><span class="sxs-lookup"><span data-stu-id="46e3c-147">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="46e3c-148">Como resultado, ya no se mantiene activamente.</span><span class="sxs-lookup"><span data-stu-id="46e3c-148">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="46e3c-149">Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="46e3c-149">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="46e3c-150">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="46e3c-150">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="46e3c-151">Usar `<image>`</span><span class="sxs-lookup"><span data-stu-id="46e3c-151">Using `<image>`</span></span>

<span data-ttu-id="46e3c-152">En este tema, se muestra cómo usar el `<image>` elemento para mostrar imágenes con varios efectos especiales.</span><span class="sxs-lookup"><span data-stu-id="46e3c-152">In this topic, we will illustrate how to use the `<image>` element to display pictures with various special effects.</span></span>

<span data-ttu-id="46e3c-153">Si quisiera mostrar una imagen cargada desde un origen externo, normalmente usaría el elemento proporcionado en HTML y, a continuación, apuntaría el atributo de propiedad src a la ubicación del archivo `<img>` de imagen. </span><span class="sxs-lookup"><span data-stu-id="46e3c-153">If you wanted to display a picture that was loaded from an external source, you would usually use the `<img>` element provided in HTML, and then point the **src** property attribute to the location of the image file.</span></span>

<span data-ttu-id="46e3c-154">También puede usar el elemento `<image>` proporcionado en VML.</span><span class="sxs-lookup"><span data-stu-id="46e3c-154">Alternatively you can use the `<image>` element provided in VML.</span></span> <span data-ttu-id="46e3c-155">Cuando se usa el elemento , solo se puede crear un archivo de imagen y, a continuación, mostrar la imagen de forma diferente modificando los atributos `<image>` de propiedad del `<image>` elemento.</span><span class="sxs-lookup"><span data-stu-id="46e3c-155">When you use the `<image>` element, you can create only one image file and then display the image differently by altering the property attributes of the `<image>` element.</span></span> <span data-ttu-id="46e3c-156">Además, el elemento proporciona varios efectos especiales que no puede hacer simplemente con el elemento de HTML, como recortar , contraste, brillo, gamma y escala `<image>` `<img>` de [](#brightness) [grises.](#grayscale) [](#crop) [](#contrast) [](#gamma)</span><span class="sxs-lookup"><span data-stu-id="46e3c-156">Also, the `<image>` element provides several special effects that you can't do by simply using the `<img>` element of HTML, such as [cropping](#crop), [contrast](#contrast), [brightness](#brightness), [gamma](#gamma), and [grayscale](#grayscale).</span></span>

<span data-ttu-id="46e3c-157">[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="46e3c-157">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="crop"></a><span data-ttu-id="46e3c-158">Cultivo</span><span class="sxs-lookup"><span data-stu-id="46e3c-158">crop</span></span>

<span data-ttu-id="46e3c-159">Puede usar los atributos de propiedad **cropbottom**, **croptop,** **cropleft** y **cropright** del elemento para mostrar imágenes diferentes recortadas del mismo archivo `<image>` de imagen.</span><span class="sxs-lookup"><span data-stu-id="46e3c-159">You can use the **cropbottom**, **croptop**, **cropleft**, and **cropright** property attributes of the `<image>` element to display different pictures that are cropped from the same image file.</span></span>

<span data-ttu-id="46e3c-160">El valor de estos atributos de recorte representa el porcentaje de corte del borde de la imagen.</span><span class="sxs-lookup"><span data-stu-id="46e3c-160">The value of these crop attributes represents the percentage cut from the edge of the picture.</span></span> <span data-ttu-id="46e3c-161">El valor puede ser cualquier número entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="46e3c-161">The value can be any number between 0 to 1.</span></span> <span data-ttu-id="46e3c-162">De forma predeterminada, el valor se establece en 0, lo que indica que no se recorta desde el borde.</span><span class="sxs-lookup"><span data-stu-id="46e3c-162">By default, the value is set to 0, indicating no crop from the edge.</span></span> <span data-ttu-id="46e3c-163">El valor 0,1 indica un recorte del 10 % desde el borde, el valor 0,15 indica un recorte del 15 % desde el borde, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="46e3c-163">The value 0.1 indicates a cropping of 10 percent from the edge, The value 0.15 indicates a cropping of 15 percent from the edge, and so on.</span></span>

<span data-ttu-id="46e3c-164">Por ejemplo, para mostrar cinco imágenes recortadas del mismo archivo de imagen, puede usar el elemento y especificar distintos valores de recorte, como se muestra en la siguiente representación `<image>` de VML:</span><span class="sxs-lookup"><span data-stu-id="46e3c-164">For example, to display five pictures that are all cropped from the same image file, you can use the `<image>` element and specify different crop values, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![image1 \-2.jpg (1969 bytes)](images/image1-2.jpg)![image1 \-3.jpg (1148 bytes)](images/image1-3.jpg)![image1 \-4.jpg (1686 bytes)](images/image1-4.jpg)![image1 \-5.jpg (1364 bytes)](images/image1-5.jpg)


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





<span data-ttu-id="46e3c-170">La primera imagen, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , no tiene ningún valor de recorte.</span><span class="sxs-lookup"><span data-stu-id="46e3c-170">The first image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />`, doesn't have any crop value.</span></span> <span data-ttu-id="46e3c-171">Por lo tanto, el 100 % de la imagen original se muestra con un tamaño de 100 puntos por 80 puntos.</span><span class="sxs-lookup"><span data-stu-id="46e3c-171">Therefore, 100 percent of the original image is displayed at a size of 100 points by 80 points.</span></span>

<span data-ttu-id="46e3c-172">La segunda imagen, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , tiene algunos valores de recorte.</span><span class="sxs-lookup"><span data-stu-id="46e3c-172">The second image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>`, has some crop values.</span></span> <span data-ttu-id="46e3c-173">`cropbottom="0.2"` indica que el 20 por ciento de la imagen se recortará desde la parte inferior; `cropright="0.15"` indica que el 15 por ciento de la imagen se recortará desde el borde derecho.</span><span class="sxs-lookup"><span data-stu-id="46e3c-173">`cropbottom="0.2"` indicates that 20 percent of the picture will be cropped from the bottom; `cropright="0.15"` indicates that 15 percent of the picture will be cropped from the right edge.</span></span> <span data-ttu-id="46e3c-174">A continuación, la imagen restante se muestra con un tamaño de 85 puntos por 64 puntos.</span><span class="sxs-lookup"><span data-stu-id="46e3c-174">The remaining picture is then displayed at a size of 85 points by 64 points.</span></span>

<span data-ttu-id="46e3c-175">De forma similar, las imágenes tercera, cuarta y quinta tienen algunos valores de recorte.</span><span class="sxs-lookup"><span data-stu-id="46e3c-175">Similarly the third, fourth, and fifth images have some crop values.</span></span> <span data-ttu-id="46e3c-176">La imagen original se recorta según los valores de recorte y, a continuación, se muestra según el valor de ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="46e3c-176">The original picture is cropped according to the crop values, and is then displayed according to the value of width and height.</span></span>

<span data-ttu-id="46e3c-177">[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="46e3c-177">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="contrast"></a><span data-ttu-id="46e3c-178">contraste</span><span class="sxs-lookup"><span data-stu-id="46e3c-178">contrast</span></span>

<span data-ttu-id="46e3c-179">Puede usar el atributo de propiedad **gain** del `<image>` elemento para mostrar varias imágenes con diferentes configuraciones de contraste.</span><span class="sxs-lookup"><span data-stu-id="46e3c-179">You can use the **gain** property attribute of the `<image>` element to display various pictures that have different contrast settings.</span></span>

<span data-ttu-id="46e3c-180">El valor del atributo de propiedad **gain** puede ser cualquier número.</span><span class="sxs-lookup"><span data-stu-id="46e3c-180">The value of the **gain** property attribute can be any number.</span></span> <span data-ttu-id="46e3c-181">De forma predeterminada, el valor es 1, lo que indica el uso del mismo contraste que la imagen original.</span><span class="sxs-lookup"><span data-stu-id="46e3c-181">By default, the value is 1, indicating the use of the same contrast as the original image.</span></span> <span data-ttu-id="46e3c-182">El valor 0 indica que no hay contraste.</span><span class="sxs-lookup"><span data-stu-id="46e3c-182">The value 0 indicates no contrast.</span></span> <span data-ttu-id="46e3c-183">Cuanto mayor sea el número, mayor será el contraste.</span><span class="sxs-lookup"><span data-stu-id="46e3c-183">The larger the number, the higher the contrast.</span></span>

<span data-ttu-id="46e3c-184">Por ejemplo, para mostrar cinco imágenes que tienen una configuración de contraste diferente, puede usar el elemento y establecer un valor diferente para el atributo de propiedad gain, como se muestra en la siguiente representación `<image>` de VML: </span><span class="sxs-lookup"><span data-stu-id="46e3c-184">For example, to display five pictures that have different contrast settings, you can use the `<image>` element and set a different value for the **gain** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![image2 \-2.jpg (270 bytes)](images/image2-2.jpg)![imagen2 \-3.jpg (1919 bytes)](images/image2-3.jpg)![imagen2 \-4.jpg (3143 bytes)](images/image2-4.jpg)![imagen2 \-5.jpg (1724 bytes)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





<span data-ttu-id="46e3c-190">Cuando el **atributo de** propiedad gain se establece en 0, toda la imagen se vuelve gris porque no hay contraste.</span><span class="sxs-lookup"><span data-stu-id="46e3c-190">When the **gain** property attribute is set to 0, the entire image becomes gray because there is no contrast.</span></span> <span data-ttu-id="46e3c-191">El contraste es más evidente cuando el atributo de propiedad **gain** se establece en 3 que cuando se establece en 0,5.</span><span class="sxs-lookup"><span data-stu-id="46e3c-191">The contrast is more noticeable when the **gain** property attribute is set to 3 than when it is set to 0.5.</span></span> <span data-ttu-id="46e3c-192">El contraste se invierte cuando el atributo de propiedad **gain** se establece en un valor negativo como -0,4.</span><span class="sxs-lookup"><span data-stu-id="46e3c-192">The contrast is reversed when the **gain** property attribute is set to a negative value such as -0.4.</span></span>

<span data-ttu-id="46e3c-193">[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="46e3c-193">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="brightness"></a><span data-ttu-id="46e3c-194">luminosidad</span><span class="sxs-lookup"><span data-stu-id="46e3c-194">brightness</span></span>

<span data-ttu-id="46e3c-195">Puede usar el atributo **de propiedad blacklevel** del elemento para mostrar `<image>` varias imágenes que tienen una configuración de brillo diferente.</span><span class="sxs-lookup"><span data-stu-id="46e3c-195">You can use the **blacklevel** property attribute of the `<image>` element to display various pictures that have different brightness settings.</span></span>

<span data-ttu-id="46e3c-196">El valor del atributo **de propiedad blacklevel** puede ser cualquier valor entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="46e3c-196">The value of the **blacklevel** property attribute can be any value between 0 to 1.</span></span> <span data-ttu-id="46e3c-197">De forma predeterminada, el valor es 0, lo que indica que se conserva el nivel de brillo de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="46e3c-197">By default, the value is 0, indicating that the level of brightness in the original image is preserved.</span></span> <span data-ttu-id="46e3c-198">El valor 1 indica el nivel más alto de brillo.</span><span class="sxs-lookup"><span data-stu-id="46e3c-198">The value 1 indicates the highest level of brightness.</span></span>

<span data-ttu-id="46e3c-199">Por ejemplo, para mostrar cinco imágenes que tienen una configuración de brillo diferente, puede usar el elemento y establecer un valor diferente para el atributo de propiedad blacklevel, como se muestra en la siguiente representación `<image>` de VML: </span><span class="sxs-lookup"><span data-stu-id="46e3c-199">For example, to display five pictures that have different brightness settings, you can use the `<image>` element and set a different value for the **blacklevel** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![image3 \-2.jpg (2579 bytes)](images/image3-2.jpg)![imagen3 \-3.jpg (2330 bytes)](images/image3-3.jpg)![image3 \-4.jpg (2727 bytes)](images/image3-4.jpg)![image3 \-5.jpg (2435 bytes)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





<span data-ttu-id="46e3c-205">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="46e3c-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="grayscale"></a><span data-ttu-id="46e3c-206">escala de grises</span><span class="sxs-lookup"><span data-stu-id="46e3c-206">grayscale</span></span>

<span data-ttu-id="46e3c-207">Puede usar el atributo **de propiedad de escala** de grises del elemento para mostrar imágenes con o sin escala de `<image>` grises.</span><span class="sxs-lookup"><span data-stu-id="46e3c-207">You can use the **grayscale** property attribute of the `<image>` element to display pictures with or without grayscale.</span></span>

<span data-ttu-id="46e3c-208">El valor del atributo **de propiedad de escala** de grises puede ser true o false.</span><span class="sxs-lookup"><span data-stu-id="46e3c-208">The value of the **grayscale** property attribute can be either true or false.</span></span> <span data-ttu-id="46e3c-209">De forma predeterminada, el valor se establece en false para que la imagen se muestre en color.</span><span class="sxs-lookup"><span data-stu-id="46e3c-209">By default, the value is set to false so that the image will be displayed in color.</span></span> <span data-ttu-id="46e3c-210">Si el valor se establece en true, la imagen se mostrará en escala de grises.</span><span class="sxs-lookup"><span data-stu-id="46e3c-210">If the value is set to true, the image will be displayed in grayscale.</span></span>

<span data-ttu-id="46e3c-211">Por ejemplo, como se muestra en la imagen siguiente, la primera imagen usa la configuración predeterminada (false) del atributo de escala de grises ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span><span class="sxs-lookup"><span data-stu-id="46e3c-211">For example, as shown in the following picture, the first image uses the default setting (false)of the grayscale attribute (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span></span> <span data-ttu-id="46e3c-212">Por lo tanto, la imagen se muestra en color.</span><span class="sxs-lookup"><span data-stu-id="46e3c-212">Therefore, the picture is displayed in color.</span></span>

<span data-ttu-id="46e3c-213">La segunda imagen establece el atributo de escala de grises en true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span><span class="sxs-lookup"><span data-stu-id="46e3c-213">The second image sets the grayscale attribute to true (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span></span> <span data-ttu-id="46e3c-214">Por lo tanto, la imagen se muestra en escala de grises, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="46e3c-214">Therefore, the picture is displayed in grayscale, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![image4 \-2.jpg (2138 bytes)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





<span data-ttu-id="46e3c-217">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="46e3c-217">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="gamma"></a><span data-ttu-id="46e3c-218">gamma</span><span class="sxs-lookup"><span data-stu-id="46e3c-218">gamma</span></span>

<span data-ttu-id="46e3c-219">Puede usar el atributo de propiedad **gamma** del elemento para mostrar imágenes `<image>` con diferentes configuraciones gamma.</span><span class="sxs-lookup"><span data-stu-id="46e3c-219">You can use the **gamma** property attribute of the `<image>` element to display pictures that have different gamma settings.</span></span>

<span data-ttu-id="46e3c-220">El valor del atributo de propiedad gamma puede ser cualquier valor entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="46e3c-220">The value of the gamma property attribute can be any value between 0 and 1.</span></span> <span data-ttu-id="46e3c-221">De forma predeterminada, el valor se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="46e3c-221">By default, the value is set to 1.</span></span>

<span data-ttu-id="46e3c-222">Por ejemplo, para mostrar tres imágenes que tienen una configuración gamma diferente, puede usar el elemento y establecer un valor diferente del atributo de propiedad gamma, como se muestra en la siguiente representación `<image>` de VML: </span><span class="sxs-lookup"><span data-stu-id="46e3c-222">For example, to display three pictures that have different gamma settings, you can use the `<image>` element and set a different value of the **gamma** property attribute, as shown in the following VML representation:</span></span>

![image5 \-1.jpg (2714 bytes)](images/image5-1.jpg)![image5 \-2.jpg (2729 bytes)](images/image5-2.jpg)![image5 \-3.jpg (2726 bytes)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





<span data-ttu-id="46e3c-226">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span><span class="sxs-lookup"><span data-stu-id="46e3c-226">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span></span>

 

 