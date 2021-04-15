---
title: Usar el elemento TextBox
description: Usar el elemento TextBox
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Web Workshop, elemento TextBox
- diseñar páginas web, elemento TextBox
- Lenguaje de marcado de vectores (VML), elemento TextBox
- VML (Lenguaje de marcado de vectores), elemento TextBox
- gráficos vectoriales, elemento TextBox
- Elemento TextBox
- Elementos VML, TextBox
- Formas VML, elemento TextBox
- Lenguaje de marcado de vectores (VML), adjuntar texto
- VML (Lenguaje de marcado de vectores), adjuntar texto
- gráficos vectoriales, adjuntar texto
- Formas VML, adjuntar texto
- Adjuntar texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388a359ca8cf4e320f95d708b4cf7055287d424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488223"
---
# <a name="using-the-textbox-element"></a><span data-ttu-id="7caa7-116">Usar el elemento TextBox</span><span class="sxs-lookup"><span data-stu-id="7caa7-116">Using the Textbox Element</span></span>

<span data-ttu-id="7caa7-117">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7caa7-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7caa7-118">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="7caa7-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7caa7-119">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="7caa7-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7caa7-120">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="7caa7-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7caa7-121">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7caa7-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7caa7-122">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7caa7-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="examples"></a><span data-ttu-id="7caa7-123">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="7caa7-123">Examples:</span></span>

<span data-ttu-id="7caa7-124">Para adjuntar texto a un rectángulo, puede escribir las líneas siguientes en la `<BODY>` región de la página web:</span><span class="sxs-lookup"><span data-stu-id="7caa7-124">To attach text to a rectangle, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





<span data-ttu-id="7caa7-125">Para adjuntar un hipervínculo a un rectángulo redondeado con relleno degradado, puede escribir las líneas siguientes en la `<BODY>` región de la página web:</span><span class="sxs-lookup"><span data-stu-id="7caa7-125">To attach a hyperlink to a rounded rectangle that is gradient-filled, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![textbox2.gif (1147 bytes)](images/textbox2.gif)


```HTML
<body>
<v:roundrect style='width:80pt;height:30pt;' fillcolor="red">
<v:fill type="gradient" />
<v:textbox>
<a href="https://home.microsoft.com/"> Click here</a>
</v:textbox>
</v:roundrect>
</body>
```





<span data-ttu-id="7caa7-127">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span><span class="sxs-lookup"><span data-stu-id="7caa7-127">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span></span>

 

 