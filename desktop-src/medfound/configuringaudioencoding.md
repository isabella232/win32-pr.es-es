---
description: Configuración de la codificación de audio
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Configuración de la codificación de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47595f440d10ad0d3c5695f117204f357035d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275140"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a><span data-ttu-id="ee648-103">Configuración de la codificación de audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="ee648-103">Configuring Audio Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="ee648-104">El codificador Windows Media Audio enumera todos los tipos de salida admitidos en su forma completa.</span><span class="sxs-lookup"><span data-stu-id="ee648-104">The Windows Media Audio encoder enumerates all of its supported output types in their complete form.</span></span> <span data-ttu-id="ee648-105">Recupere el tipo que desee llamando a **IMediaObject:: GetOutputType** o **IMFTransform:: GetAvailableOutputType** y, a continuación, establezca el tipo recuperado, sin modificar, como el tipo de salida llamando a **IMediaObject:: SetOutputType** o **IMFTransform:: SetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="ee648-105">Retrieve the type that you want by calling **IMediaObject::GetOutputType** or **IMFTransform::GetAvailableOutputType**, and then set the retrieved type, unaltered, as the output type by calling **IMediaObject::SetOutputType** or **IMFTransform::SetOutputType**.</span></span>

<span data-ttu-id="ee648-106">Los tipos de medios de salida que admite el codificador de audio cambian a medida que se configuran las propiedades del codificador.</span><span class="sxs-lookup"><span data-stu-id="ee648-106">The output media types supported by the audio encoder change as encoder properties are configured.</span></span> <span data-ttu-id="ee648-107">Debe configurar todas las propiedades del codificador que desee usar antes de enumerar el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="ee648-107">You must configure all of the encoder properties you want to use before you enumerate the output type.</span></span>

<span data-ttu-id="ee648-108">Los codificadores de audio admiten los modos de dos pasos y VBR, pero se configuran de forma diferente que para el vídeo.</span><span class="sxs-lookup"><span data-stu-id="ee648-108">Two-pass and VBR modes are supported by the audio encoders, but are configured differently than for video.</span></span> <span data-ttu-id="ee648-109">Para obtener más información, consulte [enumeración de tipos de audio para modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="ee648-109">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="ee648-110">Los tipos de entrada admitidos por el codificador de audio no estarán disponibles hasta que se establezca el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="ee648-110">The input types supported by the audio encoder are not available until you set the output type.</span></span> <span data-ttu-id="ee648-111">Si llama a **IMediaObject:: GetInputType** o **IMFTransform:: GetInputType** antes de establecer un tipo de salida, el método devuelve DMO \_ e \_ no hay \_ más \_ elementos o MFT \_ e \_ no hay \_ más \_ tipos respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ee648-111">If you call **IMediaObject::GetInputType** or **IMFTransform::GetInputType** before setting an output type, the method returns DMO\_E\_NO\_MORE\_ITEMS or MFT\_E\_NO\_MORE\_TYPES respectively.</span></span> <span data-ttu-id="ee648-112">Una vez establecido el tipo de salida, el codificador enumera los tipos de entrada que admite para el tipo de salida seleccionado.</span><span class="sxs-lookup"><span data-stu-id="ee648-112">After the output type is set, the encoder enumerates the input types that it supports for the selected output type.</span></span>

<span data-ttu-id="ee648-113">El codificador de Windows Media Audio no realiza ningún muestreo de audio.</span><span class="sxs-lookup"><span data-stu-id="ee648-113">No audio resampling is performed by the Windows Media Audio encoder.</span></span> <span data-ttu-id="ee648-114">Esto significa que el tipo de salida del codificador y el tipo de entrada del codificador deben tener el mismo número de canales, bits por muestra y velocidad de muestra.</span><span class="sxs-lookup"><span data-stu-id="ee648-114">This means that the encoder output type and the encoder input type must have the same number of channels, bits per sample, and sample rate.</span></span> <span data-ttu-id="ee648-115">Para obtener más información, vea [Buscar tipos de salida del codificador de audio](findingaudioencoderoutputtypes.md).</span><span class="sxs-lookup"><span data-stu-id="ee648-115">For more information, see [Finding Audio Encoder Output Types](findingaudioencoderoutputtypes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="ee648-116">Cada tipo de salida enumerado por el codificador de audio contiene una estructura **WAVEFORMATEX** (señalada por el **tipo de \_ medio am \_ . pbFormat**) con datos extendidos anexados.</span><span class="sxs-lookup"><span data-stu-id="ee648-116">Each output type enumerated by the audio encoder contains a **WAVEFORMATEX** structure (pointed to by **AM\_MEDIA\_TYPE.pbFormat**) with extended data appended to it.</span></span> <span data-ttu-id="ee648-117">**WAVEFORMATEX. cbSize** especifica el tamaño de los datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="ee648-117">The size of the extended data is specified by **WAVEFORMATEX.cbSize**.</span></span> <span data-ttu-id="ee648-118">Estos datos se deben mantener con el contenido codificado para que se pueda entregar al descodificador.</span><span class="sxs-lookup"><span data-stu-id="ee648-118">This data must be kept with the encoded content so that it can be delivered to the decoder.</span></span> <span data-ttu-id="ee648-119">No se puede descomprimir el contenido sin los datos de formato extendido.</span><span class="sxs-lookup"><span data-stu-id="ee648-119">The content cannot be decompressed without the extended format data.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ee648-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee648-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee648-121">Trabajar con audio</span><span class="sxs-lookup"><span data-stu-id="ee648-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



