---
title: if pred - vs
description: Inicio de un elemento if pred - vs... else- vs... endif- vs block, con la condición tomada del contenido del registro de predicado.
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567784"
---
# <a name="if-pred---vs"></a>if pred - vs

Inicio de un elemento if pred - vs... [else - vs](else---vs.md)... [endif- vs](endif---vs.md) block, con la condición tomada del contenido del registro de predicado.

## <a name="syntax"></a>Sintaxis



| si \[ ! \] pred.replicateSwiquele |
|-------------------------------|



 

Donde:

-   \[!\] un modificador NOT opcional. Esto modifica el valor en el registro de predicado.
-   pred es el registro de predicado, p0. Vea [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   replicateSwiquele es un único componente que se copia (o replica) en los cuatro componentes (se desliza). Los componentes válidos son: x, y, z, w o r, g, b, a.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| si se pred                |      |      | x    | x     | x    | x     |



 

Esta instrucción se usa para omitir un bloque de código, en función de un canal del registro de predicado. Cada bloque \_ pred debe terminar con una instrucción else o endif.

Entre las restricciones se incluyen:

si \_ se pueden anidar bloques pred. Esto cuenta con la profundidad total de anidamiento dinámico junto con bloques [ \_ if comp.](if-comp---vs.md)

Un bloque si el pred no puede bloquear un bloque de bucle, debe estar completamente dentro de él \_ o rodearse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




