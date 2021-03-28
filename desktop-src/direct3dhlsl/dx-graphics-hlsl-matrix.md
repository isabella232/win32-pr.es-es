---
title: Tipo de matriz
description: Una matriz es un tipo de datos Especial que contiene entre uno y dieciséis componentes. Cada componente de una matriz debe ser del mismo tipo.
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
ms.openlocfilehash: c580706a2ddae3e4a94c138a1ca0f6932457732a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076532"
---
# <a name="matrix-type"></a>Tipo de matriz

Una matriz es un tipo de datos Especial que contiene entre uno y dieciséis componentes. Cada componente de una matriz debe ser del mismo tipo.



|                         |
|-------------------------|
| **Nombre de TypeComponents** |



 

## <a name="components"></a>Componentes



| Elemento                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | Un nombre único que contiene tres partes. La primera parte es uno de los tipos [escalares](dx-graphics-hlsl-data-types.md) . La segunda parte es el número de filas. La tercera parte es el número de columnas. El número de filas y columnas es un entero positivo comprendido entre 1 y 4, ambos incluidos.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**<br/>                                         | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a>Ejemplos

A continuación se muestran algunos ejemplos:


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



Una matriz se puede declarar con esta sintaxis también:


```
matrix <Type, Number> VariableName
```



El tipo de matriz utiliza corchetes angulares para especificar el tipo, el número de filas y el número de columnas. En este ejemplo se crea una matriz de punto flotante, con dos filas y dos columnas. Se puede usar cualquiera de los tipos de datos escalares.

Este es un ejemplo:


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





