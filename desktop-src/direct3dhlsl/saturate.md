---
title: Saturación (referencia de HLSL)
description: Fija el resultado de una operación aritmética de punto flotante de precisión única o doble a \ 0.0 f... 1.0 f \ intervalo.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05b6048777ac7b6ecd2c4b59ff3c9e0287380949
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104420025"
---
# <a name="saturate-hlsl-reference"></a>Saturación (referencia de HLSL)

Fija el resultado de una operación aritmética de punto flotante de precisión única o doble a \[ 0,0 f... 1.0 intervalo de f \] .



| \_sábado |
|-------|



 

El modificador de resultado de instrucción **saturada** realiza la siguiente operación en los valores de resultado de una operación aritmética de punto flotante que tiene el \_ SAT aplicado:

`min(1.0f, max(0.0f, value))`

donde min () y Max () en la expresión anterior se comportan de la manera en que operan [min](min--sm4---asm-.md), [Max](max--sm4---asm-.md), [dmin](dmin--sm5---asm-.md)o [dmáx](dmax--sm5---asm-.md) .

`_sat(NaN)` devuelve 0, según las reglas de min y Max.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este modificador es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de instrucciones](instruction-modifiers.md)
</dt> </dl>

 

 




