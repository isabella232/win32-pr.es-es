---
title: dsy - ps
description: Calcule la velocidad de cambio en la dirección Y del destino de representación.
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 735b0d3ae75abe76e5075b3d22612ad0d56c7a21bab74f29010f47b54d161324
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950545"
---
# <a name="dsy---ps"></a>dsy - ps

Calcule la velocidad de cambio en la dirección Y del destino de representación.

## <a name="syntax"></a>Syntax



| dsy dst, src |
|--------------|



 

Donde:

-   dst es un registro de destino.
-   src es un registro de origen de entrada.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dsy                   |      |      |      |      |      | x    | x     | x    | x     |



 

La tasa de cambio calculada desde el registro de origen es una aproximación al contenido del mismo registro en píxeles adyacentes que ejecutan el sombreador de píxeles en el paso de bloqueo con el píxel actual.

Las [instrucciones dsx](dsx---ps.md) And dsy calculan su resultado observando el contenido actual del registro de origen (por componente) para los distintos píxeles del área local que se ejecuta en el paso de bloqueo. La fórmula exacta usada para calcular el degradado varía en función del hardware, pero debe ser coherente con la forma en que el hardware realiza las mismas operaciones como parte del proceso de cálculo de nivel de detalle para el muestreo de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[ldd- ps](texldd---ps.md)
</dt> </dl>

 

 




