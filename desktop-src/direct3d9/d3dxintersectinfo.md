---
description: Describe una intersección de triángulo.
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: Estructura D3DXINTERSECTINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINTERSECTINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 31a98e9a7095e81e962b2996dedb9bdf5871533d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707878"
---
# <a name="d3dxintersectinfo-structure"></a>Estructura D3DXINTERSECTINFO

Describe una intersección de triángulo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**FaceIndex**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Índice del triángulo que ha alcanzado el rayo.

</dd> <dt>

**U**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada de Barycentric dentro del triángulo en el que se corta el rayo.

</dd> <dt>

**V**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada de Barycentric dentro del triángulo en el que se corta el rayo.

</dd> <dt>

**Tribu**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Distancia a lo largo del rayo en el que se produjo la intersección.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
