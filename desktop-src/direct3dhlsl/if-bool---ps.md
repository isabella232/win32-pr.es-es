---
title: if bool - ps
description: Inicio de un bloque if.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 611ec04a5c3a53bbb8c6c35380bd0d9f824dc697a7d27a3656b262d885fb4eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457515"
---
# <a name="if-bool---ps"></a>if bool - ps

Inicio de un bloque if.

## <a name="syntax"></a>Sintaxis



| if bool |
|---------|



 

Donde:

-   bool es un número de registro bool (booleano). Vea [Registro booleano constante.](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| if bool               |      |      |      |      |      | x    | x     | x    | x     |



 

Si el registro booleano de origen en la instrucción if es true, se ejecuta el código incluido en la instrucción if y la instrucción [endif](endif---ps.md) correspondiente - ps u otra cosa [- ps.](else---ps.md) De lo contrario, el código incluido por el otro : ps... endif: se ejecutan las instrucciones ps. Esta instrucción consume una ranura de instrucciones.

Un bloque if se puede anidar.

Un bloque if no puede bloquear un bloque de bucle.

Un bloque if puede ir seguido de un bloque de instrucciones o de otra instrucción [ps](else---ps.md) o [una instrucción endif - ps.](endif---ps.md)

## <a name="example"></a>Ejemplo

Esta instrucción proporciona control de flujo estático condicional.


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

[else: ps](else---ps.md)
</dt> <dt>

[endif: ps](endif---ps.md)
</dt> </dl>

 

 




