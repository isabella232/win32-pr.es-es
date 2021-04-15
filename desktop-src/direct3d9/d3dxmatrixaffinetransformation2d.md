---
description: Crea una matriz de transformación afín 2D en el plano XY. Los argumentos NULL se tratan como transformaciones de identidad.
ms.assetid: 335de919-ae4d-405d-b6bb-ca6bdc2d568a
title: Función D3DXMatrixAffineTransformation2D (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6edd0658eb80ec53d19b6c136a672cb78a2087b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707837"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx9mathh"></a>Función D3DXMatrixAffineTransformation2D (D3dx9math. h)

Crea una matriz de transformación afín 2D en el plano XY. Los argumentos **null** se tratan como transformaciones de identidad.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_          FLOAT       Scaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*Escalado* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de escala.

</dd> <dt>

*pRotationCenter* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) , un punto que identifica el centro de rotación. Si este argumento es **null**, se aplica una matriz identidad M <sub>RC</sub> a la fórmula en la sección Comentarios.

</dd> <dt>

*Giro* \[ de de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Ángulo de rotación.

</dd> <dt>

*pTranslation* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) que representa la traslación. Si este argumento es **null**, se aplica una matriz Identity MT a la fórmula en la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que es una matriz de transformación afín.

## <a name="remarks"></a>Observaciones

Esta función calcula la matriz de transformación afín con la fórmula siguiente, con la concatenación de matriz evaluada en orden de izquierda a derecha:

M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT

donde:

M <sub>out</sub> = matriz de salida (*pOut*)

MS = matriz de escalado (*escala*)

M <sub>RC</sub> = centro de la matriz de rotación (*pRotationCenter*)

M <sub>r</sub> = matriz de rotación (*giro*)

MT = matriz de traslación (*pTranslation*)

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut. De esta manera, la función **D3DXMatrixAffineTransformation2D** se puede usar como parámetro de otra función.

En el caso de las transformaciones afines 3D, use [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md)
</dt> <dt>

[Transformaciones (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
