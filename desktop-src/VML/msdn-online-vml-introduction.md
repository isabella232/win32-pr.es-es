---
title: Introducción a VML
description: Introducción a VML
ms.assetid: 8b603e95-3f02-47d6-9c5c-c781fa5d8459
keywords:
- Lenguaje de marcado de vectores (VML), referencia
- VML (Lenguaje de marcado de vectores), referencia
- gráficos vectoriales, referencia de VML
- gráficos vectoriales, Lenguaje de marcado de vectores (VML)
- referencia de Lenguaje de marcado de vectores (VML)
- Referencia de VML
- Lenguaje de marcado de vectores (VML), elemento de forma
- VML (Lenguaje de marcado de vectores), elemento de forma
- gráficos vectoriales, elemento de forma
- Elemento de forma
- Elementos VML, forma
- Lenguaje de marcado de vectores (VML), VBScript
- VML (Lenguaje de marcado de vectores), VBScript
- Lenguaje de marcado de vectores (VML), JavaScript
- VML (Lenguaje de marcado de vectores), JavaScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7a370519e3f173e7418f1aa0510cac768ff46c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420871"
---
# <a name="vml-introduction"></a><span data-ttu-id="98f6c-118">Introducción a VML</span><span class="sxs-lookup"><span data-stu-id="98f6c-118">VML Introduction</span></span>

<span data-ttu-id="98f6c-119">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="98f6c-119">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="98f6c-120">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="98f6c-120">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="98f6c-121">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="98f6c-121">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="98f6c-122">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="98f6c-122">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="98f6c-123">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="98f6c-123">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="98f6c-124">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="98f6c-124">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="98f6c-125">En este documento se proporciona una referencia detallada completa de la implementación del Lenguaje de marcado de vectores (VML) que se incluye con Microsoft Office 2000.</span><span class="sxs-lookup"><span data-stu-id="98f6c-125">This document gives a complete detailed reference to the implementation of the Vector Markup Language (VML) that is shipped with Microsoft Office 2000.</span></span> <span data-ttu-id="98f6c-126">Otras implementaciones pueden variar.</span><span class="sxs-lookup"><span data-stu-id="98f6c-126">Other implementations may vary.</span></span> <span data-ttu-id="98f6c-127">Consulte la [especificación de VML](https://www.w3.org/TR/NOTE-datetime.html) para obtener más información sobre VML como estándar.</span><span class="sxs-lookup"><span data-stu-id="98f6c-127">Consult the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) for more information about VML as a standard.</span></span>

<span data-ttu-id="98f6c-128">VML se define como un conjunto de elementos XML y los atributos correspondientes para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="98f6c-128">VML is defined as a set of XML elements and the corresponding attributes for each element.</span></span> <span data-ttu-id="98f6c-129">Dado que el elemento de **forma** es el bloque de creación básico de VML, haga clic [aquí](shape-element--vml.md) para comenzar la referencia.</span><span class="sxs-lookup"><span data-stu-id="98f6c-129">Since the **Shape** element is the basic building block of VML, click [here](shape-element--vml.md) to begin the reference.</span></span>

<span data-ttu-id="98f6c-130">Tenga en cuenta que esta referencia contiene varios ejemplos y demostraciones.</span><span class="sxs-lookup"><span data-stu-id="98f6c-130">Note that this reference contains several examples and demos.</span></span> <span data-ttu-id="98f6c-131">Debe tener Microsoft Internet Explorer 5,0 o posterior instalado para ver el VML en directo.</span><span class="sxs-lookup"><span data-stu-id="98f6c-131">You must have Microsoft Internet Explorer 5.0 or greater installed to view the live VML.</span></span>

<span data-ttu-id="98f6c-132">Además de la información sobre el uso de elementos y atributos como etiquetas XML que amplían HTML, esta referencia contiene sintaxis y ejemplos que muestran cómo usar las características de scripting y Document Object Model de Internet Explorer 5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="98f6c-132">In addition to the information about using elements and attributes as XML tags that extend HTML, this reference contains syntax and examples that show how to use the scripting and the Document Object Model features of Internet Explorer 5 or greater.</span></span> <span data-ttu-id="98f6c-133">El uso de scripts con VML le permite crear elementos "sobre la marcha" y manipular atributos en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="98f6c-133">Using script with VML enables you to create elements "on the fly" and manipulate attributes in real time.</span></span>

<span data-ttu-id="98f6c-134">En este ejemplo se usa VBScript y JavaScript.</span><span class="sxs-lookup"><span data-stu-id="98f6c-134">This examples in this reference uses VBScript and Javascript.</span></span> <span data-ttu-id="98f6c-135">Si utiliza un lenguaje de scripting diferente del que se muestra en un ejemplo, debe coincidir con las mayúsculas y minúsculas de todos los nombres de elementos y atributos.</span><span class="sxs-lookup"><span data-stu-id="98f6c-135">If you use use a different scripting language than the one shown in an example, you must match the case of all element and attribute names.</span></span> <span data-ttu-id="98f6c-136">La referencia proporciona sintaxis de scripting que es correcta para los lenguajes que distinguen mayúsculas de minúsculas, como JavaScript.</span><span class="sxs-lookup"><span data-stu-id="98f6c-136">The reference gives scripting syntax that is correct for case-sensitive languages such as JavaScript.</span></span> <span data-ttu-id="98f6c-137">Si duda sobre el caso de caracteres correctos, use un examinador de objetos (por ejemplo, OLEView) para explorar el VGX.DLL para determinar el uso exacto de un elemento o atributo.</span><span class="sxs-lookup"><span data-stu-id="98f6c-137">If in doubt regarding the correct character case, use an object browser (such as OLEView) to explore the VGX.DLL to determine the exact case of an element or attribute.</span></span> <span data-ttu-id="98f6c-138">Tenga en cuenta que cuando se usa VML como etiquetas XML, la distinción de mayúsculas y minúsculas depende del tipo de documento del documento subyacente.</span><span class="sxs-lookup"><span data-stu-id="98f6c-138">Note that when VML is used as XML tags, case sensitivity depends on the document type of you underlying document.</span></span> <span data-ttu-id="98f6c-139">Si usa un modo STRICT. DOCTYPE, Elements y Attributes distinguirán mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="98f6c-139">If you are using a strict mode !DOCTYPE, elements and attributes will be case sensitive.</span></span>

[<span data-ttu-id="98f6c-140">Referencia de VML</span><span class="sxs-lookup"><span data-stu-id="98f6c-140">The VML Reference</span></span>](shape-element--vml.md)

 

 