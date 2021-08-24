---
description: Agrega dos valores de color para crear un nuevo valor de color.
ms.assetid: 7743392d-4676-4408-93e9-f92d4bf02411
title: Función D3DXColorAdd (D3dx9math.h)
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
ms.openlocfilehash: bb96d811f94975d8c7be3225349fd4412a0d1168167066001888084a4ef59136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631615"
---
# <a name="d3dxcoloradd-function"></a>Función D3DXColorAdd

Agrega dos valores de color para crear un nuevo valor de color.

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

Puntero a una [**estructura D3DXCOLOR**](d3dxcolor.md) que es el resultado de la operación.

</dd> <dt>

*pC1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Puntero a una estructura [**D3DXCOLOR de**](d3dxcolor.md) origen.

</dd> <dt>

*pC2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Puntero a una estructura [**D3DXCOLOR de**](d3dxcolor.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Esta función devuelve un puntero a una [**estructura D3DXCOLOR**](d3dxcolor.md) que es la suma de dos valores de color.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en pOut. De esta manera, la **función D3DXColorAdd** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorSubtract**](d3dxcolorsubtract.md)
</dt> </dl>

 

 




