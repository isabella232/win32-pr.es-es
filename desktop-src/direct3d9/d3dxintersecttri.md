---
description: Calcula la intersección de un rayo y un triángulo.
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: Función D3DXIntersectTri (D3DX9Mesh. h)
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
ms.openlocfilehash: 41c7012cea0a533dc447db0575def6b418d0e59e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670235"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a>Función D3DXIntersectTri (D3DX9Mesh. h)

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

*P0* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que describe la primera posición del vértice del triángulo.

</dd> <dt>

*P1* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que describe la segunda posición del vértice del triángulo.

</dd> <dt>

*P2* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que describe la tercera posición del vértice del triángulo.

</dd> <dt>

*pRayPos* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica el punto en el que comienza el rayo.

</dd> <dt>

*pRayDir* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la dirección del rayo.

</dd> <dt>

*PU* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Barycentric coordenadas de aciertos, U.

</dd> <dt>

*PV* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Barycentric coordenadas de aciertos, V.

</dd> <dt>

*pDist* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Distancia del parámetro de intersección de rayo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Devuelve **true** si el rayo forma una intersección con el área del triángulo. De lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

La función [**D3DXIntersect**](d3dxintersect.md) proporciona una manera de comprender los puntos en y alrededor de un triángulo, independientemente de dónde se encuentre realmente el triángulo. Esta función devuelve el punto resultante mediante la siguiente ecuación: v1 + U (V2-V1) + V (V3-V1).

Cualquier punto del V1V2V3 de plano se puede representar mediante la coordenada Barycentric (U, V). El parámetro U controla la cantidad de v2 que se pondera en el resultado, y el parámetro V controla la cantidad de V3 que se pondera en el resultado. Por último, el valor de \[ 1-(U + V) \] controla la cantidad de V1 que se pondera en el resultado.

Las coordenadas de Barycentric son una forma de coordenadas generales. En este contexto, el uso de coordenadas Barycentric representa un cambio en los sistemas de coordenadas. Lo que sucede para las coordenadas cartesianas es true para las coordenadas Barycentric.

Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
