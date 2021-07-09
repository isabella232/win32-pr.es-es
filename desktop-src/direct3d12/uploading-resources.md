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
# <a name="uploading-different-types-of-resources"></a>Carga de diferentes tipos de recursos

Muestra cómo usar un búfer para cargar datos de búfer constante y datos de búfer de vértices en la GPU, y cómo subasigna y coloca correctamente los datos en búferes. El uso de un solo búfer aumenta la flexibilidad de uso de memoria y proporciona a las aplicaciones un control más estricto sobre el uso de memoria. También se muestran las diferencias entre los modelos Direct3D 11 y Direct3D 12 para cargar diferentes tipos de recursos.

## <a name="upload-different-types-of-resources"></a>Upload diferentes tipos de recursos

En Direct3D 12, se crea un búfer para dar cabida a distintos tipos de datos de recursos para la carga y se copian los datos de recursos en el mismo búfer de forma similar para los distintos datos de recursos. A continuación, se crean vistas individuales para enlazar esos datos de recursos a la canalización de gráficos en el modelo de enlace de recursos de Direct3D 12.

En Direct3D 11, se crean búferes independientes para distintos tipos de datos de recursos (tenga en cuenta los distintos usados en el código de ejemplo de Direct3D 11 a continuación), se enlaza explícitamente cada búfer de recursos a la canalización de gráficos y se actualizan los datos de recursos con distintos métodos en función de los distintos tipos de `BindFlags` recursos.

En Direct3D 12 y Direct3D 11, debe usar recursos de carga solo donde la CPU escribirá los datos una vez y la GPU los leerá una vez.

En algunos casos,
* la GPU leerá los datos varias veces o
* la GPU no leerá los datos linealmente o
* la representación ya está significativamente limitada por GPU.

En esos casos, la mejor opción podría ser usar [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) o [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) para copiar los datos del búfer de carga en un recurso predeterminado.

Un recurso predeterminado puede residir en memoria de vídeo física en GPU discretas.

### <a name="code-example-direct3d-11"></a>Ejemplo de código: Direct3D 11

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

### <a name="code-example-direct3d-12"></a>Ejemplo de código: Direct3D 12

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

Tenga en cuenta el uso de las estructuras [**auxiliares CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) y [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).

## <a name="constants"></a>Constantes

Para establecer constantes, vértices e índices dentro de un montón de carga o reversión, use las siguientes API.

-   [**ID3D12Device::CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [**ID3D12GraphicsCommandList::IASetIndexBuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a>Recursos

Los recursos son el concepto de Direct3D que abstrae el uso de memoria física de GPU. Los recursos requieren espacio de direcciones virtuales de GPU para acceder a la memoria física. La creación de recursos es de subproceso libre.

Hay tres tipos de recursos con respecto a la creación de direcciones virtuales y la flexibilidad en Direct3D 12.

### <a name="committed-resources"></a>Recursos confirmados

Los recursos confirmados son la idea más común de los recursos de Direct3D a lo largo de las generaciones. La creación de un recurso de este tipo asigna un intervalo de direcciones virtuales, un montón implícito lo suficientemente grande como para ajustarse a todo el recurso, y confirma el intervalo de direcciones virtuales en la memoria física encapsulada por el montón. Las propiedades implícitas del montón deben pasarse para que coincidan con la paridad funcional con versiones anteriores de Direct3D. Consulte [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

### <a name="reserved-resources"></a>Recursos reservados

Los recursos reservados son equivalentes a los recursos en mosaico de Direct3D 11. En su creación, solo se asigna un intervalo de direcciones virtuales y no se asigna a ningún montón. La aplicación asignará estos recursos a montones más adelante. Actualmente, las funcionalidades de estos recursos no se modifican desde Direct3D 11, ya que se pueden asignar a un montón con una granularidad de mosaico de 64 KB [**con UpdateTileMappings.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) Consulte [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).

### <a name="placed-resources"></a>Recursos colocados

Como novedad de Direct3D 12, puede crear montones independientes de los recursos. Después, puede buscar varios recursos dentro de un único montón. Puede hacerlo sin crear recursos en mosaico o reservados, lo que permite las funcionalidades de todos los tipos de recursos que la aplicación puede crear directamente. Es posible que se superpongan varios recursos y debe usar [**id3D12GraphicsCommandList::ResourceBarcommand**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) para volver a usar la memoria física correctamente. Consulte [**ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).

## <a name="resource-size-reflection"></a>Reflexión del tamaño de los recursos

Debe usar la reflexión de tamaño de recurso para comprender cuántas texturas de espacio con diseños de textura desconocidos requieren en montones. También se admiten búferes, pero principalmente por comodidad.

Debe tener en cuenta las principales discrepancias de alineación para ayudar a empaquetar los recursos de forma más densa.

Por ejemplo, una matriz de un solo elemento  con un búfer de  un byte devuelve un tamaño de 64 KB y una alineación de 64 KB, ya que los búferes solo pueden estar alineados con 64 KB.

Además, una matriz de tres elementos con dos texturas alineadas de 64 KB de un solo texel y una textura alineada de 4 MB de un solo texel notifica tamaños diferentes en función del orden de la matriz. Si las texturas alineadas de 4 MB están en el centro, el *tamaño resultante* es de 12 MB. De lo contrario, el tamaño resultante es de 8 MB. La alineación devuelta siempre sería de 4 MB, el superconjunto de todas las alineaciones de la matriz de recursos.

Haga referencia a las SIGUIENTES API.

- [**INFORMACIÓN DE ASIGNACIÓN DE RECURSOS D3D12 \_ \_ \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
- [**GetResourceAllocationInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a>Alineación del búfer

Las restricciones de alineación del búfer no han cambiado de Direct3D 11, en particular:

- 4 MB para texturas de varias muestras.
- 64 KB para texturas y búferes de ejemplo único.

## <a name="related-topics"></a>Temas relacionados

* [Suballocation dentro de los búferes](large-buffers.md)
