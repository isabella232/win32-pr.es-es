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
ms.openlocfilehash: 3c7929a7ebab01b17aca3e11cb98de8796bf568cd08a3a7b04d8f3395f531d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067915"
---
# <a name="precise"></a>Preciso

Deshabilitación por instrucción de la refactorización aritmética.



| precise (máscara de componentes) |
|--------------------------|



 

Este modificador requiere la marca de sombreador global "REFACTORING \_ ALLOWED". Cuando REFACTORIZACIÓN PERMITIDA está presente, los compiladores o controladores pueden forzar los resultados de componentes individuales de instrucciones individuales para que sean precisos o no \_ refactorizables. Si los componentes de [**una**](mad--sm4---asm-.md) instrucción loca se  etiquetan como precisos, el hardware debe ejecutar una instrucción loca o el equivalente exacto, y no puede dividirla en una multiplicación seguida de una suma. Por el contrario, una multiplicación seguida de una suma, donde una o ambas se marcan como precisas, no se pueden combinar en un **grupo fusionado.**

Si no se ha especificado REFACTORING ALLOWED, no se permite \_ **el** modificador preciso. No es necesario porque todo es preciso. El **modificador** preciso afecta a cualquier operación, no solo a la aritmética.

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este modificador se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de instrucciones del modelo de sombreador 5](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




