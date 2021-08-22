---
description: 'Función D3DXMatrixAffineTransformation (D3DX10Math.h): crea una matriz de transformación afín 3D. Los argumentos NULL se tratan como transformaciones de identidad.'
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: Función D3DXMatrixAffineTransformation (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5c847d537eaa79b266ef785f40806c37e2503b2b9a8a97bf99a678c7dff219de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609525"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a>Función D3DXMatrixAffineTransformation (D3DX10Math.h)

Crea una matriz de transformación afín 3D. **Los** argumentos NULL se tratan como transformaciones de identidad.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*Escalado* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Factor de escalado.

</dd> <dt>

*pRotationCenter* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a [**D3DXVECTOR3,**](d3d10-d3dxvector3.md)un punto que identifica el centro de rotación. Si este argumento es **NULL,** se aplica una matriz M <sub>rc</sub> de identidad a la fórmula en Comentarios.

</dd> <dt>

*pRotation* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero a [**un D3DXQUATERNION**](d3d10-d3dxquaternion.md) que especifica la rotación. Si este argumento es **NULL,** se aplica una matriz <sub>M r</sub> de identidad a la fórmula en Comentarios.

</dd> <dt>

*pTranslation* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3 que representa la traducción. Si este argumento es **NULL,** se aplica una matriz mt de identidad a la fórmula en Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a una estructura D3DXMATRIX que es una matriz de transformación afín.

## <a name="remarks"></a>Comentarios

Esta función calcula la matriz de transformación afín con la siguiente fórmula, con la concatenación de matrices evaluada en orden de izquierda a derecha:

M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ

donde:

M<sub>out</sub> = matriz de salida (pOut)

Ms = matriz de escalado (escalado)

M<sub>rc</sub> = centro de la matriz de rotación (pRotationCenter)

M<sub>r</sub> = matriz de rotación (pRotation)

Mt = matriz de traducción (pTranslation)

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De este modo, la función D3DXMatrixAffineTransformation se puede usar como parámetro para otra función.

Para las transformaciones de afín 2D, use D3DXMatrixAffineTransformation2D.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
