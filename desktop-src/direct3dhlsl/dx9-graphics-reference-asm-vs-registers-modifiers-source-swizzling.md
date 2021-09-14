---
title: Source Register Swling (referencia de HLSL VS)
description: Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal. Swling hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal. El desdobado no afecta a los datos de registro de origen.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c075d8ff47b1f76adf378b6a583cd4d675651a87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241622"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a>Source Register Swling (referencia de HLSL VS)

Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal. Swling hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal. El desdobado no afecta a los datos de registro de origen.

## <a name="component-swizzling"></a>Desdobado de componentes

Como se muestra en la tabla siguiente, el desdobado se puede aplicar a los componentes individuales de los datos de registro de origen (donde es uno de los registros de entrada válidos del sombreador de vértices, frente a [ \_ \_ 1 1).](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)



| Modificador de componente                 | Descripción    |
|------------------------------------|----------------|
| r. \[ xyzw \] \[ xyzw \] \[ xyzw \] \[ xyzw xyzw\] | Sw swzzle de origen |



 

-   Los cuatro componentes siempre se copian. Si se especifican menos de cuatro componentes, se repite el último componente (xy significa .xyyy). Si no se especifica ningún componente, x se repite (.xxxx).
-   Los componentes pueden aparecer en cualquier orden. v0.ywx da como resultado v0.ywxx.
-   Los componentes rgba se pueden usar respectivamente para xyzw (r para x, g para b, etc.).
-   En estas instrucciones se implementa el registro de origen de componentes únicos: exp, expp, log, logp, pow, rcp, rsq. El resultado de estas instrucciones se copia en los cuatro componentes de registro de destino.

No se puede usar swling en [m3x2 -](m3x2---vs.md)vs , [m3x3 - vs](m3x3---vs.md), [m4x3 - vs](m4x3---vs.md)y [m4x4 - vs](m4x4---vs.md) instructions.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




