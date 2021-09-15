---
title: label - vs
description: Marque la siguiente instrucción como que tiene un índice de etiqueta. | label - vs
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e2b72fe21301aa66d8428dc3696ceb3f12e6214
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567760"
---
# <a name="label---vs"></a>label - vs

Marque la siguiente instrucción como que tiene un índice de etiqueta.

## <a name="syntax"></a>Sintaxis



| etiqueta l\# |
|-----------|



 

donde \# identifica el número de etiqueta.

Para vs 2 0 y vs 2 x, el número de etiqueta debe estar entre \_ \_ \_ \_ 0 y 15.

Para vs 2 sw, vs 3 0 y vs 3 sw, el número de etiqueta debe estar entre \_ \_ \_ \_ \_ \_ 0 y 2047.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| etiqueta                  |      | x    | x    | x     | x    | x     |



 

Esta instrucción define una etiqueta que se encuentra en la siguiente instrucción del sombreador. La instrucción de etiqueta solo puede estar presente directamente después de una [instrucción ret](ret---vs.md) (que define el final de la subrutina anterior o el programa principal).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




