---
description: 'Función D3DXColorAdjustContrast (D3DX10Math.h): ajusta el valor de contraste de un color.'
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: Función D3DXColorAdjustContrast (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 09781c5c11560c3497a5af57528cf478f6259816
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113333"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a>Función D3DXColorAdjustContrast (D3DX10Math.h)

Ajusta el valor de contraste de un color.

## <a name="syntax"></a>Sintaxis


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     c
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

\[in, out \] Puntero a [**D3DXCOLOR**](d3d10-d3dxcolor.md) que es el resultado de la operación.

</dd> <dt>

*pC* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Puntero a una estructura D3DXCOLOR de origen.

</dd> <dt>

*c* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor de contraste. Este parámetro interpola linealmente entre el porcentaje de gris del cincuenta por ciento y el color, pC. No hay límites en el valor de c. Si este parámetro es cero, el color devuelto es un gris del 50 por ciento. Si este parámetro es 1, el color devuelto es el color original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Esta función devuelve un puntero a una estructura D3DXCOLOR que es el resultado del ajuste de contraste.

## <a name="remarks"></a>Comentarios

El canal alfa de entrada se copia, sin modificar, en el canal alfa de salida.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, esta función se puede usar como parámetro para otra función.

Esta función interpola los componentes de color rojo, verde y azul de una estructura D3DXCOLOR entre el cincuenta por ciento de gris y un valor de contraste especificado, como se muestra en el ejemplo siguiente.


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



Si c es mayor que 0 y menor que 1, se reduce el contraste. Si c es mayor que 1, se aumenta el contraste.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
