---
title: estructura de cuaternión (Windowsnumerics.h)
description: Vector de cuatro dimensiones, que se usa para representar una rotación.
ms.assetid: A6B25885-8ECB-4039-9DC6-41D5F3A02489
keywords:
- estructura de cuaternión
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
ms.openlocfilehash: 16688687b494fac98074ce933ba01dc194093da0ed2013b51f0bee0f41f31b3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825225"
---
# <a name="quaternion-structure"></a>quaternion (estructura)

Vector de cuatro dimensiones, que se usa para representar una rotación.

Un cuaternión puede girar eficazmente un objeto sobre el vector (x, y, z) por el ángulo theta, donde w = cos(theta/2). Normalmente, los cuaterniones se usan para la interpolación suave entre dos ángulos y para evitar el problema de bloqueo que puede producirse con los ángulos euler.

Este tipo solo está disponible en C++. Su equivalente de .NET [es System.Numerics.Quaternion.](/dotnet/api/system.numerics.quaternion?view=netframework-4.8)

## <a name="constructors"></a>Constructores

| Nombre | Descripción |
|-|-|
| `quaternion()` | Crea un cuaternión sin inicializar. |
| `quaternion(float x, float y, float z, float w)` | Crea un cuaternión con los valores especificados. |
| `quaternion(float3 vectorPart, float scalarPart)` | Crea un cuaternión a partir de float3 y escalar. |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | Convierte un **objeto Microsoft.Graphics.Canvas.Numerics.Quaternion** en un cuaternión. |

## <a name="functions"></a>Functions

| Nombre | Descripción |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | Crea un cuaternión a partir de un vector y un ángulo para girar sobre el vector. |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Crea un cuaternión a partir de los ángulos de guión, inclinación y giro especificados. |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | Crea un cuaternión a partir de una matriz de rotación. |
| `bool is_identity(quaternion const& value)` | Comprueba si se trata de un cuaternión de identidad (sin rotación). |
| `float length(quaternion const& value)` | Calcula la longitud de un cuaternión. |
| `float length_squared(quaternion const& value)` | Calcula la longitud al cuadrado de un cuaternión. |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | Calcula el producto escalar de dos cuaterniones. |
| `quaternion normalize(quaternion const& value)` | Divide cada componente de un cuaternión por la longitud del cuaternión. |
| `quaternion conjugate(quaternion const& value)` | Calcula el conjugado de un cuaternión. |
| `quaternion inverse(quaternion const& value)` | Calcula el inverso de un cuaternión. |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | Interpola entre dos cuaterniones mediante la interpolación lineal esférica. |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | Interpola linealmente entre dos cuaterniones. |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | Concatena dos cuaterniones; el resultado representa la primera rotación seguida de la segunda rotación. |

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
| `quaternion operator- (quaternion const& value)` | Invierte el signo de cada componente del cuaternión. |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | In-place agrega dos cuaterniones. |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | In-place resta un cuaternión de otro cuaternión. |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | In-place multiplica un cuaternión por otro cuaternión. |
| `quaternion& operator*= (quaternion& value1, float value2)` | La nultipia local nultiplies a un cuaternión por un valor escalar. |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | In-place divide un cuaternión por otro cuaternión. |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | Determina si dos instancias de cuaternión son iguales. |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | Determina si dos instancias de cuaternión no son iguales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | Convierte un cuaternión en **Microsoft.Graphics.Canvas.Numerics.Quaternion**. |

## <a name="fields"></a>Campos

| Nombre | Descripción |
|-|-|
| `float x` | Valor X del componente vectorial del cuaternión. |
| `float y` | Valor Y del componente vectorial del cuaternión. |
| `float z` | Valor Z del componente vectorial del cuaternión. |
| `float w` | Componente de rotación del cuaternión. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Espacio de nombres | Windows::Foundation::Numerics |
| Header | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Vea también

[API windowsnumerics.h](windowsnumerics-h-apis-portal.md)
