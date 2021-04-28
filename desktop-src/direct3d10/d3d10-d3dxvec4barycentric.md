---
description: 'Función D3DXVec4BaryCentric (D3DX10Math.h): devuelve un punto en coordenadas centradas en Barycentric, utilizando los vectores 4D especificados.'
ms.assetid: 44406135-3270-4f2e-bb53-29affb2510f2
title: Función D3DXVec4BaryCentric (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 935432d1634a7fd35401d92471b1f366075ac8b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102993"
---
# <a name="d3dxvec4barycentric-function-d3dx10mathh"></a>Función D3DXVec4BaryCentric (D3DX10Math.h)

Devuelve un punto en coordenadas centradas en Bary, utilizando los vectores 4D especificados.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _In_       D3DXVECTOR4 *pOut,
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2,
  _In_ const D3DXVECTOR4 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntero a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que es el resultado de la operación.

</dd> <dt>

*pV1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntero a una estructura D3DXVECTOR4 de origen.

</dd> <dt>

*pV2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntero a una estructura D3DXVECTOR4 de origen.

</dd> <dt>

*pV3* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntero a una estructura D3DXVECTOR4 de origen.

</dd> <dt>

*f* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Factor de ponderación. Vea la sección Comentarios.

</dd> <dt>

*g* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Factor de ponderación. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntero a una estructura D3DXVECTOR4 en coordenadas centradas en baría.

## <a name="remarks"></a>Comentarios

La función D3DXVec4BaryCentric proporciona una manera de comprender los puntos dentro y alrededor de un triángulo, independientemente de dónde se encuentra realmente el triángulo. Esta función devuelve el punto resultante mediante la siguiente ecuación: V1 + f(V2-V1) + g(V3-V1).

Cualquier punto del plano V1V2V3 se puede representar mediante la coordenada baricéntrica (f,g). El parámetro f controla la cantidad de V2 que se pondera en el resultado y el parámetro g controla la cantidad de V3 que se pondera en el resultado. Por último, 1-f-g controla la cantidad de V1 que se pondera en el resultado.

Tenga en cuenta las siguientes relaciones.

-   Si (f>=0 &, & g>=0 &, & 1-f-g>=0), el punto está dentro del triángulo V1V2V3.
-   Si (f==0 &, & g>=0 &, & 1-f-g>=0), el punto está en la línea V1V3.
-   Si (f>=0 &, & g==0 &, & 1-f-g>=0), el punto está en la línea V1V2.
-   Si (f>=0 &, & g>=0 &, & 1-f-g==0), el punto está en la línea V2V3.

Las coordenadas barycéntricas son una forma de coordenadas generales. En este contexto, el uso de coordenadas baricéntricas representa un cambio en los sistemas de coordenadas. Lo que se aplica a las coordenadas cartesianas es true para las coordenadas baríntricas.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De este modo, la función D3DXVec4BaryCentric se puede usar como parámetro para otra función.

Las coordenadas barítricas definen un punto dentro de un triángulo en términos de los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas baricéntricas, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
