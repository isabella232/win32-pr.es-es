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
# <a name="uploading-texture-data-through-buffers"></a>Cargar datos de textura a través de búferes

La carga de datos de textura 2D o 3D es similar a la carga de datos 1D, salvo que las aplicaciones necesitan prestar atención a la alineación de datos relacionada con el paso de las filas. Los búferes se pueden usar de forma ortogonal y simultánea desde varias partes de la canalización de gráficos y son muy flexibles.

-   [Carga de datos de textura a través de búferes](#upload-texture-data-via-buffers)
-   [asincrónica](#copying)
-   [Asignación y desasignación](#mapping-and-unmapping)
-   [Alineación del búfer](#buffer-alignment)
-   [Temas relacionados](#related-topics)

## <a name="upload-texture-data-via-buffers"></a>Carga de datos de textura a través de búferes

Las aplicaciones deben cargar datos a través de [**ID3D12GraphicsCommandList:: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) o [**ID3D12GraphicsCommandList:: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion). Es mucho más probable que los datos de textura sean más grandes, se tenga acceso a ellos de forma repetida y se beneficien de la mayor coherencia en la caché de los diseños de memoria no lineales que otros datos de recursos. Cuando se utilizan búferes en D3D12, las aplicaciones tienen control total sobre la colocación de los datos y la organización asociada con la copia de los datos de recursos, siempre que se satisfagan los requisitos de alineación de memoria.

En el ejemplo se resalta el lugar en el que la aplicación simplemente alisa los datos 2D en 1D antes de colocarlos en el búfer. En el caso de un escenario de 2D de mipmap, la aplicación puede aplanar cada subrecurso de manera discreta y con rapidez usar un algoritmo de subasignación 1D, o bien usar una técnica de subasignación de 2D más complicada para minimizar el uso de memoria de vídeo. Se espera que la primera técnica se use con más frecuencia, ya que es más sencilla. La segunda técnica puede ser útil cuando se empaquetan datos en un disco o a través de una red. En cualquier caso, la aplicación debe seguir llamando a las API de copia de cada subrecurso.

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

Tenga en cuenta el uso de las estructuras [**auxiliares \_ CD3DX12 \_ propiedades del montón**](cd3dx12-heap-properties.md) y la ubicación de la [**copia de \_ textura \_ \_ CD3DX12**](cd3dx12-texture-copy-location.md)y los métodos [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) y [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

## <a name="copying"></a>asincrónica

Los métodos de D3D12 permiten a las aplicaciones reemplazar los datos iniciales de D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)y Resource. Un subrecurso 3D único de los datos de textura de la fila principal puede encontrarse en recursos de búfer. [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) puede copiar los datos de textura del búfer en un recurso de textura con un diseño de textura desconocido y viceversa. Las aplicaciones deben preferir este tipo de técnica para rellenar los recursos de GPU a los que se accede con frecuencia, mediante la creación de búferes grandes en un montón de carga mientras se crean los recursos de GPU a los que se accede con frecuencia en un montón predeterminado que no tiene acceso de CPU. Esta técnica admite eficazmente GPU discretas y sus grandes cantidades de memoria inaccesible a la CPU, sin tener que usar arquitecturas UMA con frecuencia.

Tenga en cuenta las dos constantes siguientes:

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [**\_Superficie de SUBrecursos de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [**\_Superficie de \_ Subrecursos colocada en D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [**D3D12 \_ \_ Ubicación de copia de textura \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [**\_Tipo de \_ copia de textura D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a>Asignación y desasignación

La asignación [**y la**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) [**desasignación**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) se pueden llamar mediante varios subprocesos de forma segura. La primera llamada a **map** asigna un intervalo de direcciones virtuales de CPU para el recurso. La última llamada a DEALLOCATE desasigna el intervalo de direcciones **virtuales de la** CPU. La dirección virtual de CPU se devuelve normalmente a la aplicación.

Cada vez que se pasan datos entre la CPU y la GPU a través de los recursos de montones de readback, [**se debe usar**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) [**asignar y desasignar**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) para admitir todos los sistemas D3D12 se admite en. Mantener los intervalos lo más estrechos posible maximiza la eficacia en los sistemas que requieren intervalos (consulte [**el \_ intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).

El rendimiento de las herramientas de depuración no solo se beneficia del uso preciso de los intervalos en todas las llamadas de [**asignación de asignación**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) , sino también de las aplicaciones que desasignan recursos cuando ya no se realizan modificaciones de la CPU.

El método D3D11 de usar [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (con el conjunto de parámetros discard) para cambiar el nombre de los recursos no se admite en D3D12. Las aplicaciones deben implementar el cambio de nombre de recursos. Todas las llamadas de **mapa** no se \_ sobrescriben implícitamente y son multiproceso. Es responsabilidad de la aplicación asegurarse de que cualquier trabajo de GPU relevante contenido en las listas de comandos finaliza antes de tener acceso a los datos con la CPU. Las llamadas a D3D12 a la **asignación** no vacían implícitamente ningún búfer de comandos ni bloquean la espera para que la GPU finalice el trabajo. Como resultado, el mapa y [**la**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) **desasignación** se pueden optimizar incluso en algunos escenarios.

## <a name="buffer-alignment"></a>Alineación del búfer

Restricciones de alineación del búfer:

-   La copia de Subrecursos lineal debe estar alineada a 512 bytes (con el paso de fila alineado con los \_ bytes de alineación de tono de datos de D3D12 Texture \_ \_ \_ ).
-   Las lecturas de datos constantes deben ser un múltiplo de 256 bytes desde el principio del montón (es decir, solo desde direcciones de 256 bytes alineadas).
-   Las lecturas de datos de índice deben ser un múltiplo del tamaño del tipo de datos del índice (es decir, solo de las direcciones que están alineadas naturalmente para los datos).
-   [**ID3D12GraphicsCommandList::D rawinstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) y [**ID3D12GraphicsCommandList::D**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) los datos rawindexedinstanced deben ser de desplazamientos que sean múltiplos de 4 (es decir, solo de direcciones que estén alineadas con DWORD).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subasignación dentro de búferes](large-buffers.md)
</dt> </dl>

 

 