---
title: Dibujo indirecto y selección de GPU
description: El ejemplo D3D12ExecuteIndirect muestra cómo usar comandos indirectos para dibujar contenido. También se muestra cómo se pueden manipular estos comandos en la GPU en un sombreador de proceso antes de que se emita.
ms.assetid: 09F90837-D6BF-498E-8018-5C28EDD9BDC3
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b016170fbd3b675d5d5a20c1de87f24b04d4804
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072960"
---
# <a name="indirect-drawing-and-gpu-culling"></a>Dibujo indirecto y selección de GPU

El ejemplo D3D12ExecuteIndirect muestra cómo usar comandos indirectos para dibujar contenido. También se muestra cómo se pueden manipular estos comandos en la GPU en un sombreador de proceso antes de que se emita.

-   [Definición de los comandos indirectos](#define-the-indirect-commands)
-   [Creación de una firma raíz de gráficos y proceso](#create-a-graphics-and-compute-root-signature)
-   [Creación de una vista de recursos de sombreador (SRV) para el sombreador de proceso](#create-a-shader-resource-view-srv-for-the-compute-shader)
-   [Creación de búferes de comandos indirectos](#create-the-indirect-command-buffers)
-   [Creación de los UAV de proceso](#create-the-compute-uavs)
-   [Dibujar el marco](#drawing-the-frame)
-   [Ejecución del ejemplo](#run-the-sample)
-   [Temas relacionados](#related-topics)

El ejemplo crea un búfer de comandos que describe las llamadas a draw 1024. Cada llamada a draw representa un triángulo con un color, una posición y una velocidad aleatorios. Los triángulos se animan sin fin a través de la pantalla. Hay dos modos en este ejemplo. En el primer modo, un sombreador de proceso inspecciona los comandos indirectos y decide si agregar o no ese comando a una vista de acceso desordenado (UAV) que describe los comandos que se deben ejecutar. En el segundo modo, todos los comandos simplemente se ejecutan. Al presionar la barra espaciadora, se alternará entre modos.

## <a name="define-the-indirect-commands"></a>Definición de los comandos indirectos

Para empezar, definimos el aspecto que deben tener los comandos indirectos. En este ejemplo, los comandos que queremos ejecutar son:

<dl> 1. Actualice la vista de búfer constante (CBV).  
2. Dibuje el triángulo.  
</dl>

Estos comandos de dibujo se representan mediante la siguiente estructura en la definición de clase **D3D12ExecuteIndirect.** Los comandos se ejecutan secuencialmente en el orden en que se definen en esta estructura.

``` syntax
  
// Data structure to match the command signature used for ExecuteIndirect.
struct IndirectCommand
{
       D3D12_GPU_VIRTUAL_ADDRESS cbv;
       D3D12_DRAW_ARGUMENTS drawArguments;
};
```



| Flujo de llamadas                                              | Parámetros |
|--------------------------------------------------------|------------|
| Dirección virtual de GPU D3D12 \_ \_ \_ (simplemente UINT64)         |            |
| [**ARGUMENTOS DE \_ DRAW D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments) |            |



 

Para acompaña a la estructura de datos, también se crea una firma de comando que indica a la GPU cómo interpretar los datos pasados a la API [**ExecuteIndirect.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) Esto, y la mayor parte del código siguiente, se agrega al **método LoadAssets.**

``` syntax
// Create the command signature used for indirect drawing.
{
       // Each command consists of a CBV update and a DrawInstanced call.
       D3D12_INDIRECT_ARGUMENT_DESC argumentDescs[2] = {};
       argumentDescs[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT_BUFFER_VIEW;
       argumentDescs[0].ConstantBufferView.RootParameterIndex = Cbv;
       argumentDescs[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW;

       D3D12_COMMAND_SIGNATURE_DESC commandSignatureDesc = {};
       commandSignatureDesc.pArgumentDescs = argumentDescs;
       commandSignatureDesc.NumArgumentDescs = _countof(argumentDescs);
       commandSignatureDesc.ByteStride = sizeof(IndirectCommand);

       ThrowIfFailed(m_device->CreateCommandSignature(&commandSignatureDesc, m_rootSignature.Get(), IID_PPV_ARGS(&m_commandSignature)));
}
```



| Flujo de llamadas                                                               | Parámetros                                                              |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**D3D12 \_ INDIRECT \_ ARGUMENT \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) | [**TIPO DE ARGUMENTO INDIRECTO D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type) |
| [**D3D12 \_ COMMAND \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc) |                                                                         |
| [**CreateCommandSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)   |                                                                         |



 

## <a name="create-a-graphics-and-compute-root-signature"></a>Creación de una firma raíz de gráficos y proceso

También creamos un gráfico y una firma raíz de proceso. La firma raíz de gráficos simplemente define un CBV raíz. Tenga en cuenta que asignamos el índice de este parámetro raíz en [**D3D12 \_ INDIRECT \_ ARGUMENT \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) (mostrado anteriormente) cuando se define la firma del comando. La firma raíz de proceso define:

-   Una tabla de descriptores común con tres ranuras (dos SRV y un UAV):
    -   Un SRV expone los búferes constantes al sombreador de proceso
    -   Un SRV expone el búfer de comandos al sombreador de proceso
    -   El UAV es donde el sombreador de proceso guarda los comandos de los triángulos visibles.
-   Cuatro constantes raíz:
    -   Mitad del ancho de un lado del triángulo
    -   Posición z de los vértices del triángulo
    -   Desplazamiento +/- x del plano de selección en el espacio homogéneo \[ -1,1\]
    -   Número de comandos indirectos en el búfer de comandos

``` syntax
// Create the root signatures.
{
       CD3DX12_ROOT_PARAMETER rootParameters[GraphicsRootParametersCount];
       rootParameters[Cbv].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_VERTEX);

       CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
       rootSignatureDesc.Init(_countof(rootParameters), rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

       ComPtr<ID3DBlob> signature;
       ComPtr<ID3DBlob> error;
       ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
       ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

       // Create compute signature.
       CD3DX12_DESCRIPTOR_RANGE ranges[2];
       ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 2, 0);
       ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

       CD3DX12_ROOT_PARAMETER computeRootParameters[ComputeRootParametersCount];
       computeRootParameters[SrvUavTable].InitAsDescriptorTable(2, ranges);
       computeRootParameters[RootConstants].InitAsConstants(4, 0);

       CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc;
       computeRootSignatureDesc.Init(_countof(computeRootParameters), computeRootParameters);

       ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
       ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
}
```



| Flujo de llamadas                                                             | Parámetros                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**PARÁMETRO RAÍZ CD3DX12 \_ \_**](cd3dx12-root-parameter.md)            | [**VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [**CD3DX12 \_ ROOT \_ SIGNATURE \_ DESC**](cd3dx12-root-signature-desc.md) | [**MARCAS DE FIRMA RAÍZ D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))                                   |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**VERSIÓN DE FIRMA RAÍZ D3D \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [**INTERVALO DEL DESCRIPTOR CD3DX12 \_ \_**](cd3dx12-descriptor-range.md)        | [**TIPO DE INTERVALO \_ DE DESCRIPTOR D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [**PARÁMETRO RAÍZ CD3DX12 \_ \_**](cd3dx12-root-parameter.md)            | [**VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [**CD3DX12 \_ ROOT \_ SIGNATURE \_ DESC**](cd3dx12-root-signature-desc.md) | [**MARCAS DE FIRMA RAÍZ D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))                                   |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**VERSIÓN DE FIRMA RAÍZ D3D \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-a-shader-resource-view-srv-for-the-compute-shader"></a>Creación de una vista de recursos de sombreador (SRV) para el sombreador de proceso

Después de crear los objetos de estado de canalización, los búferes de vértices, una galería de símbolos de profundidad y los búferes constantes, el ejemplo crea una vista de recursos de sombreador (SRV) del búfer constante para que el sombreador de proceso pueda acceder a los datos del búfer constante.

``` syntax
// Create shader resource views (SRV) of the constant buffers for the
// compute shader to read from.
       D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
       srvDesc.Format = DXGI_FORMAT_UNKNOWN;
       srvDesc.ViewDimension = D3D12_SRV_DIMENSION_BUFFER;
       srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
       srvDesc.Buffer.NumElements = TriangleCount;
       srvDesc.Buffer.StructureByteStride = sizeof(ConstantBufferData);
       srvDesc.Buffer.Flags = D3D12_BUFFER_SRV_FLAG_NONE;

       CD3DX12_CPU_DESCRIPTOR_HANDLE cbvSrvHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), CbvSrvOffset, m_cbvSrvUavDescriptorSize);
       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              srvDesc.Buffer.FirstElement = frame * TriangleCount;
              m_device->CreateShaderResourceView(m_constantBuffer.Get(), &srvDesc, cbvSrvHandle);
              cbvSrvHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
       }
```



<table>
<thead>
<tr class="header">
<th>Flujo de llamadas</th>
<th>Parámetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a><br />
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></td>

</tr>
</tbody>
</table>



 

## <a name="create-the-indirect-command-buffers"></a>Creación de búferes de comandos indirectos

A continuación, creamos los búferes de comandos indirectos y definimos su contenido mediante el código siguiente. Dibujamos los mismos vértices de triángulo 1024 veces, pero apuntamos a una ubicación de búfer constante diferente con cada llamada a draw.

``` syntax
       D3D12_GPU_VIRTUAL_ADDRESS gpuAddress = m_constantBuffer->GetGPUVirtualAddress();
       UINT commandIndex = 0;

       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              for (UINT n = 0; n < TriangleCount; n++)
              {
                    commands[commandIndex].cbv = gpuAddress;
                    commands[commandIndex].drawArguments.VertexCountPerInstance = 3;
                    commands[commandIndex].drawArguments.InstanceCount = 1;
                    commands[commandIndex].drawArguments.StartVertexLocation = 0;
                    commands[commandIndex].drawArguments.StartInstanceLocation = 0;

                    commandIndex++;
                    gpuAddress += sizeof(ConstantBufferData);
              }
       }
```



| Flujo de llamadas                    | Parámetros                                                          |
|------------------------------|---------------------------------------------------------------------|
| DIRECCIÓN VIRTUAL de GPU D3D12 \_ \_ \_ | [**GetGPUVirtualAddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress) |



 

Después de cargar los búferes de comandos en la GPU, también creamos un SRV de ellos para que el sombreador de proceso lea. Esto es muy similar al SRV creado del búfer constante.

``` syntax
// Create SRVs for the command buffers.
       D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
       srvDesc.Format = DXGI_FORMAT_UNKNOWN;
       srvDesc.ViewDimension = D3D12_SRV_DIMENSION_BUFFER;
       srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
       srvDesc.Buffer.NumElements = TriangleCount;
       srvDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
       srvDesc.Buffer.Flags = D3D12_BUFFER_SRV_FLAG_NONE;

       CD3DX12_CPU_DESCRIPTOR_HANDLE commandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), CommandsOffset, m_cbvSrvUavDescriptorSize);
       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              srvDesc.Buffer.FirstElement = frame * TriangleCount;
              m_device->CreateShaderResourceView(m_commandBuffer.Get(), &srvDesc, commandsHandle);
              commandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
       }
```



<table>
<thead>
<tr class="header">
<th>Flujo de llamadas</th>
<th>Parámetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a><br />
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags"><strong>D3D12_BUFFER_SRV_FLAG</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></td>

</tr>
</tbody>
</table>



 

## <a name="create-the-compute-uavs"></a>Creación de los UAV de proceso

Es necesario crear los UAV que almacenarán los resultados del trabajo de proceso. Cuando el sombreador de proceso considera que un triángulo es visible para el destino de representación, se anexará a este UAV y, a continuación, lo consumirá la API [**ExecuteIndirect.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

``` syntax
CD3DX12_CPU_DESCRIPTOR_HANDLE processedCommandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), ProcessedCommandsOffset, m_cbvSrvUavDescriptorSize);
for (UINT frame = 0; frame < FrameCount; frame++)
{
       // Allocate a buffer large enough to hold all of the indirect commands
       // for a single frame as well as a UAV counter.
       commandBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(CommandBufferSizePerFrame + sizeof(UINT), D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS);
       CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
       ThrowIfFailed(m_device->CreateCommittedResource(
             &heapProps,
             D3D12_HEAP_FLAG_NONE,
             &commandBufferDesc,
             D3D12_RESOURCE_STATE_COPY_DEST,
             nullptr,
             IID_PPV_ARGS(&m_processedCommandBuffers[frame])));

       D3D12_UNORDERED_ACCESS_VIEW_DESC uavDesc = {};
       uavDesc.Format = DXGI_FORMAT_UNKNOWN;
       uavDesc.ViewDimension = D3D12_UAV_DIMENSION_BUFFER;
       uavDesc.Buffer.FirstElement = 0;
       uavDesc.Buffer.NumElements = TriangleCount;
       uavDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
       uavDesc.Buffer.CounterOffsetInBytes = CommandBufferSizePerFrame;
       uavDesc.Buffer.Flags = D3D12_BUFFER_UAV_FLAG_NONE;

       m_device->CreateUnorderedAccessView(
             m_processedCommandBuffers[frame].Get(),
             m_processedCommandBuffers[frame].Get(),
             &uavDesc,
             processedCommandsHandle);

       processedCommandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
}
```



<table>
<thead>
<tr class="header">
<th>Flujo de llamadas</th>
<th>Parámetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="cd3dx12-resource-desc.md"><strong>CD3DX12_RESOURCE_DESC</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc"><strong>D3D12_UNORDERED_ACCESS_VIEW_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_uav_dimension"><strong>D3D12_UAV_DIMENSION</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags"><strong>D3D12_BUFFER_UAV_FLAGS</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview"><strong>CreateUnorderedAccessView</strong></a></td>

</tr>
</tbody>
</table>



 

## <a name="drawing-the-frame"></a>Dibujar el marco

Cuando llegue el momento de dibujar el marco, si estamos en el modo cuando se invoca el sombreador [](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch) de proceso y la GPU procesa comandos indirectos, primero enviaremos ese trabajo para rellenar el búfer de comandos para [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect). Los fragmentos de código siguientes se agregan al **método PopulateCommandLists.**

``` syntax
// Record the compute commands that will cull triangles and prevent them from being processed by the vertex shader.
if (m_enableCulling)
{
       UINT frameDescriptorOffset = m_frameIndex * CbvSrvUavDescriptorCountPerFrame;
       D3D12_GPU_DESCRIPTOR_HANDLE cbvSrvUavHandle = m_cbvSrvUavHeap->GetGPUDescriptorHandleForHeapStart();

       m_computeCommandList->SetComputeRootSignature(m_computeRootSignature.Get());

       ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvUavHeap.Get() };
       m_computeCommandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

       m_computeCommandList->SetComputeRootDescriptorTable(
              SrvUavTable,
              CD3DX12_GPU_DESCRIPTOR_HANDLE(cbvSrvUavHandle, CbvSrvOffset + frameDescriptorOffset, m_cbvSrvUavDescriptorSize));

       m_computeCommandList->SetComputeRoot32BitConstants(RootConstants, 4, reinterpret_cast<void*>(&m_csRootConstants), 0);

       // Reset the UAV counter for this frame.
       m_computeCommandList->CopyBufferRegion(m_processedCommandBuffers[m_frameIndex].Get(), CommandBufferSizePerFrame, m_processedCommandBufferCounterReset.Get(), 0, sizeof(UINT));

       D3D12_RESOURCE_BARRIER barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_processedCommandBuffers[m_frameIndex].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_UNORDERED_ACCESS);
       m_computeCommandList->ResourceBarrier(1, &barrier);

       m_computeCommandList->Dispatch(static_cast<UINT>(ceil(TriangleCount / float(ComputeThreadBlockSize))), 1, 1);
}

ThrowIfFailed(m_computeCommandList->Close());
```



<table>
<thead>
<tr class="header">
<th>Flujo de llamadas</th>
<th>Parámetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle"><strong>D3D12_GPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature"><strong>SetComputeRootSignature</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable"><strong>SetComputeRootDescriptorTable</strong></a></td>
<td><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants"><strong>SetComputeRoot32BitConstants</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion"><strong>CopyBufferRegion</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></td>
<td><dl><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch"><strong>Dispatch</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Cerca</strong></a></td>

</tr>
</tbody>
</table>



 

A continuación, ejecutaremos los comandos en el UAV (selección de GPU habilitada) o en el búfer de comandos completo (selección de GPU deshabilitada).

``` syntax
// Record the rendering commands.
{
       // Set necessary state.
       m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

       ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvUavHeap.Get() };
       m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

       m_commandList->RSSetViewports(1, &m_viewport);
       m_commandList->RSSetScissorRects(1, m_enableCulling ? &m_cullingScissorRect : &m_scissorRect);

       // Indicate that the command buffer will be used for indirect drawing
       // and that the back buffer will be used as a render target.
       D3D12_RESOURCE_BARRIER barriers[2] = {
              CD3DX12_RESOURCE_BARRIER::Transition(
                    m_enableCulling ? m_processedCommandBuffers[m_frameIndex].Get() : m_commandBuffer.Get(),
                    m_enableCulling ? D3D12_RESOURCE_STATE_UNORDERED_ACCESS : D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE,
                    D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT),
              CD3DX12_RESOURCE_BARRIER::Transition(
                    m_renderTargets[m_frameIndex].Get(),
                    D3D12_RESOURCE_STATE_PRESENT,
                    D3D12_RESOURCE_STATE_RENDER_TARGET)
       };

       m_commandList->ResourceBarrier(_countof(barriers), barriers);

       CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
       CD3DX12_CPU_DESCRIPTOR_HANDLE dsvHandle(m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
       m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, &dsvHandle);

       // Record commands.
       const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
       m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
       m_commandList->ClearDepthStencilView(dsvHandle, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

       m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
       m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);

       if (m_enableCulling)
       {
              // Draw the triangles that have not been culled.
              m_commandList->ExecuteIndirect(
                    m_commandSignature.Get(),
                    TriangleCount,
                    m_processedCommandBuffers[m_frameIndex].Get(),
                    0,
                    m_processedCommandBuffers[m_frameIndex].Get(),
                    CommandBufferSizePerFrame);
       }
       else
       {
              // Draw all of the triangles.
              m_commandList->ExecuteIndirect(
                    m_commandSignature.Get(),
                    TriangleCount,
                    m_commandBuffer.Get(),
                    CommandBufferSizePerFrame * m_frameIndex,
                    nullptr,
                    0);
       }

       // Indicate that the command buffer may be used by the compute shader
       // and that the back buffer will now be used to present.
       barriers[0].Transition.StateBefore = D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT;
       barriers[0].Transition.StateAfter = m_enableCulling ? D3D12_RESOURCE_STATE_COPY_DEST : D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE;
       barriers[1].Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
       barriers[1].Transition.StateAfter = D3D12_RESOURCE_STATE_PRESENT;

       m_commandList->ResourceBarrier(_countof(barriers), barriers);

       ThrowIfFailed(m_commandList->Close());
}
```



<table>
<thead>
<tr class="header">
<th>Flujo de llamadas</th>
<th>Parámetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature"><strong>SetGraphicsRootSignature</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports"><strong>RSSetViewports</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects"><strong>RSSetScissorRects</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></td>
<td><dl><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>

</tr>
<tr class="even">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets"><strong>OMSetRenderTargets</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview"><strong>ClearRenderTargetView</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview"><strong>ClearDepthStencilView</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_clear_flags"><strong>D3D12_CLEAR_FLAGS</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></td>
<td><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect"><strong>ExecuteIndirect</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Cerca</strong></a></td>

</tr>
</tbody>
</table>



 

Si estamos en modo de selección de GPU, la cola de comandos de gráficos esperará a que se complete el trabajo de proceso antes de empezar a ejecutar los comandos indirectos. En el **método OnRender** se agrega el siguiente fragmento de código.

``` syntax
// Execute the compute work.
if (m_enableCulling)
{
       ID3D12CommandList* ppCommandLists[] = { m_computeCommandList.Get() };
       m_computeCommandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);
       m_computeCommandQueue->Signal(m_computeFence.Get(), m_fenceValues[m_frameIndex]);

       // Execute the rendering work only when the compute work is complete.
       m_commandQueue->Wait(m_computeFence.Get(), m_fenceValues[m_frameIndex]);
}

// Execute the rendering work.
ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);
```



| Flujo de llamadas                                                             | Parámetros |
|-----------------------------------------------------------------------|------------|
| [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                        |            |
| [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) |            |
| [**Señal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                           |            |
| [**Esperar**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                               |            |
| [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                        |            |
| [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) |            |



 

## <a name="run-the-sample"></a>Ejecución del ejemplo

Ejemplo con la selección primitiva de GPU.

![captura de pantalla de la muestra indirecta exectue con la selección de GPU](images/executeindirect-withculling.png)

Ejemplo sin la selección primitiva de GPU.

![captura de pantalla de la muestra indirecta exectue sin selección de GPU](images/executeindirect-withoutculling.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tutoriales de código D3D12](d3d12-code-walk-throughs.md)
</dt> <dt>

[Tutoriales de vídeo de aprendizaje avanzado de DirectX: Ejecución de la selección de GPU indirecta y asincrónica](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[Dibujo indirecto](indirect-drawing.md)
</dt> </dl>

 

 
