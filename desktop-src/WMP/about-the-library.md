---
title: Acerca de la biblioteca
description: Acerca de la biblioteca
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows Media Player, biblioteca
- Modelo de objetos de Windows Media Player, biblioteca
- modelo de objetos, biblioteca
- Control ActiveX de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX, biblioteca para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, biblioteca para el modelo de objetos
- Windows Media Player Mobile, biblioteca para el modelo de objetos
- Biblioteca de Media Player de Windows, acerca de
- Biblioteca, acerca de
- metadatos, biblioteca de Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1781329a78bcb2e9cb25c45135e03465b9d63df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695232"
---
# <a name="about-the-library"></a><span data-ttu-id="b8324-113">Acerca de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8324-113">About the Library</span></span>

<span data-ttu-id="b8324-114">La biblioteca es una base de datos de información, o *metadatos*, sobre el contenido multimedia digital que está disponible para Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b8324-114">The library is a database of information, or *metadata*, about the digital media content that is available to Windows Media Player.</span></span> <span data-ttu-id="b8324-115">Parte de la información se muestra en el panel **biblioteca** del reproductor; hay más disponible a través del código.</span><span class="sxs-lookup"><span data-stu-id="b8324-115">Some of the information is displayed in the **Library** pane in the Player; more of it is available through code.</span></span>

<span data-ttu-id="b8324-116">(En Windows Media Player serie 9 y versiones anteriores, esta característica se denomina **biblioteca multimedia**).</span><span class="sxs-lookup"><span data-stu-id="b8324-116">(In Windows Media Player 9 Series and earlier, this feature is called **Media Library**.)</span></span>

<span data-ttu-id="b8324-117">La biblioteca ofrece a los usuarios una forma sencilla de organizar y acceder al contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="b8324-117">The library gives users an easy way to organize and access digital media content.</span></span> <span data-ttu-id="b8324-118">Por ejemplo, los usuarios pueden ver música organizada por álbum, por intérprete, por género o simplemente como una lista de toda la música.</span><span class="sxs-lookup"><span data-stu-id="b8324-118">For example, users can view music organized by album, by artist, by genre, or simply as a list of all music.</span></span> <span data-ttu-id="b8324-119">Puede usar el modelo de objetos del SDK de Windows Media Player para tener acceso a la biblioteca para reproducir contenido, recuperar listas de reproducción, agregar contenido, quitar contenido y cambiar los metadatos asociados.</span><span class="sxs-lookup"><span data-stu-id="b8324-119">You can use the Windows Media Player SDK object model to access the library to play content, retrieve playlists, add content, remove content, and change the associated metadata.</span></span> <span data-ttu-id="b8324-120">Windows Media Player protege la privacidad de los usuarios al restringir la capacidad de obtener acceso a la biblioteca desde el código bajo ciertas condiciones.</span><span class="sxs-lookup"><span data-stu-id="b8324-120">Windows Media Player protects users' privacy by restricting your ability to access the library from code under certain conditions.</span></span> <span data-ttu-id="b8324-121">Para obtener más información sobre los derechos de acceso, consulte [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b8324-121">For more information about access rights, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b8324-122">La biblioteca almacena metadatos acerca de dos tipos básicos de contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="b8324-122">The library stores metadata about two basic types of digital media content.</span></span> <span data-ttu-id="b8324-123">El primer tipo, los elementos multimedia digitales, son archivos de contenido individuales, como una pista de música o una fotografía.</span><span class="sxs-lookup"><span data-stu-id="b8324-123">The first type, digital media items, are individual content files, such as a music track or a photo.</span></span> <span data-ttu-id="b8324-124">El segundo tipo, las listas de reproducción, son archivos que representan un grupo de elementos multimedia digitales, que normalmente se prevé que se reproduzcan en un orden especificado.</span><span class="sxs-lookup"><span data-stu-id="b8324-124">The second type, playlists, are files that represent a group of digital media items, typically intended to be played in a specified order.</span></span> <span data-ttu-id="b8324-125">Los metadatos asociados con el contenido multimedia digital se almacenan como pares de nombre y valor.</span><span class="sxs-lookup"><span data-stu-id="b8324-125">The metadata associated with digital media content is stored as name-value pairs.</span></span> <span data-ttu-id="b8324-126">Por ejemplo, los metadatos que describen a la persona que realizó una canción se denominan "intérprete" y el valor asociado a él normalmente es una cadena de texto que contiene el nombre del remitente.</span><span class="sxs-lookup"><span data-stu-id="b8324-126">For example, the metadata that describes the person who performed a song is named "Artist" and the value associated with it typically is a text string containing the performer's name.</span></span> <span data-ttu-id="b8324-127">Cada nombre de metadatos único se denomina *atributo*.</span><span class="sxs-lookup"><span data-stu-id="b8324-127">Each unique metadata name is called an *attribute*.</span></span> <span data-ttu-id="b8324-128">Para obtener una lista de atributos admitidos, vea la [referencia de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b8324-128">For a listing of supported attributes, see the [Attribute Reference](attribute-reference.md).</span></span> <span data-ttu-id="b8324-129">Para obtener información sobre el uso de atributos en el código, vea [atributos de elemento multimedia](media-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b8324-129">For information about using attributes in code, see [Media Item Attributes](media-item-attributes.md).</span></span>

<span data-ttu-id="b8324-130">En las secciones siguientes se proporciona más información sobre cómo trabajar con la biblioteca:</span><span class="sxs-lookup"><span data-stu-id="b8324-130">The following sections provide more information about working with the library:</span></span>

-   [<span data-ttu-id="b8324-131">Obtener acceso a la biblioteca mediante programación</span><span class="sxs-lookup"><span data-stu-id="b8324-131">Accessing the Library Programmatically</span></span>](accessing-the-library-programmatically.md)
-   [<span data-ttu-id="b8324-132">Acerca de los servicios de biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8324-132">About Library Services</span></span>](about-library-services.md)

## <a name="related-topics"></a><span data-ttu-id="b8324-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8324-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8324-134">**Acerca del modelo de objetos de Player**</span><span class="sxs-lookup"><span data-stu-id="b8324-134">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




