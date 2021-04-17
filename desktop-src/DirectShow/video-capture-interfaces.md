---
description: Interfaces de captura de vídeo
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Interfaces de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c88ab86833a3570789dee311b36d49f382c9cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677544"
---
# <a name="video-capture-interfaces"></a><span data-ttu-id="ed3fc-103">Interfaces de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ed3fc-103">Video Capture Interfaces</span></span>

<span data-ttu-id="ed3fc-104">Estas interfaces admiten la captura de vídeo, mediante dispositivos de Microsoft® Windows® Driver Model (WDM) o los dispositivos heredados de Microsoft® video para Windows® (VFW).</span><span class="sxs-lookup"><span data-stu-id="ed3fc-104">These interfaces support video capture, using Microsoft® Windows® Driver Model (WDM) devices or legacy Microsoft® Video for Windows® (VFW) devices.</span></span>



| <span data-ttu-id="ed3fc-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="ed3fc-105">Interface</span></span>                                                        | <span data-ttu-id="ed3fc-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed3fc-106">Description</span></span>                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed3fc-107">**IAMAnalogVideoDecoder**</span><span class="sxs-lookup"><span data-stu-id="ed3fc-107">**IAMAnalogVideoDecoder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | <span data-ttu-id="ed3fc-108">Controlar la digitalización de vídeo en una tarjeta de captura de vídeo WDM.</span><span class="sxs-lookup"><span data-stu-id="ed3fc-108">Control video digitization on a WDM video capture card.</span></span>                                                      |
| [<span data-ttu-id="ed3fc-109">**IAMBufferNegotiation**</span><span class="sxs-lookup"><span data-stu-id="ed3fc-109">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | <span data-ttu-id="ed3fc-110">Controla cómo un PIN asigna los búferes.</span><span class="sxs-lookup"><span data-stu-id="ed3fc-110">Control how a pin allocates buffers.</span></span>                                                                         |
| [<span data-ttu-id="ed3fc-111">**IAMCopyCaptureFileProgress**</span><span class="sxs-lookup"><span data-stu-id="ed3fc-111">**IAMCopyCaptureFileProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | <span data-ttu-id="ed3fc-112">Interfaz de devolución de llamada para recibir el progreso de una operación de copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="ed3fc-112">Callback interface to receive the progress of a file copy operation.</span></span>                                         |
| [<span data-ttu-id="ed3fc-113">**IAMCrossbar**</span><span class="sxs-lookup"><span data-stu-id="ed3fc-113">**IAMCrossbar**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | <span data-ttu-id="ed3fc-114">Cree una conexión de hardware entre un origen de audio o vídeo WDM y un dispositivo de captura WDM.</span><span class="sxs-lookup"><span data-stu-id="ed3fc-114">Create a hardware connection between a WDM audio or video source and a WDM capture device.</span></span>                   |
| [<span data-ttu-id="ed3fc-115">**IAMDroppedFrames**</span><span class="sxs-lookup"><span data-stu-id="ed3fc-115">**IAMDroppedFrames**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | <span data-ttu-id="ed3fc-116">Consultar un filtro de captura sobre el rendimiento de la captura.</span><span class="sxs-lookup"><span data-stu-id="ed3fc-116">Query a capture filter about capture performance.</span></span>                                                            |
| [<span data-ttu-id="ed3fc-117">**IAMStreamControl**</span><span class="sxs-lookup"><span data-stu-id="ed3fc-117">**IAMStreamControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | <span data-ttu-id="ed3fc-118">Controlar las horas de inicio y detención de flujos individuales.</span><span class="sxs-lookup"><span data-stu-id="ed3fc-118">Control the start and stop times of individual streams.</span></span>                                                      |
| [<span data-ttu-id="ed3fc-119">**IAMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="ed3fc-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | <span data-ttu-id="ed3fc-120">Consulta y establece el formato de salida del filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="ed3fc-120">Query and set the capture filter's output format.</span></span>                                                            |
| [<span data-ttu-id="ed3fc-121">**IAMVfwCaptureDialogs**</span><span class="sxs-lookup"><span data-stu-id="ed3fc-121">**IAMVfwCaptureDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | <span data-ttu-id="ed3fc-122">Mostrar los cuadros de diálogo proporcionados por los controladores de captura VFW.</span><span class="sxs-lookup"><span data-stu-id="ed3fc-122">Display the dialog boxes provided by VFW capture drivers.</span></span>                                                    |
| [<span data-ttu-id="ed3fc-123">**IAMVideoControl**</span><span class="sxs-lookup"><span data-stu-id="ed3fc-123">**IAMVideoControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | <span data-ttu-id="ed3fc-124">Controle la imagen desde un dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="ed3fc-124">Control the picture from a capture device.</span></span>                                                                   |
| [<span data-ttu-id="ed3fc-125">**IAMVideoProcAmp**</span><span class="sxs-lookup"><span data-stu-id="ed3fc-125">**IAMVideoProcAmp**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | <span data-ttu-id="ed3fc-126">Ajuste las cualidades de una señal de vídeo, como el brillo, el contraste, el matiz, la saturación, la gamma y la nitidez.</span><span class="sxs-lookup"><span data-stu-id="ed3fc-126">Adjust the qualities of a video signal, such as brightness, contrast, hue, saturation, gamma, and sharpness.</span></span> |
| [<span data-ttu-id="ed3fc-127">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="ed3fc-127">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | <span data-ttu-id="ed3fc-128">Cree gráficos de filtro para la captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ed3fc-128">Build filter graphs for video capture.</span></span>                                                                       |
| [<span data-ttu-id="ed3fc-129">**IFileSinkFilter2**</span><span class="sxs-lookup"><span data-stu-id="ed3fc-129">**IFileSinkFilter2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | <span data-ttu-id="ed3fc-130">Especifique el nombre y los atributos de un archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="ed3fc-130">Specify the name and attributes of an output file.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="ed3fc-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed3fc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed3fc-132">Interfaces de control de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="ed3fc-132">External Device Control Interfaces</span></span>](external-device-control-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ed3fc-133">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ed3fc-133">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



