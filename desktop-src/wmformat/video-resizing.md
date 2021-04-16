---
title: Cambio de tamaño de vídeo
description: Cambio de tamaño de vídeo
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- SDK de Windows Media Format, cambio de tamaño de vídeo
- SDK de Windows Media Format, cambiar tamaño de vídeo
- Advanced Systems Format (ASF), cambio de tamaño de vídeo
- ASF (formato de sistemas avanzados), cambio de tamaño de vídeo
- Advanced Systems Format (ASF), cambiar el tamaño de vídeo
- ASF (formato de sistemas avanzados), cambiar el tamaño del vídeo
- cambio de tamaño de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268553"
---
# <a name="video-resizing"></a><span data-ttu-id="25d0e-110">Cambio de tamaño de vídeo</span><span class="sxs-lookup"><span data-stu-id="25d0e-110">Video Resizing</span></span>

<span data-ttu-id="25d0e-111">Al definir la configuración de un flujo de vídeo, debe especificar un ancho y un alto para los fotogramas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="25d0e-111">When you define the settings for a video stream, you must specify a width and height for the video frames.</span></span> <span data-ttu-id="25d0e-112">Este tamaño de vídeo determina el tamaño de los fotogramas de vídeo codificados en la sección de datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="25d0e-112">This video size determines the size of the video frames encoded in the data section of the file.</span></span> <span data-ttu-id="25d0e-113">Sin embargo, el tamaño de vídeo de un perfil no determina, o limita, el tamaño del medio de entrada que se entrega al escritor o el tamaño de los medios de salida que se reciben del lector.</span><span class="sxs-lookup"><span data-stu-id="25d0e-113">However, the video size in a profile does not determine, or limit, the size of the input media that you deliver to the writer, or the size of the output media you receive from the reader.</span></span> <span data-ttu-id="25d0e-114">El escritor puede cambiar el tamaño de los fotogramas de vídeo para que se adapten a las necesidades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="25d0e-114">The writer can resize the video frames to suit the needs of your application.</span></span>

<span data-ttu-id="25d0e-115">El tamaño de la imagen de vídeo se puede considerar en tres fases: tamaño del vídeo de entrada, tamaño de vídeo de flujo y tamaño de vídeo de salida.</span><span class="sxs-lookup"><span data-stu-id="25d0e-115">Video image size can be thought of as going through three stages: input video size, stream video size, and output video size.</span></span>

<span data-ttu-id="25d0e-116">El tamaño del vídeo de entrada es el tamaño de los fotogramas que se pasan como muestras al objeto escritor.</span><span class="sxs-lookup"><span data-stu-id="25d0e-116">Input video size is the size of the frames that you pass as samples to the writer object.</span></span> <span data-ttu-id="25d0e-117">Este tamaño se define como una de las propiedades de entrada de vídeo necesarias.</span><span class="sxs-lookup"><span data-stu-id="25d0e-117">You define this size as one of the required video input properties.</span></span> <span data-ttu-id="25d0e-118">Para obtener más información sobre las propiedades de entrada, consulte [para enumerar los formatos de entrada](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="25d0e-118">For more information about input properties, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

<span data-ttu-id="25d0e-119">El tamaño de vídeo de Stream es el tamaño de los marcos de la sección de datos del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="25d0e-119">Stream video size is the size of the frames in the data section of the ASF file.</span></span> <span data-ttu-id="25d0e-120">Este tamaño se define como uno de los valores de configuración de secuencia necesarios en el perfil.</span><span class="sxs-lookup"><span data-stu-id="25d0e-120">You define this size as one of the required stream configuration settings in the profile.</span></span> <span data-ttu-id="25d0e-121">Si está escribiendo un archivo y el tamaño del vídeo de entrada es diferente del tamaño del vídeo de flujo, el escritor cambia el tamaño de los fotogramas durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="25d0e-121">If you are writing a file and the input video size is different from the stream video size, the writer resizes the frames while encoding.</span></span> <span data-ttu-id="25d0e-122">Para obtener más información sobre las propiedades de secuencias de vídeo, consulte [configuración de secuencias de vídeo](configuring-video-streams.md).</span><span class="sxs-lookup"><span data-stu-id="25d0e-122">For more information about video stream properties, see [Configuring Video Streams](configuring-video-streams.md).</span></span>

<span data-ttu-id="25d0e-123">El tamaño del vídeo de salida es el tamaño de los fotogramas entregados por el lector o el lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="25d0e-123">Output video size is the size of the frames delivered by the reader or synchronous reader.</span></span> <span data-ttu-id="25d0e-124">Este tamaño se define como una de las propiedades de salida de vídeo necesarias.</span><span class="sxs-lookup"><span data-stu-id="25d0e-124">You define this size as one of the required video output properties.</span></span> <span data-ttu-id="25d0e-125">Si está leyendo un archivo y el tamaño del vídeo de salida es diferente del tamaño del vídeo de flujo, el lector cambia el tamaño de los fotogramas durante la descodificación.</span><span class="sxs-lookup"><span data-stu-id="25d0e-125">If you are reading a file and the output video size is different from the stream video size, the reader resizes the frames while decoding.</span></span>

<span data-ttu-id="25d0e-126">No se puede establecer un tamaño de vídeo de flujo en un número impar de píxeles de ancho.</span><span class="sxs-lookup"><span data-stu-id="25d0e-126">You cannot set a stream video size to an odd number of pixels wide.</span></span> <span data-ttu-id="25d0e-127">Si establece el ancho de una secuencia de vídeo en un valor impar, el escritor no aceptará el perfil, o bien el vídeo resultante se codificará con una línea negra hacia abajo para componer la diferencia.</span><span class="sxs-lookup"><span data-stu-id="25d0e-127">If you set the width of a video stream to an odd value, either the profile will not be accepted by the writer, or the resulting video will be encoded with a black line down one side to make up the difference.</span></span>

<span data-ttu-id="25d0e-128">Debe tener cuidado al cambiar el tamaño del vídeo.</span><span class="sxs-lookup"><span data-stu-id="25d0e-128">You should take care when resizing video.</span></span> <span data-ttu-id="25d0e-129">Las imágenes tienden a ser más adecuadas en su resolución original.</span><span class="sxs-lookup"><span data-stu-id="25d0e-129">Images tend to look their best at their original resolution.</span></span> <span data-ttu-id="25d0e-130">A menudo, el cambio de tamaño de las imágenes puede producir distorsiones y convertir el texto en ilegible.</span><span class="sxs-lookup"><span data-stu-id="25d0e-130">Resizing images can often cause distortion and make text illegible.</span></span> <span data-ttu-id="25d0e-131">Si comprime vídeo a una velocidad de bits baja, también encontrará que el cambio de tamaño de las distorsiones puede conducir a artefactos de compresión graves.</span><span class="sxs-lookup"><span data-stu-id="25d0e-131">If you are compressing video to a low bit rate, you will also find that resizing distortions can lead to severe compression artifacts.</span></span>

<span data-ttu-id="25d0e-132">El códec de pantalla de Windows Media Video 9 no admite el cambio de tamaño.</span><span class="sxs-lookup"><span data-stu-id="25d0e-132">The Windows Media Video 9 Screen codec does not support resizing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25d0e-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="25d0e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25d0e-134">**Características de escritura de archivos**</span><span class="sxs-lookup"><span data-stu-id="25d0e-134">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="25d0e-135">**Trabajar con entradas**</span><span class="sxs-lookup"><span data-stu-id="25d0e-135">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="25d0e-136">**Trabajar con salidas**</span><span class="sxs-lookup"><span data-stu-id="25d0e-136">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




