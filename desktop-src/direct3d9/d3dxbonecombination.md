---
description: Describe un subconjunto de la malla que tiene la misma combinación de atributo y hueso.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: Estructura D3DXBONECOMBINATION (D3dx9mesh. h)
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
ms.openlocfilehash: 3553ba37d0d9376fa5912143fb58849f03c5a83a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083743"
---
# <a name="d3dxbonecombination-structure"></a>Estructura D3DXBONECOMBINATION

Describe un subconjunto de la malla que tiene la misma combinación de atributo y hueso.

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

Identificador de la tabla de atributos.

</dd> <dt>

**FaceStart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Superficie inicial.

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

**BoneId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Puntero a una matriz de valores que identifican cada uno de los huesos que se pueden dibujar en una sola llamada de dibujo. Tenga en cuenta que la matriz puede ser de longitud variable para dar cabida a las combinaciones de longitud variable de [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).

El tamaño de la matriz varía en función del tipo de malla generado. Un tamaño de matriz de malla sin indexar es igual al número de pesos por vértice (pMaxVertexInfl en [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)). Un tamaño de matriz de malla indizada es igual al número de entradas de la paleta de la matriz de huesos (paletteSize en [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El subconjunto de la malla descrito por **D3DXBONECOMBINATION** se puede representar en una sola llamada de dibujo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
