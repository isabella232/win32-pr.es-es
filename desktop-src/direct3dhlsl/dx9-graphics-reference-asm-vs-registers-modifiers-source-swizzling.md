---
title: Swling del registro de origen (referencia de HLSL VS)
description: Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal. Swling hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal. El desdobado no afecta a los datos de registro de origen.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03dd2d9051c185d1be1ccb6fce18549bf5aa3414975c9a600bb8f8c47f78d4c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854555"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a>Swling del registro de origen (referencia de HLSL VS)

Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal. Swling hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal. El desdobado no afecta a los datos de registro de origen.

## <a name="component-swizzling"></a>Desdobado de componentes

Como se muestra en la tabla siguiente, el desdobado se puede aplicar a los componentes individuales de los datos de registro de origen (donde es uno de los registros válidos de entrada del sombreador de vértices, frente a [ \_ \_ 1 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).



| Modificador de componente                 | Descripción    |
|------------------------------------|----------------|
| r. \[ xyzw \] \[ xyzw \] \[ xyzw \] \[ xyzw xyzw\] | Sw swzzle de origen |



 

-   Los cuatro componentes siempre se copian. Si se especifican menos de cuatro componentes, se repite el último componente (xy significa .xyyy). Si no se especifica ningún componente, x se repite (.xxxx).
-   Los componentes pueden aparecer en cualquier orden. v0.ywx da como resultado v0.ywxx.
-   Los componentes rgba se pueden usar respectivamente para xyzw (r para x, g para b, etc.).
-   Estas instrucciones implementan swzzles de componente único de registro de origen: exp, expp, log, logp, pow, rcp, rsq. El resultado de estas instrucciones se copia en los cuatro componentes de registro de destino.

Swling no se puede usar en [m3x2 -](m3x2---vs.md)frente a , [m3x3 - frente](m3x3---vs.md)a , [m4x3 - frente](m4x3---vs.md)a , y [m4x4 - frente](m4x4---vs.md) a instrucciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




