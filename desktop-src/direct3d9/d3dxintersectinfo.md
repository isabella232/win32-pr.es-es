---
description: 'Estructura D3DXINTERSECTINFO: describe una intersección de triángulo de rayo.'
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: Estructura D3DXINTERSECTINFO (D3dx9mesh.h)
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
ms.openlocfilehash: f4a63c7f4a479bfbe9dcb49f485ce0acb8db6486
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969780"
---
# <a name="d3dxintersectinfo-structure"></a>D3DXINTERSECTINFO (estructura)

Describe una intersección de triángulo de rayo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**FaceIndex**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Índice del triángulo que alcanzó el rayo.

</dd> <dt>

**U**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada centrada en barras dentro del triángulo donde el rayo forma intersección.

</dd> <dt>

**V**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada centrada en barras dentro del triángulo donde el rayo forma intersección.

</dd> <dt>

**Dist**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Distancia a lo largo del rayo donde se produjo la intersección.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las coordenadas centradas en barras definen un punto dentro de un triángulo en términos de los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas centradas en barras, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
