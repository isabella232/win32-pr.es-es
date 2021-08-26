---
title: CD3DX12_RESOURCE_DESC estructura (D3dx12.h)
description: Una estructura auxiliar para permitir la inicialización sencilla de una estructura \_ DESC resource de D3D12. \_
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- CD3DX12_RESOURCE_DESC estructura
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c9d92953abdb0cf77a7a55f7b64341b857a111baaef0d84d4d44855b02efb2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028305"
---
# <a name="cd3dx12_resource_desc-structure"></a>ESTRUCTURA \_ \_ DESC DESC DE RECURSOS CD3DX12

Una estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ \_ DESC resource de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ RESOURCE \_ DESC()**
</dt> <dd>

Crea una nueva instancia de RESOURCE DESC CD3DX12 sin \_ \_ inicializar.

</dd> <dt>

**EXPLICIT CD3DX12 \_ RESOURCE \_ DESC(const D3D12 \_ RESOURCE \_ DESC& o)**
</dt> <dd>

Crea una nueva instancia de un DESC DE CD3DX12 RESOURCE, inicializado con el contenido de otra estructura \_ \_ [**\_ \_ DESC RESOURCE de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)

</dd> <dt>

**CD3DX12 \_ RESOURCE \_ DESC(D3D12 \_ RESOURCE DIMENSION \_ dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI \_ FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12 \_ TEXTURE LAYOUT \_ layout, D3D12 \_ RESOURCE \_ FLAGS flags)**
</dt> <dd>

Crea una nueva instancia de un \_ DESC DESC DESC DE CD3DX12 \_ RESOURCE, inicializando los parámetros siguientes:

[**D3D12 \_ Dimensión \_ DIMENSIÓN DE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) RECURSOS

Alineación de UINT64

Ancho de UINT64

Alto de UINT

UINT16 depthOrArraySize

UINT16 mipLevels

[**DXGI \_ Formato FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

UINT sampleCount

UINT sampleQuality

[**D3D12 \_ DISEÑO \_ DE TEXTURA**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)

[**D3D12 \_ Marcas \_ DE MARCAS DE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) RECURSOS

</dd> <dt>

**static inline Buffer(const D3D12 \_ RESOURCE ALLOCATION INFO& \_ \_ resAllocInfo, D3D12 \_ RESOURCE \_ FLAGS flags = D3D12 \_ RESOURCE FLAG \_ \_ NONE)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO&**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) resAllocInfo

(opt) [**D3D12 \_ Marcas \_ de RESOURCE FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 \_ RESOURCE FLAG \_ \_ NONE

</dd> <dt>

**static inline Buffer(UINT64 width, D3D12 \_ RESOURCE \_ FLAGS flags = D3D12 \_ RESOURCE FLAG \_ \_ NONE, UINT64 alignment = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

Ancho de UINT64

(opt) [**D3D12 \_ Marcas \_ de RESOURCE FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 \_ RESOURCE FLAG \_ \_ NONE

(opt) Alineación de UINT64 = 0

</dd> <dt>

**static inline Tex1D(DXGI \_ FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12 \_ RESOURCE \_ FLAGS flags = D3D12 \_ RESOURCE FLAG \_ \_ NONE, D3D12 \_ TEXTURE LAYOUT layout = \_ D3D12 \_ TEXTURE LAYOUT \_ \_ UNKNOWN, UINT64 alignment = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**DXGI \_ Formato FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Ancho de UINT64

(opt) UINT16 arraySize = 1

(opt) UINT16 mipLevels = 0

(opt) [**D3D12 \_ Marcas \_ de RESOURCE FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 \_ RESOURCE FLAG \_ \_ NONE

(opt) [**D3D12 \_ DISEÑO \_ DE TEXTURA**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) DISEÑO = DISEÑO DE TEXTURA D3D12 \_ \_ \_ DESCONOCIDO

(opt) Alineación de UINT64 = 0

</dd> <dt>

**static inline Tex2D(DXGI \_ FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12 \_ RESOURCE \_ FLAGS flags = D3D12 \_ RESOURCE FLAG \_ \_ NONE, D3D12 \_ TEXTURE LAYOUT layout = \_ D3D12 \_ TEXTURE LAYOUT \_ \_ UNKNOWN, UINT64 alignment = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**DXGI \_ Formato FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Ancho de UINT64

Alto de UINT

(opt) UINT16 arraySize = 1

(opt) UINT16 mipLevels = 0

(opt) UINT sampleCount = 1

(opt) UINT sampleQuality = 0

(opt) [**D3D12 \_ Marcas \_ de RESOURCE FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 \_ RESOURCE FLAG \_ \_ NONE

(opt) [**D3D12 \_ DISEÑO \_ DE TEXTURA**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) DISEÑO = DISEÑO DE TEXTURA D3D12 \_ \_ \_ DESCONOCIDO

(opt) Alineación de UINT64 = 0

</dd> <dt>

**static inline Texas3D(DXGI \_ FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12 \_ RESOURCE \_ FLAGS flags = D3D12 \_ RESOURCE FLAG \_ \_ NONE, D3D12 \_ TEXTURE LAYOUT layout = \_ D3D12 \_ TEXTURE LAYOUT \_ \_ UNKNOWN, UINT64 alignment = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**DXGI \_ Formato FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Ancho de UINT64

Alto de UINT

Profundidad UINT16

(opt) UINT16 mipLevels = 0

(opt) [**D3D12 \_ Marcas \_ de RESOURCE FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 \_ RESOURCE FLAG \_ \_ NONE

(opt) [**D3D12 \_ DISEÑO \_ DE TEXTURA**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) DISEÑO = DISEÑO DE TEXTURA D3D12 \_ \_ \_ DESCONOCIDO

(opt) Alineación de UINT64 = 0

</dd> <dt>

**inline Depth() const**
</dt> <dd>

Si Dimension == [**D3D12 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D, devuelve DepthOrArraySize. Si dimension != D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE3D, devuelve 1.

</dd> <dt>

**inline ArraySize() const**
</dt> <dd>

Si dimension != D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE3D, devuelve DepthOrArraySize. Si Dimension == D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE3D, devuelve 1. Consulte [**DIMENSIÓN DE RECURSOS D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.

</dd> <dt>

**inline PlaneCount(ID3D12Device \* pDevice) const**
</dt> <dd>

Devuelve D3D12GetFormatPlaneCount(pDevice, Format). Vea [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) e [**ID3D12Device.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)

</dd> <dt>

**inline Subresources(ID3D12Device \* pDevice) const**
</dt> <dd>

Devuelve el número de subrecursos, calculado como MipLevels \* ArraySize() \* PlaneCount(pDevice).

</dd> <dt>

**inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**
</dt> <dd>

Calcula un índice de subrecurso mediante [**D3D12CalcSubresource**](d3d12calcsubresource.md).

</dd> <dt>

**operator const D3D12 \_ RESOURCE \_ DESC&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> <dt>

**operator == (const D3D12 \_ RESOURCE \_ DESC& l, const D3D12 \_ RESOURCE \_ DESC& r)**
</dt> <dd>

Devuelve true si todos los miembros de cada estructura son idénticos.

</dd> <dt>

**operator != (const D3D12 \_ RESOURCE \_ DESC& l, const D3D12 \_ RESOURCE \_ DESC& r)**
</dt> <dd>

Devuelve false si todos los miembros de cada estructura son idénticos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ RESOURCE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

