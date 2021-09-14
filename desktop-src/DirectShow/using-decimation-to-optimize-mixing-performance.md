---
description: Uso de Decimation para optimizar el rendimiento de la combinación
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Uso de Decimation para optimizar el rendimiento de la combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e9e4ddfe3bbba3eb5eeab91b7cf0e8b9cbfa03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127275068"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a>Uso de Decimation para optimizar el rendimiento de la combinación

> [!IMPORTANT]
> La optimización descrita en esta sección depende en gran medida del hardware subyacente. A menos que pueda garantizar qué tipo de hardware gráfico se usará con la aplicación, puede degradar gravemente la apariencia de la imagen de vídeo.

 

LA FUNCIÓN requiere una gran capacidad de procesamiento, que en sistemas más recientes se proporciona principalmente mediante la tarjeta gráfica. Pero incluso si la tarjeta gráfica y el descodificador pueden admitir resoluciones de 1920 x 1080, es posible que el usuario no siempre tenga el monitor establecido en esta resolución. En este caso, el chip gráfico es necesario para crear una imagen de 1920 x 1080 y, a continuación, reducir la resolución antes de enviarla al búfer de fotogramas.

Dado que se trata de una pérdida de potencia de procesamiento, el VMR proporciona una manera de diezmar (reducir) la imagen en el momento en que se representa en la superficie de DirectDraw. Esto elimina la copia de memoria adicional necesaria si es necesario cambiar el tamaño de la imagen una vez que se ha representado.

**VMR-7:** Para habilitar la decimación, llame a [**IVMRMixerControl::SetMixingPrefs con**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) la marca MixerPref \_ DecimateOutput.

**VMR-9:** Para habilitar la decimación, llame a [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con la marca MixerPref9 \_ DecimateOutput.

Se **debe llamar al método SetMixingPrefs** antes de que se conecte vmr. Las marcas de preferencias de combinación no se pueden cambiar una vez que se ejecuta el gráfico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del modo de combinación de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



