---
title: Colores de formas
description: En este artículo se describe la coloración de formas en VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Taller web, colores de formas
- diseñar páginas web, colorear formas
- Lenguaje de marcado de vectores (VML), colores de formas
- VML (Lenguaje de marcado de vectores), colores de formas
- gráficos vectoriales, colores de formas
- Formas de VML, colores
- colores de formas
- Lenguaje de marcado de vectores (VML),nombres de color de palabra clave
- VML (Lenguaje de marcado de vectores),nombres de color de palabra clave
- gráficos vectoriales, nombres de color de palabra clave
- nombres de color de palabra clave
- Lenguaje de marcado de vectores (VML), trillizos RGB
- VML (Lenguaje de marcado de vectores),trillizos RGB
- gráficos vectoriales, triplets RGB
- Tripletes RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c203debd01d4234ae58900a023944511f9fc73c1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407748"
---
# <a name="coloring-shapes"></a><span data-ttu-id="9424c-118">Colores de formas</span><span class="sxs-lookup"><span data-stu-id="9424c-118">Coloring Shapes</span></span>

<span data-ttu-id="9424c-119">En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9424c-119">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9424c-120">Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="9424c-120">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9424c-121">A partir de diciembre de 2011, este tema se archivó.</span><span class="sxs-lookup"><span data-stu-id="9424c-121">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9424c-122">Como resultado, ya no se mantiene activamente.</span><span class="sxs-lookup"><span data-stu-id="9424c-122">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9424c-123">Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="9424c-123">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9424c-124">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9424c-124">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9424c-125">Como se mencionó en secciones anteriores, puede usar "rojo" para representar un color en rojo, "azul" para representar un color en azul, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="9424c-125">As we mentioned in earlier sections, you can use "red" to represent a color in red, "blue" to represent a color in blue, and so on.</span></span> <span data-ttu-id="9424c-126">En este tema, se ilustrará cómo dibujar formas en el color que desee.</span><span class="sxs-lookup"><span data-stu-id="9424c-126">In this topic, we will illustrate how to draw shapes in any color you want.</span></span>

<span data-ttu-id="9424c-127">VML extiende la sintaxis de color HTML y CSS.</span><span class="sxs-lookup"><span data-stu-id="9424c-127">VML extends HTML and CSS color syntax.</span></span> <span data-ttu-id="9424c-128">Cuando el tipo de atributo de un elemento VML es color , como **fillcolor** y **strokecolor,** puede expresar el color mediante un nombre de [color](#keyword-color-name) de palabra clave o un [triplete RGB](#rgb-triplet).</span><span class="sxs-lookup"><span data-stu-id="9424c-128">When the attribute type of a VML element is color -- such as **fillcolor** and **strokecolor** -- you can express the color by using either a [keyword color name](#keyword-color-name) or an [RGB triplet](#rgb-triplet).</span></span>

<span data-ttu-id="9424c-129">[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="9424c-129">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="keyword-color-name"></a><span data-ttu-id="9424c-130">Nombre de color de palabra clave</span><span class="sxs-lookup"><span data-stu-id="9424c-130">Keyword Color Name</span></span>

<span data-ttu-id="9424c-131">HTML 4.0 define una lista de nombres de color de palabra clave.</span><span class="sxs-lookup"><span data-stu-id="9424c-131">HTML 4.0 defines a list of keyword color names.</span></span> <span data-ttu-id="9424c-132">Son aqua, black, blue, brewia, gray, green, lime, maroon, brew, purple, red, silver, teal, white y yellow.</span><span class="sxs-lookup"><span data-stu-id="9424c-132">They are aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, and yellow.</span></span> <span data-ttu-id="9424c-133">El valor RGB de estos 16 colores se define en la [especificación HTML 4.0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span><span class="sxs-lookup"><span data-stu-id="9424c-133">The RGB value for these 16 colors are defined in [HTML 4.0 specification](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span></span>

<span data-ttu-id="9424c-134">Por ejemplo, puede dibujar un rectángulo relleno con amarillo especificando y darle un contorno azul especificando , como se muestra en la siguiente representación `fillcolor="yellow"` `strokecolor="blue"` de VML:</span><span class="sxs-lookup"><span data-stu-id="9424c-134">For example, you can draw a rectangle filled with yellow by specifying `fillcolor="yellow"`, and give it a blue outline by specifying `strokecolor="blue"`, as shown in the following VML representation:</span></span>

![color1.gif (305 bytes)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





<span data-ttu-id="9424c-136">[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="9424c-136">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rgb-triplet"></a><span data-ttu-id="9424c-137">Triplete RGB</span><span class="sxs-lookup"><span data-stu-id="9424c-137">RGB Triplet</span></span>

<span data-ttu-id="9424c-138">Si el color no es un nombre [de color](#keyword-color-name)de palabra clave, puede expresar el color como un triplete decimal RGB o un triplete hexadecimal RGB.</span><span class="sxs-lookup"><span data-stu-id="9424c-138">If the color is not a [keyword color name](#keyword-color-name), you can express the color as either an RGB decimal triplet or an RGB hexadecimal triplet.</span></span> <span data-ttu-id="9424c-139">Con los tripletes RGB, puede especificar valores para los componentes rojo, verde y azul del color, estableciendo cada componente en un valor que va de 0 a 255 en decimal o de 00 a FF en hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="9424c-139">With RGB triplets, you can specify values for the red, green, and blue components of the color, setting each component to a value ranging from 0 through 255 in decimal, or 00 through FF in hexadecimal.</span></span>

<span data-ttu-id="9424c-140">Por ejemplo, puede crear un rectángulo que se rellena con un color personalizado con un valor RGB de 253, 249, 186 en decimal especificando o , como se muestra en la siguiente representación `fillcolor="rgb(253,249, 186)"` `fillcolor="#FDF9BA"` de VML.</span><span class="sxs-lookup"><span data-stu-id="9424c-140">For example, you can create a rectangle that is filled with a customized color with an RGB value of 253, 249, 186 in decimal by specifying either `fillcolor="rgb(253,249, 186)"` or `fillcolor="#FDF9BA"`, as shown in the following VML representation.</span></span> <span data-ttu-id="9424c-141">En hexadecimal, el valor 253 se convierte en FD, 249 se convierte en F9 y 186 se convierte en BA.</span><span class="sxs-lookup"><span data-stu-id="9424c-141">In hexadecimal, the value 253 becomes FD, 249 becomes F9, and 186 becomes BA.</span></span>

![color2.gif (305 bytes)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





<span data-ttu-id="9424c-143">Si rgb en hexadecimal tiene un patrón como XXYYZZ, puede abreviar a XYZ.</span><span class="sxs-lookup"><span data-stu-id="9424c-143">If the RGB in hexadecimal has a pattern such as XXYYZZ, you can abbreviate it to XYZ.</span></span> <span data-ttu-id="9424c-144">Por ejemplo, \# "66FF99" se puede escribir como \# "6F9".</span><span class="sxs-lookup"><span data-stu-id="9424c-144">For example, "\#66FF99" can be written out as "\#6F9".</span></span>

<span data-ttu-id="9424c-145">[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="9424c-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="9424c-146">Resumen</span><span class="sxs-lookup"><span data-stu-id="9424c-146">Summary</span></span>

<span data-ttu-id="9424c-147">En VML, puede representar un color en uno de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="9424c-147">In VML, you can represent a color in one of the following formats:</span></span>

1.  <span data-ttu-id="9424c-148">fillcolor="blue"</span><span class="sxs-lookup"><span data-stu-id="9424c-148">fillcolor="blue"</span></span>
2.  <span data-ttu-id="9424c-149">fillcolor="rgb(0,0,255)"</span><span class="sxs-lookup"><span data-stu-id="9424c-149">fillcolor="rgb(0,0,255)"</span></span>
3.  <span data-ttu-id="9424c-150">fillcolor=" \# 0000ff"</span><span class="sxs-lookup"><span data-stu-id="9424c-150">fillcolor="\#0000ff"</span></span>

 

 