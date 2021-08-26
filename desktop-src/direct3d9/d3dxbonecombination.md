---
description: Describe un subconjunto de la malla que tiene el mismo atributo y combinación de teclas.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: Estructura D3DXCORECOMBINATION (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 72d60b5c87d43763be4700ba7931c61c41cf0101d80390afb737c7f4afda83a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952495"
---
# <a name="d3dxbonecombination-structure"></a>D3DXDXCOMBINATION (estructura)

Describe un subconjunto de la malla que tiene el mismo atributo y combinación de teclas.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**AttribId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador de tabla de atributos.

</dd> <dt>

**FaceStart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Cara inicial.

</dd> <dt>

**FaceCount**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Recuento de caras.

</dd> <dt>

**VertexStart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Vértice inicial.

</dd> <dt>

**VertexCount**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Recuento de vértices.

</dd> <dt>

**Id Desaeso**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Puntero a una matriz de valores que identifican cada uno de los esqueletos que se pueden dibujar en una sola llamada de dibujo. Tenga en cuenta que la matriz puede ser de longitud variable para dar cabida a combinaciones de longitud variable de [**ConvertToIndexedBlendedMesh.**](id3dxskininfo--converttoindexedblendedmesh.md)

El tamaño de la matriz varía en función del tipo de malla generada. Un tamaño de matriz de malla no indexada es igual al número de pesos por vértice (pMaxVertexInfl en [**ConvertToBlendedMesh).**](id3dxskininfo--converttoblendedmesh.md) El tamaño de una matriz de malla indizada es igual al número de entradas de la paleta de matrices de matriz (paletteSize en [**ConvertToIndexedBlendedMesh).**](id3dxskininfo--converttoindexedblendedmesh.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

El subconjunto de la malla descrito por **D3DXPXCOMBINATION** se puede representar en una sola llamada de dibujo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
