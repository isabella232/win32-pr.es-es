---
title: Crear un componente básico de Direct3D 12
description: En este tema se describe el flujo de llamadas para crear un componente básico de Direct3D 12.
ms.assetid: A0FB108B-15C1-42AD-9277-D5CB63FA8329
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: d0c7ead9ce67ee23a0668304a006d6cd67fb3d67
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "104758865"
---
# <a name="creating-a-basic-direct3d-12-component"></a><span data-ttu-id="56e9e-103">Crear un componente básico de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="56e9e-103">Creating a basic Direct3D 12 component</span></span>

> [!NOTE]
> <span data-ttu-id="56e9e-104">Consulte el repositorio [DirectX-Graphics-samples](https://github.com/Microsoft/DirectX-Graphics-Samples) para gráficos de DirectX 12 que muestran cómo crear aplicaciones de uso intensivo de gráficos para Windows 10.</span><span class="sxs-lookup"><span data-stu-id="56e9e-104">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="56e9e-105">En este tema se describe el flujo de llamadas para crear un componente básico de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="56e9e-105">This topic describes the call flow to create a basic Direct3D 12 component.</span></span>

-   [<span data-ttu-id="56e9e-106">Flujo de código para una aplicación sencilla</span><span class="sxs-lookup"><span data-stu-id="56e9e-106">Code flow for a simple app</span></span>](#code-flow-for-a-simple-app)
    -   [<span data-ttu-id="56e9e-107">Inicialización</span><span class="sxs-lookup"><span data-stu-id="56e9e-107">Initialize</span></span>](#initialize)
    -   [<span data-ttu-id="56e9e-108">Actualizar</span><span class="sxs-lookup"><span data-stu-id="56e9e-108">Update</span></span>](#update)
    -   [<span data-ttu-id="56e9e-109">Render</span><span class="sxs-lookup"><span data-stu-id="56e9e-109">Render</span></span>](#render)
    -   [<span data-ttu-id="56e9e-110">Borrar</span><span class="sxs-lookup"><span data-stu-id="56e9e-110">Destroy</span></span>](#destroy)
-   [<span data-ttu-id="56e9e-111">Ejemplo de código para una aplicación sencilla</span><span class="sxs-lookup"><span data-stu-id="56e9e-111">Code example for a simple app</span></span>](#code-example-for-a-simple-app)
    -   [<span data-ttu-id="56e9e-112">clase D3D12HelloTriangle</span><span class="sxs-lookup"><span data-stu-id="56e9e-112">class D3D12HelloTriangle</span></span>](#class-d3d12hellotriangle)
    -   [<span data-ttu-id="56e9e-113">OnInit ()</span><span class="sxs-lookup"><span data-stu-id="56e9e-113">OnInit()</span></span>](#oninit)
    -   [<span data-ttu-id="56e9e-114">LoadPipeline()</span><span class="sxs-lookup"><span data-stu-id="56e9e-114">LoadPipeline()</span></span>](#loadpipeline)
    -   [<span data-ttu-id="56e9e-115">LoadAssets()</span><span class="sxs-lookup"><span data-stu-id="56e9e-115">LoadAssets()</span></span>](#loadassets)
    -   [<span data-ttu-id="56e9e-116">Actualizar ()</span><span class="sxs-lookup"><span data-stu-id="56e9e-116">OnUpdate()</span></span>](#onupdate)
    -   [<span data-ttu-id="56e9e-117">OnRender ()</span><span class="sxs-lookup"><span data-stu-id="56e9e-117">OnRender()</span></span>](#onrender)
    -   [<span data-ttu-id="56e9e-118">PopulateCommandList()</span><span class="sxs-lookup"><span data-stu-id="56e9e-118">PopulateCommandList()</span></span>](#populatecommandlist)
    -   [<span data-ttu-id="56e9e-119">WaitForPreviousFrame()</span><span class="sxs-lookup"><span data-stu-id="56e9e-119">WaitForPreviousFrame()</span></span>](#waitforpreviousframe)
    -   [<span data-ttu-id="56e9e-120">Aldestruir ()</span><span class="sxs-lookup"><span data-stu-id="56e9e-120">OnDestroy()</span></span>](#ondestroy)
-   [<span data-ttu-id="56e9e-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56e9e-121">Related topics</span></span>](#related-topics)

## <a name="code-flow-for-a-simple-app"></a><span data-ttu-id="56e9e-122">Flujo de código para una aplicación sencilla</span><span class="sxs-lookup"><span data-stu-id="56e9e-122">Code flow for a simple app</span></span>

<span data-ttu-id="56e9e-123">El bucle más externo de un programa D3D 12 sigue un proceso de gráficos muy estándar:</span><span class="sxs-lookup"><span data-stu-id="56e9e-123">The outermost loop of a D3D 12 program follows a very standard graphics process:</span></span>

> [!TIP]
> <span data-ttu-id="56e9e-124">Las características nuevas de Direct3D 12 van seguidas de una nota.</span><span class="sxs-lookup"><span data-stu-id="56e9e-124">Features new to Direct3D 12 are followed by a note.</span></span>

-   [<span data-ttu-id="56e9e-125">Inicialización</span><span class="sxs-lookup"><span data-stu-id="56e9e-125">Initialize</span></span>](#initialize)
-   <span data-ttu-id="56e9e-126">**Pueden**</span><span class="sxs-lookup"><span data-stu-id="56e9e-126">**Repeat**</span></span>
    -   [<span data-ttu-id="56e9e-127">Actualizar</span><span class="sxs-lookup"><span data-stu-id="56e9e-127">Update</span></span>](#update)
    -   [<span data-ttu-id="56e9e-128">Render</span><span class="sxs-lookup"><span data-stu-id="56e9e-128">Render</span></span>](#render)
-   [<span data-ttu-id="56e9e-129">Borrar</span><span class="sxs-lookup"><span data-stu-id="56e9e-129">Destroy</span></span>](#destroy)

### <a name="initialize"></a><span data-ttu-id="56e9e-130">Inicialización</span><span class="sxs-lookup"><span data-stu-id="56e9e-130">Initialize</span></span>

<span data-ttu-id="56e9e-131">La inicialización implica configurar primero las variables y las clases globales, y una función Initialize debe preparar la canalización y los recursos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-131">Initialization involves first setting up the global variables and classes, and an initialize function must prepare the pipeline and assets.</span></span>

-   <span data-ttu-id="56e9e-132">Inicialice la canalización.</span><span class="sxs-lookup"><span data-stu-id="56e9e-132">Initialize the pipeline.</span></span>
    -   <span data-ttu-id="56e9e-133">Habilitar la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="56e9e-133">Enable the debug layer.</span></span>
    -   <span data-ttu-id="56e9e-134">Cree el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56e9e-134">Create the device.</span></span>
    -   <span data-ttu-id="56e9e-135">Cree la cola de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-135">Create the command queue.</span></span>
    -   <span data-ttu-id="56e9e-136">Cree la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="56e9e-136">Create the swap chain.</span></span>
    -   <span data-ttu-id="56e9e-137">Cree un montón de descriptores de vista de destino de representación (RTV).</span><span class="sxs-lookup"><span data-stu-id="56e9e-137">Create a render target view (RTV) descriptor heap.</span></span>
        > [!Note]  
        > <span data-ttu-id="56e9e-138">Un [montón de descriptores](descriptor-heaps.md) puede considerarse como una matriz de [descriptores.](descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="56e9e-138">A [descriptor heap](descriptor-heaps.md) can be thought of as an array of [descriptors](descriptors.md).</span></span> <span data-ttu-id="56e9e-139">Donde cada descriptor describe completamente un objeto en la GPU.</span><span class="sxs-lookup"><span data-stu-id="56e9e-139">Where each descriptor fully describes an object to the GPU.</span></span>

    -   <span data-ttu-id="56e9e-140">Crear recursos de marco (una vista de destino de representación para cada fotograma).</span><span class="sxs-lookup"><span data-stu-id="56e9e-140">Create frame resources (a render target view for each frame).</span></span>
    -   <span data-ttu-id="56e9e-141">Cree un asignador de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-141">Create a command allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="56e9e-142">Un asignador de comandos administra el almacenamiento subyacente de [las listas de comandos y agrupaciones](recording-command-lists-and-bundles.md).</span><span class="sxs-lookup"><span data-stu-id="56e9e-142">A command allocator manages the underlying storage for [command lists and bundles](recording-command-lists-and-bundles.md).</span></span>
         
-   <span data-ttu-id="56e9e-143">Inicialice los recursos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-143">Initialize the assets.</span></span>
    -   <span data-ttu-id="56e9e-144">Cree una firma raíz vacía.</span><span class="sxs-lookup"><span data-stu-id="56e9e-144">Create an empty root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="56e9e-145">Una [firma raíz](root-signatures.md) de gráficos define qué recursos se enlazan a la canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-145">A graphics [root signature](root-signatures.md) defines what resources are bound to the graphics pipeline.</span></span>

    -   <span data-ttu-id="56e9e-146">Compile los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="56e9e-146">Compile the shaders.</span></span>
    -   <span data-ttu-id="56e9e-147">Cree el diseño de entrada de vértices.</span><span class="sxs-lookup"><span data-stu-id="56e9e-147">Create the vertex input layout.</span></span>
    -   <span data-ttu-id="56e9e-148">Cree una descripción del objeto de estado de la [canalización](managing-graphics-pipeline-state-in-direct3d-12.md) y, a continuación, cree el objeto.</span><span class="sxs-lookup"><span data-stu-id="56e9e-148">Create a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) description, then create the object.</span></span>
        > [!Note]  
        > <span data-ttu-id="56e9e-149">Un objeto de estado de canalización mantiene el estado de todos los sombreadores establecidos actualmente, así como ciertos objetos de estado de función fija (como el *ensamblador de entrada*, *tesselator*, el *rasterizador* y la *fusión de salida*).</span><span class="sxs-lookup"><span data-stu-id="56e9e-149">A pipeline state object maintains the state of all currently set shaders as well as certain fixed function state objects (such as the *input assembler*, *tesselator*, *rasterizer* and *output merger*).</span></span>

    -   <span data-ttu-id="56e9e-150">Cree la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-150">Create the command list.</span></span>
    -   <span data-ttu-id="56e9e-151">Cierre la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-151">Close the command list.</span></span>
    -   <span data-ttu-id="56e9e-152">Cree y cargue los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="56e9e-152">Create and load the vertex buffers.</span></span>
    -   <span data-ttu-id="56e9e-153">Cree las vistas de búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="56e9e-153">Create the vertex buffer views.</span></span>
    -   <span data-ttu-id="56e9e-154">Cree una barrera.</span><span class="sxs-lookup"><span data-stu-id="56e9e-154">Create a fence.</span></span>
        > [!Note]  
        > <span data-ttu-id="56e9e-155">Una barrera se utiliza para sincronizar la CPU con la GPU (consulte [sincronización de varios motores](./user-mode-heap-synchronization.md)).</span><span class="sxs-lookup"><span data-stu-id="56e9e-155">A fence is used to synchronize the CPU with the GPU (see [Multi-engine synchronization](./user-mode-heap-synchronization.md)).</span></span>

    -   <span data-ttu-id="56e9e-156">Cree un identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="56e9e-156">Create an event handle.</span></span>
    -   <span data-ttu-id="56e9e-157">Espere a que finalice la GPU.</span><span class="sxs-lookup"><span data-stu-id="56e9e-157">Wait for the GPU to finish.</span></span>
        > [!Note]  
        > <span data-ttu-id="56e9e-158">Compruebe la barrera.</span><span class="sxs-lookup"><span data-stu-id="56e9e-158">Check on the fence!</span></span>

<span data-ttu-id="56e9e-159">Consulte la [clase D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [LoadPipeline](#loadpipeline) y [LoadAssets](#loadassets).</span><span class="sxs-lookup"><span data-stu-id="56e9e-159">Refer to [class D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [LoadPipeline](#loadpipeline) and [LoadAssets](#loadassets).</span></span>

### <a name="update"></a><span data-ttu-id="56e9e-160">Actualizar</span><span class="sxs-lookup"><span data-stu-id="56e9e-160">Update</span></span>

<span data-ttu-id="56e9e-161">Actualice todo lo que debe cambiar desde el último fotograma.</span><span class="sxs-lookup"><span data-stu-id="56e9e-161">Update everything that should change since the last frame.</span></span>

-   <span data-ttu-id="56e9e-162">Modifique la constante, el vértice, los búferes de índice y todo lo demás, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="56e9e-162">Modify the constant, vertex, index buffers, and everything else, as necessary.</span></span>

<span data-ttu-id="56e9e-163">Consulte [Actualizar](#onupdate).</span><span class="sxs-lookup"><span data-stu-id="56e9e-163">Refer to [OnUpdate](#onupdate).</span></span>

### <a name="render"></a><span data-ttu-id="56e9e-164">Representación</span><span class="sxs-lookup"><span data-stu-id="56e9e-164">Render</span></span>

<span data-ttu-id="56e9e-165">Dibuje el nuevo mundo.</span><span class="sxs-lookup"><span data-stu-id="56e9e-165">Draw the new world.</span></span>

-   <span data-ttu-id="56e9e-166">Rellene la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-166">Populate the command list.</span></span>
    -   <span data-ttu-id="56e9e-167">Restablezca el asignador de la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-167">Reset the command list allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="56e9e-168">Vuelva a usar la memoria asociada al asignador de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-168">Re-use the memory that is associated with the command allocator.</span></span>

         

    -   <span data-ttu-id="56e9e-169">Restablezca la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-169">Reset the command list.</span></span>
    -   <span data-ttu-id="56e9e-170">Establezca la firma raíz de los gráficos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-170">Set the graphics root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="56e9e-171">Establece la firma raíz de gráficos que se va a utilizar para la lista de comandos actual.</span><span class="sxs-lookup"><span data-stu-id="56e9e-171">Sets the graphics root signature to use for the current command list.</span></span>

         

    -   <span data-ttu-id="56e9e-172">Establezca los rectángulos de ventanilla y tijeras.</span><span class="sxs-lookup"><span data-stu-id="56e9e-172">Set the viewport and scissor rectangles.</span></span>
    -   <span data-ttu-id="56e9e-173">Establecer una barrera de recursos, que indica que el búfer de reserva se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="56e9e-173">Set a resource barrier, indicating the back buffer is to be used as a render target.</span></span>
        > [!Note]  
        > <span data-ttu-id="56e9e-174">Las barreras de recursos se usan para administrar las transiciones de recursos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-174">Resource barriers are used to manage resource transitions.</span></span>

         

    -   <span data-ttu-id="56e9e-175">Grabe comandos en la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-175">Record commands into the command list.</span></span>
    -   <span data-ttu-id="56e9e-176">Indica que se usará el búfer de reserva para presentar después de que se ejecute la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-176">Indicate the back buffer will be used to present after the command list has executed.</span></span>
        > [!Note]  
        > <span data-ttu-id="56e9e-177">Otra llamada para establecer una barrera de recursos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-177">Another call to set a resource barrier.</span></span>

         

    -   <span data-ttu-id="56e9e-178">Cierre la lista de comandos para realizar más grabaciones.</span><span class="sxs-lookup"><span data-stu-id="56e9e-178">Close the command list to further recording.</span></span>
-   <span data-ttu-id="56e9e-179">Ejecute la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-179">Execute the command list.</span></span>
-   <span data-ttu-id="56e9e-180">Presente el marco.</span><span class="sxs-lookup"><span data-stu-id="56e9e-180">Present the frame.</span></span>
-   <span data-ttu-id="56e9e-181">Espere a que finalice la GPU.</span><span class="sxs-lookup"><span data-stu-id="56e9e-181">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="56e9e-182">Siga actualizando y comprobando la barrera.</span><span class="sxs-lookup"><span data-stu-id="56e9e-182">Keep updating and checking the fence.</span></span>

<span data-ttu-id="56e9e-183">Consulte [OnRender](#onrender).</span><span class="sxs-lookup"><span data-stu-id="56e9e-183">Refer to [OnRender](#onrender).</span></span>

### <a name="destroy"></a><span data-ttu-id="56e9e-184">Destruir</span><span class="sxs-lookup"><span data-stu-id="56e9e-184">Destroy</span></span>

<span data-ttu-id="56e9e-185">Cierre la aplicación correctamente.</span><span class="sxs-lookup"><span data-stu-id="56e9e-185">Cleanly close down the app.</span></span>

-   <span data-ttu-id="56e9e-186">Espere a que finalice la GPU.</span><span class="sxs-lookup"><span data-stu-id="56e9e-186">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="56e9e-187">Comprobación final en la barrera.</span><span class="sxs-lookup"><span data-stu-id="56e9e-187">Final check on the fence.</span></span>

-   <span data-ttu-id="56e9e-188">Cierre el identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="56e9e-188">Close the event handle.</span></span>

<span data-ttu-id="56e9e-189">Consulte el [.](#ondestroy)</span><span class="sxs-lookup"><span data-stu-id="56e9e-189">Refer to [OnDestroy](#ondestroy).</span></span>

## <a name="code-example-for-a-simple-app"></a><span data-ttu-id="56e9e-190">Ejemplo de código para una aplicación sencilla</span><span class="sxs-lookup"><span data-stu-id="56e9e-190">Code example for a simple app</span></span>

<span data-ttu-id="56e9e-191">Lo siguiente expande el flujo de código anterior para incluir el código necesario para un ejemplo básico.</span><span class="sxs-lookup"><span data-stu-id="56e9e-191">The following expands the code flow above to include the code required for a basic sample.</span></span>

### <a name="class-d3d12hellotriangle"></a><span data-ttu-id="56e9e-192">clase D3D12HelloTriangle</span><span class="sxs-lookup"><span data-stu-id="56e9e-192">class D3D12HelloTriangle</span></span>

<span data-ttu-id="56e9e-193">En primer lugar, defina la clase en un archivo de encabezado, incluida una ventanilla, un rectángulo de tijera y un búfer de vértices mediante las estructuras:</span><span class="sxs-lookup"><span data-stu-id="56e9e-193">First define the class in a header file, including a viewport, scissor rectangle and vertex buffer using the structures:</span></span>

-   [<span data-ttu-id="56e9e-194">**Ventanilla de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="56e9e-194">**D3D12\_VIEWPORT**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [<span data-ttu-id="56e9e-195">**D3D12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="56e9e-195">**D3D12\_RECT**</span></span>](d3d12-rect.md)
-   [<span data-ttu-id="56e9e-196">**D3D12 \_ \_ vista de búfer de vértices \_**</span><span class="sxs-lookup"><span data-stu-id="56e9e-196">**D3D12\_VERTEX\_BUFFER\_VIEW**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

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

### <a name="oninit"></a><span data-ttu-id="56e9e-197">OnInit ()</span><span class="sxs-lookup"><span data-stu-id="56e9e-197">OnInit()</span></span>

<span data-ttu-id="56e9e-198">En el archivo de código fuente principal de los proyectos, inicie la inicialización de los objetos:</span><span class="sxs-lookup"><span data-stu-id="56e9e-198">In the projects main source file, start initializing the objects:</span></span>

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a><span data-ttu-id="56e9e-199">LoadPipeline()</span><span class="sxs-lookup"><span data-stu-id="56e9e-199">LoadPipeline()</span></span>

<span data-ttu-id="56e9e-200">En el código siguiente se crean los aspectos básicos de una canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-200">The following code creates the basics for a graphics pipeline.</span></span> <span data-ttu-id="56e9e-201">El proceso de creación de dispositivos y cadenas de intercambio es muy similar a Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="56e9e-201">The process of creating devices and swap chains is very similar to Direct3D 11.</span></span>

-   <span data-ttu-id="56e9e-202">Habilitar la capa de depuración, con llamadas a:</span><span class="sxs-lookup"><span data-stu-id="56e9e-202">Enable the debug layer, with calls to:</span></span><dl>

[<span data-ttu-id="56e9e-203">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="56e9e-203">**D3D12GetDebugInterface**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [<span data-ttu-id="56e9e-204">**ID3D12Debug::EnableDebugLayer**</span><span class="sxs-lookup"><span data-stu-id="56e9e-204">**ID3D12Debug::EnableDebugLayer**</span></span>](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   <span data-ttu-id="56e9e-205">Cree el dispositivo:</span><span class="sxs-lookup"><span data-stu-id="56e9e-205">Create the device:</span></span><dl>

[<span data-ttu-id="56e9e-206">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="56e9e-206">**CreateDXGIFactory1**</span></span>](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [<span data-ttu-id="56e9e-207">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="56e9e-207">**D3D12CreateDevice**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   <span data-ttu-id="56e9e-208">Rellene una descripción de la cola de comandos y, a continuación, cree la cola de comandos:</span><span class="sxs-lookup"><span data-stu-id="56e9e-208">Fill out a command queue description, then create the command queue:</span></span><dl>

[<span data-ttu-id="56e9e-209">**Descripción de la cola de comandos de D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="56e9e-209">**D3D12\_COMMAND\_QUEUE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [<span data-ttu-id="56e9e-210">**ID3D12Device::CreateCommandQueue**</span><span class="sxs-lookup"><span data-stu-id="56e9e-210">**ID3D12Device::CreateCommandQueue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   <span data-ttu-id="56e9e-211">Rellene una descripción de intercambio y, a continuación, cree la cadena de intercambio:</span><span class="sxs-lookup"><span data-stu-id="56e9e-211">Fill out a swapchain description, then create the swap chain:</span></span> <dl>

[<span data-ttu-id="56e9e-212">**\_desc. \_ cadena de intercambio de DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="56e9e-212">**DXGI\_SWAP\_CHAIN\_DESC**</span></span>](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [<span data-ttu-id="56e9e-213">**IDXGIFactory::CreateSwapChain**</span><span class="sxs-lookup"><span data-stu-id="56e9e-213">**IDXGIFactory::CreateSwapChain**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [<span data-ttu-id="56e9e-214">**IDXGISwapChain3::GetCurrentBackBufferIndex**</span><span class="sxs-lookup"><span data-stu-id="56e9e-214">**IDXGISwapChain3::GetCurrentBackBufferIndex**</span></span>](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   <span data-ttu-id="56e9e-215">Rellene una descripción del montón.</span><span class="sxs-lookup"><span data-stu-id="56e9e-215">Fill out a heap description.</span></span> <span data-ttu-id="56e9e-216">a continuación, cree un montón de descriptores:</span><span class="sxs-lookup"><span data-stu-id="56e9e-216">then create a descriptor heap:</span></span> <dl>

[<span data-ttu-id="56e9e-217">**DESC. del \_ descriptor de D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="56e9e-217">**D3D12\_DESCRIPTOR\_HEAP\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [<span data-ttu-id="56e9e-218">**ID3D12Device::CreateDescriptorHeap**</span><span class="sxs-lookup"><span data-stu-id="56e9e-218">**ID3D12Device::CreateDescriptorHeap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [<span data-ttu-id="56e9e-219">**ID3D12Device::GetDescriptorHandleIncrementSize**</span><span class="sxs-lookup"><span data-stu-id="56e9e-219">**ID3D12Device::GetDescriptorHandleIncrementSize**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   <span data-ttu-id="56e9e-220">Cree la vista de destino de representación:</span><span class="sxs-lookup"><span data-stu-id="56e9e-220">Create the render target view:</span></span> <dl>

[<span data-ttu-id="56e9e-221">**\_Identificador de \_ descriptor de CPU de CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="56e9e-221">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE**</span></span>](cd3dx12-cpu-descriptor-handle.md)  
    [<span data-ttu-id="56e9e-222">**GetCPUDescriptorHandleForHeapStart**</span><span class="sxs-lookup"><span data-stu-id="56e9e-222">**GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="56e9e-223">**IDXGISwapChain:: GetBuffer**</span><span class="sxs-lookup"><span data-stu-id="56e9e-223">**IDXGISwapChain::GetBuffer**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [<span data-ttu-id="56e9e-224">**ID3D12Device::CreateRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="56e9e-224">**ID3D12Device::CreateRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   <span data-ttu-id="56e9e-225">Cree el asignador de comandos: [**ID3D12Device:: CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span><span class="sxs-lookup"><span data-stu-id="56e9e-225">Create the command allocator: [**ID3D12Device::CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span></span>

<span data-ttu-id="56e9e-226">En pasos posteriores, las listas de comandos se obtienen del asignador de comandos y se envían a la cola de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-226">In later steps, command lists are obtained from the command allocator and submitted to the command queue.</span></span>

<span data-ttu-id="56e9e-227">Cargue las dependencias de la canalización de representación (tenga en cuenta que la creación de un dispositivo de deformación de software es totalmente opcional).</span><span class="sxs-lookup"><span data-stu-id="56e9e-227">Load the rendering pipeline dependencies (note that the creation of a software WARP device is entirely optional).</span></span>


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



### <a name="loadassets"></a><span data-ttu-id="56e9e-228">LoadAssets()</span><span class="sxs-lookup"><span data-stu-id="56e9e-228">LoadAssets()</span></span>

<span data-ttu-id="56e9e-229">Cargar y preparar los recursos es un proceso largo.</span><span class="sxs-lookup"><span data-stu-id="56e9e-229">Loading and preparing assets is a lengthy process.</span></span> <span data-ttu-id="56e9e-230">Muchas de estas fases son similares a D3D 11, aunque algunas son nuevas en D3D 12.</span><span class="sxs-lookup"><span data-stu-id="56e9e-230">Many of these stages are similar to D3D 11, though some are new to D3D 12.</span></span>

<span data-ttu-id="56e9e-231">En Direct3D 12, el estado de canalización requerido se adjunta a una lista de comandos a través de un [objeto de estado de canalización](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO).</span><span class="sxs-lookup"><span data-stu-id="56e9e-231">In Direct3D 12, required pipeline state is attached to a command list via a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO).</span></span> <span data-ttu-id="56e9e-232">En este ejemplo se muestra cómo crear un PSO.</span><span class="sxs-lookup"><span data-stu-id="56e9e-232">This example shows how to create a PSO.</span></span> <span data-ttu-id="56e9e-233">Puede almacenar el PSO como una variable miembro y reutilizarlo tantas veces como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="56e9e-233">You can store the PSO as a member variable and reuse it as many times as needed.</span></span>

<span data-ttu-id="56e9e-234">Un montón de descriptores define las vistas y cómo obtener acceso a los recursos (por ejemplo, una vista de destino de representación).</span><span class="sxs-lookup"><span data-stu-id="56e9e-234">A descriptor heap defines the views and how to access resources (for example, a render target view).</span></span>

<span data-ttu-id="56e9e-235">Con el asignador de la lista de comandos y el PSO, puede crear la lista de comandos real, que se ejecutará más adelante.</span><span class="sxs-lookup"><span data-stu-id="56e9e-235">With the command list allocator and PSO, you can create the actual command list, which will be executed at a later time.</span></span>

<span data-ttu-id="56e9e-236">Se llama a las siguientes API y procesos en sucesión.</span><span class="sxs-lookup"><span data-stu-id="56e9e-236">The following APIs and processes are called in succession.</span></span>

-   <span data-ttu-id="56e9e-237">Cree una firma raíz vacía mediante la estructura de la aplicación auxiliar disponible:</span><span class="sxs-lookup"><span data-stu-id="56e9e-237">Create an empty root signature, using the available helper structure:</span></span> <dl>

[<span data-ttu-id="56e9e-238">**Descripción de la \_ firma raíz de CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="56e9e-238">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md)  
    [<span data-ttu-id="56e9e-239">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="56e9e-239">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [<span data-ttu-id="56e9e-240">**ID3D12Device::CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="56e9e-240">**ID3D12Device::CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   <span data-ttu-id="56e9e-241">Cargar y compilar los sombreadores: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span><span class="sxs-lookup"><span data-stu-id="56e9e-241">Load and compile the shaders: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span></span>
-   <span data-ttu-id="56e9e-242">Cree el diseño de entrada de vértice: [**D3D12 \_ elemento de entrada \_ \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="56e9e-242">Create the vertex input layout: [**D3D12\_INPUT\_ELEMENT\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span></span>
-   <span data-ttu-id="56e9e-243">Rellene la descripción del estado de la canalización con las estructuras auxiliares disponibles y, a continuación, cree el estado de la canalización de gráficos:</span><span class="sxs-lookup"><span data-stu-id="56e9e-243">Fill out a pipeline state description, using the helper structures available, then create the graphics pipeline state:</span></span> <dl>

[<span data-ttu-id="56e9e-244">**\_Descripción de \_ Estado de canalización de gráficos de \_ D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="56e9e-244">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [<span data-ttu-id="56e9e-245">**Descripción de CD3DX12 \_ rasterizador \_**</span><span class="sxs-lookup"><span data-stu-id="56e9e-245">**CD3DX12\_RASTERIZER\_DESC**</span></span>](cd3dx12-rasterizer-desc.md)  
    [<span data-ttu-id="56e9e-246">**CD3DX12 \_ Blend \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="56e9e-246">**CD3DX12\_BLEND\_DESC**</span></span>](cd3dx12-blend-desc.md)  
    [<span data-ttu-id="56e9e-247">**ID3D12Device::CreateGraphicsPipelineState**</span><span class="sxs-lookup"><span data-stu-id="56e9e-247">**ID3D12Device::CreateGraphicsPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   <span data-ttu-id="56e9e-248">Crear y cerrar, una lista de comandos:</span><span class="sxs-lookup"><span data-stu-id="56e9e-248">Create, then close, a command list:</span></span> <dl>

[<span data-ttu-id="56e9e-249">**ID3D12Device::CreateCommandList**</span><span class="sxs-lookup"><span data-stu-id="56e9e-249">**ID3D12Device::CreateCommandList**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [<span data-ttu-id="56e9e-250">**ID3D12GraphicsCommandList:: Close**</span><span class="sxs-lookup"><span data-stu-id="56e9e-250">**ID3D12GraphicsCommandList::Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   <span data-ttu-id="56e9e-251">Cree el búfer de vértices: [**ID3D12Device:: CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="56e9e-251">Create the vertex buffer: [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>
-   <span data-ttu-id="56e9e-252">Copie los datos del vértice en el búfer de vértices:</span><span class="sxs-lookup"><span data-stu-id="56e9e-252">Copy the vertex data to the vertex buffer:</span></span><dl>

[<span data-ttu-id="56e9e-253">**ID3D12Resource:: Map**</span><span class="sxs-lookup"><span data-stu-id="56e9e-253">**ID3D12Resource::Map**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [<span data-ttu-id="56e9e-254">**ID3D12Resource:: desasignar**</span><span class="sxs-lookup"><span data-stu-id="56e9e-254">**ID3D12Resource::Unmap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   <span data-ttu-id="56e9e-255">Inicialice la vista del búfer de vértices: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span><span class="sxs-lookup"><span data-stu-id="56e9e-255">Initialize the vertex buffer view: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span></span>
-   <span data-ttu-id="56e9e-256">Cree e inicialice la barrera: [**ID3D12Device:: CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span><span class="sxs-lookup"><span data-stu-id="56e9e-256">Create and initialize the fence: [**ID3D12Device::CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span></span>
-   <span data-ttu-id="56e9e-257">Cree un identificador de evento para usarlo con la sincronización de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="56e9e-257">Create an event handle for use with frame synchronization.</span></span>
-   <span data-ttu-id="56e9e-258">Espere a que finalice la GPU.</span><span class="sxs-lookup"><span data-stu-id="56e9e-258">Wait for the GPU to finish.</span></span>


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



### <a name="onupdate"></a><span data-ttu-id="56e9e-259">Actualizar ()</span><span class="sxs-lookup"><span data-stu-id="56e9e-259">OnUpdate()</span></span>

<span data-ttu-id="56e9e-260">Para un ejemplo simple, no se actualiza nada.</span><span class="sxs-lookup"><span data-stu-id="56e9e-260">For a simple example, nothing is updated.</span></span>


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a><span data-ttu-id="56e9e-261">OnRender ()</span><span class="sxs-lookup"><span data-stu-id="56e9e-261">OnRender()</span></span>

<span data-ttu-id="56e9e-262">Durante la configuración, la variable miembro **m \_ commandList** se usó para registrar y ejecutar todos los comandos de configuración.</span><span class="sxs-lookup"><span data-stu-id="56e9e-262">During set up, the member variable **m\_commandList** was used to record and execute all of the set up commands.</span></span> <span data-ttu-id="56e9e-263">Ahora puede volver a usar ese miembro en el bucle de representación principal.</span><span class="sxs-lookup"><span data-stu-id="56e9e-263">You can now reuse that member in the main render loop.</span></span>

<span data-ttu-id="56e9e-264">La representación implica una llamada a para rellenar la lista de comandos y, a continuación, se puede ejecutar la lista de comandos y se presenta el siguiente búfer en la cadena de intercambio:</span><span class="sxs-lookup"><span data-stu-id="56e9e-264">Rendering involves a call to populate the command list, then the command list can be executed and the next buffer in the swap chain presented:</span></span>

-   <span data-ttu-id="56e9e-265">Rellene la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-265">Populate the command list.</span></span>
-   <span data-ttu-id="56e9e-266">Ejecute la lista de comandos: [**ID3D12CommandQueue:: ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span><span class="sxs-lookup"><span data-stu-id="56e9e-266">Execute the command list: [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>
-   <span data-ttu-id="56e9e-267">[**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) el marco.</span><span class="sxs-lookup"><span data-stu-id="56e9e-267">[**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) the frame.</span></span>
-   <span data-ttu-id="56e9e-268">Espere a que finalice la GPU.</span><span class="sxs-lookup"><span data-stu-id="56e9e-268">Wait on the GPU to finish.</span></span>


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



### <a name="populatecommandlist"></a><span data-ttu-id="56e9e-269">PopulateCommandList()</span><span class="sxs-lookup"><span data-stu-id="56e9e-269">PopulateCommandList()</span></span>

<span data-ttu-id="56e9e-270">Debe restablecer el asignador de la lista de comandos y la lista de comandos antes de poder reutilizarlos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-270">You must reset the command list allocator and the command list itself before you can reuse them.</span></span> <span data-ttu-id="56e9e-271">En escenarios más avanzados, puede tener sentido restablecer el asignador cada varios fotogramas.</span><span class="sxs-lookup"><span data-stu-id="56e9e-271">In more advanced scenarios it might make sense to reset the allocator every several frames.</span></span> <span data-ttu-id="56e9e-272">La memoria está asociada al asignador que no se puede liberar inmediatamente después de ejecutar una lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="56e9e-272">Memory is associated with the allocator that can't be released immediately after executing a command list.</span></span> <span data-ttu-id="56e9e-273">En este ejemplo se muestra cómo restablecer el asignador después de cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="56e9e-273">This example shows how to reset the allocator after every frame.</span></span>

<span data-ttu-id="56e9e-274">Ahora, vuelva a usar la lista de comandos para el marco actual.</span><span class="sxs-lookup"><span data-stu-id="56e9e-274">Now, reuse the command list for the current frame.</span></span> <span data-ttu-id="56e9e-275">Vuelva a adjuntar la ventanilla a la lista de comandos (que se debe hacer siempre que se restablezca una lista de comandos y antes de que se ejecute la lista de comandos), indicar que el recurso se usará como destino de representación, grabar comandos y, a continuación, indicar que el destino de representación se usará para presentar cuando la lista de comandos termine de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="56e9e-275">Reattach the viewport to the command list (which must be done whenever a command list is reset, and before the command list is executed), indicate that the resource will be in use as a render target, record commands, and then indicate that the render target will be used to present when the command list is done executing.</span></span>

<span data-ttu-id="56e9e-276">Al rellenar las listas de comandos, se llama a los siguientes métodos y procesos a su vez:</span><span class="sxs-lookup"><span data-stu-id="56e9e-276">Populating command lists calls the following methods and processes in turn:</span></span>

-   <span data-ttu-id="56e9e-277">Restablezca el asignador de comandos y la lista de comandos:</span><span class="sxs-lookup"><span data-stu-id="56e9e-277">Reset the command allocator, and command list:</span></span> <dl>

[<span data-ttu-id="56e9e-278">**ID3D12CommandAllocator:: RESET**</span><span class="sxs-lookup"><span data-stu-id="56e9e-278">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [<span data-ttu-id="56e9e-279">**ID3D12GraphicsCommandList:: RESET**</span><span class="sxs-lookup"><span data-stu-id="56e9e-279">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   <span data-ttu-id="56e9e-280">Establezca la firma raíz, la ventanilla y los rectángulos de tijeras:</span><span class="sxs-lookup"><span data-stu-id="56e9e-280">Set the root signature, viewport and scissors rectangles:</span></span> <dl>

[<span data-ttu-id="56e9e-281">**ID3D12GraphicsCommandList::SetGraphicsRootSignature**</span><span class="sxs-lookup"><span data-stu-id="56e9e-281">**ID3D12GraphicsCommandList::SetGraphicsRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [<span data-ttu-id="56e9e-282">**ID3D12GraphicsCommandList::RSSetViewports**</span><span class="sxs-lookup"><span data-stu-id="56e9e-282">**ID3D12GraphicsCommandList::RSSetViewports**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [<span data-ttu-id="56e9e-283">**ID3D12GraphicsCommandList::RSSetScissorRects**</span><span class="sxs-lookup"><span data-stu-id="56e9e-283">**ID3D12GraphicsCommandList::RSSetScissorRects**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   <span data-ttu-id="56e9e-284">Indica que el búfer de reserva se va a usar como destino de representación:</span><span class="sxs-lookup"><span data-stu-id="56e9e-284">Indicate that the back buffer is to be used as a render target:</span></span> <dl>

[<span data-ttu-id="56e9e-285">**ID3D12GraphicsCommandList::ResourceBarrier**</span><span class="sxs-lookup"><span data-stu-id="56e9e-285">**ID3D12GraphicsCommandList::ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [<span data-ttu-id="56e9e-286">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span><span class="sxs-lookup"><span data-stu-id="56e9e-286">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="56e9e-287">**ID3D12GraphicsCommandList::OMSetRenderTargets**</span><span class="sxs-lookup"><span data-stu-id="56e9e-287">**ID3D12GraphicsCommandList::OMSetRenderTargets**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   <span data-ttu-id="56e9e-288">Grabe los comandos:</span><span class="sxs-lookup"><span data-stu-id="56e9e-288">Record the commands:</span></span><dl>

[<span data-ttu-id="56e9e-289">**ID3D12GraphicsCommandList::ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="56e9e-289">**ID3D12GraphicsCommandList::ClearRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [<span data-ttu-id="56e9e-290">**ID3D12GraphicsCommandList::IASetPrimitiveTopology**</span><span class="sxs-lookup"><span data-stu-id="56e9e-290">**ID3D12GraphicsCommandList::IASetPrimitiveTopology**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [<span data-ttu-id="56e9e-291">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="56e9e-291">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [<span data-ttu-id="56e9e-292">**ID3D12GraphicsCommandList::D rawInstanced**</span><span class="sxs-lookup"><span data-stu-id="56e9e-292">**ID3D12GraphicsCommandList::DrawInstanced**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   <span data-ttu-id="56e9e-293">Indica que el búfer de reserva se usará ahora para presentar: [**ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="56e9e-293">Indicate the back buffer will now be used to present: [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>
-   <span data-ttu-id="56e9e-294">Cierre la lista de comandos: [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span><span class="sxs-lookup"><span data-stu-id="56e9e-294">Close the command list: [**ID3D12GraphicsCommandList::Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span></span>


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



### <a name="waitforpreviousframe"></a><span data-ttu-id="56e9e-295">WaitForPreviousFrame()</span><span class="sxs-lookup"><span data-stu-id="56e9e-295">WaitForPreviousFrame()</span></span>

<span data-ttu-id="56e9e-296">En el código siguiente se muestra un uso simplificado de las barreras.</span><span class="sxs-lookup"><span data-stu-id="56e9e-296">The following code shows an over-simplified use of fences.</span></span>

> [!Note]  
> <span data-ttu-id="56e9e-297">Esperar a que se complete un fotograma es demasiado ineficaz para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="56e9e-297">Waiting for a frame to complete is too inefficient for most apps.</span></span>

 

<span data-ttu-id="56e9e-298">Se llama a las siguientes API y procesos en orden:</span><span class="sxs-lookup"><span data-stu-id="56e9e-298">The following APIs and processes are called in order:</span></span>

-   [<span data-ttu-id="56e9e-299">**ID3D12CommandQueue:: Signal**</span><span class="sxs-lookup"><span data-stu-id="56e9e-299">**ID3D12CommandQueue::Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [<span data-ttu-id="56e9e-300">**ID3D12Fence::GetCompletedValue**</span><span class="sxs-lookup"><span data-stu-id="56e9e-300">**ID3D12Fence::GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [<span data-ttu-id="56e9e-301">**ID3D12Fence::SetEventOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="56e9e-301">**ID3D12Fence::SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   <span data-ttu-id="56e9e-302">Espere el evento.</span><span class="sxs-lookup"><span data-stu-id="56e9e-302">Wait for the event.</span></span>
-   <span data-ttu-id="56e9e-303">Actualice el índice del marco: [**IDXGISwapChain3:: GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span><span class="sxs-lookup"><span data-stu-id="56e9e-303">Update the frame index: [**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span></span>


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



### <a name="ondestroy"></a><span data-ttu-id="56e9e-304">Aldestruir ()</span><span class="sxs-lookup"><span data-stu-id="56e9e-304">OnDestroy()</span></span>

<span data-ttu-id="56e9e-305">Cierre la aplicación correctamente.</span><span class="sxs-lookup"><span data-stu-id="56e9e-305">Cleanly close down the app.</span></span>

-   <span data-ttu-id="56e9e-306">Espere a que finalice la GPU.</span><span class="sxs-lookup"><span data-stu-id="56e9e-306">Wait for the GPU to finish.</span></span>
-   <span data-ttu-id="56e9e-307">Cierre el evento.</span><span class="sxs-lookup"><span data-stu-id="56e9e-307">Close the event.</span></span>


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a><span data-ttu-id="56e9e-308">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56e9e-308">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56e9e-309">Descripción de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="56e9e-309">Understanding Direct3D 12</span></span>](directx-12-getting-started.md)
</dt> <dt>

[<span data-ttu-id="56e9e-310">Ejemplos de trabajo</span><span class="sxs-lookup"><span data-stu-id="56e9e-310">Working Samples</span></span>](working-samples.md)
</dt> </dl>

 

 
