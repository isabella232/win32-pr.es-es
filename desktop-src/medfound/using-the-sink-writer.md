---
description: .
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Uso del escritor de receptor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46157eae6fe851468515f9d9653adb33918ebb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001581"
---
# <a name="using-the-sink-writer"></a><span data-ttu-id="d6598-103">Uso del escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="d6598-103">Using the Sink Writer</span></span>

## <a name="overview"></a><span data-ttu-id="d6598-104">Información general</span><span class="sxs-lookup"><span data-stu-id="d6598-104">Overview</span></span>

### <a name="file-container-types"></a><span data-ttu-id="d6598-105">Tipos de contenedor de archivos</span><span class="sxs-lookup"><span data-stu-id="d6598-105">File Container Types</span></span>

<span data-ttu-id="d6598-106">El escritor de receptores tiene compatibilidad integrada con varios tipos de contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="d6598-106">The sink writer has built-in support for several file container types.</span></span> <span data-ttu-id="d6598-107">Para obtener una lista completa, consulte [MF \_ Transcode \_ CONTAINERTYPE](mf-transcode-containertype.md).</span><span class="sxs-lookup"><span data-stu-id="d6598-107">For a complete list, see [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md).</span></span> <span data-ttu-id="d6598-108">Puede admitir tipos de contenedor adicionales escribiendo un receptor de [multimedia](media-sinks.md)personalizado.</span><span class="sxs-lookup"><span data-stu-id="d6598-108">You can support additional container types by writing a custom [media sink](media-sinks.md).</span></span> <span data-ttu-id="d6598-109">El contenedor de archivos se especifica cuando se crea una nueva instancia del escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="d6598-109">The file container is specified when you create a new instance of the sink writer.</span></span>

### <a name="stream-formats"></a><span data-ttu-id="d6598-110">Formatos de secuencia</span><span class="sxs-lookup"><span data-stu-id="d6598-110">Stream Formats</span></span>

<span data-ttu-id="d6598-111">Para cada flujo, la aplicación debe especificar lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d6598-111">For each stream, the application must specify the following.</span></span>

-   <span data-ttu-id="d6598-112">El *formato de entrada* es el formato que la aplicación envía al escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="d6598-112">The *input format* is the format that the application sends to the sink writer.</span></span>
-   <span data-ttu-id="d6598-113">El *formato de salida* es el formato que se escribirá en el archivo.</span><span class="sxs-lookup"><span data-stu-id="d6598-113">The *output format* is the format that will be written to the file.</span></span>

<span data-ttu-id="d6598-114">Los formatos de entrada y salida se pueden comprimir o descomprimir.</span><span class="sxs-lookup"><span data-stu-id="d6598-114">The input and output formats can be either compressed or uncompressed.</span></span> <span data-ttu-id="d6598-115">El escritor del receptor admite las siguientes combinaciones:</span><span class="sxs-lookup"><span data-stu-id="d6598-115">The sink writer supports the following combinations:</span></span>

-   <span data-ttu-id="d6598-116">Entrada sin comprimir con salida comprimida.</span><span class="sxs-lookup"><span data-stu-id="d6598-116">Uncompressed input with compressed output.</span></span> <span data-ttu-id="d6598-117">Este es el caso típico y se usa para codificar o transcodificar escenarios.</span><span class="sxs-lookup"><span data-stu-id="d6598-117">This is the typical case, and is used for encoding or transcoding scenarios.</span></span> <span data-ttu-id="d6598-118">Un codificador Microsoft Media Foundation debe estar disponible que acepte el tipo de entrada y codifique en el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="d6598-118">A Microsoft Media Foundation encoder must be available that accepts the input type and encodes to the output type.</span></span>
-   <span data-ttu-id="d6598-119">Entrada comprimida con salida idéntica.</span><span class="sxs-lookup"><span data-stu-id="d6598-119">Compressed input with identical output.</span></span> <span data-ttu-id="d6598-120">Use esta combinación para Remux un archivo sin transcodificar.</span><span class="sxs-lookup"><span data-stu-id="d6598-120">Use this combination to remux a file without transcoding.</span></span>
-   <span data-ttu-id="d6598-121">Entrada sin comprimir con salida idéntica.</span><span class="sxs-lookup"><span data-stu-id="d6598-121">Uncompressed input with identical output.</span></span> <span data-ttu-id="d6598-122">Use esta combinación para escribir audio sin comprimir o vídeo en un contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="d6598-122">Use this combination to write uncompressed audio or video to a file container.</span></span>

<span data-ttu-id="d6598-123">El escritor del receptor no admite el cambio de tamaño de vídeo, la conversión de velocidad de fotogramas o el remuestreo de audio, a menos que el codificador proporcione estas funciones.</span><span class="sxs-lookup"><span data-stu-id="d6598-123">The sink writer does not support video resizing, frame-rate conversion, or audio resampling, unless these functions are provided by the encoder.</span></span> <span data-ttu-id="d6598-124">De lo contrario, la aplicación puede usar [procesadores de señal digital](windowsmediadigitalsignalprocessors.md) para convertir los datos de entrada, antes de enviar los datos al</span><span class="sxs-lookup"><span data-stu-id="d6598-124">Otherwise, the application can use [Digital Signal Processors](windowsmediadigitalsignalprocessors.md) to convert the input data, before sending the data to the</span></span>

## <a name="creating-the-sink-writer"></a><span data-ttu-id="d6598-125">Creación del escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="d6598-125">Creating the Sink Writer</span></span>

<span data-ttu-id="d6598-126">Hay dos funciones que crean el escritor del receptor:</span><span class="sxs-lookup"><span data-stu-id="d6598-126">There are two functions that create the sink writer:</span></span>

-   <span data-ttu-id="d6598-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) toma la dirección URL de un archivo de salida o un puntero a una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="d6598-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) takes the URL of an output file or a pointer to a byte stream.</span></span> <span data-ttu-id="d6598-128">Esta función crea el receptor de medios internamente.</span><span class="sxs-lookup"><span data-stu-id="d6598-128">This function creates the media sink internally.</span></span>
-   <span data-ttu-id="d6598-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) toma un puntero a un receptor de medios que ya ha creado la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d6598-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) takes a pointer to a media sink that has already been created by the application.</span></span>

<span data-ttu-id="d6598-130">Si usa uno de los receptores de medios integrados, es preferible usar la función [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) , ya que el autor de la llamada no necesita configurar el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="d6598-130">If you are using one of the built-in media sinks, the [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) function is preferable, because the caller does not need to configure the media sink.</span></span>

<span data-ttu-id="d6598-131">El método [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) proporciona varias opciones para especificar el tipo de contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="d6598-131">The [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) method provides several options for specifying the type of file container.</span></span> <span data-ttu-id="d6598-132">En el caso más simple, la función usa la extensión de nombre de archivo en la dirección URL para seleccionar el contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="d6598-132">In the simplest case, the function uses the file name extension in the URL to select the file container.</span></span> <span data-ttu-id="d6598-133">Para obtener más información, consulte la página de referencia de funciones.</span><span class="sxs-lookup"><span data-stu-id="d6598-133">For details, refer to the function reference page.</span></span>

<span data-ttu-id="d6598-134">Por ejemplo, el código siguiente especifica el nombre de archivo "Output. WMV" de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="d6598-134">For example, the following code specifies the file name "output.wmv" for the URL.</span></span> <span data-ttu-id="d6598-135">En función de la extensión de nombre de archivo, el escritor de receptores cargará el [receptor de medios ASF](asf-media-sinks.md) para crear un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="d6598-135">Based on the file name extension, the sink writer will load the [ASF Media Sink](asf-media-sinks.md) to create an Advanced Systems Format (ASF) file.</span></span>


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



<span data-ttu-id="d6598-136">En el caso de [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), el tipo de archivo viene determinado por el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="d6598-136">In the case of [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), the file type is determined by the media sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6598-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d6598-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6598-138">Escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="d6598-138">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 



