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
# <a name="using-decimation-to-optimize-mixing-performance"></a>Usar la Diezmación para optimizar el rendimiento de combinación

> [!IMPORTANT]
> La optimización descrita en esta sección depende en gran medida del hardware subyacente. A menos que pueda garantizar el tipo de hardware de gráficos que se utilizará con la aplicación, puede degradar gravemente la apariencia de la imagen de vídeo.

 

HDTV requiere una gran cantidad de potencia de procesamiento, que en la mayoría de los sistemas se proporciona principalmente mediante la tarjeta gráfica. Pero incluso si la tarjeta gráfica y el descodificador pueden admitir resoluciones de 1920 x 1080, es posible que el monitor no tenga siempre el monitor establecido en esta resolución. En este caso, se necesita el chip de gráficos para crear una imagen 1920 x 1080 y, a continuación, reducir la resolución antes de enviarla al búfer de fotogramas.

Dado que se trata de un desperdicio de la potencia de procesamiento, el VMR proporciona una manera de diezmar (reducir) la imagen en el momento en que se representa en la superficie de DirectDraw. Esto elimina la copia de memoria adicional requerida si se tiene que cambiar el tamaño de la imagen después de representarla.

**VMR-7:** Para habilitar la diezmación, llame a [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) con la \_ marca DecimateOutput de MixerPref.

**VMR-9:** Para habilitar la diezmación, llame a [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con la \_ marca DecimateOutput de MixerPref9.

Se debe llamar al método **SetMixingPrefs** antes de que se conecte el VMR. Las marcas de preferencia de combinación no se pueden cambiar una vez que el gráfico se está ejecutando.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el modo de mezcla de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



