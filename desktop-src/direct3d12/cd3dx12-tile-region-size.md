---
title: CD3DX12_TILE_REGION_SIZE estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura TILE REGION SIZE de D3D12. \_ \_ \_
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- CD3DX12_TILE_REGION_SIZE estructura
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
ms.openlocfilehash: 9cc1b96ae4d7d33101068a1ba08f0314b99950146e91a352ab49fea714376471
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119615"
---
# <a name="cd3dx12_tile_region_size-structure"></a>Estructura DE TAMAÑO DE REGIÓN DE MOSAICO CD3DX12 \_ \_ \_

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**\_ TILE REGION SIZE \_ \_ de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)

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

**CD3DX12 \_ TILE \_ REGION \_ SIZE()**
</dt> <dd>

Crea una nueva instancia sin inicializar de UN TAMAÑO DE REGIÓN DE MOSAICO CD3DX12. \_ \_ \_

</dd> <dt>

**explicit CD3DX12 \_ TILE \_ REGION \_ SIZE(const D3D12 \_ TILE REGION SIZE &\_ \_ o)**
</dt> <dd>

Crea una nueva instancia de UN CD3DX12 TILE REGION SIZE, inicializado con el contenido de otra estructura \_ \_ TILE REGION SIZE \_ [**\_ \_ \_ de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)

</dd> <dt>

**CD3DX12 \_ TILE \_ REGION \_ SIZE(UINT numTiles, BOOL useBox, ancho UINT, alto UINT16, profundidad UINT16)**
</dt> <dd>

Crea una nueva instancia de UN TAMAÑO DE REGIÓN DE MOSAICO CD3DX12, \_ \_ \_ inicializando los parámetros siguientes:

UINT numTiles

BOOL useBox

Ancho de UINT

Alto de UINT16

Profundidad UINT16

</dd> <dt>

**operator const D3D12 \_ TILE \_ REGION SIZE \_&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TAMAÑO DE LA REGIÓN DEL ICONO D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





