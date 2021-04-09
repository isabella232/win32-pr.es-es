---
description: Utiliza la interpolación lineal para crear un valor de color.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: Función D3DXColorLerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914745"
---
# <a name="d3dxcolorlerp-function"></a>D3DXColorLerp función)

Utiliza la interpolación lineal para crear un valor de color.

## <a name="syntax"></a>Sintaxis


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
  _In_          FLOAT     s
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

</dd> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Parámetro que se interpola linealmente entre los colores, pC1 y pC2, tratando ambos como vectores 4D. No hay ningún límite en el valor de s.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Esta función devuelve un puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el resultado de la interpolación lineal.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut. De esta manera, la función **D3DXColorLerp** se puede usar como parámetro de otra función.

Esta función interpola los componentes rojo, verde, azul y alfa de una estructura [**D3DXCOLOR**](d3dxcolor.md) entre dos colores, tal y como se muestra en el ejemplo siguiente.


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



Si va a interpolar linealmente entre los colores A y B, y s es 0, el color resultante es. Si es 1, el color resultante es el color B.

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

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 
