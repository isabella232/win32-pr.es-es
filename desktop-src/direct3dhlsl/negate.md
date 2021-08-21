---
title: Negate
description: Invierte el signo del valor de un operando de origen utilizado en una operación aritmética.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1f220cb0a5becf823ecc547e29c9d4c7363aa8b885355bb76f1182fae333f84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089156"
---
# <a name="negate"></a>Negate

Invierte el signo del valor de un operando de origen utilizado en una operación aritmética.



| \-  |
|-----|



 

Para las instrucciones y el punto flotante de precisión sencilla y doble, el modificador negate invierte el signo de los números del operando de origen, incluidos los valores INF. Al aplicar **negate** en NaN se conserva NaN, aunque no se define el patrón de bits NaN determinado que da como resultado.

Para las instrucciones de entero, **el modificador negate** toma el complemento 2 de los números del operando de origen.

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

 

 




