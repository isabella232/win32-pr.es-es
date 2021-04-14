---
description: Esta aplicación de ejemplo utiliza las API de audio principales para representar datos de audio en un dispositivo de salida especificado por el usuario. Este ejemplo muestra el almacenamiento en búfer basado en temporizador para un cliente de representación en modo exclusivo.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6145f65de3de9425f7ba2f023a669ec0b57a3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496366"
---
# <a name="renderexclusivetimerdriven"></a><span data-ttu-id="8a765-104">RenderExclusiveTimerDriven</span><span class="sxs-lookup"><span data-stu-id="8a765-104">RenderExclusiveTimerDriven</span></span>

<span data-ttu-id="8a765-105">Esta aplicación de ejemplo utiliza las API de audio principales para representar datos de audio en un dispositivo de salida especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8a765-105">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="8a765-106">Este ejemplo muestra el almacenamiento en búfer basado en temporizador para un cliente de representación en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="8a765-106">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="8a765-107">En el caso de una secuencia en modo exclusivo, el cliente comparte el búfer del extremo con el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="8a765-107">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="8a765-108">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="8a765-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8a765-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a765-109">Description</span></span>](#description)
-   [<span data-ttu-id="8a765-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a765-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="8a765-111">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a765-111">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="8a765-112">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a765-112">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="8a765-113">Ver los archivos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a765-113">View the Sample Files</span></span>](#view-the-sample-files)
-   [<span data-ttu-id="8a765-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a765-114">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="8a765-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a765-115">Description</span></span>

<span data-ttu-id="8a765-116">En este ejemplo se muestran las características siguientes.</span><span class="sxs-lookup"><span data-stu-id="8a765-116">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="8a765-117">[MMDEVICE API](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="8a765-117">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="8a765-118">WASAPI para las operaciones de administración de secuencias.</span><span class="sxs-lookup"><span data-stu-id="8a765-118">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a765-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a765-119">Requirements</span></span>



| <span data-ttu-id="8a765-120">Producto</span><span class="sxs-lookup"><span data-stu-id="8a765-120">Product</span></span>                                                        | <span data-ttu-id="8a765-121">Versión</span><span class="sxs-lookup"><span data-stu-id="8a765-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="8a765-122">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="8a765-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="8a765-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a765-123">Windows 7</span></span> |
| <span data-ttu-id="8a765-124">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8a765-124">Visual Studio</span></span>                                                  | <span data-ttu-id="8a765-125">2008</span><span class="sxs-lookup"><span data-stu-id="8a765-125">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="8a765-126">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a765-126">Downloading the Sample</span></span>

<span data-ttu-id="8a765-127">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="8a765-127">This sample is available in the following locations.</span></span>



| <span data-ttu-id="8a765-128">Location</span><span class="sxs-lookup"><span data-stu-id="8a765-128">Location</span></span>    | <span data-ttu-id="8a765-129">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="8a765-129">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a765-130">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="8a765-130">Windows SDK</span></span> | <span data-ttu-id="8a765-131">\\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ RenderExclusiveTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="8a765-131">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="8a765-132">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a765-132">Building the Sample</span></span>

<span data-ttu-id="8a765-133">Para compilar el ejemplo RenderExclusiveTimerDriven, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="8a765-133">To build the RenderExclusiveTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="8a765-134">Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo RenderExclusiveTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="8a765-134">Open the CMD shell for the Windows SDK and change to the RenderExclusiveTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="8a765-135">Ejecute el comando `start WASAPIRenderExclusiveTimerDriven.sln` en el directorio RenderExclusiveTimerDriven para abrir el proyecto WASAPIRenderExclusiveTimerDriven en la ventana de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8a765-135">Run the command `start WASAPIRenderExclusiveTimerDriven.sln` in the RenderExclusiveTimerDriven directory to open the WASAPIRenderExclusiveTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="8a765-136">En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** .</span><span class="sxs-lookup"><span data-stu-id="8a765-136">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="8a765-137">Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK.</span><span class="sxs-lookup"><span data-stu-id="8a765-137">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="8a765-138">En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, WASAPIRenderExclusiveTimerDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="8a765-138">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveTimerDriven.vcproj.</span></span>

## <a name="view-the-sample-files"></a><span data-ttu-id="8a765-139">Ver los archivos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a765-139">View the Sample Files</span></span>

<span data-ttu-id="8a765-140">Si compila la aplicación de demostración correctamente, se genera un archivo ejecutable WASAPIRenderExclusiveTimerDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="8a765-140">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveTimerDriven.exe, is generated.</span></span> <span data-ttu-id="8a765-141">Para ejecutarlo, escriba `WASAPIRenderExclusiveTimerDriven` en una ventana de comandos seguida de los argumentos obligatorios u opcionales.</span><span class="sxs-lookup"><span data-stu-id="8a765-141">To run it, type `WASAPIRenderExclusiveTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="8a765-142">En el ejemplo siguiente se muestra cómo ejecutar el ejemplo mediante un que especifica la duración de la reproducción en el dispositivo de consola predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8a765-142">The following example shows how to run the sample by a specifying playback duration on the default console device.</span></span>

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

<span data-ttu-id="8a765-143">En la tabla siguiente se muestran los argumentos.</span><span class="sxs-lookup"><span data-stu-id="8a765-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="8a765-144">Argumento</span><span class="sxs-lookup"><span data-stu-id="8a765-144">Argument</span></span>        | <span data-ttu-id="8a765-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a765-145">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="8a765-146">-?</span><span class="sxs-lookup"><span data-stu-id="8a765-146">-?</span></span>              | <span data-ttu-id="8a765-147">Muestra la ayuda.</span><span class="sxs-lookup"><span data-stu-id="8a765-147">Shows help.</span></span>                                                |
| <span data-ttu-id="8a765-148">-H</span><span class="sxs-lookup"><span data-stu-id="8a765-148">-h</span></span>              | <span data-ttu-id="8a765-149">Muestra la ayuda.</span><span class="sxs-lookup"><span data-stu-id="8a765-149">Shows help.</span></span>                                                |
| <span data-ttu-id="8a765-150">-f</span><span class="sxs-lookup"><span data-stu-id="8a765-150">-f</span></span>              | <span data-ttu-id="8a765-151">Frecuencia de onda sinusoidal en Hz.</span><span class="sxs-lookup"><span data-stu-id="8a765-151">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="8a765-152">-l</span><span class="sxs-lookup"><span data-stu-id="8a765-152">-l</span></span>              | <span data-ttu-id="8a765-153">Latencia de representación de audio en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="8a765-153">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="8a765-154">-d</span><span class="sxs-lookup"><span data-stu-id="8a765-154">-d</span></span>              | <span data-ttu-id="8a765-155">Duración de onda sinusoidal en segundos.</span><span class="sxs-lookup"><span data-stu-id="8a765-155">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="8a765-156">-M</span><span class="sxs-lookup"><span data-stu-id="8a765-156">-m</span></span>              | <span data-ttu-id="8a765-157">Deshabilita el uso de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="8a765-157">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="8a765-158">-consola</span><span class="sxs-lookup"><span data-stu-id="8a765-158">-console</span></span>        | <span data-ttu-id="8a765-159">Use el dispositivo de consola predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8a765-159">Use the default console device.</span></span>                            |
| <span data-ttu-id="8a765-160">-comunicaciones</span><span class="sxs-lookup"><span data-stu-id="8a765-160">-communications</span></span> | <span data-ttu-id="8a765-161">Use el dispositivo de comunicación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8a765-161">Use the default communication device.</span></span>                      |
| <span data-ttu-id="8a765-162">-multimedia</span><span class="sxs-lookup"><span data-stu-id="8a765-162">-multimedia</span></span>     | <span data-ttu-id="8a765-163">Use el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8a765-163">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="8a765-164">-punto de conexión</span><span class="sxs-lookup"><span data-stu-id="8a765-164">-endpoint</span></span>       | <span data-ttu-id="8a765-165">Use el identificador de extremo especificado en el valor del modificador.</span><span class="sxs-lookup"><span data-stu-id="8a765-165">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="8a765-166">Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo para la sesión de representación.</span><span class="sxs-lookup"><span data-stu-id="8a765-166">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="8a765-167">Una vez que el usuario especifica un dispositivo, la aplicación representa una onda sinusoidal en 440 Hz durante 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="8a765-167">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="8a765-168">Estos valores se pueden modificar especificando los valores de modificador-f y-d.</span><span class="sxs-lookup"><span data-stu-id="8a765-168">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="8a765-169">RenderExclusiveTimerDriven muestra el almacenamiento en búfer basado en temporizador.</span><span class="sxs-lookup"><span data-stu-id="8a765-169">RenderExclusiveTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="8a765-170">En este modo, el cliente debe esperar durante un período de tiempo (la mitad de la latencia, especificada por el valor del modificador-d, en milisegundos).</span><span class="sxs-lookup"><span data-stu-id="8a765-170">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="8a765-171">Cuando el cliente se reactiva, a mitad del período de procesamiento, extrae el siguiente conjunto de ejemplos del motor.</span><span class="sxs-lookup"><span data-stu-id="8a765-171">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="8a765-172">Antes de cada paso de procesamiento en el bucle de almacenamiento en búfer, el cliente debe averiguar la cantidad de datos que se van a representar para que los datos no desbordan el búfer.</span><span class="sxs-lookup"><span data-stu-id="8a765-172">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="8a765-173">Los datos de audio que se van a reproducir en el dispositivo especificado se pueden procesar habilitando el almacenamiento en búfer basado en eventos.</span><span class="sxs-lookup"><span data-stu-id="8a765-173">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="8a765-174">Este modo se muestra en el ejemplo RenderExclusiveTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="8a765-174">This mode is demonstrated in the RenderExclusiveTimerDriven sample.</span></span>

<span data-ttu-id="8a765-175">Para obtener más información sobre la representación de una secuencia, vea [representar un flujo](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="8a765-175">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a765-176">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a765-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a765-177">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="8a765-177">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



