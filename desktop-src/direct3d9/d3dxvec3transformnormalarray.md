---
description: 'Función D3DXVec3TransformNormalArray (D3dx9math.h): transforma una matriz (x, y, z, 0) por una matriz determinada.'
ms.assetid: c12fad52-d541-483f-a919-e6031aa4f761
title: Función D3DXVec3TransformNormalArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74da959002bfbd0c488e630f09c89e848708b1b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063727"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx9mathh"></a>Función D3DXVec3TransformNormalArray (D3dx9math.h)

Transforma una matriz (x, y, z, 0) por una matriz determinada.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
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

Puntero a la [**matriz D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.

</dd> <dt>

*OutStride* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Paso entre vectores en el flujo de datos de salida.

</dd> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a la matriz [**D3DXVECTOR3 de**](d3dxvector3.md) origen.

</dd> <dt>

*VStride* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Paso entre vectores en el flujo de datos de entrada.

</dd> <dt>

*pM* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.

</dd> <dt>

*n* \[ en\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de elementos de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una [**matriz D3DXVECTOR3**](d3dxvector3.md) que es la matriz transformada.

## <a name="remarks"></a>Observaciones

Esta función transforma el vector *(pV*->x, *pV*->y, *pV*->z, 0) por la matriz a la que apunta *pM*.

Si desea transformar un normal, la matriz que pasa a esta función debe ser la transpuesta de la inversa de la matriz que usaría para transformar un punto.

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXVec3TransformNormalArray** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
