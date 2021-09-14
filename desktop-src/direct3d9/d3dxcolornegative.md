---
description: Crea el valor de color negativo de un valor de color.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: Función D3DXColorNegative (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6d4d8559e64580897aec5261c450dc739496e75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170470"
---
# <a name="d3dxcolornegative-function"></a>Función D3DXColorNegative

Crea el valor de color negativo de un valor de color.

## <a name="syntax"></a>Sintaxis


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Puntero a una [**estructura D3DXCOLOR**](d3dxcolor.md) que es el resultado de la operación.

</dd> <dt>

*pC* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Puntero a una estructura [**D3DXCOLOR de**](d3dxcolor.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Esta función devuelve un puntero a una [**estructura D3DXCOLOR**](d3dxcolor.md) que es el valor de color negativo del valor de color.

## <a name="remarks"></a>Observaciones

El canal alfa de entrada se copia, sin modificar, en el canal alfa de salida.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la **función D3DXColorNegative** se puede usar como parámetro para otra función.

Esta función devuelve el valor de color negativo restando 1,0 de los componentes de color de la estructura [**D3DXCOLOR,**](d3dxcolor.md) como se muestra en el ejemplo siguiente.


```
pOut->r = 1.0f - pC->r;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorLerp**](d3dxcolorlerp.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 




