---
title: Cómo funciona el ejemplo echo
description: Cómo funciona el ejemplo echo
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Complementos de Media Player de Windows, información general de ejemplo de eco
- complementos, información general de ejemplo de eco
- Complementos de procesamiento de señal digital, información general de ejemplo de eco
- Complementos DSP, información general de ejemplo de eco
- Ejemplo de complemento DSP de eco, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08814a6f0d604c7d566a0fc8d9f07b05446fca64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695342"
---
# <a name="how-the-echo-sample-works"></a><span data-ttu-id="66d72-108">Cómo funciona el ejemplo echo</span><span class="sxs-lookup"><span data-stu-id="66d72-108">How the Echo Sample Works</span></span>

<span data-ttu-id="66d72-109">El código crea el efecto de eco asignando un búfer lo suficientemente grande como para contener exactamente la cantidad de datos de audio que se pueden representar en el intervalo de tiempo especificado por el valor de tiempo de retraso.</span><span class="sxs-lookup"><span data-stu-id="66d72-109">The code creates the echo effect by allocating a buffer large enough to contain exactly the amount of audio data that can be rendered in the time frame specified by the delay time value.</span></span> <span data-ttu-id="66d72-110">El tamaño del búfer se calcula, en bytes, mediante la siguiente fórmula:</span><span class="sxs-lookup"><span data-stu-id="66d72-110">The size of the buffer is calculated, in bytes, by the following formula:</span></span>

<span data-ttu-id="66d72-111">tamaño de búfer = frecuencia de muestreo de tiempo de retraso \* / \* alineación de bloque 1000</span><span class="sxs-lookup"><span data-stu-id="66d72-111">buffer size = delay time \* sample rate / 1000 \* block alignment</span></span>

<span data-ttu-id="66d72-112">El tiempo de retardo está en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="66d72-112">The delay time is in milliseconds.</span></span> <span data-ttu-id="66d72-113">La velocidad de muestreo y los valores de alineación de bloque se proporcionan en una estructura WAVEFORMATEX.</span><span class="sxs-lookup"><span data-stu-id="66d72-113">The sample rate and block alignment values are given in a WAVEFORMATEX structure.</span></span> <span data-ttu-id="66d72-114">La velocidad de muestreo es en muestras por segundo; la división por 1000 produce muestras por milisegundo.</span><span class="sxs-lookup"><span data-stu-id="66d72-114">The sample rate is in samples per second; dividing by 1000 yields samples per millisecond.</span></span> <span data-ttu-id="66d72-115">La alineación de bloque es igual al producto del número de canales (1 para mono, 2 para estéreo) y el número de bits por muestra (8 o 16) dividido entre 8 (bits por byte).</span><span class="sxs-lookup"><span data-stu-id="66d72-115">The block alignment is equal to the product of the number of channels (1 for mono, 2 for stereo) and the number of bits per sample (8 or 16) divided by 8 (bits per byte).</span></span>

<span data-ttu-id="66d72-116">Además de la variable de puntero que apunta al encabezado del búfer de retraso, el código crea un puntero movible que recorre los datos del búfer en sincronización con el bucle de procesamiento en la función **DoProcessOutput** .</span><span class="sxs-lookup"><span data-stu-id="66d72-116">In addition to the pointer variable that points to the head of the delay buffer, the code creates a movable pointer that steps through the data in the buffer in synchronization with the processing loop in the **DoProcessOutput** function.</span></span> <span data-ttu-id="66d72-117">Cuando el puntero movible alcanza el final del búfer de retraso, vuelve al encabezado del búfer.</span><span class="sxs-lookup"><span data-stu-id="66d72-117">When the movable pointer reaches the end of the delay buffer, it moves back to the head of the buffer.</span></span> <span data-ttu-id="66d72-118">Un búfer que se usa de esta manera se denomina búfer circular.</span><span class="sxs-lookup"><span data-stu-id="66d72-118">A buffer used in this manner is called a circular buffer.</span></span>

<span data-ttu-id="66d72-119">Una vez que el búfer de retraso existe y Windows Media Player ha asignado un búfer de entrada para proporcionar datos de audio y un búfer de salida para recibir los datos de audio procesados, el procesamiento de eco es similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="66d72-119">Once the delay buffer exists, and Windows Media Player has allocated an input buffer to supply audio data and an output buffer to receive processed audio data, the echo processing proceeds like this:</span></span>

1.  <span data-ttu-id="66d72-120">Escriba un bucle que permita el procesamiento de cada ejemplo de audio en el búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="66d72-120">Enter a loop that allows processing of each audio sample in the input buffer.</span></span>
2.  <span data-ttu-id="66d72-121">Recupera un ejemplo del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="66d72-121">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="66d72-122">A continuación, mueva el puntero de búfer de entrada hacia delante hasta el ejemplo siguiente para preparar la siguiente iteración del bucle.</span><span class="sxs-lookup"><span data-stu-id="66d72-122">Then, move the input buffer pointer forward to the next sample to prepare for the next loop iteration.</span></span>
3.  <span data-ttu-id="66d72-123">Recupera un ejemplo del búfer de retraso.</span><span class="sxs-lookup"><span data-stu-id="66d72-123">Retrieve a sample from the delay buffer.</span></span>
4.  <span data-ttu-id="66d72-124">Copie el ejemplo del búfer de entrada a la misma ubicación en el búfer de retraso desde el que se recuperó el último ejemplo de retraso.</span><span class="sxs-lookup"><span data-stu-id="66d72-124">Copy the sample from the input buffer to the same location in the delay buffer from which the last delay sample was retrieved.</span></span>
5.  <span data-ttu-id="66d72-125">Mueva el puntero de búfer de retraso hacia delante al siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="66d72-125">Move the delay buffer pointer forward to the next sample.</span></span> <span data-ttu-id="66d72-126">Si el puntero se desplaza más allá del final del búfer, muévalo al encabezado del búfer.</span><span class="sxs-lookup"><span data-stu-id="66d72-126">If the pointer moves past the end of the buffer, move it to the head of the buffer.</span></span>
6.  <span data-ttu-id="66d72-127">Combine el ejemplo del búfer de entrada con el ejemplo del búfer de retraso.</span><span class="sxs-lookup"><span data-stu-id="66d72-127">Combine the sample from the input buffer with the sample from the delay buffer.</span></span>
7.  <span data-ttu-id="66d72-128">Copie el resultado en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="66d72-128">Copy the result to the output buffer.</span></span> <span data-ttu-id="66d72-129">A continuación, mueva el puntero del búfer de salida hacia delante a la unidad siguiente para preparar la siguiente iteración del bucle.</span><span class="sxs-lookup"><span data-stu-id="66d72-129">Then, move the output buffer pointer forward to the next unit to prepare for the next loop iteration.</span></span>
8.  <span data-ttu-id="66d72-130">Repita el proceso hasta que se procesen todos los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="66d72-130">Repeat until all the samples are processed.</span></span>

<span data-ttu-id="66d72-131">Cuando una muestra de entrada recuperada en el paso 2 se copia en el búfer de retraso en el paso 4, permanece allí hasta que el puntero móvil recorre cada ejemplo en el búfer de retraso y finalmente vuelve a la misma posición.</span><span class="sxs-lookup"><span data-stu-id="66d72-131">When an input sample retrieved in step 2 is copied to the delay buffer in step 4, it remains there until the movable pointer steps through each sample in the delay buffer and finally returns to the same position.</span></span> <span data-ttu-id="66d72-132">Dado que el tamaño del búfer de retraso está diseñado para que se corresponda con el tiempo de retardo, el tiempo transcurrido entre el ejemplo que se copia en el búfer de retraso y el ejemplo que se recupera una vez más es igual al retraso especificado (más cualquier latencia introducida por el procesamiento real).</span><span class="sxs-lookup"><span data-stu-id="66d72-132">Because the size of the delay buffer is designed to correspond to the delay time, the elapsed time between the sample being copied to the delay buffer and the sample being retrieved once again equals the specified delay (plus any latency introduced by the actual processing).</span></span>

<span data-ttu-id="66d72-133">Cuando se inicia un flujo, no se generan datos de retraso hasta que ha transcurrido el tiempo de retraso.</span><span class="sxs-lookup"><span data-stu-id="66d72-133">When a stream starts, no delay data is generated until the delay time has elapsed.</span></span> <span data-ttu-id="66d72-134">Por lo tanto, es importante que el búfer de retraso contenga inicialmente el silencio.</span><span class="sxs-lookup"><span data-stu-id="66d72-134">Therefore, it is important that the delay buffer initially contains silence.</span></span> <span data-ttu-id="66d72-135">Si el búfer de retraso contiene datos aleatorios, el usuario oirá el ruido en blanco hasta que el complemento genere suficientes datos de retraso para sobrescribir todo el búfer de retraso.</span><span class="sxs-lookup"><span data-stu-id="66d72-135">If the delay buffer contains random data, the user will hear white noise until the plug-in generates enough delay data to overwrite the entire delay buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66d72-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66d72-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66d72-137">**Información general del ejemplo echo**</span><span class="sxs-lookup"><span data-stu-id="66d72-137">**Echo Sample Overview**</span></span>](echo-sample-overview.md)
</dt> </dl>

 

 




