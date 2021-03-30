---
title: Cómo funcionan los paquetes de descarga de Windows Media (en desuso)
description: Cómo funcionan los paquetes de descarga de Windows Media (en desuso)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Metaarchivos de Windows Media, paquetes de descarga de Windows Media
- Windows Media Player, paquetes de descarga de Windows Media
- metaarchivos, paquetes de descarga de Windows Media
- Windows Media, paquetes de descarga de Windows Media
- Paquetes de descarga de Windows Media, acerca de
- Paquetes de descarga de Windows Media, cómo funcionan los paquetes
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148792"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a><span data-ttu-id="b3297-109">Cómo funcionan los paquetes de descarga de Windows Media (en desuso)</span><span class="sxs-lookup"><span data-stu-id="b3297-109">How Windows Media Download Packages Work (deprecated)</span></span>

<span data-ttu-id="b3297-110">En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b3297-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="b3297-111">Un paquete de descarga de Windows Media se inicia desde un sitio web cuando un usuario hace clic en un vínculo en un explorador Web, como Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b3297-111">A Windows Media Download package is launched from a website when a user clicks a link in a Web browser, such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="b3297-112">Esta acción abre Windows Media Player y, a continuación, descarga y desempaqueta el paquete de descarga de Windows Media en el disco duro del usuario en una carpeta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b3297-112">This action opens Windows Media Player and then downloads and un-packages the Windows Media Download package on the user's hard disk in a default folder.</span></span>

<span data-ttu-id="b3297-113">Una vez extraídos los archivos del paquete de descarga de Windows Media, Windows Media Player busca una lista de reproducción de metarchivo de Windows Media con una extensión de nombre de archivo. ASX entre los archivos empaquetados.</span><span class="sxs-lookup"><span data-stu-id="b3297-113">Once the files have been extracted from the Windows Media Download package, Windows Media Player locates a Windows Media metafile playlist with an .asx file name extension among the packaged files.</span></span> <span data-ttu-id="b3297-114">Si encuentra uno, el reproductor crea una lista de reproducción basada en el metarchivo incluido.</span><span class="sxs-lookup"><span data-stu-id="b3297-114">If it finds one, the Player creates a playlist based on the included metafile.</span></span> <span data-ttu-id="b3297-115">Los archivos que contienen contenido multimedia se agregan a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b3297-115">Files that contain multimedia content are then added to the library.</span></span>

<span data-ttu-id="b3297-116">Windows Media Player también busca un elemento de **máscara** en el metarchivo.</span><span class="sxs-lookup"><span data-stu-id="b3297-116">Windows Media Player also looks for a **SKIN** element in the metafile.</span></span> <span data-ttu-id="b3297-117">Si el elemento **Skin** contiene una referencia a un archivo de borde con la extensión de nombre de archivo. WMZ, el reproductor carga el borde en el panel **reproducción en curso** .</span><span class="sxs-lookup"><span data-stu-id="b3297-117">If the **SKIN** element contains a reference to a border file with a .wmz file name extension, the Player loads the border into the **Now Playing** pane.</span></span> <span data-ttu-id="b3297-118">A continuación, el reproductor comienza a reproducir el contenido proporcionado en el paquete.</span><span class="sxs-lookup"><span data-stu-id="b3297-118">The Player then starts to play the content provided in the package.</span></span>

<span data-ttu-id="b3297-119">En el diagrama siguiente se muestra cómo se empaqueta el contenido en un archivo de descarga de Windows Media, se envía a un sitio web, se descarga y se reproduce en un equipo cliente mediante Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b3297-119">The following diagram shows how content is packaged in a Windows Media Download file, posted to a website, downloaded, and played on a client computer using Windows Media Player.</span></span>

![Cómo se obtiene y se reproduce un archivo de descarga de Windows Media.](images/wmd-image.png) <span data-ttu-id="b3297-121">Descarga de Windows Media</span><span class="sxs-lookup"><span data-stu-id="b3297-121">Windows Media Download</span></span>

<span data-ttu-id="b3297-122">En la tabla siguiente se describen los tres elementos que componen un paquete de descarga de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b3297-122">The following table describes the three elements that make up a Windows Media Download package.</span></span>



| <span data-ttu-id="b3297-123">Elemento Package</span><span class="sxs-lookup"><span data-stu-id="b3297-123">Package element</span></span>    | <span data-ttu-id="b3297-124">Función</span><span class="sxs-lookup"><span data-stu-id="b3297-124">Function</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="b3297-125">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="b3297-125">File name extensions</span></span>                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="b3297-126">Borde</span><span class="sxs-lookup"><span data-stu-id="b3297-126">Border</span></span>             | <span data-ttu-id="b3297-127">Una interfaz de usuario fija y personalizada creada por el propietario del contenido para mostrar, vincular y reproducir todos los medios empaquetados en el paquete de descarga de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b3297-127">A fixed, customized user interface created by the content owner for displaying, linking, and playing all media packaged in the Windows Media Download package.</span></span> <span data-ttu-id="b3297-128">Las técnicas utilizadas para crear bordes son similares a las que se usan para crear máscaras.</span><span class="sxs-lookup"><span data-stu-id="b3297-128">The techniques used to create borders are similar to those used to create skins.</span></span> | <span data-ttu-id="b3297-129">.wmz</span><span class="sxs-lookup"><span data-stu-id="b3297-129">.wmz</span></span>                                     |
| <span data-ttu-id="b3297-130">Lista de reproducción de metarchivo</span><span class="sxs-lookup"><span data-stu-id="b3297-130">Metafile Playlist</span></span>  | <span data-ttu-id="b3297-131">Metarchivo de Windows Media que contiene elementos de **entrada** , información de lista de reproducción y una identidad de elemento de **máscara** para los archivos de contenido.</span><span class="sxs-lookup"><span data-stu-id="b3297-131">A Windows Media metafile that contains **ENTRY** elements, playlist information, and a **SKIN** element identity for content files.</span></span>                                                                                                             | <span data-ttu-id="b3297-132">.asx</span><span class="sxs-lookup"><span data-stu-id="b3297-132">.asx</span></span>                                     |
| <span data-ttu-id="b3297-133">Contenido multimedia</span><span class="sxs-lookup"><span data-stu-id="b3297-133">Multimedia Content</span></span> | <span data-ttu-id="b3297-134">Archivo que contiene cualquier formato de audio o vídeo compatible con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b3297-134">A file containing any audio or video format that is supported by Windows Media Player.</span></span>                                                                                                                                                          | <span data-ttu-id="b3297-135">. WMA,. wmv,. ASF,. wav,. avi,. mpg,. mp3</span><span class="sxs-lookup"><span data-stu-id="b3297-135">.wma, .wmv, .asf, .wav, .avi, .mpg, .mp3</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b3297-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3297-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3297-137">**Paquetes de descarga de Windows Media (en desuso)**</span><span class="sxs-lookup"><span data-stu-id="b3297-137">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




