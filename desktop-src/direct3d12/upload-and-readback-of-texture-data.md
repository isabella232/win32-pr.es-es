---
title: Carga de datos de textura a través de búferes
description: La carga de datos de textura 2D o 3D es similar a la carga de datos 1D, salvo que las aplicaciones deben prestar más atención a la alineación de datos relacionada con el tono de fila.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c095d93237a44369cb249d6de9e514fa7021a91fb78430ddc428c88e4e71b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027995"
---
# <a name="uploading-texture-data-through-buffers"></a>Carga de datos de textura a través de búferes

La carga de datos de textura 2D o 3D es similar a la carga de datos 1D, salvo que las aplicaciones deben prestar más atención a la alineación de datos relacionada con el tono de fila. Los búferes se pueden usar ortogonal y simultáneamente desde varias partes de la canalización de gráficos, y son muy flexibles.

-   [Upload Datos de textura a través de búferes](#upload-texture-data-via-buffers)
-   [asincrónica](#copying)
-   [Asignación y desapping](#mapping-and-unmapping)
-   [Alineación del búfer](#buffer-alignment)
-   [Temas relacionados](#related-topics)

## <a name="upload-texture-data-via-buffers"></a>Upload Datos de textura a través de búferes

Las aplicaciones deben cargar datos a través [**de ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) o [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion). Es mucho más probable que los datos de textura sean más grandes, se acceda repetidamente y se beneficien de la mejor coherencia de caché de los diseños de memoria no lineal que otros datos de recursos. Cuando se usan búferes en D3D12, las aplicaciones tienen control total sobre la colocación y la disposición de los datos asociados con la copia de datos de recursos, siempre y cuando se cumplen los requisitos de alineación de memoria.

El ejemplo resalta dónde la aplicación simplemente aplana los datos 2D en 1D antes de colocarlos en el búfer. En el escenario de mipmap 2D, la aplicación puede aplanar cada sub-recurso discretamente y usar rápidamente un algoritmo de subatribución 1D, o bien usar una técnica de subatribución 2D más complicada para minimizar el uso de memoria de vídeo. Se espera que la primera técnica se utilice con más frecuencia, ya que es más sencilla. La segunda técnica puede ser útil al empaquetar datos en un disco o a través de una red. En cualquier caso, la aplicación todavía debe llamar a las API de copia para cada sub-recurso.

```cpp
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

Tenga en cuenta el uso de las estructuras auxiliares [**CD3DX12 \_ HEAP \_ PROPERTIES**](cd3dx12-heap-properties.md) y [**CD3DX12 \_ TEXTURE COPY \_ \_ LOCATION**](cd3dx12-texture-copy-location.md)y los métodos [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) y [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

## <a name="copying"></a>asincrónica

Los métodos D3D12 permiten a las aplicaciones reemplazar a D3D11 [**UpdateSubresource,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource) [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)y los datos iniciales del recurso. Un único subrecurso 3D de datos de textura principal de fila puede encontrarse en recursos de búfer. [**CopyTextureRegion puede**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) copiar los datos de textura del búfer en un recurso de textura con un diseño de textura desconocido, y viceversa. Las aplicaciones deben preferir este tipo de técnica para rellenar los recursos de GPU a los que se accede con frecuencia, mediante la creación de búferes grandes en un montón DE CARGA mientras se crean los recursos de GPU a los que se accede con frecuencia en un montón DEFAULT que no tiene acceso a la CPU. Esta técnica admite eficazmente GPU discretas y sus grandes cantidades de memoria inaccesible para la CPU, sin que las arquitecturas de UMA se ve afectadas habitualmente.

Tenga en cuenta las dos constantes siguientes:

```cpp
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [**SUPERFICIE DE SUBRECURSO D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [**SUPERFICIE DE SUBRECURSO COLOCADO EN D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [**UBICACIÓN DE COPIA DE TEXTURA D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [**TIPO DE COPIA DE TEXTURA D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a>Asignación y desapping

[**Varios**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) subprocesos pueden llamar a Map y [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) de forma segura. La primera llamada a **Map** asigna un intervalo de direcciones virtuales de CPU para el recurso. La última llamada a **Unmap** desasigna el intervalo de direcciones virtuales de CPU. La dirección virtual de CPU se devuelve normalmente a la aplicación.

Cada vez que se pasan datos entre la CPU y la GPU a través de recursos en montones de readback, se deben usar [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) y [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) para admitir todos los sistemas en los que se admite D3D12. Mantener los intervalos lo más ajustados posible maximiza la eficacia en los sistemas que requieren intervalos (consulte [**D3D12 \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).

El rendimiento de las herramientas de depuración no solo [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)se beneficia del uso preciso de intervalos en todas las llamadas a Map  /  [**Unmap,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) sino también de las aplicaciones que no asignan recursos cuando ya no se realizarán modificaciones en la CPU.

El método D3D11 de usar [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (con el parámetro DISCARD establecido) para cambiar el nombre de los recursos no se admite en D3D12. Las aplicaciones deben implementar el cambio de nombre de los recursos. Todas **las llamadas** a Map son implícitamente NO OVERWRITE y \_ multiproceso. Es responsabilidad de la aplicación asegurarse de que cualquier trabajo de GPU relevante incluido en las listas de comandos finaliza antes de que los datos de acceso con la CPU. Las llamadas D3D12 a **Map** no vacían implícitamente ningún búfer de comandos ni bloquean la espera a que la GPU finalice el trabajo. Como resultado, **Map** y [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) incluso se pueden optimizar en algunos escenarios.

## <a name="buffer-alignment"></a>Alineación del búfer

Restricciones de alineación del búfer:

-   La copia de subrecursos lineal debe alinearse con 512 bytes (con el paso de fila alineado con los bytes de ALINEACIÓN DE PITCH DE DATOS DE TEXTURA D3D12). \_ \_ \_ \_
-   Las lecturas de datos constantes deben ser un múltiplo de 256 bytes desde el principio del montón (es decir, solo desde direcciones alineadas de 256 bytes).
-   Las lecturas de datos de índice deben ser un múltiplo del tamaño del tipo de datos de índice (es decir, solo desde direcciones alineadas de forma natural para los datos).
-   Los datos [**ID3D12GraphicsCommandList::ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) deben ser de desplazamientos que sean múltiplo de 4 (es decir, solo de direcciones alineadas con DWORD).

## <a name="related-topics"></a>Temas relacionados

* [Subasignación en los búferes](large-buffers.md)
