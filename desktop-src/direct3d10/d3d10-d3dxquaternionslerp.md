---
description: 'Función D3DXQuaternionSlerp (D3DX10Math.h): interpola entre dos cuaterniones mediante la interpolación lineal esférica.'
ms.assetid: 487e1df1-bf20-49cb-ad14-61fcf1300904
title: Función D3DXQuaternionSlerp (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSlerp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 04cd3d82e4ca4e3f3357ab0114b57602f7e8a543
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103123"
---
# <a name="d3dxquaternionslerp-function-d3dx10mathh"></a>Función D3DXQuaternionSlerp (D3DX10Math.h)

Interpola entre dos cuaterniones mediante la interpolación lineal esférica.

## <a name="syntax"></a>Sintaxis


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntero a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.

</dd> <dt>

*pQ1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero a una estructura D3DXQUATERNION de origen.

</dd> <dt>

*pQ2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero a una estructura D3DXQUATERNION de origen.

</dd> <dt>

*t* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Parámetro que indica hasta qué punto se debe interpolar entre los cuaterniones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntero a una estructura D3DXQUATERNION que es el resultado de la interpolación.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De este modo, la función D3DXQuaternionSlerp se puede usar como parámetro para otra función.

Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
