---
description: Transforma el vector 3D normal de la matriz especificada.
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: Función D3DXVec3TransformNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8dd0bf3fa2083d2cf0cc0cea72343f4774a586f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280467"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a>Función D3DXVec3TransformNormal (D3dx9math. h)

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

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.

</dd> <dt>

*PV* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a la estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.

</dd> <dt>

*p. m* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el vector transformado.

## <a name="remarks"></a>Observaciones

Esta función transforma el vector (*PV*->x, *PV*->y, *PV*->z, 0) por la matriz a la que señala *PM*.

Si desea transformar un normal, la matriz que se pasa a esta función debe ser la transformación del inverso de la matriz que se usaría para transformar un punto.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXVec3TransformNormal** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




