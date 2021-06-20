---
description: Esta aplicación de ejemplo, que muestra el almacenamiento en búfer controlado por temporizador, usa core Audio API para representar datos de audio en un dispositivo de salida especificado por el usuario.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: RenderSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89d2814f359668f8724d3deb65a7c2a9eeff5b06
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410098"
---
# <a name="rendersharedtimerdriven"></a><span data-ttu-id="81488-103">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="81488-103">RenderSharedTimerDriven</span></span>

<span data-ttu-id="81488-104">Esta aplicación de ejemplo usa core Audio API para representar datos de audio en un dispositivo de salida especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="81488-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="81488-105">En este ejemplo se muestra el almacenamiento en búfer controlado por temporizador para un cliente de representación en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="81488-105">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="81488-106">Para una secuencia en modo compartido, el cliente comparte el búfer del punto de conexión con el motor de audio.</span><span class="sxs-lookup"><span data-stu-id="81488-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="81488-107">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="81488-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="81488-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="81488-108">Description</span></span>](#description)
-   [<span data-ttu-id="81488-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81488-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="81488-110">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="81488-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="81488-111">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="81488-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="81488-112">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="81488-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="81488-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81488-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="81488-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="81488-114">Description</span></span>

<span data-ttu-id="81488-115">En este ejemplo se muestran las siguientes características.</span><span class="sxs-lookup"><span data-stu-id="81488-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="81488-116">[MMDevice API para](mmdevice-api.md) la enumeración y selección de dispositivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="81488-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="81488-117">WASAPI para operaciones de administración de flujos.</span><span class="sxs-lookup"><span data-stu-id="81488-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="81488-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81488-118">Requirements</span></span>



| <span data-ttu-id="81488-119">Producto</span><span class="sxs-lookup"><span data-stu-id="81488-119">Product</span></span>                                                        | <span data-ttu-id="81488-120">Versión</span><span class="sxs-lookup"><span data-stu-id="81488-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="81488-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="81488-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="81488-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="81488-122">Windows 7</span></span> |
| <span data-ttu-id="81488-123">Programa para la mejora</span><span class="sxs-lookup"><span data-stu-id="81488-123">Visual Studio</span></span>                                                  | <span data-ttu-id="81488-124">2008</span><span class="sxs-lookup"><span data-stu-id="81488-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="81488-125">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="81488-125">Downloading the Sample</span></span>

<span data-ttu-id="81488-126">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="81488-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="81488-127">Location</span><span class="sxs-lookup"><span data-stu-id="81488-127">Location</span></span>    | <span data-ttu-id="81488-128">Ruta de acceso o dirección URL</span><span class="sxs-lookup"><span data-stu-id="81488-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81488-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="81488-129">Windows SDK</span></span> | <span data-ttu-id="81488-130">\\Archivos de \\ programa Microsoft SDK de Windows \\ \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ RenderSharedTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="81488-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="81488-131">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="81488-131">Building the Sample</span></span>

<span data-ttu-id="81488-132">Para compilar el ejemplo RenderSharedTimerDriven, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="81488-132">To build the RenderSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="81488-133">Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo RenderSharedTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="81488-133">Open the CMD shell for the Windows SDK and change to the RenderSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="81488-134">Ejecute el comando en el directorio RenderSharedTimerDriven para abrir el proyecto `start WASAPIRenderSharedTimerDriven.sln` WASAPIRenderSharedTimerDriven en la Visual Studio anterior.</span><span class="sxs-lookup"><span data-stu-id="81488-134">Run the command `start WASAPIRenderSharedTimerDriven.sln` in the RenderSharedTimerDriven directory to open the WASAPIRenderSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="81488-135">En la ventana, seleccione  la **configuración** de  la solución Depurar o Liberar, seleccione el menú Compilar en la barra de menús y seleccione la **opción Compilar.**</span><span class="sxs-lookup"><span data-stu-id="81488-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="81488-136">Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio tendrá acceso al entorno de compilación del SDK.</span><span class="sxs-lookup"><span data-stu-id="81488-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="81488-137">En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, WASAPIRenderSharedTimerDriven.vcproj.</span><span class="sxs-lookup"><span data-stu-id="81488-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="81488-138">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="81488-138">Running the Sample</span></span>

<span data-ttu-id="81488-139">Si compila correctamente la aplicación de demostración, se genera WASAPIRenderSharedTimerDriven.exe archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="81488-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="81488-140">Para ejecutarlo, escriba `WASAPIRenderSharedTimerDriven` una ventana de comandos seguida de argumentos obligatorios u opcionales.</span><span class="sxs-lookup"><span data-stu-id="81488-140">To run it, type `WASAPIRenderSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="81488-141">En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de reproducción en el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81488-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="81488-142">En la tabla siguiente se muestran los argumentos.</span><span class="sxs-lookup"><span data-stu-id="81488-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="81488-143">Argumento</span><span class="sxs-lookup"><span data-stu-id="81488-143">Argument</span></span>        | <span data-ttu-id="81488-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="81488-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="81488-145">-?</span><span class="sxs-lookup"><span data-stu-id="81488-145">-?</span></span>              | <span data-ttu-id="81488-146">Muestra ayuda.</span><span class="sxs-lookup"><span data-stu-id="81488-146">Shows help.</span></span>                                                |
| <span data-ttu-id="81488-147">-H</span><span class="sxs-lookup"><span data-stu-id="81488-147">-h</span></span>              | <span data-ttu-id="81488-148">Muestra ayuda.</span><span class="sxs-lookup"><span data-stu-id="81488-148">Shows help.</span></span>                                                |
| <span data-ttu-id="81488-149">-f</span><span class="sxs-lookup"><span data-stu-id="81488-149">-f</span></span>              | <span data-ttu-id="81488-150">Frecuencia de onda sinusoidal en Hz.</span><span class="sxs-lookup"><span data-stu-id="81488-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="81488-151">-l</span><span class="sxs-lookup"><span data-stu-id="81488-151">-l</span></span>              | <span data-ttu-id="81488-152">Latencia de representación de audio en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="81488-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="81488-153">-d</span><span class="sxs-lookup"><span data-stu-id="81488-153">-d</span></span>              | <span data-ttu-id="81488-154">Duración de la onda sinusoidal en segundos.</span><span class="sxs-lookup"><span data-stu-id="81488-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="81488-155">-M</span><span class="sxs-lookup"><span data-stu-id="81488-155">-m</span></span>              | <span data-ttu-id="81488-156">Deshabilita el uso de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="81488-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="81488-157">-console</span><span class="sxs-lookup"><span data-stu-id="81488-157">-console</span></span>        | <span data-ttu-id="81488-158">Use el dispositivo de consola predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81488-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="81488-159">-communications</span><span class="sxs-lookup"><span data-stu-id="81488-159">-communications</span></span> | <span data-ttu-id="81488-160">Use el dispositivo de comunicación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81488-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="81488-161">-multimedia</span><span class="sxs-lookup"><span data-stu-id="81488-161">-multimedia</span></span>     | <span data-ttu-id="81488-162">Use el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81488-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="81488-163">-endpoint</span><span class="sxs-lookup"><span data-stu-id="81488-163">-endpoint</span></span>       | <span data-ttu-id="81488-164">Use el identificador de punto de conexión especificado en el valor del modificador.</span><span class="sxs-lookup"><span data-stu-id="81488-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="81488-165">Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo para la sesión de representación.</span><span class="sxs-lookup"><span data-stu-id="81488-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="81488-166">Después de que el usuario especifica un dispositivo, la aplicación representa una onda sinusoidal a 440 Hz durante 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="81488-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="81488-167">Estos valores se pueden modificar especificando los valores de modificador -f y -d.</span><span class="sxs-lookup"><span data-stu-id="81488-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="81488-168">RenderSharedTimerDriven muestra el almacenamiento en búfer controlado por temporizador.</span><span class="sxs-lookup"><span data-stu-id="81488-168">RenderSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="81488-169">En este modo, el cliente debe esperar un período de tiempo (la mitad de la latencia, especificada por el valor del modificador -d, en milisegundos).</span><span class="sxs-lookup"><span data-stu-id="81488-169">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="81488-170">Cuando el cliente se reactiva, a mitad del período de procesamiento, extrae el siguiente conjunto de muestras del motor.</span><span class="sxs-lookup"><span data-stu-id="81488-170">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="81488-171">Antes de que cada procesamiento pase en el bucle de almacenamiento en búfer, el cliente debe averiguar la cantidad de datos que se representará para que los datos no sobresalan el búfer.</span><span class="sxs-lookup"><span data-stu-id="81488-171">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="81488-172">Los datos de audio que se reproducirán en el dispositivo especificado se pueden procesar habilitando el almacenamiento en búfer controlado por eventos.</span><span class="sxs-lookup"><span data-stu-id="81488-172">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="81488-173">Este modo se muestra en el [ejemplo RenderSharedEventDriven.](rendersharedeventdriven.md)</span><span class="sxs-lookup"><span data-stu-id="81488-173">This mode is demonstrated in the [RenderSharedEventDriven](rendersharedeventdriven.md) sample.</span></span>

<span data-ttu-id="81488-174">Para obtener más información sobre cómo representar una secuencia, vea [Representación de una secuencia.](rendering-a-stream.md)</span><span class="sxs-lookup"><span data-stu-id="81488-174">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="81488-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81488-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81488-176">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="81488-176">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



