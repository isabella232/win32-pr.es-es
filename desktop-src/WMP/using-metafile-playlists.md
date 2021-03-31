---
title: Usar listas de reproducción de metarchivo
description: Usar listas de reproducción de metarchivo
ms.assetid: f5711a7f-7674-4b92-8262-cee8bac4aa77
keywords:
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
ms.openlocfilehash: 71f245d1fc1610174f842347a15dfcfaa13286e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903239"
---
# <a name="using-metafile-playlists"></a><span data-ttu-id="9718e-106">Usar listas de reproducción de metarchivo</span><span class="sxs-lookup"><span data-stu-id="9718e-106">Using Metafile Playlists</span></span>

<span data-ttu-id="9718e-107">Las listas de reproducción especifican cómo se reproducirán los archivos multimedia o multimedia de streaming y qué metadatos Media Player mostrarán.</span><span class="sxs-lookup"><span data-stu-id="9718e-107">Playlists specify how the streaming media or media files will be played and what metadata Windows Media Player will display.</span></span>

<span data-ttu-id="9718e-108">En esta sección se explican varias formas de usar listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="9718e-108">This section explains several ways you can use playlists.</span></span> <span data-ttu-id="9718e-109">La sección se divide en los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="9718e-109">The section is divided into the following topics.</span></span>



| <span data-ttu-id="9718e-110">Tema</span><span class="sxs-lookup"><span data-stu-id="9718e-110">Topic</span></span>                                                                                              | <span data-ttu-id="9718e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9718e-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9718e-112">Modificar la presentación</span><span class="sxs-lookup"><span data-stu-id="9718e-112">Modifying the Display</span></span>](modifying-the-display.md)                                                 | <span data-ttu-id="9718e-113">Agregar texto, vínculos e imágenes.</span><span class="sxs-lookup"><span data-stu-id="9718e-113">Adding text, links, and images.</span></span>                                                                                                                                |
| [<span data-ttu-id="9718e-114">Redireccionamiento</span><span class="sxs-lookup"><span data-stu-id="9718e-114">Redirection</span></span>](redirection.md)                                                                     | <span data-ttu-id="9718e-115">Usar listas de reproducción para redirigir el explorador a Windows Media Player y especificar la dirección URL de una secuencia o archivo multimedia que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="9718e-115">Using playlists to redirect the browser to Windows Media Player and specifying the URL of a stream or media file to play.</span></span>                                      |
| [<span data-ttu-id="9718e-116">Obtener acceso a medios</span><span class="sxs-lookup"><span data-stu-id="9718e-116">Accessing Media</span></span>](accessing-media.md)                                                             | <span data-ttu-id="9718e-117">Usar elementos de metarchivo y sus elementos secundarios para especificar el contenido al que se va a obtener acceso y el orden y la duración de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="9718e-117">Using metafile elements and their child elements to specify the content to access, and the order and duration of their playback.</span></span>                               |
| [<span data-ttu-id="9718e-118">Usar el cambio de secuencia de eventos en directo</span><span class="sxs-lookup"><span data-stu-id="9718e-118">Using Live Event Stream Switching</span></span>](using-live-event-stream-switching.md)                         | <span data-ttu-id="9718e-119">Usar el elemento **Event** para especificar una secuencia de medios a la que obtener acceso y, a continuación, reanudar la reproducción de la secuencia original.</span><span class="sxs-lookup"><span data-stu-id="9718e-119">Using the **EVENT** element to specify a media stream to access and then resume playing the original stream.</span></span> <span data-ttu-id="9718e-120">Se usa para la inserción de anuncios.</span><span class="sxs-lookup"><span data-stu-id="9718e-120">Used for ad insertion.</span></span>                            |
| [<span data-ttu-id="9718e-121">Usar metaarchivos para la conmutación de flujos sin problemas</span><span class="sxs-lookup"><span data-stu-id="9718e-121">Using Metafiles for Seamless Stream Switching</span></span>](using-metafiles-for-seamless-stream-switching.md) | <span data-ttu-id="9718e-122">Usar el elemento **Event** para cargar previamente el siguiente flujo multimedia al que obtener acceso para evitar brechas en la presentación.</span><span class="sxs-lookup"><span data-stu-id="9718e-122">Using the **EVENT** element to preload the next media stream to access to avoid gaps in the presentation.</span></span>                                                      |
| [<span data-ttu-id="9718e-123">Usar anuncios</span><span class="sxs-lookup"><span data-stu-id="9718e-123">Using Announcements</span></span>](using-announcements.md)                                                     | <span data-ttu-id="9718e-124">Uso de un metarchivo para proporcionar información sobre la dirección URL de una secuencia multimedia, incluida la dirección IP de multidifusión, el puerto, el formato de secuencia y otras configuraciones de la estación.</span><span class="sxs-lookup"><span data-stu-id="9718e-124">Using a metafile to provide information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> |
| [<span data-ttu-id="9718e-125">Usar URL y sustitución de servidor</span><span class="sxs-lookup"><span data-stu-id="9718e-125">Using URL and Server Rollover</span></span>](using-url-and-server-rollover.md)                                 | <span data-ttu-id="9718e-126">Usar listas de reproducción de metarchivos para proporcionar un medio de propagación automática a orígenes de contenido alternativo cuando no se puede tener acceso a una secuencia o reproducirla.</span><span class="sxs-lookup"><span data-stu-id="9718e-126">Using metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span>             |
| [<span data-ttu-id="9718e-127">Usar parámetros y comandos personalizados</span><span class="sxs-lookup"><span data-stu-id="9718e-127">Using Custom Parameters and Commands</span></span>](using-custom-parameters-and-commands.md)                   | <span data-ttu-id="9718e-128">Usar el elemento **param** para definir elementos personalizados para proporcionar metadatos adicionales.</span><span class="sxs-lookup"><span data-stu-id="9718e-128">Using the **PARAM** element to define custom elements to provide additional metadata.</span></span>                                                                          |
| [<span data-ttu-id="9718e-129">Personalización de la entrega de contenido multimedia</span><span class="sxs-lookup"><span data-stu-id="9718e-129">Personalizing Media Delivery</span></span>](personalizing-media-delivery.md)                                   | <span data-ttu-id="9718e-130">Usar las preferencias de usuario para determinar el contenido de difusión.</span><span class="sxs-lookup"><span data-stu-id="9718e-130">Using user preferences to determine broadcast content.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="9718e-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9718e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9718e-132">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="9718e-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="9718e-133">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9718e-133">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="9718e-134">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9718e-134">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




