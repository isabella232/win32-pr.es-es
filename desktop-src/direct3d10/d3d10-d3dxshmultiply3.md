---
description: Calcula el producto de dos funciones armónicas esféricas (f y g). Ambas funciones son del orden N = 3.
ms.assetid: 2845f90f-c8a0-4ca9-b2f6-7491a2b4763b
title: Función D3DXSHMultiply3 (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply3
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a04e4979d412a4533b74c7d7610933527c2bdaacb9733b9eb08c6e0ad56e4e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990815"
---
# <a name="d3dxshmultiply3-function"></a>Función D3DXSHMultiply3

Calcula el producto de dos funciones armónicas esféricas *(f* y *g*). Ambas funciones son del orden N = 3.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT* D3DXSHMultiply3(
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

Puntero a los coeficientes SH de salida: la función base *Y* lm se almacena en lntes + *m* + l. El orden *N* determina la longitud de la matriz, donde siempre debe haber *N* coeficientes ntes.

</dd> <dt>

*pF* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Coeficientes SH de entrada para la primera función.

</dd> <dt>

*pG* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Segundo conjunto de coeficientes SH de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a coeficientes de salida sh.

## <a name="remarks"></a>Comentarios

El producto de dos funciones SH del orden N = 3 genera una función SH del orden 2 × *N* - 1 = 5, pero los resultados se truncan. Esto significa que el producto se desplaza ( *f* × *g* g × f ) pero no se asocia  =   ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ). 

Esta función usa la siguiente ecuación:


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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
