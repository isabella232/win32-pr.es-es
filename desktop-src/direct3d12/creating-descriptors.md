---
title: Crear descriptores
description: Describe y muestra ejemplos para crear vistas de búfer de índice, vértices y constantes; recursos del sombreador, destino de representación, acceso desordenado, salida de secuencia y vistas de la galería de símbolos de profundidad; y muestreadores. Todos los métodos para crear descriptores son de subprocesamiento libre.
ms.assetid: 0D360A7C-8A2F-49E1-A5CC-98C958B59D1C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aac9aab5dde0f5ca0864fcc1627ade984c6b6ccf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549109"
---
# <a name="creating-descriptors"></a><span data-ttu-id="b02c6-104">Crear descriptores</span><span class="sxs-lookup"><span data-stu-id="b02c6-104">Creating Descriptors</span></span>

<span data-ttu-id="b02c6-105">Describe y muestra ejemplos para crear vistas de búfer de índice, vértices y constantes; recursos del sombreador, destino de representación, acceso desordenado, salida de secuencia y vistas de la galería de símbolos de profundidad; y muestreadores.</span><span class="sxs-lookup"><span data-stu-id="b02c6-105">Describes and shows examples for creating index, vertex, and constant buffer views; shader resource, render target, unordered access, stream output and depth-stencil views; and samplers.</span></span> <span data-ttu-id="b02c6-106">Todos los métodos para crear descriptores son de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="b02c6-106">All methods for creating descriptors are free threaded.</span></span>

-   [<span data-ttu-id="b02c6-107">Vista de búfer de índice</span><span class="sxs-lookup"><span data-stu-id="b02c6-107">Index Buffer View</span></span>](#index-buffer-view)
-   [<span data-ttu-id="b02c6-108">Vista de búfer de vértices</span><span class="sxs-lookup"><span data-stu-id="b02c6-108">Vertex Buffer View</span></span>](#vertex-buffer-view)
-   [<span data-ttu-id="b02c6-109">Vista de recursos del sombreador</span><span class="sxs-lookup"><span data-stu-id="b02c6-109">Shader Resource View</span></span>](#shader-resource-view)
-   [<span data-ttu-id="b02c6-110">Vista de búfer de constantes</span><span class="sxs-lookup"><span data-stu-id="b02c6-110">Constant Buffer View</span></span>](#constant-buffer-view)
-   [<span data-ttu-id="b02c6-111">Muestra</span><span class="sxs-lookup"><span data-stu-id="b02c6-111">Sampler</span></span>](#sampler)
-   [<span data-ttu-id="b02c6-112">Vista de acceso desordenado</span><span class="sxs-lookup"><span data-stu-id="b02c6-112">Unordered Access View</span></span>](#unordered-access-view)
-   [<span data-ttu-id="b02c6-113">Vista de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="b02c6-113">Stream Output View</span></span>](#stream-output-view)
-   [<span data-ttu-id="b02c6-114">Vista de destino de representación</span><span class="sxs-lookup"><span data-stu-id="b02c6-114">Render Target View</span></span>](#render-target-view)
-   [<span data-ttu-id="b02c6-115">Vista de galería de símbolos de profundidad</span><span class="sxs-lookup"><span data-stu-id="b02c6-115">Depth Stencil View</span></span>](#depth-stencil-view)
-   [<span data-ttu-id="b02c6-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b02c6-116">Related topics</span></span>](#related-topics)

## <a name="index-buffer-view"></a><span data-ttu-id="b02c6-117">Vista de búfer de índice</span><span class="sxs-lookup"><span data-stu-id="b02c6-117">Index Buffer View</span></span>

<span data-ttu-id="b02c6-118">Para crear una vista de búfer de índice, rellene una estructura de [**vista del búfer de índice de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view) :</span><span class="sxs-lookup"><span data-stu-id="b02c6-118">To create an index buffer view, fill out a [**D3D12\_INDEX\_BUFFER\_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view) structure:</span></span>

``` syntax
typedef struct D3D12_INDEX_BUFFER_VIEW
{
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
    UINT SizeInBytes;
    DXGI_FORMAT Format;
}   D3D12_INDEX_BUFFER_VIEW;
```

<span data-ttu-id="b02c6-119">Establezca la ubicación (llamar a [**GetGPUVirtualAddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) y el tamaño del búfer, teniendo en cuenta que la \_ dirección virtual de GPU D3D12 \_ \_ se define como:</span><span class="sxs-lookup"><span data-stu-id="b02c6-119">Set the location (call [**GetGPUVirtualAddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) and size of the buffer, noting that D3D12\_GPU\_VIRTUAL\_ADDRESS is defined as:</span></span>

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

<span data-ttu-id="b02c6-120">Consulte la enumeración de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="b02c6-120">Refer to the [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enum.</span></span> <span data-ttu-id="b02c6-121">Normalmente, para un búfer de índice se puede usar la siguiente definición:</span><span class="sxs-lookup"><span data-stu-id="b02c6-121">Typically for an index buffer the following define might be used:</span></span>

`const DXGI_FORMAT StandardIndexFormat = DXGI_FORMAT_R32_UINT;`

<span data-ttu-id="b02c6-122">Por último, llame a [**ID3D12GraphicsCommandList:: IASetIndexBuffer**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer).</span><span class="sxs-lookup"><span data-stu-id="b02c6-122">Finally call [**ID3D12GraphicsCommandList::IASetIndexBuffer**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer).</span></span>

<span data-ttu-id="b02c6-123">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="b02c6-123">For example,</span></span>


```C++
// Initialize the index buffer view.
m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
```



## <a name="vertex-buffer-view"></a><span data-ttu-id="b02c6-124">Vista de búfer de vértices</span><span class="sxs-lookup"><span data-stu-id="b02c6-124">Vertex Buffer View</span></span>

<span data-ttu-id="b02c6-125">Para crear una vista de búfer de vértices, rellene una estructura de [**\_ vista de \_ búfer \_ de vértices D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view) :</span><span class="sxs-lookup"><span data-stu-id="b02c6-125">To create a vertex buffer view, fill out a [**D3D12\_VERTEX\_BUFFER\_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view) structure:</span></span>

``` syntax
typedef struct D3D12_VERTEX_BUFFER_VIEW {
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;  
    UINT SizeInBytes;  
    UINT StrideInBytes;  
} D3D12_VERTEX_BUFFER_VIEW;
```

<span data-ttu-id="b02c6-126">Establezca la ubicación (llamar a [**GetGPUVirtualAddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) y el tamaño del búfer, teniendo en cuenta que la \_ dirección virtual de GPU D3D12 \_ \_ se define como:</span><span class="sxs-lookup"><span data-stu-id="b02c6-126">Set the location (call [**GetGPUVirtualAddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) and size of the buffer, noting that D3D12\_GPU\_VIRTUAL\_ADDRESS is defined as:</span></span>

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

<span data-ttu-id="b02c6-127">El intervalo es normalmente el tamaño de una estructura de datos de vértice único, como `sizeof(Vertex);` , a continuación, llame a [**ID3D12GraphicsCommandList:: IASetVertexBuffers**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers).</span><span class="sxs-lookup"><span data-stu-id="b02c6-127">The stride is typically the size of a single vertex data structure, such as `sizeof(Vertex);`, then call [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers).</span></span>

<span data-ttu-id="b02c6-128">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="b02c6-128">For example,</span></span>


```C++
// Initialize the vertex buffer view.
m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
m_vertexBufferView.SizeInBytes = SampleAssets::VertexDataSize;
m_vertexBufferView.StrideInBytes = SampleAssets::StandardVertexStride;
```



## <a name="shader-resource-view"></a><span data-ttu-id="b02c6-129">Vista de recursos del sombreador</span><span class="sxs-lookup"><span data-stu-id="b02c6-129">Shader Resource View</span></span>

<span data-ttu-id="b02c6-130">Para crear una vista de recursos del sombreador, rellene una estructura de [**\_ \_ \_ \_ Descripción de recursos de sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) :</span><span class="sxs-lookup"><span data-stu-id="b02c6-130">To create a shader resource view, fill out a [**D3D12\_SHADER\_RESOURCE\_VIEW\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) structure:</span></span>

``` syntax
typedef struct D3D12_SHADER_RESOURCE_VIEW_DESC  
    {  
    DXGI_FORMAT Format;  
    D3D12_SRV_DIMENSION ViewDimension;  
    UINT Shader4ComponentMapping;  
    union   
        {  
        D3D12_BUFFER_SRV Buffer;  
        D3D12_TEX1D_SRV Texture1D;  
        D3D12_TEX1D_ARRAY_SRV Texture1DArray;  
        D3D12_TEX2D_SRV Texture2D;  
        D3D12_TEX2D_ARRAY_SRV Texture2DArray;  
        D3D12_TEX2DMS_SRV Texture2DMS;  
        D3D12_TEX2DMS_ARRAY_SRV Texture2DMSArray;  
        D3D12_TEX3D_SRV Texture3D;  
        D3D12_TEXCUBE_SRV TextureCube;  
        D3D12_TEXCUBE_ARRAY_SRV TextureCubeArray;  
        }   ;  
    }   D3D12_SHADER_RESOURCE_VIEW_DESC; 
```

<span data-ttu-id="b02c6-131">El `ViewDimension` campo se establece en cero o en un valor de la enumeración de [**\_ \_ \_ marcadores SRV de búfer D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags) .</span><span class="sxs-lookup"><span data-stu-id="b02c6-131">The `ViewDimension` field is set to zero, or one value of the [**D3D12\_BUFFER\_SRV\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags) enum.</span></span>

<span data-ttu-id="b02c6-132">Las enumeraciones y estructuras a las que hace referencia la [**\_ vista de recursos del sombreador de D3D12 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) son:</span><span class="sxs-lookup"><span data-stu-id="b02c6-132">The enums and structures referenced by [**D3D12\_SHADER\_RESOURCE\_VIEW\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) are:</span></span>

-   [<span data-ttu-id="b02c6-133">**formato de DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="b02c6-133">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [<span data-ttu-id="b02c6-134">**\_SRV de búfer de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b02c6-134">**D3D12\_BUFFER\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv)
-   [<span data-ttu-id="b02c6-135">**D3D12 \_ TEX1D \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-135">**D3D12\_TEX1D\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv)
-   [<span data-ttu-id="b02c6-136">**D3D12 \_ TEX1D \_ array \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-136">**D3D12\_TEX1D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [<span data-ttu-id="b02c6-137">**D3D12 \_ TEX2D \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-137">**D3D12\_TEX2D\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [<span data-ttu-id="b02c6-138">**D3D12 \_ TEX2D \_ array \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-138">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="b02c6-139">**D3D12 \_ TEX2DMS \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-139">**D3D12\_TEX2DMS\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv)
-   [<span data-ttu-id="b02c6-140">**D3D12 \_ TEX2DMS \_ array \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-140">**D3D12\_TEX2DMS\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [<span data-ttu-id="b02c6-141">**D3D12 \_ TEX3D \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-141">**D3D12\_TEX3D\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv)
-   [<span data-ttu-id="b02c6-142">**D3D12 \_ TEXCUBE \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-142">**D3D12\_TEXCUBE\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv)
-   [<span data-ttu-id="b02c6-143">**D3D12 \_ TEXCUBE \_ array \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-143">**D3D12\_TEXCUBE\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv)

<span data-ttu-id="b02c6-144">Tenga en cuenta que se ha `ResourceMinLODClamp` agregado Float a SRVs para Tex1D/2D/3D/Cube.</span><span class="sxs-lookup"><span data-stu-id="b02c6-144">Note below that float `ResourceMinLODClamp` has been added to SRVs for Tex1D/2D/3D/Cube.</span></span> <span data-ttu-id="b02c6-145">En D3D11, era una propiedad de un recurso, pero esto no coincidía con el modo en que se implementaba en el hardware.</span><span class="sxs-lookup"><span data-stu-id="b02c6-145">In D3D11, it was a property of a resource, but this did not match how it was implemented in hardware.</span></span> <span data-ttu-id="b02c6-146">`StructureByteStride` se ha agregado al búfer SRVs, donde en D3D11 era una propiedad del recurso.</span><span class="sxs-lookup"><span data-stu-id="b02c6-146">`StructureByteStride` has been added to Buffer SRVs, where in D3D11 it was a property of the resource.</span></span> <span data-ttu-id="b02c6-147">Si el intervalo es distinto de cero, que indica una vista de búfer estructurado y el formato debe establecerse en el formato de DXGI \_ \_ desconocido.</span><span class="sxs-lookup"><span data-stu-id="b02c6-147">If the stride is nonzero, that indicates a structured buffer view, and the format must be set to DXGI\_FORMAT\_UNKNOWN.</span></span>

<span data-ttu-id="b02c6-148">Por último, para crear la vista de recursos del sombreador, llame a [**ID3D12Device:: CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="b02c6-148">Finally, to create the shader resource view, call [**ID3D12Device::CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview).</span></span>

<span data-ttu-id="b02c6-149">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="b02c6-149">For example,</span></span>


```C++
// Describe and create an SRV.
D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
srvDesc.Format = tex.Format;
srvDesc.Texture2D.MipLevels = tex.MipLevels;
srvDesc.Texture2D.MostDetailedMip = 0;
srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);
```



## <a name="constant-buffer-view"></a><span data-ttu-id="b02c6-150">Vista de búfer de constantes</span><span class="sxs-lookup"><span data-stu-id="b02c6-150">Constant Buffer View</span></span>

<span data-ttu-id="b02c6-151">Para crear una vista de búfer de constantes, rellene una D3D12 de búfer de constantes de la [**\_ \_ \_ vista \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc) :</span><span class="sxs-lookup"><span data-stu-id="b02c6-151">To create a constant buffer view, fill out a [**D3D12\_CONSTANT\_BUFFER\_VIEW\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc) structure:</span></span>

``` syntax
typedef struct D3D12_CONSTANT_BUFFER_VIEW_DESC {
  D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
  UINT   SizeInBytes;
} D3D12_CONSTANT_BUFFER_VIEW_DESC;
```

<span data-ttu-id="b02c6-152">Después, llame a [**ID3D12Device:: CreateConstantBufferView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview).</span><span class="sxs-lookup"><span data-stu-id="b02c6-152">Then call [**ID3D12Device::CreateConstantBufferView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview).</span></span>

<span data-ttu-id="b02c6-153">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="b02c6-153">For example,</span></span>


```C++
// Describe and create a constant buffer view.
D3D12_CONSTANT_BUFFER_VIEW_DESC cbvDesc = {};
cbvDesc.BufferLocation = m_constantBuffer->GetGPUVirtualAddress();
cbvDesc.SizeInBytes = (sizeof(ConstantBuffer) + 255) & ~255;    // CB size is required to be 256-byte aligned.
m_device->CreateConstantBufferView(&cbvDesc, m_cbvHeap->GetCPUDescriptorHandleForHeapStart());
```



## <a name="sampler"></a><span data-ttu-id="b02c6-154">Muestra</span><span class="sxs-lookup"><span data-stu-id="b02c6-154">Sampler</span></span>

<span data-ttu-id="b02c6-155">Para crear un ejemplo, rellene una [**estructura \_ \_ DESC de muestra de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc) :</span><span class="sxs-lookup"><span data-stu-id="b02c6-155">To create a sample, fill out a [**D3D12\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc) structure:</span></span>

``` syntax
typedef struct D3D12_SAMPLER_DESC
{
    D3D12_FILTER Filter;
    D3D12_TEXTURE_ADDRESS_MODE AddressU;
    D3D12_TEXTURE_ADDRESS_MODE AddressV;
    D3D12_TEXTURE_ADDRESS_MODE AddressW;
    FLOAT MipLODBias;
    UINT MaxAnisotropy;
    D3D12_COMPARISON_FUNC ComparisonFunc;
    FLOAT BorderColor[4]; // RGBA
    FLOAT MinLOD;
    FLOAT MaxLOD;
} D3D12_SAMPLER_DESC;
```

<span data-ttu-id="b02c6-156">Para rellenar esta estructura, consulte las enumeraciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="b02c6-156">To fill out this structure, refer to the following enums:</span></span>

-   [<span data-ttu-id="b02c6-157">**Filtro de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b02c6-157">**D3D12\_FILTER**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)
-   [<span data-ttu-id="b02c6-158">**\_Tipo de filtro D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b02c6-158">**D3D12\_FILTER\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_type)
-   [<span data-ttu-id="b02c6-159">**\_Tipo de \_ reducción de filtro de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b02c6-159">**D3D12\_FILTER\_REDUCTION\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_reduction_type)
-   [<span data-ttu-id="b02c6-160">**\_Modo de \_ dirección de textura D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b02c6-160">**D3D12\_TEXTURE\_ADDRESS\_MODE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)
-   [<span data-ttu-id="b02c6-161">**FUNC. de \_ comparación D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b02c6-161">**D3D12\_COMPARISON\_FUNC**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)

<span data-ttu-id="b02c6-162">Por último, llame a [**ID3D12Device:: CreateSampler**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler).</span><span class="sxs-lookup"><span data-stu-id="b02c6-162">Finally, call [**ID3D12Device::CreateSampler**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler).</span></span>

<span data-ttu-id="b02c6-163">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="b02c6-163">For example,</span></span>


```C++
// Describe and create a sampler.
D3D12_SAMPLER_DESC samplerDesc = {};
samplerDesc.Filter = D3D12_FILTER_MIN_MAG_MIP_LINEAR;
samplerDesc.AddressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.AddressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.AddressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.MinLOD = 0;
samplerDesc.MaxLOD = D3D12_FLOAT32_MAX;
samplerDesc.MipLODBias = 0.0f;
samplerDesc.MaxAnisotropy = 1;
samplerDesc.ComparisonFunc = D3D12_COMPARISON_FUNC_ALWAYS;
m_device->CreateSampler(&samplerDesc, m_samplerHeap->GetCPUDescriptorHandleForHeapStart());
```



## <a name="unordered-access-view"></a><span data-ttu-id="b02c6-164">Vista de acceso desordenado</span><span class="sxs-lookup"><span data-stu-id="b02c6-164">Unordered Access View</span></span>

<span data-ttu-id="b02c6-165">Para crear una vista de acceso desordenado, rellene una estructura de descripción de la [**\_ \_ \_ vista \_ de acceso desordenado de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc) :</span><span class="sxs-lookup"><span data-stu-id="b02c6-165">To create an unordered access view, fill out a [**D3D12\_UNORDERED\_ACCESS\_VIEW\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc) structure:</span></span>

``` syntax
typedef struct D3D12_UNORDERED_ACCESS_VIEW_DESC
{
    DXGI_FORMAT Format;
    D3D12_UAV_DIMENSION ViewDimension;

    union
    {
        D3D12_BUFFER_UAV Buffer;
        D3D12_TEX1D_UAV Texture1D;
        D3D12_TEX1D_ARRAY_UAV Texture1DArray;
        D3D12_TEX2D_UAV Texture2D;
        D3D12_TEX2D_ARRAY_UAV Texture2DArray;
        D3D12_TEX3D_UAV Texture3D;
    };
} D3D12_UNORDERED_ACCESS_VIEW_DESC;
```

<span data-ttu-id="b02c6-166">El `ViewDimension` campo se establece en cero o en un valor de la enumeración [**D3D12 \_ buffer \_ UAV \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) .</span><span class="sxs-lookup"><span data-stu-id="b02c6-166">The `ViewDimension` field is set to zero, or one value of the [**D3D12\_BUFFER\_UAV\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) enum.</span></span>

<span data-ttu-id="b02c6-167">Consulte las siguientes enumeraciones y estructuras:</span><span class="sxs-lookup"><span data-stu-id="b02c6-167">Refer to the following enums and structures:</span></span>

-   [<span data-ttu-id="b02c6-168">**formato de DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="b02c6-168">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [<span data-ttu-id="b02c6-169">**\_UAV de búfer de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b02c6-169">**D3D12\_BUFFER\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav)
-   [<span data-ttu-id="b02c6-170">**D3D12 \_ TEX1D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-170">**D3D12\_TEX1D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [<span data-ttu-id="b02c6-171">**D3D12 \_ TEX1D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-171">**D3D12\_TEX1D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [<span data-ttu-id="b02c6-172">**D3D12 \_ TEX2D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-172">**D3D12\_TEX2D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [<span data-ttu-id="b02c6-173">**D3D12 \_ TEX2D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-173">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)
-   [<span data-ttu-id="b02c6-174">**D3D12 \_ TEX3D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-174">**D3D12\_TEX3D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

<span data-ttu-id="b02c6-175">`StructureByteStride` se ha agregado al búfer UAVs, donde en D3D11 era una propiedad del recurso.</span><span class="sxs-lookup"><span data-stu-id="b02c6-175">`StructureByteStride` has been added to Buffer UAVs, where in D3D11 it was a property of the resource.</span></span> <span data-ttu-id="b02c6-176">Si el intervalo es distinto de cero, que indica una vista de búfer estructurado y el formato debe establecerse en el formato de DXGI \_ \_ desconocido.</span><span class="sxs-lookup"><span data-stu-id="b02c6-176">If the stride is nonzero, that indicates a structured buffer view, and the format must be set to DXGI\_FORMAT\_UNKNOWN.</span></span>

<span data-ttu-id="b02c6-177">Por último, llame a [**ID3D12Device:: CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span><span class="sxs-lookup"><span data-stu-id="b02c6-177">Finally call [**ID3D12Device::CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span></span>

<span data-ttu-id="b02c6-178">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="b02c6-178">For example,</span></span>


```C++
// Create the unordered access views (UAVs) that store the results of the compute work.
CD3DX12_CPU_DESCRIPTOR_HANDLE processedCommandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), ProcessedCommandsOffset, m_cbvSrvUavDescriptorSize);
for (UINT frame = 0; frame < FrameCount; frame++)
{
    // Allocate a buffer large enough to hold all of the indirect commands
    // for a single frame as well as a UAV counter.
    commandBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(CommandBufferSizePerFrame + sizeof(UINT), D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS);
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
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

// Allocate a buffer that can be used to reset the UAV counters and initialize it to 0.
ThrowIfFailed(m_device->CreateCommittedResource(
    &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
    D3D12_HEAP_FLAG_NONE,
    &CD3DX12_RESOURCE_DESC::Buffer(sizeof(UINT)),
    D3D12_RESOURCE_STATE_GENERIC_READ,
    
    nullptr,
    IID_PPV_ARGS(&m_processedCommandBufferCounterReset)));

UINT8* pMappedCounterReset = nullptr;
CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
ThrowIfFailed(m_processedCommandBufferCounterReset->Map(0, &readRange, reinterpret_cast<void**>(&pMappedCounterReset)));
ZeroMemory(pMappedCounterReset, sizeof(UINT));
m_processedCommandBufferCounterReset->Unmap(0, nullptr);
```



## <a name="stream-output-view"></a><span data-ttu-id="b02c6-179">Vista de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="b02c6-179">Stream Output View</span></span>

<span data-ttu-id="b02c6-180">Para crear una vista de salida de flujo, rellene una estructura [**\_ DESC de \_ salida \_ de flujo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .</span><span class="sxs-lookup"><span data-stu-id="b02c6-180">To create a stream output view, fill out a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

``` syntax
typedef struct D3D12_STREAM_OUTPUT_DESC  
    {  
    _Field_size_full_(NumEntries)  const D3D12_SO_DECLARATION_ENTRY *pSODeclaration;  
    UINT NumEntries;  
    _Field_size_full_(NumStrides)  const UINT *pBufferStrides;  
    UINT NumStrides;  
    UINT RasterizedStream;  
    }   D3D12_STREAM_OUTPUT_DESC;  
```

<span data-ttu-id="b02c6-181">Después, llame a [**ID3D12GraphicsCommandList:: SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets).</span><span class="sxs-lookup"><span data-stu-id="b02c6-181">Then call [**ID3D12GraphicsCommandList::SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets).</span></span>

## <a name="render-target-view"></a><span data-ttu-id="b02c6-182">Vista de destino de representación</span><span class="sxs-lookup"><span data-stu-id="b02c6-182">Render Target View</span></span>

<span data-ttu-id="b02c6-183">Para crear una vista de destino de representación, rellene una estructura de [**DESC de vista de destino de representación de D3D12 \_ \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc) .</span><span class="sxs-lookup"><span data-stu-id="b02c6-183">To create a render target view, fill out a [**D3D12\_RENDER\_TARGET\_VIEW\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc) structure.</span></span>

``` syntax
typedef struct D3D12_RENDER_TARGET_VIEW_DESC
{
    DXGI_FORMAT Format;
    D3D12_RTV_DIMENSION ViewDimension;

    union
    {
        D3D12_BUFFER_RTV Buffer;
        D3D12_TEX1D_RTV Texture1D;
        D3D12_TEX1D_ARRAY_RTV Texture1DArray;
        D3D12_TEX2D_RTV Texture2D;
        D3D12_TEX2D_ARRAY_RTV Texture2DArray;
        D3D12_TEX2DMS_RTV Texture2DMS;
        D3D12_TEX2DMS_ARRAY_RTV Texture2DMSArray;
        D3D12_TEX3D_RTV Texture3D;
    };
} D3D12_RENDER_TARGET_VIEW_DESC;
```

<span data-ttu-id="b02c6-184">El `ViewDimension` campo se establece en cero o en un valor de la enumeración de [**\_ \_ dimensiones D3D12 RTV**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_rtv_dimension) .</span><span class="sxs-lookup"><span data-stu-id="b02c6-184">The `ViewDimension` field is set to zero, or one value of the [**D3D12\_RTV\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_rtv_dimension) enum.</span></span>

<span data-ttu-id="b02c6-185">Consulte las siguientes enumeraciones y estructuras:</span><span class="sxs-lookup"><span data-stu-id="b02c6-185">Refer to the following enums and structures:</span></span>

-   [<span data-ttu-id="b02c6-186">**formato de DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="b02c6-186">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [<span data-ttu-id="b02c6-187">**D3D12 \_ búfer \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-187">**D3D12\_BUFFER\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv)
-   [<span data-ttu-id="b02c6-188">**D3D12 \_ TEX1D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-188">**D3D12\_TEX1D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [<span data-ttu-id="b02c6-189">**D3D12 \_ TEX1D \_ matriz \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-189">**D3D12\_TEX1D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [<span data-ttu-id="b02c6-190">**D3D12 \_ TEX2D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-190">**D3D12\_TEX2D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [<span data-ttu-id="b02c6-191">**D3D12 \_ TEX2DMS \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-191">**D3D12\_TEX2DMS\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv)
-   [<span data-ttu-id="b02c6-192">**D3D12 \_ TEX2D \_ matriz \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-192">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="b02c6-193">**D3D12 \_ TEX2DMS \_ matriz \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-193">**D3D12\_TEX2DMS\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [<span data-ttu-id="b02c6-194">**D3D12 \_ TEX3D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-194">**D3D12\_TEX3D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)

<span data-ttu-id="b02c6-195">Por último, llame a [**ID3D12Device:: CreateRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview).</span><span class="sxs-lookup"><span data-stu-id="b02c6-195">Finally, call [**ID3D12Device::CreateRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview).</span></span>

<span data-ttu-id="b02c6-196">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="b02c6-196">For example,</span></span>

```C++
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
```



## <a name="depth-stencil-view"></a><span data-ttu-id="b02c6-197">Vista de galería de símbolos de profundidad</span><span class="sxs-lookup"><span data-stu-id="b02c6-197">Depth Stencil View</span></span>

<span data-ttu-id="b02c6-198">Para crear una vista de galería de símbolos de profundidad, rellene una estructura de D3D12 de estarcido de profundidad de la [**\_ \_ \_ vista \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc) :</span><span class="sxs-lookup"><span data-stu-id="b02c6-198">To create a depth stencil view, fill out a [**D3D12\_DEPTH\_STENCIL\_VIEW\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc) structure:</span></span>

``` syntax
typedef struct D3D12_DEPTH_STENCIL_VIEW_DESC  
    {  
    DXGI_FORMAT Format;  
    D3D12_DSV_DIMENSION ViewDimension;  
    D3D12_DSV_FLAGS Flags;  
    union   
        {  
        D3D12_TEX1D_DSV Texture1D;  
        D3D12_TEX1D_ARRAY_DSV Texture1DArray;  
        D3D12_TEX2D_DSV Texture2D;  
        D3D12_TEX2D_ARRAY_DSV Texture2DArray;  
        D3D12_TEX2DMS_DSV Texture2DMS;  
        D3D12_TEX2DMS_ARRAY_DSV Texture2DMSArray;  
        }   ;  
    }   D3D12_DEPTH_STENCIL_VIEW_DESC;  
```

<span data-ttu-id="b02c6-199">El `ViewDimension` campo se establece en cero o en un valor de la enumeración de [**\_ \_ dimensiones D3D12 DSV**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_dimension) .</span><span class="sxs-lookup"><span data-stu-id="b02c6-199">The `ViewDimension` field is set to zero, or one value of the [**D3D12\_DSV\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_dimension) enum.</span></span> <span data-ttu-id="b02c6-200">Consulte la enumeración [**D3D12 \_ DSV \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_flags) para ver la configuración de la marca.</span><span class="sxs-lookup"><span data-stu-id="b02c6-200">Refer to the [**D3D12\_DSV\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_flags) enum for the flag settings.</span></span>

<span data-ttu-id="b02c6-201">Consulte las siguientes enumeraciones y estructuras:</span><span class="sxs-lookup"><span data-stu-id="b02c6-201">Refer to the following enums and structures:</span></span>

-   [<span data-ttu-id="b02c6-202">**formato de DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="b02c6-202">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [<span data-ttu-id="b02c6-203">**D3D12 \_ TEX1D \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-203">**D3D12\_TEX1D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [<span data-ttu-id="b02c6-204">**D3D12 \_ TEX1D \_ array \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-204">**D3D12\_TEX1D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [<span data-ttu-id="b02c6-205">**D3D12 \_ TEX2D \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-205">**D3D12\_TEX2D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [<span data-ttu-id="b02c6-206">**D3D12 \_ TEX2D \_ array \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-206">**D3D12\_TEX2D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [<span data-ttu-id="b02c6-207">**D3D12 \_ TEX2DMS \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-207">**D3D12\_TEX2DMS\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv)
-   [<span data-ttu-id="b02c6-208">**D3D12 \_ TEX2DMS \_ array \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="b02c6-208">**D3D12\_TEX2DMS\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)

<span data-ttu-id="b02c6-209">Por último, llame a [**ID3D12Device:: CreateDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview).</span><span class="sxs-lookup"><span data-stu-id="b02c6-209">Finally, call [**ID3D12Device::CreateDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview).</span></span>

<span data-ttu-id="b02c6-210">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="b02c6-210">For example,</span></span>


```C++
// Create the depth stencil view.
{
    D3D12_DEPTH_STENCIL_VIEW_DESC depthStencilDesc = {};
    depthStencilDesc.Format = DXGI_FORMAT_D32_FLOAT;
    depthStencilDesc.ViewDimension = D3D12_DSV_DIMENSION_TEXTURE2D;
    depthStencilDesc.Flags = D3D12_DSV_FLAG_NONE;

    D3D12_CLEAR_VALUE depthOptimizedClearValue = {};
    depthOptimizedClearValue.Format = DXGI_FORMAT_D32_FLOAT;
    depthOptimizedClearValue.DepthStencil.Depth = 1.0f;
    depthOptimizedClearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Tex2D(DXGI_FORMAT_D32_FLOAT, m_width, m_height, 1, 0, 1, 0, D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL),
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &depthOptimizedClearValue,
        IID_PPV_ARGS(&m_depthStencil)
        ));

    m_device->CreateDepthStencilView(m_depthStencil.Get(), &depthStencilDesc, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



## <a name="related-topics"></a><span data-ttu-id="b02c6-211">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b02c6-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b02c6-212">Descriptores de</span><span class="sxs-lookup"><span data-stu-id="b02c6-212">Descriptors</span></span>](descriptors.md)
</dt> <dt>

[<span data-ttu-id="b02c6-213">Montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="b02c6-213">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 