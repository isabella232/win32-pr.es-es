---
title: Implementación de IMediaObject AllocateStreamingResources
description: Implementación de IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Complementos de Windows Media Player, echo ejemplo de recursos de streaming
- complementos, echo ejemplo de recursos de streaming
- Complementos de procesamiento de señal digital, echo ejemplo de recursos de streaming
- Complementos DSP, echo ejemplo de recursos de streaming
- Ejemplo de complemento DSP de eco, recursos de streaming
- Ejemplo de complemento DSP de eco, búfer de retraso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e347e35eaabbcbcc00a586e4cba0d8ad31cc6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418831"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a><span data-ttu-id="742f9-109">Implementación de IMediaObject:: AllocateStreamingResources</span><span class="sxs-lookup"><span data-stu-id="742f9-109">Implementing IMediaObject::AllocateStreamingResources</span></span>

<span data-ttu-id="742f9-110">En el ejemplo echo, el método **AllocateStreamingResources** crea el búfer de retraso.</span><span class="sxs-lookup"><span data-stu-id="742f9-110">In the Echo sample, the **AllocateStreamingResources** method creates the delay buffer.</span></span> <span data-ttu-id="742f9-111">Para ello, hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="742f9-111">It does this by doing the following:</span></span>

1.  <span data-ttu-id="742f9-112">Calcular un tamaño para el búfer que corresponde al tiempo de retraso especificado para el tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="742f9-112">Calculating a size for the buffer that corresponds to the specified delay time for the given media type.</span></span>
2.  <span data-ttu-id="742f9-113">Asignando nueva memoria o reasignando el tamaño del búfer si ya existe.</span><span class="sxs-lookup"><span data-stu-id="742f9-113">Either allocating new memory or reallocating the buffer size if it already exists.</span></span>
3.  <span data-ttu-id="742f9-114">Llamar a un método que rellena el búfer con valores que representan el silencio.</span><span class="sxs-lookup"><span data-stu-id="742f9-114">Calling a method that fills the buffer with values representing silence.</span></span>

<span data-ttu-id="742f9-115">El valor del silencio es diferente en función de la profundidad de bits.</span><span class="sxs-lookup"><span data-stu-id="742f9-115">The value for silence is different depending upon the bit depth.</span></span> <span data-ttu-id="742f9-116">En el caso de audio de 8 bits, el silencio se representa mediante el valor hexadecimal 80; en el caso de audio de 16 bits, el silencio se representa con cero.</span><span class="sxs-lookup"><span data-stu-id="742f9-116">For 8-bit audio, silence is represented by the hex value 80; for 16-bit audio, silence is represented by zero.</span></span>

## <a name="calculating-the-delay-buffer-size"></a><span data-ttu-id="742f9-117">Calcular el tamaño del búfer de retraso</span><span class="sxs-lookup"><span data-stu-id="742f9-117">Calculating the Delay Buffer Size</span></span>

<span data-ttu-id="742f9-118">Para calcular el tamaño necesario para el búfer de retraso, primero debe recuperar una estructura **WAVEFORMATEX** que contenga información sobre los datos de audio.</span><span class="sxs-lookup"><span data-stu-id="742f9-118">In order to calculate the size required for the delay buffer, you must first retrieve a **WAVEFORMATEX** structure that contains information about the audio data.</span></span> <span data-ttu-id="742f9-119">En el ejemplo siguiente se recupera un puntero a esta estructura a partir de la estructura de **\_ \_ tipo de medio DMO** de entrada:</span><span class="sxs-lookup"><span data-stu-id="742f9-119">The following example retrieves a pointer to this structure from the input **DMO\_MEDIA\_TYPE** structure:</span></span>


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



<span data-ttu-id="742f9-120">Una vez que haya almacenado un puntero a la estructura **WAVEFORMATEX** adecuada, puede inspeccionar sus miembros y usarlos para calcular el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="742f9-120">Once you have stored a pointer to the proper **WAVEFORMATEX** structure, you can inspect its members and use them to calculate the required buffer size.</span></span> <span data-ttu-id="742f9-121">En el ejemplo de código siguiente se muestra esto:</span><span class="sxs-lookup"><span data-stu-id="742f9-121">The following code example demonstrates this:</span></span>


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



<span data-ttu-id="742f9-122">Este algoritmo calcula el tamaño del búfer multiplicando el tiempo de retraso, en milisegundos, por el número de muestras por milisegundo, multiplicando el resultado por el número de canales y multiplicando el resultado por el número de bytes por muestra.</span><span class="sxs-lookup"><span data-stu-id="742f9-122">This algorithm computes the buffer size by multiplying the delay time, in milliseconds, by the number of samples per millisecond, then multiplying the result by the number of channels, and then multiplying the result by the number of bytes per sample.</span></span> <span data-ttu-id="742f9-123">El número de canales y el número de bytes por muestra no son obvios; se codifican en el miembro nBlockAlign.</span><span class="sxs-lookup"><span data-stu-id="742f9-123">The number of channels and the number of bytes per sample are not obvious; they are encoded in the nBlockAlign member.</span></span> <span data-ttu-id="742f9-124">La división por 1000 reduce el valor de nSamplesPerSec a muestras por milisegundo; el milisegundo es la unidad deseada porque el tiempo de retardo se expresa en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="742f9-124">Dividing by 1000 reduces the nSamplesPerSec value to samples per millisecond; the millisecond is the desired unit because the delay time is expressed in milliseconds.</span></span>

## <a name="allocating-the-delay-buffer-memory"></a><span data-ttu-id="742f9-125">Asignación de memoria de búfer de retraso</span><span class="sxs-lookup"><span data-stu-id="742f9-125">Allocating the Delay Buffer Memory</span></span>

<span data-ttu-id="742f9-126">Una vez que haya calculado los requisitos de memoria, puede asignar el búfer.</span><span class="sxs-lookup"><span data-stu-id="742f9-126">Once you have calculated the memory requirements, you can allocate the buffer.</span></span> <span data-ttu-id="742f9-127">Es posible que sea necesario eliminar el búfer si existe, como cuando el usuario invoca la página de propiedades para cambiar el valor de tiempo de retraso.</span><span class="sxs-lookup"><span data-stu-id="742f9-127">The buffer may need to be deleted if it exists, such as when the user invokes the property page to change the delay time value.</span></span> <span data-ttu-id="742f9-128">En el código siguiente se muestra la asignación del búfer de retraso:</span><span class="sxs-lookup"><span data-stu-id="742f9-128">The following code demonstrates allocating the delay buffer:</span></span>


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



<span data-ttu-id="742f9-129">Si el búfer se asigna correctamente, debe mover el puntero movible al encabezado del búfer, tal y como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="742f9-129">If the buffer is successfully allocated, you should move the movable pointer to the head of the buffer, as demonstrated in the following example:</span></span>


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a><span data-ttu-id="742f9-130">Llenado del búfer de retraso con silencio</span><span class="sxs-lookup"><span data-stu-id="742f9-130">Filling the Delay Buffer with Silence</span></span>

<span data-ttu-id="742f9-131">Es conveniente escribir un método para rellenar el búfer de retraso con valores que representan el silencio.</span><span class="sxs-lookup"><span data-stu-id="742f9-131">It is convenient to write a method to fill the delay buffer with values representing silence.</span></span> <span data-ttu-id="742f9-132">El método debe recibir el puntero a la estructura WAVEFORMATEX válida y, a continuación, inspeccionar el miembro wBitsPerSample para determinar si el audio es de 8 bits o superior.</span><span class="sxs-lookup"><span data-stu-id="742f9-132">The method should receive the pointer to the valid WAVEFORMATEX structure and then inspect the wBitsPerSample member to determine whether the audio is 8-bit or higher.</span></span> <span data-ttu-id="742f9-133">En el ejemplo siguiente se rellena el búfer de retraso con el valor correcto para el silencio:</span><span class="sxs-lookup"><span data-stu-id="742f9-133">The following example fills the delay buffer with the correct value for silence:</span></span>


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



<span data-ttu-id="742f9-134">No olvide agregar la declaración adelantada de la función al archivo de encabezado echo. h en la sección privada:</span><span class="sxs-lookup"><span data-stu-id="742f9-134">Remember to add the forward declaration for the function to the header file Echo.h in the private section:</span></span>


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



<span data-ttu-id="742f9-135">Debe agregar código al final de AllocateStreamingResources para llamar a este método cada vez que se crea o se cambia el tamaño del búfer de retraso.</span><span class="sxs-lookup"><span data-stu-id="742f9-135">You should add code at the end of AllocateStreamingResources to call this method each time the delay buffer is created or resized.</span></span> <span data-ttu-id="742f9-136">En el código de ejemplo siguiente se pasa el puntero WAVEFORMATEX denominado pWave al nuevo método:</span><span class="sxs-lookup"><span data-stu-id="742f9-136">The following example code passes the WAVEFORMATEX pointer named pWave to the new method:</span></span>


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a><span data-ttu-id="742f9-137">Reasignar la memoria del búfer de retraso</span><span class="sxs-lookup"><span data-stu-id="742f9-137">Reallocating the Delay Buffer Memory</span></span>

<span data-ttu-id="742f9-138">Cuando el usuario cambia el tiempo de retraso mediante la página de propiedades, el tamaño del búfer de retraso también debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="742f9-138">When the user changes the delay time by using the property page, the size of the delay buffer must change as well.</span></span> <span data-ttu-id="742f9-139">Ya ha agregado el código a AllocateStreamingResources para cambiar el tamaño del búfer, pero debe agregar una línea de código a CEcho::p \_ retraso de UT para llamar al método de asignación de recursos cada vez que cambie el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="742f9-139">You've already added the code to AllocateStreamingResources to resize the buffer, but you need to add a line of code to CEcho::put\_delay to call the resource allocation method each time the property value changes.</span></span> <span data-ttu-id="742f9-140">Este es el código:</span><span class="sxs-lookup"><span data-stu-id="742f9-140">Here is the code:</span></span>


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a><span data-ttu-id="742f9-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="742f9-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="742f9-142">**Trabajar con recursos de streaming**</span><span class="sxs-lookup"><span data-stu-id="742f9-142">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




