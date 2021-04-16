---
description: Marcas que se usan para especificar las opciones de creación de una malla.
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: Enumeración D3DX10_MESH (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: c2387024512a42c0a9e06ac1818b0282121cd0eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678845"
---
# <a name="d3dx10_mesh-enumeration"></a>\_Enumeración de malla D3DX10

Marcas que se usan para especificar las opciones de creación de una malla.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ MESH \_ 32 \_ bits**
</dt> <dd>

La malla tiene índices de 32 bits en lugar de índices de 16 bits. Vea la sección Comentarios.

</dd> <dt>

<span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**Adyacencia de D3DX10 \_ mesh \_ GS \_**
</dt> <dd>

Indica que la malla contiene datos de adyacencia del sombreador de geometría.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una malla de 32 bits (D3DXMESH \_ 32 bits) puede admitir teóricamente (2 ³ ²)-1 caras y vértices. Sin embargo, la asignación de memoria para una malla que es grande en un sistema operativo de 32 bits no es práctica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




