---
description: Ejemplo de DVApp
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Ejemplo de DVApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86653781d08921bf638e7798fb34f3a86e8d34a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152438"
---
# <a name="dvapp-sample"></a><span data-ttu-id="40982-103">Ejemplo de DVApp</span><span class="sxs-lookup"><span data-stu-id="40982-103">DVApp Sample</span></span>

## <a name="description"></a><span data-ttu-id="40982-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="40982-104">Description</span></span>

<span data-ttu-id="40982-105">Aplicación de captura de vídeo digital (DV).</span><span class="sxs-lookup"><span data-stu-id="40982-105">Digital Video (DV) capture application.</span></span>

<span data-ttu-id="40982-106">Este ejemplo muestra cómo crear varios tipos de gráficos de filtro para controlar las videocámaras DV.</span><span class="sxs-lookup"><span data-stu-id="40982-106">This sample demonstrates how to build various types of filter graphs for controlling DV camcorders.</span></span> <span data-ttu-id="40982-107">También muestra cómo realizar la captura, la vista previa, la transmisión y el control de dispositivos con una videocámara DV.</span><span class="sxs-lookup"><span data-stu-id="40982-107">It also shows how to perform capture, preview, transmit, and device control with a DV camcorder.</span></span>

### <a name="usage"></a><span data-ttu-id="40982-108">Uso</span><span class="sxs-lookup"><span data-stu-id="40982-108">Usage</span></span>

<span data-ttu-id="40982-109">La aplicación DVApp admite los siguientes modos:</span><span class="sxs-lookup"><span data-stu-id="40982-109">The DVApp application supports the following modes:</span></span>

-   <span data-ttu-id="40982-110">Versión preliminar: representa el DV del camascopio en una ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="40982-110">Preview: Renders DV from the camcorder to a video window.</span></span>
-   <span data-ttu-id="40982-111">DV to Type-1 file: captura datos de DV del camascopio en un archivo DV de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="40982-111">DV to type-1 file: Captures DV data from the camcorder to a type-1 DV file.</span></span>
-   <span data-ttu-id="40982-112">Archivo de tipo 1 a DV: transmite datos de un archivo DV de tipo 1 a la videocámara.</span><span class="sxs-lookup"><span data-stu-id="40982-112">Type-1 file to DV: Transmits data from a type-1 DV file to the camcorder.</span></span>
-   <span data-ttu-id="40982-113">DV to Type-2 File: captura los datos de DV del camascopio en un archivo DV de tipo 2.</span><span class="sxs-lookup"><span data-stu-id="40982-113">DV to type-2 file: Captures DV data from the camcorder to a type-2 DV file.</span></span>
-   <span data-ttu-id="40982-114">Escriba-2 archivo en DV: transmite datos de un archivo DV de tipo 2 a la videocámara.</span><span class="sxs-lookup"><span data-stu-id="40982-114">Type-2 file to DV: Transmits data from a type-2 DV file to the camcorder.</span></span>

<span data-ttu-id="40982-115">Los modos de captura y transmisión también realizan la vista previa.</span><span class="sxs-lookup"><span data-stu-id="40982-115">The capture and transmit modes also perform preview.</span></span> <span data-ttu-id="40982-116">Cada uno de esos modos tiene también una opción **no vista previa** , lo que deshabilita la vista previa.</span><span class="sxs-lookup"><span data-stu-id="40982-116">Each of those modes has a **No Preview** option as well, which disables preview.</span></span> <span data-ttu-id="40982-117">La captura sin vista previa es más eficaz y puede reducir el número de fotogramas quitados.</span><span class="sxs-lookup"><span data-stu-id="40982-117">Capturing without preview is more efficient and can reduce the number of dropped frames.</span></span>

<span data-ttu-id="40982-118">La aplicación se inicia en modo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="40982-118">The application starts in preview mode.</span></span> <span data-ttu-id="40982-119">Para seleccionar otro modo, elija un modo en el menú **modo de gráfico** .</span><span class="sxs-lookup"><span data-stu-id="40982-119">To select another mode, choose a mode from the **Graph Mode** menu.</span></span> <span data-ttu-id="40982-120">En cada modo, DVApp crea un gráfico de filtros que admite la funcionalidad de ese modo.</span><span class="sxs-lookup"><span data-stu-id="40982-120">For each mode, DVApp builds a filter graph that supports the functionality of that mode.</span></span> <span data-ttu-id="40982-121">Para guardar el gráfico como un archivo GraphEdit (. GRF), seleccione **guardar el gráfico en el archivo** en el menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="40982-121">To save the graph as a GraphEdit (.grf) file, select **Save Graph to File** from the **File** menu.</span></span> <span data-ttu-id="40982-122">Salga de DVApp antes de abrir el archivo en GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="40982-122">Quit DVApp before opening the file in GraphEdit.</span></span>

<span data-ttu-id="40982-123">Para capturar en un archivo:</span><span class="sxs-lookup"><span data-stu-id="40982-123">To capture to a file:</span></span>

1.  <span data-ttu-id="40982-124">En el menú **archivo** , elija **establecer archivo de salida** y escriba un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="40982-124">From the **File** menu, choose **Set Output File** and enter a file name.</span></span>
2.  <span data-ttu-id="40982-125">En el menú **modo de gráfico** , seleccione un modo de *DV a archivo* (tipo 1 o 2, con o sin vista previa).</span><span class="sxs-lookup"><span data-stu-id="40982-125">From the **Graph Mode** menu, select a *DV to File* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="40982-126">Haga clic en **registro**.</span><span class="sxs-lookup"><span data-stu-id="40982-126">Click **Record**.</span></span>
4.  <span data-ttu-id="40982-127">Si el camascopio está en modo VTR, haga clic en **reproducir**.</span><span class="sxs-lookup"><span data-stu-id="40982-127">If the camcorder is in VTR mode, click **Play**.</span></span>
5.  <span data-ttu-id="40982-128">Para detener la captura, haga clic en **detener**.</span><span class="sxs-lookup"><span data-stu-id="40982-128">To stop capturing, click **Stop**.</span></span>

<span data-ttu-id="40982-129">Para transmitir desde un archivo al camascopio:</span><span class="sxs-lookup"><span data-stu-id="40982-129">To transmit from a file to the camcorder:</span></span>

1.  <span data-ttu-id="40982-130">En el menú **archivo** , haga clic en **establecer archivo de entrada** y seleccione un archivo DV.</span><span class="sxs-lookup"><span data-stu-id="40982-130">From the **File** menu, click **Set Input File** and select a DV file.</span></span> <span data-ttu-id="40982-131">El archivo debe coincidir con el modo seleccionado (tipo 1 o tipo 2).</span><span class="sxs-lookup"><span data-stu-id="40982-131">The file must match the selected mode (type 1 or type 2).</span></span>
2.  <span data-ttu-id="40982-132">En el menú **modo de gráfico** , seleccione un *archivo en modo DV* (tipo 1 o tipo 2, con o sin vista previa).</span><span class="sxs-lookup"><span data-stu-id="40982-132">From the **Graph Mode** menu, select a *File to DV* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="40982-133">Haga clic en **Reproducir**.</span><span class="sxs-lookup"><span data-stu-id="40982-133">Click **Play**.</span></span>
4.  <span data-ttu-id="40982-134">Para grabar los datos en cinta, haga clic en **grabar**.</span><span class="sxs-lookup"><span data-stu-id="40982-134">To record the data to tape, click **Record**.</span></span>
5.  <span data-ttu-id="40982-135">Para detener la transmisión, haga clic en **detener**.</span><span class="sxs-lookup"><span data-stu-id="40982-135">To stop transmitting, click **Stop**.</span></span>

<span data-ttu-id="40982-136">Si el camascopio está en modo VTR, el usuario puede controlar el mecanismo de transporte a través de los botones de estilo VCR de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="40982-136">If the camcorder is in VTR mode, the user can control the transport mechanism through the application's VCR-style buttons.</span></span> <span data-ttu-id="40982-137">Para buscar la cinta, escriba el código de acceso de destino y haga clic en el botón Buscar.</span><span class="sxs-lookup"><span data-stu-id="40982-137">To seek the tape, enter the target timecode and click the seek button.</span></span>

<span data-ttu-id="40982-138">Para limitar la cantidad de datos que captura la aplicación, elija **capturar tamaño** en el menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="40982-138">To limit how much data the application captures, choose **Capture Size** from the **File** menu.</span></span>

<span data-ttu-id="40982-139">Para comprobar el formato de cinta (NTSC o PAL), seleccione **comprobar cinta** en el menú de **Opciones** .</span><span class="sxs-lookup"><span data-stu-id="40982-139">To check the tape format (NTSC or PAL), choose **Check Tape** from the **Options** menu.</span></span>

<span data-ttu-id="40982-140">Para cambiar el tamaño de la ventana de vista previa, elija **cambiar el tamaño de descodificación** en el menú **Opciones** .</span><span class="sxs-lookup"><span data-stu-id="40982-140">To change the size of the preview window, choose **Change Decode Size** from the **Options** menu.</span></span>

### <a name="programming-notes"></a><span data-ttu-id="40982-141">Notas de programación</span><span class="sxs-lookup"><span data-stu-id="40982-141">Programming Notes</span></span>

<span data-ttu-id="40982-142">El propósito principal de esta aplicación es mostrar cómo crear varios gráficos de captura y transmisión de DV.</span><span class="sxs-lookup"><span data-stu-id="40982-142">The main purpose of this application is to show how to build various DV capture and transmit graphs.</span></span>

### <a name="device-arrival-and-removal"></a><span data-ttu-id="40982-143">Llegada y eliminación de dispositivos</span><span class="sxs-lookup"><span data-stu-id="40982-143">Device Arrival and Removal</span></span>

<span data-ttu-id="40982-144">La aplicación controla la llegada y eliminación de dispositivos, con dos técnicas diferentes.</span><span class="sxs-lookup"><span data-stu-id="40982-144">The application handles device arrival and removal, using two different techniques.</span></span> <span data-ttu-id="40982-145">En el caso de la llegada del dispositivo, el bucle de mensajes de la aplicación responde a \_ los mensajes de WM DEVICECHANGE.</span><span class="sxs-lookup"><span data-stu-id="40982-145">For device arrival, the application's message loop responds to WM\_DEVICECHANGE messages.</span></span> <span data-ttu-id="40982-146">Para la eliminación del dispositivo, la aplicación responde a los eventos [**\_ \_ perdidos del dispositivo EC**](ec-device-lost.md) desde el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="40982-146">For device removal, the application responds to [**EC\_DEVICE\_LOST**](ec-device-lost.md) events from the filter graph manager.</span></span> <span data-ttu-id="40982-147">Cualquier enfoque funciona, aunque el \_ evento de dispositivo EC \_ perdido depende de la existencia del dispositivo en el gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="40982-147">Either approach works, although the EC\_DEVICE\_LOST event depends on the existence of the device in the filter graph.</span></span>

<span data-ttu-id="40982-148">La aplicación solo controla un dispositivo cada vez.</span><span class="sxs-lookup"><span data-stu-id="40982-148">The application only handles one device at a time.</span></span> <span data-ttu-id="40982-149">Si se quita el dispositivo actual, la aplicación busca otro dispositivo DV en el sistema.</span><span class="sxs-lookup"><span data-stu-id="40982-149">If the current device is removed, the application looks for another DV device on the system.</span></span>

<span data-ttu-id="40982-150">En algunas videocámaras DV, el usuario debe apagar el dispositivo cuando lo cambie entre el modo de cámara y el modo VTR, lo que desencadena un mensaje perdido del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40982-150">On some DV camcorders, the user must shut off the device when switching it between camera mode and VTR mode, which triggers a device-lost message.</span></span> <span data-ttu-id="40982-151">La aplicación responde habilitando o deshabilitando los comandos de menú correspondientes.</span><span class="sxs-lookup"><span data-stu-id="40982-151">The application responds by enabling or disabling the appropriate menu commands.</span></span> <span data-ttu-id="40982-152">Sin embargo, si el usuario alterna rápidamente entre los modos, es posible que la videocámara no genere un mensaje perdido por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40982-152">However, if the user toggles rapidly between modes, the camcorder might not generate a device-lost message.</span></span> <span data-ttu-id="40982-153">Puede forzar la actualización de los menús eligiendo el **modo de actualización** en el menú **Opciones** .</span><span class="sxs-lookup"><span data-stu-id="40982-153">You can force the menus to update by choosing **Refresh Mode** from the **Options** menu.</span></span> <span data-ttu-id="40982-154">Algunas videocámaras DV pueden alternar entre modos sin apagar, pero solo se envía un mensaje de pérdida del dispositivo cuando cambian al modo VTR.</span><span class="sxs-lookup"><span data-stu-id="40982-154">Some DV camcorders can toggle modes without shutting off, but send a device-lost message only when they switch to VTR mode.</span></span>

### <a name="device-control"></a><span data-ttu-id="40982-155">Control de dispositivos</span><span class="sxs-lookup"><span data-stu-id="40982-155">Device Control</span></span>

<span data-ttu-id="40982-156">La funcionalidad del botón **reproducir** y **grabar** depende del modo actual:</span><span class="sxs-lookup"><span data-stu-id="40982-156">The functionality of the **Play** and **Record** button depends on the current mode:</span></span>

-   <span data-ttu-id="40982-157">Versión preliminar: el gráfico de filtros se ejecuta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="40982-157">Preview: The filter graph runs automatically.</span></span> <span data-ttu-id="40982-158">El botón de **reproducción** inicia el transporte.</span><span class="sxs-lookup"><span data-stu-id="40982-158">The **Play** button starts the transport.</span></span>
-   <span data-ttu-id="40982-159">Capturar en archivo: el botón **grabar** ejecuta el gráfico y el botón de **reproducción** inicia el transporte.</span><span class="sxs-lookup"><span data-stu-id="40982-159">Capture to file: The **Record** button runs the graph, and the **Play** button starts the transport.</span></span>
-   <span data-ttu-id="40982-160">Transmitir al dispositivo: el botón **reproducir** ejecuta el gráfico y el botón **grabar** inicia el transporte.</span><span class="sxs-lookup"><span data-stu-id="40982-160">Transmit to device: The **Play** button runs the graph, and the **Record** button starts the transport.</span></span>

<span data-ttu-id="40982-161">La aplicación de ejemplo no realiza la captura con precisión de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="40982-161">The sample application does not perform frame-accurate capture.</span></span> <span data-ttu-id="40982-162">En varios puntos, la aplicación llama a la función **Sleep** para esperar a que el dispositivo responda.</span><span class="sxs-lookup"><span data-stu-id="40982-162">At various points, the application calls the **Sleep** function to wait for the device to respond.</span></span> <span data-ttu-id="40982-163">Las camcorders DV más recientes envían una notificación cuando cambia el estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40982-163">Newer DV camcorders send a notification when the state of the device changes.</span></span> <span data-ttu-id="40982-164">Es posible que los dispositivos más antiguos no admitan notificaciones; para los fines de un ejemplo, llamar a **Sleep** es una solución más sencilla.</span><span class="sxs-lookup"><span data-stu-id="40982-164">Older devices might not support notification; for the purposes of a sample, calling **Sleep** is a simpler solution.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="40982-165">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="40982-165">Downloading the Sample</span></span>

<span data-ttu-id="40982-166">Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="40982-166">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="40982-167">Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ raíz \] del SDK* \\ \\ multimedia \\ DirectShow \\ Capture \\ DVApp.</span><span class="sxs-lookup"><span data-stu-id="40982-167">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Capture\\DVApp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40982-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40982-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40982-169">Control de una videocámara DV</span><span class="sxs-lookup"><span data-stu-id="40982-169">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="40982-170">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="40982-170">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="40982-171">Ejemplos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="40982-171">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



