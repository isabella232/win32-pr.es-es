---
title: Crear una presentación de HTMLView
description: Crear una presentación de HTMLView
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Listas de reproducción de metarchivos de Windows Media, presentaciones de HTMLView
- listas de reproducción, presentaciones de HTMLView
- listas de reproducción de metarchivos, presentaciones de HTMLView
- Listas de reproducción de metarchivos de Windows Media, crear presentaciones HTMLView
- listas de reproducción, creación de presentaciones HTMLView
- listas de reproducción de metarchivos, crear presentaciones HTMLView
- crear presentaciones de HTMLView
- Windows Media Player, crear presentaciones de HTMLView
- Media Player de Windows, presentaciones de HTMLView
- HTMLView, crear presentaciones
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418857"
---
# <a name="creating-an-htmlview-presentation"></a><span data-ttu-id="5328e-113">Crear una presentación de HTMLView</span><span class="sxs-lookup"><span data-stu-id="5328e-113">Creating an HTMLView Presentation</span></span>

<span data-ttu-id="5328e-114">Para crear una presentación HTMLView básica, necesita al menos tres elementos:</span><span class="sxs-lookup"><span data-stu-id="5328e-114">To create a basic HTMLView presentation, you need at least three elements:</span></span>

-   <span data-ttu-id="5328e-115">**Contenido multimedia digital.**</span><span class="sxs-lookup"><span data-stu-id="5328e-115">**Digital media content.**</span></span> <span data-ttu-id="5328e-116">Se trata de uno o más archivos de audio o vídeo que Windows Media Player reproduce.</span><span class="sxs-lookup"><span data-stu-id="5328e-116">This is one or more audio or video files that Windows Media Player plays.</span></span>
-   <span data-ttu-id="5328e-117">**Una página web.**</span><span class="sxs-lookup"><span data-stu-id="5328e-117">**A webpage.**</span></span> <span data-ttu-id="5328e-118">Este es el contenido basado en Web que se muestra en la característica **reproducción en curso** de la interfaz de usuario del reproductor.</span><span class="sxs-lookup"><span data-stu-id="5328e-118">This is the Web-based content that displays in the **Now Playing** feature of the Player UI.</span></span>
-   <span data-ttu-id="5328e-119">**Un metarchivo de Windows Media.**</span><span class="sxs-lookup"><span data-stu-id="5328e-119">**A Windows Media metafile.**</span></span> <span data-ttu-id="5328e-120">Esta es la lista de reproducción de metarchivo que dirige a Windows Media Player para combinar el contenido multimedia digital con la Página Web.</span><span class="sxs-lookup"><span data-stu-id="5328e-120">This is the metafile playlist that directs Windows Media Player to combine the digital media content with the webpage.</span></span>

<span data-ttu-id="5328e-121">Un archivo. ASX es un archivo de texto que proporciona información acerca de una secuencia de archivos y su presentación.</span><span class="sxs-lookup"><span data-stu-id="5328e-121">An .asx file is a text file that provides information about a file stream and its presentation.</span></span> <span data-ttu-id="5328e-122">En función de la sintaxis de lenguaje de marcado extensible (XML), los archivos. ASX pueden contener una variedad de elementos, cada uno identificado por una etiqueta con atributos asociados.</span><span class="sxs-lookup"><span data-stu-id="5328e-122">Based on Extensible Markup Language (XML) syntax, .asx files can contain a variety of elements, each identified by a tag with associated attributes.</span></span> <span data-ttu-id="5328e-123">El elemento **param** proporciona una manera de asociar un parámetro personalizado a una entrada determinada en una lista de reproducción de metarchivo o en todo el metarchivo.</span><span class="sxs-lookup"><span data-stu-id="5328e-123">The **PARAM** element provides a way to associate a custom parameter with either a particular entry in a metafile playlist or the entire metafile.</span></span> <span data-ttu-id="5328e-124">Uno de los nombres de parámetro predefinidos disponibles para su uso es "HTMLView".</span><span class="sxs-lookup"><span data-stu-id="5328e-124">One of the predefined parameter names available for your use is "HTMLView".</span></span> <span data-ttu-id="5328e-125">Este es el parámetro que hace que la Página Web especificada por el valor de dirección URL se muestre en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5328e-125">This is the parameter that causes the webpage specified by the URL value to be displayed in Windows Media Player.</span></span>

<span data-ttu-id="5328e-126">En el ejemplo de código siguiente se muestra un archivo. ASX que combina un solo archivo multimedia digital con una única página web:</span><span class="sxs-lookup"><span data-stu-id="5328e-126">The following example code shows an .asx file that combines a single digital media file with a single webpage:</span></span>


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="5328e-127">Cuando Windows Media Player abre el archivo. asx en el ejemplo anterior, reproduce el audio desde el archivo denominado Content1. WMA y abre la página web llamada htmlview.htm en la característica **reproducción en curso** del reproductor en modo completo.</span><span class="sxs-lookup"><span data-stu-id="5328e-127">When Windows Media Player opens the .asx file in the preceding example, it plays the audio from the file named content1.wma and opens the webpage named htmlview.htm in the **Now Playing** feature of the full-mode Player.</span></span> <span data-ttu-id="5328e-128">El usuario puede pausar, buscar y detener el contenido de audio mediante los controles de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="5328e-128">The user can pause, seek, and stop the audio content using the Windows Media Player controls.</span></span>

<span data-ttu-id="5328e-129">Puede cambiar fácilmente la página web que se muestra para cada elemento de contenido asociando un elemento **param** a cada entrada, como se muestra en el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="5328e-129">You can easily change the webpage that is displayed for each piece of content by associating a **PARAM** element with each entry, as the following code example shows:</span></span>


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="5328e-130">En el ejemplo anterior, Windows Media Player primero muestra la página web htmlview1.htm mientras se reproduce el archivo de audio digital Content1. WMA.</span><span class="sxs-lookup"><span data-stu-id="5328e-130">In the preceding example, Windows Media Player first displays the webpage htmlview1.htm while playing the digital audio file content1.wma.</span></span> <span data-ttu-id="5328e-131">Cuando el reproductor Abra la entrada siguiente en la lista de reproducción, content2. WMA, la página web que se muestra en **ahora se reproducen** los cambios en htmlview2.htm.</span><span class="sxs-lookup"><span data-stu-id="5328e-131">When the Player opens the next entry in the playlist, content2.wma, the webpage displayed in **Now Playing** changes to htmlview2.htm.</span></span> <span data-ttu-id="5328e-132">De esta forma, puede especificar la página web que el usuario verá para cada parte de contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="5328e-132">In this way, you can specify which webpage the user sees for each piece of digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5328e-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5328e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5328e-134">**Mostrar páginas web en Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="5328e-134">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="5328e-135">**Elemento PARAM**</span><span class="sxs-lookup"><span data-stu-id="5328e-135">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




