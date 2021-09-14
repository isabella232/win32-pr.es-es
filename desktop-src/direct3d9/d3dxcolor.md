---
description: 'Estructura D3DXCOLOR (D3dx9math.h): describe los valores de color.'
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: Estructura D3DXCOLOR (D3dx9math.h)
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
ms.openlocfilehash: 58b02abc49b695169674a2579b73dc2359801a73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174810"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a>Estructura D3DXCOLOR (D3dx9math.h)

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



## <a name="members"></a>Members

<dl> <dt>

**r**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente rojo del color.

</dd> <dt>

**g**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente verde del color.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente azul del color.

</dd> <dt>

**Un**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente alfa del color.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los programadores de C++ pueden aprovechar la sobrecarga de operadores y la conversión de tipos con las extensiones [**D3DXCOLOR**](d3dxcolor-extensions.md), que implementan constructores sobrecargados, así como operadores de asignación, unario y binario (incluida la igualdad).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
