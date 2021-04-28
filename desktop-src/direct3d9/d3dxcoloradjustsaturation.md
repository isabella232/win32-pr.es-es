---
description: 'Función D3DXColorAdjustSaturation (D3dx9math.h): ajusta el valor de saturación de un color.'
ms.assetid: 1f66c3b4-2f02-4993-80c6-c484180c2459
title: Función D3DXColorAdjustSaturation (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 878cdd83a04f594da3133eda314486af96ac3d56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115873"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx9mathh"></a>Función D3DXColorAdjustSaturation (D3dx9math.h)

Ajusta el valor de saturación de un color.

## <a name="syntax"></a>Sintaxis


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
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

Valor de saturación. Este parámetro interpola linealmente entre el color convertido en escala de grises y el color original, pC. No hay límites en el valor de s. Si s es 0, el color devuelto es el color de escala de grises. Si s es 1, el color devuelto es el color original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Esta función devuelve un puntero a una [**estructura D3DXCOLOR**](d3dxcolor.md) que es el resultado del ajuste de saturación.

## <a name="remarks"></a>Comentarios

El canal alfa de entrada se copia, sin modificar, en el canal alfa de salida.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, esta función se puede usar como parámetro para otra función.

Esta función interpola los componentes de color rojo, verde y azul de una estructura [**D3DXCOLOR**](d3dxcolor.md) entre un color no saturado y un color, como se muestra en el ejemplo siguiente.


```
    // Approximate values for each component's contribution to luminance.
    // Based upon the NTSC standard described in ITU-R Recommendation BT.709.
    FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;
    
    pOut->r = grey + s * (pC->r - grey);
```



Si s es mayor que 0 y menor que 1, se reduce la saturación. Si s es mayor que 1, se aumenta la saturación.

El color de escala de grises se calcula como:


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorAdjustContrast**](d3dxcoloradjustcontrast.md)
</dt> </dl>

 

 
