---
title: Formato del portapapeles HTML
description: En esta sección se describe el formato del portapapeles HTML.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Interfaz de usuario de Windows, Portapapeles
- portapapeles, cortar datos
- portapapeles, copiar datos
- portapapeles, pegar datos
- portapapeles, formatos
- portapapeles, formato HTML
- portapapeles, cortar texto HTML
- portapapeles, pegar texto HTML
- CF_HTML formato del portapapeles
- portapapeles, formato de CF_HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cdcd9c2fc982a7cbde38bba4b7dec6738f1793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075895"
---
# <a name="html-clipboard-format"></a><span data-ttu-id="40f91-113">Formato del portapapeles HTML</span><span class="sxs-lookup"><span data-stu-id="40f91-113">HTML Clipboard Format</span></span>

<span data-ttu-id="40f91-114">Los requisitos para transferir texto HTML por medio del portapapeles difieren en función del escenario.</span><span class="sxs-lookup"><span data-stu-id="40f91-114">The requirements for transferring HTML text by means of the clipboard differ depending on scenario.</span></span> <span data-ttu-id="40f91-115">Este artículo está relacionado con la corte y pegado de fragmentos de un documento HTML.</span><span class="sxs-lookup"><span data-stu-id="40f91-115">This article is concerned with cutting and pasting fragments of an HTML document.</span></span> <span data-ttu-id="40f91-116">Puede haber requisitos para transferir documentos HTML completos a través del portapapeles; sin embargo, este artículo está controlado por un requisito para transferir fragmentos del texto HTML seleccionado.</span><span class="sxs-lookup"><span data-stu-id="40f91-116">There may be requirements for transferring entire HTML documents through the clipboard; however, this article is driven by a requirement to transfer fragments of selected HTML text.</span></span> <span data-ttu-id="40f91-117">Como tal, un método que requiera copiar el documento HTML completo en el portapapeles se considera demasiado pesado.</span><span class="sxs-lookup"><span data-stu-id="40f91-117">As such, a method that required the entire HTML document to be copied to the clipboard is seen as too heavyweight.</span></span>

<span data-ttu-id="40f91-118">El \_ formato del portapapeles HTML de CF permite que un fragmento de texto HTML sin formato y su contexto se almacenen en el portapapeles como ASCII.</span><span class="sxs-lookup"><span data-stu-id="40f91-118">The CF\_HTML clipboard format allows a fragment of raw HTML text and its context to be stored on the clipboard as ASCII.</span></span> <span data-ttu-id="40f91-119">Esto permite que una aplicación examine el contexto del fragmento HTML, que consta de todas las etiquetas adyacentes, para que las etiquetas circundantes del fragmento HTML se puedan anotar con sus atributos.</span><span class="sxs-lookup"><span data-stu-id="40f91-119">This allows the context of the HTML fragment, which consists of all preceding surrounding tags, to be examined by an application so that the surrounding tags of the HTML fragment can be noted with their attributes.</span></span> <span data-ttu-id="40f91-120">Aunque es el caso de las aplicaciones decidir cómo interpretar estos fragmentos, algunas instrucciones básicas se incluyen aquí en función de las implementaciones de IE4/MSHTML.</span><span class="sxs-lookup"><span data-stu-id="40f91-120">Although it is up to applications to decide how to interpret such fragments, some basic guidelines are included here based on IE4/MSHTML implementations.</span></span>

<span data-ttu-id="40f91-121">El nombre oficial del portapapeles (la cadena usada por RegisterClipboardFormat) es el formato HTML.</span><span class="sxs-lookup"><span data-stu-id="40f91-121">The official name of the clipboard (the string used by RegisterClipboardFormat) is HTML Format.</span></span>

-   [<span data-ttu-id="40f91-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="40f91-122">Description</span></span>](#description)
-   [<span data-ttu-id="40f91-123">Escenarios</span><span class="sxs-lookup"><span data-stu-id="40f91-123">Scenarios</span></span>](#scenarios)

## <a name="description"></a><span data-ttu-id="40f91-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="40f91-124">Description</span></span>

<span data-ttu-id="40f91-125">El \_ HTML de CF tiene un formato de texto completo (por ejemplo, entre otras cosas, en el espíritu HTML y usa UTF-8) e incluye un `description` , un opcional `context` y, dentro del contexto, `fragment` .</span><span class="sxs-lookup"><span data-stu-id="40f91-125">CF\_HTML is entirely text format (to be, among other things, in the HTML spirit, and uses UTF-8) and includes a `description`, an optional `context`, and, within the context, the `fragment`.</span></span>

<span data-ttu-id="40f91-126">El siguiente es un ejemplo de un portapapeles:</span><span class="sxs-lookup"><span data-stu-id="40f91-126">The following is an example of a clipboard:</span></span>


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



<span data-ttu-id="40f91-127">La descripción incluye el número de versión y los desplazamientos del portapapeles, lo que indica dónde se inicia y finaliza el contexto y el fragmento.</span><span class="sxs-lookup"><span data-stu-id="40f91-127">The description includes the clipboard version number and offsets, indicating where the context and the fragment start and end.</span></span> <span data-ttu-id="40f91-128">La descripción es una lista de palabras clave de texto ASCII (min/Mayús no es significativa) seguida de una cadena y separadas por dos puntos (:).</span><span class="sxs-lookup"><span data-stu-id="40f91-128">The description is a list of ASCII text keywords (min/maj is not meaningful) followed by a string and separated by a colon (:).</span></span>

<span data-ttu-id="40f91-129">**Versión**: número de versión de VV del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="40f91-129">**Version**: vv version number of the clipboard.</span></span> <span data-ttu-id="40f91-130">La versión inicial es 0,9.</span><span class="sxs-lookup"><span data-stu-id="40f91-130">Starting version is 0.9.</span></span>

<span data-ttu-id="40f91-131">**StartHTML**: byteCount desde el principio del Portapapeles hasta el inicio del contexto, o-1 si no hay ningún contexto.</span><span class="sxs-lookup"><span data-stu-id="40f91-131">**StartHTML**: bytecount from the beginning of the clipboard to the start of the context, or -1 if no context.</span></span>

<span data-ttu-id="40f91-132">**Entext: byteCount** desde el principio del Portapapeles hasta el final del contexto, o-1 si no hay contexto.</span><span class="sxs-lookup"><span data-stu-id="40f91-132">**EndHTML**: bytecount from the beginning of the clipboard to the end of the context, or -1 if no context.</span></span>

<span data-ttu-id="40f91-133">**StartFragment**: byteCount desde el principio del Portapapeles hasta el inicio del fragmento.</span><span class="sxs-lookup"><span data-stu-id="40f91-133">**StartFragment**: bytecount from the beginning of the clipboard to the start of the fragment.</span></span>

<span data-ttu-id="40f91-134">**EndFragment**: byteCount desde el principio del Portapapeles hasta el final del fragmento.</span><span class="sxs-lookup"><span data-stu-id="40f91-134">**EndFragment**: bytecount from the beginning of the clipboard to the end of the fragment.</span></span>

<span data-ttu-id="40f91-135">**StartSelection**: byteCount desde el principio del Portapapeles hasta el inicio de la selección.</span><span class="sxs-lookup"><span data-stu-id="40f91-135">**StartSelection**: bytecount from the beginning of the clipboard to the start of the selection.</span></span>

<span data-ttu-id="40f91-136">**EndSelection**: byteCount desde el principio del Portapapeles hasta el final de la selección.</span><span class="sxs-lookup"><span data-stu-id="40f91-136">**EndSelection**: bytecount from the beginning of the clipboard to the end of the selection.</span></span>

<span data-ttu-id="40f91-137">Las palabras clave StartSelection y EndSelection son opcionales y deben omitirse ambos si no desea que la aplicación genere esta información.</span><span class="sxs-lookup"><span data-stu-id="40f91-137">The StartSelection and EndSelection keywords are optional and must both be omitted if you do not want the application to generate this information.</span></span>

<span data-ttu-id="40f91-138">Otra información de este tipo podría agregarse aquí más adelante, ya que el código HTML se inicia en el StartHTMLoffset.</span><span class="sxs-lookup"><span data-stu-id="40f91-138">Other information of this kind could be added here later, since the HTML starts at the StartHTMLoffset.</span></span> <span data-ttu-id="40f91-139">Por ejemplo, se podrían agregar varios pares de StartFragment/EndFragment más adelante para admitir la selección no contigua de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="40f91-139">For example, multiple pairs of StartFragment / EndFragment could be added later to support noncontiguous selection of fragments.</span></span>

<span data-ttu-id="40f91-140">Para la comodidad de los programas que generan el bytecounts, bytecounts podría quedar rellenado con ceros.</span><span class="sxs-lookup"><span data-stu-id="40f91-140">For the convenience of the programs generating the bytecounts, bytecounts could be left padded by zeros.</span></span> <span data-ttu-id="40f91-141">Por ejemplo, los programas que generan el bytecounts podrían afectar arbitrariamente los diez (10) ceros a cada palabra clave (StartHTML: 0000000000) y, a continuación, cuando se conoce el byteCount exacto de StartHTML (por ejemplo, 71), el programa puede reemplazar el número de ceros adecuado por el byteCount (StartHTML: 0000000071).</span><span class="sxs-lookup"><span data-stu-id="40f91-141">For example, programs generating the bytecounts could arbitrarily affect ten (10) zeros to each keyword (StartHTML: 0000000000) and then, when the exact StartHTML bytecount is known (say, 71), the program can replace the appropriate number of zeros by the bytecount (StartHTML: 0000000071).</span></span>

<span data-ttu-id="40f91-142">El único juego de caracteres que admite el portapapeles es Unicode en su codificación UTF-8.</span><span class="sxs-lookup"><span data-stu-id="40f91-142">The only character set supported by the clipboard is Unicode in its UTF-8 encoding.</span></span> <span data-ttu-id="40f91-143">Dado que los primeros caracteres de UTF-8 y ASCII coinciden, la descripción es siempre ASCII, pero los bytes del contexto (a partir de StartHTML) podrían usar cualquier otro carácter codificado en UTF-8.</span><span class="sxs-lookup"><span data-stu-id="40f91-143">Because the first characters of UTF-8 and ASCII match, the description is always ASCII, but the bytes of the context (starting at StartHTML) could be using any other characters coded in UTF-8.</span></span>

<span data-ttu-id="40f91-144">El final de las líneas en el encabezado de formato del portapapeles podría ser CR o CR/LF o LF.</span><span class="sxs-lookup"><span data-stu-id="40f91-144">End of lines in the clipboard format header could be CR or CR/LF or LF.</span></span>

<span data-ttu-id="40f91-145">El fragmento contiene código HTML puro y válido que representa el área seleccionada por el usuario (para copiarla, por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="40f91-145">The fragment contains pure, valid HTML representing the area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="40f91-146">Contiene el texto seleccionado más las etiquetas de apertura y los atributos de cualquier elemento que tenga una etiqueta de cierre dentro del texto seleccionado y las etiquetas de cierre al final del fragmento para cualquier etiqueta de apertura incluida.</span><span class="sxs-lookup"><span data-stu-id="40f91-146">This contains the selected text plus the opening tags and attributes of any element that has an end tag within the selected text, and end tags at the end of the fragment for any start tag included.</span></span> <span data-ttu-id="40f91-147">Esta es toda la información necesaria para el pegado básico de un fragmento HTML.</span><span class="sxs-lookup"><span data-stu-id="40f91-147">This is all information required for basic pasting of an HTML fragment.</span></span>

<span data-ttu-id="40f91-148">El fragmento debe ir precedido y seguido de los comentarios HTML</span><span class="sxs-lookup"><span data-stu-id="40f91-148">The fragment should be preceded and followed by the HTML comments</span></span> <!--StartFragment--> <span data-ttu-id="40f91-149">y</span><span class="sxs-lookup"><span data-stu-id="40f91-149">and</span></span> <!--EndFragment--> <span data-ttu-id="40f91-150">(no se permite ningún espacio entre el!--y el texto) para indicar cómo se inicia y finaliza el fragmento.</span><span class="sxs-lookup"><span data-stu-id="40f91-150">(no space allowed between the !-- and the text) to conveniently indicate where the fragment starts and ends.</span></span> <span data-ttu-id="40f91-151">Por lo tanto, el inicio y el final del fragmento se indican mediante la presencia de estos comentarios y los recuentos de bytes StartFragment y EndFragment en la descripción.</span><span class="sxs-lookup"><span data-stu-id="40f91-151">Thus the start and end of the fragment are indicated by the presence of these comments and by StartFragment and EndFragment byte counts in the description.</span></span> <span data-ttu-id="40f91-152">Se espera que las herramientas generen esta información.</span><span class="sxs-lookup"><span data-stu-id="40f91-152">Tools are expected to produce this information.</span></span> <span data-ttu-id="40f91-153">Esta redundancia se ha introducido para poder encontrar rápidamente el inicio del fragmento (desde el recuento de bytes) y marcar la posición del fragmento directamente en el árbol HTML.</span><span class="sxs-lookup"><span data-stu-id="40f91-153">This redundancy has been introduced to be able to rapidly find the start of the fragment (from the byte count) and mark the position of the fragment directly in the HTML tree.</span></span>

<span data-ttu-id="40f91-154">La selección indica dentro del fragmento el área HTML exacta que el usuario ha seleccionado (para copiarlo, por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="40f91-154">The selection indicates inside the fragment the exact HTML area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="40f91-155">Esto agrega más información al fragmento indicando el texto exacto seleccionado, sin las etiquetas de apertura y las etiquetas de cierre que se han agregado para asegurarse de que el fragmento es HTML con formato correcto.</span><span class="sxs-lookup"><span data-stu-id="40f91-155">This adds more information to the fragment by indicating the exact selected text, without the opening tags and end tags that have been added to ensure the fragment is well-formed HTML.</span></span>

<span data-ttu-id="40f91-156">La selección es opcional, ya que se incluye suficiente información en el fragmento para el pegado básico.</span><span class="sxs-lookup"><span data-stu-id="40f91-156">The selection is optional, as sufficient information is included in the fragment for basic pasting.</span></span> <span data-ttu-id="40f91-157">Si no se almacena la selección, StartSelection y EndSelection no se almacenan en el encabezado.</span><span class="sxs-lookup"><span data-stu-id="40f91-157">If the selection is not stored, both StartSelection and EndSelection are not stored in the header.</span></span>

<span data-ttu-id="40f91-158">El contexto es un documento HTML válido y completo.</span><span class="sxs-lookup"><span data-stu-id="40f91-158">The context is a valid, complete HTML document.</span></span> <span data-ttu-id="40f91-159">Este artículo contiene el fragmento y todas las etiquetas adyacentes anteriores (etiquetas de inicio y finalización; las etiquetas circundantes anteriores representan todos los nodos primarios del fragmento, hasta el nodo HTML).</span><span class="sxs-lookup"><span data-stu-id="40f91-159">This article contains the fragment and all preceding surrounding tags (start and end tags; these preceding surrounding tags represent all the parent nodes of the fragment, until the HTML node).</span></span> <span data-ttu-id="40f91-160">El artículo también contiene el encabezado completo y permite incluir los elementos BASE y título, por ejemplo, para que se pueda obtener esta información adicional.</span><span class="sxs-lookup"><span data-stu-id="40f91-160">The article also contains the complete HEAD, and allows the BASE and TITLE elements, for example, to be included so this additional information can be obtained.</span></span> <span data-ttu-id="40f91-161">Una aplicación que copia un fragmento de HTML en el portapapeles puede optar por crear un elemento BASE para incluirlo en el contexto si este elemento no está ya presente para que se puedan resolver las direcciones URL parciales del fragmento.</span><span class="sxs-lookup"><span data-stu-id="40f91-161">An application copying a fragment of HTML to the clipboard can choose to create a BASE element to include in the context if such an element is not already present so that partial URLs in the fragment can be resolved.</span></span>

<span data-ttu-id="40f91-162">El contexto es opcional, ya que se incluye suficiente información en el fragmento para que tenga lugar el pegado básico de un fragmento HTML.</span><span class="sxs-lookup"><span data-stu-id="40f91-162">The context is optional, as sufficient information is included in the fragment for basic pasting of an HTML fragment to take place.</span></span> <span data-ttu-id="40f91-163">Si no se almacena el contexto, solo se almacena el fragmento y StartHTML = endhtml =-1.</span><span class="sxs-lookup"><span data-stu-id="40f91-163">If the context is not stored, the fragment only is stored and the StartHTML=EndHTML=-1.</span></span>

## <a name="scenarios"></a><span data-ttu-id="40f91-164">Escenarios</span><span class="sxs-lookup"><span data-stu-id="40f91-164">Scenarios</span></span>

<span data-ttu-id="40f91-165">En los escenarios siguientes se describe cómo el editor HTML IE4/MSHTML controla el corte y pegado HTML. otras aplicaciones pueden o no seguir estos escenarios.</span><span class="sxs-lookup"><span data-stu-id="40f91-165">The following scenarios describe how the IE4/MSHTML HTML editor handles HTML cut and paste; other applications may or may not follow these scenarios.</span></span> <span data-ttu-id="40f91-166">El formato del portapapeles que se describe aquí está diseñado para permitir la flexibilidad en el modo en que una aplicación elige funcionar.</span><span class="sxs-lookup"><span data-stu-id="40f91-166">The clipboard format described here is intended to allow flexibility for how an application chooses to function.</span></span> <span data-ttu-id="40f91-167">(Estos escenarios muestran solo un buen código HTML, es decir, no hay etiquetas superpuestas).</span><span class="sxs-lookup"><span data-stu-id="40f91-167">(These scenarios show only good HTML, that is, no overlapping tags.)</span></span>

1.  <span data-ttu-id="40f91-168">Fragmento simple de HTML.</span><span class="sxs-lookup"><span data-stu-id="40f91-168">Simple Fragment of HTML.</span></span>
    -   -   <span data-ttu-id="40f91-169">Texto HTML:</span><span class="sxs-lookup"><span data-stu-id="40f91-169">HTML text:</span></span>

            <span data-ttu-id="40f91-170"><BODY>Esto es normal si se pone en <B>negrita </B>y está en negrita <I> <B>cursiva </B></I> .</BODY></span><span class="sxs-lookup"><span data-stu-id="40f91-170"><BODY>This is normal <B>This is bold </B><I><B>This is bold italic </B>This is italic </I></BODY></span></span>

        -   <span data-ttu-id="40f91-171">Aparece como:</span><span class="sxs-lookup"><span data-stu-id="40f91-171">Appears as:</span></span>

            <span data-ttu-id="40f91-172">Esto es normal si se pone en **negrita** y está en negrita    \* **cursiva**   .</span><span class="sxs-lookup"><span data-stu-id="40f91-172">This is normal **This is bold**  \***This is bold italic**  This is italic\*</span></span>

        -   <span data-ttu-id="40f91-173">El texto \* \* que se encuentra entre el se selecciona y se copia en el portapapeles:</span><span class="sxs-lookup"><span data-stu-id="40f91-173">The text between the \*\* is selected and copied to the clipboard:</span></span>

            <span data-ttu-id="40f91-174">Esto **es normal si se pone** en \* \* **negrita** ,    \*    \* \*  es decir, si está en cursiva.</span><span class="sxs-lookup"><span data-stu-id="40f91-174">This is normal **This is** \*\* **bold**   \***This is bold italic**  This\*\*\* *is italic*</span></span>

        -   <span data-ttu-id="40f91-175">Esto es lo que se incluirá en el portapapeles (tenga en cuenta que se trata de la interpretación de IE4/MSHTML):</span><span class="sxs-lookup"><span data-stu-id="40f91-175">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <span data-ttu-id="40f91-176">Versión: 0.9</span><span class="sxs-lookup"><span data-stu-id="40f91-176">Version:0.9</span></span>

            <span data-ttu-id="40f91-177">StartHTML: 71</span><span class="sxs-lookup"><span data-stu-id="40f91-177">StartHTML:71</span></span>

            <span data-ttu-id="40f91-178">DHTML: 160</span><span class="sxs-lookup"><span data-stu-id="40f91-178">EndHTML:160</span></span>

            <span data-ttu-id="40f91-179">StartFragment: 130</span><span class="sxs-lookup"><span data-stu-id="40f91-179">StartFragment:130</span></span>

            <span data-ttu-id="40f91-180">EndFragment: 150</span><span class="sxs-lookup"><span data-stu-id="40f91-180">EndFragment:150</span></span>

            <span data-ttu-id="40f91-181">**StartSelection: 130**</span><span class="sxs-lookup"><span data-stu-id="40f91-181">**StartSelection:130**</span></span>

            <span data-ttu-id="40f91-182">**EndSelection: 150**</span><span class="sxs-lookup"><span data-stu-id="40f91-182">**EndSelection:150**</span></span>

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            <span data-ttu-id="40f91-183">**<B>Bold</B><I><B>es negrita cursiva</B></I>**</span><span class="sxs-lookup"><span data-stu-id="40f91-183">**<B>bold</B><I><B>This is bold italic</B>This</I>**</span></span>

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   <span data-ttu-id="40f91-184">En este escenario, solo la etiqueta de cuerpo y la etiqueta HTML aparecen en el contexto como precede al fragmento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="40f91-184">In this scenario only the BODY tag and the HTML tag appear in the context as it precedes the selected fragment.</span></span> <span data-ttu-id="40f91-185">Tenga en cuenta que las etiquetas de inicio y las etiquetas de cierre se incluyen en el contexto.</span><span class="sxs-lookup"><span data-stu-id="40f91-185">Note that start tags and end tags are included in the context.</span></span> <span data-ttu-id="40f91-186">La selección, como delimitada por StartSelection y EndSelection, se muestra en negrita.</span><span class="sxs-lookup"><span data-stu-id="40f91-186">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

2.  <span data-ttu-id="40f91-187">Fragmento de una tabla en HTML.</span><span class="sxs-lookup"><span data-stu-id="40f91-187">Fragment of a table in HTML.</span></span>
    -   -   <span data-ttu-id="40f91-188">Texto HTML:</span><span class="sxs-lookup"><span data-stu-id="40f91-188">HTML text:</span></span>

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="40f91-189">Head1</span><span class="sxs-lookup"><span data-stu-id="40f91-189">Head1</span></span></TH><TD><span data-ttu-id="40f91-190">Elemento 1</span><span class="sxs-lookup"><span data-stu-id="40f91-190">Item 1</span></span></TD><TD><span data-ttu-id="40f91-191">Item 2</span><span class="sxs-lookup"><span data-stu-id="40f91-191">Item 2</span></span></TD><TD><span data-ttu-id="40f91-192">Item 3</span><span class="sxs-lookup"><span data-stu-id="40f91-192">Item 3</span></span></TD><TD><span data-ttu-id="40f91-193">Elemento 4</span><span class="sxs-lookup"><span data-stu-id="40f91-193">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="40f91-194">Elemento 5</span><span class="sxs-lookup"><span data-stu-id="40f91-194">Item 5</span></span></TD><TD><span data-ttu-id="40f91-195">Elemento 6</span><span class="sxs-lookup"><span data-stu-id="40f91-195">Item 6</span></span></TD><TD><span data-ttu-id="40f91-196">Elemento 7</span><span class="sxs-lookup"><span data-stu-id="40f91-196">Item 7</span></span></TD><TD><span data-ttu-id="40f91-197">Elemento 8</span><span class="sxs-lookup"><span data-stu-id="40f91-197">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="40f91-198">Head2</span><span class="sxs-lookup"><span data-stu-id="40f91-198">Head2</span></span></TH><TD><span data-ttu-id="40f91-199">Elemento 9</span><span class="sxs-lookup"><span data-stu-id="40f91-199">Item 9</span></span></TD><TD><span data-ttu-id="40f91-200">Elemento 10</span><span class="sxs-lookup"><span data-stu-id="40f91-200">Item 10</span></span></TD><TD><span data-ttu-id="40f91-201">Elemento 11</span><span class="sxs-lookup"><span data-stu-id="40f91-201">Item 11</span></span></TD><TD><span data-ttu-id="40f91-202">Elemento 12</span><span class="sxs-lookup"><span data-stu-id="40f91-202">Item 12</span></span></TD></TR></TABLE></BODY>

        -   <span data-ttu-id="40f91-203">Aparece como: ></span><span class="sxs-lookup"><span data-stu-id="40f91-203">Appears as: ></span></span><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="40f91-204">Head1</span><span class="sxs-lookup"><span data-stu-id="40f91-204">Head1</span></span></TH><TD><span data-ttu-id="40f91-205">Elemento 1</span><span class="sxs-lookup"><span data-stu-id="40f91-205">Item 1</span></span></TD><TD><span data-ttu-id="40f91-206">Item 2</span><span class="sxs-lookup"><span data-stu-id="40f91-206">Item 2</span></span></TD><TD><span data-ttu-id="40f91-207">Item 3</span><span class="sxs-lookup"><span data-stu-id="40f91-207">Item 3</span></span></TD><TD><span data-ttu-id="40f91-208">Elemento 4</span><span class="sxs-lookup"><span data-stu-id="40f91-208">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="40f91-209">Elemento 5</span><span class="sxs-lookup"><span data-stu-id="40f91-209">Item 5</span></span></TD><TD><span data-ttu-id="40f91-210">Elemento 6</span><span class="sxs-lookup"><span data-stu-id="40f91-210">Item 6</span></span></TD><TD><span data-ttu-id="40f91-211">Elemento 7</span><span class="sxs-lookup"><span data-stu-id="40f91-211">Item 7</span></span></TD><TD><span data-ttu-id="40f91-212">Elemento 8</span><span class="sxs-lookup"><span data-stu-id="40f91-212">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="40f91-213">Head2</span><span class="sxs-lookup"><span data-stu-id="40f91-213">Head2</span></span></TH><TD><span data-ttu-id="40f91-214">Elemento 9</span><span class="sxs-lookup"><span data-stu-id="40f91-214">Item 9</span></span></TD><TD><span data-ttu-id="40f91-215">Elemento 10</span><span class="sxs-lookup"><span data-stu-id="40f91-215">Item 10</span></span></TD><TD><span data-ttu-id="40f91-216">Elemento 11</span><span class="sxs-lookup"><span data-stu-id="40f91-216">Item 11</span></span></TD><TD><span data-ttu-id="40f91-217">Elemento 12</span><span class="sxs-lookup"><span data-stu-id="40f91-217">Item 12</span></span></TD></TR></TABLE><span data-ttu-id="40f91-218"><. \[ CDATA\[\]\]></span><span class="sxs-lookup"><span data-stu-id="40f91-218"><!\[CDATA\[\]\]></span></span>
        -   <span data-ttu-id="40f91-219">Los elementos item 6, Item7 (, Item 10 y Item 11 de la tabla se seleccionan como un bloque y se copian en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="40f91-219">The Item 6, Item7, Item 10, and Item 11 elements of the table are selected as a block and copied to the clipboard.</span></span>
        -   <span data-ttu-id="40f91-220">Esto es lo que se incluirá en el portapapeles (tenga en cuenta que se trata de la interpretación de IE4/MSHTML):</span><span class="sxs-lookup"><span data-stu-id="40f91-220">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            <span data-ttu-id="40f91-221">**<TR><TD>Elemento 6 elemento </TD> <TD> 7 elemento </TD> </TR> <TR> <TD> 10 </TD> <TD> elemento 11</TD></TR>**</span><span class="sxs-lookup"><span data-stu-id="40f91-221">**<TR><TD>Item 6</TD><TD>Item 7</TD></TR><TR><TD>Item 10</TD><TD>Item 11</TD></TR>**</span></span>

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  <span data-ttu-id="40f91-222">Pegar un fragmento de una lista ordenada en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="40f91-222">Pasting a fragment of an ordered list into plain text.</span></span>
    -   -   <span data-ttu-id="40f91-223">Texto HTML:</span><span class="sxs-lookup"><span data-stu-id="40f91-223">HTML text:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="40f91-224">Elemento 1</span><span class="sxs-lookup"><span data-stu-id="40f91-224">Item 1</span></span><LI><span data-ttu-id="40f91-225">Item 2</span><span class="sxs-lookup"><span data-stu-id="40f91-225">Item 2</span></span><LI><span data-ttu-id="40f91-226">Item 3</span><span class="sxs-lookup"><span data-stu-id="40f91-226">Item 3</span></span><LI><span data-ttu-id="40f91-227">Elemento 4</span><span class="sxs-lookup"><span data-stu-id="40f91-227">Item 4</span></span><LI><span data-ttu-id="40f91-228">Elemento 5</span><span class="sxs-lookup"><span data-stu-id="40f91-228">Item 5</span></span><LI><span data-ttu-id="40f91-229">Elemento 6</span><span class="sxs-lookup"><span data-stu-id="40f91-229">Item 6</span></span></OL></BODY>

        -   <span data-ttu-id="40f91-230">Aparece como:</span><span class="sxs-lookup"><span data-stu-id="40f91-230">Appears as:</span></span>
            1.  <span data-ttu-id="40f91-231">Elemento 1</span><span class="sxs-lookup"><span data-stu-id="40f91-231">Item 1</span></span>
            2.  <span data-ttu-id="40f91-232">Item 2</span><span class="sxs-lookup"><span data-stu-id="40f91-232">Item 2</span></span>
            3.  <span data-ttu-id="40f91-233">Item 3</span><span class="sxs-lookup"><span data-stu-id="40f91-233">Item 3</span></span>
            4.  <span data-ttu-id="40f91-234">Elemento 4</span><span class="sxs-lookup"><span data-stu-id="40f91-234">Item 4</span></span>
            5.  <span data-ttu-id="40f91-235">Elemento 5</span><span class="sxs-lookup"><span data-stu-id="40f91-235">Item 5</span></span>
            6.  <span data-ttu-id="40f91-236">Elemento 6</span><span class="sxs-lookup"><span data-stu-id="40f91-236">Item 6</span></span>
        -   <span data-ttu-id="40f91-237">El usuario selecciona y copia los elementos 3 a 5 en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="40f91-237">The user selects and copies items 3 through 5 to the clipboard.</span></span> <span data-ttu-id="40f91-238">El siguiente código HTML está en el portapapeles:</span><span class="sxs-lookup"><span data-stu-id="40f91-238">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="40f91-239"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="40f91-239"><DOCTYPE...><HTML><BODY></span></span><OL TYPE = a>

            <!-- StartFragment-->

            <span data-ttu-id="40f91-240">**<LI>Elemento 3 elemento <LI> 4 <LI> elemento 5**</span><span class="sxs-lookup"><span data-stu-id="40f91-240">**<LI>Item 3<LI>Item 4<LI>Item 5**</span></span>

            <!-- EndFragment-->

            </OL></BODY></HTML>

            <span data-ttu-id="40f91-241">La selección, como delimitada por StartSelection y EndSelection, se muestra en negrita.</span><span class="sxs-lookup"><span data-stu-id="40f91-241">The selection, as delimited by StartSelection and EndSelection, is show in bold.</span></span>

        -   <span data-ttu-id="40f91-242">Si este fragmento se pega ahora en un documento vacío, se creará el siguiente código HTML:</span><span class="sxs-lookup"><span data-stu-id="40f91-242">If this fragment is now pasted into an empty document, the following HTML will be created:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="40f91-243">Item 3</span><span class="sxs-lookup"><span data-stu-id="40f91-243">Item 3</span></span><LI><span data-ttu-id="40f91-244">Elemento 4</span><span class="sxs-lookup"><span data-stu-id="40f91-244">Item 4</span></span><LI><span data-ttu-id="40f91-245">Elemento 5</span><span class="sxs-lookup"><span data-stu-id="40f91-245">Item 5</span></span></OL></BODY>

        -   <span data-ttu-id="40f91-246">Aparecen como:</span><span class="sxs-lookup"><span data-stu-id="40f91-246">Appearing as:</span></span>
            1.  <span data-ttu-id="40f91-247">Item 3</span><span class="sxs-lookup"><span data-stu-id="40f91-247">Item 3</span></span>
            2.  <span data-ttu-id="40f91-248">Elemento 4</span><span class="sxs-lookup"><span data-stu-id="40f91-248">Item 4</span></span>
            3.  <span data-ttu-id="40f91-249">Elemento 5</span><span class="sxs-lookup"><span data-stu-id="40f91-249">Item 5</span></span>

4.  <span data-ttu-id="40f91-250">Pegar una región parcialmente seleccionada.</span><span class="sxs-lookup"><span data-stu-id="40f91-250">Pasting a partially selected region.</span></span>
    -   -   <span data-ttu-id="40f91-251">Texto HTML:</span><span class="sxs-lookup"><span data-stu-id="40f91-251">HTML text:</span></span>

            <P> <span data-ttu-id="40f91-252">IE4/MSHTML es un editor WYSIWYG que admite:</span><span class="sxs-lookup"><span data-stu-id="40f91-252">IE4/MSHTML is a WYSIWYG Editor that supports :</span></span><UL><LI><span data-ttu-id="40f91-253">Cortar</span><span class="sxs-lookup"><span data-stu-id="40f91-253">Cut</span></span><LI><span data-ttu-id="40f91-254">Copiar</span><span class="sxs-lookup"><span data-stu-id="40f91-254">Copy</span></span><LI><span data-ttu-id="40f91-255">Pegar</span><span class="sxs-lookup"><span data-stu-id="40f91-255">Paste</span></span></UL><P><span data-ttu-id="40f91-256">Esta es una herramienta excelente.</span><span class="sxs-lookup"><span data-stu-id="40f91-256">This is a Great Tool !</span></span>

        -   <span data-ttu-id="40f91-257">Aparece como: IE4/MSHTML es un editor WYSIWYG que admite:</span><span class="sxs-lookup"><span data-stu-id="40f91-257">Appears as:IE4/MSHTML is a WYSIWYG Editor that supports :</span></span>
            -   -   <span data-ttu-id="40f91-258">Cortar</span><span class="sxs-lookup"><span data-stu-id="40f91-258">Cut</span></span>
                -   <span data-ttu-id="40f91-259">Copiar</span><span class="sxs-lookup"><span data-stu-id="40f91-259">Copy</span></span>
                -   <span data-ttu-id="40f91-260">Pegar</span><span class="sxs-lookup"><span data-stu-id="40f91-260">Paste</span></span>

        -   <span data-ttu-id="40f91-261">El usuario selecciona "WYSIWYG" hasta "COP". El siguiente código HTML está en el portapapeles:</span><span class="sxs-lookup"><span data-stu-id="40f91-261">The user selects from "WYSIWYG" until "Cop".The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="40f91-262"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="40f91-262"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <P>

            <span data-ttu-id="40f91-263">**Editor WYSIWYG, que admite**</span><span class="sxs-lookup"><span data-stu-id="40f91-263">**WYSIWYG Editor, which supports**</span></span>

            <span data-ttu-id="40f91-264">**<UL><LI>Cortar <LI> COP**</span><span class="sxs-lookup"><span data-stu-id="40f91-264">**<UL><LI>Cut<LI>Cop**</span></span>

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   <span data-ttu-id="40f91-265">El usuario selecciona "opiar" hasta "excelente".</span><span class="sxs-lookup"><span data-stu-id="40f91-265">The user selects from "opy" until "Great".</span></span>

            <span data-ttu-id="40f91-266">El siguiente código HTML está en el portapapeles:</span><span class="sxs-lookup"><span data-stu-id="40f91-266">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="40f91-267"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="40f91-267"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <UL><LI>

            <span data-ttu-id="40f91-268">**copiar y <LI> pegar </UL> <P> esto es una excelente**</span><span class="sxs-lookup"><span data-stu-id="40f91-268">**opy<LI>Paste</UL><P> This is a Great**</span></span>

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            <span data-ttu-id="40f91-269">La selección, como delimitada por StartSelection y EndSelection, se muestra en negrita.</span><span class="sxs-lookup"><span data-stu-id="40f91-269">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

 

 




