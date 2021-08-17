---
title: 'lit : frente a'
description: Proporciona compatibilidad parcial para la iluminación mediante el cálculo de coeficientes de iluminación de dos productos de punto y un exponente.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e5b5ff3451424251d778886af3841c673ce5a85d91022db9144c62574c16640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089328"
---
# <a name="lit---vs"></a>lit : frente a

Proporciona compatibilidad parcial para la iluminación mediante el cálculo de coeficientes de iluminación de dos productos de punto y un exponente.

## <a name="syntax"></a>Syntax



| lit dst, src |
|--------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Encendido                    | x    | x    | x    | x     | x    | x     |



 

Se supone que el vector de origen contiene los valores que se muestran en el pseudocódigo siguiente.


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



El fragmento de código siguiente muestra las operaciones realizadas.


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



La aritmética de precisión reducida es aceptable al evaluar el componente y de destino (dest.y). Una implementación debe admitir al menos ocho bits de fracción en el argumento power. Los productos de puntos se calculan con vectores normalizados y los límites de fijación son de -128 a 128.

El error debe corresponder a una combinación [logp - vs](logp---vs.md) y [exp - vs,](exp---vs.md) o no más de un bit significativo para un componente de color de 8 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




