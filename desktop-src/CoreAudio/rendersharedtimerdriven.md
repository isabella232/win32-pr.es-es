---
description: Esta aplicación de ejemplo utiliza las API de audio principales para representar datos de audio en un dispositivo de salida especificado por el usuario.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: RenderSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de4ce441a12d65b8bebb843c7b9a168443b34592
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807555"
---
# <a name="rendersharedtimerdriven"></a><span data-ttu-id="555a6-103">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="555a6-103">RenderSharedTimerDriven</span></span>

<span data-ttu-id="555a6-104">Esta aplicación de ejemplo utiliza las API de audio principales para representar datos de audio en un dispositivo de salida especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="555a6-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="555a6-105">Este ejemplo muestra el almacenamiento en búfer basado en temporizador para un cliente de representación en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="555a6-105">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="555a6-106">En el caso de una secuencia en modo compartido, el cliente comparte el búfer del extremo con el motor de audio.</span><span class="sxs-lookup"><span data-stu-id="555a6-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="555a6-107">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="555a6-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="555a6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="555a6-108">Description</span></span>](#description)
-   [<span data-ttu-id="555a6-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="555a6-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="555a6-110">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="555a6-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="555a6-111">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="555a6-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="555a6-112">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="555a6-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="555a6-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="555a6-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="555a6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="555a6-114">Description</span></span>

<span data-ttu-id="555a6-115">En este ejemplo se muestran las características siguientes.</span><span class="sxs-lookup"><span data-stu-id="555a6-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="555a6-116">[MMDEVICE API](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="555a6-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="555a6-117">WASAPI para las operaciones de administración de secuencias.</span><span class="sxs-lookup"><span data-stu-id="555a6-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="555a6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="555a6-118">Requirements</span></span>



| <span data-ttu-id="555a6-119">Producto</span><span class="sxs-lookup"><span data-stu-id="555a6-119">Product</span></span>                                                        | <span data-ttu-id="555a6-120">Versión</span><span class="sxs-lookup"><span data-stu-id="555a6-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="555a6-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="555a6-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="555a6-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="555a6-122">Windows 7</span></span> |
| <span data-ttu-id="555a6-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="555a6-123">Visual Studio</span></span>                                                  | <span data-ttu-id="555a6-124">2008</span><span class="sxs-lookup"><span data-stu-id="555a6-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="555a6-125">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="555a6-125">Downloading the Sample</span></span>

<span data-ttu-id="555a6-126">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="555a6-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="555a6-127">Location</span><span class="sxs-lookup"><span data-stu-id="555a6-127">Location</span></span>    | <span data-ttu-id="555a6-128">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="555a6-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="555a6-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="555a6-129">Windows SDK</span></span> | <span data-ttu-id="555a6-130">\\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ RenderSharedTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="555a6-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="555a6-131">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="555a6-131">Building the Sample</span></span>

<span data-ttu-id="555a6-132">Para compilar el ejemplo RenderSharedTimerDriven, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="555a6-132">To build the RenderSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="555a6-133">Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo RenderSharedTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="555a6-133">Open the CMD shell for the Windows SDK and change to the RenderSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="555a6-134">Ejecute el comando `start WASAPIRenderSharedTimerDriven.sln` en el directorio RenderSharedTimerDriven para abrir el proyecto WASAPIRenderSharedTimerDriven en la ventana de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="555a6-134">Run the command `start WASAPIRenderSharedTimerDriven.sln` in the RenderSharedTimerDriven directory to open the WASAPIRenderSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="555a6-135">En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** .</span><span class="sxs-lookup"><span data-stu-id="555a6-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="555a6-136">Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK.</span><span class="sxs-lookup"><span data-stu-id="555a6-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="555a6-137">En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, WASAPIRenderSharedTimerDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="555a6-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="555a6-138">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="555a6-138">Running the Sample</span></span>

<span data-ttu-id="555a6-139">Si compila la aplicación de demostración correctamente, se genera un archivo ejecutable WASAPIRenderSharedTimerDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="555a6-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="555a6-140">Para ejecutarlo, escriba `WASAPIRenderSharedTimerDriven` en una ventana de comandos seguida de los argumentos obligatorios u opcionales.</span><span class="sxs-lookup"><span data-stu-id="555a6-140">To run it, type `WASAPIRenderSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="555a6-141">En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de la reproducción en el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="555a6-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="555a6-142">En la tabla siguiente se muestran los argumentos.</span><span class="sxs-lookup"><span data-stu-id="555a6-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="555a6-143">Argumento</span><span class="sxs-lookup"><span data-stu-id="555a6-143">Argument</span></span>        | <span data-ttu-id="555a6-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="555a6-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="555a6-145">-?</span><span class="sxs-lookup"><span data-stu-id="555a6-145">-?</span></span>              | <span data-ttu-id="555a6-146">Muestra la ayuda.</span><span class="sxs-lookup"><span data-stu-id="555a6-146">Shows help.</span></span>                                                |
| <span data-ttu-id="555a6-147">-H</span><span class="sxs-lookup"><span data-stu-id="555a6-147">-h</span></span>              | <span data-ttu-id="555a6-148">Muestra la ayuda.</span><span class="sxs-lookup"><span data-stu-id="555a6-148">Shows help.</span></span>                                                |
| <span data-ttu-id="555a6-149">-f</span><span class="sxs-lookup"><span data-stu-id="555a6-149">-f</span></span>              | <span data-ttu-id="555a6-150">Frecuencia de onda sinusoidal en Hz.</span><span class="sxs-lookup"><span data-stu-id="555a6-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="555a6-151">-l</span><span class="sxs-lookup"><span data-stu-id="555a6-151">-l</span></span>              | <span data-ttu-id="555a6-152">Latencia de representación de audio en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="555a6-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="555a6-153">-d</span><span class="sxs-lookup"><span data-stu-id="555a6-153">-d</span></span>              | <span data-ttu-id="555a6-154">Duración de onda sinusoidal en segundos.</span><span class="sxs-lookup"><span data-stu-id="555a6-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="555a6-155">-M</span><span class="sxs-lookup"><span data-stu-id="555a6-155">-m</span></span>              | <span data-ttu-id="555a6-156">Deshabilita el uso de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="555a6-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="555a6-157">-consola</span><span class="sxs-lookup"><span data-stu-id="555a6-157">-console</span></span>        | <span data-ttu-id="555a6-158">Use el dispositivo de consola predeterminado.</span><span class="sxs-lookup"><span data-stu-id="555a6-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="555a6-159">-comunicaciones</span><span class="sxs-lookup"><span data-stu-id="555a6-159">-communications</span></span> | <span data-ttu-id="555a6-160">Use el dispositivo de comunicación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="555a6-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="555a6-161">-multimedia</span><span class="sxs-lookup"><span data-stu-id="555a6-161">-multimedia</span></span>     | <span data-ttu-id="555a6-162">Use el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="555a6-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="555a6-163">-punto de conexión</span><span class="sxs-lookup"><span data-stu-id="555a6-163">-endpoint</span></span>       | <span data-ttu-id="555a6-164">Use el identificador de extremo especificado en el valor del modificador.</span><span class="sxs-lookup"><span data-stu-id="555a6-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="555a6-165">Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo para la sesión de representación.</span><span class="sxs-lookup"><span data-stu-id="555a6-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="555a6-166">Una vez que el usuario especifica un dispositivo, la aplicación representa una onda sinusoidal en 440 Hz durante 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="555a6-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="555a6-167">Estos valores se pueden modificar especificando los valores de modificador-f y-d.</span><span class="sxs-lookup"><span data-stu-id="555a6-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="555a6-168">RenderSharedTimerDriven muestra el almacenamiento en búfer basado en temporizador.</span><span class="sxs-lookup"><span data-stu-id="555a6-168">RenderSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="555a6-169">En este modo, el cliente debe esperar durante un período de tiempo (la mitad de la latencia, especificada por el valor del modificador-d, en milisegundos).</span><span class="sxs-lookup"><span data-stu-id="555a6-169">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="555a6-170">Cuando el cliente se reactiva, a mitad del período de procesamiento, extrae el siguiente conjunto de ejemplos del motor.</span><span class="sxs-lookup"><span data-stu-id="555a6-170">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="555a6-171">Antes de cada paso de procesamiento en el bucle de almacenamiento en búfer, el cliente debe averiguar la cantidad de datos que se van a representar para que los datos no desbordan el búfer.</span><span class="sxs-lookup"><span data-stu-id="555a6-171">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="555a6-172">Los datos de audio que se van a reproducir en el dispositivo especificado se pueden procesar habilitando el almacenamiento en búfer basado en eventos.</span><span class="sxs-lookup"><span data-stu-id="555a6-172">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="555a6-173">Este modo se muestra en el ejemplo [RenderSharedEventDriven](rendersharedeventdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="555a6-173">This mode is demonstrated in the [RenderSharedEventDriven](rendersharedeventdriven.md) sample.</span></span>

<span data-ttu-id="555a6-174">Para obtener más información sobre la representación de una secuencia, vea [representar un flujo](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="555a6-174">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="555a6-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="555a6-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="555a6-176">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="555a6-176">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



