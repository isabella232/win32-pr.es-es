---
title: Ajustar el tamaño de las formas
description: Ajustar el tamaño de las formas
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Web Workshop, escalar formas
- diseñar páginas web, ajustar el tamaño de las formas
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
ms.openlocfilehash: e2e7c64fdc0eaa32df1f22b06734b366609ee319
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792105"
---
# <a name="scaling-shapes"></a><span data-ttu-id="ddfb6-115">Ajustar el tamaño de las formas</span><span class="sxs-lookup"><span data-stu-id="ddfb6-115">Scaling Shapes</span></span>

<span data-ttu-id="ddfb6-116">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ddfb6-116">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ddfb6-117">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="ddfb6-117">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ddfb6-118">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="ddfb6-118">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ddfb6-119">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="ddfb6-119">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ddfb6-120">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ddfb6-120">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ddfb6-121">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ddfb6-121">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ddfb6-122">Ha aprendido cómo dibujar y colorear formas en una página web mediante VML.</span><span class="sxs-lookup"><span data-stu-id="ddfb6-122">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="ddfb6-123">En este tema, se muestra cómo escalar formas a cualquier tamaño que desee.</span><span class="sxs-lookup"><span data-stu-id="ddfb6-123">In this topic, we will illustrate how to scale shapes to any size you want.</span></span>

<span data-ttu-id="ddfb6-124">VML usa la misma sintaxis definida en la sección de [detalles del modelo de representación visual](https://www.w3.org/TR/PR-CSS2/visudet.mdl) de la [especificación CSS2](https://www.w3.org/TR/PR-CSS2/) para especificar el tamaño del cuadro contenedor de forma que el contenido de una forma se represente (dibuje) dentro del cuadro contenedor.</span><span class="sxs-lookup"><span data-stu-id="ddfb6-124">VML uses the same syntax defined in the [Visual Rendering Model Details](https://www.w3.org/TR/PR-CSS2/visudet.mdl) section of the [CSS2 specification](https://www.w3.org/TR/PR-CSS2/) to specify the size of the containing box so that the contents of a shape will be rendered (drawn) within the containing box.</span></span> <span data-ttu-id="ddfb6-125">Puede usar los atributos de estilo **ancho** y **alto** para definir el tamaño del cuadro contenedor.</span><span class="sxs-lookup"><span data-stu-id="ddfb6-125">You can use the **width** and **height** style attributes to define the size of the containing box.</span></span>

<span data-ttu-id="ddfb6-126">Por ejemplo, si dibuja un óvalo y especifica **Style**= ' width: 75pt; height: 100pt ', el óvalo se dibujará dentro de un cuadro contenedor con un tamaño de 75 puntos (ancho) de 100 puntos (alto), tal como se muestra en la siguiente imagen:</span><span class="sxs-lookup"><span data-stu-id="ddfb6-126">For example, if you draw an oval and specify **style**='width:75pt;height:100pt', the oval will be drawn within a containing box at a size of 75 points (width) by 100 points (height), as shown in the following picture:</span></span>

![oval1.gif (660 bytes)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





<span data-ttu-id="ddfb6-128">Si cambia el tamaño a **Style**= ' width: 120pt; height: 140pt ', la elipse se vuelve más grande porque se escala en el nuevo cuadro contenedor con un tamaño de 120 puntos (ancho) de 140 puntos (alto), como se muestra en la siguiente imagen:</span><span class="sxs-lookup"><span data-stu-id="ddfb6-128">If you change the size to **style**='width:120pt;height:140pt', the oval becomes larger because it is scaled within the new containing box at a size of 120 points (width) by 140 points (height), as shown in the following picture:</span></span>

![oval2.gif (966 bytes)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





<span data-ttu-id="ddfb6-130">Si cambia el tamaño a **Style**= ' width: 60pt; height: 40pt ', la elipse se vuelve más pequeña porque se escala en el nuevo cuadro contenedor con un tamaño de 60 puntos (ancho) de 40 puntos (alto), tal como se muestra en la siguiente imagen:</span><span class="sxs-lookup"><span data-stu-id="ddfb6-130">If you change the size to **style**='width:60pt;height:40pt', the oval becomes smaller because it is scaled within the new containing box at a size of 60 points (width) by 40 points (height), as shown in the following picture:</span></span>

![oval3.gif (394 bytes)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 