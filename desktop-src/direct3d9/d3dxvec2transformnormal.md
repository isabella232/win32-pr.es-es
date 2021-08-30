---
description: 'Función D3DXVec2TransformNormal (D3dx9math.h): transforma el vector 2D normal por la matriz dada.'
ms.assetid: aa9adf6d-5aae-4acf-bbd9-f5c14d90470e
title: Función D3DXVec2TransformNormal (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bb1cc78bdb1b2e4fc713bf85b99046010d2f74f8cedb5d7fecef7089b7d3a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849655"
---
# <a name="d3dxvec2transformnormal-function-d3dx9mathh"></a>Función D3DXVec2TransformNormal (D3dx9math.h)

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

## <a name="remarks"></a>Comentarios

Esta función transforma el vector *(pV-*>x, *pV-*>y, 0, 0) por la matriz a la que apunta *pM*.

Si desea transformar un normal, la matriz que pase a esta función debe ser la transponer del inverso de la matriz que se usaría para transformar un punto.

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXVec2TransformNormal** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Transform**](d3dxvec2transform.md)
</dt> <dt>

[**D3DXVec2TransformCoord**](d3dxvec2transformcoord.md)
</dt> </dl>

 

 




