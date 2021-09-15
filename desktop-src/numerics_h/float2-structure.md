---
title: Estructura float2 (Windowsnumerics.h)
description: Vector con dos componentes.
ms.assetid: 1A23C1E3-F34F-4249-80EA-92A13CD4B34F
keywords:
- float2 (estructura)
topic_type:
- apiref
api_name:
- float2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72398bdc087e0f7a0845703a2cefea40b5465b21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574712"
---
# <a name="float2-structure"></a>float2 (estructura)

Vector con dos componentes.

Este tipo solo está disponible en C++. Su equivalente de .NET [es System.Numerics.Vector2.](/dotnet/api/system.numerics.vector2?view=netframework-4.8)

## <a name="constructors"></a>Constructores

| Nombre | Descripción |
|-|-|
| `float2()` | Crea un valor float2 no inicializado. |
| `float2(float x, float y)` | Crea un objeto float2 con los valores especificados. |
| `explicit float2(float value)` | Crea un elemento float2 con todos los componentes establecidos en el valor especificado. |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | Convierte un **objeto Microsoft.Graphics.Canvas.Numerics.Vector2** en float2. |
| `float2(Windows::Foundation::Point const& value)` | Convierte un [**Windows. Foundation.Point**](/uwp/api/Windows.Foundation.Point) a float2. |
| `float2(Windows::Foundation::Size const& value)` | Convierte un [**Windows. Foundation.Size**](/uwp/api/Windows.Foundation.Size) a float2. |

## <a name="functions"></a>Functions

| Nombre | Descripción |
|-|-|
| `float length(float2 const& value)` | Calcula la longitud, o distancia euclidana, del vector. |
| `float length_squared(float2 const& value)` | Calcula la longitud, o distancia euclidana, del vector al cuadrado. |
| `float distance(float2 const& value1, float2 const& value2)` | Calcula la distancia euclidana entre dos vectores. |
| `float distance_squared(float2 const& value1, float2 const& value2)` | Calcula la distancia euclidana entre dos vectores al cuadrado. |
| `float dot(float2 const& value1, float2 const& value2)` | Calcula el producto de puntos de dos vectores. |
| `float2 normalize(float2 const& value)` | Crea un vector de unidad a partir del vector especificado. |
| `float2 reflect(float2 const& vector, float2 const& normal)` | Determina el vector de reflexión del vector especificado y normal. |
| `float2 min(float2 const& value1, float2 const& value2)` | Devuelve un vector que contiene el valor más bajo de cada par de componentes correspondiente. |
| `float2 max(float2 const& value1, float2 const& value2)` | Devuelve un vector que contiene el valor más alto de cada par de componentes correspondiente. |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | Restringe un valor para que esté dentro de un intervalo especificado. |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | Realiza una interpolación lineal entre dos vectores. |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | Transforma el vector (x, y, 0, 1) por la matriz especificada. |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | Transforma el vector (x, y, 0, 1) por la matriz especificada. |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | Transforma el vector normal (x, y, 0, 0) por la matriz especificada. |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | Transforma el vector normal (x, y, 0, 0) por la matriz especificada. |
| `float2 transform(float2 const& value, quaternion const& rotation)` | Transforma un valor float2 por el cuaternión dado. |

## <a name="methods"></a>Métodos

| Nombre | Descripción |
|-|-|
| `static float2 zero()` | Devuelve un valor float2 con todos sus componentes establecidos en cero. |
| `static float2 one()` | Devuelve un valor float2 con todos sus componentes establecidos en uno. |
| `static float2 unit_x()` | Devuelve float2 (1, 0). |
| `static float2 unit_y()` | Devuelve float2 (0, 1). |

## <a name="operators"></a>Operadores

| Nombre | Descripción |
|-|-|
| `operator Windows::Foundation::Point() const` | Convierte un valor float2 en un [**Windows. Foundation.Point**](/uwp/api/Windows.Foundation.Point). |
| `operator Windows::Foundation::Size() const` | Convierte float2 en un [**Windows. Foundation.Size**](/uwp/api/Windows.Foundation.Size). |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | Agrega dos vectores. |
| `float2 operator- (float2 const& value1, float2 const& value2)` | Resta un vector de un vector. |
| `float2 operator* (float2 const& value1, float2 const& value2)` | Multiplica los componentes de dos vectores entre sí. |
| `float2 operator* (float2 const& value1, float value2)` | Multiplica un vector por un valor escalar. |
| `float2 operator* (float value1, float2 const& value2)` | Multiplica un vector por un valor escalar. |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | Divide los componentes de un vector entre los componentes de otro vector. |
| `float2 operator/ (float2 const& value1, float value2)` | Divide un vector por un valor escalar. |
| `float2 operator- (float2 const& value)` | Devuelve un vector que apunta en la dirección opuesta. |
| `float2& operator+= (float2& value1, float2 const& value2)` | In-place agrega dos vectores. |
| `float2& operator-= (float2& value1, float2 const& value2)` | In-place resta un vector de un vector. |
| `float2& operator*= (float2& value1, float2 const& value2)` | In-place multiplica los componentes de dos vectores entre sí. |
| `float2& operator*= (float2& value1, float value2)` | In-place multiplica un vector por un valor escalar. |
| `float2& operator/= (float2& value1, float2 const& value2)` | In-place divide los componentes de un vector entre los componentes de otro vector. |
| `float2& operator/= (float2& value1, float value2)` | In-place divide un vector por un valor escalar. |
| `bool operator== (float2 const& value1, float2 const& value2)` | Determina si dos instancias de float2 son iguales. |
| `bool operator!= (float2 const& value1, float2 const& value2)` | Determina si dos instancias de float2 no son iguales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | Convierte float2 en **Microsoft.Graphics.Canvas.Numerics.Vector2.** |

## <a name="fields"></a>Campos

| Nombre | Descripción |
|-|-|
| `float x` | Componente X del vector. |
| `float y` | Componente Y del vector. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Espacio de nombres | Windows::Foundation::Numerics |
| Encabezado | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Consulte también

[API windowsnumerics.h](windowsnumerics-h-apis-portal.md)
