---
description: 'Función D3DXVec4Normalize (D3DX10Math.h): devuelve la versión normalizada de un vector 4D.'
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: Función D3DXVec4Normalize (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 1577ff3109c2cc3ca547f68f7841ecebb2f03569
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102913"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a>Función D3DXVec4Normalize (D3DX10Math.h)

Devuelve la versión normalizada de un vector 4D.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntero a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que es el resultado de la operación.

</dd> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntero a la estructura D3DXVECTOR4 de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntero a una estructura D3DXVECTOR4 que es la versión normalizada del vector.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXVec4Normalize se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
