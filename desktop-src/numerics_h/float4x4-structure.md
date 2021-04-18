---
title: estructura float4x4 (Windowsnumerics. h)
description: Matriz 4x4 utilizada para las transformaciones 3D.
ms.assetid: C0D2198A-B547-4153-AD02-9A47835FD272
keywords:
- estructura float4x4
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
ms.openlocfilehash: 71c91de5eef404db33eff118568540be912d551d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721610"
---
# <a name="float4x4-structure"></a>estructura float4x4

Matriz 4x4 utilizada para las transformaciones 3D.

Este tipo de matriz utiliza un diseño de vector de fila. Los valores x, y y z del vector de conversión de esta matriz se corresponden con los campos M41, M42, M43.

Este tipo solo está disponible en C++. Su equivalente de .NET es [System. Numerics. Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).

## <a name="constructors"></a>Constructores

| Nombre | Descripción |
|-|-|
| `float4x4()` | Crea un float4x4 no inicializado. |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | Crea un float4x4 con los valores especificados. |
| `explicit float4x4(float3x2 value)` | Crea un float4x4 a partir de un float3x2. |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | Convierte un **Microsoft. Graphics. Canvas. Numerics. Matrix4x4** en float4x4. |

## <a name="functions"></a>Functions

| Nombre | Descripción |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | Crea una cartelera esférica que gira en torno a la posición de un objeto especificado, utilizando un sistema de coordenadas de la mano derecha. |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | Crea una cartelera cilíndrica que gira en torno a un eje especificado, utilizando un sistema de coordenadas de la mano derecha. |
| `float4x4 make_float4x4_translation(float3 const& position)` | Crea una matriz de traslación. |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | Crea una matriz de traslación. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | Crea una matriz de escala, centrada en el origen. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | Crea una matriz de escala, centrada en el punto especificado. |
| `float4x4 make_float4x4_scale(float3 const& scales)` | Crea una matriz de escala, centrada en el origen. |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | Crea una matriz de escala, centrada en el punto especificado. |
| `float4x4 make_float4x4_scale(float scale)` | Crea una matriz de escala, centrada en el origen. |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | Crea una matriz de escala, centrada en el punto especificado. |
| `float4x4 make_float4x4_rotation_x(float radians)` | Crea una matriz de rotación del eje x, centrada en el origen. |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | Crea una matriz de rotación del eje x, centrada en el punto especificado. |
| `float4x4 make_float4x4_rotation_y(float radians)` | Crea una matriz de rotación del eje y, centrada en el origen. |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | Crea una matriz de rotación del eje y, centrada en el punto especificado. |
| `float4x4 make_float4x4_rotation_z(float radians)` | Crea una matriz de rotación del eje z, centrada en el origen. |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | Crea una matriz de rotación del eje z, centrada en el punto especificado. |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | Crea una matriz que gira en torno a un vector arbitrario. |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | Crea una matriz de proyección en perspectiva basada en un campo de vista, utilizando un sistema de coordenadas de la mano derecha. |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | Crea una matriz de proyección en perspectiva con un sistema de coordenadas de la mano derecha. |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | Crea una matriz de proyección en perspectiva personalizada mediante un sistema de coordenadas de la mano derecha. |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | Crea una matriz de proyección ortográfica mediante un sistema de coordenadas de la mano derecha. |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | Crea una matriz de proyección ortográfica personalizada mediante un sistema de coordenadas de la mano derecha. |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | Crea una matriz de vista mediante un sistema de coordenadas de la mano derecha. |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | Crea una matriz universal mediante un sistema de coordenadas de la mano derecha. Se puede usar para colocar objetos en el espacio 3D. |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | Crea una matriz de rotación a partir de un cuaternión. |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Crea una matriz de rotación a partir de una guiñada, un tono y un rollo especificados. |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | Crea una matriz que aplana la geometría en un plano especificado como si proyectara una sombra desde una fuente de luz especificada. |
| `float4x4 make_float4x4_reflection(plane const& value)` | Crea una matriz que refleja el sistema de coordenadas sobre un plano especificado. |
| `bool is_identity(float4x4 const& value)` | Comprueba si se trata de una matriz de identidad. |
| `float determinant(float4x4 const& value)` | Calcula el factor determinante de la matriz. |
| `float3 translation(float4x4 const& value)` | Obtiene el vector de traslación de la matriz. |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | Calcula el inverso de una matriz. Devuelve true si se puede invertir la matriz; de lo contrario, false. |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | Extrae los componentes escalar, traslación y rotación de una matriz de escala 3D/giro/traslación (SRT). Devuelve true si la matriz se puede descomponer; de lo contrario, false. |
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
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | Resta todos los componentes de una matriz de otra matriz. |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | Multiplica una matriz por otra matriz. Esto tiene el efecto de concatenar dos transformaciones. |
| `float4x4 operator* (float4x4 const& value1, float value2)` | Multiplica cada componente de una matriz por un valor escalar. |
| `float4x4 operator- (float4x4 const& value)` | Niega cada componente de una matriz. |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | En contexto agrega cada componente de una matriz a otra matriz. |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | En contexto resta cada componente de una matriz de otra matriz. |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | En contexto multiplica una matriz por otra matriz. Esto tiene el efecto de concatenar dos transformaciones. |
| `float4x4& operator*= (float4x4& value1, float value2)` | En contexto multiplica cada componente de una matriz por un valor escalar. |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | Determina si dos instancias de float4x4 son iguales. |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | Determina si dos instancias de float4x4 no son iguales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | Convierte un float4x4 en **Microsoft. Graphics. Canvas. Numerics. Matrix4x4**. |

## <a name="fields"></a>Campos

| Nombre | Descripción |
|-|-|
| `float m11` | Valor de la fila 1 columna 1 de la matriz. |
| `float m12` | Valor de la fila 1 columna 2 de la matriz. |
| `float m13` | Valor de la fila 1 columna 3 de la matriz. |
| `float m14` | Valor de la fila 1 columna 4 de la matriz. |
| `float m21` | Valor de la fila 2 columna 1 de la matriz. |
| `float m22` | Valor de la fila 2 columna 2 de la matriz. |
| `float m23` | Valor de la fila 2 columna 3 de la matriz. |
| `float m24` | Valor de la fila 2 columna 4 de la matriz. |
| `float m31` | Valor de la fila 3 columna 1 de la matriz. |
| `float m32` | Valor de la fila 3 columna 2 de la matriz. |
| `float m33` | Valor de la fila 3 columna 3 de la matriz. |
| `float m34` | Valor de la fila 3 columna 4 de la matriz. |
| `float m41` | Valor de la fila 4 columna 1 de la matriz. |
| `float m42` | Valor de la fila 4 columna 2 de la matriz. |
| `float m43` | Valor de la fila 4 columna 3 de la matriz. |
| `float m44` | Valor de la fila 4 columna 4 de la matriz. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Espacio de nombres | Windows:: Foundation:: Numerics |
| Encabezado | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Vea también

[API de windowsnumerics. h](windowsnumerics-h-apis-portal.md)
