---
description: 'Función D3DXVec4Cross (D3DX10Math.h): determina el producto cruzado en cuatro dimensiones.'
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: Función D3DXVec4Cross (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 8d9b2d93a6c4166eaa2aa8b7bbdbe7e1473288ec209d5e6d43a4c9331121105e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914622"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a>Función D3DXVec4Cross (D3DX10Math.h)

Determina el producto cruzado en cuatro dimensiones.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntero a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que es el resultado de la operación.

</dd> <dt>

*pV1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntero a una estructura D3DXVECTOR4 de origen.

</dd> <dt>

*pV2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntero a una estructura D3DXVECTOR4 de origen.

</dd> <dt>

*pV3* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntero a una estructura D3DXVECTOR4 de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntero a una estructura D3DXVECTOR4 que es el producto cruzado.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De este modo, la función D3DXVec4Cross se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
