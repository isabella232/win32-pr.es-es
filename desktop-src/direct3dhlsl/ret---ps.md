---
title: ret - ps
description: Toma la dirección de una instrucción de la pila de direcciones de devolución y continúa la ejecución desde ella. En el caso de la función main, esta instrucción detiene la ejecución del sombreador.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b77d2bb63655a83716d74621a5ece097259b0a90461f902801c375a079f118f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853785"
---
# <a name="ret---ps"></a>ret - ps

Toma la dirección de una instrucción de la pila de direcciones de devolución y continúa la ejecución desde ella. En el caso de la función main, esta instrucción detiene la ejecución del sombreador.

## <a name="syntax"></a>Syntax



| Ret |
|-----|



 

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Ret                   |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrucción toma la dirección de una instrucción de la pila de direcciones de devolución y continúa la ejecución desde ella. En el caso de la función main, esta instrucción detiene la ejecución del sombreador.

La instrucción ret consume un espacio de instrucciones del sombreador de vértices.

Si un sombreador no contiene subrutinas, el uso de ret al final del programa principal es opcional.

No se permiten varias instrucciones return en el programa principal o en ninguna subrutina, la primera instrucción return se trata como el final del programa principal o la subrutina.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




