---
title: Valor absoluto
description: Tome el valor absoluto de un operando de origen utilizado en una operación aritmética.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 904ff3bb89e71a95a1c88851426ba283987ba6b96f336c91dd443794ee5e143d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795414"
---
# <a name="absolute-value"></a>Valor absoluto

Tome el valor absoluto de un operando de origen utilizado en una operación aritmética.



| \_Abs |
|-------|



 

Este modificador solo se usa para instrucciones y punto flotante de precisión sencilla y doble. El **\_ modificador abs** fuerza el signo de los números en el positivo del operando de origen, incluidos los valores INF.

La aplicación **\_ de abs** en NaN conserva NaN, aunque no se define el patrón de bits NaN determinado que da como resultado.

Cuando se combina abs con \_ el [modificador negate,](negate.md) la combinación fuerza el signo a ser negativo, como si se aplicara primero el modificador **\_ abs** y, a continuación, **negate**.

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

 

 




