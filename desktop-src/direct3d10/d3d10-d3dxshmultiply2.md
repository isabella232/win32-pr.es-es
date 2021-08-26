---
description: Calcula el producto de dos funciones de armónicas esféricas (f y g). Ambas funciones son del orden N = 2.
ms.assetid: 9e0942ce-e39d-4147-9472-cda8a97fd390
title: Función D3DXSHMultiply2 (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c6fba685a763a00e529e70b7c0f08a97706f3c5f2be4dba7c923ed5b4b102742
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070005"
---
# <a name="d3dxshmultiply2-function-d3dx10mathh"></a>Función D3DXSHMultiply2 (D3DX10Math.h)

Calcula el producto de dos funciones de armónicas esféricas (*f* y *g*). Ambas funciones son del orden N = 2.

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

Puntero a los coeficientes sh de salida: la función base *Y* lm se almacena en lntes + *m* + l. El orden *N* determina la longitud de la matriz, donde siempre debe haber *N* coeficientes mientos.

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

El producto de dos funciones SH del orden N = 2 genera una función SH del orden 2 × *N* - 1 = 3, pero los resultados se truncan. Esto significa que el producto se desplaza ( *f* × *g* g × f ) pero no se asocia  =   ( *f* × (*g* × *h*) ≠ ( *f* × *g*) × *h* ). 

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

 

 
