---
description: Describe un cuaternión.
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: Estructura D3DXQUATERNION (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 405e48c99d7298708af193016930a8defdf9d600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362665"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a>Estructura D3DXQUATERNION (D3DX10Math. h)

Describe un cuaternión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**x**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente x.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente y.

</dd> <dt>

**z**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente z.

</dd> <dt>

**w**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente w-.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los cuaterniones agregan un cuarto elemento a los \[ valores x, y, z \] que definen un vector, lo que da lugar a vectores 4D arbitrarios. Sin embargo, a continuación se muestra cómo cada elemento de un cuaternión de unidad se relaciona con una rotación de ángulo de eje (donde q representa un cuaternión de unidad (x, y, z, w), se normaliza el eje y Theta es la rotación del CCW deseada sobre el eje):


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
