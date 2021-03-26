---
title: Registro de origen permutación (HLSL VS Reference)
description: Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal. Permutación hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal. Permutación no afecta a los datos de registro de origen.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c075d8ff47b1f76adf378b6a583cd4d675651a87
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104420013"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a>Registro de origen permutación (HLSL VS Reference)

Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal. Permutación hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal. Permutación no afecta a los datos de registro de origen.

## <a name="component-swizzling"></a>Componente permutación

Como se muestra en la tabla siguiente, permutación se puede aplicar a los componentes individuales de los datos del registro de origen (donde es uno de los registros de entrada del sombreador de vértices válidos [, vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).



| Modificador de componente                 | Descripción    |
|------------------------------------|----------------|
| r. \[ xyzw \] \[ xyzw \] \[ xyzw \] \[ xyzw\] | Swizzle de origen |



 

-   Siempre se copian los cuatro componentes. Si se especifican menos de cuatro componentes, el último componente se repite (XY Means. xyyy). Si no se especifica ningún componente, x se repite (. xxxx).
-   Los componentes pueden aparecer en cualquier orden. v0. YWX da como resultado v0. ywxx.
-   Los componentes RGBA se pueden usar respectivamente para xyzw (r para x, g para b, etc.).
-   Estas instrucciones implementan un componente de registro de origen único swizzles: EXP, EXPP, log, logP, pow, RCP, RSQ. El resultado de estas instrucciones se copia en los cuatro componentes de registro de destino.

Permutación no se puede usar en las instrucciones [m3x2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [m4x3-vs](m4x3---vs.md)y [M4x4-vs](m4x4---vs.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




