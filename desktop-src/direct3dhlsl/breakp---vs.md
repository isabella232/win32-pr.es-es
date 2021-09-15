---
title: breakp- vs
description: Interrumpir condicionalmente el bucle actual en el punto de conexión más cercano (frente a o endrep) frente a usar uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574017"
---
# <a name="breakp---vs"></a>breakp- vs

Salga condicionalmente del bucle actual en el punto de conexión más cercano [( frente](endloop---vs.md) a o [endrep ) frente a](endrep---vs.md). Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.

## <a name="syntax"></a>Sintaxis



| breakp \[ ! \] p0. {x\|y\|z\|w} |
|-----------------------------|



 

Donde:

-   \[!\] booleano opcional NOT.
-   p0 es el registro de predicado. Vea [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} es la réplica necesaria en p0.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| breakp                 |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




