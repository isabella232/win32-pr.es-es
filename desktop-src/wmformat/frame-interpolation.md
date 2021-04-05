---
title: Interpolación de fotogramas
description: Interpolación de fotogramas
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- SDK de Windows Media Format, interpolación de marcos
- códecs, interpolación de fotogramas
- interpolación de fotogramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077318"
---
# <a name="frame-interpolation"></a><span data-ttu-id="8d33d-106">Interpolación de fotogramas</span><span class="sxs-lookup"><span data-stu-id="8d33d-106">Frame Interpolation</span></span>

<span data-ttu-id="8d33d-107">La interpolación de fotogramas es el proceso de creación de fotogramas de vídeo intermedios basados en los datos de dos fotogramas consecutivos de vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="8d33d-107">Frame interpolation is the process of creating intermediate video frames based on the data in two consecutive frames of encoded video.</span></span> <span data-ttu-id="8d33d-108">En efecto, la interpolación de fotogramas aumenta la [*velocidad de fotogramas*](wmformat-glossary.md) del vídeo codificado en el momento de la descodificación.</span><span class="sxs-lookup"><span data-stu-id="8d33d-108">In effect, frame interpolation increases the [*frame rate*](wmformat-glossary.md) of encoded video at the time of decoding.</span></span> <span data-ttu-id="8d33d-109">Puede usar la interpolación de fotogramas para mejorar la suavidad de la reproducción de secuencias de vídeo con velocidades de fotogramas bajas.</span><span class="sxs-lookup"><span data-stu-id="8d33d-109">You can use frame interpolation to improve the smoothness of playback for video streams with low frame rates.</span></span>

<span data-ttu-id="8d33d-110">Dado que se trata de una característica de descodificación, no implica ninguna opción de codificación especial y no agrega ninguna sobrecarga al contenido.</span><span class="sxs-lookup"><span data-stu-id="8d33d-110">Because this is a decoding feature, it does not involve any special encoding options and adds no overhead to the content.</span></span> <span data-ttu-id="8d33d-111">La interpolación de fotogramas se especifica como una configuración de salida en el objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="8d33d-111">Frame interpolation is specified as an output setting in the reader object.</span></span>

<span data-ttu-id="8d33d-112">Solo el códec de Windows Media Video 9 admite la interpolación de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="8d33d-112">Only the Windows Media Video 9 codec supports frame interpolation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d33d-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8d33d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d33d-114">**Características del códec**</span><span class="sxs-lookup"><span data-stu-id="8d33d-114">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="8d33d-115">**IWMReaderAdvanced2::SetOutputSetting**</span><span class="sxs-lookup"><span data-stu-id="8d33d-115">**IWMReaderAdvanced2::SetOutputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[<span data-ttu-id="8d33d-116">**Configuración de salida**</span><span class="sxs-lookup"><span data-stu-id="8d33d-116">**Output Settings**</span></span>](output-settings.md)
</dt> </dl>

 

 




