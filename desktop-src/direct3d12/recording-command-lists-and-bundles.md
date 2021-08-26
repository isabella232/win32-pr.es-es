---
title: Creación y grabación de listas de comandos y agrupaciones
description: En este tema se describen las listas y agrupaciones de comandos de grabación en aplicaciones de Direct3D 12. Tanto las listas de comandos como los paquetes permiten a las aplicaciones registrar llamadas de dibujo o de cambio de estado para su posterior ejecución en la unidad de procesamiento de gráficos (GPU).
ms.assetid: 0074B796-33A4-4AA1-A4E7-48A2A63F25B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480819cbd421b30cbf54a58578c02056d37d7e36bf2ead845c19e438df54cbb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850721"
---
# <a name="creating-and-recording-command-lists-and-bundles"></a>Creación y grabación de listas de comandos y agrupaciones

En este tema se describen las listas y agrupaciones de comandos de grabación en aplicaciones de Direct3D 12. Tanto las listas de comandos como los paquetes permiten a las aplicaciones registrar llamadas de dibujo o de cambio de estado para su posterior ejecución en la unidad de procesamiento de gráficos (GPU).

Más allá de las listas de comandos, la API aprovecha la funcionalidad presente en el hardware de GPU mediante la adición de un segundo nivel de listas de comandos, que se conocen como *agrupaciones*. El propósito de los paquetes es permitir que las aplicaciones a agrupar un pequeño número de comandos de API para su posterior ejecución. En el momento de la creación del paquete, el controlador realizará tanto procesamiento previo como sea posible para que se ejecuten más adelante. Los paquetes están diseñados para usarse y volver a usarse en cualquier número de veces. Por otro lado, las listas de comandos se suelen ejecutar solo una sola vez. Sin embargo, una *lista* de comandos se puede ejecutar varias veces (siempre y cuando la aplicación garantice que las ejecuciones anteriores se hayan completado antes de enviar nuevas ejecuciones).

Sin embargo, normalmente, la compilación de llamadas API en agrupaciones, llamadas API y agrupaciones en listas de comandos y listas de comandos en un solo fotograma, se muestra en el diagrama siguiente, y se indica la reutilización del lote **1** en la lista de comandos **1** y la lista de comandos **2,** y que los nombres de los métodos de API en el diagrama son igual que ejemplos, se pueden usar muchas llamadas API diferentes.

![compilar comandos, agrupaciones y listas de comandos en marcos](images/gpu-workitems.png)

Hay diferentes restricciones para crear y ejecutar agrupaciones y listas de comandos directas, y estas diferencias se observan en este tema.

## <a name="creating-command-lists"></a>Creación de listas de comandos

Las listas y agrupaciones de comandos directos se crean mediante una llamada a [**ID3D12Device::CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) o [**ID3D12Device4::CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1).

Use [**ID3D12Device4::CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1) para crear una lista de comandos cerrada, en lugar de crear una nueva lista y cerrarla inmediatamente. Esto evita la ineficacia de crear una lista con un asignador y PSO, pero no usarlos.

[**ID3D12Device::CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) toma los parámetros siguientes como entrada:

### <a name="d3d12_command_list_type"></a>TIPO DE LISTA DE COMANDOS D3D12 \_ \_ \_

La [**enumeración D3D12 \_ COMMAND LIST \_ \_ TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) indica el tipo de lista de comandos que se está creando. Puede ser una lista de comandos directos, una agrupación, una lista de comandos de proceso o una lista de comandos de copia.

### <a name="id3d12commandallocator"></a>ID3D12CommandAllocator

Un asignador de comandos permite a la aplicación administrar la memoria asignada para las listas de comandos. El asignador de comandos se crea mediante una [**llamada a CreateCommandAllocator.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator) Al crear una lista de comandos, el tipo de lista de comandos del asignador, especificado por [**D3D12 \_ COMMAND \_ LIST \_ TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type), debe coincidir con el tipo de lista de comandos que se va a crear. Un asignador determinado no se puede  asociar a más de una lista de comandos de grabación a la vez, aunque se puede usar un asignador de comandos para crear cualquier número de [**objetos GraphicsCommandList.**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)

Para reclamar la memoria asignada por un asignador de comandos, una aplicación llama a [**ID3D12CommandAllocator::Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset). Esto permite reutilizar el asignador para nuevas commmands, pero no reducirá su tamaño subyacente. Pero antes de hacerlo, la aplicación debe asegurarse de que la GPU ya no ejecuta ninguna lista de comandos asociada al asignador. De lo contrario, se producirá un error en la llamada. Además, tenga en cuenta que esta API no es de subproceso libre y, por lo tanto, no se puede llamar en el mismo asignador al mismo tiempo desde varios subprocesos.

### <a name="id3d12pipelinestate"></a>ID3D12PipelineState

Estado inicial de la canalización para la lista de comandos. En Microsoft Direct3D 12, la mayoría del estado de canalización de gráficos se establece en una lista de comandos mediante el [**objeto ID3D12PipelineState.**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) Una aplicación creará un gran número de ellos, normalmente durante la inicialización de la aplicación y, a continuación, el estado se actualiza cambiando el objeto de estado enlazado actualmente mediante [**ID3D12GraphicsCommandList::SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate). Para obtener más información sobre los objetos de estado de canalización, vea Administración del estado de canalización [de gráficos en Direct3D 12.](managing-graphics-pipeline-state-in-direct3d-12.md)

Tenga en cuenta que las agrupaciones no heredan el estado de canalización establecido por llamadas anteriores en listas de comandos directos que son sus familias.

Si este parámetro es NULL, se usa un estado predeterminado.

## <a name="recording-command-lists"></a>Grabación de listas de comandos

Inmediatamente después de crearse, las listas de comandos se encuentran en estado de grabación. También puede volver a usar una lista de comandos existente llamando a I [**D3D12GraphicsCommandList::Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset), que también deja la lista de comandos en estado de grabación. A [**diferencia de ID3D12CommandAllocator::Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset), puede llamar a **Reset** mientras se sigue ejecutando la lista de comandos. Un patrón típico es enviar una lista de comandos y restablecerla inmediatamente para reutilizar la memoria asignada para otra lista de comandos. Tenga en cuenta que solo una lista de comandos asociada a cada asignador de comandos puede estar en un estado de grabación a la vez.

Una vez que una lista de comandos está en estado de grabación, simplemente llame a los métodos de la interfaz [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) para agregar comandos a la lista. Muchos de estos métodos habilitan una funcionalidad común de Direct3D que será familiar para los desarrolladores de Microsoft Direct3D 11. Otras API son nuevas para Direct3D 12.

Después de agregar comandos a la lista de comandos, se realiza la transición de la lista de comandos fuera del estado de grabación mediante una llamada a [**Cerrar**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).

Los asignadores de comandos pueden crecer, pero no reducirse: se debe considerar la agrupación y la utilización de asignadores para aumentar la eficacia de la aplicación. Puede grabar varias listas en el mismo asignador antes de restablecerlo, siempre que solo una lista esté grabando en un asignador determinado a la vez. Puede visualizar cada lista como propietaria de una parte del asignador que indica qué [**id3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) se ejecutará.

Una estrategia de agrupación de asignadores simple debe tener como objetivo aproximadamente `numCommandLists * MaxFrameLatency` los asignadores. Por ejemplo, si registra 6 listas y permite hasta 3 fotogramas latentes, razonablemente podría esperar entre 18 y 20 asignadores. Una estrategia de agrupación más avanzada, que reutiliza los asignadores para varias listas en el mismo subproceso, podría tener como objetivo `numRecordingThreads * MaxFrameLatency` asignadores. Con el ejemplo anterior, si se registraron 2 listas en el subproceso A, 2 en el subproceso B, 1 en el subproceso C y 1 en el subproceso D, podría tener como objetivo realista entre 12 y 14 asignadores.

Use una barrera para determinar cuándo se puede reutilizar un asignador determinado.

Como las listas de comandos se pueden restablecer inmediatamente después de la ejecución, se pueden agrupar trivialmente, agregándolos de nuevo al grupo después de cada llamada a [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

## <a name="example"></a>Ejemplo

Los fragmentos de código siguientes ilustran la creación y grabación de una lista de comandos. Tenga en cuenta que este ejemplo incluye las siguientes características de Direct3D 12:

-   Objetos de estado de canalización: se usan para establecer la mayoría de los parámetros de estado de la canalización de representación desde dentro de una lista de comandos. Para obtener más información, vea [Administración del estado de canalización de gráficos en Direct3D 12.](managing-graphics-pipeline-state-in-direct3d-12.md)
-   Montón de descriptor: las aplicaciones usan montones de descriptores para administrar el enlace de canalización a recursos de memoria.
-   Barrera de recursos: se usa para administrar la transición de recursos de un estado a otro, como desde una vista de destino de representación a una vista de recursos de sombreador. Para más información, consulte [Uso de barreras de recursos para sincronizar estados de recursos.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

Por ejemplo,


```C++
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



Una vez creada y registrada una lista de comandos, se puede ejecutar mediante una cola de comandos. Para obtener más información, vea [Ejecutar y sincronizar listas de comandos](executing-and-synchronizing-command-lists.md).

## <a name="reference-counting"></a>Recuento de referencias

La mayoría de las API de D3D12 siguen usando el recuento de referencias siguiendo las convenciones COM. Una excepción importante a esto son las API de lista de comandos gráficos D3D12. Todas las API de [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) no incluyen referencias a los objetos pasados a esas API. Esto significa que las aplicaciones son responsables de garantizar que nunca se envía una lista de comandos para su ejecución que haga referencia a un recurso destructor.

## <a name="command-list-errors"></a>Errores de la lista de comandos

La mayoría de las API [**de ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) no devuelven errores. Los errores detectados durante la creación de la lista de comandos se aplazan [**hasta ID3D12GraphicsCommandList::Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close). La única excepción es DXGI \_ ERROR \_ DEVICE \_ REMOVED, que se aplaza aún más. Tenga en cuenta que esto es diferente de D3D11, donde muchos errores de validación de parámetros se descartan de forma silenciosa y nunca se devuelven al autor de la llamada.

Las aplicaciones pueden esperar ver errores DXGI \_ DEVICE REMOVED en las siguientes llamadas \_ API:

-   Cualquier método de creación de recursos
-   [**ID3D12Resource::Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)
-   [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**GetDeviceRemovedReason**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)

## <a name="command-list-api-restrictions"></a>Restricciones de API de la lista de comandos

Solo se puede llamar a algunas API de lista de comandos en determinados tipos de listas de comandos. En la tabla siguiente se muestra qué API de lista de comandos son válidas para llamar a en cada tipo de lista de comandos. También muestra qué API son válidas para llamar a en un paso de representación [**D3D12.**](./direct3d-12-render-passes.md) 

| Nombre de la API                                         | Gráficos | Proceso | Copiar | Bundle | En Paso de representación |
|--------------------------------------------------|:--------:|:-------:|:----:|:------:|:--------------:|
| AtomicCopyBufferUINT                             | ✓        | ✓       | ✓    |        |                |
| AtomicCopyBufferUINT64                           | ✓        | ✓       | ✓    |        |                |
| BeginEvent                                       | ✓        |         |      |        | ✓              |
| BeginRenderPass                                  | ✓        |         |      |        |                |
| BuildRaytracingAccelerationStructure             | ✓        | ✓       |      |        |                |
| ClearDepthStencilView                            | ✓        |         |      |        |                |
| ClearRenderTargetView                            | ✓        |         |      |        |                |
| ClearState                                       | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewFloat                    | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewUint                     | ✓        | ✓       |      |        |                |
| CopyBufferRegion                                 | ✓        | ✓       | ✓    |        |                |
| CopyRaytracingAccelerationStructure              | ✓        | ✓       |      |        |                |
| CopyResource                                     | ✓        | ✓       | ✓    |        |                |
| CopyTextureRegion                                | ✓        | ✓       | ✓    |        |                |
| CopyTiles                                        | ✓        | ✓       | ✓    |        |                |
| DiscardResource                                  | ✓        | ✓       |      |        |                |
| Dispatch                                         | ✓        | ✓       |      | ✓      |                |
| DispatchRays                                     | ✓        | ✓       |      | ✓      |                |
| DrawIndexedInstanced                             | ✓        |         |      | ✓      | ✓              |
| DrawInstanced                                    | ✓        |         |      | ✓      | ✓              |
| EmitRaytracingAccelerationStructurePostbuildInfo | ✓        | ✓       |      |        |                |
| EndQuery                                         | ✓        | ✓       | ✓    |        | ✓              |
| EndRenderPass                                    | ✓        |         |      |        | ✓              |
| ExecuteBundle                                    | ✓        |         |      |        | ✓              |
| ExecuteIndirect                                  | ✓        | ✓       |      | ✓      | ✓              |
| ExecuteMetaCommand                               | ✓        | ✓       |      |        |                |
| IASetIndexBuffer                                 | ✓        |         |      | ✓      | ✓              |
| IASetPrimitiveTopology                           | ✓        |         |      | ✓      | ✓              |
| IASetVertexBuffers                               | ✓        |         |      | ✓      | ✓              |
| InitializeMetaCommand                            | ✓        | ✓       |      |        |                |
| OMSetBlendFactor                                 | ✓        |         |      | ✓      | ✓              |
| OMSetDepthBounds                                 | ✓        |         |      | ✓      | ✓              |
| OMSetRenderTargets                               | ✓        |         |      |        |                |
| OMSetStencilRef                                  | ✓        |         |      | ✓      | ✓              |
| ResolveQueryData                                 | ✓        | ✓       | ✓    |        |                |
| ResolveSubresource                               | ✓        |         |      |        |                |
| ResolveSubresourceRegion                         | ✓        |         |      |        |                |
| ResourceBarrier                                  | ✓        | ✓       | ✓    |        | ✓              |
| RSSetScissorRects                                | ✓        |         |      |        | ✓              |
| RSSetShadingRate                                 | ✓        |         |      | ✓      | ✓              |
| RSSetShadingRateImage                            | ✓        |         |      | ✓      | ✓              |
| RSSetViewports                                   | ✓        |         |      |        | ✓              |
| SetComputeRoot32BitConstant                      | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRoot32BitConstants                     | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootConstantBufferView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootDescriptorTable                    | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootShaderResourceView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootSignature                          | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootUnorderedAccessView                | ✓        | ✓       |      | ✓      | ✓              |
| SetDescriptorHeaps                               | ✓        | ✓       |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstant                     | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstants                    | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootConstantBufferView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootDescriptorTable                   | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootShaderResourceView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootSignature                         | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootUnorderedAccessView               | ✓        |         |      | ✓      | ✓              |
| SetPipelineState                                 | ✓        | ✓       |      | ✓      | ✓              |
| SetPipelineState1                                | ✓        | ✓       |      | ✓      |                |
| SetPredication                                   | ✓        | ✓       |      |        | ✓              |
| SetProtectedResourceSession                      | ✓        | ✓       | ✓    |        |                |
| SetSamplePositions                               | ✓        |         |      | ✓      | ✓              |
| SetViewInstanceMask                              | ✓        |         |      | ✓      | ✓              |
| SOSetTargets                                     | ✓        |         |      |        | ✓              |
| WriteBufferImmediate                             | ✓        | ✓       | ✓    | ✓      | ✓              |

## <a name="bundle-restrictions"></a>Restricciones de agrupación

Las restricciones permiten a los controladores de Direct3D 12 realizar la mayor parte del trabajo asociado a los paquetes en tiempo de registro, lo que permite ejecutar la API [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) con una sobrecarga baja. Todos los objetos de estado de canalización a los que hace referencia una agrupación deben tener los mismos formatos de destino de representación, formato de búfer de profundidad y descripciones de ejemplo.

Las siguientes llamadas API de lista de comandos no se permiten en las listas de comandos creadas con el tipo: D3D12 \_ COMMAND \_ LIST TYPE \_ \_ BUNDLE:

-   Cualquier método Clear
-   Cualquier método Copy
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
-   [**ResolveSubresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)
-   [**BeginEvent**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
-   [**EndQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
-   [**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)
-   [**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
-   [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)
-   [**RSSetScissorRects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)

Se puede llamar a [**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) en una agrupación, pero los montones del descriptor de agrupación deben coincidir con el montón del descriptor de lista de comandos que realiza la llamada.

Si se llama a cualquiera de estas API en una agrupación, el tiempo de ejecución quitará la llamada. La capa de depuración emitirá un error cada vez que esto ocurra.

## <a name="related-topics"></a>Temas relacionados

[Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md)