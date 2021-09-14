---
description: Corrección de relación de aspecto
ms.assetid: 0ed6010b-9168-44b1-be49-0c9d5d77ce3f
title: Corrección de relación de aspecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2460f7ecce1513394d941eafe8bdf8a7a80e9727
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162254"
---
# <a name="aspect-ratio-correction"></a>Corrección de relación de aspecto

Este tema se aplica a Windows XP Service Pack 2 o posterior.

En el modo de combinación, vmr puede cambiar el tamaño del vídeo a la relación de aspecto correcta. (Excepción: vea [Combinación no cuadrada).](non-square-mixing.md) Esto puede requerir la extensión del vídeo si la relación de aspecto preferida no es la misma que la relación de aspecto físico de la imagen. Por ejemplo, el formato de vídeo digital (DV) es de 720 x 480 píxeles (3:2), pero debe mostrarse con una relación de aspecto de 4:3.

VmR admite dos comportamientos diferentes para la corrección de la relación de aspecto:

-   Ajuste el tamaño horizontal o vertical para que la imagen siempre se ajuste, nunca se rebaje. Este es ahora el comportamiento predeterminado.
-   Ajuste el tamaño horizontal, ya sea ajustando o reduciendo el vídeo.

Dado que el segundo comportamiento (solo ajuste horizontal) puede implicar la reducción del vídeo, la imagen de salida puede tener menos resolución. Por esta razón, se prefiere el primer comportamiento. Por ejemplo, en el caso del vídeo de 720 x 480 con una relación de aspecto de 4:3, el comportamiento predeterminado genera una imagen de 720 x 550, mientras que el ajuste horizontal genera una imagen de 640 x 480 más pequeña.

**VMR-7:** para establecer la preferencia de corrección de relación de aspecto, llame a [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect). Establezca la marca MIXERPref ARAdjustXorY para el comportamiento predeterminado o desactive esta marca solo para \_ el ajuste horizontal.

**VMR-9:** para establecer la preferencia de corrección de relación de aspecto, llame a [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs). Establezca la marca MIXERPref9 ARAdjustXorY para el comportamiento predeterminado o desactive esta marca solo para \_ el ajuste horizontal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del modo de combinación de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



