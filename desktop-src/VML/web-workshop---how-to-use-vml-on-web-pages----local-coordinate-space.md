---
title: Usar el espacio de coordenadas local
description: Usar el espacio de coordenadas local
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- Web Workshop, espacio de coordenadas local
- diseñar páginas web, espacio de coordenadas local
- Lenguaje de marcado de vectores (VML), espacio de coordenadas local
- VML (Lenguaje de marcado de vectores), espacio de coordenadas local
- gráficos vectoriales, espacio de coordenadas local
- espacio de coordenadas local
- Formas VML, espacio de coordenadas local
- Lenguaje de marcado de vectores (VML), agrupar formas
- VML (Lenguaje de marcado de vectores), agrupar formas
- gráficos vectoriales, agrupar formas
- Formas VML, agrupación
- agrupar formas
- Lenguaje de marcado de vectores (VML), ajustar el tamaño de las formas
- VML (Lenguaje de marcado de vectores), ajustar el tamaño de las formas
- gráficos vectoriales, ajustar el tamaño de las formas
- Formas VML, escalado
- ajustar el tamaño de las formas
- Lenguaje de marcado de vectores (VML), ajustar el tamaño de las formas
- VML (Lenguaje de marcado de vectores), ajustar el tamaño de las formas
- gráficos vectoriales, ajustar el tamaño de las formas
- Formas VML, ajustar tamaño
- cambiar el tamaño de las formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c82d77ce16ae60bfc1249125d25b1139aeb8f44e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793450"
---
# <a name="using-local-coordinate-space"></a><span data-ttu-id="33532-125">Usar el espacio de coordenadas local</span><span class="sxs-lookup"><span data-stu-id="33532-125">Using Local Coordinate Space</span></span>

<span data-ttu-id="33532-126">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="33532-126">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="33532-127">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="33532-127">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="33532-128">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="33532-128">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="33532-129">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="33532-129">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="33532-130">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="33532-130">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="33532-131">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="33532-131">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="33532-132">Como ha aprendido, puede especificar los atributos de estilo **ancho** y **alto** para definir el tamaño de un cuadro contenedor en el que se representará el contenido de una forma o un grupo.</span><span class="sxs-lookup"><span data-stu-id="33532-132">As you've learned, you can specify the **width** and **height** style attributes to define the size of a containing box within which the contents of a shape or group will be rendered.</span></span> <span data-ttu-id="33532-133">En este tema, explicaremos qué espacio de coordenadas local es y cómo se usa en VML para escalar formas.</span><span class="sxs-lookup"><span data-stu-id="33532-133">In this topic, we will explain what Local Coordinate Space is, and how it is used in VML to scale shapes.</span></span>

<span data-ttu-id="33532-134">Si se le pidió que dibujara un rectángulo de una pulgada por dos pulgadas en una parte del papel de la cuadrícula, lo primero que desfigurarías es dónde empezar (el punto de origen).</span><span class="sxs-lookup"><span data-stu-id="33532-134">If you were asked to draw a one-inch by two-inch rectangle on a piece of grid paper, the first thing you would figure out is where to start (the originating point).</span></span> <span data-ttu-id="33532-135">A continuación, debería averiguar cómo asignar una pulgada a las celdas del papel de la cuadrícula (la coordenada).</span><span class="sxs-lookup"><span data-stu-id="33532-135">Then, you would figure out how to map one inch to the cells of the grid paper (the coordinate).</span></span>

<span data-ttu-id="33532-136">Del mismo modo, cuando el contenido de una forma o un grupo se representan dentro de su cuadro contenedor en una página web, se deben definir el punto de origen y la coordenada.</span><span class="sxs-lookup"><span data-stu-id="33532-136">Similarly, when the contents of a shape or group are rendered inside its containing box on a Web page, the originating point and the coordinate must be defined.</span></span> <span data-ttu-id="33532-137">VML proporciona el espacio de coordenadas local para permitir que cada forma o grupo defina su propio punto de origen y coordenada.</span><span class="sxs-lookup"><span data-stu-id="33532-137">VML provides Local Coordinate Space to allow each shape or group to define its own originating point and coordinate.</span></span> <span data-ttu-id="33532-138">Si no especifica un espacio de coordenadas, se usará el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="33532-138">If you don't specify a coordinate space, the default one will be used.</span></span> <span data-ttu-id="33532-139">De forma predeterminada, el origen comienza en la esquina superior izquierda del cuadro contenedor.</span><span class="sxs-lookup"><span data-stu-id="33532-139">By default, the origination starts at the top-left corner of the containing box.</span></span>

<span data-ttu-id="33532-140">Por ejemplo, la representación VML del óvalo rojo que se muestra a continuación no especifica los atributos de la propiedad **coordsize** y **coordorigin** .</span><span class="sxs-lookup"><span data-stu-id="33532-140">For example, the VML representation for the red oval shown below doesn't specify the **coordsize** and **coordorigin** property attributes.</span></span> <span data-ttu-id="33532-141">Por lo tanto, se utiliza un espacio de coordenadas local predeterminado.</span><span class="sxs-lookup"><span data-stu-id="33532-141">Therefore, a default local coordinate space is used.</span></span> <span data-ttu-id="33532-142">El tamaño del óvalo es 100 puntos (ancho) por 75 puntos (alto).</span><span class="sxs-lookup"><span data-stu-id="33532-142">The size of the oval is 100 points (width) by 75 points (height).</span></span> <span data-ttu-id="33532-143">Puede cambiar el tamaño del óvalo especificando otro ancho o alto, como ha aprendido en el tema formas de [escala](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) .</span><span class="sxs-lookup"><span data-stu-id="33532-143">You can resize the oval by specifying a different width or height, as you've learned in the [Scale Shapes](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) topic.</span></span>

![oval1.gif (627 bytes)](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





<span data-ttu-id="33532-145">Cuando la forma se vuelve más complicada, o cuando desea agrupar varias formas y escalarlas juntas, debe usar la característica de espacio de coordenadas local que se proporciona en VML.</span><span class="sxs-lookup"><span data-stu-id="33532-145">When the shape becomes more complicated, or when you would like to group several shapes and scale them together, you should use the Local Coordinate Space feature provided in VML.</span></span>

<span data-ttu-id="33532-146">Para cada forma o grupo, puede usar los atributos de la propiedad **coordsize** y **coordorigin** para definir el espacio de coordenadas local del grupo o de la forma.</span><span class="sxs-lookup"><span data-stu-id="33532-146">For each shape or group, you can use the **coordsize** and **coordorigin** property attributes to define the shape's or group's local coordinate space.</span></span> <span data-ttu-id="33532-147">El atributo **coordsize** especifica el número de unidades a lo largo del ancho y el alto del cuadro contenedor.</span><span class="sxs-lookup"><span data-stu-id="33532-147">The **coordsize** attribute specifies the number of units along the width and the height of the containing box.</span></span> <span data-ttu-id="33532-148">El atributo **coordorigin** define la coordenada en la esquina superior izquierda del cuadro contenedor.</span><span class="sxs-lookup"><span data-stu-id="33532-148">The **coordorigin** attribute defines the coordinate at the top left corner of the containing box.</span></span> <span data-ttu-id="33532-149">Toda la información relacionada con la posición (como el ancho, el alto, la izquierda, la parte superior, la ruta de acceso, etc.) se expresa en términos de la unidad en el espacio de coordenadas local.</span><span class="sxs-lookup"><span data-stu-id="33532-149">All position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span>

<span data-ttu-id="33532-150">Por ejemplo, como se muestra en la representación VML siguiente, `width: 100pt; height: 100pt;` define el tamaño del cuadro contenedor para que la forma sea 100 puntos por 100 puntos.</span><span class="sxs-lookup"><span data-stu-id="33532-150">For example, as shown in the following VML representation, `width: 100pt; height: 100pt;` defines the size of the containing box for the shape to be 100 points by 100 points.</span></span>

![cord1.gif (836 bytes)](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   <span data-ttu-id="33532-152">`coordsize="21600,21600"` define el tamaño del espacio de coordenadas local para que la forma sea 21600 unidades por 21600 unidades.</span><span class="sxs-lookup"><span data-stu-id="33532-152">`coordsize="21600,21600"` defines the size of the Local Coordinate Space for the shape to be 21600 units by 21600 units.</span></span> <span data-ttu-id="33532-153">Por lo tanto, una unidad en el espacio de coordenadas local es equivalente a 1/216 punto.</span><span class="sxs-lookup"><span data-stu-id="33532-153">Therefore, one unit in the Local Coordinate Space is equivalent to 1/216 point.</span></span>
-   <span data-ttu-id="33532-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` define el contorno de la forma como una forma de rombo.</span><span class="sxs-lookup"><span data-stu-id="33532-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` defines the outline of the shape as a diamond shape.</span></span> <span data-ttu-id="33532-155">Como hemos aprendido, toda la información relacionada con la posición (como el ancho, el alto, la izquierda, la parte superior, la ruta de acceso, etc.) se expresa en términos de la unidad en el espacio de coordenadas local.</span><span class="sxs-lookup"><span data-stu-id="33532-155">As we've learned, all position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span> <span data-ttu-id="33532-156">Por lo tanto, 10800 en el `<path>` significa 10800 unidades, que es equivalente a 50 puntos.</span><span class="sxs-lookup"><span data-stu-id="33532-156">Therefore, 10800 in the `<path>` means 10800 units, which is equivalent to 50 points.</span></span>

<span data-ttu-id="33532-157">Si desea cambiar el tamaño de esta forma de rombo, solo tiene que especificar un ancho o un alto distintos; es decir, no tiene que cambiar ningún valor de `<path>` .</span><span class="sxs-lookup"><span data-stu-id="33532-157">When you want to resize this diamond shape, simply specify a different width or height -- that's it; you don't have to change any value in the `<path>`.</span></span> <span data-ttu-id="33532-158">Para esta forma complicada, si no usó la característica de espacio de coordenadas local, tendría que cambiar todos los valores de cada vez que deseara cambiar su `<path>` tamaño.</span><span class="sxs-lookup"><span data-stu-id="33532-158">For this complicated shape, if you didn't use the Local Coordinate Space feature, you would have to change every value in the `<path>` whenever you wanted to resize it.</span></span>

<span data-ttu-id="33532-159">Por ejemplo, puede escalar la forma de rombo simplemente especificando un ancho o un alto distintos, tal como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="33532-159">For example, you can scale the diamond shape by simply specifying a different width or height, as shown in the following VML representation:</span></span>

![cord2.gif (1692 bytes)](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





<span data-ttu-id="33532-161">También puede usar el espacio de coordenadas local en el `<group>` elemento para que el contenido de todas las formas dentro del grupo se escale juntos según la misma coordenada.</span><span class="sxs-lookup"><span data-stu-id="33532-161">You can also use Local Coordinate Space in the `<group>` element so that the contents of all shapes within the group are scaled together according to the same coordinate.</span></span> <span data-ttu-id="33532-162">Después, siempre que quiera escalar o trasladar un grupo de formas, solo tiene que cambiar el ancho y el alto, o la configuración **coordsize** y **coordorigin** del grupo.</span><span class="sxs-lookup"><span data-stu-id="33532-162">Then, whenever you want to scale or move a group of shapes, simply change the width and height, or **coordsize** and **coordorigin** settings, of the group.</span></span>

<span data-ttu-id="33532-163">Por ejemplo, en la representación VML siguiente, `<v:group style='... width:200pt;height:200pt;'>` define el tamaño del cuadro contenedor para que el grupo sea 200 puntos por 200 puntos.</span><span class="sxs-lookup"><span data-stu-id="33532-163">For example, in the following VML representation, `<v:group style='... width:200pt;height:200pt;'>` defines the size of the containing box for the group to be 200 points by 200 points.</span></span>

![cord3.gif (645 bytes)](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   <span data-ttu-id="33532-165">`coordsize="1000,1000"` define el tamaño del espacio de coordenadas local para que el grupo sea 1000 unidades por 1000 unidades.</span><span class="sxs-lookup"><span data-stu-id="33532-165">`coordsize="1000,1000"` defines the size of the Local Coordinate Space for the group to be 1000 units by 1000 units.</span></span> <span data-ttu-id="33532-166">Por lo tanto, 1 unidad en el espacio de coordenadas local es equivalente a 1/5 punto.</span><span class="sxs-lookup"><span data-stu-id="33532-166">Therefore, 1 unit in the Local Coordinate Space is equivalent to 1/5 point.</span></span>
-   <span data-ttu-id="33532-167">`coordorigin="-500,-500"` define la esquina superior izquierda del cuadro contenedor para que sea "-500,-500".</span><span class="sxs-lookup"><span data-stu-id="33532-167">`coordorigin="-500,-500"` defines the top left corner of the containing box to be "-500, -500".</span></span> <span data-ttu-id="33532-168">Por lo tanto, el sistema de coordenadas dentro del cuadro que contiene va de-500 a 500 a lo largo del eje x y de-500 a 500 a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="33532-168">Therefore, the coordinate system inside the containing box ranges from -500 to 500 along the x-axis, and -500 to 500 along the y-axis.</span></span> <span data-ttu-id="33532-169">En otras palabras, el centro del cuadro contenedor es "0,0".</span><span class="sxs-lookup"><span data-stu-id="33532-169">In other words, the center of the containing box is "0, 0".</span></span>
-   <span data-ttu-id="33532-170">`<v:oval style='... width:400;height:300;'>` define el tamaño del cuadro contenedor para que el óvalo rojo sea 400 unidades (ancho) de 300 unidades (alto).</span><span class="sxs-lookup"><span data-stu-id="33532-170">`<v:oval style='... width:400;height:300;'>` defines the size of the containing box for the red oval to be 400 units (width) by 300 units (height).</span></span> <span data-ttu-id="33532-171">Dado que una unidad en el espacio de coordenadas local es equivalente a 1/5 punto, el tamaño del cuadro contenedor para el óvalo rojo es de 80 puntos (ancho) de 60 puntos (alto).</span><span class="sxs-lookup"><span data-stu-id="33532-171">Because one unit in the Local Coordinate Space is equivalent to 1/5 point, the size of the containing box for the red oval is 80 points (width) by 60 points (height).</span></span>

<span data-ttu-id="33532-172">Del mismo modo, el tamaño del cuadro contenedor para el roundrect verde es 50 puntos (ancho) por 40 puntos (alto).</span><span class="sxs-lookup"><span data-stu-id="33532-172">Similarly, the size of the containing box for the green roundrect is 50 points (width) by 40 points (height).</span></span>

<span data-ttu-id="33532-173">Cuando desee cambiar el tamaño del óvalo rojo y del roundrect verde, simplemente cambie `<v:group style='... width:200pt;height:200pt;'>` .</span><span class="sxs-lookup"><span data-stu-id="33532-173">When you want to to resize both the red oval and the green roundrect, simply change `<v:group style='... width:200pt;height:200pt;'>`.</span></span> <span data-ttu-id="33532-174">Es decir, no tiene que cambiar el tamaño de las dos formas de forma individual.</span><span class="sxs-lookup"><span data-stu-id="33532-174">That's it -- you don't have to individually change the size of the two shapes.</span></span>

<span data-ttu-id="33532-175">Por ejemplo, si cambia `<v:group style='... width:200pt;height:200pt;'>` a `<v:group style='... width:300pt;height:300pt;'>` , las formas serán mayores, tal como se muestra en la siguiente imagen:</span><span class="sxs-lookup"><span data-stu-id="33532-175">For example, if you change `<v:group style='... width:200pt;height:200pt;'>` to `<v:group style='... width:300pt;height:300pt;'>`, the shapes become larger, as shown in the following picture:</span></span>

![cord4.gif (943 bytes)](images/cord4.gif)



<span data-ttu-id="33532-177">También observará que las formas se encuentran de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="33532-177">You'd also notice that the shapes are located differently.</span></span> <span data-ttu-id="33532-178">Esto se debe a que las formas se dibujan desde "0,0", que se encuentra en el centro del cuadro contenedor.</span><span class="sxs-lookup"><span data-stu-id="33532-178">This is because the shapes are drawn from "0, 0" which is located at the center of the containing box.</span></span> <span data-ttu-id="33532-179">Como aumenta el tamaño del cuadro contenedor, también se mueve el centro del cuadro contenedor.</span><span class="sxs-lookup"><span data-stu-id="33532-179">Because you make the containing box bigger, the center of the containing box is also moved.</span></span>

<span data-ttu-id="33532-180">Si cambia `coordorigin="-500,-500"` a `coordorigin="0,0"` , como se muestra en la siguiente imagen, observará que el óvalo rojo y el roundrect verde se desplazan hacia arriba en la nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="33532-180">If you change `coordorigin="-500,-500"` to `coordorigin="0,0"`, as shown in the following picture, you'll notice that the red oval and the green roundrect are both shifted up to the new location.</span></span> <span data-ttu-id="33532-181">Esto se debe a que "0,0" ahora busca en la esquina superior izquierda del cuadro contenedor.</span><span class="sxs-lookup"><span data-stu-id="33532-181">This is because "0, 0" now locates at the top left corner of the containing box.</span></span>

![cord5.gif (648 bytes)](images/cord5.gif)



<span data-ttu-id="33532-183">También es importante tener en cuenta que el cuadro contenedor no establece una región de recorte.</span><span class="sxs-lookup"><span data-stu-id="33532-183">It is also important to note that the containing box does not establish a clipping region.</span></span> <span data-ttu-id="33532-184">Los gráficos se pueden dibujar fuera de los límites del cuadro contenedor.</span><span class="sxs-lookup"><span data-stu-id="33532-184">Graphics may be drawn outside the boundaries of the containing box.</span></span> <span data-ttu-id="33532-185">El cuadro contenedor solo sirve para asignar el espacio de coordenadas local al espacio de la página.</span><span class="sxs-lookup"><span data-stu-id="33532-185">The containing box merely serves to map the local coordinate space to the page space.</span></span>

<span data-ttu-id="33532-186">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span><span class="sxs-lookup"><span data-stu-id="33532-186">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span></span>

 

 