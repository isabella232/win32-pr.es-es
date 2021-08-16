---
title: rsq- vs
description: Calcula la raíz cuadrada recíproca (solo positiva) del escalar de origen. | rsq- vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 937f89a018943d9ab8f74a4a328316d5d68dca7d48730a06b80814dacbd8ed68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510914"
---
# <a name="rsq---vs"></a>rsq- vs

Calcula la raíz cuadrada recíproca (solo positiva) del escalar de origen.

## <a name="syntax"></a>Syntax



| rsq dst, src |
|--------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicate sw siple, es decir, exactamente uno de los componentes .x, .y, .z, .w swzzle (o los componentes .r, .g, .b, .a equivalentes).

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Lrq                    | x    | x    | x    | x     | x    | x     |



 

El fragmento de código siguiente muestra las operaciones realizadas.


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

La precisión debe ser al menos un error absoluto de 1,0/(2 además del intervalo (1.0, 4.0) porque las implementaciones comunes separarán la mantisa y el exponente.

Si source no tiene subíndices, se usa el componente x. La salida debe ser exactamente 1.0 si la entrada es exactamente 1.0. Un origen de 0,0 produce infinito.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




