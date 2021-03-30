---
title: Reproducción de secuencias Web en DirectShow
description: Reproducción de secuencias Web en DirectShow
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- Windows Media Format SDK, DirectShow
- SDK de Windows Media Format, reproducción de secuencias Web
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), reproducción de secuencias Web
- ASF (formato de sistemas avanzados), reproducción de secuencias Web
- DirectShow, reproducción de secuencias Web
- Secuencias Web, DirectShow
- Secuencias Web, reproducción en DirectShow
- secuencias, reproducción de secuencias Web en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994049"
---
# <a name="web-stream-playback-in-directshow"></a><span data-ttu-id="b266b-113">Reproducción de secuencias Web en DirectShow</span><span class="sxs-lookup"><span data-stu-id="b266b-113">Web Stream Playback in DirectShow</span></span>

<span data-ttu-id="b266b-114">Microsoft DirectShow admite secuencias web (consulte [secuencias web](web-streams.md) para obtener más información) en escenarios de reproducción de archivos mediante el filtro de [lector ASF de WM](wm-asf-reader-filter.md) , pero debe escribir su propio filtro de DirectShow para capturar y conservar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b266b-114">Microsoft DirectShow supports Web streams (see [Web Streams](web-streams.md) for more information) in file playback scenarios through the [WM ASF Reader](wm-asf-reader-filter.md) filter, but you must write your own DirectShow filter to capture and persist the stream.</span></span>

> [!Note]  
> <span data-ttu-id="b266b-115">Para reproducir secuencias Web en el contenido que se transmite desde un servidor que ejecuta Windows Media Services, use el control ActiveX® de la serie Windows Media Player 9 incrustado en una página web.</span><span class="sxs-lookup"><span data-stu-id="b266b-115">To play back Web streams in content that is being streamed from a server running Windows Media Services, use the Windows Media Player 9 Series ActiveX® control embedded in a Web page.</span></span>

 

<span data-ttu-id="b266b-116">Cuando se proporciona un archivo que contiene secuencias de tipo WMMEDIATYPE \_ FileTransfer, el lector ASF de WM creará un PIN de salida para él.</span><span class="sxs-lookup"><span data-stu-id="b266b-116">When given a file containing streams of type WMMEDIATYPE\_FileTransfer, the WM ASF Reader will create an output pin for it.</span></span> <span data-ttu-id="b266b-117">El bloque de formato será una estructura de [**\_ \_ formato de Webstream de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) .</span><span class="sxs-lookup"><span data-stu-id="b266b-117">The format block will be a [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure.</span></span> <span data-ttu-id="b266b-118">Si no hay ningún filtro de nivel inferior disponible que pueda controlar ese tipo de medio, el PIN permanecerá sin conexión, pero el archivo seguirá reproduciendo las secuencias de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="b266b-118">If no downstream filter is available that can handle that media type, then the pin will remain unconnected, but the file will still play the audio and/or video streams.</span></span>

<span data-ttu-id="b266b-119">Es importante comprender que cada ejemplo multimedia de una secuencia web contiene una estructura de [**\_ \_ \_ encabezado de ejemplo WMT Webstream**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , que tiene una longitud variable en función de la longitud de su miembro **wszURL** .</span><span class="sxs-lookup"><span data-stu-id="b266b-119">It is important to understand that each media sample in a Web stream contains a [**WMT\_WEBSTREAM\_SAMPLE\_HEADER**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) structure, which has a variable length depending on the length of its **wszURL** member.</span></span> <span data-ttu-id="b266b-120">El puntero a los datos de ejemplo apunta inicialmente a esta estructura y debe avanzar el puntero más allá de la estructura para obtener acceso a los datos reales de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b266b-120">The pointer to the sample data initially points to this structure, and you must advance the pointer past the structure in order to access the actual data in the stream.</span></span> <span data-ttu-id="b266b-121">El filtro del controlador de la secuencia Web se debe basar en la clase **CBaseRenderer** .</span><span class="sxs-lookup"><span data-stu-id="b266b-121">Your Web stream handler filter should be based on the **CBaseRenderer** class.</span></span> <span data-ttu-id="b266b-122">En el método **DoRenderSample** , el filtro deberá analizar la estructura para obtener información sobre la secuencia web y, a continuación, realizar la acción adecuada.</span><span class="sxs-lookup"><span data-stu-id="b266b-122">In the **DoRenderSample** method, the filter will need to parse the structure for information about the Web stream, and then perform the appropriate action.</span></span> <span data-ttu-id="b266b-123">Normalmente, esto implicará guardar el archivo en el disco y, a continuación, llamar a **CommitUrlCacheEntry** y **CreateUrlCacheEntry** para colocar los archivos en la memoria caché de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b266b-123">Typically, this will involve saving the file to disk, and then calling **CommitUrlCacheEntry** and **CreateUrlCacheEntry** to place the files into the Internet Explorer cache.</span></span> <span data-ttu-id="b266b-124">El filtro debe administrar los archivos de varias partes, es decir, los archivos que son más grandes que un ejemplo y también debe controlar los comandos de representación, que se especifican en el miembro **\_ Header de ejemplo Webstream de WMT \_ \_ . wSampleType** .</span><span class="sxs-lookup"><span data-stu-id="b266b-124">The filter must handle multipart files, that is, files that are larger than one sample, and also must handle render commands, which are specified by the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wSampleType** member.</span></span> <span data-ttu-id="b266b-125">El filtro envía un **\_ \_ evento OLE de EC** a la aplicación, junto con el texto de la cadena de ejemplo de **\_ Webstream \_ \_ . wszURL de WMT** que contiene el nombre del archivo que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="b266b-125">The filter sends an **EC\_OLE\_EVENT** to the application, along with the text of the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wszURL** string which contains the name of the file to be rendered.</span></span> <span data-ttu-id="b266b-126">A continuación, la aplicación hace que el explorador muestre la página especificada.</span><span class="sxs-lookup"><span data-stu-id="b266b-126">The application then causes the browser to display the specified page.</span></span> <span data-ttu-id="b266b-127">Si la secuencia Web se ha creado correctamente, el archivo ya debe estar en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="b266b-127">If the Web stream has been authored correctly, the file should already be in the cache.</span></span>

<span data-ttu-id="b266b-128">Para obtener más información sobre los **\_ \_ eventos OLE** **CBaseRenderer**, **DoRenderSample** y EC, vea la documentación del SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b266b-128">For more information on **CBaseRenderer**, **DoRenderSample**, and **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b266b-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b266b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b266b-130">**Secuencias Web**</span><span class="sxs-lookup"><span data-stu-id="b266b-130">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




