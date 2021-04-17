---
description: Codificación de vídeo con compresión temporal
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Codificación de vídeo con compresión temporal (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706117"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a><span data-ttu-id="61990-103">Codificación de vídeo con compresión temporal (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="61990-103">Video Encoding with Temporal Compression (Microsoft Media Foundation)</span></span>

<span data-ttu-id="61990-104">Para lograr los mayores índices de compresión posibles, los códecs Windows Media Video utilizan la *compresión temporal*.</span><span class="sxs-lookup"><span data-stu-id="61990-104">To achieve the highest compression ratios possible, the Windows Media Video codecs use *temporal compression*.</span></span> <span data-ttu-id="61990-105">La compresión temporal es una técnica para reducir el tamaño de vídeo comprimido sin codificar cada fotograma como una imagen completa.</span><span class="sxs-lookup"><span data-stu-id="61990-105">Temporal compression is a technique of reducing compressed video size by not encoding each frame as a complete image.</span></span> <span data-ttu-id="61990-106">Los fotogramas que se codifican completamente (como una imagen estática) se denominan *fotogramas clave*.</span><span class="sxs-lookup"><span data-stu-id="61990-106">The frames that are encoded completely (like a static image) are called *key frames*.</span></span> <span data-ttu-id="61990-107">Todos los demás fotogramas del vídeo se representan mediante datos que especifican el cambio desde el último fotograma.</span><span class="sxs-lookup"><span data-stu-id="61990-107">All other frames in the video are represented by data specifying the change since the last frame.</span></span> <span data-ttu-id="61990-108">Estos fotogramas se denominan *fotogramas Delta*.</span><span class="sxs-lookup"><span data-stu-id="61990-108">These frames are called *delta frames*.</span></span>

<span data-ttu-id="61990-109">La cantidad de compresión que se puede lograr mediante la compresión temporal depende del contenido.</span><span class="sxs-lookup"><span data-stu-id="61990-109">The amount of compression that can be achieved using temporal compression depends upon the content.</span></span> <span data-ttu-id="61990-110">Si el vídeo es estático, sin mucho movimiento u otros cambios en la imagen, se pueden crear muchos fotogramas Delta para cada fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="61990-110">If the video is static, without a lot of motion or other changes in image, many delta frames can be created for each key frame.</span></span> <span data-ttu-id="61990-111">Los fotogramas más Delta que se usan, menor es el flujo de vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="61990-111">The more delta frames that are used, the smaller the encoded video stream.</span></span> <span data-ttu-id="61990-112">Sin embargo, si el vídeo es dinámico, con gran cantidad de movimiento o cambio de color, la ventaja de usar la compresión temporal es menor.</span><span class="sxs-lookup"><span data-stu-id="61990-112">However, if the video is dynamic, with lots of motion or changing colors, the benefit of using temporal compression is smaller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61990-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61990-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61990-114">Trabajar con vídeo</span><span class="sxs-lookup"><span data-stu-id="61990-114">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



