---
title: Valor absoluto
description: Toma el valor absoluto de un operando de origen utilizado en una operación aritmética.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27ceefa2c4b4ee2eb890b0692a33266e89a18cfb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358507"
---
# <a name="absolute-value"></a>Valor absoluto

Toma el valor absoluto de un operando de origen utilizado en una operación aritmética.



| \_ABS |
|-------|



 

Este modificador se usa solo para las instrucciones y el punto flotante de precisión sencilla y doble. El modificador **\_ ABS** fuerza el signo de los números en el operando de origen Positive, incluidos los valores INF.

Al aplicar **\_ ABS** en Nan, se conservan Nan, aunque el patrón de bits Nan determinado que Results no está definido.

Cuando \_ se combina ABS con el modificador [Negate](negate.md) , la combinación obliga al signo a ser negativo, como si se aplicara primero el modificador **\_ ABS** y luego el valor **negado**.

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

 

 




