---
description: 'Función D3DXMatrixRotationQuaternion (D3DX10Math.h): crea una matriz de rotación a partir de un cuaternión.'
ms.assetid: dcbf8696-b959-4475-a250-6094dd5fe358
title: Función D3DXMatrixRotationQuaternion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationQuaternion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d95d28b7f7106df9ddfb43a9175f5c19292d52c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103433"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx10mathh"></a>Función D3DXMatrixRotationQuaternion (D3DX10Math.h)

Crea una matriz de rotación a partir de un cuaternión.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*pQ* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero a la estructura D3DXQUATERNION de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a una estructura D3DXMATRIX creada a partir del cuaternión de origen.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De este modo, la función D3DXMatrixRotationQuaternion se puede usar como parámetro para otra función.

Para obtener información sobre cómo calcular valores de cuaternión a partir de un vector de dirección (x, y, z) y un ángulo de rotación, vea [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
