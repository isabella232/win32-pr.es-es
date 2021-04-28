---
description: 'Función D3DXMatrixTransformation2D (D3DX10Math.h): crea una matriz de transformación 2D que representa las transformaciones en el plano xy. Los argumentos NULL se tratan como transformaciones de identidad.'
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: Función D3DXMatrixTransformation2D (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4ef112c346fd222f5e25935740e47ab62273628f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103363"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a>Función D3DXMatrixTransformation2D (D3DX10Math.h)

Crea una matriz de transformación 2D que representa las transformaciones en el plano xy. **Los** argumentos NULL se tratan como transformaciones de identidad.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       ScalingRotation,
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

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que contiene el resultado de las transformaciones.

</dd> <dt>

*pScalingCenter* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntero a [**D3DXVECTOR2,**](d3d10-d3dxvector2.md)un punto que identifica el centro de escalado. Si este argumento es **NULL,** se aplica una matriz <sub>M sc</sub> de identidad a la fórmula en Comentarios.

</dd> <dt>

*ScalingRotation* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Puntero al factor de rotación de escalado.

</dd> <dt>

*pScaling* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntero a una estructura D3DXVECTOR2, un punto que identifica la escala. Si este argumento es **NULL,** se aplica una matriz Ms de identidad a la fórmula en Comentarios.

</dd> <dt>

*pRotationCenter* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntero a una estructura D3DXVECTOR2, un punto que identifica el centro de rotación. Si este argumento es **NULL,** se aplica una matriz M <sub>rc</sub> de identidad a la fórmula en Comentarios.

</dd> <dt>

*Rotación* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ángulo de rotación en radianes.

</dd> <dt>

*pTranslation* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntero a una estructura D3DXVECTOR2, que identifica la traducción. Si este argumento es **NULL,** se aplica una matriz mt de identidad a la fórmula en Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a una estructura D3DXMATRIX que contiene la matriz de transformación.

## <a name="remarks"></a>Comentarios

Esta función calcula la matriz de transformación con la siguiente fórmula, con la concatenación de matrices evaluada en orden de izquierda a derecha:

M<sub>out</sub> = (M<sub>sc</sub>)/¹ \* (M<sub>sr</sub>)/ntes \* \* Ms M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)/¹ \* M<sub>r</sub> M \* <sub>rc</sub> \* Mt

donde:

M<sub>out</sub> = matriz de salida (pOut)

M<sub>sc</sub> = matriz del centro de escalado (pScalingCenter)

M<sub>sr</sub> = matriz de rotación de escalado (pScalingRotation)

Ms = matriz de escalado (escalado pScaling)

M<sub>rc</sub> = centro de la matriz de rotación (pRotationCenter)

M<sub>r</sub> = matriz de rotación (rotación)

Mt = matriz de traducción (pTranslation)

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXMatrixTransformation2D se puede usar como parámetro para otra función.

Para las transformaciones 3D, use [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
