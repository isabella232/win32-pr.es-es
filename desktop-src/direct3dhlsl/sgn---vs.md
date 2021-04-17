---
title: SGN-vs
description: Calcula el signo de la entrada.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419936"
---
# <a name="sgn---vs"></a>SGN-vs

Calcula el signo de la entrada.

## <a name="syntax"></a>Sintaxis



| SGN DST, src0, SRC1, src2 |
|---------------------------|



 

, donde

-   DST es el registro de destino.
-   src0 es un registro de origen.
-   SRC1 es un registro temporal que contiene resultados intermedios. Tras la ejecución, el contenido es indefinido.
-   src2 es un registro temporal que contiene resultados intermedios. Tras la ejecución, el contenido es indefinido.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| signo                    |      | x    | x    | x     | x    | x     |



 

Esta instrucción funciona como se muestra a continuación.


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



SRC1 y src2 deben ser [registros temporales](dx9-graphics-reference-asm-vs-registers-temporary.md)diferentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




