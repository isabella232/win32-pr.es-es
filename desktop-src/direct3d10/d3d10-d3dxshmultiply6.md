---
description: Calcula el producto de dos funciones de armónicos esféricos (f y g). Ambas funciones son del orden N = 6.
ms.assetid: 3b68b238-c1ae-4ab8-89ed-bdf815463143
title: Función D3DXSHMultiply6 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply6
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0768bb8be1f2f23693a431a2c0ea8f3d5a6846d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649433"
---
# <a name="d3dxshmultiply6-function"></a>D3DXSHMultiply6 función)

Calcula el producto de dos funciones de armónicos esféricos (f y g). Ambas funciones son del orden N = 6.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT* D3DXSHMultiply6(
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

Puntero a los coeficientes SH de salida: la función base *Y* LM se almacenan en l ² + *m* + l. El orden *N* determina la longitud de la matriz, donde siempre debe haber un coeficiente de *N*².

</dd> <dt>

*PF* \[ de\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Los coeficientes SH de entrada para la primera función.

</dd> <dt>

*PG* \[ de\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Segundo conjunto de coeficientes SH de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a los coeficientes de salida SH.

## <a name="remarks"></a>Observaciones

El producto de dos funciones SH de order N = 6 genera una función SH de order 2 × *N* -1 = 11, pero los resultados se truncan. Esto significa que el producto se desactivará ( *f* × *g*  =  *g* × *f* ), pero no se asocia ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).

Esta función usa la siguiente ecuación:


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



donde y \_ son las funciones de base de l l, donde f (s) y g (s) usan la siguiente función SH:


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
