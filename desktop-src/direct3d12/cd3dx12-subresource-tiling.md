---
title: CD3DX12_SUBRESOURCE_TILING estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura \_ DE TILING DE SUBCURSOS D3D12. \_
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- CD3DX12_SUBRESOURCE_TILING estructura
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36a0625b2389783ea4dafa65930e3095329e5bf5e2cfd4c57813e5251f81b88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987985"
---
# <a name="cd3dx12_subresource_tiling-structure"></a>Estructura DE \_ TILING DE SUBCURSOS CD3DX12 \_

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**\_ DE TILING DE \_ SUBCURSOS D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**TILING DE \_ SUBRECURSOS \_ CD3DX12()**
</dt> <dd>

Crea una nueva instancia sin inicializar de UN \_ TILING DE SUBCURSOS CD3DX12. \_

</dd> <dt>

**EXPLICIT CD3DX12 \_ SUBRESOURCE \_ TILING(const D3D12 \_ SUBRESOURCE \_ TILING &o)**
</dt> <dd>

Crea una nueva instancia de UN TILING DE SUBCURSOS CD3DX12, inicializado con el contenido de otra estructura \_ \_ DE [**\_ \_ TILING de SUBRESOURCE de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource)**
</dt> <dd>

Crea una nueva instancia de UN TILING DE SUBCURSOS CD3DX12, \_ \_ inicializando los parámetros siguientes:

UINT widthInTiles

UINT16 heightInTiles

Profundidad de UINT16InTiles

UINT startTileIndexInOverallResource

</dd> <dt>

**operator const D3D12 \_ SUBRESOURCE \_ TILING&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ETIQUETADO DE SUBRECURSOS D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





