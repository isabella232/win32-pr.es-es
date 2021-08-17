---
title: rcp - vs
description: Calcula el recíproco del escalar de origen. | rcp - vs
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d9ec2c011e4f365f7cedc1191522836db098da976c4ce3c5153169a1d87f180d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672305"
---
# <a name="rcp---vs"></a>rcp - vs

Calcula el recíproco del escalar de origen.

## <a name="syntax"></a>Syntax



| rcp dst, src |
|--------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicar swzzle, es decir, exactamente uno de los componentes .x, .y, .z, .w swzzle (o los componentes .r, .g, .b, .a equivalentes).

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| rcp                    | x    | x    | x    | x     | x    | x     |



 

El fragmento de código siguiente muestra las operaciones realizadas.


```
float f = src0;
if(f == 0.0f)
{
    f = FLT_MAX;
}
else 
{
    if(f != 1.0)
    {
        f = 1/f;
    }
}

dest = f;
```



La salida debe ser exactamente 1.0 si la entrada es exactamente 1.0. Una fuente de 0,0 produce infinito.

La precisión debe ser de al menos un error absoluto de 1,0/(2):2): en el intervalo (1.0, 2.0), ya que las implementaciones comunes separarán la mantisa y el exponente.

Si el origen no tiene subíndices, se usa el componente x.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




