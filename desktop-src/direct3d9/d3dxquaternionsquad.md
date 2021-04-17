---
description: Interpola entre cuaterniones mediante la interpolación Quadrangle esférica.
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: Función D3DXQuaternionSquad (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e4fa980d551ac43f66035c1dcaa46d1c1c590a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698220"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a>Función D3DXQuaternionSquad (D3dx9math. h)

Interpola entre cuaterniones mediante la interpolación Quadrangle esférica.

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

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.

</dd> <dt>

*pQ1* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.

</dd> <dt>

*PA* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.

</dd> <dt>

*PB* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.

</dd> <dt>

*PC* \[ de de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.

</dd> <dt>

*t* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Parámetro que indica hasta qué punto se debe interpolar entre los cuaterniones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la interpolación Quadrangle esférica.

## <a name="remarks"></a>Observaciones

Esta función usa la siguiente secuencia de operaciones de interpolación lineal esférica:


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXQuaternionSquad** se puede usar como parámetro de otra función.

Para obtener un ejemplo de la interpolación entre cuaterniones, vea el ejemplo SkinnedMesh. Puede obtener este ejemplo y obtener información sobre él desde el SDK de DirectX. Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

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

[**D3DXQuaternionLn**](d3dxquaternionln.md)
</dt> <dt>

[**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
