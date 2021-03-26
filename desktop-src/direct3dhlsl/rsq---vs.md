---
title: RSQ-vs
description: Calcula la raíz cuadrada recíproca (solo positivo) del escalar de origen. | RSQ-vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f477d6f7d8a7ff94472c689bf5844183e2f016ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986559"
---
# <a name="rsq---vs"></a>RSQ-vs

Calcula la raíz cuadrada recíproca (solo positivo) del escalar de origen.

## <a name="syntax"></a>Sintaxis



| RSQ DST, src |
|--------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| rsq                    | x    | x    | x    | x     | x    | x     |



 

En el siguiente fragmento de código se muestran las operaciones realizadas.


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



El valor absoluto se toma antes del procesamiento.

La precisión debe ser al menos de 1,0/(2 ² ²) error absoluto en el intervalo (1,0, 4,0) porque las implementaciones comunes separan la mantisa y el exponente.

Si el origen no tiene ningún subíndice, se usa el componente x. La salida debe ser exactamente 1,0 si la entrada es exactamente 1,0. Un origen de 0,0 produce infinito.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




