---
description: Determina si un cuaternión es un cuaternión de identidad.
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: Función D3DXQuaternionIsIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2b02bdddb4b7a2d31a685f576434e34952c0a22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708021"
---
# <a name="d3dxquaternionisidentity-function"></a>D3DXQuaternionIsIdentity función)

Determina si un cuaternión es un cuaternión de identidad.

## <a name="syntax"></a>Sintaxis


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pQ* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) cuya identidad se probará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Si el cuaternión es un cuaternión de identidad, esta función devuelve **true**. De lo contrario, esta función devuelve **false**.

## <a name="remarks"></a>Observaciones

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

[**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
</dt> </dl>

 

 
