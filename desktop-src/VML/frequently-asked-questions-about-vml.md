---
title: Preguntas más frecuentes sobre VML
description: Preguntas más frecuentes sobre VML
ms.assetid: f7f2ce12-facf-4042-b2a7-acaa3e25816a
keywords:
- Lenguaje de marcado de vectores (VML), p + f
- VML (Lenguaje de marcado de vectores), preguntas más frecuentes
- gráficos vectoriales, p + f
- Lenguaje de marcado de vectores (VML), preguntas más frecuentes
- VML (Lenguaje de marcado de vectores), preguntas más frecuentes
- gráficos vectoriales, preguntas más frecuentes
- Lenguaje de marcado de vectores (VML), diferencias de GIF
- VML (Lenguaje de marcado de vectores), diferencias de GIF
- Lenguaje de marcado de vectores (VML), diferencias de PNG
- VML (Lenguaje de marcado de vectores), diferencias de PNG
- gráficos vectoriales, diferencias de formato de tramas
- Lenguaje de marcado de vectores (VML), XML
- VML (Lenguaje de marcado de vectores), XML
- gráficos vectoriales, XML
- Lenguaje de marcado de vectores (VML), animación
- VML (Lenguaje de marcado de vectores), animación
- gráficos vectoriales, animación
- Lenguaje de marcado de vectores (VML), Macromedia Flash
- VML (Lenguaje de marcado de vectores), Macromedia Flash
- gráficos vectoriales, Macromedia Flash
- formatos de trama
- animación
- Macromedia Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e108f2055e7a0fbae1c5ed542fe68c59ec9b212b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995469"
---
# <a name="frequently-asked-questions-about-vml"></a><span data-ttu-id="bda18-126">Preguntas más frecuentes sobre VML</span><span class="sxs-lookup"><span data-stu-id="bda18-126">Frequently Asked Questions About VML</span></span>

<span data-ttu-id="bda18-127">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bda18-127">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bda18-128">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="bda18-128">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bda18-129">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="bda18-129">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bda18-130">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="bda18-130">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bda18-131">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bda18-131">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bda18-132">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bda18-132">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="does-vml-compete-with-gif-and-png"></a><span data-ttu-id="bda18-133">¿El VML compite con GIF y PNG?</span><span class="sxs-lookup"><span data-stu-id="bda18-133">Does VML compete with GIF and PNG?</span></span>

<span data-ttu-id="bda18-134">No.</span><span class="sxs-lookup"><span data-stu-id="bda18-134">No.</span></span> <span data-ttu-id="bda18-135">Tanto GIF como PNG son formatos de trama (o de mapa de bits) que se pueden usar para almacenar gráficos vectoriales.</span><span class="sxs-lookup"><span data-stu-id="bda18-135">Both GIF and PNG are raster (or bit-mapped) formats that can be used to store vector graphics.</span></span> <span data-ttu-id="bda18-136">Los formatos de trama almacenan cada píxel, mientras que los formatos vectoriales como VML usan descripciones matemáticas o esquemas para describir los gráficos.</span><span class="sxs-lookup"><span data-stu-id="bda18-136">Raster formats store every pixel, whereas vector formats such as VML use mathematical descriptions or outlines to describe the graphics.</span></span> <span data-ttu-id="bda18-137">Los gráficos vectoriales almacenados en un formato basado en vectores son más compactos que los almacenados en formatos de trama, lo que da lugar a tiempos de descarga más rápidos para los usuarios Web.</span><span class="sxs-lookup"><span data-stu-id="bda18-137">Vector graphics stored in a vector-based format are more compact than those stored in raster formats, resulting in faster download times for Web users.</span></span>

<span data-ttu-id="bda18-138">Además, los gráficos VML se entregan en línea a la página HTML en lugar de depender de archivos externos, como es el caso de los formatos GIF y PNG actuales.</span><span class="sxs-lookup"><span data-stu-id="bda18-138">In addition, VML graphics are delivered inline to the HTML page rather than relying on external files, as is the case with GIF and PNG today.</span></span> <span data-ttu-id="bda18-139">Esto permite que los gráficos VML escalen e interactúen con otros elementos de la página web a medida que se cambia el tamaño de la página, lo que mejora la experiencia del usuario final.</span><span class="sxs-lookup"><span data-stu-id="bda18-139">This allows VML graphics to scale and interact with other Web page elements as the page is resized, thus improving the end-user experience.</span></span>

<span data-ttu-id="bda18-140">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="bda18-140">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="why-is-microsoft-supporting-another-xml-based-standard-when-xml-is-hardly-in-use-and-is-young-enough-as-it-is"></a><span data-ttu-id="bda18-141">¿Por qué Microsoft admite otro estándar basado en XML cuando el código XML no está en uso y es lo suficientemente joven como?</span><span class="sxs-lookup"><span data-stu-id="bda18-141">Why is Microsoft supporting another XML-based standard when XML is hardly in use and is young enough as it is?</span></span>

<span data-ttu-id="bda18-142">XML es una manera eficaz y sencilla de representar datos estructurados en la web y complementa totalmente el HTML para su presentación.</span><span class="sxs-lookup"><span data-stu-id="bda18-142">XML is a powerful yet simple way to represent structured data on the Web, and fully complements HTML for display.</span></span> <span data-ttu-id="bda18-143">VML es un ejemplo de muchos formatos basados en XML específicos de la aplicación que se desarrollarán e implementarán en los próximos meses.</span><span class="sxs-lookup"><span data-stu-id="bda18-143">VML is one example of the many application-specific, XML-based formats that will be developed and implemented in the coming months.</span></span> <span data-ttu-id="bda18-144">Por ejemplo, en la siguiente versión de Office, VML se usará para anotar documentos HTML, para conservar la información de formato de los gráficos de Office Art entre el formato de archivo de Office nativo y HTML, lo que permite a los usuarios de Office cambiar sin problemas entre los dos formatos.</span><span class="sxs-lookup"><span data-stu-id="bda18-144">For instance, in the next version of Office, VML will be used to annotate HTML documents -- to preserve formatting information of Office Art graphics between the native Office file format and HTML, thus enabling Office users to switch seamlessly between the two formats.</span></span>

<span data-ttu-id="bda18-145">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="bda18-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="who-will-support-vml"></a><span data-ttu-id="bda18-146">¿Quién será compatible con VML?</span><span class="sxs-lookup"><span data-stu-id="bda18-146">Who will support VML?</span></span>

<span data-ttu-id="bda18-147">Esperamos que muchos proveedores admitan VML.</span><span class="sxs-lookup"><span data-stu-id="bda18-147">We expect many vendors to support VML.</span></span> <span data-ttu-id="bda18-148">Por ejemplo, Autodesk, Hewlett-Packard, Macromedia y VISIO han prometido la compatibilidad con VML en versiones futuras de sus productos.</span><span class="sxs-lookup"><span data-stu-id="bda18-148">For example, Autodesk, Hewlett-Packard, Macromedia, and VISIO have pledged support for VML in future versions of their products.</span></span> <span data-ttu-id="bda18-149">Microsoft ha prometido la compatibilidad con VML en versiones futuras de sus plataformas, como Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bda18-149">Microsoft has pledged support for VML in future versions of its platforms such as Internet Explorer.</span></span> <span data-ttu-id="bda18-150">Además, VML se usará en la próxima generación de Office para habilitar la acción de ida y vuelta entre el formato de Office y HTML.</span><span class="sxs-lookup"><span data-stu-id="bda18-150">In addition, VML will be used in the next generation of Office to enable "round-tripping" between the Office format and HTML.</span></span>

<span data-ttu-id="bda18-151">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="bda18-151">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="does-vml-support-animation"></a><span data-ttu-id="bda18-152">¿Admite VML la animación?</span><span class="sxs-lookup"><span data-stu-id="bda18-152">Does VML support animation?</span></span>

<span data-ttu-id="bda18-153">No, actualmente no.</span><span class="sxs-lookup"><span data-stu-id="bda18-153">No, it currently doesn't.</span></span> <span data-ttu-id="bda18-154">Sin embargo, estamos trabajando con nuestros asociados de VML para agregar funcionalidad de animación en el formato VML.</span><span class="sxs-lookup"><span data-stu-id="bda18-154">However, we are working with our VML partners to add animation capability into the VML format.</span></span> <span data-ttu-id="bda18-155">Dado que VML se basa en XML, el conjunto de etiquetas se puede extender fácilmente para obtener funcionalidad adicional.</span><span class="sxs-lookup"><span data-stu-id="bda18-155">Since VML is based on XML, the tag set can be easily extended for additional functionality.</span></span>

<span data-ttu-id="bda18-156">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="bda18-156">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="does-vml-replace-macromedia-flash-didnt-macromedia-just-submit-their-flash-format-for-vector-graphics-to-the-w3c"></a><span data-ttu-id="bda18-157">¿Reemplaza VML Macromedia Flash?</span><span class="sxs-lookup"><span data-stu-id="bda18-157">Does VML replace Macromedia Flash?</span></span> <span data-ttu-id="bda18-158">¿No se ha enviado Macromedia el formato Flash para los gráficos vectoriales al W3C?</span><span class="sxs-lookup"><span data-stu-id="bda18-158">Didn't Macromedia just submit their Flash format for vector graphics to the W3C?</span></span>

<span data-ttu-id="bda18-159">No.</span><span class="sxs-lookup"><span data-stu-id="bda18-159">No.</span></span> <span data-ttu-id="bda18-160">VML es un formato de entrega y de intercambio basado en texto para gráficos vectoriales, mientras que Flash es un formato binario para la entrega de gráficos basados en vectores y animaciones.</span><span class="sxs-lookup"><span data-stu-id="bda18-160">VML is a text-based interchange and delivery format for vector graphics, whereas Flash is a binary format for the delivery of vector-based graphics and animation.</span></span>

<span data-ttu-id="bda18-161">Macromedia no ha enviado su formato de archivo al W3C.</span><span class="sxs-lookup"><span data-stu-id="bda18-161">Macromedia did not submit their file format to the W3C.</span></span> <span data-ttu-id="bda18-162">Sin embargo, abrieron su formato de archivo para los desarrolladores de aplicaciones, los desarrolladores web y los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="bda18-162">However, they did open their file format up for application developers, Web developers and end users.</span></span> <span data-ttu-id="bda18-163">Consulte <https://www.macromedia.com> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="bda18-163">See <https://www.macromedia.com> for more information.</span></span>

[<span data-ttu-id="bda18-164">Volver a la información general de VML</span><span class="sxs-lookup"><span data-stu-id="bda18-164">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

 