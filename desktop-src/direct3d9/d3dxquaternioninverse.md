---
description: Conjuga y vuelve a normalizar un cuaternión.
ms.assetid: 25407a60-f7c0-4063-8d1d-2d6d03bdb217
title: Función D3DXQuaternionInverse (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionInverse
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2f830b7f8f797e4ed94eb22b4c2a05c3bd3e4cd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424484"
---
# <a name="d3dxquaternioninverse-function-d3dx9mathh"></a>Función D3DXQuaternionInverse (D3dx9math. h)

Conjuga y vuelve a normalizar un cuaternión.

## <a name="syntax"></a>Sintaxis


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
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

Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el cuaternión inverso del cuaternión.

## <a name="remarks"></a>Observaciones


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXQuaternionInverse** se puede usar como parámetro de otra función.

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

[**D3DXQuaternionConjugate**](d3dxquaternionconjugate.md)
</dt> <dt>

[**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md)
</dt> </dl>

 

 




