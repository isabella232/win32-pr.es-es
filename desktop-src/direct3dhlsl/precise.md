---
title: Preciso
description: Deshabilitación por instrucción de la refactorización aritmética.
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f288fb5dafee0e29c8c11cab72156f7ad3d569
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532860"
---
# <a name="precise"></a>Preciso

Deshabilitación por instrucción de la refactorización aritmética.



| preciso (máscara de componentes) |
|--------------------------|



 

Este modificador requiere la marca del sombreador global "Refactoring \_ allowed". Cuando está presente la refactorización \_ permitida, los resultados de componentes individuales de las instrucciones individuales pueden verse obligados a ser precisos o no refactorizables por los compiladores o los controladores. Si los componentes de una instrucción de [**Mad**](mad--sm4---asm-.md) se etiquetan como **precisos**, el hardware debe ejecutar una instrucción de **Mad** o el equivalente exacto, y no puede dividirlo en una multiplicación seguida de una suma. Por el contrario, un multiplicado seguido por una suma, donde uno o ambos se marcan como **precisos**, no se pueden combinar en un **Mad** fundido.

Si \_ no se ha especificado la REfactorización permitido, no se permite el modificador **preciso** . No es necesario porque todo es preciso. El modificador **preciso** afecta a cualquier operación, no solo a aritmética.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este modificador es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de instrucciones del modelo de sombreador 5](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




