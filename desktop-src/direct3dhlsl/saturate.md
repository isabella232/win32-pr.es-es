---
title: Saturate (referencia hlsl)
description: Fija el resultado de una operación aritmética de punto flotante de precisión sencilla o doble a \ 0,0f... Intervalo de 1,0f\.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 25e771bd53dbb8a4b0d2eaf8162675cd556c071344b249562defe4a06e715f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790748"
---
# <a name="saturate-hlsl-reference"></a>Saturate (referencia hlsl)

Fija el resultado de una operación aritmética de punto flotante de precisión sencilla o doble a \[ 0,0f... Intervalo de 1,0f. \]



| \_Sentado |
|-------|



 

El **modificador saturate** instruction result realiza la siguiente operación en los valores de resultado a partir de una operación aritmética de punto flotante que se le \_ ha aplicado:

`min(1.0f, max(0.0f, value))`

donde min() y max() en la expresión anterior se comportan de la manera en que [funcionan min,](min--sm4---asm-.md) [max,](max--sm4---asm-.md) [dmin](dmin--sm5---asm-.md)o [dmax.](dmax--sm5---asm-.md)

`_sat(NaN)` devuelve 0, según las reglas para min y max.

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este modificador se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de instrucción](instruction-modifiers.md)
</dt> </dl>

 

 




