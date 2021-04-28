---
description: 'Función D3DXVec3TransformNormal (D3dx9math.h): transforma el vector 3D normal según la matriz especificada.'
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: Función D3DXVec3TransformNormal (D3dx9math.h)
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
ms.openlocfilehash: 50fb09a4619be9c3dbcff98bc939d6f99ad33bd4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115623"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a>Función D3DXVec3TransformNormal (D3dx9math.h)

Transforma el vector 3D normal según la matriz especificada.

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

Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.

</dd> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a la estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen.

</dd> <dt>

*pM* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una [**estructura D3DXVECTOR3**](d3dxvector3.md) que es el vector transformado.

## <a name="remarks"></a>Comentarios

Esta función transforma el vector (*pV*->x, *pV*->y, *pV*->z, 0) por la matriz a la que apunta *pM*.

Si desea transformar un normal, la matriz que pasa a esta función debe ser la transpuesta de la inversa de la matriz que usaría para transformar un punto.

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXVec3TransformNormal** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




