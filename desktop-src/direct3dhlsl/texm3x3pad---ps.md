---
title: texm3x3pad - ps
description: Realiza la multiplicación de la primera o la segunda fila de una matriz de tres filas multiplicada. Esta instrucción debe usarse en combinación con texasm3x3 - ps, texm3x3spec - ps, texm3x3vspec - ps o texm3x3tex - ps.
ms.assetid: 375526ee-cd58-4179-9b21-c63f17282f6b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10e473b30417d6797ffe227eff11b0d5d607264560bfd8506b76f333e0275cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787711"
---
# <a name="texm3x3pad---ps"></a>texm3x3pad - ps

Realiza la multiplicación de la primera o la segunda fila de una matriz de tres filas multiplicada. Esta instrucción debe usarse en combinación con [texm3x3 - ps](texm3x3---ps.md), [texm3x3spec - ps](texm3x3spec---ps.md), [texm3x3vspec - ps](texm3x3vspec---ps.md)o [texm3x3tex - ps](texm3x3tex---ps.md).

## <a name="syntax"></a>Syntax



| texm3x3pad dst, src |
|---------------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3pad            | x    | x    | x    |      |      |      |       |      |       |



 

Esta instrucción no se puede usar por sí misma.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




