---
title: EvaluateAttributeSnapped función)
description: Evalúa en el píxel centroide con un desplazamiento.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- EvaluateAttributeSnapped de función HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70a9389ed9e9f4fff16f82610cb611bc4da2c7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104996816"
---
# <a name="evaluateattributesnapped-function"></a>EvaluateAttributeSnapped función)

Evalúa en el píxel centroide con un desplazamiento.

## <a name="syntax"></a>Sintaxis

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de de\]
</dt> <dd>

Tipo: **attrib Numeric**

Valor de entrada.

</dd> <dt>

*desplazamiento* \[ de\]
</dt> <dd>

Tipo: **INT2**

Desplazamiento 2D desde el centro de píxeles mediante una cuadrícula de 16x16.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El intervalo para el parámetro de *desplazamiento* debe definirse mediante el siguiente código de byte.

Solo se usan los 4 bits menos significativos de los dos primeros componentes (U, V) del desplazamiento de píxeles. La conversión del punto fijo de 4 bits a Float es la siguiente (MSB... LSB), donde el MSB es una parte de la fracción y determina el signo:

-   1000 =-0.5 f (-8/16)
-   1001 =-0.4375 f (-7/16)
-   1010 =-0.375 f (-6/16)
-   1011 =-0.3125 f (-5/16)
-   1100 =-0,25 f (-4/16)
-   1101 =-0.1875 f (-3/16)
-   1110 =-0,125 f (-2/16)
-   1111 =-0.0625 f (-1/16)
-   0000 = 0.0 f (0/16)
-   0001 = 0.0625 f (1/16)
-   0010 = 0,125 f (2/16)
-   0011 = 0.1875 f (3/16)
-   0100 = 0,25 f (4/16)
-   0101 = 0.3125 f (5/16)
-   0110 = 0.375 f (6/16)
-   0111 = 0.4375 f (7/16)

> [!Note]  
> Los bordes izquierdo y superior de un píxel se incluyen en el desplazamiento; sin embargo, no se incluyen los bordes inferior y derecho. Se omiten todos los demás bits del entero de 32 bits y los valores de desplazamiento de V.

 

Una implementación puede tomar el desplazamiento proporcionado por el sombreador y obtener un valor de punto fijo de 32 bits completo (28,4), que abarca el intervalo válido, realizando el siguiente cálculo:


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



Si una implementación de debe asignar el desplazamiento a un desplazamiento de punto flotante, realiza el cálculo siguiente:


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




