---
title: Una lista de reproducción avanzada
description: Una lista de reproducción avanzada
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
keywords:
- Listas de reproducción de metarchivos de Windows Media, ejemplos de listas de reproducción
- listas de reproducción, ejemplos de listas de reproducción
- listas de reproducción de metarchivos, ejemplos de listas de reproducción
- Listas de reproducción de metarchivos de Windows Media, listas de reproducción de ejemplo
- listas de reproducción, listas de reproducción de ejemplo
- listas de reproducción de metarchivos, listas de reproducción de ejemplo
- Listas de reproducción de metarchivos de Windows Media, listas de reproducción de ejemplo
- listas de reproducción, listas de reproducción de ejemplo
- listas de reproducción de metarchivos, listas de reproducción de ejemplo
- Listas de reproducción de metarchivos de Windows Media, ejemplo de código
- listas de reproducción, ejemplo de código
- listas de reproducción de metarchivos, ejemplo de código
- Listas de reproducción de metarchivos de Windows Media, ejemplo de lista de reproducción avanzada
- listas de reproducción, ejemplo de lista de reproducción avanzada
- listas de reproducción de metarchivos, ejemplo de lista de reproducción avanzada
- Media Player de Windows, ejemplos de lista de reproducción
- Windows Media Player, listas de reproducción de ejemplo
- Windows Media Player, listas de reproducción de ejemplo
- Windows Media Player, ejemplo de lista de reproducción avanzada
- ejemplos de listas de reproducción
- listas de reproducción de ejemplo
- listas de reproducción de ejemplo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f52251fedb13d41be5c94706bee4460c3f13c1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075512"
---
# <a name="an-advanced-playlist"></a><span data-ttu-id="10b99-125">Una lista de reproducción avanzada</span><span class="sxs-lookup"><span data-stu-id="10b99-125">An Advanced Playlist</span></span>

<span data-ttu-id="10b99-126">En el siguiente ejemplo de lista de reproducción se muestra cómo usar un conjunto más completo de elementos de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="10b99-126">The following playlist example shows how to use a more complete set of playlist elements.</span></span> <span data-ttu-id="10b99-127">Al escribir su propio código, tendrá que cambiar todas las direcciones URL y los nombres de archivo a nombres de archivo válidos a los que se pueda tener acceso desde el Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="10b99-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="10b99-128">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="10b99-128">Example Code</span></span>


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="10b99-129">En la tabla siguiente se describe la lista de reproducción avanzada anterior.</span><span class="sxs-lookup"><span data-stu-id="10b99-129">The following table describes the preceding advanced playlist.</span></span>



| <span data-ttu-id="10b99-130">Línea</span><span class="sxs-lookup"><span data-stu-id="10b99-130">Line</span></span>                                                                                            | <span data-ttu-id="10b99-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="10b99-131">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | <span data-ttu-id="10b99-132">El elemento [ASX](asx-element.md) identifica el cliente (Windows Media Player) que es una lista de reproducción de metarchivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="10b99-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="10b99-133">El atributo **version** especifica el número de versión de los elementos de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="10b99-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | <span data-ttu-id="10b99-134">El elemento [title](title-element--metafile.md) identifica el título de la lista de reproducción en su conjunto.</span><span class="sxs-lookup"><span data-stu-id="10b99-134">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="10b99-135">Windows Media Player muestra estos metadatos como el título de la muestra.</span><span class="sxs-lookup"><span data-stu-id="10b99-135">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | <span data-ttu-id="10b99-136">El elemento [abstracto](abstract-element.md) proporciona la información sobre herramientas para el título de presentación.</span><span class="sxs-lookup"><span data-stu-id="10b99-136">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the show title.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | <span data-ttu-id="10b99-137">El elemento [MOREINFO](moreinfo-element.md) vincula el título de la presentación a una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="10b99-137">The [MOREINFO](moreinfo-element.md) element links the show title to an URL.</span></span> <span data-ttu-id="10b99-138">Al pausar el puntero del mouse sobre el título Mostrar, se obtiene acceso a la información sobre herramientas, si se define.</span><span class="sxs-lookup"><span data-stu-id="10b99-138">Pausing the mouse pointer over the show title accesses the ToolTip, if defined.</span></span> <span data-ttu-id="10b99-139">Al seleccionar el título de la presentación, se abre la dirección URL designada.</span><span class="sxs-lookup"><span data-stu-id="10b99-139">Selecting the show title will then open the designated URL.</span></span>                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | <span data-ttu-id="10b99-140">El elemento [banner](banner-element.md) crea un Banner publicitario en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="10b99-140">The [BANNER](banner-element.md) element creates an advertising banner in Windows Media Player.</span></span> <span data-ttu-id="10b99-141">El atributo **href** especifica el gráfico de banner (que debe tener de 194 píxeles de ancho y 32 píxeles de alto).</span><span class="sxs-lookup"><span data-stu-id="10b99-141">The **HREF** attribute specifies the banner graphic (which must be 194 pixels wide by 32 pixels tall).</span></span>                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | <span data-ttu-id="10b99-142">El elemento [abstracto](abstract-element.md) proporciona la información sobre herramientas para el **banner**.</span><span class="sxs-lookup"><span data-stu-id="10b99-142">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the **BANNER**.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | <span data-ttu-id="10b99-143">El elemento [MOREINFO](moreinfo-element.md) vincula el gráfico de **banner** a una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="10b99-143">The [MOREINFO](moreinfo-element.md) element links the **BANNER** graphic to a URL.</span></span> <span data-ttu-id="10b99-144">Al mantener el puntero del mouse sobre el **banner** se accede a una información sobre herramientas, si se define.</span><span class="sxs-lookup"><span data-stu-id="10b99-144">Holding the mouse pointer over the **BANNER** accesses a ToolTip, if defined.</span></span> <span data-ttu-id="10b99-145">Al seleccionar el **banner** se abrirá la dirección URL designada.</span><span class="sxs-lookup"><span data-stu-id="10b99-145">Selecting the **BANNER** will open the designated URL.</span></span>                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | <span data-ttu-id="10b99-146">El elemento [param](param-element.md) define un parámetro personalizado.</span><span class="sxs-lookup"><span data-stu-id="10b99-146">The [PARAM](param-element.md) element defines a custom parameter.</span></span> <span data-ttu-id="10b99-147">El atributo **Name** define el nombre del parámetro personalizado como "Track".</span><span class="sxs-lookup"><span data-stu-id="10b99-147">The **name** attribute defines the name of the custom parameter as "track".</span></span> <span data-ttu-id="10b99-148">El atributo **Value** define el valor de "Track" para que sea "1".</span><span class="sxs-lookup"><span data-stu-id="10b99-148">The **value** attribute defines the value of "track" to be "1".</span></span>                                                                                                                          |
| `</BANNER>`                                                                                 | <span data-ttu-id="10b99-149">Cierra el elemento **banner**</span><span class="sxs-lookup"><span data-stu-id="10b99-149">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | <span data-ttu-id="10b99-150">Comienza el bloque de elementos de [entrada](entry-element.md) .</span><span class="sxs-lookup"><span data-stu-id="10b99-150">Begins the [ENTRY](entry-element.md) element block.</span></span> <span data-ttu-id="10b99-151">Este elemento define un clip en una lista de reproducción mediante la especificación de un vínculo en el elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="10b99-151">This element defines a clip in a playlist by specifying a link in the **REF** element.</span></span> <span data-ttu-id="10b99-152">Establecer **ClientSkip** en "no" significa que el usuario no puede avanzar o saltar rápidamente al siguiente clip</span><span class="sxs-lookup"><span data-stu-id="10b99-152">Setting **ClientSkip** to "no" means that the user cannot fast forward or jump to the next clip</span></span>                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | <span data-ttu-id="10b99-153">Crea un Banner publicitario.</span><span class="sxs-lookup"><span data-stu-id="10b99-153">Creates an advertising banner.</span></span> <span data-ttu-id="10b99-154">El **href** es el gráfico de banner (194x32 píxeles).</span><span class="sxs-lookup"><span data-stu-id="10b99-154">The **HREF** is the banner graphic (194x32 pixels).</span></span>                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | <span data-ttu-id="10b99-155">Proporciona la información sobre herramientas para el banner.</span><span class="sxs-lookup"><span data-stu-id="10b99-155">Provides the ToolTip for the banner.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="10b99-156">Proporciona un vínculo a la dirección URL del banner.</span><span class="sxs-lookup"><span data-stu-id="10b99-156">Provides a link to the URL for the banner.</span></span> <span data-ttu-id="10b99-157">Al seleccionar el banner se conecta a la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="10b99-157">Selecting the banner connects to the URL.</span></span>                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | <span data-ttu-id="10b99-158">Cierra el elemento **banner**</span><span class="sxs-lookup"><span data-stu-id="10b99-158">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="10b99-159">Proporciona un vínculo a la dirección URL del texto del **título** del clip.</span><span class="sxs-lookup"><span data-stu-id="10b99-159">Provides a link to the URL for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | <span data-ttu-id="10b99-160">Comentario.</span><span class="sxs-lookup"><span data-stu-id="10b99-160">A comment.</span></span> <span data-ttu-id="10b99-161">Los [comentarios](comments.md) solo están visibles cuando se ve el código.</span><span class="sxs-lookup"><span data-stu-id="10b99-161">[Comments](comments.md) are only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | <span data-ttu-id="10b99-162">Proporciona la información sobre herramientas para el texto del **título** del clip.</span><span class="sxs-lookup"><span data-stu-id="10b99-162">Provides the ToolTip for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | <span data-ttu-id="10b99-163">Identifica el título del clip.</span><span class="sxs-lookup"><span data-stu-id="10b99-163">Identifies the title of the clip.</span></span> <span data-ttu-id="10b99-164">Es el **título** del clip porque está anidado dentro de un elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="10b99-164">It is the clip **TITLE** because it is nested within an **ENTRY** element.</span></span> <span data-ttu-id="10b99-165">Windows Media Player muestra estos metadatos como el título del clip.</span><span class="sxs-lookup"><span data-stu-id="10b99-165">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | <span data-ttu-id="10b99-166">Identifica al autor del clip multimedia.</span><span class="sxs-lookup"><span data-stu-id="10b99-166">Identifies the author of the media clip.</span></span> <span data-ttu-id="10b99-167">Estos metadatos se muestran como el **autor** del clip mediante Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="10b99-167">This metadata is displayed as the clip **AUTHOR** by Windows Media Player.</span></span>                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | <span data-ttu-id="10b99-168">El elemento [Copyright](copyright-element.md) especifica los derechos de autor asociados con el clip multimedia.</span><span class="sxs-lookup"><span data-stu-id="10b99-168">The [COPYRIGHT](copyright-element.md) element specifies the copyrights associated with the media clip.</span></span> <span data-ttu-id="10b99-169">Windows Media Player muestra estos metadatos como el COPYRIGHT del clip.</span><span class="sxs-lookup"><span data-stu-id="10b99-169">Windows Media Player displays this metadata as the clip COPYRIGHT.</span></span>                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="10b99-170">Un comentario, en el mismo formato que los comentarios **XML** .</span><span class="sxs-lookup"><span data-stu-id="10b99-170">A comment, in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | <span data-ttu-id="10b99-171">Dirección URL para el contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="10b99-171">URL for the media content.</span></span> <span data-ttu-id="10b99-172">El elemento [ref](ref-element.md) identifica la línea como un puntero a contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="10b99-172">The [REF](ref-element.md) element identifies the line as a pointer to media content.</span></span> <span data-ttu-id="10b99-173">El atributo **href** es la dirección URL del archivo. Tenga en cuenta el uso del cierre de tipo XML del elemento "/>" en lugar de " &lt; /ref &gt; ".</span><span class="sxs-lookup"><span data-stu-id="10b99-173">The **HREF** attribute is the URL to the file.Note the use of the XML-like closing of the element , "/>" instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="10b99-174">Dado que este elemento no tiene elementos secundarios, se cierra a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="10b99-174">Because this element does not have child elements, it closes itself.</span></span><br/> |
| `</ENTRY>`                                                                                  | <span data-ttu-id="10b99-175">Especifica el final de del primer elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="10b99-175">Specifies the end of the of the first **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | <span data-ttu-id="10b99-176">Comienza el segundo elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="10b99-176">Begins the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | <span data-ttu-id="10b99-177">Identifica el título del segundo clip.</span><span class="sxs-lookup"><span data-stu-id="10b99-177">Identifies the title of the second clip.</span></span>                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | <span data-ttu-id="10b99-178">Identifica al autor del segundo clip multimedia.</span><span class="sxs-lookup"><span data-stu-id="10b99-178">Identifies the author of the second media clip.</span></span>                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | <span data-ttu-id="10b99-179">Comentario.</span><span class="sxs-lookup"><span data-stu-id="10b99-179">A comment.</span></span> <span data-ttu-id="10b99-180">Solo estará visible cuando se vea el código.</span><span class="sxs-lookup"><span data-stu-id="10b99-180">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | <span data-ttu-id="10b99-181">Este es el texto de la información sobre herramientas para el texto del **título** del clip.</span><span class="sxs-lookup"><span data-stu-id="10b99-181">This is the ToolTip text for the **TITLE** text of the clip.</span></span>                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="10b99-182">Comentario.</span><span class="sxs-lookup"><span data-stu-id="10b99-182">A comment.</span></span> <span data-ttu-id="10b99-183">Solo estará visible cuando se vea el código.</span><span class="sxs-lookup"><span data-stu-id="10b99-183">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | <span data-ttu-id="10b99-184">Identifica la línea como un puntero a contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="10b99-184">Identifies the line as a pointer to media content.</span></span> <span data-ttu-id="10b99-185">El atributo **href** es la dirección URL del archivo.</span><span class="sxs-lookup"><span data-stu-id="10b99-185">The **HREF** attribute is the URL to the file.</span></span>                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | <span data-ttu-id="10b99-186">Especifica el final del segundo elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="10b99-186">Specifies the end of the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | <span data-ttu-id="10b99-187">Especifica el final de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="10b99-187">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="10b99-188">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="10b99-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10b99-189">**Crear listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="10b99-189">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="10b99-190">**Listas de reproducción de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="10b99-190">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="10b99-191">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="10b99-191">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="10b99-192">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="10b99-192">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="10b99-193">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="10b99-193">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





