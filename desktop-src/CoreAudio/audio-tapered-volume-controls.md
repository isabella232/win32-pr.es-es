---
description: Audio-Tapered controles de volumen
ms.assetid: 3b1adef5-40e9-4527-aa79-5a71f201fdfc
title: Audio-Tapered controles de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cca0879d27d0eba3d49ca22b019442f882bf917
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807478"
---
# <a name="audio-tapered-volume-controls"></a>Audio-Tapered controles de volumen

La interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) administra los controles de volumen con el número de audio cónico. Estos controles son idóneos para aplicaciones Windows que muestran controles deslizantes de volumen. Para un control deslizante de volumen que está vinculado a un control de volumen con inclinación de audio, cada cambio en la posición del control deslizante produce un cambio en la sonoridad percibida que es proporcional a la distancia recorrida por el control deslizante. En el caso de una distancia de desplazamiento determinada, la cantidad por la que aumenta o disminuye la sonoridad percibida es aproximadamente la misma, independientemente de si el movimiento del control deslizante se produce en la parte inferior, superior o intermedia del intervalo de movimiento del control deslizante. La sonoridad percibida varía aproximadamente de manera lineal con el logaritmo de la potencia de la señal de audio.

El término *cono de audio* hacía referencia originalmente a la forma cónica del elemento resistente en un potenciómetro que se usa como control de volumen en un dispositivo de electrónica de audio. Un elemento resistente con la inclinación de audio es más ancho en la posición del volumen cero y más estrecho en la posición máxima del volumen. El potenciómetro controla el nivel de voltaje de la señal de audio que el dispositivo reproduce a través de sus altavoces. La inclinación está diseñada para producir una relación lineal aproximadamente entre la posición del limpialunas del potenciómetro y la sonoridad percibida en los hablantes. La relación entre la posición del limpialunas y el voltaje en los altavoces no es lineal.

En cambio, un elemento resistente con un cono lineal tiene un ancho uniforme sobre el intervalo de movimiento del limpiaparabrisas del potenciómetro. Como resultado, el voltaje en los altavoces varía linealmente con la posición del limpiaparabrisas. La relación entre la posición del limpialunas y la sonoridad no es lineal.

Del mismo modo, una aplicación de Windows que muestra un control deslizante de volumen define una relación entre la posición del control deslizante y el nivel de la señal de salida en los altavoces. La relación puede, en efecto, ser cónica lineal o con un cono de audio.

En el diagrama siguiente se muestra la asignación de la posición del control deslizante al voltaje de salida y a la sonoridad percibida para un control de volumen con inclinación lineal.

![diagrama de salida de un control de volumen con inclinación lineal](images/taper1.jpg)

En el lado izquierdo del diagrama anterior, el nivel de voltaje de salida del convertidor de audio digital a analógico (DAC) aumenta de forma lineal a medida que el control deslizante de volumen se desplaza desde su posición mínima (con la etiqueta min) hasta su posición máxima (con la etiqueta Max). La etiqueta V<sub>FS</sub> en el eje vertical representa el voltaje de salida de la DAC a gran escala.

Sin embargo, la sonoridad percibida varía aproximadamente como el logaritmo de la potencia de la señal de audio, tal como se muestra en el lado derecho del diagrama anterior. Por lo tanto, el movimiento del control deslizante sobre un intervalo cerca del valor mínimo tiene como resultado un cambio relativamente grande en la sonoridad percibida, pero el movimiento del control deslizante sobre un intervalo del mismo ancho cerca del valor máximo produce un cambio relativamente pequeño en la sonoridad percibida.

En el lado derecho del diagrama anterior, la sonoridad en el eje vertical se mide en decibelios (dB) en relación con la configuración de energía a gran escala (en 0 decibelios). La curva de sonoridad forma una intersección con el eje vertical a menos infinito, pero solo la parte de la curva de 0 decibelios a – 96 decibelios aparece en el diagrama. La decisión de mostrar solo esta parte de la curva es algo arbitraria, pero – 96 decibelios representa la potencia en el nivel de salida siguiente a más bajo de una DAC de 16 bits con respecto a la potencia a gran escala. Este valor se calcula como 20<sup>.</sup> log ₁ ₀ (1/65535).

Dado que los pequeños cambios en la posición del control deslizante cerca del valor mínimo del diagrama anterior producen grandes cambios de sonoridad, es posible que el usuario tenga dificultades para controlar esta región. Los movimientos relativamente pequeños del control deslizante pueden extender el volumen por encima o por debajo del nivel deseado. Un control de volumen mejorado proporcionaría una relación más lineal entre la posición del control deslizante y la sonoridad.

En el diagrama siguiente se muestra la asignación de la posición del control deslizante al voltaje de salida y a la sonoridad percibida para un control de volumen con inclinación de audio.

![diagrama de salida para control de volumen con inclinación de audio](images/taper2.jpg)

Como se muestra en el lado derecho del diagrama anterior, la sonoridad percibida varía aproximadamente linealmente con los cambios en la posición del control deslizante. Para que esto suceda, el voltaje de la DAC debe variar de forma no lineal con la posición, tal como se muestra en el lado izquierdo del diagrama. La curva asymptotically se aproxima a 0 voltios a medida que el control deslizante se desplaza hacia la izquierda desde el valor máximo. El voltaje en la posición del control deslizante mínima es muy pequeño, pero puede que no sea exactamente cero.

Los siguientes métodos de la interfaz **IAudioEndpointVolume** usan valores de volumen que se miden en decibelios:

-   [**IAudioEndpointVolume::GetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevel)
-   [**IAudioEndpointVolume::GetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)

Estos métodos producen una relación lineal aproximadamente entre la configuración del volumen y la sonoridad percibida. El intervalo de volumen en decibelios de los controles de volumen administrados por estos métodos depende del dispositivo de punto de conexión de audio. Para determinar el intervalo de volumen de un dispositivo determinado, llame al método [**IAudioEndpointVolume:: GetVolumeRange**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange) .

Por el contrario, la configuración de volumen para los siguientes métodos de la interfaz **IAudioEndpointVolume** sigue una curva más decónica sobre el intervalo de volúmenes:

-   [**IAudioEndpointVolume::GetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::GetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevelscalar)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

En Windows Vista, estos métodos usan una curva que es intermedia entre la curva con inclinación de audio que se muestra en el diagrama anterior y una curva con inclinación lineal. Tenga en cuenta que la forma de la curva podría cambiar en versiones futuras de Windows. Los primeros cuatro métodos de la lista anterior expresan los niveles de volumen como valores normalizados en el intervalo de 0,0 (volumen mínimo) a 1,0 (volumen máximo). Para los dos últimos métodos de la lista, llame al método [**IAudioEndpointVolume:: GetVolumeStepInfo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo) para obtener el número de pasos en el intervalo de volumen.

Las siguientes interfaces usan curvas con inclinación lineal para su configuración de volumen:

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)
-   [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)

Para obtener más información acerca de estas interfaces, vea [control de volumen de sesión](session-volume-controls.md). Y para obtener información sobre los intervalos de volumen y los niveles de volumen predeterminados en las distintas versiones de Windows, consulte [configuración predeterminada del volumen de audio](/windows-hardware/drivers/audio/default-audio-volume-settings).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles de volumen](volume-controls.md)
</dt> </dl>

 

 
