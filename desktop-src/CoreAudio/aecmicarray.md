---
description: En este ejemplo se usan las API de audio principales para capturar una secuencia de voz de alta calidad. El ejemplo admite la cancelación de eco acústico (AEC) y el procesamiento de la matriz de micrófonos mediante AEC DMO, también denominado DSP de captura de voz, proporcionado por Microsoft.
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: AECMicArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153526"
---
# <a name="aecmicarray"></a><span data-ttu-id="bfbe3-104">AECMicArray</span><span class="sxs-lookup"><span data-stu-id="bfbe3-104">AECMicArray</span></span>

<span data-ttu-id="bfbe3-105">En este ejemplo se usan las API de audio principales para capturar una secuencia de voz de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-105">This sample uses the Core Audio APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="bfbe3-106">El ejemplo admite la cancelación de eco acústico (AEC) y el procesamiento de la matriz de micrófonos mediante AEC DMO, también denominado DSP de captura de voz, proporcionado por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-106">The sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO, also called the Voice capture DSP, provided by Microsoft .</span></span>

<span data-ttu-id="bfbe3-107">Este tema contiene las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-107">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="bfbe3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfbe3-108">Description</span></span>](#description)
-   [<span data-ttu-id="bfbe3-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfbe3-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="bfbe3-110">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="bfbe3-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="bfbe3-111">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="bfbe3-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="bfbe3-112">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="bfbe3-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="bfbe3-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bfbe3-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="bfbe3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfbe3-114">Description</span></span>

<span data-ttu-id="bfbe3-115">En este ejemplo se muestran las características siguientes.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="bfbe3-116">[MMDevice](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-116">[MMDevice](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="bfbe3-117">[WASAPI](wasapi.md) para las operaciones de administración de secuencias como el inicio y la detención de la secuencia, la conmutación por secuencias.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, stream switching.</span></span>
-   <span data-ttu-id="bfbe3-118">[DeviceTopology](devicetopology-api.md) para enumerar los adaptadores de audio.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-118">[DeviceTopology](devicetopology-api.md) for enumerating audio adapters.</span></span>
-   <span data-ttu-id="bfbe3-119">[EndpointVolume](endpointvolume-api.md) controlan los niveles de volumen de las [sesiones de audio](audio-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="bfbe3-119">[EndpointVolume](endpointvolume-api.md) control the volume levels of [audio sessions](audio-sessions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfbe3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfbe3-120">Requirements</span></span>



| <span data-ttu-id="bfbe3-121">Producto</span><span class="sxs-lookup"><span data-stu-id="bfbe3-121">Product</span></span>                                                        | <span data-ttu-id="bfbe3-122">Versión</span><span class="sxs-lookup"><span data-stu-id="bfbe3-122">Version</span></span>                     |
|----------------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="bfbe3-123">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="bfbe3-123">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="bfbe3-124">Windows Vista o posterior</span><span class="sxs-lookup"><span data-stu-id="bfbe3-124">Windows Vista or later</span></span>      |
| <span data-ttu-id="bfbe3-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bfbe3-125">Visual Studio</span></span>                                                  | <span data-ttu-id="bfbe3-126">2005 (ediciones que no son Express)</span><span class="sxs-lookup"><span data-stu-id="bfbe3-126">2005 (non-express editions)</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="bfbe3-127">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="bfbe3-127">Downloading the Sample</span></span>

<span data-ttu-id="bfbe3-128">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-128">This sample is available in the following locations.</span></span>



| <span data-ttu-id="bfbe3-129">Location</span><span class="sxs-lookup"><span data-stu-id="bfbe3-129">Location</span></span>    | <span data-ttu-id="bfbe3-130">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="bfbe3-130">Path/URL</span></span>                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfbe3-131">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="bfbe3-131">Windows SDK</span></span> | <span data-ttu-id="bfbe3-132">\\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ AECMicArray \\ ...</span><span class="sxs-lookup"><span data-stu-id="bfbe3-132">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\AECMicArray\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="bfbe3-133">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="bfbe3-133">Building the Sample</span></span>

<span data-ttu-id="bfbe3-134">Para compilar el ejemplo AecSDKDemo, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="bfbe3-134">To build the AecSDKDemo sample, use the following steps:</span></span>

1.  <span data-ttu-id="bfbe3-135">Abra una ventana de comandos del SDK.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-135">Open an SDK command window.</span></span>
2.  <span data-ttu-id="bfbe3-136">Escriba **CD% MSSDK% \\ setup**.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-136">Type **cd %MSSDK%\\Setup**.</span></span>
3.  <span data-ttu-id="bfbe3-137">Ejecute VCIntegrate.exe.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-137">Run VCIntegrate.exe.</span></span>

    <span data-ttu-id="bfbe3-138">A partir de este momento, las ventanas de comandos tendrán la configuración de entorno adecuada para compilar una aplicación que aprovecha el SDK.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-138">From this point forward, command windows will have the proper environment settings to build an application that takes advantage of the SDK.</span></span>

4.  <span data-ttu-id="bfbe3-139">Compile el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-139">Build the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="bfbe3-140">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="bfbe3-140">Running the Sample</span></span>

<span data-ttu-id="bfbe3-141">Si compila la aplicación de demostración correctamente, se genera un archivo ejecutable AecSDKDemo.exe.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-141">If you build the demo application successfully, an executable file, AecSDKDemo.exe is generated.</span></span> <span data-ttu-id="bfbe3-142">Para ejecutarlo, escriba `AecSDKDemo` en una ventana de comandos seguida de los argumentos obligatorios u opcionales, tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-142">To run it, type `AecSDKDemo` in a command window followed by required or optional arguments as described below.</span></span>

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

<span data-ttu-id="bfbe3-143">En la tabla siguiente se muestran los argumentos.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="bfbe3-144">Argumento</span><span class="sxs-lookup"><span data-stu-id="bfbe3-144">Argument</span></span>  | <span data-ttu-id="bfbe3-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfbe3-145">Description</span></span>                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfbe3-146">-out</span><span class="sxs-lookup"><span data-stu-id="bfbe3-146">-out</span></span>      | <span data-ttu-id="bfbe3-147">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-147">Required.</span></span> <span data-ttu-id="bfbe3-148">Especifica el nombre del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-148">Specifies output file name.</span></span>                                                                                                 |
| <span data-ttu-id="bfbe3-149">-mod</span><span class="sxs-lookup"><span data-stu-id="bfbe3-149">-mod</span></span>      | <span data-ttu-id="bfbe3-150">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-150">Required.</span></span> <span data-ttu-id="bfbe3-151">Especifica el modo del sistema de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-151">Specifies voice capture system mode.</span></span> <span data-ttu-id="bfbe3-152">Consulte la sección "configuración de la captura de voz DMO" del archivo Léame de ejemplo para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-152">Refer to "Configuring the voice capture DMO" section in the sample readme for details.</span></span> |
| <span data-ttu-id="bfbe3-153">-feat</span><span class="sxs-lookup"><span data-stu-id="bfbe3-153">-feat</span></span>     | <span data-ttu-id="bfbe3-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-154">Optional.</span></span> <span data-ttu-id="bfbe3-155">Activa el modo de característica en (1) o desactivado (0).</span><span class="sxs-lookup"><span data-stu-id="bfbe3-155">Turns feature mode on (1) or off (0).</span></span>                                                                                       |
| <span data-ttu-id="bfbe3-156">-NS</span><span class="sxs-lookup"><span data-stu-id="bfbe3-156">-ns</span></span>       | <span data-ttu-id="bfbe3-157">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-157">Optional.</span></span> <span data-ttu-id="bfbe3-158">Activa la supresión de ruido en (1) o desactivado (0).</span><span class="sxs-lookup"><span data-stu-id="bfbe3-158">Turns noise suppression on (1) or off (0).</span></span> <span data-ttu-id="bfbe3-159">El modo de característica debe estar activado para especificar esto.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-159">Feature mode must be on for specifying this.</span></span>                                     |
| <span data-ttu-id="bfbe3-160">-AGC</span><span class="sxs-lookup"><span data-stu-id="bfbe3-160">-agc</span></span>      | <span data-ttu-id="bfbe3-161">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-161">Optional.</span></span> <span data-ttu-id="bfbe3-162">Desactiva el AGC digital (1) o desactivado (0).</span><span class="sxs-lookup"><span data-stu-id="bfbe3-162">Turns digital AGC on (1) or off (0).</span></span> <span data-ttu-id="bfbe3-163">El modo de característica debe estar activado para especificar esto.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-163">Feature mode must be on for specifying this.</span></span>                                           |
| <span data-ttu-id="bfbe3-164">-cntrclip</span><span class="sxs-lookup"><span data-stu-id="bfbe3-164">-cntrclip</span></span> | <span data-ttu-id="bfbe3-165">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-165">Optional.</span></span> <span data-ttu-id="bfbe3-166">Activa el recorte central en (1) o desactivado (0).</span><span class="sxs-lookup"><span data-stu-id="bfbe3-166">Turns center clipping on (1) or off (0).</span></span> <span data-ttu-id="bfbe3-167">El modo de característica debe estar activado para especificar esto.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-167">Feature mode must be on for specifying this.</span></span>                                       |
| <span data-ttu-id="bfbe3-168">-spkdev</span><span class="sxs-lookup"><span data-stu-id="bfbe3-168">-spkdev</span></span>   | <span data-ttu-id="bfbe3-169">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-169">Optional.</span></span> <span data-ttu-id="bfbe3-170">Especifica el índice de dispositivo de altavoz.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-170">Specifies speaker device index.</span></span> <span data-ttu-id="bfbe3-171">Si no se especifica, se le pedirá al usuario que seleccione.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-171">If not specified, the user will be asked to select.</span></span>                                         |
| <span data-ttu-id="bfbe3-172">-micdev</span><span class="sxs-lookup"><span data-stu-id="bfbe3-172">-micdev</span></span>   | <span data-ttu-id="bfbe3-173">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-173">Optional.</span></span> <span data-ttu-id="bfbe3-174">Especifica el índice del dispositivo de micrófono.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-174">Specifies microphone device index.</span></span> <span data-ttu-id="bfbe3-175">Si no se especifica, se le pedirá al usuario que seleccione.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-175">If not specified, the user will be asked to select.</span></span>                                      |
| <span data-ttu-id="bfbe3-176">-duración</span><span class="sxs-lookup"><span data-stu-id="bfbe3-176">-duration</span></span> | <span data-ttu-id="bfbe3-177">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-177">Optional.</span></span> <span data-ttu-id="bfbe3-178">Especifica cuánto tiempo se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-178">Specifies how long the application runs.</span></span>                                                                                    |



 

<span data-ttu-id="bfbe3-179">Esta aplicación de ejemplo no reproduce señales.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-179">This sample application does not play any signals.</span></span> <span data-ttu-id="bfbe3-180">Para ejecutar la demostración correctamente para los modos habilitados para AEC (modo 0 y 4), los usuarios deben reproducir algunas señales de audio a través del mismo dispositivo de altavoz especificado para DMO (es decir, el dispositivo especificado por la opción "-spkdev"), que simula la voz de un extremo en un escenario de charla bidireccional.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-180">To run the demo properly for AEC enabled modes (mode 0 and 4), users must play some audio signals through the same speaker device specified for the DMO (that is, the device specified by the "-spkdev" option), which simulates the far-end voice in a two-way chatting scenario.</span></span> <span data-ttu-id="bfbe3-181">Los usuarios pueden usar cualquier reproductor para reproducir señales de audio.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-181">Users can use any player to play any audio signals.</span></span> <span data-ttu-id="bfbe3-182">Si no hay ningún flujo de representación activo en el dispositivo de altavoz seleccionado, el DMO no se procesará.</span><span class="sxs-lookup"><span data-stu-id="bfbe3-182">If there is no active render stream on the selected speaker device, the DMO will fail to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfbe3-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bfbe3-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfbe3-184">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="bfbe3-184">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



