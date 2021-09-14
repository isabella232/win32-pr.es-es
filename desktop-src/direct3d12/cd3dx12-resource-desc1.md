---
title: CD3DX12_RESOURCE_DESC1 estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de [**una D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) estructura.
keywords:
- CD3DX12_RESOURCE_DESC1 estructura
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 87fe62c475e1d961258671355c4c9be133bf0a41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966859"
---
# <a name="cd3dx12_resource_desc1-structure"></a>CD3DX12_RESOURCE_DESC1 estructura

Estructura auxiliar para permitir la inicialización sencilla de [**una D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) estructura.

## <a name="syntax"></a>Sintaxis

```cpp
struct CD3DX12_RESOURCE_DESC1 : public D3D12_RESOURCE_DESC1
{
    CD3DX12_RESOURCE_DESC1();
    explicit CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1& o) noexcept;
    CD3DX12_RESOURCE_DESC1(
        D3D12_RESOURCE_DIMENSION dimension,
        UINT64 alignment,
        UINT64 width,
        UINT height,
        UINT16 depthOrArraySize,
        UINT16 mipLevels,
        DXGI_FORMAT format,
        UINT sampleCount,
        UINT sampleQuality,
        D3D12_TEXTURE_LAYOUT layout,
        D3D12_RESOURCE_FLAGS flags,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        UINT64 width,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex1D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex2D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        UINT sampleCount = 1,
        UINT sampleQuality = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex3D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 depth,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    inline UINT16 Depth() const noexcept;
    inline UINT16 ArraySize() const noexcept;
    inline UINT8 PlaneCount(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT Subresources(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice) noexcept;
};
inline bool operator==(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
inline bool operator!=(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
```

## <a name="members"></a>Members

`CD3DX12_RESOURCE_DESC1`

Constructor predeterminado. Crea una nueva instancia sin inicializar de un **CD3DX12_RESOURCE_DESC1**.

`CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1&)`

Constructor que crea una nueva instancia de un **CD3DX12_RESOURCE_DESC1** inicializado con el contenido de una [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) estructura.

`CD3DX12_RESOURCE_DESC1(D3D12_RESOURCE_DIMENSION, UINT64, UINT64, UINT, UINT16, UINT16, DXGI_FORMAT, UINT, UINT, D3D12_TEXTURE_LAYOUT, D3D12_RESOURCE_FLAGS, UINT = 0, UINT = 0, UINT = 0)`

Constructor que crea una nueva instancia de un **CD3DX12_RESOURCE_DESC1** inicializado con los parámetros pasados a ella.

`Buffer(const D3D12_RESOURCE_ALLOCATION_INFO&, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE)`

Función estática que construye y devuelve una nueva instancia de **un** CD3DX12_RESOURCE_DESC1 inicializado con estos valores.

|Miembro de datos|value|
|-|-|
|Dimensión|D3D12_RESOURCE_DIMENSION_BUFFER|
|Alineación|*resAllocInfo*. Alineación|
|Ancho|*resAllocInfo*. SizeInBytes|
|Alto|1|
|DepthOrArraySize|1|
|MipLevels|1|
|Formato|DXGI_FORMAT_UNKNOWN|
|SampleDesc.Count|1|
|SampleDesc.Quality|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Marcas|*flags*|
|SamplerFeedbackMipRegion.Width|0|
|SamplerFeedbackMipRegion.Height|0|
|SamplerFeedbackMipRegion.Depth|0|

`Buffer(UINT64, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, UINT64 = 0)`

Función estática que construye y devuelve una nueva instancia de **un** CD3DX12_RESOURCE_DESC1 inicializado con estos valores.

|Miembro de datos|value|
|-|-|
|Dimensión|D3D12_RESOURCE_DIMENSION_BUFFER|
|Alineación|*Alineación*|
|Ancho|*width*|
|Alto|1|
|DepthOrArraySize|1|
|MipLevels|1|
|Formato|DXGI_FORMAT_UNKNOWN|
|SampleDesc.Count|1|
|SampleDesc.Quality|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Marcas|*flags*|
|SamplerFeedbackMipRegion.Width|0|
|SamplerFeedbackMipRegion.Height|0|
|SamplerFeedbackMipRegion.Depth|0|

`Tex1D(DXGI_FORMAT, UINT64, UINT16 = 1, UINT16 = 0, D3D12_RESOURCE_FLAGS D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

Función estática que construye y devuelve una nueva instancia de **un** CD3DX12_RESOURCE_DESC1 inicializado con estos valores.

|Miembro de datos|value|
|-|-|
|Dimensión|D3D12_RESOURCE_DIMENSION_TEXTURE1D|
|Alineación|*Alineación*|
|Ancho|*width*|
|Alto|1|
|DepthOrArraySize|*arraySize*|
|MipLevels|*mipLevels*|
|Formato|*format*|
|SampleDesc.Count|1|
|SampleDesc.Quality|0|
|Layout|*Diseño*|
|Marcas|*flags*|
|SamplerFeedbackMipRegion.Width|0|
|SamplerFeedbackMipRegion.Height|0|
|SamplerFeedbackMipRegion.Depth|0|

`Tex2D(DXGI_FORMAT, UINT64, UINT, UINT16 = 1, UINT16 = 0, UINT = 1, UINT = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0, UINT = 0, UINT = 0, UINT = 0)`

Función estática que construye y devuelve una nueva instancia de **un** CD3DX12_RESOURCE_DESC1 inicializado con estos valores.

|Miembro de datos|value|
|-|-|
|Dimensión|D3D12_RESOURCE_DIMENSION_TEXTURE2D|
|Alineación|*Alineación*|
|Ancho|*width*|
|Alto|*height*|
|DepthOrArraySize|*arraySize*|
|MipLevels|*mipLevels*|
|Formato|*format*|
|SampleDesc.Count|*sampleCount*|
|SampleDesc.Quality|*sampleQuality*|
|Layout|*Diseño*|
|Marcas|*flags*|
|SamplerFeedbackMipRegion.Width|*samplerFeedbackMipRegionWidth*|
|SamplerFeedbackMipRegion.Height|*samplerFeedbackMipRegionHeight*|
|SamplerFeedbackMipRegion.Depth|*samplerFeedbackMipRegionDepth*|

`Tex3D(DXGI_FORMAT, UINT64, UINT, UINT16, UINT16 = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

Función estática que construye y devuelve una nueva instancia de **un** CD3DX12_RESOURCE_DESC1 inicializado con estos valores.

|Miembro de datos|value|
|-|-|
|Dimensión|D3D12_RESOURCE_DIMENSION_TEXTURE3D|
|Alineación|*Alineación*|
|Ancho|*width*|
|Alto|*height*|
|DepthOrArraySize|*Profundidad*|
|MipLevels|*mipLevels*|
|Formato|*format*|
|SampleDesc.Count|1|
|SampleDesc.Quality|0|
|Layout|*Diseño*|
|Marcas|*flags*|
|SamplerFeedbackMipRegion.Width|0|
|SamplerFeedbackMipRegion.Height|0|
|SamplerFeedbackMipRegion.Depth|0|

`Depth`

Devuelve un **UINT16** que contiene la profundidad del recurso.

`ArraySize`

Devuelve un **UINT16** que contiene el tamaño de la matriz del recurso.

`PlaneCount(ID3D12Device*)`

Devuelve un **UINT8 que** contiene el recuento de plano para el formato del recurso.

`Subresources(ID3D12Device*)`

Devuelve un **UINT** que contiene el número de subrecursos del recurso.

`CalcSubresource(UINT, UINT, UINT)`

Ejecuta y devuelve un **UINT** que contiene un índice de subrecursos para el recurso en función de los parámetros que se le han pasado.

`operator==(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

Una función libre que devuelve si los dos parámetros son iguales en el nivel de `true` miembro; de lo contrario, `false` .

`operator!=(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

Función gratuita que devuelve si los dos parámetros son miembros no `true` iguales; en caso contrario, `false` .

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Consulte también

* [D3DX12_RESOURCE_DESC1](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1)
* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
