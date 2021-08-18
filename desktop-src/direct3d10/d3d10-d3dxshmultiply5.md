---
description: Calcula el producto de dos funciones de armónicas esféricas (f y g). Ambas funciones tienen el orden N = 5.
ms.assetid: c72231a1-9db3-4701-b7ad-4509028ce508
title: Función D3DXSHMultiply5 (D3DX10Math.h)
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
ms.openlocfilehash: a022fa883a1b1e809f965ec94813741a285447e9f6935c1adca370b5aef6c061
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990775"
---
# <a name="d3dxshmultiply5-function"></a>Función D3DXSHMultiply5

Calcula el producto de dos funciones de armónicas esféricas (f y g). Ambas funciones tienen el orden N = 5.

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

*pOut* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a los coeficientes sh de salida: la función base *Y* lm se almacena en *l* ntes + *m* + l. El orden N determina la longitud de la matriz, donde siempre debe haber *N* coeficientes mientos.

</dd> <dt>

*pF* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Coeficientes sh de entrada para la primera función.

</dd> <dt>

*pG* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Segundo conjunto de coeficientes sh de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a coeficientes de salida sh.

## <a name="remarks"></a>Comentarios

El producto de dos funciones SH del orden N = 5 genera una función SH del orden 2 × *N* - 1 = 9, pero los resultados se truncan. Esto significa que el producto se desplaza ( *f* × *g* g × f ) pero no se asocia  =   ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ). 

Esta función usa la ecuación siguiente:


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



donde y i(s) es la función base de ith SH y donde \_ f(s) y g(s) usan la siguiente función SH:


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
