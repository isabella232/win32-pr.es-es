---
title: Cómo usar VML en páginas web
description: Cómo usar VML en páginas web
ms.assetid: ae20b789-1890-4560-bcc0-536f126c5a41
keywords:
- Lenguaje de marcado de vectores (VML), Web Workshop
- VML (Lenguaje de marcado de vectores), Web Workshop
- gráficos vectoriales, Web Workshop
- Lenguaje de marcado de vectores (VML), diseñar páginas web
- VML (Lenguaje de marcado de vectores), diseñar páginas web
- gráficos vectoriales, diseñar páginas web
- diseñar páginas web, tareas de VML
- Web Workshop, tareas de VML
- diseñar páginas web, Lenguaje de marcado de vectores (VML)
- Web Workshop, Lenguaje de marcado de vectores (VML)
- Lenguaje de marcado de vectores (VML), World Wide Web Consortium (W3C)
- VML (Lenguaje de marcado de vectores), World Wide Web Consortium (W3C)
- gráficos vectoriales, World Wide Web Consortium (W3C)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189353fd5a6c50ffbdcf3fe2ad3efe7e82b8e219
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676435"
---
# <a name="how-to-use-vml-on-webpages"></a><span data-ttu-id="13548-116">Cómo usar VML en páginas web</span><span class="sxs-lookup"><span data-stu-id="13548-116">How to Use VML on Webpages</span></span>

<span data-ttu-id="13548-117">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="13548-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="13548-118">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="13548-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="13548-119">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="13548-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="13548-120">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="13548-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="13548-121">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="13548-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="13548-122">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="13548-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="13548-123">Este documento complementa la [especificación de lenguaje de marcado de vectores (VML)](https://www.w3.org/TR/NOTE-datetime.html) que se envió a la World Wide Web Consortium (W3C).</span><span class="sxs-lookup"><span data-stu-id="13548-123">This document supplements the [Vector Markup Language (VML) specification](https://www.w3.org/TR/NOTE-datetime.html) that was submitted to the World Wide Web Consortium (W3C).</span></span> <span data-ttu-id="13548-124">Con este documento y la especificación de VML completa, debería poder usar VML para diseñar páginas Web.</span><span class="sxs-lookup"><span data-stu-id="13548-124">With this document and the complete VML specification, you should be able to use VML to design webpages.</span></span> <span data-ttu-id="13548-125">Se supone que ya tiene un conocimiento práctico de HTML.</span><span class="sxs-lookup"><span data-stu-id="13548-125">We have assumed that you already have a working knowledge of HTML.</span></span>

## <a name="part-i-basic-topics"></a><span data-ttu-id="13548-126">Parte I: temas básicos</span><span class="sxs-lookup"><span data-stu-id="13548-126">Part I: Basic Topics</span></span>

-   [<span data-ttu-id="13548-127">Dibujar formas básicas</span><span class="sxs-lookup"><span data-stu-id="13548-127">Drawing Basic Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----drawing-basic-shapes.md)
-   [<span data-ttu-id="13548-128">Usar formas predefinidas</span><span class="sxs-lookup"><span data-stu-id="13548-128">Using Predefined Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----using-predefined-shapes.md)
-   [<span data-ttu-id="13548-129">Colorear formas</span><span class="sxs-lookup"><span data-stu-id="13548-129">Coloring Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----coloring-shapes.md)
-   [<span data-ttu-id="13548-130">Ajustar el tamaño de las formas</span><span class="sxs-lookup"><span data-stu-id="13548-130">Scaling Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md)
-   [<span data-ttu-id="13548-131">Colocar formas</span><span class="sxs-lookup"><span data-stu-id="13548-131">Positioning Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----positioning-shapes.md)
-   [<span data-ttu-id="13548-132">Agrupar formas</span><span class="sxs-lookup"><span data-stu-id="13548-132">Grouping Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----grouping-shapes.md)

## <a name="part-ii-advanced-topics"></a><span data-ttu-id="13548-133">Parte II: temas avanzados</span><span class="sxs-lookup"><span data-stu-id="13548-133">Part II: Advanced Topics</span></span>

-   [<span data-ttu-id="13548-134">Usar el elemento TipoForma</span><span class="sxs-lookup"><span data-stu-id="13548-134">Using the Shapetype Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----shapetype--element.md)
-   [<span data-ttu-id="13548-135">Usar el elemento stroke</span><span class="sxs-lookup"><span data-stu-id="13548-135">Using the Stroke Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----stroke--element.md)
-   [<span data-ttu-id="13548-136">Uso del elemento de relleno</span><span class="sxs-lookup"><span data-stu-id="13548-136">Using the Fill Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)
-   [<span data-ttu-id="13548-137">Usar el elemento Image</span><span class="sxs-lookup"><span data-stu-id="13548-137">Using the Image Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----image--element.md)
-   [<span data-ttu-id="13548-138">Usar el elemento Background</span><span class="sxs-lookup"><span data-stu-id="13548-138">Using the Background Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----background--element.md)
-   [<span data-ttu-id="13548-139">Usar el elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="13548-139">Using the Shadow Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----shadow--element.md)
-   [<span data-ttu-id="13548-140">Usar el elemento path</span><span class="sxs-lookup"><span data-stu-id="13548-140">Using the Path Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----path--element.md)
-   [<span data-ttu-id="13548-141">Usar el elemento TextBox</span><span class="sxs-lookup"><span data-stu-id="13548-141">Using the Textbox Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----textbox--element.md)
-   [<span data-ttu-id="13548-142">Usar el espacio de coordenadas local</span><span class="sxs-lookup"><span data-stu-id="13548-142">Using Local Coordinate Space</span></span>](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md)
-   [<span data-ttu-id="13548-143">Usar el elemento formulas</span><span class="sxs-lookup"><span data-stu-id="13548-143">Using the Formulas Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----formulas--element.md)
-   [<span data-ttu-id="13548-144">Usar el elemento handles</span><span class="sxs-lookup"><span data-stu-id="13548-144">Using the Handles Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----handles--element.md)
-   [<span data-ttu-id="13548-145">Usar el elemento Textpath</span><span class="sxs-lookup"><span data-stu-id="13548-145">Using the Textpath Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----textpath--element.md)

> [!Note]  
> <span data-ttu-id="13548-146">Los ejemplos que se proporcionan en esta referencia están diseñados para Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="13548-146">The samples provided in this reference are designed for Internet Explorer.</span></span> <span data-ttu-id="13548-147">También hemos proporcionado ilustraciones siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="13548-147">We have also provided illustrations where possible.</span></span>

 

 

 