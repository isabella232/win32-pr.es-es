---
title: Crear un componente básico de Direct3D 12
description: En este tema se describe el flujo de llamada para crear un componente básico de Direct3D 12.
ms.assetid: A0FB108B-15C1-42AD-9277-D5CB63FA8329
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: d0c7ead9ce67ee23a0668304a006d6cd67fb3d67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466365"
---
# <a name="creating-a-basic-direct3d-12-component"></a>Crear un componente básico de Direct3D 12

> [!NOTE]
> Consulte el [repositorio DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) para obtener ejemplos de gráficos de DirectX 12 que muestran cómo compilar aplicaciones con un uso intensivo de gráficos para Windows 10.

En este tema se describe el flujo de llamada para crear un componente básico de Direct3D 12.

-   [Flujo de código para una aplicación sencilla](#code-flow-for-a-simple-app)
    -   [Inicialización](#initialize)
    -   [Actualizar](#update)
    -   [Render](#render)
    -   [Destruir](#destroy)
-   [Ejemplo de código para una aplicación sencilla](#code-example-for-a-simple-app)
    -   [Clase D3D12HelloTriangle](#class-d3d12hellotriangle)
    -   [OnInit()](#oninit)
    -   [LoadPipeline()](#loadpipeline)
    -   [LoadAssets()](#loadassets)
    -   [OnUpdate()](#onupdate)
    -   [OnRender()](#onrender)
    -   [PopulateCommandList()](#populatecommandlist)
    -   [WaitForPreviousFrame()](#waitforpreviousframe)
    -   [OnDestroy()](#ondestroy)
-   [Temas relacionados](#related-topics)

## <a name="code-flow-for-a-simple-app"></a>Flujo de código para una aplicación sencilla

El bucle más externo de un programa D3D 12 sigue un proceso de gráficos muy estándar:

> [!TIP]
> Las características nuevas de Direct3D 12 van seguidas de una nota.

-   [Inicialización](#initialize)
-   **Repetir**
    -   [Actualizar](#update)
    -   [Render](#render)
-   [Destruir](#destroy)

### <a name="initialize"></a>Inicialización

La inicialización implica primero la configuración de las variables globales y las clases, y una función initialize debe preparar la canalización y los recursos.

-   Inicialice la canalización.
    -   Habilite la capa de depuración.
    -   Cree el dispositivo.
    -   Cree la cola de comandos.
    -   Cree la cadena de intercambio.
    -   Cree un montón de descriptores de vista de destino de representación (RTV).
        > [!Note]  
        > Un [montón de descriptores](descriptor-heaps.md) se puede pensar en como una matriz [de descriptores](descriptors.md). Donde cada descriptor describe completamente un objeto para la GPU.

    -   Cree recursos de marco (una vista de destino de representación para cada fotograma).
    -   Cree un asignador de comandos.
        > [!Note]  
        > Un asignador de comandos administra el almacenamiento subyacente para las [listas de comandos y agrupa](recording-command-lists-and-bundles.md).
         
-   Inicialice los recursos.
    -   Cree una firma raíz vacía.
        > [!Note]  
        > Una firma [raíz de gráficos](root-signatures.md) define qué recursos están enlazados a la canalización de gráficos.

    -   Compile los sombreadores.
    -   Cree el diseño de entrada del vértice.
    -   Cree una descripción [del objeto de estado de](managing-graphics-pipeline-state-in-direct3d-12.md) canalización y, a continuación, cree el objeto .
        > [!Note]  
        > Un objeto de estado de canalización mantiene el estado de todos los sombreadores establecidos actualmente, así como determinados objetos de estado de función fijos (como el *ensamblador* de entrada, *el teator,* *el rasterizador* y la fusión *de salida).*

    -   Cree la lista de comandos.
    -   Cierre la lista de comandos.
    -   Cree y cargue los búferes de vértices.
    -   Cree las vistas del búfer de vértices.
    -   Cree una barrera.
        > [!Note]  
        > Se usa una barrera para sincronizar la CPU con la GPU (consulte [Sincronización de varios motores).](./user-mode-heap-synchronization.md)

    -   Cree un identificador de eventos.
    -   Espere a que finalice la GPU.
        > [!Note]  
        > Compruebe la barrera.

Consulte la [clase D3D12HelloTriangle,](#class-d3d12hellotriangle) [OnInit,](#oninit) [LoadPipeline](#loadpipeline) [y LoadAssets.](#loadassets)

### <a name="update"></a>Actualizar

Actualice todo lo que debe cambiar desde el último fotograma.

-   Modifique la constante, los vértices, los búferes de índice y todo lo demás, según sea necesario.

Consulte [OnUpdate](#onupdate).

### <a name="render"></a>Representación

Dibuje el nuevo mundo.

-   Rellene la lista de comandos.
    -   Restablezca el asignador de la lista de comandos.
        > [!Note]  
        > Vuelva a usar la memoria asociada al asignador de comandos.

         

    -   Restablezca la lista de comandos.
    -   Establezca la firma raíz de gráficos.
        > [!Note]  
        > Establece la firma raíz de gráficos que se usará para la lista de comandos actual.

         

    -   Establezca la ventanilla y los rectángulos de rectángulos de rectángulos.
    -   Establezca una barrera de recursos, lo que indica que el búfer de reserva se va a usar como destino de representación.
        > [!Note]  
        > Las barreras de recursos se usan para administrar las transiciones de recursos.

         

    -   Registre los comandos en la lista de comandos.
    -   Indique que el búfer de reserva se usará para presentarse después de que se haya ejecutado la lista de comandos.
        > [!Note]  
        > Otra llamada para establecer una barrera de recursos.

         

    -   Cierre la lista de comandos para seguir grabando.
-   Ejecute la lista de comandos.
-   Presente el marco.
-   Espere a que finalice la GPU.
    > [!Note]  
    > Siga actualizando y comprobando la barrera.

Consulte [OnRender](#onrender).

### <a name="destroy"></a>Destruir

Cierre la aplicación de forma limpia.

-   Espere a que finalice la GPU.
    > [!Note]  
    > Comprobación final en la barrera.

-   Cierre el identificador del evento.

Consulte [OnDestroy](#ondestroy).

## <a name="code-example-for-a-simple-app"></a>Ejemplo de código para una aplicación sencilla

A continuación se expande el flujo de código anterior para incluir el código necesario para un ejemplo básico.

### <a name="class-d3d12hellotriangle"></a>Clase D3D12HelloTriangle

En primer lugar, defina la clase en un archivo de encabezado, incluida una ventanilla, un rectángulo de rectángulos y un búfer de vértices mediante las estructuras :

-   [**VENTANILLA D3D12 \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [**D3D12 \_ RECT**](d3d12-rect.md)
-   [**VISTA BÚFER DE VÉRTICES D3D12 \_ \_ \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

```cpp
#include "DXSample.h"

using namespace DirectX;
using namespace Microsoft::WRL;

class D3D12HelloTriangle : public DXSample
{
public:
    D3D12HelloTriangle(UINT width, UINT height, std::wstring name);

    virtual void OnInit();
    virtual void OnUpdate();
    virtual void OnRender();
    virtual void OnDestroy();

private:
    static const UINT FrameCount = 2;

    struct Vertex
    {
        XMFLOAT3 position;
        XMFLOAT4 color;
    };

    // Pipeline objects.
    D3D12_VIEWPORT m_viewport;
    D3D12_RECT m_scissorRect;
    ComPtr<IDXGISwapChain3> m_swapChain;
    ComPtr<ID3D12Device> m_device;
    ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
    ComPtr<ID3D12CommandAllocator> m_commandAllocator;
    ComPtr<ID3D12CommandQueue> m_commandQueue;
    ComPtr<ID3D12RootSignature> m_rootSignature;
    ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
    ComPtr<ID3D12PipelineState> m_pipelineState;
    ComPtr<ID3D12GraphicsCommandList> m_commandList;
    UINT m_rtvDescriptorSize;

    // App resources.
    ComPtr<ID3D12Resource> m_vertexBuffer;
    D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;

    // Synchronization objects.
    UINT m_frameIndex;
    HANDLE m_fenceEvent;
    ComPtr<ID3D12Fence> m_fence;
    UINT64 m_fenceValue;

    void LoadPipeline();
    void LoadAssets();
    void PopulateCommandList();
    void WaitForPreviousFrame();
};
```

### <a name="oninit"></a>OnInit()

En el archivo de código fuente principal de los proyectos, empiece a inicializar los objetos :

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a>LoadPipeline()

El código siguiente crea los conceptos básicos de una canalización de gráficos. El proceso de creación de dispositivos e intercambio de cadenas es muy similar a Direct3D 11.

-   Habilite la capa de depuración, con llamadas a:<dl>

[**D3D12GetDebugInterface**](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [**ID3D12Debug::EnableDebugLayer**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   Cree el dispositivo:<dl>

[**CreateDXGIFactory1**](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   Rellene una descripción de la cola de comandos y, a continuación, cree la cola de comandos:<dl>

[**D3D12 \_ COMMAND \_ QUEUE \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [**ID3D12Device::CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   Rellene una descripción de la cadena de intercambio y, a continuación, cree la cadena de intercambio: <dl>

[**DXGI \_ SWAP \_ CHAIN \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [**IDXGIFactory::CreateSwapChain**](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   Rellene una descripción del montón. a continuación, cree un montón de descriptores: <dl>

[**D3D12 \_ DESCRIPTOR \_ HEAP \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [**ID3D12Device::CreateDescriptorHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   Cree la vista de destino de representación: <dl>

[**IDENTIFICADOR DEL DESCRIPTOR DE \_ CPU CD3DX12 \_ \_**](cd3dx12-cpu-descriptor-handle.md)  
    [**GetCPUDescriptorHandleForHeapStart**](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [**IDXGISwapChain::GetBuffer**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [**ID3D12Device::CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   Cree el asignador de comandos: [**ID3D12Device::CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).

En pasos posteriores, las listas de comandos se obtienen del asignador de comandos y se envían a la cola de comandos.

Cargue las dependencias de canalización de representación (tenga en cuenta que la creación de un dispositivo WARP de software es completamente opcional).


```cpp
void D3D12HelloTriangle::LoadPipeline()
{
#if defined(_DEBUG)
    // Enable the D3D12 debug layer.
    {
        
        ComPtr<ID3D12Debug> debugController;
        if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&debugController))))
        {
            debugController->EnableDebugLayer();
        }
    }
#endif

    ComPtr<IDXGIFactory4> factory;
    ThrowIfFailed(CreateDXGIFactory1(IID_PPV_ARGS(&factory)));

    if (m_useWarpDevice)
    {
        ComPtr<IDXGIAdapter> warpAdapter;
        ThrowIfFailed(factory->EnumWarpAdapter(IID_PPV_ARGS(&warpAdapter)));

        ThrowIfFailed(D3D12CreateDevice(
            warpAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }
    else
    {
        ComPtr<IDXGIAdapter1> hardwareAdapter;
        GetHardwareAdapter(factory.Get(), &hardwareAdapter);

        ThrowIfFailed(D3D12CreateDevice(
            hardwareAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }

    // Describe and create the command queue.
    D3D12_COMMAND_QUEUE_DESC queueDesc = {};
    queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
    queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

    ThrowIfFailed(m_device->CreateCommandQueue(&queueDesc, IID_PPV_ARGS(&m_commandQueue)));

    // Describe and create the swap chain.
    DXGI_SWAP_CHAIN_DESC swapChainDesc = {};
    swapChainDesc.BufferCount = FrameCount;
    swapChainDesc.BufferDesc.Width = m_width;
    swapChainDesc.BufferDesc.Height = m_height;
    swapChainDesc.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
    swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
    swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_DISCARD;
    swapChainDesc.OutputWindow = Win32Application::GetHwnd();
    swapChainDesc.SampleDesc.Count = 1;
    swapChainDesc.Windowed = TRUE;

    ComPtr<IDXGISwapChain> swapChain;
    ThrowIfFailed(factory->CreateSwapChain(
        m_commandQueue.Get(),        // Swap chain needs the queue so that it can force a flush on it.
        &swapChainDesc,
        &swapChain
        ));

    ThrowIfFailed(swapChain.As(&m_swapChain));

    // This sample does not support fullscreen transitions.
    ThrowIfFailed(factory->MakeWindowAssociation(Win32Application::GetHwnd(), DXGI_MWA_NO_ALT_ENTER));

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();

    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
            rtvHandle.Offset(1, m_rtvDescriptorSize);
        }
    }

    ThrowIfFailed(m_device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));
}
```



### <a name="loadassets"></a>LoadAssets()

La carga y preparación de recursos es un proceso largo. Muchas de estas fases son similares a D3D 11, aunque algunas son nuevas en D3D 12.

En Direct3D 12, el estado de canalización necesario se adjunta a una lista de comandos a través de un objeto [de estado de canalización](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO). En este ejemplo se muestra cómo crear un PSO. Puede almacenar el PSO como una variable miembro y reutilizarlo tantas veces como sea necesario.

Un montón de descriptores define las vistas y cómo acceder a los recursos (por ejemplo, una vista de destino de representación).

Con el asignador de lista de comandos y PSO, puede crear la lista de comandos real, que se ejecutará más adelante.

Las siguientes API y procesos se llaman en sucesión.

-   Cree una firma raíz vacía con la estructura auxiliar disponible: <dl>

[**CD3DX12 \_ ROOT \_ SIGNATURE \_ DESC**](cd3dx12-root-signature-desc.md)  
    [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [**ID3D12Device::CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   Cargue y compile los sombreadores: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).
-   Cree el diseño de entrada del vértice: [**D3D12 \_ INPUT \_ ELEMENT \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).
-   Rellene una descripción del estado de canalización con las estructuras auxiliares disponibles y, a continuación, cree el estado de canalización de gráficos: <dl>

[**D3D12 ESTADO DE CANALIZACIÓN \_ \_ DE \_ \_ GRÁFICOS DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [**CD3DX12 \_ RASTERIZER \_ DESC**](cd3dx12-rasterizer-desc.md)  
    [**CD3DX12 \_ BLEND \_ DESC**](cd3dx12-blend-desc.md)  
    [**ID3D12Device::CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   Cree y cierre una lista de comandos: <dl>

[**ID3D12Device::CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [**ID3D12GraphicsCommandList::Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   Cree el búfer de vértices: [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).
-   Copie los datos del vértice en el búfer del vértice:<dl>

[**ID3D12Resource::Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [**ID3D12Resource::Unmap**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   Inicialice la vista del búfer de vértices: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).
-   Cree e inicialice la barrera: [**ID3D12Device::CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).
-   Cree un identificador de eventos para usarlo con la sincronización de fotogramas.
-   Espere a que finalice la GPU.


```cpp
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
        CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_UPLOAD);
        auto desc = CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize);
        ThrowIfFailed(m_device->CreateCommittedResource(
            &heapProps,
            D3D12_HEAP_FLAG_NONE,
            &desc,
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



### <a name="onupdate"></a>OnUpdate()

Para obtener un ejemplo sencillo, no se actualiza nada.


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a>OnRender()

Durante la configuración, se usó la variable **miembro m \_ commandList** para registrar y ejecutar todos los comandos de configuración. Ahora puede reutilizar ese miembro en el bucle de representación principal.

La representación implica una llamada para rellenar la lista de comandos y, a continuación, se puede ejecutar la lista de comandos y el siguiente búfer en la cadena de intercambio presentada:

-   Rellene la lista de comandos.
-   Ejecute la lista de comandos: [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).
-   [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) el marco.
-   Espere a que finalice la GPU.


```cpp
void D3D12HelloTriangle::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(1, 0));

    WaitForPreviousFrame();
}
```



### <a name="populatecommandlist"></a>PopulateCommandList()

Debe restablecer el asignador de lista de comandos y la propia lista de comandos para poder reutilizarlos. En escenarios más avanzados, podría tener sentido restablecer el asignador cada varios fotogramas. La memoria está asociada al asignador que no se puede liberar inmediatamente después de ejecutar una lista de comandos. En este ejemplo se muestra cómo restablecer el asignador después de cada fotograma.

Ahora, vuelva a usar la lista de comandos para el marco actual. Vuelva a adjuntar la ventanilla a la lista de comandos (que debe realizarse cada vez que se restablezca una lista de comandos y antes de que se ejecute la lista de comandos), indique que el recurso se usará como destino de representación, registre comandos y, a continuación, indique que el destino de representación se usará para presentar cuando la lista de comandos haya terminado de ejecutarse.

Rellenar listas de comandos llama a los siguientes métodos y procesos a su vez:

-   Restablezca el asignador de comandos y la lista de comandos: <dl>

[**ID3D12CommandAllocator::Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [**ID3D12GraphicsCommandList::Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   Establezca los rectángulos de firma raíz, ventanilla y ándulos: <dl>

[**ID3D12GraphicsCommandList::SetGraphicsRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [**ID3D12GraphicsCommandList::RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [**ID3D12GraphicsCommandList::RSSetScissorRects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   Indique que el búfer de reserva se va a usar como destino de representación: <dl>

[**ID3D12GraphicsCommandList::ResourceBar dataset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   Registre los comandos:<dl>

[**ID3D12GraphicsCommandList::ClearRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [**ID3D12GraphicsCommandList::IASetPrimitiveTopology**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [**ID3D12GraphicsCommandList::D rawInstanced**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   Indique que el búfer de reserva se usará ahora para presentar: [**ID3D12GraphicsCommandList::ResourceBarcommand**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).
-   Cierre la lista de comandos: [**ID3D12GraphicsCommandList::Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).


```cpp
void D3D12HelloTriangle::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocator->Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
    m_commandList->RSSetViewports(1, &m_viewport);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET);
    m_commandList->ResourceBarrier(1, &barrier);

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->DrawInstanced(3, 1, 0, 0);

    // Indicate that the back buffer will now be used to present.
    barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
    m_commandList->ResourceBarrier(1, &barrier);

    ThrowIfFailed(m_commandList->Close());
}
```



### <a name="waitforpreviousframe"></a>WaitForPreviousFrame()

El código siguiente muestra un uso sobre simplificado de barreras.

> [!Note]  
> Esperar a que se complete un fotograma es demasiado ineficaz para la mayoría de las aplicaciones.

 

Se llama a las siguientes API y procesos en orden:

-   [**ID3D12CommandQueue::Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [**ID3D12Fence::GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [**ID3D12Fence::SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   Espere al evento.
-   Actualice el índice del marco: [**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).


```cpp
void D3D12HelloTriangle::WaitForPreviousFrame()
{
    // WAITING FOR THE FRAME TO COMPLETE BEFORE CONTINUING IS NOT BEST PRACTICE.
    // This is code implemented as such for simplicity. More advanced samples 
    // illustrate how to use fences for efficient resource usage.

    // Signal and increment the fence value.
    const UINT64 fence = m_fenceValue;
    ThrowIfFailed(m_commandQueue->Signal(m_fence.Get(), fence));
    m_fenceValue++;

    // Wait until the previous frame is finished.
    if (m_fence->GetCompletedValue() < fence)
    {
        ThrowIfFailed(m_fence->SetEventOnCompletion(fence, m_fenceEvent));
        WaitForSingleObject(m_fenceEvent, INFINITE);
    }

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();
}
```



### <a name="ondestroy"></a>OnDestroy()

Cierre correctamente la aplicación.

-   Espere a que finalice la GPU.
-   Cierre el evento.


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Ejemplos de trabajo](working-samples.md)
</dt> </dl>

 

 
