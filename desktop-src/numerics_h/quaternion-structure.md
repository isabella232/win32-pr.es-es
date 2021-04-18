---
title: estructura cuaternión (Windowsnumerics. h)
description: Un vector de cuatro dimensiones, que se usa para representar un giro.
ms.assetid: A6B25885-8ECB-4039-9DC6-41D5F3A02489
keywords:
- cuaternión (estructura)
topic_type:
- apiref
api_name:
- quaternion structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ae169232f83e6753505f9d5d07fffac09e67e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721608"
---
# <a name="quaternion-structure"></a>cuaternión (estructura)

Un vector de cuatro dimensiones, que se usa para representar un giro.

Un cuaternión puede girar de forma eficaz un objeto sobre el vector (x, y, z) en el ángulo Theta, donde w = cos (Theta/2). Los cuaterniones se suelen usar para la interpolación suave entre dos ángulos y para evitar el problema de bloqueo de gimbal que puede producirse con los ángulos de Euler.

Este tipo solo está disponible en C++. Su equivalente de .NET es [System. Numerics. Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).

## <a name="constructors"></a>Constructores

| Nombre | Descripción |
|-|-|
| `quaternion()` | Crea un cuaternión no inicializado. |
| `quaternion(float x, float y, float z, float w)` | Crea un cuaternión con los valores especificados. |
| `quaternion(float3 vectorPart, float scalarPart)` | Crea un cuaternión a partir de un float3 y un valor escalar. |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | Convierte un **valor de Microsoft. Graphics. Canvas. Numerics. cuaternión** en un cuaternión. |

## <a name="functions"></a>Functions

| Nombre | Descripción |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | Crea un cuaternión a partir de un vector y un ángulo para girar sobre el vector. |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Crea un cuaternión a partir de los ángulos de guiñada, de brea y de rollo especificados. |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | Crea un cuaternión a partir de una matriz de rotación. |
| `bool is_identity(quaternion const& value)` | Comprueba si se trata de un cuaternión de identidad (sin giro). |
| `float length(quaternion const& value)` | Calcula la longitud de un cuaternión. |
| `float length_squared(quaternion const& value)` | Calcula la longitud cuadrada de un cuaternión. |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | Calcula el producto escalar de dos cuaterniones. |
| `quaternion normalize(quaternion const& value)` | Divide cada componente de un cuaternión por la longitud del cuaternión. |
| `quaternion conjugate(quaternion const& value)` | Calcula el conjugado de un cuaternión. |
| `quaternion inverse(quaternion const& value)` | Calcula el inverso de un cuaternión. |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | Interpola entre dos cuaterniones mediante la interpolación lineal esférica. |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | Interpola linealmente entre dos cuaterniones. |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | Concatena dos cuaterniones; el resultado representa el primer giro seguido del segundo giro. |

## <a name="methods"></a>Métodos

| Nombre | Descripción |
|-|-|
| `static quaternion identity()` | Devuelve una instancia del cuaternión de identidad. |

## <a name="operators"></a>Operadores

| Nombre | Descripción |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | Agrega dos cuaterniones. |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | Resta un cuaternión de otro cuaternión. |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | Multiplica un cuaternión por otro cuaternión. |
| `quaternion operator* (quaternion const& value1, float value2)` | Multiplica un cuaternión por un valor escalar. |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | Divide un cuaternión por otro cuaternión. |
| `quaternion operator- (quaternion const& value)` | Voltea el signo de cada componente del cuaternión. |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | En contexto agrega dos cuaterniones. |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | En contexto resta un cuaternión de otro cuaternión. |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | En contexto multiplica un cuaternión por otro cuaternión. |
| `quaternion& operator*= (quaternion& value1, float value2)` | En contexto, nultiplies un cuaternión por un valor escalar. |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | En contexto divide un cuaternión por otro cuaternión. |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | Determina si dos instancias de Quaternion son iguales. |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | Determina si dos instancias de Quaternion no son iguales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | Convierte un cuaternión en **Microsoft. Graphics. Canvas. Numerics. Quaternion**. |

## <a name="fields"></a>Campos

| Nombre | Descripción |
|-|-|
| `float x` | Valor X del componente de vector del cuaternión. |
| `float y` | Valor Y del componente de vector del cuaternión. |
| `float z` | Valor Z del componente de vector del cuaternión. |
| `float w` | Componente de rotación del cuaternión. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Espacio de nombres | Windows:: Foundation:: Numerics |
| Encabezado | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Vea también

[API de windowsnumerics. h](windowsnumerics-h-apis-portal.md)
