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
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574024"
---
# <a name="breakp---ps"></a>breakp: ps

Interrumpir condicionalmente el bucle actual en el [endloop más cercano: ps](endloop---ps.md) o [endrep - ps](endrep---ps.md). Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.

## <a name="syntax"></a>Sintaxis



| breakp \[ ! \] p0. {x\|y\|z\|w} |
|-----------------------------|



 

Donde:

-   \[!\] es un modificador negate opcional.
-   p0 es el [registro de predicado.](dx9-graphics-reference-asm-ps-registers-predicate.md)
-   {x \| y \| z \| w} es la réplica necesaria en p0.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| breakp                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




