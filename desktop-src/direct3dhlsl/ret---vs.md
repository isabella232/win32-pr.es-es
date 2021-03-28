---
title: RET-vs
description: Se devuelve de una subrutina o de una función principal.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b91a9f2fb30dbd243e29043a1655d441215bc75
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358477"
---
# <a name="ret---vs"></a>RET-vs

Se devuelve de una subrutina o de una función principal.

## <a name="syntax"></a>Sintaxis



| direcc |
|-----|



 

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| direcc                    |      | x    | x    | x     | x    | x     |



 

Esta instrucción toma la dirección de una instrucción de la pila de direcciones devuelta y continúa la ejecución de ella. En el caso de la función Main, esta instrucción detiene la ejecución del sombreador.

La instrucción RET consume una ranura de instrucciones del sombreador de vértices.

Si un sombreador no contiene subrutinas, el uso de RET al final del programa principal es opcional.

No se permiten varias instrucciones Return en el programa principal o en cualquier subrutina, la primera instrucción return se trata como el final del programa o subrutina principal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




