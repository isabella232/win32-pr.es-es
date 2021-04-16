---
description: Corrección de la relación de aspecto
ms.assetid: 0ed6010b-9168-44b1-be49-0c9d5d77ce3f
title: Corrección de la relación de aspecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2460f7ecce1513394d941eafe8bdf8a7a80e9727
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659285"
---
# <a name="aspect-ratio-correction"></a><span data-ttu-id="0e410-103">Corrección de la relación de aspecto</span><span class="sxs-lookup"><span data-stu-id="0e410-103">Aspect Ratio Correction</span></span>

<span data-ttu-id="0e410-104">Este tema se aplica a Windows XP Service Pack 2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="0e410-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="0e410-105">En el modo de combinación, VMR ajusta el tamaño del vídeo a la relación de aspecto correcta.</span><span class="sxs-lookup"><span data-stu-id="0e410-105">In mixing mode, the VMR sizes the video to the correct aspect ratio.</span></span> <span data-ttu-id="0e410-106">(Excepción: vea [combinación no cuadrada](non-square-mixing.md)). Esto puede requerir la ampliación del vídeo si la relación de aspecto preferida no es igual que la relación de aspecto física de la imagen.</span><span class="sxs-lookup"><span data-stu-id="0e410-106">(Exception: See [Non-Square Mixing](non-square-mixing.md).) This may require stretching the video if the preferred aspect ratio is not the same as the image's physical aspect ratio.</span></span> <span data-ttu-id="0e410-107">Por ejemplo, el formato de vídeo digital (DV) es 720 x 480 píxeles (3:2), pero debe mostrarse con una relación de aspecto de 4:3.</span><span class="sxs-lookup"><span data-stu-id="0e410-107">For example, digital video (DV) format is 720 x 480 pixels (3:2) but should be displayed at a 4:3 aspect ratio.</span></span>

<span data-ttu-id="0e410-108">VMR admite dos comportamientos diferentes para la corrección de la relación de aspecto:</span><span class="sxs-lookup"><span data-stu-id="0e410-108">The VMR supports two different behaviors for aspect ratio correction:</span></span>

-   <span data-ttu-id="0e410-109">Ajuste el tamaño horizontal o vertical para que la imagen se ajuste siempre, nunca se reduzca.</span><span class="sxs-lookup"><span data-stu-id="0e410-109">Adjust either the horizontal or vertical size, so that the image is always stretched, never shrunk.</span></span> <span data-ttu-id="0e410-110">Este es ahora el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0e410-110">This is now the default behavior.</span></span>
-   <span data-ttu-id="0e410-111">Ajuste el tamaño horizontal, ya sea estirando o reduciendo el vídeo.</span><span class="sxs-lookup"><span data-stu-id="0e410-111">Adjust the horizontal size, either stretching or shrinking the video.</span></span>

<span data-ttu-id="0e410-112">Dado que el segundo comportamiento (solo ajuste horizontal) puede implicar la reducción del vídeo, la imagen de salida puede tener menos resolución.</span><span class="sxs-lookup"><span data-stu-id="0e410-112">Because the second behavior (horizontal adjustment only) may entail shrinking the video, the output image may have less resolution.</span></span> <span data-ttu-id="0e410-113">Por esta razón, se prefiere el primer comportamiento.</span><span class="sxs-lookup"><span data-stu-id="0e410-113">For this reason, the first behavior is preferred.</span></span> <span data-ttu-id="0e410-114">Por ejemplo, en el caso del vídeo 720 x 480 con una relación de aspecto de 4:3, el comportamiento predeterminado genera una imagen de 720 x 550, mientras que el ajuste horizontal produce una imagen de 640 x 480 más pequeña.</span><span class="sxs-lookup"><span data-stu-id="0e410-114">For example, in the case of 720 x 480 video at 4:3 aspect ratio, the default behavior produces a 720 x 550 image, while horizontal adjustment produces a smaller 640 x 480 image.</span></span>

<span data-ttu-id="0e410-115">**VMR-7**: para establecer la preferencia de corrección de la relación de aspecto, llame a [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect).</span><span class="sxs-lookup"><span data-stu-id="0e410-115">**VMR-7**: To set the aspect ratio correction preference, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect).</span></span> <span data-ttu-id="0e410-116">Establezca la \_ marca MixerPref ARAdjustXorY para el comportamiento predeterminado o desactive esta marca solo para el ajuste horizontal.</span><span class="sxs-lookup"><span data-stu-id="0e410-116">Set the MixerPref\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

<span data-ttu-id="0e410-117">**VMR-9**: para establecer la preferencia de corrección de la relación de aspecto, llame a [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs).</span><span class="sxs-lookup"><span data-stu-id="0e410-117">**VMR-9**: To set the aspect ratio correction preference, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs).</span></span> <span data-ttu-id="0e410-118">Establezca la \_ marca MixerPref9 ARAdjustXorY para el comportamiento predeterminado o desactive esta marca solo para el ajuste horizontal.</span><span class="sxs-lookup"><span data-stu-id="0e410-118">Set the MixerPref9\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e410-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e410-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e410-120">Usar el modo de mezcla de VMR</span><span class="sxs-lookup"><span data-stu-id="0e410-120">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



