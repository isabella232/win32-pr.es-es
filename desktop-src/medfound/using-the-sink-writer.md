---
description: Uso del escritor de receptores
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Uso del escritor de receptores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4fa472bd1a5121454b3ffb06def7082508432b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110493"
---
# <a name="using-the-sink-writer"></a><span data-ttu-id="f4d13-103">Uso del escritor de receptores</span><span class="sxs-lookup"><span data-stu-id="f4d13-103">Using the Sink Writer</span></span>

## <a name="overview"></a><span data-ttu-id="f4d13-104">Información general</span><span class="sxs-lookup"><span data-stu-id="f4d13-104">Overview</span></span>

### <a name="file-container-types"></a><span data-ttu-id="f4d13-105">Tipos de contenedor de archivos</span><span class="sxs-lookup"><span data-stu-id="f4d13-105">File Container Types</span></span>

<span data-ttu-id="f4d13-106">El escritor de receptores tiene compatibilidad integrada con varios tipos de contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="f4d13-106">The sink writer has built-in support for several file container types.</span></span> <span data-ttu-id="f4d13-107">Para obtener una lista completa, vea [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md).</span><span class="sxs-lookup"><span data-stu-id="f4d13-107">For a complete list, see [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md).</span></span> <span data-ttu-id="f4d13-108">Puede admitir tipos de contenedor adicionales escribiendo un receptor [de medios personalizado.](media-sinks.md)</span><span class="sxs-lookup"><span data-stu-id="f4d13-108">You can support additional container types by writing a custom [media sink](media-sinks.md).</span></span> <span data-ttu-id="f4d13-109">El contenedor de archivos se especifica cuando se crea una nueva instancia del escritor de receptores.</span><span class="sxs-lookup"><span data-stu-id="f4d13-109">The file container is specified when you create a new instance of the sink writer.</span></span>

### <a name="stream-formats"></a><span data-ttu-id="f4d13-110">Formatos de secuencia</span><span class="sxs-lookup"><span data-stu-id="f4d13-110">Stream Formats</span></span>

<span data-ttu-id="f4d13-111">Para cada secuencia, la aplicación debe especificar lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="f4d13-111">For each stream, the application must specify the following.</span></span>

-   <span data-ttu-id="f4d13-112">El *formato de entrada* es el formato que la aplicación envía al escritor receptor.</span><span class="sxs-lookup"><span data-stu-id="f4d13-112">The *input format* is the format that the application sends to the sink writer.</span></span>
-   <span data-ttu-id="f4d13-113">El *formato de* salida es el formato que se escribirá en el archivo.</span><span class="sxs-lookup"><span data-stu-id="f4d13-113">The *output format* is the format that will be written to the file.</span></span>

<span data-ttu-id="f4d13-114">Los formatos de entrada y salida se pueden comprimir o descomprimir.</span><span class="sxs-lookup"><span data-stu-id="f4d13-114">The input and output formats can be either compressed or uncompressed.</span></span> <span data-ttu-id="f4d13-115">El escritor de receptores admite las siguientes combinaciones:</span><span class="sxs-lookup"><span data-stu-id="f4d13-115">The sink writer supports the following combinations:</span></span>

-   <span data-ttu-id="f4d13-116">Entrada sin comprimir con salida comprimida.</span><span class="sxs-lookup"><span data-stu-id="f4d13-116">Uncompressed input with compressed output.</span></span> <span data-ttu-id="f4d13-117">Este es el caso típico y se usa para escenarios de codificación o transcodificación.</span><span class="sxs-lookup"><span data-stu-id="f4d13-117">This is the typical case, and is used for encoding or transcoding scenarios.</span></span> <span data-ttu-id="f4d13-118">Debe Microsoft Media Foundation codificador que acepte el tipo de entrada y se codifica en el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="f4d13-118">A Microsoft Media Foundation encoder must be available that accepts the input type and encodes to the output type.</span></span>
-   <span data-ttu-id="f4d13-119">Entrada comprimida con salida idéntica.</span><span class="sxs-lookup"><span data-stu-id="f4d13-119">Compressed input with identical output.</span></span> <span data-ttu-id="f4d13-120">Use esta combinación para volver a experienciar un archivo sin transcodificación.</span><span class="sxs-lookup"><span data-stu-id="f4d13-120">Use this combination to remux a file without transcoding.</span></span>
-   <span data-ttu-id="f4d13-121">Entrada sin comprimir con una salida idéntica.</span><span class="sxs-lookup"><span data-stu-id="f4d13-121">Uncompressed input with identical output.</span></span> <span data-ttu-id="f4d13-122">Use esta combinación para escribir audio o vídeo sin comprimir en un contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="f4d13-122">Use this combination to write uncompressed audio or video to a file container.</span></span>

<span data-ttu-id="f4d13-123">El sistema de escritura del receptor no admite el cambio de tamaño de vídeo, la conversión de la velocidad de fotogramas o el cambio demuestreo de audio, a menos que el codificador proporciona estas funciones.</span><span class="sxs-lookup"><span data-stu-id="f4d13-123">The sink writer does not support video resizing, frame-rate conversion, or audio resampling, unless these functions are provided by the encoder.</span></span> <span data-ttu-id="f4d13-124">De lo contrario, la aplicación puede usar [procesadores de señal digital](windowsmediadigitalsignalprocessors.md) para convertir los datos de entrada, antes de enviar los datos a</span><span class="sxs-lookup"><span data-stu-id="f4d13-124">Otherwise, the application can use [Digital Signal Processors](windowsmediadigitalsignalprocessors.md) to convert the input data, before sending the data to the</span></span>

## <a name="creating-the-sink-writer"></a><span data-ttu-id="f4d13-125">Creación del escritor de receptores</span><span class="sxs-lookup"><span data-stu-id="f4d13-125">Creating the Sink Writer</span></span>

<span data-ttu-id="f4d13-126">Hay dos funciones que crean el sistema de escritura del receptor:</span><span class="sxs-lookup"><span data-stu-id="f4d13-126">There are two functions that create the sink writer:</span></span>

-   <span data-ttu-id="f4d13-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) toma la dirección URL de un archivo de salida o un puntero a una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="f4d13-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) takes the URL of an output file or a pointer to a byte stream.</span></span> <span data-ttu-id="f4d13-128">Esta función crea el receptor multimedia internamente.</span><span class="sxs-lookup"><span data-stu-id="f4d13-128">This function creates the media sink internally.</span></span>
-   <span data-ttu-id="f4d13-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) toma un puntero a un receptor multimedia que la aplicación ya ha creado.</span><span class="sxs-lookup"><span data-stu-id="f4d13-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) takes a pointer to a media sink that has already been created by the application.</span></span>

<span data-ttu-id="f4d13-130">Si usa uno de los receptores de medios integrados, es preferible la función [**MFCreateSinkWriterFromURL,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) ya que el autor de la llamada no necesita configurar el receptor multimedia.</span><span class="sxs-lookup"><span data-stu-id="f4d13-130">If you are using one of the built-in media sinks, the [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) function is preferable, because the caller does not need to configure the media sink.</span></span>

<span data-ttu-id="f4d13-131">El [**método MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) proporciona varias opciones para especificar el tipo de contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="f4d13-131">The [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) method provides several options for specifying the type of file container.</span></span> <span data-ttu-id="f4d13-132">En el caso más sencillo, la función usa la extensión de nombre de archivo en la dirección URL para seleccionar el contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="f4d13-132">In the simplest case, the function uses the file name extension in the URL to select the file container.</span></span> <span data-ttu-id="f4d13-133">Para obtener más información, consulte la página de referencia de función.</span><span class="sxs-lookup"><span data-stu-id="f4d13-133">For details, refer to the function reference page.</span></span>

<span data-ttu-id="f4d13-134">Por ejemplo, el código siguiente especifica el nombre de archivo "output.wmv" para la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f4d13-134">For example, the following code specifies the file name "output.wmv" for the URL.</span></span> <span data-ttu-id="f4d13-135">Según la extensión de nombre de archivo, el sistema de escritura del receptor cargará el receptor de medios [de ASF](asf-media-sinks.md) para crear un archivo de formato de sistemas avanzados (ASF).</span><span class="sxs-lookup"><span data-stu-id="f4d13-135">Based on the file name extension, the sink writer will load the [ASF Media Sink](asf-media-sinks.md) to create an Advanced Systems Format (ASF) file.</span></span>


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



<span data-ttu-id="f4d13-136">En el caso de [**MFCreateSinkWriterFromMediaSink,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)el tipo de archivo viene determinado por el receptor multimedia.</span><span class="sxs-lookup"><span data-stu-id="f4d13-136">In the case of [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), the file type is determined by the media sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4d13-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4d13-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4d13-138">Escritor de receptores</span><span class="sxs-lookup"><span data-stu-id="f4d13-138">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 



