---
title: Estructura float4 (Windowsnumerics.h)
description: Vector con cuatro componentes.
ms.assetid: AC07C6D0-E7FD-4582-B40D-4838F49FB8B4
keywords:
- float4 (estructura)
topic_type:
- apiref
api_name:
- float4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb1af9bee9a571abf58fb20539945effc3ff1ee81cbb48a4d90c1510aebcd4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825285"
---
# <a name="float4-structure"></a>float4 (estructura)

Vector con cuatro componentes.

Este tipo solo está disponible en C++. Su equivalente de .NET [es System.Numerics.Vector4.](/dotnet/api/system.numerics.vector4?view=netframework-4.8)

## <a name="constructors"></a>Constructores

| Nombre | Descripción |
|-|-|
| `float4()` | Crea un valor float4 no inicializado. |
| `float4(float x, float y, float z, float w)` | Crea un elemento float4 con los valores especificados. |
| `float4(float2 value, float z, float w)` | Crea un float4 con x e y copiados de float2 más los valores z y w especificados. |
| `float4(float3 value, float w)` | Crea un elemento float4 con x, y y z copiados de float3 más el valor w especificado. |
| `explicit float4(float value)` | Crea un elemento float4 con todos los com.ents establecidos en el valor especificado. |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | Convierte un **objeto Microsoft.Graphics.Canvas.Numerics.Vector4** en float4. |

## <a name="functions"></a>Funciones

| Nombre | Descripción |
|-|-|
| `float length(float4 const& value)` | Calcula la longitud, o distancia euclidana, del vector. |
| `float length_squared(float4 const& value)` | Calcula la longitud, o distancia euclidana, del vector al cuadrado. |
| `float distance(float4 const& value1, float4 const& value2)` | Calcula la distancia euclidana entre dos vectores. |
| `float distance_squared(float4 const& value1, float4 const& value2)` | Calcula la distancia euclidana entre dos vectores al cuadrado. |
| `float dot(float4 const& vector1, float4 const& vector2)` | Calcula el producto de puntos de dos vectores. |
| `float4 normalize(float4 const& vector)` | Crea un vector de unidad a partir del vector especificado. |
| `float4 min(float4 const& value1, float4 const& value2)` | Devuelve un vector que contiene el valor más bajo de cada par de componentes correspondiente. |
| `float4 max(float4 const& value1, float4 const& value2)` | Devuelve un vector que contiene el valor más alto de cada par de componentes correspondiente. |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | Restringe un valor para que esté dentro de un intervalo especificado. |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | Realiza una interpolación lineal entre dos vectores. |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | Transforma un valor float4 por la matriz dada. |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | Transforma un valor float3 por la matriz dada y devuelve float4. |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | Transforma un valor float2 por la matriz dada y devuelve float4. |
| `float4 transform(float4 const& value, quaternion const& rotation)` | Transforma un valor float4 por el cuaternión dado. |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | Transforma un valor float3 por el cuaternión dado y devuelve float4. |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | Transforma un valor float2 por el cuaternión dado y devuelve un valor float4. |

## <a name="methods"></a>Métodos

| Nombre | Descripción |
|-|-|
| `static float4 zero()` | Devuelve un valor float4 con todos sus componentes establecidos en cero. |
| `static float4 one()` | Devuelve un valor float4 con todos sus componentes establecidos en uno. |
| `static float4 unit_x()` | Devuelve float4 (1, 0, 0, 0). |
| `static float4 unit_y()` | Devuelve float4 (0, 1, 0, 0). |
| `static float4 unit_z()` | Devuelve float4 (0, 0, 1, 0). |
| `static float4 unit_w()` | Devuelve float4 (0, 0, 0, 1). |

## <a name="operators"></a>Operadores

| Nombre | Descripción |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | Agrega dos vectores. |
| `float4 operator- (float4 const& value1, float4 const& value2)` | Resta un vector de un vector. |
| `float4 operator* (float4 const& value1, float4 const& value2)` | Multiplica los componentes de dos vectores entre sí. |
| `float4 operator* (float4 const& value1, float value2)` | Multiplica un vector por un valor escalar. |
| `float4 operator* (float value1, float4 const& value2)` | Multiplica un vector por un valor escalar. |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | Divide los componentes de un vector entre los componentes de otro vector. |
| `float4 operator/ (float4 const& value1, float value2)` | Divide un vector por un valor escalar. |
| `float4 operator- (float4 const& value)` | Devuelve un vector que apunta en la dirección opuesta. |
| `float4& operator+= (float4& value1, float4 const& value2)` | In-place agrega dos vectores. |
| `float4& operator-= (float4& value1, float4 const& value2)` | In-place resta un vector de un vector. |
| `float4& operator*= (float4& value1, float4 const& value2)` | In-place multiplica los componentes de dos vectores entre sí. |
| `float4& operator*= (float4& value1, float value2)` | In-place multiplica un vector por un valor escalar. |
| `float4& operator/= (float4& value1, float4 const& value2)` | In-place divide los componentes de un vector entre los componentes de otro vector. |
| `float4& operator/= (float4& value1, float value2)` | In-place divide un vector por un valor escalar. |
| `bool operator== (float4 const& value1, float4 const& value2)` | Determina si dos instancias de float4 son iguales. |
| `bool operator!= (float4 const& value1, float4 const& value2)` | Determina si dos instancias de float4 no son iguales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | Convierte float4 en **Microsoft.Graphics.Canvas.Numerics.Vector4.** |

## <a name="fields"></a>Campos

| Nombre | Descripción |
|-|-|
| `float x` | Componente X del vector. |
| `float y` | Componente Y del vector. |
| `float z` | Componente Z del vector. |
| `float w` | Componente W del vector. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Espacio de nombres | Windows::Foundation::Numerics |
| Header | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Vea también

[API windowsnumerics.h](windowsnumerics-h-apis-portal.md)
