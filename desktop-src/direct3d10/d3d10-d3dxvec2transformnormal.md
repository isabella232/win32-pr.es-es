---
description: 'Función D3DXVec2TransformNormal (D3DX10Math.h): transforma el vector 2D normal por la matriz dada.'
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: Función D3DXVec2TransformNormal (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 403562ab779ebf532e1c1ebcec4ce21a2beadd7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108303"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a>Función D3DXVec2TransformNormal (D3DX10Math.h)

Transforma el vector 2D normal por la matriz especificada.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Puntero a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que es el resultado de la operación.

</dd> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntero a la estructura D3DXVECTOR2 de origen.

</dd> <dt>

*pM* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Puntero a una estructura D3DXVECTOR2 que es el vector transformado.

## <a name="remarks"></a>Comentarios

Esta función transforma el vector (pV->x, pV->y, 0, 0) por la matriz a la que apunta pM.

Si desea transformar un normal, la matriz que pase a esta función debe ser la transponer del inverso de la matriz que se usaría para transformar un punto.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De este modo, la **función D3DXVec2TransformNormal** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
