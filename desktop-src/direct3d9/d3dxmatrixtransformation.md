---
description: 'Función D3DXMatrixTransformation (D3dx9math.h): crea una matriz de transformación. Los argumentos NULL se tratan como transformaciones de identidad.'
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: Función D3DXMatrixTransformation (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc3b6502a8015564207f208166cec15227d3b18a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974340"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a>Función D3DXMatrixTransformation (D3dx9math.h)

Crea una matriz de transformación. **Los** argumentos NULL se tratan como transformaciones de identidad.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
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

*pScalingCenter* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que identifica el punto central de escalado. Si este argumento es **NULL,** se aplica una matriz <sub>M sc</sub> de identidad a la fórmula en Comentarios.

</dd> <dt>

*pScalingRotation* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que especifica la rotación de escalado. Si este argumento es **NULL,** se aplica una matriz M <sub>sr</sub> de identidad a la fórmula en Comentarios.

</dd> <dt>

*pScaling* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) el vector de escalado. Si este argumento es **NULL,** se aplica una matriz Ms de identidad a la fórmula en Comentarios.

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

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que representa la traducción. Si este argumento es **NULL,** se aplica una matriz mt de identidad a la fórmula en Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es la matriz de transformación.

## <a name="remarks"></a>Observaciones

Esta función calcula la matriz de transformación con la fórmula siguiente, con la concatenación de matrices evaluada en orden de izquierda a derecha:

M<sub>out</sub> = (M<sub>sc</sub>)/¹ \* (M<sub>sr</sub>)/¹ \* Ms M \* <sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)/¹ \* M<sub>r</sub> M \* <sub>rc</sub> \* Mt

donde:

M <sub>out</sub> = matriz de salida (*pOut*)

M <sub>sc</sub> = matriz del centro de escalado (*pScalingCenter*)

M <sub>sr</sub> = matriz de rotación de escalado (*pScalingRotation*)

Ms = matriz de escalado (*pScaling*)

M <sub>rc</sub> = centro de la matriz de rotación (*pRotationCenter*)

M <sub>r</sub> = matriz de rotación (*pRotation*)

Mt = matriz de traducción (*pTranslation*)

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXMatrixTransformation** se puede usar como parámetro para otra función.

Para las transformaciones 2D, use [**D3DXMatrixTransformation2D.**](d3dxmatrixtransformation2d.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[Transformaciones (Direct3D 9)](transforms.md)
</dt> </dl>

 

 




