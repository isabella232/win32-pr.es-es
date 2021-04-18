---
title: CD3DX12_TILE_SHAPE estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una estructura de forma de mosaico de D3D12 \_ \_ .
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- Estructura de CD3DX12_TILE_SHAPE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998a14e1bd4898d83d049ea50bc056abaeb68544
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707764"
---
# <a name="cd3dx12_tile_shape-structure"></a>CD3DX12 \_ estructura de forma de mosaico \_

Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ forma de mosaico de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Forma de mosaico CD3DX12 \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ forma de mosaico CD3DX12 \_ .

</dd> <dt>

**forma de mosaico de CD3DX12 explícita \_ \_ ( \_ forma de mosaico const D3D12 \_ &o)**
</dt> <dd>

Crea una nueva instancia de una \_ forma de mosaico CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ forma de mosaico D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .

</dd> <dt>

**\_Forma de mosaico CD3DX12 \_ (uint WIDTHINTEXELS, uint HEIGHTINTEXELS, uint depthInTexels)**
</dt> <dd>

Crea una nueva instancia de una \_ forma de mosaico CD3DX12 \_ , inicializando los siguientes parámetros:

UINT widthInTexels

UINT heightInTexels

UINT depthInTexels

</dd> <dt>

**operador const D3D12 \_ forma de mosaico \_& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Forma de mosaico D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





