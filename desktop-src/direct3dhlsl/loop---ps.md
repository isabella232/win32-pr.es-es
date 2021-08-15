---
title: loop - ps
description: 'Inicia un bucle... endloop: bloque ps.'
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a08d2954b478bd6afd0c52d517e07a82ba3ee148dd07f839ec7d8787d93c2134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510988"
---
# <a name="loop---ps"></a>loop - ps

Inicia un bucle... [endloop: bloque ps.](endloop---ps.md)

## <a name="syntax"></a>Syntax



| loop aL, i\# |
|--------------|



 

Donde:

-   aL es el [registro del contador de bucles](dx9-graphics-reference-asm-ps-registers-loop-counter.md) que mantiene el recuento de bucles actual.
-   i \# es un registro de entero [constante.](dx9-graphics-reference-asm-ps-registers-constant-integer.md) Vea Notas.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| bucle                  |      |      |      |      |      |      |       | x    | x     |



 

-   El [registro de contadores](dx9-graphics-reference-asm-ps-registers-loop-counter.md) de bucles (aL) contiene el número de bucles actual y se puede usar para el direccionamiento relativo en el registro de [color](dx9-graphics-reference-asm-ps-registers-input-color.md) de entrada (v ) dentro del bloque \# de bucle.
-   i \# .x especifica el recuento de iteraciones. El intervalo legal es \[ 0, 255 \] . Tenga en cuenta que esta instrucción no incrementa ni disminuye el valor de i \# .x.
-   i .y especifica el valor inicial del registro del contador de \# bucles (aL). [](dx9-graphics-reference-asm-ps-registers-loop-counter.md) El intervalo legal es \[ 0, 255 \] . Tenga en cuenta que esta instrucción no incrementa ni disminuye el valor de i \# .y.
-   i \# .z especifica el tamaño del paso o el intervalo. El intervalo legal es \[ -128, 127 \] .
-   El bloque de bucle no usa i \# .w y debe ser 0.
-   Los bloques de bucle pueden estar anidados. Vea [Flow control de datos](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   Cuando se anida, el valor del registro de [contador](dx9-graphics-reference-asm-ps-registers-loop-counter.md) de bucles (aL) hace referencia al bloque de bucle de encierre inmediato.
-   Los bloques de bucle pueden estar completamente dentro de un bloque if \* o rodearse completamente. No se permite ningún estrango.

## <a name="example"></a>Ejemplo


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




