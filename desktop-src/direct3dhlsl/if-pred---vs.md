---
title: Si Pred-vs
description: 'Inicio de una en caso de Pred-vs... Else-vs... endif: bloque de vs, con la condición tomada del contenido del registro de predicado.'
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358472"
---
# <a name="if-pred---vs"></a>Si Pred-vs

Inicio de una en caso de Pred-vs... [else-vs](else---vs.md)... [endif:](endif---vs.md) bloque de vs, con la condición tomada del contenido del registro de predicado.

## <a name="syntax"></a>Sintaxis



| Si \[ ! \] Pred. replicateSwizzle |
|-------------------------------|



 

Donde:

-   \[!\] un modificador NOT opcional. Esto modifica el valor en el registro del predicado.
-   Pred es el registro de predicado, P0. Vea [registro de predicados](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   replicateSwizzle es un componente único que se copia (o se replica) en los cuatro componentes (swizzled). Los componentes válidos son: x, y, z, w o r, g, b, a.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Si es Pred                |      |      | x    | x     | x    | x     |



 

Esta instrucción se usa para omitir un bloque de código, basado en un canal del registro del predicado. Cada si el \_ bloque Pred debe terminar con una instrucción else o endif.

Entre las restricciones se incluyen:

Si \_ se pueden anidar los bloques pred. Cuenta con la profundidad de anidamiento dinámica total junto con los bloques de [ \_ COMP if](if-comp---vs.md) .

Un \_ bloque if Pred no puede ocupar un bloque de bucle, debe estar completamente dentro de él o encerrarlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




