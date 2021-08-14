---
title: CD3DX12_TILE_SHAPE estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura TILE SHAPE de D3D12. \_ \_
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- CD3DX12_TILE_SHAPE estructura
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
ms.openlocfilehash: 0b02f699ab06ef93f3eeace3ce515b0947030e4824e2cb0fa51034c3e33f51dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987875"
---
# <a name="cd3dx12_tile_shape-structure"></a>Estructura TILE SHAPE de CD3DX12 \_ \_

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ TILE \_ SHAPE de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)

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

**FORMA DE MOSAICO CD3DX12() \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de una FORMA DE MOSAICO CD3DX12. \_ \_

</dd> <dt>

**explicit CD3DX12 \_ TILE \_ SHAPE(const D3D12 \_ TILE SHAPE &\_ o)**
</dt> <dd>

Crea una nueva instancia de UNA FORMA DE MOSAICO CD3DX12, inicializada con el contenido de otra estructura \_ \_ TILE [**\_ \_ SHAPE de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)

</dd> <dt>

**CD3DX12 \_ TILE \_ SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels)**
</dt> <dd>

Crea una nueva instancia de UN OBJETO TILE SHAPE de CD3DX12, \_ \_ inicializando los parámetros siguientes:

Ancho de UINTInTexels

Alto de UINTInTexels

Profundidad de UINTInTexels

</dd> <dt>

**operator const D3D12 \_ TILE \_ SHAPE&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FORMA DE MOSAICO D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





