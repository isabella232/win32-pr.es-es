---
title: Introducción a DirectWrite
description: Las personas se comunican con texto todo el tiempo en sus vidas diarias.
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite, acerca de
- DirectWrite, características tipográficas
- tipografía
- DirectWrite, texto internacional
- Fuentes de DirectWrite, OpenType
- Fuentes OpenType
- DirectWrite, ClearType
- ClearType
- DirectWrite, información general sobre API
- DirectWrite, IDWriteFontFace
- IDWriteFontFace
- DirectWrite, representación de texto
- DirectWrite, modos de representación
- DirectWrite, interoperación GDI
- DirectWrite, interoperabilidad
- interoperabilidad, DirectWrite
- interoperabilidad, Interfaz de dispositivo gráfico (GDI)
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904797"
---
# <a name="introducing-directwrite"></a><span data-ttu-id="c9cbe-122">Introducción a DirectWrite</span><span class="sxs-lookup"><span data-stu-id="c9cbe-122">Introducing DirectWrite</span></span>

<span data-ttu-id="c9cbe-123">Las personas se comunican con texto todo el tiempo en sus vidas diarias.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-123">People communicate with text all the time in their daily lives.</span></span> <span data-ttu-id="c9cbe-124">Es la forma principal de que los usuarios consuman un volumen de información cada vez mayor.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-124">It is the primary way for people to consume an increasing volume of information.</span></span> <span data-ttu-id="c9cbe-125">En el pasado, solía usarse el contenido impreso, principalmente documentos, periódicos, libros, etc.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-125">In the past, it used to be through printed content, primarily documents, newspapers, books, and so on.</span></span> <span data-ttu-id="c9cbe-126">Cada vez es un contenido en línea en su equipo Windows.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-126">Increasingly, it is online content on their Windows PC.</span></span> <span data-ttu-id="c9cbe-127">Un usuario de Windows típico emplea mucho tiempo en leer la pantalla del equipo.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-127">A typical Windows user spends a lot of time reading from their computer screen.</span></span> <span data-ttu-id="c9cbe-128">Es posible que estén explorando la web, examinando el correo electrónico, redactando un informe, rellenando una hoja de cálculo o escribiendo software, pero lo que realmente está haciendo es leer.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-128">They might be surfing the Web, scanning e-mail, composing a report, filling in a spreadsheet, or writing software, but what they're really doing is reading.</span></span> <span data-ttu-id="c9cbe-129">Aunque el texto y las fuentes conforman casi todas las partes de la experiencia del usuario en Windows, para la mayoría de los usuarios, la lectura en la pantalla no es tan agradable como leer la salida impresa.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-129">Even though text and fonts permeate nearly every part of the user experience in Windows, for most users, reading on the screen is not as enjoyable as reading printed output.</span></span>

<span data-ttu-id="c9cbe-130">En el caso de los desarrolladores de aplicaciones de Windows, la escritura de código de control de texto es un desafío debido a los mayores requisitos para mejorar la legibilidad, el sofisticado formato y el control de diseño, y la compatibilidad con los distintos idiomas que debe mostrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-130">For Windows application developers, writing text-handling code is a challenge because of the increased requirements for better readability, sophisticated formatting and layout control, and support for the multiple languages the application must display.</span></span> <span data-ttu-id="c9cbe-131">Incluso el sistema de control de texto más básico debe permitir la entrada de texto, el diseño, la visualización, la edición y la copia y el pegado.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-131">Even the most basic text-handling system must allow for text input, layout, display, editing, and copying and pasting.</span></span> <span data-ttu-id="c9cbe-132">Normalmente, los usuarios de Windows esperan más de estas características básicas, por lo que requieren editores sencillos para admitir varias fuentes, varios estilos de párrafo, imágenes incrustadas, revisión ortográfica y otras características.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-132">Windows users commonly expect even more than these basic features, requiring even simple editors to support multiple fonts, various paragraph styles, embedded images, spell checking, and other features.</span></span> <span data-ttu-id="c9cbe-133">El diseño de interfaz de usuario moderno también ya no se limita al formato único, texto sin formato, pero debe presentar una mejor experiencia con fuentes enriquecidas y diseños de texto.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-133">Modern UI design is also no longer confined to single format, plain text, but needs to present a better experience with rich fonts and text layouts.</span></span>

<span data-ttu-id="c9cbe-134">Se trata de una introducción a cómo [DirectWrite](direct-write-portal.md) permite a las aplicaciones Windows mejorar la experiencia de texto para la interfaz de usuario y los documentos.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-134">This is an introduction to how [DirectWrite](direct-write-portal.md) enables Windows applications to enhance the text experience for UI and documents.</span></span>

## <a name="improving-the-text-experience"></a><span data-ttu-id="c9cbe-135">Mejorar la experiencia de texto</span><span class="sxs-lookup"><span data-stu-id="c9cbe-135">Improving the Text Experience</span></span>

<span data-ttu-id="c9cbe-136">Las aplicaciones modernas de Windows tienen requisitos sofisticados para el texto en la interfaz de usuario y los documentos.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-136">Modern Windows applications have sophisticated requirements for text in their UI and documents.</span></span> <span data-ttu-id="c9cbe-137">Esto incluye una mejor legibilidad, compatibilidad con una gran variedad de lenguajes y scripts, y un rendimiento de representación superior.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-137">These include better readability, support for a large variety of languages and scripts, and superior rendering performance.</span></span> <span data-ttu-id="c9cbe-138">Además, la mayoría de las aplicaciones existentes requieren una forma de llevar a cabo inversiones existentes en la base de código WindowsWin32.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-138">In addition, most existing applications require a way to carry forward existing investments in the WindowsWin32 code base.</span></span>

<span data-ttu-id="c9cbe-139">[DirectWrite](direct-write-portal.md) proporciona las tres características siguientes que permiten a los desarrolladores de aplicaciones Windows mejorar la experiencia de texto dentro de sus aplicaciones: independencia del sistema de representación, tipografía de alta calidad y varios niveles de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-139">[DirectWrite](direct-write-portal.md) provides the following three features that enable Windows application developers to improve the text experience within their applications: independence from the rendering system, high-quality typography, and multiple layers of functionality.</span></span>

## <a name="rendering-system-independence"></a><span data-ttu-id="c9cbe-140">Independencia Rendering-System</span><span class="sxs-lookup"><span data-stu-id="c9cbe-140">Rendering-System Independence</span></span>

<span data-ttu-id="c9cbe-141">[DirectWrite](direct-write-portal.md) es independiente de cualquier tecnología de gráficos determinada.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-141">[DirectWrite](direct-write-portal.md) is independent of any particular graphics technology.</span></span> <span data-ttu-id="c9cbe-142">Las aplicaciones pueden usar la tecnología de representación que mejor se adapte a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-142">Applications are free to use the rendering technology best suited to their needs.</span></span> <span data-ttu-id="c9cbe-143">Esto proporciona a las aplicaciones la flexibilidad de seguir representando algunas partes de su aplicación a través de GDI y otras partes a través de Direct3D o [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="c9cbe-143">This gives applications the flexibility to continue rendering some parts of their application through GDI and other parts through Direct3D or [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="c9cbe-144">De hecho, una aplicación podría optar por representar DirectWrite a través de una pila de representación de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-144">In fact, an application could choose to render DirectWrite through a proprietary rendering stack.</span></span>

## <a name="high-quality-typography"></a><span data-ttu-id="c9cbe-145">Tipografía de High-Quality</span><span class="sxs-lookup"><span data-stu-id="c9cbe-145">High-Quality Typography</span></span>

<span data-ttu-id="c9cbe-146">[DirectWrite](direct-write-portal.md) aprovecha los avances de la tecnología de fuentes [OpenType](../intl/opentype-font-format.md) para habilitar la tipografía de alta calidad en una aplicación Windows.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-146">[DirectWrite](direct-write-portal.md) takes advantage of the advances in [OpenType](../intl/opentype-font-format.md) Font technology to enable high quality typography within a Windows application.</span></span> <span data-ttu-id="c9cbe-147">El sistema de fuentes DirectWrite proporciona servicios para trabajar con la enumeración de fuentes, la reserva de fuentes y el almacenamiento en caché de fuentes, que son necesarios para las aplicaciones de control de fuentes.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-147">The DirectWrite font system provides services for dealing with font enumeration, font fallback, and font caching, which are all needed by applications for handling fonts.</span></span>

<span data-ttu-id="c9cbe-148">La compatibilidad con [OpenType](../intl/opentype-font-format.md) proporcionada por [DirectWrite](direct-write-portal.md) permite a los desarrolladores agregar a sus aplicaciones características tipográficas avanzadas y compatibilidad con texto internacional.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-148">The [OpenType](../intl/opentype-font-format.md) support provided by [DirectWrite](direct-write-portal.md) enables developers to add to their applications advanced typographic features and support for international text.</span></span>

## <a name="support-for-advanced-typographic-features"></a><span data-ttu-id="c9cbe-149">Compatibilidad con características tipográficas avanzadas</span><span class="sxs-lookup"><span data-stu-id="c9cbe-149">Support for Advanced Typographic Features</span></span>

<span data-ttu-id="c9cbe-150">[DirectWrite](direct-write-portal.md) permite a los desarrolladores de aplicaciones desbloquear las características de las fuentes OpenType que no se pueden usar en WINFORMS o GDI.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-150">[DirectWrite](direct-write-portal.md) enables application developers to unlock the features of OpenType fonts that they couldn't use in WinForms or GDI.</span></span> <span data-ttu-id="c9cbe-151">El objeto [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) de DirectWrite expone muchas de las características avanzadas de las fuentes OpenType, como alternativas estilísticas y caracteres floreados.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-151">The DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) object exposes many of the advanced features of OpenType fonts, such as stylistic alternates and swashes.</span></span> <span data-ttu-id="c9cbe-152">El kit de desarrollo de software (SDK) de Microsoft Windows proporciona un conjunto de fuentes [OpenType](../intl/opentype-font-format.md) de ejemplo diseñadas con características enriquecidas, como las fuentes Pericles y pescadero.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-152">The Microsoft Windows Software Development Kit (SDK) provides a set of sample [OpenType](../intl/opentype-font-format.md) fonts that are designed with rich features, such as the Pericles and Pescadero fonts.</span></span> <span data-ttu-id="c9cbe-153">Para obtener más información sobre las características de OpenType, consulte [características de fuentes OpenType](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c9cbe-153">For more details on OpenType features, see [OpenType Font Features](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span></span>

## <a name="support-for-international-text"></a><span data-ttu-id="c9cbe-154">Compatibilidad con texto internacional</span><span class="sxs-lookup"><span data-stu-id="c9cbe-154">Support for International Text</span></span>

<span data-ttu-id="c9cbe-155">[DirectWrite](direct-write-portal.md) usa fuentes [OpenType](../intl/opentype-font-format.md) para permitir una amplia compatibilidad con texto internacional.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-155">[DirectWrite](direct-write-portal.md) uses [OpenType](../intl/opentype-font-format.md) fonts to enable broad support for international text.</span></span> <span data-ttu-id="c9cbe-156">Se admiten características Unicode como suplentes, BIDI, salto de línea y UVS.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-156">Unicode features such as surrogates, BIDI, line breaking, and UVS are supported.</span></span> <span data-ttu-id="c9cbe-157">La función de los scripts guiados por el lenguaje, la sustitución de números y la forma de glifos garantizan que el texto de cualquier script tenga el diseño y la representación correctos.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-157">Language-guided script itemization, number substitution, and glyph shaping ensure that text in any script has the correct layout and rendering.</span></span>

<span data-ttu-id="c9cbe-158">Actualmente se admiten los siguientes scripts:</span><span class="sxs-lookup"><span data-stu-id="c9cbe-158">The following scripts are currently supported:</span></span>

> [!Note]  
> <span data-ttu-id="c9cbe-159">En el caso de los scripts marcados con, no hay \* fuentes del sistema predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-159">For scripts marked with an \*, there are no default system fonts.</span></span> <span data-ttu-id="c9cbe-160">Las aplicaciones deben instalar las fuentes que admiten estos scripts.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-160">Applications must install fonts that support these scripts.</span></span>

 

-   <span data-ttu-id="c9cbe-161">Árabe</span><span class="sxs-lookup"><span data-stu-id="c9cbe-161">Arabic</span></span>
-   <span data-ttu-id="c9cbe-162">Armenio</span><span class="sxs-lookup"><span data-stu-id="c9cbe-162">Armenian</span></span>
-   <span data-ttu-id="c9cbe-163">Bengala</span><span class="sxs-lookup"><span data-stu-id="c9cbe-163">Bengala</span></span>
-   <span data-ttu-id="c9cbe-164">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="c9cbe-164">Bopomofo</span></span>
-   <span data-ttu-id="c9cbe-165">Pantallas\*</span><span class="sxs-lookup"><span data-stu-id="c9cbe-165">Braille\*</span></span>
-   <span data-ttu-id="c9cbe-166">Canadiense indígena silábico</span><span class="sxs-lookup"><span data-stu-id="c9cbe-166">Canadian aboriginal syllabics</span></span>
-   <span data-ttu-id="c9cbe-167">Cheroqui</span><span class="sxs-lookup"><span data-stu-id="c9cbe-167">Cherokee</span></span>
-   <span data-ttu-id="c9cbe-168">Chino (simplificado & tradicional)</span><span class="sxs-lookup"><span data-stu-id="c9cbe-168">Chinese (Simplified & Traditional)</span></span>
-   <span data-ttu-id="c9cbe-169">Cirílico</span><span class="sxs-lookup"><span data-stu-id="c9cbe-169">Cyrillic</span></span>
-   <span data-ttu-id="c9cbe-170">Copto\*</span><span class="sxs-lookup"><span data-stu-id="c9cbe-170">Coptic\*</span></span>
-   <span data-ttu-id="c9cbe-171">Devanagari</span><span class="sxs-lookup"><span data-stu-id="c9cbe-171">Devanagari</span></span>
-   <span data-ttu-id="c9cbe-172">Dígito</span><span class="sxs-lookup"><span data-stu-id="c9cbe-172">Ethiopic</span></span>
-   <span data-ttu-id="c9cbe-173">Georgiano</span><span class="sxs-lookup"><span data-stu-id="c9cbe-173">Georgian</span></span>
-   <span data-ttu-id="c9cbe-174">Letra\*</span><span class="sxs-lookup"><span data-stu-id="c9cbe-174">Glagolitic\*</span></span>
-   <span data-ttu-id="c9cbe-175">Griego</span><span class="sxs-lookup"><span data-stu-id="c9cbe-175">Greek</span></span>
-   <span data-ttu-id="c9cbe-176">Gujarati</span><span class="sxs-lookup"><span data-stu-id="c9cbe-176">Gujarati</span></span>
-   <span data-ttu-id="c9cbe-177">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="c9cbe-177">Gurmukhi</span></span>
-   <span data-ttu-id="c9cbe-178">Hebreo</span><span class="sxs-lookup"><span data-stu-id="c9cbe-178">Hebrew</span></span>
-   <span data-ttu-id="c9cbe-179">Japonés</span><span class="sxs-lookup"><span data-stu-id="c9cbe-179">Japanese</span></span>
-   <span data-ttu-id="c9cbe-180">Canarés</span><span class="sxs-lookup"><span data-stu-id="c9cbe-180">Kannada</span></span>
-   <span data-ttu-id="c9cbe-181">Jemer</span><span class="sxs-lookup"><span data-stu-id="c9cbe-181">Khmer</span></span>
-   <span data-ttu-id="c9cbe-182">Coreano</span><span class="sxs-lookup"><span data-stu-id="c9cbe-182">Korean</span></span>
-   <span data-ttu-id="c9cbe-183">Lao</span><span class="sxs-lookup"><span data-stu-id="c9cbe-183">Lao</span></span>
-   <span data-ttu-id="c9cbe-184">Latín</span><span class="sxs-lookup"><span data-stu-id="c9cbe-184">Latin</span></span>
-   <span data-ttu-id="c9cbe-185">Malayalam</span><span class="sxs-lookup"><span data-stu-id="c9cbe-185">Malayalam</span></span>
-   <span data-ttu-id="c9cbe-186">Mongol</span><span class="sxs-lookup"><span data-stu-id="c9cbe-186">Mongolian</span></span>
-   <span data-ttu-id="c9cbe-187">Myanmar</span><span class="sxs-lookup"><span data-stu-id="c9cbe-187">Myanmar</span></span>
-   <span data-ttu-id="c9cbe-188">Nuevo tai lue moderno</span><span class="sxs-lookup"><span data-stu-id="c9cbe-188">New Tai Lue</span></span>
-   <span data-ttu-id="c9cbe-189">Ogham\*</span><span class="sxs-lookup"><span data-stu-id="c9cbe-189">Ogham\*</span></span>
-   <span data-ttu-id="c9cbe-190">Odia</span><span class="sxs-lookup"><span data-stu-id="c9cbe-190">Odia</span></span>
-   <span data-ttu-id="c9cbe-191">' Phags-pa</span><span class="sxs-lookup"><span data-stu-id="c9cbe-191">'Phags-pa</span></span>
-   <span data-ttu-id="c9cbe-192">Rúnica\*</span><span class="sxs-lookup"><span data-stu-id="c9cbe-192">Runic\*</span></span>
-   <span data-ttu-id="c9cbe-193">Cingalés</span><span class="sxs-lookup"><span data-stu-id="c9cbe-193">Sinhala</span></span>
-   <span data-ttu-id="c9cbe-194">Siríaco</span><span class="sxs-lookup"><span data-stu-id="c9cbe-194">Syriac</span></span>
-   <span data-ttu-id="c9cbe-195">Tai le</span><span class="sxs-lookup"><span data-stu-id="c9cbe-195">Tai Le</span></span>
-   <span data-ttu-id="c9cbe-196">Tamil</span><span class="sxs-lookup"><span data-stu-id="c9cbe-196">Tamil</span></span>
-   <span data-ttu-id="c9cbe-197">Telugu</span><span class="sxs-lookup"><span data-stu-id="c9cbe-197">Telugu</span></span>
-   <span data-ttu-id="c9cbe-198">Thaana</span><span class="sxs-lookup"><span data-stu-id="c9cbe-198">Thaana</span></span>
-   <span data-ttu-id="c9cbe-199">Tailandés</span><span class="sxs-lookup"><span data-stu-id="c9cbe-199">Thai</span></span>
-   <span data-ttu-id="c9cbe-200">Tibetano</span><span class="sxs-lookup"><span data-stu-id="c9cbe-200">Tibetan</span></span>
-   <span data-ttu-id="c9cbe-201">Yi</span><span class="sxs-lookup"><span data-stu-id="c9cbe-201">Yi</span></span>

## <a name="multiple-layers-of-functionality"></a><span data-ttu-id="c9cbe-202">Varios niveles de funcionalidad</span><span class="sxs-lookup"><span data-stu-id="c9cbe-202">Multiple Layers of Functionality</span></span>

<span data-ttu-id="c9cbe-203">[DirectWrite](direct-write-portal.md) proporciona capas de funcionalidad factorizadas, donde cada capa interactúa sin problemas con el siguiente.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-203">[DirectWrite](direct-write-portal.md) provides factored layers of functionality, with each layer interacting seamlessly with the next.</span></span> <span data-ttu-id="c9cbe-204">El diseño de la API permite a los desarrolladores de aplicaciones tener libertad y flexibilidad para adoptar capas individuales en función de sus necesidades y programación.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-204">The API design gives application developers the freedom and flexibility to adopt individual layers depending on their needs and schedule.</span></span> <span data-ttu-id="c9cbe-205">En el diagrama siguiente se muestra la relación entre estas capas.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-205">The following diagram shows the relationship between these layers.</span></span>

![diagrama de capas de directwrite y cómo se comunican con una aplicación o marco de interfaz de usuario y la API de gráficos](images/intro-01.png)

<span data-ttu-id="c9cbe-207">La API de diseño de texto proporciona la funcionalidad de nivel más alto disponible en [DirectWrite](direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="c9cbe-207">The text layout API provides the highest level functionality available from [DirectWrite](direct-write-portal.md).</span></span> <span data-ttu-id="c9cbe-208">Proporciona servicios para que la aplicación mida, muestre e interactúe con cadenas de texto con formato enriquecido.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-208">It provides services for the application to measure, display, and interact with richly formatted text strings.</span></span> <span data-ttu-id="c9cbe-209">Esta API de texto se puede usar en aplicaciones que actualmente usan Win32 DrawText para compilar una interfaz de usuario moderna con texto con formato enriquecido.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-209">This text API can be used in applications that currently use Win32's DrawText to build a modern UI with richly formatted text.</span></span>

<span data-ttu-id="c9cbe-210">Las aplicaciones con un uso intensivo de texto que implementan su propio motor de diseño pueden usar la siguiente capa hacia abajo: el procesador de scripts.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-210">Text-intensive applications that implement their own layout engine may use the next layer down: the script processor.</span></span> <span data-ttu-id="c9cbe-211">El procesador de scripts divide un fragmento de texto en bloques de scripts y controla la asignación entre representaciones Unicode a la representación de glifo adecuada en la fuente, por lo que el texto del script puede mostrarse correctamente en el idioma correcto.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-211">The script processor breaks down a chunk of text into script blocks and handles the mapping between Unicode representations to the appropriate glyph representation in the font so the text of the script can be correctly displayed in the correct language.</span></span> <span data-ttu-id="c9cbe-212">El sistema de diseño utilizado por el nivel de API de diseño de texto se basa en el sistema de procesamiento de fuentes y scripts.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-212">The layout system used by the text layout API layer is built upon the font and script processing system.</span></span>

<span data-ttu-id="c9cbe-213">La capa de representación de glifos es el nivel más bajo de funcionalidad y proporciona la funcionalidad de representación de glifos para las aplicaciones que implementan su propio motor de diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-213">The glyph-rendering layer is the lowest layer of functionality and provides glyph-rendering functionality for applications that implement their own text layout engine.</span></span> <span data-ttu-id="c9cbe-214">La capa de representación del glifo también es útil para las aplicaciones que implementan un representador personalizado para modificar el comportamiento del dibujo de glifos a través de la función de devolución de llamada en la API de formato de texto de [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c9cbe-214">The glyph rendering layer is also useful for applications that implement a custom renderer to modify the glyph-drawing behavior through the callback function in the [DirectWrite](direct-write-portal.md) text-formatting API.</span></span>

<span data-ttu-id="c9cbe-215">El sistema de fuentes [directwrite](direct-write-portal.md) está disponible para todos los niveles funcionales de directwrite y permite que una aplicación tenga acceso a la información de fuentes y glifos.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-215">The [DirectWrite](direct-write-portal.md) font system is available to all the DirectWrite functional layers and enables an application to access font and glyph information.</span></span> <span data-ttu-id="c9cbe-216">Está diseñado para administrar tecnologías de fuentes y formatos de datos comunes.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-216">It is designed to handle common font technologies and data formats.</span></span> <span data-ttu-id="c9cbe-217">El modelo de fuente DirectWrite sigue la práctica tipográfica común de admitir cualquier número de pesos, estilos y estirados de la misma familia de fuentes.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-217">The DirectWrite font model follows the common typographic practice of supporting any number of weights, styles, and stretches in the same font family.</span></span> <span data-ttu-id="c9cbe-218">Este modelo, el mismo modelo seguido de WPF y CSS, especifica que las fuentes que difieren solo en peso (negrita, luz, etc.), estilo (vertical, cursiva u oblicuo) o Stretch (estrecho, condensado, ancho, etc.) se consideran miembros de una sola familia de fuentes.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-218">This model, the same model followed by WPF and CSS, specifies that fonts differing only in weight (bold, light, and so on), style (upright, italic, or oblique) or stretch (narrow, condensed, wide, and so on) are considered to be members of a single font family.</span></span>

### <a name="improved-text-rendering-with-cleartype"></a><span data-ttu-id="c9cbe-219">Representación de texto mejorada con ClearType</span><span class="sxs-lookup"><span data-stu-id="c9cbe-219">Improved Text Rendering with ClearType</span></span>

<span data-ttu-id="c9cbe-220">Mejorar la legibilidad en la pantalla es un requisito clave para todas las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-220">Improving readability on the screen is a key requirement for all Windows applications.</span></span> <span data-ttu-id="c9cbe-221">La evidencia de Research en la psicología cognitiva indica que es necesario poder reconocer cada letra con precisión y que incluso el espaciado entre las letras es fundamental para el procesamiento rápido.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-221">The evidence from research in cognitive psychology indicates that we need to be able to recognize every letter accurately and that even spacing between letters is critical for fast processing.</span></span> <span data-ttu-id="c9cbe-222">Las letras y palabras que no son simétricas se perciben como feo y degradan la experiencia de lectura.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-222">Letters and words that are not symmetrical are perceived as ugly and degrade the reading experience.</span></span> <span data-ttu-id="c9cbe-223">Kevin Larson, el grupo de tecnologías avanzadas de lectura de Microsoft, escribió un artículo sobre el asunto que se publicó en el espectro IEEE.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-223">Kevin Larson, Microsoft Advanced Reading Technologies group, wrote an article on the subject that was published in Spectrum IEEE.</span></span> <span data-ttu-id="c9cbe-224">El artículo se denomina "tecnología de texto" ( https://www.spectrum.ieee.org/print/5049) .</span><span class="sxs-lookup"><span data-stu-id="c9cbe-224">The article is called "The Technology of Text" (https://www.spectrum.ieee.org/print/5049).</span></span>

<span data-ttu-id="c9cbe-225">El texto en [DirectWrite](direct-write-portal.md) se representa con Microsoft ClearType, lo que mejora la claridad y la legibilidad del texto.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-225">Text in [DirectWrite](direct-write-portal.md) is rendered using Microsoft ClearType, which enhances the clarity and readability of text.</span></span> <span data-ttu-id="c9cbe-226">ClearType aprovecha el hecho de que las pantallas LCD modernas tienen bandas RGB para cada píxel que se pueden controlar individualmente.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-226">ClearType takes advantage of the fact that modern LCD displays have RGB stripes for each pixel that can be controlled individually.</span></span> <span data-ttu-id="c9cbe-227">DirectWrite usa las últimas mejoras de ClearType, que se incluyen primero en Windows Vista con Windows Presentation Foundation, que le permite evaluar no solo las letras individuales, sino también el espaciado entre las letras.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-227">DirectWrite uses the latest enhancements to ClearType, first included with Windows Vista with Windows Presentation Foundation, that enables it to evaluate not just the individual letters but also the spacing between letters.</span></span> <span data-ttu-id="c9cbe-228">Antes de estas mejoras de ClearType, el texto con un tamaño de "lectura" de 10 o 12 puntos era difícil de mostrar: podríamos colocar 1 píxel entre letras, que a menudo era demasiado pequeño o 2 píxeles, lo que a menudo era demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-228">Before these ClearType enhancements, text with a "reading" size of 10 or 12 points was difficult to display: we could place either 1 pixel in between letters, which was often too little, or 2 pixels, which was often too much.</span></span> <span data-ttu-id="c9cbe-229">El uso de la resolución adicional en los subpíxeles nos proporciona el espaciado fraccionario, lo que mejora la simetría y la simetría de toda la página.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-229">Using the extra resolution in the subpixels provides us with fractional spacing, which improves the evenness and symmetry of the entire page.</span></span>

<span data-ttu-id="c9cbe-230">En la ilustración siguiente se muestra cómo los glifos pueden comenzar en cualquier límite de subpíxeles cuando se usa el posicionamiento de subpíxeles.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-230">The following two illustration show how glyphs may begin on any sub-pixel boundary when sub-pixel positioning is used.</span></span>

<span data-ttu-id="c9cbe-231">La siguiente ilustración se representa mediante la versión de GDI del representador ClearType, que no empleaba el posicionamiento de subpíxeles.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-231">The following illustration is rendered using the GDI version of the ClearType renderer, which did not employ sub-pixel positioning.</span></span>

![Ilustración de "tecnología" representada sin posicionamiento de subpíxeles](images/intro-03.png)

<span data-ttu-id="c9cbe-233">La siguiente ilustración se representa mediante la versión de [DirectWrite](direct-write-portal.md) del representador ClearType, que usa el posicionamiento de subpíxeles.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-233">The following illustration is rendered using the [DirectWrite](direct-write-portal.md) version of the ClearType renderer, which uses sub-pixel positioning.</span></span>

![Ilustración de "tecnología" representada con posicionamiento de subpíxeles](images/intro-04.png)

<span data-ttu-id="c9cbe-235">Tenga en cuenta que el espaciado entre las letras h y n es más incluso en la segunda imagen y la letra o se espacia más allá de la letra n, incluso con la letra l.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-235">Note that the spacing between the letters h and n is more even in the second image and the letter o is spaced further from the letter n, more even with the letter l.</span></span> <span data-ttu-id="c9cbe-236">Tenga en cuenta también cómo el tallo de las letras l es más natural.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-236">Also note how the stems on the letters l are more natural looking.</span></span>

<span data-ttu-id="c9cbe-237">La posición de ClearType de subpíxeles ofrece el espaciado más preciso de los caracteres en la pantalla, especialmente en tamaños pequeños en los que la diferencia entre un subpíxel y un píxel entero representa una proporción significativa del ancho del glifo.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-237">The subpixel ClearType positioning offers the most accurate spacing of characters on screen, especially at small sizes where the difference between a sub-pixel and a whole pixel represents a significant proportion of glyph width.</span></span> <span data-ttu-id="c9cbe-238">Permite medir el texto en el espacio de resolución ideal y representarlo en su posición natural en la franja de color LCD, con granularidad de subpíxeles.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-238">It enables text to be measured in ideal resolution space and rendered at its natural position at the LCD color stripe, with subpixel granularity.</span></span> <span data-ttu-id="c9cbe-239">El texto que se mide y se representa mediante esta tecnología es, por definición, independiente de la resolución, lo que significa que se consigue el mismo diseño de texto en el intervalo de varias resoluciones de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-239">Text measured and rendered using this technology is, by definition, resolution-independent, meaning that the exact same layout of text is achieved across the range of various display resolutions.</span></span>

<span data-ttu-id="c9cbe-240">A diferencia de cualquier tipo de representación de GDI de GDI, ClearType de subpíxel ofrece el ancho de caracteres más preciso.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-240">Unlike either type of GDI ClearType rendering, sub-pixel ClearType offers the most accurate width of characters.</span></span>

<span data-ttu-id="c9cbe-241">La API de cadena de texto adopta la representación de texto de subpíxeles de forma predeterminada, lo que significa que mide el texto en su resolución ideal independiente de la resolución de pantalla actual y genera el resultado de posicionamiento del glifo en función de los anchos de avance del glifo realmente escalados y los desplazamientos de posición.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-241">The Text String API adopts sub-pixel text rendering by default, which means it measures text at its ideal resolution independent of the current display resolution, and produces the glyph positioning result based on the truly scaled glyph advance widths and positioning offsets.</span></span>

<span data-ttu-id="c9cbe-242">En el caso de texto de tamaño grande, [DirectWrite](direct-write-portal.md) también habilita el suavizado de contorno a lo largo del eje y para que los bordes sean más suaves y representaciones como el diseñador de fuentes previsto.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-242">For large-sized text, [DirectWrite](direct-write-portal.md) also enables anti-aliasing along the y-axis to make the edges smoother and render letters as the font designer intended.</span></span> <span data-ttu-id="c9cbe-243">En la ilustración siguiente se muestra el suavizado de contorno de la dirección y.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-243">The following illustration shows y-direction anti-aliasing.</span></span>

![Ilustración de "ClearType" representada como texto GDI y como texto de directwrite con suavizado de contorno de la dirección y](images/intro-05.png)

<span data-ttu-id="c9cbe-245">Aunque el texto de [DirectWrite](direct-write-portal.md) se coloca y se representa con ClearType de subpíxeles de forma predeterminada, hay disponibles otras opciones de representación.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-245">Although [DirectWrite](direct-write-portal.md) text is positioned and rendered using sub-pixel ClearType by default, other rendering options are available.</span></span> <span data-ttu-id="c9cbe-246">Muchas aplicaciones existentes usan GDI para representar la mayor parte de su interfaz de usuario y algunas aplicaciones usan controles de edición del sistema que siguen usando GDI para la representación de texto.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-246">Many existing applications use GDI to render most of their UI, and some applications use system editing controls that continue to use GDI for text rendering.</span></span> <span data-ttu-id="c9cbe-247">Al agregar texto de DirectWrite a estas aplicaciones, puede que sea necesario sacrificar las mejoras de la experiencia de lectura proporcionadas por ClearType de subpíxeles para que el texto tenga una apariencia coherente en toda la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-247">When adding DirectWrite text to these applications, it may be necessary to sacrifice the reading experience improvements provided by sub-pixel ClearType so that text has a consistent appearance across the application.</span></span>

<span data-ttu-id="c9cbe-248">Para cumplir estos requisitos, [DirectWrite](direct-write-portal.md) también admite las siguientes opciones de representación:</span><span class="sxs-lookup"><span data-stu-id="c9cbe-248">To meet these requirements, [DirectWrite](direct-write-portal.md) also supports the following rendering options:</span></span>

-   <span data-ttu-id="c9cbe-249">ClearType de subpíxel (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="c9cbe-249">Sub-pixel ClearType (default).</span></span>
-   <span data-ttu-id="c9cbe-250">ClearType de subpíxel con suavizado de contorno en las dimensiones horizontal y vertical.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-250">Sub-pixel ClearType with anti-aliasing in both horizontal and vertical dimensions.</span></span>
-   <span data-ttu-id="c9cbe-251">Texto con alias.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-251">Aliased text.</span></span>
-   <span data-ttu-id="c9cbe-252">El ancho natural de GDI (usado por Microsoft Word Vista de lectura, por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="c9cbe-252">GDI natural-width (used by Microsoft Word Reading View, for example).</span></span>
-   <span data-ttu-id="c9cbe-253">Compatible con GDI: ancho (incluido mapa de bits incrustado de Asia oriental).</span><span class="sxs-lookup"><span data-stu-id="c9cbe-253">GDI compatible-width (including East Asian embedded bitmap).</span></span>

<span data-ttu-id="c9cbe-254">Cada uno de estos modos de representación se puede ajustar a través de la API de DirectWrite y a través del nuevo sintonizador ClearType de bandeja de entrada de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-254">Each of these rendering modes can be fine-tuned through the DirectWrite API and through the new Windows 7 inbox ClearType tuner.</span></span>

> [!Note]  
> <span data-ttu-id="c9cbe-255">A partir de Windows 8, debe usar el suavizado de contorno de texto de la grisización en la mayoría de los casos.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-255">Starting with Windows 8, you should use greyscale text antialiasing in most cases.</span></span> <span data-ttu-id="c9cbe-256">Consulte la siguiente sección para más información.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-256">See the next section for more information.</span></span>

 

### <a name="support-for-natural-layout"></a><span data-ttu-id="c9cbe-257">Compatibilidad con el diseño natural</span><span class="sxs-lookup"><span data-stu-id="c9cbe-257">Support for Natural Layout</span></span>

<span data-ttu-id="c9cbe-258">El diseño natural es independiente de la resolución, por lo que el espaciado de los caracteres no cambia a medida que se acerca o aleja, o en función de los PPP de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-258">Natural layout is resolution-independent, so the spacing of characters doesn't change as you zoom in or out, or depending on the DPI of the display.</span></span> <span data-ttu-id="c9cbe-259">Una ventaja secundaria es que el espaciado es cierto para el diseño de la fuente.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-259">A secondary advantage is that spacing is true to the design of the font.</span></span> <span data-ttu-id="c9cbe-260">El diseño natural es posible gracias a la compatibilidad de DirectWrite con la representación natural, lo que significa que los glifos individuales se pueden colocar en una fracción de un píxel.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-260">Natural layout is made possible by DirectWrite's support for natural rendering, which means individual glyphs can be positioned to a fraction of a pixel.</span></span>

<span data-ttu-id="c9cbe-261">Aunque el diseño natural es el valor predeterminado, algunas aplicaciones necesitan representar texto con el mismo espaciado y apariencia que GDI.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-261">While natural layout is the default, some applications need to render text with the same spacing and appearance as GDI.</span></span> <span data-ttu-id="c9cbe-262">Para estas aplicaciones, DirectWrite proporciona modos de medida natural GDI clásico y GDI y los modos de representación correspondientes.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-262">For such applications, DirectWrite provides GDI classic and GDI natural measuring modes and corresponding rendering modes.</span></span>

<span data-ttu-id="c9cbe-263">Cualquiera de los modos de representación anteriores se puede combinar con cualquiera de los dos modos de suavizado de contorno: ClearType o escala de grises.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-263">Any of the above rendering modes can be combined with either of the two antialiasing modes: ClearType or grayscale.</span></span> <span data-ttu-id="c9cbe-264">El suavizado de contorno de ClearType simula una resolución más alta al manipular individualmente los valores de color rojo, verde y azul de cada píxel.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-264">ClearType antialiasing simulations a higher resolution by individually manipulating the red, green, and blue color values of each pixel.</span></span> <span data-ttu-id="c9cbe-265">El suavizado de escala de grises calcula solo un valor de cobertura (o alfa) para cada píxel.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-265">Grayscale antialiasing computes only one coverage (or alpha) value for each pixel.</span></span> <span data-ttu-id="c9cbe-266">ClearType es el valor predeterminado, pero se recomienda el suavizado de escala de grises para las aplicaciones de la tienda Windows porque es más rápido y es compatible con el suavizado de contorno estándar, mientras que sigue siendo muy legible.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-266">ClearType is the default, but grayscale antialiasing is recommended for Windows Store apps because it is faster and is compatible with standard antialiasing, while still being highly readable.</span></span>

## <a name="api-overview"></a><span data-ttu-id="c9cbe-267">Información general acerca de la API</span><span class="sxs-lookup"><span data-stu-id="c9cbe-267">API Overview</span></span>

<span data-ttu-id="c9cbe-268">La interfaz [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) es el punto de partida para usar la funcionalidad de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-268">The [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface is the starting point for using DirectWrite functionality.</span></span> <span data-ttu-id="c9cbe-269">El generador es el objeto raíz que crea un conjunto de objetos que se pueden usar juntos.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-269">The factory is the root object that creates a set of objects that can be used together.</span></span>

<span data-ttu-id="c9cbe-270">La operación de formato y diseño es un requisito previo para las operaciones, ya que el texto debe tener el formato correcto y estar diseñado para un conjunto especificado de restricciones antes de que se pueda dibujar o probar la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-270">The formatting and layout operation is a prerequisite to the operations, as text needs to be properly formatted and laid out to a specified set of constraints before it can be drawn or hit-tested.</span></span> <span data-ttu-id="c9cbe-271">Dos objetos clave que se pueden crear con un [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) para este propósito son [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) y [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="c9cbe-271">Two key objects that you can create with an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) for this purpose are [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="c9cbe-272">Un objeto **IDWriteTextFormat** representa la información de formato para un párrafo de texto.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-272">An **IDWriteTextFormat** object represents the formatting information for a paragraph of text.</span></span> <span data-ttu-id="c9cbe-273">La función [**IDWriteFactory:: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) toma la cadena de entrada, las restricciones asociadas, como la dimensión del espacio que se va a rellenar y el objeto **IDWriteTextFormat** , y coloca el resultado analizado y con formato completo en **IDWriteTextLayout** para usarlo en operaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-273">The [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) function takes the input string, the associated constraints such as the dimension of the space to be filled, and the **IDWriteTextFormat** object, and puts the fully analyzed and formatted result into **IDWriteTextLayout** to use in subsequent operations.</span></span>

<span data-ttu-id="c9cbe-274">A continuación, la aplicación puede representar el texto mediante la función [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) proporcionada por [Direct2D](../direct2d/direct2d-portal.md) o implementando una función de devolución de llamada que puede usar GDI, Direct2D u otros sistemas de gráficos para representar los glifos.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-274">The application can then render the text using the [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) function provided by [Direct2D](../direct2d/direct2d-portal.md) or by implementing a callback function that can use GDI, Direct2D, or other graphics systems to render the glyphs.</span></span> <span data-ttu-id="c9cbe-275">Para un solo formato de texto, la función [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) en Direct2D proporciona una manera más sencilla de dibujar texto sin tener que crear primero un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="c9cbe-275">For a single format text, the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function on Direct2D provides a simpler way to draw text without having to first create a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a><span data-ttu-id="c9cbe-276">Aplicar formato y dibujar "Hola mundo" con DirectWrite</span><span class="sxs-lookup"><span data-stu-id="c9cbe-276">Formatting and Drawing "Hello World" Using DirectWrite</span></span>

<span data-ttu-id="c9cbe-277">En el ejemplo de código siguiente se muestra cómo una aplicación puede dar formato a un solo párrafo mediante [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) y dibujarlo mediante la función [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) de [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="c9cbe-277">The following code example shows how an application can format a single paragraph using [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and draw it using the [Direct2D](../direct2d/direct2d-portal.md)[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function.</span></span>


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a><span data-ttu-id="c9cbe-278">Acceder al sistema de fuentes</span><span class="sxs-lookup"><span data-stu-id="c9cbe-278">Accessing the Font System</span></span>

<span data-ttu-id="c9cbe-279">Además de especificar un nombre de familia de fuentes para la cadena de texto mediante la interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) en el ejemplo anterior, [DirectWrite](direct-write-portal.md) proporciona a las aplicaciones un mayor control sobre la selección de fuentes a través de la enumeración de fuentes y la capacidad de crear una colección de fuentes personalizada basada en fuentes de documentos incrustadas.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-279">In addition to specifying a font family name for the text string by using the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface in the example above, [DirectWrite](direct-write-portal.md) provides applications more control over font selection through font enumeration and the ability to create custom font collection based on embedded document fonts.</span></span>

<span data-ttu-id="c9cbe-280">El objeto [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) es una colección de familias de fuentes.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-280">The [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) object is a collection of font families.</span></span> <span data-ttu-id="c9cbe-281">DirectWrite proporciona acceso al conjunto de fuentes instaladas en el sistema a través de una colección de fuentes especial denominada colección de fuentes del sistema.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-281">DirectWrite provides access to the set of fonts installed on the system through a special font collection called the system font collection.</span></span> <span data-ttu-id="c9cbe-282">Esto se obtiene llamando al método [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) del objeto [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="c9cbe-282">This is obtained by calling the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) object.</span></span> <span data-ttu-id="c9cbe-283">Una aplicación también puede crear una colección de fuentes personalizada a partir de un conjunto de fuentes enumeradas por una devolución de llamada definida por la aplicación, es decir, fuentes privadas instaladas por una aplicación o fuentes incrustadas en un documento.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-283">An application can also create a custom font collection from a set of fonts enumerated by an application-defined callback, that is, private fonts installed by an application, or fonts embedded in a document.</span></span>

<span data-ttu-id="c9cbe-284">A continuación, la aplicación puede llamar a [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) para obtener un objeto FontFamily específico dentro de la colección y, a continuación, llamar a [**IDWriteFontFamily:: GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) para obtener un objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) específico.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-284">The application can then call [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) to get to a specific FontFamily object within the collection, and then call [**IDWriteFontFamily::GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) to get to a specific [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object.</span></span> <span data-ttu-id="c9cbe-285">El objeto **IDWriteFont** representa una fuente de una colección de fuentes y expone propiedades y algunas métricas de fuente básicas.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-285">The **IDWriteFont** object represents a font in a font collection and exposes properties and a few basic font metrics.</span></span>

<span data-ttu-id="c9cbe-286">[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) es otro objeto que representa una fuente y expone un conjunto completo de métricas en una fuente.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-286">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) is another object that represents a font and exposes a full set of metrics on a font.</span></span> <span data-ttu-id="c9cbe-287">El **IDWriteFontFace** se puede crear directamente a partir de un nombre de fuente; una aplicación no tiene que obtener una colección de fuentes para tener acceso a ella.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-287">The **IDWriteFontFace** can be created directly from a font name; an application does not have to get a font collection to access it.</span></span> <span data-ttu-id="c9cbe-288">Resulta útil para una aplicación de diseño de texto como Microsoft Word que necesita consultar los detalles de una fuente específica.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-288">It is useful for a text layout application such as Microsoft Word that needs to query the details for a specific font.</span></span>

<span data-ttu-id="c9cbe-289">En el diagrama siguiente se ilustra la relación entre estos objetos.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-289">The following diagram illustrates the relationship between these objects.</span></span>

![diagrama de la relación entre una colección de fuentes, una familia de fuentes y una fuente](images/fontcollection.png)

### <a name="idwritefontface"></a><span data-ttu-id="c9cbe-291">IDWriteFontFace</span><span class="sxs-lookup"><span data-stu-id="c9cbe-291">IDWriteFontFace</span></span>

<span data-ttu-id="c9cbe-292">El objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) representa una fuente y proporciona información más detallada sobre la fuente que el objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) .</span><span class="sxs-lookup"><span data-stu-id="c9cbe-292">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object represents a font and provides more detailed information about the font than the [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object does.</span></span> <span data-ttu-id="c9cbe-293">Las métricas de fuente y glifo de **IDWriteFontFace** son útiles para las aplicaciones que implementan el diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-293">The font and glyph metrics from the **IDWriteFontFace** are useful for applications that implement text layout.</span></span>

<span data-ttu-id="c9cbe-294">La mayoría de las aplicaciones principales no usarán estas API directamente y, en su lugar, utilizará [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) o especificará el nombre de la familia de fuentes directamente.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-294">Most mainstream applications will not use these APIs directly, and instead will use [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) or specify the font family name directly.</span></span>

<span data-ttu-id="c9cbe-295">En la tabla siguiente se resumen los escenarios de uso de los dos objetos.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-295">The following table summarizes the usage scenarios for the two objects.</span></span>



| <span data-ttu-id="c9cbe-296">Category</span><span class="sxs-lookup"><span data-stu-id="c9cbe-296">Category</span></span>                                                                                                         | [<span data-ttu-id="c9cbe-297">**IDWriteFont**</span><span class="sxs-lookup"><span data-stu-id="c9cbe-297">**IDWriteFont**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [<span data-ttu-id="c9cbe-298">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="c9cbe-298">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="c9cbe-299">API para admitir la interacción del usuario, como una interfaz de usuario del selector de fuentes: Descripción y otras API informativas</span><span class="sxs-lookup"><span data-stu-id="c9cbe-299">APIs to support user interaction such as a font-chooser user interface: description and other informational APIs</span></span> | <span data-ttu-id="c9cbe-300">Sí</span><span class="sxs-lookup"><span data-stu-id="c9cbe-300">Yes</span></span>                                        | <span data-ttu-id="c9cbe-301">No</span><span class="sxs-lookup"><span data-stu-id="c9cbe-301">No</span></span>                                                 |
| <span data-ttu-id="c9cbe-302">API para admitir la asignación de fuentes: familia, estilo, peso, stretch, cobertura de caracteres</span><span class="sxs-lookup"><span data-stu-id="c9cbe-302">APIs to support font mapping: family, style, weight, stretch, character coverage</span></span>                                 | <span data-ttu-id="c9cbe-303">Sí</span><span class="sxs-lookup"><span data-stu-id="c9cbe-303">Yes</span></span>                                        | <span data-ttu-id="c9cbe-304">No</span><span class="sxs-lookup"><span data-stu-id="c9cbe-304">No</span></span>                                                 |
| <span data-ttu-id="c9cbe-305">DrawText API</span><span class="sxs-lookup"><span data-stu-id="c9cbe-305">DrawText API</span></span>                                                                                                     | <span data-ttu-id="c9cbe-306">Sí</span><span class="sxs-lookup"><span data-stu-id="c9cbe-306">Yes</span></span>                                        | <span data-ttu-id="c9cbe-307">No</span><span class="sxs-lookup"><span data-stu-id="c9cbe-307">No</span></span>                                                 |
| <span data-ttu-id="c9cbe-308">API usadas para la representación</span><span class="sxs-lookup"><span data-stu-id="c9cbe-308">APIs used for rendering</span></span>                                                                                          | <span data-ttu-id="c9cbe-309">No</span><span class="sxs-lookup"><span data-stu-id="c9cbe-309">No</span></span>                                         | <span data-ttu-id="c9cbe-310">Sí</span><span class="sxs-lookup"><span data-stu-id="c9cbe-310">Yes</span></span>                                                |
| <span data-ttu-id="c9cbe-311">API utilizadas para el diseño de texto: métricas del glifo, etc.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-311">APIs used for text layout: glyph metrics, and so on</span></span>                                                              | <span data-ttu-id="c9cbe-312">No</span><span class="sxs-lookup"><span data-stu-id="c9cbe-312">No</span></span>                                         | <span data-ttu-id="c9cbe-313">Sí</span><span class="sxs-lookup"><span data-stu-id="c9cbe-313">Yes</span></span>                                                |
| <span data-ttu-id="c9cbe-314">API para el control de la interfaz de usuario y el diseño de texto: métricas de toda la fuente</span><span class="sxs-lookup"><span data-stu-id="c9cbe-314">APIs for UI control and text layout: font-wide metrics</span></span>                                                           | <span data-ttu-id="c9cbe-315">Sí</span><span class="sxs-lookup"><span data-stu-id="c9cbe-315">Yes</span></span>                                        | <span data-ttu-id="c9cbe-316">Sí</span><span class="sxs-lookup"><span data-stu-id="c9cbe-316">Yes</span></span>                                                |



 

<span data-ttu-id="c9cbe-317">A continuación se muestra una aplicación de ejemplo que enumera las fuentes de la colección de fuentes del sistema.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-317">The following is an example application that enumerates the fonts in the system font collection.</span></span>


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a><span data-ttu-id="c9cbe-318">Representación de texto</span><span class="sxs-lookup"><span data-stu-id="c9cbe-318">Text rendering</span></span>

<span data-ttu-id="c9cbe-319">Las API de representación de texto permiten que los glifos de una fuente [DirectWrite](direct-write-portal.md) se representen en una superficie de [Direct2D](../direct2d/direct2d-portal.md) o en un mapa de bits independiente del dispositivo GDI o que se conviertan en esquemas o mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-319">The text rendering APIs enable glyphs in a [DirectWrite](direct-write-portal.md) font to be rendered to a [Direct2D](../direct2d/direct2d-portal.md) surface or to a GDI device independent bitmap, or to be converted to outlines or bitmaps.</span></span> <span data-ttu-id="c9cbe-320">La representación de ClearType en DirectWrite admite el posicionamiento de subpíxeles con una nitidez y un contraste mejorados en comparación con las implementaciones anteriores en Windows.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-320">The ClearType rendering in DirectWrite supports sub-pixel positioning with improved sharpness and contrast compared to previous implementations on Windows.</span></span> <span data-ttu-id="c9cbe-321">DirectWrite también admite texto en blanco y negro con alias para admitir escenarios en los que intervienen fuentes asiáticas Orientales con mapas de bits incrustados o en los que el usuario ha deshabilitado el suavizado de fuentes de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-321">DirectWrite also supports aliased black-and-white text to support scenarios involving East Asian fonts with embedded bitmaps, or where the user has disabled font smoothing of any type.</span></span>

<span data-ttu-id="c9cbe-322">Todas las opciones son ajustables por todos los botones ClearType disponibles a los que se puede acceder a través de las API de [DirectWrite](direct-write-portal.md) y también se exponen a través del nuevo applet del panel de control de Windows 7 ClearType Tuner.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-322">All the options are adjustable by all the available ClearType knobs accessible through the [DirectWrite](direct-write-portal.md) APIs, and also exposed via the new Windows 7 ClearType tuner control panel applet.</span></span>

<span data-ttu-id="c9cbe-323">Hay dos API disponibles para la representación de glifos, una que proporciona una representación acelerada mediante hardware a través de [Direct2D](../direct2d/direct2d-portal.md) y la otra que proporciona la representación de software a un mapa de bits de GDI.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-323">There are two APIs available for rendering glyphs, one providing hardware-accelerated rendering through [Direct2D](../direct2d/direct2d-portal.md) and the other providing software rendering to a GDI bitmap.</span></span> <span data-ttu-id="c9cbe-324">Una aplicación que usa [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e implementa la devolución de llamada [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) puede llamar a cualquiera de estas funciones como respuesta a una devolución de llamada [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="c9cbe-324">An application using [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) and implementing the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) callback can call either of these functions in response to a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback.</span></span> <span data-ttu-id="c9cbe-325">Además, las aplicaciones que implementan su propio diseño o tratan los datos de nivel de glifo pueden utilizar estas API.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-325">Also, applications that implement their own layout or deal with glyph-level data can use these APIs.</span></span>

1.  [<span data-ttu-id="c9cbe-326">**ID2DRenderTarget::D rawGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="c9cbe-326">**ID2DRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    <span data-ttu-id="c9cbe-327">Las aplicaciones pueden usar la API de [Direct2D](../direct2d/direct2d-portal.md) [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) para proporcionar aceleración de hardware para la representación de texto mediante la GPU.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-327">Applications can use the [Direct2D](../direct2d/direct2d-portal.md) API [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) to provide hardware acceleration for text rendering using the GPU.</span></span> <span data-ttu-id="c9cbe-328">La aceleración de hardware afecta a todas las fases de la canalización de representación de texto: desde combinar glifos en ejecuciones de glifos y filtrar el mapa de bits de ejecución de glifos, para aplicar el algoritmo de mezcla ClearType a la salida mostrada final.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-328">Hardware acceleration affects all phases of the text rendering pipeline—from merging glyphs into glyph runs and filtering the glyph-run bitmap, to applying the ClearType blending algorithm to the final displayed output.</span></span> <span data-ttu-id="c9cbe-329">Esta es la API recomendada para obtener el mejor rendimiento de representación.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-329">This is the recommended API for getting the best rendering performance.</span></span>

2.  [<span data-ttu-id="c9cbe-330">**IDWriteBitmapRenderTarget::D rawGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="c9cbe-330">**IDWriteBitmapRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    <span data-ttu-id="c9cbe-331">Las aplicaciones pueden usar el método [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para realizar una representación de software de una ejecución de glifos en un mapa de bits 32-bpp.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-331">Applications can use the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to perform a software-rendering of a run of glyphs to a 32-bpp bitmap.</span></span> <span data-ttu-id="c9cbe-332">El objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) encapsula un mapa de bits y un contexto de dispositivo de memoria que se puede usar para representar glifos.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-332">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object encapsulates a bitmap and a memory device context that can be used for rendering glyphs.</span></span> <span data-ttu-id="c9cbe-333">Esta API es útil si desea permanecer en GDI porque tiene una base de código existente que se representa en GDI.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-333">This API is useful if you want to stay with GDI because you have an existing code base that renders in GDI.</span></span>

<span data-ttu-id="c9cbe-334">Si tiene una aplicación que tiene código de diseño de texto existente que usa GDI y desea conservar su código de diseño existente, pero usar [DirectWrite](direct-write-portal.md) solo para el paso final de los glifos de representación, [**IDWriteGdiInterop:: CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) proporciona el puente entre las dos API.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-334">If you have an application that has existing text layout code that uses GDI, and you want to preserve its existing layout code but use [DirectWrite](direct-write-portal.md) just for the final step of rendering glyphs, [**IDWriteGdiInterop::CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) provides the bridge between the two APIs.</span></span> <span data-ttu-id="c9cbe-335">Antes de llamar a esta función, la aplicación usará la función **IDWriteGdiInterop:: CreateFontFaceFromHdc** para obtener una referencia de fuente a partir de un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-335">Before calling this function, the application will use the **IDWriteGdiInterop::CreateFontFaceFromHdc** function to get a font-face reference from a device context.</span></span>

> [!Note]  
> <span data-ttu-id="c9cbe-336">En la mayoría de los escenarios, es posible que las aplicaciones no tengan que usar estas API de representación de glifos.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-336">For most scenarios, applications may not need to use these glyph-rendering APIs.</span></span> <span data-ttu-id="c9cbe-337">Después de que una aplicación haya creado un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , puede utilizar el método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) para representar el texto.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-337">After an application has created an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, it can use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method to render the text.</span></span>

 

## <a name="custom-rendering-modes"></a><span data-ttu-id="c9cbe-338">Modos de representación personalizados</span><span class="sxs-lookup"><span data-stu-id="c9cbe-338">Custom Rendering Modes</span></span>

<span data-ttu-id="c9cbe-339">Varios parámetros afectan a la representación de texto, como gamma, nivel de ClearType, geometría de píxeles y contraste mejorado.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-339">A number of parameters affect text rendering, such as gamma, ClearType level, pixel geometry, and enhanced contrast.</span></span> <span data-ttu-id="c9cbe-340">Los parámetros de representación se encapsulan mediante un objeto, que implementa la interfaz [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) pública.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-340">Rendering parameters are encapsulated by an object, which implements the public [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) interface.</span></span> <span data-ttu-id="c9cbe-341">El objeto de parámetros de representación se inicializa automáticamente en función de las propiedades de hardware o las preferencias de usuario especificadas mediante el applet de panel de control ClearType en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-341">The rendering parameters object is automatically initialized based on hardware properties and/or user preferences specified through the ClearType control panel applet in Windows 7.</span></span> <span data-ttu-id="c9cbe-342">Por lo general, si un cliente usa la API de diseño de [directwrite](direct-write-portal.md) , directwrite seleccionará automáticamente un modo de representación que se corresponda con el modo de medición especificado.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-342">Generally, if a client uses the [DirectWrite](direct-write-portal.md) layout API, DirectWrite will automatically select a rendering mode that corresponds to the specified measuring mode.</span></span>

<span data-ttu-id="c9cbe-343">Las aplicaciones que desean más control pueden usar [**IDWriteFactory:: CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) para implementar las distintas opciones de representación.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-343">Applications that want more control can use [**IDWriteFactory::CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) to implement the different rendering options.</span></span> <span data-ttu-id="c9cbe-344">Esta función también se puede usar para establecer la gamma, la geometría de píxeles y el contraste mejorado.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-344">This function can also be used to set the gamma, pixel geometry, and enhanced contrast.</span></span>

<span data-ttu-id="c9cbe-345">A continuación se muestran las diversas opciones de representación disponibles:</span><span class="sxs-lookup"><span data-stu-id="c9cbe-345">The following are the various rendering options available:</span></span>

-   <span data-ttu-id="c9cbe-346">Suavizado de contorno de subpíxeles</span><span class="sxs-lookup"><span data-stu-id="c9cbe-346">Sub-pixel anti-aliasing</span></span>

    <span data-ttu-id="c9cbe-347">La aplicación establece el parámetro *renderingMode* en el \_ modo de representación de DWRITE \_ \_ natural para especificar la representación con suavizado de contorno solo en la dimensión horizontal.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-347">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL to specify rendering with anti-aliasing in the horizontal dimension only.</span></span>

-   <span data-ttu-id="c9cbe-348">Suavizado de contorno de subpíxeles en dimensiones horizontales y verticales.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-348">Sub-pixel anti-aliasing in both horizontal and vertical dimensions.</span></span>

    <span data-ttu-id="c9cbe-349">La aplicación establece el parámetro *renderingMode* en el \_ modo de representación de DWRITE \_ \_ \_ simétrico natural para especificar la representación con suavizado de contorno en las dimensiones horizontal y vertical.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-349">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL\_SYMMETRIC to specify rendering with anti-aliasing in both horizontal and vertical dimensions.</span></span> <span data-ttu-id="c9cbe-350">Esto hace que las curvas y las líneas diagonales parezcan más suaves a costa de cierta suavidad y se suelen usar en tamaños superiores a 16 PPEM.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-350">This makes curves and diagonal lines look smoother at the expense of some softness, and is typically used at sizes above 16 ppem.</span></span>

-   <span data-ttu-id="c9cbe-351">Texto con alias</span><span class="sxs-lookup"><span data-stu-id="c9cbe-351">Aliased Text</span></span>

    <span data-ttu-id="c9cbe-352">La aplicación establece el parámetro *renderingMode* en el \_ modo de representación de DWRITE \_ \_ con alias para especificar el texto con alias.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-352">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_ALIASED to specify aliased text.</span></span>

-   <span data-ttu-id="c9cbe-353">Texto en escala de grises</span><span class="sxs-lookup"><span data-stu-id="c9cbe-353">Grayscale Text</span></span>

    <span data-ttu-id="c9cbe-354">La aplicación establece el parámetro *pixelGeometry* en DWRITE \_ píxeles \_ Geometry \_ Flat para especificar el texto de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-354">The application sets the *pixelGeometry* parameter to DWRITE\_PIXEL\_GEOMETRY\_FLAT to specify grayscale text.</span></span>

-   <span data-ttu-id="c9cbe-355">Compatible con GDI: ancho (incluido mapa de bits incrustado de Asia oriental)</span><span class="sxs-lookup"><span data-stu-id="c9cbe-355">GDI compatible-width (including East Asian embedded bitmap)</span></span>

    <span data-ttu-id="c9cbe-356">La aplicación establece el parámetro *renderingMode* en el \_ modo de representación de DWRITE \_ \_ GDI \_ clásico para especificar el suavizado de contorno de ancho compatible con GDI.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-356">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_CLASSIC to specify GDI compatible-width anti-aliasing.</span></span>

-   <span data-ttu-id="c9cbe-357">Ancho natural de GDI</span><span class="sxs-lookup"><span data-stu-id="c9cbe-357">GDI natural-width</span></span>

    <span data-ttu-id="c9cbe-358">La aplicación establece el parámetro *renderingMode* en el modo de representación de DWRITE de \_ \_ \_ GDI \_ natural para especificar el suavizado de contorno compatible de ancho natural de GDI.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-358">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_NATURAL to specify GDI natural-width compatible anti-aliasing.</span></span>

-   <span data-ttu-id="c9cbe-359">Texto de esquema</span><span class="sxs-lookup"><span data-stu-id="c9cbe-359">Outline text</span></span>

    <span data-ttu-id="c9cbe-360">Para la representación en tamaños grandes, es posible que un desarrollador de aplicaciones prefiera representar con el contorno de fuente en lugar de rasterizarlo en un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-360">For rendering at large sizes, an application developer might prefer to render by using the font outline rather than by rasterizing into a bitmap.</span></span> <span data-ttu-id="c9cbe-361">La aplicación establece el parámetro *renderingMode* en **el \_ esquema del \_ modo \_ de representación DWRITE** para especificar que la representación debe omitir el rasterizador y utilizar los contornos directamente.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-361">The application sets the *renderingMode* parameter to **DWRITE\_RENDERING\_MODE\_OUTLINE** to specify that rendering should bypass the rasterizer and use the outlines directly.</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="c9cbe-362">Interoperabilidad con GDI</span><span class="sxs-lookup"><span data-stu-id="c9cbe-362">GDI Interoperability</span></span>

<span data-ttu-id="c9cbe-363">La interfaz [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) proporciona interoperabilidad con GDI.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-363">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface provides interoperability with GDI.</span></span> <span data-ttu-id="c9cbe-364">Esto permite a las aplicaciones continuar su inversión existente en las bases de código GDI y usar de forma selectiva [DirectWrite](direct-write-portal.md) para la representación o el diseño.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-364">This enables applications to continue their existing investment in GDI code bases and selectively use [DirectWrite](direct-write-portal.md) for either rendering or layout.</span></span>

<span data-ttu-id="c9cbe-365">A continuación se muestran las API que permiten a una aplicación migrar a o desde el sistema de fuentes de GDI:</span><span class="sxs-lookup"><span data-stu-id="c9cbe-365">The following are the APIs that enable an application to migrate to or from the GDI font system:</span></span>

-   [<span data-ttu-id="c9cbe-366">**CreateFontFromLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="c9cbe-366">**CreateFontFromLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    <span data-ttu-id="c9cbe-367">Crea un objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) que coincide con las propiedades especificadas por la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="c9cbe-367">Creates an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object that matches the properties specified by the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

-   [<span data-ttu-id="c9cbe-368">**ConvertFontToLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="c9cbe-368">**ConvertFontToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    <span data-ttu-id="c9cbe-369">Inicializa una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) basada en las propiedades compatibles con GDI del [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)especificado.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-369">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont).</span></span>

-   [<span data-ttu-id="c9cbe-370">**ConvertFontFaceToLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="c9cbe-370">**ConvertFontFaceToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    <span data-ttu-id="c9cbe-371">Inicializa una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) basada en las propiedades compatibles con GDI del [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)especificado.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-371">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface).</span></span>

-   [<span data-ttu-id="c9cbe-372">**CreateFontFaceFromHdc**</span><span class="sxs-lookup"><span data-stu-id="c9cbe-372">**CreateFontFaceFromHdc**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    <span data-ttu-id="c9cbe-373">Crea un objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) que corresponde al **HFONT** seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-373">Creates an [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object that corresponds to the currently selected **HFONT**.</span></span>

## <a name="conclusion"></a><span data-ttu-id="c9cbe-374">Conclusión</span><span class="sxs-lookup"><span data-stu-id="c9cbe-374">Conclusion</span></span>

<span data-ttu-id="c9cbe-375">Mejorar la experiencia de lectura es de gran valor para los usuarios, ya sea en la pantalla o en papel.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-375">Improving the reading experience is of great value to users whether it is on the screen or on paper.</span></span> <span data-ttu-id="c9cbe-376">[DirectWrite](direct-write-portal.md) proporciona la facilidad de uso y el modelo de programación por capas para que los desarrolladores de aplicaciones mejoren la experiencia de texto en sus aplicaciones Windows.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-376">[DirectWrite](direct-write-portal.md) provides the ease of use and the layered programming model for application developers to improve the text experience for their Windows applications.</span></span> <span data-ttu-id="c9cbe-377">Las aplicaciones pueden usar DirectWrite para representar texto con formato enriquecido para su interfaz de usuario y sus documentos con la API de diseño.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-377">Applications can use DirectWrite to render richly formatted text for their UI and documents with the layout API.</span></span> <span data-ttu-id="c9cbe-378">En escenarios más complejos, una aplicación puede trabajar directamente con glifos, fuentes de acceso, etc., y aprovechar la potencia de DirectWrite para ofrecer tipografía de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-378">For more complex scenarios, an application can work directly with glyphs, access fonts, and so on, and harness the power of DirectWrite to deliver high-quality typography.</span></span>

<span data-ttu-id="c9cbe-379">Las capacidades de interoperabilidad de [DirectWrite](direct-write-portal.md) permiten a los desarrolladores de aplicaciones llevar adelante sus códigos base de Win32 existentes y adoptar DirectWrite de manera selectiva dentro de sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c9cbe-379">The interoperability capabilities of [DirectWrite](direct-write-portal.md) enable application developers to carry forward their existing Win32 codebases and adopt DirectWrite selectively within their applications.</span></span>

 

 