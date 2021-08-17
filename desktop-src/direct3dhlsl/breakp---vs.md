---
title: 'breakp: vs'
description: Interrumpir condicionalmente el bucle actual en el endloop más cercano (frente a o endrep) frente a Usar uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a768acaecaa77a42990b34c50cd8eccb24d61353550751f3ed830e7844d7624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794319"
---
# <a name="breakp---vs"></a>breakp: vs

Interrumpir condicionalmente el bucle actual en el [endloop más](endloop---vs.md) cercano ( frente a [o endrep ) frente a](endrep---vs.md). Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.

## <a name="syntax"></a>Syntax



| breakp \[ ! \] p0. {x\|y\|z\|w} |
|-----------------------------|



 

Donde:

-   \[!\] booleano opcional NOT.
-   p0 es el registro de predicado. Vea [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} es el swzzle de replicación necesario en p0.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| breakp                 |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




