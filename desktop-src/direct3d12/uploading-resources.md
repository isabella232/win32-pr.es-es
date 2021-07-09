---
title: Carga de diferentes tipos de recursos
description: Muestra cómo usar un búfer para cargar datos de búfer constante y datos de búfer de vértices en la GPU, y cómo subasigna y coloca correctamente los datos en búferes.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03d4755124bbadcdd255a6e99739b710845ab14
ms.sourcegitcommit: a30d0436a84986234df673c6def6694d5a8579f6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113563785"
---
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="42acb-103">Carga de diferentes tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="42acb-103">Uploading different types of resources</span></span>

<span data-ttu-id="42acb-104">Muestra cómo usar un búfer para cargar datos de búfer constante y datos de búfer de vértices en la GPU, y cómo subasigna y coloca correctamente los datos en búferes.</span><span class="sxs-lookup"><span data-stu-id="42acb-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="42acb-105">El uso de un solo búfer aumenta la flexibilidad de uso de memoria y proporciona a las aplicaciones un control más estricto sobre el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="42acb-105">The use of a single buffer increases memory usage flexibility, and provides applications with tighter control over memory usage.</span></span> <span data-ttu-id="42acb-106">También se muestran las diferencias entre los modelos Direct3D 11 y Direct3D 12 para cargar diferentes tipos de recursos.</span><span class="sxs-lookup"><span data-stu-id="42acb-106">Also shows the differences between the Direct3D 11 and Direct3D 12 models for uploading different types of resources.</span></span>

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="42acb-107">Upload diferentes tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="42acb-107">Upload different types of resources</span></span>

<span data-ttu-id="42acb-108">En Direct3D 12, se crea un búfer para dar cabida a distintos tipos de datos de recursos para la carga y se copian los datos de recursos en el mismo búfer de forma similar para los distintos datos de recursos.</span><span class="sxs-lookup"><span data-stu-id="42acb-108">In Direct3D 12, you create one buffer to accommodate different types of resource data for uploading, and you copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="42acb-109">A continuación, se crean vistas individuales para enlazar esos datos de recursos a la canalización de gráficos en el modelo de enlace de recursos de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="42acb-109">Individual views are then created to bind those resource data to the graphics pipeline in the Direct3D 12 resource binding model.</span></span>

<span data-ttu-id="42acb-110">En Direct3D 11, se crean búferes independientes para distintos tipos de datos de recursos (tenga en cuenta los distintos usados en el código de ejemplo de Direct3D 11 a continuación), se enlaza explícitamente cada búfer de recursos a la canalización de gráficos y se actualizan los datos de recursos con distintos métodos en función de los distintos tipos de `BindFlags` recursos.</span><span class="sxs-lookup"><span data-stu-id="42acb-110">In Direct3D 11, you create separate buffers for different types of resource data (note the different `BindFlags` used in the Direct3D 11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="42acb-111">En Direct3D 12 y Direct3D 11, debe usar recursos de carga solo donde la CPU escribirá los datos una vez y la GPU los leerá una vez.</span><span class="sxs-lookup"><span data-stu-id="42acb-111">In both Direct3D 12 and Direct3D 11, you should use upload resources only where the CPU will write the data once, and the GPU will read it once.</span></span>

<span data-ttu-id="42acb-112">En algunos casos,</span><span class="sxs-lookup"><span data-stu-id="42acb-112">In some cases,</span></span>
* <span data-ttu-id="42acb-113">la GPU leerá los datos varias veces o</span><span class="sxs-lookup"><span data-stu-id="42acb-113">the GPU will read the data multiple times, or</span></span>
* <span data-ttu-id="42acb-114">la GPU no leerá los datos linealmente o</span><span class="sxs-lookup"><span data-stu-id="42acb-114">the GPU won't read the data linearly, or</span></span>
* <span data-ttu-id="42acb-115">la representación ya está significativamente limitada por GPU.</span><span class="sxs-lookup"><span data-stu-id="42acb-115">the rendering is significantly GPU-limited already.</span></span>

<span data-ttu-id="42acb-116">En esos casos, la mejor opción podría ser usar [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) o [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) para copiar los datos del búfer de carga en un recurso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="42acb-116">In those cases, the better option might be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span>

<span data-ttu-id="42acb-117">Un recurso predeterminado puede residir en memoria de vídeo física en GPU discretas.</span><span class="sxs-lookup"><span data-stu-id="42acb-117">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-direct3d-11"></a><span data-ttu-id="42acb-118">Ejemplo de código: Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="42acb-118">Code Example: Direct3D 11</span></span>

```cpp
// Direct3D 11: Separate buffers for each resource type.

void main()
{
    // ...

    // Create a constant buffer.
    float constantBufferData[] = ...;

    D3D11_BUFFER_DESC constantBufferDesc = {0};  
    constantBufferDesc.ByteWidth = sizeof(constantBufferData);  
    constantBufferDesc.Usage = D3D11_USAGE_DYNAMIC;  
    constantBufferDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;  
    constantBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;  

    ComPtr<ID3D11Buffer> constantBuffer;
    d3dDevice->CreateBuffer(  
        &constantBufferDesc,  
        NULL,
        &constantBuffer  
        );

    // Create a vertex buffer.
    float vertexBufferData[] = ...;

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(vertexBufferData);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;

    ComPtr<ID3D11Buffer> vertexBuffer;
    d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        NULL,
        &vertexBuffer
        );

    // ...
}

void DrawFrame()
{
    // ...

    // Bind buffers to the graphics pipeline.
    d3dDeviceContext->VSSetConstantBuffers(0, 1, constantBuffer.Get());
    d3dDeviceContext->IASetVertexBuffers(0, 1, vertexBuffer.Get(), ...);

    // Update the constant buffer.
    D3D11_MAPPED_SUBRESOURCE mappedResource;  
    d3dDeviceContext->Map(
        constantBuffer.Get(),
        0, 
        D3D11_MAP_WRITE_DISCARD,
        0,
        &mappedResource
        );
    memcpy(mappedResource.pData, constantBufferData,
        sizeof(contatnBufferData));
    d3dDeviceContext->Unmap(constantBuffer.Get(), 0);  

    // Update the vertex buffer.
    d3dDeviceContext->UpdateSubresource(
        vertexBuffer.Get(),
        0,
        NULL,
        vertexBufferData,
        sizeof(vertexBufferData),
        0
    );

    // ...
}
```

### <a name="code-example-direct3d-12"></a><span data-ttu-id="42acb-119">Ejemplo de código: Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="42acb-119">Code Example: Direct3D 12</span></span>

```cpp
// Direct3D 12: One buffer to accommodate different types of resources

ComPtr<ID3D12Resource> m_spUploadBuffer;
UINT8* m_pDataBegin = nullptr;    // starting position of upload buffer
UINT8* m_pDataCur = nullptr;      // current position of upload buffer
UINT8* m_pDataEnd = nullptr;      // ending position of upload buffer

void main()
{
    //
    // Initialize an upload buffer
    //

    InitializeUploadBuffer(64 * 1024);

    // ...
}

void DrawFrame()
{
    // ...

    // Set vertices data to the upload buffer.

    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float),
            sizeof(float), 
            verticesOffset
            ));

    // Set constant data to the upload buffer.

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT, 
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model.

    D3D12_VERTEX_BUFFER_VIEW vertexBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + verticesOffset,
        sizeof(vertices), // size
        sizeof(float) * 4,  // stride
    };

    commandList->IASetVertexBuffers( 
        0,
        1,
        &vertexBufferViewDesc,
        ));

    // Create constant buffer views for the new binding model.

    D3D12_CONSTANT_BUFFER_VIEW_DESC constantBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + constantsOffset,
        sizeof(constants) // size
         };

    d3dDevice->CreateConstantBufferView(
        &constantBufferViewDesc,
        ...
        ));

    // Continue command list building and execution ...
}

//
// Create an upload buffer and keep it always mapped.
//

HRESULT InitializeUploadBuffer(SIZE_T uSize)
{
    HRESULT hr = d3dDevice->CreateCommittedResource(
         &CD3DX12_HEAP_PROPERTIES( D3D12_HEAP_TYPE_UPLOAD ),    
               D3D12_HEAP_FLAG_NONE, 
               &CD3DX12_RESOURCE_DESC::Buffer( uSize ), 
               D3D12_RESOURCE_STATE_GENERIC_READ, nullptr,  
               IID_PPV_ARGS( &m_spUploadBuffer ) );

    if (SUCCEEDED(hr))
    {
        void* pData;
        //
        // No CPU reads will be done from the resource.
        //
        CD3DX12_RANGE readRange(0, 0);
        m_spUploadBuffer->Map( 0, &readRange, &pData ); 
        m_pDataCur = m_pDataBegin = reinterpret_cast< UINT8* >( pData );
        m_pDataEnd = m_pDataBegin + uSize;
    }
    return hr;
}

//
// Sub-allocate from the buffer, with offset aligned.
//

HRESULT SuballocateFromBuffer(SIZE_T uSize, UINT uAlign)
{
    m_pDataCur = reinterpret_cast< UINT8* >(
        Align(reinterpret_cast< SIZE_T >(m_pDataCur), uAlign)
        );

    return (m_pDataCur + uSize > m_pDataEnd) ? E_INVALIDARG : S_OK;
}

//
// Place and copy data to the upload buffer.
//

HRESULT SetDataToUploadBuffer(
    const void* pData, 
    UINT bytesPerData, 
    UINT dataCount, 
    UINT alignment, 
    UINT& byteOffset
    )
{
    SIZE_T byteSize = bytesPerData * dataCount;
    HRESULT hr = SuballocateFromBuffer(byteSize, alignment);
    if (SUCCEEDED(hr))
    {
        byteOffset = UINT(m_pDataCur - m_pDataBegin);
        memcpy(m_pDataCur, pData, byteSize); 
        m_pDataCur += byteSize;
    }
    return hr;
}

//
// Align uLocation to the next multiple of uAlign.
//

UINT Align(UINT uLocation, UINT uAlign)
{
    if ( (0 == uAlign) || (uAlign & (uAlign-1)) )
    {
        ThrowException("non-pow2 alignment");
    }

    return ( (uLocation + (uAlign-1)) & ~(uAlign-1) );
}
```

<span data-ttu-id="42acb-120">Tenga en cuenta el uso de las estructuras [**auxiliares CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) y [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span><span class="sxs-lookup"><span data-stu-id="42acb-120">Note the use of the helper structures [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="42acb-121">Constantes</span><span class="sxs-lookup"><span data-stu-id="42acb-121">Constants</span></span>

<span data-ttu-id="42acb-122">Para establecer constantes, vértices e índices dentro de un montón de carga o reversión, use las siguientes API.</span><span class="sxs-lookup"><span data-stu-id="42acb-122">To set constants, vertices, and indexes within an upload or readback heap, use the following APIs.</span></span>

-   [<span data-ttu-id="42acb-123">**ID3D12Device::CreateConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="42acb-123">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="42acb-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="42acb-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="42acb-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="42acb-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="42acb-126">Recursos</span><span class="sxs-lookup"><span data-stu-id="42acb-126">Resources</span></span>

<span data-ttu-id="42acb-127">Los recursos son el concepto de Direct3D que abstrae el uso de memoria física de GPU.</span><span class="sxs-lookup"><span data-stu-id="42acb-127">Resources are the Direct3D concept that abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="42acb-128">Los recursos requieren espacio de direcciones virtuales de GPU para acceder a la memoria física.</span><span class="sxs-lookup"><span data-stu-id="42acb-128">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="42acb-129">La creación de recursos es de subproceso libre.</span><span class="sxs-lookup"><span data-stu-id="42acb-129">Resource creation is free-threaded.</span></span>

<span data-ttu-id="42acb-130">Hay tres tipos de recursos con respecto a la creación de direcciones virtuales y la flexibilidad en Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="42acb-130">There are three types of resources with respect to virtual address creation and flexibility in Direct3D 12.</span></span>

### <a name="committed-resources"></a><span data-ttu-id="42acb-131">Recursos confirmados</span><span class="sxs-lookup"><span data-stu-id="42acb-131">Committed resources</span></span>

<span data-ttu-id="42acb-132">Los recursos confirmados son la idea más común de los recursos de Direct3D a lo largo de las generaciones.</span><span class="sxs-lookup"><span data-stu-id="42acb-132">Committed resources are the most common idea of Direct3D resources over the generations.</span></span> <span data-ttu-id="42acb-133">La creación de un recurso de este tipo asigna un intervalo de direcciones virtuales, un montón implícito lo suficientemente grande como para ajustarse a todo el recurso, y confirma el intervalo de direcciones virtuales en la memoria física encapsulada por el montón.</span><span class="sxs-lookup"><span data-stu-id="42acb-133">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="42acb-134">Las propiedades implícitas del montón deben pasarse para que coincidan con la paridad funcional con versiones anteriores de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="42acb-134">The implicit heap properties must be passed to match functional parity with previous Direct3D versions.</span></span> <span data-ttu-id="42acb-135">Consulte [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="42acb-135">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

### <a name="reserved-resources"></a><span data-ttu-id="42acb-136">Recursos reservados</span><span class="sxs-lookup"><span data-stu-id="42acb-136">Reserved resources</span></span>

<span data-ttu-id="42acb-137">Los recursos reservados son equivalentes a los recursos en mosaico de Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="42acb-137">Reserved resources are equivalent to Direct3D 11 tiled resources.</span></span> <span data-ttu-id="42acb-138">En su creación, solo se asigna un intervalo de direcciones virtuales y no se asigna a ningún montón.</span><span class="sxs-lookup"><span data-stu-id="42acb-138">On their creation, only a virtual address range is allocated, and not mapped to any heap.</span></span> <span data-ttu-id="42acb-139">La aplicación asignará estos recursos a montones más adelante.</span><span class="sxs-lookup"><span data-stu-id="42acb-139">The application will map such resources to heaps later.</span></span> <span data-ttu-id="42acb-140">Actualmente, las funcionalidades de estos recursos no se modifican desde Direct3D 11, ya que se pueden asignar a un montón con una granularidad de mosaico de 64 KB [**con UpdateTileMappings.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)</span><span class="sxs-lookup"><span data-stu-id="42acb-140">The capabilities of such resources are currently unchanged from Direct3D 11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="42acb-141">Consulte [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span><span class="sxs-lookup"><span data-stu-id="42acb-141">Refer to [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span></span>

### <a name="placed-resources"></a><span data-ttu-id="42acb-142">Recursos colocados</span><span class="sxs-lookup"><span data-stu-id="42acb-142">Placed resources</span></span>

<span data-ttu-id="42acb-143">Como novedad de Direct3D 12, puede crear montones independientes de los recursos.</span><span class="sxs-lookup"><span data-stu-id="42acb-143">New for Direct3D 12, you can create heaps separate from resources.</span></span> <span data-ttu-id="42acb-144">Después, puede buscar varios recursos dentro de un único montón.</span><span class="sxs-lookup"><span data-stu-id="42acb-144">Afterward, you can locate multiple resources within a single heap.</span></span> <span data-ttu-id="42acb-145">Puede hacerlo sin crear recursos en mosaico o reservados, lo que permite las funcionalidades de todos los tipos de recursos que la aplicación puede crear directamente.</span><span class="sxs-lookup"><span data-stu-id="42acb-145">You can do that without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by your application.</span></span> <span data-ttu-id="42acb-146">Es posible que se superpongan varios recursos y debe usar [**id3D12GraphicsCommandList::ResourceBarcommand**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) para volver a usar la memoria física correctamente.</span><span class="sxs-lookup"><span data-stu-id="42acb-146">Multiple resources might overlap, and you must use the [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to re-use physical memory correctly.</span></span> <span data-ttu-id="42acb-147">Consulte [**ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span><span class="sxs-lookup"><span data-stu-id="42acb-147">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="42acb-148">Reflexión del tamaño de los recursos</span><span class="sxs-lookup"><span data-stu-id="42acb-148">Resource size reflection</span></span>

<span data-ttu-id="42acb-149">Debe usar la reflexión de tamaño de recurso para comprender cuántas texturas de espacio con diseños de textura desconocidos requieren en montones.</span><span class="sxs-lookup"><span data-stu-id="42acb-149">You must use resource size reflection to understand how much space textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="42acb-150">También se admiten búferes, pero principalmente por comodidad.</span><span class="sxs-lookup"><span data-stu-id="42acb-150">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="42acb-151">Debe tener en cuenta las principales discrepancias de alineación para ayudar a empaquetar los recursos de forma más densa.</span><span class="sxs-lookup"><span data-stu-id="42acb-151">You should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="42acb-152">Por ejemplo, una matriz de un solo elemento  con un búfer de  un byte devuelve un tamaño de 64 KB y una alineación de 64 KB, ya que los búferes solo pueden estar alineados con 64 KB.</span><span class="sxs-lookup"><span data-stu-id="42acb-152">For example, a single-element array with a one-byte-buffer returns a *Size* of 64KB, and an *Alignment* of 64KB, because buffers can be only 64KB-aligned.</span></span>

<span data-ttu-id="42acb-153">Además, una matriz de tres elementos con dos texturas alineadas de 64 KB de un solo texel y una textura alineada de 4 MB de un solo texel notifica tamaños diferentes en función del orden de la matriz.</span><span class="sxs-lookup"><span data-stu-id="42acb-153">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="42acb-154">Si las texturas alineadas de 4 MB están en el centro, el *tamaño resultante* es de 12 MB.</span><span class="sxs-lookup"><span data-stu-id="42acb-154">If the 4MB aligned textures is in the middle, then the resulting *Size* is 12MB.</span></span> <span data-ttu-id="42acb-155">De lo contrario, el tamaño resultante es de 8 MB.</span><span class="sxs-lookup"><span data-stu-id="42acb-155">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="42acb-156">La alineación devuelta siempre sería de 4 MB, el superconjunto de todas las alineaciones de la matriz de recursos.</span><span class="sxs-lookup"><span data-stu-id="42acb-156">The Alignment returned would always be 4MB, the superset of all alignments in the resource array.</span></span>

<span data-ttu-id="42acb-157">Haga referencia a las SIGUIENTES API.</span><span class="sxs-lookup"><span data-stu-id="42acb-157">Reference the following APIs.</span></span>

- [<span data-ttu-id="42acb-158">**INFORMACIÓN DE ASIGNACIÓN DE RECURSOS D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42acb-158">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
- [<span data-ttu-id="42acb-159">**GetResourceAllocationInfo**</span><span class="sxs-lookup"><span data-stu-id="42acb-159">**GetResourceAllocationInfo**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="42acb-160">Alineación del búfer</span><span class="sxs-lookup"><span data-stu-id="42acb-160">Buffer alignment</span></span>

<span data-ttu-id="42acb-161">Las restricciones de alineación del búfer no han cambiado de Direct3D 11, en particular:</span><span class="sxs-lookup"><span data-stu-id="42acb-161">Buffer alignment restrictions have not changed from Direct3D 11, notably:</span></span>

- <span data-ttu-id="42acb-162">4 MB para texturas de varias muestras.</span><span class="sxs-lookup"><span data-stu-id="42acb-162">4 MB for multi-sample textures.</span></span>
- <span data-ttu-id="42acb-163">64 KB para texturas y búferes de ejemplo único.</span><span class="sxs-lookup"><span data-stu-id="42acb-163">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42acb-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42acb-164">Related topics</span></span>

* [<span data-ttu-id="42acb-165">Suballocation dentro de los búferes</span><span class="sxs-lookup"><span data-stu-id="42acb-165">Suballocation within buffers</span></span>](large-buffers.md)
