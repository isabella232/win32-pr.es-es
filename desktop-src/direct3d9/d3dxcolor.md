---
description: Describe los valores de color.
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: Estructura D3DXCOLOR (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: c7e5c1ac12341ccf6272714511959ee9a131ba4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678817"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a>Estructura D3DXCOLOR (D3dx9math. h)

Describe los valores de color.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a>Miembros

<dl> <dt>

**r**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente rojo del color.

</dd> <dt>

**g**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente verde del color.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente azul del color.

</dd> <dt>

**un**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente alfa del color.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los programadores de C++ pueden aprovechar las ventajas de la sobrecarga de operadores y la conversión de tipos con las [**extensiones de D3DXCOLOR**](d3dxcolor-extensions.md), que implementan constructores sobrecargados, así como operadores de asignación, unario y binario (incluida la igualdad).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
