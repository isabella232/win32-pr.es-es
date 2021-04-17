---
description: Procesadores de señal digital
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Procesadores de señal digital
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0961554d9c9902e68f74c6b2b57662b23846614f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697918"
---
# <a name="digital-signal-processors"></a><span data-ttu-id="208fc-103">Procesadores de señal digital</span><span class="sxs-lookup"><span data-stu-id="208fc-103">Digital Signal Processors</span></span>

<span data-ttu-id="208fc-104">En esta sección se describen los objetos de procesador de señal digital (DSP) proporcionados por Windows.</span><span class="sxs-lookup"><span data-stu-id="208fc-104">This section describes the digital signal processor (DSP) objects provided by Windows.</span></span>

<span data-ttu-id="208fc-105">Microsoft usa el término *procesador de señal digital* para designar un conjunto de objetos com que realizan transformaciones en datos de audio y vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="208fc-105">Microsoft uses the term *digital signal processor* to designate a set of COM objects that perform transformations on uncompressed audio and video data.</span></span> <span data-ttu-id="208fc-106">Los DSP descritos en este SDK transforman audio y vídeo en diversos formatos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="208fc-106">The DSPs described in this SDK transform audio and video in a variety of uncompressed formats.</span></span>

<span data-ttu-id="208fc-107">Los DSP pueden usarse por sí solos o en combinación con los códecs de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="208fc-107">The DSPs can be used by themselves, or in combination with audio and video codecs.</span></span> <span data-ttu-id="208fc-108">A excepción del DSP de captura de voz, cada DSP mostrado aquí implementa dos interfaces independientes pero similares.</span><span class="sxs-lookup"><span data-stu-id="208fc-108">With the exception of the Voice Capture DSP, each DSP listed here implements two separate but similar interfaces.</span></span>



| <span data-ttu-id="208fc-109">Interfaz</span><span class="sxs-lookup"><span data-stu-id="208fc-109">Interface</span></span>                              | <span data-ttu-id="208fc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="208fc-110">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="208fc-111">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="208fc-111">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="208fc-112">Compatible con Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="208fc-112">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="208fc-113">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="208fc-113">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="208fc-114">Compatible con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="208fc-114">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="208fc-115">Puede configurar los DSP mediante la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para establecer propiedades.</span><span class="sxs-lookup"><span data-stu-id="208fc-115">You can configure the DSPs by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to set properties.</span></span> <span data-ttu-id="208fc-116">Algunos de los DSP tienen interfaces adicionales que establecen propiedades.</span><span class="sxs-lookup"><span data-stu-id="208fc-116">Some of the DSPs have additional interfaces that set properties.</span></span> <span data-ttu-id="208fc-117">Para utilizar estas interfaces, llame al método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de cualquier otra interfaz del DSP.</span><span class="sxs-lookup"><span data-stu-id="208fc-117">To use these interfaces, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of any other interface of the DSP.</span></span> <span data-ttu-id="208fc-118">En el tema de referencia de cada DSP se enumeran las propiedades, interfaces y otras características admitidas.</span><span class="sxs-lookup"><span data-stu-id="208fc-118">The reference topic for each DSP lists the supported properties, interfaces, and other features.</span></span>

<span data-ttu-id="208fc-119">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="208fc-119">This section contains the following topics.</span></span>



| <span data-ttu-id="208fc-120">DSP</span><span class="sxs-lookup"><span data-stu-id="208fc-120">DSP</span></span>                                                      | <span data-ttu-id="208fc-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="208fc-121">Description</span></span>                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="208fc-122">DSP de remuestreador de audio</span><span class="sxs-lookup"><span data-stu-id="208fc-122">Audio Resampler DSP</span></span>](audioresampler.md)                | <span data-ttu-id="208fc-123">Convierte la velocidad de muestreo de una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="208fc-123">Converts the sampling rate of an audio stream.</span></span>       |
| [<span data-ttu-id="208fc-124">DSP de transformación de control de color</span><span class="sxs-lookup"><span data-stu-id="208fc-124">Color Control Transform DSP</span></span>](colorcontroltransform.md) | <span data-ttu-id="208fc-125">Ajusta las características de color de una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="208fc-125">Adjusts the color characteristics of a video stream.</span></span> |
| [<span data-ttu-id="208fc-126">DSP de convertidor de colores</span><span class="sxs-lookup"><span data-stu-id="208fc-126">Color Converter DSP</span></span>](colorconverter.md)                | <span data-ttu-id="208fc-127">Convierte un flujo de vídeo entre formatos de color.</span><span class="sxs-lookup"><span data-stu-id="208fc-127">Converts a video stream between color formats.</span></span>       |
| [<span data-ttu-id="208fc-128">DSP de convertidor de velocidad de fotogramas</span><span class="sxs-lookup"><span data-stu-id="208fc-128">Frame Rate Converter DSP</span></span>](framerateconverter.md)       | <span data-ttu-id="208fc-129">Cambia la velocidad de fotogramas de una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="208fc-129">Changes the frame rate of a video stream.</span></span>            |
| [<span data-ttu-id="208fc-130">Vídeo de tamaño DSP</span><span class="sxs-lookup"><span data-stu-id="208fc-130">Video Resizer DSP</span></span>](videoresizer.md)                    | <span data-ttu-id="208fc-131">Cambia el tamaño de una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="208fc-131">Resizes a video stream.</span></span>                              |
| [<span data-ttu-id="208fc-132">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="208fc-132">Voice Capture DSP</span></span>](voicecapturedmo.md)                 | <span data-ttu-id="208fc-133">Encapsula varios DSP relacionados con la captura de voz.</span><span class="sxs-lookup"><span data-stu-id="208fc-133">Encapsulates several DSPs related to voice capture.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="208fc-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="208fc-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="208fc-135">Referencia de programación de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="208fc-135">Media Foundation Programming Reference</span></span>](media-foundation-programming-reference.md)
</dt> </dl>

 

 
