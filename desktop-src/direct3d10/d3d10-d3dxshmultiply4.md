---
description: Calcula el producto de dos funciones armónicas esféricas (f y g). Ambas funciones son del orden N = 4.
ms.assetid: 05427a18-447e-45d7-a851-e580298c9a1f
title: Función D3DXSHMultiply4 (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply4
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 78305930eb76b3632737c10482768b9db363deae84f14cf5b73f962d265de2a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990015"
---
# <a name="d3dxshmultiply4-function"></a>Función D3DXSHMultiply4

Calcula el producto de dos funciones armónicas esféricas *(f* y *g*). Ambas funciones son del orden N = 4.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT* D3DXSHMultiply4(
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

El producto de dos funciones SH del orden N = 4 genera una función SH del orden 2 × *N* - 1 = 7, pero los resultados se truncan. Esto significa que el producto se desplaza ( *f* × *g* g × f ) pero no se asocia  =   ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ). 

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
