---
title: if pred - vs
description: 'Inicio de un elemento if pred - vs... else - vs... endif: vs block, con la condición tomada del contenido del registro de predicado.'
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad9aba5c9f18b88577a456764a71cc27637d24856cdafa95d811344034d514f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511911"
---
# <a name="if-pred---vs"></a>if pred - vs

Inicio de un elemento if pred - vs... [else : frente a](else---vs.md)... [endif- vs](endif---vs.md) block, con la condición tomada del contenido del registro de predicado.

## <a name="syntax"></a>Syntax



| si \[ ! \] pred.replicateSwiquele |
|-------------------------------|



 

Donde:

-   \[!\] un modificador NOT opcional. Esto modifica el valor en el registro de predicado.
-   pred es el registro de predicado, p0. Vea [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   replicateSwzzle es un único componente que se copia (o replica) en los cuatro componentes (despláctese). Los componentes válidos son: x, y, z, w o r, g, b, a.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| si pred                |      |      | x    | x     | x    | x     |



 

Esta instrucción se usa para omitir un bloque de código, en función de un canal del registro de predicado. Cada bloque \_ pred debe terminar con una instrucción else o endif.

Entre las restricciones se incluyen:

si \_ se pueden anidar bloques pred. Esto cuenta para la profundidad total de anidamiento dinámico junto con bloques [if \_ comp.](if-comp---vs.md)

Un bloque si el pred no puede encontrarse en un bloque de bucle, debe estar completamente dentro de él \_ o rodearse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




