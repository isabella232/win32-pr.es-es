---
description: 'Estructura D3DXQUATERNION (D3dx9math.h): describe un cuaternión.'
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: Estructura D3DXQUATERNION (D3dx9math.h)
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
- d3dx9math.h
ms.openlocfilehash: 9818772163d5286d764c0f025b955a663457dd853c2db0efec8ad0b0a4967c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524617"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a>Estructura D3DXQUATERNION (D3dx9math.h)

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

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente x.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente Y.

</dd> <dt>

**Z**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente z.

</dd> <dt>

**w**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

W-component.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los cuaterniones agregan un cuarto elemento a los valores x, y, z que definen un vector, lo que da lugar \[ \] a vectores 4D arbitrarios. Sin embargo, a continuación se muestra cómo cada elemento de un cuaternión de unidad se relaciona con una rotación de ángulo de eje (donde q representa un cuaternión de unidad (x, y, z, w), el eje se normaliza y theta es la rotación ccW deseada sobre el eje):


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



Los programadores de C++ pueden aprovechar la sobrecarga de operadores y la conversión de tipos con las extensiones [**D3DXQUATERNION**](d3dxquaternion-extensions.md), que implementan constructores sobrecargados y operadores de asignación, unario y binario (incluida la igualdad).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[Vectores, vértices y cuaterniones (Direct3D 9)](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
