---
title: estructura de plano (Windowsnumerics.h)
description: Esta estructura representa un plano utilizando un vector 3D normal y un valor de distancia.
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- estructura de plano
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
ms.openlocfilehash: 1479841c5e82c47e98b255d718bf1c74f50feafdec8b2bb951c43fa46cab71b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869577"
---
# <a name="plane-structure"></a>estructura de plano

Esta estructura representa un plano utilizando un vector 3D normal y un valor de distancia.

Este tipo solo está disponible en C++. Su equivalente de .NET [es System.Numerics.Plane.](/dotnet/api/system.numerics.plane?view=netframework-4.8)

## <a name="constructors"></a>Constructores

| Nombre | Descripción |
|-|-|
| `plane()` | Crea un plano sin inicializar. |
| `plane(float x, float y, float z, float d)` | Crea un plano con los valores especificados. |
| `plane(float3 normal, float d)` | Crea un plano a partir de float3 y una distancia. |
| `explicit plane(float4 value)` | Crea un plano a partir de float4. |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | Convierte un **objeto Microsoft.Graphics.Canvas.Numerics.Plane** en un plano. |

## <a name="functions"></a>Funciones

| Nombre | Descripción |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | Crea un plano a partir de un conjunto de tres posiciones de vértice, que deben ser diferentes y no estar en una línea recta. |
| `plane normalize(plane const& value)` | Cambia los coeficientes del vector normal de un plano para que sea de longitud de unidad. |
| `plane transform(plane const& plane, float4x4 const& matrix)` | Transforma un plano normalizado mediante una matriz. |
| `plane transform(plane const& plane, quaternion const& rotation)` | Transforma un plano normalizado mediante una rotación de cuaternión. |
| `float dot(plane const& plane, float4 const& value)` | Calcula el producto de punto de un plano con un vector. |
| `float dot_coordinate(plane const& plane, float3 const& value)` | Calcula el producto de punto de un plano con una coordenada float3. A diferencia \_ del punto normal, este cálculo incluye el valor del plano d. |
| `float dot_normal(plane const& plane, float3 const& value)` | Calcula el producto de punto de un plano con un valor float3 normal. A diferencia \_ de la coordenada de puntos, este cálculo omite el valor del plano d. |

## <a name="operators"></a>Operadores

| Nombre | Descripción |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | Determina si dos instancias del plano son iguales. |
| `bool operator!= (plane const& value1, plane const& value2)` | Determina si dos instancias del plano no son iguales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | Convierte un plano en **un objeto Microsoft.Graphics.Canvas.Numerics.Plane.** |

## <a name="fields"></a>Campos

| Nombre | Descripción |
|-|-|
| `float3 normal` | Vector normal del plano. |
| `float d` | Distancia del plano a lo largo de su normal desde el origen. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Espacio de nombres | Windows::Foundation::Numerics |
| Header | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Vea también

[API windowsnumerics.h](windowsnumerics-h-apis-portal.md)
