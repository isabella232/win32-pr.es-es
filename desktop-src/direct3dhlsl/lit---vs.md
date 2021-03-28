---
title: Lit-vs
description: Proporciona compatibilidad parcial para la iluminación mediante el cálculo de los coeficientes de iluminación de dos productos DOT y un exponente.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99c25c377ff6064a704d56b9e7b31d41b37117e5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983858"
---
# <a name="lit---vs"></a>Lit-vs

Proporciona compatibilidad parcial para la iluminación mediante el cálculo de los coeficientes de iluminación de dos productos DOT y un exponente.

## <a name="syntax"></a>Sintaxis



| Lit DST, src |
|--------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| encender                    | x    | x    | x    | x     | x    | x     |



 

Se supone que el vector de origen contiene los valores que se muestran en el siguiente pseudocódigo.


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



En el siguiente fragmento de código se muestran las operaciones realizadas.


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



La aritmética de precisión reducida es aceptable en la evaluación del componente y de destino (dest. y). Una implementación de debe admitir al menos ocho bits de fracción en el argumento de potencia. Los productos de punto se calculan con vectores normalizados y los límites de la abrazadera son de-128 a 128.

El error debe corresponder a una combinación [logP-vs](logp---vs.md) y [exp-vs](exp---vs.md) , o no más de aproximadamente un bit significativo para un componente de color de 8 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




