---
description: Calcula el producto de dos funciones representadas mediante SH (f y g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: Función D3DXSHMultiply2 (D3dx9math. h)
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
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717704"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a>Función D3DXSHMultiply2 (D3dx9math. h)

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

*pOut* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a la función YLM de los coeficientes de SH de salida se almacena en l \* l + m + l.

</dd> <dt>

*PF* \[ de\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Entrada SH coeffs para la primera función.

</dd> <dt>

*PG* \[ de\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Segundo conjunto de entrada SH coeffs.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a los coeficientes de salida SH.

## <a name="remarks"></a>Observaciones

El orden es un número entre 2 y 6, ambos inclusive. Por lo tanto, esta página documenta varias funciones: D3DXSHMultiply2, D3DXSHMultiply3,... D3DXSHMultiply6.

Calcula el producto de dos funciones representadas mediante SH (f y g), donde *pOut* \[ i \] = int (y \_ i (s) g (s) \* \* ), donde y \_ i es la función i + d, f (s) y g (s) son funciones SH (SUM \_ i (y \_ i) \* \_ ). El orden O determina las longitudes de las matrices, donde siempre debe haber coeficientes O ^ 2. En general, el producto de dos funciones SH de order O genera una función SH de orden 2 \* O-1, pero los resultados se truncan. Esto significa que el producto se desactivará (f \* g = = g \* f), pero no se asocia (f \* (g \* h)! = (f \* g) \* h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
