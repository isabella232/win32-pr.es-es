---
title: Usar el elemento Shadow
description: Usar el elemento Shadow
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Web Workshop, elemento Shadow
- diseñar páginas web, elemento Shadow
- Lenguaje de marcado de vectores (VML), elemento Shadow
- VML (Lenguaje de marcado de vectores), elemento Shadow
- gráficos vectoriales, elemento Shadow
- elemento Shadow
- Elementos VML, sombra
- Formas VML, elemento Shadow
- Lenguaje de marcado de vectores (VML), dibujar con efectos de sombra
- VML (Lenguaje de marcado de vectores), dibujar con efectos de sombra
- gráficos vectoriales, dibujar con efectos de sombra
- Formas VML, dibujar con efectos de sombra
- dibujar con efectos de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe32651fbeab6b84b49a40bae05a08ba3d9c33a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421315"
---
# <a name="using-the-shadow-element"></a><span data-ttu-id="4f648-116">Usar el elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="4f648-116">Using the Shadow Element</span></span>

<span data-ttu-id="4f648-117">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4f648-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4f648-118">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="4f648-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4f648-119">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="4f648-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4f648-120">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="4f648-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4f648-121">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4f648-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4f648-122">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4f648-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4f648-123">En este tema, se muestra cómo usar el `<shadow>` subelemento para dibujar una forma que tiene varios efectos de sombra.</span><span class="sxs-lookup"><span data-stu-id="4f648-123">In this topic, we will illustrate how to use the `<shadow>` sub-element to draw a shape that has various shadow effects.</span></span>

<span data-ttu-id="4f648-124">Puede colocar el `<shadow>` subelemento dentro de `<shape>` , `<shapetype>` o cualquier elemento de forma predefinido para dibujar una forma con una sombra.</span><span class="sxs-lookup"><span data-stu-id="4f648-124">You can place the `<shadow>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to draw a shape with a shadow.</span></span> <span data-ttu-id="4f648-125">Después, puede usar los atributos de propiedad del `<shadow>` subelemento para personalizar la sombra.</span><span class="sxs-lookup"><span data-stu-id="4f648-125">You can then use the property attributes of the `<shadow>` sub-element to customize the shadow.</span></span>

<span data-ttu-id="4f648-126">Por ejemplo, para crear una forma con una sombra, tal como se muestra en la siguiente imagen, puede escribir las líneas siguientes en la `<BODY>` región de la página web:</span><span class="sxs-lookup"><span data-stu-id="4f648-126">For example, to create a shape with a shadow, as shown in the following picture, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![shape1.gif (887 bytes)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   <span data-ttu-id="4f648-128">`on="t"` e `type="perspective"` indican que debe activar la sombra con el tipo de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="4f648-128">`on="t"` and `type="perspective"` indicate to turn on the shadow using the perspective type.</span></span>
-   <span data-ttu-id="4f648-129">El **origen** y el **desplazamiento** indican dónde dibujar la sombra.</span><span class="sxs-lookup"><span data-stu-id="4f648-129">The **origin** and **offset** indicate where to draw the shadow.</span></span>
-   <span data-ttu-id="4f648-130">`matrix="..."` Especifica la matriz de transformación de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="4f648-130">`matrix="..."` specifies the perspective transform matrix.</span></span>

<span data-ttu-id="4f648-131">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span><span class="sxs-lookup"><span data-stu-id="4f648-131">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span></span>

 

 