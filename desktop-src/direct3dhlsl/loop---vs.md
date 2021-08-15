---
title: 'loop: vs'
description: Iniciar un bucle... bloque endloop.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a211014137f35c39a6b89cd16f0e27687b4daafd89841f752312f459531cab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986445"
---
# <a name="loop---vs"></a>loop: vs

Iniciar un bucle... [bloque endloop.](endloop---vs.md)

## <a name="syntax"></a>Syntax



| loop aL, i\# |
|--------------|



 

Donde:

-   aL es el [registro del contador de bucles](dx9-graphics-reference-asm-vs-registers-loop-counter.md) que mantiene el recuento de bucles actual.
-   i \# es un registro de entero [constante.](dx9-graphics-reference-asm-vs-registers-constant-integer.md) Vea Notas.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| bucle                   |      | x    | x    | x     | x    | x     |



 

-   El [registro de contadores](dx9-graphics-reference-asm-vs-registers-loop-counter.md) de bucles (aL) contiene el número de bucles actual y se puede usar para el direccionamiento relativo en el registro de enteros constantes [(c](dx9-graphics-reference-asm-vs-registers-constant-integer.md) ) o los registros de salida (o ) dentro del bloque \# de [](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) \# bucle.
-   i \# .x especifica el recuento de iteraciones. El intervalo legal es \[ 0, 255 \] . Tenga en cuenta que esta instrucción no incrementa ni disminuye el valor de i \# .x.
-   i .y especifica el valor inicial del registro del contador de \# bucles (aL). [](dx9-graphics-reference-asm-vs-registers-loop-counter.md) El intervalo legal es \[ 0, 255 \] . Tenga en cuenta que esta instrucción no incrementa ni disminuye el valor de i \# .y.
-   i \# .z especifica el tamaño del paso o el intervalo. El intervalo legal es \[ -128, 127 \] .
-   i \# .w no se usa y debe establecerse en 0.
-   Los bloques de bucle pueden estar anidados. Vea [Flow límites de anidamiento de controles .](dx9-graphics-reference-asm-vs-instructions-flow-control.md)
-   Cuando está anidado, el valor del registro de [contadores](dx9-graphics-reference-asm-vs-registers-loop-counter.md) de bucles (aL) hace referencia al bloque de bucle de encierre inmediato.
-   Los bloques de bucle pueden estar completamente dentro de un bloque if \* o rodearse completamente. No se permite ningún estrango.

## <a name="example"></a>Ejemplo


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




