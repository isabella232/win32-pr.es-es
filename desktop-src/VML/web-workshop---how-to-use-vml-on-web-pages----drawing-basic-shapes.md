---
title: Dibujar formas básicas
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Web Workshop, dibujar formas
- diseñar páginas web, dibujar formas
- Lenguaje de marcado de vectores (VML), dibujar formas
- VML (Lenguaje de marcado de vectores), dibujar formas
- gráficos vectoriales, dibujar formas
- dibujar formas
- Formas VML, dibujo
- Lenguaje de marcado de vectores (VML), XML
- VML (Lenguaje de marcado de vectores), XML
- gráficos vectoriales, XML
- Lenguaje de marcado de vectores (VML), CSS2
- VML (Lenguaje de marcado de vectores), CSS2
- gráficos vectoriales, CSS2
- Lenguaje de marcado de vectores (VML), elementos
- VML (Lenguaje de marcado de vectores), elementos
- gráficos vectoriales, elementos
- Elementos VML, dibujar formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ab25fc9310750c9f49c5978a063c76639ec4bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488167"
---
# <a name="drawing-basic-shapes"></a><span data-ttu-id="d2695-121">Dibujar formas básicas</span><span class="sxs-lookup"><span data-stu-id="d2695-121">Drawing Basic Shapes</span></span>

<span data-ttu-id="d2695-122">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d2695-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d2695-123">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="d2695-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d2695-124">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="d2695-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d2695-125">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="d2695-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d2695-126">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d2695-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d2695-127">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d2695-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d2695-128">En este tema, explicaremos lo fácil que es dibujar una forma mediante VML.</span><span class="sxs-lookup"><span data-stu-id="d2695-128">In this topic, we will illustrate how easy it is to draw a shape using VML.</span></span>

<span data-ttu-id="d2695-129">Para crear un óvalo rojo en una página web, como se muestra en la siguiente imagen, puede dibujar el óvalo mediante una herramienta de edición de gráficos, guardar el dibujo como mapa de bits y, a continuación, insertar el mapa de bits en la página web:</span><span class="sxs-lookup"><span data-stu-id="d2695-129">To create a red oval on a Web page, as shown in the following picture, you can draw the oval by using a graphic edit tool, save your drawing as a bitmap, and then insert the bitmap on your Web page:</span></span>

![oval1.gif (627 bytes)](images/oval1.gif)

<span data-ttu-id="d2695-131">Como alternativa, puede usar VML para dibujar gráficos.</span><span class="sxs-lookup"><span data-stu-id="d2695-131">Alternatively, you can use VML to draw graphics.</span></span> <span data-ttu-id="d2695-132">En el ejemplo anterior, puede escribir las líneas siguientes en la `<BODY>` región de la página web para dibujar el óvalo rojo:</span><span class="sxs-lookup"><span data-stu-id="d2695-132">In the preceding example, you can type the following lines in the `<BODY>` region of your Web page to draw the red oval:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





<span data-ttu-id="d2695-133">`<v:...>` y `</v:...>` son la etiqueta inicial y la etiqueta final en la [sintaxis XML](#xml-structure).`style='width:100pt; height:75pt'`</span><span class="sxs-lookup"><span data-stu-id="d2695-133">`<v:...>` and `</v:...>` are the start tag and end tag in [XML syntax](#xml-structure).`style='width:100pt; height:75pt'`</span></span> <span data-ttu-id="d2695-134">proporciona [información de CSS](#css-information).</span><span class="sxs-lookup"><span data-stu-id="d2695-134">provides [CSS information](#css-information).</span></span> <span data-ttu-id="d2695-135">**oval** y **fillColor**= "red" son [elementos VML](#vml-elements).</span><span class="sxs-lookup"><span data-stu-id="d2695-135">**oval** and **fillcolor**="red" are [VML elements](#vml-elements).</span></span>

<span data-ttu-id="d2695-136">Puede modificar los gráficos simplemente cambiando sus atributos de propiedad en VML.</span><span class="sxs-lookup"><span data-stu-id="d2695-136">You can alter the graphics by simply changing their property attributes in VML.</span></span> <span data-ttu-id="d2695-137">En el ejemplo anterior, si cambia `fillcolor="red"` a `fillcolor="blue"` , como se muestra en la representación VML siguiente, el óvalo rojo cambiará a azul:</span><span class="sxs-lookup"><span data-stu-id="d2695-137">In the preceding example, if you change `fillcolor="red"` to `fillcolor="blue"`, as shown in the following VML representation, the red oval will change to blue:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





<span data-ttu-id="d2695-138">Los exploradores que admiten VML pueden representar y mostrar los gráficos representados en VML sin tener que descargar archivos de imagen independientes.</span><span class="sxs-lookup"><span data-stu-id="d2695-138">Browsers that support VML can render and display the graphics represented in VML without having to download separate image files.</span></span> <span data-ttu-id="d2695-139">La mayoría de los gráficos representados en VML se representan más rápido en los exploradores y requieren menos espacio en disco y tiempo de descarga.</span><span class="sxs-lookup"><span data-stu-id="d2695-139">Most graphics represented in VML are rendered faster in browsers, and require less disk space and download time.</span></span>

<span data-ttu-id="d2695-140">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="d2695-140">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="xml-structure"></a><span data-ttu-id="d2695-141">Estructura XML</span><span class="sxs-lookup"><span data-stu-id="d2695-141">XML Structure</span></span>

<span data-ttu-id="d2695-142">VML está formateado de acuerdo con las reglas de lenguaje de marcado extensible (XML).</span><span class="sxs-lookup"><span data-stu-id="d2695-142">VML is formatted according to the rules of Extensible Markup Language (XML).</span></span> <span data-ttu-id="d2695-143">Cualquier analizador XML estándar puede analizar VML y entregar los datos resultantes a un procesador específico de VML.</span><span class="sxs-lookup"><span data-stu-id="d2695-143">Any standard XML parser can parse VML and hand off the resulting data to a VML-specific processor.</span></span> <span data-ttu-id="d2695-144">Para que los exploradores sepan cómo entregar los datos a un procesador específico de VML, debe escribir información como [espacios de nombres](web-workshop---how-to-use-vml-on-web-pages----appendix.md) y [objetos personalizados incrustados](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span><span class="sxs-lookup"><span data-stu-id="d2695-144">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) and [embedded custom objects](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span></span> <span data-ttu-id="d2695-145">Después, puede usar VML para escribir gráficos en la `<BODY>` región tal como hizo en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="d2695-145">You can then use VML to type graphics in the `<BODY>` region just as you did in the preceding example.</span></span>

<span data-ttu-id="d2695-146">El `"v:"` prefijo en cada etiqueta XML identifica la etiqueta como VML.</span><span class="sxs-lookup"><span data-stu-id="d2695-146">The `"v:"` prefix on each XML tag identifies the tag as VML.</span></span> <span data-ttu-id="d2695-147">El `"v:"` Prefijo de la `<BODY>` región debe ser coherente con `<html xmlns:v="...">` .</span><span class="sxs-lookup"><span data-stu-id="d2695-147">The `"v:"` prefix in the `<BODY>` region should be consistent with `<html xmlns:v="...">`.</span></span>

<span data-ttu-id="d2695-148">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="d2695-148">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="css-information"></a><span data-ttu-id="d2695-149">Información de CSS</span><span class="sxs-lookup"><span data-stu-id="d2695-149">CSS Information</span></span>

<span data-ttu-id="d2695-150">VML usa [hojas de estilo CSS, nivel 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) para determinar el tamaño de los gráficos y colocar los gráficos en una página web.</span><span class="sxs-lookup"><span data-stu-id="d2695-150">VML uses [Cascading Style Sheets, Level 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) to determine the size of the graphics and to position the graphics on a Web page.</span></span> <span data-ttu-id="d2695-151">En el ejemplo anterior, se especifica el tamaño del óvalo como 100 puntos (ancho) en 75 puntos (alto) ( `style='width:100pt;height:75pt'` ).</span><span class="sxs-lookup"><span data-stu-id="d2695-151">In the preceding example, we specified the size of the oval as 100 points (width) by 75 points (height) (`style='width:100pt;height:75pt'` ).</span></span>

<span data-ttu-id="d2695-152">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="d2695-152">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vml-elements"></a><span data-ttu-id="d2695-153">Elementos VML</span><span class="sxs-lookup"><span data-stu-id="d2695-153">VML Elements</span></span>

<span data-ttu-id="d2695-154">En el ejemplo anterior, usamos un elemento predefinido VML `<oval>` para dibujar un óvalo.</span><span class="sxs-lookup"><span data-stu-id="d2695-154">In the preceding example, we used a VML predefined `<oval>` element to draw an oval.</span></span> <span data-ttu-id="d2695-155">Después usamos el atributo **fillColor** Property del `<oval>` elemento para rellenar el óvalo con color rojo.</span><span class="sxs-lookup"><span data-stu-id="d2695-155">We then used the **fillcolor** property attribute of the `<oval>` element to fill the oval with red.</span></span>

<span data-ttu-id="d2695-156">En función de las etiquetas de [Inicio, las etiquetas de cierre y Empty-Element](https://www.w3.org/TR/REC-xml#sec-starttags) sección de etiquetas de [XML 1,0](https://www.w3.org/TR/REC-xml), las etiquetas de elementos vacíos se pueden usar para cualquier elemento que no tenga contenido.</span><span class="sxs-lookup"><span data-stu-id="d2695-156">Based upon the [Start-Tags, End-Tags, and Empty-Element Tags](https://www.w3.org/TR/REC-xml#sec-starttags) section of [XML 1.0 specification](https://www.w3.org/TR/REC-xml), empty-element tags may be used for any element that has no content.</span></span> <span data-ttu-id="d2695-157">Por ejemplo, tal y como se muestra en la siguiente representación VML, no hay contenido (subelemento) dentro del `<oval>` elemento.</span><span class="sxs-lookup"><span data-stu-id="d2695-157">For example, as shown in the following VML representation, there is no content (sub-element) within the `<oval>` element.</span></span> <span data-ttu-id="d2695-158">(Observe que el **estilo** y el **fillColor** son los atributos del `<oval>` elemento; no son elementos secundarios).</span><span class="sxs-lookup"><span data-stu-id="d2695-158">(Note that the **style** and **fillcolor** are the attributes of the `<oval>` element; they are not sub-elements.)</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



<span data-ttu-id="d2695-159">Por lo tanto, puede usar la etiqueta de elemento vacío, tal como se muestra en la siguiente representación de VML, para representar lo mismo que la línea anterior.</span><span class="sxs-lookup"><span data-stu-id="d2695-159">Therefore, you can use the empty-element tag, as shown in the following VML representation, to represent the same thing as the above line.</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



<span data-ttu-id="d2695-160">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="d2695-160">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="d2695-161">Resumen</span><span class="sxs-lookup"><span data-stu-id="d2695-161">Summary</span></span>

<span data-ttu-id="d2695-162">Puede usar VML para dibujar gráficos en una página web y, a continuación, personalizar esos gráficos simplemente cambiando sus atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d2695-162">You can use VML to draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span> <span data-ttu-id="d2695-163">Además, la mayoría de los gráficos representados en VML se representan más rápido en los exploradores y tardan menos tiempo en descargarse y en el espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="d2695-163">Also, most graphics represented in VML are rendered faster in browsers, and take less download time and disk space.</span></span>

 

 