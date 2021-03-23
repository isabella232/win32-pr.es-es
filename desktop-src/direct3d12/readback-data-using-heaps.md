---
title: Lectura de datos a través de un búfer
description: Para volver a leer los datos de la GPU (por ejemplo, para capturar una captura de pantalla), use un montón readback.
ms.assetid: 2F515B2C-3317-4AA8-81E1-7762ED895F77
ms.localizationpriority: high
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: 752d97d517a48a38adabc7c8fe51d11d47c1d8d3
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/05/2021
ms.locfileid: "104549149"
---
# <a name="read-back-data-via-a-buffer"></a><span data-ttu-id="bd78b-103">Lectura de datos a través de un búfer</span><span class="sxs-lookup"><span data-stu-id="bd78b-103">Read back data via a buffer</span></span>

<span data-ttu-id="bd78b-104">Para volver a leer los datos de la GPU (por ejemplo, para capturar una captura de pantalla), use un montón readback.</span><span class="sxs-lookup"><span data-stu-id="bd78b-104">To read back data from the GPU (for example, to capture a screen shot), you use a readback heap.</span></span> <span data-ttu-id="bd78b-105">Esta técnica está relacionada con la [carga de datos de textura a través de un búfer](upload-and-readback-of-texture-data.md), con algunas diferencias.</span><span class="sxs-lookup"><span data-stu-id="bd78b-105">This technique is related to [Uploading texture data via a buffer](upload-and-readback-of-texture-data.md), with a few differences.</span></span>

- <span data-ttu-id="bd78b-106">Para leer los datos, cree un montón con la **D3D12_HEAP_TYPE** establecida en [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type), en lugar de **D3D12_HEAP_TYPE_UPLOAD**.</span><span class="sxs-lookup"><span data-stu-id="bd78b-106">To read back data, you create a heap with the **D3D12_HEAP_TYPE** set to [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type), instead of **D3D12_HEAP_TYPE_UPLOAD**.</span></span>
- <span data-ttu-id="bd78b-107">El recurso del montón de reserva de lectura siempre debe ser un **D3D12_RESOURCE_DIMENSION_BUFFER**.</span><span class="sxs-lookup"><span data-stu-id="bd78b-107">The resource on the read-back heap must always be a **D3D12_RESOURCE_DIMENSION_BUFFER**.</span></span>
- <span data-ttu-id="bd78b-108">Puede usar una barrera para detectar cuándo finaliza la GPU el procesamiento de un fotograma (cuando finaliza la escritura de datos en el búfer de salida).</span><span class="sxs-lookup"><span data-stu-id="bd78b-108">You use a fence to detect when the GPU completes processing a frame (when it is done writing data into your output buffer).</span></span> <span data-ttu-id="bd78b-109">Esto es importante, porque el método [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) no se sincroniza con la GPU (por el contrario, *el equivalente de* Direct3D 11 se sincroniza).</span><span class="sxs-lookup"><span data-stu-id="bd78b-109">This is important, because the [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) method doesn't synchronize with the GPU (conversely, the Direct3D 11 equivalent *does* synchronize).</span></span> <span data-ttu-id="bd78b-110">Las llamadas de **mapa** de Direct3D 12 se comportan como si se llamara al equivalente de Direct3D 11 con la marca de NO_OVERWRITE.</span><span class="sxs-lookup"><span data-stu-id="bd78b-110">Direct3D 12 **Map** calls behave as if you called the Direct3D 11 equivalent with the NO_OVERWRITE flag.</span></span>
- <span data-ttu-id="bd78b-111">Una vez que los datos estén listos (incluida cualquier barrera de recursos necesaria), llame a [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) para que los datos de readback estén visibles para la CPU.</span><span class="sxs-lookup"><span data-stu-id="bd78b-111">After the data is ready (including any necessary resource barrier), call [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) to make the readback data visible to the CPU.</span></span>

## <a name="code-example"></a><span data-ttu-id="bd78b-112">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="bd78b-112">Code example</span></span>

<span data-ttu-id="bd78b-113">En el ejemplo de código siguiente se muestra el esquema general del proceso de lectura de datos de la GPU a la CPU a través de un búfer.</span><span class="sxs-lookup"><span data-stu-id="bd78b-113">The code example below shows the general outline of the process of reading back data from the GPU to the CPU via a buffer.</span></span>

```cppwinrt

// The output buffer (created below) is on a default heap, so only the GPU can access it.

D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
D3D12_RESOURCE_DESC outputBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize, D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS) };
winrt::com_ptr<::ID3D12Resource> outputBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &defaultHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &outputBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(outputBuffer),
    outputBuffer.put_void()));

// The readback buffer (created below) is on a readback heap, so that the CPU can access it.

D3D12_HEAP_PROPERTIES readbackHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_READBACK) };
D3D12_RESOURCE_DESC readbackBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize) };
winrt::com_ptr<::ID3D12Resource> readbackBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &readbackHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &readbackBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(readbackBuffer),
    readbackBuffer.put_void()));

{
    D3D12_RESOURCE_BARRIER outputBufferResourceBarrier
    {
        CD3DX12_RESOURCE_BARRIER::Transition(
            outputBuffer.get(),
            D3D12_RESOURCE_STATE_COPY_DEST,
            D3D12_RESOURCE_STATE_COPY_SOURCE)
    };
    commandList->ResourceBarrier(1, &outputBufferResourceBarrier);
}

commandList->CopyResource(readbackBuffer.get(), outputBuffer.get());

// Code goes here to close, execute (and optionally reset) the command list, and also
// to use a fence to wait for the command queue.

// The code below assumes that the GPU wrote FLOATs to the buffer.

D3D12_RANGE readbackBufferRange{ 0, outputBufferSize };
FLOAT * pReadbackBufferData{};
winrt::check_hresult(
    readbackBuffer->Map
    (
        0,
        &readbackBufferRange,
        reinterpret_cast<void**>(&pReadbackBufferData)
    )
);

// Code goes here to access the data via pReadbackBufferData.

D3D12_RANGE emptyRange{ 0, 0 };
readbackBuffer->Unmap
(
    0,
    &emptyRange
);
```

<span data-ttu-id="bd78b-114">Para una implementación completa de una rutina de captura de pantalla que lea la textura de destino de representación y la escriba en el disco como un archivo, consulte el *Kit de herramientas de DirectX para* [Screengrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp)de DX12.</span><span class="sxs-lookup"><span data-stu-id="bd78b-114">For a full implementation of a screenshot routine that reads the render target texture, and writes it to disk as a file, see *DirectX Tool Kit for DX12*'s [ScreenGrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd78b-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd78b-115">Related topics</span></span>

* [<span data-ttu-id="bd78b-116">Subasignación dentro de un búfer</span><span class="sxs-lookup"><span data-stu-id="bd78b-116">Suballocation within a buffer</span></span>](large-buffers.md)
