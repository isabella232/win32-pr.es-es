---
description: ¿Por qué el codificador de vídeo rechaza un formato de salida que intento establecer, cuando recupero el formato del mismo objeto?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: ¿Por qué el codificador de vídeo rechaza un formato de salida que intento establecer, cuando recupero el formato del mismo objeto?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680908ec814fe322585c1ac97d3bb79deddaf034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082427"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a><span data-ttu-id="74f2e-103">¿Por qué el codificador de vídeo rechaza un formato de salida que intento establecer, cuando recupero el formato del mismo objeto?</span><span class="sxs-lookup"><span data-stu-id="74f2e-103">Why does the video encoder reject an output format that I try to set, when I retrieved the format from the same object?</span></span>

<span data-ttu-id="74f2e-104">A diferencia de los tipos de salida del codificador de audio, las salidas admitidas enumeradas por los codificadores de vídeo no se completan tal y como se entregan.</span><span class="sxs-lookup"><span data-stu-id="74f2e-104">Unlike audio encoder output types, the supported outputs enumerated by the video encoders are not complete as delivered.</span></span> <span data-ttu-id="74f2e-105">Debe establecer la velocidad de bits de la secuencia en el miembro **dwBitrate** de la estructura **VIDEOINFOHEADER** para que coincida con el valor establecido para la propiedad [MFPKEY \_ RAVG](mfpkey-ravgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="74f2e-105">You must set the bit rate of the stream in the **dwBitrate** member of the **VIDEOINFOHEADER** structure to match the value set for the [MFPKEY\_RAVG](mfpkey-ravgproperty.md) property.</span></span>

<span data-ttu-id="74f2e-106">Una vez que todas las opciones estén establecidas de la manera que desee, debe recuperar los datos privados del códec y anexarlos a la estructura **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="74f2e-106">After all of the options are set the way that you want them, you must retrieve the codec private data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="74f2e-107">Para obtener más información, consulte [uso de datos privados de códecs de vídeo](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="74f2e-107">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="74f2e-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74f2e-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74f2e-109">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="74f2e-109">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



