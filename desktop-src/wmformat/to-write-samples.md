---
title: Para escribir ejemplos
description: Para escribir ejemplos
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- Advanced Systems Format (ASF), escribir ejemplos
- ASF (formato de sistemas avanzados), escribir ejemplos
- Advanced Systems Format (ASF), pasar ejemplos al escritor
- ASF (formato de sistemas avanzados), pasar ejemplos al escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738014b3c42441e878105d12a8ebf23ce4b266f7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420255"
---
# <a name="to-write-samples"></a><span data-ttu-id="c0700-107">Para escribir ejemplos</span><span class="sxs-lookup"><span data-stu-id="c0700-107">To Write Samples</span></span>

<span data-ttu-id="c0700-108">Cuando haya identificado y configurado las entradas para el archivo que está escribiendo, puede empezar a pasar ejemplos al escritor.</span><span class="sxs-lookup"><span data-stu-id="c0700-108">When you have identified and configured the inputs for the file you are writing, you can begin passing samples to the writer.</span></span> <span data-ttu-id="c0700-109">Debe pasar los ejemplos en el orden en tiempo de presentación, si es posible, para que el proceso de escritura sea más eficaz.</span><span class="sxs-lookup"><span data-stu-id="c0700-109">You should pass samples in presentation-time order, if possible, to make the writing process more efficient.</span></span>

<span data-ttu-id="c0700-110">Antes de pasar cualquier ejemplo, debe establecer el escritor para aceptarlo llamando a [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="c0700-110">Before passing any samples, you must set the writer to accept them by calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="c0700-111">Para pasar un ejemplo al escritor, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c0700-111">To pass a sample to the writer, perform the following steps:</span></span>

1.  <span data-ttu-id="c0700-112">Asigne un búfer y recupere un puntero a la interfaz [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) llamando a [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span><span class="sxs-lookup"><span data-stu-id="c0700-112">Allocate a buffer and retrieve a pointer to the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface by calling [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span></span>
2.  <span data-ttu-id="c0700-113">Recupere la dirección del búfer creado en el paso 1 mediante una llamada a [**INSSBuffer:: getBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="c0700-113">Retrieve the address of the buffer created in step 1 by calling [**INSSBuffer::GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).</span></span>
3.  <span data-ttu-id="c0700-114">Copie los datos de ejemplo en la ubicación del búfer, asegurándose de que el ejemplo que se ha pasado quepa en el búfer asignado.</span><span class="sxs-lookup"><span data-stu-id="c0700-114">Copy your sample data to the buffer location, making sure that the sample passed will fit in the allocated buffer.</span></span> <span data-ttu-id="c0700-115">Puede usar cualquier función de copia de memoria para copiar los datos.</span><span class="sxs-lookup"><span data-stu-id="c0700-115">You can use any memory copying function to copy your data.</span></span> <span data-ttu-id="c0700-116">Una opción común es memcpy, que se incluye en la biblioteca estándar de tiempo de ejecución de C.</span><span class="sxs-lookup"><span data-stu-id="c0700-116">A common choice is memcpy, which is included in the standard C run-time library.</span></span>
4.  <span data-ttu-id="c0700-117">Actualice la cantidad de datos que se usan en el búfer para reflejar el tamaño real del ejemplo llamando a [**INSSBuffer:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span><span class="sxs-lookup"><span data-stu-id="c0700-117">Update the amount of data used in the buffer to reflect the actual size of the sample by calling [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span></span>
5.  <span data-ttu-id="c0700-118">Pase la interfaz de búfer al escritor junto con el número de entrada y el tiempo de muestra mediante el método [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="c0700-118">Pass the buffer interface to the writer along with the input number and sample time using the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span> <span data-ttu-id="c0700-119">Todos los ejemplos de audio de una entrada representan la misma duración del contenido, de modo que puede indicar el tiempo de muestra agregando la duración de ejemplo a un total acumulado.</span><span class="sxs-lookup"><span data-stu-id="c0700-119">All audio samples for an input represent the same duration of content, so you can figure the sample time by adding the sample duration to a running total.</span></span> <span data-ttu-id="c0700-120">En el caso de vídeo, debe calcular el tiempo en función de la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="c0700-120">For video, you need to calculate the time based on the frame rate.</span></span>

<span data-ttu-id="c0700-121">**WriteSample** funciona de forma asincrónica y puede que no termine de escribir los datos del búfer antes de que la aplicación esté lista para volver a llamar al método.</span><span class="sxs-lookup"><span data-stu-id="c0700-121">**WriteSample** works asynchronously and might not finish writing the data from the buffer before your application is ready to call the method again.</span></span> <span data-ttu-id="c0700-122">Por lo tanto, es importante llamar a **AllocateSample** una vez para cada llamada a **WriteSample**.</span><span class="sxs-lookup"><span data-stu-id="c0700-122">Therefore, it is important to call **AllocateSample** once for each call to **WriteSample**.</span></span> <span data-ttu-id="c0700-123">Sin embargo, puede liberar la interfaz **INSSBuffer** inmediatamente después de llamar a **WriteSample**.</span><span class="sxs-lookup"><span data-stu-id="c0700-123">However, you can release the **INSSBuffer** interface immediately after calling **WriteSample**.</span></span>

<span data-ttu-id="c0700-124">Cuando haya terminado de pasar los ejemplos, llame a [**IWMWriter:: EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).</span><span class="sxs-lookup"><span data-stu-id="c0700-124">When you have finished passing samples, call [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).</span></span>

<span data-ttu-id="c0700-125">**Nota:** Es importante que los ejemplos de todas las secuencias del archivo se pasen al escritor en la sincronización entre sí.</span><span class="sxs-lookup"><span data-stu-id="c0700-125">**Note** It is important that samples from all streams in the file are passed to the writer in synchronization with one another.</span></span> <span data-ttu-id="c0700-126">Es decir, siempre que sea posible, debe pasar ejemplos al escritor en el orden en tiempo de presentación dentro de la tolerancia de sincronización especificada en [**IWMWriterAdvanced:: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span><span class="sxs-lookup"><span data-stu-id="c0700-126">That is, whenever possible you should pass samples to the writer in presentation-time order within the sync tolerance specified in [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span></span> <span data-ttu-id="c0700-127">Los mejores resultados se logran cuando los datos se entregan a cada flujo en unidades de un segundo o menos.</span><span class="sxs-lookup"><span data-stu-id="c0700-127">Best results are achieved when data is delivered to each stream in units of one second or less.</span></span>

<span data-ttu-id="c0700-128">Las secuencias también deben terminar aproximadamente al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="c0700-128">Streams should also end at approximately the same time.</span></span> <span data-ttu-id="c0700-129">Por ejemplo, no debe escribir un archivo con una secuencia de audio de 45 segundos de duración y un flujo de vídeo de 50 segundos de duración.</span><span class="sxs-lookup"><span data-stu-id="c0700-129">For example, you should not write a file with an audio stream that is 45 seconds long and a video stream that is 50 seconds long.</span></span> <span data-ttu-id="c0700-130">Si codifica este tipo de archivo con entradas sin modificar, algunos de los datos de audio al final de la secuencia se quitarán (aunque sea la secuencia más corta).</span><span class="sxs-lookup"><span data-stu-id="c0700-130">If you encode such a file with unaltered inputs, some of the audio data at the end of the stream will be dropped (even though it is the shorter stream).</span></span> <span data-ttu-id="c0700-131">Para que el trabajo de codificación de archivos funcione, debe agregar 5 segundos de silencio a la entrada de audio para que una secuencia no finalice varios segundos antes que otra.</span><span class="sxs-lookup"><span data-stu-id="c0700-131">To make the file encoding work, you should add 5 seconds of silence to the audio input so that one stream does not end several seconds before another.</span></span> <span data-ttu-id="c0700-132">No es necesario que los tipos de secuencia con ejemplos intermitentes, como secuencias de texto o de imagen, se rellenen de esta manera.</span><span class="sxs-lookup"><span data-stu-id="c0700-132">It is not necessary for stream types with intermittent samples, like text or image streams, to be padded in this way.</span></span> <span data-ttu-id="c0700-133">Las secuencias de comandos de script también deben seguir todas estas reglas.</span><span class="sxs-lookup"><span data-stu-id="c0700-133">Script command streams should also follow all these rules.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0700-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0700-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0700-135">**Interfaz INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="c0700-135">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="c0700-136">**Interfaz IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="c0700-136">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="c0700-137">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="c0700-137">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




