---
title: Insertar formatos de secuencias nativas en archivos ASF (QASF)
description: Insertar formatos de secuencias nativas en archivos ASF (QASF)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- SDK de Windows Media Format, formatos de secuencias nativas (QASF)
- SDK de Windows Media Format, insertar formatos de secuencias nativas en archivos ASF (QASF)
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), insertar formatos de secuencias nativas (QASF)
- ASF (formato de sistemas avanzados), insertar formatos de secuencias nativas (QASF)
- Advanced Systems Format (ASF), formatos de secuencias nativas (QASF)
- ASF (formato de sistemas avanzados), formatos de secuencias nativas (QASF)
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, formatos de secuencias nativas (QASF)
- DirectShow, insertar formatos de secuencias nativas en archivos ASF (QASF)
- SDK de Windows Media Format, QASF
- Advanced Systems Format (ASF), QASF
- ASF (formato de sistemas avanzados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4736c450b3620a05fe01dcc1808adc297ebbd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903748"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a><span data-ttu-id="cd32a-118">Insertar formatos de secuencias nativas en archivos ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="cd32a-118">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>

<span data-ttu-id="cd32a-119">De forma predeterminada, el [escritor ASF de WM](wm-asf-writer-filter.md) espera secuencias de audio y vídeo sin comprimir en sus clavijas de entrada y usa el SDK de Windows Media Format para tener acceso a los códecs Windows Media Audio y Windows Media Video, que comprimen las secuencias.</span><span class="sxs-lookup"><span data-stu-id="cd32a-119">By default, the [WM ASF Writer](wm-asf-writer-filter.md) expects uncompressed audio and video streams on its input pins, and uses the Windows Media Format SDK to access the Windows Media Audio and Windows Media Video codecs, which compress the streams.</span></span> <span data-ttu-id="cd32a-120">Sin embargo, el contenedor de archivos ASF puede usarse para cualquier tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cd32a-120">But the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="cd32a-121">Al colocar los datos multimedia digitales en un contenedor de archivos ASF, puede agregar características proporcionadas por ASF, como metadatos y administración de derechos digitales (DRM), sin tener que transcodificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="cd32a-121">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="cd32a-122">Para crear un archivo ASF que contenga contenido que no esté basado en Windows Media, la aplicación debe comprimir la secuencia del gráfico de filtros ascendente del escritor ASF de WM y omitir el mecanismo de compresión del escritor ASF de WM llamando a [**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="cd32a-122">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



<span data-ttu-id="cd32a-123">A continuación, configure el filtro con el perfil deseado.</span><span class="sxs-lookup"><span data-stu-id="cd32a-123">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="cd32a-124">Es fundamental que el tipo de medio del flujo de entrada coincida exactamente con el formato del perfil.</span><span class="sxs-lookup"><span data-stu-id="cd32a-124">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="cd32a-125">En algunos casos, puede ser necesario examinar el formato del flujo de entrada y crear un perfil personalizado para que coincida con él.</span><span class="sxs-lookup"><span data-stu-id="cd32a-125">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span> <span data-ttu-id="cd32a-126">Para obtener más información, vea [para crear archivos ASF con códecs de terceros](to-create-asf-files-using-third-party-codecs.md).</span><span class="sxs-lookup"><span data-stu-id="cd32a-126">For more information, see [To Create ASF Files Using Third-Party Codecs](to-create-asf-files-using-third-party-codecs.md).</span></span>

<span data-ttu-id="cd32a-127">Cuando conecte el escritor ASF de WM al filtro de nivel superior, use el método **IGraphBuilder:: ConnectDirect** .</span><span class="sxs-lookup"><span data-stu-id="cd32a-127">When you connect the WM ASF Writer to the upstream filter, use the **IGraphBuilder::ConnectDirect** method.</span></span> <span data-ttu-id="cd32a-128">No use ningún método de "conexión inteligente", como **IGraphBuilder:: Connect** o **IGraphBuilder:: RenderFile** , para conectar el filtro porque se deshabilitará el modo "omitir compresión" del filtro.</span><span class="sxs-lookup"><span data-stu-id="cd32a-128">Do not use any "intelligent connect" methods such as **IGraphBuilder::Connect** or **IGraphBuilder::RenderFile** to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

 

 




