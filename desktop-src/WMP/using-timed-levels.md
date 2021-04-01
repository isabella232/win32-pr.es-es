---
title: Usar niveles de tiempo
description: Usar niveles de tiempo
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- visualizaciones, eventos con tiempo
- visualizaciones personalizadas, eventos con tiempo
- visualizaciones, matriz de frecuencia
- visualizaciones personalizadas, matriz de frecuencia
- visualizaciones, matriz de onda
- visualizaciones personalizadas, matriz de onda
- visualizaciones, variable de estado
- visualizaciones personalizadas, variable de estado
- visualizaciones, variable timeStamp
- visualizaciones personalizadas, variable timeStamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d9a23818d57305b3b205ea2e17b6dda2884e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075747"
---
# <a name="using-timed-levels"></a>Usar niveles de tiempo

La estructura **TimedLevel** se compone 2 2 de Matrices unidimensionales, un valor de estado y un valor de marca de tiempo.

## <a name="frequency-array"></a>Matriz de frecuencia

La matriz de frecuencia es una matriz bidimensional. La primera dimensión de cada matriz corresponde al canal de audio estéreo (izquierda o derecha) y la segunda corresponde a los niveles de frecuencia (en bytes) de la instantánea, donde el espectro de audio se divide en regiones 1024.

Puede obtener los datos de la matriz de frecuencia que se proporcionan en la Media Player de Windows de la siguiente manera:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



El valor de Snapshot es para el canal izquierdo y contiene el valor de la parte más baja del espectro de frecuencias. Por ejemplo, si la instantánea tiene un valor grande, indica que la parte de 1024th más baja del espectro de frecuencia es de gran frecuencia. Un valor de cero indica que no hay valores de frecuencia bajo en esa parte del espectro del canal izquierdo. Si tiene una señal monofalsas, solo la primera dimensión tiene valores válidos.

Si la señal no es estéreo, la segunda contendrá una copia de la señal mono. Es decir, Frequency \[ 0 \] \[ *n* \] y Frequency \[ 1 n contendrán \] \[  \] los mismos datos, donde *n* es el índice de una celda determinada.

## <a name="waveform-array"></a>Matriz de onda

La matriz de la forma de onda también es una matriz bidimensional. La primera dimensión de la matriz corresponde al canal (izquierda o derecha) y la segunda corresponde a los niveles de energía (en bytes) de la instantánea, donde la potencia de audio se divide en segmentos de tiempo contiguos de 1024.

Puede obtener los datos de la matriz de forma de onda de Windows Media Player de la siguiente manera:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



El valor de Snapshot es para el canal izquierdo y contiene el primer valor de la instantánea cuantificada de los valores de energía. Cuando se toma una instantánea, consta de 1024 pequeñas mediciones incrementales de la energía de audio. La primera medición incremental de la potencia de audio genera el valor más bajo de la matriz. Tenga en cuenta que los valores de la potencia se miden entre-128 y + 127, pero los valores de la matriz van de 0 a 255. Si tiene una onda monofalsas, solo la primera tendrá valores válidos.

Si la señal no es estéreo, la segunda contendrá una copia de la señal mono. Es decir, la forma de onda \[ 0 n y la forma de \] \[  \] onda 1 n contendrán \[ \] \[  \] los mismos datos, donde *n* es el índice de una celda determinada.

## <a name="state"></a>Estado

La variable de Estado refleja el estado de reproducción de audio de Windows Media Player. Los valores de enumeración PlayerState son


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



Puede usar esta variable para realizar distintas acciones en función del estado de reproducción de audio. Por ejemplo, puede reproducir un tipo de visualización cuando el audio se reproduce y otro cuando se detiene.

## <a name="time-stamp"></a>Marca de tiempo

La variable timeStamp refleja la hora actual en que se toma la instantánea. Se puede usar para medir la frecuencia con la que se toman las instantáneas.

Puede usar esta variable para las animaciones. Si las instantáneas son demasiado frecuentes, puede degradar correctamente la imagen para que se muestre de la manera que elija.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de render**](implementing-render.md)
</dt> </dl>

 

 




