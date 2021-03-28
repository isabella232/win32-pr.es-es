---
title: RET-PS
description: Toma la dirección de una instrucción de la pila de direcciones devuelta y continúa la ejecución de ella. En el caso de la función Main, esta instrucción detiene la ejecución del sombreador.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0535a4fcd66a1872b5eaa9ec97c292de710b48c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983834"
---
# <a name="ret---ps"></a>RET-PS

Toma la dirección de una instrucción de la pila de direcciones devuelta y continúa la ejecución de ella. En el caso de la función Main, esta instrucción detiene la ejecución del sombreador.

## <a name="syntax"></a>Sintaxis



| direcc |
|-----|



 

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| direcc                   |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrucción toma la dirección de una instrucción de la pila de direcciones devuelta y continúa la ejecución de ella. En el caso de la función Main, esta instrucción detiene la ejecución del sombreador.

La instrucción RET consume una ranura de instrucciones del sombreador de vértices.

Si un sombreador no contiene subrutinas, el uso de RET al final del programa principal es opcional.

No se permiten varias instrucciones Return en el programa principal o en cualquier subrutina, la primera instrucción return se trata como el final del programa o subrutina principal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




