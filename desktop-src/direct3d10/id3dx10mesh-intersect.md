---
description: Determina si un rayo forma una intersección con esta malla.
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: Método ID3DX10Mesh::Intersect (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1693db027baad13d69c43e394407ed8eb037d2dbb95eb217ccca473d1f91d08a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634555"
---
# <a name="id3dx10meshintersect-method"></a>Método ID3DX10Mesh::Intersect

Determina si un rayo forma una intersección con esta malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Intersect(
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRayPos* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) especificando el punto donde comienza el rayo.

</dd> <dt>

*pRayDir* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) especificando la dirección del rayo.

</dd> <dt>

*pHitCount* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Número de veces que el rayo formaba intersección con la malla.

</dd> <dt>

*pFaceIndex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero a un valor de índice de la cara más cercana al origen del rayo, si pHit es **TRUE.**

</dd> <dt>

*pU* \[ En\]
</dt> <dd>

Tipo: **\* float**

Puntero a una coordenada de posición centrada en barras, U.

</dd> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **\* float**

Puntero a una coordenada de posición centrada en barras, V.

</dd> <dt>

*pDist* \[ En\]
</dt> <dd>

Tipo: **\* float**

Puntero a una distancia de parámetro de intersección de rayo.

</dd> <dt>

*ppAllHits* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntero a una [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)que contiene una matriz de estructuras [**DE INFORMACIÓN \_ INTERSECT \_ de D3DX10.**](d3dx10-intersect-info.md) Esta es una lista de todos los aciertos que se produjeron en la prueba de intersección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Esta API proporciona una manera de comprender los puntos dentro y alrededor de un triángulo, independientemente de dónde se encuentra realmente el triángulo. Esta función devuelve el punto resultante mediante la siguiente ecuación: V1 + U(V2 - V1) + V(V3 - V1).

Cualquier punto del plano V1V2V3 se puede representar mediante la coordenada centrada en barras (U,V). El parámetro U controla la cantidad de V2 que se pondera en el resultado y el parámetro V controla la cantidad de V3 que se pondera en el resultado. Por último, el valor de 1 - (U + V) controla la cantidad de V1 que se \[ pondera en el \] resultado.

Las coordenadas centradas en barras son una forma de coordenadas generales. En este contexto, el uso de coordenadas centradas en barras representa un cambio en los sistemas de coordenadas. Lo que es cierto para las coordenadas cartesianas es true para las coordenadas barídricas.

Las coordenadas centradas en barras definen un punto dentro de un triángulo en términos de los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas centradas en barras, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
