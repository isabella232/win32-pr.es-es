---
title: Atributos de elemento multimedia
description: Atributos de elemento multimedia
ms.assetid: d43addec-e06c-4ef3-9012-3ecf589b105c
keywords:
- Windows Media Player, biblioteca
- Modelo de objetos de Windows Media Player, biblioteca
- modelo de objetos, biblioteca
- Windows Media Player Mobile, biblioteca para el modelo de objetos
- Control ActiveX de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX, biblioteca para el modelo de objetos
- Windows Media Player, atributos para elementos multimedia
- Modelo de objetos de Windows Media Player, atributos para elementos multimedia
- modelo de objetos, atributos para elementos multimedia
- Windows Media Player Mobile, atributos para elementos multimedia
- Control ActiveX de Windows Media Player, atributos para elementos multimedia
- Control ActiveX móvil de Windows Media Player, atributos para elementos multimedia
- Control ActiveX, atributos para elementos multimedia
- Biblioteca de Media Player de Windows, atributos para elementos multimedia
- Biblioteca, atributos para elementos multimedia
- atributos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ac8595cc07504c9cd3e195431513a1f8565e87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075688"
---
# <a name="media-item-attributes"></a><span data-ttu-id="36933-120">Atributos de elemento multimedia</span><span class="sxs-lookup"><span data-stu-id="36933-120">Media Item Attributes</span></span>

<span data-ttu-id="36933-121">Cuando examine la biblioteca en Media Player de Windows, normalmente verá una gran cantidad de información sobre un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="36933-121">When you look at the library in Windows Media Player, you typically see a great deal of information about a media item.</span></span> <span data-ttu-id="36933-122">Además del nombre de una pista de audio, por ejemplo, es probable que vea el nombre del álbum en el que se encuentra la pista, los nombres del intérprete y el compositor, el género de la música, etc.</span><span class="sxs-lookup"><span data-stu-id="36933-122">In addition to the name of an audio track, for example, you will likely see the name of the album the track is on, the names of the artist and composer, the genre of the music, and so on.</span></span>

<span data-ttu-id="36933-123">En el modelo de objetos de Windows Media Player, estos elementos de metadatos se denominan atributos.</span><span class="sxs-lookup"><span data-stu-id="36933-123">In the Windows Media Player object model, these metadata items are called attributes.</span></span> <span data-ttu-id="36933-124">El modelo de objetos de incluye propiedades y métodos que se pueden usar para consultar elementos multimedia y listas de reproducción de atributos.</span><span class="sxs-lookup"><span data-stu-id="36933-124">The object model includes properties and methods you can use to query media items and playlists for attributes.</span></span> <span data-ttu-id="36933-125">Después, puede mostrar los valores de atributo en la interfaz de usuario o el código puede realizar acciones en función del valor de un atributo.</span><span class="sxs-lookup"><span data-stu-id="36933-125">You can then display attribute values in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="36933-126">En los temas siguientes se describe cómo trabajar con atributos de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="36933-126">The following topics describe working with media item attributes.</span></span>



| <span data-ttu-id="36933-127">Tema</span><span class="sxs-lookup"><span data-stu-id="36933-127">Topic</span></span>                                                                                      | <span data-ttu-id="36933-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="36933-128">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36933-129">Descripción de los orígenes de atributos</span><span class="sxs-lookup"><span data-stu-id="36933-129">Understanding Attribute Sources</span></span>](understanding-attribute-sources.md)                     | <span data-ttu-id="36933-130">Describe cómo afecta el origen de un elemento multimedia a los atributos que se pueden asociar a él.</span><span class="sxs-lookup"><span data-stu-id="36933-130">Describes how the source of a media item affects the attributes that may be associated with it.</span></span> |
| [<span data-ttu-id="36933-131">Leer valores de atributo</span><span class="sxs-lookup"><span data-stu-id="36933-131">Reading Attribute Values</span></span>](reading-attribute-values.md)                                   | <span data-ttu-id="36933-132">Muestra los métodos para recuperar el valor de un atributo.</span><span class="sxs-lookup"><span data-stu-id="36933-132">Shows the methods for retrieving the value of an attribute.</span></span>                                     |
| [<span data-ttu-id="36933-133">Atributos con varios valores</span><span class="sxs-lookup"><span data-stu-id="36933-133">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md)                     | <span data-ttu-id="36933-134">Muestra los métodos para recuperar el valor de un atributo con varios valores.</span><span class="sxs-lookup"><span data-stu-id="36933-134">Shows the methods for retrieving the value of a multi-valued attribute.</span></span>                         |
| [<span data-ttu-id="36933-135">Leer valores de atributo de un CD o DVD</span><span class="sxs-lookup"><span data-stu-id="36933-135">Reading Attribute Values from a CD or DVD</span></span>](reading-attribute-values-from-a-cd-or-dvd.md) | <span data-ttu-id="36933-136">Proporciona una aplicación de ejemplo que Lee todos los atributos de un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="36933-136">Provides a sample application that reads all of the attributes of a media item.</span></span>                 |
| [<span data-ttu-id="36933-137">Cambiar valores de atributo</span><span class="sxs-lookup"><span data-stu-id="36933-137">Changing Attribute Values</span></span>](changing-attribute-values.md)                                 | <span data-ttu-id="36933-138">Muestra el método para cambiar el valor de un atributo.</span><span class="sxs-lookup"><span data-stu-id="36933-138">Shows the method for changing the value of an attribute.</span></span>                                        |
| [<span data-ttu-id="36933-139">Valores de atributo para el contenido de TV</span><span class="sxs-lookup"><span data-stu-id="36933-139">Attribute Values for TV Content</span></span>](attribute-values-for-tv-content.md)                     | <span data-ttu-id="36933-140">Muestra cómo especificar los atributos para el contenido de vídeo digital que contiene programas de TV.</span><span class="sxs-lookup"><span data-stu-id="36933-140">Shows how to specify attributes for digital video content that contains TV shows.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="36933-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36933-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36933-142">**Atributos de lista de reproducción**</span><span class="sxs-lookup"><span data-stu-id="36933-142">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> <dt>

[<span data-ttu-id="36933-143">**Trabajar con la biblioteca**</span><span class="sxs-lookup"><span data-stu-id="36933-143">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




