---
title: ret - vs
description: Devuelve desde una subrutina o una función principal.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bec0356f2f1542da421a807598707e4857033c13cda2077d9281ac24e4fc3e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853775"
---
# <a name="ret---vs"></a>ret - vs

Devuelve desde una subrutina o una función principal.

## <a name="syntax"></a>Syntax



| Ret |
|-----|



 

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Ret                    |      | x    | x    | x     | x    | x     |



 

Esta instrucción toma la dirección de una instrucción de la pila de direcciones de devolución y continúa la ejecución desde ella. En el caso de la función main, esta instrucción detiene la ejecución del sombreador.

La instrucción ret consume un espacio de instrucciones del sombreador de vértices.

Si un sombreador no contiene subrutinas, el uso de ret al final del programa principal es opcional.

No se permiten varias instrucciones return en el programa principal o en ninguna subrutina, la primera instrucción return se trata como el final del programa principal o la subrutina.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




