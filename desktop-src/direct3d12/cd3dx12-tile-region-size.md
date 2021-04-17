---
title: CD3DX12_TILE_REGION_SIZE estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una estructura de tamaño de la región de mosaico de D3D12 \_ \_ \_ .
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- Estructura de CD3DX12_TILE_REGION_SIZE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707766"
---
# <a name="cd3dx12_tile_region_size-structure"></a>CD3DX12 \_ estructura de tamaño de la región de mosaico \_ \_

Estructura auxiliar para habilitar la inicialización sencilla de una estructura de tamaño de la [**\_ región de mosaico de \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ tamaño de la región de mosaico \_ \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un tamaño de región de mosaico de CD3DX12 \_ \_ \_ .

</dd> <dt>

**tamaño de la región de mosaico de CD3DX12 explícito \_ \_ \_ (const D3D12 tamaño de la \_ región de mosaico \_ \_ &o)**
</dt> <dd>

Crea una nueva instancia de un tamaño de región de mosaico de CD3DX12 \_ \_ \_ , inicializada con el contenido de otra estructura de tamaño de la [**\_ región de mosaico \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .

</dd> <dt>

**CD3DX12 \_ tamaño de la región de mosaico \_ \_ (uint NumTiles, bool useBox, uint width, UINT16 height, UInt16 Depth)**
</dt> <dd>

Crea una nueva instancia de un tamaño de región de mosaico de CD3DX12 \_ \_ \_ , inicializando los siguientes parámetros:

UINT numTiles

BOOL useBox

Ancho de UINT

Alto de UINT16

Profundidad UINT16

</dd> <dt>

**operador const D3D12 \_ tamaño de la región de mosaico \_ \_& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ tamaño de la región de mosaico \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





