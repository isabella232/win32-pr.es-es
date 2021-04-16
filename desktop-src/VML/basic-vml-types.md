---
title: Tipos VML básicos
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Migre las páginas web y las aplicaciones que se basan en VML en SVG u otros estándares ampliamente admitidos.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Lenguaje de marcado de vectores (VML), tipos básicos
- VML (Lenguaje de marcado de vectores), tipos básicos
- gráficos vectoriales, tipos básicos de VML
- Lenguaje de marcado de vectores (VML), tipos
- VML (Lenguaje de marcado de vectores), tipos
- gráficos vectoriales, tipos VML
- tipos VML básicos
- tipo booleano
- tipo de fracción
- tipo de ordinal
- tipo de longitud
- tipo de medida
- tipo de ángulo
- tipo de color
- tipo de fuente
- tipo de mapa de bits
- tipo de vector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05b058c919496b608b875f96e6c03bbeb0d50e8
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104557360"
---
# <a name="basic-vml-types"></a><span data-ttu-id="e7842-121">Tipos VML básicos</span><span class="sxs-lookup"><span data-stu-id="e7842-121">Basic VML Types</span></span>

<span data-ttu-id="e7842-122">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e7842-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e7842-123">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="e7842-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e7842-124">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="e7842-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e7842-125">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="e7842-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e7842-126">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e7842-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e7842-127">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e7842-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e7842-128">**Contents**</span><span class="sxs-lookup"><span data-stu-id="e7842-128">**Contents**</span></span>

-   [<span data-ttu-id="e7842-129">Introducción</span><span class="sxs-lookup"><span data-stu-id="e7842-129">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="e7842-130">boolean</span><span class="sxs-lookup"><span data-stu-id="e7842-130">boolean</span></span>](#boolean)
-   [<span data-ttu-id="e7842-131">fraction</span><span class="sxs-lookup"><span data-stu-id="e7842-131">fraction</span></span>](#fraction)
-   [<span data-ttu-id="e7842-132">ordinal</span><span class="sxs-lookup"><span data-stu-id="e7842-132">ordinate</span></span>](#ordinate)
-   [<span data-ttu-id="e7842-133">length</span><span class="sxs-lookup"><span data-stu-id="e7842-133">length</span></span>](#length)
    -   [<span data-ttu-id="e7842-134">Representaciones alternativas</span><span class="sxs-lookup"><span data-stu-id="e7842-134">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="e7842-135">Medi</span><span class="sxs-lookup"><span data-stu-id="e7842-135">measure</span></span>](#measure)
    -   [<span data-ttu-id="e7842-136">Representaciones alternativas</span><span class="sxs-lookup"><span data-stu-id="e7842-136">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="e7842-137">angle</span><span class="sxs-lookup"><span data-stu-id="e7842-137">angle</span></span>](#angle)
    -   [<span data-ttu-id="e7842-138">Representaciones alternativas</span><span class="sxs-lookup"><span data-stu-id="e7842-138">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="e7842-139">color</span><span class="sxs-lookup"><span data-stu-id="e7842-139">color</span></span>](#color)
    -   [<span data-ttu-id="e7842-140">Unidades de color</span><span class="sxs-lookup"><span data-stu-id="e7842-140">Color units</span></span>](#color-units)
    -   [<span data-ttu-id="e7842-141">Colores HTML</span><span class="sxs-lookup"><span data-stu-id="e7842-141">HTML colors</span></span>](#html-colors)
    -   [<span data-ttu-id="e7842-142">Colores de esquema</span><span class="sxs-lookup"><span data-stu-id="e7842-142">Scheme colors</span></span>](#scheme-colors)
    -   [<span data-ttu-id="e7842-143">Colores del sistema</span><span class="sxs-lookup"><span data-stu-id="e7842-143">System colors</span></span>](#system-colors)
    -   [<span data-ttu-id="e7842-144">Colores puros</span><span class="sxs-lookup"><span data-stu-id="e7842-144">Pure colors</span></span>](#pure-colors)
    -   [<span data-ttu-id="e7842-145">Ajustes de color</span><span class="sxs-lookup"><span data-stu-id="e7842-145">Color adjustments</span></span>](#color-adjustments)
-   [<span data-ttu-id="e7842-146">tipo</span><span class="sxs-lookup"><span data-stu-id="e7842-146">font</span></span>](#font)
-   [<span data-ttu-id="e7842-147">bitmap</span><span class="sxs-lookup"><span data-stu-id="e7842-147">bitmap</span></span>](#bitmap)
    -   [<span data-ttu-id="e7842-148">Formatos de archivo de imagen</span><span class="sxs-lookup"><span data-stu-id="e7842-148">Picture file formats</span></span>](#picture-file-formats)
-   [<span data-ttu-id="e7842-149">medios</span><span class="sxs-lookup"><span data-stu-id="e7842-149">vector</span></span>](#vector)

## <a name="introduction"></a><span data-ttu-id="e7842-150">Introducción</span><span class="sxs-lookup"><span data-stu-id="e7842-150">Introduction</span></span>

<span data-ttu-id="e7842-151">Esta propuesta usa un pequeño número de tipos básicos, que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e7842-151">This proposal uses a small number of basic types, listed in the table below.</span></span>



| <span data-ttu-id="e7842-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7842-152">Type</span></span>                  | <span data-ttu-id="e7842-153">Elemento</span><span class="sxs-lookup"><span data-stu-id="e7842-153">Element</span></span>           | <span data-ttu-id="e7842-154">Representación fundamental</span><span class="sxs-lookup"><span data-stu-id="e7842-154">Fundamental Representation</span></span> | <span data-ttu-id="e7842-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7842-155">Description</span></span>                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7842-156">boolean</span><span class="sxs-lookup"><span data-stu-id="e7842-156">boolean</span></span>](#boolean)   |                   | <span data-ttu-id="e7842-157">1 bit</span><span class="sxs-lookup"><span data-stu-id="e7842-157">1 bit</span></span>                      | <span data-ttu-id="e7842-158">Valor booleano: true o false.</span><span class="sxs-lookup"><span data-stu-id="e7842-158">A boolean value: true or false.</span></span>                                                                      |
| [<span data-ttu-id="e7842-159">fraction</span><span class="sxs-lookup"><span data-stu-id="e7842-159">fraction</span></span>](#fraction) |                   | <span data-ttu-id="e7842-160">número 2 6</span><span class="sxs-lookup"><span data-stu-id="e7842-160">number 2 6</span></span>                 | <span data-ttu-id="e7842-161">Un valor numérico, escalado por 2 6 (65536) y almacenado como un entero con signo.</span><span class="sxs-lookup"><span data-stu-id="e7842-161">A numeric value, scaled by 2 6 (65536) and stored as a signed integer.</span></span>                               |
| [<span data-ttu-id="e7842-162">ordinal</span><span class="sxs-lookup"><span data-stu-id="e7842-162">ordinate</span></span>](#ordinate) |                   | <span data-ttu-id="e7842-163">signo más de entero de 30 bits</span><span class="sxs-lookup"><span data-stu-id="e7842-163">30-bit integer plus sign</span></span>   | <span data-ttu-id="e7842-164">Parte de una coordenada (por ejemplo, en una ruta de acceso), los valores definidos por coordenadas.</span><span class="sxs-lookup"><span data-stu-id="e7842-164">Part of a coordinate (e.g., in a path ), the values defined by coord.</span></span>                                |
| [<span data-ttu-id="e7842-165">length</span><span class="sxs-lookup"><span data-stu-id="e7842-165">length</span></span>](#length)     |                   | [<span data-ttu-id="e7842-166">PERTENEZCA</span><span class="sxs-lookup"><span data-stu-id="e7842-166">EMU</span></span>](#length)             | <span data-ttu-id="e7842-167">Una longitud física, como el ancho de una línea o el tamaño de una fuente.</span><span class="sxs-lookup"><span data-stu-id="e7842-167">A physical length, such as the width of a line or the size of a font.</span></span>                                |
| [<span data-ttu-id="e7842-168">Medi</span><span class="sxs-lookup"><span data-stu-id="e7842-168">measure</span></span>](#measure)   |                   | <span data-ttu-id="e7842-169">UME o número 2 6</span><span class="sxs-lookup"><span data-stu-id="e7842-169">EMU or number 2 6</span></span>          | <span data-ttu-id="e7842-170">Una longitud física, incluido un número de píxeles del dispositivo o una fracción de otra cantidad.</span><span class="sxs-lookup"><span data-stu-id="e7842-170">Either a physical length, including a number of device pixels, or a fraction of some other quantity.</span></span> |
| [<span data-ttu-id="e7842-171">angle</span><span class="sxs-lookup"><span data-stu-id="e7842-171">angle</span></span>](#angle)       |                   | <span data-ttu-id="e7842-172">grados 2 6</span><span class="sxs-lookup"><span data-stu-id="e7842-172">degrees 2 6</span></span>                | <span data-ttu-id="e7842-173">Un ángulo; Positive es el sentido de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="e7842-173">An angle; positive is clockwise.</span></span>                                                                     |
| [<span data-ttu-id="e7842-174">color</span><span class="sxs-lookup"><span data-stu-id="e7842-174">color</span></span>](#color)       | [<span data-ttu-id="e7842-175">c</span><span class="sxs-lookup"><span data-stu-id="e7842-175">c</span></span>](#color)       | <span data-ttu-id="e7842-176">complejas</span><span class="sxs-lookup"><span data-stu-id="e7842-176">complex</span></span>                    | <span data-ttu-id="e7842-177">Elemento que permite derivar un color.</span><span class="sxs-lookup"><span data-stu-id="e7842-177">An element that allows a color to be derived.</span></span>                                                        |
| [<span data-ttu-id="e7842-178">tipo</span><span class="sxs-lookup"><span data-stu-id="e7842-178">font</span></span>](#font)         | [<span data-ttu-id="e7842-179">tipo</span><span class="sxs-lookup"><span data-stu-id="e7842-179">font</span></span>](#font)     | <span data-ttu-id="e7842-180">complejas</span><span class="sxs-lookup"><span data-stu-id="e7842-180">complex</span></span>                    | <span data-ttu-id="e7842-181">Descripción de una fuente.</span><span class="sxs-lookup"><span data-stu-id="e7842-181">A description of a font.</span></span>                                                                             |
| [<span data-ttu-id="e7842-182">bitmap</span><span class="sxs-lookup"><span data-stu-id="e7842-182">bitmap</span></span>](#bitmap)     | [<span data-ttu-id="e7842-183">bitmap</span><span class="sxs-lookup"><span data-stu-id="e7842-183">bitmap</span></span>](#bitmap) | <span data-ttu-id="e7842-184">href</span><span class="sxs-lookup"><span data-stu-id="e7842-184">href</span></span>                       | <span data-ttu-id="e7842-185">Referencia a un archivo de imagen externo.</span><span class="sxs-lookup"><span data-stu-id="e7842-185">A reference to an external picture file.</span></span>                                                             |
| [<span data-ttu-id="e7842-186">medios</span><span class="sxs-lookup"><span data-stu-id="e7842-186">vector</span></span>](#vector)     | [<span data-ttu-id="e7842-187">v</span><span class="sxs-lookup"><span data-stu-id="e7842-187">v</span></span>](#vector)      | <span data-ttu-id="e7842-188">complejas</span><span class="sxs-lookup"><span data-stu-id="e7842-188">complex</span></span>                    | <span data-ttu-id="e7842-189">Descripción de una ruta de acceso de vector</span><span class="sxs-lookup"><span data-stu-id="e7842-189">A description of a vector path</span></span>                                                                       |



 

<span data-ttu-id="e7842-190">La "representación fundamental" es la representación de precisión más alta que la propuesta requiere que el mantenimiento de una implementación conforme. los datos se perderán si la implementación no puede representar los datos con la precisión requerida.</span><span class="sxs-lookup"><span data-stu-id="e7842-190">The "fundamental representation" is the highest precision representation that the proposal requires a conforming implementation to maintain; data will be lost if the implementation is not able to represent the data to the precision required.</span></span> <span data-ttu-id="e7842-191">Los tipos de color, fuente y Vector corresponden a los elementos que tienen la misma estructura, en cierto sentido, no son tipos básicos. sin embargo, es conveniente tratarlos como tal en esta propuesta.</span><span class="sxs-lookup"><span data-stu-id="e7842-191">The color, font, and vector types correspond to elements which themselves have structure -- in a sense, they are not basic types; however, it is convenient to treat them as such within this proposal.</span></span>

<span data-ttu-id="e7842-192">Cada tipo básico no complejo tiene un elemento asociado con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="e7842-192">Each non-complex basic type has an associated element of the same name.</span></span> <span data-ttu-id="e7842-193">Estos nombres de elemento están reservados y no se pueden usar para ningún otro propósito dentro de las extensiones, incluso si el uso está dentro de un elemento de extensión de vista "SKIP".</span><span class="sxs-lookup"><span data-stu-id="e7842-193">These element names are reserved and may not be used for any other purpose within extensions, even if the use is within an onview="skip" extension element.</span></span> <span data-ttu-id="e7842-194">Debido a esto, es posible que una implementación que encuentra XML desconocido proporcione un almacenamiento interno eficaz del XML desconocido, siempre y cuando los valores se incluyan en los elementos "tipo".</span><span class="sxs-lookup"><span data-stu-id="e7842-194">Because of this, it is possible for an implementation that encounters unknown XML to provide efficient internal storage of the unknown XML as long as the values are enclosed in the "type" elements.</span></span>


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



<span data-ttu-id="e7842-195">En el primer ejemplo anterior, la cadena "1,578" se debe almacenar como una secuencia de caracteres (la implementación no sabe si es una cadena o un número). en el segundo ejemplo, el elemento de fracción indica que el contenido es un número, por lo que se puede convertir en la representación de fracción de precisión alta.</span><span class="sxs-lookup"><span data-stu-id="e7842-195">In the first example above, the string "1.578" must be stored as a sequence of characters (the implementation does not know whether it is a string or a number); in the second example, the fraction element indicates that the content is a number, thus it may be converted to the high precision fraction representation.</span></span>

<span data-ttu-id="e7842-196">Los tipos complejos (incluido el mapa de bits) tienen asociados nombres de elementos que se utilizan para delimitar el valor.</span><span class="sxs-lookup"><span data-stu-id="e7842-196">Complex types (including bitmap) have associated element names that are used to delimit the value.</span></span> <span data-ttu-id="e7842-197">Esto simplifica el análisis asegurándose de que las tareas de análisis más complejas estén asociadas a etiquetas de elementos únicas.</span><span class="sxs-lookup"><span data-stu-id="e7842-197">This simplifies parsing by ensuring that the more complex parsing tasks are associated with unique element tags.</span></span>

<span data-ttu-id="e7842-198">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-198">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="boolean"></a><span data-ttu-id="e7842-199">boolean</span><span class="sxs-lookup"><span data-stu-id="e7842-199">boolean</span></span>


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="e7842-200">Un valor booleano se representa como una palabra clave que indica el estado de la marca.</span><span class="sxs-lookup"><span data-stu-id="e7842-200">A boolean value is represented as a keyword indicating the state of the flag.</span></span> <span data-ttu-id="e7842-201">Las palabras clave siguientes están definidas.</span><span class="sxs-lookup"><span data-stu-id="e7842-201">The following keywords are defined.</span></span>



| <span data-ttu-id="e7842-202">Valor para true</span><span class="sxs-lookup"><span data-stu-id="e7842-202">Value for true</span></span> | <span data-ttu-id="e7842-203">Valor para false</span><span class="sxs-lookup"><span data-stu-id="e7842-203">Value for false</span></span> |
|----------------|-----------------|
| <span data-ttu-id="e7842-204">true</span><span class="sxs-lookup"><span data-stu-id="e7842-204">true</span></span>           | <span data-ttu-id="e7842-205">false</span><span class="sxs-lookup"><span data-stu-id="e7842-205">false</span></span>           |
| <span data-ttu-id="e7842-206">sí</span><span class="sxs-lookup"><span data-stu-id="e7842-206">yes</span></span>            | <span data-ttu-id="e7842-207">no</span><span class="sxs-lookup"><span data-stu-id="e7842-207">no</span></span>              |
| <span data-ttu-id="e7842-208">en</span><span class="sxs-lookup"><span data-stu-id="e7842-208">on</span></span>             | <span data-ttu-id="e7842-209">apagado</span><span class="sxs-lookup"><span data-stu-id="e7842-209">off</span></span>             |
| <span data-ttu-id="e7842-210">t</span><span class="sxs-lookup"><span data-stu-id="e7842-210">t</span></span>              | <span data-ttu-id="e7842-211">f</span><span class="sxs-lookup"><span data-stu-id="e7842-211">f</span></span>               |
| <span data-ttu-id="e7842-212">1</span><span class="sxs-lookup"><span data-stu-id="e7842-212">1</span></span>              | <span data-ttu-id="e7842-213">0</span><span class="sxs-lookup"><span data-stu-id="e7842-213">0</span></span>               |



 

<span data-ttu-id="e7842-214">Una implementación puede escribir cualquier valor y debe reconocer todos los valores.</span><span class="sxs-lookup"><span data-stu-id="e7842-214">An implementation may write any value and must recognize all values.</span></span> <span data-ttu-id="e7842-215">Una implementación es gratuita para cambiar los valores de una representación a otra.</span><span class="sxs-lookup"><span data-stu-id="e7842-215">An implementation is free to change values from one representation to another.</span></span>

<span data-ttu-id="e7842-216">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-216">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="fraction"></a><span data-ttu-id="e7842-217">fraction</span><span class="sxs-lookup"><span data-stu-id="e7842-217">fraction</span></span>


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="e7842-218">Todos los valores numéricos (es decir, los valores de cantidades no dimensionales) dentro de esta propuesta se pueden almacenar como enteros si se escalan por 2 6 (65536).</span><span class="sxs-lookup"><span data-stu-id="e7842-218">All numeric values (i.e., values of dimensionless quantities) within this proposal can be stored as integers by scaling them by 2  6 (65536).</span></span> <span data-ttu-id="e7842-219">Se puede proporcionar un número en este formulario, con el sufijo f o como un número decimal sin sufijo.</span><span class="sxs-lookup"><span data-stu-id="e7842-219">A number may be given either in this form, with the suffix f or as a decimal number with no suffix.</span></span> <span data-ttu-id="e7842-220">Por lo tanto, los siguientes elementos hipotéticos representan el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="e7842-220">Thus, the following hypothetical elements represent the same value.</span></span>


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



<span data-ttu-id="e7842-221">Una cantidad con el sufijo f debe ser un número entero; no se permiten números fraccionarios.</span><span class="sxs-lookup"><span data-stu-id="e7842-221">A quantity with the f suffix must be a whole number; fractional numbers are not permitted.</span></span> <span data-ttu-id="e7842-222">El entero resultante debe ser representable como un número de complemento de 32 bits 2. por lo tanto, el intervalo efectivo de la representación es 32768 (de hecho, menor que 32768 y mayor o igual que-32768).</span><span class="sxs-lookup"><span data-stu-id="e7842-222">The resultant integer must be representable as a 32-bit 2's complement signed number; thus, the effective range of the representation is  32768 (in fact, less than 32768 and greater than or equal to -32768.)</span></span>

<span data-ttu-id="e7842-223">Se requiere una implementación compatible para conservar los valores que se expresan como valores f.</span><span class="sxs-lookup"><span data-stu-id="e7842-223">A conforming implementation is required to preserve values that are expressed as f values.</span></span> <span data-ttu-id="e7842-224">Los valores representados como números decimales se pueden convertir a un valor f y almacenarlos de este modo.</span><span class="sxs-lookup"><span data-stu-id="e7842-224">Values represented as decimal numbers may be converted to an f value and stored that way.</span></span> <span data-ttu-id="e7842-225">Una aplicación puede registrar valores generados internamente en cualquier unidad adecuada; sin embargo, un valor leído de un documento existente debe mantenerse en la precisión original completa o debe convertirse en un valor f.</span><span class="sxs-lookup"><span data-stu-id="e7842-225">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an f value.</span></span>

<span data-ttu-id="e7842-226">Si la implementación no puede hacerlo, debe advertir al usuario de que se pueden perder datos.</span><span class="sxs-lookup"><span data-stu-id="e7842-226">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="e7842-227">(Es aceptable emitir una advertencia de este tipo cuando se encuentren los datos generados externamente).</span><span class="sxs-lookup"><span data-stu-id="e7842-227">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="e7842-228">Cuando un valor decimal se convierte en formato f, la implementación puede utilizar cualquier modo de redondeo aritmético; sin embargo, un número entero se debe convertir al formato f exactamente.</span><span class="sxs-lookup"><span data-stu-id="e7842-228">When a decimal value is converted into f format, the implementation may use any arithmetic rounding mode; however, a whole number must be converted to the f format exactly.</span></span> <span data-ttu-id="e7842-229">Se recomienda que las implementaciones se conviertan por redondeo a menos infinito y que la conversión siempre sea exacta.</span><span class="sxs-lookup"><span data-stu-id="e7842-229">It is recommended that implementations convert by rounding to minus infinity and that the convertion always be exact.</span></span>

<span data-ttu-id="e7842-230">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-230">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="ordinate"></a><span data-ttu-id="e7842-231">ordinal</span><span class="sxs-lookup"><span data-stu-id="e7842-231">ordinate</span></span>


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="e7842-232">Las unidades del sistema de coordenadas establecido por coordenadas son de algún tipo nominal, que se conoce como ordinal.</span><span class="sxs-lookup"><span data-stu-id="e7842-232">The units of the coordinate system established by coord are of some nominal type, which is referred to as ordinate.</span></span> <span data-ttu-id="e7842-233">Se trata de una medida de longitud, pero solo se usa en relación con el rectángulo que establece la coordenadas.</span><span class="sxs-lookup"><span data-stu-id="e7842-233">This is a measure of length, but it is only used in relation to the rectangle that coord establishes.</span></span> <span data-ttu-id="e7842-234">Cualquier valor de tipo ordinal se escalará con los valores *w* y *h* de la coordenadas y la relación resultante utilizada para establecer una medición real en el dispositivo de salida.</span><span class="sxs-lookup"><span data-stu-id="e7842-234">Any value of type ordinate will be scaled by the *w* and *h* values of the coord and the resulting ratio used to establish a real measurement on the output device.</span></span>

<span data-ttu-id="e7842-235">Una implementación compatible debe ser capaz de controlar valores ordinales de hasta 30 bits más signo (es decir, un entero con signo de 31 bits, no un entero con signo de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="e7842-235">A conforming implementation must be able to handle ordinate values of up to 30 bits plus sign (i.e., a 31-bit signed integer, not a 32-bit signed integer).</span></span> <span data-ttu-id="e7842-236">No obstante, se recomienda que las implementaciones intenten generar coordenadas para la ruta de acceso y elementos similares que tengan aproximadamente 16 bits de precisión.</span><span class="sxs-lookup"><span data-stu-id="e7842-236">It is recommended, however, that implementations attempt to produce coordinates for path and similar elements that have about 16 bits of precision.</span></span> <span data-ttu-id="e7842-237">Esto minimizará la posibilidad de subdesbordamiento o desbordamiento en una implementación no conforme.</span><span class="sxs-lookup"><span data-stu-id="e7842-237">This will minimize the chance of either underflow or overflow in a non-conforming implementation.</span></span>

<span data-ttu-id="e7842-238">los valores de ordinales son siempre integrales.</span><span class="sxs-lookup"><span data-stu-id="e7842-238">ordinate values are always integral.</span></span> <span data-ttu-id="e7842-239">Un separador decimal no puede aparecer en un valor de tipo ordinal.</span><span class="sxs-lookup"><span data-stu-id="e7842-239">A decimal point may not appear in a value of type ordinate.</span></span> <span data-ttu-id="e7842-240">No se pueden anexar especificadores de unidad a valores de tipo ordinal.</span><span class="sxs-lookup"><span data-stu-id="e7842-240">No unit specifiers may be appended to values of type ordinate.</span></span>

<span data-ttu-id="e7842-241">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-241">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="length"></a><span data-ttu-id="e7842-242">length</span><span class="sxs-lookup"><span data-stu-id="e7842-242">length</span></span>


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="e7842-243">Una longitud es una medida real o, a veces, una medida en píxeles del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7842-243">A length is a real-world measurement or, sometimes, a measurement in device pixels.</span></span> <span data-ttu-id="e7842-244">Se recomienda que las implementaciones eviten el uso de píxeles del dispositivo (PX).</span><span class="sxs-lookup"><span data-stu-id="e7842-244">It is recommended that implementations avoid the use of device pixels (px).</span></span>

<span data-ttu-id="e7842-245">Todos los calificadores de unidad de [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) estándar se permiten en una longitud.</span><span class="sxs-lookup"><span data-stu-id="e7842-245">All the standard [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) unit qualifiers are permitted on a length.</span></span> <span data-ttu-id="e7842-246">Además, se puede usar el calificador UEM.</span><span class="sxs-lookup"><span data-stu-id="e7842-246">In addition, the qualifier emu may be used.</span></span> <span data-ttu-id="e7842-247">Este calificador hace referencia a una unidad, la UME (unidad de métricas en inglés), que es un denominador común de las cantidades de medida en uso generalizado en gráficos de equipos.</span><span class="sxs-lookup"><span data-stu-id="e7842-247">This qualifier refers to a unit -- the EMU (English Metric Unit) -- which is a common denominator of the measurement quantities in widespread use in computer graphics.</span></span> <span data-ttu-id="e7842-248">La UEM es de <sup>pulgada</sup> /914400, es decir, hay 914400 UME por pulgada.</span><span class="sxs-lookup"><span data-stu-id="e7842-248">The EMU is <sup>inch</sup> / 914400, i.e., there are 914400 EMU per inch.</span></span> <span data-ttu-id="e7842-249">En la tabla siguiente se muestra el número de EMUs en un número pequeño de unidades que se encuentran normalmente.</span><span class="sxs-lookup"><span data-stu-id="e7842-249">The following table lists the number of EMUs in a small number of commonly encountered units.</span></span>



| <span data-ttu-id="e7842-250">Número de EMUs</span><span class="sxs-lookup"><span data-stu-id="e7842-250">Number of EMUs</span></span> | <span data-ttu-id="e7842-251">Número por pulgada</span><span class="sxs-lookup"><span data-stu-id="e7842-251">Number per Inch</span></span> | <span data-ttu-id="e7842-252">Número por milímetro</span><span class="sxs-lookup"><span data-stu-id="e7842-252">Number per Millimeter</span></span> | <span data-ttu-id="e7842-253">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7842-253">Description</span></span>             |
|----------------|-----------------|-----------------------|-------------------------|
| <span data-ttu-id="e7842-254">360</span><span class="sxs-lookup"><span data-stu-id="e7842-254">360</span></span>            |                 | <span data-ttu-id="e7842-255">0,01</span><span class="sxs-lookup"><span data-stu-id="e7842-255">0.01</span></span>                  | <span data-ttu-id="e7842-256">Win32 HIMETRIC</span><span class="sxs-lookup"><span data-stu-id="e7842-256">Win32 HIMETRIC</span></span>          |
| <span data-ttu-id="e7842-257">12700</span><span class="sxs-lookup"><span data-stu-id="e7842-257">12700</span></span>          | <span data-ttu-id="e7842-258">72</span><span class="sxs-lookup"><span data-stu-id="e7842-258">72</span></span>              |                       | <span data-ttu-id="e7842-259">Elija</span><span class="sxs-lookup"><span data-stu-id="e7842-259">"point"</span></span>                 |
| <span data-ttu-id="e7842-260">635</span><span class="sxs-lookup"><span data-stu-id="e7842-260">635</span></span>            | <span data-ttu-id="e7842-261">1440</span><span class="sxs-lookup"><span data-stu-id="e7842-261">1440</span></span>            |                       | <span data-ttu-id="e7842-262">Win32 TWIP</span><span class="sxs-lookup"><span data-stu-id="e7842-262">Win32 TWIP</span></span>              |
| <span data-ttu-id="e7842-263">762</span><span class="sxs-lookup"><span data-stu-id="e7842-263">762</span></span>            | <span data-ttu-id="e7842-264">1200</span><span class="sxs-lookup"><span data-stu-id="e7842-264">1200</span></span>            |                       | <span data-ttu-id="e7842-265">Impresora de alta resolución</span><span class="sxs-lookup"><span data-stu-id="e7842-265">High-resolution printer</span></span> |



 

<span data-ttu-id="e7842-266">No se permiten números fraccionarios de EMUs.</span><span class="sxs-lookup"><span data-stu-id="e7842-266">Fractional numbers of EMUs are not permitted.</span></span> <span data-ttu-id="e7842-267">Cualquier medida debe representarse como un número entero con signo de 32 bits de EMUs; esto limita la magnitud de una medida a 2348 pulgadas: aproximadamente 59 metros o 65 metros.</span><span class="sxs-lookup"><span data-stu-id="e7842-267">Any measurement must be representable as a 32-bit signed integral number of EMUs -- this limits the magnitude of a measurement to 2348 inches -- about 59 meters or 65 yards.</span></span> <span data-ttu-id="e7842-268">Dado que las mediciones siempre hacen referencia al tamaño de una representación en un dispositivo de salida de pantalla o de tamaño de página nominal, siempre estarán dentro de este intervalo.</span><span class="sxs-lookup"><span data-stu-id="e7842-268">Because the measurements always refer to the size of a rendering on a nominally screen- or page-sized output device, they will always be within this range.</span></span>

<span data-ttu-id="e7842-269">No obstante, tenga en cuenta que la representación no es adecuada para las mediciones del mundo real y que se registran (por ejemplo, para registrar el tamaño real de una ruta de acceso) se debe usar otra representación.</span><span class="sxs-lookup"><span data-stu-id="e7842-269">Notice, however, that the representation is inappropriate for real-world measurements and that where these are recorded (for example, to record the real-world size of a path) some other representation must be used.</span></span>

<span data-ttu-id="e7842-270">Se requiere una implementación compatible para conservar los valores que son un número exacto de EMUs.</span><span class="sxs-lookup"><span data-stu-id="e7842-270">A conforming implementation is required to preserve values that are exact numbers of EMUs.</span></span> <span data-ttu-id="e7842-271">Los valores representados de otra forma se pueden convertir a un valor de UEM y almacenarse de esta manera.</span><span class="sxs-lookup"><span data-stu-id="e7842-271">Values represented in any other way may be converted to an EMU value and stored that way.</span></span> <span data-ttu-id="e7842-272">Una aplicación puede registrar valores generados internamente en cualquier unidad adecuada; sin embargo, un valor leído de un documento existente debe mantenerse en la precisión original completa o debe convertirse en un valor de UEM.</span><span class="sxs-lookup"><span data-stu-id="e7842-272">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an EMU value.</span></span>

<span data-ttu-id="e7842-273">Si la implementación no puede hacerlo, debe advertir al usuario de que se pueden perder datos.</span><span class="sxs-lookup"><span data-stu-id="e7842-273">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="e7842-274">(Es aceptable emitir una advertencia de este tipo cuando se encuentren los datos generados externamente).</span><span class="sxs-lookup"><span data-stu-id="e7842-274">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="e7842-275">En la práctica, la longitud física se usa para relativamente pocas mediciones en esta propuesta.</span><span class="sxs-lookup"><span data-stu-id="e7842-275">In practice, physical lengths are used for relatively few measurements in this proposal.</span></span> <span data-ttu-id="e7842-276">Los datos que suelen ser más importantes son los datos de la ruta de acceso y se codifican en el sistema de coordenadas definido, de forma individual, por coordenadas.</span><span class="sxs-lookup"><span data-stu-id="e7842-276">The data which is normally most important is the path data and this is encoded in the coordinate system defined, on a per-shape basis, by coord.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="e7842-277">Representaciones alternativas</span><span class="sxs-lookup"><span data-stu-id="e7842-277">Alternative representations</span></span>

<span data-ttu-id="e7842-278">Las representaciones de longitud estándar de HTML se definen mediante [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span><span class="sxs-lookup"><span data-stu-id="e7842-278">The standard length representations of HTML are defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span></span> <span data-ttu-id="e7842-279">Las unidades relativas, con la excepción del píxel, no son significativas en el contexto en el que se usan las longitudes en esta propuesta y no deben usarse.</span><span class="sxs-lookup"><span data-stu-id="e7842-279">Relative units, with the exception of the pixel, are not meaningful in the context within which lengths are used in this proposal and must not be used.</span></span> <span data-ttu-id="e7842-280">Si el documento registra el tamaño de píxel previsto (destino), define la traslación de píxeles en la UME; de lo contrario, debe usarse el valor predeterminado de 90 PPP definido por [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span><span class="sxs-lookup"><span data-stu-id="e7842-280">If the document records the intended (target) pixel size, this defines the translation of pixels into EMU; otherwise, the default of 90 dpi defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) should be used.</span></span>

<span data-ttu-id="e7842-281">Con la excepción de la UEM, cualquier valor se puede proporcionar como una fracción decimal.</span><span class="sxs-lookup"><span data-stu-id="e7842-281">With the exception of emu, any value may be given as a decimal fraction.</span></span> <span data-ttu-id="e7842-282">Cuando se convierte un valor decimal en la UME, la implementación puede utilizar cualquier modo de redondeo aritmético.</span><span class="sxs-lookup"><span data-stu-id="e7842-282">When a decimal value is converted to EMU, the implementation may use any arithmetic rounding mode.</span></span> <span data-ttu-id="e7842-283">(La única manera de que una aplicación de creación garantice un resultado determinado es especificarla en la UEM).</span><span class="sxs-lookup"><span data-stu-id="e7842-283">(The only way for an authoring application to guarantee a particular result is to specify it in emu.)</span></span>

<span data-ttu-id="e7842-284">Si no se proporciona ningún especificador de unidad en un valor de longitud, la implementación debe asumir la UME.</span><span class="sxs-lookup"><span data-stu-id="e7842-284">If no unit specifier is given in a length value, the implementation must assume emu.</span></span>

<span data-ttu-id="e7842-285">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-285">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="measure"></a><span data-ttu-id="e7842-286">measure</span><span class="sxs-lookup"><span data-stu-id="e7842-286">measure</span></span>


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="e7842-287">Una medida es una cantidad que puede ser una [longitud](#length) o una [fracción](#fraction).</span><span class="sxs-lookup"><span data-stu-id="e7842-287">A measure is a quantity that may be either a [length](#length) or a [fraction](#fraction).</span></span> <span data-ttu-id="e7842-288">Esto es muy parecido a las medidas de longitud de HTML y CSS, que pueden ser, en muchos casos, medidas físicas o porcentajes de otra cantidad.</span><span class="sxs-lookup"><span data-stu-id="e7842-288">This closely resembles the HTML and CSS length measurements, which can, in many cases, either be physical measurements or percentages of some other quantity.</span></span> <span data-ttu-id="e7842-289">Si no se especifica ningún especificador de unidad, se debe suponer que el valor es una fracción decimal (por lo tanto, este comportamiento se hereda de fracción, no de longitud).</span><span class="sxs-lookup"><span data-stu-id="e7842-289">If no unit specifier is given, the value must be assumed to be a decimal fraction (thus, this behavior is inherited from fraction, not from length.)</span></span>

<span data-ttu-id="e7842-290">A diferencia de la longitud, un valor de píxel tiene un significado definido por el contexto, por lo que la conversión a la UME normalmente no es apropiada.</span><span class="sxs-lookup"><span data-stu-id="e7842-290">Unlike length, a pixel value has a context-defined meaning, so conversion to emu is normally inappropriate.</span></span> <span data-ttu-id="e7842-291">Hay tres representaciones fundamentales posibles que debe mantener la implementación (es decir, una representación no se puede convertir en otra sin pérdida de información).</span><span class="sxs-lookup"><span data-stu-id="e7842-291">There are three possible fundamental representations that the implementation must maintain (i.e., one representation cannot be converted into another without loss of information).</span></span>

1.  <span data-ttu-id="e7842-292">Un valor fraccionario debe mantenerse en el formato de [fracción](#fraction) (un valor "f").</span><span class="sxs-lookup"><span data-stu-id="e7842-292">A fractional value should be maintained in the [fraction](#fraction) format (an " f " value).</span></span>
2.  <span data-ttu-id="e7842-293">Una longitud física debe mantenerse en la UEM.</span><span class="sxs-lookup"><span data-stu-id="e7842-293">A physical length should be maintained in EMU.</span></span>
3.  <span data-ttu-id="e7842-294">Un valor de píxel debe mantenerse como un número entero de píxeles.</span><span class="sxs-lookup"><span data-stu-id="e7842-294">A pixel value should be maintained as a whole number of pixels.</span></span>

<span data-ttu-id="e7842-295">No se permiten números fraccionarios de píxeles.</span><span class="sxs-lookup"><span data-stu-id="e7842-295">Fractional numbers of pixels are not permitted.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="e7842-296">Representaciones alternativas</span><span class="sxs-lookup"><span data-stu-id="e7842-296">Alternative representations</span></span>

<span data-ttu-id="e7842-297">Se permiten todas las representaciones alternativas de la [fracción](#fraction) y la [longitud](#length) .</span><span class="sxs-lookup"><span data-stu-id="e7842-297">All the alternate representations of both [fraction](#fraction) and [length](#length) are permitted.</span></span>

<span data-ttu-id="e7842-298">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-298">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="angle"></a><span data-ttu-id="e7842-299">angle</span><span class="sxs-lookup"><span data-stu-id="e7842-299">angle</span></span>


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="e7842-300">La representación fundamental de un ángulo es un número de grados múltiplos por 2 6 (65536) y se almacena como un entero.</span><span class="sxs-lookup"><span data-stu-id="e7842-300">The fundamental representation of an angle is a number of degrees multipled by 2 6 (65536) and stored as an integer.</span></span> <span data-ttu-id="e7842-301">Dado que el espacio de coordenadas se invierte (el eje y positivo está inactivo), un ángulo en el sentido de las agujas del reloj es positivo.</span><span class="sxs-lookup"><span data-stu-id="e7842-301">Because the coordinate space is inverted (positive y axis is down), a clockwise angle is positive.</span></span> <span data-ttu-id="e7842-302">Se requiere una implementación compatible para conservar la precisión completa de este tipo de valor.</span><span class="sxs-lookup"><span data-stu-id="e7842-302">A conforming implementation is required to preserve the full precision of such a value.</span></span>

<span data-ttu-id="e7842-303">Se permite que una implementación use cualquier intervalo para ángulos y se le permite normalise un ángulo (por ejemplo, de-180 a + 180 o 0 a 360).</span><span class="sxs-lookup"><span data-stu-id="e7842-303">An implementation is permitted to use any range for angles and is permitted to normalise an angle (for example to -180  to +180  or 0 to 360 ).</span></span> <span data-ttu-id="e7842-304">No es necesario que las implementaciones sean coherentes. sin embargo, la representación entera de un ángulo no debe superar el intervalo de un entero con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e7842-304">Implementations are not required to be consistent; however, the integral representation of an angle must not exceed the range of a 32-bit signed integer.</span></span>

<span data-ttu-id="e7842-305">El sufijo FD se usa para identificar esta representación de un ángulo (grado fraccionario).</span><span class="sxs-lookup"><span data-stu-id="e7842-305">The suffix fd is used to identify this representation of an angle (fractional degree).</span></span> <span data-ttu-id="e7842-306">Observe que esto se distingue del sufijo f para una fracción sin dimensiones, aunque se puede usar una aritmética idéntica para admitirlo.</span><span class="sxs-lookup"><span data-stu-id="e7842-306">Notice that this is distinguished from the f suffix for a dimensionless fraction although identical arithmetic can be used to support it.</span></span> <span data-ttu-id="e7842-307">El valor predeterminado para un valor de angular es simple degrees, es decir, un valor sin escala.</span><span class="sxs-lookup"><span data-stu-id="e7842-307">The default for an angular value is simple degrees, i.e., an unscaled value.</span></span> <span data-ttu-id="e7842-308">Esto también puede señalizarse con el sufijo "" (el símbolo de grado); sin embargo, el uso de esto depende de tener una codificación de documento adecuada; por lo tanto, el regrado del sufijo también se define como la media de grados.</span><span class="sxs-lookup"><span data-stu-id="e7842-308">This may also be signalled with the suffix " " (the degree symbol); however, use of this depends on having a suitable document encoding -- consequently, the suffix deg is also defined to mean degrees.</span></span> <span data-ttu-id="e7842-309">El conjunto completo de posibles sufijos es como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="e7842-309">The full set of possible suffices are as follows.</span></span>



| <span data-ttu-id="e7842-310">Sufijo</span><span class="sxs-lookup"><span data-stu-id="e7842-310">Suffix</span></span>       | <span data-ttu-id="e7842-311">Factor de conversión</span><span class="sxs-lookup"><span data-stu-id="e7842-311">Conversion Factor</span></span> | <span data-ttu-id="e7842-312">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7842-312">Comments</span></span>                               |
|--------------|-------------------|----------------------------------------|
| <span data-ttu-id="e7842-313">FD</span><span class="sxs-lookup"><span data-stu-id="e7842-313">fd</span></span>           | <span data-ttu-id="e7842-314">1</span><span class="sxs-lookup"><span data-stu-id="e7842-314">1</span></span>                 | <span data-ttu-id="e7842-315">Representación interna de alta precisión</span><span class="sxs-lookup"><span data-stu-id="e7842-315">High-precision internal representation</span></span> |
| <span data-ttu-id="e7842-316">ninguno, DEG,</span><span class="sxs-lookup"><span data-stu-id="e7842-316">none, deg,</span></span>   | <span data-ttu-id="e7842-317">65536</span><span class="sxs-lookup"><span data-stu-id="e7842-317">65536</span></span>             | <span data-ttu-id="e7842-318">Degrees (Grados)</span><span class="sxs-lookup"><span data-stu-id="e7842-318">Degrees</span></span>                                |
| <span data-ttu-id="e7842-319">rad</span><span class="sxs-lookup"><span data-stu-id="e7842-319">rad</span></span>          | <span data-ttu-id="e7842-320">65536pi/180</span><span class="sxs-lookup"><span data-stu-id="e7842-320">65536pi/180</span></span>       | <span data-ttu-id="e7842-321">Radians</span><span class="sxs-lookup"><span data-stu-id="e7842-321">Radians</span></span>                                |



 

### <a name="alternative-representations"></a><span data-ttu-id="e7842-322">Representaciones alternativas</span><span class="sxs-lookup"><span data-stu-id="e7842-322">Alternative representations</span></span>

<span data-ttu-id="e7842-323">La transformación de escalado tiene discontinuidades en múltiplos impares de 45.</span><span class="sxs-lookup"><span data-stu-id="e7842-323">The scaling transformation has discontinuities at odd multiples of 45 .</span></span> <span data-ttu-id="e7842-324">Por lo tanto, es muy importante para la conversión de cualquier cantidad inexacta que esté bien definida.</span><span class="sxs-lookup"><span data-stu-id="e7842-324">It is, therefore, extremely important for the conversion of any inexact quantity to be well defined.</span></span> <span data-ttu-id="e7842-325">Por esta razón, la aritmética de la conversión se define para redondear hacia menos infinito.</span><span class="sxs-lookup"><span data-stu-id="e7842-325">For this reason, the arithmetic of conversion is defined to round towards minus infinity.</span></span>

<span data-ttu-id="e7842-326">Como esto puede ser difícil o imposible de garantizar en algunas implementaciones, el uso de lo siguiente se define como una característica de nivel 3:</span><span class="sxs-lookup"><span data-stu-id="e7842-326">Because this may be difficult or impossible to guarantee in some implementations, the use of the following is defined to be a level 3 feature:</span></span>

1.  <span data-ttu-id="e7842-327">Cualquier valor de grado fraccionario.</span><span class="sxs-lookup"><span data-stu-id="e7842-327">Any fractional degree value.</span></span>
2.  <span data-ttu-id="e7842-328">Cualquier valor en radianes</span><span class="sxs-lookup"><span data-stu-id="e7842-328">Any radian value</span></span>

<span data-ttu-id="e7842-329">Por lo tanto, los valores calificados FD y valores enteros no calificados, o valores enteros calificados en grados o deben controlarse exactamente mediante una implementación de nivel 0 compatible. otros valores no necesitan.</span><span class="sxs-lookup"><span data-stu-id="e7842-329">Thus, values qualified fd and unqualified integral values, or integral values qualified deg or   must be handled exactly by a conforming level 0 implementation; other values need not.</span></span> <span data-ttu-id="e7842-330">Se recomienda encarecidamente que cualquier implementación controle la conversión de un valor de grado fraccionario a un valor de grado escalado (FD) exactamente.</span><span class="sxs-lookup"><span data-stu-id="e7842-330">It is strongly recommended that any implementation handle the conversion from a fractional degree value to a scaled (fd) degree value exactly.</span></span> <span data-ttu-id="e7842-331">Esto se puede hacer sin compatibilidad de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="e7842-331">This can be done without floating point support.</span></span>

<span data-ttu-id="e7842-332">Los más requisitos de la conversión distinguen FD de f.</span><span class="sxs-lookup"><span data-stu-id="e7842-332">The more exacting requirements for conversion distinguish fd from f.</span></span>

<span data-ttu-id="e7842-333">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-333">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="color"></a><span data-ttu-id="e7842-334">color</span><span class="sxs-lookup"><span data-stu-id="e7842-334">color</span></span>


```HTML
c
<!element c  %color;>
```



<span data-ttu-id="e7842-335">Los colores son una parte esencial de los gráficos modernos del equipo.</span><span class="sxs-lookup"><span data-stu-id="e7842-335">Colors are an essential part of modern computer graphics.</span></span> <span data-ttu-id="e7842-336">La propuesta usa los métodos establecidos para especificar colores fijos.</span><span class="sxs-lookup"><span data-stu-id="e7842-336">The proposal uses the established methods of specifying fixed colors.</span></span> <span data-ttu-id="e7842-337">Sin embargo, los colores de los diagramas rara vez son colores estáticos simples; a menudo se derivan de otros elementos del diagrama.</span><span class="sxs-lookup"><span data-stu-id="e7842-337">However, colors in diagrams are rarely simple static colors; they are often derived from other elements in the diagram.</span></span> <span data-ttu-id="e7842-338">Gran parte de esta información es específica de la aplicación, por lo que esta propuesta proporciona dos mecanismos muy básicos para especificar este comportamiento:</span><span class="sxs-lookup"><span data-stu-id="e7842-338">Much of this information is very application-specific, so this proposal provides two very basic mechanisms to specify such behavior:</span></span>

1.  <span data-ttu-id="e7842-339">Un color puede derivarse de otro color de la misma forma.</span><span class="sxs-lookup"><span data-stu-id="e7842-339">A color may be derived from another color in the same shape.</span></span>
2.  <span data-ttu-id="e7842-340">Se define un pequeño número de operaciones aritméticas para derivar, o modificar, un color.</span><span class="sxs-lookup"><span data-stu-id="e7842-340">A small number of arithmetic operations are defined for deriving, or modifying, a color.</span></span>

<span data-ttu-id="e7842-341">El mecanismo de forma de prototipo lo complementa gracias a que permite definir prototipos a partir de los cuales se pueden heredar los colores.</span><span class="sxs-lookup"><span data-stu-id="e7842-341">The prototype shape mechanism supplements this by allow prototypes to be defined from which colors can be inherited.</span></span>


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



<span data-ttu-id="e7842-342">Un valor de color es un supraconjunto de la [definición de color CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span><span class="sxs-lookup"><span data-stu-id="e7842-342">A color value is a superset of the [CSS1 color definition](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span> <span data-ttu-id="e7842-343">Las extensiones permiten determinar el valor de color RGB de otros colores dentro de la forma o de una combinación de colores general definida mediante CSS1.</span><span class="sxs-lookup"><span data-stu-id="e7842-343">The extensions allow the RGB color value to be determined from other colors within the shape or from an overall color scheme defined using CSS1.</span></span>

<span data-ttu-id="e7842-344">Si el valor de un elemento se define como un color, el *contenido* de un elemento define el valor de color por medio de un token de color único modificado opcionalmente por una operación aritmética en el color RGB correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e7842-344">If the value of an element is defined to be a color, the *content* of an element defines the color value by means of a single color token optionally modified by an arithmetic operation on the corresponding RGB color.</span></span>

<span data-ttu-id="e7842-345">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-345">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-units"></a><span data-ttu-id="e7842-346">Unidades de color</span><span class="sxs-lookup"><span data-stu-id="e7842-346">Color units</span></span>

<span data-ttu-id="e7842-347">El conjunto completo de tokens de color procede de diversos orígenes: HTML, CSS1 y esta propuesta.</span><span class="sxs-lookup"><span data-stu-id="e7842-347">The full set of color tokens come from a variety of sources: HTML, CSS1, and this proposal.</span></span> <span data-ttu-id="e7842-348">Se definen como se indica a continuación mediante la notación de [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) o la notación XPointer definida para la vinculación XML.</span><span class="sxs-lookup"><span data-stu-id="e7842-348">They are defined as follows using notation from [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) or the XPointer notation defined for XML linking.</span></span>

<span data-ttu-id="e7842-349">En las definiciones de XPointer, el origen de ubicación es el elemento que contiene el valor de color y la expresión hace referencia al conjunto de elementos completo de la forma como si cualquier elemento de prototipo base se hubiera combinado con la forma.</span><span class="sxs-lookup"><span data-stu-id="e7842-349">In the XPointer definitions, the location source is the element containing the color value, and the expression refers to the whole element set of the shape as though any base prototype elements had been merged with the shape.</span></span> <span data-ttu-id="e7842-350">Cuando el elemento correspondiente no existe, se utiliza en su lugar el valor predeterminado de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="e7842-350">When the corresponding element does not exist, the default value for that element is used in its place.</span></span>



| <span data-ttu-id="e7842-351">Color</span><span class="sxs-lookup"><span data-stu-id="e7842-351">Color</span></span>            | <span data-ttu-id="e7842-352">Definición</span><span class="sxs-lookup"><span data-stu-id="e7842-352">Definition</span></span>                                                                                                  | <span data-ttu-id="e7842-353">Nivel</span><span class="sxs-lookup"><span data-stu-id="e7842-353">Level</span></span> | <span data-ttu-id="e7842-354">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7842-354">Description</span></span>                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7842-355">name</span><span class="sxs-lookup"><span data-stu-id="e7842-355">name</span></span>             | <span data-ttu-id="e7842-356">Consulte a continuación</span><span class="sxs-lookup"><span data-stu-id="e7842-356">See below</span></span>                                                                                                   | <span data-ttu-id="e7842-357">0</span><span class="sxs-lookup"><span data-stu-id="e7842-357">0</span></span>     | <span data-ttu-id="e7842-358">Nombre del color HTML, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e7842-358">HTML color name, as listed in the table below.</span></span>                                                                                                                            |
| <span data-ttu-id="e7842-359">\#rr'gg'bb'</span><span class="sxs-lookup"><span data-stu-id="e7842-359">\#rr'gg'bb'</span></span>      | <span data-ttu-id="e7842-360">\#rr'gg'bb'</span><span class="sxs-lookup"><span data-stu-id="e7842-360">\#rr'gg'bb'</span></span>                                                                                                 | <span data-ttu-id="e7842-361">0</span><span class="sxs-lookup"><span data-stu-id="e7842-361">0</span></span>     | <span data-ttu-id="e7842-362">Representación de color CSS1/sRGB estándar con valores en el intervalo comprendido entre 0 y 255, que se representan con 2 dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="e7842-362">Standard CSS1/sRGB color representation using values in the range 0..255 represented using 2 hexadecimal digits each.</span></span>                                                     |
| <span data-ttu-id="e7842-363">\#RGB</span><span class="sxs-lookup"><span data-stu-id="e7842-363">\#rgb</span></span>            | <span data-ttu-id="e7842-364">\#RRGGBB</span><span class="sxs-lookup"><span data-stu-id="e7842-364">\#rrggbb</span></span>                                                                                                    | <span data-ttu-id="e7842-365">1</span><span class="sxs-lookup"><span data-stu-id="e7842-365">1</span></span>     | <span data-ttu-id="e7842-366">Formato CSS1 reducido con solo tres dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="e7842-366">Shortened CSS1 form with only three hexadecimal digits.</span></span>                                                                                                                   |
| <span data-ttu-id="e7842-367">RGB (r, g, b)</span><span class="sxs-lookup"><span data-stu-id="e7842-367">rgb(r,g,b)</span></span>       | <span data-ttu-id="e7842-368">\#c i b</span><span class="sxs-lookup"><span data-stu-id="e7842-368">\#(r)(g)(b)</span></span>                                                                                                 | <span data-ttu-id="e7842-369">1</span><span class="sxs-lookup"><span data-stu-id="e7842-369">1</span></span>     | <span data-ttu-id="e7842-370">CSS1 forma RGB; los elementos del valor RGB se convierten tal y como se define en [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span><span class="sxs-lookup"><span data-stu-id="e7842-370">CSS1 rgb form; the elements of the rgb value are converted as defined in [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span>                                      |
| <span data-ttu-id="e7842-371">fill</span><span class="sxs-lookup"><span data-stu-id="e7842-371">fill</span></span>             | <span data-ttu-id="e7842-372">antecesor (1, forma)</span><span class="sxs-lookup"><span data-stu-id="e7842-372">ancestor(1,shape)</span></span><br/> <span data-ttu-id="e7842-373">secundario (1, relleno)</span><span class="sxs-lookup"><span data-stu-id="e7842-373">child(1, fill)</span></span><br/> <span data-ttu-id="e7842-374">secundario (1, color)</span><span class="sxs-lookup"><span data-stu-id="e7842-374">child(1, color)</span></span><br/>                           | <span data-ttu-id="e7842-375">1</span><span class="sxs-lookup"><span data-stu-id="e7842-375">1</span></span>     | <span data-ttu-id="e7842-376">Color de relleno de primer plano de la forma.</span><span class="sxs-lookup"><span data-stu-id="e7842-376">The foreground fill color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="e7842-377">fillBack</span><span class="sxs-lookup"><span data-stu-id="e7842-377">fillBack</span></span>         | <span data-ttu-id="e7842-378">antecesor (1, forma)</span><span class="sxs-lookup"><span data-stu-id="e7842-378">ancestor(1,shape)</span></span><br/> <span data-ttu-id="e7842-379">secundario (1, relleno)</span><span class="sxs-lookup"><span data-stu-id="e7842-379">child(1, fill)</span></span><br/> <span data-ttu-id="e7842-380">secundario (1, atrás)</span><span class="sxs-lookup"><span data-stu-id="e7842-380">child(1, back)</span></span><br/> <span data-ttu-id="e7842-381">secundario (1, color)</span><span class="sxs-lookup"><span data-stu-id="e7842-381">child(1, color)</span></span><br/> | <span data-ttu-id="e7842-382">1</span><span class="sxs-lookup"><span data-stu-id="e7842-382">1</span></span>     | <span data-ttu-id="e7842-383">Color de fondo del relleno de la forma.</span><span class="sxs-lookup"><span data-stu-id="e7842-383">The background color of the shape fill.</span></span>                                                                                                                                   |
| <span data-ttu-id="e7842-384">line</span><span class="sxs-lookup"><span data-stu-id="e7842-384">line</span></span>             | <span data-ttu-id="e7842-385">antecesor (1, forma)</span><span class="sxs-lookup"><span data-stu-id="e7842-385">ancestor(1,shape)</span></span><br/> <span data-ttu-id="e7842-386">secundario (1, línea)</span><span class="sxs-lookup"><span data-stu-id="e7842-386">child(1, line)</span></span><br/> <span data-ttu-id="e7842-387">secundario (1, color)</span><span class="sxs-lookup"><span data-stu-id="e7842-387">child(1, color)</span></span><br/>                           | <span data-ttu-id="e7842-388">1</span><span class="sxs-lookup"><span data-stu-id="e7842-388">1</span></span>     | <span data-ttu-id="e7842-389">Color de la línea de primer plano de la forma.</span><span class="sxs-lookup"><span data-stu-id="e7842-389">The foreground line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="e7842-390">lineBack</span><span class="sxs-lookup"><span data-stu-id="e7842-390">lineBack</span></span>         | <span data-ttu-id="e7842-391">antecesor (1, forma)</span><span class="sxs-lookup"><span data-stu-id="e7842-391">ancestor(1,shape)</span></span><br/> <span data-ttu-id="e7842-392">secundario (1, línea)</span><span class="sxs-lookup"><span data-stu-id="e7842-392">child(1, line)</span></span><br/> <span data-ttu-id="e7842-393">secundario (1, atrás)</span><span class="sxs-lookup"><span data-stu-id="e7842-393">child(1,back)</span></span> <br/> <span data-ttu-id="e7842-394">secundario (1, color)</span><span class="sxs-lookup"><span data-stu-id="e7842-394">child(1, color)</span></span><br/> | <span data-ttu-id="e7842-395">1</span><span class="sxs-lookup"><span data-stu-id="e7842-395">1</span></span>     | <span data-ttu-id="e7842-396">Color de línea de fondo de la forma.</span><span class="sxs-lookup"><span data-stu-id="e7842-396">The background line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="e7842-397">lineOrFill</span><span class="sxs-lookup"><span data-stu-id="e7842-397">lineOrFill</span></span>       | <span data-ttu-id="e7842-398">línea, relleno</span><span class="sxs-lookup"><span data-stu-id="e7842-398">line, fill</span></span>                                                                                                  | <span data-ttu-id="e7842-399">1</span><span class="sxs-lookup"><span data-stu-id="e7842-399">1</span></span>     | <span data-ttu-id="e7842-400">Valor de línea si no se ha predeterminado; de lo contrario, el valor de relleno.</span><span class="sxs-lookup"><span data-stu-id="e7842-400">The line value if not defaulted, otherwise the fill value.</span></span> <span data-ttu-id="e7842-401">Esto devuelve eficazmente el color que está en el borde de la forma.</span><span class="sxs-lookup"><span data-stu-id="e7842-401">This effectively returns the color that is at the edge of the shape.</span></span>                                           |
| <span data-ttu-id="e7842-402">fillThenLine</span><span class="sxs-lookup"><span data-stu-id="e7842-402">fillThenLine</span></span>     | <span data-ttu-id="e7842-403">relleno, línea</span><span class="sxs-lookup"><span data-stu-id="e7842-403">fill, line</span></span>                                                                                                  | <span data-ttu-id="e7842-404">1</span><span class="sxs-lookup"><span data-stu-id="e7842-404">1</span></span>     | <span data-ttu-id="e7842-405">Valor de relleno si no se ha predeterminado, de lo contrario, el valor de línea.</span><span class="sxs-lookup"><span data-stu-id="e7842-405">The fill value if not defaulted, otherwise the line value.</span></span> <span data-ttu-id="e7842-406">Esto devuelve el color de la forma principal (si la forma no está rellena, el resultado será el color de la línea).</span><span class="sxs-lookup"><span data-stu-id="e7842-406">This effectively returns the main shape color (if the shape is unfilled, the result will be the line color).</span></span>   |
| <span data-ttu-id="e7842-407">shadow</span><span class="sxs-lookup"><span data-stu-id="e7842-407">shadow</span></span>           | <span data-ttu-id="e7842-408">antecesor (1, forma)</span><span class="sxs-lookup"><span data-stu-id="e7842-408">ancestor(1,shape)</span></span><br/> <span data-ttu-id="e7842-409">secundario (1, sombra)</span><span class="sxs-lookup"><span data-stu-id="e7842-409">child(1, shadow)</span></span><br/> <span data-ttu-id="e7842-410">secundario (1, color)</span><span class="sxs-lookup"><span data-stu-id="e7842-410">child(1, color)</span></span><br/>                         | <span data-ttu-id="e7842-411">2</span><span class="sxs-lookup"><span data-stu-id="e7842-411">2</span></span>     | <span data-ttu-id="e7842-412">Color de la sombra (esta es una característica de nivel 2).</span><span class="sxs-lookup"><span data-stu-id="e7842-412">The color of the shadow (this is a level 2 feature).</span></span>                                                                                                                      |
| <span data-ttu-id="e7842-413">scheme</span><span class="sxs-lookup"><span data-stu-id="e7842-413">scheme</span></span>           | <span data-ttu-id="e7842-414">Consulte a continuación</span><span class="sxs-lookup"><span data-stu-id="e7842-414">See below</span></span>                                                                                                   | <span data-ttu-id="e7842-415">1</span><span class="sxs-lookup"><span data-stu-id="e7842-415">1</span></span>     | <span data-ttu-id="e7842-416">Un color de esquema del esquema definido para el documento; Vea a continuación.</span><span class="sxs-lookup"><span data-stu-id="e7842-416">A scheme color from the scheme defined for the document; see below.</span></span>                                                                                                       |
| <span data-ttu-id="e7842-417">esquema (*Índice*)</span><span class="sxs-lookup"><span data-stu-id="e7842-417">scheme(*index*)</span></span>  | <span data-ttu-id="e7842-418">Consulte a continuación</span><span class="sxs-lookup"><span data-stu-id="e7842-418">See below</span></span>                                                                                                   | <span data-ttu-id="e7842-419">1</span><span class="sxs-lookup"><span data-stu-id="e7842-419">1</span></span>     | <span data-ttu-id="e7842-420">*Índice* de color de esquema, empezando desde 0; Vea a continuación.</span><span class="sxs-lookup"><span data-stu-id="e7842-420">Scheme color *index*, starting from 0; see below.</span></span>                                                                                                                         |
| <span data-ttu-id="e7842-421">this</span><span class="sxs-lookup"><span data-stu-id="e7842-421">this</span></span>             | <span data-ttu-id="e7842-422">Tácita</span><span class="sxs-lookup"><span data-stu-id="e7842-422">Implied</span></span>                                                                                                     | <span data-ttu-id="e7842-423">2</span><span class="sxs-lookup"><span data-stu-id="e7842-423">2</span></span>     | <span data-ttu-id="e7842-424">La operación (relleno de una ruta de acceso o dibujo) se define de otra forma (por ejemplo, como un mapa de bits) y el color especifica una "modificación" a los colores de la forma implícita.</span><span class="sxs-lookup"><span data-stu-id="e7842-424">The operation (filling a path, or drawing it) is defined in some other way (for example, as a bitmap), and the color specifies a "modification" to the colors so implied.</span></span> |
| <span data-ttu-id="e7842-425">paleta (*Índice*)</span><span class="sxs-lookup"><span data-stu-id="e7842-425">palette(*index*)</span></span> | <span data-ttu-id="e7842-426">Tácita</span><span class="sxs-lookup"><span data-stu-id="e7842-426">Implied</span></span>                                                                                                     | <span data-ttu-id="e7842-427">3</span><span class="sxs-lookup"><span data-stu-id="e7842-427">3</span></span>     | <span data-ttu-id="e7842-428">Se comporta de la misma manera que esto, salvo que se identifica exactamente una entrada en una tabla de colores de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="e7842-428">Behaves in the same way as this, except that exactly one entry in a bitmap color table is identified.</span></span> <span data-ttu-id="e7842-429">Solo se permite cuando se indica explícitamente.</span><span class="sxs-lookup"><span data-stu-id="e7842-429">Permitted only where explicitly stated.</span></span>                             |
| <span data-ttu-id="e7842-430">ninguno</span><span class="sxs-lookup"><span data-stu-id="e7842-430">none</span></span>             | \-                                                                                                          | <span data-ttu-id="e7842-431">2</span><span class="sxs-lookup"><span data-stu-id="e7842-431">2</span></span>     | <span data-ttu-id="e7842-432">Indica la ausencia de un color; se puede utilizar para cancelar una operación de dibujo que utiliza el color.</span><span class="sxs-lookup"><span data-stu-id="e7842-432">Indicates the absence of a color; may be used to cancel a drawing operation that uses the color.</span></span>                                                                          |
| <span data-ttu-id="e7842-433">sistema</span><span class="sxs-lookup"><span data-stu-id="e7842-433">system</span></span>           | <span data-ttu-id="e7842-434">Consulte a continuación</span><span class="sxs-lookup"><span data-stu-id="e7842-434">See below</span></span>                                                                                                   | <span data-ttu-id="e7842-435">3</span><span class="sxs-lookup"><span data-stu-id="e7842-435">3</span></span>     | <span data-ttu-id="e7842-436">Color definido por la interfaz de usuario del sistema.</span><span class="sxs-lookup"><span data-stu-id="e7842-436">A color defined by the system user interface.</span></span>                                                                                                                             |



 

<span data-ttu-id="e7842-437">Este color permite que un valor de color especifique una modificación de un color que se deriva de otra manera. en concreto, se puede especificar una sola operación para todos los colores de un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="e7842-437">The this color allows a color value to specify a modification to a color which is derived in some other way; in particular, a single operation may be specified for all the colors in a bitmap.</span></span> <span data-ttu-id="e7842-438">El color de la paleta (*Índice*) identifica una entrada determinada en un mapa de bits asignado a la paleta.</span><span class="sxs-lookup"><span data-stu-id="e7842-438">The palette(*index*) color identifies a particular entry in a palette-mapped bitmap.</span></span> <span data-ttu-id="e7842-439">El uso de esto solo se define para grabar una entrada de la tabla de colores que se debe considerar transparente en dicho mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="e7842-439">Use of this is only defined for recording a color table entry that should be regarded as transparent in such a bitmap.</span></span>

<span data-ttu-id="e7842-440">La definición de un valor de color no debe hacer referencia a sí mismo, ya sea directa o indirectamente.</span><span class="sxs-lookup"><span data-stu-id="e7842-440">The definition of a color value must not refer to itself, either directly or indirectly.</span></span> <span data-ttu-id="e7842-441">Si se encuentra una definición de este tipo, se recomienda, pero no es necesario, que la implementación trate el valor sin definir como negro.</span><span class="sxs-lookup"><span data-stu-id="e7842-441">If such a definition is encountered, it is recommended, but not required, that the implementation treat the undefined value as black.</span></span>

<span data-ttu-id="e7842-442">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-442">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="html-colors"></a><span data-ttu-id="e7842-443">Colores HTML</span><span class="sxs-lookup"><span data-stu-id="e7842-443">HTML colors</span></span>

<span data-ttu-id="e7842-444">[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) define los siguientes dieciséis nombres de color:</span><span class="sxs-lookup"><span data-stu-id="e7842-444">[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) defines the following sixteen color names:</span></span>



<span data-ttu-id="e7842-445">Nombres de colores y valores sRGB</span><span class="sxs-lookup"><span data-stu-id="e7842-445">Color names and sRGB values</span></span>

![Ejemplo de color negro.](images/black.gif)

<span data-ttu-id="e7842-447">Black = " \# 000000"</span><span class="sxs-lookup"><span data-stu-id="e7842-447">Black = "\#000000"</span></span>

![Ejemplo de color verde.](images/green.gif)

<span data-ttu-id="e7842-449">Verde = " \# 008000"</span><span class="sxs-lookup"><span data-stu-id="e7842-449">Green = "\#008000"</span></span>

![Ejemplo de color Silver.](images/silver.gif)

<span data-ttu-id="e7842-451">Silver = " \# C0C0C0"</span><span class="sxs-lookup"><span data-stu-id="e7842-451">Silver = "\#C0C0C0"</span></span>

![Ejemplo de color Lima.](images/lime.gif)

<span data-ttu-id="e7842-453">Lima = " \# 00FF00"</span><span class="sxs-lookup"><span data-stu-id="e7842-453">Lime = "\#00FF00"</span></span>

![Ejemplo de color gris.](images/gray.gif)

<span data-ttu-id="e7842-455">Gray = " \# 808080"</span><span class="sxs-lookup"><span data-stu-id="e7842-455">Gray = "\#808080"</span></span>

![Ejemplo de color oliva.](images/olive.gif)

<span data-ttu-id="e7842-457">Oliva = " \# 808000"</span><span class="sxs-lookup"><span data-stu-id="e7842-457">Olive = "\#808000"</span></span>

![Ejemplo de color blanco.](images/white.gif)

<span data-ttu-id="e7842-459">Blanco = " \# FFFFFF"</span><span class="sxs-lookup"><span data-stu-id="e7842-459">White = "\#FFFFFF"</span></span>

![Ejemplo de color YWLLOW.](images/yellow.gif)

<span data-ttu-id="e7842-461">Amarillo = " \# FFFF00"</span><span class="sxs-lookup"><span data-stu-id="e7842-461">Yellow = "\#FFFF00"</span></span>

![Ejemplo de color granate.](images/maroon.gif)

<span data-ttu-id="e7842-463">Granate = " \# 800000"</span><span class="sxs-lookup"><span data-stu-id="e7842-463">Maroon = "\#800000"</span></span>

![Ejemplo de color marino.](images/navy.gif)

<span data-ttu-id="e7842-465">Navy = " \# 000080"</span><span class="sxs-lookup"><span data-stu-id="e7842-465">Navy = "\#000080"</span></span>

![Ejemplo de color rojo.](images/red.gif)

<span data-ttu-id="e7842-467">Red = " \# FF0000"</span><span class="sxs-lookup"><span data-stu-id="e7842-467">Red = "\#FF0000"</span></span>

![Ejemplo de color azul.](images/blue.gif)

<span data-ttu-id="e7842-469">Blue = " \# 0000FF"</span><span class="sxs-lookup"><span data-stu-id="e7842-469">Blue = "\#0000FF"</span></span>

![Ejemplo de color púrpura.](images/purple.gif)

<span data-ttu-id="e7842-471">Púrpura = " \# 800080"</span><span class="sxs-lookup"><span data-stu-id="e7842-471">Purple = "\#800080"</span></span>

![Ejemplo de color verde azulado.](images/teal.gif)

<span data-ttu-id="e7842-473">Verde azulado = " \# 008080"</span><span class="sxs-lookup"><span data-stu-id="e7842-473">Teal = "\#008080"</span></span>

![Ejemplo de color Fuchsia.](images/fuchsia.gif)

<span data-ttu-id="e7842-475">Fuchsia = " \# FF00FF"</span><span class="sxs-lookup"><span data-stu-id="e7842-475">Fuchsia = "\#FF00FF"</span></span>

![Ejemplo de color aguamarina.](images/aqua.gif)

<span data-ttu-id="e7842-477">Aguamarina = " \# 00FFFF"</span><span class="sxs-lookup"><span data-stu-id="e7842-477">Aqua = "\#00FFFF"</span></span>



 

<span data-ttu-id="e7842-478">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-478">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="scheme-colors"></a><span data-ttu-id="e7842-479">Colores de esquema</span><span class="sxs-lookup"><span data-stu-id="e7842-479">Scheme colors</span></span>

<span data-ttu-id="e7842-480">Los colores de esquema a los que se hace referencia en el esquema se definen en el nivel de documento mediante la etiqueta meta con un atributo de nombre de "esquema de color del tema".</span><span class="sxs-lookup"><span data-stu-id="e7842-480">The scheme colors referenced by scheme are defined at the document level using the meta tag with a name attribute of "Theme Color Scheme".</span></span>


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



<span data-ttu-id="e7842-481">Esta etiqueta permite definir hasta ocho colores de esquema.</span><span class="sxs-lookup"><span data-stu-id="e7842-481">This tag allows up to eight scheme colors to be defined.</span></span> <span data-ttu-id="e7842-482">De forma predeterminada, los colores no definidos deben ser negros.</span><span class="sxs-lookup"><span data-stu-id="e7842-482">Undefined colors should default to black.</span></span> <span data-ttu-id="e7842-483">Los colores del esquema permiten cambiar la combinación de colores utilizada para un documento completo simplemente modificando el contenido de la combinación de colores del tema.</span><span class="sxs-lookup"><span data-stu-id="e7842-483">The scheme colors allow the color scheme used for a complete document to be changed just by altering the Theme Color Scheme contents.</span></span> <span data-ttu-id="e7842-484">Para asegurarse de que los gráficos importados de distintas aplicaciones de creación hacen un uso coherente de los colores del esquema, se definen las siguientes interpretaciones.</span><span class="sxs-lookup"><span data-stu-id="e7842-484">To ensure that graphics imported from different authoring applications make consistent use of the scheme colors, the following interpretations are defined.</span></span> <span data-ttu-id="e7842-485">El "uso" es una breve descripción del propósito y la columna "Descripción" proporciona detalles adicionales.</span><span class="sxs-lookup"><span data-stu-id="e7842-485">The "usage" is a short description of the purpose, and the "description" column provides additional details.</span></span>



| <span data-ttu-id="e7842-486">Índice</span><span class="sxs-lookup"><span data-stu-id="e7842-486">Index</span></span> | <span data-ttu-id="e7842-487">Nombre</span><span class="sxs-lookup"><span data-stu-id="e7842-487">Name</span></span>              | <span data-ttu-id="e7842-488">Uso</span><span class="sxs-lookup"><span data-stu-id="e7842-488">Usage</span></span>                         | <span data-ttu-id="e7842-489">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7842-489">Description</span></span>                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7842-490">0</span><span class="sxs-lookup"><span data-stu-id="e7842-490">0</span></span>     | <span data-ttu-id="e7842-491">esquema. Background</span><span class="sxs-lookup"><span data-stu-id="e7842-491">scheme.background</span></span> | <span data-ttu-id="e7842-492">Información previa</span><span class="sxs-lookup"><span data-stu-id="e7842-492">Background</span></span>                    | <span data-ttu-id="e7842-493">Color utilizado para el fondo de un gráfico (y, con frecuencia, para toda la página).</span><span class="sxs-lookup"><span data-stu-id="e7842-493">The color used for the background of a graphic (and, frequently, for the whole page).</span></span>                                    |
| <span data-ttu-id="e7842-494">1</span><span class="sxs-lookup"><span data-stu-id="e7842-494">1</span></span>     | <span data-ttu-id="e7842-495">Scheme. Text</span><span class="sxs-lookup"><span data-stu-id="e7842-495">scheme.text</span></span>       | <span data-ttu-id="e7842-496">Texto y líneas</span><span class="sxs-lookup"><span data-stu-id="e7842-496">Text and lines</span></span>                | <span data-ttu-id="e7842-497">Color del texto adjunto a una forma y el color de línea estándar.</span><span class="sxs-lookup"><span data-stu-id="e7842-497">The color for text attached to a shape and the standard line color.</span></span>                                                      |
| <span data-ttu-id="e7842-498">2</span><span class="sxs-lookup"><span data-stu-id="e7842-498">2</span></span>     | <span data-ttu-id="e7842-499">Scheme. Shadow</span><span class="sxs-lookup"><span data-stu-id="e7842-499">scheme.shadow</span></span>     | <span data-ttu-id="e7842-500">Shadows</span><span class="sxs-lookup"><span data-stu-id="e7842-500">Shadows</span></span>                       | <span data-ttu-id="e7842-501">Color de sombra estándar: el color que se usa normalmente para las sombras de formas.</span><span class="sxs-lookup"><span data-stu-id="e7842-501">Standard shadow color -- the color typically used for shape shadows.</span></span>                                                     |
| <span data-ttu-id="e7842-502">3</span><span class="sxs-lookup"><span data-stu-id="e7842-502">3</span></span>     | <span data-ttu-id="e7842-503">Scheme. title</span><span class="sxs-lookup"><span data-stu-id="e7842-503">scheme.title</span></span>      | <span data-ttu-id="e7842-504">Texto del título</span><span class="sxs-lookup"><span data-stu-id="e7842-504">Title text</span></span>                    | <span data-ttu-id="e7842-505">Color que se va a usar para el título o el texto del título.</span><span class="sxs-lookup"><span data-stu-id="e7842-505">The color to use for heading or title text.</span></span>                                                                              |
| <span data-ttu-id="e7842-506">4</span><span class="sxs-lookup"><span data-stu-id="e7842-506">4</span></span>     | <span data-ttu-id="e7842-507">Scheme. Fill</span><span class="sxs-lookup"><span data-stu-id="e7842-507">scheme.fill</span></span>       | <span data-ttu-id="e7842-508">Rellena</span><span class="sxs-lookup"><span data-stu-id="e7842-508">Fills</span></span>                         | <span data-ttu-id="e7842-509">Color de relleno estándar: el color que se suele usar para rellenar formas.</span><span class="sxs-lookup"><span data-stu-id="e7842-509">Standard fill color -- the color typically used to fill shapes.</span></span>                                                          |
| <span data-ttu-id="e7842-510">5</span><span class="sxs-lookup"><span data-stu-id="e7842-510">5</span></span>     | <span data-ttu-id="e7842-511">Scheme. acento</span><span class="sxs-lookup"><span data-stu-id="e7842-511">scheme.accent</span></span>     | <span data-ttu-id="e7842-512">Destacado</span><span class="sxs-lookup"><span data-stu-id="e7842-512">Accent</span></span>                        | <span data-ttu-id="e7842-513">Color normal "resaltado" que se usa para enfatizar un elemento importante de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="e7842-513">Normal "highlight" color used to emphasis an important element of a graphic.</span></span>                                             |
| <span data-ttu-id="e7842-514">6</span><span class="sxs-lookup"><span data-stu-id="e7842-514">6</span></span>     | <span data-ttu-id="e7842-515">Scheme. HyperLink</span><span class="sxs-lookup"><span data-stu-id="e7842-515">scheme.hyperlink</span></span>  | <span data-ttu-id="e7842-516">Acento e hipervínculo</span><span class="sxs-lookup"><span data-stu-id="e7842-516">Accent and hyperlink</span></span>          | <span data-ttu-id="e7842-517">Color de resaltado utilizado para los hipervínculos.</span><span class="sxs-lookup"><span data-stu-id="e7842-517">Highlight color used for hyperlinks.</span></span> <span data-ttu-id="e7842-518">Se puede usar para otros fines en los que el color denota un vínculo a otra información.</span><span class="sxs-lookup"><span data-stu-id="e7842-518">May be used for other purposes where the color denotes a link to other information.</span></span> |
| <span data-ttu-id="e7842-519">7</span><span class="sxs-lookup"><span data-stu-id="e7842-519">7</span></span>     | <span data-ttu-id="e7842-520">esquema. seguido</span><span class="sxs-lookup"><span data-stu-id="e7842-520">scheme.followed</span></span>   | <span data-ttu-id="e7842-521">Hipervínculo de acento y seguido</span><span class="sxs-lookup"><span data-stu-id="e7842-521">Accent and followed hyperlink</span></span> | <span data-ttu-id="e7842-522">Color de resaltado para los hipervínculos seguidos; también es adecuado para los vínculos "hacia atrás".</span><span class="sxs-lookup"><span data-stu-id="e7842-522">Highlight color for followed hyperlinks; also appropriate for "backwards" links.</span></span>                                         |



 

<span data-ttu-id="e7842-523">Se puede hacer referencia a un color de esquema por nombre o por índice, por lo que Scheme. Fill y Scheme (4) tienen el mismo color.</span><span class="sxs-lookup"><span data-stu-id="e7842-523">A scheme color may be referred to either by name or by index, thus scheme.fill and scheme(4) are the same color.</span></span>

<span data-ttu-id="e7842-524">Los colores del esquema no participan en el esquema de valores predeterminados si no se especifica ningún color.</span><span class="sxs-lookup"><span data-stu-id="e7842-524">Scheme colors do not participate in the defaulting scheme if a color is not specified.</span></span> <span data-ttu-id="e7842-525">Un color de relleno no especificado siempre debe interpretarse como blanco, independientemente del color del esquema color 4.</span><span class="sxs-lookup"><span data-stu-id="e7842-525">An unspecified fill color must always be interpreted as white, regardless of the color of scheme color 4.</span></span> <span data-ttu-id="e7842-526">Los colores de "acento" deben contrastar con los colores de fondo (0) y relleno (4), y los colores de texto y título deben tener la misma propiedad.</span><span class="sxs-lookup"><span data-stu-id="e7842-526">The "accent" colors should contrast with both the background (0) and the fill (4) colors, and text and title text colors should have the same property.</span></span> <span data-ttu-id="e7842-527">Una técnica estándar es hacer que los acentos estén coloreados y el texto estándar no esté coloreado (normalmente, blanco o negro).</span><span class="sxs-lookup"><span data-stu-id="e7842-527">One standard technique is to make the accents colored and the standard text uncolored (typically black or white).</span></span>

<span data-ttu-id="e7842-528">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-528">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="system-colors"></a><span data-ttu-id="e7842-529">Colores del sistema</span><span class="sxs-lookup"><span data-stu-id="e7842-529">System colors</span></span>

<span data-ttu-id="e7842-530">A veces, las aplicaciones registran colores en función de la configuración del sistema operativo dentro de los gráficos.</span><span class="sxs-lookup"><span data-stu-id="e7842-530">Applications sometimes record colors based on operating system settings within graphics.</span></span> <span data-ttu-id="e7842-531">Normalmente, son transitorios y no es necesario escribirlos. las definiciones de thesystemcolor existen únicamente para admitir esto.</span><span class="sxs-lookup"><span data-stu-id="e7842-531">Normally these are transient and need not be written out; thesystemcolor definitions exist solely to support this.</span></span> <span data-ttu-id="e7842-532">Un color del sistema se introduce definiendo una etiqueta adecuada en un nuevo espacio de nombres e insertando la información adecuada en el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="e7842-532">A system color is introduced by defining an appropriate tag in a new namespace and inserting the appropriate information in the element content.</span></span>

<span data-ttu-id="e7842-533">Esta propuesta define esta etiqueta para codificar los colores de la interfaz de usuario de Windows definidos en el archivo de encabezado Winuser. h.</span><span class="sxs-lookup"><span data-stu-id="e7842-533">This proposal defines such a tag to encode the Windows user interface colors defined in the winuser.h header file.</span></span>


```HTML
win.color
<!element win.color #pcdata>
```



<span data-ttu-id="e7842-534">El contenido del elemento es un entero único que contiene el valor de la definición de COLOR correspondiente \_ de Winuser. h.</span><span class="sxs-lookup"><span data-stu-id="e7842-534">The content of the element is a single integer which contains the value of the relevant COLOR\_ define from winuser.h.</span></span> <span data-ttu-id="e7842-535">Se puede adoptar una técnica similar para cualquier especificación de color específica del sistema o de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e7842-535">A similar technique can be adopted for any system- or application-specific color specification.</span></span> <span data-ttu-id="e7842-536">Se recomienda encarecidamente que esta característica se use solo para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="e7842-536">It is strongly recommended that this feature be used only for backward compatibility.</span></span>

<span data-ttu-id="e7842-537">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-537">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="pure-colors"></a><span data-ttu-id="e7842-538">Colores puros</span><span class="sxs-lookup"><span data-stu-id="e7842-538">Pure colors</span></span>


```HTML
pure
<!elementpure empty>
```



<span data-ttu-id="e7842-539">Si el elemento <pure/> aparece en un valor de color, es una sugerencia que indica que el color no debe aproximarse mediante un patrón de interpolación.</span><span class="sxs-lookup"><span data-stu-id="e7842-539">If the element <pure/> appears in a color value, it is a hint that the color should not be approximated by a dither pattern.</span></span> <span data-ttu-id="e7842-540">Se trata de una característica de nivel 1, y no es necesario que una implementación compatible lo respete.</span><span class="sxs-lookup"><span data-stu-id="e7842-540">This is a level 1 feature, and a conforming implementation need not honor it.</span></span> <span data-ttu-id="e7842-541">La designación es importante para los gráficos que se muestran en los dispositivos de resolución media, como las pantallas de vídeo, donde las características pequeñas (como las líneas) pueden producir un alias incorrecto con colores propuestos.</span><span class="sxs-lookup"><span data-stu-id="e7842-541">The designation is important for graphics displayed on medium-resolution devices, such as video displays, where small features (such as lines) may cause bad aliasing with dithered colors.</span></span> <span data-ttu-id="e7842-542">En dispositivos como las impresoras, que normalmente traman todos los colores excepto los colores totalmente saturados, el tramado suele ser suficientemente adecuado para evitar este problema.</span><span class="sxs-lookup"><span data-stu-id="e7842-542">On devices such as printers, which normally dither all colors except for the few fully saturated colors, the dithering is normally sufficiently fine to avoid this problem.</span></span>

<span data-ttu-id="e7842-543">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-543">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-adjustments"></a><span data-ttu-id="e7842-544">Ajustes de color</span><span class="sxs-lookup"><span data-stu-id="e7842-544">Color adjustments</span></span>

<span data-ttu-id="e7842-545">El color base se puede ajustar mediante operaciones aritméticas en el valor RGB.</span><span class="sxs-lookup"><span data-stu-id="e7842-545">The base color may be adjusted by arithmetic operations on the RGB value.</span></span> <span data-ttu-id="e7842-546">Estas operaciones se definen mediante elementos adicionales dentro del valor de color.</span><span class="sxs-lookup"><span data-stu-id="e7842-546">These operations are defined using additional elements within the color value.</span></span> <span data-ttu-id="e7842-547">Estos ajustes solo son útiles cuando se aplican a los colores derivados de otros elementos.</span><span class="sxs-lookup"><span data-stu-id="e7842-547">Such adjustments are useful only when applied to colors derived from other elements.</span></span> <span data-ttu-id="e7842-548">Es válido especificar un ajuste de este tipo en un valor de color fijo. sin embargo, se permite a una implementación reducir esto al valor RGB correspondiente y almacenarlo en lugar del original.</span><span class="sxs-lookup"><span data-stu-id="e7842-548">It is valid to specify such an adjustment on a fixed color value; however, an implementation is permitted to reduce this to the corresponding RGB value and store that instead of the original.</span></span>

<span data-ttu-id="e7842-549">Todas las características de ajuste de color descritas en esta sección son características de nivel 1.</span><span class="sxs-lookup"><span data-stu-id="e7842-549">All the color adjustment features described in this section are level 1 features.</span></span>


```HTML
color.adjustment
<!entity % color.adjustment  -- change to make to a color --
  "( %color.op; )?, ( %color.adj; )*"
>

color.op
<!entity % color.op          -- arithmetic operation --
  "( darken | lighten | add | subtract | reverseSubtract |
  blackWhite )"
>
<!element   darken           %color.parameter;>
<!element   lighten          %color.parameter;>
<!element   add              %color.parameter;>
<!element   subtract         %color.parameter;>
<!element   reversesubtract  %color.parameter;>
<!element   blackwhite       %color.parameter;>

color.parameter
<!entity % color.parameter  "#pcdata" >

color.adj
<!entity % color.adj          -- additional adjustment to color --
  "invert | invert128 | gray"
>
<!element   invert       empty>
<!element   INVERT128    empty>
<!element   gray         empty>
```



<span data-ttu-id="e7842-550">El parámetro de las seis primeras operaciones es un valor numérico entero único en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="e7842-550">The parameter of the first six operations is a single integral numeric value in the range 0 to 255.</span></span> <span data-ttu-id="e7842-551">El ajuste se realiza en el valor RGB de 3x8bit como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="e7842-551">The adjustment is performed on the 3x8bit RGB value as follows:</span></span>

1.  <span data-ttu-id="e7842-552">Si <gray/> se especifica, el valor RGB se sustituye por yyy, donde y es el valor de luminancia (y ') calculado a partir del valor sRGB en el siguiente ITU-r BT. 709.</span><span class="sxs-lookup"><span data-stu-id="e7842-552">If <gray/> is specified, the RGB value is replaced by yyy, where y is the luminance (y') value calculated from the sRGB value in following the ITU-r BT.709.</span></span> <span data-ttu-id="e7842-553">Este cálculo es:</span><span class="sxs-lookup"><span data-stu-id="e7842-553">This calculation is:</span></span>
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  <span data-ttu-id="e7842-554">Si se especifica una modificación de color. op, cada componente se ajusta por separado según la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e7842-554">If a color.op modification is given, each component is separately adjusted according to the table below.</span></span> <span data-ttu-id="e7842-555">c es el valor del componente y p es el valor de color. parámetro.</span><span class="sxs-lookup"><span data-stu-id="e7842-555">c is the component value, and p is the color.parameter value.</span></span>

    | <span data-ttu-id="e7842-556">Operación</span><span class="sxs-lookup"><span data-stu-id="e7842-556">Operation</span></span>       | <span data-ttu-id="e7842-557">Fórmula</span><span class="sxs-lookup"><span data-stu-id="e7842-557">Formula</span></span>                            |
    |-----------------|------------------------------------|
    | <span data-ttu-id="e7842-558">oscuro</span><span class="sxs-lookup"><span data-stu-id="e7842-558">darken</span></span>          | <span data-ttu-id="e7842-559">c: = CXP/255</span><span class="sxs-lookup"><span data-stu-id="e7842-559">c := cxp/255</span></span>                       |
    | <span data-ttu-id="e7842-560">aclarar</span><span class="sxs-lookup"><span data-stu-id="e7842-560">lighten</span></span>         | <span data-ttu-id="e7842-561">c: = 255-(255-c) XP/255</span><span class="sxs-lookup"><span data-stu-id="e7842-561">c := 255 - (255-c)xp/255</span></span>           |
    | <span data-ttu-id="e7842-562">add</span><span class="sxs-lookup"><span data-stu-id="e7842-562">add</span></span>             | <span data-ttu-id="e7842-563">c: = c + p</span><span class="sxs-lookup"><span data-stu-id="e7842-563">c := c + p</span></span>                         |
    | <span data-ttu-id="e7842-564">restar</span><span class="sxs-lookup"><span data-stu-id="e7842-564">subtract</span></span>        | <span data-ttu-id="e7842-565">c: = c-p</span><span class="sxs-lookup"><span data-stu-id="e7842-565">c := c - p</span></span>                         |
    | <span data-ttu-id="e7842-566">reversesubtract</span><span class="sxs-lookup"><span data-stu-id="e7842-566">reversesubtract</span></span> | <span data-ttu-id="e7842-567">c: = p-c</span><span class="sxs-lookup"><span data-stu-id="e7842-567">c := p - c</span></span>                         |
    | <span data-ttu-id="e7842-568">blackwhite</span><span class="sxs-lookup"><span data-stu-id="e7842-568">blackwhite</span></span>      | <span data-ttu-id="e7842-569">Si c < p thenc: = 0elsec: = 255</span><span class="sxs-lookup"><span data-stu-id="e7842-569">if c < p thenc := 0elsec := 255</span></span> |

    

     

    <span data-ttu-id="e7842-570">En cada caso, si el valor del componente calculado, c, supera 255, se usa 255 y si es menor que 0, se utiliza 0.</span><span class="sxs-lookup"><span data-stu-id="e7842-570">In each case, if the calculated component value, c, exceeds 255, then 255 is used, and if it is less than 0, then 0 is used.</span></span>

3.  <span data-ttu-id="e7842-571">Si <INVERT128/> se especifica, el valor 128 se resta o se agrega a cada componente de acuerdo con si el componente es menor que 128 o no.</span><span class="sxs-lookup"><span data-stu-id="e7842-571">If <INVERT128/> is given, the value 128 is subtracted or added to each component according to whether the component is less than 128 or not.</span></span>
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  <span data-ttu-id="e7842-572">Si <invert/> se especifica, cada componente se reemplaza por 255 menos el valor del componente.</span><span class="sxs-lookup"><span data-stu-id="e7842-572">If <invert/> is given, each component is replaced by 255 minus the value of the component.</span></span>
    ```HTML
    c := 255-c
    ```

    

<span data-ttu-id="e7842-573">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-573">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="font"></a><span data-ttu-id="e7842-574">fuente</span><span class="sxs-lookup"><span data-stu-id="e7842-574">font</span></span>


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



<span data-ttu-id="e7842-575">Una fuente se identifica mediante un atributo de estilo, tal como se define en la [sección 5,2 de CSS1 (propiedades de fuente)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) .</span><span class="sxs-lookup"><span data-stu-id="e7842-575">A font is identified using a style attribute as defined in [CSS1 section 5.2 (font properties)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) .</span></span> <span data-ttu-id="e7842-576">El cuerpo del elemento Font es, en la actualidad, undefined, pero se puede usar en el futuro para codificar la información de fuente estándar.</span><span class="sxs-lookup"><span data-stu-id="e7842-576">The body of the font element is, at present, undefined but may be used in the future to encode standard font information.</span></span> <span data-ttu-id="e7842-577">Las implementaciones iniciales de esta propuesta deben conservar pero no interpretar la información.</span><span class="sxs-lookup"><span data-stu-id="e7842-577">Initial implementations of this proposal should preserve but not interpret the information.</span></span>

<span data-ttu-id="e7842-578">Es posible que se agregue compatibilidad en el futuro para obtener información de fuentes fuera de línea (fuentes descargables o recursos compartidos de fuentes).</span><span class="sxs-lookup"><span data-stu-id="e7842-578">It is conceivable that support will be added in the future for out-of-line font information (downloadable fonts, or shared font resources).</span></span> <span data-ttu-id="e7842-579">Esto se realizará mediante un elemento de vínculo XML dentro del contenido del elemento de fuente, asegurándose de que Compatbility hacia atrás con implementaciones iniciales.</span><span class="sxs-lookup"><span data-stu-id="e7842-579">This will be done by an XML-link element within the content of the font element, ensuring backward compatbility with initial implementations.</span></span>

<span data-ttu-id="e7842-580">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-580">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="bitmap"></a><span data-ttu-id="e7842-581">bitmap</span><span class="sxs-lookup"><span data-stu-id="e7842-581">bitmap</span></span>


```HTML
bitmap
<!element   bitmap   empty>
<!attlist   bitmap
   XML-link    cdata               #fixed "simple"
   href        cdata               #REQUIRED
   title       cdata               #implied
   behavior    cdata               #implied
   show        (embed|replace|new) #fixed "embed"
   inline      (true|false)        #fixed "true"
   actuate     (auto|user)         #fixed "auto"
>
```



<span data-ttu-id="e7842-582">El elemento Bitmap permite incluir en un gráfico una referencia a un recurso de imagen fuera de línea (normalmente un mapa de bits).</span><span class="sxs-lookup"><span data-stu-id="e7842-582">The bitmap element allows a reference to an out-of-line picture resource (normally a bitmap) to be included in a graphic.</span></span>

<span data-ttu-id="e7842-583">el mapa de bits es una característica de nivel 1.</span><span class="sxs-lookup"><span data-stu-id="e7842-583">bitmap is a level 1 feature.</span></span>

<span data-ttu-id="e7842-584">El atributo Behavior se puede usar para indicar cómo debe controlar el mapa de bits una aplicación de edición.</span><span class="sxs-lookup"><span data-stu-id="e7842-584">The behavior attribute may be used to indicate how the bitmap should be handled by an editing application.</span></span> <span data-ttu-id="e7842-585">El valor puede ser uno de los tokens siguientes o ambos.</span><span class="sxs-lookup"><span data-stu-id="e7842-585">The value may be one or both of the following tokens.</span></span>



| <span data-ttu-id="e7842-586">Token</span><span class="sxs-lookup"><span data-stu-id="e7842-586">Token</span></span>    | <span data-ttu-id="e7842-587">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7842-587">Description</span></span>                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7842-588">Separe</span><span class="sxs-lookup"><span data-stu-id="e7842-588">separate</span></span> | <span data-ttu-id="e7842-589">Marca el mapa de bits como una entidad independiente, que no se debe considerar como parte integral del documento.</span><span class="sxs-lookup"><span data-stu-id="e7842-589">Marks the bitmap as a separate entity, which should not be regarded as an integral part of the document.</span></span> <span data-ttu-id="e7842-590">El mapa de bits no debe mantenerse con el documento.</span><span class="sxs-lookup"><span data-stu-id="e7842-590">The bitmap should not be kept with the document.</span></span> <span data-ttu-id="e7842-591">Si se copia el documento, no se debe copiar el mapa de bits; Si se mueve el documento, el mapa de bits no debe moverse con él.</span><span class="sxs-lookup"><span data-stu-id="e7842-591">If the document is copied, the bitmap should not be copied; if the document is moved, the bitmap should not be moved with it.</span></span> |
| <span data-ttu-id="e7842-592">original</span><span class="sxs-lookup"><span data-stu-id="e7842-592">original</span></span> | <span data-ttu-id="e7842-593">El atributo title identifica la ubicación original del mapa de bits como una dirección URL. de lo contrario, no se especifica el significado de title.</span><span class="sxs-lookup"><span data-stu-id="e7842-593">The title attribute identifies the original location of the bitmap as a URL; otherwise, the meaning of title is not specified.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="e7842-594">Estos valores son sugerencias para el comportamiento esperado.</span><span class="sxs-lookup"><span data-stu-id="e7842-594">These values are both hints as to the expected behavior.</span></span> <span data-ttu-id="e7842-595">La opción independiente hace referencia al comportamiento de los datos a los que hace referencia href.</span><span class="sxs-lookup"><span data-stu-id="e7842-595">The separate option refers to the behavior of the data referred to by href.</span></span> <span data-ttu-id="e7842-596">Si se proporcionan tanto independiente como original, se espera que la aplicación ignore el URI de href y que se vuelva a generar el mapa de bits a partir de los datos originales.</span><span class="sxs-lookup"><span data-stu-id="e7842-596">If both separate and original are given, the application is expected to disregard the href URI and regenerate the bitmap from the original data.</span></span> <span data-ttu-id="e7842-597">Si solo se proporciona el original, se espera que la aplicación use el URI de href para buscar el mapa de bits, pero puede proporcionar al usuario la opción de volver a generarlo.</span><span class="sxs-lookup"><span data-stu-id="e7842-597">If only original is given, the application is expected to use the href URI to find the bitmap but may give the user the option of regenerating it.</span></span>

<span data-ttu-id="e7842-598">Es válido para que el URI de href y el atributo de título tengan el mismo valor (léxico) (es adecuado si el mapa de bits al que se hace referencia no está "almacenado con" el documento).</span><span class="sxs-lookup"><span data-stu-id="e7842-598">It is valid to make the href URI and the title attribute the same (lexical) value -- this is appropriate if the referenced bitmap is not "stored with" the document.</span></span> <span data-ttu-id="e7842-599">Está previsto (aunque no es necesario) que se use href para la propia copia del documento del mapa de bits, que puede eliminarse si se eliminan las formas de referencia, y ese título se usa para indicar una copia compartida.</span><span class="sxs-lookup"><span data-stu-id="e7842-599">It is intended (though not required) that href be used for the document's own copy of the bitmap -- which may be deleted if the referencing shapes are deleted -- and that title be used to indicate a shared copy.</span></span> <span data-ttu-id="e7842-600">Por lo tanto, si ambos contienen el mismo valor, no hay ninguna copia específica del documento.</span><span class="sxs-lookup"><span data-stu-id="e7842-600">Thus, if both contain the same value there is no document-specific copy.</span></span>

<span data-ttu-id="e7842-601">Las aplicaciones pueden pasar por alto la sugerencia si no caben en el modelo de almacenamiento real de los datos XML.</span><span class="sxs-lookup"><span data-stu-id="e7842-601">Applications may disregard the hint if it does not fit in with the actual storage model of the XML data.</span></span>

<span data-ttu-id="e7842-602">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-602">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="picture-file-formats"></a><span data-ttu-id="e7842-603">Formatos de archivo de imagen</span><span class="sxs-lookup"><span data-stu-id="e7842-603">Picture file formats</span></span>

<span data-ttu-id="e7842-604">En el contexto de esta propuesta, los datos externos son invariablemente un mapa de bits o un archivo que se usa para generar un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="e7842-604">Within the context of this proposal, external data is invariably either a bitmap or a file which is used to produce a bitmap.</span></span> <span data-ttu-id="e7842-605">En el nivel de representación 0, no es necesario admitir ningún formato de mapa de bits externo: las rutas de acceso solo se pueden rellenar con colores sólidos.</span><span class="sxs-lookup"><span data-stu-id="e7842-605">At render level 0, no external bitmap format need be supported -- paths may only be filled with solid colors.</span></span> <span data-ttu-id="e7842-606">Para representar el conjunto completo de rellenos de nivel de representación 1, deben admitirse los mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="e7842-606">To render the full set of render level 1 fills, bitmaps need to be supported.</span></span> <span data-ttu-id="e7842-607">El nivel de representación 1 incluye (solo) los formatos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e7842-607">Render level 1 includes (only) the following formats:</span></span>

1.  <span data-ttu-id="e7842-608">JFIF, es decir, los datos de formato ISO/IEC 10918 incrustados dentro de un archivo con el encabezado JFIF (que se puede considerar como un marcador APP0 determinado después del creador de SOI) e incluye (solo) el intervalo de formatos JPEG admitidos por el código IJG V6.</span><span class="sxs-lookup"><span data-stu-id="e7842-608">JFIF, i.e. ISO/IEC 10918 format data embedded within a file with the JFIF header (which may be regarded as a particular APP0 marker after the SOI maker) and including (only) the range of JPEG formats supported by the IJG v6 code.</span></span>
2.  <span data-ttu-id="e7842-609">PNG, tal como se define en la especificación de la versión 1,0 de PNG.</span><span class="sxs-lookup"><span data-stu-id="e7842-609">PNG, as defined by the PNG version 1.0 specification.</span></span>

<span data-ttu-id="e7842-610">El nivel de representación 2 también incluye compatibilidad para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e7842-610">Render level 2 also includes support for the following:</span></span>

-   <span data-ttu-id="e7842-611">GIF, tal como se define en la especificación de GIF publicada por CompuServ en 1987 (normalmente denominada "GIF87a").</span><span class="sxs-lookup"><span data-stu-id="e7842-611">GIF, as defined by the GIF specification published by CompuServ in 1987 (normally referred to as "GIF87a").</span></span> <span data-ttu-id="e7842-612">GIF89a también se debe admitir en este nivel, sujeto a la restricción de que los datos no deben contener ningún bloque de extensión que necesiten interpretación para mostrar el mapa de bits que no sea el requisito de extensionswithouta de control de gráficos para la entrada del usuario o un tiempo de retraso.</span><span class="sxs-lookup"><span data-stu-id="e7842-612">GIF89a must also be supported at this level, subject to the restriction that the data must not contain any extension blocks that need interpretation to display the bitmap other than graphics control extensionswithouta requirement for user input or a delay time.</span></span> <span data-ttu-id="e7842-613">Esto permite incluir comentarios, pero no la extensión de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="e7842-613">This allows comments to be included, but not the plain text extension.</span></span> <span data-ttu-id="e7842-614">Una aplicación puede insertar extensiones de aplicación (0x21, 0xFF) pero, con la terminología de esta propuesta, estas deben contener solo datos de edición, no de representación.</span><span class="sxs-lookup"><span data-stu-id="e7842-614">An application may insert application (0x21, 0xFF) extensions but, using the terminology of this proposal, these must contain only editing, not rendering, data.</span></span>

<span data-ttu-id="e7842-615">Cualquier otro formato de datos utilizado en el gráfico obliga a que el gráfico tenga al menos el nivel de edición 3 y, posiblemente, el nivel 3 de representación (si los datos son necesarios para representar el gráfico).</span><span class="sxs-lookup"><span data-stu-id="e7842-615">Any other data format used in the graphic forces that graphic to be at least editing level 3 and possibly rendering level 3 (if the data is necessary to render the graphic).</span></span> <span data-ttu-id="e7842-616">Se recomienda que una aplicación publique los formatos que admite.</span><span class="sxs-lookup"><span data-stu-id="e7842-616">An application is encouraged to publish the formats which it supports.</span></span> <span data-ttu-id="e7842-617">Por ejemplo, Microsoft Office admite los siguientes formatos adicionales de forma nativa y, por tanto, puede escribir datos de edición en este formato:</span><span class="sxs-lookup"><span data-stu-id="e7842-617">For example, Microsoft Office supports the following additional formats natively and may therefore write editing data in this form:</span></span>

1.  <span data-ttu-id="e7842-618">WMF--metarchivo de Windows (formato Win 3,1)</span><span class="sxs-lookup"><span data-stu-id="e7842-618">WMF -- Windows metafile (Win 3.1 format)</span></span>
2.  <span data-ttu-id="e7842-619">EMF: metarchivo mejorado de Windows (formato Win32)</span><span class="sxs-lookup"><span data-stu-id="e7842-619">EMF -- Windows "enhanced" metafile (Win32 format)</span></span>
3.  <span data-ttu-id="e7842-620">PICT--Mac OS archivo PICT de QuickDraw (todas las versiones, pero sin registros de QuickTime ni otras extensiones)</span><span class="sxs-lookup"><span data-stu-id="e7842-620">PICT -- Mac OS QuickDraw PICT file (all versions but with no QuickTime records or other extensions)</span></span>
4.  <span data-ttu-id="e7842-621">BMP: formato de archivo de mapa de bits de Windows, "OS/2" (BITMAPCORE), BITMAPINFO (, BITMAPV4 y BITMAPV5</span><span class="sxs-lookup"><span data-stu-id="e7842-621">BMP -- Windows bitmap file format, "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4, and BITMAPV5 formats</span></span>

<span data-ttu-id="e7842-622">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="e7842-622">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vector"></a><span data-ttu-id="e7842-623">vector</span><span class="sxs-lookup"><span data-stu-id="e7842-623">vector</span></span>


```HTML
v
<!element v "( #pcdata | p )*">
```



<span data-ttu-id="e7842-624">Una ruta de acceso de gráfico vectorial se codifica como Pcdata.</span><span class="sxs-lookup"><span data-stu-id="e7842-624">A vector graphic path is encoded as pcdata.</span></span> <span data-ttu-id="e7842-625">El contenido del elemento v es mixto, que contiene una descripción de la ruta de acceso del vector opcionalmente parametrizada con p Elements.</span><span class="sxs-lookup"><span data-stu-id="e7842-625">The content of the v element is mixed, containing a vector path description optionally parameterized with p elements.</span></span>

[<span data-ttu-id="e7842-626">Volver a la información general de VML</span><span class="sxs-lookup"><span data-stu-id="e7842-626">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

