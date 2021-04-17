---
description: Describe un plano.
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: Estructura D3DXPLANE (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717557"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a>Estructura D3DXPLANE (D3dx9math. h)

Describe un plano.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**un**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Un coeficiente del plano de recorte en la ecuación de plano general. Vea la sección Comentarios.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

El coeficiente b del plano de recorte en la ecuación de plano general. Vea la sección Comentarios.

</dd> <dt>

**c**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coeficiente c del plano de recorte en la ecuación de plano general. Vea la sección Comentarios.

</dd> <dt>

**d**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coeficiente d del plano de recorte en la ecuación de plano general. Vea la sección Comentarios.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los miembros de la estructura **D3DXPLANE** adoptan la forma de la ecuación de plano general. Se ajustan a la ecuación de plano general **para que x**+ **b** y + **c** z + **d** w = 0.

Los programadores de C++ pueden aprovechar las ventajas de la sobrecarga de operadores y la conversión de tipos con las [**extensiones de D3DXPLANE**](d3dxplane-extensions.md) que implementan constructores sobrecargados y operadores de asignación, unario y binario (incluida la igualdad).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
