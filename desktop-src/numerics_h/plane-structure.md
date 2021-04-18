---
title: estructura de plano (Windowsnumerics. h)
description: Esta estructura representa un plano mediante un vector 3D normal y un valor de distancia.
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- estructura del plano
topic_type:
- apiref
api_name:
- plane structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d870e2769121b4aec542235081011406e439d579
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721609"
---
# <a name="plane-structure"></a>estructura del plano

Esta estructura representa un plano mediante un vector 3D normal y un valor de distancia.

Este tipo solo está disponible en C++. Su equivalente de .NET es [System. Numerics. Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).

## <a name="constructors"></a>Constructores

| Nombre | Descripción |
|-|-|
| `plane()` | Crea un plano no inicializado. |
| `plane(float x, float y, float z, float d)` | Crea un plano con los valores especificados. |
| `plane(float3 normal, float d)` | Crea un plano a partir de un float3 y una distancia. |
| `explicit plane(float4 value)` | Crea un plano a partir de una FLOAT4. |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | Convierte un **Microsoft. Graphics. Canvas. Numerics. Plane** en un plano. |

## <a name="functions"></a>Functions

| Nombre | Descripción |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | Crea un plano a partir de un conjunto de tres posiciones de vértice, que deben ser diferentes y no en una línea recta. |
| `plane normalize(plane const& value)` | Cambia los coeficientes del vector normal de un plano para que sea de longitud de unidad. |
| `plane transform(plane const& plane, float4x4 const& matrix)` | Transforma un plano normalizado mediante una matriz. |
| `plane transform(plane const& plane, quaternion const& rotation)` | Transforma un plano normalizado mediante una rotación de cuaternión. |
| `float dot(plane const& plane, float4 const& value)` | Calcula el producto escalar de un plano con un vector. |
| `float dot_coordinate(plane const& plane, float3 const& value)` | Calcula el producto escalar de un plano con una coordenada float3. A diferencia \_ de DOT normal, este cálculo incluye el valor de plano d. |
| `float dot_normal(plane const& plane, float3 const& value)` | Calcula el producto escalar de un plano con un float3 normal. A diferencia \_ de la coordenada de puntos, este cálculo omite el valor de plano d. |

## <a name="operators"></a>Operadores

| Nombre | Descripción |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | Determina si dos instancias de plano son iguales. |
| `bool operator!= (plane const& value1, plane const& value2)` | Determina si dos instancias de plano no son iguales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | Convierte un plano en un **Microsoft. Graphics. Canvas. Numerics. Plane**. |

## <a name="fields"></a>Campos

| Nombre | Descripción |
|-|-|
| `float3 normal` | Vector normal del plano. |
| `float d` | Distancia del plano a lo largo de su normal desde el origen. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Espacio de nombres | Windows:: Foundation:: Numerics |
| Encabezado | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Vea también

[API de windowsnumerics. h](windowsnumerics-h-apis-portal.md)
