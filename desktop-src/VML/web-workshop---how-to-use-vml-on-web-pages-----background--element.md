---
title: Usar el elemento Background
description: Usar el elemento Background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Web Workshop, elemento Background
- diseñar páginas web, elemento Background
- Lenguaje de marcado de vectores (VML), elemento Background
- VML (Lenguaje de marcado de vectores), elemento Background
- gráficos vectoriales, elemento Background
- Background (elemento)
- Elementos VML, Fondo
- Formas VML, elemento Background
- Lenguaje de marcado de vectores (VML), personalizar el fondo
- VML (Lenguaje de marcado de vectores), personalizar el fondo
- gráficos vectoriales, personalizar el fondo
- Formas VML, personalizar el fondo
- Personalización del fondo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904654"
---
# <a name="using-the-background-element"></a><span data-ttu-id="70789-116">Usar el elemento Background</span><span class="sxs-lookup"><span data-stu-id="70789-116">Using the Background Element</span></span>

<span data-ttu-id="70789-117">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="70789-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="70789-118">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="70789-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="70789-119">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="70789-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="70789-120">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="70789-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="70789-121">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="70789-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="70789-122">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="70789-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="70789-123">En este tema, veremos cómo puede personalizar el fondo de una página web mediante el `<background>` elemento proporcionado en VML.</span><span class="sxs-lookup"><span data-stu-id="70789-123">In this topic, we will illustrate how you can customize the background of a Web page by using the `<background>` element provided in VML.</span></span>

<span data-ttu-id="70789-124">Como ha aprendido en el tema [de `<fill>` uso](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) , puede colocar el `<fill>` subelemento dentro de `<shape>` , `<shapetype>` o cualquier elemento de forma predefinido para describir cómo rellenar la forma.</span><span class="sxs-lookup"><span data-stu-id="70789-124">As you've learned from the [Use `<fill>`](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) topic, you can place the `<fill>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span>

<span data-ttu-id="70789-125">Del mismo modo, puede colocar el `<fill>` subelemento dentro del `<background>` elemento para describir cómo rellenar el fondo de una página web.</span><span class="sxs-lookup"><span data-stu-id="70789-125">Similarly, you can place the `<fill>` sub-element inside the `<background>` element to describe how to fill the background of a Web page.</span></span> <span data-ttu-id="70789-126">Después, puede usar los atributos de propiedad del `<fill>` subelemento para personalizar el efecto de relleno, como [relleno de degradado](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [relleno de patrón](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)o [relleno de imagen](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span><span class="sxs-lookup"><span data-stu-id="70789-126">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [pattern fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), or [picture fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span></span>

<span data-ttu-id="70789-127">Por ejemplo, para dibujar un fondo con relleno degradado, puede escribir las líneas siguientes en la `<BODY>` región de la página web:</span><span class="sxs-lookup"><span data-stu-id="70789-127">For example, to draw a gradient-filled background, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





<span data-ttu-id="70789-128">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span><span class="sxs-lookup"><span data-stu-id="70789-128">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span></span>

 

 