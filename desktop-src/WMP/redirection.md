---
title: Redireccionamiento
description: Redireccionamiento
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Listas de reproducción de metarchivos de Windows Media, redirección
- listas de reproducción, redirección
- listas de reproducción de metarchivo, redirección
- Media Player de Windows, redirección
- redirección
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356746"
---
# <a name="redirection"></a><span data-ttu-id="4172f-108">Redireccionamiento</span><span class="sxs-lookup"><span data-stu-id="4172f-108">Redirection</span></span>

<span data-ttu-id="4172f-109">La lista de reproducción redirigirá el explorador a Windows Media Player para reproducir el archivo multimedia o la secuencia de medios designada.</span><span class="sxs-lookup"><span data-stu-id="4172f-109">The playlist will redirect the browser to Windows Media Player to play the designated media stream or media file.</span></span> <span data-ttu-id="4172f-110">La lista de reproducción de metarchivos más básica contiene solo el localizador uniforme de recursos (URL) de un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="4172f-110">The most basic metafile playlist contains only the Uniform Resource Locator (URL) of a media file.</span></span>

<span data-ttu-id="4172f-111">Para crear una lista de reproducción de metarchivo básica, abra el editor de texto que prefiera, como el Bloc de notas de Microsoft, y escriba el código de ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="4172f-111">To create a basic metafile playlist, open your favorite text editor, such as Microsoft Notepad, and type the following example code.</span></span>


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



<span data-ttu-id="4172f-112">Sustituya una ruta de acceso válida al archivo de Windows Media mediante la sintaxis de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4172f-112">Substitute a valid path to your Windows Media file using the syntax in the following table.</span></span>



| <span data-ttu-id="4172f-113">Origen de contenido</span><span class="sxs-lookup"><span data-stu-id="4172f-113">Source of content</span></span>                                                                                 | <span data-ttu-id="4172f-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4172f-114">Syntax</span></span>                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="4172f-115">El contenido es un archivo de un servidor de Windows Media</span><span class="sxs-lookup"><span data-stu-id="4172f-115">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="4172f-116">mms://ServerName/Path/FileName.wma</span><span class="sxs-lookup"><span data-stu-id="4172f-116">mms://ServerName/Path/FileName.wma</span></span>        |
| <span data-ttu-id="4172f-117">El contenido es una multidifusión de difusión a la que se tiene acceso desde una estación de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4172f-117">Content is a broadcast multicast that is accessed from a Windows Media station</span></span>                    | https://WebServerName/Stations/kxyz.nsc    |
| <span data-ttu-id="4172f-118">El contenido es una unidifusión de difusión a la que se tiene acceso desde un punto de publicación en un servidor de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4172f-118">Content is a broadcast unicast that is accessed from a publishing point on a Windows Media server</span></span> | <span data-ttu-id="4172f-119">mms://ServerName/PublishingPointAlias</span><span class="sxs-lookup"><span data-stu-id="4172f-119">mms://ServerName/PublishingPointAlias</span></span>     |
| <span data-ttu-id="4172f-120">El contenido es un archivo de un servidor Web</span><span class="sxs-lookup"><span data-stu-id="4172f-120">Content is a file on a web server</span></span>                                                                 | https://WebServerName/Path/Filename.wma    |
| <span data-ttu-id="4172f-121">El contenido es un archivo de un disco duro local</span><span class="sxs-lookup"><span data-stu-id="4172f-121">Content is a file on a local hard disk</span></span>                                                            | <span data-ttu-id="4172f-122">file://c: \\ ruta de acceso \\ nombreDeArchivo. WMA</span><span class="sxs-lookup"><span data-stu-id="4172f-122">file://c:\\Path\\Filename.wma</span></span>             |
| <span data-ttu-id="4172f-123">El contenido es un archivo de un recurso compartido de red</span><span class="sxs-lookup"><span data-stu-id="4172f-123">Content is a file on a network share</span></span>                                                              | <span data-ttu-id="4172f-124">file:// \\ \\ ServerName \\ rutaDeAcceso \\ nombreDeArchivo. WMA</span><span class="sxs-lookup"><span data-stu-id="4172f-124">file://\\\\ServerName\\Path\\Filename.wma</span></span> |
| <span data-ttu-id="4172f-125">El contenido es un archivo de un servidor de Windows Media</span><span class="sxs-lookup"><span data-stu-id="4172f-125">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="4172f-126">mms://ServerName/Path/FileName.wmv</span><span class="sxs-lookup"><span data-stu-id="4172f-126">mms://ServerName/Path/FileName.wmv</span></span>        |



 

<span data-ttu-id="4172f-127">Guarde el archivo que ha creado con un nombre de archivo y una extensión, tal y como se describe en [extensiones de nombre de archivo](file-name-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="4172f-127">Save the file you have created with a file name and extension as described in [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="4172f-128">Haga doble clic en él en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="4172f-128">Double-click it in Windows Explorer.</span></span> <span data-ttu-id="4172f-129">Windows Media Player debe abrir e iniciar el streaming del contenido.</span><span class="sxs-lookup"><span data-stu-id="4172f-129">Windows Media Player should open and start streaming the content.</span></span> <span data-ttu-id="4172f-130">Puede guardar el archivo en el servidor Web, junto con las páginas web, y vincularlo con un elemento **href** , o insertarlo en una página web mediante la etiqueta de **objeto** de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="4172f-130">You can save the file to your web server, along with your webpages, and link to it with an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** tag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4172f-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4172f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4172f-132">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="4172f-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="4172f-133">**Usar listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="4172f-133">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="4172f-134">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4172f-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="4172f-135">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4172f-135">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




