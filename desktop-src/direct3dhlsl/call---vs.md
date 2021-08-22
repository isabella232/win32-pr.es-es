---
title: call - vs
description: Realiza una llamada de función a la instrucción marcada con la etiqueta proporcionada. | call - vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2321224b10ca1f7822b19e48ebbb58c1e01c261720f64a8b39331fbceab75fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986895"
---
# <a name="call---vs"></a>call - vs

Realiza una llamada de función a la instrucción marcada con la etiqueta proporcionada.

## <a name="syntax"></a>Syntax



| llamar a l\# |
|----------|



 

donde l es una etiqueta, frente a marcar el principio de la subrutina a la \# que se va a llamar. [](label---vs.md)

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| llamada                   |      | x    | x    | x     | x    | x     |



 

Esta instrucción hace lo siguiente:

1.  Dirección de inserción de la siguiente instrucción en la pila de direcciones de retorno.
2.  Continúe la ejecución desde la instrucción marcada por la etiqueta .

En el sombreador de vértices 2 0, no se permiten llamadas \_ de anidamiento.

En el sombreador de vértices 2 x, la profundidad de anidamiento está limitada por el elemento StaticFlowControlDepth de la estructura \_ [**D3DVSHADERCAPS2 \_ 0.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) Para obtener más información, [**vea GetDeviceCaps.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps)

En el sombreador de \_ vértices 3 0, se permiten cuatro niveles de anidamiento de llamadas.

Solo se permiten llamadas de reenvío. Esto significa que la ubicación de la etiqueta dentro del sombreador de vértices debe estar después de la instrucción de llamada que hace referencia a ella.

Si se invoca una instrucción de llamada dentro del [bucle](loop---vs.md)... [bloque endloop,](endloop---vs.md) el valor del registro de [contador](dx9-graphics-reference-asm-vs-registers-loop-counter.md) de bucles (aL) es accesible dentro de la subrutina.

Si una subrutina hace referencia al registro de contador de [bucles](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) situado fuera de la subrutina, cada instancia de la llamada a esta subrutina debe estar rodeado por un [bucle](loop---vs.md)... [bloque endloop.](endloop---vs.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
