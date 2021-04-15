---
title: Apéndice (VML)
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Web Workshop, espacios de nombres
- Web Workshop, estilos de comportamiento
- diseñar páginas web, espacios de nombres
- diseñar páginas web, estilos de comportamiento
- Lenguaje de marcado de vectores (VML), espacios de nombres
- VML (Lenguaje de marcado de vectores), espacios de nombres
- gráficos vectoriales, espacios de nombres
- Lenguaje de marcado de vectores (VML), estilos de comportamiento
- VML (Lenguaje de marcado de vectores), estilos de comportamiento
- gráficos vectoriales, estilos de comportamiento
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d4e7a6a7e44671b7ee835eea263d9ce36a27d8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421824"
---
# <a name="appendix-vml"></a><span data-ttu-id="8e25b-114">Apéndice (VML)</span><span class="sxs-lookup"><span data-stu-id="8e25b-114">Appendix (VML)</span></span>

<span data-ttu-id="8e25b-115">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8e25b-115">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8e25b-116">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="8e25b-116">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8e25b-117">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="8e25b-117">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8e25b-118">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="8e25b-118">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8e25b-119">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8e25b-119">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8e25b-120">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8e25b-120">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8e25b-121">Para que los exploradores sepan cómo entregar los datos a un procesador específico de VML, debe escribir información como espacios de nombres y estilos de comportamiento.</span><span class="sxs-lookup"><span data-stu-id="8e25b-121">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as namespaces and behavior styles.</span></span> <span data-ttu-id="8e25b-122">Después, puede usar VML para escribir gráficos en la `<BODY>` región.</span><span class="sxs-lookup"><span data-stu-id="8e25b-122">You can then use VML to type graphics in the `<BODY>` region.</span></span>

<span data-ttu-id="8e25b-123">En este tema:</span><span class="sxs-lookup"><span data-stu-id="8e25b-123">In this topic:</span></span>

-   [<span data-ttu-id="8e25b-124">Espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="8e25b-124">Namespaces</span></span>](#namespaces)
-   [<span data-ttu-id="8e25b-125">Estilos de comportamiento</span><span class="sxs-lookup"><span data-stu-id="8e25b-125">Behavior Styles</span></span>](#behavior-styles)

## <a name="namespaces"></a><span data-ttu-id="8e25b-126">Espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="8e25b-126">Namespaces</span></span>

<span data-ttu-id="8e25b-127">Un mecanismo XML indica el espacio de nombres del que procede un elemento.</span><span class="sxs-lookup"><span data-stu-id="8e25b-127">An XML mechanism indicates the namespace that an element comes from.</span></span> <span data-ttu-id="8e25b-128">Si cambia del análisis en HTML al análisis en XML, este mecanismo indica el modificador en HTML.</span><span class="sxs-lookup"><span data-stu-id="8e25b-128">If you switch from parsing in HTML to parsing in XML, this mechanism indicates the switch within HTML.</span></span>

<span data-ttu-id="8e25b-129">Pregunte al expendedor del procesador VML qué información es necesaria para el espacio de nombres XML.</span><span class="sxs-lookup"><span data-stu-id="8e25b-129">Ask the vender of your VML processor what information is required for the XML namespace.</span></span>

<span data-ttu-id="8e25b-130">Si utiliza Microsoft Internet Explorer para representar VML, escriba siempre la siguiente línea en la `<HTML>` etiqueta:</span><span class="sxs-lookup"><span data-stu-id="8e25b-130">If you use Microsoft Internet Explorer to render VML, always type the following line in the `<HTML>` tag:</span></span>


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



<span data-ttu-id="8e25b-131">Esta información indica a Internet Explorer que cambie al espacio de nombres "urn: schemas-microsoft-com: VML" al analizar una etiqueta XML con un prefijo `v:` y a entregar los datos resultantes al procesador VML.</span><span class="sxs-lookup"><span data-stu-id="8e25b-131">This information tells Internet Explorer to switch to namespace "urn:schemas-microsoft-com:vml" when parsing an XML tag with a prefix `v:`, and to hand off the resulting data to the VML processor.</span></span>

<span data-ttu-id="8e25b-132">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="8e25b-132">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="behavior-styles"></a><span data-ttu-id="8e25b-133">Estilos de comportamiento</span><span class="sxs-lookup"><span data-stu-id="8e25b-133">Behavior Styles</span></span>

<span data-ttu-id="8e25b-134">VML se define en Microsoft Internet Explorer como un comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8e25b-134">VML is defined in Microsoft Internet Explorer as a default behavior.</span></span>

<span data-ttu-id="8e25b-135">Para representar VML, escriba siempre las líneas siguientes en la `<HEAD>` región:</span><span class="sxs-lookup"><span data-stu-id="8e25b-135">To render VML, always type the following lines in the `<HEAD>` region:</span></span>


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



<span data-ttu-id="8e25b-136">VML se implementa en Internet Explorer a través de VGX.DLL.</span><span class="sxs-lookup"><span data-stu-id="8e25b-136">VML is implemented in Internet Explorer through VGX.DLL.</span></span> <span data-ttu-id="8e25b-137">Si la instalación inicial del explorador no incluía el comportamiento de VML, puede que tenga que agregarlo como una opción.</span><span class="sxs-lookup"><span data-stu-id="8e25b-137">If your initial installation of the browser did not include VML behavior, you may need to add it as an option.</span></span> <span data-ttu-id="8e25b-138">No es necesario agregar una `<object>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="8e25b-138">You do not need to add an `<object>` tag.</span></span>

 

 
