---
title: Crear montones de descriptor
description: Para crear y configurar un montón de descriptores, debe seleccionar un tipo de montón de descriptores, determinar el número de descriptores que contiene y establecer marcas que indiquen si es visible para la CPU o el sombreador.
ms.assetid: 58677023-692C-4BA4-90B7-D568F3DD3F73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e472a0749634d5cbaa9cbf1cde5e11202d4c4f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549089"
---
# <a name="creating-descriptor-heaps"></a>Crear montones de descriptor

Para crear y configurar un montón de descriptores, debe seleccionar un tipo de montón de descriptores, determinar el número de descriptores que contiene y establecer marcas que indiquen si es visible para la CPU o el sombreador.

-   [Tipos de montones de descriptor](#descriptor-heap-types)
-   [Propiedades del montón de descriptores](#descriptor-heap-properties)
-   [Identificadores de descriptor](#descriptor-handles)
-   [Métodos del montón descriptor](#descriptor-heap-methods)
-   [Contenedor del montón de descriptor mínimo](#minimal-descriptor-heap-wrapper)
-   [Temas relacionados](#related-topics)

## <a name="descriptor-heap-types"></a>Tipos de montones de descriptor

Un miembro de la enumeración de tipo de montón del [**\_ descriptor \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) determina el tipo de montón:

``` syntax
typedef enum D3D12_DESCRIPTOR_HEAP_TYPE
{
    D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV,    // Constant buffer/Shader resource/Unordered access views
    D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER,        // Samplers
    D3D12_DESCRIPTOR_HEAP_TYPE_RTV,            // Render target view
    D3D12_DESCRIPTOR_HEAP_TYPE_DSV,            // Depth stencil view
    D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES       // Simply the number of descriptor heap types
} D3D12_DESCRIPTOR_HEAP_TYPE;
```

## <a name="descriptor-heap-properties"></a>Propiedades del montón de descriptores

Las propiedades del montón se establecen en la estructura de [**\_ \_ \_ DESC del descriptor de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) , que hace referencia al [**\_ \_ \_ tipo de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) del descriptor D3D12 y a las enumeraciones del [**\_ \_ montón \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) del descriptor de D3D12.

\_Opcionalmente, el sombreador de marca del descriptor de descriptor D3D12 se \_ \_ \_ \_ puede establecer en un montón de descriptores para indicar que se va a enlazar en una lista de comandos para que lo hagan las referencias de los sombreadores. Los montones de descriptor creados *sin* esta marca permiten a las aplicaciones la opción de ensayar los descriptores en la memoria de la CPU antes de copiarlos en un montón de descriptor visible del sombreador, por comodidad. Pero también es adecuado para las aplicaciones crear descriptores directamente en montones de descriptor visibles del sombreador sin necesidad de ensayar nada en la CPU.

Esta marca solo se aplica a CBV, SRV, UAV y muestreadores. No se aplica a otros tipos de montón descriptor, ya que los sombreadores no hacen referencia directamente a los demás tipos.

Por ejemplo, describa y cree un montón de descriptores de muestra.


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



Describir y crear una vista de búfer de constantes (CBV), la vista de recursos del sombreador (SRV) y el montón del descriptor de la vista de acceso no ordenado (UAV).


```C++
// Describe and create a shader resource view (SRV) and unordered
// access view (UAV) descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC srvUavHeapDesc = {};
srvUavHeapDesc.NumDescriptors = DescriptorCount;
srvUavHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
srvUavHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&srvUavHeapDesc, IID_PPV_ARGS(&m_srvUavHeap)));

m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
m_srvUavDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV);
```



## <a name="descriptor-handles"></a>Identificadores de descriptor

Las estructuras identificador de [**\_ \_ descriptor \_ de D3D12 de GPU**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) y D3D12 de [**\_ \_ \_ identificador de CPU**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) identifican descriptores específicos en un montón de descriptores. Un identificador es un poco como un puntero, pero la aplicación no debe desreferenciarlo manualmente; de lo contrario, el comportamiento es indefinido. El uso de los identificadores debe pasar por la API. Un controlador se puede copiar libremente o pasar a las API que operan en y usan descriptores. No hay ningún recuento de referencias, por lo que la aplicación debe asegurarse de que no usa un identificador después de que se haya eliminado el montón de descriptor subyacente.

Las aplicaciones pueden averiguar el tamaño del incremento de los descriptores para un tipo de montón descriptor determinado, de modo que puedan generar identificadores en cualquier ubicación de un montón de descriptores manualmente a partir del identificador de la base. Las aplicaciones nunca deben codificar los tamaños de incremento del identificador del descriptor y siempre deberían consultarlos para una instancia de dispositivo determinada; de lo contrario, el comportamiento es indefinido. Las aplicaciones tampoco deben usar los tamaños de incremento y los controladores para realizar su propio examen o manipulación de los datos del montón de descriptor, ya que los resultados de hacerlo no están definidos. Es posible que los identificadores no se utilicen realmente como punteros, sino como servidores proxy para los punteros, para evitar desreferenciaciones accidentales.

> [!Note]
>
> Hay una estructura auxiliar, CD3DX12 \_ \_ de descriptor \_ de GPU, definida en el encabezado d3dx12. h, que hereda la estructura de [**\_ \_ \_ identificador del descriptor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) y proporciona inicialización y otras operaciones útiles. Del mismo modo \_ , \_ \_ se define la estructura de la aplicación auxiliar de controlador del descriptor de CPU CD3DX12 para la estructura de [**\_ \_ \_ controlador del descriptor de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)

 

Ambas estructuras auxiliares se usan al rellenar las listas de comandos.


```C++
// Fill the command list with all the render commands and dependent state.
void D3D12nBodyGravity::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated
    // command lists have finished execution on the GPU; apps should use
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocators[m_frameIndex]->Reset());

    // However, when ExecuteCommandList() is called on a particular command
    // list, that command list can then be reset at any time and must be before
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocators[m_frameIndex].Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetPipelineState(m_pipelineState.Get());
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

    m_commandList->SetGraphicsRootConstantBufferView(RootParameterCB, m_constantBufferGS->GetGPUVirtualAddress() + m_frameIndex * sizeof(ConstantBufferGS));

    ID3D12DescriptorHeap* ppHeaps[] = { m_srvUavHeap.Get() };
    m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_POINTLIST);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.0f, 0.1f, 0.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);

    // Render the particles.
    float viewportHeight = static_cast<float>(static_cast<UINT>(m_viewport.Height) / m_heightInstances);
    float viewportWidth = static_cast<float>(static_cast<UINT>(m_viewport.Width) / m_widthInstances);
    for (UINT n = 0; n < ThreadCount; n++)
    {
        const UINT srvIndex = n + (m_srvIndex[n] == 0 ? SrvParticlePosVelo0 : SrvParticlePosVelo1);

        D3D12_VIEWPORT viewport;
        viewport.TopLeftX = (n % m_widthInstances) * viewportWidth;
        viewport.TopLeftY = (n / m_widthInstances) * viewportHeight;
        viewport.Width = viewportWidth;
        viewport.Height = viewportHeight;
        viewport.MinDepth = D3D12_MIN_DEPTH;
        viewport.MaxDepth = D3D12_MAX_DEPTH;
        m_commandList->RSSetViewports(1, &viewport);

        CD3DX12_GPU_DESCRIPTOR_HANDLE srvHandle(m_srvUavHeap->GetGPUDescriptorHandleForHeapStart(), srvIndex, m_srvUavDescriptorSize);
        m_commandList->SetGraphicsRootDescriptorTable(RootParameterSRV, srvHandle);

        m_commandList->DrawInstanced(ParticleCount, 1, 0, 0);
    }

    m_commandList->RSSetViewports(1, &m_viewport);

    // Indicate that the back buffer will now be used to present.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList->Close());
}
```



## <a name="descriptor-heap-methods"></a>Métodos del montón descriptor

Los montones de descriptor ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) se heredan de [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable). Esto impone la responsabilidad de la administración de la residencia de los montones de descriptor en las aplicaciones, al igual que los montones de recursos. Los métodos de administración de la residencia solo se aplican a los montones visibles del sombreador, ya que los montones no visibles del sombreador no son visibles directamente en la GPU.

El método [**ID3D12Device:: GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) permite a las aplicaciones desplazar manualmente los identificadores en un montón (generando identificadores en cualquier parte de un montón de descriptores). El identificador de la ubicación de inicio del montón procede de [**ID3D12DescriptorHeap:: GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap:: GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart). El desvío se realiza agregando el tamaño del incremento \* el número de descriptores que se van a desplazar al inicio del montón del descriptor. Tenga en cuenta que el tamaño de incremento no se puede considerar como un tamaño de bytes, ya que las aplicaciones no deben desreferenciar los identificadores como si fueran memoria: la memoria a la que apunta tiene un diseño no normalizado y puede variar incluso para un dispositivo determinado.

[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) devuelve un identificador de CPU para los montones de descriptor visibles de la CPU. Devuelve un identificador nulo (y el nivel de depuración informará de un error) si el montón descriptor no es visible para la CPU.

[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) devuelve un identificador de GPU para montones de descriptor visibles del sombreador. Devuelve un identificador nulo (y el nivel de depuración informará de un error) si el montón del descriptor no es visible para el sombreador.

Por ejemplo, crear vistas de destino de representación para mostrar el texto de D2D mediante un dispositivo 11on12.


```C++
    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_d3d12Device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_d3d12Device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    
    }
```



## <a name="minimal-descriptor-heap-wrapper"></a>Contenedor del montón de descriptor mínimo

Es probable que los desarrolladores de aplicaciones deseen crear su propio código auxiliar para administrar los controladores y los montones de descriptores. A continuación se muestra un ejemplo básico. Los contenedores más sofisticados podrían, por ejemplo, realizar un seguimiento de los tipos de descriptores en un montón y almacenar los argumentos de creación del descriptor.

``` syntax
class CDescriptorHeapWrapper
{
public:
    CDescriptorHeapWrapper() { memset(this, 0, sizeof(*this)); }

    HRESULT Create(
        ID3D12Device* pDevice, 
        D3D12_DESCRIPTOR_HEAP_TYPE Type, 
        UINT NumDescriptors, 
        bool bShaderVisible = false)
    {
        D3D12_DESCRIPTOR_HEAP_DESC Desc;
        Desc.Type = Type;
        Desc.NumDescriptors = NumDescriptors;
        Desc.Flags = (bShaderVisible ? D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE : D3D12_DESCRIPTOR_HEAP_FLAG_NONE);
       
        HRESULT hr = pDevice->CreateDescriptorHeap(&Desc, 
                               __uuidof(ID3D12DescriptorHeap), 
                               (void**)&pDH);
        if (FAILED(hr)) return hr;

        hCPUHeapStart = pDH->GetCPUDescriptorHandleForHeapStart();
        hGPUHeapStart = pDH->GetGPUDescriptorHandleForHeapStart();

        HandleIncrementSize = pDevice->GetDescriptorHandleIncrementSize(Desc.Type);
        return hr;
    }
    operator ID3D12DescriptorHeap*() { return pDH; }

    D3D12_CPU_DESCRIPTOR_HANDLE hCPU(UINT index)
    {
        return hCPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_GPU_DESCRIPTOR_HANDLE hGPU(UINT index) 
    {
        assert(Desc.Flags&D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE); 
        return hGPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_DESCRIPTOR_HEAP_DESC Desc;
    CComPtr<ID3D12DescriptorHeap> pDH;
    D3D12_CPU_DESCRIPTOR_HANDLE hCPUHeapStart;
    D3D12_GPU_DESCRIPTOR_HANDLE hGPUHeapStart;
    UINT HandleIncrementSize;
};
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> </dl>

 

 