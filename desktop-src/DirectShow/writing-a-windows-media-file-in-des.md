---
description: Escritura de un archivo de Windows Media en DES
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Escritura de un archivo de Windows Media en DES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689668"
---
# <a name="writing-a-windows-media-file-in-des"></a><span data-ttu-id="e59bc-103">Escritura de un archivo de Windows Media en DES</span><span class="sxs-lookup"><span data-stu-id="e59bc-103">Writing a Windows Media File in DES</span></span>

<span data-ttu-id="e59bc-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="e59bc-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="e59bc-105">En esta sección se describe cómo escribir un archivo de Windows Media mediante los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="e59bc-105">This section describes how to write a Windows Media file using [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e59bc-106">No utilice el motor de representación inteligente para escribir archivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e59bc-106">Do not use the Smart Render Engine to write Windows Media files.</span></span> <span data-ttu-id="e59bc-107">Use siempre el motor de representación básico (CLSID \_ RenderEngine).</span><span class="sxs-lookup"><span data-stu-id="e59bc-107">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

 

<span data-ttu-id="e59bc-108">Para escribir un archivo de Windows Media, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e59bc-108">To write a Windows Media file, do the following:</span></span>

1.  <span data-ttu-id="e59bc-109">Llame a **SetSite** en el motor de representación con un puntero al proveedor de claves.</span><span class="sxs-lookup"><span data-stu-id="e59bc-109">Call **SetSite** on the render engine, with a pointer to your key provider.</span></span>
2.  <span data-ttu-id="e59bc-110">Cree el front-end del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e59bc-110">Build the front end of the graph.</span></span> <span data-ttu-id="e59bc-111">(Vea [representar un proyecto](rendering-a-project.md)).</span><span class="sxs-lookup"><span data-stu-id="e59bc-111">(See [Rendering a Project](rendering-a-project.md).)</span></span>
3.  <span data-ttu-id="e59bc-112">Cree el filtro del [escritor ASF de WM](wm-asf-writer-filter.md) y agréguelo al gráfico.</span><span class="sxs-lookup"><span data-stu-id="e59bc-112">Create the [WM ASF Writer](wm-asf-writer-filter.md) filter and add it to the graph.</span></span>
4.  <span data-ttu-id="e59bc-113">Use la interfaz [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) en el filtro de escritor ASF de WM para establecer el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="e59bc-113">Use the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface on the WM ASF Writer filter to set the file name.</span></span>
5.  <span data-ttu-id="e59bc-114">Configure el escritor ASF de WM para que use un perfil de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e59bc-114">Configure the WM ASF Writer to use a Windows Media profile.</span></span> <span data-ttu-id="e59bc-115">Cada perfil tiene un número predefinido de secuencias.</span><span class="sxs-lookup"><span data-stu-id="e59bc-115">Each profile has a predefined number of streams.</span></span> <span data-ttu-id="e59bc-116">Debe elegir un perfil que coincida con los grupos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="e59bc-116">You must choose a profile that matches the groups in your project.</span></span>

    <span data-ttu-id="e59bc-117">La interfaz [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) contiene algunos métodos diferentes para configurar el perfil.</span><span class="sxs-lookup"><span data-stu-id="e59bc-117">The [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface contains a few different methods for setting the profile.</span></span> <span data-ttu-id="e59bc-118">Por ejemplo, el método **ConfigureFilterUsingProfileGuid** especifica un perfil de sistema como un GUID.</span><span class="sxs-lookup"><span data-stu-id="e59bc-118">For example, the **ConfigureFilterUsingProfileGuid** method specifies a system profile as a GUID.</span></span> <span data-ttu-id="e59bc-119">O bien, puede usar los métodos de formato de Windows Media para obtener un puntero **IWMProfile** y, a continuación, llamar a [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile).</span><span class="sxs-lookup"><span data-stu-id="e59bc-119">Or, you can use Windows Media Format methods to get an **IWMProfile** pointer and then call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile).</span></span> <span data-ttu-id="e59bc-120">Para obtener más información, consulte [configuración del escritor ASF](configuring-the-asf-writer.md).</span><span class="sxs-lookup"><span data-stu-id="e59bc-120">For more information, see [Configuring the ASF Writer](configuring-the-asf-writer.md).</span></span>

6.  <span data-ttu-id="e59bc-121">Conecte el front-end al escritor ASF.</span><span class="sxs-lookup"><span data-stu-id="e59bc-121">Connect the front end to the ASF Writer.</span></span> <span data-ttu-id="e59bc-122">El front-end del gráfico contiene un PIN de salida para cada grupo.</span><span class="sxs-lookup"><span data-stu-id="e59bc-122">The front end of the graph contains one output pin for each group.</span></span> <span data-ttu-id="e59bc-123">Suponiendo que haya especificado un perfil compatible, el escritor ASF debe tener un conjunto coincidente de clavijas de entrada.</span><span class="sxs-lookup"><span data-stu-id="e59bc-123">Assuming that you specified a compatible profile, the ASF Writer should have a matching set of input pins.</span></span> <span data-ttu-id="e59bc-124">Conecte cada pin de salida al pin de entrada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e59bc-124">Connect each output pin to the corresponding input pin.</span></span> <span data-ttu-id="e59bc-125">La forma más fácil de hacerlo es usar el método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) .</span><span class="sxs-lookup"><span data-stu-id="e59bc-125">The easiest way to do this is using the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="e59bc-126">En primer lugar, cree una nueva instancia del [generador de gráficos de captura](capture-graph-builder.md) e inicialícela con un puntero al administrador de gráficos de filtro:</span><span class="sxs-lookup"><span data-stu-id="e59bc-126">First, create a new instance of the [Capture Graph Builder](capture-graph-builder.md) and initialize it with a pointer to the Filter Graph Manager:</span></span>

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    <span data-ttu-id="e59bc-127">A continuación, recupere el PIN de salida para cada grupo mediante una llamada al método [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="e59bc-127">Next, retrieve the output pin for each group by calling the [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) method.</span></span> <span data-ttu-id="e59bc-128">Llame a **RenderStream** para conectar el PIN al escritor ASF:</span><span class="sxs-lookup"><span data-stu-id="e59bc-128">Call **RenderStream** to connect the pin to the ASF Writer:</span></span>

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a><span data-ttu-id="e59bc-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e59bc-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e59bc-130">Usar Windows Media con los servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="e59bc-130">Using Windows Media With DirectShow Editing Services</span></span>](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



