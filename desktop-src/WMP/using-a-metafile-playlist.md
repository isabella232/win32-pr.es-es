---
title: Usar una lista de reproducción de metarchivo
description: Usar una lista de reproducción de metarchivo
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Listas de reproducción de metarchivos de Windows Media, usar
- listas de reproducción de metarchivos, usar
- listas de reproducción, usar
- Listas de reproducción de metarchivos de Windows Media, acerca de
- listas de reproducción de metarchivos, acerca de
- listas de reproducción, acerca de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775385"
---
# <a name="using-a-metafile-playlist"></a><span data-ttu-id="8e57a-109">Usar una lista de reproducción de metarchivo</span><span class="sxs-lookup"><span data-stu-id="8e57a-109">Using a Metafile Playlist</span></span>

<span data-ttu-id="8e57a-110">Dado que no se puede vincular directamente desde una página web a un servidor multimedia de streaming, se usan listas de reproducción de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="8e57a-110">Because you cannot link directly from a webpage to a streaming media server, you use metafile playlists.</span></span> <span data-ttu-id="8e57a-111">Las listas de reproducción de metarchivos contienen la información que necesita Windows Media Player y se almacenan en un servidor Web.</span><span class="sxs-lookup"><span data-stu-id="8e57a-111">The metafile playlists contain the information needed by Windows Media Player and are stored on a web server.</span></span> <span data-ttu-id="8e57a-112">Después, puede vincular desde el documento Web a una lista de reproducción de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="8e57a-112">You can then link from the Web document to a metafile playlist.</span></span> <span data-ttu-id="8e57a-113">Cuando se abre una lista de reproducción de metarchivo, el control se transfiere a Windows Media Player, que procesa el archivo, se conecta al servidor de streaming multimedia y reproduce el contenido especificado.</span><span class="sxs-lookup"><span data-stu-id="8e57a-113">When a metafile playlist is opened, control transfers to Windows Media Player, which processes the file, connects to the streaming media server, and plays the specified content.</span></span>

<span data-ttu-id="8e57a-114">En primer lugar, el explorador descarga la lista de reproducción del metarchivo en el directorio de caché del usuario.</span><span class="sxs-lookup"><span data-stu-id="8e57a-114">The browser first downloads the metafile playlist to the user's cache directory.</span></span> <span data-ttu-id="8e57a-115">Dado que la lista de reproducción del metarchivo es pequeña, se trata de un paso muy rápido.</span><span class="sxs-lookup"><span data-stu-id="8e57a-115">Because the metafile playlist is small, this is a very quick step.</span></span> <span data-ttu-id="8e57a-116">A continuación, el equipo del usuario busca en su tabla asociaciones de archivo la Asociación de la lista de reproducción del metarchivo con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8e57a-116">The user's computer then finds in its file associations table the association of the metafile playlist with Windows Media Player.</span></span> <span data-ttu-id="8e57a-117">Windows Media Player abre e interpreta el scripting en la lista de reproducción de metarchivos, que contiene, entre otras cosas, la dirección URL del contenido de streaming.</span><span class="sxs-lookup"><span data-stu-id="8e57a-117">Windows Media Player opens and interprets the scripting in the metafile playlist, which contains, among other things, the URL of the streaming content.</span></span> <span data-ttu-id="8e57a-118">Windows Media Player usa la dirección URL para buscar el contenido e iniciar el flujo.</span><span class="sxs-lookup"><span data-stu-id="8e57a-118">Windows Media Player uses the URL to locate the content and initiate the stream.</span></span> <span data-ttu-id="8e57a-119">El scripting de lista de reproducción de metarchivo controla la experiencia de streaming.</span><span class="sxs-lookup"><span data-stu-id="8e57a-119">The metafile playlist scripting then controls the streaming experience.</span></span>

<span data-ttu-id="8e57a-120">Dado que las listas de reproducción de metarchivos funcionan a través de una aplicación auxiliar asociada con el tipo ASXMIME (Application/Mplayer2 o video/x-MS-ASF), son compatibles con cualquier explorador que admita aplicaciones auxiliares.</span><span class="sxs-lookup"><span data-stu-id="8e57a-120">Because metafile playlists work through a helper application associated with the ASXMIME type (application/mplayer2 or video/x-ms-asf), they are compatible with any browser that supports helper applications.</span></span> <span data-ttu-id="8e57a-121">Los ejemplos que se muestran en este documento funcionarán con Microsoft Internet Explorer 4,0 y versiones posteriores, y con Netscape Navigator 4,0 y versiones posteriores en las plataformas Microsoft Win32® y Apple Macintosh.</span><span class="sxs-lookup"><span data-stu-id="8e57a-121">The examples shown in this document will work with Microsoft Internet Explorer 4.0 and later, and with Netscape Navigator 4.0 and later on Microsoft Win32® and Apple Macintosh platforms.</span></span> <span data-ttu-id="8e57a-122">En todos los ejemplos, tendrá que asegurarse de que los archivos multimedia digitales a los que se hace referencia tienen rutas de acceso y nombres de archivo válidos para el entorno.</span><span class="sxs-lookup"><span data-stu-id="8e57a-122">In all examples, you will have to be sure that any digital media files referenced have valid paths and file names for your environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e57a-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e57a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e57a-124">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8e57a-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="8e57a-125">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8e57a-125">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="8e57a-126">**Información general de los metaarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8e57a-126">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




