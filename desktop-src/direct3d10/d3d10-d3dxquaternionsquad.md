---
description: 'Función D3DXQuaternionSquad (D3DX10Math.h): interpola entre cuaterniones, mediante la interpolación de cuadrángulo esférico.'
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: Función D3DXQuaternionSquad (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9671b2a161124228c264da7eac0a2aa3a915ff95
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108763"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a>Función D3DXQuaternionSquad (D3DX10Math.h)

Interpola entre cuaterniones mediante la interpolación de cuadrángulo esférica.

## <a name="syntax"></a>Sintaxis


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
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

*pA* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero a una estructura D3DXQUATERNION de origen.

</dd> <dt>

*pB* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero a una estructura D3DXQUATERNION de origen.

</dd> <dt>

*pC* \[ En\]
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

Puntero a una estructura D3DXQUATERNION que es el resultado de la interpolación esférica de cuadrángulo.

## <a name="remarks"></a>Comentarios

Esta función usa la siguiente secuencia de operaciones de interpolación lineal esférica:


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXQuaternionSquad se puede usar como parámetro para otra función.

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

 

 
