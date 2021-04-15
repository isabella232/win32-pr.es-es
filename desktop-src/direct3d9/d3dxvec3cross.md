---
description: Determina el producto cruzado de dos vectores 3D.
ms.assetid: c9623f35-c8fc-4fbe-87b6-0e5bb8ebd5e8
title: Función D3DXVec3Cross (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ba0d8a80690f43d5f8e9f6df55aa3b2e0db23dc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707872"
---
# <a name="d3dxvec3cross-function"></a>D3DXVec3Cross función)

Determina el producto cruzado de dos vectores 3D.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXVec3Cross(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.

</dd> <dt>

*pV1* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.

</dd> <dt>

*pV2* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el producto cruzado de dos vectores 3D.

## <a name="remarks"></a>Observaciones

Esta función determina el producto cruzado con el código siguiente.


```
D3DXVECTOR3 v;
    
v.x = pV1->y * pV2->z - pV1->z * pV2->y;
v.y = pV1->z * pV2->x - pV1->x * pV2->z;
v.z = pV1->x * pV2->y - pV1->y * pV2->x;
    
*pOut = v;
```



El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXVec3Cross** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Dot**](d3dxvec3dot.md)
</dt> </dl>

 

 




