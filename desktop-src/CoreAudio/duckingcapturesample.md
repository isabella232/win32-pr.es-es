---
description: En esta aplicación de ejemplo se muestra la apertura y el cierre de secuencias de comunicación y la causa de los eventos que una aplicación puede obtener para implementar la atenuación de la secuencia.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 636fe39e8fa27beee14ab17548f5929d1d937b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907511"
---
# <a name="duckingcapturesample"></a><span data-ttu-id="02b43-103">DuckingCaptureSample</span><span class="sxs-lookup"><span data-stu-id="02b43-103">DuckingCaptureSample</span></span>

<span data-ttu-id="02b43-104">En esta aplicación de ejemplo se muestra la apertura y el cierre de secuencias de comunicación y la causa de los eventos que una aplicación puede obtener para implementar la atenuación de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="02b43-104">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="02b43-105">Esta aplicación implementa un cliente de chat que usa las API de audio principales para leer los datos de audio de un dispositivo de comunicación y reproducirlos en el dispositivo de salida.</span><span class="sxs-lookup"><span data-stu-id="02b43-105">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span>

<span data-ttu-id="02b43-106">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="02b43-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="02b43-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="02b43-107">Description</span></span>](#description)
-   [<span data-ttu-id="02b43-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02b43-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="02b43-109">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="02b43-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="02b43-110">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="02b43-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="02b43-111">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="02b43-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="02b43-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02b43-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="02b43-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="02b43-113">Description</span></span>

<span data-ttu-id="02b43-114">En este ejemplo se muestran las características siguientes.</span><span class="sxs-lookup"><span data-stu-id="02b43-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="02b43-115">[MMDEVICE API](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="02b43-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="02b43-116">[WASAPI](wasapi.md) para acceder al dispositivo de captura y representación de comunicaciones, las operaciones de administración de secuencias y el control de eventos de pato.</span><span class="sxs-lookup"><span data-stu-id="02b43-116">[WASAPI](wasapi.md) for accessing the communications capture and render device, stream management operations, and handling ducking events.</span></span>
-   <span data-ttu-id="02b43-117">[API de Wave](/previous-versions//ms713499(v=vs.85)) para acceder al dispositivo de comunicaciones y capturar entradas de audio.</span><span class="sxs-lookup"><span data-stu-id="02b43-117">[WAVE APIs](/previous-versions//ms713499(v=vs.85)) for accessing the communications device and capturing audio input.</span></span>

## <a name="requirements"></a><span data-ttu-id="02b43-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02b43-118">Requirements</span></span>



| <span data-ttu-id="02b43-119">Producto</span><span class="sxs-lookup"><span data-stu-id="02b43-119">Product</span></span>                                                        | <span data-ttu-id="02b43-120">Versión</span><span class="sxs-lookup"><span data-stu-id="02b43-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="02b43-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="02b43-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="02b43-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02b43-122">Windows 7</span></span> |
| <span data-ttu-id="02b43-123">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="02b43-123">Visual Studio 2008</span></span>                                             |           |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="02b43-124">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="02b43-124">Downloading the Sample</span></span>

<span data-ttu-id="02b43-125">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="02b43-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="02b43-126">Location</span><span class="sxs-lookup"><span data-stu-id="02b43-126">Location</span></span>    | <span data-ttu-id="02b43-127">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="02b43-127">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b43-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="02b43-128">Windows SDK</span></span> | <span data-ttu-id="02b43-129">\\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ DuckingCaptureSample \\ ...</span><span class="sxs-lookup"><span data-stu-id="02b43-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingCaptureSample\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="02b43-130">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="02b43-130">Building the Sample</span></span>

<span data-ttu-id="02b43-131">Para compilar el ejemplo DuckingCaptureSample, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="02b43-131">To build the DuckingCaptureSample sample, use the following steps:</span></span>

1.  <span data-ttu-id="02b43-132">Abra DuckingCaptureSample. sln en Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="02b43-132">Open the DuckingCaptureSample.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="02b43-133">En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** .</span><span class="sxs-lookup"><span data-stu-id="02b43-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="02b43-134">Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK.</span><span class="sxs-lookup"><span data-stu-id="02b43-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="02b43-135">En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, DuckingCaptureSample. vcproj.</span><span class="sxs-lookup"><span data-stu-id="02b43-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingCaptureSample.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="02b43-136">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="02b43-136">Running the Sample</span></span>

<span data-ttu-id="02b43-137">Si compila la aplicación correctamente, se genera un archivo ejecutable DuckingCaptureSample.exe.</span><span class="sxs-lookup"><span data-stu-id="02b43-137">If you build the application successfully, an executable file, DuckingCaptureSample.exe, is generated.</span></span> <span data-ttu-id="02b43-138">Para ejecutarlo, seleccione **iniciar depuración** o **iniciar sin depurar** en el menú **depurar** o escriba `DuckingCaptureSample` en una ventana de comandos.</span><span class="sxs-lookup"><span data-stu-id="02b43-138">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingCaptureSample` in a command window.</span></span>

<span data-ttu-id="02b43-139">DuckingCaptureSample proporciona al usuario dos implementaciones para capturar audio desde el dispositivo de consola predeterminado: WASAPI y Wave API.</span><span class="sxs-lookup"><span data-stu-id="02b43-139">DuckingCaptureSample provides the user with two implementations to capture audio from the default console device: WASAPI and Wave APIs.</span></span> <span data-ttu-id="02b43-140">Para iniciar una sesión de captura, seleccione un modo y haga clic en **iniciar** en la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="02b43-140">To start a capture session, select a mode and click **Start** on the application's user interface.</span></span> <span data-ttu-id="02b43-141">Para finalizar la sesión, haga clic en **detener**.</span><span class="sxs-lookup"><span data-stu-id="02b43-141">To end the session, click **Stop**.</span></span> <span data-ttu-id="02b43-142">Según el dispositivo especificado por el usuario (entrada o salida), la aplicación usa la API de MMDevice para obtener una referencia al dispositivo de comunicación de representación o captura predeterminado.</span><span class="sxs-lookup"><span data-stu-id="02b43-142">Depending on the device specified by the user (input or output), the application uses MMDevice API to get a reference to the default rendering or capture communication device.</span></span> <span data-ttu-id="02b43-143">Una vez que el usuario inicia una sesión de chat, la aplicación realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="02b43-143">After the user starts a chat session, the application performs the following tasks:</span></span>

-   <span data-ttu-id="02b43-144">Crea e inicializa un cliente de audio en modo basado en eventos.</span><span class="sxs-lookup"><span data-stu-id="02b43-144">Creates and initializes an audio client in event-driven mode.</span></span>
-   <span data-ttu-id="02b43-145">Asocia el cliente con el identificador de evento que indica que los ejemplos están listos para su captura o representación.</span><span class="sxs-lookup"><span data-stu-id="02b43-145">Associates the client with the event handle that signals that samples are ready for capture or rendering.</span></span>
-   <span data-ttu-id="02b43-146">Configura un cliente de captura y un cliente de representación para el transporte.</span><span class="sxs-lookup"><span data-stu-id="02b43-146">Sets up a capture client and a rendering client for the transport.</span></span>
-   <span data-ttu-id="02b43-147">Crea el subproceso de chat e inicia el motor de audio.</span><span class="sxs-lookup"><span data-stu-id="02b43-147">Creates the chat thread and starts the audio engine.</span></span>

<span data-ttu-id="02b43-148">Para capturar datos de audio, con cada paso de procesamiento, el ejemplo usa el cliente de captura para obtener la cantidad total de datos capturados que están disponibles en el búfer, leer datos del dispositivo de entrada predeterminado y liberar el paquete y hacer que el búfer esté disponible para leer el siguiente conjunto de datos capturados.</span><span class="sxs-lookup"><span data-stu-id="02b43-148">For capturing audio data, with each processing pass, the sample uses the capture client to get the total amount of captured data that is available in the buffer, read data from the default input device, and release the packet and make the buffer available for reading the next set of captured data.</span></span>

<span data-ttu-id="02b43-149">Para la representación, la aplicación determina la cantidad de datos que se ponen en cola para reproducirlos en el búfer del extremo de captura.</span><span class="sxs-lookup"><span data-stu-id="02b43-149">For rendering, the application determines the amount of data that is queued up to play in the capture endpoint buffer.</span></span> <span data-ttu-id="02b43-150">En consecuencia, escribe en el búfer y libera el búfer como preparación para la siguiente fase de procesamiento hasta que se han escrito todos los datos.</span><span class="sxs-lookup"><span data-stu-id="02b43-150">It accordingly writes to the buffer and releases the buffer in preparation for the next processing pass until all of the data has been written.</span></span> <span data-ttu-id="02b43-151">Para la representación, los marcos silenciosos se preparan para evitar que el motor de audio se ponga en proceso en el inicio.</span><span class="sxs-lookup"><span data-stu-id="02b43-151">For rendering, silent frames are prerolled to prevent the audio engine from glitching on startup.</span></span> <span data-ttu-id="02b43-152">DuckingCaptureSample también muestra cómo ocultar el flujo de representación del mezclador de volumen.</span><span class="sxs-lookup"><span data-stu-id="02b43-152">DuckingCaptureSample also shows how to hide the render stream from the volume mixer.</span></span>

<span data-ttu-id="02b43-153">Para obtener más información acerca de la característica de atenuación de flujos, consulte [uso de un dispositivo de comunicación](using-the-communication-device.md).</span><span class="sxs-lookup"><span data-stu-id="02b43-153">For more information about the stream attenuation feature, see [Using a Communication Device](using-the-communication-device.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02b43-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02b43-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02b43-155">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="02b43-155">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
