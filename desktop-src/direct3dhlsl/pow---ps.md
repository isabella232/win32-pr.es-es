---
title: Pow-PS
description: SRC1 de precisión completa ABS (src0). | Pow-PS
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986295"
---
# <a name="pow---ps"></a>Pow-PS

<sup>SRC1</sup>de precisión completa ABS (src0).

## <a name="syntax"></a>Sintaxis



| Pow DST, src0, SRC1 |
|---------------------|



 

, donde

-   DST es el registro de destino.
-   src0 es un registro de origen de entrada. El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).
-   SRC1 es un registro de origen de entrada. El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| pow                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Esta instrucción funciona de la siguiente manera:

dest. x = dest. y = dest. z = dest. w = \[ ABS (src0) \] <sup>SRC1</sup>;

Se trata de una instrucción escalar, por lo que los registros de origen deben tener replicar swizzles para indicar qué canales se usan.

La potencia de entrada (SRC1) debe ser un escalar.

El resultado escalar se replica en los cuatro canales de salida.

Esta instrucción se puede expandir como exp (SRC1 \* log (src0)).

El registro de DST debe ser un registro temporal y no debe ser el mismo registro que SRC1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




