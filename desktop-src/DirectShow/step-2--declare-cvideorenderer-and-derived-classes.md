---
description: Este tema es el paso 2 del tutorial reproducción de audio y vídeo en DirectShow.
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 'Paso 2: declarar CVideoRenderer y clases derivadas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11474c57e70d8632a53ac0b858d61d2bddf1e86b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688085"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a><span data-ttu-id="b0321-103">Paso 2: declarar CVideoRenderer y clases derivadas</span><span class="sxs-lookup"><span data-stu-id="b0321-103">Step 2: Declare CVideoRenderer and Derived Classes</span></span>

<span data-ttu-id="b0321-104">Este tema es el paso 2 del tutorial [reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b0321-104">This topic is step 2 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="b0321-105">El código completo se muestra en el tema [ejemplo de reproducción de DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="b0321-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="b0321-106">DirectShow proporciona varios filtros diferentes que representan vídeo:</span><span class="sxs-lookup"><span data-stu-id="b0321-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="b0321-107">[**Filtro de representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="b0321-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="b0321-108">[Filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="b0321-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="b0321-109">[Filtro de representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="b0321-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="b0321-110">Para obtener más información sobre las diferencias entre estos filtros, consulte [elección del representador de vídeo adecuado](choosing-the-right-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="b0321-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="b0321-111">En este tutorial, se usa la siguiente clase abstracta para ajustar el filtro de representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b0321-111">In this tutorial, the following abstract class is used to wrap the video renderer filter.</span></span>


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



<span data-ttu-id="b0321-112">Notas:</span><span class="sxs-lookup"><span data-stu-id="b0321-112">Notes:</span></span>

-   <span data-ttu-id="b0321-113">El `HasVideo` método devuelve **true** si se ha creado el representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b0321-113">The `HasVideo` method returns **TRUE** if the video renderer has been created.</span></span>
-   <span data-ttu-id="b0321-114">El `AddToGraph` método agrega el representador de vídeo al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="b0321-114">The `AddToGraph` method adds the video renderer to the filter graph.</span></span>
-   <span data-ttu-id="b0321-115">El `FinalizeGraph` método finaliza el paso de creación de gráficos.</span><span class="sxs-lookup"><span data-stu-id="b0321-115">The `FinalizeGraph` method completes the graph-building step.</span></span>
-   <span data-ttu-id="b0321-116">El `UpdateVideoWindow` método actualiza el rectángulo de destino de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b0321-116">The `UpdateVideoWindow` method updates the video destination rectangle.</span></span>
-   <span data-ttu-id="b0321-117">El `Repaint` método vuelve a dibujar el fotograma de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="b0321-117">The `Repaint` method redraws the current video frame.</span></span>
-   <span data-ttu-id="b0321-118">El `DisplayModeChanged` método controla los cambios del modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="b0321-118">The `DisplayModeChanged` method handles display-mode changes.</span></span>

<span data-ttu-id="b0321-119">Cada uno de estos métodos se describe en detalle más adelante en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="b0321-119">Each of these methods is described in detail later in this tutorial.</span></span>

<span data-ttu-id="b0321-120">A continuación, declare una clase derivada para encapsular cada uno de los tres representadores de vídeo: EVR, VMR-9 y VMR-7.</span><span class="sxs-lookup"><span data-stu-id="b0321-120">Next, declare a derived class to wrap each of the three video renderers: the EVR, the VMR-9, and the VMR-7.</span></span>

### <a name="cevr-class"></a><span data-ttu-id="b0321-121">Clase CEVR</span><span class="sxs-lookup"><span data-stu-id="b0321-121">CEVR Class</span></span>

<span data-ttu-id="b0321-122">La `CEVR` clase administra el EVR.</span><span class="sxs-lookup"><span data-stu-id="b0321-122">The `CEVR` class manages the EVR.</span></span> <span data-ttu-id="b0321-123">Contiene un puntero a las interfaces [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) y [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) de EVR.</span><span class="sxs-lookup"><span data-stu-id="b0321-123">It contains a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) and [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interfaces of the EVR.</span></span>


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a><span data-ttu-id="b0321-124">Clase CVMR9</span><span class="sxs-lookup"><span data-stu-id="b0321-124">CVMR9 Class</span></span>

<span data-ttu-id="b0321-125">La `CVMR9` clase administra el VMR-9.</span><span class="sxs-lookup"><span data-stu-id="b0321-125">The `CVMR9` class manages the VMR-9.</span></span> <span data-ttu-id="b0321-126">Contiene un puntero a la interfaz [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="b0321-126">It contains a pointer to the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a><span data-ttu-id="b0321-127">Clase CVMR7</span><span class="sxs-lookup"><span data-stu-id="b0321-127">CVMR7 Class</span></span>

<span data-ttu-id="b0321-128">La `CVMR7` clase administra el VMR-7.</span><span class="sxs-lookup"><span data-stu-id="b0321-128">The `CVMR7` class manages the VMR-7.</span></span> <span data-ttu-id="b0321-129">Contiene un puntero a la interfaz [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="b0321-129">It contains a pointer to the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



<span data-ttu-id="b0321-130">Siguiente: [paso 3: compilar el gráfico de filtro](step-3--build-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="b0321-130">Next: [Step 3: Build the Filter Graph](step-3--build-the-filter-graph.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0321-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b0321-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0321-132">Reproducción de audio y vídeo en DirectShow</span><span class="sxs-lookup"><span data-stu-id="b0321-132">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="b0321-133">Usar el representador de mezcla de vídeo</span><span class="sxs-lookup"><span data-stu-id="b0321-133">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="b0321-134">Representación de vídeo</span><span class="sxs-lookup"><span data-stu-id="b0321-134">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
