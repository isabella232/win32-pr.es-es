---
title: Configurar secuencias de captura de pantalla
description: Configurar secuencias de captura de pantalla
ms.assetid: 974e679f-0bf6-412b-9e80-43370de7605a
keywords:
- flujos, configurar secuencias de captura de pantalla
- códecs, configurar secuencias de captura de pantalla
- secuencias de captura de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8200c4a6e733c2bb7f908b79cb73dbb2c3244dc4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994924"
---
# <a name="configuring-screen-capture-streams"></a><span data-ttu-id="aa044-106">Configurar secuencias de captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="aa044-106">Configuring Screen Capture Streams</span></span>

<span data-ttu-id="aa044-107">Las secuencias que usan el códec de pantalla de Windows Media® vídeo 9 se configuran mediante aplicaciones de la misma manera que las secuencias de vídeo normales.</span><span class="sxs-lookup"><span data-stu-id="aa044-107">Streams that use the Windows Media® Video 9 Screen codec are configured by applications in the same way as normal video streams.</span></span> <span data-ttu-id="aa044-108">Sin embargo, si establece el nivel de complejidad de vídeo en 0, el escritor pasará por alto cualquier valor de calidad de vídeo establecido con [**IWMVideoMediaProps:: SetQuality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality).</span><span class="sxs-lookup"><span data-stu-id="aa044-108">However, if you set the video complexity level to 0, the writer will ignore any video quality value set with [**IWMVideoMediaProps::SetQuality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality).</span></span> <span data-ttu-id="aa044-109">Para obtener más información, vea [obtener buenos resultados con el códec de pantalla de Windows Media Video 9](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span><span class="sxs-lookup"><span data-stu-id="aa044-109">For more information, see [Getting Good Results with the Windows Media Video 9 Screen Codec](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa044-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa044-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa044-111">**Configuración de secuencias**</span><span class="sxs-lookup"><span data-stu-id="aa044-111">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="aa044-112">**Configuración común para todos los flujos**</span><span class="sxs-lookup"><span data-stu-id="aa044-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="aa044-113">**Configuración de secuencias de vídeo**</span><span class="sxs-lookup"><span data-stu-id="aa044-113">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




