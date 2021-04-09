---
title: Usar el elemento Textpath
description: Usar el elemento Textpath
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Web Workshop, elemento textpath
- diseñar páginas web, elemento textpath
- Lenguaje de marcado de vectores (VML), elemento textpath
- VML (Lenguaje de marcado de vectores), elemento textpath
- graphics Vector, elemento textpath
- elemento textpath
- Elementos VML, textpath
- Formas VML, elemento textpath
- Lenguaje de marcado de vectores (VML), dibujar texto
- VML (Lenguaje de marcado de vectores), texto de dibujo
- gráficos vectoriales, dibujar texto VML
- dibujar texto
- Formas VML, texto de dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148c032d14307dc07ec56911f4c5cc45a4c69664
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149585"
---
# <a name="using-the-textpath-element"></a><span data-ttu-id="dc275-116">Usar el elemento Textpath</span><span class="sxs-lookup"><span data-stu-id="dc275-116">Using the Textpath Element</span></span>

<span data-ttu-id="dc275-117">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="dc275-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dc275-118">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="dc275-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dc275-119">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="dc275-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dc275-120">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="dc275-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dc275-121">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="dc275-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dc275-122">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="dc275-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dc275-123">En este tema, se muestra cómo usar el `<textpath>` elemento para dibujar texto con varios estilos.</span><span class="sxs-lookup"><span data-stu-id="dc275-123">In this topic, we will illustrate how to use the `<textpath>` element to draw text with various styles.</span></span>

<span data-ttu-id="dc275-124">Puede colocar el `<textpath>` subelemento dentro `<shape>` o `<shapetype>` para dibujar el texto.</span><span class="sxs-lookup"><span data-stu-id="dc275-124">You can place the `<textpath>` sub-element inside `<shape>` or `<shapetype>` to draw text.</span></span> <span data-ttu-id="dc275-125">Después, puede usar los atributos de propiedad del `<textpath>` subelemento para personalizar el texto.</span><span class="sxs-lookup"><span data-stu-id="dc275-125">You can then use the property attributes of the `<textpath>` sub-element to customize the text.</span></span> <span data-ttu-id="dc275-126">También puede usar el `<formulas>` subelemento para definir el contorno del texto.</span><span class="sxs-lookup"><span data-stu-id="dc275-126">You can also use the `<formulas>` sub-element to define the outline of the text.</span></span>

<span data-ttu-id="dc275-127">Por ejemplo, para crear el texto que se muestra en la siguiente imagen, puede escribir la representación de VML a continuación.</span><span class="sxs-lookup"><span data-stu-id="dc275-127">For example, to create the text shown in the following picture, you can type the VML representation below.</span></span> <span data-ttu-id="dc275-128">Observe que usamos el `<shapetype>` elemento para definir un prototipo para el contorno del texto.</span><span class="sxs-lookup"><span data-stu-id="dc275-128">Notice that we use the `<shapetype>` element to define a prototype for the outline of the text.</span></span> <span data-ttu-id="dc275-129">A continuación, se crean instancias de dos formas del mismo TipoForma.</span><span class="sxs-lookup"><span data-stu-id="dc275-129">We then instantiate two shapes from the same shapetype.</span></span> <span data-ttu-id="dc275-130">Simplemente puede cambiar el atributo de propiedad de **cadena** para mostrar texto diferente.</span><span class="sxs-lookup"><span data-stu-id="dc275-130">You can simply change the **string** property attribute to display different text.</span></span>

![\-1.gif shape1 (4898 bytes)](images/shape1-1t.gif)

![\-2.gif shape1 (2789 bytes)](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





<span data-ttu-id="dc275-133">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858398) .</span><span class="sxs-lookup"><span data-stu-id="dc275-133">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858398) .</span></span>

 

 