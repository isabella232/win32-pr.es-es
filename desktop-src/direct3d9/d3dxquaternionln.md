---
description: Calcula el logaritmo natural.
ms.assetid: 73ca7d13-1e20-48fc-b0ed-0d3127d094a7
title: Función D3DXQuaternionLn (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b51fcc77da29216acd2bfc1c011a063014da5d69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548046"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a>Función D3DXQuaternionLn (D3dx9math. h)

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

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.

</dd> <dt>

*pQ* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a la estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el logaritmo natural.

## <a name="remarks"></a>Observaciones

La función **D3DXQuaternionLn** solo funciona para los cuaterniones de unidad.


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXQuaternionLn** se puede usar como parámetro de otra función.

Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionExp**](d3dxquaternionexp.md)
</dt> <dt>

[**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
</dt> </dl>

 

 




