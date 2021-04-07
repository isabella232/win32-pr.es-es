---
description: Transforma una matriz (x, y, z, 1) por una matriz determinada y proyecta el resultado de nuevo en w = 1.
ms.assetid: f1595861-d8cb-4787-8078-b9ba6f76507e
title: Función D3DXVec3TransformCoordArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoordArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 414fd17c3d7077b4aeb399b734b4a6c811a8a291
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003972"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx9mathh"></a>Función D3DXVec3TransformCoordArray (D3dx9math. h)

Transforma una matriz (x, y, z, 1) por una matriz determinada y proyecta el resultado de nuevo en w = 1.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXVec3TransformCoordArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.

</dd> <dt>

Retrasos  \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Intervalo entre vectores en el flujo de datos de salida.

</dd> <dt>

*PV* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a la matriz de [**D3DXVECTOR3**](d3dxvector3.md) de origen.

</dd> <dt>

*VStride* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Intervalo entre vectores en el flujo de datos de entrada.

</dd> <dt>

*p. m* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de elementos de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es la matriz transformada.

## <a name="remarks"></a>Observaciones

Esta función transforma la matriz *PV (* x, y, z, 1) de la matriz *PM* y proyecta el resultado de nuevo en w = 1.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md) se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
