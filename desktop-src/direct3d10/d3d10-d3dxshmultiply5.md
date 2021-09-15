---
description: Calcula el producto de dos funciones armónicas esféricas (f y g). Ambas funciones son del orden N = 5.
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
ms.openlocfilehash: b43fb89bdd5d6f75a4adca86323786d4a2bddac1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474506"
---
# <a name="d3dxshmultiply5-function"></a>Función D3DXSHMultiply5

Calcula el producto de dos funciones armónicas esféricas (f y g). Ambas funciones son del orden N = 5.

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

Puntero a los coeficientes SH de salida: la función base *Y* lm se almacena en *l* miento + *m* + l. El orden N determina la longitud de la matriz, donde siempre debe haber *N* coeficientes ntes.

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

## <a name="remarks"></a>Observaciones

El producto de dos funciones SH del orden N = 5 genera una función SH del orden 2 × *N* - 1 = 9, pero los resultados se truncan. Esto significa que el producto conmuta ( *f* × *g g*× f ) pero no asocia (  =   *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ). 

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

 

 
