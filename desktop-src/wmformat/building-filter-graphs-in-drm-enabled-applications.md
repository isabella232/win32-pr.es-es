---
title: Generar gráficos de filtro en aplicaciones de DRM-Enabled
description: Generar gráficos de filtro en aplicaciones de DRM-Enabled
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- SDK de Windows Media Format, crear gráficos de filtros
- Windows Media Format SDK, DirectShow
- SDK de Windows Media Format, aplicaciones habilitadas para DRM
- Advanced Systems Format (ASF), generar gráficos de filtros
- ASF (formato de sistemas avanzados), crear gráficos de filtros
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), aplicaciones habilitadas para DRM
- ASF (formato de sistemas avanzados), aplicaciones habilitadas para DRM
- DirectShow, crear gráficos de filtros
- DirectShow, aplicaciones habilitadas para DRM
- Administración de derechos digitales (DRM), DirectShow
- DRM (administración de derechos digitales), DirectShow
- Administración de derechos digitales (DRM), crear gráficos de filtros
- DRM (administración de derechos digitales), crear gráficos de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944037a00c208e1427d3d19aa6c9dc0a352ec5fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358705"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a><span data-ttu-id="f01c0-118">Generar gráficos de filtro en aplicaciones de DRM-Enabled</span><span class="sxs-lookup"><span data-stu-id="f01c0-118">Building Filter Graphs in DRM-Enabled Applications</span></span>

<span data-ttu-id="f01c0-119">Si la aplicación de DirectShow admite la reproducción de archivos protegidos con DRM, por lo general no debe usar **RenderFile** para crear el gráfico de filtros porque no hay ninguna manera de especificar qué derechos de DRM solicita antes de que se abra el archivo.</span><span class="sxs-lookup"><span data-stu-id="f01c0-119">If your DirectShow application supports playback of DRM-protected files, then you generally should not use **RenderFile** to create the filter graph because there is no way to specify which DRM rights you are requesting before the file is opened.</span></span> <span data-ttu-id="f01c0-120">De forma predeterminada, el lector ASF de WM solicita únicamente los derechos de reproducción.</span><span class="sxs-lookup"><span data-stu-id="f01c0-120">The WM ASF Reader by default asks for only playback rights.</span></span> <span data-ttu-id="f01c0-121">El filtro no se agrega al gráfico y, por lo tanto, no lo pueden detectar las aplicaciones hasta que un archivo se abre correctamente.</span><span class="sxs-lookup"><span data-stu-id="f01c0-121">The filter is not added to the graph, and is therefore not discoverable by applications, until a file is successfully opened.</span></span>

<span data-ttu-id="f01c0-122">Para compilar un gráfico de reproducción habilitado con DRM mediante el [lector ASF de WM](wm-asf-reader-filter.md), debe crear una instancia del filtro mediante **CoCreateInstance**, agregarlo al gráfico de filtros mediante **IGraphBuilder:: addFilter**, configurarlo y, a continuación, representar sus clavijas de salida.</span><span class="sxs-lookup"><span data-stu-id="f01c0-122">To build a DRM-enabled playback graph using the [WM ASF Reader](wm-asf-reader-filter.md), you must instantiate the filter using **CoCreateInstance**, add it to the filter graph using **IGraphBuilder::AddFilter**, configure it, and then render its output pins.</span></span> <span data-ttu-id="f01c0-123">Esta técnica se muestra en el ejemplo PlayWndASF.</span><span class="sxs-lookup"><span data-stu-id="f01c0-123">This technique is demonstrated in the PlayWndASF sample.</span></span> <span data-ttu-id="f01c0-124">Al compilar el gráfico de esta manera, ya tiene el puntero **IBaseFilter** que se puede usar para llamar a **QueryService** para obtener **IWMDRMWriter**.</span><span class="sxs-lookup"><span data-stu-id="f01c0-124">When you build the graph in this way, you already have the **IBaseFilter** pointer that can be used to call **QueryService** to obtain **IWMDRMWriter**.</span></span> <span data-ttu-id="f01c0-125">Sin embargo, esta interfaz no está disponible hasta que el lector ASF de WM crea internamente el objeto lector del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="f01c0-125">However, this interface is not available until the Windows Media Format SDK reader object is created internally by the WM ASF Reader.</span></span> <span data-ttu-id="f01c0-126">La primera oportunidad que tiene la aplicación para establecer derechos DRM es en su \_ controlador de eventos WMT no \_ Rights \_ ex, tal como se muestra en este fragmento de código:</span><span class="sxs-lookup"><span data-stu-id="f01c0-126">The first opportunity the application has to set DRM rights is in its WMT\_NO\_RIGHTS\_EX event handler, as shown in this code snippet:</span></span>


```C++
case WMT_NO_RIGHTS_EX:

    IServiceProvider *pServiceProvider;
    IWMDRMReader pWMDRMReader;
    JIF(g_pReader->QueryInterface(IID_IServiceProvider, (void **) &pServiceProvider));
    JIF(pServiceProvider->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader)); 
    SAFE_RELEASE(pServiceProvider);

    // Set the rights we want for this file. These are the actions we 
    // might want to perform on the file. Here we ask for two rights only.
    // In a real application you should enable users to select which 
    // rights they want.
    hr = pWMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
        BYTE*) wszRights, (sizeof(wszRights) / sizeof(wszRights[0])) * 2);
    SAFE_RELEASE(pWMDRMReader);
    if (FAILED(hr))
    {
       Msg(TEXT("SetDRMProperty Failed!  hr=0x%x\n"), hr);
       return hr;
    }
    // Now proceed with license acqusition.
    if( pEventData->pData )
    {
        hr = HandleNoRightsEx(pEventData->hrStatus, 
        (WM_GET_LICENSE_DATA *)pEventData->pData);
    }
    else
    {
         hr = E_FAIL;
    }
    break;

```



## <a name="related-topics"></a><span data-ttu-id="f01c0-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f01c0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f01c0-128">**Características de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="f01c0-128">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="f01c0-129">**Lista de atributos de DRM**</span><span class="sxs-lookup"><span data-stu-id="f01c0-129">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="f01c0-130">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="f01c0-130">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="f01c0-131">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="f01c0-131">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="f01c0-132">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="f01c0-132">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[<span data-ttu-id="f01c0-133">**IWMDRMWriter**</span><span class="sxs-lookup"><span data-stu-id="f01c0-133">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




