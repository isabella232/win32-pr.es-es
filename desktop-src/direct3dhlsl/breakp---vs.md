---
title: breakp-vs
description: Divida condicionalmente el bucle actual en el ENDLOOP-vs o endrep-vs más cercano. Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077094"
---
# <a name="breakp---vs"></a>breakp-vs

Divida condicionalmente el bucle actual en el [ENDLOOP-vs](endloop---vs.md) o [endrep-vs](endrep---vs.md)más cercano. Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.

## <a name="syntax"></a>Sintaxis



| breakp \[ ! \] P0. x1|sí|z|con |
|-----------------------------|



 

Donde:

-   \[!\] booleano opcional no.
-   P0 es el registro del predicado. Vea [registro de predicados](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} es el swizzle de replicación necesario en P0.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| breakp                 |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




