---
description: Construye un plano a partir de un punto y un normal.
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: Función D3DXPlaneFromPointNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8eeb8ea3a1725e0bf615be888d8e862c97730a2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717551"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a>Función D3DXPlaneFromPointNormal (D3dx9math. h)

Construye un plano a partir de un punto y un normal.

## <a name="syntax"></a>Sintaxis


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntero a la estructura [**D3DXPLANE**](d3dxplane.md) que es el resultado de la operación.

</dd> <dt>

*PPoint* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que define el punto usado para construir el plano.

</dd> <dt>

*pNormal* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que define el uso normal para construir el plano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntero a la estructura [**D3DXPLANE**](d3dxplane.md) construida a partir del punto y el normal.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXPlaneFromPointNormal** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneFromPoints**](d3dxplanefrompoints.md)
</dt> </dl>

 

 




