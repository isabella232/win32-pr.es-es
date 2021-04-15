---
description: Devuelve el componente z tomando el producto cruzado de dos vectores 2D.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: Función D3DXVec2CCW (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707861"
---
# <a name="d3dxvec2ccw-function"></a>D3DXVec2CCW función)

Devuelve el componente z tomando el producto cruzado de dos vectores 2D.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pV1* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.

</dd> <dt>

*pV2* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Componente z.

## <a name="remarks"></a>Observaciones

Esta función determina el componente z determinando el producto cruzado basado en la siguiente fórmula: ((x1, Y1, 0) Cross (x2, Y2, 0)). O tal y como se muestra en el ejemplo siguiente.


```
pV1->x * pV2->y - pV1->y * pV2->x
```



Si el valor del componente z es positivo, el vector V2 es en sentido contrario a las agujas del reloj desde el vector v1. Esta información es útil para la selección de la cara posterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Dot**](d3dxvec2dot.md)
</dt> </dl>

 

 
