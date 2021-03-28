---
title: etiqueta-frente
description: Marque la instrucción siguiente como un índice de etiqueta. | etiqueta-frente
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e2b72fe21301aa66d8428dc3696ceb3f12e6214
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998238"
---
# <a name="label---vs"></a>etiqueta-frente

Marque la instrucción siguiente como un índice de etiqueta.

## <a name="syntax"></a>Sintaxis



| etiqueta l\# |
|-----------|



 

donde \# identifica el número de etiqueta.

Para vs \_ 2 \_ 0 y vs \_ 2 \_ x, el número de etiqueta debe estar entre 0 y 15.

En vs \_ 2 \_ SW, vs \_ 3 \_ 0 y vs \_ 3 \_ SW, el número de etiqueta debe estar entre 0 y 2047.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| etiqueta                  |      | x    | x    | x     | x    | x     |



 

Esta instrucción define una etiqueta que se encuentra en la siguiente instrucción del sombreador. La instrucción de etiqueta solo puede estar presente directamente después de una instrucción [RET](ret---vs.md) (que define el final de la subrutina o el programa principal anterior).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




