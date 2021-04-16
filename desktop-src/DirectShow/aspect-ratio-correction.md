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
# <a name="aspect-ratio-correction"></a>Corrección de la relación de aspecto

Este tema se aplica a Windows XP Service Pack 2 o posterior.

En el modo de combinación, VMR ajusta el tamaño del vídeo a la relación de aspecto correcta. (Excepción: vea [combinación no cuadrada](non-square-mixing.md)). Esto puede requerir la ampliación del vídeo si la relación de aspecto preferida no es igual que la relación de aspecto física de la imagen. Por ejemplo, el formato de vídeo digital (DV) es 720 x 480 píxeles (3:2), pero debe mostrarse con una relación de aspecto de 4:3.

VMR admite dos comportamientos diferentes para la corrección de la relación de aspecto:

-   Ajuste el tamaño horizontal o vertical para que la imagen se ajuste siempre, nunca se reduzca. Este es ahora el comportamiento predeterminado.
-   Ajuste el tamaño horizontal, ya sea estirando o reduciendo el vídeo.

Dado que el segundo comportamiento (solo ajuste horizontal) puede implicar la reducción del vídeo, la imagen de salida puede tener menos resolución. Por esta razón, se prefiere el primer comportamiento. Por ejemplo, en el caso del vídeo 720 x 480 con una relación de aspecto de 4:3, el comportamiento predeterminado genera una imagen de 720 x 550, mientras que el ajuste horizontal produce una imagen de 640 x 480 más pequeña.

**VMR-7**: para establecer la preferencia de corrección de la relación de aspecto, llame a [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect). Establezca la \_ marca MixerPref ARAdjustXorY para el comportamiento predeterminado o desactive esta marca solo para el ajuste horizontal.

**VMR-9**: para establecer la preferencia de corrección de la relación de aspecto, llame a [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs). Establezca la \_ marca MixerPref9 ARAdjustXorY para el comportamiento predeterminado o desactive esta marca solo para el ajuste horizontal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el modo de mezcla de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



