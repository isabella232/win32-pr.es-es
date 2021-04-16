---
description: Generar gráficos de filtro para escribir archivos ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Generar gráficos de filtro para escribir archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495455"
---
# <a name="building-filter-graphs-to-write-asf-files"></a><span data-ttu-id="ae37b-103">Generar gráficos de filtro para escribir archivos ASF</span><span class="sxs-lookup"><span data-stu-id="ae37b-103">Building Filter Graphs to Write ASF Files</span></span>

<span data-ttu-id="ae37b-104">Al crear contenido basado en Windows Media, las aplicaciones suelen usar uno de los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="ae37b-104">When creating Windows Media–based content, applications typically use one of the following scenarios:</span></span>

-   <span data-ttu-id="ae37b-105">Convertir o transcodificar contenido de otro formato en el formato de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ae37b-105">Converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="ae37b-106">Insertar contenido que no está basado en Windows Media (formatos de secuencia nativo) en archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="ae37b-106">Inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="ae37b-107">Capturar datos activos y codificarlos inmediatamente en el formato de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ae37b-107">Capturing live data and encoding it immediately into Windows Media Format.</span></span>

<span data-ttu-id="ae37b-108">Transcodificar archivos ASF</span><span class="sxs-lookup"><span data-stu-id="ae37b-108">Transcoding ASF Files</span></span>

<span data-ttu-id="ae37b-109">Puede crear un gráfico de filtros de transcodificación de archivos mediante el [escritor ASF de WM](wm-asf-writer-filter.md) de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="ae37b-109">You can build a file-transcoding filter graph using the [WM ASF Writer](wm-asf-writer-filter.md) in various ways.</span></span> <span data-ttu-id="ae37b-110">La manera más fácil es agregar el escritor ASF de WM al gráfico de filtro y, a continuación, usar el método IGraphBuilder:: RenderFile para generar el gráfico automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ae37b-110">The easiest way is to add the WM ASF Writer to the filter graph and then use the IGraphBuilder::RenderFile method to build the graph automatically.</span></span>

<span data-ttu-id="ae37b-111">Una manera alternativa es agregar cada filtro manualmente al gráfico y conectar los pin.</span><span class="sxs-lookup"><span data-stu-id="ae37b-111">An alternative way is to add each filter manually to the graph and connect the pins.</span></span> <span data-ttu-id="ae37b-112">Después de agregar el escritor ASF de WM, configúrelo con los métodos IConfigAsfWriter si el perfil predeterminado no es adecuado y conecte las clavijas de entrada del escritor ASF de WM a los pin de salida correspondientes en los filtros de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="ae37b-112">After adding the WM ASF Writer, configure it by using the IConfigAsfWriter methods if the default profile is not suitable, and connect the WM ASF Writer input pins to the corresponding output pins on the upstream filters.</span></span>

<span data-ttu-id="ae37b-113">En la ilustración siguiente se muestran configuraciones típicas del gráfico de filtros de transcodificación ASF de WM.</span><span class="sxs-lookup"><span data-stu-id="ae37b-113">The following illustration shows typical WM ASF Writer transcoding filter graph configurations.</span></span>

![gráfico de filtros de transcodificación](images/asf-transcode.png)

<span data-ttu-id="ae37b-115">Insertar formatos de secuencias nativas en archivos ASF</span><span class="sxs-lookup"><span data-stu-id="ae37b-115">Inserting Native Stream Formats Into ASF Files</span></span>

<span data-ttu-id="ae37b-116">De forma predeterminada, el filtro del escritor ASF de WM espera secuencias de audio y vídeo sin comprimir en sus clavijas de entrada, y usa los códecs Windows Media Audio y Windows Media Video para comprimir las secuencias.</span><span class="sxs-lookup"><span data-stu-id="ae37b-116">By default, the WM ASF Writer filter expects uncompressed audio and video streams on its input pins, and uses the Windows Media Audio and Windows Media Video codecs to compress the streams.</span></span> <span data-ttu-id="ae37b-117">Sin embargo, el contenedor de archivos ASF puede usarse para cualquier tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ae37b-117">However, the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="ae37b-118">Al colocar los datos multimedia digitales en un contenedor de archivos ASF, puede agregar características proporcionadas por ASF, como metadatos y administración de derechos digitales (DRM), sin tener que transcodificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="ae37b-118">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="ae37b-119">Para crear un archivo ASF que contenga contenido que no esté basado en Windows Media, la aplicación debe comprimir la secuencia del gráfico de filtros ascendente del escritor ASF de WM y omitir el mecanismo de compresión del escritor ASF de WM llamando a [**IConfigAsfWriter2:: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ae37b-119">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



<span data-ttu-id="ae37b-120">A continuación, configure el filtro con el perfil deseado.</span><span class="sxs-lookup"><span data-stu-id="ae37b-120">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="ae37b-121">Es fundamental que el tipo de medio del flujo de entrada coincida exactamente con el formato del perfil.</span><span class="sxs-lookup"><span data-stu-id="ae37b-121">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="ae37b-122">En algunos casos, puede ser necesario examinar el formato del flujo de entrada y crear un perfil personalizado para que coincida con él.</span><span class="sxs-lookup"><span data-stu-id="ae37b-122">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span>

<span data-ttu-id="ae37b-123">Cuando conecte el escritor ASF de WM al filtro de nivel superior, use el método IGraphBuilder:: ConnectDirect.</span><span class="sxs-lookup"><span data-stu-id="ae37b-123">When you connect the WM ASF Writer to the upstream filter, use the IGraphBuilder::ConnectDirect method.</span></span> <span data-ttu-id="ae37b-124">No use ningún método de "conexión inteligente", como IGraphBuilder:: Connect o IGraphBuilder:: RenderFile, para conectar el filtro porque se deshabilitará el modo "omitir compresión" del filtro.</span><span class="sxs-lookup"><span data-stu-id="ae37b-124">Do not use any "intelligent connect" methods such as IGraphBuilder::Connect or IGraphBuilder::RenderFile to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

<span data-ttu-id="ae37b-125">Captura directa desde un dispositivo a un archivo ASF</span><span class="sxs-lookup"><span data-stu-id="ae37b-125">Capturing Directly from a Device to an ASF File</span></span>

<span data-ttu-id="ae37b-126">Al capturar audio o vídeo directamente en un archivo ASF, el gráfico de filtros tendrá un aspecto similar al siguiente, en función del tipo de dispositivo de captura que se esté usando.</span><span class="sxs-lookup"><span data-stu-id="ae37b-126">When capturing audio or video directly to an ASF file, the filter graph will look similar to the following, depending on the type of capture device being used.</span></span>

![gráfico de captura de vídeo de Windows Media](images/asf-webcam.png)

<span data-ttu-id="ae37b-128">Para obtener más información sobre la creación de gráficos de captura de vídeo y audio, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="ae37b-128">For more information about creating video and audio capture graphs, see the following topics:</span></span>

-   [<span data-ttu-id="ae37b-129">Captura de audio</span><span class="sxs-lookup"><span data-stu-id="ae37b-129">Audio Capture</span></span>](audio-capture.md)
-   [<span data-ttu-id="ae37b-130">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ae37b-130">Video Capture</span></span>](video-capture.md)

<span data-ttu-id="ae37b-131">El escritor ASF de WM no se ejecutará a menos que todos los pin estén conectados.</span><span class="sxs-lookup"><span data-stu-id="ae37b-131">The WM ASF Writer will not run unless all of its pins are connected.</span></span> <span data-ttu-id="ae37b-132">Si configura el escritor ASF de WM con el perfil de sistema predeterminado (no recomendado) o cualquier perfil con secuencias de audio y vídeo, se creará un PIN de entrada para cada flujo y cada uno de esos PIN debe estar conectado.</span><span class="sxs-lookup"><span data-stu-id="ae37b-132">If you configure the WM ASF Writer with the default system profile (not recommended), or any profile with audio and video streams, then it will create an input pin for each stream and each of those pins must be connected.</span></span> <span data-ttu-id="ae37b-133">Si no desea capturar audio, por ejemplo, asegúrese de configurar el filtro con un perfil de solo vídeo para que no se cree ningún PIN de audio.</span><span class="sxs-lookup"><span data-stu-id="ae37b-133">If you do not intend to capture audio, for example, then be sure to configure the filter with a video-only profile so that no audio pin is created.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae37b-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae37b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae37b-135">Crear archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="ae37b-135">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



