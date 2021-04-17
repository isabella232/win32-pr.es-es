---
title: Procesamiento de los datos de audio
description: Procesamiento de los datos de audio
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- Complementos de Media Player de Windows, método echo de ejemplo DoProcessOutput
- complementos, método echo de ejemplo DoProcessOutput
- Complementos de procesamiento de señal digital, ejemplo echo método DoProcessOutput
- Complementos DSP, método echo de ejemplo DoProcessOutput
- Ejemplo de complemento DSP de eco, método DoProcessOutput
- Ejemplo de complemento DSP de eco, datos de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc14acb99aed20825ff970025363c6a795a0c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704723"
---
# <a name="processing-the-audio-data"></a><span data-ttu-id="5511f-109">Procesamiento de los datos de audio</span><span class="sxs-lookup"><span data-stu-id="5511f-109">Processing the Audio Data</span></span>

<span data-ttu-id="5511f-110">La implementación predeterminada de **DoProcessOutput** comienza mediante la recuperación de un puntero a una estructura **WAVEFORMATEX** válida, tal como se hizo en **AllocateStreamingResources**.</span><span class="sxs-lookup"><span data-stu-id="5511f-110">The default implementation of **DoProcessOutput** begins by retrieving a pointer to a valid **WAVEFORMATEX** structure, exactly like was done in **AllocateStreamingResources**.</span></span> <span data-ttu-id="5511f-111">A continuación, usa la información de esa estructura para calcular el número de muestras en el búfer de entrada en espera de ser procesadas.</span><span class="sxs-lookup"><span data-stu-id="5511f-111">It then uses the information in that structure to calculate the number of samples in the input buffer waiting to be processed.</span></span> <span data-ttu-id="5511f-112">El código siguiente procede de la implementación predeterminada:</span><span class="sxs-lookup"><span data-stu-id="5511f-112">The following code is from the default implementation:</span></span>


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



<span data-ttu-id="5511f-113">A continuación, el código inspecciona el miembro **wBitsPerSample** para determinar la profundidad de bits del audio.</span><span class="sxs-lookup"><span data-stu-id="5511f-113">Then, the code inspects the **wBitsPerSample** member to determine the bit depth of the audio.</span></span> <span data-ttu-id="5511f-114">Este valor se usa en una instrucción switch para proporcionar procesamiento independiente para audio de 8 y 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5511f-114">This value is used in a switch statement to provide separate processing for 8-bit and 16-bit audio.</span></span>

## <a name="differences-between-8-bit-and-16-bit-audio"></a><span data-ttu-id="5511f-115">Diferencias entre audio de 8 y 16 bits</span><span class="sxs-lookup"><span data-stu-id="5511f-115">Differences Between 8-bit and 16-bit Audio</span></span>

<span data-ttu-id="5511f-116">Hay diferencias importantes entre el audio de 8 y 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5511f-116">There are important differences between 8-bit and 16-bit audio.</span></span> <span data-ttu-id="5511f-117">Por lo tanto, las rutinas de procesamiento para crear el efecto de eco son diferentes.</span><span class="sxs-lookup"><span data-stu-id="5511f-117">Therefore, the processing routines to create the echo effect are different.</span></span> <span data-ttu-id="5511f-118">Los dos formatos se diferencian de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="5511f-118">The two formats differ in the following ways:</span></span>

-   <span data-ttu-id="5511f-119">Cada formato tiene un tamaño de muestra diferente: los ejemplos de 8 bits ocupan un byte de memoria, mientras que los ejemplos de 16 bits ocupan dos bytes.</span><span class="sxs-lookup"><span data-stu-id="5511f-119">Each format has a different sample size: 8-bit samples each occupy one byte of memory, while 16-bit samples each occupy two bytes.</span></span>
-   <span data-ttu-id="5511f-120">Cada formato representa la amplitud de audio de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="5511f-120">Each format represents the audio amplitude differently.</span></span> <span data-ttu-id="5511f-121">el audio de 8 bits se representa mediante un entero sin signo con un intervalo de 0 a 255; un valor de 128 representa el silencio.</span><span class="sxs-lookup"><span data-stu-id="5511f-121">8-bit audio is represented by an unsigned integer with a range from 0 to 255; a value of 128 represents silence.</span></span> <span data-ttu-id="5511f-122">el audio de 16 bits se representa mediante un entero con signo con un intervalo de-32768 a 32767; un valor de cero representa el silencio.</span><span class="sxs-lookup"><span data-stu-id="5511f-122">16-bit audio is represented by a signed integer with a range from -32768 to 32767; a value of zero represents silence.</span></span>

<span data-ttu-id="5511f-123">Aunque el proceso de creación del efecto de eco es fundamentalmente idéntico para cada formato, los detalles deben diferir ligeramente.</span><span class="sxs-lookup"><span data-stu-id="5511f-123">While the process of creating the echo effect is fundamentally identical for each format, the details must differ slightly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5511f-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5511f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5511f-125">**Implementación de CEcho::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="5511f-125">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




