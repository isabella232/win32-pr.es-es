---
title: Función EvaluateAttributeSnapped
description: Se evalúa en el centroide de píxeles con un desplazamiento.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- Función EvaluateAttributeSnapped HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5408b2c8133947b948bc42eb6ff0c725584b0cf2c60ccf0731a9d584d3c898a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512022"
---
# <a name="evaluateattributesnapped-function"></a>Función EvaluateAttributeSnapped

Se evalúa en el centroide de píxeles con un desplazamiento.

## <a name="syntax"></a>Sintaxis

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **attrib numeric**

Valor de entrada.

</dd> <dt>

*desplazamiento* \[ En\]
</dt> <dd>

Tipo: **int2**

Desplazamiento 2D desde el centro de píxeles mediante una cuadrícula de 16 x 16.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El intervalo del *parámetro offset* debe definirse mediante el siguiente código de bytes.

Solo se usan los cuatro bits menos significativos de los dos primeros componentes (U, V) del desplazamiento de píxeles. La conversión del punto fijo de 4 bits a float es la siguiente (MSB... LSB), donde el MSB forma parte de la fracción y determina el signo:

-   1000 = -0,5f (-8 / 16)
-   1001 = -0,4375f (-7 / 16)
-   1010 = -0,375f (-6 / 16)
-   1011 = -0,3125f (-5 / 16)
-   1100 = -0,25f (-4 / 16)
-   1101 = -0,1875f (-3 / 16)
-   1110 = -0,125f (-2 / 16)
-   1111 = -0,0625f (-1 / 16)
-   0000 = 0,0f ( 0 /16)
-   0001 = 0,0625f ( 1 /16)
-   0010 = 0,125f ( 2 /16)
-   0011 = 0,1875f ( 3 /16)
-   0100 = 0,25f ( 4 /16)
-   0101 = 0,3125f ( 5 /16)
-   0110 = 0,375f ( 6 /16)
-   0111 = 0,4375f ( 7 /16)

> [!Note]  
> Los bordes izquierdo y superior de un píxel se incluyen en el desplazamiento; sin embargo, no se incluyen los bordes inferior y derecho. Todos los demás bits del entero de 32 bits que usted y los valores de desplazamiento de V se omiten.

 

Una implementación puede tomar el desplazamiento proporcionado por el sombreador y obtener un valor de punto fijo completo de 32 bits (28,4), que abarca el intervalo válido, realizando el siguiente cálculo:


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



Si una implementación debe asignar el desplazamiento a un desplazamiento de punto flotante, realiza el siguiente cálculo:


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




