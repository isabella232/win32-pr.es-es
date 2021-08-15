---
title: Estructura float3x2 (Windowsnumerics.h)
description: Matriz 3x2, que se usa para transformaciones 2D.
ms.assetid: 5C2A4C30-3EC4-4DE9-A42A-6A19F96F8D69
keywords:
- float3x2 (estructura)
topic_type:
- apiref
api_name:
- float3x2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d403446fa3544bdb001c065e9874f812a829680e19a5e6b526ed12276fd6e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971764"
---
# <a name="float3x2-structure"></a>float3x2 (estructura)

Matriz 3x2, que se usa para transformaciones 2D.

Este tipo de matriz usa un diseño de vector de fila. Las x e y del vector de traducción de esta matriz corresponden a los campos m31, m32.

Este tipo solo está disponible en C++. Su equivalente de .NET [es System.Numerics.Matrix3x2.](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8)

## <a name="constructors"></a>Constructores

| Nombre | Descripción |
|-|-|
| `float3x2()` | Crea un elemento float3x2 no inicializado. |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | Crea un objeto float3x2 con los valores especificados. |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | Convierte un **objeto Microsoft.Graphics.Canvas.Numerics.Matrix3x2** en float3x2. |

## <a name="functions"></a>Functions

| Nombre | Descripción |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | Crea una matriz de traslación. |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | Crea una matriz de traslación. |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | Crea una matriz de escalado centrada en el origen. |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | Crea una matriz de escalado, centrada en el punto especificado. |
| `float3x2 make_float3x2_scale(float2 const& scales)` | Crea una matriz de escalado centrada en el origen. |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | Crea una matriz de escalado, centrada en el punto especificado. |
| `float3x2 make_float3x2_scale(float scale)` | Crea una matriz de escalado centrada en el origen. |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | Crea una matriz de escalado, centrada en el punto especificado. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | Crea una matriz de asimetría centrada en el origen. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | Crea una matriz de asimetría centrada en el punto especificado. |
| `float3x2 make_float3x2_rotation(float radians)` | Crea una matriz de rotación centrada en el origen. |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | Crea una matriz de rotación, centrada en el punto especificado. |
| `bool is_identity(float3x2 const& value)` | Comprueba si se trata de una matriz de identidad. |
| `float determinant(float3x2 const& value)` | Calcula el determinante de la matriz. |
| `float2 translation(float3x2 const& value)` | Obtiene el vector de traducción de la matriz. |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | Calcula el inverso de una matriz. Devuelve true si se puede invertir la matriz; False en caso contrario. |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | Interpola linealmente entre los valores correspondientes de dos matrices. |

## <a name="methods"></a>Métodos

| Nombre | Descripción |
|-|-|
| `static float3x2 identity()` | Devuelve una instancia de la matriz de identidad. |

## <a name="operators"></a>Operadores

| Nombre | Descripción |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | Agrega cada componente de una matriz a otra matriz. |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | Resta cada componente de una matriz de otra matriz. |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | Multiplica una matriz por otra matriz. Esto tiene el efecto de concatenar dos transformaciones. |
| `float3x2 operator* (float3x2 const& value1, float value2)` | Multiplica cada componente de una matriz por un valor escalar. |
| `float3x2 operator- (float3x2 const& value)` | Niega cada componente de una matriz. |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | In-place agrega cada componente de una matriz a otra matriz. |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | In-place resta cada componente de una matriz de otra matriz. |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | In-place multiplica una matriz por otra matriz. Esto tiene el efecto de concatenar dos transformaciones. |
| `float3x2& operator*= (float3x2& value1, float value2)` | In-place multiplica cada componente de una matriz por un valor escalar. |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | Determina si dos instancias de float3x2 son iguales. |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | Determina si dos instancias de float3x2 no son iguales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | Convierte float3x2 en **Microsoft.Graphics.Canvas.Numerics.Matrix3x2**. |

## <a name="fields"></a>Campos

| Nombre | Descripción |
|-|-|
| `float m11` | Valor en la fila 1 columna 1 de la matriz. |
| `float m12` | Valor en la fila 1 columna 2 de la matriz. |
| `float m21` | Valor en la fila 2 columna 1 de la matriz. |
| `float m22` | Valor de la fila 2, columna 2 de la matriz. |
| `float m31` | Valor de la fila 3, columna 1 de la matriz. |
| `float m32` | Valor de la fila 3, columna 2 de la matriz. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Espacio de nombres | Windows::Foundation::Numerics |
| Header | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Consulte también

[API windowsnumerics.h](windowsnumerics-h-apis-portal.md)
