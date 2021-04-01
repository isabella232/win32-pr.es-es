---
title: Usar el elemento path
description: Usar el elemento path
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Web Workshop, elemento path
- diseñar páginas web, elemento path
- Lenguaje de marcado de vectores (VML), elemento path
- VML (Lenguaje de marcado de vectores), elemento path
- gráficos vectoriales, elemento path
- elemento path
- Elementos VML, ruta de acceso
- Formas VML, elemento path
- Lenguaje de marcado de vectores (VML), personalizar contornos de formas
- VML (Lenguaje de marcado de vectores), personalizar contornos de formas
- gráficos vectoriales, personalizar contornos de formas
- Formas VML, personalizar esquemas
- personalizar contornos de formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba82d0ab946ef8937b68b4934f9c4d928bd25225
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793462"
---
# <a name="using-the-path-element"></a><span data-ttu-id="5ca74-116">Usar el elemento path</span><span class="sxs-lookup"><span data-stu-id="5ca74-116">Using the Path Element</span></span>

<span data-ttu-id="5ca74-117">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5ca74-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5ca74-118">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="5ca74-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5ca74-119">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="5ca74-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5ca74-120">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="5ca74-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5ca74-121">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5ca74-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5ca74-122">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5ca74-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5ca74-123">Ha aprendido que puede usar los elementos de forma predefinidos de VML, como `<oval>` ,, `<line>` , `<polyline>` , `<curve>` `<rect>` , `<roundrect>` y `<arc>` --para dibujar una forma.</span><span class="sxs-lookup"><span data-stu-id="5ca74-123">You've learned that you can use the VML predefined shape elements -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` -- to draw a shape.</span></span> <span data-ttu-id="5ca74-124">En este tema, se muestra cómo usar el `<path>` subelemento para personalizar el contorno de una forma.</span><span class="sxs-lookup"><span data-stu-id="5ca74-124">In this topic, we will illustrate how to use the `<path>` sub-element to customize the outline of a shape.</span></span>

<span data-ttu-id="5ca74-125">Puede colocar el `<path>` subelemento dentro del `<shape>` `<shapetype>` elemento o.</span><span class="sxs-lookup"><span data-stu-id="5ca74-125">You can place the `<path>` sub-element inside the `<shape>` or `<shapetype>` element.</span></span> <span data-ttu-id="5ca74-126">Después, puede usar los atributos de propiedad del `<path>` subelemento para personalizar el contorno de la forma.</span><span class="sxs-lookup"><span data-stu-id="5ca74-126">You can then use the property attributes of the `<path>` sub-element to customize the outline of the shape.</span></span>

<span data-ttu-id="5ca74-127">Por ejemplo, para dibujar la forma personalizada que se muestra en la siguiente imagen, puede usar el `<path>` subelemento para definir el contorno de la forma, como se muestra en la siguiente representación de VML:</span><span class="sxs-lookup"><span data-stu-id="5ca74-127">For example, to draw the customized shape illustrated in the following picture, you can use the `<path>` sub-element to define the outline of the shape, as shown in the following VML representation:</span></span>

![shape1.gif (1301 bytes)](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   <span data-ttu-id="5ca74-129">Los valores `m 8,65` indican que el dibujo comienza en el punto (8, 65).</span><span class="sxs-lookup"><span data-stu-id="5ca74-129">The values `m 8,65` indicate that the drawing starts at the point (8,65).</span></span>
-   <span data-ttu-id="5ca74-130">Los valores `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indican que una línea recta comienza en el punto actual (8, 65) y termina en el punto especificado (72, 65), que se convierte en el nuevo punto actual.</span><span class="sxs-lookup"><span data-stu-id="5ca74-130">The values `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indicate that a straight line begins at the current point (8, 65) and ends at the given point (72, 65), which becomes the new current point.</span></span> <span data-ttu-id="5ca74-131">Una nueva línea comienza en el punto actual (72, 65) y termina en el punto dado, que se convierte en el nuevo punto actual, y así sucesivamente, al punto final (60, 100).</span><span class="sxs-lookup"><span data-stu-id="5ca74-131">A new line begins at the current point (72, 65) and ends at the given point, which becomes the new current point, and so on, to the final point (60, 100).</span></span>
-   <span data-ttu-id="5ca74-132">`x` indica que la ruta de acceso se cerrará con una línea recta que comienza en el punto actual (60, 100) y termina en el punto original (8, 65).</span><span class="sxs-lookup"><span data-stu-id="5ca74-132">`x` indicates that the path will close by a straight line that starts at the current point (60, 100) and ends at the original point (8, 65).</span></span>
-   <span data-ttu-id="5ca74-133">`e` indica detener dibujo.</span><span class="sxs-lookup"><span data-stu-id="5ca74-133">`e` indicates stop drawing.</span></span>

<span data-ttu-id="5ca74-134">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span><span class="sxs-lookup"><span data-stu-id="5ca74-134">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span></span>

 

 