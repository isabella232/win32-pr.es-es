---
title: Cargar diferentes tipos de recursos
description: Muestra cómo utilizar un búfer para cargar datos de búfer de constantes y datos de búfer de vértices en la GPU, y cómo subasignar y colocar datos correctamente en los búferes.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2edca2cd9f4d3becf5036056a89f91c50f2c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103430"
---
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="75405-103">Cargar diferentes tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="75405-103">Uploading Different Types of Resources</span></span>

<span data-ttu-id="75405-104">Muestra cómo utilizar un búfer para cargar datos de búfer de constantes y datos de búfer de vértices en la GPU, y cómo subasignar y colocar datos correctamente en los búferes.</span><span class="sxs-lookup"><span data-stu-id="75405-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="75405-105">El uso de un único búfer aumenta la flexibilidad del uso de memoria y proporciona a las aplicaciones un control más estricto del uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="75405-105">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="75405-106">También se muestran las diferencias entre los modelos D3D11 y D3D12 para cargar diferentes tipos de recursos.</span><span class="sxs-lookup"><span data-stu-id="75405-106">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span>

-   [<span data-ttu-id="75405-107">Cargar diferentes tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="75405-107">Upload Different Types of Resources</span></span>](#upload-different-types-of-resources)
    -   [<span data-ttu-id="75405-108">Ejemplo de código: D3D11</span><span class="sxs-lookup"><span data-stu-id="75405-108">Code Example: D3D11</span></span>](#code-example-d3d11)
    -   [<span data-ttu-id="75405-109">Ejemplo de código: D3D12</span><span class="sxs-lookup"><span data-stu-id="75405-109">Code Example: D3D12</span></span>](#code-example-d3d12)
-   [<span data-ttu-id="75405-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="75405-110">Constants</span></span>](#constants)
-   [<span data-ttu-id="75405-111">Recursos</span><span class="sxs-lookup"><span data-stu-id="75405-111">Resources</span></span>](#uploading-different-types-of-resources)
-   [<span data-ttu-id="75405-112">Reflexión del tamaño de los recursos</span><span class="sxs-lookup"><span data-stu-id="75405-112">Resource size reflection</span></span>](#resource-size-reflection)
-   [<span data-ttu-id="75405-113">Alineación del búfer</span><span class="sxs-lookup"><span data-stu-id="75405-113">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="75405-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75405-114">Related topics</span></span>](#related-topics)

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="75405-115">Cargar diferentes tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="75405-115">Upload Different Types of Resources</span></span>

<span data-ttu-id="75405-116">En D3D12, las aplicaciones crean un búfer para acomodar distintos tipos de datos de recursos para cargar y copian los datos de recursos en el mismo búfer de forma similar para los distintos datos de recursos.</span><span class="sxs-lookup"><span data-stu-id="75405-116">In D3D12, applications create one buffer to accommodate different types of resource data for uploading, and copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="75405-117">A continuación, se crean vistas individuales para enlazar esos datos de recursos a la canalización de gráficos en el nuevo modelo de enlace de recursos.</span><span class="sxs-lookup"><span data-stu-id="75405-117">Individual views are then created to bind those resource data to the graphics pipeline in the new resource binding model.</span></span>

<span data-ttu-id="75405-118">En D3D11, las aplicaciones crean búferes independientes para diferentes tipos de datos de recursos (tenga en cuenta los distintos `BindFlags` usados en el código de ejemplo D3D11 que se muestra a continuación), enlazando explícitamente cada búfer de recursos a la canalización de gráficos y actualizando los datos de recursos con diferentes métodos basados en diferentes tipos de recursos.</span><span class="sxs-lookup"><span data-stu-id="75405-118">In D3D11, applications create separate buffers for different types of resource data (note the different `BindFlags` used in the D3D11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="75405-119">Tanto en D3D12 como en D3D11, las aplicaciones solo deben usar los recursos de carga en los que la CPU escribirá los datos una vez y la GPU los leerá una vez.</span><span class="sxs-lookup"><span data-stu-id="75405-119">In both D3D12 and D3D11, applications should only use upload resources where the CPU will write the data once and the GPU will read it once.</span></span> <span data-ttu-id="75405-120">Si la GPU va a leer los datos varias veces, la GPU no leerá los datos de forma lineal o la representación ya está limitada por GPU.</span><span class="sxs-lookup"><span data-stu-id="75405-120">If the GPU will read the data multiple times, the GPU will not read the data linearly, or the rendering is significantly GPU-limited already.</span></span> <span data-ttu-id="75405-121">La mejor opción puede ser usar [**ID3D12GraphicsCommandList:: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) o [**ID3D12GraphicsCommandList:: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) para copiar los datos del búfer de carga en un recurso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="75405-121">The better option may be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span> <span data-ttu-id="75405-122">Un recurso predeterminado puede residir en la memoria de vídeo física en GPU discretas.</span><span class="sxs-lookup"><span data-stu-id="75405-122">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-d3d11"></a><span data-ttu-id="75405-123">Ejemplo de código: D3D11</span><span class="sxs-lookup"><span data-stu-id="75405-123">Code Example: D3D11</span></span>

``` syntax
// D3D11: Separate buffers for each resource type.

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

### <a name="code-example-d3d12"></a><span data-ttu-id="75405-124">Ejemplo de código: D3D12</span><span class="sxs-lookup"><span data-stu-id="75405-124">Code Example: D3D12</span></span>

``` syntax
// D3D12: One buffer to accommodate different types of resources

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

<span data-ttu-id="75405-125">Tenga en cuenta el uso de las estructuras [**auxiliares \_ CD3DX12 \_ propiedades del montón**](cd3dx12-heap-properties.md) y la [**\_ \_ Descripción del recurso CD3DX12**](cd3dx12-resource-desc.md).</span><span class="sxs-lookup"><span data-stu-id="75405-125">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_RESOURCE\_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="75405-126">Constantes</span><span class="sxs-lookup"><span data-stu-id="75405-126">Constants</span></span>

<span data-ttu-id="75405-127">Para establecer constantes, vértices e índices dentro de un montón de carga o Readback, use las siguientes API:</span><span class="sxs-lookup"><span data-stu-id="75405-127">To set constants, vertices and indexes within an Upload or Readback heap, use the following APIs:</span></span>

-   [<span data-ttu-id="75405-128">**ID3D12Device::CreateConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="75405-128">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="75405-129">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="75405-129">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="75405-130">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="75405-130">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="75405-131">Recursos</span><span class="sxs-lookup"><span data-stu-id="75405-131">Resources</span></span>

<span data-ttu-id="75405-132">Los recursos son el concepto D3D, que abstrae el uso de la memoria física de GPU.</span><span class="sxs-lookup"><span data-stu-id="75405-132">Resources are the D3D concept which abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="75405-133">Los recursos requieren espacio de direcciones virtuales de GPU para tener acceso a la memoria física.</span><span class="sxs-lookup"><span data-stu-id="75405-133">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="75405-134">La creación de recursos es de subproceso libre.</span><span class="sxs-lookup"><span data-stu-id="75405-134">Resource creation is free-threaded.</span></span>

<span data-ttu-id="75405-135">Hay tres tipos de recursos con respecto a la creación de direcciones virtuales y la flexibilidad en D3D12:</span><span class="sxs-lookup"><span data-stu-id="75405-135">There are three types of resources with respect to virtual address creation and flexibility in D3D12:</span></span>

-   <span data-ttu-id="75405-136">Recursos confirmados</span><span class="sxs-lookup"><span data-stu-id="75405-136">Committed resources</span></span>

    <span data-ttu-id="75405-137">Los recursos confirmados son la idea más común de los recursos D3D en las generaciones.</span><span class="sxs-lookup"><span data-stu-id="75405-137">Committed resources are the most common idea of D3D resources over the generations.</span></span> <span data-ttu-id="75405-138">Al crear este tipo de recurso, se asigna un intervalo de direcciones virtuales, un montón implícito lo suficientemente grande como para ajustarse a todo el recurso y se confirma el intervalo de direcciones virtuales en la memoria física encapsulada por el montón.</span><span class="sxs-lookup"><span data-stu-id="75405-138">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="75405-139">Las propiedades implícitas del montón deben pasarse para coincidir con la paridad funcional con las versiones anteriores de D3D.</span><span class="sxs-lookup"><span data-stu-id="75405-139">The implicit heap properties must be passed to match functional parity with previous D3D versions.</span></span> <span data-ttu-id="75405-140">Consulte [**ID3D12Device:: CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="75405-140">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

-   <span data-ttu-id="75405-141">Recursos reservados</span><span class="sxs-lookup"><span data-stu-id="75405-141">Reserved resources</span></span>

    <span data-ttu-id="75405-142">Los recursos reservados son equivalentes a los recursos en mosaico de D3D11.</span><span class="sxs-lookup"><span data-stu-id="75405-142">Reserved resources are equivalent to D3D11 tiled resources.</span></span> <span data-ttu-id="75405-143">En su creación, solo se asigna un intervalo de direcciones virtuales y no se asigna a ningún montón.</span><span class="sxs-lookup"><span data-stu-id="75405-143">On their creation, only a virtual address range is allocated and not mapped to any heap.</span></span> <span data-ttu-id="75405-144">La aplicación asignará estos recursos a los montones más adelante.</span><span class="sxs-lookup"><span data-stu-id="75405-144">The application will map such resources to heaps later.</span></span> <span data-ttu-id="75405-145">Actualmente, las capacidades de estos recursos no se han modificado a través de D3D11, ya que se pueden asignar a un montón en una granularidad de mosaicos de 64 KB con [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span><span class="sxs-lookup"><span data-stu-id="75405-145">The capabilities of such resources are currently unchanged over D3D11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="75405-146">Consulte [ **ID3D12Device:: CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span><span class="sxs-lookup"><span data-stu-id="75405-146">Refer to [**ID3D12Device::CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span></span>

-   <span data-ttu-id="75405-147">Recursos colocados</span><span class="sxs-lookup"><span data-stu-id="75405-147">Placed resources</span></span>

    <span data-ttu-id="75405-148">En el caso de D3D12, las aplicaciones pueden crear montones independientes de los recursos.</span><span class="sxs-lookup"><span data-stu-id="75405-148">New for D3D12, applications may create heaps separate from resources.</span></span> <span data-ttu-id="75405-149">Posteriormente, la aplicación puede buscar varios recursos en un solo montón.</span><span class="sxs-lookup"><span data-stu-id="75405-149">Afterward, the application may locate multiple resources within a single heap.</span></span> <span data-ttu-id="75405-150">Esto puede hacerse sin crear recursos en mosaico o reservados, lo que permite que las aplicaciones puedan crear directamente las capacidades de todos los tipos de recursos.</span><span class="sxs-lookup"><span data-stu-id="75405-150">This can be done without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by applications.</span></span> <span data-ttu-id="75405-151">Se pueden superponer varios recursos y la aplicación debe usar `TiledResourceBarrier` para volver a usar la memoria física correctamente.</span><span class="sxs-lookup"><span data-stu-id="75405-151">Multiple resources may overlap, and the application must use the `TiledResourceBarrier` to re-use physical memory correctly.</span></span> <span data-ttu-id="75405-152">Consulte [ **ID3D12Device:: CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span><span class="sxs-lookup"><span data-stu-id="75405-152">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="75405-153">Reflexión del tamaño de los recursos</span><span class="sxs-lookup"><span data-stu-id="75405-153">Resource size reflection</span></span>

<span data-ttu-id="75405-154">Las aplicaciones deben usar la reflexión del tamaño de los recursos para comprender cuánta texturas de sala con diseños de texturas desconocidos requieren en montones.</span><span class="sxs-lookup"><span data-stu-id="75405-154">Applications must use resource size reflection to understand how much room textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="75405-155">También se admiten los búferes, pero principalmente para mayor comodidad.</span><span class="sxs-lookup"><span data-stu-id="75405-155">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="75405-156">Las aplicaciones deben tener en cuenta las principales discrepancias de alineación, para ayudar a empaquetar los recursos con mayor densidad.</span><span class="sxs-lookup"><span data-stu-id="75405-156">Applications should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="75405-157">Por ejemplo, una matriz de un solo elemento con un búfer de un byte devuelve un tamaño de 64 KB y una alineación de 64 KB, ya que los búferes solo pueden ser de 64 KB.</span><span class="sxs-lookup"><span data-stu-id="75405-157">For example, a single-element array with a one-byte-buffer returns a Size of 64KB and an Alignment of 64KB, as buffers currently can only be 64KB aligned.</span></span>

<span data-ttu-id="75405-158">Además, una matriz de tres elementos con dos texturas alineadas de 64 bits de un solo textura y una textura alineada de 4 MB de un solo textura tienen tamaños diferentes en función del orden de la matriz.</span><span class="sxs-lookup"><span data-stu-id="75405-158">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="75405-159">Si las texturas alineadas de 4 MB están en el centro, el tamaño resultante es 12MB.</span><span class="sxs-lookup"><span data-stu-id="75405-159">If the 4MB aligned textures is in the middle, the resulting Size is 12MB.</span></span> <span data-ttu-id="75405-160">De lo contrario, el tamaño resultante es 8 MB.</span><span class="sxs-lookup"><span data-stu-id="75405-160">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="75405-161">La alineación devuelta siempre sería de 4 MB, el superconjunto de todas las alineaciones de la matriz de recursos.</span><span class="sxs-lookup"><span data-stu-id="75405-161">The Alignment returned would always be 4MB, the super-set of all alignments in the resource array.</span></span>

<span data-ttu-id="75405-162">Haga referencia a las siguientes API:</span><span class="sxs-lookup"><span data-stu-id="75405-162">Reference the following APIs:</span></span>

-   [<span data-ttu-id="75405-163">**\_Información de \_ asignación de recursos de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="75405-163">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [<span data-ttu-id="75405-164">**GetResourceAllocationInfo**</span><span class="sxs-lookup"><span data-stu-id="75405-164">**GetResourceAllocationInfo**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="75405-165">Alineación del búfer</span><span class="sxs-lookup"><span data-stu-id="75405-165">Buffer alignment</span></span>

<span data-ttu-id="75405-166">Las restricciones de alineación del búfer no han cambiado desde D3D11, en particular:</span><span class="sxs-lookup"><span data-stu-id="75405-166">Buffer alignment restrictions have not changed from D3D11, notably:</span></span>

-   <span data-ttu-id="75405-167">4 MB para las texturas de varios ejemplos.</span><span class="sxs-lookup"><span data-stu-id="75405-167">4 MB for multi-sample textures.</span></span>
-   <span data-ttu-id="75405-168">64 KB para texturas y búferes de muestra única.</span><span class="sxs-lookup"><span data-stu-id="75405-168">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75405-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75405-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75405-170">Subasignación dentro de búferes</span><span class="sxs-lookup"><span data-stu-id="75405-170">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




