---
description: Forma una intersección con el rayo especificado con el subconjunto de malla especificado. Esto proporciona una funcionalidad similar a D3DXIntersect.
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: Función D3DXIntersectSubset (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95a987730706f32654aab8f63feed61ae87c4d58d27ccccdaed9767d3303bbf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460385"
---
# <a name="d3dxintersectsubset-function"></a>Función D3DXIntersectSubset

Forma una intersección con el rayo especificado con el subconjunto de malla especificado. Esto proporciona una funcionalidad similar a [**D3DXIntersect.**](d3dxintersect.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntero a una [**interfaz ID3DXBaseMesh,**](id3dxbasemesh.md) que representa la malla que se va a probar. La malla debe estar ordenada por atributos.

</dd> <dt>

*AttribId* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Identificador de atributo del subconjunto con el que se interseca.

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

*pHit* \[ out\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)\***

Puntero a bool. Si el rayo forma una intersección con una cara triangular en la malla, este valor se establecerá en **TRUE.** De lo contrario, este valor se establece en **FALSE.**

</dd> <dt>

*pFaceIndex* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a un valor de índice de la cara más cercana al origen del rayo, si pHit es **TRUE.**

</dd> <dt>

*pU* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a una coordenada de posición centrada en barras, U.

</dd> <dt>

*pV* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a una coordenada de posición centrada en barras, V.

</dd> <dt>

*pDist* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a una distancia de parámetro de intersección de rayo.

</dd> <dt>

*ppAllHits* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Matriz [**de estructuras D3DXINTERSECTINFO,**](d3dxintersectinfo.md) que representa todos los aciertos, no solo los aciertos más cercanos.

</dd> <dt>

*pCountOfHits* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Número de elementos de la matriz devueltos desde ppAllHits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: \_ E OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La **función D3DXIntersectSubset** proporciona una manera de comprender los puntos dentro y alrededor de un triángulo, independientemente de dónde se encuentra realmente el triángulo. Esta función devuelve el punto resultante mediante la siguiente ecuación: V1 + U(V2 - V1) + V(V3 - V1).

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

 

 
