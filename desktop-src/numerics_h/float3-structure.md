---
title: Estructura float3 (Windowsnumerics.h)
description: Vector con tres componentes.
ms.assetid: CAA10ADA-C5A8-4B75-A0A9-5C5B3FDD9A07
keywords:
- float3 (estructura)
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
ms.openlocfilehash: 521c63f99c35e68f18d9a6c0a81118f647ff131effb0f6528e2ef3882c43e234
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939524"
---
# <a name="float3-structure"></a>float3 (estructura)

Vector con tres componentes.

Este tipo solo está disponible en C++. Su equivalente de .NET [es System.Numerics.Vector3.](/dotnet/api/system.numerics.vector3?view=netframework-4.8)

## <a name="constructors"></a>Constructores

| Nombre | Descripción |
|-|-|
| `float3()` | Crea un elemento float3 sin inicializar. |
| `float3(float x, float y, float z)` | Crea un objeto float3 con los valores especificados. |
| `float3(float2 value, float z)` | Crea un float3 con x e y copiados de float2 más el valor z especificado. |
| `explicit float3(float value)` | Crea un float3 con todos los componentes establecidos en el valor especificado. |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | Convierte un **objeto Microsoft.Graphics.Canvas.Numerics.Vector3** en float3. |

## <a name="functions"></a>Funciones

| Nombre | Descripción |
|-|-|
| `float length(float3 const& value)` | Calcula la longitud, o distancia euclidana, del vector. |
| `float length_squared(float3 const& value)` | Calcula la longitud, o distancia euclidana, del vector al cuadrado. |
| `float distance(float3 const& value1, float3 const& value2)` | Calcula la distancia euclideña entre dos vectores. |
| `float distance_squared(float3 const& value1, float3 const& value2)` | Calcula la distancia euclidana entre dos vectores al cuadrado. |
| `float dot(float3 const& vector1, float3 const& vector2)` | Calcula el producto de punto de dos vectores. |
| `float3 normalize(float3 const& value)` | Crea un vector de unidad a partir del vector especificado. |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | Calcula el producto vectorial de dos vectores. |
| `float3 reflect(float3 const& vector, float3 const& normal)` | Determina el vector de reflexión del vector especificado y normal. |
| `float3 min(float3 const& value1, float3 const& value2)` | Devuelve un vector que contiene el valor más bajo de cada par de componentes correspondiente. |
| `float3 max(float3 const& value1, float3 const& value2)` | Devuelve un vector que contiene el valor más alto de cada par de componentes correspondiente. |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | Restringe un valor para que esté dentro de un intervalo especificado. |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | Realiza una interpolación lineal entre dos vectores. |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | Transforma el vector (x, y, z, 1) por la matriz especificada. |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | Transforma el vector normal (x, y, z, 0) por la matriz especificada. |
| `float3 transform(float3 const& value, quaternion const& rotation)` | Transforma un valor float3 por el cuaternión dado. |

## <a name="methods"></a>Métodos

| Nombre | Descripción |
|-|-|
| `static float3 zero()` | Devuelve un valor float3 con todos sus componentes establecidos en cero. |
| `static float3 one()` | Devuelve un valor float3 con todos sus componentes establecidos en uno. |
| `static float3 unit_x()` | Devuelve float3 (1, 0, 0). |
| `static float3 unit_y()` | Devuelve float3 (0, 1, 0). |
| `static float3 unit_z()` | Devuelve float3 (0, 0, 1). |

## <a name="operators"></a>Operadores

| Nombre | Descripción |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | Agrega dos vectores. |
| `float3 operator- (float3 const& value1, float3 const& value2)` | Resta un vector de un vector. |
| `float3 operator* (float3 const& value1, float3 const& value2)` | Multiplica los componentes de dos vectores entre sí. |
| `float3 operator* (float3 const& value1, float value2)` | Multiplica un vector por un escalar. |
| `float3 operator* (float value1, float3 const& value2)` | Multiplica un vector por un escalar. |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | Divide los componentes de un vector entre los componentes de otro vector. |
| `float3 operator/ (float3 const& value1, float value2)` | Divide un vector por un valor escalar. |
| `float3 operator- (float3 const& value)` | Devuelve un vector que apunta en la dirección opuesta. |
| `float3& operator+= (float3& value1, float3 const& value2)` | In-place agrega dos vectores. |
| `float3& operator-= (float3& value1, float3 const& value2)` | In-place resta un vector de un vector. |
| `float3& operator*= (float3& value1, float3 const& value2)` | In-place multiplica los componentes de dos vectores entre sí. |
| `float3& operator*= (float3& value1, float value2)` | In-place multiplica un vector por un escalar. |
| `float3& operator/= (float3& value1, float3 const& value2)` | In-place divide los componentes de un vector entre los componentes de otro vector. |
| `float3& operator/= (float3& value1, float value2)` | In-place divide un vector por un valor escalar. |
| `bool operator== (float3 const& value1, float3 const& value2)` | Determina si dos instancias de float3 son iguales. |
| `bool operator!= (float3 const& value1, float3 const& value2)` | Determina si dos instancias de float3 no son iguales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | Convierte float3 en **Microsoft.Graphics.Canvas.Numerics.Vector3.** |

## <a name="fields"></a>Campos

| Nombre | Descripción |
|-|-|
| `float x` | Componente X del vector. |
| `float y` | Componente Y del vector. |
| `float z` | Componente Z del vector. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Espacio de nombres | Windows::Foundation::Numerics |
| Header | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Vea también

[API de windowsnumerics.h](windowsnumerics-h-apis-portal.md)
