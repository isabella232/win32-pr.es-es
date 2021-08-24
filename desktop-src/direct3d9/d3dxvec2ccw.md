---
description: Devuelve el componente z tomando el producto cruzado de dos vectores 2D.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: Función D3DXVec2CCW (D3dx9math.h)
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
ms.openlocfilehash: 2b38adaf28b6e2394608cfb6f73f4a39d803d4fd5106f826d810a5c8dfd02618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630705"
---
# <a name="d3dxvec2ccw-function"></a>Función D3DXVec2CCW

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

*pV1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.

</dd> <dt>

*pV2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Componente z.

## <a name="remarks"></a>Comentarios

Esta función determina el componente z mediante la determinación del producto cruzado en función de la fórmula siguiente: ((x1,y1,0) cross (x2,y2,0)). O como se muestra en el ejemplo siguiente.


```
pV1->x * pV2->y - pV1->y * pV2->x
```



Si el valor del componente z es positivo, el vector V2 es en sentido contrario a las agujas del reloj del vector V1. Esta información es útil para la selección de caras atrás.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Dot**](d3dxvec2dot.md)
</dt> </dl>

 

 
