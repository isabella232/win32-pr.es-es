---
title: Escribir archivos ASF
description: Escribir archivos ASF
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- SDK de Windows Media Format, escribir archivos ASF
- SDK de Windows Media Format, crear archivos ASF
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), escribir archivos
- ASF (formato de sistemas avanzados), escribir archivos
- Advanced Systems Format (ASF), crear archivos
- ASF (formato de sistemas avanzados), crear archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c13c1af0d3699c89d26f007e00675ea563639c4e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904404"
---
# <a name="writing-asf-files"></a><span data-ttu-id="12dba-110">Escribir archivos ASF</span><span class="sxs-lookup"><span data-stu-id="12dba-110">Writing ASF Files</span></span>

<span data-ttu-id="12dba-111">Puede usar el objeto escritor del SDK de Windows Media Format para crear archivos ASF a partir de datos multimedia digitales.</span><span class="sxs-lookup"><span data-stu-id="12dba-111">You can use the writer object of the Windows Media Format SDK to create ASF files from digital media data.</span></span> <span data-ttu-id="12dba-112">Para crear una instancia del objeto de escritor, llame a la función [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) .</span><span class="sxs-lookup"><span data-stu-id="12dba-112">To create an instance of the writer object, call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="12dba-113">El objeto escritor coordina la funcionalidad de una serie de componentes, incluidos los códecs, que son externos al SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="12dba-113">The writer object coordinates the functionality of a number of components, including codecs, which are external to the Windows Media Format SDK.</span></span>

<span data-ttu-id="12dba-114">La funcionalidad básica del objeto escritor se puede desglosar en los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="12dba-114">The basic functionality of the writer object can be broken down into the following steps.</span></span> <span data-ttu-id="12dba-115">En estos pasos, "la aplicación" hace referencia al programa que se escribe con el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="12dba-115">In these steps, "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="12dba-116">La aplicación proporciona al escritor un perfil que se utilizará para crear el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="12dba-116">The application supplies the writer with a profile to use in creating the ASF file.</span></span> <span data-ttu-id="12dba-117">Cuando el escritor carga los datos del perfil, asigna un número de entrada a cada conexión del perfil.</span><span class="sxs-lookup"><span data-stu-id="12dba-117">When the writer loads the profile data, it assigns an input number to each connection of the profile.</span></span>
2.  <span data-ttu-id="12dba-118">La aplicación proporciona al escritor un nombre de archivo de salida para el archivo que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="12dba-118">The application supplies the writer with an output file name for the file to be written.</span></span> <span data-ttu-id="12dba-119">El escritor crea un objeto de receptor del archivo de escritura para administrar la entrada y la creación del archivo.</span><span class="sxs-lookup"><span data-stu-id="12dba-119">The writer creates a writer file sink object to manage the file creation and input.</span></span> <span data-ttu-id="12dba-120">Para obtener más información, consulte [objeto de receptor del archivo de escritura](writer-file-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="12dba-120">For more information, see [Writer File Sink Object](writer-file-sink-object.md).</span></span>
3.  <span data-ttu-id="12dba-121">El escritor crea un encabezado para el nuevo archivo basándose en la información del perfil.</span><span class="sxs-lookup"><span data-stu-id="12dba-121">The writer creates a header for the new file based on information in the profile.</span></span>
4.  <span data-ttu-id="12dba-122">La aplicación pasa muestras sin comprimir al escritor.</span><span class="sxs-lookup"><span data-stu-id="12dba-122">The application passes uncompressed samples to the writer.</span></span> <span data-ttu-id="12dba-123">Las muestras se pasan de una en una en los búferes encapsulados en los objetos de búfer.</span><span class="sxs-lookup"><span data-stu-id="12dba-123">Samples are passed one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="12dba-124">La aplicación debe pasar ejemplos para cada flujo simultáneamente para que el escritor reciba todos los ejemplos en el orden en tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="12dba-124">The application should pass samples for each stream concurrently so that the writer receives all samples in presentation-time order.</span></span>
5.  <span data-ttu-id="12dba-125">El escritor pasa los ejemplos al códec adecuado para la compresión.</span><span class="sxs-lookup"><span data-stu-id="12dba-125">The writer passes the samples to the appropriate codec for compression.</span></span> <span data-ttu-id="12dba-126">Cuando el escritor recibe los ejemplos comprimidos, los intercala con ejemplos de las otras secuencias para que los ejemplos se incluyan en el archivo en el orden temporal de la presentación, independientemente de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="12dba-126">When the writer receives the compressed samples, it interleaves them with samples from the other streams so that samples go into the file in presentation time order irrespective of stream.</span></span> <span data-ttu-id="12dba-127">Los datos de ejemplo se convierten en paquetes y se escriben en la sección de datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="12dba-127">The sample data is then made into packets and written to the data section of the file.</span></span>
6.  <span data-ttu-id="12dba-128">Cuando se procesan todos los ejemplos, el sistema de escritura puede Agregar un índice al archivo para mejorar el rendimiento de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="12dba-128">When all samples are processed, the writer can add an index to the file to enhance seeking performance.</span></span>

<span data-ttu-id="12dba-129">Estos pasos se muestran en la aplicación de ejemplo WMStats, entre otros.</span><span class="sxs-lookup"><span data-stu-id="12dba-129">These steps are illustrated in the WMStats sample application, among others.</span></span> <span data-ttu-id="12dba-130">Para obtener más información, vea [aplicaciones de ejemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="12dba-130">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="12dba-131">El escritor también admite una funcionalidad más avanzada, lo que le permite hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="12dba-131">The writer also supports more advanced functionality, enabling you to do the following:</span></span>

-   <span data-ttu-id="12dba-132">Edite los metadatos en el encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="12dba-132">Edit metadata in the header of the file.</span></span>
-   <span data-ttu-id="12dba-133">Escribir muestras precomprimidas.</span><span class="sxs-lookup"><span data-stu-id="12dba-133">Write precompressed samples.</span></span>
-   <span data-ttu-id="12dba-134">Escribir en receptores de red para transmitir datos en directo.</span><span class="sxs-lookup"><span data-stu-id="12dba-134">Write to network sinks for streaming live data.</span></span>
-   <span data-ttu-id="12dba-135">Escribir en los receptores de archivos para opciones avanzadas de control de archivos.</span><span class="sxs-lookup"><span data-stu-id="12dba-135">Write to file sinks for advanced file control options.</span></span>
-   <span data-ttu-id="12dba-136">Escriba los receptores de envío para la distribución en los servidores que entregarán contenido a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="12dba-136">Write to push sinks for distribution to servers that will deliver content to end users.</span></span>
-   <span data-ttu-id="12dba-137">Proporcione ejemplos de postview para la comprobación de la salida.</span><span class="sxs-lookup"><span data-stu-id="12dba-137">Deliver postview samples for verification of output.</span></span>
-   <span data-ttu-id="12dba-138">Entregue las estadísticas de rendimiento del escritor.</span><span class="sxs-lookup"><span data-stu-id="12dba-138">Deliver writer-performance statistics.</span></span>

<span data-ttu-id="12dba-139">En las secciones siguientes se describe detalladamente el uso del objeto de escritura.</span><span class="sxs-lookup"><span data-stu-id="12dba-139">The following sections describe the use of the writer object in detail.</span></span>



| <span data-ttu-id="12dba-140">Sección</span><span class="sxs-lookup"><span data-stu-id="12dba-140">Section</span></span>                                                                    | <span data-ttu-id="12dba-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="12dba-141">Description</span></span>                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12dba-142">Para el uso de perfiles con Writer</span><span class="sxs-lookup"><span data-stu-id="12dba-142">To Use Profiles with the Writer</span></span>](to-use-profiles-with-the-writer.md)     | <span data-ttu-id="12dba-143">Describe cómo especificar un perfil para usarlo con el escritor.</span><span class="sxs-lookup"><span data-stu-id="12dba-143">Describes how to specify a profile to use with the writer.</span></span>                                             |
| [<span data-ttu-id="12dba-144">Trabajar con entradas</span><span class="sxs-lookup"><span data-stu-id="12dba-144">Working with Inputs</span></span>](working-with-inputs.md)                             | <span data-ttu-id="12dba-145">Describe cómo identificar y configurar los valores de entrada en el escritor.</span><span class="sxs-lookup"><span data-stu-id="12dba-145">Describes how to identify and configure the input settings in the writer.</span></span>                              |
| [<span data-ttu-id="12dba-146">Para editar los metadatos con el escritor</span><span class="sxs-lookup"><span data-stu-id="12dba-146">To Edit Metadata with the Writer</span></span>](to-edit-metadata-with-the-writer.md)   | <span data-ttu-id="12dba-147">Describe cómo utilizar el escritor para editar los metadatos de un archivo nuevo.</span><span class="sxs-lookup"><span data-stu-id="12dba-147">Describes how to use the writer to edit metadata for a new file.</span></span>                                       |
| [<span data-ttu-id="12dba-148">Para escribir ejemplos</span><span class="sxs-lookup"><span data-stu-id="12dba-148">To Write Samples</span></span>](to-write-samples.md)                                   | <span data-ttu-id="12dba-149">Describe cómo pasar ejemplos al escritor.</span><span class="sxs-lookup"><span data-stu-id="12dba-149">Describes how to pass samples to the writer.</span></span>                                                           |
| [<span data-ttu-id="12dba-150">Configuración de las extensiones de unidad de datos</span><span class="sxs-lookup"><span data-stu-id="12dba-150">Setting Data Unit Extensions</span></span>](setting-data-unit-extensions.md)           | <span data-ttu-id="12dba-151">Describe cómo agregar datos extendidos a ejemplos.</span><span class="sxs-lookup"><span data-stu-id="12dba-151">Describes how to add extended data to samples.</span></span>                                                         |
| [<span data-ttu-id="12dba-152">Escribir ejemplos comprimidos</span><span class="sxs-lookup"><span data-stu-id="12dba-152">Writing Compressed Samples</span></span>](writing-compressed-samples.md)               | <span data-ttu-id="12dba-153">Describe cómo pasar ejemplos previamente comprimidos al escritor.</span><span class="sxs-lookup"><span data-stu-id="12dba-153">Describes how to pass pre-compressed samples to the writer.</span></span>                                            |
| [<span data-ttu-id="12dba-154">Escribir secuencias de imagen</span><span class="sxs-lookup"><span data-stu-id="12dba-154">Writing Image Streams</span></span>](writing-image-streams.md)                         | <span data-ttu-id="12dba-155">Describe cómo configurar una entrada para un flujo de imagen.</span><span class="sxs-lookup"><span data-stu-id="12dba-155">Describes how to configure an input for an image stream.</span></span>                                               |
| [<span data-ttu-id="12dba-156">Escribir ejemplos de imagen de vídeo</span><span class="sxs-lookup"><span data-stu-id="12dba-156">Writing Video Image Samples</span></span>](writing-video-image-samples.md)             | <span data-ttu-id="12dba-157">Describe cómo configurar los ejemplos de imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="12dba-157">Describes how to configure Video Image samples.</span></span>                                                        |
| [<span data-ttu-id="12dba-158">Escribir secuencias de velocidad de bits variable</span><span class="sxs-lookup"><span data-stu-id="12dba-158">Writing Variable Bit Rate Streams</span></span>](writing-variable-bit-rate-streams.md) | <span data-ttu-id="12dba-159">Describe cómo escribir secuencias de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="12dba-159">Describes how to write variable bit rate (VBR) streams.</span></span>                                                |
| [<span data-ttu-id="12dba-160">Uso de la codificación de Two-Pass</span><span class="sxs-lookup"><span data-stu-id="12dba-160">Using Two-Pass Encoding</span></span>](using-two-pass-encoding.md)                     | <span data-ttu-id="12dba-161">Describe cómo hacer que el códec realice una fase preliminar antes de escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="12dba-161">Describes how to have the codec perform a preliminary pass before writing the file.</span></span>                    |
| [<span data-ttu-id="12dba-162">Para forzar la inserción de Key-Frame</span><span class="sxs-lookup"><span data-stu-id="12dba-162">To Force Key-Frame Insertion</span></span>](to-force-key-frame-insertion.md)           | <span data-ttu-id="12dba-163">Describe cómo forzar manualmente el códec para codificar un ejemplo como un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="12dba-163">Describes how to manually force the codec to encode a sample as a key frame.</span></span>                           |
| [<span data-ttu-id="12dba-164">Para administrar la latencia del escritor</span><span class="sxs-lookup"><span data-stu-id="12dba-164">To Manage Writer Latency</span></span>](to-manage-writer-latency.md)                   | <span data-ttu-id="12dba-165">Describe cómo minimizar el tiempo que tarda el escritor en procesar muestras en un archivo o receptor de salida.</span><span class="sxs-lookup"><span data-stu-id="12dba-165">Describes how to minimize the time it takes the writer to process samples into an output file or sink.</span></span> |
| [<span data-ttu-id="12dba-166">Trabajar con receptores de escritor</span><span class="sxs-lookup"><span data-stu-id="12dba-166">Working with Writer Sinks</span></span>](working-with-writer-sinks.md)                 | <span data-ttu-id="12dba-167">Describe cómo usar receptores de escritor para enviar el contenido a archivos o ubicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="12dba-167">Describes how to use writer sinks to deliver your content to files or network locations.</span></span>               |
| [<span data-ttu-id="12dba-168">Para obtener estadísticas del escritor</span><span class="sxs-lookup"><span data-stu-id="12dba-168">To Get Writer Statistics</span></span>](to-get-writer-statistics.md)                   | <span data-ttu-id="12dba-169">Describe cómo obtener estadísticas para el escritor.</span><span class="sxs-lookup"><span data-stu-id="12dba-169">Describes how to get statistics for the writer.</span></span>                                                        |
| [<span data-ttu-id="12dba-170">Para usar la vista previa del escritor</span><span class="sxs-lookup"><span data-stu-id="12dba-170">To Use Writer Postview</span></span>](to-use-writer-postview.md)                       | <span data-ttu-id="12dba-171">Describe cómo obtener ejemplos sin comprimir mientras escribe un archivo para su comprobación.</span><span class="sxs-lookup"><span data-stu-id="12dba-171">Describes how to get uncompressed samples as you write a file for verification.</span></span>                        |



 

## <a name="related-topics"></a><span data-ttu-id="12dba-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12dba-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12dba-173">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="12dba-173">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="12dba-174">**Objeto receptor de archivos de Writer**</span><span class="sxs-lookup"><span data-stu-id="12dba-174">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="12dba-175">**Objeto de receptor de red del escritor**</span><span class="sxs-lookup"><span data-stu-id="12dba-175">**Writer Network Sink Object**</span></span>](writer-network-sink-object.md)
</dt> <dt>

[<span data-ttu-id="12dba-176">**Objeto de Writer**</span><span class="sxs-lookup"><span data-stu-id="12dba-176">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




