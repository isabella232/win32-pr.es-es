---
title: Saturate (referencia de HLSL)
description: Fija el resultado de una operación aritmética de punto flotante de precisión sencilla o doble a \ 0,0f... Intervalo de 1,0f\.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05b6048777ac7b6ecd2c4b59ff3c9e0287380949
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573688"
---
# <a name="saturate-hlsl-reference"></a>Saturate (referencia de HLSL)

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
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de instrucción](instruction-modifiers.md)
</dt> </dl>

 

 




