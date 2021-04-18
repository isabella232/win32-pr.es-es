---
description: Este artículo contiene instrucciones para la estimación del vector de movimiento con las API de vídeo de Direct3D 12.
ms.assetid: ''
title: Estimación de movimiento en vídeos de Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 7fdb6146e1bb77c673eb89d944bcf42a8babce49
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "105721179"
---
# <a name="direct3d-video-motion-estimation"></a><span data-ttu-id="a1dd2-103">Estimación de movimiento en vídeos de Direct3D</span><span class="sxs-lookup"><span data-stu-id="a1dd2-103">Direct3D video motion estimation</span></span>

<span data-ttu-id="a1dd2-104">Este artículo contiene instrucciones para la estimación del vector de movimiento con las API de vídeo de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-104">This article contains guidance for motion vector estimation with Direct3D 12 video APIs.</span></span> <span data-ttu-id="a1dd2-105">Esta característica se presentó en Windows 10, versión 2004 (10,0; Compilación 19041).</span><span class="sxs-lookup"><span data-stu-id="a1dd2-105">This feature was introduced in Windows 10, version 2004 (10.0; Build 19041).</span></span> <span data-ttu-id="a1dd2-106">La estimación de movimiento es el proceso por el que se determinan los vectores de movimiento que describen la transformación de una imagen 2D a otra.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-106">Motion estimation is the process of determining motion vectors that describe the transformation from one 2D image to another.</span></span> <span data-ttu-id="a1dd2-107">La estimación de movimiento es una parte esencial de la codificación de vídeo y se puede usar en algoritmos de conversión de velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-107">Motion estimation is an essential part of video encoding and can be used in frame rate conversion algorithms.</span></span> 

<span data-ttu-id="a1dd2-108">Aunque la estimación de movimiento se puede implementar con sombreadores, el propósito de la característica de estimación de movimiento D3D12 es exponer la aceleración de funciones fijas para la búsqueda de movimiento y descargar esta parte del trabajo de 3D.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-108">While motion estimation can be implemented with shaders, the purpose of the D3D12 Motion Estimation feature is to expose fixed function acceleration for motion searching to offload this part of the work from 3D.</span></span> <span data-ttu-id="a1dd2-109">A menudo, esto viene en forma de exponer el estimador de movimiento del codificador de vídeo GPU.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-109">Often this comes in the form of exposing the GPU video encoder motion estimator.</span></span> <span data-ttu-id="a1dd2-110">El objetivo de la estimación de movimiento de D3D12 es el flujo óptico, pero debe tenerse en cuentan que los estimadores de movimiento del codificador pueden estar optimizados para mejorar la compresión.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-110">The goal of D3D12 Motion estimation is optical flow, but it should be noted that encoder motion estimators may be optimized for improving compression.</span></span>


## <a name="checking-for-support"></a><span data-ttu-id="a1dd2-111">Comprobando la compatibilidad</span><span class="sxs-lookup"><span data-stu-id="a1dd2-111">Checking for Support</span></span>

<span data-ttu-id="a1dd2-112">Determine la compatibilidad con todas las características de vídeo D3D llamando a [ID3D12VideoDevice:: CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) y pasando un valor de la enumeración [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) para especificar la característica para la que se consulta la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-112">Determine support for all D3D video features by calling [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) and passing in a value from the [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify the feature for which support is being queried.</span></span> <span data-ttu-id="a1dd2-113">Para consultar el tamaño de bloque y las resoluciones admitidos para un formato determinado, use el valor **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** y proporcione una estructura de [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) para *pFeatureSupportData* como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-113">To query the supported block size and resolutions for a given format, use the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** value and supply a [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) structure for the *pFeatureSupportData* as shown in the example below.</span></span> <span data-ttu-id="a1dd2-114">En la versión actual, solo se admite **DXGI_FORMAT_NV12** , por lo que es posible que sea necesario convertir el color en otros formatos y Downsampled para usar la estimación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-114">In the current release, only **DXGI_FORMAT_NV12** is supported, so content in other formats may need to be color converted and downsampled to use motion estimation.</span></span>

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a><span data-ttu-id="a1dd2-115">Objeto de contexto del estimador de movimiento</span><span class="sxs-lookup"><span data-stu-id="a1dd2-115">The motion estimator context object</span></span>

<span data-ttu-id="a1dd2-116">El objeto [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) mantiene el contexto de las operaciones de estimación de movimiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-116">The [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) object maintains context for video motion estimation operations.</span></span> <span data-ttu-id="a1dd2-117">Cree una nueva instancia de esta interfaz mediante una llamada a [ID3D12VideoDevice1:: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span><span class="sxs-lookup"><span data-stu-id="a1dd2-117">Create a new instance of this interface by calling [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span></span>

<span data-ttu-id="a1dd2-118">El tamaño de bloque seleccionado, la precisión y el intervalo de tamaño admitido dependerían de los valores admitidos por el hardware devuelto por la comprobación de características de **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** .</span><span class="sxs-lookup"><span data-stu-id="a1dd2-118">The selected block size, precision, and supported size range would depend on values supported by hardware returned from the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** feature check.</span></span> <span data-ttu-id="a1dd2-119">Puede seleccionar un intervalo de tamaño inferior al admitido por el controlador.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-119">You can select a smaller size range than the driver supports.</span></span> <span data-ttu-id="a1dd2-120">El intervalo de tamaño informa de los tamaños de asignación internos.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-120">Size range informs internal allocation sizes.</span></span>

```c++
D3D12_VIDEO_MOTION_ESTIMATOR_DESC motionEstimatorDesc = { 
    0, //NodeIndex
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionEstimator> spVideoMotionEstimator;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionEstimator(
    &motionEstimatorDesc, 
    nullptr,
    IID_PPV_ARGS(&spVideoMotionEstimator)));
```



## <a name="storage-of-motion-vectors"></a><span data-ttu-id="a1dd2-121">Almacenamiento de vectores de movimiento</span><span class="sxs-lookup"><span data-stu-id="a1dd2-121">Storage of motion vectors</span></span>

<span data-ttu-id="a1dd2-122">[ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) almacena vectores de movimiento.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-122">The [ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) stores motion vectors.</span></span> <span data-ttu-id="a1dd2-123">La estructura [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) devuelta por [ID3D12VideoEncodeCommandList:: EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion)usa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-123">This interface is used by the [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) structure returned from [ID3D12VideoEncodeCommandList::EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion).</span></span> <span data-ttu-id="a1dd2-124">La textura 2D de salida resuelta es una [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) textura donde R contiene el componente horizontal y G contiene el componente vertical del vector de movimiento.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-124">The resolved output 2D texture is a [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) texture where R holds the horizontal component and G holds the vertical component of the motion vector.</span></span> <span data-ttu-id="a1dd2-125">Esta textura tiene un tamaño que contiene un par de componentes por bloque.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-125">This texture is sized to hold one pair of components per block.</span></span> <span data-ttu-id="a1dd2-126">Llame a [ID3D12VideoEncodeCommandList:: ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) para trasladar la salida del vector de movimiento de **EstimateMotion** desde formatos dependientes del hardware a un formato coherente definido por las API de estimación de movimiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-126">Call [ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) to translates the motion vector output of **EstimateMotion** from hardware-dependent formats into a consistent format defined by the video motion estimation APIs.</span></span>

```c++
D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC MotionVectorHeapDesc = { 
    0, // NodeIndex 
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionVectorHeap> spVideoMotionVectorHeap;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionVectorHeap(
    &MotionVectorHeapDesc, 
    nullptr, 
    IID_PPV_ARGS(&spVideoMotionVectorHeap)));
```

```cpp
    CD3DX12_RESOURCE_DESC::Tex2D(
        DXGI_FORMAT_R16G16_SINT, 
        Align(1920, 16) / 16, // This example uses a 16x16 block size. Pixel width and height
        Align(1080, 16) / 16, // are adjusted to store the vectors for those blocks.
        1, // ArraySize
        1  // MipLevels
        );

    ATL::CComPtr< ID3D12Resource > spResolvedMotionVectors;
    VERIFY_SUCCEEDED(pDevice->CreateCommittedResource(
        &Properties,
        D3D12_HEAP_FLAG_NONE,
        &resolvedMotionVectorDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        IID_PPV_ARGS(&spResolvedMotionVectors)));
```

 <span data-ttu-id="a1dd2-127">**ID3D12VideoMotionVectorHeap** también se utiliza para proporcionar vectores de sugerencia en la estructura de [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) .</span><span class="sxs-lookup"><span data-stu-id="a1dd2-127">**ID3D12VideoMotionVectorHeap** is also used to supply hint vectors in the [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) structure.</span></span>



## <a name="estimate-motion-in-a-command-list"></a><span data-ttu-id="a1dd2-128">Movimiento de estimación en una lista de comandos</span><span class="sxs-lookup"><span data-stu-id="a1dd2-128">Estimate motion in a command list</span></span>

<span data-ttu-id="a1dd2-129">Llame a [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) desde un [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) para invocar la operación de estimación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-129">Call the [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) from a [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) to invoke the motion estimation operation.</span></span>

<span data-ttu-id="a1dd2-130">En el ejemplo siguiente se ejecuta la búsqueda de movimiento y se resuelven los vectores de movimiento en la textura 2D con [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span><span class="sxs-lookup"><span data-stu-id="a1dd2-130">The example below executes the motion search and resolves the motion vectors to the 2D texture with [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>  <span data-ttu-id="a1dd2-131">Los recursos de D3D12 utilizados como entrada para **EstimateMotion** deben estar en el estado [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) y el recurso escrito en **ResolveMotionVectorHeap** debe estar en el estado [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .</span><span class="sxs-lookup"><span data-stu-id="a1dd2-131">D3D12 Resources used as input to **EstimateMotion** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state and the resource written to by **ResolveMotionVectorHeap** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state.</span></span>

```cpp
const D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT outputArgs = {spVideoMotionVectorHeap};

const D3D12_VIDEO_MOTION_ESTIMATOR_INPUT inputArgs = {
    spCurrentResource,
    0,
    spReferenceResource,
    0,
    nullptr // pHintMotionVectorHeap
    };

spCommandList->EstimateMotion(spVideoMotionEstimator, &outputArgs, &inputArgs);

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT outputArgs = { 
    spResolvedMotionVectors,
    {}};

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT inputArgs = {
    spVideoMotionVectorHeap,
    1920,
    1080
    };

spCommandList->ResolveMotionVectorHeap(&outputArgs, &inputArgs);
        
VERIFY(spCommandList->Close());

// Execute Commandlist.
ID3D12CommandList *ppCommandLists[1] = { spCommandList.p };
spCommandQueue->ExecuteCommandLists(1, ppCommandLists);
```


## <a name="protected-resources"></a><span data-ttu-id="a1dd2-132">Recursos protegidos</span><span class="sxs-lookup"><span data-stu-id="a1dd2-132">Protected resources</span></span>

<span data-ttu-id="a1dd2-133">La estimación del vector de movimiento de Direct3D 12 admite la lectura y escritura de recursos protegidos de DRM de hardware cuando el controlador lo admite.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-133">Direct3D 12 motion vector estimation supports reading from and writing to hardware DRM protected resources when supported by the driver.</span></span> <span data-ttu-id="a1dd2-134">Si los recursos de entrada están protegidos con DRM de hardware, la salida también es un recurso protegido por DRM de hardware. Los métodos que se usan para crear el objeto de contexto de estimación de movimiento y el montón de vector de movimiento,  [ID3D12VideoDevice1:: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) y [ID3D12VideoDevice1:: CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), ambos aceptan un [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) que se usa para administrar el acceso a los recursos protegidos.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-134">If the input resources are hardware DRM protected, the output is also a hardware DRM protected resource.The methods used to create the motion estimation context object and the motion vector heap,  [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) and [ID3D12VideoDevice1::CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), both accept a [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) that is used to manage access to protected resources.</span></span> 

<span data-ttu-id="a1dd2-135">Use [ID3D12VideoMotionEstimator:: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) y [ID3D12VideoMotionVectorHeap:: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) para recuperar los objetos **ID3D12ProtectedResourceSession** proporcionados cuando se crearon los objetos.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-135">Use [ID3D12VideoMotionEstimator::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) and [ID3D12VideoMotionVectorHeap::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) to retrieve the **ID3D12ProtectedResourceSession** objects provided when the objects were created.</span></span>



## <a name="related-topics"></a><span data-ttu-id="a1dd2-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1dd2-136">Related topics</span></span>

* [<span data-ttu-id="a1dd2-137">API de vídeo de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a1dd2-137">Direct3D 12 Video APIs</span></span>](direct3d-12-video-apis.md)
* [<span data-ttu-id="a1dd2-138">Guía de programación de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a1dd2-138">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
