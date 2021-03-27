---
title: bucle-vs
description: Iniciar un bucle... bloque ENDLOOP.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6a96a1ce53b850ec8feeba282055e8111b275bfd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996921"
---
# <a name="loop---vs"></a>bucle-vs

Iniciar un bucle... bloque [ENDLOOP](endloop---vs.md) .

## <a name="syntax"></a>Sintaxis



| bucle aL, i\# |
|--------------|



 

Donde:

-   aL es el [registro del contador de bucles](dx9-graphics-reference-asm-vs-registers-loop-counter.md) que contiene el número de bucles actual.
-   i \# es un [registro entero constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md). Vea Notas.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| bucle                   |      | x    | x    | x     | x    | x     |



 

-   El [registro de contador de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) contiene el recuento de bucles actual y se puede usar para el direccionamiento relativo en el [registro de enteros constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c \# ) o los [registros de salida](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) dentro del bloque de bucle.
-   i \# . x especifica el número de iteraciones. El intervalo legal es \[ 0, 255 \] . Tenga en cuenta que esta instrucción no incrementa ni reduce el valor de i \# . x.
-   i \# . y especifica el valor inicial del registro de [contadores del bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al). El intervalo legal es \[ 0, 255 \] . Tenga en cuenta que esta instrucción no incrementa ni disminuye el valor de i \# . y.
-   i \# . z especifica el tamaño de paso/STRIDE. El intervalo válido es \[ -128, 127 \] .
-   i \# . w no se utiliza y debe establecerse en 0.
-   Los bloques de bucle pueden estar anidados. Consulte [límites de anidamiento de control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   Cuando está anidado, el valor del [registro de contador de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) hace referencia al bloque de bucle de inclusión inmediato.
-   Los bloques de bucle pueden estar completamente dentro \* de un bloque if o por completo. No se permite la necesidad de estar en el mismo.

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

 

 




