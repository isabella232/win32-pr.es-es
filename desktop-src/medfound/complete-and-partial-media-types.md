---
description: En este tema se describe la diferencia entre los tipos de medios completos y los tipos de medios parciales.
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: Tipos de medios completos y parciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac772c09668ee3db96e42d25b3089fa74be104af
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547390"
---
# <a name="complete-and-partial-media-types"></a><span data-ttu-id="40d2b-103">Tipos de medios completos y parciales</span><span class="sxs-lookup"><span data-stu-id="40d2b-103">Complete and Partial Media Types</span></span>

<span data-ttu-id="40d2b-104">En este tema se describe la diferencia entre los tipos de medios completos y los tipos de medios parciales.</span><span class="sxs-lookup"><span data-stu-id="40d2b-104">This topic describes the difference between complete media types and partial media types.</span></span>

## <a name="complete-media-types"></a><span data-ttu-id="40d2b-105">Tipos de medios completos</span><span class="sxs-lookup"><span data-stu-id="40d2b-105">Complete Media Types</span></span>

<span data-ttu-id="40d2b-106">Un tipo de medio *completo* es aquél que define por completo el formato del flujo multimedia.</span><span class="sxs-lookup"><span data-stu-id="40d2b-106">A *complete* media type is one that fully defines the format of the media stream.</span></span> <span data-ttu-id="40d2b-107">Dado un tipo de medio completo, un componente de canalización puede analizar los datos de secuencia asociados al tipo de medio, sin ambigüedad.</span><span class="sxs-lookup"><span data-stu-id="40d2b-107">Given a complete media type, a pipeline component can parse the stream data associated with the media type, with no ambiguity.</span></span>

<span data-ttu-id="40d2b-108">En el caso de los formatos sin comprimir, en los siguientes temas se definen los atributos necesarios para un tipo de medio completo:</span><span class="sxs-lookup"><span data-stu-id="40d2b-108">For uncompressed formats, the following topics define the attributes that are required for a complete media type:</span></span>

-   <span data-ttu-id="40d2b-109">Audio: [tipos de medios de audio sin comprimir](uncompressed-audio-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="40d2b-109">Audio: [Uncompressed Audio Media Types](uncompressed-audio-media-types.md)</span></span>
-   <span data-ttu-id="40d2b-110">Vídeo: [tipos de medios de vídeo sin comprimir](uncompressed-video-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="40d2b-110">Video: [Uncompressed Video Media Types](uncompressed-video-media-types.md)</span></span>

<span data-ttu-id="40d2b-111">En el caso de las secuencias comprimidas (o *codificadas*), el códec define la definición de un tipo de medio completo.</span><span class="sxs-lookup"><span data-stu-id="40d2b-111">For compressed (or *encoded*) streams, the definition of a complete media type is defined by the codec.</span></span> <span data-ttu-id="40d2b-112">Sin embargo, si se conoce algún atributo de tipo sin comprimir para el flujo comprimido, estos valores deben incluirse en el tipo de medio del flujo comprimido.</span><span class="sxs-lookup"><span data-stu-id="40d2b-112">However, if any uncompressed type attributes are known for the compressed stream, these values should be included in the media type for the compressed stream.</span></span> <span data-ttu-id="40d2b-113">Por ejemplo, si se conoce el tamaño del marco, establezca el atributo de [**\_ tamaño de \_ marco \_ MF MT**](mf-mt-frame-size-attribute.md) en el tipo de medio, aunque técnicamente un flujo comprimido no tiene un tamaño de marco.</span><span class="sxs-lookup"><span data-stu-id="40d2b-113">For example, if the frame size is known, set the [**MF\_MT\_FRAME\_SIZE**](mf-mt-frame-size-attribute.md) attribute on the media type, even though technically a compressed stream does not have a frame size.</span></span>

## <a name="partial-media-types"></a><span data-ttu-id="40d2b-114">Tipos de medios parciales</span><span class="sxs-lookup"><span data-stu-id="40d2b-114">Partial Media Types</span></span>

<span data-ttu-id="40d2b-115">Faltan uno o varios de los atributos necesarios para un tipo de medio completo en un tipo de medio *parcial* .</span><span class="sxs-lookup"><span data-stu-id="40d2b-115">A *partial* media type is lacks one or more of the attributes needed for a complete media type.</span></span> <span data-ttu-id="40d2b-116">Al enumerar los posibles tipos de medios, un componente de Microsoft Media Foundation puede dejar un valor sin establecer para indicar que puede controlar cualquier valor.</span><span class="sxs-lookup"><span data-stu-id="40d2b-116">When enumerating possible media types, a Microsoft Media Foundation component may leave a value unset, to indicate that it can handle any value.</span></span> <span data-ttu-id="40d2b-117">Por ejemplo, un procesador de vídeo podría dejar el atributo de [**\_ \_ \_ velocidad de fotogramas MF MT**](mf-mt-frame-rate-attribute.md) sin establecer, para indicar que puede controlar cualquier velocidad de fotogramas y realizará una conversión de velocidad de fotogramas si es necesario.</span><span class="sxs-lookup"><span data-stu-id="40d2b-117">For example, a video processor might leave the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute unset, to indicate that it can handle any frame rate, and will perform a frame-rate conversion if necessary.</span></span>

<span data-ttu-id="40d2b-118">Si crea un tipo de medio parcial, debe incluir toda la información que sepa.</span><span class="sxs-lookup"><span data-stu-id="40d2b-118">If you create a partial media type, you should still include as much information as you know.</span></span> <span data-ttu-id="40d2b-119">Sin embargo, un tipo de medio no debe incluir información que sea incierto.</span><span class="sxs-lookup"><span data-stu-id="40d2b-119">However, a media type must not include information that is uncertain.</span></span> <span data-ttu-id="40d2b-120">Es mejor que falte información que equivocada.</span><span class="sxs-lookup"><span data-stu-id="40d2b-120">It is better for information to be missing than wrong.</span></span>

<span data-ttu-id="40d2b-121">Como mínimo, un tipo de medio parcial debe incluir solo dos atributos: [**\_ tipo de \_ versión \_ principal MF MT**](mf-mt-major-type-attribute.md) y [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="40d2b-121">At a minimum, a partial media type should include just two attributes: [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) and [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md).</span></span>

<span data-ttu-id="40d2b-122">A veces Media Foundation componentes deben proporcionar tipos de medios completos:</span><span class="sxs-lookup"><span data-stu-id="40d2b-122">Sometimes Media Foundation components must provide complete media types:</span></span>

-   <span data-ttu-id="40d2b-123">Los orígenes multimedia deben proporcionar tipos de salida completos.</span><span class="sxs-lookup"><span data-stu-id="40d2b-123">Media sources must provide complete output types.</span></span>
-   <span data-ttu-id="40d2b-124">Los descodificadores deben proporcionar tipos de salida completos, una vez establecido el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="40d2b-124">Decoders must provide complete output types, after the input type is set.</span></span> <span data-ttu-id="40d2b-125">Antes de que se establezca el tipo de entrada, un descodificador podría proporcionar un tipo de salida parcial.</span><span class="sxs-lookup"><span data-stu-id="40d2b-125">Before the input type is set, a decoder might provide a partial output type.</span></span>
-   <span data-ttu-id="40d2b-126">Los codificadores deben proporcionar tipos de entrada completos, una vez establecido el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="40d2b-126">Encoders must provide complete input types, after the output type is set.</span></span> <span data-ttu-id="40d2b-127">Antes de que se establezca el tipo de salida, un codificador podría proporcionar un tipo de entrada parcial.</span><span class="sxs-lookup"><span data-stu-id="40d2b-127">Before the output type is set, an encoder might provide a partial input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40d2b-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40d2b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40d2b-129">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="40d2b-129">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



