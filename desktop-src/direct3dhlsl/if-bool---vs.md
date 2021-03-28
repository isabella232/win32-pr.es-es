---
title: Si es bool-vs
description: Inicia una... otra cosa... bloque endif-vs.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ff572cbaf519cc0099f3ab68d1a0becca706f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077066"
---
# <a name="if-bool---vs"></a>Si es bool-vs

Inicia una... [otra cosa](else---vs.md)... bloque [endif-vs](endif---vs.md) .

## <a name="syntax"></a>Sintaxis



| Si es bool |
|---------|



 

donde bool es un número de registro bool. Vea [registro booleano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Si es bool                |      | x    | x    | x     | x    | x     |



 

Si el registro booleano de origen en la instrucción if es true, se ejecuta el código incluido entre la instrucción if y la otra que coincide. De lo contrario, el código delimitado por el bloque [else](else---vs.md)... se ejecutan las instrucciones [endif-vs](endif---vs.md) . Esta instrucción usa una ranura de instrucción.

Si los bloques se pueden anidar.

Un bloque If no puede ocupar un bloque de bucle.

## <a name="example"></a>Ejemplo

Esta instrucción proporciona el control de flujo estático condicional.


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[Else-vs](else---vs.md)
</dt> <dt>

[endif-vs](endif---vs.md)
</dt> </dl>

 

 




