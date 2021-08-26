---
title: 'breakp: ps'
description: 'Interrumpir condicionalmente el bucle actual en el punto de conexión más cercano: ps o endrep - ps. Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.'
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2da0d2bceea7a3e44f02e6b732337cb3447d6ef1c9798f95b664bf4da96ec2dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983325"
---
# <a name="breakp---ps"></a>breakp: ps

Salga condicionalmente del bucle actual en el [endloop más cercano: ps](endloop---ps.md) o [endrep - ps](endrep---ps.md). Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.

## <a name="syntax"></a>Syntax



| breakp \[ ! \] p0. {x\|y\|z\|w} |
|-----------------------------|



 

Donde:

-   \[!\] es un modificador negate opcional.
-   p0 es el [registro de predicado.](dx9-graphics-reference-asm-ps-registers-predicate.md)
-   {x \| y \| z \| w} es la réplica necesaria en p0.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| breakp                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




