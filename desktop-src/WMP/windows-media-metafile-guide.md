---
title: Guía de metarchivo de Windows Media
description: Guía de metarchivo de Windows Media
ms.assetid: d2360a63-f073-44b0-8637-1f22b577f51a
keywords:
- Metaarchivos de Windows Media, acerca de
- Media Player de Windows, metaarchivos
- Windows Media Player, metaarchivos de Windows Media
- metaarchivos, acerca de
- Windows Media, metaarchivos
- Listas de reproducción de metarchivos de Windows Media, acerca de
- listas de reproducción, acerca de
- listas de reproducción de metarchivos, acerca de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fcf0a4c98ae49d1cdf3b7e36e8a278f184cd4632
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994538"
---
# <a name="windows-media-metafile-guide"></a><span data-ttu-id="d2b19-111">Guía de metarchivo de Windows Media</span><span class="sxs-lookup"><span data-stu-id="d2b19-111">Windows Media Metafile Guide</span></span>

<span data-ttu-id="d2b19-112">Un metarchivo de Windows Media puede ser tan simple o complejo como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d2b19-112">A Windows Media metafile can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="d2b19-113">El metarchivo de Windows Media más básico solo contiene el localizador uniforme de recursos (URL) de algún contenido multimedia en un servidor.</span><span class="sxs-lookup"><span data-stu-id="d2b19-113">The most basic Windows Media metafile contains only the Uniform Resource Locator (URL) of some multimedia content on a server.</span></span> <span data-ttu-id="d2b19-114">El cliente, Windows Media Player, analiza esta información y, a continuación, abre el archivo multimedia o el flujo definido en el metarchivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d2b19-114">The client, Windows Media Player, parses this information and then opens the media file or stream defined in the Windows Media metafile.</span></span> <span data-ttu-id="d2b19-115">Un metarchivo complejo puede contener varios archivos o secuencias organizados en una lista de reproducción, instrucciones sobre cómo reproducir los archivos o secuencias, texto y elementos gráficos como el título, el autor y el texto de copyright, la inserción personalizada de anuncios en una secuencia en directo, los hipervínculos asociados a los elementos de la interfaz de Media Player de Windows, etc.</span><span class="sxs-lookup"><span data-stu-id="d2b19-115">A complex metafile can contain multiple files or streams arranged in a playlist, instructions on how to play the files or streams, text and graphic elements such as title, author, and copyright text, personalized ad insertion into a live stream, hyperlinks associated with elements on the Windows Media Player interface, and more.</span></span>

<span data-ttu-id="d2b19-116">En las secciones siguientes se proporciona información detallada sobre cómo crear y usar listas de reproducción de metarchivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d2b19-116">The following sections provide detailed information on how to create and use Windows Media metafile playlists.</span></span>



| <span data-ttu-id="d2b19-117">Sección</span><span class="sxs-lookup"><span data-stu-id="d2b19-117">Section</span></span>                                                            | <span data-ttu-id="d2b19-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2b19-118">Description</span></span>                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2b19-119">Tipos de listas de reproducción</span><span class="sxs-lookup"><span data-stu-id="d2b19-119">Types of Playlists</span></span>](types-of-playlists.md)                       | <span data-ttu-id="d2b19-120">Enumera las extensiones de nombre de archivo disponibles.</span><span class="sxs-lookup"><span data-stu-id="d2b19-120">Lists available file name extensions.</span></span>                                               |
| [<span data-ttu-id="d2b19-121">Crear listas de reproducción de metarchivo</span><span class="sxs-lookup"><span data-stu-id="d2b19-121">Creating Metafile Playlists</span></span>](creating-metafile-playlists.md)     | <span data-ttu-id="d2b19-122">Describe cómo crear listas de reproducción de metarchivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d2b19-122">Describes how to create Windows Media metafile playlists.</span></span>                           |
| [<span data-ttu-id="d2b19-123">Listas de reproducción de metarchivos</span><span class="sxs-lookup"><span data-stu-id="d2b19-123">Metafile Playlists</span></span>](metafile-playlists.md)                       | <span data-ttu-id="d2b19-124">Describe el uso, el script, los metadatos y el procesamiento de la lista de reproducción de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="d2b19-124">Describes metafile playlist usage, scripting, metadata, and processing.</span></span>             |
| [<span data-ttu-id="d2b19-125">Instrucciones de extensión de metarchivo</span><span class="sxs-lookup"><span data-stu-id="d2b19-125">Metafile Extension Guidelines</span></span>](metafile-extension-guidelines.md) | <span data-ttu-id="d2b19-126">Describe el uso preferido de las extensiones de nombre de archivo para la transmisión por secuencias de archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="d2b19-126">Describes the preferred use of file name extensions for streaming media files.</span></span>      |
| [<span data-ttu-id="d2b19-127">Orden de prioridad</span><span class="sxs-lookup"><span data-stu-id="d2b19-127">Order of Precedence</span></span>](order-of-precedence.md)                     | <span data-ttu-id="d2b19-128">Describe cómo los elementos de lista de reproducción de metarchivo invalidan otros elementos de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d2b19-128">Describes how metafile playlist elements override other metafile playlist elements.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d2b19-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d2b19-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2b19-130">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d2b19-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="d2b19-131">**Metaarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d2b19-131">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




