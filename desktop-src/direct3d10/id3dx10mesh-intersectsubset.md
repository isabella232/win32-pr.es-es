---
description: Determina si un rayo forma una intersección con un subconjunto de esta malla.
ms.assetid: 31f90141-60be-4c7f-8d6a-a1a97ff26d9d
title: Método ID3DX10Mesh::IntersectSubset (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.IntersectSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a08d4db92dc75f40d0073367dda9a9ea26863418
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280419"
---
# <a name="id3dx10meshintersectsubset-method"></a>ID3DX10Mesh:: IntersectSubset (método)

Determina si un rayo forma una intersección con un subconjunto de esta malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IntersectSubset(
  [in]  UINT        AttribId,
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

*AttribId* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

IDENTIFICADOR de atributo que identifica el subconjunto de la malla.

</dd> <dt>

*pRayPos* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que especifica el punto en el que comienza el rayo.

</dd> <dt>

*pRayDir* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que especifica la dirección del rayo.

</dd> <dt>

*pHitCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Número de veces que el rayo intersecó con la malla.

</dd> <dt>

*pFaceIndex* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntero a un valor de índice de la superficie más cercana al origen del rayo, si pHit es **true**.

</dd> <dt>

*PU* \[ de\]
</dt> <dd>

Tipo: **float \***

Puntero a una coordenada de posicionamiento de Barycentric, U.

</dd> <dt>

*PV* \[ de\]
</dt> <dd>

Tipo: **float \***

Puntero a una coordenada de posicionamiento de Barycentric, V.

</dd> <dt>

*pDist* \[ de\]
</dt> <dd>

Tipo: **float \***

Puntero a una distancia del parámetro de intersección de rayo.

</dd> <dt>

*ppAllHits* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntero a una [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)que contiene una matriz de estructuras de [**\_ \_ información de intersección D3DX10**](d3dx10-intersect-info.md) . Esta es una lista de todos los aciertos que se produjeron en la prueba de intersección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Esta API proporciona una manera de comprender los puntos en y alrededor de un triángulo, independientemente de dónde se encuentre realmente el triángulo. Esta función devuelve el punto resultante mediante la siguiente ecuación: v1 + U (V2-V1) + V (V3-V1).

Cualquier punto del V1V2V3 de plano se puede representar mediante la coordenada Barycentric (U, V). El parámetro U controla la cantidad de v2 que se pondera en el resultado, y el parámetro V controla la cantidad de V3 que se pondera en el resultado. Por último, el valor de \[ 1-(U + V) \] controla la cantidad de V1 que se pondera en el resultado.

Las coordenadas de Barycentric son una forma de coordenadas generales. En este contexto, el uso de coordenadas Barycentric representa un cambio en los sistemas de coordenadas. Lo que sucede para las coordenadas cartesianas es true para las coordenadas Barycentric.

Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
