---
title: Por qué usar DirectShow
description: Por qué usar DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, hardware
- SDK de Windows Media Format, Modelo de controlador de Windows (WDM)
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), hardware
- ASF (formato de sistemas avanzados), hardware
- Advanced Systems Format (ASF), Modelo de controlador de Windows (WDM)
- ASF (formato de sistemas avanzados), Modelo de controlador de Windows (WDM)
- DirectShow, acerca de
- DirectShow, hardware
- DirectShow, Modelo de controlador de Windows (WDM)
- Modelo de controlador de Windows (WDM)
- WDM (Modelo de controlador de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775907"
---
# <a name="why-use-directshow"></a><span data-ttu-id="df680-117">¿Por qué usar DirectShow?</span><span class="sxs-lookup"><span data-stu-id="df680-117">Why Use DirectShow?</span></span>

<span data-ttu-id="df680-118">Hay dos razones principales por las que una aplicación puede usar DirectShow en lugar del SDK de Windows Media Format directamente: para la comodidad de la arquitectura de streaming de DirectShow y para el acceso al hardware.</span><span class="sxs-lookup"><span data-stu-id="df680-118">There are two main reasons why an application might use DirectShow rather than the Windows Media Format SDK directly: for the convenience of the DirectShow streaming architecture, and for access to hardware.</span></span>

## <a name="convenience"></a><span data-ttu-id="df680-119">Comodidad</span><span class="sxs-lookup"><span data-stu-id="df680-119">Convenience</span></span>

<span data-ttu-id="df680-120">Con la arquitectura de streaming de DirectShow, solo realiza algunas llamadas a métodos para reproducir Windows Media Audio o Windows Media Video archivos.</span><span class="sxs-lookup"><span data-stu-id="df680-120">With DirectShow streaming architecture, it takes only a few method calls to play Windows Media Audio or Windows Media Video files.</span></span> <span data-ttu-id="df680-121">También se simplifica la creación de archivos.</span><span class="sxs-lookup"><span data-stu-id="df680-121">Creating files is also simplified.</span></span> <span data-ttu-id="df680-122">Solo tiene que especificar un perfil mediante la interfaz **IConfigAsfWriter** en el filtro y DirectShow carga automáticamente los componentes necesarios para representar o escribir las secuencias, y proporciona los mecanismos para transferir y sincronizar el flujo de datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="df680-122">You simply specify a profile using the **IConfigAsfWriter** interface on the filter, and DirectShow automatically loads the required components for rendering or writing the streams, and provides the mechanisms for transferring and synchronizing the flow of media data.</span></span> <span data-ttu-id="df680-123">DirectShow es especialmente útil al convertir contenido de formatos variados al formato de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="df680-123">DirectShow is especially useful when converting content from varied formats into Windows Media Format.</span></span> <span data-ttu-id="df680-124">Puede crear gráficos de filtros de DirectShow que descodifiquen una amplia variedad de tipos de archivos y de compresión y, a continuación, alimentar los flujos descodificados en el filtro del [escritor ASF de WM](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="df680-124">You can create DirectShow filter graphs that decode a wide variety of file and compression types, and then feed the decoded streams into the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span> <span data-ttu-id="df680-125">Por comparación, el ejemplo UncompAVItoWMV de este SDK solo funciona con archivos AVI sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="df680-125">By comparison, the UncompAVItoWMV sample in this SDK works only with uncompressed AVI files.</span></span> <span data-ttu-id="df680-126">Los flujos de texto y los flujos de datos arbitrarios también se pueden crear o representar mediante DirectShow, pero esto podría requerir la creación de filtros de DirectShow personalizados para procesar esas secuencias.</span><span class="sxs-lookup"><span data-stu-id="df680-126">Text streams and arbitrary data streams can also be created and/or rendered through DirectShow, but this might require you to create custom DirectShow filters for processing those streams.</span></span>

## <a name="access-to-hardware"></a><span data-ttu-id="df680-127">Acceso al hardware</span><span class="sxs-lookup"><span data-stu-id="df680-127">Access to Hardware</span></span>

<span data-ttu-id="df680-128">DirectShow es la única manera de que el código de aplicación acceda a los dispositivos de hardware basados en Modelo de controlador de Windows (WDM), como cámaras DV de 1394, sintonizadores de TV y webcams USB.</span><span class="sxs-lookup"><span data-stu-id="df680-128">DirectShow is the only way for application code to access Windows Driver Model (WDM)–based hardware devices such as 1394 DV cameras, TV tuners, and USB webcams.</span></span> <span data-ttu-id="df680-129">Si la aplicación debe capturar datos directamente desde un dispositivo de hardware basado en WDM y transcodificarlos en el formato de Windows Media, y el SDK de Windows Media Encoder no se adapta a sus necesidades, DirectShow es la única alternativa.</span><span class="sxs-lookup"><span data-stu-id="df680-129">If your application must capture data directly from a WDM-based hardware device and transcode it to Windows Media Format, and the Windows Media Encoder SDK does not suit your needs, then DirectShow is the only alternative.</span></span> <span data-ttu-id="df680-130">DirectShow también puede usarse para tener acceso a dispositivos heredados basados en vídeo para Windows.</span><span class="sxs-lookup"><span data-stu-id="df680-130">DirectShow can also be used to access legacy devices based on Video for Windows.</span></span>

 

 




