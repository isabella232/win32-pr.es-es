---
description: Agrega dos valores de color juntos para crear un nuevo valor de color.
ms.assetid: 7743392d-4676-4408-93e9-f92d4bf02411
title: Función D3DXColorAdd (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f326c9bec4802a9a94accc76b825cd1c6ea28fd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678827"
---
# <a name="d3dxcoloradd-function"></a>D3DXColorAdd función)

Agrega dos valores de color juntos para crear un nuevo valor de color.

## <a name="syntax"></a>Sintaxis


```C++
D3DXCOLOR* D3DXColorAdd(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el resultado de la operación.

</dd> <dt>

*pC1* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.

</dd> <dt>

*pC2* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Esta función devuelve un puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es la suma de dos valores de color.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor devuelto en pOut. De esta manera, la función **D3DXColorAdd** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorSubtract**](d3dxcolorsubtract.md)
</dt> </dl>

 

 




