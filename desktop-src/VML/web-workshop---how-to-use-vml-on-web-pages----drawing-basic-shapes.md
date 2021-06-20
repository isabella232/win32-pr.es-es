---
title: Dibujar formas básicas
description: En este artículo se describe el dibujo de formas básicas en VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Taller web, dibujar formas
- diseñar páginas web, dibujar formas
- Lenguaje de marcado de vectores (VML),dibujar formas
- VML (Lenguaje de marcado de vectores),dibujar formas
- gráficos vectoriales, dibujar formas
- dibujar formas
- Formas de VML, dibujo
- Lenguaje de marcado de vectores (VML),XML
- VML (Lenguaje de marcado de vectores),XML
- gráficos vectoriales, XML
- Lenguaje de marcado de vectores (VML),CSS2
- VML (Lenguaje de marcado de vectores),CSS2
- gráficos vectoriales, CSS2
- Lenguaje de marcado de vectores (VML),elements
- VML (Lenguaje de marcado de vectores),elements
- gráficos vectoriales, elementos
- Elementos VML, dibujar formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00701e8ac77bd5bda7156c04ca25427d131646bf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407738"
---
# <a name="drawing-basic-shapes"></a><span data-ttu-id="165bf-120">Dibujar formas básicas</span><span class="sxs-lookup"><span data-stu-id="165bf-120">Drawing Basic Shapes</span></span>

<span data-ttu-id="165bf-121">En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="165bf-121">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="165bf-122">Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="165bf-122">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="165bf-123">A partir de diciembre de 2011, este tema se archivó.</span><span class="sxs-lookup"><span data-stu-id="165bf-123">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="165bf-124">Como resultado, ya no se mantiene activamente.</span><span class="sxs-lookup"><span data-stu-id="165bf-124">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="165bf-125">Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="165bf-125">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="165bf-126">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="165bf-126">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="165bf-127">En este tema, mostraremos lo fácil que es dibujar una forma mediante VML.</span><span class="sxs-lookup"><span data-stu-id="165bf-127">In this topic, we will illustrate how easy it is to draw a shape using VML.</span></span>

<span data-ttu-id="165bf-128">Para crear un óvalo rojo en una página web, como se muestra en la siguiente imagen, puede dibujar el óvalo mediante una herramienta de edición gráfica, guardar el dibujo como mapa de bits e insertar el mapa de bits en la página web:</span><span class="sxs-lookup"><span data-stu-id="165bf-128">To create a red oval on a Web page, as shown in the following picture, you can draw the oval by using a graphic edit tool, save your drawing as a bitmap, and then insert the bitmap on your Web page:</span></span>

![oval1.gif (627 bytes)](images/oval1.gif)

<span data-ttu-id="165bf-130">Como alternativa, puede usar VML para dibujar gráficos.</span><span class="sxs-lookup"><span data-stu-id="165bf-130">Alternatively, you can use VML to draw graphics.</span></span> <span data-ttu-id="165bf-131">En el ejemplo anterior, puede escribir las siguientes líneas en la región de `<BODY>` la página web para dibujar el óvalo rojo:</span><span class="sxs-lookup"><span data-stu-id="165bf-131">In the preceding example, you can type the following lines in the `<BODY>` region of your Web page to draw the red oval:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





<span data-ttu-id="165bf-132">`<v:...>` y `</v:...>` son la etiqueta de inicio y la etiqueta final en la [sintaxis XML](#xml-structure).`style='width:100pt; height:75pt'`</span><span class="sxs-lookup"><span data-stu-id="165bf-132">`<v:...>` and `</v:...>` are the start tag and end tag in [XML syntax](#xml-structure).`style='width:100pt; height:75pt'`</span></span> <span data-ttu-id="165bf-133">proporciona [información de CSS](#css-information).</span><span class="sxs-lookup"><span data-stu-id="165bf-133">provides [CSS information](#css-information).</span></span> <span data-ttu-id="165bf-134">**oval** y **fillcolor**="red" son [elementos VML.](#vml-elements)</span><span class="sxs-lookup"><span data-stu-id="165bf-134">**oval** and **fillcolor**="red" are [VML elements](#vml-elements).</span></span>

<span data-ttu-id="165bf-135">Puede modificar los gráficos simplemente cambiando sus atributos de propiedad en VML.</span><span class="sxs-lookup"><span data-stu-id="165bf-135">You can alter the graphics by simply changing their property attributes in VML.</span></span> <span data-ttu-id="165bf-136">En el ejemplo anterior, si cambia a , como se muestra en la siguiente representación `fillcolor="red"` `fillcolor="blue"` de VML, el óvalo rojo cambiará a azul:</span><span class="sxs-lookup"><span data-stu-id="165bf-136">In the preceding example, if you change `fillcolor="red"` to `fillcolor="blue"`, as shown in the following VML representation, the red oval will change to blue:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





<span data-ttu-id="165bf-137">Los exploradores que admiten VML pueden representar y mostrar los gráficos representados en VML sin tener que descargar archivos de imagen independientes.</span><span class="sxs-lookup"><span data-stu-id="165bf-137">Browsers that support VML can render and display the graphics represented in VML without having to download separate image files.</span></span> <span data-ttu-id="165bf-138">La mayoría de los gráficos representados en VML se representan más rápido en los exploradores y requieren menos espacio en disco y tiempo de descarga.</span><span class="sxs-lookup"><span data-stu-id="165bf-138">Most graphics represented in VML are rendered faster in browsers, and require less disk space and download time.</span></span>

<span data-ttu-id="165bf-139">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="165bf-139">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="xml-structure"></a><span data-ttu-id="165bf-140">Estructura XML</span><span class="sxs-lookup"><span data-stu-id="165bf-140">XML Structure</span></span>

<span data-ttu-id="165bf-141">VmL tiene formato según las reglas de lenguaje de marcado extensible (XML).</span><span class="sxs-lookup"><span data-stu-id="165bf-141">VML is formatted according to the rules of Extensible Markup Language (XML).</span></span> <span data-ttu-id="165bf-142">Cualquier analizador XML estándar puede analizar VML y entregar los datos resultantes a un procesador específico de VML.</span><span class="sxs-lookup"><span data-stu-id="165bf-142">Any standard XML parser can parse VML and hand off the resulting data to a VML-specific processor.</span></span> <span data-ttu-id="165bf-143">Para que los exploradores sepan cómo entregar datos a un procesador específico de VML, debe escribir información como espacios de nombres y objetos [personalizados](web-workshop---how-to-use-vml-on-web-pages----appendix.md) [incrustados.](web-workshop---how-to-use-vml-on-web-pages----appendix.md)</span><span class="sxs-lookup"><span data-stu-id="165bf-143">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) and [embedded custom objects](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span></span> <span data-ttu-id="165bf-144">A continuación, puede usar VML para escribir gráficos en la `<BODY>` región como hizo en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="165bf-144">You can then use VML to type graphics in the `<BODY>` region just as you did in the preceding example.</span></span>

<span data-ttu-id="165bf-145">El `"v:"` prefijo de cada etiqueta XML identifica la etiqueta como VML.</span><span class="sxs-lookup"><span data-stu-id="165bf-145">The `"v:"` prefix on each XML tag identifies the tag as VML.</span></span> <span data-ttu-id="165bf-146">El `"v:"` prefijo de la región debe ser coherente con `<BODY>` `<html xmlns:v="...">` .</span><span class="sxs-lookup"><span data-stu-id="165bf-146">The `"v:"` prefix in the `<BODY>` region should be consistent with `<html xmlns:v="...">`.</span></span>

<span data-ttu-id="165bf-147">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="165bf-147">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="css-information"></a><span data-ttu-id="165bf-148">Información de CSS</span><span class="sxs-lookup"><span data-stu-id="165bf-148">CSS Information</span></span>

<span data-ttu-id="165bf-149">VML usa [Hojas de estilo CSS nivel 2 (CSS2) para](https://www.w3.org/TR/PR-CSS2/) determinar el tamaño de los gráficos y colocar los gráficos en una página web.</span><span class="sxs-lookup"><span data-stu-id="165bf-149">VML uses [Cascading Style Sheets, Level 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) to determine the size of the graphics and to position the graphics on a Web page.</span></span> <span data-ttu-id="165bf-150">En el ejemplo anterior, especificamos el tamaño del óvalo como 100 puntos (ancho) por 75 puntos (alto) ( `style='width:100pt;height:75pt'` ).</span><span class="sxs-lookup"><span data-stu-id="165bf-150">In the preceding example, we specified the size of the oval as 100 points (width) by 75 points (height) (`style='width:100pt;height:75pt'` ).</span></span>

<span data-ttu-id="165bf-151">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="165bf-151">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vml-elements"></a><span data-ttu-id="165bf-152">Elementos VML</span><span class="sxs-lookup"><span data-stu-id="165bf-152">VML Elements</span></span>

<span data-ttu-id="165bf-153">En el ejemplo anterior, se usó un elemento predefinido vml `<oval>` para dibujar un óvalo.</span><span class="sxs-lookup"><span data-stu-id="165bf-153">In the preceding example, we used a VML predefined `<oval>` element to draw an oval.</span></span> <span data-ttu-id="165bf-154">A continuación, se usa el atributo de propiedad **fillcolor** del `<oval>` elemento para rellenar el óvalo con rojo.</span><span class="sxs-lookup"><span data-stu-id="165bf-154">We then used the **fillcolor** property attribute of the `<oval>` element to fill the oval with red.</span></span>

<span data-ttu-id="165bf-155">Según la sección Etiquetas de [inicio,](https://www.w3.org/TR/REC-xml#sec-starttags) Etiquetas finales y etiquetas Empty-Element de la especificación [XML 1.0,](https://www.w3.org/TR/REC-xml)las etiquetas de elemento vacío se pueden usar para cualquier elemento que no tenga contenido.</span><span class="sxs-lookup"><span data-stu-id="165bf-155">Based upon the [Start-Tags, End-Tags, and Empty-Element Tags](https://www.w3.org/TR/REC-xml#sec-starttags) section of [XML 1.0 specification](https://www.w3.org/TR/REC-xml), empty-element tags may be used for any element that has no content.</span></span> <span data-ttu-id="165bf-156">Por ejemplo, como se muestra en la siguiente representación de VML, no hay contenido (sub element) dentro del `<oval>` elemento.</span><span class="sxs-lookup"><span data-stu-id="165bf-156">For example, as shown in the following VML representation, there is no content (sub-element) within the `<oval>` element.</span></span> <span data-ttu-id="165bf-157">(Tenga en cuenta **que el estilo** **y el color de relleno** son los atributos del `<oval>` elemento; no son sub-elementos).</span><span class="sxs-lookup"><span data-stu-id="165bf-157">(Note that the **style** and **fillcolor** are the attributes of the `<oval>` element; they are not sub-elements.)</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



<span data-ttu-id="165bf-158">Por lo tanto, puede usar la etiqueta empty-element, como se muestra en la siguiente representación de VML, para representar lo mismo que la línea anterior.</span><span class="sxs-lookup"><span data-stu-id="165bf-158">Therefore, you can use the empty-element tag, as shown in the following VML representation, to represent the same thing as the above line.</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



<span data-ttu-id="165bf-159">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="165bf-159">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="165bf-160">Resumen</span><span class="sxs-lookup"><span data-stu-id="165bf-160">Summary</span></span>

<span data-ttu-id="165bf-161">Puede usar VML para dibujar gráficos en una página web y, a continuación, personalizar esos gráficos simplemente cambiando sus atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="165bf-161">You can use VML to draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span> <span data-ttu-id="165bf-162">Además, la mayoría de los gráficos representados en VML se representan más rápido en los exploradores y toman menos tiempo de descarga y espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="165bf-162">Also, most graphics represented in VML are rendered faster in browsers, and take less download time and disk space.</span></span>

 

 