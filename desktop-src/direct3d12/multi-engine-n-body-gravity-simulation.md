---
title: Simulación de la gravedad n-Body de varios motores
description: En el ejemplo D3D12nBodyGravity se muestra cómo realizar el trabajo de proceso de forma asincrónica.
ms.assetid: B20C5575-0616-43F7-9AC9-5F802E5597B5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60782519de6f655882717c4ea657668129a6ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549093"
---
# <a name="multi-engine-n-body-gravity-simulation"></a><span data-ttu-id="b5ee8-103">Simulación de la gravedad n-Body de varios motores</span><span class="sxs-lookup"><span data-stu-id="b5ee8-103">Multi-engine n-body gravity simulation</span></span>

<span data-ttu-id="b5ee8-104">En el ejemplo **D3D12nBodyGravity** se muestra cómo realizar el trabajo de proceso de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-104">The **D3D12nBodyGravity** sample demonstrates how to do compute work asynchronously.</span></span> <span data-ttu-id="b5ee8-105">El ejemplo pone en marcha un número de subprocesos con una cola de comandos de proceso y programa el trabajo de proceso en la GPU que realiza una simulación de gravedad n-Body.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-105">The sample spins up a number of threads each with a compute command queue and schedules compute work on the GPU that performs an n-body gravity simulation.</span></span> <span data-ttu-id="b5ee8-106">Cada subproceso opera en dos búferes llenos de datos de la posición y la velocidad.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-106">Each thread operates on two buffers full of position and velocity data.</span></span> <span data-ttu-id="b5ee8-107">Con cada iteración, el sombreador de cálculo lee la posición actual y los datos de velocidad de un búfer y escribe la siguiente iteración en el otro búfer.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-107">With each iteration, the compute shader reads the current position and velocity data from one buffer and writes the next iteration into the other buffer.</span></span> <span data-ttu-id="b5ee8-108">Una vez completada la iteración, el sombreador de cálculo intercambia qué búfer es el SRV para leer los datos de posición/velocidad y cuál es el UAV para escribir las actualizaciones de posición/velocidad cambiando el estado del recurso en cada búfer.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-108">When the iteration completes, the compute shader swaps which buffer is the SRV for reading position/velocity data and which is the UAV for writing position/velocity updates by changing the resource state on each buffer.</span></span>

-   [<span data-ttu-id="b5ee8-109">Crear las firmas raíz</span><span class="sxs-lookup"><span data-stu-id="b5ee8-109">Create the root signatures</span></span>](#create-the-root-signatures)
-   [<span data-ttu-id="b5ee8-110">Creación de los búferes SRV y UAV</span><span class="sxs-lookup"><span data-stu-id="b5ee8-110">Create the SRV and UAV buffers</span></span>](#create-the-srv-and-uav-buffers)
-   [<span data-ttu-id="b5ee8-111">Crear los búferes de CBV y vértices</span><span class="sxs-lookup"><span data-stu-id="b5ee8-111">Create the CBV and vertex buffers</span></span>](#create-the-cbv-and-vertex-buffers)
-   [<span data-ttu-id="b5ee8-112">Sincronizar los subprocesos de representación y cálculo</span><span class="sxs-lookup"><span data-stu-id="b5ee8-112">Synchronize the rendering and compute threads</span></span>](#synchronize-the-rendering-and-compute-threads)
-   [<span data-ttu-id="b5ee8-113">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="b5ee8-113">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="b5ee8-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b5ee8-114">Related topics</span></span>](#related-topics)

## <a name="create-the-root-signatures"></a><span data-ttu-id="b5ee8-115">Crear las firmas raíz</span><span class="sxs-lookup"><span data-stu-id="b5ee8-115">Create the root signatures</span></span>

<span data-ttu-id="b5ee8-116">Empezamos por crear un gráfico y una firma de raíz de proceso, en el método **LoadAssets** .</span><span class="sxs-lookup"><span data-stu-id="b5ee8-116">We start out by creating both a graphics and a compute root signature, in the **LoadAssets** method.</span></span> <span data-ttu-id="b5ee8-117">Ambas signaturas raíz tienen una vista de búfer de constantes raíz (CBV) y una tabla de descriptores de vista de recursos de sombreador (SRV).</span><span class="sxs-lookup"><span data-stu-id="b5ee8-117">Both root signatures have a root constant buffer view (CBV) and a shader resource view (SRV) descriptor table.</span></span> <span data-ttu-id="b5ee8-118">La firma raíz de proceso también tiene una tabla de descriptor de vista de acceso no ordenada (UAV).</span><span class="sxs-lookup"><span data-stu-id="b5ee8-118">The compute root signature also has an unordered access view (UAV) descriptor table.</span></span>

``` syntax
 // Create the root signatures.
       {
              CD3DX12_DESCRIPTOR_RANGE ranges[2];
              ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1, 0);
              ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

              CD3DX12_ROOT_PARAMETER rootParameters[RootParametersCount];
              rootParameters[RootParameterCB].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_ALL);
              rootParameters[RootParameterSRV].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_VERTEX);
              rootParameters[RootParameterUAV].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_ALL);

              // The rendering pipeline does not need the UAV parameter.
              CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
              rootSignatureDesc.Init(_countof(rootParameters) - 1, rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

              ComPtr<ID3DBlob> signature;
              ComPtr<ID3DBlob> error;
              ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

              // Create compute signature. Must change visibility for the SRV.
              rootParameters[RootParameterSRV].ShaderVisibility = D3D12_SHADER_VISIBILITY_ALL;

              CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc(_countof(rootParameters), rootParameters, 0, nullptr);
              ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));

              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
       }
```



| <span data-ttu-id="b5ee8-119">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="b5ee8-119">Call flow</span></span>                                                             | <span data-ttu-id="b5ee8-120">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5ee8-120">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b5ee8-121">**\_Intervalo de descriptor de CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-121">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="b5ee8-122">**\_Tipo de intervalo de descriptor D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-122">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="b5ee8-123">**\_Parámetro raíz \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-123">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="b5ee8-124">**\_Visibilidad del sombreador de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-124">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="b5ee8-125">**Descripción de la \_ firma raíz de CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-125">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="b5ee8-126">**D3D12 \_ \_ marcas de firma raíz \_**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-126">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="b5ee8-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b5ee8-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="b5ee8-128">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-128">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="b5ee8-129">**Versión de la \_ firma raíz D3D \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-129">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="b5ee8-130">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-130">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [<span data-ttu-id="b5ee8-131">**Descripción de la \_ firma raíz de CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-131">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) |                                                                       |
| [<span data-ttu-id="b5ee8-132">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-132">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="b5ee8-133">**Versión de la \_ firma raíz D3D \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-133">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="b5ee8-134">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-134">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-srv-and-uav-buffers"></a><span data-ttu-id="b5ee8-135">Creación de los búferes SRV y UAV</span><span class="sxs-lookup"><span data-stu-id="b5ee8-135">Create the SRV and UAV buffers</span></span>

<span data-ttu-id="b5ee8-136">Los búferes SRV y UAV se componen de una matriz de datos de posición y velocidad.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-136">The SRV and UAV buffers consist of an array of position and velocity data.</span></span>

``` syntax
 // Position and velocity data for the particles in the system.
       // Two buffers full of Particle data are utilized in this sample.
       // The compute thread alternates writing to each of them.
       // The render thread renders using the buffer that is not currently
       // in use by the compute shader.
       struct Particle
       {
              XMFLOAT4 position;
              XMFLOAT4 velocity;
       };
```



| <span data-ttu-id="b5ee8-137">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="b5ee8-137">Call flow</span></span>                       | <span data-ttu-id="b5ee8-138">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5ee8-138">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="b5ee8-139">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-139">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

## <a name="create-the-cbv-and-vertex-buffers"></a><span data-ttu-id="b5ee8-140">Crear los búferes de CBV y vértices</span><span class="sxs-lookup"><span data-stu-id="b5ee8-140">Create the CBV and vertex buffers</span></span>

<span data-ttu-id="b5ee8-141">Para la canalización de gráficos, CBV es un **struct** que contiene dos matrices usadas por el sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-141">For the graphics pipeline, the CBV is a **struct** containing two matrices used by the geometry shader.</span></span> <span data-ttu-id="b5ee8-142">El sombreador de geometría toma la posición de cada partícula del sistema y genera una cuádruple para representarla mediante estas matrices.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-142">The geometry shader takes the position of each particle in the system and generates a quad to represent it using these matrices.</span></span>

``` syntax
 struct ConstantBufferGS
       {
              XMMATRIX worldViewProjection;
              XMMATRIX inverseView;

              // Constant buffers are 256-byte aligned in GPU memory. Padding is added
              // for convenience when computing the struct's size.
              float padding[32];
       };
```



| <span data-ttu-id="b5ee8-143">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="b5ee8-143">Call flow</span></span>                       | <span data-ttu-id="b5ee8-144">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5ee8-144">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="b5ee8-145">**XMMATRIX**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-145">**XMMATRIX**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) |            |



 

<span data-ttu-id="b5ee8-146">Como resultado, el búfer de vértices utilizado por el sombreador de vértices realmente no contiene ningún dato posicional.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-146">As a result, the vertex buffer used by the vertex shader actually does not contain any positional data.</span></span>

``` syntax
 // "Vertex" definition for particles. Triangle vertices are generated 
       // by the geometry shader. Color data will be assigned to those 
       // vertices via this struct.
       struct ParticleVertex
       {
              XMFLOAT4 color;
       };
```



| <span data-ttu-id="b5ee8-147">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="b5ee8-147">Call flow</span></span>                       | <span data-ttu-id="b5ee8-148">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5ee8-148">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="b5ee8-149">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-149">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

<span data-ttu-id="b5ee8-150">Para la canalización de proceso, CBV es un **struct** que contiene algunas constantes usadas por la simulación de gravedad n-Body en el sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-150">For the compute pipeline, the CBV is a **struct** containing some constants used by the n-body gravity simulation in the compute shader.</span></span>

``` syntax
 struct ConstantBufferCS
       {
              UINT param[4];
              float paramf[4];
       };
```

## <a name="synchronize-the-rendering-and-compute-threads"></a><span data-ttu-id="b5ee8-151">Sincronizar los subprocesos de representación y cálculo</span><span class="sxs-lookup"><span data-stu-id="b5ee8-151">Synchronize the rendering and compute threads</span></span>

<span data-ttu-id="b5ee8-152">Una vez que se inicializan todos los búferes, se iniciará la representación y el trabajo de proceso.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-152">After the buffers are all initialized, the rendering and compute work will begin.</span></span> <span data-ttu-id="b5ee8-153">El subproceso de cálculo cambiará el estado de los dos búferes de posición/velocidad entre el SRV y el UAV a medida que recorre en iteración la simulación, y el subproceso de representación debe asegurarse de que programa el trabajo en la canalización de gráficos que opera en el SRV.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-153">The compute thread will be changing the state of the two position/velocity buffers back and forth between SRV and UAV as it iterates on the simulation, and the rendering thread needs to ensure that it schedules work on the graphics pipeline that operates on the SRV.</span></span> <span data-ttu-id="b5ee8-154">Las barreras se utilizan para sincronizar el acceso a los dos búferes.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-154">Fences are used to synchronize access to the two buffers.</span></span>

<span data-ttu-id="b5ee8-155">En el subproceso de representación:</span><span class="sxs-lookup"><span data-stu-id="b5ee8-155">On the Render thread:</span></span>

``` syntax
// Render the scene.
void D3D12nBodyGravity::OnRender()
{
       // Let the compute thread know that a new frame is being rendered.
       for (int n = 0; n < ThreadCount; n++)
       {
              InterlockedExchange(&m_renderContextFenceValues[n], m_renderContextFenceValue);
       }

       // Compute work must be completed before the frame can render or else the SRV 
       // will be in the wrong state.
       for (UINT n = 0; n < ThreadCount; n++)
       {
              UINT64 threadFenceValue = InterlockedGetValue(&m_threadFenceValues[n]);
              if (m_threadFences[n]->GetCompletedValue() < threadFenceValue)
              {
                     // Instruct the rendering command queue to wait for the current 
                     // compute work to complete.
                     ThrowIfFailed(m_commandQueue->Wait(m_threadFences[n].Get(), threadFenceValue));
              }
       }

       // Record all the commands we need to render the scene into the command list.
       PopulateCommandList();

       // Execute the command list.
       ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
       m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

       // Present the frame.
       ThrowIfFailed(m_swapChain->Present(0, 0));

       MoveToNextFrame();
}
```



| <span data-ttu-id="b5ee8-156">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="b5ee8-156">Call flow</span></span>                                                              | <span data-ttu-id="b5ee8-157">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5ee8-157">Parameters</span></span> |
|------------------------------------------------------------------------|------------|
| [<span data-ttu-id="b5ee8-158">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-158">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                  |            |
| [<span data-ttu-id="b5ee8-159">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-159">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)           |            |
| [<span data-ttu-id="b5ee8-160">**GetCompletedValue**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-160">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)             |            |
| [<span data-ttu-id="b5ee8-161">**Esperar**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-161">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                |            |
| [<span data-ttu-id="b5ee8-162">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-162">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [<span data-ttu-id="b5ee8-163">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-163">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [<span data-ttu-id="b5ee8-164">**IDXGISwapChain1::Present1**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-164">**IDXGISwapChain1::Present1**</span></span>](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

<span data-ttu-id="b5ee8-165">Para simplificar el ejemplo un bit, el subproceso de cálculo espera a que la GPU Complete cada iteración antes de programar más trabajo de proceso.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-165">To simplify the sample a bit, the compute thread waits for the GPU to complete each iteration before scheduling any more compute work.</span></span> <span data-ttu-id="b5ee8-166">En la práctica, es probable que las aplicaciones deseen mantener la cola de proceso completa para lograr el máximo rendimiento de la GPU.</span><span class="sxs-lookup"><span data-stu-id="b5ee8-166">In practice, applications will likely want to keep the compute queue full to achieve maximum performance from the GPU.</span></span>

<span data-ttu-id="b5ee8-167">En el subproceso Compute:</span><span class="sxs-lookup"><span data-stu-id="b5ee8-167">On the Compute thread:</span></span>

``` syntax
DWORD D3D12nBodyGravity::AsyncComputeThreadProc(int threadIndex)
{
       ID3D12CommandQueue* pCommandQueue = m_computeCommandQueue[threadIndex].Get();
       ID3D12CommandAllocator* pCommandAllocator = m_computeAllocator[threadIndex].Get();
       ID3D12GraphicsCommandList* pCommandList = m_computeCommandList[threadIndex].Get();
       ID3D12Fence* pFence = m_threadFences[threadIndex].Get();

       while (0 == InterlockedGetValue(&m_terminating))
       {
              // Run the particle simulation.
              Simulate(threadIndex);

              // Close and execute the command list.
              ThrowIfFailed(pCommandList->Close());
              ID3D12CommandList* ppCommandLists[] = { pCommandList };

              pCommandQueue->ExecuteCommandLists(1, ppCommandLists);

              // Wait for the compute shader to complete the simulation.
              UINT64 threadFenceValue = InterlockedIncrement(&m_threadFenceValues[threadIndex]);
              ThrowIfFailed(pCommandQueue->Signal(pFence, threadFenceValue));
              ThrowIfFailed(pFence->SetEventOnCompletion(threadFenceValue, m_threadFenceEvents[threadIndex]));
              WaitForSingleObject(m_threadFenceEvents[threadIndex], INFINITE);

              // Wait for the render thread to be done with the SRV so that
              // the next frame in the simulation can run.
              UINT64 renderContextFenceValue = InterlockedGetValue(&m_renderContextFenceValues[threadIndex]);
              if (m_renderContextFence->GetCompletedValue() < renderContextFenceValue)
              {
                     ThrowIfFailed(pCommandQueue->Wait(m_renderContextFence.Get(), renderContextFenceValue));
                     InterlockedExchange(&m_renderContextFenceValues[threadIndex], 0);
              }

              // Swap the indices to the SRV and UAV.
              m_srvIndex[threadIndex] = 1 - m_srvIndex[threadIndex];

              // Prepare for the next frame.
              ThrowIfFailed(pCommandAllocator->Reset());
              ThrowIfFailed(pCommandList->Reset(pCommandAllocator, m_computeState.Get()));
       }

       return 0;
}
```



| <span data-ttu-id="b5ee8-168">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="b5ee8-168">Call flow</span></span>                                                                   | <span data-ttu-id="b5ee8-169">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5ee8-169">Parameters</span></span> |
|-----------------------------------------------------------------------------|------------|
| [<span data-ttu-id="b5ee8-170">**ID3D12CommandQueue**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-170">**ID3D12CommandQueue**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)                            |            |
| [<span data-ttu-id="b5ee8-171">**ID3D12CommandAllocator**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-171">**ID3D12CommandAllocator**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)                    |            |
| [<span data-ttu-id="b5ee8-172">**ID3D12GraphicsCommandList**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-172">**ID3D12GraphicsCommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)              |            |
| [<span data-ttu-id="b5ee8-173">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-173">**ID3D12Fence**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)                                          |            |
| [<span data-ttu-id="b5ee8-174">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-174">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="b5ee8-175">**Cercanos**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-175">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)                            |            |
| [<span data-ttu-id="b5ee8-176">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-176">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                              |            |
| [<span data-ttu-id="b5ee8-177">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-177">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)       |            |
| [<span data-ttu-id="b5ee8-178">**InterlockedIncrement**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-178">**InterlockedIncrement**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedincrement)                     |            |
| [<span data-ttu-id="b5ee8-179">**Marcar**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-179">**Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                                 |            |
| [<span data-ttu-id="b5ee8-180">**SetEventOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-180">**SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)            |            |
| [<span data-ttu-id="b5ee8-181">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-181">**WaitForSingleObject**</span></span>](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)                         |            |
| [<span data-ttu-id="b5ee8-182">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-182">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="b5ee8-183">**GetCompletedValue**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-183">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)                  |            |
| [<span data-ttu-id="b5ee8-184">**Esperar**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-184">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                     |            |
| [<span data-ttu-id="b5ee8-185">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-185">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                       |            |
| [<span data-ttu-id="b5ee8-186">**ID3D12CommandAllocator:: RESET**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-186">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)       |            |
| [<span data-ttu-id="b5ee8-187">**ID3D12GraphicsCommandList:: RESET**</span><span class="sxs-lookup"><span data-stu-id="b5ee8-187">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) |            |



 

## <a name="run-the-sample"></a><span data-ttu-id="b5ee8-188">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="b5ee8-188">Run the sample</span></span>

![una captura de pantalla de la simulación de la gravedad del cuerpo n final](images/nbodygravity.png)

## <a name="related-topics"></a><span data-ttu-id="b5ee8-190">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b5ee8-190">Related topics</span></span>

[<span data-ttu-id="b5ee8-191">Tutoriales de código D3D12</span><span class="sxs-lookup"><span data-stu-id="b5ee8-191">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)

[<span data-ttu-id="b5ee8-192">Sincronización de varios motores</span><span class="sxs-lookup"><span data-stu-id="b5ee8-192">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)