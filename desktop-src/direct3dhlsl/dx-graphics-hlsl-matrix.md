---
title: Tipo de matriz
description: Una matriz es un tipo de datos especial que contiene entre uno y dieciséis componentes. Cada componente de una matriz debe ser del mismo tipo.
ms.assetid: 728eb472-103d-4c7f-b6f6-e515fc024801
keywords:
- Tipo de matriz HLSL
topic_type:
- apiref
api_name:
- Matrix Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e6b98309c760a3da4d1e9c488e4aed049aa34f0b449042e8f00a02426cc513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726175"
---
# <a name="matrix-type"></a>Tipo de matriz

Una matriz es un tipo de datos especial que contiene entre uno y dieciséis componentes. Cada componente de una matriz debe ser del mismo tipo.



|                         |
|-------------------------|
| **Nombre de TypeComponents** |



 

## <a name="components"></a>Componentes



| Elemento                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | Nombre único que contiene tres partes. La primera parte es uno de los [tipos escalares.](dx-graphics-hlsl-data-types.md) La segunda parte es el número de filas. La tercera parte es el número de columnas. El número de filas y columnas es un entero positivo entre 1 y 4 inclusive.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre**<br/>                                         | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a>Ejemplos

Estos son algunos ejemplos:


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



Una matriz también se puede declarar mediante esta sintaxis:


```
matrix <Type, Number> VariableName
```



El tipo de matriz usa los corchetes angulares para especificar el tipo, el número de filas y el número de columnas. En este ejemplo se crea una matriz de punto flotante, con dos filas y dos columnas. Se puede usar cualquiera de los tipos de datos escalares.

Este es un ejemplo:


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de datos (HLSL de DirectX)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





