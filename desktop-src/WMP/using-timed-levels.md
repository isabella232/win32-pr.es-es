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
# <a name="using-timed-levels"></a><span data-ttu-id="346a1-113">Usar niveles de tiempo</span><span class="sxs-lookup"><span data-stu-id="346a1-113">Using Timed Levels</span></span>

<span data-ttu-id="346a1-114">La estructura **TimedLevel** se compone 2 2 de Matrices unidimensionales, un valor de estado y un valor de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="346a1-114">The **TimedLevel** structure is composed of two two-dimensional arrays, a state value, and a time stamp value.</span></span>

## <a name="frequency-array"></a><span data-ttu-id="346a1-115">Matriz de frecuencia</span><span class="sxs-lookup"><span data-stu-id="346a1-115">Frequency Array</span></span>

<span data-ttu-id="346a1-116">La matriz de frecuencia es una matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="346a1-116">The frequency array is a two-dimensional array.</span></span> <span data-ttu-id="346a1-117">La primera dimensión de cada matriz corresponde al canal de audio estéreo (izquierda o derecha) y la segunda corresponde a los niveles de frecuencia (en bytes) de la instantánea, donde el espectro de audio se divide en regiones 1024.</span><span class="sxs-lookup"><span data-stu-id="346a1-117">The first dimension of each array corresponds to the stereo audio channel (left or right), and the second corresponds to the frequency levels (in bytes) of the snapshot, where the audio spectrum is divided up into 1024 regions.</span></span>

<span data-ttu-id="346a1-118">Puede obtener los datos de la matriz de frecuencia que se proporcionan en la Media Player de Windows de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="346a1-118">You can get the frequency array data supplied from the Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



<span data-ttu-id="346a1-119">El valor de Snapshot es para el canal izquierdo y contiene el valor de la parte más baja del espectro de frecuencias.</span><span class="sxs-lookup"><span data-stu-id="346a1-119">The value of snapshot is for the left channel and contains the value of the lowest part of the frequency spectrum.</span></span> <span data-ttu-id="346a1-120">Por ejemplo, si la instantánea tiene un valor grande, indica que la parte de 1024th más baja del espectro de frecuencia es de gran frecuencia.</span><span class="sxs-lookup"><span data-stu-id="346a1-120">For example, if snapshot has a large value, it indicates that the lowest 1024th part of the frequency spectrum is rich in frequency.</span></span> <span data-ttu-id="346a1-121">Un valor de cero indica que no hay valores de frecuencia bajo en esa parte del espectro del canal izquierdo.</span><span class="sxs-lookup"><span data-stu-id="346a1-121">A value of zero indicates no low frequency values in that part of the spectrum for the left channel.</span></span> <span data-ttu-id="346a1-122">Si tiene una señal monofalsas, solo la primera dimensión tiene valores válidos.</span><span class="sxs-lookup"><span data-stu-id="346a1-122">If you have a monophonic signal, only the first dimension has valid values.</span></span>

<span data-ttu-id="346a1-123">Si la señal no es estéreo, la segunda contendrá una copia de la señal mono.</span><span class="sxs-lookup"><span data-stu-id="346a1-123">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="346a1-124">Es decir, Frequency \[ 0 \] \[ *n* \] y Frequency \[ 1 n contendrán \] \[  \] los mismos datos, donde *n* es el índice de una celda determinada.</span><span class="sxs-lookup"><span data-stu-id="346a1-124">That is, frequency\[0\]\[*n*\] and frequency\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="waveform-array"></a><span data-ttu-id="346a1-125">Matriz de onda</span><span class="sxs-lookup"><span data-stu-id="346a1-125">Waveform Array</span></span>

<span data-ttu-id="346a1-126">La matriz de la forma de onda también es una matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="346a1-126">The waveform array is also a two-dimensional array.</span></span> <span data-ttu-id="346a1-127">La primera dimensión de la matriz corresponde al canal (izquierda o derecha) y la segunda corresponde a los niveles de energía (en bytes) de la instantánea, donde la potencia de audio se divide en segmentos de tiempo contiguos de 1024.</span><span class="sxs-lookup"><span data-stu-id="346a1-127">The first dimension of the array corresponds to the channel (left or right), and the second corresponds to the power levels (in bytes) of the snapshot, where the audio power is broken up into 1024 contiguous time segments.</span></span>

<span data-ttu-id="346a1-128">Puede obtener los datos de la matriz de forma de onda de Windows Media Player de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="346a1-128">You can get the waveform array data from Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



<span data-ttu-id="346a1-129">El valor de Snapshot es para el canal izquierdo y contiene el primer valor de la instantánea cuantificada de los valores de energía.</span><span class="sxs-lookup"><span data-stu-id="346a1-129">The value of snapshot is for the left channel and contains the first value of the quantized snapshot of the power values.</span></span> <span data-ttu-id="346a1-130">Cuando se toma una instantánea, consta de 1024 pequeñas mediciones incrementales de la energía de audio.</span><span class="sxs-lookup"><span data-stu-id="346a1-130">When a snapshot is taken, it consists of 1024 tiny incremental measurements of the audio power.</span></span> <span data-ttu-id="346a1-131">La primera medición incremental de la potencia de audio genera el valor más bajo de la matriz.</span><span class="sxs-lookup"><span data-stu-id="346a1-131">The lowest value of the array is generated by the first incremental measurement of audio power.</span></span> <span data-ttu-id="346a1-132">Tenga en cuenta que los valores de la potencia se miden entre-128 y + 127, pero los valores de la matriz van de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="346a1-132">Note that the values of the power are measured from -128 to +127 but the values in the array range from 0 to 255.</span></span> <span data-ttu-id="346a1-133">Si tiene una onda monofalsas, solo la primera tendrá valores válidos.</span><span class="sxs-lookup"><span data-stu-id="346a1-133">If you have a monophonic wave, only the first dimension will have valid values.</span></span>

<span data-ttu-id="346a1-134">Si la señal no es estéreo, la segunda contendrá una copia de la señal mono.</span><span class="sxs-lookup"><span data-stu-id="346a1-134">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="346a1-135">Es decir, la forma de onda \[ 0 n y la forma de \] \[  \] onda 1 n contendrán \[ \] \[  \] los mismos datos, donde *n* es el índice de una celda determinada.</span><span class="sxs-lookup"><span data-stu-id="346a1-135">That is, waveform\[0\]\[*n*\] and waveform\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="state"></a><span data-ttu-id="346a1-136">Estado</span><span class="sxs-lookup"><span data-stu-id="346a1-136">State</span></span>

<span data-ttu-id="346a1-137">La variable de Estado refleja el estado de reproducción de audio de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="346a1-137">The state variable reflects the audio playback state of Windows Media Player.</span></span> <span data-ttu-id="346a1-138">Los valores de enumeración PlayerState son</span><span class="sxs-lookup"><span data-stu-id="346a1-138">The PlayerState enumeration values are</span></span>


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



<span data-ttu-id="346a1-139">Puede usar esta variable para realizar distintas acciones en función del estado de reproducción de audio.</span><span class="sxs-lookup"><span data-stu-id="346a1-139">You can use this variable to take different actions depending on the audio playback state.</span></span> <span data-ttu-id="346a1-140">Por ejemplo, puede reproducir un tipo de visualización cuando el audio se reproduce y otro cuando se detiene.</span><span class="sxs-lookup"><span data-stu-id="346a1-140">For example, you can play one kind of visualization when the audio is playing and another when it is stopped.</span></span>

## <a name="time-stamp"></a><span data-ttu-id="346a1-141">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="346a1-141">Time Stamp</span></span>

<span data-ttu-id="346a1-142">La variable timeStamp refleja la hora actual en que se toma la instantánea.</span><span class="sxs-lookup"><span data-stu-id="346a1-142">The timeStamp variable reflects the current time when the snapshot is taken.</span></span> <span data-ttu-id="346a1-143">Se puede usar para medir la frecuencia con la que se toman las instantáneas.</span><span class="sxs-lookup"><span data-stu-id="346a1-143">This can be used to measure how frequently the snapshots are taken.</span></span>

<span data-ttu-id="346a1-144">Puede usar esta variable para las animaciones.</span><span class="sxs-lookup"><span data-stu-id="346a1-144">You can use this variable to time your animations.</span></span> <span data-ttu-id="346a1-145">Si las instantáneas son demasiado frecuentes, puede degradar correctamente la imagen para que se muestre de la manera que elija.</span><span class="sxs-lookup"><span data-stu-id="346a1-145">If the snapshots are too frequent, you can gracefully degrade your image to display in the manner you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="346a1-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="346a1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="346a1-147">**Implementación de render**</span><span class="sxs-lookup"><span data-stu-id="346a1-147">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




