---
description: Calcula el producto de dos funciones representadas mediante SH (f y g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: Función D3DXSHMultiply2 (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 00219ed1c38105562591b63e6bef64b949b2ab4443aed68e0e6b9d64cb156cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849695"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a>Función D3DXSHMultiply2 (D3dx9math.h)

Calcula el producto de dos funciones representadas mediante SH (f y g).

## <a name="syntax"></a>Sintaxis


```C++
FLOAT* D3DXSHMultiply2(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a los coeficientes sh de salida: la función base Ylm se almacena en l \* l + m+l.

</dd> <dt>

*pF* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Coeffs sh de entrada para la primera función.

</dd> <dt>

*pG* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Segundo conjunto de coeffs sh de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a coeficientes de salida sh.

## <a name="remarks"></a>Comentarios

El pedido es un número entre 2 y 6 inclusive. Por lo tanto, esta página realmente documenta varias funciones: D3DXSHMultiply2, D3DXSHMultiply3, ... D3DXSHMultiply6.

Calcula el producto de dos funciones representadas mediante SH (f y g), donde *pOut* \[ i = \] int(y \_ i(s) \* f(s) g(s)), donde y i(s) es la función base de \* \_ ith SH, f(s) y g(s) son funciones SH (sum \_ i(y \_ i(s) \* c \_ i)). El orden O determina las longitudes de las matrices, donde siempre debe haber coeficientes de O^2. En general, el producto de dos funciones SH del orden O genera una función SH del orden 2 O a 1, pero los resultados \* se truncan. Esto significa que el producto se desplaza (f g == g f) pero no asocia \* \* (f \* (g \* h) != (f \* g) \* h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
