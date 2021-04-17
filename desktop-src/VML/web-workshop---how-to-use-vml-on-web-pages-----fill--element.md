---
title: Uso del elemento de relleno
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Web Workshop, elemento Fill
- diseñar páginas web, elemento Fill
- Lenguaje de marcado de vectores (VML), elemento Fill
- VML (Lenguaje de marcado de vectores), elemento Fill
- Vector Graphics, Fill (elemento)
- elemento Fill
- Elementos VML, relleno
- Formas VML, elemento Fill
- Lenguaje de marcado de vectores (VML), relleno degradado
- VML (Lenguaje de marcado de vectores), relleno degradado
- gráficos vectoriales, relleno degradado
- Formas VML, relleno degradado
- formas con relleno degradado
- Lenguaje de marcado de vectores (VML), relleno de patrón
- VML (Lenguaje de marcado de vectores), relleno de patrón
- gráficos vectoriales, relleno de patrón
- Formas VML, relleno de patrón
- formas rellenas de patrones
- Lenguaje de marcado de vectores (VML), relleno de imagen
- VML (Lenguaje de marcado de vectores), relleno de imagen
- gráficos vectoriales, relleno de imagen
- Formas VML, relleno de imagen
- formas rellenas de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf497a3120f53e24f1cff2bf7084469754bbaf7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104556203"
---
# <a name="using-the-fill-element"></a><span data-ttu-id="103b2-127">Uso del elemento de relleno</span><span class="sxs-lookup"><span data-stu-id="103b2-127">Using the Fill Element</span></span>

<span data-ttu-id="103b2-128">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="103b2-128">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="103b2-129">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="103b2-129">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="103b2-130">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="103b2-130">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="103b2-131">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="103b2-131">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="103b2-132">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="103b2-132">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="103b2-133">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="103b2-133">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="103b2-134">Como ha aprendido, puede usar el atributo de propiedad **fillColor** de un elemento de forma predefinido, como `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` , `<arc>` --para especificar el color que se utiliza para rellenar la forma.</span><span class="sxs-lookup"><span data-stu-id="103b2-134">As you've learned, you can use the **fillcolor** property attribute of a predefined shape element -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color that is used to fill the shape.</span></span> <span data-ttu-id="103b2-135">En este tema, se muestra cómo dibujar una forma que se rellena con efectos más avanzados.</span><span class="sxs-lookup"><span data-stu-id="103b2-135">In this topic, we will illustrate how to draw a shape that is filled with more advanced effects.</span></span>

<span data-ttu-id="103b2-136">Puede colocar el `<fill>` subelemento dentro de `<shape>` , o `<shapetype>` , o cualquier elemento de forma predefinido para describir cómo rellenar la forma.</span><span class="sxs-lookup"><span data-stu-id="103b2-136">You can place the `<fill>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span> <span data-ttu-id="103b2-137">Después, puede usar los atributos de propiedad del `<fill>` subelemento para personalizar el efecto de relleno, como [relleno de degradado](#gradient-fill), [relleno de patrón](#pattern-fill), [relleno de imagen](#picture-fill).</span><span class="sxs-lookup"><span data-stu-id="103b2-137">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](#gradient-fill), [pattern fill](#pattern-fill), [picture fill](#picture-fill).</span></span>

<span data-ttu-id="103b2-138">En este tema:</span><span class="sxs-lookup"><span data-stu-id="103b2-138">In this topic:</span></span>

-   [<span data-ttu-id="103b2-139">Relleno de degradado</span><span class="sxs-lookup"><span data-stu-id="103b2-139">Gradient Fill</span></span>](#gradient-fill)
-   [<span data-ttu-id="103b2-140">Relleno de patrón</span><span class="sxs-lookup"><span data-stu-id="103b2-140">Pattern Fill</span></span>](#pattern-fill)
-   [<span data-ttu-id="103b2-141">Relleno de imagen</span><span class="sxs-lookup"><span data-stu-id="103b2-141">Picture Fill</span></span>](#picture-fill)

## <a name="gradient-fill"></a><span data-ttu-id="103b2-142">Relleno de degradado</span><span class="sxs-lookup"><span data-stu-id="103b2-142">Gradient Fill</span></span>

<span data-ttu-id="103b2-143">Para dibujar una forma con relleno degradado, puede establecer el atributo de la propiedad **Type** del `<fill>` subelemento en "gradient" o "gradientRadial" y, a continuación, especificar otros atributos de propiedad del `<fill>` subelemento, como **método**, **color2**, **Focus** y **Angle**.</span><span class="sxs-lookup"><span data-stu-id="103b2-143">To draw a gradient-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "gradient" or "gradientRadial", and then specify other property attributes of the `<fill>` sub-element, such as **method**, **color2**, **focus**, and **angle**.</span></span>

<span data-ttu-id="103b2-144">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="103b2-144">**Examples:**</span></span>

<span data-ttu-id="103b2-145">Para crear una forma con relleno degradado horizontalmente, puede establecer el atributo de la propiedad **Type** en "degradado", como se muestra en la siguiente representación VML:</span><span class="sxs-lookup"><span data-stu-id="103b2-145">To create a shape that is gradient-filled horizontally, you can set the **type** property attribute to "gradient", as shown in the following VML representation:</span></span>

![horizontal1.gif (3055 bytes)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




<span data-ttu-id="103b2-147">Si cambia el atributo de la propiedad **fillColor** de la forma, la forma se rellena con un color diferente.</span><span class="sxs-lookup"><span data-stu-id="103b2-147">If you change the **fillcolor** property attribute of the shape, the shape is then gradient-filled with a different color.</span></span> <span data-ttu-id="103b2-148">Puede Agregar un segundo color especificando el atributo de la propiedad **color2** del `<fill>` subelemento.</span><span class="sxs-lookup"><span data-stu-id="103b2-148">You can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element.</span></span> <span data-ttu-id="103b2-149">Por ejemplo, para crear una forma con relleno degradado de dos colores, puede Agregar un segundo color especificando el atributo de propiedad **color2** del `<fill>` subelemento, tal como se muestra en la siguiente representación VML:</span><span class="sxs-lookup"><span data-stu-id="103b2-149">For example, to create a shape that is gradient-filled in two colors, you can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element, as shown in the following VML representation:</span></span>

![horizontal2.gif (3127 bytes)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




<span data-ttu-id="103b2-151">Puede establecer el atributo de la propiedad del **método** en "linear" o "Sigma" o "any" o "none".</span><span class="sxs-lookup"><span data-stu-id="103b2-151">You can set the **method** property attribute to "linear" or "sigma" or "any" or "none".</span></span> <span data-ttu-id="103b2-152">El efecto del degradado es ligeramente diferente.</span><span class="sxs-lookup"><span data-stu-id="103b2-152">The effect of the gradient is slightly different.</span></span> <span data-ttu-id="103b2-153">Además, puede usar el atributo de propiedad **Angle**,**Focus**,**focussize** o **focusposition** para cambiar el modo en que el degradado va.</span><span class="sxs-lookup"><span data-stu-id="103b2-153">Also, you can use the **angle**,**focus**,**focussize**, or **focusposition** property attribute to change how the gradient goes.</span></span>

<span data-ttu-id="103b2-154">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="103b2-154">**Examples:**</span></span>

 

<span data-ttu-id="103b2-155">Para crear una forma con relleno degradado verticalmente, puede establecer el atributo de propiedad de ángulo en Angle = "-90", como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="103b2-155">To create a shape that is gradient-filled vertically, you can set the angle property attribute to angle="-90", as shown in the following VML representation:</span></span>

![vertical1.gif (3836 bytes)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




<span data-ttu-id="103b2-157">Para crear una forma con relleno degradado desde el movimiento diagonal hacia arriba, puede establecer el atributo de propiedad de **ángulo** en Angle = "-135", como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="103b2-157">To create a shape that is gradient-filled from diagonal moving up, you can set the **angle** property attribute to angle="-135", as shown in the following VML representation:</span></span>

![dialgonalup1.gif (5816 bytes)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




<span data-ttu-id="103b2-159">Para crear una forma con relleno degradado desde el movimiento diagonal hacia abajo, puede establecer el atributo de propiedad de **ángulo** en Angle = "-45", como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="103b2-159">To create a shape that is gradient-filled from diagonal moving down, you can set the **angle** property attribute to angle="-45", as shown in the following VML representation:</span></span>

![diagonaldown1.gif (5753 bytes)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




<span data-ttu-id="103b2-161">Para crear una forma con relleno degradado desde el centro, puede especificar `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , tal como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="103b2-161">To create a shape that is gradient-filled from the center, you can specify `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"`, as shown in the following VML representation:</span></span>

![fromcenter1.gif (4598 bytes)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




<span data-ttu-id="103b2-163">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="103b2-163">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="pattern-fill"></a><span data-ttu-id="103b2-164">Relleno de patrón</span><span class="sxs-lookup"><span data-stu-id="103b2-164">Pattern Fill</span></span>

<span data-ttu-id="103b2-165">Para dibujar una forma con relleno de patrón, puede establecer el atributo de la propiedad **Type** del `<fill>` subelemento en "pattern" y, a continuación, especificar otros atributos de propiedad del `<fill>` subelemento, como **src** y **color2**.</span><span class="sxs-lookup"><span data-stu-id="103b2-165">To draw a pattern-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "pattern", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="103b2-166">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="103b2-166">**Examples:**</span></span>

<span data-ttu-id="103b2-167">Para crear una forma rellenada con una imagen de patrón, puede especificar el atributo de propiedad de **tipo** en "pattern" y apuntar el atributo de propiedad **src** a la ubicación del archivo de imagen de patrón, tal y como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="103b2-167">To create a shape that is filled with a pattern image, you can specify the **type** property attribute to "pattern", and point the **src** property attribute to the location of the pattern image file, as shown in the following VML representation:</span></span>

![pattern1.gif (872 bytes)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




<span data-ttu-id="103b2-169">Si apunta el atributo de propiedad **src** a un archivo de patrón diferente, puede crear una forma que se rellene con un patrón diferente.</span><span class="sxs-lookup"><span data-stu-id="103b2-169">If you point the **src** property attribute to a different pattern file, you can create a shape that is filled with a different pattern.</span></span> <span data-ttu-id="103b2-170">Además, puede cambiar el color especificando un valor diferente para el atributo de propiedad **fillColor** o **color2** , tal como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="103b2-170">Also, you can change the color by specifying a different value for the **fillcolor** or **color2** property attribute, as shown in the following VML representation:</span></span>

![pattern2.gif (831 bytes)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




<span data-ttu-id="103b2-172">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="103b2-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="picture-fill"></a><span data-ttu-id="103b2-173">Relleno de imagen</span><span class="sxs-lookup"><span data-stu-id="103b2-173">Picture Fill</span></span>

<span data-ttu-id="103b2-174">Para dibujar una forma con relleno de imagen, puede establecer el atributo de la propiedad **Type** del `<fill>` subelemento en "Frame" y, a continuación, especificar otros atributos de propiedad del `<fill>` subelemento, como **src** y **color2**.</span><span class="sxs-lookup"><span data-stu-id="103b2-174">To draw a picture-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "frame", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="103b2-175">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="103b2-175">**Examples:**</span></span>

<span data-ttu-id="103b2-176">Para crear una forma rellenada con un archivo de imagen, puede especificar el atributo de propiedad de **tipo** en "Frame" y, a continuación, apuntar el atributo de la propiedad **src** a la ubicación del archivo de imagen, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="103b2-176">To create a shape that is filled with a picture file, you can specify the **type** property attribute to "frame", and then point the **src** property attribute to the location of the picture file, as shown in the following VML representation:</span></span>

![picture1.gif (8496 bytes)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




<span data-ttu-id="103b2-178">Puede crear fácilmente una forma rellenada con una imagen diferente si apunta el atributo de propiedad **src** a otro archivo.</span><span class="sxs-lookup"><span data-stu-id="103b2-178">You can easily create a shape that is filled with a different picture by pointing the **src** property attribute to another file.</span></span>

<span data-ttu-id="103b2-179">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span><span class="sxs-lookup"><span data-stu-id="103b2-179">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span></span>

 

 