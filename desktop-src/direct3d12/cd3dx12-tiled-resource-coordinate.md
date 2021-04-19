---
title: CD3DX12_TILED_RESOURCE_COORDINATE estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una estructura de coordenadas de recursos en mosaico de D3D12 \_ \_ \_ .
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- Estructura de CD3DX12_TILED_RESOURCE_COORDINATE
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
ms.openlocfilehash: 281afeab8d1172e9cae749512612129dd001161b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707760"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a>CD3DX12 \_ estructura de \_ coordenadas de recursos en mosaico \_

Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**coordenadas de recursos en mosaico de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .

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

**CD3DX12 \_ \_ coordenada de recursos en mosaico \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ coordenada de recursos en mosaico de CD3DX12 \_ \_ .

</dd> <dt>

**coordenada de recursos en mosaico de CD3DX12 explícita \_ \_ \_ (const D3D12 \_ \_ coordenada de recursos en mosaico \_ &o)**
</dt> <dd>

Crea una nueva instancia de una \_ \_ coordenada de recursos \_ en mosaico CD3DX12, inicializada con el contenido de otra estructura de [**coordenadas de \_ recursos en mosaico \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .

</dd> <dt>

**CD3DX12 \_ \_ coordenada de recursos en mosaico \_ (UINT x, UINT y, UINT z, uint subresource)**
</dt> <dd>

Crea una nueva instancia de una \_ coordenada de recursos en mosaico CD3DX12 \_ \_ , inicializando los parámetros siguientes:

UINT x

UINT y

UINT z

Subrecurso UINT

</dd> <dt>

**operador const D3D12 \_ \_ coordenada de recursos en mosaico \_& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ \_ coordenada de recursos en mosaico \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





