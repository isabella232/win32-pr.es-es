---
title: mul
description: Multiplica x e y mediante matemáticas de matriz. Las columnas x e y de la dimensión interna deben ser iguales.
ms.assetid: 9945388a-d802-4dbe-bdb7-4eadb8751c39
keywords:
- mul HLSL
topic_type:
- apiref
api_name:
- mul
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6362c734cbbf30defa8fed75f28c6f39397d75977488d9efc170d2647a9b3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950365"
---
# <a name="mul"></a>mul

Multiplica x e y mediante matemáticas de matriz. Las columnas x e y de la dimensión interna deben ser iguales.



| ret mul(x, y) |
|---------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                                                           |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El valor de entrada x. Si x es un vector, se trata como un vector de fila.<br/>    |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[en \] El valor de entrada y . Si y es un vector, se trata como un vector de columna.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Resultado de x veces y. El resultado tiene la dimensión x-rows x y-columns.

## <a name="type-description"></a>Descripción del tipo

Hay 9 versiones sobrecargadas de esta función; las versiones sobrecargadas controlan los distintos casos de los tipos y tamaños de los argumentos de entrada.



| Versión | Nombre | Propósito | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md) | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                                                                     |
|---------|------|---------|---------------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------|
| 1       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | escalar                                                        | igual que la entrada x                                                | 1                                                                        |
|         | Ret  | out     | escalar                                                        | igual que la entrada x                                                | 1                                                                        |
| 2       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | vector                                                        | float, int                                                     | cualquiera                                                                      |
|         | Ret  | out     | vector                                                        | float, int                                                     | mismas dimensiones que la entrada y                                             |
| 3       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | matriz                                                        | float, int                                                     | cualquiera                                                                      |
|         | Ret  | out     | matriz                                                        | igual que la entrada y                                                | mismas dimensiones que la entrada y                                             |
| 4       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vector                                                        | float, int                                                     | cualquiera                                                                      |
|         | y    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | Ret  | out     | vector                                                        | float, int                                                     | mismas dimensiones que la entrada x                                             |
| 5       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vector                                                        | float, int                                                     | cualquiera                                                                      |
|         | y    | in      | vector                                                        | float, int                                                     | las mismas dimensiones que la entrada x                                             |
|         | Ret  | out     | escalar                                                        | float, int                                                     | 1                                                                        |
| 6       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vector                                                        | float, int                                                     | cualquiera                                                                      |
|         | y    | in      | matriz                                                        | float, int                                                     | rows = same dimension(s) as input x, columns = any                       |
|         | Ret  | out     | vector                                                        | float, int                                                     | mismas dimensiones que las columnas de entrada y                                     |
| 7       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matriz                                                        | float, int                                                     | cualquiera                                                                      |
|         | y    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | Ret  | out     | matriz                                                        | float, int                                                     | las mismas dimensiones que la entrada x                                             |
| 8       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matriz                                                        | float, int                                                     | cualquiera                                                                      |
|         | y    | in      | vector                                                        | float, int                                                     | número de columnas en la entrada x                                             |
|         | Ret  | out     | vector                                                        | float, int                                                     | número de filas en la entrada x                                                |
| 9       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matriz                                                        | float, int                                                     | cualquiera                                                                      |
|         | y    | in      | matriz                                                        | float, int                                                     | rows = número de columnas en la entrada x                                      |
|         | Ret  | out     | matriz                                                        | float, int                                                     | rows = number of rows in input x, columns = number of columns in input y |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) y modelos de sombreador superiores | Sí       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





