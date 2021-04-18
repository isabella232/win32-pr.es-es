---
description: Crea una matriz de transformación. Los argumentos NULL se tratan como transformaciones de identidad.
ms.assetid: 99c75ce9-3683-4753-b635-760eb8aaf46e
title: Función D3DXMatrixTransformation (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: db1d88ad04e4aaa51232cfdba3168779805b22c3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721527"
---
# <a name="d3dxmatrixtransformation-function-d3dx10mathh"></a>Función D3DXMatrixTransformation (D3DX10Math. h)

Crea una matriz de transformación. Los argumentos **null** se tratan como transformaciones de identidad.

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

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*pScalingCenter* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que identifica el punto central de escalado. Si este argumento es **null**, se aplica una matriz identidad M <sub>SC</sub> a la fórmula en la sección Comentarios.

</dd> <dt>

*pScalingRotation* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero a un [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que especifica la rotación del escalado. Si este argumento es **null**, se aplica una matriz de identidad M <sub>Sr</sub> a la fórmula en la sección Comentarios.

</dd> <dt>

*pScaling* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3, el vector de escala. Si este argumento es **null**, se aplica una matriz de identidad MS a la fórmula en la sección Comentarios.

</dd> <dt>

*pRotationCenter* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3, un punto que identifica el centro de rotación. Si este argumento es **null**, se aplica una matriz identidad M <sub>RC</sub> a la fórmula en la sección Comentarios.

</dd> <dt>

*Prot.* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero a una estructura D3DXQUATERNION que especifica la rotación. Si este argumento es **null**, se aplica una matriz de identidad M <sub>r</sub> a la fórmula en la sección Comentarios.

</dd> <dt>

*pTranslation* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3 que representa la traslación. Si este argumento es **null**, se aplica una matriz Identity MT a la fórmula en la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a una estructura D3DXMATRIX que es la matriz de transformación.

## <a name="remarks"></a>Observaciones

Esta función calcula la matriz de transformación con la fórmula siguiente, con la concatenación de matriz evaluada en orden de izquierda a derecha:

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>Sr</sub>) ⁻ ¹ \* MS \* m<sub>Sr</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* M<sub>RC</sub> \* MT

donde:

M<sub>out</sub> = matriz de salida (pOut)

M<sub>SC</sub> = matriz de centro de escalado (pScalingCenter)

M<sub>Sr</sub> = matriz de rotación de escala (pScalingRotation)

MS = matriz de escalado (pScaling)

M<sub>RC</sub> = centro de la matriz de rotación (pRotationCenter)

M<sub>r</sub> = matriz de rotación (Prot.)

MT = matriz de traslación (pTranslation)

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut. De esta manera, la función D3DXMatrixTransformation se puede usar como parámetro de otra función.

Para las transformaciones 2D, use [**D3DXMatrixTransformation2D**](d3d10-d3dxmatrixtransformation2d.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
