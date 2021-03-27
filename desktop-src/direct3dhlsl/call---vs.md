---
title: llamada-vs
description: Realiza una llamada de función a la instrucción marcada con la etiqueta proporcionada. | llamada-vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c797e7ef6745f5710752fe059d2a2ff1f94a8aa3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003742"
---
# <a name="call---vs"></a>llamada-vs

Realiza una llamada de función a la instrucción marcada con la etiqueta proporcionada.

## <a name="syntax"></a>Sintaxis



| llamar a l\# |
|----------|



 

donde l \# es una [etiqueta,](label---vs.md) que marca el principio de la subrutina a la que se va a llamar.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| llamada                   |      | x    | x    | x     | x    | x     |



 

Esta instrucción hace lo siguiente:

1.  Dirección de extracción de la instrucción siguiente a la pila de direcciones devuelta.
2.  Continúe con la ejecución de la instrucción marcada por la etiqueta.

En el sombreador de vértices 2 \_ 0, no se permiten las llamadas anidadas.

En el sombreador de vértices 2 \_ x, la profundidad de anidamiento está limitada por el elemento StaticFlowControlDepth de la estructura [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) . Para obtener más información, vea [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).

En el sombreador de vértices 3 \_ 0, se permiten cuatro niveles de anidamiento de llamadas.

Solo se permiten llamadas hacia delante. Esto significa que la ubicación de la etiqueta dentro del sombreador de vértices debe ser después de la instrucción de llamada que hace referencia a ella.

Si una instrucción de llamada se invoca dentro del [bucle](loop---vs.md)... bloque [ENDLOOP](endloop---vs.md) , el valor del [registro de contador de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) es accesible dentro de la subrutina.

Si una subrutina hace referencia al [registro de contador de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) ubicado fuera de la subrutina, cada instancia de la llamada a esta subrutina debe estar rodeada por un [bucle](loop---vs.md)... bloque [ENDLOOP](endloop---vs.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
