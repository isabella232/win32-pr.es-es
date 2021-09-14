---
description: 'Función D3DXVec2TransformCoord (D3dx9math.h): transforma un vector 2D mediante una matriz determinada, proyectando el resultado de nuevo en w = 1.'
ms.assetid: 0c0efdf8-77df-4f4a-86ce-89e11555f4dc
title: Función D3DXVec2TransformCoord (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 717af9eed2c7cedae7ac292a19239e13521dfa74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060693"
---
# <a name="d3dxvec2transformcoord-function-d3dx9mathh"></a>Función D3DXVec2TransformCoord (D3dx9math.h)

Transforma un vector 2D mediante una matriz determinada, proyectando el resultado de nuevo en w = 1.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntero a la [**estructura D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.

</dd> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a la estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.

</dd> <dt>

*pM* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntero a una [**estructura D3DXVECTOR2**](d3dxvector2.md) que es el vector transformado.

## <a name="remarks"></a>Observaciones

Esta función transforma el vector, *pV* (x, y, 0, 1), por la matriz, *pM*, proyectando el resultado de nuevo en w=1.

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXVec2TransformCoord** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Transform**](d3dxvec2transform.md)
</dt> <dt>

[**D3DXVec2TransformNormal**](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




