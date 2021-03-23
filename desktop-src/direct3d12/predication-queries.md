---
title: Consultas de Predication
description: En el ejemplo D3D12PredicationQueries se muestra la selección de la oclusión mediante montones de consulta de DirectX 12 y predication. En el tutorial se describe el código adicional necesario para extender el ejemplo HelloConstBuffer para controlar las consultas de predication.
ms.assetid: F61817BB-45BC-4977-BE4A-EE0FDAFBCB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad14e55864ee8d568acc0c9eb46134834d27ff54
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/05/2021
ms.locfileid: "104549063"
---
# <a name="predication-queries"></a><span data-ttu-id="7fac3-104">Consultas de Predication</span><span class="sxs-lookup"><span data-stu-id="7fac3-104">Predication queries</span></span>

<span data-ttu-id="7fac3-105">En el ejemplo **D3D12PredicationQueries** se muestra la selección de la oclusión mediante montones de consulta de DirectX 12 y predication.</span><span class="sxs-lookup"><span data-stu-id="7fac3-105">The **D3D12PredicationQueries** sample demonstrates occlusion culling using DirectX 12 query heaps and predication.</span></span> <span data-ttu-id="7fac3-106">En el tutorial se describe el código adicional necesario para extender el ejemplo **HelloConstBuffer** para controlar las consultas de predication.</span><span class="sxs-lookup"><span data-stu-id="7fac3-106">The walkthrough describes the additional code needed to extend the **HelloConstBuffer** sample to handle predication queries.</span></span>

-   [<span data-ttu-id="7fac3-107">Crear un montón de descriptor de estarcido de profundidad y un montón de consulta de oclusión</span><span class="sxs-lookup"><span data-stu-id="7fac3-107">Create a depth stencil descriptor heap and an occlusion query heap</span></span>](#create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap)
-   [<span data-ttu-id="7fac3-108">Habilitar combinación alfa</span><span class="sxs-lookup"><span data-stu-id="7fac3-108">Enable alpha blending</span></span>](#enable-alpha-blending)
-   [<span data-ttu-id="7fac3-109">Deshabilitar las escrituras de color y de profundidad</span><span class="sxs-lookup"><span data-stu-id="7fac3-109">Disable color and depth writes</span></span>](#disable-color-and-depth-writes)
-   [<span data-ttu-id="7fac3-110">Crear un búfer para almacenar los resultados de la consulta</span><span class="sxs-lookup"><span data-stu-id="7fac3-110">Create a buffer to store the results of the query</span></span>](#create-a-buffer-to-store-the-results-of-the-query)
-   [<span data-ttu-id="7fac3-111">Dibujar las cuatro cuádruples y realizar y resolver la consulta de oclusión</span><span class="sxs-lookup"><span data-stu-id="7fac3-111">Draw the quads and perform and resolve the occlusion query</span></span>](#draw-the-quads-and-perform-and-resolve-the-occlusion-query)
-   [<span data-ttu-id="7fac3-112">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="7fac3-112">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="7fac3-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7fac3-113">Related topics</span></span>](#related-topics)

## <a name="create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap"></a><span data-ttu-id="7fac3-114">Crear un montón de descriptor de estarcido de profundidad y un montón de consulta de oclusión</span><span class="sxs-lookup"><span data-stu-id="7fac3-114">Create a depth stencil descriptor heap and an occlusion query heap</span></span>

<span data-ttu-id="7fac3-115">En el método **LoadPipeline** , cree un montón de descriptor de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="7fac3-115">In the **LoadPipeline** method create a depth stencil descriptor heap.</span></span>

``` syntax
              // Describe and create a depth stencil view (DSV) descriptor heap.
              D3D12_DESCRIPTOR_HEAP_DESC dsvHeapDesc = {};
              dsvHeapDesc.NumDescriptors = 1;
              dsvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_DSV;
              dsvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
              ThrowIfFailed(m_device->CreateDescriptorHeap(&dsvHeapDesc, IID_PPV_ARGS(&m_dsvHeap)));
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7fac3-116">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="7fac3-116">Call flow</span></span></th>
<th><span data-ttu-id="7fac3-117">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fac3-117">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7fac3-118"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-118"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="7fac3-119"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-119"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a></span></span><br />
<span data-ttu-id="7fac3-120">[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="7fac3-120">[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7fac3-121"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-121"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="7fac3-122">En el método **LoadAssets** , cree un montón para las consultas de oclusión.</span><span class="sxs-lookup"><span data-stu-id="7fac3-122">In the **LoadAssets** method create a heap for occlusion queries.</span></span>

``` syntax
     // Describe and create a heap for occlusion queries.
              D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
              queryHeapDesc.Count = 1;
              queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
              ThrowIfFailed(m_device->CreateQueryHeap(&queryHeapDesc, IID_PPV_ARGS(&m_queryHeap)));
```



| <span data-ttu-id="7fac3-123">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="7fac3-123">Call flow</span></span>                                                 | <span data-ttu-id="7fac3-124">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fac3-124">Parameters</span></span>                                                |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="7fac3-125">**D3D12 \_ \_ DESC del montón de consulta \_**</span><span class="sxs-lookup"><span data-stu-id="7fac3-125">**D3D12\_QUERY\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc) | [<span data-ttu-id="7fac3-126">**\_Tipo de \_ montón de consulta D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7fac3-126">**D3D12\_QUERY\_HEAP\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type) |
| [<span data-ttu-id="7fac3-127">**CreateQueryHeap**</span><span class="sxs-lookup"><span data-stu-id="7fac3-127">**CreateQueryHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)   |                                                           |



 

## <a name="enable-alpha-blending"></a><span data-ttu-id="7fac3-128">Habilitar combinación alfa</span><span class="sxs-lookup"><span data-stu-id="7fac3-128">Enable alpha blending</span></span>

<span data-ttu-id="7fac3-129">Este ejemplo dibuja dos cuádruples e ilustra una consulta de oclusión binaria.</span><span class="sxs-lookup"><span data-stu-id="7fac3-129">This sample draws two quads and illustrates a binary occlusion query.</span></span> <span data-ttu-id="7fac3-130">El cuádruple en el anverso se anima en la pantalla y, en ocasiones, se ocluidos.</span><span class="sxs-lookup"><span data-stu-id="7fac3-130">The quad in front animates across the screen, and the one in back will occasionally be occluded.</span></span> <span data-ttu-id="7fac3-131">En el método **LoadAssets** , la combinación alfa está habilitada para este ejemplo, de modo que podamos ver en qué punto D3D tiene en cuenta el cuádruple de back ocluidos.</span><span class="sxs-lookup"><span data-stu-id="7fac3-131">In the **LoadAssets** method, alpha blending is enabled for this sample so that we can see at what point D3D considers the quad in back occluded.</span></span>

``` syntax
     // Enable alpha blending so we can visualize the occlusion query results.
              CD3DX12_BLEND_DESC blendDesc(CD3DX12_DEFAULT);
              blendDesc.RenderTarget[0] =
              {
                     TRUE, FALSE,
                     D3D12_BLEND_SRC_ALPHA, D3D12_BLEND_INV_SRC_ALPHA, D3D12_BLEND_OP_ADD,
                     D3D12_BLEND_ONE, D3D12_BLEND_ZERO, D3D12_BLEND_OP_ADD,
                     D3D12_LOGIC_OP_NOOP,
                     D3D12_COLOR_WRITE_ENABLE_ALL,
              };
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7fac3-132">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="7fac3-132">Call flow</span></span></th>
<th><span data-ttu-id="7fac3-133">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fac3-133">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7fac3-134"><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-134"><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="7fac3-135"><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-135"><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a></span></span><br />
<span data-ttu-id="7fac3-136">[<strong>D3D12_BLEND</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_blend)</span><span class="sxs-lookup"><span data-stu-id="7fac3-136">[<strong>D3D12_BLEND</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend)</span></span><br />
<span data-ttu-id="7fac3-137">[<strong>D3D12_BLEND_OP</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_blend_op)</span><span class="sxs-lookup"><span data-stu-id="7fac3-137">[<strong>D3D12_BLEND_OP</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend_op)</span></span><br />
<span data-ttu-id="7fac3-138">[<strong>D3D12_LOGIC_OP</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_logic_op)</span><span class="sxs-lookup"><span data-stu-id="7fac3-138">[<strong>D3D12_LOGIC_OP</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_logic_op)</span></span><br />
<span data-ttu-id="7fac3-139">[<strong>D3D12_COLOR_WRITE_ENABLE</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_color_write_enable)</span><span class="sxs-lookup"><span data-stu-id="7fac3-139">[<strong>D3D12_COLOR_WRITE_ENABLE</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_color_write_enable)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="disable-color-and-depth-writes"></a><span data-ttu-id="7fac3-140">Deshabilitar las escrituras de color y de profundidad</span><span class="sxs-lookup"><span data-stu-id="7fac3-140">Disable color and depth writes</span></span>

<span data-ttu-id="7fac3-141">La consulta de oclusión se realiza mediante la representación de una cuádruple que cubre la misma área que la de la cuádruple cuya visibilidad se desea probar.</span><span class="sxs-lookup"><span data-stu-id="7fac3-141">The occlusion query is performed by rendering a quad that covers the same area as the quad whose visibility we want to test.</span></span> <span data-ttu-id="7fac3-142">En escenas más complejas, es probable que la consulta sea un volumen de límite, en lugar de un cuádruple sencillo.</span><span class="sxs-lookup"><span data-stu-id="7fac3-142">In more complex scenes, the query would likely be a bounding volume, rather than a simple quad.</span></span> <span data-ttu-id="7fac3-143">En cualquier caso, se crea un nuevo estado de canalización que deshabilita la escritura en el destino de representación y el búfer z para que la propia consulta de oclusión no afecte al resultado visible de la fase de representación.</span><span class="sxs-lookup"><span data-stu-id="7fac3-143">In either case, a new pipeline state is created that disables writing to the render target and the z buffer so that the occlusion query itself does not affect the visible output of the rendering pass.</span></span>

<span data-ttu-id="7fac3-144">En el método **LoadAssets** , deshabilite las escrituras de color y las escrituras de profundidad para el estado de la consulta de la oclusión.</span><span class="sxs-lookup"><span data-stu-id="7fac3-144">In the **LoadAssets** method, disable color writes and depth writes for the occlusion query's state.</span></span>

``` syntax
 // Disable color writes and depth writes for the occlusion query's state.
              psoDesc.BlendState.RenderTarget[0].RenderTargetWriteMask = 0;
              psoDesc.DepthStencilState.DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ZERO;

              ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_queryState)));
```



| <span data-ttu-id="7fac3-145">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="7fac3-145">Call flow</span></span>                                                                            | <span data-ttu-id="7fac3-146">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fac3-146">Parameters</span></span>                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="7fac3-147">**\_Descripción de \_ Estado de canalización de gráficos de \_ D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7fac3-147">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) | [<span data-ttu-id="7fac3-148">**D3D12 \_ \_ máscara de escritura de profundidad \_**</span><span class="sxs-lookup"><span data-stu-id="7fac3-148">**D3D12\_DEPTH\_WRITE\_MASK**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) |
| [<span data-ttu-id="7fac3-149">**CreateGraphicsPipelineState**</span><span class="sxs-lookup"><span data-stu-id="7fac3-149">**CreateGraphicsPipelineState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)      |                                                             |



 

## <a name="create-a-buffer-to-store-the-results-of-the-query"></a><span data-ttu-id="7fac3-150">Crear un búfer para almacenar los resultados de la consulta</span><span class="sxs-lookup"><span data-stu-id="7fac3-150">Create a buffer to store the results of the query</span></span>

<span data-ttu-id="7fac3-151">En el método **LoadAssets** se debe crear un búfer para almacenar los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="7fac3-151">In the **LoadAssets** method a buffer needs to be created to store the results of the query.</span></span> <span data-ttu-id="7fac3-152">Cada consulta requiere 8 bytes de espacio en la memoria de GPU.</span><span class="sxs-lookup"><span data-stu-id="7fac3-152">Each query requires 8 bytes of space in GPU memory.</span></span> <span data-ttu-id="7fac3-153">Este ejemplo solo realiza una consulta y, para mayor simplicidad y legibilidad, crea un búfer exactamente ese tamaño (aunque esta llamada de función asignará una página de 64K de la memoria de GPU, es probable que la mayoría de las aplicaciones reales creen un búfer mayor).</span><span class="sxs-lookup"><span data-stu-id="7fac3-153">This sample only performs one query and for simplicity and readability creates a buffer exactly that size (even though this function call will allocate a 64K page of GPU memory - most real apps would likely create a larger buffer).</span></span>

``` syntax
 // Create the query result buffer.
              CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
              auto queryBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(8);
              ThrowIfFailed(m_device->CreateCommittedResource(
                     &heapProps,
                     D3D12_HEAP_FLAG_NONE,
                     &queryBufferDesc,
                     D3D12_RESOURCE_STATE_GENERIC_READ,
                     nullptr,
                     IID_PPV_ARGS(&m_queryResult)
                     ));
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7fac3-154">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="7fac3-154">Call flow</span></span></th>
<th><span data-ttu-id="7fac3-155">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fac3-155">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7fac3-156"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-156"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="7fac3-157"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-157"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br />
<span data-ttu-id="7fac3-158">[<strong>D3D12_HEAP_TYPE</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="7fac3-158">[<strong>D3D12_HEAP_TYPE</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span></span><br />
<span data-ttu-id="7fac3-159">[<strong>D3D12_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="7fac3-159">[<strong>D3D12_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags)</span></span><br />
<span data-ttu-id="7fac3-160">[<strong>CD3DX12_RESOURCE_DESC</strong>] (cd3dx12-resource-desc.md)</span><span class="sxs-lookup"><span data-stu-id="7fac3-160">[<strong>CD3DX12_RESOURCE_DESC</strong>](cd3dx12-resource-desc.md)</span></span><br />
<span data-ttu-id="7fac3-161">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="7fac3-161">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="draw-the-quads-and-perform-and-resolve-the-occlusion-query"></a><span data-ttu-id="7fac3-162">Dibujar las cuatro cuádruples y realizar y resolver la consulta de oclusión</span><span class="sxs-lookup"><span data-stu-id="7fac3-162">Draw the quads and perform and resolve the occlusion query</span></span>

<span data-ttu-id="7fac3-163">Una vez realizada la instalación, el bucle principal se actualiza en el método **PopulateCommandLists** .</span><span class="sxs-lookup"><span data-stu-id="7fac3-163">Having done the setup, the main loop is updated in the **PopulateCommandLists** method.</span></span>

<dl> 1. <span data-ttu-id="7fac3-164">Dibuje las cuatro cuádruples desde atrás hacia delante para que el efecto de transparencia funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="7fac3-164">Draw the quads from back to front to make the transparency effect work properly.</span></span> <span data-ttu-id="7fac3-165">Dibujar el cuádruple de vuelta al frente se predica en el resultado de la consulta del fotograma anterior y es una técnica bastante común para esto.</span><span class="sxs-lookup"><span data-stu-id="7fac3-165">Drawing the quad in back to front is predicated on the result of the previous frame’s query and is a fairly common technique for this.</span></span>  
2. <span data-ttu-id="7fac3-166">Cambie el PSO para deshabilitar el destino de representación y las escrituras de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="7fac3-166">Change the PSO to disable render target and depth stencil writes.</span></span>  
3. <span data-ttu-id="7fac3-167">Realice la consulta de oclusión.</span><span class="sxs-lookup"><span data-stu-id="7fac3-167">Perform the occlusion query.</span></span>  
4. <span data-ttu-id="7fac3-168">Resuelva la consulta de oclusión.</span><span class="sxs-lookup"><span data-stu-id="7fac3-168">Resolve the occlusion query.</span></span>  
</dl>

``` syntax
       // Draw the quads and perform the occlusion query.
       {
              CD3DX12_GPU_DESCRIPTOR_HANDLE cbvFarQuad(m_cbvHeap->GetGPUDescriptorHandleForHeapStart(), m_frameIndex * CbvCountPerFrame, m_cbvSrvDescriptorSize);
              CD3DX12_GPU_DESCRIPTOR_HANDLE cbvNearQuad(cbvFarQuad, m_cbvSrvDescriptorSize);

              m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
              m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);

              // Draw the far quad conditionally based on the result of the occlusion query
              // from the previous frame.
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
              m_commandList->SetPredication(m_queryResult.Get(), 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
              m_commandList->DrawInstanced(4, 1, 0, 0);

              // Disable predication and always draw the near quad.
              m_commandList->SetPredication(nullptr, 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvNearQuad);
              m_commandList->DrawInstanced(4, 1, 4, 0);

              // Run the occlusion query with the bounding box quad.
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
              m_commandList->SetPipelineState(m_queryState.Get());
              m_commandList->BeginQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);
              m_commandList->DrawInstanced(4, 1, 8, 0);
              m_commandList->EndQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);

              // Resolve the occlusion query and store the results in the query result buffer
              // to be used on the subsequent frame.
              m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_GENERIC_READ, D3D12_RESOURCE_STATE_COPY_DEST));
              m_commandList->ResolveQueryData(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0, 1, m_queryResult.Get(), 0);
              m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_GENERIC_READ));
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7fac3-169">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="7fac3-169">Call flow</span></span></th>
<th><span data-ttu-id="7fac3-170">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fac3-170">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7fac3-171"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-171"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="7fac3-172"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-172"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7fac3-173"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-173"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span></span></td>
<td><span data-ttu-id="7fac3-174"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-174"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7fac3-175"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-175"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7fac3-176"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-176"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7fac3-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span></span></td>
<td><span data-ttu-id="7fac3-178"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-178"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7fac3-179"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-179"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7fac3-180"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-180"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span></span></td>
<td><span data-ttu-id="7fac3-181"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-181"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7fac3-182"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-182"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7fac3-183"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-183"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7fac3-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7fac3-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>SetPipelineState</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>SetPipelineState</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7fac3-186"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-186"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></span></span></td>
<td><span data-ttu-id="7fac3-187"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-187"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7fac3-188"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-188"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7fac3-189"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>EndQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-189"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>EndQuery</strong></a></span></span></td>
<td><span data-ttu-id="7fac3-190"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-190"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7fac3-191"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-191"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="7fac3-192"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-192"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br />
<span data-ttu-id="7fac3-193">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="7fac3-193">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7fac3-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></span></span></td>
<td><span data-ttu-id="7fac3-195"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-195"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7fac3-196"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-196"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="7fac3-197"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fac3-197"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br />
<span data-ttu-id="7fac3-198">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="7fac3-198">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="run-the-sample"></a><span data-ttu-id="7fac3-199">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="7fac3-199">Run the sample</span></span>

<span data-ttu-id="7fac3-200">No ocluidos:</span><span class="sxs-lookup"><span data-stu-id="7fac3-200">Not occluded:</span></span>

![dos cuadros no ocluidos](images/not-occluded.png)

<span data-ttu-id="7fac3-202">Ocluidos</span><span class="sxs-lookup"><span data-stu-id="7fac3-202">Occluded:</span></span>

![un cuadro totalmente ocluidos](images/occluded.png)

<span data-ttu-id="7fac3-204">Ocluidos parcial:</span><span class="sxs-lookup"><span data-stu-id="7fac3-204">Partially occluded:</span></span>

![un cuadro parcialmente ocluidos](images/partially-occluded.png)

## <a name="related-topics"></a><span data-ttu-id="7fac3-206">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7fac3-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fac3-207">Tutoriales de código D3D12</span><span class="sxs-lookup"><span data-stu-id="7fac3-207">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="7fac3-208">Predication</span><span class="sxs-lookup"><span data-stu-id="7fac3-208">Predication</span></span>](predication.md)
</dt> <dt>

[<span data-ttu-id="7fac3-209">Consultas</span><span class="sxs-lookup"><span data-stu-id="7fac3-209">Queries</span></span>](queries.md)
</dt> </dl>

 

 
