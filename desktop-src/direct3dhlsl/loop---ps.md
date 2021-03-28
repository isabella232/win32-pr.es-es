---
title: bucle-PS
description: 'Inicia un bucle... ENDLOOP: bloque PS.'
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf4c71641003d460e9752dcf33f983c70a82e4f6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077100"
---
# <a name="loop---ps"></a>bucle-PS

Inicia un bucle... [ENDLOOP: bloque PS](endloop---ps.md) .

## <a name="syntax"></a>Sintaxis



| bucle aL, i\# |
|--------------|



 

Donde:

-   aL es el [registro del contador de bucles](dx9-graphics-reference-asm-ps-registers-loop-counter.md) que contiene el número de bucles actual.
-   i \# es un [registro entero constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md). Vea Notas.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| bucle                  |      |      |      |      |      |      |       | x    | x     |



 

-   El [registro de contador de bucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) contiene el número de bucles actual y se puede usar para el direccionamiento relativo en el [registro de color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) dentro del bloque de bucle.
-   i \# . x especifica el número de iteraciones. El intervalo legal es \[ 0, 255 \] . Tenga en cuenta que esta instrucción no incrementa ni reduce el valor de i \# . x.
-   i \# . y especifica el valor inicial del registro de [contadores del bucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al). El intervalo legal es \[ 0, 255 \] . Tenga en cuenta que esta instrucción no incrementa ni disminuye el valor de i \# . y.
-   i \# . z especifica el tamaño de paso/STRIDE. El intervalo válido es \[ -128, 127 \] .
-   i \# . w no se usa en el bloque de bucle y debe ser 0.
-   Los bloques de bucle pueden estar anidados. Vea [limitaciones del control de flujo](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   Cuando está anidado, el valor del [registro de contador de bucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) hace referencia al bloque de bucle de inclusión inmediato.
-   Los bloques de bucle pueden estar completamente dentro \* de un bloque if o por completo. No se permite la necesidad de estar en el mismo.

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

 

 




