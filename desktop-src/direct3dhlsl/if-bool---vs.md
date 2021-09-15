---
title: if bool - vs
description: Inicia una excepción if... Más... endif- vs block.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ff572cbaf519cc0099f3ab68d1a0becca706f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568928"
---
# <a name="if-bool---vs"></a>if bool - vs

Inicia una excepción if... [else](else---vs.md)... [endif- vs](endif---vs.md) block.

## <a name="syntax"></a>Sintaxis



| if bool |
|---------|



 

donde bool es un número de registro bool. Vea [Registro booleano constante.](dx9-graphics-reference-asm-vs-registers-constant-boolean.md)

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| if bool                |      | x    | x    | x     | x    | x     |



 

Si el registro booleano de origen en la instrucción if es true, se ejecuta el código incluido en la instrucción if y el objeto matching else. De lo contrario, el código incluido por [el otro ...](else---vs.md) [endif: se ejecutan](endif---vs.md) las instrucciones vs. Esta instrucción consume una ranura de instrucciones.

si los bloques se pueden anidar.

Un bloque if no puede bloquear un bloque de bucle.

## <a name="example"></a>Ejemplo

Esta instrucción proporciona control de flujo estático condicional.


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

[else - vs](else---vs.md)
</dt> <dt>

[endif- vs](endif---vs.md)
</dt> </dl>

 

 




