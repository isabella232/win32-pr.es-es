---
description: Crea una matriz de transformación afín 3D. Los argumentos NULL se tratan como transformaciones de identidad.
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: Función D3DXMatrixAffineTransformation (D3DX10Math. h)
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
ms.openlocfilehash: 27fee5a620d75c3930b1bc2f8a85415db1320a47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698371"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a>Función D3DXMatrixAffineTransformation (D3DX10Math. h)

Crea una matriz de transformación afín 3D. Los argumentos **null** se tratan como transformaciones de identidad.

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

*pOut* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*Escalado* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de escala.

</dd> <dt>

*pRotationCenter* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), un punto que identifica el centro de rotación. Si este argumento es **null**, se aplica una matriz identidad M <sub>RC</sub> a la fórmula en la sección Comentarios.

</dd> <dt>

*Prot.* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero a un [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que especifica la rotación. Si este argumento es **null**, se aplica una matriz de identidad M <sub>r</sub> a la fórmula en la sección Comentarios.

</dd> <dt>

*pTranslation* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3 que representa la traslación. Si este argumento es **null**, se aplica una matriz Identity MT a la fórmula en la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a una estructura D3DXMATRIX que es una matriz de transformación afín.

## <a name="remarks"></a>Observaciones

Esta función calcula la matriz de transformación afín con la fórmula siguiente, con la concatenación de matriz evaluada en orden de izquierda a derecha:

M<sub>out</sub> = MS \* (M<sub>RC</sub>)-1 \* m<sub>r</sub> \* m<sub>RC</sub> \* MT

donde:

M<sub>out</sub> = matriz de salida (pOut)

MS = matriz de escalado (escala)

M<sub>RC</sub> = centro de la matriz de rotación (pRotationCenter)

M<sub>r</sub> = matriz de rotación (Prot.)

MT = matriz de traslación (pTranslation)

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut. De esta manera, la función D3DXMatrixAffineTransformation se puede usar como parámetro de otra función.

En el caso de las transformaciones afines de 2D, use D3DXMatrixAffineTransformation2D.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
