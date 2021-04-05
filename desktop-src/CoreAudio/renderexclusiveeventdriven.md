---
description: Esta aplicación de ejemplo utiliza las API de audio principales para representar datos de audio en un dispositivo de salida especificado por el usuario.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b94fa423cd4d4e7dc7121e927696529bfadf9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080218"
---
# <a name="renderexclusiveeventdriven"></a><span data-ttu-id="b89b9-103">RenderExclusiveEventDriven</span><span class="sxs-lookup"><span data-stu-id="b89b9-103">RenderExclusiveEventDriven</span></span>

<span data-ttu-id="b89b9-104">Esta aplicación de ejemplo utiliza las API de audio principales para representar datos de audio en un dispositivo de salida especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b89b9-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="b89b9-105">Este ejemplo muestra el almacenamiento en búfer basado en eventos para un cliente de representación en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="b89b9-105">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="b89b9-106">En el caso de una secuencia en modo exclusivo, el cliente comparte el búfer del extremo con el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="b89b9-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="b89b9-107">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="b89b9-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b89b9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b89b9-108">Description</span></span>](#description)
-   [<span data-ttu-id="b89b9-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b89b9-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b89b9-110">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b89b9-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b89b9-111">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b89b9-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b89b9-112">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b89b9-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="b89b9-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b89b9-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="b89b9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b89b9-114">Description</span></span>

<span data-ttu-id="b89b9-115">En este ejemplo se muestran las características siguientes.</span><span class="sxs-lookup"><span data-stu-id="b89b9-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="b89b9-116">[MMDEVICE API](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="b89b9-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="b89b9-117">WASAPI para las operaciones de administración de secuencias.</span><span class="sxs-lookup"><span data-stu-id="b89b9-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="b89b9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b89b9-118">Requirements</span></span>



| <span data-ttu-id="b89b9-119">Producto</span><span class="sxs-lookup"><span data-stu-id="b89b9-119">Product</span></span>                                                        | <span data-ttu-id="b89b9-120">Versión</span><span class="sxs-lookup"><span data-stu-id="b89b9-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="b89b9-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="b89b9-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="b89b9-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b89b9-122">Windows 7</span></span> |
| <span data-ttu-id="b89b9-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b89b9-123">Visual Studio</span></span>                                                  | <span data-ttu-id="b89b9-124">2008</span><span class="sxs-lookup"><span data-stu-id="b89b9-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b89b9-125">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b89b9-125">Downloading the Sample</span></span>

<span data-ttu-id="b89b9-126">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="b89b9-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="b89b9-127">Location</span><span class="sxs-lookup"><span data-stu-id="b89b9-127">Location</span></span>    | <span data-ttu-id="b89b9-128">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="b89b9-128">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b89b9-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="b89b9-129">Windows SDK</span></span> | <span data-ttu-id="b89b9-130">\\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ RenderExclusiveEventDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="b89b9-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="b89b9-131">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b89b9-131">Building the Sample</span></span>

<span data-ttu-id="b89b9-132">Para compilar el ejemplo RenderExclusiveEventDriven, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="b89b9-132">To build the RenderExclusiveEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="b89b9-133">Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo RenderExclusiveEventDriven.</span><span class="sxs-lookup"><span data-stu-id="b89b9-133">Open the CMD shell for the Windows SDK and change to the RenderExclusiveEventDriven sample directory.</span></span>
2.  <span data-ttu-id="b89b9-134">Ejecute el comando `start WASAPIRenderExclusiveEventDriven.sln` en el directorio RenderExclusiveEventDriven para abrir el proyecto WASAPIRenderExclusiveEventDriven en la ventana de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b89b9-134">Run the command `start WASAPIRenderExclusiveEventDriven.sln` in the RenderExclusiveEventDriven directory to open the WASAPIRenderExclusiveEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="b89b9-135">En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** .</span><span class="sxs-lookup"><span data-stu-id="b89b9-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="b89b9-136">Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK.</span><span class="sxs-lookup"><span data-stu-id="b89b9-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="b89b9-137">En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, WASAPIRenderExclusiveEventDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="b89b9-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b89b9-138">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b89b9-138">Running the Sample</span></span>

<span data-ttu-id="b89b9-139">Si compila la aplicación de demostración correctamente, se genera un archivo ejecutable WASAPIRenderExclusiveEventDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="b89b9-139">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveEventDriven.exe, is generated.</span></span> <span data-ttu-id="b89b9-140">Para ejecutarlo, escriba `WASAPIRenderExclusiveEventDriven` en una ventana de comandos seguida de los argumentos obligatorios u opcionales.</span><span class="sxs-lookup"><span data-stu-id="b89b9-140">To run it, type `WASAPIRenderExclusiveEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="b89b9-141">En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de la reproducción en el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b89b9-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="b89b9-142">En la tabla siguiente se muestran los argumentos.</span><span class="sxs-lookup"><span data-stu-id="b89b9-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="b89b9-143">Argumento</span><span class="sxs-lookup"><span data-stu-id="b89b9-143">Argument</span></span>        | <span data-ttu-id="b89b9-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="b89b9-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="b89b9-145">-?</span><span class="sxs-lookup"><span data-stu-id="b89b9-145">-?</span></span>              | <span data-ttu-id="b89b9-146">Muestra la ayuda.</span><span class="sxs-lookup"><span data-stu-id="b89b9-146">Shows help.</span></span>                                                |
| <span data-ttu-id="b89b9-147">-H</span><span class="sxs-lookup"><span data-stu-id="b89b9-147">-h</span></span>              | <span data-ttu-id="b89b9-148">Muestra la ayuda.</span><span class="sxs-lookup"><span data-stu-id="b89b9-148">Shows help.</span></span>                                                |
| <span data-ttu-id="b89b9-149">-f</span><span class="sxs-lookup"><span data-stu-id="b89b9-149">-f</span></span>              | <span data-ttu-id="b89b9-150">Frecuencia de onda sinusoidal en Hz.</span><span class="sxs-lookup"><span data-stu-id="b89b9-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="b89b9-151">-l</span><span class="sxs-lookup"><span data-stu-id="b89b9-151">-l</span></span>              | <span data-ttu-id="b89b9-152">Latencia de representación de audio en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="b89b9-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="b89b9-153">-d</span><span class="sxs-lookup"><span data-stu-id="b89b9-153">-d</span></span>              | <span data-ttu-id="b89b9-154">Duración de onda sinusoidal en segundos.</span><span class="sxs-lookup"><span data-stu-id="b89b9-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="b89b9-155">-M</span><span class="sxs-lookup"><span data-stu-id="b89b9-155">-m</span></span>              | <span data-ttu-id="b89b9-156">Deshabilita el uso de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="b89b9-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="b89b9-157">-consola</span><span class="sxs-lookup"><span data-stu-id="b89b9-157">-console</span></span>        | <span data-ttu-id="b89b9-158">Use el dispositivo de consola predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b89b9-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="b89b9-159">-comunicaciones</span><span class="sxs-lookup"><span data-stu-id="b89b9-159">-communications</span></span> | <span data-ttu-id="b89b9-160">Use el dispositivo de comunicación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b89b9-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="b89b9-161">-multimedia</span><span class="sxs-lookup"><span data-stu-id="b89b9-161">-multimedia</span></span>     | <span data-ttu-id="b89b9-162">Use el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b89b9-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="b89b9-163">-punto de conexión</span><span class="sxs-lookup"><span data-stu-id="b89b9-163">-endpoint</span></span>       | <span data-ttu-id="b89b9-164">Use el identificador de extremo especificado en el valor del modificador.</span><span class="sxs-lookup"><span data-stu-id="b89b9-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="b89b9-165">Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo para la sesión de representación.</span><span class="sxs-lookup"><span data-stu-id="b89b9-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="b89b9-166">Una vez que el usuario especifica un dispositivo, la aplicación representa una onda sinusoidal en 440 Hz durante 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="b89b9-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="b89b9-167">Estos valores se pueden modificar especificando los valores de modificador-f y-d.</span><span class="sxs-lookup"><span data-stu-id="b89b9-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="b89b9-168">En el ejemplo RenderExclusiveEventDriven se muestra el almacenamiento en búfer basado en eventos.</span><span class="sxs-lookup"><span data-stu-id="b89b9-168">The RenderExclusiveEventDriven sample demonstrates event-driven buffering.</span></span> <span data-ttu-id="b89b9-169">En el ejemplo se muestra cómo:</span><span class="sxs-lookup"><span data-stu-id="b89b9-169">The sample shows how to:</span></span>

-   <span data-ttu-id="b89b9-170">Cree una instancia de un cliente de audio, configúrela para que se ejecute en modo exclusivo y habilite el almacenamiento en búfer basado en eventos estableciendo la marca **\_ \_ EVENTCALLBACK STREAMFLAGS AUDCLNT** en la llamada a [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="b89b9-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="b89b9-171">Asocie el cliente a los ejemplos que estén listos para ser representados proporcionando un identificador de evento al sistema llamando al método [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .</span><span class="sxs-lookup"><span data-stu-id="b89b9-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="b89b9-172">Cree un subproceso de representación para procesar los ejemplos del motor de audio.</span><span class="sxs-lookup"><span data-stu-id="b89b9-172">Create a render thread to process samples from the audio engine.</span></span>
-   <span data-ttu-id="b89b9-173">Alinee los búferes correctamente en un límite de 128 bytes antes de enviarlos al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b89b9-173">Align the buffers properly on a 128-byte boundary before sending them to the device.</span></span> <span data-ttu-id="b89b9-174">Esto se realiza ajustando la periodicidad del motor.</span><span class="sxs-lookup"><span data-stu-id="b89b9-174">This is done by adjusting the periodicity of the engine.</span></span>
-   <span data-ttu-id="b89b9-175">Compruebe el formato de combinación del punto de conexión del dispositivo para determinar si se pueden representar los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="b89b9-175">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="b89b9-176">Si el dispositivo no admite el formato de combinación, los datos se convierten en PCM.</span><span class="sxs-lookup"><span data-stu-id="b89b9-176">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="b89b9-177">Controlar el cambio de flujo.</span><span class="sxs-lookup"><span data-stu-id="b89b9-177">Handle stream switching.</span></span>

<span data-ttu-id="b89b9-178">Una vez iniciada la sesión de representación y iniciada la secuencia, el motor de audio señala el identificador de eventos proporcionado para notificar al cliente cada vez que un búfer está listo para que lo procese el cliente.</span><span class="sxs-lookup"><span data-stu-id="b89b9-178">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="b89b9-179">Los datos de audio también se pueden procesar en un bucle controlado por temporizador.</span><span class="sxs-lookup"><span data-stu-id="b89b9-179">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="b89b9-180">Este modo se muestra en el ejemplo [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="b89b9-180">This mode is demonstrated in the [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) sample.</span></span>

<span data-ttu-id="b89b9-181">Para obtener más información sobre la representación de una secuencia, vea [representar un flujo](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="b89b9-181">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b89b9-182">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b89b9-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b89b9-183">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="b89b9-183">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



