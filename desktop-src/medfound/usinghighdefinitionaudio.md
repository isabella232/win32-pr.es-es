---
description: Usar High-Definition audio
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Usar High-Definition audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812578"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a><span data-ttu-id="dcc9c-103">Usar High-Definition audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="dcc9c-103">Using High-Definition Audio (Microsoft Media Foundation)</span></span>

<span data-ttu-id="dcc9c-104">El audio de alta definición, en el contexto de los códecs Windows Media Audio, es cualquier tipo de audio con más de dos canales o más de 16 bits por muestra.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-104">High-definition audio, in the context of the Windows Media Audio codecs, is any audio type with more than two channels or more than 16 bits per sample.</span></span> <span data-ttu-id="dcc9c-105">El audio de alta definición es compatible con las categorías Professional y Lossless del [codificador de Windows Media Audio](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="dcc9c-105">High-definition audio is supported by the Professional and Lossless categories of the [Windows Media Audio Encoder](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="dcc9c-106">Los tipos de audio sin comprimir de alta definición se definen mediante la estructura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dcc9c-106">Uncompressed high-definition audio types are defined using the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> <span data-ttu-id="dcc9c-107">**WAVEFORMATEXTENSIBLE** es una extensión estructurada de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dcc9c-107">**WAVEFORMATEXTENSIBLE** is a structured extension of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="dcc9c-108">Cuando se usa DMOs, el miembro de **formatType** de la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) que describe un tipo de audio de alta definición debe establecerse en WMCFORMAT \_ WaveFormatEx, del mismo modo que para el audio normal; no hay ningún identificador de formato especial para **WAVEFORMATEXTENSIBLE**.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-108">When you are using DMOs, the **formattype** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure that describes a high-definition audio type must be set to WMCFORMAT\_WaveFormatEx, just as it is for normal audio; there is no special format identifier for **WAVEFORMATEXTENSIBLE**.</span></span> <span data-ttu-id="dcc9c-109">Si un formato usa **WAVEFORMATEXTENSIBLE** , debe establecer el miembro **cbSize** de la estructura **WAVEFORMATEX** en 22.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-109">If a format uses **WAVEFORMATEXTENSIBLE** , you must set the **cbSize** member of the **WAVEFORMATEX** structure to 22.</span></span>

<span data-ttu-id="dcc9c-110">Al usar Media Foundation, puede crear el tipo de medio correcto a partir de una estructura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) mediante la función [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).</span><span class="sxs-lookup"><span data-stu-id="dcc9c-110">When using Media Foundation, you can construct the correct media type from a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure by using the function [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).</span></span>

<span data-ttu-id="dcc9c-111">Los tipos de salida de varios canales que admite el códec Windows Media Audio 10 Professional no usan [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), pero notifican el número correcto de canales y bits por muestra en la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dcc9c-111">The multi-channel output types supported by the Windows Media Audio 10 Professional codec do not use [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), but report the correct number of channels and bits per sample in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="dcc9c-112">Como con todos los tipos de audio que describen el contenido de Windows Media Audio comprimido, hay información adicional anexada a la estructura **WAVEFORMATEX** usada por el descodificador para la descompresión.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-112">As with all audio types describing compressed Windows Media Audio content, there is additional information appended to the **WAVEFORMATEX** structure that is used by the decoder for decompression.</span></span>

## <a name="decoding-high-definition-audio"></a><span data-ttu-id="dcc9c-113">Descodificar High-Definition audio</span><span class="sxs-lookup"><span data-stu-id="dcc9c-113">Decoding High-Definition Audio</span></span>

<span data-ttu-id="dcc9c-114">Para descodificar el audio de alta definición, debe establecer la propiedad [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-114">To decode high-definition audio, you must set the [MFPKEY\_WMADEC\_HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) property to VARIANT\_TRUE.</span></span> <span data-ttu-id="dcc9c-115">Si no se establece esta propiedad, el descodificador entregará contenido estéreo con un máximo de 16 bits por muestra, independientemente del formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-115">If this property is not set, the decoder will deliver stereo content with a maximum of 16 bits per sample, regardless of the compressed format.</span></span>

> [!Note]  
> <span data-ttu-id="dcc9c-116">El audio de alta definición solo es compatible con Windows XP, Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-116">High-definition audio is supported only for Windows XP, Windows Vista and later.</span></span> <span data-ttu-id="dcc9c-117">En versiones anteriores de Windows, Windows Media Audio contenido codificado con alta definición se representa como audio de dos canales con un máximo de 16 bits por muestra.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-117">On earlier versions of Windows, Windows Media Audio content encoded with high definition is rendered as two-channel audio with a maximum of 16 bits per sample.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="dcc9c-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dcc9c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcc9c-119">Trabajar con audio</span><span class="sxs-lookup"><span data-stu-id="dcc9c-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 
