---
description: 'Función D3DXMatrixTransformation2D (D3dx9math.h): crea una matriz de transformación 2D que representa las transformaciones en el plano xy. Los argumentos NULL se tratan como transformaciones de identidad.'
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: Función D3DXMatrixTransformation2D (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 754ea3124f5c2433e459331d4ebc7727a9c2519a982d1def09c7e16e794e6ae9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750105"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a>Función D3DXMatrixTransformation2D (D3dx9math.h)

Crea una matriz de transformación 2D que representa las transformaciones en el plano xy. **Los** argumentos NULL se tratan como transformaciones de identidad.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       pScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
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

Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que contiene el resultado de las transformaciones.

</dd> <dt>

*pScalingCenter* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una [**estructura D3DXVECTOR2,**](d3dxvector2.md) un punto que identifica el centro de escalado. Si este argumento es **NULL,** se aplica una matriz <sub>M sc</sub> de identidad a la fórmula en Comentarios.

</dd> <dt>

*pScalingRotation* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

El factor de rotación de escalado.

</dd> <dt>

*pScaling* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una [**estructura D3DXVECTOR2,**](d3dxvector2.md) un punto que identifica la escala. Si este argumento es **NULL,** se aplica una matriz Ms de identidad a la fórmula en Comentarios.

</dd> <dt>

*pRotationCenter* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una [**estructura D3DXVECTOR2,**](d3dxvector2.md) un punto que identifica el centro de rotación. Si este argumento es **NULL,** se aplica una matriz M <sub>rc</sub> de identidad a la fórmula en Comentarios.

</dd> <dt>

*Rotación* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ángulo de rotación en radianes.

</dd> <dt>

*pTranslation* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una [**estructura D3DXVECTOR2,**](d3dxvector2.md) que identifica la traducción. Si este argumento es **NULL,** se aplica una matriz mt de identidad a la fórmula en Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que contiene la matriz de transformación.

## <a name="remarks"></a>Comentarios

Esta función calcula la matriz de transformación con la siguiente fórmula, con la concatenación de matrices evaluada en orden de izquierda a derecha:

M<sub>out</sub> = (M<sub>sc</sub>)/¹ \* (M<sub>sr</sub>)/ntes \* \* Ms M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)/¹ \* M<sub>r</sub> M \* <sub>rc</sub> \* Mt

donde:

M <sub>out</sub> = matriz de salida (*pOut*)

M <sub>sc</sub> = matriz del centro de escalado (*pScalingCenter*)

M <sub>sr</sub> = matriz de rotación de escalado (*pScalingRotation*)

Ms = matriz de escalado (*escalado pScaling*)

M <sub>rc</sub> = centro de la matriz de rotación (*pRotationCenter*)

M <sub>r</sub> = matriz de rotación (*Rotación*)

Mt = matriz de traducción (*pTranslation*)

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la **función D3DXMatrixTransformation2D** se puede usar como parámetro para otra función.

Para las transformaciones 3D, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[Transformaciones (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
