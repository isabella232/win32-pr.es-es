---
description: 'Función D3DXQuaternionLn (D3DX10Math.h): calcula el logaritmo natural.'
ms.assetid: 576cf676-bb42-45ec-8e45-4612a7cdb167
title: Función D3DXQuaternionLn (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLn
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9abaaa231e424e55e496b7901882e9da17c59786
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103213"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a>Función D3DXQuaternionLn (D3DX10Math.h)

Calcula el logaritmo natural.

## <a name="syntax"></a>Sintaxis


```C++
D3DXQUATERNION* D3DXQuaternionLn(
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

Puntero a una estructura D3DXQUATERNION que es el logaritmo natural.

## <a name="remarks"></a>Comentarios

La función D3DXQuaternionLn solo funciona para cuaterniones de unidad.


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXQuaternionLn se puede usar como parámetro para otra función.

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

 

 
