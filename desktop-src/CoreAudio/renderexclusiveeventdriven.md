---
description: Esta aplicación de ejemplo, que muestra el almacenamiento en búfer controlado por eventos, usa core Audio API para representar datos de audio en un dispositivo de salida especificado por el usuario.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75553496219d0a4ddaf6685089de802e034f94cb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405138"
---
# <a name="renderexclusiveeventdriven"></a><span data-ttu-id="884ed-103">RenderExclusiveEventDriven</span><span class="sxs-lookup"><span data-stu-id="884ed-103">RenderExclusiveEventDriven</span></span>

<span data-ttu-id="884ed-104">Esta aplicación de ejemplo usa core Audio API para representar datos de audio en un dispositivo de salida especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="884ed-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="884ed-105">En este ejemplo se muestra el almacenamiento en búfer controlado por eventos para un cliente de representación en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="884ed-105">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="884ed-106">Para una secuencia en modo exclusivo, el cliente comparte el búfer del punto de conexión con el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="884ed-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="884ed-107">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="884ed-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="884ed-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="884ed-108">Description</span></span>](#description)
-   [<span data-ttu-id="884ed-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="884ed-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="884ed-110">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="884ed-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="884ed-111">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="884ed-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="884ed-112">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="884ed-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="884ed-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="884ed-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="884ed-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="884ed-114">Description</span></span>

<span data-ttu-id="884ed-115">En este ejemplo se muestran las siguientes características.</span><span class="sxs-lookup"><span data-stu-id="884ed-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="884ed-116">[MMDevice API para](mmdevice-api.md) la enumeración y selección de dispositivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="884ed-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="884ed-117">WASAPI para operaciones de administración de flujos.</span><span class="sxs-lookup"><span data-stu-id="884ed-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="884ed-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="884ed-118">Requirements</span></span>



| <span data-ttu-id="884ed-119">Producto</span><span class="sxs-lookup"><span data-stu-id="884ed-119">Product</span></span>                                                        | <span data-ttu-id="884ed-120">Versión</span><span class="sxs-lookup"><span data-stu-id="884ed-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="884ed-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="884ed-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="884ed-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="884ed-122">Windows 7</span></span> |
| <span data-ttu-id="884ed-123">Programa para la mejora</span><span class="sxs-lookup"><span data-stu-id="884ed-123">Visual Studio</span></span>                                                  | <span data-ttu-id="884ed-124">2008</span><span class="sxs-lookup"><span data-stu-id="884ed-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="884ed-125">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="884ed-125">Downloading the Sample</span></span>

<span data-ttu-id="884ed-126">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="884ed-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="884ed-127">Location</span><span class="sxs-lookup"><span data-stu-id="884ed-127">Location</span></span>    | <span data-ttu-id="884ed-128">Ruta de acceso o dirección URL</span><span class="sxs-lookup"><span data-stu-id="884ed-128">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="884ed-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="884ed-129">Windows SDK</span></span> | <span data-ttu-id="884ed-130">\\Archivos de \\ programa Microsoft SDK de Windows \\ \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ RenderExclusiveEventDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="884ed-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="884ed-131">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="884ed-131">Building the Sample</span></span>

<span data-ttu-id="884ed-132">Para compilar el ejemplo RenderExclusiveEventDriven, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="884ed-132">To build the RenderExclusiveEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="884ed-133">Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo RenderExclusiveEventDriven.</span><span class="sxs-lookup"><span data-stu-id="884ed-133">Open the CMD shell for the Windows SDK and change to the RenderExclusiveEventDriven sample directory.</span></span>
2.  <span data-ttu-id="884ed-134">Ejecute el comando en el directorio RenderExclusiveEventDriven para abrir el proyecto `start WASAPIRenderExclusiveEventDriven.sln` WASAPIRenderExclusiveEventDriven en la Visual Studio cliente.</span><span class="sxs-lookup"><span data-stu-id="884ed-134">Run the command `start WASAPIRenderExclusiveEventDriven.sln` in the RenderExclusiveEventDriven directory to open the WASAPIRenderExclusiveEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="884ed-135">En la ventana, seleccione  la **configuración** de  la solución Depurar o Liberar, seleccione el menú Compilar en la barra de menús y seleccione la **opción Compilar.**</span><span class="sxs-lookup"><span data-stu-id="884ed-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="884ed-136">Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio tendrá acceso al entorno de compilación del SDK.</span><span class="sxs-lookup"><span data-stu-id="884ed-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="884ed-137">En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, WASAPIRenderExclusiveEventDriven.vcproj.</span><span class="sxs-lookup"><span data-stu-id="884ed-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="884ed-138">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="884ed-138">Running the Sample</span></span>

<span data-ttu-id="884ed-139">Si compila correctamente la aplicación de demostración, se genera WASAPIRenderExclusiveEventDriven.exe archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="884ed-139">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveEventDriven.exe, is generated.</span></span> <span data-ttu-id="884ed-140">Para ejecutarlo, escriba `WASAPIRenderExclusiveEventDriven` una ventana de comandos seguida de argumentos obligatorios u opcionales.</span><span class="sxs-lookup"><span data-stu-id="884ed-140">To run it, type `WASAPIRenderExclusiveEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="884ed-141">En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de reproducción en el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="884ed-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="884ed-142">En la tabla siguiente se muestran los argumentos.</span><span class="sxs-lookup"><span data-stu-id="884ed-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="884ed-143">Argumento</span><span class="sxs-lookup"><span data-stu-id="884ed-143">Argument</span></span>        | <span data-ttu-id="884ed-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="884ed-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="884ed-145">-?</span><span class="sxs-lookup"><span data-stu-id="884ed-145">-?</span></span>              | <span data-ttu-id="884ed-146">Muestra ayuda.</span><span class="sxs-lookup"><span data-stu-id="884ed-146">Shows help.</span></span>                                                |
| <span data-ttu-id="884ed-147">-H</span><span class="sxs-lookup"><span data-stu-id="884ed-147">-h</span></span>              | <span data-ttu-id="884ed-148">Muestra ayuda.</span><span class="sxs-lookup"><span data-stu-id="884ed-148">Shows help.</span></span>                                                |
| <span data-ttu-id="884ed-149">-f</span><span class="sxs-lookup"><span data-stu-id="884ed-149">-f</span></span>              | <span data-ttu-id="884ed-150">Frecuencia de onda sinusoidal en Hz.</span><span class="sxs-lookup"><span data-stu-id="884ed-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="884ed-151">-l</span><span class="sxs-lookup"><span data-stu-id="884ed-151">-l</span></span>              | <span data-ttu-id="884ed-152">Latencia de representación de audio en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="884ed-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="884ed-153">-d</span><span class="sxs-lookup"><span data-stu-id="884ed-153">-d</span></span>              | <span data-ttu-id="884ed-154">Duración de la onda sinusoidal en segundos.</span><span class="sxs-lookup"><span data-stu-id="884ed-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="884ed-155">-M</span><span class="sxs-lookup"><span data-stu-id="884ed-155">-m</span></span>              | <span data-ttu-id="884ed-156">Deshabilita el uso de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="884ed-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="884ed-157">-console</span><span class="sxs-lookup"><span data-stu-id="884ed-157">-console</span></span>        | <span data-ttu-id="884ed-158">Use el dispositivo de consola predeterminado.</span><span class="sxs-lookup"><span data-stu-id="884ed-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="884ed-159">-communications</span><span class="sxs-lookup"><span data-stu-id="884ed-159">-communications</span></span> | <span data-ttu-id="884ed-160">Use el dispositivo de comunicación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="884ed-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="884ed-161">-multimedia</span><span class="sxs-lookup"><span data-stu-id="884ed-161">-multimedia</span></span>     | <span data-ttu-id="884ed-162">Use el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="884ed-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="884ed-163">-endpoint</span><span class="sxs-lookup"><span data-stu-id="884ed-163">-endpoint</span></span>       | <span data-ttu-id="884ed-164">Use el identificador de punto de conexión especificado en el valor del modificador.</span><span class="sxs-lookup"><span data-stu-id="884ed-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="884ed-165">Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo para la sesión de representación.</span><span class="sxs-lookup"><span data-stu-id="884ed-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="884ed-166">Después de que el usuario especifica un dispositivo, la aplicación representa una onda sinusoidal a 440 Hz durante 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="884ed-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="884ed-167">Estos valores se pueden modificar especificando los valores de modificador -f y -d.</span><span class="sxs-lookup"><span data-stu-id="884ed-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="884ed-168">El ejemplo RenderExclusiveEventDriven muestra el almacenamiento en búfer controlado por eventos.</span><span class="sxs-lookup"><span data-stu-id="884ed-168">The RenderExclusiveEventDriven sample demonstrates event-driven buffering.</span></span> <span data-ttu-id="884ed-169">En el ejemplo se muestra cómo:</span><span class="sxs-lookup"><span data-stu-id="884ed-169">The sample shows how to:</span></span>

-   <span data-ttu-id="884ed-170">Cree una instancia de un cliente de audio, configúrelo para que se ejecute en modo exclusivo y habilite el almacenamiento en búfer controlado por eventos estableciendo la marca **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** en la llamada a [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="884ed-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="884ed-171">Asocie el cliente con los ejemplos que están listos para representarse proporcionando un identificador de eventos al sistema mediante una llamada al [**método IAudioClient::SetEventHandle.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)</span><span class="sxs-lookup"><span data-stu-id="884ed-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="884ed-172">Cree un subproceso de representación para procesar ejemplos desde el motor de audio.</span><span class="sxs-lookup"><span data-stu-id="884ed-172">Create a render thread to process samples from the audio engine.</span></span>
-   <span data-ttu-id="884ed-173">Alinee los búferes correctamente en un límite de 128 bytes antes de enviarlos al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="884ed-173">Align the buffers properly on a 128-byte boundary before sending them to the device.</span></span> <span data-ttu-id="884ed-174">Esto se realiza ajustando la periodicidad del motor.</span><span class="sxs-lookup"><span data-stu-id="884ed-174">This is done by adjusting the periodicity of the engine.</span></span>
-   <span data-ttu-id="884ed-175">Compruebe el formato de combinación del punto de conexión del dispositivo para determinar si se pueden representar las muestras.</span><span class="sxs-lookup"><span data-stu-id="884ed-175">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="884ed-176">Si el dispositivo no admite el formato de combinación, los datos se convierten a PCM.</span><span class="sxs-lookup"><span data-stu-id="884ed-176">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="884ed-177">Controlar la conmutación de secuencias.</span><span class="sxs-lookup"><span data-stu-id="884ed-177">Handle stream switching.</span></span>

<span data-ttu-id="884ed-178">Una vez que comienza la sesión de representación y se inicia la secuencia, el motor de audio señala el identificador de eventos proporcionado para notificar al cliente cada vez que un búfer está listo para que el cliente lo procese.</span><span class="sxs-lookup"><span data-stu-id="884ed-178">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="884ed-179">Los datos de audio también se pueden procesar en un bucle controlado por temporizador.</span><span class="sxs-lookup"><span data-stu-id="884ed-179">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="884ed-180">Este modo se muestra en el [ejemplo RenderExclusiveTimerDriven.](renderexclusivetimerdriven.md)</span><span class="sxs-lookup"><span data-stu-id="884ed-180">This mode is demonstrated in the [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) sample.</span></span>

<span data-ttu-id="884ed-181">Para obtener más información sobre cómo representar una secuencia, vea [Representación de una secuencia.](rendering-a-stream.md)</span><span class="sxs-lookup"><span data-stu-id="884ed-181">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="884ed-182">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="884ed-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="884ed-183">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="884ed-183">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



