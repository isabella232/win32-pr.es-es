---
title: Usar anuncios
description: Usar anuncios
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Listas de reproducción de metarchivos de Windows Media, anuncios
- listas de reproducción, anuncios
- listas de reproducción de metarchivos, anuncios
- Media Player de Windows, anuncios
- anuncios
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704625"
---
# <a name="using-announcements"></a><span data-ttu-id="ff995-108">Usar anuncios</span><span class="sxs-lookup"><span data-stu-id="ff995-108">Using Announcements</span></span>

<span data-ttu-id="ff995-109">Un anuncio es un archivo que contiene información sobre la dirección URL de una secuencia multimedia, incluida la dirección IP de multidifusión, el puerto, el formato de secuencia y otras configuraciones de la estación.</span><span class="sxs-lookup"><span data-stu-id="ff995-109">An announcement is a file that contains information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> <span data-ttu-id="ff995-110">Los anuncios los crea el administrador de Windows Media cuando se crea una secuencia de publicación de unidifusión o multidifusión.</span><span class="sxs-lookup"><span data-stu-id="ff995-110">Announcements are created by Windows Media Administrator when a unicast or multicast publishing stream is created.</span></span> <span data-ttu-id="ff995-111">El cliente puede cargar rápidamente el archivo de anuncio y, después, continuar para acceder al archivo multimedia de streaming.</span><span class="sxs-lookup"><span data-stu-id="ff995-111">The client can quickly load the announcement file, then proceed to access the streaming media file.</span></span>

<span data-ttu-id="ff995-112">En el caso de un punto de publicación de unidifusión, se abre la secuencia de medios del punto de publicación.</span><span class="sxs-lookup"><span data-stu-id="ff995-112">For a unicast publishing point, the publishing point media stream is opened.</span></span> <span data-ttu-id="ff995-113">En el caso de un punto de publicación de multidifusión, se extrae la dirección URL de un archivo de la estación de difusión con una extensión. NSC y se tiene acceso a los medios de streaming.</span><span class="sxs-lookup"><span data-stu-id="ff995-113">For a multicast publishing point, the URL is extracted from a broadcast station file with an .nsc extension, and the streaming media is accessed.</span></span> <span data-ttu-id="ff995-114">A diferencia de una secuencia de unidifusión, no hay información de encabezado en una secuencia de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="ff995-114">Unlike a unicast stream, no header information is contained in a multicast stream.</span></span> <span data-ttu-id="ff995-115">Esa información procede del archivo de la estación de difusión con una extensión. NSC.</span><span class="sxs-lookup"><span data-stu-id="ff995-115">That information comes from the broadcast station file with an .nsc extension.</span></span> <span data-ttu-id="ff995-116">Windows Media Player suele abrir primero un archivo de anuncio, que es un uso para listas de reproducción de metarchivos, que apunta a la ubicación del archivo de la estación de difusión.</span><span class="sxs-lookup"><span data-stu-id="ff995-116">Windows Media Player usually first opens an announcement file, which is one use for metafile playlists, that points to the location of the broadcast station file.</span></span>

<span data-ttu-id="ff995-117">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff995-117">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="ff995-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff995-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff995-119">**Crear listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="ff995-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="ff995-120">**Usar listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="ff995-120">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




