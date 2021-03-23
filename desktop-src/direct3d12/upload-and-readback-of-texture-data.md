---
title: Cargar datos de textura a través de búferes
description: La carga de datos de textura 2D o 3D es similar a la carga de datos 1D, salvo que las aplicaciones necesitan prestar atención a la alineación de datos relacionada con el paso de las filas.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadbd1e71b3c9895b75c973397488472b57f8eb1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549176"
---
# <a name="uploading-texture-data-through-buffers"></a><span data-ttu-id="af527-103">Cargar datos de textura a través de búferes</span><span class="sxs-lookup"><span data-stu-id="af527-103">Uploading Texture Data Through Buffers</span></span>

<span data-ttu-id="af527-104">La carga de datos de textura 2D o 3D es similar a la carga de datos 1D, salvo que las aplicaciones necesitan prestar atención a la alineación de datos relacionada con el paso de las filas.</span><span class="sxs-lookup"><span data-stu-id="af527-104">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="af527-105">Los búferes se pueden usar de forma ortogonal y simultánea desde varias partes de la canalización de gráficos y son muy flexibles.</span><span class="sxs-lookup"><span data-stu-id="af527-105">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span>

-   [<span data-ttu-id="af527-106">Carga de datos de textura a través de búferes</span><span class="sxs-lookup"><span data-stu-id="af527-106">Upload Texture Data via Buffers</span></span>](#upload-texture-data-via-buffers)
-   [<span data-ttu-id="af527-107">asincrónica</span><span class="sxs-lookup"><span data-stu-id="af527-107">Copying</span></span>](#copying)
-   [<span data-ttu-id="af527-108">Asignación y desasignación</span><span class="sxs-lookup"><span data-stu-id="af527-108">Mapping and unmapping</span></span>](#mapping-and-unmapping)
-   [<span data-ttu-id="af527-109">Alineación del búfer</span><span class="sxs-lookup"><span data-stu-id="af527-109">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="af527-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af527-110">Related topics</span></span>](#related-topics)

## <a name="upload-texture-data-via-buffers"></a><span data-ttu-id="af527-111">Carga de datos de textura a través de búferes</span><span class="sxs-lookup"><span data-stu-id="af527-111">Upload Texture Data via Buffers</span></span>

<span data-ttu-id="af527-112">Las aplicaciones deben cargar datos a través de [**ID3D12GraphicsCommandList:: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) o [**ID3D12GraphicsCommandList:: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span><span class="sxs-lookup"><span data-stu-id="af527-112">Applications must upload data via [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span></span> <span data-ttu-id="af527-113">Es mucho más probable que los datos de textura sean más grandes, se tenga acceso a ellos de forma repetida y se beneficien de la mayor coherencia en la caché de los diseños de memoria no lineales que otros datos de recursos.</span><span class="sxs-lookup"><span data-stu-id="af527-113">Texture data is much more likely to be larger, accessed repeatedly, and benefit from the improved cache-coherency of non-linear memory layouts than other resource data.</span></span> <span data-ttu-id="af527-114">Cuando se utilizan búferes en D3D12, las aplicaciones tienen control total sobre la colocación de los datos y la organización asociada con la copia de los datos de recursos, siempre que se satisfagan los requisitos de alineación de memoria.</span><span class="sxs-lookup"><span data-stu-id="af527-114">When buffers are used in D3D12, applications have full control on data placement and arrangement associated with copying resource data around, as long as the memory alignment requirements are satisfied.</span></span>

<span data-ttu-id="af527-115">En el ejemplo se resalta el lugar en el que la aplicación simplemente alisa los datos 2D en 1D antes de colocarlos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="af527-115">The sample highlights where the application simply flattens 2D data into 1D before placing it in the buffer.</span></span> <span data-ttu-id="af527-116">En el caso de un escenario de 2D de mipmap, la aplicación puede aplanar cada subrecurso de manera discreta y con rapidez usar un algoritmo de subasignación 1D, o bien usar una técnica de subasignación de 2D más complicada para minimizar el uso de memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="af527-116">For the mipmap 2D scenario, the application can either flatten each sub-resource discretely and quickly use a 1D sub-allocation algorithm, or, use a more complicated 2D sub-allocation technique to minimize video memory utilization.</span></span> <span data-ttu-id="af527-117">Se espera que la primera técnica se use con más frecuencia, ya que es más sencilla.</span><span class="sxs-lookup"><span data-stu-id="af527-117">The first technique is expected to be used more often as it is simpler.</span></span> <span data-ttu-id="af527-118">La segunda técnica puede ser útil cuando se empaquetan datos en un disco o a través de una red.</span><span class="sxs-lookup"><span data-stu-id="af527-118">The second technique may be useful when packing data onto a disk or across a network.</span></span> <span data-ttu-id="af527-119">En cualquier caso, la aplicación debe seguir llamando a las API de copia de cada subrecurso.</span><span class="sxs-lookup"><span data-stu-id="af527-119">In either case, the application must still call the copy APIs for each sub-resource.</span></span>

``` syntax
// Prepare a pBitmap in memory, with bitmapWidth, bitmapHeight, and pixel format of DXGI_FORMAT_B8G8R8A8_UNORM. 
//
// Sub-allocate from the buffer for texture data.
//

D3D12_SUBRESOURCE_FOOTPRINT pitchedDesc = { 0 };
pitchedDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
pitchedDesc.Width = bitmapWidth;
pitchedDesc.Height = bitmapHeight;
pitchedDesc.Depth = 1;
pitchedDesc.RowPitch = Align(bitmapWidth * sizeof(DWORD), D3D12_TEXTURE_DATA_PITCH_ALIGNMENT);

//
// Note that the helper function UpdateSubresource in D3DX12.h, and ID3D12Device::GetCopyableFootprints 
// can help applications fill out D3D12_SUBRESOURCE_FOOTPRINT and D3D12_PLACED_SUBRESOURCE_FOOTPRINT structures.
//
// Refer to the D3D12 Code example for the previous section "Uploading Different Types of Resources"
// for the code for SuballocateFromBuffer.
//

SuballocateFromBuffer(
    pitchedDesc.Height * pitchedDesc.RowPitch,
    D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT
    );

D3D12_PLACED_SUBRESOURCE_FOOTPRINT placedTexture2D = { 0 };
placedTexture2D.Offset = m_pDataCur – m_pDataBegin;
placedTexture2D.Footprint = pitchedDesc;

//
// Copy texture data from DWORD* pBitmap->pixels to the buffer
//

for (UINT y = 0; y < bitmapHeight; y++)
{
  UINT8 *pScan = m_pDataBegin + placedTexture2D.Offset + y * pitchedDesc.RowPitch;
  memcpy( pScan, &(pBitmap->pixels[y * bitmapWidth]), sizeof(DWORD) * bitmapWidth );
}

//
// Create default texture2D resource.
//

D3D12_RESOURCE_DESC  textureDesc { ... };

CComPtr<ID3D12Resource> texture2D;
d3dDevice->CreateCommittedResource( 
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT), 
        D3D12_HEAP_FLAG_NONE, &textureDesc, 
        D3D12_RESOURCE_STATE_COPY_DEST, 
        nullptr, 
        IID_PPV_ARGS(&texture2D) );

//
// Copy heap data to texture2D.
//

commandList->CopyTextureRegion( 
        &CD3DX12_TEXTURE_COPY_LOCATION( texture2D, 0 ), 
        0, 0, 0, 
        &CD3DX12_TEXTURE_COPY_LOCATION( m_spUploadHeap, placedTexture2D ), 
        nullptr );
```

<span data-ttu-id="af527-120">Tenga en cuenta el uso de las estructuras [**auxiliares \_ CD3DX12 \_ propiedades del montón**](cd3dx12-heap-properties.md) y la ubicación de la [**copia de \_ textura \_ \_ CD3DX12**](cd3dx12-texture-copy-location.md)y los métodos [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) y [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span><span class="sxs-lookup"><span data-stu-id="af527-120">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_TEXTURE\_COPY\_LOCATION**](cd3dx12-texture-copy-location.md), and the methods [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) and [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span></span>

## <a name="copying"></a><span data-ttu-id="af527-121">asincrónica</span><span class="sxs-lookup"><span data-stu-id="af527-121">Copying</span></span>

<span data-ttu-id="af527-122">Los métodos de D3D12 permiten a las aplicaciones reemplazar los datos iniciales de D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)y Resource.</span><span class="sxs-lookup"><span data-stu-id="af527-122">D3D12 methods enable applications to replace D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion), and resource initial data.</span></span> <span data-ttu-id="af527-123">Un subrecurso 3D único de los datos de textura de la fila principal puede encontrarse en recursos de búfer.</span><span class="sxs-lookup"><span data-stu-id="af527-123">A single 3D subresource worth of row-major texture data may be located in buffer resources.</span></span> <span data-ttu-id="af527-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) puede copiar los datos de textura del búfer en un recurso de textura con un diseño de textura desconocido y viceversa.</span><span class="sxs-lookup"><span data-stu-id="af527-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) can copy that texture data from the buffer to a texture resource with an unknown texture layout, and vice versa.</span></span> <span data-ttu-id="af527-125">Las aplicaciones deben preferir este tipo de técnica para rellenar los recursos de GPU a los que se accede con frecuencia, mediante la creación de búferes grandes en un montón de carga mientras se crean los recursos de GPU a los que se accede con frecuencia en un montón predeterminado que no tiene acceso de CPU.</span><span class="sxs-lookup"><span data-stu-id="af527-125">Applications should prefer this type of technique to populate frequently accessed GPU resources, by creating large buffers in an UPLOAD heap while creating the frequently accessed GPU resources in a DEFAULT heap that has no CPU access.</span></span> <span data-ttu-id="af527-126">Esta técnica admite eficazmente GPU discretas y sus grandes cantidades de memoria inaccesible a la CPU, sin tener que usar arquitecturas UMA con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="af527-126">Such a technique efficiently supports discrete GPUs and their large amounts of CPU-inaccessible memory, without commonly impairing UMA architectures.</span></span>

<span data-ttu-id="af527-127">Tenga en cuenta las dos constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="af527-127">Note the following two constants:</span></span>

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [<span data-ttu-id="af527-128">**\_Superficie de SUBrecursos de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="af527-128">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [<span data-ttu-id="af527-129">**\_Superficie de \_ Subrecursos colocada en D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="af527-129">**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [<span data-ttu-id="af527-130">**D3D12 \_ \_ Ubicación de copia de textura \_**</span><span class="sxs-lookup"><span data-stu-id="af527-130">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [<span data-ttu-id="af527-131">**\_Tipo de \_ copia de textura D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="af527-131">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [<span data-ttu-id="af527-132">**ID3D12Device::GetCopyableFootprints**</span><span class="sxs-lookup"><span data-stu-id="af527-132">**ID3D12Device::GetCopyableFootprints**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [<span data-ttu-id="af527-133">**ID3D12GraphicsCommandList::CopyResource**</span><span class="sxs-lookup"><span data-stu-id="af527-133">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="af527-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="af527-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="af527-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="af527-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="af527-136">**ID3D12GraphicsCommandList::CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="af527-136">**ID3D12GraphicsCommandList::CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="af527-137">**ID3D12CommandQueue::UpdateTileMappings**</span><span class="sxs-lookup"><span data-stu-id="af527-137">**ID3D12CommandQueue::UpdateTileMappings**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a><span data-ttu-id="af527-138">Asignación y desasignación</span><span class="sxs-lookup"><span data-stu-id="af527-138">Mapping and unmapping</span></span>

<span data-ttu-id="af527-139">La asignación [**y la**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) [**desasignación**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) se pueden llamar mediante varios subprocesos de forma segura.</span><span class="sxs-lookup"><span data-stu-id="af527-139">[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) can be called by multiple threads safely.</span></span> <span data-ttu-id="af527-140">La primera llamada a **map** asigna un intervalo de direcciones virtuales de CPU para el recurso.</span><span class="sxs-lookup"><span data-stu-id="af527-140">The first call to **Map** allocates a CPU virtual address range for the resource.</span></span> <span data-ttu-id="af527-141">La última llamada a DEALLOCATE desasigna el intervalo de direcciones **virtuales de la** CPU.</span><span class="sxs-lookup"><span data-stu-id="af527-141">The last call to **Unmap** deallocates the CPU virtual address range.</span></span> <span data-ttu-id="af527-142">La dirección virtual de CPU se devuelve normalmente a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="af527-142">The CPU virtual address is commonly returned to the application.</span></span>

<span data-ttu-id="af527-143">Cada vez que se pasan datos entre la CPU y la GPU a través de los recursos de montones de readback, [**se debe usar**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) [**asignar y desasignar**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) para admitir todos los sistemas D3D12 se admite en.</span><span class="sxs-lookup"><span data-stu-id="af527-143">Whenever data is passed between the CPU and GPU through resources in readback heaps, [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) must be used to support all systems D3D12 is supported on.</span></span> <span data-ttu-id="af527-144">Mantener los intervalos lo más estrechos posible maximiza la eficacia en los sistemas que requieren intervalos (consulte [**el \_ intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span><span class="sxs-lookup"><span data-stu-id="af527-144">Keeping the ranges as tight as possible maximizes efficiency on the systems that require ranges (refer to [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span></span>

<span data-ttu-id="af527-145">El rendimiento de las herramientas de depuración no solo se beneficia del uso preciso de los intervalos en todas las llamadas de [**asignación de asignación**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) , sino también de las aplicaciones que desasignan recursos cuando ya no se realizan modificaciones de la CPU.</span><span class="sxs-lookup"><span data-stu-id="af527-145">The performance of debugging tools benefit not only from the accurate usage of ranges on all [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) calls, but also from applications unmapping resources when CPU modifications will no longer be made.</span></span>

<span data-ttu-id="af527-146">El método D3D11 de usar [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (con el conjunto de parámetros discard) para cambiar el nombre de los recursos no se admite en D3D12.</span><span class="sxs-lookup"><span data-stu-id="af527-146">The D3D11 method of using [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (with the DISCARD parameter set) to rename resources is not supported in D3D12.</span></span> <span data-ttu-id="af527-147">Las aplicaciones deben implementar el cambio de nombre de recursos.</span><span class="sxs-lookup"><span data-stu-id="af527-147">Applications must implement resource renaming themselves.</span></span> <span data-ttu-id="af527-148">Todas las llamadas de **mapa** no se \_ sobrescriben implícitamente y son multiproceso.</span><span class="sxs-lookup"><span data-stu-id="af527-148">All **Map** calls are implicitly NO\_OVERWRITE and multi-threaded.</span></span> <span data-ttu-id="af527-149">Es responsabilidad de la aplicación asegurarse de que cualquier trabajo de GPU relevante contenido en las listas de comandos finaliza antes de tener acceso a los datos con la CPU.</span><span class="sxs-lookup"><span data-stu-id="af527-149">It is the application’s responsibility to ensure that any relevant GPU work contained in command lists is finished before the accessing data with the CPU.</span></span> <span data-ttu-id="af527-150">Las llamadas a D3D12 a la **asignación** no vacían implícitamente ningún búfer de comandos ni bloquean la espera para que la GPU finalice el trabajo.</span><span class="sxs-lookup"><span data-stu-id="af527-150">D3D12 calls to **Map** do not implicitly flush any command buffers, nor do they block waiting for the GPU to finish work.</span></span> <span data-ttu-id="af527-151">Como resultado, el mapa y [**la**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) **desasignación** se pueden optimizar incluso en algunos escenarios.</span><span class="sxs-lookup"><span data-stu-id="af527-151">As a result, **Map** and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) may even be optimized out in some scenarios.</span></span>

## <a name="buffer-alignment"></a><span data-ttu-id="af527-152">Alineación del búfer</span><span class="sxs-lookup"><span data-stu-id="af527-152">Buffer alignment</span></span>

<span data-ttu-id="af527-153">Restricciones de alineación del búfer:</span><span class="sxs-lookup"><span data-stu-id="af527-153">Buffer alignment restrictions:</span></span>

-   <span data-ttu-id="af527-154">La copia de Subrecursos lineal debe estar alineada a 512 bytes (con el paso de fila alineado con los \_ bytes de alineación de tono de datos de D3D12 Texture \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="af527-154">Linear subresource copying must be aligned to 512 bytes (with the row pitch aligned to D3D12\_TEXTURE\_DATA\_PITCH\_ALIGNMENT bytes).</span></span>
-   <span data-ttu-id="af527-155">Las lecturas de datos constantes deben ser un múltiplo de 256 bytes desde el principio del montón (es decir, solo desde direcciones de 256 bytes alineadas).</span><span class="sxs-lookup"><span data-stu-id="af527-155">Constant data reads must be a multiple of 256 bytes from the beginning of the heap (i.e. only from addresses that are 256-byte aligned).</span></span>
-   <span data-ttu-id="af527-156">Las lecturas de datos de índice deben ser un múltiplo del tamaño del tipo de datos del índice (es decir, solo de las direcciones que están alineadas naturalmente para los datos).</span><span class="sxs-lookup"><span data-stu-id="af527-156">Index data reads must be a multiple of the index data type size (i.e. only from addresses that are naturally aligned for the data).</span></span>
-   <span data-ttu-id="af527-157">[**ID3D12GraphicsCommandList::D rawinstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) y [**ID3D12GraphicsCommandList::D**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) los datos rawindexedinstanced deben ser de desplazamientos que sean múltiplos de 4 (es decir, solo de direcciones que estén alineadas con DWORD).</span><span class="sxs-lookup"><span data-stu-id="af527-157">[**ID3D12GraphicsCommandList::DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) and [**ID3D12GraphicsCommandList::DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) data must be from offsets that are multiples of 4 (i.e. only from addresses that are DWORD aligned).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af527-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af527-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af527-159">Subasignación dentro de búferes</span><span class="sxs-lookup"><span data-stu-id="af527-159">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 