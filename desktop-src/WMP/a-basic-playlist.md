---
title: Una lista de reproducción básica
description: Una lista de reproducción básica
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
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
- Listas de reproducción de metarchivos de Windows Media, ejemplo de lista de reproducción básica
- listas de reproducción, ejemplo básico de lista de reproducción
- listas de reproducción de metarchivos, ejemplo básico de lista de reproducción
- Media Player de Windows, ejemplos de lista de reproducción
- Windows Media Player, listas de reproducción de ejemplo
- Windows Media Player, listas de reproducción de ejemplo
- Windows Media Player, ejemplo básico de lista de reproducción
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
ms.openlocfilehash: 804bc69c9ab3b243030cd2c87545e6362ccfca79
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314788"
---
# <a name="a-basic-playlist"></a><span data-ttu-id="a1b60-125">Una lista de reproducción básica</span><span class="sxs-lookup"><span data-stu-id="a1b60-125">A Basic Playlist</span></span>

<span data-ttu-id="a1b60-126">En el siguiente ejemplo de lista de reproducción se muestra un conjunto básico de elementos de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a1b60-126">The following playlist example shows a basic set of playlist elements.</span></span> <span data-ttu-id="a1b60-127">Al escribir su propio código, tendrá que cambiar todas las direcciones URL y los nombres de archivo a nombres de archivo válidos a los que se pueda tener acceso desde el Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="a1b60-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="a1b60-128">**Ejemplo de código**</span><span class="sxs-lookup"><span data-stu-id="a1b60-128">**Code Example**</span></span>


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="a1b60-129">En la tabla siguiente se proporcionan detalles sobre el uso de cada elemento en el código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a1b60-129">The following table provides details on the use of each element in the example code.</span></span>



| <span data-ttu-id="a1b60-130">Línea</span><span class="sxs-lookup"><span data-stu-id="a1b60-130">Line</span></span>                                                                                            | <span data-ttu-id="a1b60-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1b60-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | <span data-ttu-id="a1b60-132">El elemento [ASX](asx-element.md) identifica el cliente (Windows Media Player) que es una lista de reproducción de metarchivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a1b60-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="a1b60-133">El atributo **version** especifica el número de versión de los elementos de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="a1b60-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a1b60-134">\<TITLE>Demostración básica de listas de reproducción\</TITLE></span><span class="sxs-lookup"><span data-stu-id="a1b60-134">\<TITLE>Basic Playlist Demo\</TITLE></span></span>                                                  | <span data-ttu-id="a1b60-135">El elemento [title](title-element--metafile.md) identifica el título de la lista de reproducción en su conjunto.</span><span class="sxs-lookup"><span data-stu-id="a1b60-135">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="a1b60-136">Windows Media Player muestra estos metadatos como el título de la muestra.</span><span class="sxs-lookup"><span data-stu-id="a1b60-136">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | <span data-ttu-id="a1b60-137">Comienza el elemento de [entrada](entry-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a1b60-137">Begins the [ENTRY](entry-element.md) element.</span></span> <span data-ttu-id="a1b60-138">Un elemento de **entrada** es una manera de definir un clip determinado en una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a1b60-138">An **ENTRY** element is a way to define a particular clip in a playlist</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a1b60-139">\<TITLE>Una entrada en una lista de reproducción básica\</TITLE></span><span class="sxs-lookup"><span data-stu-id="a1b60-139">\<TITLE>An Entry in a basic playlist\</TITLE></span></span>                                         | <span data-ttu-id="a1b60-140">Identifica el título del clip de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a1b60-140">Identifies the title of the playlist clip .</span></span> <span data-ttu-id="a1b60-141">Es diferente del elemento de **título** anterior porque este está anidado dentro de un elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="a1b60-141">It is different than the previous **TITLE** element because this one is nested within an **ENTRY** element.</span></span> <span data-ttu-id="a1b60-142">Windows Media Player muestra estos metadatos como el título del clip.</span><span class="sxs-lookup"><span data-stu-id="a1b60-142">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a1b60-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span><span class="sxs-lookup"><span data-stu-id="a1b60-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span></span>                                              | <span data-ttu-id="a1b60-144">El elemento [Author](author-element.md) identifica el autor del clip multimedia.</span><span class="sxs-lookup"><span data-stu-id="a1b60-144">The [AUTHOR](author-element.md) element identifies the author of the media clip .</span></span> <span data-ttu-id="a1b60-145">Windows Media Player muestra estos metadatos como **autor** del clip.</span><span class="sxs-lookup"><span data-stu-id="a1b60-145">Windows Media Player displays this metadata as the clip **AUTHOR**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | <span data-ttu-id="a1b60-146">Comentario.</span><span class="sxs-lookup"><span data-stu-id="a1b60-146">A comment.</span></span> <span data-ttu-id="a1b60-147">Los [comentarios](comments.md) solo están visibles cuando se ve el código y tienen el mismo formato que los comentarios **XML** .</span><span class="sxs-lookup"><span data-stu-id="a1b60-147">[Comments](comments.md) are visible only when the code is viewed, and are in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | <span data-ttu-id="a1b60-148">Puntero real al archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="a1b60-148">Actual pointer to the media file.</span></span> <span data-ttu-id="a1b60-149">El elemento [ref](ref-element.md) identifica la línea como un puntero a contenido multimedia, mientras que el atributo **href** es la dirección URL del archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="a1b60-149">The [REF](ref-element.md) element identifies the line as a pointer to media content, while the **HREF** attribute is the URL to the media file.</span></span> <span data-ttu-id="a1b60-150">En este caso, la dirección URL usa el protocolo MMS, por lo que apunta a un servidor de Windows Media. Los archivos multimedia del servidor multimedia normalmente no se mantienen en la misma ubicación que los documentos HTML.</span><span class="sxs-lookup"><span data-stu-id="a1b60-150">In this case, the URL uses the MMS protocol, so it points to a Windows Media server.Media files on your media server are not usually kept in the same location as your HTML documents.</span></span><br/> <span data-ttu-id="a1b60-151">Observe el uso del cierre de tipo XML del elemento, "/>", en lugar de " &lt; /ref &gt; ".</span><span class="sxs-lookup"><span data-stu-id="a1b60-151">Note the use of the XML-like closing of the element , "/>", instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="a1b60-152">Dado que este elemento no tiene elementos secundarios, se cierra a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="a1b60-152">Because this element does not have child elements, it closes itself.</span></span><br/> |
| \</ENTRY>                                                                                  | <span data-ttu-id="a1b60-153">Especifica el final del elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="a1b60-153">Specifies the end of the **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | <span data-ttu-id="a1b60-154">Especifica el final de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a1b60-154">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="a1b60-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1b60-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1b60-156">**Crear listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="a1b60-156">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="a1b60-157">**Listas de reproducción de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="a1b60-157">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="a1b60-158">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="a1b60-158">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="a1b60-159">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a1b60-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="a1b60-160">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a1b60-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





