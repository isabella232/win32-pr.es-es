---
title: Leer archivos con el lector sincrónico
description: Leer archivos con el lector sincrónico
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- SDK de Windows Media Format, leer archivos
- SDK de Windows Media Format, lectores sincrónicos
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- Advanced Systems Format (ASF), leer archivos
- ASF (formato de sistemas avanzados), lectura de archivos
- lectores sincrónicos, interfaz IWMReaderCallback
- IWMReaderCallback, lectores sincrónicos
- lectores sincrónicos, leer archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420243"
---
# <a name="reading-files-with-the-synchronous-reader"></a><span data-ttu-id="8ea6c-112">Leer archivos con el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="8ea6c-112">Reading Files with the Synchronous Reader</span></span>

<span data-ttu-id="8ea6c-113">Puede usar el lector sincrónico para leer un archivo ASF mediante llamadas sincrónicas en lugar de los métodos asincrónicos en el objeto Reader.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-113">You can use the synchronous reader to read an ASF file using synchronous calls instead of the asynchronous methods in the reader object.</span></span> <span data-ttu-id="8ea6c-114">El uso de llamadas sincrónicas reduce el número de subprocesos necesarios para leer un archivo.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-114">Using synchronous calls reduces the number of threads required to read a file.</span></span> <span data-ttu-id="8ea6c-115">El lector asincrónico usa varios subprocesos para el procesamiento de secuencias.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-115">The asynchronous reader uses multiple threads for processing streams.</span></span> <span data-ttu-id="8ea6c-116">En el caso de los archivos con varias secuencias, el número de subprocesos utilizados puede llegar a ser muy grande.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-116">For files with multiple streams, the number of threads used can become very large.</span></span> <span data-ttu-id="8ea6c-117">El lector sincrónico solo usa un subproceso.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-117">The synchronous reader uses only one thread.</span></span>

<span data-ttu-id="8ea6c-118">El lector sincrónico se diseñó para satisfacer las necesidades de creación de contenido y aplicaciones de edición de archivos.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-118">The synchronous reader was designed to meet the needs of content creation and file editing applications.</span></span> <span data-ttu-id="8ea6c-119">Puede usar el lector sincrónico para otras aplicaciones, pero su funcionalidad es limitada.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-119">You can use the synchronous reader for other applications, but its functionality is limited.</span></span>

<span data-ttu-id="8ea6c-120">El lector sincrónico puede abrir archivos que son locales o archivos en una red mediante el nombre de la ruta de acceso UNC (por ejemplo, " \\ \\ someshare \\ somedirectory \\ somefile. WMV").</span><span class="sxs-lookup"><span data-stu-id="8ea6c-120">The synchronous reader can open files that are local, or files on a network using the UNC path name (such as "\\\\someshare\\somedirectory\\somefile.wmv").</span></span> <span data-ttu-id="8ea6c-121">No se pueden transmitir archivos al lector sincrónico ni abrir archivos desde una ubicación de Internet.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-121">You cannot stream files to the synchronous reader, or open files from an Internet location.</span></span> <span data-ttu-id="8ea6c-122">El lector sincrónico también proporciona compatibilidad para utilizar la interfaz com de **IStream** como origen.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-122">The synchronous reader also provides support for using the **IStream** COM interface as a source.</span></span>

<span data-ttu-id="8ea6c-123">El lector sincrónico proporciona más versatilidad para recuperar ejemplos de un archivo ASF que el lector asincrónico.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-123">The synchronous reader provides more versatility for retrieving samples from an ASF file than the asynchronous reader.</span></span> <span data-ttu-id="8ea6c-124">El lector sincrónico puede proporcionar ejemplos por número de secuencia y por salida.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-124">The synchronous reader can deliver samples by stream number as well as by output.</span></span> <span data-ttu-id="8ea6c-125">Los ejemplos proporcionados por el número de secuencia se pueden comprimir o descomprimir.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-125">Samples delivered by stream number can be compressed or uncompressed.</span></span> <span data-ttu-id="8ea6c-126">El lector sincrónico también puede cambiar entre la entrega comprimida y sin comprimir durante la reproducción. Esta característica se conoce como "edición rápida".</span><span class="sxs-lookup"><span data-stu-id="8ea6c-126">The synchronous reader can also switch between compressed and uncompressed delivery during playback; this feature is known as "fast editing."</span></span> <span data-ttu-id="8ea6c-127">Esta característica permite a una aplicación de edición leer contenido basado en Windows Media y pasarlo directamente al escritor hasta que se alcance un fotograma deseado.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-127">This feature enables an editing application to read Windows Media-based content and pass it directly through to the writer until a desired frame is reached.</span></span> <span data-ttu-id="8ea6c-128">En ese momento, la aplicación puede indicar al lector que comience a entregar contenido sin comprimir, que la aplicación puede modificar y pasar al escritor para volver a comprimirlo.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-128">At that point the application can tell the reader to start delivering uncompressed content, which the application can then modify and pass to the writer for recompression.</span></span> <span data-ttu-id="8ea6c-129">Cuando la aplicación haya terminado de modificar los fotogramas especificados, puede indicar al lector que empiece a entregar fotogramas comprimidos de nuevo.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-129">When the application has finished modifying the specified frames, it can tell the reader to start delivering compressed frames again.</span></span>

<span data-ttu-id="8ea6c-130">La funcionalidad más básica del objeto lector sincrónico se puede desglosar en los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-130">The most basic functionality of the synchronous reader object can be broken down into the following steps.</span></span> <span data-ttu-id="8ea6c-131">En estos pasos "la aplicación" hace referencia al programa que se escribe con el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-131">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="8ea6c-132">La aplicación pasa al lector sincrónico el nombre de un archivo que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-132">The application passes to the synchronous reader the name of a file to read.</span></span> <span data-ttu-id="8ea6c-133">Cuando el lector sincrónico abre el archivo, asigna un número de salida a cada flujo.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-133">When the synchronous reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="8ea6c-134">Si el archivo usa exclusión mutua, el lector asigna una salida única para todos los flujos mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-134">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
2.  <span data-ttu-id="8ea6c-135">La aplicación obtiene información sobre la configuración de las distintas salidas del lector.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-135">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="8ea6c-136">La información recopilada permitirá a la aplicación representar correctamente los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-136">The information gathered will enable the application to properly render media samples.</span></span>
3.  <span data-ttu-id="8ea6c-137">La aplicación comienza a solicitar muestras, de una en una, del lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-137">The application begins requesting samples, one at a time, from the synchronous reader.</span></span> <span data-ttu-id="8ea6c-138">El lector sincrónico entrega cada ejemplo en un objeto de búfer para el que entrega la interfaz [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .</span><span class="sxs-lookup"><span data-stu-id="8ea6c-138">The synchronous reader delivers each sample in a buffer object for which it delivers the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface.</span></span>
4.  <span data-ttu-id="8ea6c-139">La aplicación es responsable de representar los datos después de que los entregue el lector.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-139">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="8ea6c-140">El SDK de Windows Media Format no proporciona ninguna rutina de representación.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-140">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="8ea6c-141">Normalmente, las aplicaciones usarán otros SDK para representar datos, como el SDK de Microsoft Direct X o las funciones multimedia del SDK de la plataforma Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-141">Typically, applications will use other SDKs to render data, such as the Microsoft Direct X SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>

<span data-ttu-id="8ea6c-142">Estos pasos se ilustran en la aplicación de ejemplo WMSyncReader.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-142">These steps are illustrated in the WMSyncReader sample application.</span></span> <span data-ttu-id="8ea6c-143">Para obtener más información, vea [aplicaciones de ejemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="8ea6c-143">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="8ea6c-144">El lector sincrónico también admite una funcionalidad más avanzada.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-144">The synchronous reader also supports more advanced functionality.</span></span> <span data-ttu-id="8ea6c-145">El lector sincrónico le permite hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8ea6c-145">The synchronous reader enables you to do the following:</span></span>

-   <span data-ttu-id="8ea6c-146">Especifique un intervalo de muestras para recuperar por hora o por número de marco.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-146">Specify a range of samples to retrieve by time or by frame number.</span></span>
-   <span data-ttu-id="8ea6c-147">Control de la selección de flujo para flujos mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-147">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="8ea6c-148">Abra un archivo mediante la interfaz COM estándar, **IStream**.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-148">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="8ea6c-149">Leer los datos de perfil del encabezado de archivo.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-149">Read profile data from the file header.</span></span>
-   <span data-ttu-id="8ea6c-150">Leer metadatos del encabezado de archivo.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-150">Read metadata from the file header.</span></span>
-   <span data-ttu-id="8ea6c-151">Cambiar entre los ejemplos de flujo y salida durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-151">Switch between stream and output samples during playback.</span></span>
-   <span data-ttu-id="8ea6c-152">Cambiar entre los ejemplos de secuencias comprimidas y sin comprimir durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-152">Switch between compressed and uncompressed stream samples during playback.</span></span>

<span data-ttu-id="8ea6c-153">En las secciones siguientes se describe detalladamente el uso del objeto de lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-153">The following sections describe the use of the synchronous reader object in detail.</span></span>

-   [<span data-ttu-id="8ea6c-154">Para crear un lector sincrónico y abrir un archivo</span><span class="sxs-lookup"><span data-stu-id="8ea6c-154">To Create a Synchronous Reader and Open a File</span></span>](to-create-a-synchronous-reader-and-open-a-file.md)
-   [<span data-ttu-id="8ea6c-155">Para buscar números de secuencia y números de salida</span><span class="sxs-lookup"><span data-stu-id="8ea6c-155">To Find Stream Numbers and Output Numbers</span></span>](to-find-stream-numbers-and-output-numbers.md)
-   [<span data-ttu-id="8ea6c-156">Para recuperar ejemplos de medios con el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="8ea6c-156">To Retrieve Media Samples with the Synchronous Reader</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="8ea6c-157">Para buscar por tiempo mediante el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="8ea6c-157">To Seek By Time Using the Synchronous Reader</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
-   [<span data-ttu-id="8ea6c-158">Para buscar por número de marco mediante el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="8ea6c-158">To Seek By Frame Number Using the Synchronous Reader</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [<span data-ttu-id="8ea6c-159">Para buscar por el código de tiempo de SMPTE mediante el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="8ea6c-159">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [<span data-ttu-id="8ea6c-160">Para recuperar ejemplos de secuencias con el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="8ea6c-160">To Retrieve Stream Samples with the Synchronous Reader</span></span>](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="8ea6c-161">Para recuperar muestras comprimidas con el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="8ea6c-161">To Retrieve Compressed Samples with the Synchronous Reader</span></span>](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

<span data-ttu-id="8ea6c-162">**Código de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="8ea6c-162">**Example Code**</span></span>

<span data-ttu-id="8ea6c-163">En el ejemplo de código siguiente se muestra cómo leer ejemplos de un archivo ASF mediante el lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-163">The following example code shows how to read samples from an ASF file using the synchronous reader.</span></span> <span data-ttu-id="8ea6c-164">Especifica por el número de marco un intervalo de muestras que se van a proporcionar.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-164">It specifies by frame number a range of samples to deliver.</span></span>


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="8ea6c-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ea6c-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ea6c-166">**Interfaz IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="8ea6c-166">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="8ea6c-167">**Leer archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="8ea6c-167">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="8ea6c-168">**Objeto del lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="8ea6c-168">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> </dl>

 

 




