---
description: Capturar vídeo en un archivo de Windows Media
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Capturar vídeo en un archivo de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279802"
---
# <a name="capturing-video-to-a-windows-media-file"></a><span data-ttu-id="ec830-103">Capturar vídeo en un archivo de Windows Media</span><span class="sxs-lookup"><span data-stu-id="ec830-103">Capturing Video to a Windows Media File</span></span>

<span data-ttu-id="ec830-104">Para capturar vídeo y codificarlo en un archivo Windows Media Video (WMV), conecte el PIN de captura al filtro del [escritor ASF de WM](wm-asf-writer-filter.md) , tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="ec830-104">To capture video and encode it to a Windows Media Video (WMV) file, connect the capture pin to the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the following diagram.</span></span>

![gráfico de captura de Windows Media](images/vidcap03.png)

<span data-ttu-id="ec830-106">La forma más sencilla de compilar este grafo es especificar MEDIASUBTYPE \_ ASF en el método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :</span><span class="sxs-lookup"><span data-stu-id="ec830-106">The easiest way to build this graph is by specifing MEDIASUBTYPE\_Asf in the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method:</span></span>


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



<span data-ttu-id="ec830-107">El valor MEDIASUBTYPE \_ ASF indica al generador de gráficos de captura que use el filtro de escritor ASF de WM como receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="ec830-107">The value MEDIASUBTYPE\_Asf tells the Capture Graph Builder to use the WM ASF Writer filter as the file sink.</span></span> <span data-ttu-id="ec830-108">El generador de gráficos de captura crea el filtro, lo agrega al gráfico y llama a [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) para establecer el nombre del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="ec830-108">The Capture Graph Builder creates the filter, adds it to the graph, and calls [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) to set the name of the output file.</span></span> <span data-ttu-id="ec830-109">Devuelve un puntero al filtro como un parámetro saliente (</span><span class="sxs-lookup"><span data-stu-id="ec830-109">It returns a pointer to the filter as an outgoing parameter (</span></span>


```
pASFWriter
```



<span data-ttu-id="ec830-110">en el ejemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="ec830-110">in the previous example).</span></span>

<span data-ttu-id="ec830-111">Use la interfaz [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) en el escritor ASF de WM para establecer el perfil de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ec830-111">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface on the WM ASF Writer to set the Windows Media profile.</span></span> <span data-ttu-id="ec830-112">Debe hacerlo antes de conectar cualquier PIN en el escritor ASF de WM.</span><span class="sxs-lookup"><span data-stu-id="ec830-112">You must do this before you connect any pins on the WM ASF Writer.</span></span>


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



<span data-ttu-id="ec830-113">Para obtener más información acerca de cómo configurar el perfil, vea [crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="ec830-113">For more information about setting the profile, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="ec830-114">Llame a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar el filtro de captura al escritor ASF:</span><span class="sxs-lookup"><span data-stu-id="ec830-114">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the capture filter to the ASF Writer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



<span data-ttu-id="ec830-115">Cada pin de entrada del filtro de escritura ASF de WM corresponde a una secuencia en el perfil de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ec830-115">Each input pin on the WM ASF Writer filter corresponds to a stream in the Windows Media profile.</span></span> <span data-ttu-id="ec830-116">Debe conectar cada pin para que el contenido del archivo coincida con el perfil.</span><span class="sxs-lookup"><span data-stu-id="ec830-116">You must connect every pin, so that the file content matches the profile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec830-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec830-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec830-118">Capturar vídeo en un archivo</span><span class="sxs-lookup"><span data-stu-id="ec830-118">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



