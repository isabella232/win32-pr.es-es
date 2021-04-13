---
description: Transforma el vector 3D normal de la matriz especificada.
ms.assetid: 8068b80f-6222-4f23-8b1c-2ff5592fa898
title: Función D3DXVec3TransformNormal (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 602f366d3d7ccbcd37804226323d5584eed034f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362659"
---
# <a name="d3dxvec3transformnormal-function-d3dx10mathh"></a>Función D3DXVec3TransformNormal (D3DX10Math. h)

Transforma el vector 3D normal de la matriz especificada.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que es el resultado de la operación.

</dd> <dt>

*PV* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a la estructura de D3DXVECTOR3 de origen.

</dd> <dt>

*p. m* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a la estructura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a una estructura D3DXVECTOR3 que es el vector transformado.

## <a name="remarks"></a>Observaciones

Esta función transforma el vector (pV->x, pV->y, pV->z, 0) por la matriz a la que señala pM.

Si desea transformar un normal, la matriz que se pasa a esta función debe ser la transformación del inverso de la matriz que se usaría para transformar un punto.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut. De esta manera, la función **D3DXVec3TransformNormal** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
