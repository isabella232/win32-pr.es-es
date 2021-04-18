---
description: Realiza una interpolación lineal entre dos vectores 3D.
ms.assetid: f3f06f1b-8824-47f0-b2ed-c212fa4c3225
title: Función D3DXVec3Lerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed6905cc0b13908a4e60e221737e9b5dc5a627f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718526"
---
# <a name="d3dxvec3lerp-function"></a>D3DXVec3Lerp función)

Realiza una interpolación lineal entre dos vectores 3D.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXVec3Lerp(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_          FLOAT       s
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

</dd> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Parámetro que se interpola linealmente entre los vectores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la interpolación lineal.

## <a name="remarks"></a>Observaciones

Esta función realiza la interpolación lineal basada en la siguiente fórmula: v1 + s (V2-V1).

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXVec3Lerp** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
