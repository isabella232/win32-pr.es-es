---
title: CD3DX12_RESOURCE_DESC estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de DESC de recursos D3D12 \_ .
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- Estructura de CD3DX12_RESOURCE_DESC
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
ms.openlocfilehash: 1b341646b2dee7f469235c0b0bc9bb4550e56ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718495"
---
# <a name="cd3dx12_resource_desc-structure"></a>CD3DX12 \_ estructura de DESC de recursos \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ DESC de recursos D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .

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

**\_ \_ Descripción del recurso CD3DX12 ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ Descripción de recurso CD3DX12 \_ .

</dd> <dt>

**\_Descripción del recurso CD3DX12 explícito \_ (const \_ D3D12 \_& desc.**
</dt> <dd>

Crea una nueva instancia de una \_ Descripción de recurso CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ DESC de recursos D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .

</dd> <dt>

**\_Descripción del recurso CD3DX12 \_ ( \_ \_ dimensión de dimensión de recursos D3D12, alineación UInt64, ancho UInt64, uint alto, Uint16 depthOrArraySize, UInt16 mipLevels, \_ formato de formato de DXGI, uint sampleCount, uint sampleQuality, \_ \_ diseño de diseño de textura de D3D12, marcas de marcas de recursos de D3D12 \_ \_ )**
</dt> <dd>

Crea una nueva instancia de una \_ Descripción de recurso CD3DX12 \_ , inicializando los parámetros siguientes:

[**D3D12 \_ Dimensión de \_ dimensión de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)

Alineación UINT64

UINT64 (ancho)

Alto de UINT

UINT16 depthOrArraySize

UINT16 mipLevels

[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

UINT sampleCount

UINT sampleQuality

[**D3D12 \_ Diseño \_ de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)

[**D3D12 \_ Marcas de \_ marcadores de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags)

</dd> <dt>

**Búfer alineado estático ( \_ \_ \_ información de asignación de recursos de const D3D12& resAllocInfo, D3D12 marcas de \_ recursos marcadores \_ = D3D12 \_ marca de recurso \_ \_ ninguno)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ \_ \_ Información de asignación de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

rechace [**D3D12 \_ Marcas de \_ marcadores de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = marca de recurso D3D12 \_ \_ \_ ninguno

</dd> <dt>

**Búfer alineado estático (UINT64 width, D3D12 \_ Resource \_ Flag Flags = \_ D3D12 \_ marcador \_ de recurso None, UINT64 Alignment = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT64 (ancho)

rechace [**D3D12 \_ Marcas de \_ marcadores de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = marca de recurso D3D12 \_ \_ \_ ninguno

rechace Alineación UINT64 = 0

</dd> <dt>

**Static inline Tex1D ( \_ formato de formato de DXGI, UINT64 width, Uint16 tamaño = 1, Uint16 mipLevels = 0, D3D12 Flag Flag \_ \_ Flags = D3D12 \_ \_ marcador \_ de recurso None, D3D12 \_ diseño de textura \_ layout = D3D12 \_ diseño de textura \_ \_ desconocido, UINT64 Alignment = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

UINT64 (ancho)

rechace UINT16 tamaño = 1

rechace UINT16 mipLevels = 0

rechace [**D3D12 \_ Marcas de \_ marcadores de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = marca de recurso D3D12 \_ \_ \_ ninguno

rechace [**D3D12 \_ Distribución de \_ diseño de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = Diseño de textura D3D12 \_ \_ \_ desconocido

rechace Alineación UINT64 = 0

</dd> <dt>

**Static inline Tex2D ( \_ formato de formato de DXGI, UINT64 width, uint height, Uint16 tamaño = 1, Uint16 mipLevels = 0, uint sampleCount = 1, uint sampleQuality = 0, D3D12 marcadores de \_ recursos \_ Flags = D3D12 \_ \_ marcador \_ de recurso None, D3D12 diseño de textura de la textura \_ \_ = D3D12 \_ \_ diseño de textura \_ desconocido, UINT64 Alignment = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

UINT64 (ancho)

Alto de UINT

rechace UINT16 tamaño = 1

rechace UINT16 mipLevels = 0

rechace UINT sampleCount = 1

rechace UINT sampleQuality = 0

rechace [**D3D12 \_ Marcas de \_ marcadores de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = marca de recurso D3D12 \_ \_ \_ ninguno

rechace [**D3D12 \_ Distribución de \_ diseño de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = Diseño de textura D3D12 \_ \_ \_ desconocido

rechace Alineación UINT64 = 0

</dd> <dt>

**Static inline Tex3D ( \_ formato de formato de DXGI, UINT64 width, uint height, UInt16 Depth, UINT16 mipLevels = 0, D3D12 \_ indicadores de marcadores de recursos \_ = D3D12 \_ \_ marca de recurso \_ None, D3D12 diseño de \_ textura \_ layout = D3D12 \_ diseño de textura \_ \_ desconocido, alineación UINT64 = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

UINT64 (ancho)

Alto de UINT

Profundidad UINT16

rechace UINT16 mipLevels = 0

rechace [**D3D12 \_ Marcas de \_ marcadores de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = marca de recurso D3D12 \_ \_ \_ ninguno

rechace [**D3D12 \_ Distribución de \_ diseño de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = Diseño de textura D3D12 \_ \_ \_ desconocido

rechace Alineación UINT64 = 0

</dd> <dt>

**Profundidad en línea () Const**
</dt> <dd>

Si Dimension = = [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D, devuelve DepthOrArraySize. Si Dimension! = D3D12 \_ \_ de la dimensión \_ de recursos TEXTURE3D, devuelve 1.

</dd> <dt>

**Inline tamaño () Const**
</dt> <dd>

Si Dimension! = D3D12 \_ \_ de la dimensión \_ de recursos TEXTURE3D, devuelve DepthOrArraySize. Si Dimension = = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, devuelve 1. Consulte [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.

</dd> <dt>

**Inline PlaneCount (ID3D12Device \* pDevice) Const**
</dt> <dd>

Devuelve D3D12GetFormatPlaneCount (pDevice, Format). Vea [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) y [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).

</dd> <dt>

**Subrecursos insertados (ID3D12Device \* pDevice) Const**
</dt> <dd>

Devuelve el número de Subrecursos, calculado como MipLevels \* tamaño () \* PlaneCount (pDevice).

</dd> <dt>

**Inline CalcSubresource (UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**
</dt> <dd>

Calcula un índice de Subrecursos mediante [**D3D12CalcSubresource**](d3d12calcsubresource.md).

</dd> <dt>

**Operator const D3D12 \_ \_ DESC& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> <dt>

**operador = = (const D3D12 \_ \_ DESC& l, const D3D12 \_ Resource \_ DESC& r)**
</dt> <dd>

Devuelve true si todos los miembros de cada estructura son idénticos.

</dd> <dt>

**Operator! = (const D3D12 \_ Resource \_ DESC& l, const D3D12 \_ Resource \_ DESC& r)**
</dt> <dd>

Devuelve false si todos los miembros de cada estructura son idénticos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Descripción del recurso D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

