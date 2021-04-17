---
title: Usar elementos PARAM en una página web que se muestra en Firefox
description: Usar elementos PARAM en una página web que se muestra en Firefox
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Windows Media Player, elementos PARAM en el elemento OBJECT
- Modelo de objetos de Windows Media Player, elementos PARAM en el elemento OBJECT
- modelo de objetos, elementos PARAM en el elemento OBJECT
- Windows Media Player Mobile, elementos PARAM en el elemento OBJECT
- Control ActiveX de Windows Media Player, elementos PARAM en el elemento OBJECT
- Control ActiveX móvil de Windows Media Player, elementos PARAM en el elemento OBJECT
- Control ActiveX, elementos PARAM en el elemento OBJECT
- incrustación, páginas web
- Incrustación de páginas web, elementos PARAM en el elemento OBJECT
- Elementos PARAM en el elemento OBJECT
- Windows Media Player, Firefox
- Modelo de objetos de Windows Media Player, Firefox
- modelo de objetos, Firefox
- Windows Media Player Mobile, Firefox
- Control ActiveX de Windows Media Player, Firefox
- Control ActiveX móvil de Windows Media Player, Firefox
- Control ActiveX, Firefox
- Firefox, elementos PARAM en el elemento OBJECT
- Incrustación de páginas web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b045d111ff3cd0de09f54a8cf7ac25028fa1dc6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "104357820"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="b0aed-122">Usar elementos PARAM en una página web que se muestra en Firefox</span><span class="sxs-lookup"><span data-stu-id="b0aed-122">Using PARAM Elements in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="b0aed-123">Puede usar elementos PARAM dentro de un elemento OBJECT para establecer el estado inicial del control Player.</span><span class="sxs-lookup"><span data-stu-id="b0aed-123">You can use PARAM elements inside an OBJECT element to set the initial state of the Player control.</span></span> <span data-ttu-id="b0aed-124">Por ejemplo, los elementos PARAM en el ejemplo siguiente especifican que el control debería reproducir Seattle. wmv automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b0aed-124">For example, the PARAM elements in the following example specify that the control should play seattle.wmv automatically.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



<span data-ttu-id="b0aed-125">La mayoría de los elementos PARAM se pueden interpretar por Internet Explorer y Firefox.</span><span class="sxs-lookup"><span data-stu-id="b0aed-125">Most PARAM elements can be interpreted by Internet Explorer and by Firefox.</span></span> <span data-ttu-id="b0aed-126">Sin embargo, hay algunos elementos PARAM que no admite el complemento Firefox.</span><span class="sxs-lookup"><span data-stu-id="b0aed-126">However, there are a few PARAM elements that the Firefox plug-in does not support.</span></span> <span data-ttu-id="b0aed-127">Para obtener información sobre los elementos de parámetro admitidos por el complemento de Firefox, vea [elementos param en un elemento Object](param-elements-in-an-object-element.md).</span><span class="sxs-lookup"><span data-stu-id="b0aed-127">For information about which PARAM elements are supported by the Firefox plug-in, see [PARAM Elements in an OBJECT Element](param-elements-in-an-object-element.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0aed-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b0aed-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0aed-129">**Uso del control de Media Player de Windows con Firefox**</span><span class="sxs-lookup"><span data-stu-id="b0aed-129">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




