---
title: Implementación de DoProcessOutput
description: Implementación de DoProcessOutput
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Complementos de Windows Media Player, audio DSP
- complementos, DSP de audio
- Complementos de procesamiento de señal digital, DoProcessOutput
- Complementos DSP, DoProcessOutput
- Complementos de DSP de audio, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68562444a3a8f0bfacad26fc5246181d33cefa2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418811"
---
# <a name="implementing-doprocessoutput"></a><span data-ttu-id="8bf5a-108">Implementación de DoProcessOutput</span><span class="sxs-lookup"><span data-stu-id="8bf5a-108">Implementing DoProcessOutput</span></span>

<span data-ttu-id="8bf5a-109">Para procesar los datos de audio, debe realizar varios pasos en **DoProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-109">To process audio data, you'll need to perform several steps in **DoProcessOutput**.</span></span> <span data-ttu-id="8bf5a-110">En los pasos siguientes se usa el código de ejemplo del Asistente para complementos como ejemplos.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-110">The following steps use the plug-in wizard sample code as examples.</span></span> <span data-ttu-id="8bf5a-111">Si desea crear un complemento DSP de audio que procese el contenido multimedia del mismo tipo que el código de ejemplo del Asistente para complementos, solo tendrá que cambiar el código de procesamiento real al que se hace referencia en el paso 6.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-111">If you want to create an audio DSP plug-in that processes media content of the same type that the plug-in wizard sample code does, you'll only need to change the actual processing code referred to in step 6.</span></span> <span data-ttu-id="8bf5a-112">A continuación se enumeran todos los pasos implementados en **DoProcessOutput**:</span><span class="sxs-lookup"><span data-stu-id="8bf5a-112">Following are all the steps implemented in **DoProcessOutput**:</span></span>

-   <span data-ttu-id="8bf5a-113">Si el complemento no está habilitado actualmente, simplemente copie los datos sin modificar en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-113">If the plug-in is not currently enabled, simply copy the data unchanged into the output buffer.</span></span> <span data-ttu-id="8bf5a-114">Si el complemento convierte los datos en un formato diferente, también debe realizar el procesamiento de la conversión aquí.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-114">If your plug-in converts the data into a different format, you must also do the conversion processing here.</span></span>

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   <span data-ttu-id="8bf5a-115">Recupera un puntero a la estructura de formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-115">Retrieve a pointer to the input format structure.</span></span> <span data-ttu-id="8bf5a-116">Deberá recuperar los datos de los miembros de esta estructura, de modo que copie el puntero de *m \_ mtInput*.**pbformat** a una variable de puntero local de un tipo que coincide con el tipo de estructura de formato.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-116">You'll need to retrieve member data from this structure, so copy the pointer from *m\_mtInput*.**pbformat** to a local pointer variable of a type that matches the format structure type.</span></span> <span data-ttu-id="8bf5a-117">En el ejemplo siguiente se almacena un puntero a una estructura de formato de entrada de **WAVEFORMATEX** :</span><span class="sxs-lookup"><span data-stu-id="8bf5a-117">The following example stores a pointer to a **WAVEFORMATEX** input format structure:</span></span>

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   <span data-ttu-id="8bf5a-118">Calcular el número de muestras que se van a procesar.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-118">Calculate the number of samples to process.</span></span> <span data-ttu-id="8bf5a-119">El código de ejemplo que genera el Asistente para complementos realiza este paso dividiendo el número de bytes que va a procesar el miembro **nBlockAlign** de la estructura de formato de entrada WAVEFORMATEX y multiplicando el resultado por el número de canales, que se almacenó en el miembro **nChannels** .</span><span class="sxs-lookup"><span data-stu-id="8bf5a-119">The sample code that the plug-in wizard generates performs this step by dividing the number of bytes to process by the **nBlockAlign** member of the WAVEFORMATEX input format structure, and then multiplying the result by the number of channels, which was stored in the **nChannels** member.</span></span> <span data-ttu-id="8bf5a-120">El ejemplo siguiente es del código de ejemplo del Asistente para complementos:</span><span class="sxs-lookup"><span data-stu-id="8bf5a-120">The following example is from the plug-in wizard sample code:</span></span>

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  <span data-ttu-id="8bf5a-121">Determine la profundidad de bits del audio.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-121">Determine the bit depth of the audio.</span></span> <span data-ttu-id="8bf5a-122">El código de ejemplo del Asistente para complementos determina el audio de 8 o 16 bits mediante la inspección del miembro **wBitsPerSample** de la estructura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="8bf5a-122">The plug-in wizard sample code determines 8-bit or 16-bit audio by inspecting the **wBitsPerSample** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="8bf5a-123">A continuación, utiliza ese valor en una instrucción switch para proporcionar rutinas de procesamiento independientes para cada profundidad de bits.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-123">It then uses that value in a switch statement to provide separate processing routines for each bit depth.</span></span> <span data-ttu-id="8bf5a-124">Es posible que tenga que usar una técnica diferente al tratar con otros tipos de formato y profundidades de bits.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-124">You may need to use a different technique when dealing with other format types and bit depths.</span></span>
    2.  <span data-ttu-id="8bf5a-125">Cree un bucle para recorrer los ejemplos de audio en el búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-125">Create a loop to step through the audio samples in the input buffer.</span></span>
    3.  <span data-ttu-id="8bf5a-126">Recupera un ejemplo del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-126">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="8bf5a-127">Para ello, desreferencia el puntero de datos de entrada y almacena el resultado en una variable de tipo int. En el caso de audio de 16 bits, debe reconvertir el puntero de BYTEs en un puntero corto para controlar la precisión de ejemplo de audio mayor.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-127">You do this by dereferencing the input data pointer and storing the result in a variable of type int. For 16-bit audio, you must recast the BYTE pointer to a short pointer to handle the greater audio sample precision.</span></span> <span data-ttu-id="8bf5a-128">Una vez que tenga el valor, puede incrementar inmediatamente el puntero *pbInputData* para que apunte al ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-128">Once you have the value, you can immediately increment the *pbInputData* pointer so that it points to the next sample.</span></span> <span data-ttu-id="8bf5a-129">En los siguientes ejemplos se muestra lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8bf5a-129">The following examples demonstrate this:</span></span>

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    <span data-ttu-id="8bf5a-130">O bien</span><span class="sxs-lookup"><span data-stu-id="8bf5a-130">-or-</span></span>

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  <span data-ttu-id="8bf5a-131">Realice el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-131">Perform the processing.</span></span> <span data-ttu-id="8bf5a-132">Aquí es donde se aplican los algoritmos que cambian el ejemplo de algún modo.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-132">This is where you apply the algorithms that change the sample somehow.</span></span> <span data-ttu-id="8bf5a-133">Lo que hace aquí depende de usted.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-133">What you do here is up to you.</span></span>
    2.  <span data-ttu-id="8bf5a-134">Escriba los datos procesados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-134">Write the processed data to the output buffer.</span></span> <span data-ttu-id="8bf5a-135">Incremente inmediatamente el puntero en el búfer de salida, como en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8bf5a-135">Immediately increment the pointer to the output buffer, as in the following example:</span></span>

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  <span data-ttu-id="8bf5a-136">Repita el bucle hasta que se hayan procesado todos los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-136">Repeat the loop until all the samples have been processed.</span></span>
    2.  <span data-ttu-id="8bf5a-137">Devuelve un **valor HRESULT** adecuado.</span><span class="sxs-lookup"><span data-stu-id="8bf5a-137">Return an appropriate **HRESULT**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bf5a-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bf5a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bf5a-139">**Implementar un complemento de DSP de audio**</span><span class="sxs-lookup"><span data-stu-id="8bf5a-139">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




