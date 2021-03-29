---
description: VMR requisitos del sistema
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: VMR requisitos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277581"
---
# <a name="vmr-system-requirements"></a><span data-ttu-id="8bb1e-103">VMR requisitos del sistema</span><span class="sxs-lookup"><span data-stu-id="8bb1e-103">VMR System Requirements</span></span>

<span data-ttu-id="8bb1e-104">La VMR utiliza exclusivamente las capacidades de procesamiento de gráficos de la tarjeta de presentación del equipo; la VMR no realiza ninguna fusión ni representación de vídeo con el procesador del host, porque para ello afectaría en gran medida a la velocidad de fotogramas y la calidad del vídeo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-104">The VMR uses the graphics-processing capabilities of the computer's display card exclusively; the VMR does not perform any blending or rendering of video using the host processor, because to do so would greatly impact the frame rate and quality of the video being displayed.</span></span> <span data-ttu-id="8bb1e-105">Cuando se aprovechan las nuevas características que ofrece la VMR, especialmente la combinación de varias secuencias de vídeo o imágenes de aplicaciones, el rendimiento general obtenido depende en gran medida de las capacidades de la tarjeta gráfica que se usa en el equipo.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-105">When taking advantage of the new features offered by the VMR, particularly blending of multiple video streams and/or application images, the overall performance obtained is highly dependent on the capabilities of the graphics card being used on the computer.</span></span> <span data-ttu-id="8bb1e-106">Las tarjetas gráficas que funcionan bien con la VMR tienen la siguiente compatibilidad de hardware integrada:</span><span class="sxs-lookup"><span data-stu-id="8bb1e-106">Graphics cards that perform well with the VMR have the following hardware support built into them:</span></span>

-   <span data-ttu-id="8bb1e-107">Compatibilidad con las superficies de textura de Direct3D de YUV y "no potencia de 2".</span><span class="sxs-lookup"><span data-stu-id="8bb1e-107">Support for YUV and "non-power of 2" Direct3D texture surfaces.</span></span>
-   <span data-ttu-id="8bb1e-108">La capacidad de StretchBlt de las superficies YUV a RGB DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-108">The ability to StretchBlt from YUV to RGB DirectDraw surfaces.</span></span>
-   <span data-ttu-id="8bb1e-109">Al menos 16 MB de memoria de vídeo si se van a combinar varias secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-109">At least 16MB of video memory if multiple video streams are to be blended together.</span></span> <span data-ttu-id="8bb1e-110">La cantidad real de memoria necesaria depende del tamaño de la imagen de las secuencias de vídeo y la resolución del modo de presentación que se está usando.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-110">The actual amount of memory required is dependent on the image size of the video streams and resolution of the display mode being used.</span></span>
-   <span data-ttu-id="8bb1e-111">Compatibilidad con una superposición de RGB o la capacidad de fusionar con una superficie de superposición de YUV.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-111">Support for an RGB overlay or the ability to blend to a YUV overlay surface.</span></span>
-   <span data-ttu-id="8bb1e-112">Vídeo acelerado por hardware (compatibilidad con la aceleración de vídeo de DirectX).</span><span class="sxs-lookup"><span data-stu-id="8bb1e-112">Hardware-accelerated video (support for DirectX Video Acceleration) decoding.</span></span>
-   <span data-ttu-id="8bb1e-113">Tasas de relleno de alto nivel de píxeles.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-113">High pixel fill rates.</span></span>

> [!Note]  
> <span data-ttu-id="8bb1e-114">La VMR requiere que el monitor de sistema se establezca para una profundidad de color de al menos 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-114">The VMR requires that the system monitor be set for a color depth of at least 16 bits.</span></span> <span data-ttu-id="8bb1e-115">No se puede poner VMR en un estado de ejecución si el monitor está configurado para 256 colores.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-115">The VMR cannot be put into a run state if the monitor is set for 256 colors.</span></span> <span data-ttu-id="8bb1e-116">Además, algunas tarjetas de vídeo no pueden realizar operaciones de Direct3D cuando la pantalla se establece en 24 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-116">Also, some video cards cannot perform Direct3D operations when the display is set to 24 bits per pixel.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8bb1e-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bb1e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bb1e-118">Acerca de la presentación de la combinación de vídeo</span><span class="sxs-lookup"><span data-stu-id="8bb1e-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



