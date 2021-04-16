---
description: Usar el códec Windows Media Audio Voice
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Usar el códec Windows Media Audio Voice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d636bd97b76e23acc6b68da87c8a206b17dea60a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547315"
---
# <a name="using-the-windows-media-audio-voice-codec"></a><span data-ttu-id="a9cce-103">Usar el códec Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="a9cce-103">Using the Windows Media Audio Voice Codec</span></span>

<span data-ttu-id="a9cce-104">El códec Windows Media Audio Voice proporciona compresión de baja velocidad de bits optimizada para audio que contiene voz.</span><span class="sxs-lookup"><span data-stu-id="a9cce-104">The Windows Media Audio Voice codec provides low bit-rate compression optimized for audio containing speech.</span></span> <span data-ttu-id="a9cce-105">La capacidad del códec para generar ejemplos pequeños se debe al intervalo de frecuencias limitado de los sonidos de la voz humana.</span><span class="sxs-lookup"><span data-stu-id="a9cce-105">The ability of the codec to produce such small samples is due to the limited frequency range of the sounds of the human voice.</span></span> <span data-ttu-id="a9cce-106">Esta optimización significa que un codificador de voz dedicado crea una salida de mala calidad para el contenido que contiene sonidos más complicados, como música.</span><span class="sxs-lookup"><span data-stu-id="a9cce-106">This optimization means that a dedicated voice encoder creates poor-quality output for content that contains more complicated sounds, like music.</span></span> <span data-ttu-id="a9cce-107">Sin embargo, el códec de voz de Windows Media Audio compensa este posible problema de calidad al proporcionar modos independientes de voz, música y contenido mixto.</span><span class="sxs-lookup"><span data-stu-id="a9cce-107">However, the Windows Media Audio Voice codec compensates for this potential quality issue by providing separate modes for voice, music, and mixed content.</span></span> <span data-ttu-id="a9cce-108">El códec analiza el contenido mixto para determinar el modo que se va a utilizar para cada parte del archivo.</span><span class="sxs-lookup"><span data-stu-id="a9cce-108">The codec analyzes mixed content to determine which mode to use for each portion of the file.</span></span>

<span data-ttu-id="a9cce-109">El códec de Windows Media Audio Voice se implementa en el objeto Encoder identificado por el identificador de clase CLSID \_ CWMSPEncMediaObject2 y en el objeto descodificador identificado por el identificador de clase CLSID \_ CWMSPDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="a9cce-109">The Windows Media Audio Voice codec is implemented in the encoder object identified by the class identifier CLSID\_CWMSPEncMediaObject2, and in the decoder object identified by the class identifier CLSID\_CWMSPDecMediaObject.</span></span> <span data-ttu-id="a9cce-110">La etiqueta de formato de los tipos de medios que usan este códec es 0x00A.</span><span class="sxs-lookup"><span data-stu-id="a9cce-110">The format tag of media types using this codec is 0x00A.</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="a9cce-111">Configurar el codificador</span><span class="sxs-lookup"><span data-stu-id="a9cce-111">Configuring the Encoder</span></span>

<span data-ttu-id="a9cce-112">El codificador de voz admite tres modos: voz, música y mixto.</span><span class="sxs-lookup"><span data-stu-id="a9cce-112">The voice encoder supports three modes: speech, music, and mixed.</span></span> <span data-ttu-id="a9cce-113">Cada modo está optimizado para obtener los mejores resultados para ese tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="a9cce-113">Each mode is optimized to get the best results for that type of content.</span></span> <span data-ttu-id="a9cce-114">Puede configurar el modo del codificador de voz mediante los métodos de **IPropertyStore** para establecer la propiedad MFPKEY de [ \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="a9cce-114">You can configure the mode of the voice encoder by using the methods of **IPropertyStore** to set the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property.</span></span>

<span data-ttu-id="a9cce-115">Cuando se configura para contenido mixto, el códec de Windows Media Audio Voice detectará automáticamente el paso de música en el contenido.</span><span class="sxs-lookup"><span data-stu-id="a9cce-115">When configured for mixed content, the Windows Media Audio Voice codec will automatically detect passages of music in the content.</span></span> <span data-ttu-id="a9cce-116">Si no está satisfecho con los resultados, puede especificar la ubicación de la música en el contenido mediante una lista de decisiones de edición (EDL).</span><span class="sxs-lookup"><span data-stu-id="a9cce-116">If you are not satisfied with the results, you can specify the location of music in the content using an editing decision list (EDL).</span></span> <span data-ttu-id="a9cce-117">Para obtener más información, consulte [uso de una lista de decisiones de edición para la codificación de voz](usingavoiceeditingdecisionlist.md).</span><span class="sxs-lookup"><span data-stu-id="a9cce-117">For more information, see [Using an Editing Decision List for Encoding Voice](usingavoiceeditingdecisionlist.md).</span></span>

<span data-ttu-id="a9cce-118">A diferencia de los otros codificadores de audio, puede establecer el valor de la ventana de búfer para el contenido de voz mediante la propiedad [MFPKEY \_ WMAVOICE \_ enc \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="a9cce-118">Unlike the other audio encoders, you can set the buffer window value for voice content by using the [MFPKEY\_WMAVOICE\_ENC\_BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) property.</span></span> <span data-ttu-id="a9cce-119">Sin embargo, los valores predeterminados deben funcionar correctamente en la mayoría de los casos.</span><span class="sxs-lookup"><span data-stu-id="a9cce-119">However, the default values should work fine in most cases.</span></span>

> [!Note]  
>    <span data-ttu-id="a9cce-120">Al configurar el codificador de voz, es muy importante que establezca el tipo de salida antes de establecer el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a9cce-120">When configuring the voice encoder, it is very important that you set the output type before you set the input type.</span></span> <span data-ttu-id="a9cce-121">Este es el orden recomendado de las operaciones para todos los códecs de audio, pero el codificador de voz puede informar de los tipos de salida erróneos si se establece una entrada cuando se llama a **IMediaObject:: GetOutputType** o **IMFTransform:: GetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="a9cce-121">This is the recommended order of operations for all of the audio codecs, but the voice encoder can report erroneous output types if an input is set when you call **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

 

## <a name="decoding"></a><span data-ttu-id="a9cce-122">Descodificación</span><span class="sxs-lookup"><span data-stu-id="a9cce-122">Decoding</span></span>

<span data-ttu-id="a9cce-123">No hay ningún requisito especial para descodificar el audio de voz.</span><span class="sxs-lookup"><span data-stu-id="a9cce-123">There are no special requirements for decoding voice audio.</span></span> <span data-ttu-id="a9cce-124">Obtener más información, consulte [configuración de la descodificación de audio](configuringaudiodecoding.md).</span><span class="sxs-lookup"><span data-stu-id="a9cce-124">Form more information, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9cce-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9cce-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9cce-126">Trabajar con audio</span><span class="sxs-lookup"><span data-stu-id="a9cce-126">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



