---
title: Lenguaje de marcado de vectores (VML)
description: Lenguaje de marcado de vectores (VML)
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Lenguaje de marcado de vectores (VML), acerca de
- VML (Lenguaje de marcado de vectores), acerca de
- gráficos vectoriales, acerca de
- gráficos vectoriales, Lenguaje de marcado de vectores (VML)
- Lenguaje de marcado de vectores (VML), World Wide Web Consortium (W3C)
- VML (Lenguaje de marcado de vectores), World Wide Web Consortium (W3C)
- gráficos vectoriales, World Wide Web Consortium (W3C)
- gráficos vectoriales, ventajas de VML
- Lenguaje de marcado de vectores (VML), ventajas
- VML (Lenguaje de marcado de vectores), ventajas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ba51fd041f36915eaafe20201876653f597e04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105678614"
---
# <a name="vector-markup-language-vml"></a><span data-ttu-id="303c3-113">Lenguaje de marcado de vectores (VML)</span><span class="sxs-lookup"><span data-stu-id="303c3-113">Vector Markup Language (VML)</span></span>

<span data-ttu-id="303c3-114">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="303c3-114">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="303c3-115">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="303c3-115">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!NOTE]
> <span data-ttu-id="303c3-116">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="303c3-116">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="303c3-117">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="303c3-117">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="303c3-118">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="303c3-118">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="303c3-119">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="303c3-119">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

<span data-ttu-id="303c3-120">Lenguaje de marcado de vectores (VML) es un formato de intercambio, edición y entrega basado en XML para gráficos vectoriales de alta calidad en la web que satisface las necesidades de los usuarios de productividad y los profesionales de diseño gráfico.</span><span class="sxs-lookup"><span data-stu-id="303c3-120">Vector Markup Language (VML) is an XML-based exchange, editing, and delivery format for high-quality vector graphics on the Web that meets the needs of both productivity users and graphic design professionals.</span></span> <span data-ttu-id="303c3-121">XML es un lenguaje emergente sencillo, flexible y abierto basado en texto que complementa HTML.</span><span class="sxs-lookup"><span data-stu-id="303c3-121">XML is an emerging simple, flexible, and open text-based language that complements HTML.</span></span> <span data-ttu-id="303c3-122">(Vea la [sección XML](/documentation/?frame=true) de MSDN Library para obtener información detallada sobre XML).</span><span class="sxs-lookup"><span data-stu-id="303c3-122">(See the [XML section](/documentation/?frame=true) of the MSDN Library for detailed information on XML.)</span></span>

<span data-ttu-id="303c3-123">VML es compatible actualmente con Microsoft Internet Explorer versión 5,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="303c3-123">VML is currently supported by Microsoft Internet Explorer version 5.0 or later.</span></span>

<span data-ttu-id="303c3-124">VML se ha propuesto al W3C como estándar para los gráficos vectoriales en la web (vea [lenguaje de marcado de vectores (VML)](https://www.w3.org/TR/NOTE-VML)).</span><span class="sxs-lookup"><span data-stu-id="303c3-124">VML has been proposed to the W3C as a standard for vector graphics on the Web (see [Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-VML)).</span></span> <span data-ttu-id="303c3-125">Microsoft continúa liderando la carga en el desarrollo y la implementación de tecnologías basadas en XML, trabajando con los principales asociados del sector (AutoDesk, Hewlett-Packard, Macromedia, Visio) y el W3C para avanzar en los estándares basados en Web.</span><span class="sxs-lookup"><span data-stu-id="303c3-125">Microsoft is continuing to lead the charge in the development and implementation of XML-based technologies, working with leading industry partners (AutoDesk, Hewlett-Packard, Macromedia, Visio) and the W3C to advance Web-based standards.</span></span> <span data-ttu-id="303c3-126">Esperamos trabajar con el W3C para impulsar en última instancia un formato estándar para los gráficos vectoriales en la Web.</span><span class="sxs-lookup"><span data-stu-id="303c3-126">We expect to work with the W3C to ultimately drive to one standard format for vector graphics on the Web.</span></span>

<span data-ttu-id="303c3-127">VML también es compatible con Microsoft Office 2000 o posterior.</span><span class="sxs-lookup"><span data-stu-id="303c3-127">VML is also supported by Microsoft Office 2000 or later.</span></span> <span data-ttu-id="303c3-128">Microsoft Word, Microsoft Excel y Microsoft PowerPoint se pueden usar para crear gráficos VML.</span><span class="sxs-lookup"><span data-stu-id="303c3-128">Microsoft Word, Microsoft Excel, and Microsoft PowerPoint can be used to create VML graphics.</span></span>

### <a name="using-vml"></a><span data-ttu-id="303c3-129">Usar VML</span><span class="sxs-lookup"><span data-stu-id="303c3-129">Using VML</span></span>

<span data-ttu-id="303c3-130">Para usar VML en las páginas web, use un elemento de estilo para importar el comportamiento de VML, tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="303c3-130">To use VML in your web pages, use a style element to import the VML behavior, as shown in the following code.</span></span>

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

<span data-ttu-id="303c3-131">A continuación, declare el espacio de nombres VML, tal como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="303c3-131">Next, declare the VML namespace, as shown in the following code sample.</span></span>

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

<span data-ttu-id="303c3-132">Por último, agregue elementos VML para definir efectos visuales.</span><span class="sxs-lookup"><span data-stu-id="303c3-132">Finally, add VML elements to define visuals effects.</span></span> <span data-ttu-id="303c3-133">Por ejemplo, el siguiente código VML crea un óvalo rojo.</span><span class="sxs-lookup"><span data-stu-id="303c3-133">For example, the following VML code creates a red oval.</span></span>

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> <span data-ttu-id="303c3-134">Para obtener los mejores resultados cuando se usan documentos en modo Strict, asegúrese de que el marcado es válido y está bien formado.</span><span class="sxs-lookup"><span data-stu-id="303c3-134">For best results when using strict mode documents, be sure that your markup is valid and well-formed.</span></span> <span data-ttu-id="303c3-135">Para obtener más información, vea la. Página de referencia DOCTYPE.</span><span class="sxs-lookup"><span data-stu-id="303c3-135">For more information, please see the !DOCTYPE reference page.</span></span>


### <a name="benefits-of-vml"></a><span data-ttu-id="303c3-136">Ventajas de VML</span><span class="sxs-lookup"><span data-stu-id="303c3-136">Benefits of VML</span></span>

-   <span data-ttu-id="303c3-137">VML facilita la creación de usuarios y autores de productividad.</span><span class="sxs-lookup"><span data-stu-id="303c3-137">VML makes authoring easier for productivity users and authors.</span></span> <span data-ttu-id="303c3-138">Facilita el intercambio (a través de cortar y pegar) y la edición posterior de los gráficos vectoriales entre una gran variedad de aplicaciones de productividad y diseño.</span><span class="sxs-lookup"><span data-stu-id="303c3-138">It facilitates the exchange (via cut and paste) and subsequent editing of vector graphics between a wide variety of productivity and design applications.</span></span>
-   <span data-ttu-id="303c3-139">VML proporciona descargas gráficas más rápidas y una mejor experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="303c3-139">VML provides faster graphic downloads and a better user experience.</span></span> <span data-ttu-id="303c3-140">Permite la entrega de gráficos vectoriales escalables completamente integrados y de alta calidad en la web, en un formato basado en texto abierto.</span><span class="sxs-lookup"><span data-stu-id="303c3-140">It allows the delivery of high-quality, fully integrated, scalable vector graphics to the Web, in an open text-based format.</span></span> <span data-ttu-id="303c3-141">En lugar de hacer referencia a gráficos como archivos externos, los gráficos VML se entregan en línea con la página HTML, lo que les permite interactuar y escalar con la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="303c3-141">Rather than referencing graphics as external files, VML graphics are delivered inline with the HTML page, allowing them to interact and scale with user interaction.</span></span>
-   <span data-ttu-id="303c3-142">VML está abierto y basado en estándares.</span><span class="sxs-lookup"><span data-stu-id="303c3-142">VML is open and standards-based.</span></span> <span data-ttu-id="303c3-143">Es un formato basado en XML.</span><span class="sxs-lookup"><span data-stu-id="303c3-143">It is an XML-based format.</span></span> <span data-ttu-id="303c3-144">XML 1,0 es un lenguaje abierto, simple y basado en texto para describir los datos estructurados en la web y complementa el código HTML para mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="303c3-144">XML 1.0 is an open, simple, text-based language for describing structured data on the Web, and complements HTML for display.</span></span> <span data-ttu-id="303c3-145">VML también admite otros estándares del W3C, como Hojas de estilo CSS 2,0 (CSS), que especifica la información de estilo y la posición en 2D, así como el Document Object Model (DOM), que permite a los desarrolladores interactuar de forma coherente con los elementos de la página como objetos.</span><span class="sxs-lookup"><span data-stu-id="303c3-145">VML also supports other W3C standards, such as Cascading Style Sheets 2.0 (CSS), which specifies style information and 2-D positioning, as well as the Document Object Model (DOM), which allows developers to interact consistently with page elements as objects.</span></span>

### <a name="for-additional-information"></a><span data-ttu-id="303c3-146">Para obtener información adicional</span><span class="sxs-lookup"><span data-stu-id="303c3-146">For additional information</span></span>

<span data-ttu-id="303c3-147">Vea los vínculos siguientes:</span><span class="sxs-lookup"><span data-stu-id="303c3-147">See the links below:</span></span>

-   <span data-ttu-id="303c3-148">Para obtener respuestas a las preguntas más frecuentes sobre VML, vea las [preguntas más frecuentes sobre VML](frequently-asked-questions-about-vml.md).</span><span class="sxs-lookup"><span data-stu-id="303c3-148">For answers to frequently asked questions about VML, see the [VML FAQ](frequently-asked-questions-about-vml.md).</span></span>
-   <span data-ttu-id="303c3-149">Para ver un tutorial sobre el uso de VML en páginas web, consulte [Cómo usar VML en páginas web](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), que complementa la [especificación de VML](https://www.w3.org/TR/NOTE-datetime.html) enviada al W3C.</span><span class="sxs-lookup"><span data-stu-id="303c3-149">For a tutorial on using VML on Web pages, see [How to Use VML on Web Pages](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), which complements the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) submitted to the W3C.</span></span>
-   <span data-ttu-id="303c3-150">Para obtener información sobre los tipos de datos de VML, vea el documento [tipos básicos de VML](basic-vml-types.md) .</span><span class="sxs-lookup"><span data-stu-id="303c3-150">For information on VML data types, see the [Basic VML Types](basic-vml-types.md) document.</span></span>
-   <span data-ttu-id="303c3-151">Para obtener la referencia completa en VML, incluida la información sobre cómo usar VML con etiquetas y scripts, vea la [referencia de VML](msdn-online-vml-introduction.md).</span><span class="sxs-lookup"><span data-stu-id="303c3-151">For the complete reference on VML, including information on how to use VML with tags as well as scripting, see the [VML Reference](msdn-online-vml-introduction.md).</span></span>