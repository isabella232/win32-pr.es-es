---
title: estructura float3 (Windowsnumerics. h)
description: Vector con tres componentes.
ms.assetid: CAA10ADA-C5A8-4B75-A0A9-5C5B3FDD9A07
keywords:
- estructura float3
topic_type:
- apiref
api_name:
- float3 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae524205c900c63438a50094dcd551a4903632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721618"
---
# <a name="float3-structure"></a>estructura float3

Vector con tres componentes.

Este tipo solo está disponible en C++. Su equivalente de .NET es [System. Numerics. Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).

## <a name="constructors"></a>Constructores

| Nombre | Descripción |
|-|-|
| `float3()` | Crea un float3 no inicializado. |
| `float3(float x, float y, float z)` | Crea un float3 con los valores especificados. |
| `float3(float2 value, float z)` | Crea un float3 con x e y copiados de un float2 más el valor z especificado. |
| `explicit float3(float value)` | Crea un float3 con todos los componentes establecidos en el valor especificado. |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | Convierte un **Microsoft. Graphics. Canvas. Numerics. Vector3** en un float3. |

## <a name="functions"></a>Functions

| Nombre | Descripción |
|-|-|
| `float length(float3 const& value)` | Calcula la longitud o la distancia euclidiana del vector. |
| `float length_squared(float3 const& value)` | Calcula la longitud, o euclidiana, del vector cuadrado. |
| `float distance(float3 const& value1, float3 const& value2)` | Calcula la distancia euclidiana entre dos vectores. |
| `float distance_squared(float3 const& value1, float3 const& value2)` | Calcula la distancia euclidiana entre dos vectores con un cuadrado. |
| `float dot(float3 const& vector1, float3 const& vector2)` | Calcula el producto escalar de dos vectores. |
| `float3 normalize(float3 const& value)` | Crea un vector de unidad a partir del vector especificado. |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | Calcula el producto vectorial de dos vectores. |
| `float3 reflect(float3 const& vector, float3 const& normal)` | Determina el vector de reflejo del vector dado y el normal. |
| `float3 min(float3 const& value1, float3 const& value2)` | Devuelve un vector que contiene el valor más bajo de cada par coincidente de componentes. |
| `float3 max(float3 const& value1, float3 const& value2)` | Devuelve un vector que contiene el valor más alto de cada par coincidente de componentes. |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | Restringe un valor para que esté dentro de un intervalo especificado. |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | Realiza una interpolación lineal entre dos vectores. |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | Transforma el vector (x, y, z, 1) de la matriz especificada. |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | Transforma el vector normal (x, y, z, 0) de la matriz especificada. |
| `float3 transform(float3 const& value, quaternion const& rotation)` | Transforma un float3 por el cuaternión dado. |

## <a name="methods"></a>Métodos

| Nombre | Descripción |
|-|-|
| `static float3 zero()` | Devuelve un float3 con todos sus componentes establecidos en cero. |
| `static float3 one()` | Devuelve un float3 con todos sus componentes establecidos en uno. |
| `static float3 unit_x()` | Devuelve el float3 (1,0). |
| `static float3 unit_y()` | Devuelve float3 (0, 1, 0). |
| `static float3 unit_z()` | Devuelve float3 (0, 0, 1). |

## <a name="operators"></a>Operadores

| Nombre | Descripción |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | Agrega dos vectores. |
| `float3 operator- (float3 const& value1, float3 const& value2)` | Resta un vector de un vector. |
| `float3 operator* (float3 const& value1, float3 const& value2)` | Multiplica los componentes de dos vectores entre sí. |
| `float3 operator* (float3 const& value1, float value2)` | Multiplica un vector por un valor escalar. |
| `float3 operator* (float value1, float3 const& value2)` | Multiplica un vector por un valor escalar. |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | Divide los componentes de un vector por los componentes de otro vector. |
| `float3 operator/ (float3 const& value1, float value2)` | Divide un vector por un valor escalar. |
| `float3 operator- (float3 const& value)` | Devuelve un vector que apunta en la dirección opuesta. |
| `float3& operator+= (float3& value1, float3 const& value2)` | En contexto, agrega dos vectores. |
| `float3& operator-= (float3& value1, float3 const& value2)` | En contexto resta un vector de un vector. |
| `float3& operator*= (float3& value1, float3 const& value2)` | En contexto multiplica los componentes de dos vectores entre sí. |
| `float3& operator*= (float3& value1, float value2)` | En contexto multiplica un vector por un valor escalar. |
| `float3& operator/= (float3& value1, float3 const& value2)` | En contexto divide los componentes de un vector por los componentes de otro vector. |
| `float3& operator/= (float3& value1, float value2)` | In-Place divide un vector por un valor escalar. |
| `bool operator== (float3 const& value1, float3 const& value2)` | Determina si dos instancias de float3 son iguales. |
| `bool operator!= (float3 const& value1, float3 const& value2)` | Determina si dos instancias de float3 no son iguales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | Convierte un float3 en un **Microsoft. Graphics. Canvas. Numerics. Vector3**. |

## <a name="fields"></a>Campos

| Nombre | Descripción |
|-|-|
| `float x` | Componente X del vector. |
| `float y` | Componente Y del vector. |
| `float z` | Componente Z del vector. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Espacio de nombres | Windows:: Foundation:: Numerics |
| Encabezado | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Vea también

[API de windowsnumerics. h](windowsnumerics-h-apis-portal.md)
