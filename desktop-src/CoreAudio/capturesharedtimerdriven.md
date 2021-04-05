---
description: Esta aplicación de ejemplo usa las API de audio principales para capturar datos de audio de un dispositivo de entrada especificado por el usuario y lo escribe en un archivo. wav con el nombre único en el directorio actual. Este ejemplo muestra el almacenamiento en búfer basado en temporizador.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080208"
---
# <a name="capturesharedtimerdriven"></a><span data-ttu-id="a33e0-104">CaptureSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="a33e0-104">CaptureSharedTimerDriven</span></span>

<span data-ttu-id="a33e0-105">Esta aplicación de ejemplo usa las API de audio principales para capturar datos de audio de un dispositivo de entrada especificado por el usuario y lo escribe en un archivo. wav con el nombre único en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="a33e0-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="a33e0-106">Este ejemplo muestra el almacenamiento en búfer basado en temporizador.</span><span class="sxs-lookup"><span data-stu-id="a33e0-106">This sample demonstrates timer-driven buffering.</span></span>

<span data-ttu-id="a33e0-107">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="a33e0-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a33e0-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a33e0-108">Description</span></span>](#description)
-   [<span data-ttu-id="a33e0-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a33e0-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a33e0-110">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a33e0-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="a33e0-111">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a33e0-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="a33e0-112">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a33e0-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="a33e0-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a33e0-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="a33e0-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a33e0-114">Description</span></span>

<span data-ttu-id="a33e0-115">En este ejemplo se muestran las características siguientes.</span><span class="sxs-lookup"><span data-stu-id="a33e0-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="a33e0-116">[MMDEVICE API](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="a33e0-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="a33e0-117">[WASAPI](wasapi.md) para las operaciones de administración de secuencias.</span><span class="sxs-lookup"><span data-stu-id="a33e0-117">[WASAPI](wasapi.md) for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="a33e0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a33e0-118">Requirements</span></span>



| <span data-ttu-id="a33e0-119">Producto</span><span class="sxs-lookup"><span data-stu-id="a33e0-119">Product</span></span>                                                        | <span data-ttu-id="a33e0-120">Versión</span><span class="sxs-lookup"><span data-stu-id="a33e0-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="a33e0-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a33e0-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="a33e0-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a33e0-122">Windows 7</span></span> |
| <span data-ttu-id="a33e0-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a33e0-123">Visual Studio</span></span>                                                  | <span data-ttu-id="a33e0-124">2008</span><span class="sxs-lookup"><span data-stu-id="a33e0-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="a33e0-125">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a33e0-125">Downloading the Sample</span></span>

<span data-ttu-id="a33e0-126">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="a33e0-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="a33e0-127">Location</span><span class="sxs-lookup"><span data-stu-id="a33e0-127">Location</span></span>    | <span data-ttu-id="a33e0-128">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="a33e0-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a33e0-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a33e0-129">Windows SDK</span></span> | <span data-ttu-id="a33e0-130">\\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ CaptureSharedTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="a33e0-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="a33e0-131">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a33e0-131">Building the Sample</span></span>

<span data-ttu-id="a33e0-132">Para compilar el ejemplo CaptureSharedTimerDriven, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a33e0-132">To build the CaptureSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="a33e0-133">Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo CaptureSharedTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="a33e0-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="a33e0-134">Ejecute el comando `start WASAPICaptureSharedTimerDriven.sln` en el directorio CaptureSharedTimerDriven para abrir el proyecto WASAPICaptureSharedTimerDriven en la ventana de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a33e0-134">Run the command `start WASAPICaptureSharedTimerDriven.sln` in the CaptureSharedTimerDriven directory to open the WASAPICaptureSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="a33e0-135">En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** .</span><span class="sxs-lookup"><span data-stu-id="a33e0-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="a33e0-136">Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK.</span><span class="sxs-lookup"><span data-stu-id="a33e0-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="a33e0-137">En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, WASAPICaptureSharedTimerDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="a33e0-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a33e0-138">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a33e0-138">Running the Sample</span></span>

<span data-ttu-id="a33e0-139">Si compila la aplicación de demostración correctamente, se genera un archivo ejecutable WASAPICaptureSharedTimerDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="a33e0-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="a33e0-140">Para ejecutarlo, escriba `WASAPICaptureSharedTimerDriven` en una ventana de comandos seguida de los argumentos obligatorios u opcionales.</span><span class="sxs-lookup"><span data-stu-id="a33e0-140">To run it, type `WASAPICaptureSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="a33e0-141">En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de la captura en el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a33e0-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="a33e0-142">En la tabla siguiente se muestran los argumentos.</span><span class="sxs-lookup"><span data-stu-id="a33e0-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="a33e0-143">Argumento</span><span class="sxs-lookup"><span data-stu-id="a33e0-143">Argument</span></span>        | <span data-ttu-id="a33e0-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="a33e0-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="a33e0-145">-?</span><span class="sxs-lookup"><span data-stu-id="a33e0-145">-?</span></span>              | <span data-ttu-id="a33e0-146">Muestra la ayuda.</span><span class="sxs-lookup"><span data-stu-id="a33e0-146">Shows help.</span></span>                                                |
| <span data-ttu-id="a33e0-147">-H</span><span class="sxs-lookup"><span data-stu-id="a33e0-147">-h</span></span>              | <span data-ttu-id="a33e0-148">Muestra la ayuda.</span><span class="sxs-lookup"><span data-stu-id="a33e0-148">Shows help.</span></span>                                                |
| <span data-ttu-id="a33e0-149">-l</span><span class="sxs-lookup"><span data-stu-id="a33e0-149">-l</span></span>              | <span data-ttu-id="a33e0-150">Latencia de captura de audio en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="a33e0-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="a33e0-151">-d</span><span class="sxs-lookup"><span data-stu-id="a33e0-151">-d</span></span>              | <span data-ttu-id="a33e0-152">Duración de la captura de audio en segundos.</span><span class="sxs-lookup"><span data-stu-id="a33e0-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="a33e0-153">-M</span><span class="sxs-lookup"><span data-stu-id="a33e0-153">-m</span></span>              | <span data-ttu-id="a33e0-154">Deshabilita el uso de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="a33e0-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="a33e0-155">-consola</span><span class="sxs-lookup"><span data-stu-id="a33e0-155">-console</span></span>        | <span data-ttu-id="a33e0-156">Use el dispositivo de consola predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a33e0-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="a33e0-157">-comunicaciones</span><span class="sxs-lookup"><span data-stu-id="a33e0-157">-communications</span></span> | <span data-ttu-id="a33e0-158">Use el dispositivo de comunicación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a33e0-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="a33e0-159">-multimedia</span><span class="sxs-lookup"><span data-stu-id="a33e0-159">-multimedia</span></span>     | <span data-ttu-id="a33e0-160">Use el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a33e0-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="a33e0-161">-punto de conexión</span><span class="sxs-lookup"><span data-stu-id="a33e0-161">-endpoint</span></span>       | <span data-ttu-id="a33e0-162">Use el identificador de extremo especificado en el valor del modificador.</span><span class="sxs-lookup"><span data-stu-id="a33e0-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="a33e0-163">Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo para la sesión de captura.</span><span class="sxs-lookup"><span data-stu-id="a33e0-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="a33e0-164">La consola, la comunicación y los dispositivos multimedia predeterminados aparecen seguidos de los dispositivos y los identificadores de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="a33e0-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="a33e0-165">Si no se especifica Duration, el flujo de audio del dispositivo especificado se captura durante 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="a33e0-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="a33e0-166">La aplicación escribe los datos capturados en un archivo. wav con el nombre único.</span><span class="sxs-lookup"><span data-stu-id="a33e0-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="a33e0-167">CaptureSharedTimerDriven muestra el almacenamiento en búfer basado en temporizador.</span><span class="sxs-lookup"><span data-stu-id="a33e0-167">CaptureSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="a33e0-168">En este modo, el cliente debe esperar durante un período de tiempo (la mitad de la latencia, especificada por el valor del modificador-d, en milisegundos).</span><span class="sxs-lookup"><span data-stu-id="a33e0-168">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="a33e0-169">Cuando el cliente se reactiva, a mitad del período de procesamiento, extrae el siguiente conjunto de ejemplos del motor.</span><span class="sxs-lookup"><span data-stu-id="a33e0-169">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="a33e0-170">Antes de cada paso de procesamiento en el bucle de almacenamiento en búfer, el cliente debe averiguar la cantidad de datos de captura disponibles para que los datos no desbordan el búfer de captura.</span><span class="sxs-lookup"><span data-stu-id="a33e0-170">Before each processing pass in the buffering loop, the client must find out the amount of capture data available so that the data does not overrun the capture buffer.</span></span> <span data-ttu-id="a33e0-171">Los datos de audio que se capturan desde el dispositivo especificado se pueden procesar habilitando el almacenamiento en búfer basado en eventos.</span><span class="sxs-lookup"><span data-stu-id="a33e0-171">The audio data that is captured from the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="a33e0-172">Este modo se muestra en el ejemplo [CaptureSharedEventDriven](capturesharedeventdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="a33e0-172">This mode is demonstrated in the [CaptureSharedEventDriven](capturesharedeventdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a33e0-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a33e0-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a33e0-174">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="a33e0-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



