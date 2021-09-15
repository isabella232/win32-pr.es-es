---
description: Este artículo contiene instrucciones para la estimación de vectores de movimiento con las API de vídeo de Direct3D 12.
ms.assetid: ''
title: Estimación de movimiento en vídeos de Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 7fdb6146e1bb77c673eb89d944bcf42a8babce49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569441"
---
# <a name="direct3d-video-motion-estimation"></a>Estimación de movimiento en vídeos de Direct3D

Este artículo contiene instrucciones para la estimación de vectores de movimiento con las API de vídeo de Direct3D 12. Esta característica se introdujo en Windows 10 versión 2004 (10.0; Compilación 19041). La estimación del movimiento es el proceso de determinar los vectores de movimiento que describen la transformación de una imagen 2D a otra. La estimación del movimiento es una parte esencial de la codificación de vídeo y se puede usar en algoritmos de conversión de velocidad de fotogramas. 

Aunque la estimación del movimiento se puede implementar con sombreadores, el propósito de la característica Estimación de movimiento D3D12 es exponer la aceleración de funciones fijas para la búsqueda de movimiento para descargar esta parte del trabajo desde 3D. A menudo, esto se produce en forma de exposición del estimador de movimiento del codificador de vídeo de GPU. El objetivo de la estimación de movimiento de D3D12 es el flujo óptico, pero debe tenerse en cuenta que los estimadores de movimiento del codificador se pueden optimizar para mejorar la compresión.


## <a name="checking-for-support"></a>Comprobación del soporte técnico

Determine la compatibilidad con todas las características de vídeo D3D llamando a [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) y pasando un valor de la enumeración [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) para especificar la característica para la que se está consultando compatibilidad. Para consultar el tamaño de bloque admitido y las resoluciones para un formato determinado, use el valor **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** y proporcione una estructura [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) para *pFeatureSupportData* como se muestra en el ejemplo siguiente. En la versión actual, solo se **admite** DXGI_FORMAT_NV12, por lo que es posible que el contenido de otros formatos deba convertirse en color y muestrear hacia abajo para usar la estimación de movimiento.

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a>Objeto de contexto del estimador de movimiento

El [objeto ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) mantiene el contexto para las operaciones de estimación de movimiento de vídeo. Cree una nueva instancia de esta interfaz llamando a [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).

El tamaño de bloque seleccionado, la precisión y el intervalo de tamaño admitidos dependerán de los valores admitidos por el hardware devuelto por la comprobación de **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** características. Puede seleccionar un intervalo de tamaño más pequeño del que admite el controlador. El intervalo de tamaño informa de los tamaños de asignación internos.

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



## <a name="storage-of-motion-vectors"></a>Storage de vectores de movimiento

[ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) almacena vectores de movimiento. Esta interfaz se usa en la [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) estructura devuelta desde [ID3D12VideoEncodeCommandList::EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion). La textura 2D de [](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) salida resuelta es una textura DXGI_FORMAT_R16G16_SINT donde R contiene el componente horizontal y G contiene el componente vertical del vector de movimiento. Esta textura tiene el tamaño para contener un par de componentes por bloque. Llame a [ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) para traducir la salida del vector de movimiento de **EstimateMotion** de los formatos dependientes del hardware a un formato coherente definido por las API de estimación de movimiento de vídeo.

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

 **ID3D12VideoMotionVectorHeap** también se usa para proporcionar vectores de sugerencia en [la D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) estructura.



## <a name="estimate-motion-in-a-command-list"></a>Estimar el movimiento en una lista de comandos

Llame a [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) desde [id3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) para invocar la operación de estimación de movimiento.

En el ejemplo siguiente se ejecuta la búsqueda de movimiento y se resuelven los vectores de movimiento en la textura 2D [con D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).  Los recursos D3D12 que se usan como entrada para **EstimateMotion** deben estar en el estado [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) y el recurso escrito en **ResolveMotionVectorHeap** debe estar en el [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) estado.

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


## <a name="protected-resources"></a>Recursos protegidos

La estimación del vector de movimiento de Direct3D 12 admite la lectura y escritura en recursos protegidos con DRM de hardware cuando el controlador lo admite. Si los recursos de entrada están protegidos por DRM de hardware, la salida también es un recurso protegido por DRM de hardware. Los métodos usados para crear el objeto de contexto de estimación de movimiento y el montón de vectores de  [movimiento, ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) e [ID3D12VideoDevice1::CreateVideoMotionVectorHeap,](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap)aceptan un [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) que se usa para administrar el acceso a los recursos protegidos. 

Use [ID3D12VideoMotionEstimator::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) e [ID3D12VideoMotionVectorHeap::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) para recuperar los objetos **ID3D12ProtectedResourceSession** proporcionados cuando se crearon los objetos.



## <a name="related-topics"></a>Temas relacionados

* [API de vídeo de Direct3D 12](direct3d-12-video-apis.md)
* [Media Foundation de programación](media-foundation-programming-guide.md)
