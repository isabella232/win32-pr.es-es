---
title: Uso del elemento de relleno
description: En este artículo se describe el uso del elemento Fill de VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Taller web, elemento fill
- diseñar páginas web, elemento fill
- Lenguaje de marcado de vectores (VML),elemento fill
- VML (Lenguaje de marcado de vectores),elemento fill
- gráficos vectoriales, elemento fill
- elemento fill
- Elementos VML, fill
- Formas de VML, elemento fill
- Lenguaje de marcado de vectores (VML), relleno de degradado
- VML (Lenguaje de marcado de vectores), relleno de degradado
- gráficos vectoriales, relleno de degradado
- Formas de VML, relleno de degradado
- formas rellenas de degradado
- Lenguaje de marcado de vectores (VML), relleno de patrón
- VML (Lenguaje de marcado de vectores), relleno de patrón
- gráficos vectoriales, relleno de patrón
- Formas de VML, relleno de patrón
- formas rellenas de patrones
- Lenguaje de marcado de vectores (VML),relleno de imagen
- VML (Lenguaje de marcado de vectores), relleno de imagen
- gráficos vectoriales, relleno de imagen
- Formas de VML, relleno de imagen
- formas rellenas de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb243e4896443fd36a1b22c2ac3a0ab0bedfb2b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407798"
---
# <a name="using-the-fill-element"></a><span data-ttu-id="1d219-126">Uso del elemento de relleno</span><span class="sxs-lookup"><span data-stu-id="1d219-126">Using the Fill Element</span></span>

<span data-ttu-id="1d219-127">En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1d219-127">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1d219-128">Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="1d219-128">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1d219-129">A partir de diciembre de 2011, este tema se archivó.</span><span class="sxs-lookup"><span data-stu-id="1d219-129">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1d219-130">Como resultado, ya no se mantiene activamente.</span><span class="sxs-lookup"><span data-stu-id="1d219-130">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1d219-131">Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="1d219-131">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1d219-132">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1d219-132">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1d219-133">Como ha aprendido, puede usar el atributo de propiedad **fillcolor** de un elemento de forma predefinido( como , , , , , , ) para especificar el color que se usa para rellenar la `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma.</span><span class="sxs-lookup"><span data-stu-id="1d219-133">As you've learned, you can use the **fillcolor** property attribute of a predefined shape element -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color that is used to fill the shape.</span></span> <span data-ttu-id="1d219-134">En este tema, se ilustrará cómo dibujar una forma que se rellena con efectos más avanzados.</span><span class="sxs-lookup"><span data-stu-id="1d219-134">In this topic, we will illustrate how to draw a shape that is filled with more advanced effects.</span></span>

<span data-ttu-id="1d219-135">Puede colocar el sub element dentro de , o , o cualquier elemento de forma predefinido para `<fill>` describir cómo rellenar la `<shape>` `<shapetype>` forma.</span><span class="sxs-lookup"><span data-stu-id="1d219-135">You can place the `<fill>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span> <span data-ttu-id="1d219-136">A continuación, puede usar los atributos de propiedad del sub elemento para personalizar el efecto de relleno, como relleno de `<fill>` [degradado,](#gradient-fill)relleno [de](#pattern-fill)patrón, relleno [de imagen.](#picture-fill)</span><span class="sxs-lookup"><span data-stu-id="1d219-136">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](#gradient-fill), [pattern fill](#pattern-fill), [picture fill](#picture-fill).</span></span>

<span data-ttu-id="1d219-137">En este tema:</span><span class="sxs-lookup"><span data-stu-id="1d219-137">In this topic:</span></span>

-   [<span data-ttu-id="1d219-138">Relleno de degradado</span><span class="sxs-lookup"><span data-stu-id="1d219-138">Gradient Fill</span></span>](#gradient-fill)
-   [<span data-ttu-id="1d219-139">Relleno de patrón</span><span class="sxs-lookup"><span data-stu-id="1d219-139">Pattern Fill</span></span>](#pattern-fill)
-   [<span data-ttu-id="1d219-140">Relleno de imagen</span><span class="sxs-lookup"><span data-stu-id="1d219-140">Picture Fill</span></span>](#picture-fill)

## <a name="gradient-fill"></a><span data-ttu-id="1d219-141">Relleno de degradado</span><span class="sxs-lookup"><span data-stu-id="1d219-141">Gradient Fill</span></span>

<span data-ttu-id="1d219-142">Para dibujar una forma rellena de  degradado, puede establecer el atributo de propiedad de tipo del sub elemento en "gradient" o "gradientRadial" y, a continuación, especificar otros atributos de propiedad del sub elemento, como el método `<fill>` `<fill>` , **color2**, **el foco** y el **ángulo**.</span><span class="sxs-lookup"><span data-stu-id="1d219-142">To draw a gradient-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "gradient" or "gradientRadial", and then specify other property attributes of the `<fill>` sub-element, such as **method**, **color2**, **focus**, and **angle**.</span></span>

<span data-ttu-id="1d219-143">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="1d219-143">**Examples:**</span></span>

<span data-ttu-id="1d219-144">Para crear una forma con relleno de degradado  horizontalmente, puede establecer el atributo de propiedad de tipo en "degradado", como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="1d219-144">To create a shape that is gradient-filled horizontally, you can set the **type** property attribute to "gradient", as shown in the following VML representation:</span></span>

![horizontal1.gif (3055 bytes)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




<span data-ttu-id="1d219-146">Si cambia el atributo **de propiedad fillcolor** de la forma, la forma se rellena con degradado con un color diferente.</span><span class="sxs-lookup"><span data-stu-id="1d219-146">If you change the **fillcolor** property attribute of the shape, the shape is then gradient-filled with a different color.</span></span> <span data-ttu-id="1d219-147">Puede agregar un segundo color especificando el atributo de propiedad **color2** del `<fill>` sub elemento.</span><span class="sxs-lookup"><span data-stu-id="1d219-147">You can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element.</span></span> <span data-ttu-id="1d219-148">Por ejemplo, para crear una forma que se rellena con degradado en dos colores, puede agregar un segundo color especificando el atributo de propiedad **color2** del sub elemento, como se muestra en la siguiente representación `<fill>` de VML:</span><span class="sxs-lookup"><span data-stu-id="1d219-148">For example, to create a shape that is gradient-filled in two colors, you can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element, as shown in the following VML representation:</span></span>

![horizontal2.gif (3127 bytes)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




<span data-ttu-id="1d219-150">Puede establecer el atributo **de propiedad** del método en "linear" o "sigma", "any" o "none".</span><span class="sxs-lookup"><span data-stu-id="1d219-150">You can set the **method** property attribute to "linear" or "sigma" or "any" or "none".</span></span> <span data-ttu-id="1d219-151">El efecto del degradado es ligeramente diferente.</span><span class="sxs-lookup"><span data-stu-id="1d219-151">The effect of the gradient is slightly different.</span></span> <span data-ttu-id="1d219-152">Además, puede usar el atributo de propiedad **angle**,**focus**,**focussize** o **focusposition** para cambiar cómo va el degradado.</span><span class="sxs-lookup"><span data-stu-id="1d219-152">Also, you can use the **angle**,**focus**,**focussize**, or **focusposition** property attribute to change how the gradient goes.</span></span>

<span data-ttu-id="1d219-153">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="1d219-153">**Examples:**</span></span>

 

<span data-ttu-id="1d219-154">Para crear una forma que se rellena verticalmente con degradado, puede establecer el atributo de propiedad de ángulo en angle="-90", como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="1d219-154">To create a shape that is gradient-filled vertically, you can set the angle property attribute to angle="-90", as shown in the following VML representation:</span></span>

![vertical1.gif (3836 bytes)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




<span data-ttu-id="1d219-156">Para crear una forma rellena de degradado desde la  diagonal hacia arriba, puede establecer el atributo de propiedad de ángulo en angle="-135", como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="1d219-156">To create a shape that is gradient-filled from diagonal moving up, you can set the **angle** property attribute to angle="-135", as shown in the following VML representation:</span></span>

![dialgonalup1.gif (5816 bytes)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




<span data-ttu-id="1d219-158">Para crear una forma rellena de degradado desde la  diagonal hacia abajo, puede establecer el atributo de propiedad de ángulo en angle="-45", como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="1d219-158">To create a shape that is gradient-filled from diagonal moving down, you can set the **angle** property attribute to angle="-45", as shown in the following VML representation:</span></span>

![diagonaldown1.gif (5753 bytes)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




<span data-ttu-id="1d219-160">Para crear una forma rellena de degradado desde el centro, puede especificar , como se `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="1d219-160">To create a shape that is gradient-filled from the center, you can specify `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"`, as shown in the following VML representation:</span></span>

![fromcenter1.gif (4598 bytes)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




<span data-ttu-id="1d219-162">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="1d219-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="pattern-fill"></a><span data-ttu-id="1d219-163">Relleno de patrón</span><span class="sxs-lookup"><span data-stu-id="1d219-163">Pattern Fill</span></span>

<span data-ttu-id="1d219-164">Para dibujar una forma rellena de  patrón, puede establecer el atributo de propiedad type del sub element en "pattern" y, a continuación, especificar otros atributos de propiedad del sub element, como `<fill>` `<fill>` **src** **y color2.**</span><span class="sxs-lookup"><span data-stu-id="1d219-164">To draw a pattern-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "pattern", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="1d219-165">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="1d219-165">**Examples:**</span></span>

<span data-ttu-id="1d219-166">Para crear una forma que se rellena con  una imagen de patrón, puede especificar el atributo de propiedad type en "pattern" y apuntar el atributo de propiedad **src** a la ubicación del archivo de imagen de patrón, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="1d219-166">To create a shape that is filled with a pattern image, you can specify the **type** property attribute to "pattern", and point the **src** property attribute to the location of the pattern image file, as shown in the following VML representation:</span></span>

![pattern1.gif (872 bytes)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




<span data-ttu-id="1d219-168">Si señala el atributo **de propiedad src** a un archivo de patrón diferente, puede crear una forma que se rellena con un patrón diferente.</span><span class="sxs-lookup"><span data-stu-id="1d219-168">If you point the **src** property attribute to a different pattern file, you can create a shape that is filled with a different pattern.</span></span> <span data-ttu-id="1d219-169">Además, puede cambiar el color especificando un valor diferente para el atributo de propiedad **fillcolor** o **color2,** como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="1d219-169">Also, you can change the color by specifying a different value for the **fillcolor** or **color2** property attribute, as shown in the following VML representation:</span></span>

![pattern2.gif (831 bytes)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




<span data-ttu-id="1d219-171">[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="1d219-171">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="picture-fill"></a><span data-ttu-id="1d219-172">Relleno de imagen</span><span class="sxs-lookup"><span data-stu-id="1d219-172">Picture Fill</span></span>

<span data-ttu-id="1d219-173">Para dibujar una forma rellena de  imagen, puede establecer el atributo de propiedad type del sub elemento en "frame" y, a continuación, especificar otros atributos de propiedad del sub elemento, como `<fill>` `<fill>` **src** y **color2.**</span><span class="sxs-lookup"><span data-stu-id="1d219-173">To draw a picture-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "frame", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="1d219-174">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="1d219-174">**Examples:**</span></span>

<span data-ttu-id="1d219-175">Para crear una forma que se rellena con  un archivo de imagen, puede especificar el atributo de propiedad type en "frame" y, a continuación, apuntar el atributo de propiedad **src** a la ubicación del archivo de imagen, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="1d219-175">To create a shape that is filled with a picture file, you can specify the **type** property attribute to "frame", and then point the **src** property attribute to the location of the picture file, as shown in the following VML representation:</span></span>

![picture1.gif (8496 bytes)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




<span data-ttu-id="1d219-177">Puede crear fácilmente una forma que se rellena con una imagen diferente señalando el atributo de propiedad **src** a otro archivo.</span><span class="sxs-lookup"><span data-stu-id="1d219-177">You can easily create a shape that is filled with a different picture by pointing the **src** property attribute to another file.</span></span>

<span data-ttu-id="1d219-178">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span><span class="sxs-lookup"><span data-stu-id="1d219-178">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span></span>

 

 