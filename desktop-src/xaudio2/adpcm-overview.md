---
description: Adaptive Differential Pulse Code Modulation (ADPCM) es un formato de compresión con pérdida que se implementa para XAudio2 con el fin de proporcionar características adicionales para especificar el tamaño del bloque de ejemplo de compresión.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Información general de ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb918a611cb0840b2f02dfb13b547b795fb3304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716385"
---
# <a name="adpcm-overview"></a><span data-ttu-id="e3164-103">Información general de ADPCM</span><span class="sxs-lookup"><span data-stu-id="e3164-103">ADPCM Overview</span></span>

<span data-ttu-id="e3164-104">Adaptive Differential Pulse Code Modulation (ADPCM) es un formato de compresión con pérdida que se implementa para XAudio2 con el fin de proporcionar características adicionales para especificar el tamaño del bloque de ejemplo de compresión.</span><span class="sxs-lookup"><span data-stu-id="e3164-104">Adaptive Differential Pulse Code Modulation (ADPCM) is a lossy compression format that is implemented for XAudio2 to provide additional features for specifying the size of the compression sample block.</span></span> <span data-ttu-id="e3164-105">Con un formato de compresión con pérdida, algunos datos se modifican y se pierden durante la compresión.</span><span class="sxs-lookup"><span data-stu-id="e3164-105">With a lossy compression format some data is altered and lost during compression.</span></span> <span data-ttu-id="e3164-106">ADPCM puede lograr relaciones de compresión de hasta 4:1.</span><span class="sxs-lookup"><span data-stu-id="e3164-106">ADPCM can achieve compression ratios of up to 4:1.</span></span>

<span data-ttu-id="e3164-107">La implementación de ADPCM para XAudio2 proporciona características adicionales para especificar el tamaño del bloque de ejemplo de compresión.</span><span class="sxs-lookup"><span data-stu-id="e3164-107">The implementation of ADPCM for XAudio2 provides additional features to specify the size of the compression sample block.</span></span> <span data-ttu-id="e3164-108">ADPCM permite al diseñador de audio elegir una configuración que es un compromiso adecuado entre el tamaño, la calidad y la resolución (para colocar puntos de bucle).</span><span class="sxs-lookup"><span data-stu-id="e3164-108">ADPCM enables the audio designer to choose a setting that is an appropriate compromise among size, quality, and resolution (for placing loop points).</span></span>

<span data-ttu-id="e3164-109">XAudio2 usa una versión modificada del códec Microsoft ADPCM que admite el formato de datos extendidos necesario para proporcionar tamaños de bloque de ejemplo personalizados.</span><span class="sxs-lookup"><span data-stu-id="e3164-109">XAudio2 uses a modified version of the Microsoft ADPCM codec that supports the extended data formatting required to provide custom sample block sizes.</span></span> <span data-ttu-id="e3164-110">Por esta razón, los motores de audio que no admiten esta versión del códec ADPCM no pueden reproducir los datos de audio de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e3164-110">For this reason, XAudio2 audio data cannot be played by audio engines that do not support this version of the ADPCM codec.</span></span>

> [!Note]  
> <span data-ttu-id="e3164-111">Actualmente, la compresión ADPCM solo está disponible para Windows, incluidas las implementaciones de XNA Game Studio Express para Windows.</span><span class="sxs-lookup"><span data-stu-id="e3164-111">Currently, ADPCM compression is only available for Windows, including XNA Game Studio Express for Windows deployments.</span></span>

 

## <a name="adpcm-encoding"></a><span data-ttu-id="e3164-112">Codificación ADPCM</span><span class="sxs-lookup"><span data-stu-id="e3164-112">ADPCM Encoding</span></span>

<span data-ttu-id="e3164-113">Los datos de audio se codifican en ADPCM mediante la herramienta de línea de comandos AdpcmEncode.</span><span class="sxs-lookup"><span data-stu-id="e3164-113">Audio data is encoded to ADPCM using the AdpcmEncode command-line tool.</span></span>

-   <span data-ttu-id="e3164-114">AdpcmEncode</span><span class="sxs-lookup"><span data-stu-id="e3164-114">AdpcmEncode</span></span>

    <span data-ttu-id="e3164-115">Para codificar archivos de audio como ADPCM para su uso con XAudio2, use la herramienta de línea de comandos **AdpcmEncode** .</span><span class="sxs-lookup"><span data-stu-id="e3164-115">In order to encode audio files as ADPCM for use with XAudio2, use the **AdpcmEncode** command-line tool.</span></span>

## <a name="adpcm-decoding"></a><span data-ttu-id="e3164-116">Descodificación ADPCM</span><span class="sxs-lookup"><span data-stu-id="e3164-116">ADPCM Decoding</span></span>

<span data-ttu-id="e3164-117">La descodificación de software de ADPCM es compatible con XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e3164-117">Software decoding of ADPCM is supported in XAudio2.</span></span>

-   <span data-ttu-id="e3164-118">XAudio2</span><span class="sxs-lookup"><span data-stu-id="e3164-118">XAudio2</span></span>

    <span data-ttu-id="e3164-119">Para usar datos codificados ADPCM en XAudio2, debe inicializar una estructura **ADPCMWAVEFORMAT** con valores específicos de ADPCM y pasarla como argumento a [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) cuando cree una voz de origen.</span><span class="sxs-lookup"><span data-stu-id="e3164-119">In order to use ADPCM encoded data in XAudio2, you need to initialize a **ADPCMWAVEFORMAT** structure with ADPCM specific values, and pass it as an argument to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) when you create a source voice.</span></span> <span data-ttu-id="e3164-120">Para obtener un ejemplo de carga y reproducción de un sonido en XAudio2, consulte [Cómo: reproducir un sonido con xaudio2](how-to--play-a-sound-with-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="e3164-120">For an example of loading and playing a sound in XAudio2, see [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md).</span></span>

## <a name="samplesperblock"></a><span data-ttu-id="e3164-121">SamplesPerBlock</span><span class="sxs-lookup"><span data-stu-id="e3164-121">SamplesPerBlock</span></span>

<span data-ttu-id="e3164-122">La compresión ADPCM funciona mediante la separación de la forma de onda en bloques y la predicción de la variación de los ejemplos de la forma de onda en cada bloque.</span><span class="sxs-lookup"><span data-stu-id="e3164-122">ADPCM compression works by separating the waveform into blocks, and predicting the variation of the waveform samples within each block.</span></span> <span data-ttu-id="e3164-123">El tamaño de los bloques se mide en ejemplos.</span><span class="sxs-lookup"><span data-stu-id="e3164-123">The size of the blocks is measured in samples.</span></span> <span data-ttu-id="e3164-124">El tamaño de bloque más pequeño es 32 ejemplos y el más alto es 512 ejemplos.</span><span class="sxs-lookup"><span data-stu-id="e3164-124">The smallest block size is 32 samples, and the highest is 512 samples.</span></span>

<span data-ttu-id="e3164-125">Los bloques más grandes permiten una mejor compresión, lo que da lugar a tamaños de archivo más pequeños, pero a costa de una calidad y resolución de sonido para alinear puntos de bucle.</span><span class="sxs-lookup"><span data-stu-id="e3164-125">Larger blocks allow better compression, which results in smaller file sizes, but at the expense of sound quality and resolution for aligning loop points.</span></span>

<span data-ttu-id="e3164-126">En general, la modificación del valor de SamplesPerBlock produce estos inconvenientes:</span><span class="sxs-lookup"><span data-stu-id="e3164-126">In general, modifying the SamplesPerBlock value results in these tradeoffs:</span></span>



| <span data-ttu-id="e3164-127">Si SamplesPerBlock...</span><span class="sxs-lookup"><span data-stu-id="e3164-127">If SamplesPerBlock...</span></span>      | <span data-ttu-id="e3164-128">Compresión de archivos</span><span class="sxs-lookup"><span data-stu-id="e3164-128">File Compression</span></span> | <span data-ttu-id="e3164-129">Calidad del sonido</span><span class="sxs-lookup"><span data-stu-id="e3164-129">Sound Quality</span></span> | <span data-ttu-id="e3164-130">Resolución del punto de bucle</span><span class="sxs-lookup"><span data-stu-id="e3164-130">Loop Point Resolution</span></span> |
|----------------------------|------------------|---------------|-----------------------|
| <span data-ttu-id="e3164-131">Aumenta (hasta el máximo 512)</span><span class="sxs-lookup"><span data-stu-id="e3164-131">Increases (up to max 512)</span></span>  | <span data-ttu-id="e3164-132">Medida</span><span class="sxs-lookup"><span data-stu-id="e3164-132">Increases</span></span>        | <span data-ttu-id="e3164-133">DISMINUI</span><span class="sxs-lookup"><span data-stu-id="e3164-133">Decreases</span></span>     | <span data-ttu-id="e3164-134">DISMINUI</span><span class="sxs-lookup"><span data-stu-id="e3164-134">Decreases</span></span>             |
| <span data-ttu-id="e3164-135">Disminuye (baja a min 32)</span><span class="sxs-lookup"><span data-stu-id="e3164-135">Decreases (down to min 32)</span></span> | <span data-ttu-id="e3164-136">DISMINUI</span><span class="sxs-lookup"><span data-stu-id="e3164-136">Decreases</span></span>        | <span data-ttu-id="e3164-137">Medida</span><span class="sxs-lookup"><span data-stu-id="e3164-137">Increases</span></span>     | <span data-ttu-id="e3164-138">Medida</span><span class="sxs-lookup"><span data-stu-id="e3164-138">Increases</span></span>             |



 

## <a name="restrictions"></a><span data-ttu-id="e3164-139">Restricciones</span><span class="sxs-lookup"><span data-stu-id="e3164-139">Restrictions</span></span>

<span data-ttu-id="e3164-140">Dado que ADPCM usa bloques de ejemplo que se alinean uno tras otro, una onda comprimida con ADPCM puede tener un bloque parcial sin terminar en su extremo.</span><span class="sxs-lookup"><span data-stu-id="e3164-140">Because ADPCM uses sample blocks that are aligned one after the other, a wave compressed with ADPCM may have an unfinished, partial block at its end.</span></span> <span data-ttu-id="e3164-141">El descodificador ADPCM genera un silencio para el resto de este bloque parcial, lo que evita que la onda se repita sin problemas.</span><span class="sxs-lookup"><span data-stu-id="e3164-141">The ADPCM decoder generates silence for the remainder of this partial block, which keeps the wave from looping seamlessly.</span></span>

<span data-ttu-id="e3164-142">El valor del parámetro *SamplesPerBlock* afecta a la resolución con la que se pueden alinear los datos de onda y los puntos de bucle.</span><span class="sxs-lookup"><span data-stu-id="e3164-142">The value of the *SamplesPerBlock* parameter affects the resolution with which you can align wave data and loop points.</span></span>

<span data-ttu-id="e3164-143">Si intenta aplicar la compresión a una onda no alineada, obtendrá un error o una advertencia dependiendo de si se usa la onda en cualquier evento de reproducción de bucle.</span><span class="sxs-lookup"><span data-stu-id="e3164-143">If you try to apply compression to a non-aligned wave, you will get an error or a warning depending on whether the wave is used in any looping play events.</span></span> <span data-ttu-id="e3164-144">No se puede comprimir una onda utilizada en ningún evento de reproducción de bucle.</span><span class="sxs-lookup"><span data-stu-id="e3164-144">You cannot compress a wave used in any looping play events.</span></span> <span data-ttu-id="e3164-145">Quítelo de los eventos de reproducción en bucle y vuelva a aplicar la compresión.</span><span class="sxs-lookup"><span data-stu-id="e3164-145">Remove it from the looping play events, and re-apply compression.</span></span>

<span data-ttu-id="e3164-146">Si usa la ola exclusivamente en el modo sin bucles, la restricción de alineación de bloque de ejemplo no se aplica.</span><span class="sxs-lookup"><span data-stu-id="e3164-146">If you use the wave exclusively in non-looping mode, the sample block alignment restriction does not apply.</span></span>

## <a name="adpcm-file-structure"></a><span data-ttu-id="e3164-147">Estructura de archivos ADPCM</span><span class="sxs-lookup"><span data-stu-id="e3164-147">ADPCM File Structure</span></span>

<span data-ttu-id="e3164-148">Un archivo ADPCM es un archivo RIFF estándar con los siguientes tipos de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="e3164-148">An ADPCM file is a standard RIFF file with the following chunk types.</span></span>



| <span data-ttu-id="e3164-149">Fragmento FCC</span><span class="sxs-lookup"><span data-stu-id="e3164-149">Chunk FCC</span></span>     | <span data-ttu-id="e3164-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3164-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3164-151">RIFF</span><span class="sxs-lookup"><span data-stu-id="e3164-151">RIFF</span></span>          | <span data-ttu-id="e3164-152">Fragmento RIFF estándar que contiene un tipo de archivo con el valor WAVE en los primeros cuatro bytes de su sección de datos y los demás fragmentos del archivo en el resto de la sección de datos.</span><span class="sxs-lookup"><span data-stu-id="e3164-152">Standard RIFF chunk containing a file type with the value WAVE in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="e3164-153">FMT</span><span class="sxs-lookup"><span data-stu-id="e3164-153">fmt</span></span>           | <span data-ttu-id="e3164-154">Contiene el encabezado de formato del archivo ADPCM.</span><span class="sxs-lookup"><span data-stu-id="e3164-154">Contains the format header for the ADPCM file.</span></span> <span data-ttu-id="e3164-155">Los datos de este fragmento se corresponden con una estructura **ADPCMWAVEFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="e3164-155">The data in this chunk corresponds to a **ADPCMWAVEFORMAT** structure.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e3164-156">datos</span><span class="sxs-lookup"><span data-stu-id="e3164-156">data</span></span>          | <span data-ttu-id="e3164-157">Contiene los datos de audio ADPCM codificados.</span><span class="sxs-lookup"><span data-stu-id="e3164-157">Contains the encoded ADPCM audio data.</span></span> <span data-ttu-id="e3164-158">Al usar ADPCM en XAudio2, debe leer el contenido del fragmento de datos en un búfer y pasarlo a una voz de origen como el miembro **pAudioData** de una estructura de [**\_ búfer de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="e3164-158">When you use ADPCM in XAudio2, you need to read the contents of the data chunk into a buffer, and pass it to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="e3164-159">No es necesario intercambiar bytes en el contenido del fragmento de datos.</span><span class="sxs-lookup"><span data-stu-id="e3164-159">You don't need to byte swap the contents of the data chunk.</span></span>                                                                                                                            |
| <span data-ttu-id="e3164-160">smpl y wsmp</span><span class="sxs-lookup"><span data-stu-id="e3164-160">smpl and wsmp</span></span> | <span data-ttu-id="e3164-161">Tipos de fragmentos opcionales que contienen la información de bucle del archivo ADPCM.</span><span class="sxs-lookup"><span data-stu-id="e3164-161">Optional chunk types containing the looping information for the ADPCM file.</span></span> <span data-ttu-id="e3164-162">Al usar ADPCM en XAudio2, los valores contenidos en los fragmentos de Smpl o wsmp se usan para rellenar los miembros **LoopBeginLoopLength** y **LoopCount** de la estructura de [**\_ búfer de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="e3164-162">When you use ADPCM in XAudio2, the values contained in the smpl or wsmp chunks are used to populate the **LoopBeginLoopLength** and **LoopCount** members of the [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="e3164-163">En la consola Xbox 360, debe intercambiar bytes de los datos cargados desde un fragmento smpl para tener en cuenta la diferencia modos endian entre Windows y Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="e3164-163">On the Xbox 360, you need to byte swap the data loaded from a smpl chunk to account for the endianness difference between Windows and Xbox 360.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e3164-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3164-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3164-165">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="e3164-165">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
