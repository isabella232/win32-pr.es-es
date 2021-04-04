---
description: En esta sección se describe cómo usar la API de Transcode para volver a codificar los archivos multimedia. La API de transcodificación se presentó en Windows 7.
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: API de transcodificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908637"
---
# <a name="transcode-api"></a><span data-ttu-id="280e0-104">API de transcodificación</span><span class="sxs-lookup"><span data-stu-id="280e0-104">Transcode API</span></span>

<span data-ttu-id="280e0-105">En esta sección se describe cómo usar la API de Transcode para volver a codificar los archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="280e0-105">This section describes how to use the transcode API to re-encode media files.</span></span> <span data-ttu-id="280e0-106">La API de transcodificación se presentó en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="280e0-106">The transcode API was introduced in Windows 7.</span></span>

<span data-ttu-id="280e0-107">La *transcodificación* es la conversión de un archivo multimedia digital de un formato a otro.</span><span class="sxs-lookup"><span data-stu-id="280e0-107">*Transcoding* is the conversion of a digital media file from one format to another.</span></span> <span data-ttu-id="280e0-108">La API de Transcode está diseñada para usarse con la [sesión multimedia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="280e0-108">The transcode API is designed to be used with the [Media Session](media-session.md).</span></span> <span data-ttu-id="280e0-109">Simplifica el uso de la sesión multimedia para determinados tipos de aplicaciones de transcodificación:</span><span class="sxs-lookup"><span data-stu-id="280e0-109">It simplifies the use of the Media Session for certain types of transcoding applications:</span></span>

-   <span data-ttu-id="280e0-110">Codificación de velocidad de bits constante (CBR), donde la velocidad de bits de destino se conoce de antemano.</span><span class="sxs-lookup"><span data-stu-id="280e0-110">Constant bit rate (CBR) encoding, where the target bit rate is known in advance.</span></span>
-   <span data-ttu-id="280e0-111">Como máximo, una secuencia de audio y otra de vídeo.</span><span class="sxs-lookup"><span data-stu-id="280e0-111">At most one audio stream and one video stream.</span></span>
-   <span data-ttu-id="280e0-112">Codificación de y a un archivo.</span><span class="sxs-lookup"><span data-stu-id="280e0-112">Encoding from and to a file.</span></span>

<span data-ttu-id="280e0-113">La API de Transcode no admite lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="280e0-113">Transcode API does not support the following:</span></span>

-   <span data-ttu-id="280e0-114">Velocidad de bits variable (VBR) o codificación de múltiples pasadas.</span><span class="sxs-lookup"><span data-stu-id="280e0-114">Variable bit rate (VBR) or multi-pass encoding.</span></span>
-   <span data-ttu-id="280e0-115">Varias secuencias de audio o varias secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="280e0-115">Multiple audio streams or multiple video streams.</span></span>
-   <span data-ttu-id="280e0-116">Contenido protegido con DRM que no sea archivos ASF protegidos con WMDRM.</span><span class="sxs-lookup"><span data-stu-id="280e0-116">DRM-protected content other than ASF files protected with WMDRM.</span></span>
-   <span data-ttu-id="280e0-117">Streaming en vivo, como streaming de Live-to-file o streaming en vivo.</span><span class="sxs-lookup"><span data-stu-id="280e0-117">Live streaming, such as live-to-file streaming or live-to-live streaming.</span></span>

<span data-ttu-id="280e0-118">Si la aplicación de codificación encaja dentro de estas restricciones, la API de Transcode es un modelo de programación más sencillo que el uso de la sesión multimedia por sí solo.</span><span class="sxs-lookup"><span data-stu-id="280e0-118">If your encoding application fits within these constraints, the transcode API a simpler programming model than using the Media Session alone.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="280e0-119">En esta sección</span><span class="sxs-lookup"><span data-stu-id="280e0-119">In this section</span></span>



| <span data-ttu-id="280e0-120">Tema</span><span class="sxs-lookup"><span data-stu-id="280e0-120">Topic</span></span>                                                                                          | <span data-ttu-id="280e0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="280e0-121">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="280e0-122">Acerca de la API de Transcode</span><span class="sxs-lookup"><span data-stu-id="280e0-122">About the Transcode API</span></span>](about-the-transcode-api.md)<br/>                              | <span data-ttu-id="280e0-123">Proporciona información general sobre la API de Transcode.</span><span class="sxs-lookup"><span data-stu-id="280e0-123">Provides a general overview of the transcode API.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="280e0-124">Uso de la API de Transcode</span><span class="sxs-lookup"><span data-stu-id="280e0-124">Using the Transcode API</span></span>](fast-transcode-objects.md)<br/>                               | <span data-ttu-id="280e0-125">Describe cómo una aplicación utiliza la API de Transcode.</span><span class="sxs-lookup"><span data-stu-id="280e0-125">Describes how an application uses the transcode API.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="280e0-126">Tutorial: codificación de un archivo MP4</span><span class="sxs-lookup"><span data-stu-id="280e0-126">Tutorial: Encoding an MP4 File</span></span>](tutorial--encoding-an-mp4-file-.md)<br/>               | <span data-ttu-id="280e0-127">Un tutorial paso a paso que muestra cómo usar la API de Transcode para codificar un archivo MP4.</span><span class="sxs-lookup"><span data-stu-id="280e0-127">A step-by-step tutorial that shows how to use the transcode API to encode an MP4 file.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="280e0-128">Tutorial: codificar un archivo WMA</span><span class="sxs-lookup"><span data-stu-id="280e0-128">Tutorial: Encoding a WMA File</span></span>](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | <span data-ttu-id="280e0-129">Muestra cómo usar la API de Transcode para codificar un archivo WMA.</span><span class="sxs-lookup"><span data-stu-id="280e0-129">Shows how to use the transcode API to encode a WMA file.</span></span> <span data-ttu-id="280e0-130">En este tutorial se modifica el código que se muestra en [Tutorial: codificar un archivo MP4](tutorial--encoding-an-mp4-file-.md), por lo que primero debe leer ese tutorial.</span><span class="sxs-lookup"><span data-stu-id="280e0-130">This tutorial modifies the code shown in [Tutorial: Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="280e0-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="280e0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="280e0-132">Codificación y creación de archivos</span><span class="sxs-lookup"><span data-stu-id="280e0-132">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="280e0-133">Media Foundation: conceptos esenciales</span><span class="sxs-lookup"><span data-stu-id="280e0-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="280e0-134">Información general de la codificación en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="280e0-134">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




