---
description: Audio-Tapered de volumen
ms.assetid: 3b1adef5-40e9-4527-aa79-5a71f201fdfc
title: Audio-Tapered de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cca0879d27d0eba3d49ca22b019442f882bf917
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165130"
---
# <a name="audio-tapered-volume-controls"></a>Audio-Tapered de volumen

La [**interfaz IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) administra los controles de volumen que están en cinta de audio. Estos controles son adecuados para aplicaciones Windows que muestran controles deslizantes de volumen. Para un control deslizante de volumen que está asociado a un control de volumen con cinta de audio, cada cambio en la posición del control deslizante produce un cambio en la sonoridad percibida que es proporcional a la distancia recorrida por el control deslizante. Para una distancia de desplazamiento determinada, la cantidad por la que aumenta o disminuye la sonoridad percibida es aproximadamente la misma independientemente de si el movimiento del control deslizante se produce en la parte inferior, superior o central del intervalo de movimiento del control deslizante. La sonoridad percibida varía aproximadamente linealmente con el logaritmo de la potencia de señal de audio.

El término *taper* de audio se refiere originalmente a la forma cólera del elemento represivo en un cuadro de mandos que se usa como control de volumen en un dispositivo de electrónica de audio. Un elemento resistente con cinta de audio es más ancho en la posición de volumen cero y más estrecho en la posición de volumen máximo. Elometer controla el nivel de voltaje de la señal de audio que el dispositivo reproduce a través de sus altavoces. El tapering está diseñado para generar una relación aproximadamente lineal entre la posición del wiper del ofiómetro y la sonoridad percibida en los altavoces. La relación entre la posición del wiper y el voltaje de los altavoces no es lineal.

Por el contrario, un elemento resistente con un taper lineal tiene un ancho uniforme sobre el intervalo de movimiento del wiper del iiómetro. Como resultado, el voltaje en los altavoces varía linealmente con la posición del wiper. La relación entre la posición del wiper y la sonoridad no es lineal.

De forma similar, Windows aplicación que muestra un control deslizante de volumen define una relación entre la posición del control deslizante y el nivel de señal de salida en los altavoces. La relación puede, en efecto, estar en cinta lineal o en cinta de audio.

En el diagrama siguiente se muestra la asignación de la posición del control deslizante al voltaje de salida y a la sonoridad percibida para un control de volumen con cinta lineal.

![diagrama de salida para un control de volumen en cinta lineal](images/taper1.jpg)

En el lado izquierdo del diagrama anterior, el nivel de voltaje de salida del convertidor de audio digital a análogo (DAC) aumenta linealmente a medida que el control deslizante del volumen pasa de su posición mínima (con la etiqueta Mín. ) a su posición máxima (con la etiqueta Max). La etiqueta V<sub>FS</sub> en el eje vertical representa el voltaje de salida dac a escala completa.

Sin embargo, la sonoridad percibida varía aproximadamente como el logaritmo de la potencia de la señal de audio, como se muestra en el lado derecho del diagrama anterior. Por lo tanto, el movimiento del control deslizante en un intervalo cerca del valor mínimo da como resultado un cambio relativamente grande en la sonoridad percibida, pero el movimiento del control deslizante en un intervalo del mismo ancho cerca del valor máximo provoca un cambio relativamente pequeño en la sonoridad percibida.

En el lado derecho del diagrama anterior, la sonoridad del eje vertical se mide en decibelios (dB) con respecto a la configuración de energía a escala completa (en 0 decibelios). La curva de sonoridad forma una intersección con el eje vertical a menos infinito, pero solo la parte de la curva de 0 decibelios a -96 decibelios aparece en el diagrama. La decisión de mostrar solo esta parte de la curva es algo arbitraria, pero –96 decibelios representa cómodamente la potencia en el siguiente nivel de salida inferior de una DAC de 16 bits con respecto a la potencia a escala completa. Este valor se calcula como 20<sup>.</sup> log₁₀(1/65535).

Dado que los pequeños cambios en la posición del control deslizante cerca de la configuración mínima del diagrama anterior tienen como resultado grandes cambios en la sonoridad, el usuario podría encontrar el volumen difícil de controlar sobre esta región. Los movimientos de control deslizante relativamente pequeños pueden insertar el volumen por encima o por debajo del nivel deseado. Un control de volumen mejorado proporcionaría una relación más lineal entre la posición del control deslizante y la sonoridad.

En el diagrama siguiente se muestra la asignación de la posición del control deslizante al voltaje de salida y a la sonoridad percibida para un control de volumen con cinta de audio.

![diagrama de salida para el control de volumen con cinta de audio](images/taper2.jpg)

Como se muestra en el lado derecho del diagrama anterior, la sonoridad percibida varía aproximadamente linealmente con los cambios en la posición del control deslizante. Para que esto ocurra, el voltaje dac debe variar no linealmente con la posición, como se muestra en el lado izquierdo del diagrama. La curva se aproxima asímpticamente a 0 volts a medida que el control deslizante se desplaza hacia la izquierda desde la configuración máxima. El voltaje en la posición mínima del control deslizante es muy pequeño, pero puede que no sea exactamente cero.

Los métodos siguientes de la **interfaz IAudioEndpointVolume** usan la configuración de volumen que se mide en decibelios:

-   [**IAudioEndpointVolume::GetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevel)
-   [**IAudioEndpointVolume::GetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)

Estos métodos generan una relación aproximadamente lineal entre la configuración del volumen y la sonoridad percibida. El intervalo de volúmenes en decibelios de los controles de volumen administrados por estos métodos depende del dispositivo de punto de conexión de audio. Para determinar el intervalo de volúmenes de un dispositivo determinado, llame al método [**IAudioEndpointVolume::GetVolumeRange.**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange)

Por el contrario, la configuración del volumen para los métodos siguientes en la interfaz **IAudioEndpointVolume** sigue una curva más ligeramente acodada en el intervalo de volúmenes:

-   [**IAudioEndpointVolume::GetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::GetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevelscalar)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

En Windows Vista, estos métodos usan una curva intermedia entre la curva con cinta de audio que se muestra en el diagrama anterior y una curva con cinta lineal. Tenga en cuenta que la forma de la curva podría cambiar en versiones futuras de Windows. Los cuatro primeros métodos de la lista anterior enumeran los niveles de volumen rápido como valores normalizados en el intervalo de 0,0 (volumen mínimo) a 1,0 (volumen máximo). Para los dos últimos métodos de la lista, llame al método [**IAudioEndpointVolume::GetVolumeStepInfo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo) para obtener el número de pasos del intervalo de volúmenes.

Las interfaces siguientes usan curvas con cinta lineal para su configuración de volumen:

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)
-   [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)

Para obtener más información sobre estas interfaces, vea [Controles de volumen de sesión](session-volume-controls.md). Y para obtener información sobre los intervalos de volúmenes y los niveles de volumen predeterminados en las distintas versiones de Windows, vea Volumen de [audio predeterminado Configuración](/windows-hardware/drivers/audio/default-audio-volume-settings).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles de volumen](volume-controls.md)
</dt> </dl>

 

 
