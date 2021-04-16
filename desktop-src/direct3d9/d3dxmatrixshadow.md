---
description: Crea una matriz que alisa la geometría en un plano.
ms.assetid: 8f283ff9-c879-476c-8057-f4fe77a7a9e7
title: Función D3DXMatrixShadow (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6bf1639adb7364536cce5c0dead9ef58ae10bea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689886"
---
# <a name="d3dxmatrixshadow-function-d3dx9mathh"></a>Función D3DXMatrixShadow (D3dx9math. h)

Crea una matriz que alisa la geometría en un plano.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*pLight* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que describe la posición de la luz.

</dd> <dt>

*pPlane* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntero a la estructura de [**D3DXPLANE**](d3dxplane.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que alisa la geometría en un plano.

## <a name="remarks"></a>Observaciones

La función **D3DXMatrixShadow** reduce la geometría en un plano, como si se convirtiendo una sombra de una luz.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXMatrixShadow** se puede usar como parámetro de otra función.

Esta función usa la fórmula siguiente para calcular la matriz devuelta.


```
P = normalize(Plane);
L = Light;
d = -dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



Si el componente w-Light es 0, el rayo desde el origen a la luz representa una luz direccional. Si es 1, la luz es una luz puntual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




