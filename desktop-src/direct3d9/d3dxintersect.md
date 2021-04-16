---
description: Determina si un rayo forma una intersección con una malla.
ms.assetid: 325f5b40-80ba-4400-a143-bae41146ab07
title: Función D3DXIntersect (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc877fb1301e01b05184625ba2e92a2c680cfa9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707879"
---
# <a name="d3dxintersect-function"></a>D3DXIntersect función)

Determina si un rayo forma una intersección con una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXIntersect(
  _In_        LPD3DXBASEMESH pMesh,
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

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntero a una interfaz [**ID3DXBaseMesh**](id3dxbasemesh.md) que representa la malla que se va a probar.

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

*pHit* \[ enuncia\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)\***

Puntero a un BOOLEANO. Si el rayo cruza una esfera triangular en la malla, este valor se establecerá en **true**. De lo contrario, este valor se establece en **false**.

</dd> <dt>

*pFaceIndex* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a un valor de índice de la superficie más cercana al origen del rayo, si pHit es **true**.

</dd> <dt>

*PU* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a una coordenada de posicionamiento de Barycentric, U.

</dd> <dt>

*PV* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a una coordenada de posicionamiento de Barycentric, V.

</dd> <dt>

*pDist* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a una distancia del parámetro de intersección de rayo.

</dd> <dt>

*ppAllHits* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a un objeto [**ID3DXBuffer**](id3dxbuffer.md) que contiene una matriz de estructuras [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) .

</dd> <dt>

*pCountOfHits* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a un valor DWORD que contiene el número de entradas de la matriz ppAllHits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La función **D3DXIntersect** proporciona una manera de comprender los puntos en y alrededor de un triángulo, independientemente de dónde se encuentre realmente el triángulo. Esta función devuelve el punto resultante mediante la siguiente ecuación: v1 + U (V2-V1) + V (V3-V1).

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

 

 
