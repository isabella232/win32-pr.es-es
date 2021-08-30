---
description: Crea una matriz de transformación afín 2D en el plano xy. Los argumentos NULL se tratan como transformaciones de identidad.
ms.assetid: 335de919-ae4d-405d-b6bb-ca6bdc2d568a
title: Función D3DXMatrixAffineTransformation2D (D3dx9math.h)
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
ms.openlocfilehash: d5f891a4e6e745fe2a6e215f3dd126c5b0faa11ba39b49ff2404c79c0cc12528
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119165"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx9mathh"></a>Función D3DXMatrixAffineTransformation2D (D3dx9math.h)

Crea una matriz de transformación afín 2D en el plano xy. **Los** argumentos NULL se tratan como transformaciones de identidad.

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

Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*Escalado* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Factor de escalado.

</dd> <dt>

*pRotationCenter* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una [**estructura D3DXVECTOR2,**](d3dxvector2.md) un punto que identifica el centro de rotación. Si este argumento es **NULL,** se aplica una matriz M <sub>rc</sub> de identidad a la fórmula en Comentarios.

</dd> <dt>

*Rotación* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ángulo de rotación.

</dd> <dt>

*pTranslation* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una [**estructura D3DXVECTOR2,**](d3dxvector2.md) que representa la traducción. Si este argumento es **NULL,** se aplica una matriz mt de identidad a la fórmula en Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es una matriz de transformación afín.

## <a name="remarks"></a>Comentarios

Esta función calcula la matriz de transformación afín con la siguiente fórmula, con la concatenación de matrices evaluada en orden de izquierda a derecha:

M<sub>out</sub> = Ms \* (M<sub>rc</sub>)/¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

donde:

M <sub>out</sub> = matriz de salida (*pOut*)

Ms = matriz de escalado (*Escalado*)

M <sub>rc</sub> = centro de la matriz de rotación (*pRotationCenter*)

M <sub>r</sub> = matriz de rotación (*Rotación*)

Mt = matriz de traducción (*pTranslation*)

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De este modo, la función **D3DXMatrixAffineTransformation2D** se puede usar como parámetro para otra función.

Para las transformaciones de afín 3D, use [**D3DXMatrixAffineTransformation.**](d3dxmatrixaffinetransformation.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md)
</dt> <dt>

[Transformaciones (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
