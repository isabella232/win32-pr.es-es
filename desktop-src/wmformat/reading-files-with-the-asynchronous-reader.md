---
title: Leer archivos con el lector asincrónico
description: Leer archivos con el lector asincrónico
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- SDK de Windows Media Format, leer archivos
- SDK de Windows Media Format, lectores asincrónicos
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), leer archivos
- ASF (formato de sistemas avanzados), lectura de archivos
- lectores asincrónicos, interfaz IWMReaderCallback
- IWMReaderCallback, lectores asincrónicos
- lectores asincrónicos, leer archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420244"
---
# <a name="reading-files-with-the-asynchronous-reader"></a><span data-ttu-id="ccec8-112">Leer archivos con el lector asincrónico</span><span class="sxs-lookup"><span data-stu-id="ccec8-112">Reading Files with the Asynchronous Reader</span></span>

<span data-ttu-id="ccec8-113">El lector asincrónico lee el contenido de los archivos ASF mediante varios subprocesos y llamadas asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="ccec8-113">The asynchronous reader reads the content from ASF files using multiple threads and asynchronous calls.</span></span> <span data-ttu-id="ccec8-114">Las características admitidas por el lector asincrónico hacen que sea adecuado para las aplicaciones que presentan contenido a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="ccec8-114">The features supported by the asynchronous reader make it well suited for applications that render content to end users.</span></span>

<span data-ttu-id="ccec8-115">La funcionalidad más básica del objeto lector se puede desglosar en los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ccec8-115">The most basic functionality of the reader object can be broken down into the following steps.</span></span> <span data-ttu-id="ccec8-116">En estos pasos "la aplicación" hace referencia al programa que se escribe con el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="ccec8-116">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="ccec8-117">La aplicación implementa la interfaz [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) para controlar los mensajes del lector.</span><span class="sxs-lookup"><span data-stu-id="ccec8-117">The application implements the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) interface to handle messages from the reader.</span></span> <span data-ttu-id="ccec8-118">Esto incluye dos métodos de devolución de llamada: **Alstatus**, que recibe mensajes relacionados con el estado de diversos aspectos del lector y el **ejemplo**, que recibe muestras sin comprimir del lector.</span><span class="sxs-lookup"><span data-stu-id="ccec8-118">This includes two callback methods: **OnStatus**, which receives messages relating to the status of various aspects of the reader and **OnSample**, which receives uncompressed samples from the reader.</span></span>
2.  <span data-ttu-id="ccec8-119">La aplicación pasa al lector el nombre de un archivo que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="ccec8-119">The application passes to the reader the name of a file to read.</span></span> <span data-ttu-id="ccec8-120">Cuando el lector abre el archivo, asigna un número de salida a cada flujo.</span><span class="sxs-lookup"><span data-stu-id="ccec8-120">When the reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="ccec8-121">Si el archivo usa exclusión mutua, el lector asigna una salida única para todos los flujos mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="ccec8-121">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
3.  <span data-ttu-id="ccec8-122">La aplicación obtiene información sobre la configuración de las distintas salidas del lector.</span><span class="sxs-lookup"><span data-stu-id="ccec8-122">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="ccec8-123">La información recopilada permitirá a la aplicación representar correctamente los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="ccec8-123">The information gathered will enable the application to properly render media samples.</span></span>
4.  <span data-ttu-id="ccec8-124">La aplicación indica al lector que empiece a leer los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="ccec8-124">The application instructs the reader to begin reading data from the file.</span></span> <span data-ttu-id="ccec8-125">El lector comienza a entregar muestras sin comprimir a la devolución de llamada de **ejemplo** de una en una en los búferes encapsulados en los objetos de búfer.</span><span class="sxs-lookup"><span data-stu-id="ccec8-125">The reader begins delivering uncompressed samples to the **OnSample** callback one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="ccec8-126">Los ejemplos proporcionados por el lector están en el orden en tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="ccec8-126">The samples delivered by the reader are in presentation-time order.</span></span> <span data-ttu-id="ccec8-127">El lector seguirá entregando muestras hasta que la aplicación la detenga o hasta que se alcance el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="ccec8-127">The reader will continue delivering samples until stopped by the application or until the end of the file is reached.</span></span>
5.  <span data-ttu-id="ccec8-128">La aplicación es responsable de representar los datos después de que los entregue el lector.</span><span class="sxs-lookup"><span data-stu-id="ccec8-128">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="ccec8-129">El SDK de Windows Media Format no proporciona ninguna rutina de representación.</span><span class="sxs-lookup"><span data-stu-id="ccec8-129">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="ccec8-130">Normalmente, las aplicaciones usarán otros SDK para representar datos, como Microsoft DirectX® SDK o las funciones multimedia del SDK de la plataforma Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ccec8-130">Typically, applications will use other SDKs to render data, such as the Microsoft DirectX® SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>
6.  <span data-ttu-id="ccec8-131">Cuando se completa la lectura, la aplicación indica al lector que cierre el archivo.</span><span class="sxs-lookup"><span data-stu-id="ccec8-131">When reading is complete, the application instructs the reader to close the file.</span></span>

<span data-ttu-id="ccec8-132">Estos pasos se muestran en la aplicación de ejemplo AudioPlayer, entre otros.</span><span class="sxs-lookup"><span data-stu-id="ccec8-132">These steps are illustrated in the AudioPlayer sample application, among others.</span></span> <span data-ttu-id="ccec8-133">Para obtener más información, vea [aplicaciones de ejemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="ccec8-133">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="ccec8-134">El lector también admite una funcionalidad más avanzada.</span><span class="sxs-lookup"><span data-stu-id="ccec8-134">The reader also supports more advanced functionality.</span></span> <span data-ttu-id="ccec8-135">El lector le permite hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ccec8-135">The reader enables you to do the following:</span></span>

-   <span data-ttu-id="ccec8-136">Pausar la reproducción de un archivo.</span><span class="sxs-lookup"><span data-stu-id="ccec8-136">Pause playback of a file.</span></span>
-   <span data-ttu-id="ccec8-137">Recupera las estadísticas de rendimiento del lector.</span><span class="sxs-lookup"><span data-stu-id="ccec8-137">Retrieve reader performance statistics.</span></span>
-   <span data-ttu-id="ccec8-138">Control de la selección de flujo para flujos mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="ccec8-138">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="ccec8-139">Asignación manual de búferes para la salida.</span><span class="sxs-lookup"><span data-stu-id="ccec8-139">Manually allocate buffers for output.</span></span>
-   <span data-ttu-id="ccec8-140">Proporcione su propio reloj.</span><span class="sxs-lookup"><span data-stu-id="ccec8-140">Provide your own clock.</span></span>
-   <span data-ttu-id="ccec8-141">Recuperar el estado de las operaciones de archivo (almacenamiento en búfer, descarga o guardado).</span><span class="sxs-lookup"><span data-stu-id="ccec8-141">Retrieve the status of file operations (buffering, download, or save).</span></span>
-   <span data-ttu-id="ccec8-142">Abra un archivo mediante la interfaz COM estándar, **IStream**.</span><span class="sxs-lookup"><span data-stu-id="ccec8-142">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="ccec8-143">Buscar puntos específicos en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ccec8-143">Seek to specific points in an ASF file.</span></span>
-   <span data-ttu-id="ccec8-144">Leer los datos de perfil del encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="ccec8-144">Read profile data from the header of the file.</span></span>

<span data-ttu-id="ccec8-145">En las secciones siguientes se describe detalladamente el uso del objeto Reader.</span><span class="sxs-lookup"><span data-stu-id="ccec8-145">The following sections describe the use of the reader object in detail.</span></span>

-   [<span data-ttu-id="ccec8-146">Para implementar mensajes de lector en la devolución de llamada de estado</span><span class="sxs-lookup"><span data-stu-id="ccec8-146">To Implement Reader Messages in the OnStatus Callback</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [<span data-ttu-id="ccec8-147">Para implementar la devolución de llamada de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ccec8-147">To Implement the OnSample Callback</span></span>](to-implement-the-onsample-callback.md)
-   [<span data-ttu-id="ccec8-148">Para crear un lector y abrir un archivo</span><span class="sxs-lookup"><span data-stu-id="ccec8-148">To Create a Reader and Open a File</span></span>](to-create-a-reader-and-open-a-file.md)
-   [<span data-ttu-id="ccec8-149">Para recuperar ejemplos de medios con el lector asincrónico</span><span class="sxs-lookup"><span data-stu-id="ccec8-149">To Retrieve Media Samples with the Asynchronous Reader</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [<span data-ttu-id="ccec8-150">Para buscar por tiempo mediante el lector asincrónico</span><span class="sxs-lookup"><span data-stu-id="ccec8-150">To Seek By Time Using the Asynchronous Reader</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="ccec8-151">Para buscar por número de marco mediante el lector asincrónico</span><span class="sxs-lookup"><span data-stu-id="ccec8-151">To Seek By Frame Number Using the Asynchronous Reader</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="ccec8-152">Para buscar por el código de tiempo de SMPTE mediante el lector asincrónico</span><span class="sxs-lookup"><span data-stu-id="ccec8-152">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="ccec8-153">Para buscar marcadores</span><span class="sxs-lookup"><span data-stu-id="ccec8-153">To Seek to Markers</span></span>](to-seek-to-markers.md)
-   [<span data-ttu-id="ccec8-154">Para pausar o detener la reproducción</span><span class="sxs-lookup"><span data-stu-id="ccec8-154">To Pause or Stop Playback</span></span>](to-pause-or-stop-playback.md)
-   [<span data-ttu-id="ccec8-155">Para obtener las estadísticas de rendimiento del lector</span><span class="sxs-lookup"><span data-stu-id="ccec8-155">To Get Reader Performance Statistics</span></span>](to-get-reader-performance-statistics.md)
-   [<span data-ttu-id="ccec8-156">Para usar la selección de flujo manual</span><span class="sxs-lookup"><span data-stu-id="ccec8-156">To Use Manual Stream Selection</span></span>](to-use-manual-stream-selection.md)
-   [<span data-ttu-id="ccec8-157">Para proporcionar ejemplos comprimidos con el lector asincrónico</span><span class="sxs-lookup"><span data-stu-id="ccec8-157">To Deliver Compressed Samples with the Asynchronous Reader</span></span>](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a><span data-ttu-id="ccec8-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ccec8-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccec8-159">**Leer archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="ccec8-159">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="ccec8-160">**Objeto del lector**</span><span class="sxs-lookup"><span data-stu-id="ccec8-160">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




