---
description: 'Función D3DXMatrixReflect (D3dx9math.h): crea una matriz que refleja el sistema de coordenadas sobre un plano.'
ms.assetid: f6dc3834-42f2-4ad0-8098-8c5e25e10d58
title: Función D3DXMatrixReflect (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixReflect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4118a5f0a1cd997d5fab5fecebae449d4c30b09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060724"
---
# <a name="d3dxmatrixreflect-function-d3dx9mathh"></a>Función D3DXMatrixReflect (D3dx9math.h)

Crea una matriz que refleja el sistema de coordenadas sobre un plano.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*pPlane* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntero a la estructura [**D3DXPLANE de**](d3dxplane.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que refleja el sistema de coordenadas sobre el plano de origen.

## <a name="remarks"></a>Observaciones

Esta función normaliza la ecuación del plano antes de crear la matriz reflejada.

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De este modo, la **función D3DXMatrixReflect** se puede usar como parámetro para otra función.

Esta función usa la siguiente fórmula para calcular la matriz devuelta.


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




