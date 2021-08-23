---
description: 'Función D3DXQuaternionExp (D3DX10Math.h): calcula el valor exponencial.'
ms.assetid: bd70c432-ac61-4c38-b10b-3b103e49ead8
title: Función D3DXQuaternionExp (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 61035976610cac4bb428687d9742b3a493e0ba458c8a050f4ad77891f01c26b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991135"
---
# <a name="d3dxquaternionexp-function-d3dx10mathh"></a>Función D3DXQuaternionExp (D3DX10Math.h)

Calcula el valor exponencial.

## <a name="syntax"></a>Sintaxis


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntero a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.

</dd> <dt>

*pQ* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero a la estructura D3DXQUATERNION de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntero a una estructura D3DXQUATERNION que es exponencial.

## <a name="remarks"></a>Comentarios

Este método convierte un cuaternión puro en un cuaternión de unidad. D3DXQuaternionExp espera un cuaternión puro, donde w se omite en el cálculo (w == 0).


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



donde v es la parte vectorial de un cuaternión.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De este modo, la función D3DXQuaternionExp se puede usar como parámetro para otra función.

El [**método D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) también se puede usar para configurar los puntos de control de un cuaternión.

Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
