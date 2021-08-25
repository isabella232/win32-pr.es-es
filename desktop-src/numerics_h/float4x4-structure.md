---
title: Estructura float4x4 (Windowsnumerics.h)
description: Matriz 4x4, que se usa para transformaciones 3D.
ms.assetid: C0D2198A-B547-4153-AD02-9A47835FD272
keywords:
- Float4x4 (estructura)
topic_type:
- apiref
api_name:
- float4x4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c918ee81ddac31d697ff3885e04e8cb530cd31a98f842c109f9d281786ee2539
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825275"
---
# <a name="float4x4-structure"></a>Float4x4 (estructura)

Matriz 4x4, que se usa para transformaciones 3D.

Este tipo de matriz usa un diseño de vector de fila. Las x, y y z del vector de traducción de esta matriz corresponden a los campos m41, m42, m43.

Este tipo solo está disponible en C++. Su equivalente de .NET [es System.Numerics.Matrix4x4.](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8)

## <a name="constructors"></a>Constructores

| Nombre | Descripción |
|-|-|
| `float4x4()` | Crea un elemento float4x4 no inicializado. |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | Crea un float4x4 con los valores especificados. |
| `explicit float4x4(float3x2 value)` | Crea un float4x4 a partir de float3x2. |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | Convierte **Microsoft.Graphics.Canvas.Numerics.Matrix4x4** en float4x4. |

## <a name="functions"></a>Funciones

| Nombre | Descripción |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | Crea un giro esférico que gira alrededor de una posición de objeto especificada, mediante un sistema de coordenadas con la mano derecha. |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | Crea una rotación cilíndrica que gira alrededor de un eje especificado, mediante un sistema de coordenadas con la mano derecha. |
| `float4x4 make_float4x4_translation(float3 const& position)` | Crea una matriz de traslación. |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | Crea una matriz de traslación. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | Crea una matriz de escalado centrada en el origen. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | Crea una matriz de escalado, centrada en el punto especificado. |
| `float4x4 make_float4x4_scale(float3 const& scales)` | Crea una matriz de escalado centrada en el origen. |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | Crea una matriz de escalado, centrada en el punto especificado. |
| `float4x4 make_float4x4_scale(float scale)` | Crea una matriz de escalado centrada en el origen. |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | Crea una matriz de escalado, centrada en el punto especificado. |
| `float4x4 make_float4x4_rotation_x(float radians)` | Crea una matriz de rotación del eje X, centrada en el origen. |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | Crea una matriz de rotación del eje X, centrada en el punto especificado. |
| `float4x4 make_float4x4_rotation_y(float radians)` | Crea una matriz de rotación del eje Y, centrada en el origen. |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | Crea una matriz de rotación del eje Y, centrada en el punto especificado. |
| `float4x4 make_float4x4_rotation_z(float radians)` | Crea una matriz de rotación del eje Z, centrada en el origen. |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | Crea una matriz de rotación del eje Z, centrada en el punto especificado. |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | Crea una matriz que gira en torno a un vector arbitrario. |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | Crea una matriz de proyección de perspectiva basada en un campo de vista, mediante un sistema de coordenadas con la mano derecha. |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | Crea una matriz de proyección de perspectiva mediante un sistema de coordenadas con la mano derecha. |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | Crea una matriz de proyección de perspectiva personalizada, mediante un sistema de coordenadas con la mano derecha. |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | Crea una matriz de proyección ortográfica mediante un sistema de coordenadas con la mano derecha. |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | Crea una matriz de proyección ortográfica personalizada, mediante un sistema de coordenadas con la mano derecha. |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | Crea una matriz de vistas mediante un sistema de coordenadas con la mano derecha. |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | Crea una matriz mundial con un sistema de coordenadas con la mano derecha. Se puede usar para colocar objetos en el espacio 3D. |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | Crea una matriz de rotación a partir de un cuaternión. |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Crea una matriz de rotación a partir de un yaw, pitch y roll especificados. |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | Crea una matriz que aplana la geometría en un plano especificado como si proyectara una sombra desde una fuente de luz especificada. |
| `float4x4 make_float4x4_reflection(plane const& value)` | Crea una matriz que refleja el sistema de coordenadas sobre un plano especificado. |
| `bool is_identity(float4x4 const& value)` | Comprueba si se trata de una matriz de identidad. |
| `float determinant(float4x4 const& value)` | Calcula el determinante de la matriz. |
| `float3 translation(float4x4 const& value)` | Obtiene el vector de traducción de la matriz. |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | Calcula el inverso de una matriz. Devuelve true si se puede invertir la matriz; False en caso contrario. |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | Extrae los componentes escalares, de traducción y de rotación de una matriz de escala, rotación y traducción (SRT) 3D. Devuelve true si la matriz se puede descomponer; False en caso contrario. |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | Transforma una matriz aplicando una rotación de cuaternión. |
| `float4x4 transpose(float4x4 const& matrix)` | Transpone los componentes de una matriz a lo largo de su diagonal. |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | Interpola linealmente entre los valores correspondientes de dos matrices. |

## <a name="methods"></a>Métodos

| Nombre | Descripción |
|-|-|
| `static float4x4 identity()` | Devuelve una instancia de la matriz de identidad. |

## <a name="operators"></a>Operadores

| Nombre | Descripción |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | Agrega cada componente de una matriz a otra matriz. |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | Resta cada componente de una matriz de otra matriz. |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | Multiplica una matriz por otra matriz. Esto tiene el efecto de concatenar dos transformaciones. |
| `float4x4 operator* (float4x4 const& value1, float value2)` | Multiplica cada componente de una matriz por un valor escalar. |
| `float4x4 operator- (float4x4 const& value)` | Niega cada componente de una matriz. |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | In-place agrega cada componente de una matriz a otra matriz. |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | In-place resta cada componente de una matriz de otra matriz. |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | In-place multiplica una matriz por otra matriz. Esto tiene el efecto de concatenar dos transformaciones. |
| `float4x4& operator*= (float4x4& value1, float value2)` | In-place multiplica cada componente de una matriz por un valor escalar. |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | Determina si dos instancias de float4x4 son iguales. |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | Determina si dos instancias de float4x4 no son iguales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | Convierte float4x4 en **Microsoft.Graphics.Canvas.Numerics.Matrix4x4**. |

## <a name="fields"></a>Campos

| Nombre | Descripción |
|-|-|
| `float m11` | Valor en la fila 1 columna 1 de la matriz. |
| `float m12` | Valor en la fila 1 columna 2 de la matriz. |
| `float m13` | Valor en la fila 1 columna 3 de la matriz. |
| `float m14` | Valor en la fila 1 columna 4 de la matriz. |
| `float m21` | Valor en la fila 2 columna 1 de la matriz. |
| `float m22` | Valor de la fila 2, columna 2 de la matriz. |
| `float m23` | Valor en la fila 2, columna 3 de la matriz. |
| `float m24` | Valor en la fila 2 columna 4 de la matriz. |
| `float m31` | Valor de la fila 3, columna 1 de la matriz. |
| `float m32` | Valor de la fila 3, columna 2 de la matriz. |
| `float m33` | Valor de la fila 3, columna 3 de la matriz. |
| `float m34` | Valor en la fila 3 columna 4 de la matriz. |
| `float m41` | Valor de la fila 4, columna 1 de la matriz. |
| `float m42` | Valor de la fila 4, columna 2 de la matriz. |
| `float m43` | Valor en la fila 4, columna 3 de la matriz. |
| `float m44` | Valor de la fila 4, columna 4 de la matriz. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Espacio de nombres | Windows::Foundation::Numerics |
| Header | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Vea también

[API windowsnumerics.h](windowsnumerics-h-apis-portal.md)
