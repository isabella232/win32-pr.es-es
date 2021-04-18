---
description: Transforma una matriz (x, y, 0, 1) por una matriz determinada.
ms.assetid: 11d69f65-2aef-46f4-b274-e173a11382a8
title: Función D3DXVec4TransformArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3102d1766ba43525829e045503c1838a19d4b0e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718569"
---
# <a name="d3dxvec4transformarray-function-d3dx9mathh"></a>Función D3DXVec4TransformArray (D3dx9math. h)

Transforma una matriz (x, y, 0, 1) por una matriz determinada.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR4* D3DXVec4TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR4 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntero a la matriz [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.

</dd> <dt>

Retrasos  \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Intervalo entre vectores en el flujo de datos de salida.

</dd> <dt>

*PV* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a la matriz de [**D3DXVECTOR4**](d3dxvector4.md) de origen.

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

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que es la matriz transformada.

## <a name="remarks"></a>Observaciones

Esta función transforma la matriz *PV* (x, y, 0, 1) de la matriz *PM*.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXVec4TransformArray** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
