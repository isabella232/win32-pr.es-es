---
title: if pred - ps
description: 'Inicio de un if bool - ps... else - ps... endif: bloque ps, con la condición tomada del contenido del registro de predicado.'
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1a9e1c531e5dc6cd76bdd220a94730f2fb7b859eb99d9bba217a008fb02b4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511921"
---
# <a name="if-pred---ps"></a>if pred - ps

Inicio de un [if bool - ps](if-bool---ps.md)... [else - ps](else---ps.md)... [endif: bloque ps,](endif---ps.md) con la condición tomada del contenido del registro de predicado.

## <a name="syntax"></a>Syntax



| si \[ ! \] pred.replicateSwiquele |
|-------------------------------|



 

Donde:

-   \[!\] es un modificador NOT opcional. Esto modifica el valor en el registro de predicado.
-   pred es el [registro de predicado.](dx9-graphics-reference-asm-ps-registers-predicate.md)
-   replicateSwzzle es un único componente que se copia (o replica) en los cuatro componentes (despláctese). Los componentes válidos \[ son: x, y, z, w \] o \[ r, g, b, a \] .

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| si \_ pred              |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrucción se usa para omitir un bloque de código, en función de un canal del registro de predicado. Cada bloque \_ pred debe terminar con una [instrucción else - ps](else---ps.md) o [endif - ps.](endif---ps.md)

Entre las restricciones se incluyen:

si \_ se pueden anidar bloques pred. Esto cuenta con la profundidad total de anidamiento dinámico junto con los [bloques \_ if comp.](if-comp---ps.md)

Un bloque si el pred no puede encontrarse en un bloque de bucle; debe estar completamente dentro de él \_ o rodearse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




