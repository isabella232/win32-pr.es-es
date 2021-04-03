---
title: Crear el efecto de eco
description: Crear el efecto de eco
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Complementos de Media Player de Windows, método echo de ejemplo DoProcessOutput
- complementos, método echo de ejemplo DoProcessOutput
- Complementos de procesamiento de señal digital, ejemplo echo método DoProcessOutput
- Complementos DSP, método echo de ejemplo DoProcessOutput
- Ejemplo de complemento DSP de eco, método DoProcessOutput
- Ejemplo de complemento DSP de eco, creación de efecto de eco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075160"
---
# <a name="creating-the-echo-effect"></a><span data-ttu-id="fb238-109">Crear el efecto de eco</span><span class="sxs-lookup"><span data-stu-id="fb238-109">Creating the Echo Effect</span></span>

<span data-ttu-id="fb238-110">Primero debe quitar el código del ejemplo de asistente que escala el audio.</span><span class="sxs-lookup"><span data-stu-id="fb238-110">You must first remove the code from the wizard sample that scales the audio.</span></span> <span data-ttu-id="fb238-111">En la sección de 8 bits, quite el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb238-111">From the 8-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="fb238-112">(Recuerde que m \_ fScaleFactor se ha reemplazado por m \_ dwDelayTime).</span><span class="sxs-lookup"><span data-stu-id="fb238-112">(Remember that m\_fScaleFactor was replaced by m\_dwDelayTime.)</span></span>

<span data-ttu-id="fb238-113">En la sección de 16 bits, quite el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb238-113">From the 16-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="fb238-114">La implementación de **DoProcessOutput** proporcionada por el código de ejemplo del Asistente para complementos crea un bucle while que recorre en iteración una vez cada muestra en el búfer de entrada proporcionado por Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fb238-114">The implementation of **DoProcessOutput** provided by the plug-in wizard sample code creates a while loop that iterates one time for each sample in the input buffer provided by Windows Media Player.</span></span> <span data-ttu-id="fb238-115">Este bucle funciona de la misma manera para audio de 8 y 16 bits, aunque se requiere un bucle independiente para cada uno.</span><span class="sxs-lookup"><span data-stu-id="fb238-115">This loop works the same way for both 8-bit and 16-bit audio, although a separate loop is required for each.</span></span> <span data-ttu-id="fb238-116">En cada caso, el bucle se inicia con la prueba siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb238-116">In each case, the loop initiates with the following test:</span></span>


```C++
while (dwSamplesToProcess--)

```



<span data-ttu-id="fb238-117">Una vez dentro del bucle, las rutinas de procesamiento son muy similares para audio de 8 y 16 bits.</span><span class="sxs-lookup"><span data-stu-id="fb238-117">Once inside the loop, the processing routines are very similar for 8-bit and 16-bit audio.</span></span> <span data-ttu-id="fb238-118">La principal diferencia es que el código de la sección de 8 bits cambia el intervalo de valores de datos a-128 a 127 y, a continuación, vuelve a convertir el intervalo antes de escribir los datos en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="fb238-118">The main difference is that the code in the 8-bit section changes the range of data values to -128 through 127, and then converts the range back again before writing the data to the output buffer.</span></span> <span data-ttu-id="fb238-119">Esto es importante para conservar la simetría de la forma de onda de audio durante el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="fb238-119">This is important to retain the symmetry of the audio waveform during processing.</span></span>

<span data-ttu-id="fb238-120">Ahora puede empezar a agregar y reemplazar código en el bucle de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="fb238-120">Now you can begin to add and replace code in the processing loop.</span></span>

## <a name="retrieve-a-sample-from-the-input-buffer"></a><span data-ttu-id="fb238-121">Recuperación de un ejemplo desde el búfer de entrada</span><span class="sxs-lookup"><span data-stu-id="fb238-121">Retrieve a Sample from the Input Buffer</span></span>

<span data-ttu-id="fb238-122">Durante cada iteración del bucle, se recupera un solo ejemplo del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="fb238-122">During each iteration of the loop, a single sample is retrieved from the input buffer.</span></span> <span data-ttu-id="fb238-123">En el caso de audio de 8 bits, el ejemplo se desplaza al nuevo intervalo y, a continuación, el puntero al búfer de entrada está avanzado en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="fb238-123">For 8-bit audio, the sample is shifted into the new range, and then the pointer to the input buffer is advanced to the next sample.</span></span> <span data-ttu-id="fb238-124">El código siguiente procede del Asistente para complementos:</span><span class="sxs-lookup"><span data-stu-id="fb238-124">The following code is from the plug-in wizard:</span></span>


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



<span data-ttu-id="fb238-125">En el caso de audio de 16 bits, el proceso es el mismo, salvo por la normalización:</span><span class="sxs-lookup"><span data-stu-id="fb238-125">For 16-bit audio, the process is the same except for the normalization:</span></span>


```C++
// Get the input sample.
int i = *pwInputData++;

```



<span data-ttu-id="fb238-126">Recuerde que los punteros en el código de 16 bits se han convertido al tipo **Short**.</span><span class="sxs-lookup"><span data-stu-id="fb238-126">Remember that the pointers in the 16-bit code have been converted to type **short**.</span></span>

## <a name="retrieve-a-sample-from-the-delay-buffer"></a><span data-ttu-id="fb238-127">Recuperación de un ejemplo del búfer de retraso</span><span class="sxs-lookup"><span data-stu-id="fb238-127">Retrieve a Sample from the Delay Buffer</span></span>

<span data-ttu-id="fb238-128">A continuación, recupere un solo ejemplo del búfer de retraso.</span><span class="sxs-lookup"><span data-stu-id="fb238-128">Next, retrieve a single sample from the delay buffer.</span></span> <span data-ttu-id="fb238-129">En el caso de código de 8 bits, las muestras de retraso se almacenan en su intervalo nativo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="fb238-129">For 8-bit code, the delay samples are stored in their native range of 0 to 255.</span></span> <span data-ttu-id="fb238-130">El código siguiente, que debe agregar, recupera un ejemplo de retraso de 8 bits:</span><span class="sxs-lookup"><span data-stu-id="fb238-130">The following code, which you must add, retrieves an 8-bit delay sample:</span></span>


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



<span data-ttu-id="fb238-131">En el caso de audio de 16 bits, el proceso es similar:</span><span class="sxs-lookup"><span data-stu-id="fb238-131">For 16-bit audio, the process is similar:</span></span>


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a><span data-ttu-id="fb238-132">Escribir el ejemplo de entrada en el búfer de retraso</span><span class="sxs-lookup"><span data-stu-id="fb238-132">Write the Input Sample to the Delay Buffer</span></span>

<span data-ttu-id="fb238-133">Ahora, debe almacenar el ejemplo de entrada en el búfer de retraso en la misma ubicación desde la que recuperó el ejemplo de retraso.</span><span class="sxs-lookup"><span data-stu-id="fb238-133">Now, you must store the input sample in the delay buffer in the same location from which you retrieved the delay sample.</span></span> <span data-ttu-id="fb238-134">El siguiente es el código que debe agregar para el audio de 8 bits:</span><span class="sxs-lookup"><span data-stu-id="fb238-134">The following is the code you must add for 8-bit audio:</span></span>


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



<span data-ttu-id="fb238-135">Este es el código que se va a agregar para la sección de 16 bits:</span><span class="sxs-lookup"><span data-stu-id="fb238-135">This is the code to add for the 16-bit section:</span></span>


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a><span data-ttu-id="fb238-136">Desplace el puntero de búfer de retraso</span><span class="sxs-lookup"><span data-stu-id="fb238-136">Move the Delay Buffer Pointer</span></span>

<span data-ttu-id="fb238-137">Ahora que ha finalizado el trabajo en el búfer de retraso para esta iteración, puede avanzar el puntero movible al búfer de retraso.</span><span class="sxs-lookup"><span data-stu-id="fb238-137">Now that the work in the delay buffer is finished for this iteration, you can advance the movable pointer to the delay buffer.</span></span> <span data-ttu-id="fb238-138">Si el puntero alcanza el final del búfer circular, debe cambiar su valor para que apunte al encabezado del búfer.</span><span class="sxs-lookup"><span data-stu-id="fb238-138">If the pointer reaches the end of the circular buffer, you must change its value to point to the head of the buffer.</span></span> <span data-ttu-id="fb238-139">Para hacer esto para el audio de 8 bits, use el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb238-139">To do this for 8-bit audio, use the following code:</span></span>


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



<span data-ttu-id="fb238-140">Este es el código de la sección de 16 bits:</span><span class="sxs-lookup"><span data-stu-id="fb238-140">Here is the code for the 16-bit section:</span></span>


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



<span data-ttu-id="fb238-141">Puesto que el puntero de la sección de 16 bits es realmente una copia de la variable miembro, debe recordar actualizar el valor de la variable miembro con la nueva dirección.</span><span class="sxs-lookup"><span data-stu-id="fb238-141">Since the pointer in the 16-bit section is really a copy of the member variable, you must remember to update the value in the member variable with the new address.</span></span> <span data-ttu-id="fb238-142">Si no lo hace, el puntero de búfer de retraso apuntará repetidamente al encabezado del búfer y el efecto de eco no funcionará según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="fb238-142">If you fail to do this, the delay buffer pointer will point to the head of the buffer repeatedly and your echo effect will not work as expected.</span></span> <span data-ttu-id="fb238-143">Agregue el código siguiente a la sección de 16 bits:</span><span class="sxs-lookup"><span data-stu-id="fb238-143">Add the following code to the 16-bit section:</span></span>


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a><span data-ttu-id="fb238-144">Mezclar el ejemplo de entrada con el ejemplo de retraso</span><span class="sxs-lookup"><span data-stu-id="fb238-144">Mix the Input Sample with the Delay Sample</span></span>

<span data-ttu-id="fb238-145">Aquí es donde se usan los valores de mezcla húmeda y mezcla seca para crear el ejemplo de salida final.</span><span class="sxs-lookup"><span data-stu-id="fb238-145">This is where you use the wet mix and dry mix values to create the final output sample.</span></span> <span data-ttu-id="fb238-146">Basta con multiplicar cada ejemplo por el valor de punto flotante que representa el porcentaje de la señal final para el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fb238-146">You simply multiply each sample by the floating-point value that represents the percentage of the final signal for the sample.</span></span> <span data-ttu-id="fb238-147">Multiplique el ejemplo de entrada por el valor almacenado en m \_ fDryMix; multiplique el ejemplo de retraso por el valor almacenado en m \_ fWetMix.</span><span class="sxs-lookup"><span data-stu-id="fb238-147">Multiply the input sample by the value stored in m\_fDryMix; multiply the delay sample by the value stored in m\_fWetMix.</span></span> <span data-ttu-id="fb238-148">A continuación, agregue los dos valores.</span><span class="sxs-lookup"><span data-stu-id="fb238-148">Then, add the two values.</span></span> <span data-ttu-id="fb238-149">El código que debe agregar es idéntico para las secciones de 8 y 16 bits:</span><span class="sxs-lookup"><span data-stu-id="fb238-149">The code you must add is identical for the 8-bit and 16-bit sections:</span></span>


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a><span data-ttu-id="fb238-150">Escribir los datos en el búfer de salida</span><span class="sxs-lookup"><span data-stu-id="fb238-150">Write the Data to the Output Buffer</span></span>

<span data-ttu-id="fb238-151">Por último, copie la muestra mixta en el búfer de salida y, a continuación, avance el puntero del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="fb238-151">Finally, copy the mixed sample to the output buffer, and then advance the output buffer pointer.</span></span> <span data-ttu-id="fb238-152">En el caso de audio de 8 bits, el Asistente para complementos usa el código siguiente para devolver el ejemplo a su intervalo original:</span><span class="sxs-lookup"><span data-stu-id="fb238-152">For 8-bit audio, the plug-in wizard uses the following code to return the sample to its original range:</span></span>


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



<span data-ttu-id="fb238-153">En el caso de audio de 16 bits, el asistente usa el siguiente código como último paso del bucle de procesamiento:</span><span class="sxs-lookup"><span data-stu-id="fb238-153">For 16-bit audio, the wizard uses the following code as the final step in the processing loop:</span></span>


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a><span data-ttu-id="fb238-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb238-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb238-155">**Implementación de CEcho::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="fb238-155">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




