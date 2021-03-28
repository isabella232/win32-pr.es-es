---
title: breakp-PS
description: Divida condicionalmente el bucle actual en el ENDLOOP-PS o endrep-PS más cercano. Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419944"
---
# <a name="breakp---ps"></a>breakp-PS

Divida condicionalmente el bucle actual en el [ENDLOOP-PS](endloop---ps.md) o [endrep-PS](endrep---ps.md)más cercano. Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.

## <a name="syntax"></a>Sintaxis



| breakp \[ ! \] P0. x1|sí|z|con |
|-----------------------------|



 

Donde:

-   \[!\] es un modificador opcional Negate.
-   P0 es el [registro del predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} es el swizzle de replicación necesario en P0.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| breakp                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




