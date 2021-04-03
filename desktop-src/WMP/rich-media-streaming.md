---
title: Transmisión por secuencias multimedia enriquecida
description: Transmisión por secuencias multimedia enriquecida
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Windows Media Player, presentaciones basadas en Web
- Modelo de objetos de Windows Media Player, presentaciones basadas en Web
- modelo de objetos, presentaciones basadas en Web
- Windows Media Player presentaciones móviles y basadas en Web
- Control ActiveX de Windows Media Player, presentaciones basadas en Web
- Control ActiveX móvil de Windows Media Player, presentaciones basadas en Web
- Control ActiveX, presentaciones basadas en Web
- Windows Media Player, transmisión por secuencias multimedia enriquecida
- Modelo de objetos de Windows Media Player, transmisión por secuencias multimedia enriquecida
- modelo de objetos, streaming multimedia enriquecido
- Windows Media Player Mobile, streaming multimedia enriquecido
- Control ActiveX de Windows Media Player, transmisión por secuencias multimedia enriquecida
- Control ActiveX móvil de Windows Media Player, transmisión por secuencias multimedia enriquecida
- Control ActiveX, transmisión por secuencias multimedia enriquecida
- Presentaciones basadas en Web, transmisión por secuencias multimedia enriquecida
- crear presentaciones basadas en Web, transmisión por secuencias multimedia enriquecida
- transmisión por secuencias multimedia enriquecida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778252"
---
# <a name="rich-media-streaming"></a><span data-ttu-id="7c986-120">Transmisión por secuencias multimedia enriquecida</span><span class="sxs-lookup"><span data-stu-id="7c986-120">Rich Media Streaming</span></span>

<span data-ttu-id="7c986-121">Las páginas web complejas contienen muchos componentes diferentes que normalmente se transfieren por separado.</span><span class="sxs-lookup"><span data-stu-id="7c986-121">Complex webpages contain many different components that are normally transferred separately.</span></span> <span data-ttu-id="7c986-122">En una conexión lenta, estas páginas muestran una pieza cada vez y pueden tardar varios minutos en mostrarse por completo.</span><span class="sxs-lookup"><span data-stu-id="7c986-122">On a slow connection, such pages display one piece at a time and may take several minutes to display completely.</span></span> <span data-ttu-id="7c986-123">Esto puede impedir la sincronización efectiva de páginas web con los medios digitales.</span><span class="sxs-lookup"><span data-stu-id="7c986-123">This may prevent you from effectively synchronizing webpages with your digital media.</span></span> <span data-ttu-id="7c986-124">La solución a este problema es la transmisión por secuencias multimedia enriquecida, lo que significa que se agregan las páginas web al flujo multimedia digital para que se entreguen al mismo tiempo que los datos de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="7c986-124">The solution to this problem is rich media streaming, which means adding your webpages to your digital media stream so that they are delivered at the same time as the audio or video data.</span></span>

<span data-ttu-id="7c986-125">La transmisión por secuencias multimedia enriquecida usa un diseño de conjuntos de Marcos sencillo y se comporta exactamente igual que el volteo normal de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="7c986-125">Rich media streaming uses a simple frameset layout and behaves exactly like normal URL flipping.</span></span> <span data-ttu-id="7c986-126">Al igual que en el volteo de direcciones URL, los comandos de script de URL insertados en secuencias de medios digitales se usan para mostrar el contenido en el marco de destino.</span><span class="sxs-lookup"><span data-stu-id="7c986-126">Just as in URL flipping, URL script commands embedded in digital media streams are used to display the content in the target frame.</span></span> <span data-ttu-id="7c986-127">Sin embargo, en lugar de apuntar a las páginas de la web, Windows Media Player 9 series o versiones posteriores usan los comandos de script de la dirección URL para tener acceso a los archivos de la memoria caché de Internet Explorer en los que se encuentra el contenido de HTML transmitido a medida que se recibe.</span><span class="sxs-lookup"><span data-stu-id="7c986-127">Instead of pointing to pages on the Web, however, the URL script commands are used by Windows Media Player 9 Series or later to access files in the Internet Explorer cache where the streamed HTML content is placed as it is received.</span></span> <span data-ttu-id="7c986-128">Al igual que con el volteo normal de direcciones URL, puede escribir controladores de eventos que respondan a estos comandos de script de dirección URL, o bien permitir que el control de Windows Media Player controle todo automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7c986-128">Just as with normal URL flipping, you can write event handlers that respond to these URL script commands, or you can let the Windows Media Player control handle everything automatically.</span></span>

> [!Note]  
> <span data-ttu-id="7c986-129">Cualquier contenido HTML entregado a través de la transmisión por secuencias de multimedia enriquecida se reproduce en la zona de seguridad de Internet y está sujeto a la configuración de seguridad del explorador del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c986-129">Any HTML content delivered through rich media streaming is played back in the Internet security zone, and is subject to the user's browser security settings.</span></span>

 

<span data-ttu-id="7c986-130">Para obtener más información acerca de la creación de presentaciones multimedia enriquecidas, consulte el SDK de Windows Media Format 9 series o posterior y el SDK de Windows Media Encoder 9 series.</span><span class="sxs-lookup"><span data-stu-id="7c986-130">For more information on creating rich media presentations, see the Windows Media Format 9 Series or later SDK and the Windows Media Encoder 9 Series SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c986-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c986-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c986-132">**Crear Web-Based presentaciones**</span><span class="sxs-lookup"><span data-stu-id="7c986-132">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="7c986-133">**Usar script para controlar el volteo de URL**</span><span class="sxs-lookup"><span data-stu-id="7c986-133">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




