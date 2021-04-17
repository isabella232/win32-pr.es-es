---
description: Un codificador convierte audio o vídeo sin comprimir en paquetes comprimidos en el formato especificado por la aplicación. Para convertir archivos multimedia en formato ASF, puede usar los códecs de audio y vídeo de Windows Media.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Codificadores de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a642702562cbb6a70b0380deb196c70c4f8207b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697926"
---
# <a name="windows-media-encoders"></a><span data-ttu-id="6f573-104">Codificadores de Windows Media</span><span class="sxs-lookup"><span data-stu-id="6f573-104">Windows Media Encoders</span></span>

<span data-ttu-id="6f573-105">Un codificador convierte audio o vídeo sin comprimir en paquetes comprimidos en el formato especificado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6f573-105">An encoder converts uncompressed audio or video into compressed packets in the format specified by the application.</span></span> <span data-ttu-id="6f573-106">Para convertir archivos multimedia en formato ASF, puede usar los códecs de audio y vídeo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6f573-106">For converting media files into ASF format, you can use the Windows Media audio and video codecs.</span></span>

<span data-ttu-id="6f573-107">Un codificador se identifica mediante el GUID que representa la categoría: audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="6f573-107">An encoder is identified by the GUID that represents the category: audio or video.</span></span> <span data-ttu-id="6f573-108">El tipo de salida del codificador se representa con el GUID principal y el subtipo del tipo de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="6f573-108">The encoder's output type is represented by a media type's major and the sub type GUID.</span></span>

-   <span data-ttu-id="6f573-109">Códecs de audio de Windows Media</span><span class="sxs-lookup"><span data-stu-id="6f573-109">Windows Media audio codecs</span></span>

    <span data-ttu-id="6f573-110">Categoría: **\_ categoría MFT \_ , \_ codificador de audio**</span><span class="sxs-lookup"><span data-stu-id="6f573-110">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="6f573-111">Tipo principal: MFMediaType \_ audio</span><span class="sxs-lookup"><span data-stu-id="6f573-111">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="6f573-112">SubType: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF</span><span class="sxs-lookup"><span data-stu-id="6f573-112">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="6f573-113">Códecs de vídeo de Windows Media</span><span class="sxs-lookup"><span data-stu-id="6f573-113">Windows Media video codecs</span></span>

    <span data-ttu-id="6f573-114">Categoría: **categoría de MFT \_ \_ \_ codificador de vídeo**</span><span class="sxs-lookup"><span data-stu-id="6f573-114">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="6f573-115">Tipo principal: vídeo de MFMediaType \_</span><span class="sxs-lookup"><span data-stu-id="6f573-115">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="6f573-116">SubType: MFVideoFormat \_ Wvc1, MFVideoFormat \_ Wmv3, MFVideoFormat wmv2 \_ , MFVideoFormat \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="6f573-116">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="6f573-117">Estos codificadores se implementan como [Media Foundation Transform](media-foundation-transforms.md) (MFT) y Media Foundation proporcionan acceso a la aplicación a través de la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del codificador.</span><span class="sxs-lookup"><span data-stu-id="6f573-117">These encoders are implemented as [Media Foundation transform](media-foundation-transforms.md) (MFT) and Media Foundation provides access to the application through the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the encoder.</span></span> <span data-ttu-id="6f573-118">Si utiliza componentes de capa de canalización para la codificación ASF, la MFT del codificador se inserta en la canalización como nodo de transformación, ya que es responsable de transformar los datos multimedia que fluyen a través del origen al receptor.</span><span class="sxs-lookup"><span data-stu-id="6f573-118">If you are using pipeline layer components for ASF encoding, the encoder MFT is inserted into the pipeline as a transform node because it is responsible for transforming media data that flows through the source to the sink.</span></span> <span data-ttu-id="6f573-119">Si el origen es un tipo comprimido, la canalización agrega los descodificadores necesarios para convertir el origen en un tipo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="6f573-119">If the source is a compressed type, then the pipeline adds the required decoders to convert the source into an uncompressed type.</span></span> <span data-ttu-id="6f573-120">Un codificador tiene un flujo de entrada y un flujo de salida.</span><span class="sxs-lookup"><span data-stu-id="6f573-120">An encoder has one input stream and one output stream.</span></span> <span data-ttu-id="6f573-121">El codificador recibe datos de entrada y genera datos codificados de acuerdo con la configuración y el formato establecidos por la aplicación antes de la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="6f573-121">The encoder receives input data and produces encoded data according to the configuration and format set by the application prior to the encoding session.</span></span> <span data-ttu-id="6f573-122">El formato del flujo de salida se describe mediante un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6f573-122">The format of the output stream is described by a media type.</span></span>

<span data-ttu-id="6f573-123">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="6f573-123">This section contains the following topics.</span></span>



| <span data-ttu-id="6f573-124">Tema</span><span class="sxs-lookup"><span data-stu-id="6f573-124">Topic</span></span>                                                                              | <span data-ttu-id="6f573-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f573-125">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f573-126">Crear instancias de una MFT del codificador</span><span class="sxs-lookup"><span data-stu-id="6f573-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)                  | <span data-ttu-id="6f573-127">Explica cómo crear el codificador.</span><span class="sxs-lookup"><span data-stu-id="6f573-127">Explains how to create the encoder.</span></span>                                                         |
| [<span data-ttu-id="6f573-128">Propiedades de codificación</span><span class="sxs-lookup"><span data-stu-id="6f573-128">Encoding Properties</span></span>](configuring-the-encoder.md)                                 | <span data-ttu-id="6f573-129">Explica cómo configurar el codificador mediante el establecimiento de las propiedades adecuadas en la MFT del codificador.</span><span class="sxs-lookup"><span data-stu-id="6f573-129">Explains how to configure the encoder by setting appropriate properties on the encoder MFT.</span></span> |
| [<span data-ttu-id="6f573-130">Negociación de tipo de medio en el codificador</span><span class="sxs-lookup"><span data-stu-id="6f573-130">Media Type Negotiation on the Encoder</span></span>](media-type-negotiation-on-the-encoder.md) | <span data-ttu-id="6f573-131">Explica cómo establecer los tipos de medios de entrada y salida en el codificador.</span><span class="sxs-lookup"><span data-stu-id="6f573-131">Explains how to set input and output media types on the encoder.</span></span>                            |
| [<span data-ttu-id="6f573-132">Configuración de un codificador WMV</span><span class="sxs-lookup"><span data-stu-id="6f573-132">Configuring a WMV Encoder</span></span>](configuring-a-wmv-encoder.md)                         | <span data-ttu-id="6f573-133">Explica cómo configurar un codificador Windows Media Video (WMV).</span><span class="sxs-lookup"><span data-stu-id="6f573-133">Explains how to configure a Windows Media Video (WMV) encoder.</span></span>                              |
| [<span data-ttu-id="6f573-134">Establecer un tipo de salida para un codificador WMA</span><span class="sxs-lookup"><span data-stu-id="6f573-134">Setting an Output Type for a WMA Encoder</span></span>](configuring-a-wma-encoder.md)          | <span data-ttu-id="6f573-135">Explica cómo establecer un tipo de salida en un codificador Windows Media Audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="6f573-135">Explains how to set an output type on a Windows Media Audio (WMA) encoder.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="6f573-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6f573-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f573-137">Componentes ASF de capa de canalización</span><span class="sxs-lookup"><span data-stu-id="6f573-137">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



