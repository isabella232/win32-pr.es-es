---
title: CD3DX12_SUBRESOURCE_TILING estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de mosaico de Subrecursos de D3D12 \_ .
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- Estructura de CD3DX12_SUBRESOURCE_TILING
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
ms.openlocfilehash: 07677c8a8367f58016a0236cf0b5558b852bef01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717593"
---
# <a name="cd3dx12_subresource_tiling-structure"></a>CD3DX12 \_ estructura de mosaico de SUBrecursos \_

Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ mosaico de Subrecursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .

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

**\_Mosaico de SUBrecursos de CD3DX12 \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ mosaico de Subrecursos de CD3DX12 \_ .

</dd> <dt>

**mosaico de Subrecursos CD3DX12 explícito \_ \_ (const D3D12 \_ subresource \_ mosaico &o)**
</dt> <dd>

Crea una nueva instancia de un \_ mosaico de SUBrecursos de CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ mosaicos de Subrecursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .

</dd> <dt>

**\_Mosaico de SUBrecursos de CD3DX12 \_ (uint WIDTHINTILES, UINT16 HEIGHTINTILES, UINT16 DEPTHINTILES, uint startTileIndexInOverallResource)**
</dt> <dd>

Crea una nueva instancia de un \_ mosaico de Subrecursos de CD3DX12 \_ , inicializando los siguientes parámetros:

UINT widthInTiles

UINT16 heightInTiles

UINT16 depthInTiles

UINT startTileIndexInOverallResource

</dd> <dt>

**operador const D3D12 \_ subresource \_ mosaico& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Mosaico de SUBrecursos de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





