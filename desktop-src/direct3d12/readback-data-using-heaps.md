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
# <a name="read-back-data-via-a-buffer"></a>Lectura de datos a través de un búfer

Para volver a leer los datos de la GPU (por ejemplo, para capturar una captura de pantalla), use un montón readback. Esta técnica está relacionada con la [carga de datos de textura a través de un búfer](upload-and-readback-of-texture-data.md), con algunas diferencias.

- Para leer los datos, cree un montón con la **D3D12_HEAP_TYPE** establecida en [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type), en lugar de **D3D12_HEAP_TYPE_UPLOAD**.
- El recurso del montón de reserva de lectura siempre debe ser un **D3D12_RESOURCE_DIMENSION_BUFFER**.
- Puede usar una barrera para detectar cuándo finaliza la GPU el procesamiento de un fotograma (cuando finaliza la escritura de datos en el búfer de salida). Esto es importante, porque el método [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) no se sincroniza con la GPU (por el contrario, *el equivalente de* Direct3D 11 se sincroniza). Las llamadas de **mapa** de Direct3D 12 se comportan como si se llamara al equivalente de Direct3D 11 con la marca de NO_OVERWRITE.
- Una vez que los datos estén listos (incluida cualquier barrera de recursos necesaria), llame a [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) para que los datos de readback estén visibles para la CPU.

## <a name="code-example"></a>Ejemplo de código

En el ejemplo de código siguiente se muestra el esquema general del proceso de lectura de datos de la GPU a la CPU a través de un búfer.

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

Para una implementación completa de una rutina de captura de pantalla que lea la textura de destino de representación y la escriba en el disco como un archivo, consulte el *Kit de herramientas de DirectX para* [Screengrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp)de DX12.

## <a name="related-topics"></a>Temas relacionados

* [Subasignación dentro de un búfer](large-buffers.md)
