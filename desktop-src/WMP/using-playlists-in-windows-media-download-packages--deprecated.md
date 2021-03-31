---
title: Usar listas de reproducción en paquetes de descarga de Windows Media (en desuso)
description: Usar listas de reproducción en paquetes de descarga de Windows Media (en desuso)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Metaarchivos de Windows Media, paquetes de descarga de Windows Media
- Windows Media Player, paquetes de descarga de Windows Media
- metaarchivos, paquetes de descarga de Windows Media
- Windows Media, paquetes de descarga de Windows Media
- listas de reproducción, paquetes de descarga de Windows Media
- listas de reproducción de metarchivos, paquetes de descarga de Windows Media
- Listas de reproducción de metarchivos de Windows Media, paquetes de descarga de Windows Media
- Paquetes de descarga de Windows Media, listas de reproducción
- Paquetes de descarga de Windows Media, listas de reproducción de metarchivos
- Paquetes de descarga de Windows Media, listas de reproducción de metarchivo de Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418960"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="e9d46-113">Usar listas de reproducción en paquetes de descarga de Windows Media (en desuso)</span><span class="sxs-lookup"><span data-stu-id="e9d46-113">Using Playlists in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="e9d46-114">En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e9d46-114">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="e9d46-115">Las listas de reproducción son metaarchivos de Windows Media con una extensión de nombre de archivo. ASX que proporcionan información que indica a Windows Media Player Cómo reproducir el contenido empaquetado.</span><span class="sxs-lookup"><span data-stu-id="e9d46-115">Playlists are Windows Media metafiles with an .asx file name extension that provide information that tells Windows Media Player how to play the packaged content.</span></span> <span data-ttu-id="e9d46-116">Mediante la combinación de varios archivos de contenido en un único paquete de descarga de Windows Media, puede controlar y personalizar el paquete de descarga de Windows Media mediante la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e9d46-116">By combining multiple content files into a single Windows Media Download package, you can control and customize your Windows Media Download package by using the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="e9d46-117">En general, los paquetes de descarga de Windows Media usan listas de reproducción de metarchivos para hacer referencia al contenido multimedia del paquete en lugar de a un flujo de un servidor en una intranet o en Internet.</span><span class="sxs-lookup"><span data-stu-id="e9d46-117">In general, metafile playlists are used by Windows Media Download packages to reference the multimedia content in the package rather than a stream from a server on an intranet or the Internet.</span></span> <span data-ttu-id="e9d46-118">Sin embargo, se admiten las referencias URL dentro del archivo. ASX.</span><span class="sxs-lookup"><span data-stu-id="e9d46-118">However, URL references within the .asx file are supported.</span></span>

 

<span data-ttu-id="e9d46-119">Con XML, el metarchivo proporciona la información que Windows Media Player usa para reproducir y mostrar el contenido.</span><span class="sxs-lookup"><span data-stu-id="e9d46-119">Using XML, the metafile provides the information Windows Media Player uses to play and display content.</span></span> <span data-ttu-id="e9d46-120">Las listas de reproducción se componen de varios elementos de código XML con sus etiquetas y atributos asociados.</span><span class="sxs-lookup"><span data-stu-id="e9d46-120">Playlists are made up of various XML code elements with their associated tags and attributes.</span></span> <span data-ttu-id="e9d46-121">Cada elemento de una lista de reproducción de metarchivo de Windows Media define una opción o acción determinada en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e9d46-121">Each element in a Windows Media metafile playlist defines a particular setting or action in Windows Media Player.</span></span>

<span data-ttu-id="e9d46-122">El equipo del usuario asocia un metarchivo de Windows Media que tiene una extensión de nombre de archivo. ASX con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e9d46-122">The user's computer associates a Windows Media metafile that has an .asx file name extension with Windows Media Player.</span></span> <span data-ttu-id="e9d46-123">Windows Media Player abre y analiza el código XML del metarchivo, que contiene la ruta de acceso para buscar los archivos de audio o vídeo empaquetados.</span><span class="sxs-lookup"><span data-stu-id="e9d46-123">Windows Media Player opens and parses the XML code in the metafile, which contains the path for locating the packaged audio or video files.</span></span> <span data-ttu-id="e9d46-124">A continuación, el script de metarchivo controla el audio, el vídeo y la experiencia gráfica.</span><span class="sxs-lookup"><span data-stu-id="e9d46-124">The metafile script then controls the audio, video, and graphical experience.</span></span> <span data-ttu-id="e9d46-125">El metarchivo también contiene información que Windows Media Player procesa y muestra en el cuadro desplegable lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e9d46-125">The metafile also contains information that Windows Media Player processes and displays in the playlist drop-down box.</span></span> <span data-ttu-id="e9d46-126">Inmediatamente después de que se muestre la lista, se reproducirá el primer elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="e9d46-126">Immediately after the list is displayed, the first item in the list is played.</span></span>

<span data-ttu-id="e9d46-127">Una lista de reproducción de metarchivo es un acceso directo a los archivos que contienen el contenido empaquetado.</span><span class="sxs-lookup"><span data-stu-id="e9d46-127">A metafile playlist is a shortcut to the files that contain your packaged content.</span></span> <span data-ttu-id="e9d46-128">El código siguiente es un ejemplo de un metarchivo que especifica el borde que se va a mostrar mediante el elemento **Skin** , dos canciones que se van a reproducir y la información de la lista de reproducción de cada canción.</span><span class="sxs-lookup"><span data-stu-id="e9d46-128">The following code is an example of a metafile that specifies the border to display by using the **SKIN** element, two songs to be played, and the playlist information for each song.</span></span>


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="e9d46-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9d46-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9d46-130">**Bordes de Media Player de Windows (desusado)**</span><span class="sxs-lookup"><span data-stu-id="e9d46-130">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="e9d46-131">**Paquetes de descarga de Windows Media (en desuso)**</span><span class="sxs-lookup"><span data-stu-id="e9d46-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="e9d46-132">**Metaarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e9d46-132">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




