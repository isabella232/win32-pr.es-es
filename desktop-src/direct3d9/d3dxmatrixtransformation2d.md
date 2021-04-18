---
description: Crea una matriz de transformación 2D que representa las transformaciones en el plano XY. Los argumentos NULL se tratan como transformaciones de identidad.
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: Función D3DXMatrixTransformation2D (D3dx9math. h)
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
ms.openlocfilehash: ead4d403917b5328776b33563bc477c28983d6ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717753"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a>Función D3DXMatrixTransformation2D (D3dx9math. h)

Crea una matriz de transformación 2D que representa las transformaciones en el plano XY. Los argumentos **null** se tratan como transformaciones de identidad.

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

Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que contiene el resultado de las transformaciones.

</dd> <dt>

*pScalingCenter* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) , un punto que identifica el centro de escalado. Si este argumento es **null**, se aplica una matriz identidad M <sub>SC</sub> a la fórmula en la sección Comentarios.

</dd> <dt>

*pScalingRotation* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de rotación de escala.

</dd> <dt>

*pScaling* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) , un punto que identifica la escala. Si este argumento es **null**, se aplica una matriz de identidad MS a la fórmula en la sección Comentarios.

</dd> <dt>

*pRotationCenter* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) , un punto que identifica el centro de rotación. Si este argumento es **null**, se aplica una matriz identidad M <sub>RC</sub> a la fórmula en la sección Comentarios.

</dd> <dt>

*Giro* \[ de de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Ángulo de rotación en radianes.

</dd> <dt>

*pTranslation* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) , que identifica la traducción. Si este argumento es **null**, se aplica una matriz Identity MT a la fórmula en la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que contiene la matriz de transformación.

## <a name="remarks"></a>Observaciones

Esta función calcula la matriz de transformación con la fórmula siguiente, con la concatenación de matriz evaluada en orden de izquierda a derecha:

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>Sr</sub>) ⁻ ¹ \* MS \* m<sub>Sr</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* M<sub>RC</sub> \* MT

donde:

M <sub>out</sub> = matriz de salida (*pOut*)

M <sub>SC</sub> = matriz de centro de escalado (*pScalingCenter*)

M <sub>Sr</sub> = matriz de rotación de escala (*pScalingRotation*)

MS = matriz de escalado (*pScaling*)

M <sub>RC</sub> = centro de la matriz de rotación (*pRotationCenter*)

M <sub>r</sub> = matriz de rotación (*giro*)

MT = matriz de traslación (*pTranslation*)

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut. De esta manera, la función **D3DXMatrixTransformation2D** se puede usar como parámetro de otra función.

Para las transformaciones 3D, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[Transformaciones (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
