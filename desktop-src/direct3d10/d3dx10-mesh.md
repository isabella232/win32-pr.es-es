---
description: 'D3DX10_MESH enumeración: marcas usadas para especificar opciones de creación para una malla.'
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: D3DX10_MESH enumeración (D3DX10Mesh.h)
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
ms.openlocfilehash: 2659783b0443396508465f9498eec86950f825bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105443"
---
# <a name="d3dx10_mesh-enumeration"></a>D3DX10 \_ MESH (enumeración)

Marcas usadas para especificar opciones de creación para una malla.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ MESH \_ DE 32 \_ BITS**
</dt> <dd>

La malla tiene índices de 32 bits en lugar de índices de 16 bits. Vea la sección Comentarios.

</dd> <dt>

<span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**ADYACENCIA \_ DE \_ GS DE D3DX10 MESH \_**
</dt> <dd>

Indica que la malla contiene datos de adyacencia del sombreador de geometría.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una malla de 32 bits (D3DXMESH de 32 BITS) puede admitir teóricamente \_ (2):1 caras y vértices. Sin embargo, no es práctico asignar memoria para una malla que sea grande en un sistema operativo de 32 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Mesh.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




