---
title: 'pow : ps'
description: 'Abs(src0)src1 de precisión completa. | pow : ps'
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eb108df22e1b0987a73253afcc2ce79b2af1aeff0a7d39a0aa3f57155d233b9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457225"
---
# <a name="pow---ps"></a>pow : ps

Abs(src0)<sup>src1</sup>de precisión completa.

## <a name="syntax"></a>Syntax



| pow dst, src0, src1 |
|---------------------|



 

where

-   dst es el registro de destino.
-   src0 es un registro de origen de entrada. El registro de origen requiere el uso explícito de replicar swzzle, es decir, debe especificarse exactamente uno de los componentes .x, .y, .z, .w swzzle (o .r, .g, .b, .a equivalentes).
-   src1 es un registro de origen de entrada. El registro de origen requiere el uso explícito de replicar swzzle, es decir, debe especificarse exactamente uno de los componentes .x, .y, .z, .w swzzle (o .r, .g, .b, .a equivalentes).

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| pow                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Esta instrucción funciona de la siguiente manera:

dest.x = dest.y = dest.z = dest.w = \[ abs(src0) \] <sup>src1</sup>;

Se trata de una instrucción escalar, por lo que los registros de origen deben tener swlinos de replicación para indicar qué canales se usan.

La potencia de entrada (src1) debe ser escalar.

El resultado escalar se replica en los cuatro canales de salida.

Esta instrucción se podría expandir como exp(src1 \* log(src0)).

El registro dst debe ser un registro temporal y no debe ser el mismo registro que src1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




