---
description: Usar la Diezmación para optimizar el rendimiento de combinación
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Usar la Diezmación para optimizar el rendimiento de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e9e4ddfe3bbba3eb5eeab91b7cf0e8b9cbfa03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911077"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a><span data-ttu-id="720a6-103">Usar la Diezmación para optimizar el rendimiento de combinación</span><span class="sxs-lookup"><span data-stu-id="720a6-103">Using Decimation to Optimize Mixing Performance</span></span>

> [!IMPORTANT]
> <span data-ttu-id="720a6-104">La optimización descrita en esta sección depende en gran medida del hardware subyacente.</span><span class="sxs-lookup"><span data-stu-id="720a6-104">The optimization described in this section is highly dependent on the underlying hardware.</span></span> <span data-ttu-id="720a6-105">A menos que pueda garantizar el tipo de hardware de gráficos que se utilizará con la aplicación, puede degradar gravemente la apariencia de la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="720a6-105">Unless you can guarantee what type of graphics hardware will be used with the application, it may seriously degrade the appearance of the video image.</span></span>

 

<span data-ttu-id="720a6-106">HDTV requiere una gran cantidad de potencia de procesamiento, que en la mayoría de los sistemas se proporciona principalmente mediante la tarjeta gráfica.</span><span class="sxs-lookup"><span data-stu-id="720a6-106">HDTV requires a lot of processing power, which on newer systems is provided mostly by the graphics card.</span></span> <span data-ttu-id="720a6-107">Pero incluso si la tarjeta gráfica y el descodificador pueden admitir resoluciones de 1920 x 1080, es posible que el monitor no tenga siempre el monitor establecido en esta resolución.</span><span class="sxs-lookup"><span data-stu-id="720a6-107">But even if the graphics card and the decoder can support resolutions of 1920x1080, the user may not always have their monitor set to this resolution.</span></span> <span data-ttu-id="720a6-108">En este caso, se necesita el chip de gráficos para crear una imagen 1920 x 1080 y, a continuación, reducir la resolución antes de enviarla al búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="720a6-108">In this case, the graphics chip is required to create a 1920 x 1080 image, and then reduce the resolution before sending it to the frame buffer.</span></span>

<span data-ttu-id="720a6-109">Dado que se trata de un desperdicio de la potencia de procesamiento, el VMR proporciona una manera de diezmar (reducir) la imagen en el momento en que se representa en la superficie de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="720a6-109">Since this is a waste of processing power, the VMR provides a way to decimate (reduce) the image at the time it is being rendered onto the DirectDraw surface.</span></span> <span data-ttu-id="720a6-110">Esto elimina la copia de memoria adicional requerida si se tiene que cambiar el tamaño de la imagen después de representarla.</span><span class="sxs-lookup"><span data-stu-id="720a6-110">This eliminates the extra memory copy required if the image has to be resized after it has been rendered.</span></span>

<span data-ttu-id="720a6-111">**VMR-7:** Para habilitar la diezmación, llame a [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) con la \_ marca DecimateOutput de MixerPref.</span><span class="sxs-lookup"><span data-stu-id="720a6-111">**VMR-7:** To enable decimation, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_DecimateOutput flag.</span></span>

<span data-ttu-id="720a6-112">**VMR-9:** Para habilitar la diezmación, llame a [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con la \_ marca DecimateOutput de MixerPref9.</span><span class="sxs-lookup"><span data-stu-id="720a6-112">**VMR-9:** To enable decimation, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_DecimateOutput flag.</span></span>

<span data-ttu-id="720a6-113">Se debe llamar al método **SetMixingPrefs** antes de que se conecte el VMR.</span><span class="sxs-lookup"><span data-stu-id="720a6-113">The **SetMixingPrefs** method must be called before the VMR is connected.</span></span> <span data-ttu-id="720a6-114">Las marcas de preferencia de combinación no se pueden cambiar una vez que el gráfico se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="720a6-114">The mixing preference flags cannot be changed once the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="720a6-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="720a6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="720a6-116">Usar el modo de mezcla de VMR</span><span class="sxs-lookup"><span data-stu-id="720a6-116">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



