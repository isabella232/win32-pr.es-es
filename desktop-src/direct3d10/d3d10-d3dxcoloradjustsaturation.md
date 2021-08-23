---
description: 'Función D3DXColorAdjustSaturation (D3DX10Math.h): ajusta el valor de saturación de un color.'
ms.assetid: a7ca64b4-2198-4116-8e9f-79d6c922fd09
title: Función D3DXColorAdjustSaturation (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6dbc819a1c2b8b6d4eb862b61d4ee23abbb9a2fc6e5aef6b7820d7d6a1a71482
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609545"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx10mathh"></a>Función D3DXColorAdjustSaturation (D3DX10Math.h)

Ajusta el valor de saturación de un color.

## <a name="syntax"></a>Sintaxis


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     s
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Puntero a [**un D3DXCOLOR**](d3d10-d3dxcolor.md) que es el resultado de la operación.

</dd> <dt>

*pC* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Puntero a una estructura D3DXCOLOR de origen.

</dd> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor de saturación. Este parámetro interpola linealmente entre el color convertido a escala de grises y el color original, pC. No hay límites en el valor de s. Si s es 0, el color devuelto es el color de escala de grises. Si s es 1, el color devuelto es el color original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Esta función devuelve un puntero a una estructura D3DXCOLOR que es el resultado del ajuste de saturación.

## <a name="remarks"></a>Comentarios

El canal alfa de entrada se copia, sin modificar, en el canal alfa de salida.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, esta función se puede usar como parámetro para otra función.

Esta función interpola los componentes de color rojo, verde y azul de una estructura D3DXCOLOR entre un color no saturado y un color, como se muestra en el ejemplo siguiente.


```
//Approximate values for each component's contribution to luminance.
//Based upon the NTSC standard described in ITU-R Recommendation BT.709.
FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;

pOut->r = grey + s * (pC->r - grey);
```



Si s es mayor que 0 y menor que 1, se reduce la saturación. Si s es mayor que 1, se aumenta la saturación.

El color de escala de grises se calcula como:


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
