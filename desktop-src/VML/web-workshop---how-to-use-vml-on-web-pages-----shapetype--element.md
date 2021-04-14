---
title: Usar el elemento TipoForma
description: Usar el elemento TipoForma
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Web Workshop, TipoForma (elemento)
- diseñar páginas web, TipoForma (elemento)
- Lenguaje de marcado de vectores (VML), elemento TipoForma
- VML (Lenguaje de marcado de vectores), elemento TipoForma
- Vector Graphics, TipoForma (elemento)
- TipoForma (elemento)
- Elementos VML, TipoForma
- Formas VML, elemento TipoForma
- Lenguaje de marcado de vectores (VML), definir formas usadas con frecuencia
- VML (Lenguaje de marcado de vectores), definir formas usadas con frecuencia
- gráficos vectoriales, definir formas usadas con frecuencia
- definir formas usadas con frecuencia
- Formas VML, definir las usadas con frecuencia
- Lenguaje de marcado de vectores (VML), crear instancias de copias de formas
- VML (Lenguaje de marcado de vectores), crear instancias de copias de formas
- gráficos vectoriales, crear instancias de copias de formas
- crear instancias de copias de formas
- Formas VML, crear instancias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa7ec47dde492231e8bcd54f68e4637454613b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488170"
---
# <a name="using-the-shapetype-element"></a><span data-ttu-id="7c983-121">Usar el elemento TipoForma</span><span class="sxs-lookup"><span data-stu-id="7c983-121">Using the Shapetype Element</span></span>

<span data-ttu-id="7c983-122">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7c983-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7c983-123">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="7c983-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7c983-124">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="7c983-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7c983-125">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="7c983-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7c983-126">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7c983-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7c983-127">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7c983-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7c983-128">En este tema, se muestra cómo usar el `<shapetype>` elemento para definir sus propias formas usadas con frecuencia y, a continuación, crear una instancia de las formas del TipoForma, o crearlas.</span><span class="sxs-lookup"><span data-stu-id="7c983-128">In this topic, we will illustrate how to use the `<shapetype>` element to define your own frequently-used shapes and then instantiate, or create, shapes from the shapetype.</span></span>

<span data-ttu-id="7c983-129">Si desea dibujar muchas formas que tienen las mismas propiedades o similares, sería tedioso si tuviera que escribir repetidamente los mismos atributos de propiedad para cada forma.</span><span class="sxs-lookup"><span data-stu-id="7c983-129">If you wanted to draw many shapes that have the same or similar properties, it would be tedious if you had to repeatedly type the same property attributes for each shape.</span></span> <span data-ttu-id="7c983-130">VML proporciona el `<shapetype>` elemento para que pueda definir un prototipo de una forma.</span><span class="sxs-lookup"><span data-stu-id="7c983-130">VML provides the `<shapetype>` element so that you can define a prototype of a shape.</span></span> <span data-ttu-id="7c983-131">Después, puede usar el `<shape>` elemento para crear instancias de muchas copias de formas del mismo TipoForma.</span><span class="sxs-lookup"><span data-stu-id="7c983-131">You can then use the `<shape>` element to instantiate many copies of shapes from the same shapetype.</span></span>

<span data-ttu-id="7c983-132">Puede seguir los tres pasos para definir un TipoForma y, a continuación, crear una instancia de una forma desde la TipoForma:</span><span class="sxs-lookup"><span data-stu-id="7c983-132">You can follow the three steps to define a shapetype, and then instantiate a shape from the shapetype:</span></span>

1.  <span data-ttu-id="7c983-133">Escriba un `<shapetype>` elemento y asígnele un nombre especificando el atributo id.</span><span class="sxs-lookup"><span data-stu-id="7c983-133">Type a `<shapetype>` element and give it a name by specifying the id attribute.</span></span>
2.  <span data-ttu-id="7c983-134">Describa el TipoForma mediante sus atributos o subelementos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7c983-134">Describe the shapetype by using its property attributes or sub-elements.</span></span>
3.  <span data-ttu-id="7c983-135">Cree una instancia de una forma escribiendo un `<shape>` elemento y haga referencia al atributo de tipo de la forma en el atributo ID del TipoForma.</span><span class="sxs-lookup"><span data-stu-id="7c983-135">Instantiate a shape by typing a `<shape>` element, and refer the type attribute of the shape to the id attribute of the shapetype.</span></span>

<span data-ttu-id="7c983-136">Por ejemplo, escriba las líneas siguientes para crear un TipoForma denominado "alshape":</span><span class="sxs-lookup"><span data-stu-id="7c983-136">For example, you type the following lines to create a shapetype called "MyShape":</span></span>


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



<span data-ttu-id="7c983-137">A continuación, modifique el TipoForma estableciendo algunos atributos de propiedad, como `fillcolor="red" strokecolor="blue"` .</span><span class="sxs-lookup"><span data-stu-id="7c983-137">Then, you alter the shapetype by setting some property attributes, such as `fillcolor="red" strokecolor="blue"`.</span></span> <span data-ttu-id="7c983-138">O bien, puede usar subelementos dentro del TipoForma, como `<path>` , `<fill>` , `<stroke>` (hablaremos sobre esos subelementos en temas posteriores).</span><span class="sxs-lookup"><span data-stu-id="7c983-138">Or, you can use sub-elements inside the shapetype, such as `<path>`, `<fill>`, `<stroke>` (we will talk about those sub-elements in later topics).</span></span>


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



<span data-ttu-id="7c983-139">A continuación, cree una instancia de una forma a partir de la sección TipoForma "conshape" especificando `type="#MyShape"` , tal y como se muestra en la siguiente representación de VML.</span><span class="sxs-lookup"><span data-stu-id="7c983-139">Then, you instantiate a shape from the shapetype "MyShape" by specifying `type="#MyShape"`, as shown in the following VML representation.</span></span> <span data-ttu-id="7c983-140">Esta forma hereda todas las propiedades del TipoForma ", y se muestra en el cuadro contenedor con un tamaño de 100 a 80.</span><span class="sxs-lookup"><span data-stu-id="7c983-140">This shape inherits all properties from the shapetype "MyShape", and is displayed within its containing box at a size of 100 by 80.</span></span>


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



<span data-ttu-id="7c983-141">Puede crear una instancia de otra forma desde la sección TipoForma "conshape" especificando `type="#MyShape"` y sobrescribiendo algunas propiedades, como `fillcolor="maroon"` , como se muestra en la siguiente representación VML.</span><span class="sxs-lookup"><span data-stu-id="7c983-141">You can instantiate another shape from the shapetype "MyShape" by specifying `type="#MyShape"` and overwrite some properties, such as `fillcolor="maroon"`, as shown in the following VML representation.</span></span> <span data-ttu-id="7c983-142">Esta forma hereda todas las propiedades de la sección TipoForma "disshape" excepto la propiedad fillColor y se muestra en el cuadro contenedor con un tamaño de 70 a 90.</span><span class="sxs-lookup"><span data-stu-id="7c983-142">This shape inherits all properties from the shapetype "MyShape" except the fillcolor property, and is displayed within its containing box at a size of 70 by 90.</span></span>


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



<span data-ttu-id="7c983-143">Esta es la representación VML completa del ejemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="7c983-143">Here is the complete VML representation for the preceding example:</span></span>

![\-1.gif tipo1 (477 bytes)](images/type1-1.gif)![\-2.gif tipo1 (471 bytes)](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





<span data-ttu-id="7c983-146">Como ha aprendido, cuando se crea una instancia de una forma a partir de un TipoForma, se heredan todos los atributos de propiedad del TipoForma.</span><span class="sxs-lookup"><span data-stu-id="7c983-146">As you've learned, when a shape is instantiated from a shapetype, it inherits all of the property attributes from the shapetype.</span></span> <span data-ttu-id="7c983-147">Puede sobrescribir algunos o todos los atributos heredados mediante la redefinición de los atributos dentro del `<shape>` elemento.</span><span class="sxs-lookup"><span data-stu-id="7c983-147">You can overwrite some or all of the inherited attributes by redefining attributes inside the `<shape>` element.</span></span> <span data-ttu-id="7c983-148">Tenga en cuenta que la herencia es solo un nivel.</span><span class="sxs-lookup"><span data-stu-id="7c983-148">Be aware that the inheritance is only one level.</span></span> <span data-ttu-id="7c983-149">Esto se debe a que solo un `<shape>` elemento puede hacer referencia a un `<shapetype>` elemento.</span><span class="sxs-lookup"><span data-stu-id="7c983-149">This is because only a `<shape>` element can reference a `<shapetype>` element.</span></span> <span data-ttu-id="7c983-150">Un `<shapetype>` elemento no puede hacer referencia A otro `<shapetype>` elemento.</span><span class="sxs-lookup"><span data-stu-id="7c983-150">A `<shapetype>` element cannot reference another `<shapetype>` element.</span></span>

<span data-ttu-id="7c983-151">Además, el TipoForma no pertenece a ningún grupo.</span><span class="sxs-lookup"><span data-stu-id="7c983-151">Also, a shapetype doesn't belong to any group.</span></span> <span data-ttu-id="7c983-152">Por lo tanto, el `<shapetype>` elemento puede aparecer por sí solo o dentro de un `<group>` elemento.</span><span class="sxs-lookup"><span data-stu-id="7c983-152">Therefore, the `<shapetype>` element can appear by itself or inside a `<group>` element.</span></span> <span data-ttu-id="7c983-153">Puede tener muchas formas dentro de grupos diferentes que hagan referencia al mismo TipoForma.</span><span class="sxs-lookup"><span data-stu-id="7c983-153">You can have many shapes inside different groups that reference the same shapetype.</span></span> <span data-ttu-id="7c983-154">Si aparece un TipoForma dentro de un grupo, una forma que vive en otro grupo puede seguir haciendo referencia a este TipoForma.</span><span class="sxs-lookup"><span data-stu-id="7c983-154">If a shapetype appears inside a group, a shape living in another group can still reference this shapetype.</span></span>

<span data-ttu-id="7c983-155">Por ejemplo, en la siguiente representación de VML, Rect1 y Rect2 están en GroupA y Rect3 está en GroupB.</span><span class="sxs-lookup"><span data-stu-id="7c983-155">For example, in the following VML representation, Rect1 and Rect2 are in GroupA, and Rect3 is in GroupB.</span></span> <span data-ttu-id="7c983-156">Se crean instancias de los tres rectángulos de la forma de TipoForma.</span><span class="sxs-lookup"><span data-stu-id="7c983-156">All three rectangles are instantiated from MyShape shapetype.</span></span>


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



<span data-ttu-id="7c983-157">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span><span class="sxs-lookup"><span data-stu-id="7c983-157">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span></span>

 

 