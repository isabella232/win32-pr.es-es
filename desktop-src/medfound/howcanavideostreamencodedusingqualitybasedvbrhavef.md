---
description: ¿Cómo puede una secuencia de vídeo codificada con VBR basada en la calidad tener menos fotogramas que la secuencia original?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: ¿Cómo puede una secuencia de vídeo codificada con VBR basada en la calidad tener menos fotogramas que la secuencia original?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276379"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a><span data-ttu-id="6dde8-103">¿Cómo puede una secuencia de vídeo codificada con VBR basada en la calidad tener menos fotogramas que la secuencia original?</span><span class="sxs-lookup"><span data-stu-id="6dde8-103">How can a video stream encoded using quality-based VBR have fewer frames than the original stream?</span></span>

<span data-ttu-id="6dde8-104">El número de fotogramas de una secuencia codificada puede ser menor que el número de fotogramas del original por uno de estos dos motivos: fotogramas duplicados y fotogramas descartados.</span><span class="sxs-lookup"><span data-stu-id="6dde8-104">The frame count of an encoded stream can be lower than the frame count of the original for one of two reasons: duplicate frames and dropped frames.</span></span>

<span data-ttu-id="6dde8-105">El codificador no genera normalmente fotogramas que son duplicados exactos del fotograma anterior.</span><span class="sxs-lookup"><span data-stu-id="6dde8-105">The encoder does not normally produce frames that are exact duplicates of the previous frame.</span></span> <span data-ttu-id="6dde8-106">Si necesita tener un ejemplo para cada fotograma (esto es necesario para algunos contenedores, por ejemplo), puede configurar el codificador para que genere fotogramas "ficticios" estableciendo la propiedad [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="6dde8-106">If you need to have a sample for every frame (this is required by some containers, for example), you can configure the encoder to produce "dummy" frames by setting the [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="6dde8-107">El codificador quita los fotogramas cuando no puede codificar todos los marcos sin desbordar el búfer.</span><span class="sxs-lookup"><span data-stu-id="6dde8-107">The encoder drops frames when it cannot encode all of the frames without overflowing the buffer.</span></span> <span data-ttu-id="6dde8-108">Los fotogramas quitados afectan a la calidad de la secuencia, no los fotogramas duplicados.</span><span class="sxs-lookup"><span data-stu-id="6dde8-108">Dropped frames affect the quality of the stream, duplicate frames do not.</span></span>

<span data-ttu-id="6dde8-109">Puede obtener estadísticas de fotogramas del codificador para determinar si se han quitado los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6dde8-109">You can get frame statistics from the encoder to determine whether frames have been dropped.</span></span> <span data-ttu-id="6dde8-110">Para obtener más información, vea [obtener estadísticas de codificación](gettingencodingstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="6dde8-110">For more information, see [Getting Encoding Statistics](gettingencodingstatistics.md).</span></span>

<span data-ttu-id="6dde8-111">Normalmente, las secuencias VBR basadas en la calidad solo tendrán menos fotogramas que el original si hay fotogramas duplicados (porque la velocidad de bits no está restringida).</span><span class="sxs-lookup"><span data-stu-id="6dde8-111">Typically, quality-based VBR streams will only have fewer frames than the original if there are duplicate frames (because the bit rate is not constrained).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dde8-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6dde8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dde8-113">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="6dde8-113">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



