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
# <a name="uploading-different-types-of-resources"></a>Cargar diferentes tipos de recursos

Muestra cómo utilizar un búfer para cargar datos de búfer de constantes y datos de búfer de vértices en la GPU, y cómo subasignar y colocar datos correctamente en los búferes. El uso de un único búfer aumenta la flexibilidad del uso de memoria y proporciona a las aplicaciones un control más estricto del uso de memoria. También se muestran las diferencias entre los modelos D3D11 y D3D12 para cargar diferentes tipos de recursos.

-   [Cargar diferentes tipos de recursos](#upload-different-types-of-resources)
    -   [Ejemplo de código: D3D11](#code-example-d3d11)
    -   [Ejemplo de código: D3D12](#code-example-d3d12)
-   [Constantes](#constants)
-   [Recursos](#uploading-different-types-of-resources)
-   [Reflexión del tamaño de los recursos](#resource-size-reflection)
-   [Alineación del búfer](#buffer-alignment)
-   [Temas relacionados](#related-topics)

## <a name="upload-different-types-of-resources"></a>Cargar diferentes tipos de recursos

En D3D12, las aplicaciones crean un búfer para acomodar distintos tipos de datos de recursos para cargar y copian los datos de recursos en el mismo búfer de forma similar para los distintos datos de recursos. A continuación, se crean vistas individuales para enlazar esos datos de recursos a la canalización de gráficos en el nuevo modelo de enlace de recursos.

En D3D11, las aplicaciones crean búferes independientes para diferentes tipos de datos de recursos (tenga en cuenta los distintos `BindFlags` usados en el código de ejemplo D3D11 que se muestra a continuación), enlazando explícitamente cada búfer de recursos a la canalización de gráficos y actualizando los datos de recursos con diferentes métodos basados en diferentes tipos de recursos.

Tanto en D3D12 como en D3D11, las aplicaciones solo deben usar los recursos de carga en los que la CPU escribirá los datos una vez y la GPU los leerá una vez. Si la GPU va a leer los datos varias veces, la GPU no leerá los datos de forma lineal o la representación ya está limitada por GPU. La mejor opción puede ser usar [**ID3D12GraphicsCommandList:: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) o [**ID3D12GraphicsCommandList:: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) para copiar los datos del búfer de carga en un recurso predeterminado. Un recurso predeterminado puede residir en la memoria de vídeo física en GPU discretas.

### <a name="code-example-d3d11"></a>Ejemplo de código: D3D11

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

### <a name="code-example-d3d12"></a>Ejemplo de código: D3D12

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

Tenga en cuenta el uso de las estructuras [**auxiliares \_ CD3DX12 \_ propiedades del montón**](cd3dx12-heap-properties.md) y la [**\_ \_ Descripción del recurso CD3DX12**](cd3dx12-resource-desc.md).

## <a name="constants"></a>Constantes

Para establecer constantes, vértices e índices dentro de un montón de carga o Readback, use las siguientes API:

-   [**ID3D12Device::CreateConstantBufferView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [**ID3D12GraphicsCommandList::IASetIndexBuffer**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a>Recursos

Los recursos son el concepto D3D, que abstrae el uso de la memoria física de GPU. Los recursos requieren espacio de direcciones virtuales de GPU para tener acceso a la memoria física. La creación de recursos es de subproceso libre.

Hay tres tipos de recursos con respecto a la creación de direcciones virtuales y la flexibilidad en D3D12:

-   Recursos confirmados

    Los recursos confirmados son la idea más común de los recursos D3D en las generaciones. Al crear este tipo de recurso, se asigna un intervalo de direcciones virtuales, un montón implícito lo suficientemente grande como para ajustarse a todo el recurso y se confirma el intervalo de direcciones virtuales en la memoria física encapsulada por el montón. Las propiedades implícitas del montón deben pasarse para coincidir con la paridad funcional con las versiones anteriores de D3D. Consulte [**ID3D12Device:: CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

-   Recursos reservados

    Los recursos reservados son equivalentes a los recursos en mosaico de D3D11. En su creación, solo se asigna un intervalo de direcciones virtuales y no se asigna a ningún montón. La aplicación asignará estos recursos a los montones más adelante. Actualmente, las capacidades de estos recursos no se han modificado a través de D3D11, ya que se pueden asignar a un montón en una granularidad de mosaicos de 64 KB con [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings). Consulte [ **ID3D12Device:: CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)

-   Recursos colocados

    En el caso de D3D12, las aplicaciones pueden crear montones independientes de los recursos. Posteriormente, la aplicación puede buscar varios recursos en un solo montón. Esto puede hacerse sin crear recursos en mosaico o reservados, lo que permite que las aplicaciones puedan crear directamente las capacidades de todos los tipos de recursos. Se pueden superponer varios recursos y la aplicación debe usar `TiledResourceBarrier` para volver a usar la memoria física correctamente. Consulte [ **ID3D12Device:: CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)

## <a name="resource-size-reflection"></a>Reflexión del tamaño de los recursos

Las aplicaciones deben usar la reflexión del tamaño de los recursos para comprender cuánta texturas de sala con diseños de texturas desconocidos requieren en montones. También se admiten los búferes, pero principalmente para mayor comodidad.

Las aplicaciones deben tener en cuenta las principales discrepancias de alineación, para ayudar a empaquetar los recursos con mayor densidad.

Por ejemplo, una matriz de un solo elemento con un búfer de un byte devuelve un tamaño de 64 KB y una alineación de 64 KB, ya que los búferes solo pueden ser de 64 KB.

Además, una matriz de tres elementos con dos texturas alineadas de 64 bits de un solo textura y una textura alineada de 4 MB de un solo textura tienen tamaños diferentes en función del orden de la matriz. Si las texturas alineadas de 4 MB están en el centro, el tamaño resultante es 12MB. De lo contrario, el tamaño resultante es 8 MB. La alineación devuelta siempre sería de 4 MB, el superconjunto de todas las alineaciones de la matriz de recursos.

Haga referencia a las siguientes API:

-   [**\_Información de \_ asignación de recursos de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [**GetResourceAllocationInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a>Alineación del búfer

Las restricciones de alineación del búfer no han cambiado desde D3D11, en particular:

-   4 MB para las texturas de varios ejemplos.
-   64 KB para texturas y búferes de muestra única.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subasignación dentro de búferes](large-buffers.md)
</dt> </dl>

 

 




