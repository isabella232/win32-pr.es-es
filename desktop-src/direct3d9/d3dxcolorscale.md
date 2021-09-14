---
description: Escala un valor de color.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: Función D3DXColorScale (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74020f302a26162df1e42cb4c9f020af3f64e59c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170466"
---
# <a name="d3dxcolorscale-function"></a>Función D3DXColorScale

Escala un valor de color.

## <a name="syntax"></a>Sintaxis


```C++
D3DXCOLOR* D3DXColorScale(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
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

</dd> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Factor de escala. Escala el color y lo trata como un vector 4D. No hay límites en el valor de s. Si s es 1, el color resultante es el color original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Esta función devuelve un puntero a una [**estructura D3DXCOLOR**](d3dxcolor.md) que es el valor de color escalado.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la **función D3DXColorScale** se puede usar como parámetro para otra función.

Esta función calcula el valor de color escalado multiplicando los componentes de color de la estructura [**D3DXCOLOR**](d3dxcolor.md) por el factor de escala especificado, como se muestra en el ejemplo siguiente.


```
pOut->r = pC->r * s;
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

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> </dl>

 

 
