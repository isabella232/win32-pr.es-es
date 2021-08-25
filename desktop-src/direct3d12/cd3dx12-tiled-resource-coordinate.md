---
title: CD3DX12_TILED_RESOURCE_COORDINATE estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura D3D12 \_ TILED \_ RESOURCE \_ COORDINATE.
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- CD3DX12_TILED_RESOURCE_COORDINATE estructura
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 784955545fe8e71227ffae6c5eec54acfd65b4a0ab0867f5c7de99a148976861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987855"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a>Estructura DE COORDENADA DE RECURSOS EN MOSAICO CD3DX12 \_ \_ \_

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura D3D12 \_ TILED RESOURCE \_ \_ COORDINATE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**COORDENADA DE RECURSOS \_ EN MOSAICO \_ CD3DX12() \_**
</dt> <dd>

Crea una nueva instancia de CD3DX12 TILED RESOURCE COORDINATE sin \_ \_ \_ inicializar.

</dd> <dt>

**EXPLICIT CD3DX12 \_ TILED \_ RESOURCE \_ COORDINATE(const D3D12 \_ TILED RESOURCE COORDINATE &\_ \_ o)**
</dt> <dd>

Crea una nueva instancia de CD3DX12 TILED RESOURCE COORDINATE, inicializada con el contenido de otra estructura \_ \_ \_ [**D3D12 \_ TILED \_ RESOURCE \_ COORDINATE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)

</dd> <dt>

**CD3DX12 \_ TILED \_ RESOURCE \_ COORDINATE(UINT x, UINT y, UINT z, UINT subresource)**
</dt> <dd>

Crea una nueva instancia de CD3DX12 \_ TILED \_ RESOURCE \_ COORDINATE, inicializando los parámetros siguientes:

UINT x

UINT y

UINT z

Subrecurso de UINT

</dd> <dt>

**operator const D3D12 \_ TILED \_ RESOURCE COORDINATE \_&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COORDENADA DE RECURSOS EN MOSAICO DE D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





