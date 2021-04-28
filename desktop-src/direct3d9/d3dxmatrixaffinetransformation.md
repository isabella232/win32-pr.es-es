---
description: 'Función D3DXMatrixAffineTransformation (D3dx9math.h): crea una matriz de transformación afín 3D. Los argumentos NULL se tratan como transformaciones de identidad.'
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: Función D3DXMatrixAffineTransformation (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7329ffbffe5ffd89ed64e5386246f39699618960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094173"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a>Función D3DXMatrixAffineTransformation (D3dx9math.h)

Crea una matriz de transformación afín 3D. **Los** argumentos NULL se tratan como transformaciones de identidad.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
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

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) un punto que identifica el centro de rotación. Si este argumento es **NULL,** se aplica una matriz M <sub>rc</sub> de identidad a la fórmula en Comentarios.

</dd> <dt>

*pRotation* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que especifica la rotación. Si este argumento es **NULL,** se aplica una matriz <sub>M r</sub> de identidad a la fórmula en Comentarios.

</dd> <dt>

*pTranslation* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3 que**](d3dxvector3.md) representa la traducción. Si este argumento es **NULL,** se aplica una matriz mt de identidad a la fórmula en Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es una matriz de transformación afín.

## <a name="remarks"></a>Comentarios

Esta función calcula la matriz de transformación afín con la siguiente fórmula, con la concatenación de matrices evaluada en orden de izquierda a derecha:

M<sub>out</sub> = Ms \* (M<sub>rc</sub>)/¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

donde:

M <sub>out</sub> = matriz de salida (*pOut*)

Ms = matriz de escalado (*escalado*)

M <sub>rc</sub> = centro de la matriz de rotación (*pRotationCenter*)

M <sub>r</sub> = matriz de rotación (*pRotation*)

Mt = matriz de traducción (*pTranslation*)

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De este modo, la **función D3DXMatrixAffineTransformation** se puede usar como parámetro para otra función.

Para las transformaciones de afín 2D, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixTransformation**](d3dxmatrixtransformation.md)
</dt> <dt>

[Transformaciones (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
