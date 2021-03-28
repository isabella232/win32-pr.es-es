---
title: Negate
description: Voltea el signo del valor de un operando de origen utilizado en una operación aritmética.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077080"
---
# <a name="negate"></a>Negate

Voltea el signo del valor de un operando de origen utilizado en una operación aritmética.



| \-  |
|-----|



 

En el caso de las instrucciones y el punto flotante de precisión sencilla y doble, el modificador Nega el signo de los números del operando de origen, incluidos los valores INF. Al aplicar **niega** en Nan, se conservan Nan, aunque el patrón de bits Nan determinado que Results no está definido.

En el caso de las instrucciones de entero, el modificador **Negate** toma el complemento de 2 de los números en el operando de origen.

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

 

 




