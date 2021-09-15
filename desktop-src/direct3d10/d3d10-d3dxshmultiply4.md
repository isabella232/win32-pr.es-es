---
description: Calcula el producto de dos funciones de armónicas esféricas (f y g). Ambas funciones son del orden N = 4.
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
ms.openlocfilehash: 13e8b62674ccbabbb03259f06b79f330424ddf84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474507"
---
# <a name="d3dxshmultiply4-function"></a>Función D3DXSHMultiply4

Calcula el producto de dos funciones de armónicas esféricas (*f* y *g*). Ambas funciones son del orden N = 4.

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

Puntero a los coeficientes sh de salida: la función base *Y* lm se almacena en lmiento + *m* + l. El orden *N* determina la longitud de la matriz, donde siempre debe haber *N* coeficientes mientos.

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

## <a name="remarks"></a>Observaciones

El producto de dos funciones SH del orden N = 4 genera una función SH del orden 2 × *N* - 1 = 7, pero los resultados se truncan. Esto significa que el producto se desplaza *(f* × *g g*× f ) pero no se asocia  =   ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ). 

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

 

 
