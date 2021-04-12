---
description: Calcula el producto de dos funciones de armónicos esféricos (f y g). Ambas funciones son del orden N = 5.
ms.assetid: c72231a1-9db3-4701-b7ad-4509028ce508
title: Función D3DXSHMultiply5 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply5
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b43fb89bdd5d6f75a4adca86323786d4a2bddac1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362714"
---
# <a name="d3dxshmultiply5-function"></a>D3DXSHMultiply5 función)

Calcula el producto de dos funciones de armónicos esféricos (f y g). Ambas funciones son del orden N = 5.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT* D3DXSHMultiply5(
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

Puntero a los coeficientes SH de salida: la función base *Y* LM se almacenan en *l*² + *m* + l. El orden N determina la longitud de la matriz, donde siempre debe haber un coeficiente de *N*².

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

El producto de dos funciones SH de order N = 5 genera una función SH de order 2 × *N* -1 = 9, pero los resultados se truncan. Esto significa que el producto se desactivará ( *f* × *g*  =  *g* × *f* ), pero no se asocia ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).

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

 

 
