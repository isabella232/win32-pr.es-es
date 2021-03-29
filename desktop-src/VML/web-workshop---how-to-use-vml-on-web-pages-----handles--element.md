---
title: Usar el elemento handles
description: Usar el elemento handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Web Workshop, Controls (elemento)
- diseñar páginas web, elemento handles
- Lenguaje de marcado de vectores (VML), elemento handles
- VML (Lenguaje de marcado de vectores), elemento handles
- Vector Graphics, elemento handles
- Controls (elemento)
- Elementos VML, identificadores
- Formas VML, elemento handles
- Lenguaje de marcado de vectores (VML), adjuntar texto a formas
- VML (Lenguaje de marcado de vectores), adjuntar texto a formas
- gráficos vectoriales, adjuntar texto a formas
- Formas VML, adjuntar texto
- Adjuntar texto a formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54c721d50f51c46cd4bf08393e85ad83307fc1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077810"
---
# <a name="using-the-handles-element"></a><span data-ttu-id="59a01-116">Usar el elemento handles</span><span class="sxs-lookup"><span data-stu-id="59a01-116">Using the Handles Element</span></span>

<span data-ttu-id="59a01-117">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="59a01-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="59a01-118">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="59a01-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="59a01-119">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="59a01-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="59a01-120">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="59a01-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="59a01-121">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="59a01-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="59a01-122">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="59a01-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="59a01-123">En este tema, se muestra cómo usar el `<handles>` elemento para adjuntar texto a una forma.</span><span class="sxs-lookup"><span data-stu-id="59a01-123">In this topic, we will illustrate how to use the `<handles>` element to attach text to a shape.</span></span>

<span data-ttu-id="59a01-124">Puede colocar el `<handles>` subelemento dentro de `<shape>` o `<shapetype>` para definir los elementos de la interfaz de usuario que  pueden variar los valores de ajuste de la forma.</span><span class="sxs-lookup"><span data-stu-id="59a01-124">You can place the `<handles>` sub-element inside `<shape>` or `<shapetype>` to define user interface elements that can vary the **adj** values on the shape.</span></span>

<span data-ttu-id="59a01-125">Por ejemplo, como se muestra en la siguiente representación VML, puede proporcionar un controlador de ajuste (cuadro amarillo) que los usuarios simplemente pueden arrastrar para ajustar la forma.</span><span class="sxs-lookup"><span data-stu-id="59a01-125">For example, as shown the following VML representation, you can provide an adjust handle (yellow box) that users can simply drag to adjust the shape.</span></span>

<span data-ttu-id="59a01-126">Nota: los controladores están disponibles cuando se ve esta forma VML en Microsoft Office aplicaciones, donde la forma está pensada para ser manipulable.</span><span class="sxs-lookup"><span data-stu-id="59a01-126">Note: the handles are available when this VML shape is viewed in Microsoft Office applications, where the shape is intended to be manipulable.</span></span>

![shape1.gif (564 bytes)](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





<span data-ttu-id="59a01-128">Observe que la única diferencia entre la representación de VML anterior **y la siguiente es el valor de** ajuste.</span><span class="sxs-lookup"><span data-stu-id="59a01-128">Notice that the only difference between the preceding VML representation and the following one is the **adj** value.</span></span>

![shape2.gif (1361 bytes)](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





<span data-ttu-id="59a01-130">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858393) .</span><span class="sxs-lookup"><span data-stu-id="59a01-130">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858393) .</span></span>

 

 