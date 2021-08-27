---
description: 'Función D3DXIntersectTri (D3DX9Mesh.h): calcula la intersección de un rayo y un triángulo.'
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: Función D3DXIntersectTri (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectTri
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb542c5c7bb4edb4dafffa1254b76504aaf0f256a9d694db9d55724f2c94c2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069291"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a>Función D3DXIntersectTri (D3DX9Mesh.h)

Calcula la intersección de un rayo y un triángulo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL D3DXIntersectTri(
  _In_  const D3DXVECTOR3 *p0,
  _In_  const D3DXVECTOR3 *p1,
  _In_  const D3DXVECTOR3 *p2,
  _In_  const D3DXVECTOR3 *pRayPos,
  _In_  const D3DXVECTOR3 *pRayDir,
  _Out_       FLOAT       *pU,
  _Out_       FLOAT       *pV,
  _Out_       FLOAT       *pDist
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*p0* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que describe la primera posición del vértice del triángulo.

</dd> <dt>

*p1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que describe la segunda posición del vértice del triángulo.

</dd> <dt>

*p2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que describe la tercera posición del vértice del triángulo.

</dd> <dt>

*pRayPos* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) especificando el punto donde comienza el rayo.

</dd> <dt>

*pRayDir* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) especificando la dirección del rayo.

</dd> <dt>

*pU* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Coordenadas de impacto centradas en barras, U.

</dd> <dt>

*pV* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Coordenadas de impacto centradas en barras, V.

</dd> <dt>

*pDist* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Distancia del parámetro de intersección de rayos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Devuelve **TRUE** si el rayo forma una intersección con el área del triángulo. De lo contrario, **devuelve FALSE**.

## <a name="remarks"></a>Comentarios

La [**función D3DXIntersect**](d3dxintersect.md) proporciona una manera de comprender los puntos dentro y alrededor de un triángulo, independientemente de dónde se encuentra realmente el triángulo. Esta función devuelve el punto resultante mediante la siguiente ecuación: V1 + U(V2 - V1) + V(V3 - V1).

Cualquier punto del plano V1V2V3 se puede representar mediante la coordenada centrada en barras (U,V). El parámetro U controla la cantidad de V2 que se pondera en el resultado y el parámetro V controla la cantidad de V3 que se pondera en el resultado. Por último, el valor de 1 - (U + V) controla la cantidad de V1 que se \[ pondera en el \] resultado.

Las coordenadas centradas en barras son una forma de coordenadas generales. En este contexto, el uso de coordenadas centradas en barras representa un cambio en los sistemas de coordenadas. Lo que es cierto para las coordenadas cartesianas es true para las coordenadas barídricas.

Las coordenadas centradas en barras definen un punto dentro de un triángulo en términos de los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas centradas en barras, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
