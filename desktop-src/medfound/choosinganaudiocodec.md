---
description: Elección de un códec de audio
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Elección de un códec de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b16dc0c6e65356f7d7e74b85b0671c2b41369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275146"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a><span data-ttu-id="2a8e4-103">Elección de un códec de audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="2a8e4-103">Choosing an Audio Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="2a8e4-104">El [**codificador Windows Media Audio**](windowsmediaaudioencoder.md) proporciona tres categorías de codificación de audio, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2a8e4-104">The [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md) provides three categories of audio encoding as shown in the following table.</span></span>



| <span data-ttu-id="2a8e4-105">Category</span><span class="sxs-lookup"><span data-stu-id="2a8e4-105">Category</span></span>                         | <span data-ttu-id="2a8e4-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="2a8e4-106">Purpose</span></span>                                                    |
|----------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2a8e4-107">Estándar Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="2a8e4-107">Windows Media Audio Standard</span></span>     | <span data-ttu-id="2a8e4-108">Compresión de audio de uso general.</span><span class="sxs-lookup"><span data-stu-id="2a8e4-108">General-purpose compression of audio.</span></span>                      |
| <span data-ttu-id="2a8e4-109">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="2a8e4-109">Windows Media Audio Professional</span></span> | <span data-ttu-id="2a8e4-110">Compresión de audio de varios canales y de alta definición.</span><span class="sxs-lookup"><span data-stu-id="2a8e4-110">Compressing multi-channel and high-definition audio.</span></span>       |
| <span data-ttu-id="2a8e4-111">Windows Media Audio sin pérdida de</span><span class="sxs-lookup"><span data-stu-id="2a8e4-111">Windows Media Audio Lossless</span></span>     | <span data-ttu-id="2a8e4-112">Comprimir el audio sin perder los datos originales.</span><span class="sxs-lookup"><span data-stu-id="2a8e4-112">Compressing audio without losing any of the original data.</span></span> |



 

<span data-ttu-id="2a8e4-113">La categoría estándar proporciona codificación de audio de uso general adecuada para diversos escenarios de reproducción.</span><span class="sxs-lookup"><span data-stu-id="2a8e4-113">The Standard category provides general-purpose audio encoding suitable for a variety of playback scenarios.</span></span> <span data-ttu-id="2a8e4-114">Por ejemplo, puede comprimir el audio a una velocidad de bits baja para la transmisión por secuencias a través de una red con ancho de banda limitado o para la representación en dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="2a8e4-114">For example, it can compress audio to a low bit rate for streaming over a network with limited bandwidth, or for rendering on portable devices.</span></span> <span data-ttu-id="2a8e4-115">En el otro extremo de la escala, puede generar contenido de audio comprimido para la reproducción de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="2a8e4-115">On the other end of the scale, it can produce compressed audio content for high-quality playback.</span></span> <span data-ttu-id="2a8e4-116">El énfasis de los algoritmos de codificación estándar es la música, pero también es adecuado para otro contenido de audio complejo.</span><span class="sxs-lookup"><span data-stu-id="2a8e4-116">The emphasis of the Standard encoding algorithms is on music, but they are suitable for other complex audio content as well.</span></span> <span data-ttu-id="2a8e4-117">La categoría estándar debe ser la predeterminada para el contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="2a8e4-117">The Standard category should be your default for audio content.</span></span> <span data-ttu-id="2a8e4-118">Las categorías Professional y Lossless deben usarse para satisfacer las necesidades específicas.</span><span class="sxs-lookup"><span data-stu-id="2a8e4-118">The Professional and Lossless categories should be used to meet specific needs.</span></span>

<span data-ttu-id="2a8e4-119">Un codificador independiente, el [**codificador de Windows Media Voice**](windowsmediaaudiovoiceencoder.md), proporciona compresión de voz.</span><span class="sxs-lookup"><span data-stu-id="2a8e4-119">A separate encoder, the [**Windows Media Voice Encoder**](windowsmediaaudiovoiceencoder.md), provides compression of speech.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a8e4-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a8e4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a8e4-121">Trabajar con audio</span><span class="sxs-lookup"><span data-stu-id="2a8e4-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



