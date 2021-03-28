---
title: Si es bool-PS
description: Inicio de un bloque if.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784889"
---
# <a name="if-bool---ps"></a>Si es bool-PS

Inicio de un bloque if.

## <a name="syntax"></a>Sintaxis



| Si es bool |
|---------|



 

Donde:

-   bool es un número de registro booleano (booleano). Vea [registro booleano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Si es bool               |      |      |      |      |      | x    | x     | x    | x     |



 

Si el registro de valor booleano de origen en la instrucción if es true, se ejecuta el código incluido entre la instrucción if y el [endif-PS](endif---ps.md) correspondiente, o bien el [PS](else---ps.md) . De lo contrario, el código incluido en el bloque else-PS... se ejecutan las instrucciones endif-PS. Esta instrucción usa una ranura de instrucción.

Un bloque if se puede anidar.

Un bloque If no puede ocupar un bloque de bucle.

Un bloque if puede ir seguido de un bloque de instrucciones y/o una instrucción [else-PS](else---ps.md) , y/o una instrucción [endif-PS](endif---ps.md) .

## <a name="example"></a>Ejemplo

Esta instrucción proporciona el control de flujo estático condicional.


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[Else-PS](else---ps.md)
</dt> <dt>

[endif-PS](endif---ps.md)
</dt> </dl>

 

 




