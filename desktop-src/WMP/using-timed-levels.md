---
title: Uso de niveles con tiempo
description: Uso de niveles con tiempo
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- visualizaciones, eventos con tiempo
- visualizaciones personalizadas, eventos con tiempo
- visualizaciones, matriz frequency
- visualizaciones personalizadas, matriz frequency
- visualizaciones, matriz de forma de onda
- visualizaciones personalizadas, matriz de forma de onda
- visualizaciones, variable de estado
- visualizaciones personalizadas, variable de estado
- visualizations,timeStamp variable
- visualizaciones personalizadas, variable timeStamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6ce4d675fa37a519952f1b31d3c52cd93005a82eef977b7bd7d77623f1e508
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116942"
---
# <a name="using-timed-levels"></a>Uso de niveles con tiempo

La **estructura TimedLevel** se compone de dos matrices bidimensionales, un valor de estado y un valor de marca de tiempo.

## <a name="frequency-array"></a>Matriz de frecuencia

La matriz frequency es una matriz bidimensional. La primera dimensión de cada matriz corresponde al canal de audio estéreo (izquierdo o derecho) y la segunda corresponde a los niveles de frecuencia (en bytes) de la instantánea, donde el espectro de audio se divide en 1024 regiones.

Puede obtener los datos de la matriz de frecuencia proporcionados desde el Reproductor de Windows Media de la siguiente manera:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



El valor de snapshot es para el canal izquierdo y contiene el valor de la parte más baja del espectro de frecuencia. Por ejemplo, si la instantánea tiene un valor grande, indica que la parte 1024 más baja del espectro de frecuencia tiene una gran frecuencia. Un valor de cero indica que no hay valores de frecuencia baja en esa parte del espectro para el canal izquierdo. Si tiene una señal monofónica, solo la primera dimensión tiene valores válidos.

Si la señal no es estéreo, la segunda matriz contendrá una copia de la señal mono. Es decir, la frecuencia 0 n y la frecuencia 1 n contendrán los mismos datos, donde n es el \[ \] \[  \] \[ índice en una \] \[  \] celda determinada. 

## <a name="waveform-array"></a>Matriz de forma de onda

La matriz de formas de onda también es una matriz bidimensional. La primera dimensión de la matriz corresponde al canal (izquierdo o derecho) y la segunda corresponde a los niveles de energía (en bytes) de la instantánea, donde la potencia de audio se divide en 1024 segmentos de tiempo contiguos.

Puede obtener los datos de la matriz de forma de onda Reproductor de Windows Media de la siguiente manera:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



El valor de snapshot es para el canal izquierdo y contiene el primer valor de la instantánea cuantificada de los valores de energía. Cuando se toma una instantánea, consta de 1024 pequeñas medidas incrementales de la potencia de audio. El valor más bajo de la matriz se genera mediante la primera medida incremental de la potencia de audio. Tenga en cuenta que los valores de la potencia se miden de -128 a +127, pero los valores de la matriz oscilan entre 0 y 255. Si tiene una onda monofónica, solo la primera dimensión tendrá valores válidos.

Si la señal no es estéreo, la segunda matriz contendrá una copia de la señal mono. Es decir, la forma de onda 0 n y la forma de onda 1 n contendrán los mismos datos, donde n es el \[ \] \[  \] \[ índice de una \] \[  \] celda determinada. 

## <a name="state"></a>Estado

La variable de estado refleja el estado de reproducción de audio Reproductor de Windows Media. Los valores de enumeración PlayerState son


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



Puede usar esta variable para realizar diferentes acciones en función del estado de reproducción de audio. Por ejemplo, puede reproducir un tipo de visualización cuando se reproduce el audio y otro cuando se detiene.

## <a name="time-stamp"></a>Marca de tiempo

La variable timeStamp refleja la hora actual en que se toma la instantánea. Se puede usar para medir la frecuencia con la que se toman las instantáneas.

Puede usar esta variable para el tiempo de las animaciones. Si las instantáneas son demasiado frecuentes, puede degradar correctamente la imagen para mostrarla de la manera que elija.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de Render**](implementing-render.md)
</dt> </dl>

 

 




