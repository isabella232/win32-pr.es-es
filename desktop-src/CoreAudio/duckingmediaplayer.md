---
description: En esta aplicación de ejemplo se muestra la atenuación de la secuencia mediante la implementación de un reproductor de media que muestra el comportamiento de atenuación predeterminado proporcionado por el sistema, no participa en la carga de eventos e implementa el control personalizado cuando se reciben eventos de la carga.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: DuckingMediaPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86952f1aa7b81c9a7dc711f0c4f36fc8531bd63
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105660005"
---
# <a name="duckingmediaplayer"></a><span data-ttu-id="584e6-103">DuckingMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="584e6-103">DuckingMediaPlayer</span></span>

<span data-ttu-id="584e6-104">En esta aplicación de ejemplo se muestra la atenuación de la secuencia mediante la implementación de un reproductor de media que muestra el comportamiento de atenuación predeterminado proporcionado por el sistema, no participa en la carga de eventos e implementa el control personalizado cuando se reciben eventos de la carga.</span><span class="sxs-lookup"><span data-stu-id="584e6-104">This sample application demonstrates stream attenuation by implementing a media player that shows the default attenuation behavior provided by the system, opts out of ducking events, and implements custom handling when ducking events are received.</span></span> <span data-ttu-id="584e6-105">Este ejemplo se debe usar en conjuction con [DuckingCaptureSample](duckingcapturesample.md).</span><span class="sxs-lookup"><span data-stu-id="584e6-105">This sample must be used in conjuction with [DuckingCaptureSample](duckingcapturesample.md).</span></span> <span data-ttu-id="584e6-106">Para obtener más información sobre la forma de uso de metadatos o de la atenuación de flujos, consulte [experiencia predeterminada de los patos](stream-attenuation.md).</span><span class="sxs-lookup"><span data-stu-id="584e6-106">For more information about ducking or stream attenuation, see [Default Ducking Experience](stream-attenuation.md).</span></span>

<span data-ttu-id="584e6-107">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="584e6-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="584e6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="584e6-108">Description</span></span>](#description)
-   [<span data-ttu-id="584e6-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="584e6-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="584e6-110">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="584e6-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="584e6-111">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="584e6-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="584e6-112">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="584e6-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="584e6-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="584e6-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="584e6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="584e6-114">Description</span></span>

<span data-ttu-id="584e6-115">En este ejemplo se muestran las características siguientes.</span><span class="sxs-lookup"><span data-stu-id="584e6-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="584e6-116">DirectShow para reproducir un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="584e6-116">DirectShow to play a media file.</span></span>
-   <span data-ttu-id="584e6-117">[WASAPI](wasapi.md) para la administración de transmisiones y control de eventos de pato.</span><span class="sxs-lookup"><span data-stu-id="584e6-117">[WASAPI](wasapi.md) for stream management and handling ducking events.</span></span>

## <a name="requirements"></a><span data-ttu-id="584e6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="584e6-118">Requirements</span></span>



| <span data-ttu-id="584e6-119">Producto</span><span class="sxs-lookup"><span data-stu-id="584e6-119">Product</span></span>                                                        | <span data-ttu-id="584e6-120">Versión</span><span class="sxs-lookup"><span data-stu-id="584e6-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="584e6-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="584e6-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="584e6-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="584e6-122">Windows 7</span></span> |
| <span data-ttu-id="584e6-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="584e6-123">Visual Studio</span></span>                                                  | <span data-ttu-id="584e6-124">2008</span><span class="sxs-lookup"><span data-stu-id="584e6-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="584e6-125">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="584e6-125">Downloading the Sample</span></span>

<span data-ttu-id="584e6-126">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="584e6-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="584e6-127">Location</span><span class="sxs-lookup"><span data-stu-id="584e6-127">Location</span></span>    | <span data-ttu-id="584e6-128">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="584e6-128">Path/URL</span></span>                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="584e6-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="584e6-129">Windows SDK</span></span> | <span data-ttu-id="584e6-130">\\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ DuckingMediaPlayer \\ ...</span><span class="sxs-lookup"><span data-stu-id="584e6-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingMediaPlayer\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="584e6-131">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="584e6-131">Building the Sample</span></span>

<span data-ttu-id="584e6-132">Para compilar el ejemplo DuckingMediaPlayer, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="584e6-132">To build the DuckingMediaPlayer sample, use the following steps:</span></span>

1.  <span data-ttu-id="584e6-133">Abra DuckingMediaPlayer. sln en Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="584e6-133">Open the DuckingMediaPlayer.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="584e6-134">En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** .</span><span class="sxs-lookup"><span data-stu-id="584e6-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="584e6-135">Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK.</span><span class="sxs-lookup"><span data-stu-id="584e6-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="584e6-136">En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, DuckingMediaPlayer. vcproj.</span><span class="sxs-lookup"><span data-stu-id="584e6-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingMediaPlayer.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="584e6-137">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="584e6-137">Running the Sample</span></span>

<span data-ttu-id="584e6-138">Si compila la aplicación correctamente, se genera un archivo ejecutable DuckingMediaPlayer.exe.</span><span class="sxs-lookup"><span data-stu-id="584e6-138">If you build the application successfully, an executable file, DuckingMediaPlayer.exe, is generated.</span></span> <span data-ttu-id="584e6-139">Para ejecutarlo, seleccione **iniciar depuración** o **iniciar sin depurar** en el menú **depurar** o escriba `DuckingMediaPlayer` en una ventana de comandos.</span><span class="sxs-lookup"><span data-stu-id="584e6-139">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingMediaPlayer` in a command window.</span></span>

<span data-ttu-id="584e6-140">Para ver una demostración de la pato, debe ejecutar DuckingMediaPlayer y DuckingCaptureSample simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="584e6-140">To view a demonstration of ducking, you must execute DuckingMediaPlayer and DuckingCaptureSample simultaneously.</span></span> <span data-ttu-id="584e6-141">DuckingCaptureSample abre un flujo de comunicación e indica al sistema que genere un evento de pato.</span><span class="sxs-lookup"><span data-stu-id="584e6-141">DuckingCaptureSample opens a communication stream and signals the system to generate a ducking event.</span></span> <span data-ttu-id="584e6-142">El sistema notifica a DuckingMediaPlayer cuando se produce un evento de pato y el reproductor de media realiza la acción solicitada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="584e6-142">The DuckingMediaPlayer is notified by the system when a ducking event occurs, and the media player performs the action requested by the user.</span></span>

<span data-ttu-id="584e6-143">Para deshabilitar el comportamiento de los patos:</span><span class="sxs-lookup"><span data-stu-id="584e6-143">To disable ducking behavior:</span></span>

1.  <span data-ttu-id="584e6-144">En la ventana DuckingCaptureSample, seleccione **usar el dispositivo de entrada predeterminado** y haga clic en **iniciar** para iniciar una sesión de captura desde el dispositivo de comunicación.</span><span class="sxs-lookup"><span data-stu-id="584e6-144">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="584e6-145">En el DuckingMediaPlayer, seleccione un archivo multimedia para reproducirlo y especifique la opción de patos como no **participar**.</span><span class="sxs-lookup"><span data-stu-id="584e6-145">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Opt out of Ducking**.</span></span>

<span data-ttu-id="584e6-146">Tenga en cuenta que el archivo multimedia se reproduce sin ninguna interrupción.</span><span class="sxs-lookup"><span data-stu-id="584e6-146">Notice that the media file is played without any interruption.</span></span> <span data-ttu-id="584e6-147">Los eventos generados por el sistema cuando se omite el flujo de comunicación abierto.</span><span class="sxs-lookup"><span data-stu-id="584e6-147">The events generated by the system when the communication stream opened are ignored.</span></span>

<span data-ttu-id="584e6-148">Para demostrar el comportamiento de la forma predeterminada de los patos proporcionados por el sistema, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="584e6-148">To demonstrate the default ducking behavior provided by the system, do the following:</span></span>

1.  <span data-ttu-id="584e6-149">Seleccione la opción **sonidos** en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="584e6-149">Select the **Sounds** option from the control panel.</span></span> <span data-ttu-id="584e6-150">En la pestaña **comunicaciones** , seleccione **reducir el volumen de otros sonidos en un 80%**.</span><span class="sxs-lookup"><span data-stu-id="584e6-150">On the **Communications** tab, select **Reduce the volume of other sounds by 80%**.</span></span>
2.  <span data-ttu-id="584e6-151">En la ventana DuckingCaptureSample, seleccione **usar el dispositivo de entrada predeterminado** y haga clic en **iniciar** para iniciar una sesión de captura desde el dispositivo de comunicación.</span><span class="sxs-lookup"><span data-stu-id="584e6-151">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
3.  <span data-ttu-id="584e6-152">En el DuckingMediaPlayer, seleccione un archivo multimedia para reproducirlo sin elegir ninguna de las opciones de pato.</span><span class="sxs-lookup"><span data-stu-id="584e6-152">On the DuckingMediaPlayer, select a media file to play, without choosing any of the ducking options.</span></span>
4.  <span data-ttu-id="584e6-153">En la ventana DuckingCaptureSample, haga clic en **detener** para detener la secuencia de comunicación.</span><span class="sxs-lookup"><span data-stu-id="584e6-153">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="584e6-154">Tenga en cuenta que cuando DuckingCaptureSample abre la secuencia de comunicación, el archivo multimedia que reproduce DuckingMediaPlayer se reproduce sin interrupción, pero se reduce el nivel de volumen.</span><span class="sxs-lookup"><span data-stu-id="584e6-154">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer plays without interruption, but the volume level is lowered.</span></span> <span data-ttu-id="584e6-155">Cuando se detiene la sesión de comunicación, el volumen se restablece a la configuración original.</span><span class="sxs-lookup"><span data-stu-id="584e6-155">When the communication session is stopped, the volume is reset to the original setting.</span></span> <span data-ttu-id="584e6-156">Este comportamiento de la atenuación de secuencias es el comportamiento de la forma predeterminada de los patos implementado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="584e6-156">This stream attenuation behavior is the default ducking behavior implemented by the system.</span></span>

<span data-ttu-id="584e6-157">Para ver un comportamiento personalizado de patos implementado por el reproductor de media:</span><span class="sxs-lookup"><span data-stu-id="584e6-157">To view a customized ducking behavior implemented by the media player:</span></span>

1.  <span data-ttu-id="584e6-158">En la ventana DuckingCaptureSample, seleccione **usar el dispositivo de entrada predeterminado** y haga clic en **iniciar** para iniciar una sesión de captura desde el dispositivo de comunicación.</span><span class="sxs-lookup"><span data-stu-id="584e6-158">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="584e6-159">En el DuckingMediaPlayer, seleccione un archivo multimedia para reproducirlo y especifique la opción de la pato como **pausar en Duck**.</span><span class="sxs-lookup"><span data-stu-id="584e6-159">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Pause on Duck**.</span></span>
3.  <span data-ttu-id="584e6-160">En la ventana DuckingCaptureSample, haga clic en **detener** para detener la secuencia de comunicación.</span><span class="sxs-lookup"><span data-stu-id="584e6-160">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="584e6-161">Tenga en cuenta que cuando DuckingCaptureSample abre el flujo de comunicación, el archivo multimedia que reproduce DuckingMediaPlayer está en pausa.</span><span class="sxs-lookup"><span data-stu-id="584e6-161">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer is paused.</span></span> <span data-ttu-id="584e6-162">La reproducción se reanuda cuando se detiene la sesión de comunicación.</span><span class="sxs-lookup"><span data-stu-id="584e6-162">The playback resumes when the communication session is stopped.</span></span> <span data-ttu-id="584e6-163">Este comportamiento de la atenuación de secuencias es el comportamiento de los patos implementado por el reproductor de media.</span><span class="sxs-lookup"><span data-stu-id="584e6-163">This stream attenuation behavior is the ducking behavior implemented by the media player.</span></span>

<span data-ttu-id="584e6-164">DuckingMediaPlayer también muestra cómo integrar el control de volumen para cada aplicación con el mezclador de volumen.</span><span class="sxs-lookup"><span data-stu-id="584e6-164">DuckingMediaPlayer also demonstrates how to integrate volume control for each application with the volume mixer.</span></span>

<span data-ttu-id="584e6-165">Para obtener más información acerca de la característica de atenuación de flujos, consulte [experiencia predeterminada](stream-attenuation.md)de la misma.</span><span class="sxs-lookup"><span data-stu-id="584e6-165">For more information about the stream attenuation feature, see [Default Ducking Experience](stream-attenuation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="584e6-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="584e6-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="584e6-167">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="584e6-167">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



