---
title: mul
description: Multiplica x e y utilizando la expresión matemática de matriz. Las filas x e y deben ser iguales.
ms.assetid: 9945388a-d802-4dbe-bdb7-4eadb8751c39
keywords:
- HLSL de Mul
topic_type:
- apiref
api_name:
- mul
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2e9fe545cb16f8ac1fef1935b9d7e97075521b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076530"
---
# <a name="mul"></a>mul

Multiplica x e y utilizando la expresión matemática de matriz. Las filas x e y deben ser iguales.



| RET mul (x, y) |
|---------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                                                           |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el valor de entrada x. Si x es un vector, se trata como un vector de fila.<br/>    |
| <span id="y"></span><span id="Y"></span>*sí*<br/> | \[en \] el valor de entrada y. Si y es un vector, se trata como un vector de columna.<br/> |



 

## <a name="return-value"></a>Valor devuelto

El resultado de x veces y. El resultado tiene las columnas x-Rows x y de dimensión.

## <a name="type-description"></a>Descripción del tipo

Hay 9 versiones sobrecargadas de esta función. las versiones sobrecargadas controlan los distintos casos para los tipos y tamaños de los argumentos de entrada.



| Versión | Nombre | Propósito | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md) | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                                                                     |
|---------|------|---------|---------------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------|
| 1       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | escalar                                                        | Float, int                                                     | 1                                                                        |
|         | y    | in      | escalar                                                        | igual que la entrada x                                                | 1                                                                        |
|         | direcc  | out     | escalar                                                        | igual que la entrada x                                                | 1                                                                        |
| 2       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | escalar                                                        | Float, int                                                     | 1                                                                        |
|         | y    | in      | vector                                                        | Float, int                                                     | cualquiera                                                                      |
|         | direcc  | out     | vector                                                        | Float, int                                                     | mismas dimensiones como entrada y                                             |
| 3       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | escalar                                                        | Float, int                                                     | 1                                                                        |
|         | y    | in      | matriz                                                        | Float, int                                                     | cualquiera                                                                      |
|         | direcc  | out     | matriz                                                        | igual que la entrada y                                                | mismas dimensiones como entrada y                                             |
| 4       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vector                                                        | Float, int                                                     | cualquiera                                                                      |
|         | y    | in      | escalar                                                        | Float, int                                                     | 1                                                                        |
|         | direcc  | out     | vector                                                        | Float, int                                                     | mismas dimensiones que la entrada x                                             |
| 5       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vector                                                        | Float, int                                                     | cualquiera                                                                      |
|         | y    | in      | vector                                                        | Float, int                                                     | mismas dimensiones que la entrada x                                             |
|         | direcc  | out     | escalar                                                        | Float, int                                                     | 1                                                                        |
| 6       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vector                                                        | Float, int                                                     | cualquiera                                                                      |
|         | y    | in      | matriz                                                        | Float, int                                                     | filas = mismas dimensiones que x de entrada, columnas = any                       |
|         | direcc  | out     | vector                                                        | Float, int                                                     | mismas dimensiones como columnas de entrada y                                     |
| 7       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matriz                                                        | Float, int                                                     | cualquiera                                                                      |
|         | y    | in      | escalar                                                        | Float, int                                                     | 1                                                                        |
|         | direcc  | out     | matriz                                                        | Float, int                                                     | mismas dimensiones que la entrada x                                             |
| 8       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matriz                                                        | Float, int                                                     | cualquiera                                                                      |
|         | y    | in      | vector                                                        | Float, int                                                     | número de columnas en la entrada x                                             |
|         | direcc  | out     | vector                                                        | Float, int                                                     | número de filas en la entrada x                                                |
| 9       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matriz                                                        | Float, int                                                     | cualquiera                                                                      |
|         | y    | in      | matriz                                                        | Float, int                                                     | Rows = número de columnas en la entrada x                                      |
|         | direcc  | out     | matriz                                                        | Float, int                                                     | Rows = número de filas en la entrada x, columnas = número de columnas de entrada y |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| Modelador [modelo 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) y modelos de sombreador más altos | sí       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





