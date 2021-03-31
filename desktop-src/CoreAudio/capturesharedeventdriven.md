---
description: Esta aplicación de ejemplo usa las API de audio principales para capturar datos de audio de un dispositivo de entrada especificado por el usuario y lo escribe en un archivo. wav con el nombre único en el directorio actual. Este ejemplo muestra el almacenamiento en búfer basado en eventos.
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: CaptureSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 339bd02fcb94f65be558c2dce767747ebf4fab98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153140"
---
# <a name="capturesharedeventdriven"></a><span data-ttu-id="19dd5-104">CaptureSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="19dd5-104">CaptureSharedEventDriven</span></span>

<span data-ttu-id="19dd5-105">Esta aplicación de ejemplo usa las API de audio principales para capturar datos de audio de un dispositivo de entrada especificado por el usuario y lo escribe en un archivo. wav con el nombre único en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="19dd5-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="19dd5-106">Este ejemplo muestra el almacenamiento en búfer basado en eventos.</span><span class="sxs-lookup"><span data-stu-id="19dd5-106">This sample demonstrates event-driven buffering.</span></span>

<span data-ttu-id="19dd5-107">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="19dd5-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="19dd5-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="19dd5-108">Description</span></span>](#description)
-   [<span data-ttu-id="19dd5-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19dd5-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="19dd5-110">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="19dd5-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="19dd5-111">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="19dd5-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="19dd5-112">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="19dd5-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="19dd5-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19dd5-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="19dd5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="19dd5-114">Description</span></span>

<span data-ttu-id="19dd5-115">En este ejemplo se muestran las características siguientes.</span><span class="sxs-lookup"><span data-stu-id="19dd5-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="19dd5-116">[MMDEVICE API](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="19dd5-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="19dd5-117">[WASAPI](wasapi.md) para las operaciones de administración de secuencias como el inicio y la detención de la secuencia y la conmutación por secuencias.</span><span class="sxs-lookup"><span data-stu-id="19dd5-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, and stream switching.</span></span>

## <a name="requirements"></a><span data-ttu-id="19dd5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19dd5-118">Requirements</span></span>



| <span data-ttu-id="19dd5-119">Producto</span><span class="sxs-lookup"><span data-stu-id="19dd5-119">Product</span></span>                                                        | <span data-ttu-id="19dd5-120">Versión</span><span class="sxs-lookup"><span data-stu-id="19dd5-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="19dd5-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="19dd5-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="19dd5-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="19dd5-122">Windows 7</span></span> |
| <span data-ttu-id="19dd5-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="19dd5-123">Visual Studio</span></span>                                                  | <span data-ttu-id="19dd5-124">2008</span><span class="sxs-lookup"><span data-stu-id="19dd5-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="19dd5-125">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="19dd5-125">Downloading the Sample</span></span>

<span data-ttu-id="19dd5-126">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="19dd5-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="19dd5-127">Location</span><span class="sxs-lookup"><span data-stu-id="19dd5-127">Location</span></span>    | <span data-ttu-id="19dd5-128">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="19dd5-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19dd5-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="19dd5-129">Windows SDK</span></span> | <span data-ttu-id="19dd5-130">\\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ CaptureSharedEventDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="19dd5-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="19dd5-131">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="19dd5-131">Building the Sample</span></span>

<span data-ttu-id="19dd5-132">Para compilar el ejemplo CaptureSharedEventDriven, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="19dd5-132">To build the CaptureSharedEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="19dd5-133">Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo CaptureSharedEventDriven.</span><span class="sxs-lookup"><span data-stu-id="19dd5-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedEventDriven sample directory.</span></span>
2.  <span data-ttu-id="19dd5-134">Ejecute el comando `start WASAPICaptureSharedEventDriven.sln` en el directorio CaptureSharedEventDriven para abrir el proyecto WASAPICaptureSharedEventDriven en la ventana de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="19dd5-134">Run the command `start WASAPICaptureSharedEventDriven.sln` in the CaptureSharedEventDriven directory to open the WASAPICaptureSharedEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="19dd5-135">En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** .</span><span class="sxs-lookup"><span data-stu-id="19dd5-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="19dd5-136">Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK.</span><span class="sxs-lookup"><span data-stu-id="19dd5-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="19dd5-137">En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, WASAPICaptureSharedEventDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="19dd5-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="19dd5-138">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="19dd5-138">Running the Sample</span></span>

<span data-ttu-id="19dd5-139">Si compila la aplicación de demostración correctamente, se genera un archivo ejecutable WASAPICaptureSharedEventDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="19dd5-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedEventDriven.exe, is generated.</span></span> <span data-ttu-id="19dd5-140">Para ejecutarlo, escriba `WASAPICaptureSharedEventDriven` en una ventana de comandos seguida de los argumentos obligatorios u opcionales.</span><span class="sxs-lookup"><span data-stu-id="19dd5-140">To run it, type `WASAPICaptureSharedEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="19dd5-141">En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de la captura en el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="19dd5-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="19dd5-142">En la tabla siguiente se muestran los argumentos.</span><span class="sxs-lookup"><span data-stu-id="19dd5-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="19dd5-143">Argumento</span><span class="sxs-lookup"><span data-stu-id="19dd5-143">Argument</span></span>        | <span data-ttu-id="19dd5-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="19dd5-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="19dd5-145">-?</span><span class="sxs-lookup"><span data-stu-id="19dd5-145">-?</span></span>              | <span data-ttu-id="19dd5-146">Muestra la ayuda.</span><span class="sxs-lookup"><span data-stu-id="19dd5-146">Shows help.</span></span>                                                |
| <span data-ttu-id="19dd5-147">-H</span><span class="sxs-lookup"><span data-stu-id="19dd5-147">-h</span></span>              | <span data-ttu-id="19dd5-148">Muestra la ayuda.</span><span class="sxs-lookup"><span data-stu-id="19dd5-148">Shows help.</span></span>                                                |
| <span data-ttu-id="19dd5-149">-l</span><span class="sxs-lookup"><span data-stu-id="19dd5-149">-l</span></span>              | <span data-ttu-id="19dd5-150">Latencia de captura de audio en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="19dd5-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="19dd5-151">-d</span><span class="sxs-lookup"><span data-stu-id="19dd5-151">-d</span></span>              | <span data-ttu-id="19dd5-152">Duración de la captura de audio en segundos.</span><span class="sxs-lookup"><span data-stu-id="19dd5-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="19dd5-153">-M</span><span class="sxs-lookup"><span data-stu-id="19dd5-153">-m</span></span>              | <span data-ttu-id="19dd5-154">Deshabilita el uso de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="19dd5-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="19dd5-155">-consola</span><span class="sxs-lookup"><span data-stu-id="19dd5-155">-console</span></span>        | <span data-ttu-id="19dd5-156">Use el dispositivo de consola predeterminado.</span><span class="sxs-lookup"><span data-stu-id="19dd5-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="19dd5-157">-comunicaciones</span><span class="sxs-lookup"><span data-stu-id="19dd5-157">-communications</span></span> | <span data-ttu-id="19dd5-158">Use el dispositivo de comunicación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="19dd5-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="19dd5-159">-multimedia</span><span class="sxs-lookup"><span data-stu-id="19dd5-159">-multimedia</span></span>     | <span data-ttu-id="19dd5-160">Use el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="19dd5-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="19dd5-161">-punto de conexión</span><span class="sxs-lookup"><span data-stu-id="19dd5-161">-endpoint</span></span>       | <span data-ttu-id="19dd5-162">Use el identificador de extremo especificado en el valor del modificador.</span><span class="sxs-lookup"><span data-stu-id="19dd5-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="19dd5-163">Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo para la sesión de captura.</span><span class="sxs-lookup"><span data-stu-id="19dd5-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="19dd5-164">La consola, la comunicación y los dispositivos multimedia predeterminados aparecen seguidos de los dispositivos y los identificadores de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="19dd5-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="19dd5-165">Si no se especifica Duration, el flujo de audio del dispositivo especificado se captura durante 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="19dd5-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="19dd5-166">La aplicación escribe los datos capturados en un archivo. wav con el nombre único.</span><span class="sxs-lookup"><span data-stu-id="19dd5-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="19dd5-167">CaptureSharedEventDriven muestra el almacenamiento en búfer basado en eventos.</span><span class="sxs-lookup"><span data-stu-id="19dd5-167">CaptureSharedEventDriven demonstrates event-driven buffering.</span></span> <span data-ttu-id="19dd5-168">El cliente de audio del que se ha creado una instancia para este ejemplo está configurado para ejecutarse en modo compartido y el procesamiento del cliente del búfer de audio se realiza mediante el establecimiento de la marca **\_ \_ EVENTCALLBACK STREAMFLAGS AUDCLNT** en la llamada a [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="19dd5-168">The audio client instantiated for this sample is configured to run in shared mode and the client's processing of the audio buffer is made event driven by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span> <span data-ttu-id="19dd5-169">En el ejemplo se muestra cómo el cliente debe proporcionar un identificador de evento al sistema llamando al método [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .</span><span class="sxs-lookup"><span data-stu-id="19dd5-169">The sample shows how the client must provide an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span> <span data-ttu-id="19dd5-170">Una vez iniciada la sesión de captura y iniciada la secuencia, el motor de audio señala el identificador de eventos proporcionado para notificar al cliente cada vez que un búfer está listo para que lo procese el cliente.</span><span class="sxs-lookup"><span data-stu-id="19dd5-170">After the capture session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="19dd5-171">Los datos de audio también se pueden procesar en un bucle controlado por temporizador.</span><span class="sxs-lookup"><span data-stu-id="19dd5-171">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="19dd5-172">Este modo se demostrated en el ejemplo [CaptureSharedTimerDriven](capturesharedtimerdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="19dd5-172">This mode is demostrated in the [CaptureSharedTimerDriven](capturesharedtimerdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19dd5-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19dd5-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19dd5-174">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="19dd5-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



