---
title: Si Pred-PS
description: Inicio de una expresión if bool-PS... Else-PS... bloque endif-PS, con la condición tomada del contenido del registro de predicado.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784912"
---
# <a name="if-pred---ps"></a>Si Pred-PS

Inicio de una expresión [If bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... bloque [endif-PS](endif---ps.md) , con la condición tomada del contenido del registro de predicado.

## <a name="syntax"></a>Sintaxis



| Si \[ ! \] Pred. replicateSwizzle |
|-------------------------------|



 

Donde:

-   \[!\] es un modificador NOT opcional. Esto modifica el valor en el registro del predicado.
-   Pred es el [registro del predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   replicateSwizzle es un componente único que se copia (o se replica) en los cuatro componentes (swizzled). Los componentes válidos son: \[ x, y, z, w \] o \[ r, g, b, a \] .

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Si es \_ Pred              |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrucción se usa para omitir un bloque de código, basado en un canal del registro del predicado. Cada si el \_ bloque Pred debe terminar con una instrucción [else-PS](else---ps.md) o [endif-PS](endif---ps.md) .

Entre las restricciones se incluyen:

Si \_ se pueden anidar los bloques pred. Cuenta con la profundidad de anidamiento dinámica total junto con los bloques de [ \_ COMP if](if-comp---ps.md) .

Un \_ bloque if Pred no puede ocupar un bloque de bucle; debe estar completamente dentro o delimitarlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




