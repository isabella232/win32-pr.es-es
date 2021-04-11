---
title: Uso de receptores de archivos
description: Uso de receptores de archivos
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- Formato de sistemas avanzados (ASF), receptores de archivo
- ASF (formato de sistemas avanzados), receptores de archivo
- Advanced Systems Format (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- receptores, receptores de archivo
- receptores de archivos, acerca de
- receptores de archivos, crear
- receptores de archivos, detener
- receptores de archivos, Inicio
- receptores de archivos, cerrar
- receptores, estadísticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104149125"
---
# <a name="using-file-sinks"></a><span data-ttu-id="e14da-114">Uso de receptores de archivos</span><span class="sxs-lookup"><span data-stu-id="e14da-114">Using File Sinks</span></span>

<span data-ttu-id="e14da-115">En circunstancias normales, puede simplemente pasar el escritor a un nombre de archivo de salida con el método [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) y el objeto de escritor escribirá el archivo en el disco automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e14da-115">Under normal circumstances, you can simply pass the writer an output file name using the [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) method, and the writer object will write the file to disk automatically.</span></span> <span data-ttu-id="e14da-116">En este caso, el escritor crea y controla realmente un objeto de receptor de archivos de escritor que controla la escritura del archivo en el disco.</span><span class="sxs-lookup"><span data-stu-id="e14da-116">In this case, the writer is actually creating and controlling a writer file sink object that handles writing the file to disk.</span></span> <span data-ttu-id="e14da-117">Un objeto de receptor de archivo de escritor controla el flujo de datos desde el objeto de escritor a un único archivo.</span><span class="sxs-lookup"><span data-stu-id="e14da-117">A writer file sink object controls the flow of data from the writer object to a single file.</span></span>

<span data-ttu-id="e14da-118">Puede crear sus propios receptores de archivos para obtener más control sobre cómo el receptor escribe el archivo.</span><span class="sxs-lookup"><span data-stu-id="e14da-118">You can create your own file sinks to get more control over how the sink writes the file.</span></span> <span data-ttu-id="e14da-119">También puede tener acceso al receptor del archivo de escritura predeterminado creado por el escritor en respuesta a una llamada a **SetOutputFilename**.</span><span class="sxs-lookup"><span data-stu-id="e14da-119">You can also access the default writer file sink created by the writer in response to a call to **SetOutputFilename**.</span></span>

## <a name="creating-file-sinks"></a><span data-ttu-id="e14da-120">Crear receptores de archivo</span><span class="sxs-lookup"><span data-stu-id="e14da-120">Creating File Sinks</span></span>

<span data-ttu-id="e14da-121">Para crear un receptor de archivos y agregarlo al escritor, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e14da-121">To create a file sink and add it to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="e14da-122">Cree un nuevo receptor mediante una llamada a la función [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) .</span><span class="sxs-lookup"><span data-stu-id="e14da-122">Create a new sink by calling the [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) function.</span></span>
2.  <span data-ttu-id="e14da-123">Proporcione un nombre de archivo para el receptor mediante una llamada a [**IWMWriterFileSink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).</span><span class="sxs-lookup"><span data-stu-id="e14da-123">Supply a file name for the sink by calling [**IWMWriterFileSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).</span></span>
3.  <span data-ttu-id="e14da-124">Agregue el receptor de archivos al escritor llamando a [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).</span><span class="sxs-lookup"><span data-stu-id="e14da-124">Add the file sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).</span></span>
4.  <span data-ttu-id="e14da-125">Realizar la escritura de la manera habitual.</span><span class="sxs-lookup"><span data-stu-id="e14da-125">Perform writing in the usual way.</span></span>
5.  <span data-ttu-id="e14da-126">Una vez completada la escritura, el receptor cerrará automáticamente el archivo.</span><span class="sxs-lookup"><span data-stu-id="e14da-126">After writing is completed, the sink will close the file automatically.</span></span>

## <a name="stopping-and-starting-file-sinks"></a><span data-ttu-id="e14da-127">Detención e inicio de los receptores de archivo</span><span class="sxs-lookup"><span data-stu-id="e14da-127">Stopping and Starting File Sinks</span></span>

<span data-ttu-id="e14da-128">Una vez iniciada la operación de escritura, puede dejar de escribir en un receptor de archivos llamando a [**IWMWriterFileSink2:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).</span><span class="sxs-lookup"><span data-stu-id="e14da-128">After writing operations begin, you can stop writing to a file sink by calling [**IWMWriterFileSink2::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).</span></span>

<span data-ttu-id="e14da-129">Hay muchas razones posibles por las que podría querer dejar de escribir en un receptor.</span><span class="sxs-lookup"><span data-stu-id="e14da-129">There are many potential reasons why you would want to stop writing to a sink.</span></span> <span data-ttu-id="e14da-130">Por ejemplo, si va a grabar desde un origen en directo, es posible que solo esté interesado en parte del contenido.</span><span class="sxs-lookup"><span data-stu-id="e14da-130">For example, if you are recording from a live source, you may only be interested in some of the content.</span></span>

<span data-ttu-id="e14da-131">Puede reanudar la escritura en un receptor de archivos llamando a [**IWMWriterFileSink2:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start).</span><span class="sxs-lookup"><span data-stu-id="e14da-131">You can resume writing to a file sink by calling [**IWMWriterFileSink2::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start).</span></span> <span data-ttu-id="e14da-132">Las opciones **detener** e **iniciar** usan los tiempos de presentación para controlar aproximadamente el momento en que se ejecuta el comando.</span><span class="sxs-lookup"><span data-stu-id="e14da-132">Both **Stop** and **Start** use presentation times to control approximately when the command is executed.</span></span> <span data-ttu-id="e14da-133">Puede usar los métodos [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) para obtener más control sobre las horas de inicio y detención.</span><span class="sxs-lookup"><span data-stu-id="e14da-133">You can use the [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) methods to gain more control over start and stop times.</span></span>

## <a name="closing-file-sinks"></a><span data-ttu-id="e14da-134">Cerrar los receptores de archivo</span><span class="sxs-lookup"><span data-stu-id="e14da-134">Closing File Sinks</span></span>

<span data-ttu-id="e14da-135">Normalmente, un receptor de archivo se cierra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e14da-135">Normally, a file sink is closed automatically.</span></span> <span data-ttu-id="e14da-136">Si ha terminado de escribir en un receptor, pero la escritura de operaciones en otros receptores continúa, debe cerrar explícitamente el receptor para conservar los recursos.</span><span class="sxs-lookup"><span data-stu-id="e14da-136">If you are finished writing to a sink, but writing operations to other sinks are continuing, you should explicitly close the sink to conserve resources.</span></span> <span data-ttu-id="e14da-137">Para cerrar un receptor de archivos, llame a [**IWMWriterFileSink2:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span><span class="sxs-lookup"><span data-stu-id="e14da-137">To close a file sink, call [**IWMWriterFileSink2::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span></span>

## <a name="getting-sink-statistics"></a><span data-ttu-id="e14da-138">Obtención de estadísticas de receptor</span><span class="sxs-lookup"><span data-stu-id="e14da-138">Getting Sink Statistics</span></span>

<span data-ttu-id="e14da-139">Puede obtener el tamaño de archivo y la duración de un receptor abierto llamando a [**IWMWriterFileSink2:: GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) y [**IWMWriterFileSink2:: GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e14da-139">You can get the file size and duration for an open sink by calling [**IWMWriterFileSink2::GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) and [**IWMWriterFileSink2::GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e14da-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e14da-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e14da-141">**Interfaz IWMWriterFileSink**</span><span class="sxs-lookup"><span data-stu-id="e14da-141">**IWMWriterFileSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[<span data-ttu-id="e14da-142">**Interfaz IWMWriterFileSink2**</span><span class="sxs-lookup"><span data-stu-id="e14da-142">**IWMWriterFileSink2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[<span data-ttu-id="e14da-143">**Interfaz IWMWriterFileSink3**</span><span class="sxs-lookup"><span data-stu-id="e14da-143">**IWMWriterFileSink3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[<span data-ttu-id="e14da-144">**Objeto receptor de archivos de Writer**</span><span class="sxs-lookup"><span data-stu-id="e14da-144">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="e14da-145">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="e14da-145">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




