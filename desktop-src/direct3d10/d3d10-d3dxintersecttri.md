---
description: 'Función D3DXIntersectTri (D3DX10math.h): calcula la intersección de un rayo y un triángulo.'
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: Función D3DXIntersectTri (D3DX10math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c8bf502cca48701a7d71a083e515f9988cafe303
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113243"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a>Función D3DXIntersectTri (D3DX10math.h)

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

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) que describe la primera posición del vértice del triángulo.

</dd> <dt>

*p1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) que describe la segunda posición del vértice del triángulo.

</dd> <dt>

*p2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) que describe la tercera posición del vértice del triángulo.

</dd> <dt>

*pRayPos* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) especificando el punto donde comienza el rayo.

</dd> <dt>

*pRayDir* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) especificando la dirección del rayo.

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

Cualquier punto del plano V1V2V3 se puede representar mediante la coordenada centrada en barras (U,V). El parámetro U controla la cantidad de V2 que se pondera en el resultado y el parámetro V controla la cantidad de V3 que se pondera en el resultado. Por último, el valor de 1 - (U + V) controla la cantidad de V1 que se \[ pondera en el \] resultado.

Las coordenadas centradas en barras son una forma de coordenadas generales. En este contexto, el uso de coordenadas centradas en barras representa un cambio en los sistemas de coordenadas. Lo que es cierto para las coordenadas cartesianas es true para las coordenadas barídricas.

Las coordenadas centradas en barras definen un punto dentro de un triángulo en términos de los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas centradas en barras, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
